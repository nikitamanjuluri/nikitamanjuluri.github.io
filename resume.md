---
layout: home
title: Resume
permalink: /resume/
---

## Resume

{% if site.resume_link and site.resume_link != "" %}
You can view or download my resume here: [Open resume]({{ site.resume_link }})

If you prefer, right-click the link and choose "Save link as..." to download a local copy.
{% else %}
No resume link configured. Add `resume_link: "https://drive.google.com/..."` to `_config.yml`.
{% endif %}
