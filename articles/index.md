---
layout: default
title: Articles
description: Explore all articles and tutorials published by Zvirox.
---

<div class="zv-container">

  <section class="zv-section">

    <div class="zv-section-header">

      <div>
        <div class="zv-card-category">
          ZVIROX PUBLICATION
        </div>

        <h1 class="zv-section-title">
          Articles
        </h1>
      </div>

    </div>


    {% if site.posts.size > 0 %}

      <div class="zv-article-grid">

        {% for post in site.posts %}

          <article class="zv-card">

            <div class="zv-card-body">

              {% if post.categories and post.categories.size > 0 %}

                <div class="zv-card-category">
                  {{ post.categories | first }}
                </div>

              {% endif %}


              <h2 class="zv-card-title">

                <a href="{{ post.url | relative_url }}">
                  {{ post.title }}
                </a>

              </h2>


              {% if post.description %}

                <p class="zv-card-excerpt">
                  {{ post.description }}
                </p>

              {% elsif post.excerpt %}

                <p class="zv-card-excerpt">
                  {{ post.excerpt | strip_html | truncate: 160 }}
                </p>

              {% endif %}


              <div class="zv-card-meta">

                <span>
                  {{ post.date | date: "%b %d, %Y" }}
                </span>

                <span>•</span>

                <span>
                  Read article
                </span>

              </div>

            </div>

          </article>

        {% endfor %}

      </div>

    {% else %}

      <div class="zv-panel">

        <h2 class="zv-panel-title">
          No articles yet
        </h2>

        <p>
          Zvirox articles and tutorials will appear here
          once they are published.
        </p>

      </div>

    {% endif %}

  </section>

</div>