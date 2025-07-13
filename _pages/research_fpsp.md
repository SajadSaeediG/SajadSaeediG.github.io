---
title: "Focal-plane Sensor-processor Arrays (FPSP)"
layout: page
excerpt: "FPSP"
sitemap: false
permalink: /research/fpsp/
---

<p></p>

#### A traditional camera consists of a 2D array of light-sensitive pixels. In contrast, FPSPs integrate a processor within each pixel on the same chip. FPSPs are also referred to as processor-per-pixel arrays (PPA) or cellular-processor arrays (CPA). 

<p></p>

#### Below, you will see some of the applications and advantages of FPSPs. 
   

{%- assign topic = fpsp -%}

{% for publi in site.data.publistjournal %}
{% if publi.topic == topic -%}


<div class="row">
<div class="col-sm-11 clearfix">
 <div class="well well-sm">
  <img src="{{ site.url }}{{ site.baseurl }}/images/pubpic/{{ publi.image }}" class="img-responsive" width="11%" style="float: left" />
  <p>{{ "[" }}{{ pub_number }}{{ '] ' }}{{ publi.title }}  <br> 
  <em>{{ publi.authors }}</em> <br> 
  <strong><a href="{{ publi.link.url }}">{{ publi.link.display }}</a></strong> <br>
  {% if publi.project != 0 %}
      <button type="button" class="btn-xs btn-info" onclick="window.location.href= '{{ publi.project }}'">
      PROJECT
      </button> 
  {%- endif %}
  {%- if publi.video != 0 %}
      <button type="button" class="btn-xs btn-info" onclick="window.location.href= '{{ publi.video }}'">
      VIDEO
      </button> 
  {%- endif %}
  {%- if publi.code != 0 %}
     <button type="button" class="btn-xs btn-info" onclick="window.location.href= '{{ publi.code }}'">
     CODE
     </button> 
  {%- endif %}
  {%- if publi.pdf != 0 %}
     <button type="button" class="btn-xs btn-info" onclick="window.location.href= '{{ site.baseurl }}/downloads/{{ publi.pdf }}'">
     PDF
     </button> 
  {%- endif %}
  {%- if publi.pdflink != 0 %}
      <button type="button" class="btn-xs btn-info" onclick="window.location.href= '{{ publi.pdflink }}'">
      PDF
      </button>
  {% endif %}  
  </p>
 </div>
</div>
</div>

{%- endif %}
{% endfor %}

{% for publicon in site.data.publistconf %}
{% if publicon.topic == topic -%}

<div class="row">
<div class="col-sm-11 clearfix">
<div class="well well-sm">
<img src="{{ site.url }}{{ site.baseurl }}/images/pubpic/{{ publicon.image }}" class="img-responsive" width="11%" style="float: left" />
<p>{{ "[" }}{{ pub_number }}{{ "] " }}{{ publicon.title }} <br> 
<em>{{ publicon.authors }}</em> <br>
<strong><a href="{{ publicon.venuelink }}">{{ publicon.venue }}</a></strong>  
{{ publicon.location }} <br>
{% if publicon.project != 0 %}
<button type="button" class="btn-xs btn-info" onclick="window.location.href= '{{ publicon.project }}'">
PROJECT
</button> 
{%- endif %}
{%- if publicon.video != 0 %}
<button type="button" class="btn-xs btn-info" onclick="window.location.href= '{{ publicon.video }}'">
VIDEO
</button> 
{%- endif %}
{%- if publicon.code != 0 %}
<button type="button" class="btn-xs btn-info" onclick="window.location.href= '{{ publicon.code }}'">
CODE
</button> 
{%- endif %}
{%- if publicon.codedown != 0 %}
<button type="button" class="btn-xs btn-info" onclick="window.location.href= '{{ site.baseurl }}/downloads/{{ publicon.codedown }}'">
CODE
</button> 
{%- endif %} 
{%- if publicon.pdf != 0 %}
<button type="button" class="btn-xs btn-info" onclick="window.location.href= '{{ site.baseurl }}/downloads/{{ publicon.pdf }}'">
PDF
</button>
{%- endif %}
{%- if publicon.pdflink != 0 %}
<button type="button" class="btn-xs btn-info" onclick="window.location.href= '{{ publicon.pdflink }}'">
PDF
</button>
{%- endif %}
{%- if publicon.thesislink != 0 %}
<button type="button" class="btn-xs btn-info" onclick="window.location.href= '{{ publicon.thesislink }}'">
THESIS
</button>
{%- endif %}  
{%- if publicon.slides != 0 %}
<button type="button" class="btn-xs btn-info" onclick="window.location.href= '{{ site.baseurl }}/downloads/{{ publicon.slides }}'">
SLIDES
</button>
{%- endif %}  
{%- if publicon.note != 0 %}
<button type="button" class="btn-xs btn-success" >
{{ publicon.note }}
</button>
{% endif %}    
</p>
</div>
</div>
</div>


{%- endif %}    
{% endfor %}

\
&nbsp;
