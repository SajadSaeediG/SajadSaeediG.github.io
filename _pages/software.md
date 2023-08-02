---
title: "Software"
layout: gridlay
excerpt: "Software"
sitemap: false
permalink: /software/
---

# Software

Here is a list of open-source software realeased with the papers

{% for sftwr in site.data.software %}
<div class="row">
<div class="col-sm-11 clearfix">
 <div class="well well-sm">
  <img src="{{ site.url }}{{ site.baseurl }}/images/softwarepic/{{ sftwr.image }}" class="img-responsive" width="11%" style="float: left" />
  <p><b>{{ sftwr.title }}</b></p>
  <p>{{ sftwr.description }}</p><br>
 </div>
</div>
</div>
{% endfor %}
