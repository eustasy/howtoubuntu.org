---
title: Tutorials for Ubuntu
breadcrumb: how to
---

{% for page in site.pages %}
{% if page.url contains 'how-to' and page.url != '/how-to/' unless page.url contains 'install-linux-kernel' %}

<hr>

### [{{ page.title }}]({{ page.url | relative_url }})

{{ page.excerpt | markdownify }}

{% endif %}
{% endfor %}
