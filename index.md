---
layout: homepage
title: Home
---
<div class="jumbotron jumbotron-fluid indextron">
  <div class="container text-center">
    {% for item in site.data.homepage %}
    <h4 class="d-block d-md-none mission">{{ item.line | upcase }}</h4>
    <h2 class="d-none d-md-block mission">{{ item.line | upcase }}</h2>
    <a href="{{ site.baseurl }}{{ item.buttonLink }}"><button class="btn btn-primary indexButton">{{ item.button }}</button></a>
    {% endfor %}
  </div>
</div>
