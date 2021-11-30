---
layout: default
title: Projects
---
<h1>{{ page.title }}</h1>

<div>
  <h2>Films</h2>
  <ul>
  {% assign sortedFilms = site.films | sort: 'year' | reverse %}
  {% for film in sortedFilms %}
    <li>
      <h3><a href="{{ film.url }}">{{ film.name }}</a></h3>
      <!--<h3>{{ film.year | date_to_string }}</h3>-->
      <img style="width:200px;" src="{{ film.packshot }}">
      <!--<p>{{ film.excerpt | markdownify }}</p>-->
    </li>
  {% endfor %}
  </ul>
</div>
<div>
  <h2>Books</h2>
  <ul>
    {% assign sortedBooks = site.books | sort: 'published' | reverse %}
    {% for book in sortedBooks %}
    <li>
      <h3><a href="{{ book.url }}">{{ book.title }}</a></h3>
      <img style="width:120px;" src="{{ book.coverImage }}">
    </li>
    {% endfor %}
  </ul>
</div>

<div>
  <h2>Bible Studies</h2>
  <ul>
    {% for studie in site.studies %}
    <li>
      <h3><a href="{{ studie.url }}">{{ studie.title }}</a></h3>
      <img style="height:200px;" src="{{ studie.coverImage }}">
    </li>
    {% endfor %}
  </ul>
</div>
