---
layout: page
title: Team
permalink: /team
---
AI Helps Ukraine is organized by volunteer students and friends from [Mila](https://mila.quebec). We are deeply concerned by the impacts of the war in Ukraine on research institutes and medical treatments. Many students and researchers in Ukraine are affected by war and cannot continue their work - their loss is our loss as a global community. 

{% assign people = site.data.team | sample: site.data.team.size %}
{% for person in people %}
  {% assign side = forloop.index0 | modulo: 2 %}
    {% if side == 0 %}
      {% include team-card.html %}
    {% else %}
      {% include team-card.html %}
    {% endif %}
{% endfor %}
  
