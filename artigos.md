---
layout: page
title: Artigos
permalink: /artigos/
eyebrow: Blog
description: Artigos de opinião, tecnologia, podcast, eventos e conteúdo técnico.
---

<h2>Publicações</h2>
<p>
  Reunião dos conteúdos publicados por Jorge Maia, incluindo opinião, tecnologia,
  podcast, eventos e materiais técnicos.
</p>

<div class="cards-3">
  {% for post in site.posts %}
    <article class="post-card">
      <span class="card-tag">{{ post.category | default: "Artigo" }}</span>
      <h3><a href="{{ post.url | relative_url }}">{{ post.title }}</a></h3>
      <p>{{ post.excerpt | strip_html | truncate: 130 }}</p>
      <a href="{{ post.url | relative_url }}">Ler mais</a>
    </article>
  {% endfor %}
</div>