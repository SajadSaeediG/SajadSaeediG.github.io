---
title: "Research"
layout: gridlay
excerpt: "Research"
sitemap: false
permalink: /research/
---

# Research
<p></p>

#### Research topics include:
**- Simultaneous Localization and Mapping (SLAM)**

**- Multiple-robot SLAM**

**- Focal-plane Sensor-processor Arrays (FPSP)**

**- Autonomous Mobile Robotics**

**- Aerial Robotics**

**- Marine Robotics**

**- Control Systems**
   
{% for rsch in site.data.research %}
<div class="row">
<div class="col-sm-11 clearfix">
 <div class="well well-sm">
  <img src="{{ site.url }}{{ site.baseurl }}/images/randdpic/{{ rsch.image }}" class="img-responsive" width="11%" style="float: left" />
  <p><b>{{ rsch.title }}</b></p>
  <p>{{ rsch.description }}</p>
 </div>
</div>
</div>
{% endfor %}

\
&nbsp;
