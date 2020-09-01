---
layout: default
title: "Archive"
description: "Change log and other updates"
---

<section class="hero-section over-curve pt-5 py-md-5">
    <div class="container">
        <h1 class="page-headline text-center mb-5">Archive</h1>
        <div class="hero-content-holder z-index-10 position-relative">
            {% for post in site.posts offset:9 %}
            <div class="post-preview">
                <a href="{{ post.url | prepend: site.baseurl }}">
                    <h5 class="post-title">
                        {{ post.title }} (<em>{{ post.author.display_name }}, {{ post.date | date: "%B %-d, %Y" }}</em>)
                    </h5>
                </a>
                <p>
                    {{ post.content | strip_html | truncatewords:32}}
                    <br>
                    <a href="{{ post.url }}">Read more...</a>
                </p>
            </div>
            <hr>
            {% endfor %}
        </div>
    </div><!--//container-->
</section><!--//hero-section-->   
        