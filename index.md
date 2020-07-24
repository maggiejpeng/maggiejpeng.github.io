---
layout: default
title: "Home"
---
<style>
{% for post in site.posts %}
#{{ post.id | regex_replace:'[0-9\-\/]','' }}:hover {
  background: rgba({{ post.background }},.5);
}
{% endfor %}
</style>
<div class="posts">
  {% for post in site.posts %}
  <div class="post" style="background-image: url('/images/{{ post.image }}');">
  <div class="dummy"></div>
    <a id="{{ post.id | regex_replace:'[0-9\-\/]','' }}" href="{{ post.url }}" style="opacity: 1;">
      <div class="posttitle">{{ post.title }}</div>
    </a>
  </div>
  {% endfor %}
</div>
