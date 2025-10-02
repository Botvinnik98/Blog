---
layout: default
title: "Misc"
permalink: /culture/
---

<h1>Misc</h1>

<!-- Destacados de Misc -->
<div class="featured-cards">
  {% for post in site.categories.culture limit:3 %}
    <div class="card">
      <h3><a href="{{ post.url | relative_url }}">{{ post.title }}</a></h3>
      <p>{{ post.description }}</p>
    </div>
  {% endfor %}
</div>

<!-- Últimos posts de Misc -->
<h2>Latest Posts</h2>
<div class="post-cards">
  {% for post in site.categories.culture %}
    <div class="post-card">
      <h3><a href="{{ post.url | relative_url }}">{{ post.title }}</a></h3>
      <p class="meta">{{ post.date | date: "%Y-%m-%d" }}</p>
      <p>{{ post.description }}</p>
    </div>
  {% endfor %}
</div>
