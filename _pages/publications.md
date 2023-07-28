---
title: "Publications"
layout: gridlay
excerpt: "Publications."
sitemap: false
permalink: /publications/
---

## Journal Publications
{% for publi in site.data.publist %}

<div class="row">
<div class="col-sm-11 clearfix">
 <div class="well well-sm">
  <img src="{{ site.url }}{{ site.baseurl }}/images/pubpic/{{ publi.image }}" class="img-responsive" width="11%" style="float: left" />
  <p>{{ publi.title }}  <br> 
  <em>{{ publi.authors }}</em> <br> 
  <strong><a href="{{ publi.link.url }}">{{ publi.link.display }}</a></strong> 
   {% if publi.project != 0 %}
      <button type="button" class="btn-xs btn-info" onclick="window.location.href= '{{ publi.project }}'">
      PROJECT
      </button> 
   {%- if publi.project != 0 %}
      <button type="button" class="btn-xs btn-info" onclick="window.location.href= '{{ publi.project }}'">
      PDF
      </button> 
  {% endif %}{% endif %}</p>
 </div>
</div>
</div>

{% endfor %}

## Patents
{% for publi in site.data.publistpatent %}
<div class="row">
<div class="col-sm-11 clearfix">
 <div class="well well-sm">
  <img src="{{ site.url }}{{ site.baseurl }}/images/pubpic/{{ publi.image }}" class="img-responsive" width="11%" style="float: left" />
  <p>{{ publi.title }}</p>
  <p><em>{{ publi.authors }}</em></p>
  <p><strong><a href="{{ publi.link.url }}">{{ publi.link.display }}</a></strong></p>
 </div>
</div>
</div>
{% endfor %}

## ​Book Chapters
{% for publi in site.data.publistbook %}
<div class="row">
<div class="col-sm-11 clearfix">
 <div class="well well-sm">
  <img src="{{ site.url }}{{ site.baseurl }}/images/pubpic/{{ publi.image }}" class="img-responsive" width="11%" style="float: left" />
  <p>{{ publi.title }}</p>
  <p><em>{{ publi.authors }}</em></p>
  <p><strong><a href="{{ publi.link.url }}">{{ publi.link.display }}</a></strong></p>
 </div>
</div>
</div>
{% endfor %}

## Conference Publications
{% for publicon in site.data.publistconf %}
<div class="row">
<div class="col-sm-11 clearfix">
 <div class="well well-sm">
  <img src="{{ site.url }}{{ site.baseurl }}/images/pubpic/{{ publicon.image }}" class="img-responsive" width="11%" style="float: left" />
  <p>{{ publicon.title }} <br> 
  <em>{{ publicon.authors }}</em> <br>
  {{ publicon.venue }} <br>
  {{ publicon.location }}</p>
 </div>
</div>
</div>
{% endfor %}

## PhD Thesis
{% for publicon in site.data.publistthesis %}
<div class="row">
<div class="col-sm-11 clearfix">
 <div class="well well-sm">
  <img src="{{ site.url }}{{ site.baseurl }}/images/pubpic/{{ publicon.image }}" class="img-responsive" width="11%" style="float: left" />
  <p>{{ publicon.title }}</p>
  <p><em>{{ publicon.authors }}</em></p>
  <p>{{ publicon.venue }}</p>
 </div>
</div>
</div>
{% endfor %}
