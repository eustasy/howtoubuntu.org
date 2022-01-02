---
title: Applications for Ubuntu
breadcrumb: install update upgrade to the latest version of
---

{% for page in site.pages %}
{% if page.url contains 'how-to/install-update-upgrade-to-the-latest-version-of' and page.url != '/how-to/install-update-upgrade-to-the-latest-version-of/' %}

<hr>

### [{{ page.title }}]({{ page.url | relative_url }})

{{ page.excerpt | markdownify }}

{% endif %}
{% endfor %}
