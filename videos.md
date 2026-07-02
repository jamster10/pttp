---
layout: default
title: Videos
---

<div class="page-header">
  <h1>Videos</h1>
  {% include leaf-divider.html %}
</div>

<div class="section-narrow">
  <div class="media-list">
    {% for video in site.data.videos %}
      {% include video-embed.html id=video.youtube_id title=video.title %}
    {% endfor %}
  </div>
</div>
