---
title: Publications
layout: page
---

<h2>{{page.title}}</h2>
<p>{% for post in site.pubs reversed %}
	<p><strong>{{ post.title }}.</strong><br>
	<i>{{post.author_list}}</i><br>
	{{post.venue}}, {{post.year}} 
	<a href="{{ post.publisher_link }}">Link</a>
	<a href="{{ site.url }}/assets/files/{{post.pdf}}">PDF</a></p>
{% endfor %}
</p>
