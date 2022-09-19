---
title: Speakers
layout: page
permalink: /speakers
---
{% assign people = site.data.speakers %}
{% for person in people %}
  {% if person.fullname == "TBA" %}{% continue %}{% endif %}
  {% for session in person.sessions %}
    {% assign sessionright = true %}
  {% endfor %}
  {% if sessionright %}
    {% assign side = forloop.index0 | modulo: 2 %}
      {% if side == 0 %}
        {% include speaker-card.html %}
      {% else %}
        {% include speaker-card.html %}
      {% endif %}
  {% endif %}
{% endfor %}

