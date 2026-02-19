---
title: Research
permalink: /research/
---

<section class="py-5">
  <div class="container">
    <div class="row mb-4">
      <div class="col-lg-8">
        <h1>Research</h1>
        <p class="text-muted research-intro">Our lab focuses on robotics, AI, and intelligent systems that enable robust, autonomous operation in complex real-world environments.</p>
      </div>
    </div>

    <div class="row g-4">
      {% for item in site.data.research %}
      {% assign detail_id = "researchDetail" | append: forloop.index %}
      <div class="col-md-6 col-lg-4">
        <div class="card h-100" role="button" tabindex="0" style="cursor: pointer;" data-bs-toggle="collapse" data-bs-target="#{{ detail_id }}" aria-expanded="false" aria-controls="{{ detail_id }}">
          <img class="card-img-top p-2" src="{{ item.image }}" alt="{{ item.image_alt }}" style="height: 400px; object-fit: contain;">
          <div class="card-body">
            <h2 class="h5">{{ item.title }}</h2>
            <p class="text-muted mb-2">{{ item.summary }}</p>
            <div class="collapse" id="{{ detail_id }}">
              <p class="small mb-0">{{ item.details }}</p>
            </div>
          </div>
        </div>
      </div>
      {% endfor %}
    </div>
  </div>
</section>
