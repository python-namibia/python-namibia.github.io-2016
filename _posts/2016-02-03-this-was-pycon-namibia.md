---
layout: page
title: "This was PyCon Namibia 2016"
date: 2016-02-03
excerpt: "A look back at 2016's successful PyCon Namibia"

rows1:
- column_width: 6
  widgets:
    - text: "Talks, day one"
      image: talks.jpg

    - text: "Django Girls"
      image: /django-girls.jpg

rows2:
- column_width: 6
  widgets:
    - text: "Gabriel Nhinda: advice for visitors"
      image: gabriel.jpg

    - text: "Lightning talks - the queue"
      image: /queue.jpg

rows3:
- column_width: 6
  widgets:
    - text: "Jessica & Vincent at NBC"
      image: NBC-radio.jpg

    - text: "PyCon Namibia on TV"
      image: /NBC-tv.jpg
---

Some figures
============

On 25th January 2016, PyCon Namibia opened its doors at the [University of Namibia](http://unam.edu.na) in Windhoek to:

* 118 attendees
* ... including visitors from South Africa, Zimbabwe, Zambia, Nigeria, UK, Netherlands, Germany, Canada, USA and Brazil
* 63 Namibian students
* 32 Django Girls
* ... for four days of talks and workshops

Talks
=====

The [talks](/programme) opened with a stirring keynote address by **Loek van Gent**, one of the participants in last year's event.

It was followed by talks covering a wide range of Python-related topics - its application in fields including mathematics and physics, programming theory, Python tools, libraries and techniques, web applications in Plone and Django, Python in African contexts, and Python in business, amongst others.

Workshops
=========

The two days of workshops (bookending the talks) began with a day-long [Django Girls](http://djangogirls.org) workshop, in parallel with various other introductory Python sessions aimed at ensuring participants had some key basic skills and knowledge to help them follow the talks.

The second day of workshops was more advanced and covered more specific topics, including [django CMS](http://django-cms.org), [Conda](http://conda.pydata.org/docs/), [Hypothesis](https://hypothesis.readthedocs.org) and WebSockets.

{% for row in page.rows1 %}
  <div class="row t60">

    {% for widget in row.widgets %}

      <div class="medium-{{ row.column_width }} columns frontpage-widget">
      	{% capture widget_url %}{% if widget.url contains 'http' %}{{ widget.url }}{% else %}{{ site.url }}{{ site.baseurl }}{{ widget.url }}{% endif %}{% endcapture %}

      	{% if widget.url %}
      		<a href="{{ widget_url }}">
      			{% if widget.image %}
      				{%comment%}TODO lazy loading{%endcomment%}
      				{%comment%}<img class="lazy" data-src="{{ site.urlimg }}{{ widget.image }}" width="100%" alt="" />{%endcomment%}
      				{%comment%}<noscript>{%endcomment%}
      					<img src="{{ site.urlimg }}{{ widget.image }}" width="100%" alt="" />
      				{%comment%}</noscript>{%endcomment%}
      			{% endif %}
      			{% if widget.video %}{{ widget.video }}{% endif %}
      		</a>
      	{% else %}
      			{% if widget.image %}
      				{%comment%}TODO lazy loading{%endcomment%}
      				{%comment%}<img class="lazy" data-src="{{ site.urlimg }}{{ widget.image }}" width="100%" alt="" />{%endcomment%}
      				{%comment%}<noscript>{%endcomment%}
      					<img src="{{ site.urlimg }}{{ widget.image }}" width="100%" alt="" />
      				{%comment%}</noscript>{%endcomment%}
      			{% endif %}
      	{% endif %}

      	<h2 class="font-size-h3 t10">{{ widget.title }}</h2>
      	<p>{{ widget.text }}</p>
      	{% if widget.url %}
      	  <p><a class="button tiny radius" href="{% if widget.url contains 'http' %}{{ widget.url }}{% else %}{{ site.url }}{{ site.baseurl }}{{ widget.url }}{% endif %}">{{ site.data.language.more }}</a></p>
        {% endif %}
      </div>
    {% endfor %}
  </div>
{% endfor %}

Raspberry PiLab
===============

Thanks to the support of Cardiff University's [Phoenix Project](http://www.cardiff.ac.uk/phoenix-project/home) and a grant from the [Python Software Foundation](https://www.python.org/psf/) the conference workshops were equipped with a teaching laboratory of 50 [Raspberry Pi](http://raspberrypi.org) computers, supplied at a generous discount by [The PiHut](http://thepihut.com).

Our PiLab of pre-configured machines, with appropriate software already installed for the workshops and tutorials, turned out to be an invaluable resource. For many individuals, lack of access to *suitable* computer systems is as much of a barrier to participation in open-source development as a lack of resources in the first place.

At the end of the conference batches of the Raspberry Pis were handed over to new custodians, to be used for future teaching workshops, learning, experimentation and exploration. The recipients included the department of **Computer Science at UNAM**, **PyNam** (the Python Namibia Society), **PyZim** (Python Zimbabwe) and numerous individual attendees in the Namibian Python community, amongst them several Namibian high-school pupils who attended the conference.

Django Girls
============

As usual, the Django Girls formula of an installation party the day before the tutorial and a very high ratio of coaches to learners ensured that not only was the workshop itself a success, but that it made a significant contribution to the rest of the conference as well.

The new Django Girls attendees found themselves in a friendly and supportive cohort, that ensured their introduction to Python programming was as welcoming and possible, and set them up very well to get the best out of and participate in the days that followed.

Attendees at Django Girls Windhoek left with plans for new events across Africa, in **Lagos**, **Cape Town** and **Harare**.

Lightning talks
===============

Lightning talks were held at the close of each day; by the third day, as expected, many of the first-time attendees discovered that they had a lightning talk to contribute. As usual they covered a vast array of topics, and turned out to provide some of the most interesting material for the conference.

The lightning talks highlighted the depth of ambition and desire amongst attendees, who described their plans, and in some cases, some remarkable achievements already.

{% for row in page.rows2 %}
  <div class="row t60">

    {% for widget in row.widgets %}

      <div class="medium-{{ row.column_width }} columns frontpage-widget">
      	{% capture widget_url %}{% if widget.url contains 'http' %}{{ widget.url }}{% else %}{{ site.url }}{{ site.baseurl }}{{ widget.url }}{% endif %}{% endcapture %}

      	{% if widget.url %}
      		<a href="{{ widget_url }}">
      			{% if widget.image %}
      				{%comment%}TODO lazy loading{%endcomment%}
      				{%comment%}<img class="lazy" data-src="{{ site.urlimg }}{{ widget.image }}" width="100%" alt="" />{%endcomment%}
      				{%comment%}<noscript>{%endcomment%}
      					<img src="{{ site.urlimg }}{{ widget.image }}" width="100%" alt="" />
      				{%comment%}</noscript>{%endcomment%}
      			{% endif %}
      			{% if widget.video %}{{ widget.video }}{% endif %}
      		</a>
      	{% else %}
      			{% if widget.image %}
      				{%comment%}TODO lazy loading{%endcomment%}
      				{%comment%}<img class="lazy" data-src="{{ site.urlimg }}{{ widget.image }}" width="100%" alt="" />{%endcomment%}
      				{%comment%}<noscript>{%endcomment%}
      					<img src="{{ site.urlimg }}{{ widget.image }}" width="100%" alt="" />
      				{%comment%}</noscript>{%endcomment%}
      			{% endif %}
      	{% endif %}

      	<h2 class="font-size-h3 t10">{{ widget.title }}</h2>
      	<p>{{ widget.text }}</p>
      	{% if widget.url %}
      	  <p><a class="button tiny radius" href="{% if widget.url contains 'http' %}{{ widget.url }}{% else %}{{ site.url }}{{ site.baseurl }}{{ widget.url }}{% endif %}">{{ site.data.language.more }}</a></p>
        {% endif %}
      </div>
    {% endfor %}
  </div>
{% endfor %}

Local developers and professionals
==================================

One of the aims of this conference was not just to promote Python, but open-source software in general and for Python to be a catalyst for development of a Namibian open-source movement. PyCon Namibia drew a number of local web and software developers, many of whom were not already working in Python, but who wanted to participate in an open-source event in Namibia and meet other users of open-source software.

Media attention
===============

PyCon Namibia was considered a significant event, and was covered by national media.

Various members of the conference team were invited to appear in news broadcasts. Daniele Procida was interviewed by the [Namibian Broadcasting Corporation](http://www.nbc.na)'s Good Morning Namibia, and discussed subjects including open-source software and its implications for Africa, the global Python community and Django Girls.

Jessica Upani (Chair of PyNam) and Vincent Knight appeared on NBC Radio, where they where asked about a wide range of topics, notably the significance of open-source software for business development in Africa (and were asked to predict when the first world-sweeping web application would come out of Namibia).

The conference [was also mentioned in The Namibian](http://www.namibian.com.na/index.php?page=read&id=36147), Namibia's largest-circulation daily paper.

{% for row in page.rows3 %}
  <div class="row t60">

    {% for widget in row.widgets %}

      <div class="medium-{{ row.column_width }} columns frontpage-widget">
      	{% capture widget_url %}{% if widget.url contains 'http' %}{{ widget.url }}{% else %}{{ site.url }}{{ site.baseurl }}{{ widget.url }}{% endif %}{% endcapture %}

      	{% if widget.url %}
      		<a href="{{ widget_url }}">
      			{% if widget.image %}
      				{%comment%}TODO lazy loading{%endcomment%}
      				{%comment%}<img class="lazy" data-src="{{ site.urlimg }}{{ widget.image }}" width="100%" alt="" />{%endcomment%}
      				{%comment%}<noscript>{%endcomment%}
      					<img src="{{ site.urlimg }}{{ widget.image }}" width="100%" alt="" />
      				{%comment%}</noscript>{%endcomment%}
      			{% endif %}
      			{% if widget.video %}{{ widget.video }}{% endif %}
      		</a>
      	{% else %}
      			{% if widget.image %}
      				{%comment%}TODO lazy loading{%endcomment%}
      				{%comment%}<img class="lazy" data-src="{{ site.urlimg }}{{ widget.image }}" width="100%" alt="" />{%endcomment%}
      				{%comment%}<noscript>{%endcomment%}
      					<img src="{{ site.urlimg }}{{ widget.image }}" width="100%" alt="" />
      				{%comment%}</noscript>{%endcomment%}
      			{% endif %}
      	{% endif %}

      	<h2 class="font-size-h3 t10">{{ widget.title }}</h2>
      	<p>{{ widget.text }}</p>
      	{% if widget.url %}
      	  <p><a class="button tiny radius" href="{% if widget.url contains 'http' %}{{ widget.url }}{% else %}{{ site.url }}{{ site.baseurl }}{{ widget.url }}{% endif %}">{{ site.data.language.more }}</a></p>
        {% endif %}
      </div>
    {% endfor %}
  </div>
{% endfor %}

Hiccup
======

Day two of the conference began with the news that student protests over tuition fees at UNAM had locked down the University; there would be no events taking place that day.

A number of local people wryly told us: *Welcome to Africa* - but of course, student protests and [other unexpected events can disrupt conferences anywhere](http://2015.djangocon.eu/news/boy-band-disrupts-djangocon-europe/) in the world. In a testament to the African capacity for *Getting Things Done When They Need To Be Done*, within just 45 minutes of receiving confirmation of the lockdown the organising committee had been able to find and book an alternative venue for the following day, complete with catering and AV equipment and support.

Equally impressive was the reaction of the local community, with sponsors and other attendees rallying round with help, advice and offers of equipment.

The day following the enforced pause, PyCon Namibia was back on track, and we were back at UNAM for the final two days.

Thank-yous
==========

PyCon Namibia was made possible by the [University of Namibia](http://unam.edu.na), our hosts, and [Cardiff University](http://www.cardiff.ac.uk/)'s [Phoenix Project](http://www.cardiff.ac.uk/phoenix-project/home). Both universities contributed financially to the event, and supported the participation of members of staff as conference organisers.

[Divio AG](http://divio.com) contributed financially, through the open-source [django CMS](http://django-cms.org) project, and also supported the event through a very generous allocation of staff time.

The [Python](https://www.python.org/psf/) and [Django](https://www.djangoproject.com/foundation/)  Software Foundations made significant financial contributions.

Sponsors also included [Wildfish](http://wildfish.com/) in the UK, [Praekelt](http://praekeltfoundation.org/) (South Africa) and [IMS](http://www.ims.com.na) (Namibia).

Our organisers and volunteers worked tirelessly before and during the event, and contributed a great deal of time and effort to it.

Finally, we'd also like to thank our attendees for their enthusiastic participation, not least those who travelled long distances (36 hours by bus, in the case of our attendees from Zimbabwe - that's commitment) to be there.

PyCon Namibia 2017
==================

See you in Windhoek next year. We'll be there.

*The PyCon Namibia 2016 organising committee*