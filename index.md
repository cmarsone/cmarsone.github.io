---
layout: default
description: Ingénieur en calcul haute performance à Paris. Notes et projets autour du HPC, de l’informatique quantique et des sciences.
---
<div class="home-shell">
  <section class="hero" aria-labelledby="hero-title">
    <div class="hero-copy">
      <p class="eyebrow"><span class="status-dot"></span> Ingénieur HPC <span class="eyebrow-separator">·</span> Paris, France</p>
      <h1 id="hero-title">Faire parler<br>les <em>machines</em>.</h1>
      <p class="hero-lead">Je suis Clément, ingénieur en calcul haute performance. J’explore les systèmes, les mathématiques et les idées qui rendent le calcul scientifique possible à grande échelle.</p>
      <div class="hero-actions">
        <a class="button-link" href="{{ '/About/' | relative_url }}">En savoir plus <span aria-hidden="true">↗</span></a>
        <a class="quiet-link" href="{{ '/notes/' | relative_url }}">Lire mes notes <span aria-hidden="true">↓</span></a>
      </div>
      <div class="hero-meta"><span>Calcul parallèle</span><span>CPU &amp; GPU</span><span>Sciences</span></div>
    </div>
    <div class="hero-portrait">
      <div class="portrait-frame"><img src="{{ '/images/profile.jpeg' | relative_url }}" alt="Clément Marsone à Paris"></div>
      <div class="portrait-caption"><span class="caption-mark">✳</span><span>Ingénieur, lecteur<br>et cycliste du dimanche</span></div>
      <div class="portrait-index">48°51′ N<br>2°21′ E</div>
    </div>
  </section>

  <section class="interests" aria-labelledby="interests-title">
    <div class="section-heading"><p class="eyebrow">Ce qui m’anime</p><h2 id="interests-title">À la rencontre du calcul<br>et des sciences.</h2></div>
    <div class="interest-list">
      <article class="interest-item"><span class="interest-number">01</span><div><h3>Calcul haute performance</h3><p>Programmation parallèle, architecture des processeurs et outils pour accélérer les calculs scientifiques.</p></div><span class="interest-symbol" aria-hidden="true">↗</span></article>
      <article class="interest-item"><span class="interest-number">02</span><div><h3>Informatique quantique</h3><p>Algorithmes, optimisation et passerelles entre informatique, mathématiques et physique.</p></div><span class="interest-symbol" aria-hidden="true">↗</span></article>
      <article class="interest-item"><span class="interest-number">03</span><div><h3>Curiosité sans frontières</h3><p>Des notes sur la science, mais aussi sur la musique, la philosophie et ce qui se découvre en chemin.</p></div><span class="interest-symbol" aria-hidden="true">↗</span></article>
    </div>
  </section>

  <section class="recent-notes" aria-labelledby="recent-title">
    <div class="section-topline"><div><p class="eyebrow">Carnet de bord</p><h2 id="recent-title">Notes récentes</h2></div><a class="all-link" href="{{ '/notes/' | relative_url }}">Toutes les notes <span aria-hidden="true">→</span></a></div>
    <div class="note-grid">
      {% for post in site.posts limit:4 %}
      <article class="note-card">
        <a class="note-card-link" href="{{ post.url | relative_url }}">
          <span class="note-date">{{ post.date | date: '%d.%m.%Y' }}</span>
          <h3>{{ post.title | escape }}</h3>
          <p>{{ post.excerpt | strip_html | normalize_whitespace | truncate: 135 }}</p>
          <span class="note-arrow" aria-hidden="true">↗</span>
        </a>
      </article>
      {% endfor %}
    </div>
  </section>

  <section class="closing-note">
    <p class="eyebrow">En dehors du terminal</p>
    <p>Quand je ne suis pas devant un écran, je pars rouler sur les routes d’Île-de-France — ou je retrouve un opéra, un livre de philosophie et un peu de musique sacrée.</p>
    <a class="quiet-link" href="{{ '/cycling/' | relative_url }}">Suivre mes sorties vélo <span aria-hidden="true">↗</span></a>
  </section>
</div>
