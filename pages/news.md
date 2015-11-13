---
layout: page
title: "News"
permalink: "/news/"
---

{% for post in site.posts %}
    {% if post.title != "" %}
- [{{post.title}}]({{ post.url | prepend: site.baseurl }})
    {% endif %}
{% endfor %}
