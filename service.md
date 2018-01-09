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
            {% if org.link %}
                <a href="{{ org.link }}"><img class="col one right" style="padding-left: 1em; padding-bottom: 1em" src="{{ org.img }}"></a>
            {% else %}
                <img class="col one right" style="padding-left: 1em; padding-bottom: 1em" src="{{ org.img }}">
            {% endif %}
        {% endif %}

        {% if org.role %}
            <b>{{ org.role }} &ndash; </b> 
            {% if org.link %}
                <a href="{{ org.link }}" target="_blank"><b>{{ org.title }}</b></a><br/>
            {% else %}
                <b>{{ org.title }}</b><br/>
            {% endif %}
            
            <i>{{ org.years }}</i><br/>
        {% else %}
            {% if org.shorttitle %}
                <b>{{ org.shorttitle }}</b> &ndash; {{ org.title }} &ndash; <i>{{ org.years }}</i>
            {% else %}
                {% if org.link %}
                    <a href="{{ org.link }}" target="_blank"><b>{{ org.title }}</b></a>
                {% else %}
                    <b>{{ org.title }}</b>
                {% endif %}

                &ndash; <i>{{ org.years }}</i>
            {% endif %}
        {% endif %}

        {% if org.description %}
            <br/>{{ org.description }}<br/>
        {% endif %}

        {% if org.note %}
            <br/><i>{{ org.note }}</i><br/>
        {% endif %}

        <br/>
        
    {% endfor %}
    </div><br/><hr/>
{% endfor %}
</div>