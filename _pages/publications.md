---
title: "Publications"
layout: gridlay
excerpt: "Publications."
sitemap: false
permalink: /publications/
---


# Publications

**At the end of this page, you can find the [full list of publications and patents](#full-list-of-publications). Most papers are also available on [arXiv](https://arxiv.org/search/?searchtype=author&query=Allan%2C+M+P).**

{% assign number_printed = 0 %}
{% for publi in site.data.publist %}

{% assign even_odd = number_printed | modulo: 2 %}
{% if publi.highlight == 1 %}

<div class="row">

<div class="col-sm-12 clearfix">
 <div class="well well-sm">
  <img src="{{ site.url }}{{ site.baseurl }}/images/pubpic/{{ publi.image }}" class="img-responsive" width="10%" style="float: left" />
  <p>{{ publi.title }}</p>
  <p><em>{{ publi.authors }}</em></p>
  <p><strong><a href="{{ publi.link.url }}">{{ publi.link.display }}</a></strong></p>
 </div>
</div>

{% assign number_printed = number_printed | plus: 1 %}

</div>

{% endif %}
{% endfor %}

{% assign even_odd = number_printed | modulo: 2 %}

</div>





## Patents
<em>Milan P Allan, S Gröblacher, RA Norte, M Leeuwenhoek</em><br />Novel atomic force microscopy probes with phononic crystals<br /> PCT/NL20-20/050797 (2020)

<em>Milan P Allan</em><br /> Methods of manufacturing superconductor and phononic elements <br /> <a href="https://patents.google.com/patent/US10439125B2/en?inventor=Milan+ALLAN&oq=inventor:(Milan+ALLAN)">US10439125B2 (2016)</a>

## Full List of publications

{% for publi in site.data.publist %}

  {{ publi.title }} <br />
  <em>{{ publi.authors }} </em><br /><a href="{{ publi.link.url }}">{{ publi.link.display }}</a>

{% endfor %}
