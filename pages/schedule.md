---
layout: page
title: "Schedule"
permalink: "/schedule/"
---


{% assign days = "Monday,Tuesday,Wednesday,Thursday,Friday" | split: "," %}


{% for day in days %}

## {{day}}

    {% for post in site.schedule reversed %}
        {% if post.day == day %}
- **{{ post.date | date: "%H:%M" }}** {% if {{post.speaker}} %}{{post.speaker}}:{% endif %} [{{post.title}}]({{ post.url | prepend: site.baseurl }}) ({{post.location }})
        {% endif %}
    {% endfor %}

{% endfor %}
