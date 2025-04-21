---
layout: default
---
# Bienvenido a **KASAÉKO**

> Cocina con conciencia. Descubre nuestros productos sostenibles para tu hogar.

<ul>
  {% for p in site.data.productos %}
  <li>
    <a href="/productos/{{ p.slug }}.html">
      <img src="{{ p.imagen }}" alt="{{ p.nombre }}">
      <h2>{{ p.nombre }}</h2>
    </a>
  </li>
  {% endfor %}
</ul>
