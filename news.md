---
layout: default
title: "News"
description: "Change log and other updates"
---

<section class="blog-list-section py-5">
  <div class="container">
    <h1 class="page-headline text-center mb-5">News</h1>
    <div class="row">
      {% for post in site.posts limit:9 %}
      <div class="col-12 col-lg-4 mb-5">
        <div class="post-item shadow">
          <a class="post-link" href="{{ post.url | prepend: site.baseurl }}">
            <div class="post-thumb-holder">
              <img class="img-fluid" src="/assets//blog/{{ post.image }}" alt="">
            </div><!--//post-thumb-holder-->
            <div class="post-content-holder p-4">
              <div class="post-type mb-2">
                <span class="font-weight-bold text-primary">
                  {{ post.category }}
                </span>
              </div><!--//post-type-->
              <h4 class="post-title">{{ post.title }}</h4>
              <div class="post-excerpt mb-3">
                {{ post.content | strip_html | truncatewords:32 }}
              </div><!--//post-excerpt-->
              <div class="post-author">
                <div class="row">
                  <div class="col-12 col-lg-3">
                    <div class="profile mb-3">
                      <img class="profile-image img-fluid" src="/assets/team/{{ post.author.image }}" alt=""></div>
                  </div><!--col-12-->
                  <div class="col-12 col-lg-9 pt-1">
                    <div class="name font-weight-bold">{{ post.author.display_name }}</div>
                    <div class="meta">{{ post.author.role }}</div>
                    <div>{{ post.date | date: "%B %-d, %Y" }}</div>
                  </div><!--//col-12-->
                </div><!--//row-->
              </div><!--//post-author-->
            </div><!--//post-excerpt-->
          </a><!--//post-link-->
        </div><!--//item-->
      </div><!--//col-->
      {% endfor %}
    </div><!--//row-->
    <div class="text-center"><a href="/archive" class="btn-gradient btn">More...</a></div>
  </div><!--//container-->
</section><!--//blog-list-section-->