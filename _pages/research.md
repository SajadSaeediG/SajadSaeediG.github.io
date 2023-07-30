---
title: "Research"
layout: gridlay
excerpt: "Research"
sitemap: false
permalink: /research/
---

# Research

{% for rsch in site.data.research %}
<div class="row">
<div class="col-sm-11 clearfix">
 <div class="well well-sm">
  <img src="{{ site.url }}{{ site.baseurl }}/images/researchpic/{{ rsch.image }}" class="img-responsive" width="11%" style="float: left" />
  <p>{{ rsch.title }}</p>
  <p><em>{{ rsch.description }}</em></p>
 </div>
</div>
</div>
{% endfor %}

