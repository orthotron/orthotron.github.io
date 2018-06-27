---
title: "Orthotron - Research"
layout: gridlay
excerpt: "Orthotron -- Research"
sitemap: false
permalink: /research/
---

# Research Areas 

The Orthopaedic Mechatronics Laboratory conducts research aimed at characterization and optimization of biomechanical factors influencing the performance of orthopaedic interventions. Areas of current research interest include:

{% assign number_printed = 0 %}
{% for area in site.data.research %}

{% assign even_odd = number_printed | modulo: 2 %}

{% if even_odd == 0 %}
<div class="row">
{% endif %}

<div class="col-sm-6 clearfix">
  <img src="{{ site.url }}{{ site.baseurl }}/images/{{ area.photo }}" class="img-responsive" width="50%" style="float: left" />
  <h4>{{ area.project }}</h4>
  <i>{{ area.desc }}</i>

</div>

{% assign number_printed = number_printed | plus: 1 %}

{% if even_odd == 1 %}
</div>
{% endif %}

{% endfor %}

{% assign even_odd = number_printed | modulo: 2 %}
{% if even_odd == 1 %}
</div>
{% endif %}