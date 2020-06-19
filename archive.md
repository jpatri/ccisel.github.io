---
layout: default
title: "Archive"
description: "Change log and other updates"
---

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