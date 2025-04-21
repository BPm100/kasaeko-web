---
layout: default
title: Productos
---
# Nuestros Productos

<ul>
  {% for p in site.data.productos %}
  <li>
    <h3><a href="/productos/{{ p.slug }}.html">{{ p.nombre }}</a></h3>
    <p>{{ p.descripcion }}</p>
  </li>
  {% endfor %}
</ul>
