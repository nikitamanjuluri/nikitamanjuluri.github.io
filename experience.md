---
layout: home
title: Experience
permalink: /experience/
---

{% for item in site.data.experience.work %}
### {{ item.role }} — {{ item.company }}

{{ item.dates }} — {{ item.location }}

{{ item.description }}

---
{% endfor %}
