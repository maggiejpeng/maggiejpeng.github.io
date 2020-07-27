---
layout: default
title: "Home"
---
<style>
{% for item in site.work %}
#{{ item.title | remove: ' ' }}:hover {
  background: rgba({{ item.background }},.7);
}
{% endfor %}
</style>
<div class="posts">
  {% assign sorted_work = site.work | sort:"score" %}
  {% for item in sorted_work %}
  <div class="post" style="background-image: url('{{ item.image }}');">
    <div class="dummy"></div>
    <a id="{{ item.title | remove: ' ' }}" href="{{ item.url }}" style="opacity: 1;">
    <div class="posttitle">{{ item.title }}</div>
    </a>
  </div>
  {% endfor %}
</div>
