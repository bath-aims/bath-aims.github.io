---
title: Full Members
layout: single
sidebar: 
  nav: "people"
permalink: /people/
classes: wide
---

<ul class="member-grid">
  {% assign sorted = site.members | sort: 'last'  %}
  {% for member in sorted %}
    {% unless member.listed == false %}
    {% unless member.membership == "associate" %}
    <li >
      <div class="row">
        <div class="column1">
           <a href="{{ member.homepage }}">
           <img  src="/assets/pics/{{member.pic}} " id="two_col_img"/></a>
        </div>
        <div class="column2">
        <a class="btn btn--inverse" href="{{ member.homepage }}"> {{member.given}} {{ member.last}} </a>
        <p class="small">{{ member.research }}</p>
       </div>
      </div>
    </li>
    {% endunless %}
    {% endunless %}
  {% endfor %}
</ul>

# Associate Members

<ul class="member-grid">
  {% for member in sorted %}
    {% unless member.listed == false %}
    {% if member.membership == "associate" %}
    <li >
      <div class="row">
        <div class="column1">
           <a href="{{ member.homepage }}">
           <img  src="/assets/pics/{{member.pic}} " id="two_col_img"/></a>
        </div>
        <div class="column2">
        <a class="btn btn--inverse" href="{{ member.homepage }}"> {{member.given}} {{ member.last}} </a>
        <p class="small">{{ member.research }}</p>
       </div>
      </div>
    </li>
    {% endif %}
    {% endunless %}
  {% endfor %}
</ul>
