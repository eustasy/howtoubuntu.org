---
---

## Latest Tutorials

{% for page in site.pages %}
{% if page.url contains 'how-to/' %}
{% unless page.url == '/how-to/' or page.url contains 'install-linux-kernel' %}

<hr>

### [{{ page.title }}]({{ page.url | relative_url }})

{{ page.excerpt | markdownify }}

{% endunless %}
{% endif %}
{% endfor %}

### [All Tutorials &raquo;]({{ '/how-to/' | relative_url }})
{:.text-right}
