---
title: "Software"
layout: gridlay
excerpt: "Software"
sitemap: false
permalink: /software/
---

### This page lists open-source software and datasets accompanied by publications.

## Software

Here is a list of open-source software released with the papers:

{% for sftwr in site.data.software %}
<div class="row">
<div class="col-sm-11 clearfix">
 <div class="well well-sm">
  <img src="{{ site.url }}{{ site.baseurl }}/images/softwarepic/{{ sftwr.image }}" class="img-responsive" width="11%" style="float: left" />
  <p><strong>{{ sftwr.title }}</strong><br> 
  {{ sftwr.description }}<br>
  {{ "Keywords: "}}<em>{{ sftwr.keywords }}</em> 
  {% if sftwr.link != 0 %}
      <button type="button" class="btn-xs btn-info" onclick="window.location.href= '{{ sftwr.link }}'">
      CODE
      </button> 
  {%- endif %}
  {%- if publicon.project != 0 %}
      <button type="button" class="btn-xs btn-info" onclick="window.location.href= '{{ sftwr.project }}'">
      PROJECT
      </button> 
  {% endif %}
  </p>
 </div>
</div>
</div>
{% endfor %}


## Dataset

Here is a list of open-source dataset released with the papers:

{% for dtst in site.data.dataset %}
<div class="row">
<div class="col-sm-11 clearfix">
 <div class="well well-sm">
  <img src="{{ site.url }}{{ site.baseurl }}/images/softwarepic/{{ dtst.image }}" class="img-responsive" width="11%" style="float: left" />
  <p><strong>{{ dtst.title }}</strong><br> 
  {{ dtst.description }}<br>
  {{ "Keywords: "}}<em>{{ dtst.keywords }}</em> 
  {% if dtst.link != 0 %}
      <button type="button" class="btn-xs btn-info" onclick="window.location.href= '{{ dtst.link }}'">
      DATA
      </button> 
  {%- endif %}
  {%- if publicon.project != 0 %}
      <button type="button" class="btn-xs btn-info" onclick="window.location.href= '{{ dtst.project }}'">
      PROJECT
      </button> 
  {% endif %}
  </p>
 </div>
</div>
</div>
{% endfor %}

\
&nbsp;
