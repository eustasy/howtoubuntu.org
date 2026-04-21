---
title: Kernels for Ubuntu
breadcrumb: kernels
---

## Ubuntu 26.04 LTS

Ubuntu 26.04 LTS updates the default Linux kernel from version 6.8 to 7.0.

- Ubuntu LTS releases ship with the Hardware Enablement (HWE) stack enabled.
- Since Ubuntu 24.10, crash dumps are enabled by default for desktop and server installations.
- Since Ubuntu 25.04, the `linux-lowlatency` binary package has been retired. The generic kernel can now tune responsiveness at boot time, so low-latency tuning is provided by `linux-generic` together with the `lowlatency-kernel` user-space package, which updates the GRUB command line.

For the current lifecycle table and Canonical kernel guidance, see [Ubuntu kernel lifecycle](https://ubuntu.com/kernel/lifecycle) and [Ubuntu kernels](https://ubuntu.com/kernel).

## Check HWE, Support, and Kernel Version

Ubuntu LTS releases use the Hardware Enablement stack so newer kernels can be delivered through the life of the release.

### Check your support status

```bash
hwe-support-status --verbose
```

### Check your kernel version

```bash
uname -r
cat /proc/version_signature
```

### Enable HWE

Since 2019, HWE has been on by default. You should not need to do this.

```bash
sudo apt-get install --install-recommends linux-generic-hwe-26.04
```

You can change the release at the end to any LTS release since 2020.

## Supported Ubuntu Kernels

<div class="warning">
	<h3>{% include icons/warning.svg.html %} &nbsp; Warning: Manual kernel installs are usually unnecessary</h3>
</div>
<div class="warning-sub">
	<p>These manual kernel installation guides may not be necessary for most Ubuntu systems. Ubuntu ships the HWE stack by default, so the recommended approach is usually to keep your system updated and let Ubuntu deliver the appropriate kernel through normal updates.</p>
</div>

{% assign first_lts = 1 %}
{% assign first_non_lts = 1 %}
{% assign sorted = site.data.kernels | sort: 'released' | reverse %}
{% for kernel in sorted %}
{% capture nowunix %}{{'now' | date: '%s'}}{% endcapture %}
{% capture eol %}{{kernel.eol | date: '%s'}}{% endcapture %}
{% if eol > nowunix %}
{% capture nicename %}Ubuntu Kernel {{ kernel.name }}{% if kernel.is-lts %} LTS{% endif %}{% endcapture %}
{% capture url %}{{ kernel.name }}{% endcapture %}
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
