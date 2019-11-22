---
layout: default
title: Tips & Tricks
permalink: /tips-and-tricks/
---
<div class="post-block-container">
  {% for post in site.tags.['Tips and Tricks'] %}
  <div class="post-block">
    <a href="{{post.url}}">
    {% if post.use_youtube_image == true %}
    <img src="http://img.youtube.com/vi/{{post.youtube_code}}/maxresdefault.jpg" alt="{{post.title}}" class="post-image" />
    {% else %}
    <img src="{{post.youtube_alternate_image}}" alt="{{site.title}}" class="post-image"/>
    {% endif %}
    </a>
    <h3 class="post-overview-title"><a class="post-link" href="{{ post.url }}">{{ post.title | truncate: 70 }}</a></h3>
    <span class="post-meta">
      {{ post.date | date: "%b %-d, %Y" }}</span>
    <div class="post-excerpts">
      {{ post.excerpt | truncate: 380 | strip_html | prepend: "<p class='excerpt'>" | append: "<p>" }}
    <div class="readmore-container">
      <p class="readlink"><a href="{{post.url}}" class="readmore">Read More</a></p>


  {% endfor %}
</div>
