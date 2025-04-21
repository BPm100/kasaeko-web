---
layout: default
title: Inicio
---

# Bienvenido a **KASAÉKO**

> Cocina con conciencia. Descubre nuestros productos sostenibles para tu hogar.

<ul style="list-style:none; padding:0;">
{% for p in site.data.productos %}
  <li style="margin-bottom:2rem; border-bottom:1px solid #eee; padding-bottom:1rem;">
    <h2>{{ p.nombre }}</h2>
    <img src="{{ p.imagen }}" alt="{{ p.nombre }}" style="max-width:300px; display:block; margin-bottom:1rem;">
    <p>{{ p.descripcion }}</p>
    <p><strong>Precio:</strong> {{ p.precio }}</p>
    <button class="snipcart-add-item"
      data-item-id="{{ p.slug }}"
      data-item-name="{{ p.nombre }}"
      data-item-price="{{ p.precio | remove: '€' }}"
      data-item-url="/productos/{{ p.slug }}.html"
      data-item-description="{{ p.descripcion }}">
      Añadir al carrito
    </button>
  </li>
{% endfor %}
</ul>
