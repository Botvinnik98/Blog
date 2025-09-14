---
layout: default
title: "Welcome"
permalink: /
---

# 🚀 Welcome to My Blog

Here I share reflections on financial markets, legendary investors, and hidden trading signals.

---

## ⭐ Featured (top 3)
<div class="featured-cards">
{% assign featured = site.posts | where_exp:"p","p.featured == true" | slice: 0, 3 %}
{% for post in featured %}
  <article class="card">
    <h3><a href="{{ post.url | relative_url }}">{{ post.title }}</a></h3>
    <p>{{ post.excerpt | strip_html | truncate: 180 }}</p>
  </article>
{% endfor %}
{% if featured == empty %}
  <p>Add <code>featured: true</code> in a post front matter to show it here.</p>
{% endif %}
</div>

---

## 📰 Latest Posts
<div class="post-cards">
{% for post in site.posts limit:10 %}
  <article class="post-card">
    {% if post.image %}
      <img class="post-thumb" src="{{ post.image | relative_url }}" alt="">
    {% endif %}
    <h3><a href="{{ post.url | relative_url }}">{{ post.title }}</a></h3>
    <p class="meta">
      {{ post.date | date: "%Y-%m-%d" }}{% if post.categories and post.categories.size > 0 %} · {{ post.categories | join: ', ' }}{% endif %}
    </p>
    <p>{{ post.excerpt | strip_html | truncate: 200 }}</p>
  </article>
{% endfor %}
</div>

