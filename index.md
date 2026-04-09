---
layout: default
title: Home
description: Site profissional de Jorge Maia com artigos, projetos, podcast, atividades e premiações.
---
<section class="hero-home">
  <div class="hero-bg-effects">
    <span class="hero-blur hero-blur-1"></span>
    <span class="hero-blur hero-blur-2"></span>
    <span class="hero-grid-lines"></span>
  </div>

  <div class="container hero-grid">
    <div class="hero-text">
      <span class="eyebrow">Tecnologia • Inovação • Comunidade</span>

      <h1>Jorge Maia</h1>

      <h2>
        Negócios conectados, conteúdo técnico e liderança em tecnologia
      </h2>

      <p>
        Cientista da Computação, empreendedor, consultor, palestrante e criador de
        iniciativas que conectam tecnologia, Internet das Coisas, nuvem, comunidade
        e negócios digitais.
      </p>

      <div class="hero-actions">
        <a class="btn btn-primary" href="{{ '/sobre/' | relative_url }}">Conheça a trajetória</a>
        <a class="btn btn-secondary" href="{{ '/artigos/' | relative_url }}">Ver artigos</a>
      </div>

      <div class="hero-mini-info">
        <div class="mini-item">
          <strong>Conteúdo</strong>
          <span>Artigos, vídeos e podcast</span>
        </div>

        <div class="mini-item">
          <strong>Atuação</strong>
          <span>Tecnologia, comunidade e negócios</span>
        </div>
      </div>
    </div>

    <div class="hero-visual">
      <div class="hero-image-wrap">
        <span class="image-glow"></span>
        <img src="{{ '/assets\css/img/jorgemaia.jpg' | relative_url }}" alt="Jorge Maia">
      </div>
    </div>
  </div>
</section>


<section class="highlight-section">
  <div class="container">
    <div class="section-heading">
      <span class="section-kicker">Ecossistema digital</span>
      <h2>Conteúdo, comunidade e projetos</h2>
      <p>
        Uma visão organizada dos principais pilares da presença digital de Jorge Maia:
        podcast, canal de conteúdo e projetos conectados ao universo da tecnologia.
      </p>
    </div>

    <div class="cards-3">
      <article class="info-card">
        <div class="card-top">
          <span class="card-tag">Podcast</span>
          <h3>JorgeCast</h3>
          <p>Conteúdo sobre IoT, inovação, tecnologia, carreira e negócios digitais.</p>
        </div>

        <div class="card-bottom">
          <a href="{{ '/podcast/' | relative_url }}" class="card-link">Explorar</a>
          <div class="project-logo-wrap">
            <img class="project-logo" src="{{ '/assets\css/img/jorgecast2 (2).png' | relative_url }}" alt="JorgeCast">
          </div>
        </div>
      </article>

      <article class="info-card">
        <div class="card-top">
          <span class="card-tag">Conteúdo</span>
          <h3>Canal no YouTube</h3>
          <p>Vídeos, entrevistas, eventos, bastidores e materiais técnicos.</p>
        </div>

        <div class="card-bottom">
          <a href="{{ '/youtube/' | relative_url }}" class="card-link">Explorar</a>
          <div class="project-logo-wrap">
            <img class="project-logo" src="{{ '/assets\css/img/jorgemaiayoutube.png' | relative_url }}" alt="Canal do Jorge Maia">
          </div>
        </div>
      </article>

      <article class="info-card">
        <div class="card-top">
          <span class="card-tag">Empresas</span>
          <h3>Projetos e negócios</h3>
          <p>CrazyTechLabs, comunidade, eventos, iniciativas e produtos digitais.</p>
        </div>

        <div class="card-bottom">
          <a href="{{ '/projetos/' | relative_url }}" class="card-link">Explorar</a>
          <div class="project-logo-wrap">
            <img class="project-logo logo-ctl" src="{{ '/assets\css/img/ctl.png' | relative_url }}" alt="CrazyTechLabs">
          </div>
        </div>
      </article>
    </div>
  </div>
</section>

<section class="bio-section">
  <div class="bio-bg-effects">
    <span class="bio-glow bio-glow-1"></span>
    <span class="bio-glow bio-glow-2"></span>
  </div>

  <div class="container bio-grid">
    <div class="bio-visual">
      <div class="bio-image-wrap">
        <img src="{{ '/assets\css/img/jorgemaia5.png' | relative_url }}" alt="Jorge Maia em evento">
      </div>
    </div>

    <div class="bio-content">
      <span class="bio-eyebrow">Sobre o profissional</span>

      <h2>Mais de 20 anos em software, inovação e comunidade</h2>

      <p>
        Jorge Maia atua na interseção entre desenvolvimento de software, arquitetura,
        Internet das Coisas, nuvem, educação, comunicação e empreendedorismo.
      </p>

      <p>
        Além da atuação técnica e executiva, também mantém forte presença em eventos,
        podcasts, vídeos, workshops, mentorias e projetos voltados ao ecossistema de tecnologia.
      </p>

      <div class="bio-highlights">
        <div class="bio-highlight-item">
          <strong>Atuação</strong>
          <span>Software, IoT, nuvem e arquitetura</span>
        </div>

        <div class="bio-highlight-item">
          <strong>Presença</strong>
          <span>Eventos, conteúdo, workshops e comunidade</span>
        </div>
      </div>

      <a class="btn btn-primary" href="{{ '/sobre/' | relative_url }}">Ler história completa</a>
    </div>
  </div>
</section>

<section class="posts-section">
  <div class="container">
    <div class="section-heading center">
      <span class="eyebrow">Publicações</span>
      <h2>Artigos em destaque</h2>
    </div>

    <div class="posts-grid">
      {% assign artigos = site.posts | where_exp: "post", "post.categories contains 'artigos'" | limit: 3 %}
      
      {% for post in artigos %}
        <article class="post-card">
          
          <div class="post-image">
            {% if post.title contains "S9E5" %}
              <img src="{{ '/assets\css/img/jorgecastS9E5.png' | relative_url }}" alt="{{ post.title }}">
            {% elsif post.title contains "S9E4" %}
              <img src="{{ '/assets\css/img/jorgecasts9e4.png' | relative_url }}" alt="{{ post.title }}">
            {% else %}
              <img src="{{ '/assets\css/img/jorgemaia3.webp' | relative_url }}" alt="{{ post.title }}">
            {% endif %}
          </div>

          <div class="post-content">
            <span class="card-tag">
              {{ post.categories | first | upcase }}
            </span>

            <h3>
              <a href="{{ post.url | relative_url }}">{{ post.title }}</a>
            </h3>

            <p>
              {{ post.excerpt | strip_html | truncate: 120 }}
            </p>

            <a class="post-link" href="{{ post.url | relative_url }}">
              Ler mais →
            </a>
          </div>

        </article>
      {% endfor %}
    </div>
  </div>
</section>

<section class="awards-section">
  <div class="container">
    <div class="section-heading center">
      <span class="eyebrow">Reconhecimento</span>
      <h2>Prêmios e marcos profissionais</h2>
      <p>
        Destaques que reforçam trajetória, presença em comunidade, liderança técnica
        e contribuição para o ecossistema de tecnologia.
      </p>
    </div>

    <div class="awards-grid">
      <article class="award-card">
        <div class="award-image">
          <img src="{{ '/assets\css/img/premio.png' | relative_url }}" alt="Microsoft MVP">
        </div>

        <div class="award-content">
          <span class="award-tag">Reconhecimento</span>
          <h3>Microsoft MVP</h3>
          <p>
            Reconhecimento por contribuição, compartilhamento de conhecimento e impacto
            junto à comunidade técnica.
          </p>
        </div>
      </article>

      <article class="award-card">
        <div class="award-image">
          <img src="{{ '/assets\css/img/premio2.png' | relative_url }}" alt="Eventos nacionais e internacionais">
        </div>

        <div class="award-content">
          <span class="award-tag">Participação</span>
          <h3>Eventos nacionais e internacionais</h3>
          <p>
            Palestras, workshops, meetups, conteúdos e presença ativa em iniciativas
            do ecossistema de tecnologia.
          </p>
        </div>
      </article>

      <article class="award-card">
        <div class="award-image">
          <img src="{{ '/assets\css/img/premio3.png' | relative_url }}" alt="Liderança em tecnologia">
        </div>

        <div class="award-content">
          <span class="award-tag">Liderança</span>
          <h3>Liderança em tecnologia</h3>
          <p>
            Atuação em empresas, projetos, comunidade e desenvolvimento de profissionais
            ao longo da trajetória.
          </p>
        </div>
      </article>
    </div>
  </div>
</section>