---
title: "Focal-plane Sensor-processor Arrays (FPSP)"
layout: gridlay
excerpt: "FPSP"
sitemap: false
permalink: /research/fpsp/
---

## Focal-plane Sensor-processor Arrays (FPSP)

<p></p>
<h4 class="custom-highlight">What is Focal-plane Sensor-processor Arrays (FPSP)?</h4>  
<p>A traditional camera consists of a 2D array of light-sensitive pixels. In contrast, FPSPs integrate a processor within each pixel on the same chip. FPSPs are also referred to as processor-per-pixel arrays (PPA) or cellular-processor arrays (CPA).</p> 
<img src="{{ site.url }}{{ site.baseurl }}/images/pubpic/debrunner_taco_2019.png" 
     class="img-responsive" 
     style="display: block; margin-left: auto; margin-right: auto; width: 25%;" />

<h4 class="custom-highlight">Why use FPSPs instead of traditional image sensors?</h4>

<p>FPSPs offer unique advantages over traditional image sensors and vision systems by embedding computation directly into the image sensor array. Here are the main benefits:</p>

<ul>
  <li><strong>Low Latency:</strong> Processing happens directly at the pixel level, enabling ultra-fast response times.</li>
  <li><strong>Low Power Consumption:</strong> By eliminating the need to transfer raw data to a central processor, FPSPs significantly reduce power usage.</li>
  <li><strong>High Parallelism:</strong> Each pixel includes its own processor, allowing massively parallel computation ideal for tasks like edge detection, optical flow, and motion tracking.</li>
  <li><strong>Reduced Bandwidth Requirements:</strong> Since processing is done locally, only the results—not the full image—need to be transmitted, minimizing data load.</li>
  <li><strong>Compact System Design:</strong> Combining sensing and processing on a single chip reduces the need for additional hardware and simplifies the overall system architecture.</li>
  <li><strong>Real-Time Performance:</strong> Ideal for time-sensitive applications such as robotics, drones, and mobile devices where low-latency processing is critical.</li>
</ul>



<h4 class="custom-highlight">What are the challenges of working with FPSPs?</h4>

<p>While FPSPs offer powerful advantages, they also present unique challenges that researchers and engineers must overcome:</p>

<ul>
  <li><strong>Limited On-Chip Memory:</strong> Each pixel has minimal storage, which restricts the complexity of algorithms that can be executed locally.</li>
  <li><strong>Programming Complexity:</strong> Developing code for massively parallel pixel arrays requires specialized knowledge and tools not common in traditional image processing workflows.</li>
  <li><strong>Hardware Constraints:</strong> Most FPSPs operate with low-resolution grayscale output and limited dynamic range compared to conventional image sensors.</li>
  <li><strong>Lack of Standardization:</strong> Few commercial platforms are available, and tools are often custom or experimental, making development and deployment harder.</li>
  <li><strong>Data Extraction Bottlenecks:</strong> Although local processing reduces bandwidth, extracting intermediate data from the chip can still be challenging and slow.</li>
  <li><strong>Debugging and Visualization:</strong> The parallel nature of computation makes it difficult to monitor or debug pixel-level operations in real-time.</li>
</ul>



<h4 class="custom-highlight">How are FPSPs different from event cameras?</h4>

<p>While both FPSPs and event cameras aim to overcome limitations of traditional frame-based vision sensors, they differ significantly in operation and purpose:</p>

<ul>
  <li><strong>Data Representation:</strong>  
    <ul>
      <li><strong>FPSPs:</strong> Process full image frames directly on the sensor by performing computations at each pixel.</li>
      <li><strong>Event Cameras:</strong> Only output asynchronous "events" when changes in brightness occur at individual pixels.</li>
    </ul>
  </li>
  
  <li><strong>Output Type:</strong>  
    <ul>
      <li><strong>FPSPs:</strong> Can output processed results (e.g. edge maps, motion vectors) instead of raw frames.</li>
      <li><strong>Event Cameras:</strong> Produce a continuous stream of timestamped events rather than full frames.</li>
    </ul>
  </li>
  
  <li><strong>Latency and Speed:</strong>  
    <ul>
      <li><strong>FPSPs:</strong> Achieve low latency by processing data in parallel across the pixel array.</li>
      <li><strong>Event Cameras:</strong> Have extremely low latency, reacting to changes in microseconds due to their asynchronous nature.</li>
    </ul>
  </li>

  <li><strong>Suitability:</strong>  
    <ul>
      <li><strong>FPSPs:</strong> Well-suited for low-power, frame-based processing with programmable in-sensor computing.</li>
      <li><strong>Event Cameras:</strong> Best for high-speed motion detection, low-light conditions, and sparse data processing.</li>
    </ul>
  </li>
<ul>


<p></p>
<h4 class="custom-highlight">Are there any existing hardware implementations of FPSPs?</h4>  
<p>One notable example is <a href="https://personalpages.manchester.ac.uk/staff/p.dudek/scamp/default.htm" target="_blank">SCAMP5</a>, an FPSP designed and developed by Dr. Piotr Dudek and his team at the University of Manchester. Below are some key applications and advantages of Focal-Plane Sensor-Processors (FPSPs), demonstrated using the SCAMP5 device.</p>  
<img src="{{ site.url }}{{ site.baseurl }}/images/pubpic/debrunner_hipeac_2019_auke.png" 
     class="img-responsive" 
     style="display: block; margin-left: auto; margin-right: auto; width: 25%;" />
  

{%- assign pub_number = 0 -%}
{%- assign lower_limit_yr = 2015 -%}
{%- assign upper_limit_yr = 2024 -%}

{% for year in (lower_limit_yr..upper_limit_yr) reversed %}

{% if 2008 == year or 2007 == year -%}
{% continue %}
{% endif %}

<!--
<h4  style="color:  #0000FF;">
  {{ year }}
</h4>
-->

{% for publi in site.data.publistjournal %}
{% if publi.year == year -%}
{% if publi.topic == "fpsp" -%}
{% assign pub_number = pub_number | plus: 1 %}

<p class="custom-highlight">{{  }}</p>
<p class="custom-highlight">{{  }}</p>
<p class="custom-highlight">{{  }}</p>
<div class="row">
<div class="col-sm-11 clearfix">
 <div class="well well-sm">
  <strong class="custom-highlight">{{ publi.highlight }}</strong>  
  <img src="{{ site.url }}{{ site.baseurl }}/images/pubpic/{{ publi.image }}" class="img-responsive" width="11%" style="float: left" />
  <p>{{ "[" }}{{ pub_number }}{{ '] ' }}{{ publi.title }}  <br> 
  <em>{{ publi.authors }}</em> <br> 
  <strong><a href="{{ publi.link.url }}">{{ publi.link.display }}</a></strong> <br>
  {% if publi.project != 0 %}
      <button type="button" class="btn-xs btn-info" onclick="window.location.href= '{{ publi.project }}'">
      PROJECT
      </button> 
  {%- endif %}
  {%- if publi.video != 0 %}
      <button type="button" class="btn-xs btn-info" onclick="window.location.href= '{{ publi.video }}'">
      VIDEO
      </button> 
  {%- endif %}
  {%- if publi.code != 0 %}
     <button type="button" class="btn-xs btn-info" onclick="window.location.href= '{{ publi.code }}'">
     CODE
     </button> 
  {%- endif %}
  {%- if publi.pdf != 0 %}
     <button type="button" class="btn-xs btn-info" onclick="window.location.href= '{{ site.baseurl }}/downloads/{{ publi.pdf }}'">
     PDF
     </button> 
  {%- endif %}
  {%- if publi.pdflink != 0 %}
      <button type="button" class="btn-xs btn-info" onclick="window.location.href= '{{ publi.pdflink }}'">
      PDF
      </button>
  {% endif %}  
  </p>
 </div>
</div>
</div>

{%- endif %}
{%- endif %}
{% endfor %}

{% for publicon in site.data.publistconf %}
{% if publicon.year == year -%}
{% if publicon.topic == "fpsp" -%}
{% assign pub_number = pub_number | plus: 1 %}

<p class="custom-highlight">{{  }}</p>
<p class="custom-highlight">{{  }}</p>
<p class="custom-highlight">{{  }}</p>
<div class="row">
<div class="col-sm-11 clearfix">
<div class="well well-sm">
<strong class="custom-highlight">{{ publicon.highlight }}</strong>    
<img src="{{ site.url }}{{ site.baseurl }}/images/pubpic/{{ publicon.image }}" class="img-responsive" width="11%" style="float: left" />
<p>{{ "[" }}{{ pub_number }}{{ "] " }}{{ publicon.title }} <br> 
<em>{{ publicon.authors }}</em> <br>
<strong><a href="{{ publicon.venuelink }}">{{ publicon.venue }}</a></strong>  
{{ publicon.location }} <br>
{% if publicon.project != 0 %}
<button type="button" class="btn-xs btn-info" onclick="window.location.href= '{{ publicon.project }}'">
PROJECT
</button> 
{%- endif %}
{%- if publicon.video != 0 %}
<button type="button" class="btn-xs btn-info" onclick="window.location.href= '{{ publicon.video }}'">
VIDEO
</button> 
{%- endif %}
{%- if publicon.code != 0 %}
<button type="button" class="btn-xs btn-info" onclick="window.location.href= '{{ publicon.code }}'">
CODE
</button> 
{%- endif %}
{%- if publicon.codedown != 0 %}
<button type="button" class="btn-xs btn-info" onclick="window.location.href= '{{ site.baseurl }}/downloads/{{ publicon.codedown }}'">
CODE
</button> 
{%- endif %} 
{%- if publicon.pdf != 0 %}
<button type="button" class="btn-xs btn-info" onclick="window.location.href= '{{ site.baseurl }}/downloads/{{ publicon.pdf }}'">
PDF
</button>
{%- endif %}
{%- if publicon.pdflink != 0 %}
<button type="button" class="btn-xs btn-info" onclick="window.location.href= '{{ publicon.pdflink }}'">
PDF
</button>
{%- endif %}
{%- if publicon.thesislink != 0 %}
<button type="button" class="btn-xs btn-info" onclick="window.location.href= '{{ publicon.thesislink }}'">
THESIS
</button>
{%- endif %}  
{%- if publicon.slides != 0 %}
<button type="button" class="btn-xs btn-info" onclick="window.location.href= '{{ site.baseurl }}/downloads/{{ publicon.slides }}'">
SLIDES
</button>
{%- endif %}  
{%- if publicon.note != 0 %}
<button type="button" class="btn-xs btn-success" >
{{ publicon.note }}
</button>
{% endif %}    
</p>
</div>
</div>
</div>

{%- endif %}
{%- endif %}    
{% endfor %}

{%- endfor %}

\
&nbsp;
