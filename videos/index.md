---
title: Videos about Ubuntu
breadcrumb: videos
---

{% for page in site.pages %}
{% if page.url contains 'videos' %}
{% unless page.url == '/videos/' %}

<hr>

### [{{ page.title }}]({{ page.url | relative_url }})

{{ page.excerpt | markdownify }}

{% endunless %}
{% endif %}
{% endfor %}
