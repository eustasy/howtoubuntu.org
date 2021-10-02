---
title: Tutorials
breadcrumb: how to
---

{% assign category = 'how to' %}

{% for page in site.pages %}
	{% if page.categories contains {{category}}  %}
		<a href="{{ site.baseurl }}{{ page.url }}">{{ page.title }}</a>
	{% endif %}
{% endfor %}
