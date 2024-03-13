---
title: "Allan Lab - Publications"
layout: gridlay
excerpt: "Allan Lab -- Publications."
sitemap: false
permalink: /publications/
---


# Publications

<br />

{% assign number_printed = 0 %}
{% for posterli in site.data.posters %}

{% assign even_odd = number_printed | modulo: 2 %}
{% if posterli.highlight == 1 %}

{% if even_odd == 0 %}
<div class="row">
{% endif %}

<div class="col-sm-6 clearfix">
  <pubtit>{{ posterli.title }}</pubtit>
  <img src="{{ site.url }}{{ site.baseurl }}/images/posterpic/{{ posterli.image }}" class="img-responsive" width="100%" style="float: left" />
  <p>{{ posterli.description }}</p>
  <p><em>{{ posterli.authors }}</em></p>

</div>

{% assign number_printed = number_printed | plus: 1 %}

{% if even_odd == 1 %}
</div>
{% endif %}

{% endif %}
{% endfor %}

{% assign even_odd = number_printed | modulo: 2 %}
{% if even_odd == 1 %}

{% endif %}

<p> &nbsp; </p>



## International Journal Papers

{% for publi in site.data.publist %}

  <p style="font-size: large">{{ publi.title }}</p>
  <em>{{ publi.authors }} </em><br /><a href="{{ publi.link.url }}">{{ publi.link.display }}</a>

{% endfor %}

* * *


## Domestic Conference Papers/Posters
<br />

* * *

## International Conference Papers
<br />

* * *
## Domestic Journal Papers
<br />

* * *