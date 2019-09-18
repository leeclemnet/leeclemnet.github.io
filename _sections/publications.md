---
title: Publications
icon: fas fa-copy
section_id: publications
order: 3
---

<div class="col">
  {% for pubtype in site.data.pubtypes %}
    <div class="row"> <div class="col">
    <h2> {{ pubtype.header }} </h2>
    
    <div class="row"> <div class="col mx-4">
      {% assign filtered_publications = site.data.publications | where: "type", pubtype.type %}
      {% for publication in filtered_publications %}
        <p>
          {% if publication.doi %}
            <a href="//dx.doi.org/{{ publication.doi }}" target="_blank"><b>{{ publication.title }}</b></a>
          {% else %}
            <b>{{ publication.title }}</b>
          {% endif %}
          <br/>

          <i>{{ publication.authors }}</i> <br/>

          {{ publication.venue }} <br/>

          {% if publication.note %}
            <i>{{ publication.note }}</i> <br/>
          {% endif %}

          {% if publication.award %}
            <b>{{ publication.award }}</b> <br/>
          {% endif %}

          {% if publication.links %}
            {% if publication.links.preprint %}
              <a href="{{ publication.links.preprint }}" target="_blank"><i class="far fa-file-alt"></i>&nbsp;Preprint</a>&nbsp;
            {% endif %}

            {% if publication.links.code %}
              <a href="{{ publication.links.code }}" target="_blank"><i class="fas fa-code-branch"></i>&nbsp;Code</a>&nbsp;
            {% endif %}

            {% if publication.links.slides %}
              <a href="{{ publication.links.slides }}" target="_blank"><i class="fas fa-desktop"></i>&nbsp;Slides</a>&nbsp;
            {% endif %}

            {% if publication.links.poster %}
              <a href="{{ publication.links.poster }}" target="_blank"><i class="far fa-image"></i>&nbsp;Poster</a>&nbsp;
            {% endif %}

            {% if publication.links.video %}
              <a href="{{ publication.links.video }}" target="_blank"><i class="fab fa-youtube"></i>&nbsp;Video</a>&nbsp;
            {% endif %}
            <br/>
          {% endif %}
        </p>
      {% endfor %}
    </div> </div> </div> </div>
  {% endfor %}
</div>