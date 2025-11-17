---
title: "Allan Lab - Team"
layout: gridlay
excerpt: "Allan Lab: Team members"
sitemap: false
permalink: /students/
---

### Postdoctoral researcher
<div class="row">
<div class="col-lg-6">
<img src="{{ site.url }}{{ site.baseurl }}/images/teampic/{{ site.data.students[0].photo }}" class="img-responsive" style="float: left; width: 150px; height: 200px;" />
  <h4>{{ site.data.students[0].name }}</h4>
  <p>{{ site.data.students[0].info }}</p>
  <p>Email: {{ site.data.students[0].email }}</p>
</div>
</div>

### Undergraduate Intern
{% assign number_printed = 0 %}
<div class="row">
{% for member in site.data.students offset:1 %}

{% assign even_odd = number_printed | modulo: 2 %}

{% if even_odd == 0 and number_printed != 0 %}
</div>
<div class="row">
{% endif %}

<div class="col-lg-6 clearfix">
  <img src="{{ site.url }}{{ site.baseurl }}/images/teampic/{{ member.photo }}" class="img-responsive" style="float: left; width: 150px; height: 200px;" />
  <h4>{{ member.name }}</h4>
  <p>{{ member.info }}</p>
  <p>Email: {{ member.email }}</p>
</div>

{% assign number_printed = number_printed | plus: 1 %}

{% endfor %}
</div>

