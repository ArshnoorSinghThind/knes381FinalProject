---
title: All Sections
layout: page
permalink: /sections/
---

Total sections: {{ site.sections | size }}

{% for s in site.sections %}
- {{ s.title }}
{% endfor %}

<div class="container pt-6 pb-6 pb-md-10">
  <div class="row justify-content-start">
    {% for section in site.sections %}
      <div class="col-12 col-md-4 mb-4">
        <div class="section section-summary">
          <div class="section-content">
            <h2 class="section-title">
              <a href="{{ section.url | relative_url }}">{{ section.title }}</a>
            </h2>
            <p>{{ section.excerpt | markdownify | strip_html | truncate: 100 }}</p>
          </div>
        </div>
      </div>
    {% endfor %}
  </div>
</div>
