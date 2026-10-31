---
layout: default
title: Home
---

# Welcome

Your latest posts will appear here.

{% for post in site.posts limit:10 %}
  <article>
    <h2><a href="{{ post.url | relative_url }}">{{ post.title }}</a></h2>
    <p>
      <time datetime="{{ post.date | date_to_xmlschema }}">
        {{ post.date | date: "%Y-%m-%d" }}
      </time>
    </p>
    {% if post.description %}<p>{{ post.description }}</p>{% endif %}
    {% if post.tags.size > 0 %}
      <p>
        {% for tag in post.tags %}
          <a href="{{ '/tags/' | relative_url }}#{{ tag | slugify }}">{{ tag }}</a>{% unless forloop.last %}, {% endunless %}
        {% endfor %}
      </p>
    {% endif %}
  </article>
{% endfor %}
