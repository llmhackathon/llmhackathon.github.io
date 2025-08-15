---
layout: home
title: "LLM Hackathon for Applications in Materials Science & Chemistry"
description: "Join the LLM Hackathon for Applications in Materials Science & Chemistry. A 48-hour hybrid international hackathon to innovate with Large Language Models."
keywords: "LLM, Hackathon, Materials Science, Chemistry, AI, Large Language Models, Innovation, Hybrid Hackathon, Online Hackathon, In-person Hackathon"
---

<section id="home" class="hero">
    <div class="hero-content">
        <div class="hero-text">
            <h1><span id="first-line">Learn, Build,</span><br><span id="second-line">Innovate</span></h1>
            <h2>LLM Hackathon for <span>Applications in Materials Science & Chemistry</span></h2>
            <p class="tagline">A hybrid international hackathon connecting researchers from across the globe to
                explore and help solve the biggest problems in materials science and chemistry.</p>
            <a target="_blank" rel="noopener" href="{{ site.links.registration }}" class="cta-button-large">Register
                Now</a>
            <a rel="noopener noreferrer" href="{{ site.links.slack }}" target="_blank"
                class="secondary-cta">Join Slack</a>
        </div>
        <div class="hero-image">
            <img src="{{ '/assets/images/hero-image.png' | relative_url }}" alt="Abstract illustration representing AI and coding.">
        </div>
    </div>
</section>

<section id="about" class="about-section">
    <div class="about-image">
        <img src="{{ '/assets/images/date-calendar.png' | relative_url }}"
            alt="Calendar showing hackathon dates {{ site.event.dates }}.">
    </div>
    <div class="about-content">
        <h2>About The <span>Hackathon</span></h2>
        <p>Join us for an event dedicated to solving critical challenges in materials science and chemistry
            using the power of Large Language Models, data, agents, and more. This event brings together the
            brightest minds from
            academia and industry for a ~24-hour hybrid international hackathon (in-person + online).</p>
        <div id="countdown" class="countdown-timer"></div>
    </div>
</section>

<section id="sponsors" class="sponsors-section">
    <h2 style="margin-bottom:20px;">Our <span>Partners</span></h2>
    <div class="sponsor-logos">
        {% for sponsor in site.data.sponsors.partners %}
        <img src="{{ sponsor.logo | relative_url }}" alt="{{ sponsor.alt }}"{% if sponsor.url and sponsor.url != '#' %} onclick="window.open('{{ sponsor.url }}', '_blank')" style="cursor: pointer;"{% endif %}>
        {% endfor %}
    </div>
</section>

<section id="schedule" class="schedule-section">
    <h2 style="margin-bottom:40px;">Hackathon <span>Schedule</span></h2>
    <div class="schedule-timeline">
        {% for item in site.data.schedule.items %}
        <div class="schedule-item">
            <div class="schedule-time">{{ item.time }}</div>
            <div class="schedule-details">
                <h4>{{ item.title }}</h4>
                <p>{{ item.description }}</p>
            </div>
        </div>
        {% endfor %}
    </div>
</section>

<section id="prizes" class="prizes-section">
    <h2 style="margin-bottom:40px;">Prizes <span>& More</span></h2>
    <div class="prize-grid">
        {% for prize in site.data.prizes.main_prizes %}
        <div class="prize-card">
            <p class="amount">{{ prize.amount }}</p>
            <h4>{{ prize.title }}</h4>
            <p>{{ prize.description }}</p>
        </div>
        {% endfor %}
    </div>
</section>

<section id="faq" class="faq-section-home">
    <h2 style="margin-bottom:40px;">Frequently Asked <span>Questions</span></h2>
    {% for faq in site.data.faq-home.questions %}
    <div class="faq-item">
        <button class="faq-question">{{ faq.question }}</button>
        <div class="faq-answer">
            <p>{{ faq.answer }}</p>
        </div>
    </div>
    {% endfor %}
</section>
