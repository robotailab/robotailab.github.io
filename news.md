---
title: News
permalink: /news/
---

<section class="py-5">
  <div class="container">
    <div class="row mb-4">
      <div class="col-lg-8">
        <h1>News</h1>
        <p class="text-muted">Updates and highlights from our lab.</p>
      </div>
    </div>

    <ul class="list-unstyled">
      {% for item in site.data.news %}
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
  </div>
</section>
