---
title: Kernels for Ubuntu
breadcrumb: kernels
---

## Ubuntu Kernel Support Lifecycle

{% include icons/ubuntu-kernel-support-lifecycle.svg.html %}

## Most Recent Kernel Tutorials

{% assign mrk = 0 %}
{% for page in site.pages %}
{% if mrk < 10 %} 
{% if page.url contains 'how-to/install-linux-kernel' %}
{% unless page.url == '/how-to/install-linux-kernel/' %}

<hr>

### [{{ page.title }}]({{ page.url | relative_url }})

{% increment mrk %}
{% endunless %}
{% endif %}
{% endif %}
{% endfor %}










{% assign first_lts = 1 %}
{% assign first_non_lts = 1 %}
{% assign sorted = site.data.releases | sort: 'eol' | reverse %}
{% for release in sorted %}

{% capture nowunix %}{{'now' | date: '%s'}}{% endcapture %}
{% capture posttime %}{{release.eol | date: '%s'}}{% endcapture %}
{% if posttime > nowunix %}
{% capture nicename %}Ubuntu {{ release.version }}{% if release.is-lts %} LTS{% endif %} ({{ release.name }}){% endcapture %}
{% capture url %}{{ release.version }}-{{ release.name }}{% endcapture %}
{% assign url = url | slugify %}
{% assign url = '/about-ubuntu/' | append: url %}

### {{ nicename }}
- Supported until {{release.eol | date: '%B %Y'}}.{% if release.is-lts and first_lts > 0 %}
- Recommended for most users.{% assign first_lts = 0 %}{% elsif release.is-lts %}
- No longer recommended for new installs.
- Users are recommended to use the newer LTS release.{% if release.point-releases.size > 4 %}
- It has now recieved its last planned Kernel upgrade, and any newer hardware will remain unsupported throughout its remaining lifespan.{% endif %}{% elsif first_non_lts > 0 %}
- Recommended for users who want the latest software and hardware support.{% assign first_non_lts = 0 %}{% else %}
- No longer recommended for new installs.{% endif %}
- [About {{ nicename }}]({{ url | relative_url }})

{% endif %}
{% endfor %}


{% for release in site.data.releases %}{% capture nowunix %}{{'now' | date: '%s'}}{% endcapture %}{% capture posttime %}{{release.eol | date: '%s'}}{% endcapture %}
- {% if posttime > nowunix %}**{% endif %}Ubuntu {{ release.version }}{% if release.is-lts %} LTS{% endif %} ({{ release.name }}){% if posttime > nowunix %}**{% endif %}{% endfor %}
