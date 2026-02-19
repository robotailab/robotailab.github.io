---
title: Gallery
permalink: /gallery/
---

<section class="py-5">
  <div class="container">
    <div class="row mb-4">
      <div class="col-lg-8">
        <h1>Gallery</h1>
        <p class="text-muted">Selected moments from our lab.</p>
      </div>
    </div>

    <div class="row g-4">
      {% for event in site.data.gallery %}
      <div class="col-12 col-lg-4" id="event-{{ event.id }}">
        <button class="card gallery-event text-start w-100" type="button" data-bs-toggle="modal" data-bs-target="#galleryEvent-{{ event.id }}">
          <div class="card-body">
            <div class="d-flex align-items-center gap-3">
              <img class="gallery-cover rounded" src="{{ event.cover }}" alt="{{ event.title }} cover" loading="lazy">
              <div>
                <div class="fw-semibold">{{ event.title }}</div>
                <div class="text-muted small">{{ event.date }}</div>
              </div>
            </div>
          </div>
        </button>
      </div>
      {% endfor %}
    </div>
  </div>
</section>

<style>
  .gallery-cover {
    width: 72px;
    height: 72px;
    object-fit: cover;
  }
  .gallery-event summary {
    cursor: pointer;
  }
  .gallery-event {
    border: 1px solid var(--bs-border-color);
    background: transparent;
  }
  .gallery-event:focus-visible {
    outline: 2px solid var(--bs-primary);
    outline-offset: 2px;
  }
  .masonry-grid {
    display: block;
  }
  .photo-grid {
    display: flex;
    flex-wrap: wrap;
    gap: 12px;
  }
  .photo-item img {
    display: block;
  }
</style>

{% for event in site.data.gallery %}
<div class="modal fade" id="galleryEvent-{{ event.id }}" tabindex="-1" aria-hidden="true">
  <div class="modal-dialog modal-xl modal-dialog-centered modal-dialog-scrollable">
    <div class="modal-content">
      <div class="modal-header">
        <h5 class="modal-title">{{ event.title }}</h5>
        <button type="button" class="btn-close" data-bs-dismiss="modal" aria-label="Close"></button>
      </div>
      <div class="modal-body">
        <div class="photo-grid">
          {% for photo in event.images %}
          <div class="photo-item">
            <img class="img-fluid rounded" src="{{ photo.src }}" alt="{{ event.title }} photo {{ forloop.index }}" loading="lazy"{% if photo.h %} style="height: {{ photo.h }}px; width: auto;"{% endif %}>
          </div>
          {% endfor %}
        </div>
      </div>
    </div>
  </div>
</div>
{% endfor %}
<script>
  window.addEventListener("load", () => {
    const hash = window.location.hash;
    if (hash && hash.startsWith("#galleryEvent-")) {
      const modalEl = document.querySelector(hash);
      if (modalEl && window.bootstrap && window.bootstrap.Modal) {
        const modal = new bootstrap.Modal(modalEl);
        modal.show();
      }
    }
  });
</script>
