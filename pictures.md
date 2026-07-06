---
layout: default
title: Pictures
---

<div class="page-header">
  <h1>Pictures</h1>
  {% include leaf-divider.html %}
</div>

<div class="section">
  <div class="gallery-grid">
    {% for photo in site.data.gallery %}
      <div class="gallery-item">
        <img src="{{ photo.image | relative_url }}" alt="{{ photo.caption }}" loading="lazy">
        {% if photo.caption %}<span class="gallery-caption">{{ photo.caption }}</span>{% endif %}
      </div>
    {% endfor %}
  </div>
</div>
