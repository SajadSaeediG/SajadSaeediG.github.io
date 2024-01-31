---
title: "Team"
layout: gridlay
excerpt: "Team"
sitemap: false
permalink: /team/
---

# Research Team
<p></p>

**Master of Applied Science (MASc)** - thesis-based
   
{% for msc in site.data.alumni_msc %}
<div class="row">
<div class="col-sm-11 clearfix">
 <div class="well well-sm">
 <strong><a href="{{ msc.url }}">{{ msc.name }}</a></strong> <br>
 </div>
</div>
</div>
{% endfor %}

\
&nbsp;