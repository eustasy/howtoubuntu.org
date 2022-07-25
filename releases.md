---
title: About Ubuntu
breadcrumb: about ubuntu
---

## Ubuntu Releases

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

### Ubuntu Server
- [About Ubuntu Server]({{ '/about-ubuntu/server' | relative_url }})

## Release & Support Cycle
Release and support cycles are predominantly in two flavours, long and short. Short cycles practically require upgrades twice a year (similar to a modern Windows system, whereas Long cycles require major upgrades only after several years of stable operation. Because Ubuntu operates on a process of [Time Based Releases](https://wiki.ubuntu.com/TimeBasedReleases) with set deadlines, rather than waiting for all known issues to be resolved, both the release date and the presence of issues and bugs are reliable.

- Non-LTS: Released every **6 months**, supported for 9 months. 
- Every forth release is replaced by an LTS release.
- LTS: Released every **2 years**, supported for 5 years. (First point release after 4 months)

{% include icons/ubuntu-release-support-cycle.svg.html %}

## Naming Ubuntu Releases

### Numbers
The numbers in the name relate to the year and month of release. 20.04 was released on the 4th month of the year 2020. Ubuntu 19.10 was released on the 10th month (October) of 2019. Releases are scheduled every six months, numbered as 18.04, 18.10, 19.04, 19.10, 20.04, etc. You may notice a third number in a LTS release name: these are point releases, that include newer hardware support from non-LTS releases that have been backported.

### Adjective Animal
Ubuntu release have always had the code-naming convention of an animal name as the second part, preceded by an adjective beginning with the same letter. Apart from the first few releases (back in 2004/5), they have been working through the alphabet. While the animals honored in this way are not necessarily unheard of, many of them are either uncommon or infamous in some way.
    
### Past Releases
**Bold** indicates a currently supported release.

{% for release in site.data.releases %}{% capture nowunix %}{{'now' | date: '%s'}}{% endcapture %}{% capture posttime %}{{release.eol | date: '%s'}}{% endcapture %}
- {% if posttime > nowunix %}**{% endif %}Ubuntu {{ release.version }}{% if release.is-lts %} LTS{% endif %} ({{ release.name }}){% if posttime > nowunix %}**{% endif %}{% endfor %}
