---
layout: default
title: Taggar
permalink: /tags/
---

# Tags

{% assign all_tags = site.tags | sort %}
{% for tag in all_tags %}
  <h2 id="{{ tag[0] | slugify }}">{{ tag[0] }}</h2>
  <ul>
    {% assign tagged_posts = tag[1] | sort: "date" | reverse %}
    {% for post in tagged_posts %}
      <li>
        <time datetime="{{ post.date | date_to_xmlschema }}">{{ post.date | date: "%Y-%m-%d" }}</time>
        — <a href="{{ post.url | relative_url }}">{{ post.title }}</a>
      </li>
    {% endfor %}
  </ul>
{% endfor %}
