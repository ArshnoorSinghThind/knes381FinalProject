---
title: All Sections
layout: page
permalink: /sections/
---

<div class="container pt-6 pb-6 pb-md-10">
  <div class="row justify-content-start">
    {% for section in site.sections %}
      <div class="col-12 col-md-4 mb-4">
        <div class="service service-summary">
          <div class="service-content">
            <h2 class="service-title">
              <a href="{{ section.url | relative_url }}">{{ section.title }}</a>
            </h2>
            <p>{{ section.excerpt | markdownify | strip_html | truncate: 100 }}</p>
          </div>
        </div>
      </div>
    {% endfor %}
  </div>
</div>
