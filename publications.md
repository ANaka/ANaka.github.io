---
title: Publications
layout: page
---

<h2>{{page.title}}</h2>
<p>{% for post in site.pubs reversed %}
	<p><strong>{{ post.title }}.</strong><br>
	<small>{{post.author_list}} </small><br>
	<small>{{post.venue}}, {{post.year}} <a href="{{ post.publisher_link }}">Link</a>
	<a href="{{ site.url }}/assets/files/{{post.pdf}}">PDF</a></small></p>
{% endfor %}
</p>
