---
layout: default
title: Updates
---
<!-- Feature Article -->
<div class="row mx-0 mb-3 bg-white">
    {% for post in site.posts limit:1 %}
    <img class="img-fluid" src="{{ site.baseurl }}{{ post.featureImage }}" alt="{{ post.imageAlt }}">
    <div class="p-3">
      <h1 class="featureTitle mt-3">{{ post.title | upcase }}<br>
        {% if post.subtitle %}
        <small class="text-muted">{{ post.subtitle | upcase }}</small>
        {% endif %}
      </h1>
      <div class="lead text-justify">
      <p>{{ post.excerpt }}</p>
      </div>
      <a href="{{ site.baseurl }}{{ post.url }}" class="card-link"><button class="btn btn-primary m-3">Read More</button></a>
      {% endfor %}
    </div>
</div>

<!-- Latest Blog Articles -->

<div class="row mb-5">
    <div class="card-group">
  {% for post in site.posts offset:1 limit:4 %}

      <div class="card mx-3 px-3 pt-3 pb-0 article-box">
        <img src="{{ site.baseurl }}{{ post.featureImage }}" class="card-img-top" alt="{{ post.imageAlt }}">
        <div class="card-body">
          <h5 class="card-title">{{ post.title }}</h5>
          <p class="card-text">{{ post.brief }}</p>
          <a href="{{ site.baseurl }}{{ post.url }}" class="card-link">More</a>
        </div>
      </div>
      {% endfor %}

  </div>
</div>
