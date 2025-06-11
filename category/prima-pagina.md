---
layout: default
title: "Articoli di Prima Pagina"
---

<h1 class="section-title">Prima Pagina</h1>

<p>Tutti gli articoli della sezione di inchiesta e notizie principali.</p>

<div class="article-grid" style="margin-top: 2em;">
{% for post in site.posts %}
  {% if post.category == 'prima-pagina' %}
    <div class="article">
      <h3><a href="{{ post.url }}">{{ post.title }}</a></h3>
      <span class="author">{{ post.date | date: "%-d %B %Y" }}</span>
      <p>{{ post.excerpt }}</p>
    </div>
  {% endif %}
{% endfor %}
</div>
