---
layout: default
title: "Home"
---
<div class="posts">
  {% for post in site.posts %}
  <div class="post" style="background-image: url('/images/{{ post.image }}')">
    <a href="{{ post.url }}" style="opacity: 1;">
      <h1>{{ post.title }}</h1>
    </a>
  </div>
  {% endfor %}
</div>
