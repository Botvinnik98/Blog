---
layout: default
title: "Welcome"
permalink: /
---

# 🚀 Welcome to My Blog

Here I share reflections on financial markets, legendary investors, and hidden trading signals.

---

## ⭐ Featured (top 3)
<div class="featured-grid">
{% assign featured = site.posts | where_exp:"p","p.featured == true" | slice: 0, 3 %}
{% for post in featured %}
  <article class="featured-item">
    <h3><a href="{{ post.url | relative_url }}">{{ post.title }}</a></h3>
    <p>{{ post.excerpt | strip_html | truncate: 140 }}</p>
  </article>
{% endfor %}
{% if featured == empty %}
  <p>Add <code>featured: true</code> in a post front matter to show it here.</p>
{% endif %}
</div>

---

## 📰 Latest Posts
<ul class="latest-list">
{% for post in site.posts limit:10 %}
  <li>
    <a href="{{ post.url | relative_url }}">{{ post.title }}</a>
    <small> — {{ post.date | date: "%Y-%m-%d" }}</small>
  </li>
{% endfor %}
</ul>
