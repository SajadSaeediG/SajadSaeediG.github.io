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
  <p>{{ tching.description }}</p>
  {% if tching.lab.url != 0 %}
  <p><a href="{{ tching.lab.url }}">{{ tching.lab.display }}</a></p>
  {% endif %}
 </div>
</div>
</div>
{% endfor %}


\
&nbsp;
