---
title: All Sections
layout: page
permalink: /sections/
---

{% assign sorted_sections = site.sections | sort: 'weight' %}

<ul>
  {% for s in sorted_sections %}
    <li>{{ s.title }}</li>
  {% endfor %}
</ul>
