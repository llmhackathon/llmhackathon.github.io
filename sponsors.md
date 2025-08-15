---
layout: page
title: "Sponsors & Partners"
description: "Meet our sponsors and partners supporting the LLM Hackathon for Applications in Materials Science & Chemistry."
keywords: "LLM Hackathon Sponsors, Partners, LILA, HuggingFace, AIChemy"
---

<div class="sponsor-logos">
    {% for sponsor in site.data.sponsors.partners %}
    <img src="{{ sponsor.logo | relative_url }}" alt="{{ sponsor.alt }}"{% if sponsor.url and sponsor.url != '#' %} onclick="window.open('{{ sponsor.url }}', '_blank')" style="cursor: pointer;"{% endif %}>
    {% endfor %}
</div>

## Partner Information

Our hackathon is supported by leading organizations in the AI and materials science communities:

- **LILA (Learning in Artificial Intelligence and Applications)** - Supporting AI research and applications
- **HuggingFace** - The leading platform for machine learning and AI models
- **AIChemy** - Advancing AI applications in chemistry and materials science
- **Cerebras** - First and only company in the world building AI hardware at wafer-scale.
- **FUM** - Transforming advanced materials market with AI-powered data infrastructure.
- **NSF** - Independent federal agency supporting science and engineering in all 50 states and U.S. territories.

## Sponsorship Opportunities

Interested in sponsoring future events? Contact us at [{{ site.links.main_organizer_email }}](mailto:{{ site.links.main_organizer_email }}) to learn about partnership opportunities.
