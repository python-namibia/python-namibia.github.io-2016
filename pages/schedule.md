---
layout: page
title: "Schedule"
permalink: "/schedule/"
---


{% assign days = "Monday,Tuesday,Wednesday,Thursday,Friday" | split: "," %}
{% assign schedule = site.schedule | sort: 'date' %}


{% for day in days %}

## {{day}}

    {% for post in schedule %}
        {% if post.day == day %}
- **{{ post.date | date: "%H:%M" }}** {% if {{post.speaker}} %}{{post.speaker}}:{% endif %} [{{post.title}}]({{ post.url | prepend: site.baseurl }}) ({{post.location }})
        {% endif %}
    {% endfor %}

{% endfor %}
