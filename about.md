---
layout: page
title: "About The Hackathon"
description: "Learn more about the Open Scientific Intelligence (OSI) Hackathon for the Physical Sciences & Mathematics — formerly the LLM Hackathon for Materials Science & Chemistry. Discover our mission, goals, and what makes this event unique."
keywords: "About OSI Hackathon, Open Scientific Intelligence, LLM Hackathon, Materials Science AI, Chemistry AI, Hackathon Mission, Event Goals"
---

## Open Scientific Intelligence (OSI) Hackathon for the Physical Sciences & Mathematics

Large language models (LLMs) sparked the interest of many scientists for the possibility of enabling previously intractable applications. To explore those possibilities in materials science and chemistry, we organized an annual hackathon — the LLM Hackathon for Applications in Materials Science & Chemistry. In 2023, the results showed 14 examples of LLM applications published in [**Digital Discovery**](https://doi.org/10.1039/D3DD00113J). In 2024, 34 projects were submitted across 7 on-sites and virtually, documented on [**arXiv**](https://arxiv.org/abs/2411.15221). In 2025, 120 projects were submitted across 16 sites, documented in [**From Knowledge to Action**](https://arxiv.org/abs/2605.03205).

Starting with the **October 21–22, 2026** edition, the event becomes the **Open Scientific Intelligence (OSI) Hackathon**: the frontier has moved past language models alone, and so has the hackathon. The scope expands from materials science and chemistry to the **physical sciences and mathematics**, and LLMs, autonomous agents, datasets, benchmarks, models, and scientific software are all fair game.

## Organizing Team

<div class="team-grid organizer-grid">
    <div class="team-card organizer-card">
        <img src="{{ '/assets/images/organizers/' | append: site.data.team.organizer.image | split: '/' | last | prepend: '/assets/images/organizers/' | relative_url }}" alt="Organizer Image">
        <h5>{{ site.data.team.organizer.name }}</h5>
        <p><b>{{ site.data.team.organizer.title }}</b><br>{{ site.data.team.organizer.affiliation }}</p>
        <div class="social-links">
            {% if site.data.team.organizer.social.website and site.data.team.organizer.social.website != "#" %}
            <a target="_blank" aria-label="globe" rel="noopener" href="{{ site.data.team.organizer.social.website }}"><i class="fas fa-globe"></i></a>
            {% endif %}
            {% if site.data.team.organizer.social.twitter and site.data.team.organizer.social.twitter != "#" %}
            <a target="_blank" aria-label="twitter" rel="noopener" href="{{ site.data.team.organizer.social.twitter }}"><i class="fab fa-twitter"></i></a>
            {% endif %}
            {% if site.data.team.organizer.social.github and site.data.team.organizer.social.github != "#" %}
            <a target="_blank" aria-label="github" rel="noopener" href="{{ site.data.team.organizer.social.github }}"><i class="fab fa-github"></i></a>
            {% endif %}
            {% if site.data.team.organizer.social.linkedin and site.data.team.organizer.social.linkedin != "#" %}
            <a target="_blank" aria-label="linkedin" rel="noopener" href="{{ site.data.team.organizer.social.linkedin }}"><i class="fab fa-linkedin"></i></a>
            {% endif %}
            {% if site.data.team.organizer.social.email and site.data.team.organizer.social.email != "#" %}
            <a aria-label="email" href="mailto:{{ site.data.team.organizer.social.email }}"><i class="fas fa-envelope"></i></a>
            {% endif %}
            
        </div>
    </div>
</div>

<div class="team-grid volunteer-grid">
    {% for volunteer in site.data.team.volunteers %}
    <div class="team-card volunteer-card">
        <img src="{{ volunteer.image | relative_url }}" alt="Volunteer Image">
        <h5>{{ volunteer.name }}</h5>
        <div class="social-links volunteer-social-links">
            {% if volunteer.social.website and volunteer.social.website != "#" %}
            <a target="_blank" aria-label="globe" rel="noopener" href="{{ volunteer.social.website }}"><i class="fas fa-globe"></i></a>
            {% endif %}
            {% if volunteer.social.twitter and volunteer.social.twitter != "#" %}
            <a target="_blank" aria-label="twitter" rel="noopener" href="{{ volunteer.social.twitter }}"><i class="fab fa-twitter"></i></a>
            {% endif %}
            {% if volunteer.social.github and volunteer.social.github != "#" %}
            <a target="_blank" aria-label="github" rel="noopener" href="{{ volunteer.social.github }}"><i class="fab fa-github"></i></a>
            {% endif %}
            {% if volunteer.social.linkedin and volunteer.social.linkedin != "#" %}
            <a target="_blank" aria-label="linkedin" rel="noopener" href="{{ volunteer.social.linkedin }}"><i class="fab fa-linkedin"></i></a>
            {% endif %}
            {% if volunteer.social.email and volunteer.social.email != "#" %}
            <a aria-label="email" href="mailto:{{ volunteer.social.email }}"><i class="fas fa-envelope"></i></a>
            {% endif %}
        </div>
    </div>
    {% endfor %}
</div>

## Acknowledgement

We would like to thank all our sponsors, partners, and volunteers for their incredible support in making this event possible. A special thanks to all the participants for their enthusiasm and dedication. We are excited to see the innovative solutions you will create!
