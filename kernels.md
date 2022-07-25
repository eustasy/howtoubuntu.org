---
title: Kernels for Ubuntu
breadcrumb: kernels
---

## Supported Ubuntu Kernels

{% assign first_lts = 1 %}
{% assign first_non_lts = 1 %}
{% assign sorted = site.data.kernels | sort: 'released' | reverse %}
{% for kernel in sorted %}
{% capture nowunix %}{{'now' | date: '%s'}}{% endcapture %}
{% capture eol %}{{kernel.eol | date: '%s'}}{% endcapture %}
{% if eol > nowunix %}
{% capture nicename %}Ubuntu Kernel {{ kernel.name }}{% if kernel.is-lts %} LTS{% endif %}{% endcapture %}
{% capture url %}{{ kernel.version }}{% endcapture %}
{% assign url = url | slugify %}
{% assign url = '/how-to/install-linux-kernel/' | append: url %}

### {{ nicename }}
- Supported until **{{kernel.eol | date: '%B %Y'}}**.{% if kernel.is-lts and first_lts > 0 %}
- **Latest LTS kernel**.{% assign first_lts = 0 %}{% elsif kernel.is-lts %}
- Previous LTS kernel release, users are recommended to use the newer LTS release.{% elsif first_non_lts > 0 %}
- Recommended for users who want the latest software and hardware support.{% assign first_non_lts = 0 %}{% else %}
- No longer recommended for new installs.{% endif %}
- [Install {{ nicename }}]({{ url | relative_url }})

{% endif %}
{% endfor %}

## Ubuntu Kernel Support Lifecycle

{% include icons/ubuntu-kernel-support-lifecycle.svg.html %}
