---
title: "Allan Lab - Publications"
layout: gridlay
excerpt: "Allan Lab -- Publications."
sitemap: false
permalink: /publications/
---


# Publications

<br />




{% for publi in site.data.publist %}
  {{ publi.authors }}&ensp;{{ publi.years }}&ensp;{{ publi.title }}
  &ensp;<em>{{ publi.journals }}</em><br/><a href="{{ publi.link.url }}">{{ publi.link.display }}</a>

{% endfor %}

* * *
