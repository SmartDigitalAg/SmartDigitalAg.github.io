---
title: "Allan Lab - Team"
layout: gridlay
excerpt: "Allan Lab: Team members"
sitemap: false
permalink: /team/
---

[//]: # (# Group Members)

[//]: # ()
[//]: # ([//]: # &#40; **We are  looking for new PhD students, Postdocs, and Master students to join the team** [&#40;see openings&#41;]&#40;{{ site.url }}{{ site.baseurl }}/vacancies&#41; **!**&#41;)
[//]: # (전북대학교 스마트팜학과 스마트디지털농업 연구실 구성원 입니다.)

[//]: # (Jump to [staff]&#40;#staff&#41;, [master and bachelor students]&#40;#master-and-bachelor-students&#41;, [alumni]&#40;#alumni&#41;, [administrative support]&#40;#administrative-support&#41;, [lab visitors]&#40;#lab-visitors&#41;.)

## Principal Investigator
{% assign number_printed = 0 %}
{% for member in site.data.professor %}

{% assign even_odd = number_printed | modulo: 2 %}

{% if even_odd == 0 %}
<div class="row">
{% endif %}

<div class="col-lg-6 clearfix">
  <img src="{{ site.url }}{{ site.baseurl }}/images/teampic/{{ member.photo }}" class="img-responsive" width="70%" style="float: left;" />
</div>
<div class="col-lg-6 clearfix">
  <h4>{{ member.name }}</h4>
  <p>{{ member.info }}</p>
  <br>
  <p>Major: {{ member.major }}</p>
  <p>Lab: {{ member.lab }}</p>
  <p>Lab Phone: {{ member.lab_phone }}</p>
  <p>Email: {{ member.email }}</p>
  <a href="https://code.taegon.kr/"><img src="{{ site.url }}{{ site.baseurl }}/images/teampic/{{ member.homepage }}" style="width: 50px; height: 50px;"></a>
    <a href="https://github.com/taegon"><img src="{{ site.url }}{{ site.baseurl }}/images/teampic/{{ member.github }}" style="width: 50px; height: 50px;">
    </a>
</div>
{% assign number_printed = number_printed | plus: 1 %}

{% if even_odd == 1 %}
</div>
{% endif %}

{% endfor %}


[//]: # (## Doctor)

[//]: # ()
[//]: # ({% assign number_printed = 0 %})

[//]: # ({% for member in site.data.docs %})

[//]: # ()
[//]: # ({% assign even_odd = number_printed | modulo: 2 %})

[//]: # ()
[//]: # ({% if even_odd == 0 %})

[//]: # (<div class="row">)

[//]: # ({% endif %})

[//]: # ()
[//]: # (<div class="col-sm-6 clearfix">)

[//]: # (  <img src="{{ site.url }}{{ site.baseurl }}/images/teampic/{{ member.photo }}" class="img-responsive" width="25%" style="float: left" />)

[//]: # (  <h4>{{ member.name }}</h4>)

[//]: # (  <i>{{ member.info }} <!-- <br>email: <{{ member.email }}></i> -->)

[//]: # (  <br>email: <{{ member.email }}></i>)

[//]: # (  <ul style="overflow: hidden">)

[//]: # ()
[//]: # (  {% if member.number_educ == 1 %})

[//]: # (  <li> {{ member.education1 }} </li>)

[//]: # (  {% endif %})

[//]: # ()
[//]: # (  {% if member.number_educ == 2 %})

[//]: # (  <li> {{ member.education1 }} </li>)

[//]: # (  <li> {{ member.education2 }} </li>)

[//]: # (  {% endif %})

[//]: # ()
[//]: # (  {% if member.number_educ == 3 %})

[//]: # (  <li> {{ member.education1 }} </li>)

[//]: # (  <li> {{ member.education2 }} </li>)

[//]: # (  <li> {{ member.education3 }} </li>)

[//]: # (  {% endif %})

[//]: # ()
[//]: # (  {% if member.number_educ == 4 %})

[//]: # (  <li> {{ member.education1 }} </li>)

[//]: # (  <li> {{ member.education2 }} </li>)

[//]: # (  <li> {{ member.education3 }} </li>)

[//]: # (  <li> {{ member.education4 }} </li>)

[//]: # (  {% endif %})

[//]: # ()
[//]: # (  </ul>)

[//]: # (</div>)

[//]: # ()
[//]: # ({% assign number_printed = number_printed | plus: 1 %})

[//]: # ()
[//]: # ({% if even_odd == 1 %})

[//]: # (</div>)

[//]: # ({% endif %})

[//]: # ()
[//]: # ({% endfor %})

[//]: # ()
[//]: # ({% assign even_odd = number_printed | modulo: 2 %})

[//]: # ({% if even_odd == 1 %})

[//]: # (</div>)

[//]: # ({% endif %})


[//]: # (## Master and Undergraduate education)
[//]: # ({% assign number_printed = 0 %})

[//]: # ({% for member in site.data.students %})

[//]: # ()
[//]: # ({% assign even_odd = number_printed | modulo: 2 %})

[//]: # ()
[//]: # ({% if even_odd == 0 %})

[//]: # (<div class="row">)

[//]: # ({% endif %})

[//]: # ()
[//]: # (<div class="col-sm-6 clearfix">)

[//]: # (  <img src="{{ site.url }}{{ site.baseurl }}/images/teampic/{{ member.photo }}" class="img-responsive" width="25%" style="float: left" />)

[//]: # (  <h4>{{ member.name }}</h4>)

[//]: # (  <i>{{ member.info }} <!-- <br>email: <{{ member.email }}></i> -->)

[//]: # (  <br>email: <{{ member.email }}></i>)

[//]: # (  <ul style="overflow: hidden">)

[//]: # ()
[//]: # (  {% if member.number_educ == 1 %})

[//]: # (  <li> {{ member.education1 }} </li>)

[//]: # (  {% endif %})

[//]: # ()
[//]: # (  {% if member.number_educ == 2 %})

[//]: # (  <li> {{ member.education1 }} </li>)

[//]: # (  <li> {{ member.education2 }} </li>)

[//]: # (  {% endif %})

[//]: # ()
[//]: # (  {% if member.number_educ == 3 %})

[//]: # (  <li> {{ member.education1 }} </li>)

[//]: # (  <li> {{ member.education2 }} </li>)

[//]: # (  <li> {{ member.education3 }} </li>)

[//]: # (  {% endif %})

[//]: # ()
[//]: # (  {% if member.number_educ == 4 %})

[//]: # (  <li> {{ member.education1 }} </li>)

[//]: # (  <li> {{ member.education2 }} </li>)

[//]: # (  <li> {{ member.education3 }} </li>)

[//]: # (  <li> {{ member.education4 }} </li>)

[//]: # (  {% endif %})

[//]: # ()
[//]: # (  </ul>)

[//]: # (</div>)

[//]: # ()
[//]: # ({% assign number_printed = number_printed | plus: 1 %})

[//]: # ()
[//]: # ({% if even_odd == 1 %})

[//]: # (</div>)

[//]: # ({% endif %})

[//]: # ()
[//]: # ({% endfor %})

[//]: # ()
[//]: # ({% assign even_odd = number_printed | modulo: 2 %})

[//]: # ({% if even_odd == 1 %})

[//]: # (</div>)

[//]: # ({% endif %})




[//]: # (## Former students)

[//]: # (<div class="row">)

[//]: # ()
[//]: # ()
[//]: # (<div class="col-sm-4 clearfix">)

[//]: # (<h4>under graduate education</h4>)

[//]: # ({% for member in site.data.alumni_bsc %})

[//]: # ({{ member.name }})

[//]: # ({% endfor %})

[//]: # (</div>)

[//]: # ()
[//]: # (</div>)


[//]: # (## Administrative Support)

[//]: # (<a href="mailto:Rijsewijk@Physics.LeidenUniv.nl">Ellie van Rijsewijk</a> is helping us &#40;and other groups&#41; with administration.)
