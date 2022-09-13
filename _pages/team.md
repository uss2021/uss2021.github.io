---
layout: page
title: Team
permalink: /team
---
AI Helps Ukraine is organized by volunteer students and friends from [Mila](https://mila.quebec).

{% assign people = site.data.team | sample: site.data.team.size %}
{% for person in people %}
  {% assign side = forloop.index0 | modulo: 2 %}
    {% if side == 0 %}
      {% include team-card.html %}
    {% else %}
      {% include team-card.html %}
    {% endif %}
{% endfor %}
  
