---
layout: default
---

# Bienvenido a KASAÉKO

> Cocina con conciencia. Descubre nuestros productos sostenibles para tu hogar.

<ul>
{% for p in site.data.productos %}
  <li>
    <h2>{{ p.nombre }}</h2>
    <img src="{{ p.imagen }}" alt="{{ p.nombre }}" width="300">
    <p>{{ p.descripcion }}</p>
    <p><strong>Precio:</strong> {{ p.precio }}</p>
    <button class="snipcart-add-item"
      data-item-id="{{ p.slug }}"
      data-item-name="{{ p.nombre }}"
      data-item-price="{{ p.precio | remove: '€' }}"
      data-item-url="/productos/{{ p.slug }}.html"
      data-item-description="{{ p.descripcion }}">
      A\u00f1adir al carrito
    </button>
  </li>
{% endfor %}
</ul>
