---
title: Equipment
permalink: /equipment/
---

<section class="py-5">
  <div class="container">
    <div class="row mb-4">
      <div class="col-lg-8">
        <h1>Equipment</h1>
        <p class="text-muted">Robots, sensors, and other research equipment.</p>
      </div>
    </div>

    <div class="row g-4">
      <div class="col-12">
        <div class="card h-100">
          <div class="card-body">
            <div class="d-flex flex-wrap align-items-center justify-content-between gap-2 mb-3">
              <h2 class="h5 mb-0">Robots</h2>
            </div>
            {% assign robots = site.data.equipment.robots %}
            <div class="row g-3">
              {% for robot in robots %}
              <div class="col-sm-6 col-lg-3">
                <div class="card h-100">
                  <div class="card-body pb-2">
                    <div class="d-flex flex-wrap align-items-center gap-2">
                      {% if robot.maker %}
                      <span class="badge text-bg-dark equipment-title-badge">{{ robot.maker }}</span>
                      {% endif %}
                      {% if robot.model %}
                      <span class="badge text-bg-dark equipment-title-badge">{{ robot.model }}</span>
                      {% else %}
                      <span class="badge text-bg-dark equipment-title-badge">{{ robot.name }}</span>
                      {% endif %}
                      <span class="badge text-bg-dark equipment-title-badge">{{ robot.year_label }}</span>
                    </div>
                  </div>
                  <img class="card-img-top equipment-img" src="{{ robot.image }}" alt="{{ robot.alt }}">
                  {% if robot.tags and robot.tags.size > 0 %}
                  <div class="card-body pt-2">
                    <div class="d-flex flex-wrap gap-2 mt-2">
                      {% for tag in robot.tags %}
                      <span class="badge text-bg-secondary">{{ tag }}</span>
                      {% endfor %}
                    </div>
                  </div>
                  {% endif %}
                </div>
              </div>
              {% endfor %}
            </div>
          </div>
        </div>
      </div>
      <div class="col-12">
        <div class="card h-100">
          <div class="card-body">
            <h2 class="h5">Sensors</h2>
            {% assign sensors = site.data.equipment.sensors %}
            <div class="row g-3 mt-2">
              {% for sensor in sensors %}
              <div class="col-sm-6 col-lg-3">
                <div class="card h-100">
                  <div class="card-body pb-2">
                    <div class="d-flex flex-wrap align-items-center gap-2">
                      {% if sensor.maker %}
                      <span class="badge text-bg-dark equipment-title-badge">{{ sensor.maker }}</span>
                      {% endif %}
                      {% if sensor.model %}
                      <span class="badge text-bg-dark equipment-title-badge">{{ sensor.model }}</span>
                      {% else %}
                      <span class="badge text-bg-dark equipment-title-badge">{{ sensor.name }}</span>
                      {% endif %}
                      <span class="badge text-bg-dark equipment-title-badge">{{ sensor.year_label }}</span>
                    </div>
                  </div>
                  <img class="card-img-top equipment-img" src="{{ sensor.image }}" alt="{{ sensor.alt }}">
                  {% if sensor.tags and sensor.tags.size > 0 %}
                  <div class="card-body pt-2">
                    <div class="d-flex flex-wrap gap-2 mt-2">
                      {% for tag in sensor.tags %}
                      <span class="badge text-bg-secondary">{{ tag }}</span>
                      {% endfor %}
                    </div>
                  </div>
                  {% endif %}
                </div>
              </div>
              {% endfor %}
            </div>
          </div>
        </div>
      </div>
      <div class="col-12">
        <div class="card h-100">
          <div class="card-body">
            <h2 class="h5">Other Equipment</h2>
            {% assign others = site.data.equipment.other_equipment %}
            <div class="row g-3 mt-2">
              {% for item in others %}
              <div class="col-sm-6 col-lg-3">
                <div class="card h-100">
                  <div class="card-body pb-2">
                    <div class="d-flex flex-wrap align-items-center gap-2">
                      {% if item.maker %}
                      <span class="badge text-bg-dark equipment-title-badge">{{ item.maker }}</span>
                      {% endif %}
                      {% if item.model %}
                      <span class="badge text-bg-dark equipment-title-badge">{{ item.model }}</span>
                      {% else %}
                      <span class="badge text-bg-dark equipment-title-badge">{{ item.name }}</span>
                      {% endif %}
                      <span class="badge text-bg-dark equipment-title-badge">{{ item.year_label }}</span>
                    </div>
                  </div>
                  <img class="card-img-top equipment-img" src="{{ item.image }}" alt="{{ item.alt }}">
                  {% if item.tags and item.tags.size > 0 %}
                  <div class="card-body pt-2">
                    <div class="d-flex flex-wrap gap-2 mt-2">
                      {% for tag in item.tags %}
                      <span class="badge text-bg-secondary">{{ tag }}</span>
                      {% endfor %}
                    </div>
                  </div>
                  {% endif %}
                </div>
              </div>
              {% endfor %}
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</section>
