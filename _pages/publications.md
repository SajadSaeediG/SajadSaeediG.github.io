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
  <img src="{{ site.url }}{{ site.baseurl }}/images/pubpic/{{ publi.image }}" class="img-responsive" width="12%" style="float: left" />
  <p>{{ publi.title }}</p>
  <p><em>{{ publi.authors }}</em></p>
  <p><strong><a href="{{ publi.link.url }}">{{ publi.link.display }}</a></strong></p>
 </div>
</div>
</div>

{% endif %}
{% endfor %}


## Patents

## Full List of publications

{% for publi in site.data.publist %}

  {{ publi.title }} <br />
  <em>{{ publi.authors }} </em><br /><a href="{{ publi.link.url }}">{{ publi.link.display }}</a>

{% endfor %}
