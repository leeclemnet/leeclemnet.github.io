---
title: Contact Me
navtitle: Contact
icon: fas fa-comments
section_id: contact
order: 4
---

<div class="col-md-4 ml-auto my-auto">
  <img class="img-responsive" width="100%" style="border-radius: 3%" src="assets/images/toronto.jpg">
</div>

<div class="col-md-4 mr-auto my-auto">
  {% for link in site.author.links %}
    <div class="row my-2"> <div class="col text-center text-md-left"> 
      <a href="{{ link.url }}" title="{{ link.label }}" alt="{{ link.label }}" target="_blank"> <i class="{{ link.icon }}"></i> {{ link.label }} </a> 
    </div> </div>
  {% endfor %}
</div>