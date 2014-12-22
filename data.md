---
layout: default
---

{% for person_hash in site.data.people %}
{% assign person = person_hash[1] %}
  <li>
    <a href="https://github.com/{{ person.username }}">
      {{ person.name }}
    </a>
  </li>
{% endfor %}
