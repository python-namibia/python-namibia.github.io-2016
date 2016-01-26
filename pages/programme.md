---
layout: page-fullwidth
title: "Programme"
permalink: "/programme/"
---

<h2>Thursday's talks will be held at <a href="http://www.safarihotelsnamibia.com/">Safari Hotel Conference centre</a> (Corner of Auas and Aviation Streets).</h2>


{% assign schedule = site.schedule | sort: 'date' %}

<div class="row">
  <div class="large-6 columns">
      <h3>Monday 25th: workshops</h3>
      <ul>
          {% for post in schedule %}
            {% if post.day == "Monday" %}
              <li>
                {% if {{post.date}} %}{{post.date | date: "%H:%M"}}: {% endif %}
                {% if {{post.speaker}} %}{{post.speaker}}: {% endif %} <a href="{{ post.url}}"><em>{{post.title}}</em></a>
                {% if {{post.location}} %} ({{post.location}}){% endif %}
              </li>
            {% endif %}
          {% endfor %}
      </ul>
  </div>

  <div class="large-6 columns">
      <h3>Wednesday 27th: talks</h3>
      <ul>
          {% for post in schedule %}
            {% if post.day == "Tuesday" %}
              <li>
                {% if {{post.date}} %}{{post.date | date: "%H:%M"}}: {% endif %}
                {% if {{post.speaker}} %}{{post.speaker}}: {% endif %} <a href="{{ post.url}}"><em>{{post.title}}</em></a>
                {% if {{post.location}} %} ({{post.location}}){% endif %}
              </li>
            {% endif %}
          {% endfor %}
      </ul>
  </div>
</div>

<div class="row">
  <div class="large-6 columns">
      <h3>Thursday 28th: talks</h3>
      <ul>
          {% for post in schedule %}
            {% if post.day == "Wednesday" %}
              <li>
                {% if {{post.date}} %}{{post.date | date: "%H:%M"}}: {% endif %}
                {% if {{post.speaker}} %}{{post.speaker}}: {% endif %} <a href="{{ post.url}}"><em>{{post.title}}</em></a>
                {% if {{post.location}} %} ({{post.location}}){% endif %}
              </li>
            {% endif %}
          {% endfor %}
      </ul>
  </div>
  <div class="large-6 columns">
      <h3>Friday 29th: workshops</h3>
      <ul>
          {% for post in schedule %}
            {% if post.day == "Thursday" %}
              <li>
                {% if {{post.date}} %}{{post.date | date: "%H:%M"}}: {% endif %}
                {% if {{post.speaker}} %}{{post.speaker}}: {% endif %} <a href="{{ post.url}}"><em>{{post.title}}</em></a>
                {% if {{post.location}} %} ({{post.location}}){% endif %}
              </li>
            {% endif %}
          {% endfor %}
      </ul>
  </div>
</div>


{% assign days = "Monday,Tuesday,Wednesday,Thursday,Friday" | split: "," %}
