---
title: Home
---

<section class="py-5 border-bottom">
  <div class="container">
    <div class="row align-items-stretch gy-4">
      <div class="col-lg-7">
        <span class="badge text-bg-secondary fs-5">Kwangwoon University</span>
        <h1 class="display-4 mt-3">Robotics &amp; A.I. Lab.</h1>
        <p class="lead text-muted">We conduct foundational and applied research in robotics to enable reliable autonomy in complex, dynamic environments.</p>
        <div class="d-flex flex-wrap gap-3 mt-4">
          <a class="btn btn-outline-dark btn-lg" data-theme-btn="outline" href="/people/">Meet the Team</a>
          <a class="btn btn-outline-dark btn-lg" data-theme-btn="outline" href="/research/">Research</a>
        </div>
      </div>
      <div class="col-lg-5">
        <div class="h-100">
          <img class="hero-img rounded" src="/assets/img/hero.jpg" alt="Robotics research sample">
        </div>
      </div>
    </div>
  </div>
</section>

<section class="py-4 border-bottom">
  <div class="container">
    <div class="d-flex align-items-center justify-content-between mb-3">
      <h2 class="h4 mb-0">Research Highlights</h2>
      <a class="btn btn-outline-secondary btn-sm" href="/publications/">All Publications</a>
    </div>
    <div class="row g-4">
      <div class="col-lg-4">
        <div class="card h-100">
          <div class="card-body">
            <span class="badge text-bg-dark mb-2">Featured</span>
            <img class="img-fluid rounded mb-3 highlight-img" src="/assets/img/ij28.png" alt="Prediction-conditioned reachability framework for safe crowd navigation">
            <h2 class="h5">Uncertainty-calibrated Hamilton-Jacobi value learning for safe crowd navigation</h2>
            <p class="text-muted">We combine pedestrian prediction, learned Hamilton-Jacobi reachability, and conformal uncertainty calibration within MPC to enable efficient and reliable navigation in dense and out-of-distribution crowds.</p>
            <div class="d-flex flex-wrap gap-2 mb-3">
              <span class="badge text-bg-secondary">Safe Navigation</span>
              <span class="badge text-bg-secondary">HJ Reachability</span>
            </div>
            <a class="btn btn-outline-dark btn-sm" href="/publications/">Read More</a>
          </div>
        </div>
      </div>
      <div class="col-lg-4">
        <div class="card h-100">
          <div class="card-body">
            <span class="badge text-bg-dark mb-2">Featured</span>
            <img class="img-fluid rounded mb-3 highlight-img" src="/assets/img/ij26.png" alt="Featured research image">
            <h2 class="h5">Dynamic prioritization and adaptive path planning for indoor multi-object navigation</h2>
            <p class="text-muted">We propose a multi-object navigation method that dynamically selects target order and plans efficient paths in cluttered indoor environments.</p>
            <div class="d-flex flex-wrap gap-2 mb-3">
              <span class="badge text-bg-secondary">Path Planning</span>
              <span class="badge text-bg-secondary">Multi-object Navigation</span>
            </div>
            <a class="btn btn-outline-dark btn-sm" href="/publications/">Read More</a>
          </div>
        </div>
      </div>
      <div class="col-lg-4">
        <div class="card h-100">
          <div class="card-body">
            <span class="badge text-bg-dark mb-2">Featured</span>
            <img class="img-fluid rounded mb-3 highlight-img" src="/assets/img/ij25.png" alt="Featured research image">
            <h2 class="h5">Improving Structure-From-Motion and Rendering
Quality for Thermal Image-Based 3D Gaussian
Splatting</h2>
            <p class="text-muted">We propose thermal image–based 3D Gaussian Splatting for robust novel-view synthesis in low-visibility conditions.</p>
            <div class="d-flex flex-wrap gap-2 mb-3">
              <span class="badge text-bg-secondary">Gaussian Splatting</span>
              <span class="badge text-bg-secondary">Thermal Images</span>
            </div>
            <a class="btn btn-outline-dark btn-sm" href="/publications/">Read More</a>
          </div>
        </div>
      </div>
    </div>
  </div>
</section>

<section class="py-5">
  <div class="container">
    <div class="row gy-4">
      <div class="col-lg-8">
        <div class="card h-100">
          <div class="card-body">
            <h3>Recent News</h3>
            <ul class="list-unstyled mb-3">
              {% for item in site.data.news limit:5 %}
              <li class="d-flex align-items-start flex-wrap gap-3 py-2 border-bottom">
                <span class="badge text-bg-secondary news-date-badge">{{ item.date | date: "%b %Y" }}</span>
                <div class="flex-grow-1">{{ item.title }}</div>
                {% if item.photo_link %}
                <a class="news-link" href="{{ item.photo_link }}" aria-label="Open news photo">
                  <svg viewBox="0 0 24 24" width="16" height="16" fill="none" stroke="currentColor" stroke-width="1.8" stroke-linecap="round" stroke-linejoin="round" aria-hidden="true">
                    <path d="M4 7h3l2-2h6l2 2h3v12H4z"></path>
                    <circle cx="12" cy="13" r="3.5"></circle>
                  </svg>
                </a>
                {% endif %}
                {% if item.link %}
                <a class="news-link" href="{{ item.link }}" aria-label="Open news link">
                  <svg viewBox="0 0 24 24" width="16" height="16" fill="none" stroke="currentColor" stroke-width="1.8" stroke-linecap="round" stroke-linejoin="round" aria-hidden="true">
                    <path d="M10 13a5 5 0 0 0 7.07 0l3.54-3.54a5 5 0 0 0-7.07-7.07L12 3"></path>
                    <path d="M14 11a5 5 0 0 0-7.07 0L3.39 14.54a5 5 0 0 0 7.07 7.07L12 21"></path>
                  </svg>
                </a>
                {% endif %}
              </li>
              {% endfor %}
            </ul>
            <a class="btn btn-outline-dark" data-theme-btn="outline" href="/news/">More News</a>
          </div>
        </div>
      </div>
      <div class="col-lg-4">
        <div class="card h-100">
          <div class="card-body">
            <h3>Open Positions</h3>
            <p class="text-muted">We are recruiting motivated students passionate about robotics and AI.</p>
            <div class="fw-semibold small mb-1">Openings</div>
            <ul class="small mb-3">
              <li>Graduate admissions for the Spring 2027 semester are now open for advanced research applicants.</li>
              <li>Undergraduate research positions are open year-round for hands-on robotics and AI experience.</li>
            </ul>
            <div class="small mb-3">Contact: jhyunoh (at) kw.ac.kr</div>
            <a class="btn btn-outline-dark" data-theme-btn="outline" href="/contact/">Contact</a>
          </div>
        </div>
      </div>
    </div>
  </div>
</section>
