---
layout: page-clean
permalink: /podcast/

---

<section class="podcast-apple">

  <div class="container podcast-apple-hero">

    <div class="podcast-apple-visual">
      <div class="podcast-apple-image">
        <img src="{{ '/assets\css/img/jorgemaia2.webp' | relative_url }}" alt="JorgeCast">
      </div>
    </div>

    <div class="podcast-apple-copy">
      <span class="podcast-apple-kicker">Podcast</span>

      <h2>Conversas sobre tecnologia e inovação</h2>

      <p class="podcast-apple-lead">
        O JorgeCast é um espaço de conversas sobre tecnologia, inovação, IoT,
        carreira, mercado e transformação digital.
      </p>

      <p>
        Episódios que conectam conteúdo técnico, experiências reais e o ecossistema
        de tecnologia, trazendo visão prática para profissionais e empresas.
      </p>

      <div class="podcast-apple-topics">
        <span>IoT</span>
        <span>Negócios digitais</span>
        <span>Cloud</span>
        <span>Comunidade</span>
        <span>Tendências</span>
      </div>

      <div class="podcast-apple-actions">
        <a class="btn btn-primary" href="https://www.youtube.com/canaldojorgemaia" target="_blank">
          Assistir no YouTube
        </a>

        <a class="btn btn-secondary" href="#episodios">
          Ver episódios
        </a>
      </div>
    </div>

  </div>

  <div class="container" id="episodios">

    <div class="podcast-apple-head">
      <h3>Episódios em destaque</h3>
      <p>Seleção dos episódios mais relevantes do JorgeCast.</p>
    </div>

    <div class="podcast-apple-grid">
      {% assign podcast_posts = site.posts | where_exp: "post", "post.categories contains 'podcast'" | limit: 6 %}
      {% for post in podcast_posts %}
        <a href="{{ post.url | relative_url }}" class="podcast-apple-card">

          <div class="podcast-apple-card-image">
            {% if post.title contains "S9E5" %}
              <img src="{{ '/assets\css/img/jorgecastS9E5.png' | relative_url }}">
            {% elsif post.title contains "S9E4" %}
              <img src="{{ '/assets\css/img/jorgecasts9e4.png' | relative_url }}">
            {% else %}
              <img src="{{ '/assets\css/img/jorgecastsemfundo.png' | relative_url }}">
            {% endif %}
          </div>

          <div class="podcast-apple-card-content">
            <span class="tag">Podcast</span>
            <h4>{{ post.title }}</h4>
            <p>{{ post.excerpt | strip_html | truncate: 100 }}</p>
            <span class="link">Assistir episódio →</span>
          </div>

        </a>
      {% endfor %}
    </div>

  </div>

</section>