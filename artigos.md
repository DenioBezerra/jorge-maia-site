---
<<<<<<< HEAD
layout: page-clean
<<<<<<< HEAD
=======
layout: page
>>>>>>> 3028af4c5560c319203bbff6be2d04731bacb7e5

=======
>>>>>>> e7ca9c5 (Melhorando Posts)
permalink: /artigos/
---

<section class="articles-apple">
  <div class="container articles-apple-hero">
    <div class="articles-apple-copy">
      <span class="articles-apple-kicker">Conteúdo em destaque</span>

      <h2>Publicações, opinião e conteúdo técnico</h2>

      <p class="articles-apple-lead">
        Reunião dos conteúdos publicados por Jorge Maia, incluindo episódios do
        JorgeCast, artigos técnicos, opinião, eventos e materiais do ecossistema tech.
      </p>

      <p>
        Uma área pensada para organizar melhor os conteúdos e valorizar as principais
        frentes de publicação com um visual mais limpo, editorial e profissional.
      </p>
    </div>

    <div class="articles-apple-visual">
      <div class="articles-apple-side-card">
        <img src="{{ '/assets\css/img/jorgemaiabigode.webp' | relative_url }}" alt="Jorge Maia">
      </div>
    </div>
  </div>

  <div class="container articles-apple-list">
    <div class="articles-apple-head">
      <h3>Publicações recentes</h3>
      <p>
        Episódios, artigos e conteúdos técnicos organizados em destaque para facilitar
        a leitura e a navegação.
      </p>
    </div>

    <div class="articles-apple-grid">
      {% for post in site.posts limit: 6 %}
        <article class="articles-apple-card">
          <div class="articles-apple-card-image">
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

          <div class="articles-apple-card-content">
            <span class="articles-apple-tag">
              {% if post.categories and post.categories.size > 0 %}
                {{ post.categories | first | replace: "-", " " | upcase }}
              {% else %}
                PUBLICAÇÃO
              {% endif %}
            </span>

            <h4>
              <a href="{{ post.url | relative_url }}">{{ post.title }}</a>
            </h4>

            <p>{{ post.excerpt | strip_html | truncate: 120 }}</p>

            <a class="articles-apple-link" href="{{ post.url | relative_url }}">Ler mais →</a>
          </div>
        </article>
      {% endfor %}
    </div>
  </div>
</section>