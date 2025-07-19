---
layout: page
title: "Categories"
permalink: /categories/
---

<ul>
{% assign categories = site.categories | sort %}
{% for category in categories %}
  {% assign category_name = category[0] %}
  <li>
    <a href="{{ '/categories/' | append: category_name | append: '/' | relative_url }}">{{ category_name }}</a>
    ({{ category[1].size }})
  </li>
{% endfor %}
</ul>