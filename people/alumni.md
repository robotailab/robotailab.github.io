---
title: Alumni
permalink: /people/alumni/
---

<section class="py-5">
  <div class="container">
    <div class="row mb-4">
      <div class="col-lg-8">
        <h1>Alumni</h1>
      </div>
    </div>

    {% assign alumni = site.data.people | where: "category", "alumni" %}
    {% if alumni.size == 0 %}
    <div class="alert alert-secondary">Alumni profiles will be added soon.</div>
    {% else %}
    <div class="row g-4">
      {% for person in alumni %}
      <div class="col-md-6 col-lg-4">
        <div class="card h-100">
          <div class="card-body">
            <div class="mb-2">
              <h5 class="mb-0">{{ person.name_en }}</h5>
              <div class="text-muted small">{{ person.role_en }}</div>
            </div>
            <p class="mt-2 mb-0">{{ person.focus_en }}</p>
          </div>
        </div>
      </div>
      {% endfor %}
    </div>
    {% endif %}
  </div>
</section>
