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
  {%- if msc.url != 0 %}
    <strong><a href="{{ msc.url }}">{{ msc.name }}</a></strong> <br>
  <%else%> 
    <strong><a>{{ msc.name }}</a></strong> <br>    
  {%- endif %}
 </div>
</div>
</div>
{% endfor %}

\
&nbsp;