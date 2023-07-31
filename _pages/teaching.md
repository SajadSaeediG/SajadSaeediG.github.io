---
title: "Teaching"
layout: gridlay
excerpt: "Teaching"
sitemap: false
permalink: /teaching/
---

# Teaching

{% for tching in site.data.teaching %}
<div class="row">
<div class="col-sm-11 clearfix">
 <div class="well well-sm">
  <img src="{{ site.url }}{{ site.baseurl }}/images/teachingpic/{{ tching.image }}" class="img-responsive" width="11%" style="float: left" />
  <p><b>{{ tching.title }}</b></p>
  <p>{{ tching.description }}</p><br>
 </div>
</div>
</div>
{% endfor %}
