---
title: Speakers
layout: page
toc: true
permalink: /speakers
---
{% assign people = site.data.speakers | sample: site.data.speakers.size %}
{% for person in people %}
  {% assign side = forloop.index0 | modulo: 2 %}
    {% if side == 0 %}
      {% include speaker-card.html %}
    {% else %}
      {% include speaker-card.html %}
    {% endif %}
{% endfor %}
  
