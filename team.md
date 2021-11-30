---
layout: default
title: Our Team
---
<div>
  <h2>{{ page.title }}</h2>
  <ul>
  {% for member in site.members %}
    <li>
      <h2>{{ member.name }}</h2>
      <h3>{{ member.role }}</h3>
      <p>{{ member.content | markdownify }}</p>
    </li>
  {% endfor %}
</ul>
</div>
