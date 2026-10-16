---
layout: page
title: "Sponsors & Partners"
description: "2026 and 2025 sponsors of the Open Scientific Intelligence (OSI) Hackathon, presented by the Materials Discovery Research Institute, plus how to become a partner."
keywords: "OSI Hackathon Sponsors, Partners, Materials Discovery Research Institute, UL Research Institutes, Valency, NVIDIA, Hugging Face, Labric, Adaption, Green Dynamics, NSF, NIST, Globus"
---

## 2026 sponsors

The October 21&ndash;22, 2026 Open Scientific Intelligence Hackathon is presented by the **Materials Discovery Research Institute**, with support from:

{% include sponsor-logos.html sponsors=site.data.sponsors.sponsors_2026 %}

{% for sponsor in site.data.sponsors.sponsors_2026 %}
- **[{{ sponsor.name }}]({{ sponsor.url }})** - {{ sponsor.blurb }}
{%- endfor %}

{% assign organizer = site.data.sponsors.organizer %}
<p class="sponsor-organizer">Organized at the <a href="{{ organizer.url }}" target="_blank" rel="noopener noreferrer">{{ organizer.name }}</a> <a href="{{ organizer.url }}" target="_blank" rel="noopener noreferrer" title="{{ organizer.name }}"><img src="{{ organizer.logo | relative_url }}" alt="{{ organizer.alt }}" loading="lazy" decoding="async"></a></p>

<div class="sponsor-callout">
    <h3>Want to support the hackathon?</h3>
    <p>Sponsorship funds prizes, site logistics, and the community papers that come out of every edition. If your organization wants in on the Open Scientific Intelligence Hackathon, we'd like to hear from you.</p>
    <a href="mailto:{{ site.links.main_organizer_email }}" class="cta-button">Reach out: {{ site.links.main_organizer_email }}</a>
</div>

## 2025 sponsors

The organizations who supported the 2025 edition:

{% include sponsor-logos.html sponsors=site.data.sponsors.sponsors_2025 %}

{% for sponsor in site.data.sponsors.sponsors_2025 %}
- **[{{ sponsor.name }}]({{ sponsor.url }})** - {{ sponsor.blurb }}
{%- endfor %}
