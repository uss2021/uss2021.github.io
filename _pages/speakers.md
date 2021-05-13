---
title: Speakers
layout: page
permalink: /speakers
---
# Monday June 7th
{% assign people = site.data.speakers | sample: site.data.speakers.size %}
{% for person in people %}
  {% if person.fullname == "TBA" %}{% continue %}{% endif %}
  {% for session in person.sessions %}
    {% assign sessionright = false %}
    {% if session contains "20210607" %}
        {% assign sessionright = true %}
    {% endif %}
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

# Tuesday June 8th
{% assign people = site.data.speakers | sample: site.data.speakers.size %}
{% for person in people %}
  {% if person.fullname == "TBA" %}{% continue %}{% endif %}
  {% for session in person.sessions %}
    {% assign sessionright = false %}
    {% if session contains "20210608" %}
        {% assign sessionright = true %}
    {% endif %}
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
