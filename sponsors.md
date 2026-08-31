---
layout: page
title: "Sponsors & Partners"
description: "2026 and 2025 sponsors of the Open Scientific Intelligence (OSI) Hackathon, plus how to become a 2026 partner."
keywords: "OSI Hackathon Sponsors, Partners, NSF, HuggingFace, Fum, LILA, AIChemy"
---

## 2026 partners

Confirmed so far for the October 21&ndash;22, 2026 edition &mdash; this list grows as conversations close.

<div class="sponsor-logos">
    {% for sponsor in site.data.sponsors.sponsors_2026 %}
    <img src="{{ sponsor.logo | relative_url }}" alt="{{ sponsor.alt }}" loading="lazy" decoding="async"{% if sponsor.url and sponsor.url != '#' %} onclick="window.open('{{ sponsor.url }}', '_blank')" style="cursor: pointer;"{% endif %}>
    {% endfor %}
</div>

<div class="sponsor-callout">
    <h3>We're looking for 2026 sponsors</h3>
    <p>Sponsorship funds prizes, site logistics, and the community papers that come out of every edition. If your organization wants in on the Open Scientific Intelligence Hackathon, we'd like to hear from you.</p>
    <a href="mailto:{{ site.links.main_organizer_email }}" class="cta-button">Reach out: {{ site.links.main_organizer_email }}</a>
</div>

## 2025 partners

The organizations who supported the 2025 edition:

<div class="sponsor-logos">
    {% for sponsor in site.data.sponsors.sponsors_2025 %}
    <img src="{{ sponsor.logo | relative_url }}" alt="{{ sponsor.alt }}" loading="lazy" decoding="async"{% if sponsor.url and sponsor.url != '#' %} onclick="window.open('{{ sponsor.url }}', '_blank')" style="cursor: pointer;"{% endif %}>
    {% endfor %}
</div>

- **LILA (Learning in Artificial Intelligence and Applications)** - Supporting AI research and applications
- **HuggingFace** - The leading platform for machine learning and AI models
- **AIChemy** - Advancing AI applications in chemistry and materials science
- **Cerebras** - First and only company in the world building AI hardware at wafer-scale.
- **FUM** - Transforming advanced materials market with AI-powered data infrastructure.
- **NSF** - Independent federal agency supporting science and engineering in all 50 states and U.S. territories.
- **Abstrax Tech** - Crafting innovative terpene-driven, functional flavor solutions through peer-reviewed research.
- **biostate.AI** - Transforming healthcare through next-generation RNAseq and GenAI.
