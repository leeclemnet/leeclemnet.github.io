---
title: Teaching & Service
icon: fas fa-university
section_id: teaching
background_color: bg-light
order: 3
---

<div class="row"> <div class="col">
  <h2> Teaching </h2>
  <div class="row">
    <div class="col mx-4">
      {% assign sorted_teaching = site.data.teaching %}
      {% for course in site.data.teaching %}
        <p>
          <b>{{ course.role }} &ndash; {{ course.code }} ({{ course.title }}) &ndash; {{ course.terms }} </b><br/>

            {{ course.description }}<br/>
            
            {% if course.note %}
              <i>{{ course.note }}</i><br/>
            {% endif %}
        </p>
      {% endfor %}
    </div>
  </div>
</div> </div>

<div class="row"> <div class="col">
  <h2> Professional Activities & Community Service </h2>
  <div class="row">
    <div class="col mx-4">
      {% assign sorted_service = site.data.service | sort:"title" %}
      {% for service in site.data.service %}
        <p>
          <b>{{ service.role }} &ndash; {% if service.url %} <a href="{{ service.url }}" target="_blank">{{ service.title }}</a> {% else %} {{ service.title }} {% endif %} &ndash; {{ service.years }} </b><br/>

            {{ service.description }}<br/>
            
            {% if service.note %}
              <i>{{ service.note }}</i><br/>
            {% endif %}
        </p>
      {% endfor %}
    </div>
  </div>
</div> </div>