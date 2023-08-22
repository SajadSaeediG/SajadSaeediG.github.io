---
title: "Events"
layout: gridlay
excerpt: "Events"
sitemap: false
permalink: /events/
---

# Events

{% for event in site.data.events %}
<div class="row">
<div class="col-sm-11 clearfix">
 <div class="well well-sm">
  <img src="{{ site.url }}{{ site.baseurl }}/images/teachingpic/{{ event.image }}" class="img-responsive" width="11%" style="float: left" />
  <p><b>{{ event.title }}</b></p>
  <p>{{ event.description }}</p><br>
 </div>
</div>
</div>
{% endfor %}


\
&nbsp;
