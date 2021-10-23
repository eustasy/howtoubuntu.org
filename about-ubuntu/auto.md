---
title: About Ubuntu (auto)
breadcrumb: about ubuntu (auto)
---

## Ubuntu Releases

#### Automatic

{% for release in site.data.releases %}
{% capture nowunix %}{{'now' | date: '%s'}}{% endcapture %}
{% capture posttime %}{{release.eol | date: '%s'}}{% endcapture %}
{% if posttime < nowunix %}
- Ubuntu {{ release.version }}{% if release.is-lts %} LTS{% endif %} ({{ release.name }})
{% else %}
- **Ubuntu {{ release.version }}{% if release.is-lts %} LTS{% endif %} ({{ release.name }})**
{% endif %}
{% endfor %}

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
