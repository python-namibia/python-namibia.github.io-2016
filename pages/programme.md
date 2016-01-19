---
layout: page-fullwidth
title: "Programme"
permalink: "/programme/"
---

**Please note:** this programme of talks is still subject to change - we expect to add a few more to the schedule, and some times/days may change.


{% assign schedule = site.schedule | sort: 'date' %}

<div class="row">
  <div class="large-6 columns">
      <h3>Monday 25th: workshops</h3>
      <ul>
          {% for post in schedule %}
            {% if post.day == "Monday" %}
              <li>
                {% if {{post.speaker}} %}{{post.speaker}}: {% endif %} <a href="{{ post.url}}"><em>{{post.title}}</em></a>
              </li>
            {% endif %}
          {% endfor %}
      </ul>
  </div>

  <div class="large-6 columns">
      <h3>Tuesday 26th: talks</h3>
      <ul>
          {% for post in schedule %}
            {% if post.day == "Tuesday" %}
              <li>
                {% if {{post.speaker}} %}{{post.speaker}}: {% endif %} <a href="{{ post.url}}"><em>{{post.title}}</em></a> {% if {{post.location}} %} ({{post.location}}: {{post.date | date: "%H:%M"}}) {% endif %}
              </li>
            {% endif %}
          {% endfor %}
      </ul>
  </div>
</div>

<div class="row">
  <div class="large-6 columns">
      <h3>Wednesday 27th: talks</h3>
      <ul>
          {% for post in schedule %}
            {% if post.day == "Wednesday" %}
              <li>
                {% if {{post.speaker}} %}{{post.speaker}}: {% endif %} <a href="{{ post.url}}"><em>{{post.title}}</em></a> {% if {{post.location}} %} ({{post.location}}: {{post.date | date: "%H:%M"}}) {% endif %}
              </li>
            {% endif %}
          {% endfor %}
      </ul>
  </div>
  <div class="large-6 columns">
      <h3>Thursday 28th: workshops</h3>
      <ul>
          {% for post in schedule %}
            {% if post.day == "Thursday" %}
              <li>
                {% if {{post.speaker}} %}{{post.speaker}}: {% endif %} <a href="{{ post.url}}"><em>{{post.title}}</em></a>
              </li>
            {% endif %}
          {% endfor %}
      </ul>
  </div>
</div>
<div class="row">
  <div class="large-12 columns">
      <h3>Friday: excursion</h3>
      A social event to see a little bit of Namibia beyond the city of Windhoek.
  </div>
</div>


{% assign days = "Monday,Tuesday,Wednesday,Thursday,Friday" | split: "," %}
