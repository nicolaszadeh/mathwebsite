---
layout: page
title: "Kinetic"
tag: kinetic
permalink: /tags/kinetic/
---
{% assign posts = site.tags[page.tag] %}
<ul>
  {% for post in posts %}
    <li>
      <a href="{{ post.url | relative_url }}">{{ post.title }}</a> ({{ post.date | date: "%Y-%m-%d" }})
    </li>
  {% endfor %}
</ul>