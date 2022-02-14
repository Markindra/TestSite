---
layout: default
title: Projects
---
<!-- Featured Projects -->
<section class="project-feature position-relative d-flex flex-column justify-content-center text-white">
  <div class="project-feature-scrim position-absolute">
  </div>

</section>




<!-- <section class="feature-projects position-relative d-flex flex-column justify-content-center px-0 mb-5">
  <div class="feature-projects-scrim position-absolute">
    <div class="container position-relative">
        <div class="row">
            <div class="col-md-6 offset-md-3 offset-lg-0 col-lg-9">
                <h1 class="shadow-sm">Easy to Read<br>Call to Action</h1>
                <div class="mt-4 mb-3">
                    <a href="#" class="btn btn-primary py-2 px-3">
                        Join Now
                    </a>
                </div>

            </div>
        </div>
    </div>
  </div>
-->
<!--  <div id="carouselControls" class="carousel slide" data-ride="carousel">
    <div class="carousel-inner">
      {% for item in site.data.banners %}
        {% if forloop.first == true %}
          <div class="carousel-item active">
            <img src="{{ site.baseurl }}{{ item.banner_image }}" class="d-block w-100">
          </div>
          {% else %}
          <div class="carousel-item">
            <img src="{{ site.baseurl }}{{ item.banner_image }}" class="d-block w-100">
          </div>
        {% endif %}
      {% endfor %}
    </div>
    <a class="carousel-control-prev" href="#carouselControls" role="button" data-slide="prev">
      <span class="carousel-control-prev-icon" aria-hidden="true"></span>
      <span class="sr-only">Previous</span>
    </a>
    <a class="carousel-control-next" href="#carouselControls" role="button" data-slide="next">
      <span class="carousel-control-next-icon" aria-hidden="true"></span>
      <span class="sr-only">Next</span>
    </a>
  </div>
-->



<!-- Films -->
<section>
  <div class="row mx-0 mt-0 bg-white">
    <div class="col pt-3">
      <h2 class="text-center font-weight-bold">Films</h2>
    </div>
  </div>
  <div class="row mx-0 bg-white mb-5 px-3 pb-3">
    <div class="scrolling-wrapper d-flex">
      {% assign sortedFilms = site.films | sort: 'year' | reverse %}
      {% for film in sortedFilms %}
      <div class="card scrolling-card w-75 pt-0 px-0 m-3 border-light">
        <a href="{{ site.baseurl }}{{ film.url }}">
          <div class="film-button">
            <img class="card-img-top scrolling-thumbnail" src="{{ site.baseurl }}{{ film.packshot }}">
          </div>
        </a>
        <!-- <div class="card-body text-center">
          <h3><a href="{{ site.baseurl }}{{ film.url }}">{{ film.title }}</a></h3>
          <p>Released {{ film.year | date: "%Y" }}</p>
        </div> -->
      </div>
      {% endfor %}
    </div>
  </div>
</section>

<!-- Books -->
<div class="row mt-3 mx-0 py-3 bg-white">
  <div class="col">
    <h2 class="text-center font-weight-bold">Books</h2>
  </div>
</div>
<div class="row mx-0 bg-white px-3 pb-3 mb-5">
  <div class="scrolling-wrapper d-flex">
    {% assign sortedBooks = site.books | sort: 'published' | reverse %}
    {% for book in sortedBooks %}
    <div class="col-5 col-md-3 col-xl-2 card text-center scrolling-card mx-3 mb-3 border-light">
      <img class="card-img-top" src="{{ site.baseurl }}{{ book.coverImage }}">
      <div class="card-body px-0">
        <p class="card-title"><a class="stretched-link" href="{{ site.baseurl }}{{ book.url }}">{{ book.title }}</a></p>
      </div>
    </div>
    {% endfor %}
  </div>
</div>

<!-- Horizontal scroll of Bible Studies -->
<div class="row mx-0 mt-3 py-3 bg-white">
  <div class="col">
    <h2 class="text-center font-weight-bold">Bible Studies</h2>
  </div>
</div>
<div class="row mx-0 bg-white px-3 pb-3 mb-5">
  <div class="scrolling-wrapper d-flex">
    {% for studie in site.studies %}
    <div class="col-5 col-md-3 col-xl-2 card text-center scrolling-card mx-3 mb-3 border-light">
      <img class="card-img-top" src="{{ site.baseurl }}{{ studie.coverImage }}">
      <div class="card-body px-0">
        <p class="card-title"><a class="stretched-link" href="{{ site.baseurl }}{{ studie.url }}">{{ studie.title }}</a></p>
      </div>
    </div>
    {% endfor %}
  </div>
</div>
