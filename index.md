---
layout: default
title: Accueil
---

<style>
/* Petite grille responsive pour des cartes propres */
.grid {
  display: grid;
  grid-template-columns: repeat(auto-fill, minmax(260px, 1fr));
  gap: 16px;
  margin: 24px 0;
}
.card {
  border: 1px solid #e5e7eb; /* gris clair */
  border-radius: 12px;
  padding: 16px;
  transition: transform .12s ease, box-shadow .12s ease;
  background: #fff;
}
.card:hover {
  transform: translateY(-2px);
  box-shadow: 0 6px 16px rgba(0,0,0,.06);
}
.card h3 { margin: 0 0 8px; font-size: 1.05rem; }
.card p  { margin: 0 0 12px; color: #6b7280; }
.card a  { margin-right: 10px; white-space: nowrap; }
.badge {
  display: inline-block; font-size: 12px; background:#f3f4f6; color:#374151;
  padding: 2px 8px; border-radius: 999px; margin-left: 6px;
}
.header h1 { margin-bottom: 6px; }
.subtitle { color:#6b7280; margin-top:0; }
</style>

<div class="header">
  <h1>{{ site.title }}</h1>
  <p class="subtitle">{{ site.description }}</p>
</div>

## Projets

<div class="grid">
{% for p in site.data.projects %}
  <div class="card">
    <h3>{{ p.name }}</h3>
    <p>{{ p.description }}</p>
    <div>
      <a href="https://github.com/{{ p.repo }}">Code</a>
      <a href="https://github.com/{{ p.repo }}/archive/refs/heads/main.zip">ZIP</a>
      {% if p.demo_url %}<a href="{{ p.demo_url }}">Démo</a>{% endif %}
    </div>
  </div>
{% endfor %}
</div>

## Me contacter
- LinkedIn : *(mets ton lien)*
- Email : *(mets ton email professionnel)*
