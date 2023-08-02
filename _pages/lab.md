---
title: "Lab"
layout: gridlay
excerpt: "Lab"
sitemap: false
permalink: /lab/
---

# Lab

{% for lb in site.data.lab %}
<div class="row">
<div class="col-sm-11 clearfix">
 <div class="well well-sm">
  <img src="{{ site.url }}{{ site.baseurl }}/images/teachingpic/{{ lb }}" class="img-responsive" width="11%" style="float: left" />
  <p><b>{{ lb.title }}</b></p>
  <p>{{ lb.description }}</p><br><br><br>
 </div>
</div>
</div>
{% endfor %}
