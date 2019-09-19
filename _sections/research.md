---
title: Research
icon: fas fa-cog
section_id: research
background_color: bg-light
order: 2
---

{% for project in site.data.research %}
  <div class="col-md-4 d-flex align-items-stretch border-primary">
    <div class="card mb-2" style="width: 100%">
      <img class="card-img-top mx-auto" style="width: 100%" src="{{ project.image }}">
      <div class="card-body">
        <h5 class="card-title text-center"> {{ project.title }} </h5>
        <p class="card-text text-justify"> {{ project.description }} </p>
      </div>
    </div>
  </div>
{% endfor %}