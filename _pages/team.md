---
title: "Team"
layout: gridlay
excerpt: "Team"
sitemap: false
permalink: /team/
---

# Research Team
<p></p>


{%- assign hqp_number = 0 -%}

**PhD** 
   
{% for phd in site.data.alumni_phd %}
{% assign hqp_number = hqp_number | plus: 1 %}
<div class="row">
<div class="col-sm-11 clearfix">
 <div class="well well-sm">
  {% if phd.url != 0 %}
  <p>{{ "[" }}{{ hqp_number }}{{ '] ' }}<a href="{{ phd.url }}">{{ phd.name }}</a></p>
  {% else %}
  <p>{{ "[" }}{{ hqp_number }}{{ '] ' }}{{ phd.name }}</p>
  {% endif %}
 </div>
</div>
</div>
{% endfor %}


\
&nbsp;


{%- assign hqp_number = 0 -%}

**Master of Applied Science (MASc)** - thesis-based
   
{% for msc in site.data.alumni_msc %}
{% assign hqp_number = hqp_number | plus: 1 %}
<div class="row">
<div class="col-sm-11 clearfix">
 <div class="well well-sm">
  {% if msc.url != 0 %}
  <p>{{ "[" }}{{ hqp_number }}{{ '] ' }}<a href="{{ msc.url }}">{{ msc.name }}</a></p>
  {% else %}
  <p>{{ "[" }}{{ hqp_number }}{{ '] ' }}{{ msc.name }}</p>
  {% endif %}
 </div>
</div>
</div>
{% endfor %}


\
&nbsp;

{%- assign hqp_number = 0 -%}

**Undergraduate Research Assistant (URA)** 
   
{% for bsc in site.data.alumni_bsc %}
{% assign hqp_number = hqp_number | plus: 1 %}
<div class="row">
<div class="col-sm-11 clearfix">
 <div class="well well-sm">
  {% if bsc.url != 0 %}
  <p>{{ "[" }}{{ hqp_number }}{{ '] ' }}<a href="{{ bsc.url }}">{{ bsc.name }}</a></p>
  {% else %}
  <p>{{ "[" }}{{ hqp_number }}{{ '] ' }}{{ bsc.name }}</p>
  {% endif %}
 </div>
</div>
</div>
{% endfor %}



\
&nbsp;



{%- assign hqp_number = 0 -%}

**Capstone Projects - Final Year Undergraduate Projects** 
   
{% for cap in site.data.alumni_capstone %}
{% assign hqp_number = hqp_number | plus: 1 %}
<div class="row">
<div class="col-sm-11 clearfix">
 <div class="well well-sm">
  {% if cap.prlink == 0 %}
  <p>{{ "[" }}{{ hqp_number }}{{ '] ' }}{{ cap.project }}</p>
  {% else %}
  <p>{{ "[" }}{{ hqp_number }}{{ '] ' }}<a href="{{ cap.prlink }}">{{ cap.project }}</a></p>
  {% endif %}  
  <p>
  {% if cap.link1 != 0 %}
  {{ cap.name1 }}
  {% else %}
  <p><a href="{{ cap.link1 }}">{{ cap.name1 }}</a></p>
  {% endif %}
  {{ ', ' }}&nbsp;
  {{ cap.name2 }}
  {{ ', ' }}&nbsp;
  {{ cap.name3 }}
  {{ ', ' }}&nbsp;
  {{ cap.name4 }}
  </p>
  {% if cap.award != 0 %}
  {% if cap.awlik != 0 %}
  <p><a href="{{ cap.awlink }}">{{ cap.award }}</a></p>
  {% else %}
  <p>{{ cap.award }}</p>
  {% endif %}
  {% endif %}
  {% if cap.sponsor != 0 %}
  <p><a href="{{ cap.splink }}">{{ cap.sponsor }}</a></p>
  {% endif %}    
 </div>
</div>
</div>
{% endfor %}

\
&nbsp;

