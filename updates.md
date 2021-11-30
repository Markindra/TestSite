---
layout: default
title: Updates
---
<div class="featureContainer">
  {% for post in site.posts limit:1 %}
  <img src="{{ post.featureImage }}" alt="{{ post.imageAlt }}" class="featureImage">
  <div class="featureTitle"><a href="{{ post.url }}">{{ post.title | upcase }}</a></div>
</div>
<div>{{ post.excerpt }}</div>
{% endfor %}

<hr>
<ul>
{% for post in site.posts offset:1 limit:4 %}
  <li>
    <h2><a href="{{ post.url }}">{{ post.title }}</a></h2>
    {{ post.excerpt }}
  </li>
{% endfor %}
</ul>
