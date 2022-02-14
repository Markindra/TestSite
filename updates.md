---
layout: default
title: Updates
---
<!-- Feature Post -->
<section class="post-feature position-relative d-flex flex-column justify-content-center align-content-bottom mb-5">
  {% for item in site.posts limit:1 %}
  <a href="{{ site.baseurl }}{{ item.url }}" class="text-dark py-2 px-3">
    <div class="project-feature-scrim position-absolute">
    </div>
  </a>
  {% endfor %}
  <div class="w-100 row position-absolute post-feature-title">
    <div class="mw-50 mx-auto text-center">
      {% for item in site.posts limit:1 %}

        <h1 class="display-4"><a href="{{ site.baseurl }}{{ item.url }}" class="text-dark py-2 px-3">{{ item.title | upcase }}</a></h1>
        <h2>{{ item.subtitle }}</h2>

      {% endfor %}
    </div>
  </div>
</section>

<section class="container">
  <div class="row">
    {% for item in site.posts limit:10 %}
      {% if forloop.index == 1 %}
      {% else %}
        <div class="col-12 col-md-4">
          <div class="card m-3 film-cards">
            <a class="text-dark" href="{{ site.baseurl }}{{ item.url }}">
              <img class="img-fluid" src="{{ site.baseurl }}{{ item.featureImage }}">
              <div class="card-body">
                <h5 class="card-title">{{ item.title }}</h5>
                <p class="card-text">{{ item.excerpt | strip_html | truncatewords: 25 }}</p>
              </div>
            </a>
          </div>
        </div>
    {% endif %}
    {% endfor %}
  </div>
</section>
