---
layout: default
title: Contact
---

<div class="page-header">
  <h1>Contact</h1>
  {% include leaf-divider.html %}
</div>

<div class="section-narrow">

  <div class="contact-grid">
    <div class="contact-card">
      <h3>Booking</h3>
      <a href="mailto:{{ site.booking_email }}">{{ site.booking_email }}</a>
    </div>
    <div class="contact-card">
      <h3>Press</h3>
      <a href="mailto:{{ site.press_email }}">{{ site.press_email }}</a>
    </div>
  </div>

{% include mailing-list.html %}

</div>
