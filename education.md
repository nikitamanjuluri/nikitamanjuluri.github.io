---
layout: home
title: Education
permalink: /education/
---

{% for ed in site.data.experience.education %}
### {{ ed.degree }} — {{ ed.school }}

{{ ed.dates }}

{{ ed.details }}

---
{% endfor %}
