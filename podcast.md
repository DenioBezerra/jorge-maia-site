---
layout: page
title: Podcast
permalink: /podcast/
eyebrow: JorgeCast
description: Episódios, temas e presença do Jorge Maia no universo do podcast.
---

<div class="brand-showcase">
  <img class="brand-logo" src="{{ '/assets\css/img/jorgecastsemfundo.png' | relative_url }}" alt="JorgeCast">
</div>

<h2>Sobre o JorgeCast</h2>
<p>
  O JorgeCast é um espaço de conversas sobre tecnologia, inovação, IoT, carreira, mercado
  e transformação digital.
</p>

<h2>Temas abordados</h2>
<ul>
  <li>Internet das Coisas</li>
  <li>Negócios digitais</li>
  <li>Cloud e arquitetura</li>
  <li>Comunidade e eventos</li>
  <li>Tendências tecnológicas</li>
</ul>

<h2>Episódios em destaque</h2>
<div class="cards-3">
  {% assign podcast_posts = site.posts | where_exp: "post", "post.categories contains 'podcast'" | limit: 6 %}
  {% for post in podcast_posts %}
    <article class="post-card">
      <h3><a href="{{ post.url | relative_url }}">{{ post.title }}</a></h3>
      <p>{{ post.excerpt | strip_html | truncate: 120 }}</p>
    </article>
  {% endfor %}
</div>