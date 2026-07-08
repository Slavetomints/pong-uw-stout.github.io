---
layout: default
title: LANs
permalink: /lans/
order: 4
---

# LANs
<hr>
<ul class="post-list">
  {% for lan in site.lans %}
    <li class="post-item">
      <h2>
        <a href="{{ lan.url | relative_url }}">{{ lan.title }}</a>
      </h2>
      <time datetime="{{ lan.start_date | date_to_xmlschema }}">
        {{ lan.start_date | date: "%B %d, %Y" }} - {{ lan.end_date | date: "%B %d, %Y" }}
      </time>
      {% if lan.description %}
        <p>{{ lan.description | strip_html }}</p>
      {% endif %}
    </li>
  {% endfor %}
</ul>