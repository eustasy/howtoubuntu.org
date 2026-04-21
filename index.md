---
---


<div class="featured-links">
	<!-- About Ubuntu (current version) - full width and first -->
	<a href="/about-ubuntu/26-04-resolute-raccoon/" class="featured-link about-ubuntu full-width">
		<div class="featured-title">About Ubuntu 26.04</div>
		<div class="featured-desc">Resolute Raccoon (LTS) – Released April 2026</div>
		<div class="featured-note">Learn about the latest LTS release.</div>
		<div class="featured-gradient"></div>
	</a>

	<!-- Releases -->
	<a href="/releases/" class="featured-link releases">
		<div class="featured-icon">{% include icons/history.svg.html %}</div>
		<div class="featured-title">Ubuntu Releases</div>
		<div class="featured-desc">All Ubuntu versions, LTS and standard.</div>
	</a>

	<!-- Kernels -->
	<a href="/kernels/" class="featured-link kernels">
		<div class="featured-icon">{% include icons/apps.svg.html %}</div>
		<div class="featured-title">Linux Kernels</div>
		<div class="featured-desc">Mainline and LTS kernel info & guides.</div>
	</a>

	<!-- Videos -->
	<a href="/videos/" class="featured-link videos">
		<div class="featured-icon">{% include icons/video.svg.html %}</div>
		<div class="featured-title">Ubuntu Videos</div>
		<div class="featured-desc">Watch guides, reviews, and explainers.</div>
	</a>
</div>

## Latest Tutorials

{% for page in site.pages %}
{% if page.url contains 'how-to/' %}
{% unless page.url contains 'install-linux-kernel' or page.url == '/how-to/' or page.url == '/how-to/install-update-upgrade-to-the-latest-version-of/' %}
<hr>

### [{{ page.title }}]({{ page.url | relative_url }})

{{ page.excerpt | markdownify }}

{% endunless %}
{% endif %}
{% endfor %}

### [All Tutorials &raquo;]({{ '/how-to/' | relative_url }})
{:.text-right}
