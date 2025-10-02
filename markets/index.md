---
layout: default
title: "Markets"
permalink: /markets/
---

<h1>Markets</h1>

<!-- Destacados de Markets -->
<div class="featured-cards">
  {% for post in site.categories.markets limit:3 %}
    <div class="card">
      <h3><a href="{{ post.url | relative_url }}">{{ post.title }}</a></h3>
      <p>{{ post.description }}</p>
    </div>
  {% endfor %}
</div>

<!-- Últimos posts de Markets -->
<h2>Latest Posts</h2>
<div class="post-cards">
  {% for post in site.categories.markets %}
    <div class="post-card">
      <h3><a href="{{ post.url | relative_url }}">{{ post.title }}</a></h3>
      <p class="meta">{{ post.date | date: "%Y-%m-%d" }}</p>
      <p>{{ post.description }}</p>
    </div>
  {% endfor %}
</div>

