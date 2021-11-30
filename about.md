---
layout: default
title: About
---
<h1>Our Values</h1>
<ul>
  {% for item in site.data.values %}
  <li>{{ item.name }} - {{ item.description }}
    {% if item.moreURL %}<a href="{{item.moreURL}}">{{ item.moreText }}</a>

    {% endif %}
  </li>
  {% endfor %}
</ul>
