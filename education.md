---
layout: experience
title: Education
permalink: /education/
---

<h2 style="text-align: center; font-size: 2rem; margin-bottom: 3rem; font-weight: 700;">Education</h2>

{% for ed in site.data.experience.education %}
<div style="max-width: 900px; margin: 0 auto 3rem auto; padding: 2rem; background: white; border-radius: 12px; box-shadow: 0 4px 16px rgba(0,0,0,0.08);">
  <div style="display: flex; align-items: center; gap: 2rem; margin-bottom: 1.5rem;">
    {% if ed.logo %}
    <img src="{{ ed.logo }}" alt="{{ ed.school }}" style="width: 80px; height: 80px; object-fit: contain;">
    {% endif %}
    <div style="flex: 1;">
      <h3 style="margin: 0 0 0.25rem 0; font-size: 1.5rem; color: #111;">{{ ed.school }}</h3>
      <p style="margin: 0.25rem 0; font-size: 1.1rem; color: #669bbc; font-weight: 600;">{{ ed.degree }}</p>
      {% if ed.minor %}<p style="margin: 0.25rem 0; font-size: 0.95rem; color: #666;">{{ ed.minor }} • GPA {{ ed.gpa }}</p>{% endif %}
      <p style="margin: 0.5rem 0 0 0; font-size: 0.9rem; color: #888;">{{ ed.location }} • {{ ed.dates }}</p>
    </div>
  </div>
  
  {% if ed.description %}
  <p style="line-height: 1.7; color: #444; margin-bottom: 1.5rem;">{{ ed.description }}</p>
  {% endif %}
  
  {% if ed.coursework %}
  <div>
    <h4 style="font-size: 1rem; color: #111; margin-bottom: 0.75rem; font-weight: 600;">Relevant Coursework:</h4>
    <div style="display: flex; flex-wrap: wrap; gap: 0.5rem;">
      {% for course in ed.coursework %}
      <span style="background: #f0f0f0; padding: 0.4rem 0.8rem; border-radius: 6px; font-size: 0.85rem; color: #555;">{{ course }}</span>
      {% endfor %}
    </div>
  </div>
  {% endif %}
</div>
{% endfor %}
