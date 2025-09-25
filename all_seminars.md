---
layout: single
sidebar: 
  nav: "events"
permalink: /events/all_seminars.html
---
<h1>Bath Applied and Interdisciplinary Mathematics Seminar</h1>
  <p> We hold weekly seminars and one-off events to stimulate research at the interface of mathematics, engineering, physics, biology and other disciplines. The AIMS seminars are hosted by the Department of Mathematics and encompasses many of the applied and interdisciplinary research groups at Bath. This includes the Centre for Nonlinear Mechanics, Centre for Mathematical Biology, Institute for Mathematical Innovation, and so forth. But we also host plenty of talks of interest to Analysts, Numerical Analysts, Engineers, Physicists, and so forth!

AIMS Seminars are held weekly on Tuesdays and hosted by AIMS. All seminars are at 1.15pm in 1W 3.103, University of Bath.</p>

{% assign sorted = site.categories["bnaseminar"]  | sort:"year"  %}

{% for post in sorted %}<a class="btn btn--inverse" style="width: 45%"  href="{{site.url}}{{ site.baseurl }}{{ post.url }}">{{post.excerpt}}</a>{% endfor %}
