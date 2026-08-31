---
layout: default
title: Zvirox
description: Practical technology, IT, networking and cybersecurity tutorials and guides.
---

<div class="zv-container">

  <!-- =====================================================
       HERO
       ===================================================== -->

  <section class="zv-hero">

    <div class="zv-hero-content">

      <div class="zv-card-category">
        CYBER DEFENDER • TECHNOLOGY • IT
      </div>

      <h1>
        Technology,
        <span>explained.</span>
      </h1>

      <p>
        Practical tutorials, technical guides and cybersecurity
        knowledge for people who want to understand how technology
        actually works.
      </p>

      <div style="display:flex; gap:12px; flex-wrap:wrap;">

        <a
          href="{{ '/articles/' | relative_url }}"
          class="zv-button zv-button-primary"
        >
          Explore Articles
        </a>

        <a
          href="#latest"
          class="zv-button zv-button-secondary"
        >
          Latest Posts
        </a>

      </div>

    </div>

  </section>


  <!-- =====================================================
       LATEST ARTICLES
       ===================================================== -->

  <section
    id="latest"
    class="zv-section"
  >

    <div class="zv-section-header">

      <h2 class="zv-section-title">
        Latest Articles
      </h2>

      <a
        href="{{ '/articles/' | relative_url }}"
        class="zv-section-link"
      >
        View all →
      </a>

    </div>


    <div class="zv-article-grid">

      {% if site.posts.size > 0 %}

        {% for post in site.posts limit: 6 %}

          <article class="zv-card">

            <div class="zv-card-body">

              {% if post.categories and post.categories.size > 0 %}

                <div class="zv-card-category">
                  {{ post.categories | first }}
                </div>

              {% else %}

                <div class="zv-card-category">
                  ZVIROX
                </div>

              {% endif %}


              <h3 class="zv-card-title">

                <a href="{{ post.url | relative_url }}">
                  {{ post.title }}
                </a>

              </h3>


              {% if post.excerpt %}

                <p class="zv-card-excerpt">
                  {{ post.excerpt | strip_html | truncate: 150 }}
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

      {% else %}

        <article class="zv-card">

          <div class="zv-card-body">

            <div class="zv-card-category">
              ZVIROX
            </div>

            <h3 class="zv-card-title">
              Articles coming soon
            </h3>

            <p class="zv-card-excerpt">
              Practical technology and cybersecurity tutorials
              are on the way.
            </p>

          </div>

        </article>

      {% endif %}

    </div>

  </section>


  <!-- =====================================================
       TOPICS
       ===================================================== -->

  <section class="zv-section">

    <div class="zv-section-header">

      <h2 class="zv-section-title">
        Explore Topics
      </h2>

    </div>


    <div class="zv-article-grid">

      <article class="zv-card">

        <div class="zv-card-body">

          <div class="zv-card-category">
            SECURITY
          </div>

          <h3 class="zv-card-title">
            Cybersecurity
          </h3>

          <p class="zv-card-excerpt">
            Security concepts, defensive techniques,
            threats, tools and practical security knowledge.
          </p>

          <a
            href="{{ '/categories/cybersecurity/' | relative_url }}"
            class="zv-section-link"
          >
            Explore →
          </a>

        </div>

      </article>


      <article class="zv-card">

        <div class="zv-card-body">

          <div class="zv-card-category">
            NETWORKING
          </div>

          <h3 class="zv-card-title">
            Networking
          </h3>

          <p class="zv-card-excerpt">
            Networks, protocols, troubleshooting,
            infrastructure and how the Internet works.
          </p>

          <a
            href="{{ '/categories/networking/' | relative_url }}"
            class="zv-section-link"
          >
            Explore →
          </a>

        </div>

      </article>


      <article class="zv-card">

        <div class="zv-card-body">

          <div class="zv-card-category">
            LINUX
          </div>

          <h3 class="zv-card-title">
            Linux
          </h3>

          <p class="zv-card-excerpt">
            Linux administration, command line,
            troubleshooting and practical guides.
          </p>

          <a
            href="{{ '/categories/linux/' | relative_url }}"
            class="zv-section-link"
          >
            Explore →
          </a>

        </div>

      </article>


      <article class="zv-card">

        <div class="zv-card-body">

          <div class="zv-card-category">
            IT
          </div>

          <h3 class="zv-card-title">
            IT & Technology
          </h3>

          <p class="zv-card-excerpt">
            Practical IT tutorials, troubleshooting,
            systems and technology explainers.
          </p>

          <a
            href="{{ '/categories/it/' | relative_url }}"
            class="zv-section-link"
          >
            Explore →
          </a>

        </div>

      </article>

    </div>

  </section>


  <!-- =====================================================
       ABOUT ZVIROX
       ===================================================== -->

  <section class="zv-section">

    <div class="zv-hero">

      <div class="zv-hero-content">

        <div class="zv-card-category">
          ABOUT ZVIROX
        </div>

        <h2>
          Learn technology by
          <span>understanding it.</span>
        </h2>

        <p>
          Zvirox focuses on practical technology education —
          from IT and networking to Linux and cybersecurity.
          The goal isn't just to show you which command to type,
          but to explain what is happening underneath.
        </p>

        <a
          href="{{ '/about/' | relative_url }}"
          class="zv-button zv-button-secondary"
        >
          About Zvirox
        </a>

      </div>

    </div>

  </section>

</div>