---
layout: default
title: Archive
permalink: /archive/
---

# Archive

{% assign posts_by_month = site.posts | group_by_exp: "post", "post.date | date: '%Y-%m'" | sort: "name" | reverse %}
{% for month in posts_by_month %}
  {% assign month_date = month.name | append: "-01" %}
  <h2>{{ month_date | date: "%B %Y" }}</h2>
  <ul>
    {% for post in month.items %}
      <li>
        <time datetime="{{ post.date | date_to_xmlschema }}">{{ post.date | date: "%Y-%m-%d" }}</time>
        — <a href="{{ post.url | relative_url }}">{{ post.title }}</a>
      </li>
    {% endfor %}
  </ul>
{% endfor %}
