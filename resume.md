---
layout: experience
title: Resume
permalink: /resume/
---

<h2 style="text-align: center; font-size: 2rem; margin-bottom: 2rem; font-weight: 700;">Resume</h2>

{% if site.resume_link and site.resume_link != "" %}
<div style="max-width: 1000px; margin: 0 auto 2rem auto; text-align: center;">
  <a href="{{ site.resume_link }}" target="_blank" style="display: inline-block; background: #669bbc; color: white; padding: 0.75rem 1.5rem; border-radius: 6px; text-decoration: none; font-weight: 600; margin-bottom: 2rem;">Open in New Tab / Download</a>
</div>

<div style="max-width: 1000px; margin: 0 auto; background: white; border-radius: 12px; box-shadow: 0 4px 16px rgba(0,0,0,0.08); overflow: hidden;">
  {% assign file_id = site.resume_link | split: '/d/' | last | split: '/' | first %}
  <iframe src="https://drive.google.com/file/d/{{ file_id }}/preview" style="width: 100%; height: 800px; border: none;"></iframe>
</div>

<p style="text-align: center; margin-top: 1rem; color: #888; font-size: 0.9rem;">If the preview doesn't load, <a href="{{ site.resume_link }}" target="_blank" style="color: #669bbc;">click here to view the resume</a>.</p>

{% else %}
<p style="text-align: center; color: #888;">No resume link configured.</p>
{% endif %}
