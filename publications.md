---
title: Publications
permalink: /publications/
---

<section class="py-5">
  <div class="container">
    <div class="row mb-4">
      <div class="col-12">
        <h1>Publications</h1>
        <p class="text-muted mb-2">A collection of journal articles, conference papers, and other publications from the Robotics &amp; A.I. Lab.</p>
        <div class="d-flex flex-wrap flex-lg-nowrap gap-2 mt-2">
          {% for section in site.data.publications %}
          <a class="btn btn-outline-dark btn-sm fs-6 px-3 fw-semibold text-center" data-theme-btn="outline" href="#{{ section.id }}">{{ section.title }}</a>
          {% endfor %}
        </div>
      </div>
    </div>

    {% for section in site.data.publications %}
    <div class="mb-5" style="margin-bottom: 3rem;">
      <h2 class="h4 mb-3 pub-section-title" id="{{ section.id }}">{{ section.title }}</h2>
      {% assign items = section.items %}
      {% if items.size > 0 %}
      <ol class="mb-0 pub-list" style="--pub-count: {{ items.size | plus: 1 }};">
        {% for pub in items %}
        <li class="mb-2">{{ pub.text }}</li>
        {% endfor %}
      </ol>
      {% endif %}
    </div>
    {% endfor %}
  </div>
</section>
