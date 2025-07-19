---
layout: page
title: "Math"
category: math
permalink: /categories/math/
---

{% assign category_name = page.category | default: "math" %}
{% assign posts = site.categories[category_name] | default: empty %}
{% if posts %}
<ul>
  {% for post in posts %}
    <li>
      <a href="{{ post.url | relative_url }}">{{ post.title }}</a> ({{ post.date | date: "%Y-%m-%d" }})
    </li>
  {% endfor %}
</ul>
{% else %}
<p>No posts found in this category.</p>
{% endif %}