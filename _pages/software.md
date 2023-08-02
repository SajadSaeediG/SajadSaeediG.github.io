---
title: "Software"
layout: gridlay
excerpt: "Software"
sitemap: false
permalink: /software/
---

# Software

Here is a list of open-source software released with the papers

{% for sftwr in site.data.software %}
<div class="row">
<div class="col-sm-11 clearfix">
 <div class="well well-sm">
  <img src="{{ site.url }}{{ site.baseurl }}/images/softwarepic/{{ sftwr.image }}" class="img-responsive" width="11%" style="float: left" />
  <p><strong>{{ sftwr.title }}</strong><br> 
  {{ sftwr.description }}<br>
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


# Dataset

Here is a list of open-source dataset released with the papers


