---
title: Students
permalink: /people/students/
---

<section class="py-5">
  <div class="container">
    <div class="row mb-4">
      <div class="col-lg-8">
        <h1>Students</h1>
      </div>
    </div>

    {% assign students = site.data.people | where: "category", "students" %}
    {% assign grad = students | where: "level", "graduate" %}
    {% assign grad_main = grad | where: "section", "main" %}
    {% assign grad_aff = grad | where: "section", "affiliated" %}
    {% assign undergrad = students | where: "level", "undergraduate" %}

    <h2 class="h5 mb-3">Graduate Students</h2>
    <div class="row g-4 mb-4">
      {% for person in grad_main %}
      <div class="col-md-6 col-lg-4">
        <div class="card h-100">
          <div class="card-body">
            <div class="d-flex align-items-start gap-3 mb-3">
              {% if person.image %}
              <img class="img-fluid" src="{{ person.image }}" alt="Profile photo" style="width: 120px; height: 160px; object-fit: contain;">
              {% endif %}
              <div>
                <h5 class="mb-0">{{ person.name_en }}</h5>
                <div class="text-muted small">{{ person.role_en }}</div>
              </div>
            </div>
            <p class="mt-2 mb-2">{{ person.focus_en }}</p>
            {% if person.dept_en %}
            <div class="text-muted small mb-2">{{ person.dept_en }}</div>
            {% endif %}
            {% if person.email %}
            <div class="small text-muted">E-mail: {{ person.email }}</div>
            {% endif %}
          </div>
        </div>
      </div>
      {% endfor %}
      {% if grad_main.size == 0 %}
      <div class="col-12">
        <div class="alert alert-secondary">Graduate student profiles will be added soon.</div>
      </div>
      {% endif %}
    </div>

    <h2 class="h5 mb-3">Graduate Students (Affiliated)</h2>
    <div class="row g-4 mb-4">
      {% for person in grad_aff %}
      <div class="col-md-6 col-lg-4">
        <div class="card h-100">
          <div class="card-body">
            <div class="mb-2">
              <h5 class="mb-0">{{ person.name_en }}</h5>
              <div class="text-muted small">{{ person.role_en }}</div>
            </div>
            {% if person.focus_en %}
            <p class="mt-2 mb-2">{{ person.focus_en }}</p>
            {% endif %}
            {% if person.dept_en %}
            <div class="text-muted small mb-2">{{ person.dept_en }}</div>
            {% endif %}
            {% if person.email %}
            <div class="small text-muted">E-mail: {{ person.email }}</div>
            {% endif %}
          </div>
        </div>
      </div>
      {% endfor %}
      {% if grad_aff.size == 0 %}
      <div class="col-12">
        <div class="alert alert-secondary">Affiliated graduate profiles will be added soon.</div>
      </div>
      {% endif %}
    </div>

    <h2 class="h5 mb-3">Undergraduate Researchers</h2>
    <div class="row g-4">
      {% for person in undergrad %}
      <div class="col-md-6 col-lg-4">
        <div class="card h-100">
          <div class="card-body">
            <div class="mb-2">
              <h5 class="mb-0">{{ person.name_en }}</h5>
            </div>
            <p class="text-muted small mb-2">{{ person.focus_en }}</p>
            {% if person.period %}
            <div class="small mb-3">{{ person.period }}</div>
            {% endif %}
            {% if person.email %}
            <div class="small text-muted">E-mail: {{ person.email }}</div>
            {% endif %}
          </div>
        </div>
      </div>
      {% endfor %}
      {% if undergrad.size == 0 %}
      <div class="col-12">
        <div class="alert alert-secondary">Undergraduate researcher profiles will be added soon.</div>
      </div>
      {% endif %}
    </div>
  </div>
</section>
