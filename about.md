---
layout: page
title: "About The Hackathon"
description: "Learn more about the LLM Hackathon for Applications in Materials Science & Chemistry. Discover our mission, goals, and what makes this event unique."
keywords: "About LLM Hackathon, Materials Science AI, Chemistry AI, Hackathon Mission, Event Goals"
---

## LLM Hackathon for Applications in Materials Science & Chemistry

Recently Large-language models (LLMs) caught the interest of many scientists. Recent studies suggested that these models could be useful in chemistry and materials science. To explore these possibilities, we started organizing a hackathon to showcase LLM applications in materials science and chemistry back in 2023 showcasing 14 examples of LLM applications published in [**Digital Discovery**](https://doi.org/10.1039/D3DD00113J). In 2024, 34 projects were submitted across 7 on-sites and virtually which can be found in [**arXiv**](https://arxiv.org/abs/2411.15221).

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
            {% if site.data.team.organizer.social.email and site.data.team.organizer.social.email != "#" %}
            <a aria-label="email" href="mailto:{{ site.data.team.organizer.social.email }}"><i class="fas fa-envelope"></i></a>
            {% endif %}
        </div>
    </div>
</div>

## Volunteers

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
            {% if volunteer.social.email and volunteer.social.email != "#" %}
            <a aria-label="email" href="mailto:{{ volunteer.social.email }}"><i class="fas fa-envelope"></i></a>
            {% endif %}
        </div>
    </div>
    {% endfor %}
</div>