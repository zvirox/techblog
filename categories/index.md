---
layout: default
title: Categories
description: Explore technology, IT, networking, Linux and cybersecurity topics published by Zvirox.
---

<div class="zv-container">

  <section class="zv-section">

    <div class="zv-section-header">

      <div>
        <div class="zv-card-category">
          EXPLORE ZVIROX
        </div>

        <h1 class="zv-section-title">
          Categories
        </h1>
      </div>

    </div>

    <div class="zv-article-grid">

  {% assign categories = site.categories | sort %}

{% for category in categories %}

  {% assign category_name = category[0] %}
  {% assign category_posts = category[1] %}

  {% assign category_slug = category_name | slugify %}

  <article class="zv-card">

    <div class="zv-card-body">

      <div class="zv-card-category">
        {{ category_name }}
      </div>

      <h2 class="zv-card-title">
        {{ category_name }}
      </h2>

      <p class="zv-card-excerpt">

        {{ category_posts.size }}

        {% if category_posts.size == 1 %}
          article
        {% else %}
          articles
        {% endif %}

        published in this category.

      </p>

      {% if category_slug == "networking" %}

        <a
          href="{{ '/categories/networking/' | relative_url }}"
          class="zv-section-link"
        >
          Explore →
        </a>

      {% elsif category_slug == "cybersecurity" %}

        <a
          href="{{ '/categories/cybersecurity/' | relative_url }}"
          class="zv-section-link"
        >
          Explore →
        </a>

      {% elsif category_slug == "linux" %}

        <a
          href="{{ '/categories/linux/' | relative_url }}"
          class="zv-section-link"
        >
          Explore →
        </a>

      {% elsif category_slug == "it" %}

        <a
          href="{{ '/categories/it/' | relative_url }}"
          class="zv-section-link"
        >
          Explore →
        </a>

      {% elsif category_slug == "cloud" %}

        <a
          href="{{ '/categories/cloud/' | relative_url }}"
          class="zv-section-link"
        >
          Explore →
        </a>

      {% elsif category_slug == "technology" %}

        <a
          href="{{ '/categories/technology/' | relative_url }}"
          class="zv-section-link"
        >
          Explore →
        </a>

      {% endif %}

    </div>

  </article>

      {% endfor %}

    </div>

  </section>

</div>