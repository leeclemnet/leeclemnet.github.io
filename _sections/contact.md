---
title: Contact Me
navtitle: Contact
icon: fas fa-comments
section_id: contact
order: 4
---

<div class="col text-center">
  <h3> 
  {% for link in site.author.links %}
    <a href="{{ link.url }}" title="{{ link.label }}" alt="{{ link.label }}"> <i class="{{ link.icon }}"></i> </a>
  {% endfor %}
  </h3>
</div>