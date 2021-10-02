---
title: Tutorials
breadcrumb: how to
---

{% assign category = 'how to' %}

{% for post in site.posts %}
	{% if post.categories contains {{category}}  %}
		<a href="{{ site.baseurl }}{{ post.url }}">{{ post.title }}</a>
	{% endif %}
{% endfor %}
