---
layout: experience
title: Experience
permalink: /experience/
---

## Experience

{% for item in site.data.experience.work %}
<div class="experience-item {% cycle 'image-left', 'image-right' %}" data-company="{{ item.company }}">
  {% if item.image %}
  <div class="experience-image-wrapper">
    {%- assign img_base = item.image | replace: '.webp', '' | replace: '.jpg', '' | replace: '.jpeg', '' -%}
    <img 
      class="experience-image" 
      src="{{ item.image }}" 
      srcset="{{ img_base }}-280w.webp 280w, {{ img_base }}.webp 560w, {{ img_base }}-1120w.webp 1120w"
      sizes="(max-width: 600px) 100vw, (max-width: 900px) 80vw, 380px"
      alt="{{ item.company }}">
  </div>
  {% endif %}
  <div class="experience-content">
    <h3>{{ item.role }}</h3>
    <span class="company">{{ item.company }}</span>
    <p class="meta">{{ item.location }}<br>{{ item.dates }}</p>
    <ul>
    {% assign lines = item.description | strip | split: "
" %}
    {% for line in lines %}
      {% if line != "" %}
      <li>{{ line | remove_first: "- " }}</li>
      {% endif %}
    {% endfor %}
    </ul>
    {% if item.skills %}
    <p class="skills-label"><strong>Skills:</strong> {{ item.skills }}</p>
    {% endif %}
  </div>
</div>
{% endfor %}
