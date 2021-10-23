---
title: About Ubuntu (auto)
breadcrumb: about ubuntu (auto)
---

## Ubuntu Releases

{% assign sorted = site.data.releases | sort: 'eol' | reverse %}
{% for release in sorted %}

{% capture nowunix %}{{'now' | date: '%s'}}{% endcapture %}
{% capture posttime %}{{release.eol | date: '%s'}}{% endcapture %}
{% if posttime > nowunix %}
### Ubuntu {{ release.version }}{% if release.is-lts %} LTS{% endif %} ({{ release.name }})
- Supported until {{release.eol | date: '%B %Y'}}.{% if forloop.index < 2 %}{% if release.is-lts %}
- Recommended for most users.{% else %}
- Recommended for most users.{% endif %}{% else %}
- No longer recommended for new installs.{% if release.is-lts %}
- Users are recommended to use the newer LTS release that is less dated, while still being a mature system.{% endif %}{% endif %}{% endif %}

{% endfor %}

### Ubuntu 20.04 LTS (Focal Fossa)
- Supported until April 2025.
- Recommended for most users.
- [About Ubuntu 20.04 LTS (Focal Fossa)]({{ '/about-ubuntu/20-04-focal-fossa' | relative_url }})

### Ubuntu 21.10 (Impish Indri)
- Supported until July 2023.
- Recommended for users who want the latest software and hardware support.
- [About Ubuntu 21.10 (Impish Indri)]({{ '/about-ubuntu/21-10-impish-indri' | relative_url }})

### Ubuntu 21.04 (Hirsute Hippo)
- Supported until January 2022.
- No longer recommended for new installs.
- [About Ubuntu 21.04 (Hirsute Hippo)]({{ '/about-ubuntu/21-04-hirsute-hippo' | relative_url }})

### Ubuntu 18.04 LTS (Bionic Beaver)
- Supported until April 2023.
- No longer recommended for new installs.
- It has now recieved its last planned Kernel upgrade, and any newer hardware will remain unsupported through its lifespan.
- Users are recommended to use the newer LTS release that is less dated, while still being a mature system.
- [About Ubuntu 18.04 LTS (Bionic Beaver)]({{ '/about-ubuntu/18-04-bionic-beaver' | relative_url }})

### Ubuntu Server
- [About Ubuntu Server]({{ '/about-ubuntu/server' | relative_url }})

#### Automatic

{% for release in site.data.releases %}{% capture nowunix %}{{'now' | date: '%s'}}{% endcapture %}{% capture posttime %}{{release.eol | date: '%s'}}{% endcapture %}
- {% if posttime > nowunix %}**{% endif %}Ubuntu {{ release.version }}{% if release.is-lts %} LTS{% endif %} ({{ release.name }}){% if posttime > nowunix %}**{% endif %}{% endfor %}

#### Manual
- Ubuntu 4.10 (Warty Warthog)
- Ubuntu 5.04 (Hoary Hedgehog)
- Ubuntu 5.10 (Breezy Badger)
- Ubuntu 6.06 LTS (Dapper Drake)
- Ubuntu 6.10 (Edgy Eft)
- Ubuntu 7.04 (Feisty Fawn)
- Ubuntu 7.10 (Gutsy Gibbon)
- Ubuntu 8.04 LTS (Hardy Heron)
- Ubuntu 8.10 (Intrepid Ibex)
- Ubuntu 9.04 (Jaunty Jackalope)
- Ubuntu 9.10 (Karmic Koala)
- Ubuntu 10.04 LTS (Lucid Lynx)
- Ubuntu 10.10 (Maverick Meerkat)
- Ubuntu 11.04 (Natty Narwhal)
- Ubuntu 12.04 LTS (Precise Pangolin)
- Ubuntu 12.10 (Quantal Quetzal)
- Ubuntu 13.04 (Raring Ringtail)
- Ubuntu 13.10 (Saucy Salamander)
- Ubuntu 14.04 LTS (Trusty Tahr)
- Ubuntu 14.10 (Utopic Unicorn)
- Ubuntu 15.04 (Vivid Vervet)
- Ubuntu 15.10 (Wily Werewolf)
- Ubuntu 16.04 LTS (Xenial Xerus)
- Ubuntu 16.10 (Yakkety Yak)
- Ubuntu 17.04 (Zesty Zapus)
- Ubuntu 17.10 (Artful Aardvark)
- **Ubuntu 18.04 LTS (Bionic Beaver)**
- Ubuntu 18.10 (Cosmic Cuttlefish)
- Ubuntu 19.04 (Disco Dingo)
- Ubuntu 19.10 (Eoan Ermine)
- **Ubuntu 21.04 LTS (Focal Fossa)**
- Ubuntu 20.10 (Groovy Gorilla)
- **Ubuntu 21.04 (Hirsute Hippo)**
- **Ubuntu 21.10 (Impish Indri)**
