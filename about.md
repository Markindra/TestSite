---
layout: default
title: Our Values
---
<!-- Mission Statement Header -->
<div class="row mx-0 pt-3 value-top">
  <div class="w-75 mx-auto">
    {% for article in site.articles %}
    {% if article.name == "Mission Statement" %}
    <h5 class="text-center text-white">{{ content }}</h5>
    {% endif %}
    {% endfor %}
  </div>
</div>

<!-- Value Cards -->
<div class="row mx-0 pt-3 pb-0 bg-white">
  <h3 class="text-center text-bold w-100">{{ page.title | upcase }}</h3>
</div>
<div class="row mx-0 mb-3 min-vh-50 bg-white">
  {% for item in site.data.values %}
    <div class="col-lg-6">
      <div class="card value-card my-3">
        <img class="card-img" src="{{ item.imageURL }}" alt="{{ item.imageAlt }}">
          <div class="card-img-overlay text-white d-flex text-left align-items-end">
            <div>
              <h2>{{ item.name | upcase }}</h2>
                <div class="valueBox w-75 px-3 py-1">
                  <h4>{{ item.description }}</h4>
                  {% if item.moreText %}
                  <p><a class="text-white" href="{{ item.moreURL }}">{{ item.moreText }}</a></p>
                  {% endif %}
                </div>
            </div>
          </div>
      </div>
    </div>
  {% endfor %}
</div>
