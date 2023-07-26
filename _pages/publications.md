---
title: "Publications"
layout: gridlay
excerpt: "Publications."
sitemap: false
permalink: /publications/
---


## Journal Publications
{% for publi in site.data.publist %}
{% if publi.highlight == 1 %}
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
{% endif %}
{% endfor %}

## Patents

## ​Book Chapters

## Conference Publications
{% for publi in site.data.publist-conf %}
{% if publi.highlight == 1 %}
<div class="row">
<div class="col-sm-11 clearfix">
 <div class="well well-sm">
  <img src="{{ site.url }}{{ site.baseurl }}/images/pubpic/{{ publi.image }}" class="img-responsive" width="11%" style="float: left" />
  <p>{{ publi.title }}</p>
  <p><em>{{ publi.authors }}</em></p>
  <p>{{ publi.venue }}</p>
  <p>{{ publi.location }}</p>
 </div>
</div>
</div>
{% endif %}
{% endfor %}

## PhD Thesis


