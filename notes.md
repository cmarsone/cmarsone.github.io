---
layout: default
title: Notes
description: Notes de lecture et explications sur le calcul haute performance, l’informatique quantique, les mathématiques et les sciences.
permalink: /notes/
---
<div class="archive-shell">
  <header class="page-intro">
    <p class="eyebrow">Le carnet</p>
    <h1>Notes &amp; idées.</h1>
    <p>Des explications, des lectures et des sujets explorés au fil du temps. Un carnet ouvert, entre informatique, sciences et curiosités.</p>
  </header>
  <section aria-label="Toutes les notes">
    {% assign current_year = '' %}
    {% for post in site.posts %}
      {% assign post_year = post.date | date: '%Y' %}
      {% if post_year != current_year %}
        {% unless forloop.first %}</div>{% endunless %}
        <div class="archive-year-group">
          <h2 class="archive-year">{{ post_year }}</h2>
        {% assign current_year = post_year %}
      {% endif %}
      <article class="archive-row">
        <time datetime="{{ post.date | date_to_xmlschema }}">{{ post.date | date: '%d %b' }}</time>
        <div><h3><a href="{{ post.url | relative_url }}">{{ post.title | escape }}</a></h3><p>{{ post.excerpt | strip_html | normalize_whitespace | truncate: 160 }}</p></div>
        <span aria-hidden="true">↗</span>
      </article>
      {% if forloop.last %}</div>{% endif %}
    {% endfor %}
  </section>
</div>
