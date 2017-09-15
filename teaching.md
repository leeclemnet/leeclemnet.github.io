---
layout: page
title: Teaching
order: 3
---

<hr/>
<div>

{% assign sorted_teaching = site.teaching | sort:"order" %}
{% for teaching in sorted_teaching %}
    <div><br/>
    <h3>{{ teaching.title }}</h3><br/>

    {% assign sorted_courses = teaching.courses | sort:"title" %}
    {% for course in sorted_courses %}

        {% if course.img %}
        <img class="right" style="width: 40%; padding-left: 1em" src="{{course.img}}">
        {% endif %}

        <b>{{ course.code }} &ndash; {{ course.title }}</b><br/>
        <i>{{ course.terms }}</i><br/><br/>

        {{ course.description }}<br/><br/>
        
        {% if course.note %}
        <i>{{ course.note }}</i><br/>
        {% endif %}

    {% endfor %}
    </div><br/><hr/>
{% endfor %}

</div>