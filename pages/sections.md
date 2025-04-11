---
title: All Sections
layout: page
permalink: /sections/
---

<h1>All Sections</h1>

<div class="row">
  {% assign sorted_sections = site.sections | sort: "weight" %}
  {% for section in sorted_sections %}
    <div class="col-12 col-md-6 mb-4">
      <h2><a href="{{ section.url | relative_url }}">{{ section.title }}</a></h2>
      <p>{{ section.excerpt }}</p>
    </div>
  {% endfor %}
</div>
