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
<div class="row">
<div class="col-sm-11 clearfix">
 <div class="well well-sm">
  <img src="{{ site.url }}{{ site.baseurl }}/images/pubpic/{{ conf.png }}" class="img-responsive" width="11%" style="float: left" />
  <p>{{ Optical Guide Assembly and System Including Same }}</p>
  <p><em>{{ Jason G. Gillham, Christopher A Gilson, Sajad Saeedi, Shawn O. Satchell }}</em></p>
  <p>{{ United States Patent and Trademark Office, 2017 }}</p>
  <p><strong><a href="{{ https://patents.google.com/patent/US20190017941A1/en }}">{{ US20190017941A1 }}</a></strong></p>
 </div>
</div>
</div>


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
  <p>{{ publicon.title }}</p>
  <p><em>{{ publicon.authors }}</em></p>
  <p>{{ publicon.venue }}</p>
  <p>{{ publicon.location }}</p>
 </div>
</div>
</div>
{% endfor %}

## PhD Thesis
<div class="row">
<div class="col-sm-11 clearfix">
 <div class="well well-sm">
  <img src="{{ site.url }}{{ site.baseurl }}/images/pubpic/{{ conf.png }}" class="img-responsive" width="11%" style="float: left" />
  <p>{{ Multiple-robot Simultaneous Localization and Mapping }}</p>
  <p><em>{{ Sajad Saeedi }}</em></p>
  <p>{{ University of New Brunswick, 2014 }}</p>
 </div>
</div>
</div>
