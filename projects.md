---
layout: default
title: Projects
---
<!-- Sign Up -->
<section class="project-feature position-relative d-flex flex-column justify-content-center text-white">
  <div class="project-feature-scrim position-absolute">
  </div>
  <div class="container position-relative">
    <div class="row">
      <div class="mw-50 ml-5 mt-0 d-lg-none project-feature-text">
        <h1>BE THE<br>FIRST<br>TO KNOW</h1>
        <h3 class="text-muted">Get new<br>project releases<br>in your inbox</h3>
        <div class="mt-4 mb-3">
          <a href="#" class="btn btn-primary py-2 px-3">
            Sign Up Now
          </a>
        </div>
      </div>
      <div class="mx-auto py-3 min-vw-50 px-5 d-none d-lg-block project-feature-text">
        <h1 class="display-2">BE THE<br>FIRST<br>TO KNOW</h1>
        <h5 class="display-4 text-muted">Get new<br>project releases<br>in your inbox</h5>
        <div class="mt-3 mb-3">
          <a href="#" class="btn btn-primary py-2 px-3">
            Sign Up Now
          </a>
        </div>
      </div>
    </div>
  </div>
</section>

<!-- Films -->
<section class="container-fluid film-projects">
  <div class="container">
    <div class="row mt-5 mb-3 latest-film">
      {% assign sortedFilms = site.films | sort: 'year' | reverse %}
      {% for item in sortedFilms limit:1 %}
      <div class="col-12 mb-5 align-content-center">
        <h2 class="text-center text-uppercase font-weight-lighter mb-0">Latest Film<br>
        <i class="bi bi-chevron-double-down"></i></h2>
      </div>
      <div class="col-12 col-lg-6 d-flex align-content-center">
        <div class="embed-responsive embed-responsive-16by9">
          <iframe class="embed-responsive-item" src="{{ item.trailer }}?modestbranding=1"  title="Courageous Legacy Trailer" allow="autoplay;" allowfullscreen></iframe>
        </div>
      </div>
      <div class="col-12 col-lg-6">

        <a class="text-dark" href="{{ site.baseurl }}{{ item.url }}"><h2 class="text-center">{{ item.title }}</h2></a>
        <p class="text-center">Released {{ item.year | date: "%Y" }}</p>
        <p>{{ item.excerpt }}</p>
        <p><a href="{{ site.baseurl }}{{ item.url }}">How to watch
          <i class="bi bi-chevron-right"></i></a></p>
        <!-- <div class="w-100 text-center">
          <a href="{{ site.baseurl }}/{{ allfilms.html }}"><h5>See all film projects</h5></a>
        </div> -->
      </div>
      {% endfor %}
    </div>

    <hr class="mx-5">

    <div class="row my-3">
      <div class="col-12">
        <h4 class="text-center">Other Films</h4>
      </div>
    </div>
    <div class="row">
      {% for item in sortedFilms limit:5 %}
        {% if forloop.index == 1 %}
        {% else %}
          <div class="col-6 mb-3">
            <div class="card h-100 film-cards">
              <img class="img-card-top px-lg-5" src="{{ site.baseurl }}{{ item.packshot }}">
              <div class="card-body px-0 px-lg-5 pb-0">
                <h5 class="d-none card-title font-weight-light">{{ item.title }}</h5>
                <p class="card-text">{{ item.excerpt | strip_html | truncatewords:25 }}</p>
              </div>
              <div class="card-footer film-cards pt-0 px-0 px-lg-5">
                <p><a href="{{ site.baseurl }}{{ item.url }}">More<i class="bi bi-chevron-right"></i></a></p>
              </div>
            </div>
          </div>
        {% endif %}
      {% endfor %}
    </div>



</div>
<!--
<div class="row mt-5">
  <div class="col-12">
    <a href="#">
      <img class="img-fluid" src="{{ site.baseurl }}/assets/images/premiums/AllFilmsBanner.jpg">
        <div class="banner-block">
          <h2 class="text-center d-md-none">See all films</h2>
          <h1 class="display-2 d-none d-md-block text-center">See all films</h1>
        </div>
    </a>
  </div>
</div>
-->

</section>



<!-- Books -->
<section class="container-fluid book-projects bg-white py-1 mb-3">
  <div class="row mt-3 mb-3">
    <div class="col-12">
      <h2 class="text-center text-uppercase font-weight-lighter mt-3 mb-0">Books</h2>
    </div>
  </div>
    <div class="row mb-3 justify-content-center">
      {% assign sortedBooks = site.books | where: "type", "anchor" | sort: 'published' | reverse %}
      {% for item in sortedBooks %}
      <div class="col-12 col-md-6 col-xl-4">
        <div class="card my-3 border-0 card-shadow">
          <div class="row">
            <div class="col-4 align-content-center">
              <img class="ml-3 mt-3 img-fluid rounded" src="{{ site.baseurl }}{{ item.coverImage }}">
            </div>
            <div class="col-8">
              <div class="card-body">
                <a class="text-dark" href="{{ site.baseurl }}{{ item.url }}">
                  <h5 class="text-center card-title">{{ item.title }}</h5>
                </a>
                <p class="text-center">Published on {{ item.published | date: "%b %d, %Y"}}</p>
                <p class="card-text">{{ item.excerpt | strip_html | truncatewords:25 }}</p>
              </div>
            </div>
          </div>
          <div class="card-footer bg-white border-0">
            <p class="text-right"><a href="{{ site.baseurl }}{{ item.url }}">Read more
              <i class="bi bi-chevron-right"></i></a></p>
          </div>
        </div>
      </div>
      {% endfor %}
    </div>

<!--
<div class="row mt-5">
  <div class="col-12">
    <a href="#">
      <img class="img-fluid" src="{{ site.baseurl }}/assets/images/premiums/AllBooksBanner.jpg">
        <div class="banner-block">
          <h2 class="text-center d-md-none">See all books</h2>
          <h1 class="display-2 d-none d-md-block text-center">See all books</h1>
        </div>
    </a>
  </div>
</div>
-->


</section>
