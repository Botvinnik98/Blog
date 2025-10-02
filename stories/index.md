---
layout: default
title: "Stories & Cases"
permalink: /stories/
---

<h1>Stories & Cases</h1>

<!-- Destacados de Stories -->
<div class="featured-cards">
  {% for post in site.categories.stories limit:3 %}
    <div class="card">
      <h3><a href="{{ post.url | relative_url }}">{{ post.title }}</a></h3>
      <p>{{ post.description }}</p>
    </div>
  {% endfor %}
</div>

<!-- Últimos posts de Stories -->
<h2>Latest Posts</h2>
<div class="post-cards">
  {% for post in site.categories.stories %}
    <div class="post-card">
      <h3><a href="{{ post.url | relative_url }}">{{ post.title }}</a></h3>
      <p class="meta">{{ post.date | date: "%Y-%m-%d" }}</p>
      <p>{{ post.description }}</p>
    </div>
  {% endfor %}
</div>
