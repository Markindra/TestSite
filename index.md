---
layout: homepage
title: Home
---
<div class="jumbotron jumbotron-fluid indextron">
  <div class="container text-center">
    {% for item in site.data.homepage %}
    <h1 class="mission">{{ item.line | upcase }}</h1>
    <a href="{{ site.baseurl }}{{ item.buttonLink }}"><button class="btn btn-primary indexButton">{{ item.button }}</button></a>
    {% endfor %}
  </div>
</div>
