---
layout: page
permalink: /podcast/

---

<section class="podcast-showcase">
  <div class="podcast-showcase-bg">
    <span class="podcast-glow podcast-glow-1"></span>
    <span class="podcast-glow podcast-glow-2"></span>
  </div>

  <div class="container">
    <div class="podcast-hero">
      <div class="podcast-brand-card">
        <div class="brand-showcase">
          <img class="brand-logo" src="{{ '/assets\css/img/jorgemaia2.webp' | relative_url }}" alt="JorgeCast">
        </div>
      </div>

      <div class="podcast-intro">
        <span class="podcast-kicker">Podcast</span>
        <h2>Sobre o JorgeCast</h2>
        <p class="podcast-lead">
          O JorgeCast é um espaço de conversas sobre tecnologia, inovação, Internet das Coisas,
          carreira, mercado e transformação digital.
        </p>
        <p>
          Inspirado na presença que o podcast já tem no ecossistema do Jorge Maia, esta área
          pode destacar episódios, temas recorrentes e a conexão entre conteúdo, comunidade e negócios. :contentReference[oaicite:1]{index=1}
        </p>

        <div class="podcast-topics">
          <span>Internet das Coisas</span>
          <span>Negócios digitais</span>
          <span>Cloud e arquitetura</span>
          <span>Comunidade e eventos</span>
          <span>Tendências tecnológicas</span>
        </div>

        <a class="btn btn-primary" href="{{ '/podcast/' | relative_url }}">Explorar o JorgeCast</a>
      </div>
    </div>

    <div class="podcast-episodes-head">
      <h3>Episódios em destaque</h3>
      <p>
        Publicações recentes do podcast, seguindo a mesma lógica de destaque usada no site oficial. :contentReference[oaicite:2]{index=2}
      </p>
    </div>

    <div class="podcast-episodes-grid">
      {% assign podcast_posts = site.posts | where_exp: "post", "post.categories contains 'podcast'" | limit: 6 %}
      {% for post in podcast_posts %}
        <article class="podcast-episode-card">
          <div class="podcast-episode-image">
            {% if post.title contains "S9E5" %}
              <img src="{{ '/assets\css/img/jorgecastS9E5.png' | relative_url }}" alt="{{ post.title }}">
            {% elsif post.title contains "S9E4" %}
              <img src="{{ '/assets\css/img/jorgecasts9e4.png' | relative_url }}" alt="{{ post.title }}">
            {% else %}
              <img src="{{ '/assets\css/img/jorgecastsemfundo.png' | relative_url }}" alt="{{ post.title }}">
            {% endif %}
          </div>

          <div class="podcast-episode-content">
            <span class="episode-tag">Podcast</span>
            <h4><a href="{{ post.url | relative_url }}">{{ post.title }}</a></h4>
            <p>{{ post.excerpt | strip_html | truncate: 125 }}</p>
            <a class="episode-link" href="{{ post.url | relative_url }}">Ler episódio →</a>
          </div>
        </article>
      {% endfor %}
    </div>
  </div>
</section>