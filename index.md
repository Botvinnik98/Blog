---
layout: default
title: "Welcome"
permalink: /
---

<!-- HERO full-bleed -->
<section class="full-bleed hero-band">
  <div class="inner">
    <h1 class="hero-title">Beyond The Charts</h1>
    <p class="hero-subtitle">
      Markets are not boring graphs: they are dramas with villains, heroes, and unexpected twists.  
      At BeyondTheCharts, we tell you the financial saga that Wall Street would prefer to keep secret.
    </p>
  </div>
</section>

<!-- FEATURED full-bleed (sin título) -->
<section class="full-bleed featured-band">
  <div class="inner">
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
  </div>
</section>

<!-- Latest Posts (panel estrecho con fondo, sin título) -->
<section class="narrow-panel">
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
</section>
