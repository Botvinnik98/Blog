---
layout: default
title: "Stories & Cases"
permalink: /stories/
---

<h1>Stories & Cases</h1>

<!-- Destacados -->
<div class="featured-cards">
  {% assign stories_posts = site.categories.stories | sort: "date" | reverse %}
  {% for post in stories_posts limit:3 %}
    <div class="card">
      <h3><a href="{{ post.url | relative_url }}">{{ post.title }}</a></h3>
      <p>{{ post.description }}</p>
    </div>
  {% endfor %}
</div>

<!-- Últimos -->
<h2>Latest Posts</h2>
<div class="post-cards">
  {% for post in stories_posts %}
    <div class="post-card">
      <h3><a href="{{ post.url | relative_url }}">{{ post.title }}</a></h3>
      <p class="meta">{{ post.date | date: "%Y-%m-%d" }}</p>
      <p>{{ post.description }}</p>
    </div>
  {% endfor %}
</div>
