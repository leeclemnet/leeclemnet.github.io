---
layout: page
title: Service
order: 4
---

<hr/>
<div>
{% assign sorted_service = site.service | sort:"order" %}
{% for service in sorted_service %}
    <div><br/>
    <h3>{{ service.title }}</h3><br/>

    {% for org in service.organizations %}
        {% if org.img %}
            <img class="col one right" style="padding-left: 1em" src="{{ org.img }}">
        {% endif %}

        {% if org.role %}
            <b>{{ org.role }},</b> <a href="{{ org.link }}"><b>{{ org.title }}</b></a><br/>
            <i>{{ org.years }}</i><br/>
        {% else %}
            <b>{{ org.shorttitle }}</b> &mdash; {{ org.title }} &mdash; <i>{{ org.years }}</i>
        {% endif %}

        {% if org.description %}
            <br/>{{ org.description }}<br/>
        {% endif %}

        {% if org.note %}
            <i>{{ org.note }}</i><br/>
        {% endif %}

        <br/>
        
    {% endfor %}
    </div><br/><hr/>
{% endfor %}
</div>