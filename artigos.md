---
layout: page

permalink: /artigos/

---

<section class="articles-page">
  <div class="container">
    <div class="articles-hero">
      <div class="articles-hero-copy">
        <span class="articles-kicker">Conteúdo em destaque</span>
        <h2>Publicações, opinião e conteúdo técnico</h2>
        <p>
          Reunião dos conteúdos publicados por Jorge Maia, incluindo episódios do
          JorgeCast, artigos técnicos, opinião, eventos e materiais do ecossistema tech.
        </p>
      </div>

      <div class="articles-hero-visual">
        <div class="articles-hero-card">
          <img src="{{ '/assets\css/img/jorgemaiabigode.webp' | relative_url }}" alt="Jorge Maia">
        </div>
      </div>
    </div>

    <div class="articles-list-head">
      <h3>Publicações recentes</h3>
      <p>
        Inspirado na organização do site oficial, que destaca JorgeCast e artigos técnicos
        como frentes principais de conteúdo. :contentReference[oaicite:2]{index=2}
      </p>
    </div>

    <div class="articles-grid-pro">
      {% for post in site.posts limit: 6 %}
        <article class="article-card-pro">
          <div class="article-card-image">
            {% if post.title contains "S9E5" %}
              <img src="{{ '/assets\css/img/jorgecastS9E5.png' | relative_url }}" alt="{{ post.title }}">
            {% elsif post.title contains "S9E4" %}
              <img src="{{ '/assets\css/img/jorgecasts9e4.png' | relative_url }}" alt="{{ post.title }}">
            {% elsif post.categories contains "podcast" %}
              <img src="{{ '/assets\css/img/jorgecastsemfundo.png' | relative_url }}" alt="{{ post.title }}">
            {% else %}
              <img src="{{ '/assets\css/img/jorgemaiabigode.webp' | relative_url }}" alt="{{ post.title }}">
            {% endif %}
          </div>

          <div class="article-card-content">
            <span class="article-badge">
              {% if post.categories and post.categories.size > 0 %}
                {{ post.categories | first | replace: "-", " " | upcase }}
              {% else %}
                PUBLICAÇÃO
              {% endif %}
            </span>

            <h4>
              <a href="{{ post.url | relative_url }}">{{ post.title }}</a>
            </h4>

            <p>{{ post.excerpt | strip_html | truncate: 135 }}</p>

            <a class="article-link" href="{{ post.url | relative_url }}">Ler mais →</a>
          </div>
        </article>
      {% endfor %}
    </div>
  </div>
</section>