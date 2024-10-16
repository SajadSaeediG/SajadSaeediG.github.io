---
title: "Publications"
layout: gridlay
excerpt: "Publications."
sitemap: false
permalink: /publications/
---
## Journal and Conference Publications

{%- assign pub_number = 0 -%}
{%- assign lower_limit_yr = 2005 -%}
{%- assign upper_limit_yr = 2024 -%}

{% for year in (lower_limit_yr..upper_limit_yr) reversed %}

{% if 2008 == year or 2007 == year -%}
{% continue %}
{% endif %}
<h4  style="color:  #0000FF;">
  {{ year }}
</h4>

{% for publi in site.data.publistjournal %}
{% if publi.year == year -%}
{% assign pub_number = pub_number | plus: 1 %}

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
{% if publicon.year == year -%}
{% assign pub_number = pub_number | plus: 1 %}

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
{%- endfor %}

<!--
## Journal Publications
{% for publi in site.data.publistjournal %}

<div class="row">
<div class="col-sm-11 clearfix">
 <div class="well well-sm">
  <img src="{{ site.url }}{{ site.baseurl }}/images/pubpic/{{ publi.image }}" class="img-responsive" width="11%" style="float: left" />
  <p>{{ publi.title }}  <br> 
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
  {{ publicon.location }}
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
  {%- if publicon.slides != 0 %}
      <button type="button" class="btn-xs btn-info" onclick="window.location.href= '{{ site.baseurl }}/downloads/{{ publicon.slides }}'">
      SLIDES
      </button>
   {% endif %}    
  </p>
 </div>
</div>
</div>
{% endfor %}
--->
## Patents
{% for publi in site.data.publistpatent %}
<div class="row">
<div class="col-sm-11 clearfix">
 <div class="well well-sm">
  <img src="{{ site.url }}{{ site.baseurl }}/images/pubpic/{{ publi.image }}" class="img-responsive" width="11%" style="float: left" />
  <p>{{ publi.title }}</p>
  <p><em>{{ publi.authors }}</em></p>
  <p><strong><a href="{{ publi.link.url }}">{{ publi.link.display }}</a></strong></p><br>
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
  <p><strong><a href="{{ publi.link.url }}">{{ publi.link.display }}</a></strong></p><br>
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
  <p>{{ publicon.venue }}
    {% if publicon.pdf != 0 %}
      <button type="button" class="btn-xs btn-info" onclick="window.location.href= '{{ site.baseurl }}/downloads/{{ publicon.pdf }}'">
      PDF
      </button>
  {% endif %}</p>
 </div>
</div>
</div>
{% endfor %}

\
&nbsp;
