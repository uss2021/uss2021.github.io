---
layout: page
title: Team
permalink: /team
---
USS is organized every year by volunteer students from [UNIQUE](https://sites.google.com/view/unique-neuro-ai/home). This is the organizing team of USS 2021, in random order.

{% assign people = site.data.team | sample: site.data.team.size %}
{% for person in people %}
  {% assign side = forloop.index0 | modulo: 2 %}
    {% if side == 0 %}
      {% include team-card.html %}
    {% else %}
      {% include team-card.html %}
    {% endif %}
{% endfor %}
  
