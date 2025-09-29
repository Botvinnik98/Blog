---
layout: default
title: "Welcome"
permalink: /
---

<!-- 📈 Barra de cotizaciones estilo Wall Street -->
<div class="tradingview-widget-container">
  <div class="tradingview-widget-container__widget"></div>
  <script type="text/javascript" src="https://s3.tradingview.com/external-embedding/embed-widget-ticker-tape.js" async>
  {
  "symbols": [
    { "proName": "FOREXCOM:SPXUSD", "title": "S&P 500" },
    { "proName": "NASDAQ:IXIC", "title": "NASDAQ" },
    { "proName": "DJI", "title": "Dow Jones" },
    { "proName": "CME_MINI:ES1!", "title": "E-Mini S&P Futures" },
    { "proName": "OANDA:EURUSD", "title": "EUR/USD" },
    { "proName": "COMEX:GC1!", "title": "Gold" },
    { "proName": "NYMEX:CL1!", "title": "Crude Oil" },
    { "proName": "BINANCE:BTCUSDT", "title": "Bitcoin" },
    { "proName": "BINANCE:ETHUSDT", "title": "Ethereum" }
  ],
  "showSymbolLogo": true,
  "colorTheme": "dark",
  "isTransparent": false,
  "displayMode": "adaptive",
  "locale": "en"
  }
  </script>
</div>

## BEHIND THE TAPE

Welcome to BehindTheTape. In this blog, we share insights on the markets, explore the legacy of great investors, uncover the secrets behind major financial scandals, and connect the dots between yesterday and today to understand tomorrow.

---

## Featured Articles
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

## Latest Posts
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

