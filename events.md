---
layout: default
title: Events
---

<div class="page-header">
  <h1>Events</h1>
  {% include leaf-divider.html %}
</div>

<div class="section-narrow">
  <ul class="show-list">
  {% for show in site.data.shows %}
    <li>
      <span class="show-date">{{ show.date | date: "%b %-d, %Y" }}</span>
      <span class="show-place">
        {{ show.city }} <span class="show-venue">— {{ show.venue }}</span>
      </span>
      {% if show.ticket_url != "" %}
        <a class="btn btn-outline" href="{{ show.ticket_url }}" target="_blank" rel="noopener">Tickets</a>
      {% endif %}
    </li>
  {% endfor %}
  </ul>
</div>

<div class="photo-frame" style="width: 400px; margin: auto;">
  <img src="{{ '/assets/img/band-color.jpg' | relative_url }}" alt="Playing to the Plants band photo">
</div>
