---
title: Courses
permalink: /courses/
---

<section class="py-5">
  <div class="container">
    <div class="row mb-4">
      <div class="col-lg-8">
        <h1>Courses</h1>
        <p class="text-muted">List of Recent Courses</p>
      </div>
    </div>

    <div class="row g-4">
      {% for semester in site.data.courses %}
      {% if semester.visible != false %}
      <div class="col-12">
        <div class="card">
          <div class="card-body">
            <h2 class="h5 mb-3">{{ semester.term }}</h2>
            <ul class="mb-0">
              {% for course in semester.courses %}
              <li class="d-flex align-items-center gap-2">
                <strong class="me-auto">{{ course.title }}</strong>
                {% if course.level == "Graduate" %}
                <span class="badge course-badge text-bg-dark rounded-pill ms-1 course-badge-graduate">Graduate</span>
                {% elsif course.level == "Undergraduate" %}
                <span class="badge course-badge text-bg-secondary rounded-pill ms-1">Undergraduate</span>
                {% else %}
                <span class="badge course-badge text-bg-secondary rounded-pill ms-1">{{ course.level }}</span>
                {% endif %}
              </li>
              {% endfor %}
            </ul>
          </div>
        </div>
      </div>
      {% endif %}
      {% endfor %}
    </div>

  </div>
</section>
