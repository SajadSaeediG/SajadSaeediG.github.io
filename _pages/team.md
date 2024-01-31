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


**Master of Applied Science (MASc)** - thesis-based
   
{% for msc in site.data.alumni_msc %}
{% assign hqp_number = hqp_number | plus: 1 %}
<div class="row">
<div class="col-sm-11 clearfix">
 <div class="well well-sm">
  <p><a href="{{ msc.link }}">{{ msc.name }}</a></p>
  <p><b>{{ "[" }}{{ hqp_number }}{{ '] ' }}{{ msc.name }}</b></p>
 </div>
</div>
</div>
{% endfor %}

\
&nbsp;