---
layout: page
title: Speaking
---

Speaking at tech conferences is a great way of sharing knowledge. I keep on gathering experience in this area in the course of a last year.

{% if site.data.future_talks.size > 0 %}
---
### Future talks:
<div class="talks">
<ul>
{% for talk in site.data.future_talks %}
	<li>
		<div class="talk-slides">
  			<a href={{ talk.slides }}><img src={{ talk.preview }} alt= {{ talk.title }}></a>
		</div>
		<div class="talk-info">
			<h4>{{ talk.title }}</h4>
			<p><i class="fa fa-comments"></i> <a href={{ conference.link }}>{{ talk.conference.name }}</a></p>
			<p><i class="fa fa-map-signs"></i> {{ talk.place }}</p>
			<p><i class="fa fa-calendar-check-o"></i> {{ talk.date | date: "%B %-d, %Y" }}</p>
			{% if talk.video %}
            	<p><i class="fa fa-cloud-upload"></i> <a href={{ talk.video }}>Recorded Video</a></p>
            {% endif %}
			{% if talk.code %}
            	<p><i class="fa fa-code"></i> <a href={{ talk.code }}>Code</a></p>
            {% endif %}
		</div>
	</li>
{% endfor %}
</ul>
</div>
---
### Past talks:  	
{% else %}
---
{% endif %}
<div class="talks">
<ul>
{% for talk in site.data.talks %}
	<li>
		<div class="talk-slides">
  			<a href={{ talk.slides }}><img src={{ talk.preview }} alt= {{ talk.title }}></a>
		</div>
		<div class="talk-info">
			<h4>{{ talk.title }}</h4>
			<p><i class="fa fa-comments"></i> <a href={{ conference.link }}>{{ talk.conference.name }}</a></p>
			<p><i class="fa fa-map-signs"></i> {{ talk.place }}</p>
			<p><i class="fa fa-calendar-check-o"></i> {{ talk.date | date: "%B %-d, %Y" }}</p>
			{% if talk.video %}
            	<p><i class="fa fa-cloud-upload"></i> <a href={{ talk.video }}>Recorded Video</a></p>
            {% endif %}
			{% if talk.code %}
            	<p><i class="fa fa-code"></i> <a href={{ talk.code }}>Code</a></p>
            {% endif %}
		</div>
	</li>
{% endfor %}
</ul>
</div>