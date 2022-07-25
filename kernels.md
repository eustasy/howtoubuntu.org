---
title: Kernels for Ubuntu
breadcrumb: kernels
---

## Release & Support Cycle
Release and support cycles are predominantly in two flavours, long and short. Short cycles practically require upgrades twice a year (similar to a modern Windows system, whereas Long cycles require major upgrades only after several years of stable operation. Because Ubuntu operates on a process of [Time Based Releases](https://wiki.ubuntu.com/TimeBasedReleases) with set deadlines, rather than waiting for all known issues to be resolved, both the release date and the presence of issues and bugs are reliable.

- Non-LTS: Released every **6 months**, supported for 9 months. 
- Every forth release is replaced by an LTS release.
- LTS: Released every **2 years**, supported for 5 years. (First point release after 4 months)

{% include icons/ubuntu-release-support-cycle.svg.html %}

## Most Recent Kernel Tutorials

{% assign mrk = 0 %}
{% for page in site.pages %}
{% if mrk < 10 %} 
{% if page.url contains 'how-to/install-linux-kernel' %}
{% unless page.url == '/how-to/install-linux-kernel/' %}

<hr>

### [{{ page.title }}]({{ page.url | relative_url }})

{{ page.excerpt | markdownify }}

{% increment mrk %}
{% endunless %}
{% endif %}
{% endif %}
{% endfor %}








