---
title: Projects
permalink: /projects/
---

Here are a few highlighted projects. (Each project is a file in `/_projects/`.)

{% for project in site.projects %}
<div class="card">
  <h2><a href="{{ project.url | relative_url }}">{{ project.title }}</a></h2>
  {% if project.summary %}<p class="muted">{{ project.summary }}</p>{% endif %}
  {% if project.stack %}<p class="muted"><strong>Stack:</strong> {{ project.stack | join: ", " }}</p>{% endif %}
</div>
{% endfor %}
