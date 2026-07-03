---
layout: default
title: Home
---

<div class="hero">
  <div>
    <span class="hero-eyebrow">Bastrop, TX</span>
    <h1>Playing to<br>the Plants</h1>
    <p class="hero-pitch">
      A three-piece rock band that brings dynamic texture to melodic original songs. Additionally, they offer a wide catalogue of crowd pleasing covers, ranging from Michael Jackson to System of a Down.
    </p>
    <div class="hero-actions">
      <a class="btn btn-primary" href="{{ '/music.html' | relative_url }}">Listen to the music</a>
      <a class="btn btn-outline" href="{{ '/epk.html' | relative_url }}">EPK</a>
      <a class="btn btn-outline" href="{{ '/events.html' | relative_url }}">See upcoming shows</a>
    </div>
  </div>
  {% include hero-pttp-plant.html %}
</div>
<!-- <div class="hero-photo section-narrow">
  <div class="photo-frame">
    <img src="{{ '/assets/img/stylized-band.jpg' | relative_url }}" alt="Playing to the Plants band photo">
    <span class="frame-badge">
      <svg width="20" height="20"><use href="#icon-flower"></use></svg>
    </span>
  </div>
</div> -->

{% include leaf-divider.html %}

<div class="section">
  <div class="nav-grid">
    {% for item in site.data.nav %}
      <a class="nav-card" href="{{ item.url | relative_url }}">
        <svg width="26" height="26"><use href="#icon-{{ item.icon }}"></use></svg>
        <h3>{{ item.title }}</h3>
        <p class="nav-card-blurb">{{ item.blurb }}</p>
      </a>
    {% endfor %}
  </div>
</div>

<div class="section-narrow">
  {% include mailing-list.html %}
</div>
