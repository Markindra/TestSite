---
layout: default
title: Our Team
---
<div class="row">
  <h1 class="text-center mx-auto pt-3">{{ page.title }}</h1>
</div>

<!-- Team Member Horizontal Cards -->
{% assign sortedMembers = site.members | sort: 'index' %}
<div class="row mx-0 mb-5">
  {% for member in sortedMembers %}
  <div class="col-lg-6">
    <div class="card mb-3 team-card">
      <div class="row no-gutters">
        <div class="col-4">
          <img src="{{ site.baseurl }}{{ member.imageURL }}" class="card-img mh-50 pl-3 pt-4" alt="{{ member.imageAlt }}">
        </div>
        <div class="col-8">
          <div class="card-body">
            <h5 class="card-title">{{ member.name | upcase }}<br>
              <small class="text-muted">
              {{ member.role }}</small></h5>
            <p class="card-text">{{ member.content | markdownify }}</p>
          </div>
        </div>
      </div>
    </div>
  </div>
  {% endfor %}
</div>
