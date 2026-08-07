---
layout: home
title: "Open Scientific Intelligence (OSI) Hackathon for Materials Science & Chemistry"
description: "The Open Scientific Intelligence (OSI) Hackathon returns October 2026. Formerly the LLM Hackathon — now covering agents, datasets, models, and scientific software for materials science and chemistry."
keywords: "OSI Hackathon, Open Scientific Intelligence, LLM Hackathon, Materials Science, Chemistry, AI, Agents, Datasets, Scientific Software, Hybrid Hackathon, October 2026"
---

<section id="home" class="hero">
    <div class="hero-content">
        <div class="hero-text">
            <p class="hero-announce"><span class="pulse-dot" aria-hidden="true"></span>Next edition &middot; October 2026 &middot; dates TBA</p>
            <h1>Open Scientific Intelligence Hackathon
                <span class="h1-sub">The OSI Hackathon &middot; for Materials Science &amp; Chemistry</span>
            </h1>
            <p class="tagline">Now covering more ground than LLMs: agents, datasets, models, and scientific software — all fair game against the biggest problems in materials science and chemistry. Free, hybrid, and international.</p>
            <div class="hero-actions">
                <a rel="noopener noreferrer" href="{{ site.links.slack }}" target="_blank" class="cta-button-large">Join the Slack — be first to know</a>
                <a href="{{ '/awards/' | relative_url }}" class="secondary-cta">See the 2025 awards</a>
            </div>
        </div>
        <div class="element-tile" role="img" aria-label="Periodic-table style element tile announcing the October 2026 edition of the OSI Hackathon">
            <div class="tile-number"><span>26</span><span class="tile-mass">Oct</span></div>
            <div class="tile-symbol">Osi</div>
            <div class="tile-name">OSI Hackathon</div>
            <div class="tile-detail">October 2026 &middot; dates TBA</div>
        </div>
    </div>
    <div class="hero-spectrum">
        {% include spectrum.html class="spectrum--glow spectrum--animated" %}
    </div>
</section>

<section class="stats-band" aria-label="Hackathon by the numbers">
    <div class="stats-band-inner">
        <div class="stat">
            <div class="stat-value">4th</div>
            <div class="stat-desc">edition returns October 2026</div>
        </div>
        <div class="stat">
            <div class="stat-value">34</div>
            <div class="stat-desc">projects submitted in 2024 alone</div>
        </div>
        <div class="stat">
            <div class="stat-value">2</div>
            <div class="stat-desc">community papers — Digital Discovery &amp; arXiv</div>
        </div>
        <div class="stat">
            <div class="stat-value">10+</div>
            <div class="stat-desc">on-site locations worldwide, plus virtual</div>
        </div>
    </div>
</section>

<section id="about" class="about-section">
    <figure class="about-image reveal">
        <img src="{{ '/assets/images/recap-2025.png' | relative_url }}" alt="Macro render of a glowing crystalline molecular lattice lit in sodium-amber and violet.">
        <figcaption>Where language models meet the lattice</figcaption>
    </figure>
    <div class="about-content reveal">
        <h2>About the <span>hackathon</span></h2>
        <div class="event-status-banner">
            <span class="status-dot" aria-hidden="true"></span>
            <span>2025 wrapped &middot; 2026 in planning</span>
        </div>
        <p>Every year, this hackathon brings together materials scientists, chemists, and AI researchers from around the world for an intense sprint: build something real, in teams, across time zones and on-site locations.</p>
        <p>Three editions in, the frontier has moved past language models alone — so the event has too. As the <strong>Open Scientific Intelligence (OSI) Hackathon</strong>, the 2026 edition welcomes everything that makes science machines smarter: LLMs, autonomous agents, datasets, benchmarks, models, and scientific software.</p>
        <p>The 2025 edition produced automated research assistants, novel data pipelines, and agentic lab workflows — explore them on the <a href="{{ '/awards/' | relative_url }}">awards page</a>. The next edition lands in <strong>October 2026</strong>; exact dates are being finalized. Join the <a rel="noopener noreferrer" target="_blank" href="{{ site.links.slack }}">Slack community</a> to hear first, find teammates, or propose hosting a site.</p>
    </div>
</section>

<section class="editions-section" aria-label="Past and upcoming editions">
    <div class="editions-inner reveal">
        <h2>Four <span>editions</span> and counting</h2>
        <div class="edition-row">
            <div class="edition-year">2023</div>
            <div class="edition-body">
                <h3>The proof of concept</h3>
                <p>14 LLM applications built in a single sprint, published as a peer-reviewed paper in Digital Discovery.</p>
            </div>
            <a class="edition-link" href="https://doi.org/10.1039/D3DD00113J" target="_blank" rel="noopener noreferrer">Read the paper &rarr;</a>
        </div>
        <div class="edition-row">
            <div class="edition-year">2024</div>
            <div class="edition-body">
                <h3>Going global</h3>
                <p>34 projects across 7 on-site locations and a worldwide virtual cohort, documented on arXiv.</p>
            </div>
            <a class="edition-link" href="https://arxiv.org/abs/2411.15221" target="_blank" rel="noopener noreferrer">Read the paper &rarr;</a>
        </div>
        <div class="edition-row">
            <div class="edition-year">2025</div>
            <div class="edition-body">
                <h3>Agents arrive</h3>
                <p>Agentic workflows, tool use, and lab automation took center stage across 10+ sites.</p>
            </div>
            <a class="edition-link" href="{{ '/awards/' | relative_url }}">See the awards &rarr;</a>
        </div>
        <div class="edition-row edition-row--next">
            <div class="edition-year">2026</div>
            <div class="edition-body">
                <h3>Next: the OSI Hackathon &middot; October 2026</h3>
                <p>The event becomes the Open Scientific Intelligence Hackathon — beyond LLMs, agents, datasets, models, and scientific software are all fair game. Dates are being finalized and will be announced on Slack first.</p>
            </div>
            <a class="edition-link" rel="noopener noreferrer" target="_blank" href="{{ site.links.slack }}">Get notified &rarr;</a>
        </div>
    </div>
</section>

<section id="videos" class="videos-section">
    <div class="reveal">
    <h2 style="text-align:left;">Featured <span>videos</span></h2>
    <div class="videos-grid">
        {% for video in site.data.videos.videos %}
        <div class="video-card" onclick="openVideoModal('{{ video.youtube_id }}', '{{ video.title }}')">
            <div class="video-thumbnail">
                <img src="{{ video.thumbnail }}" alt="{{ video.title }}" loading="lazy">
                <div class="play-button">
                    <svg width="68" height="48" viewBox="0 0 68 48">
                        <path d="M66.52,7.74c-0.78-2.93-2.49-5.41-5.42-6.19C55.79,.13,34,0,34,0S12.21,.13,6.9,1.55 C3.97,2.33,2.27,4.81,1.48,7.74C0.06,13.05,0,24,0,24s0.06,10.95,1.48,16.26c0.78,2.93,2.49,5.41,5.42,6.19 C12.21,47.87,34,48,34,48s21.79-0.13,27.1-1.55c2.93-0.78,4.64-3.26,5.42-6.19C67.94,34.95,68,24,68,24S67.94,13.05,66.52,7.74z" fill="#f00"></path>
                        <path d="M 45,24 27,14 27,34" fill="#fff"></path>
                    </svg>
                </div>
            </div>
            <div class="video-info">
                <h4>{{ video.title }}</h4>
                <p>{{ video.description }}</p>
            </div>
        </div>
        {% endfor %}
    </div>
    </div>
</section>

<!-- Video Modal -->
<div id="videoModal" class="video-modal" onclick="closeVideoModal()">
    <div class="video-modal-content" onclick="event.stopPropagation()">
        <span class="video-close" onclick="closeVideoModal()">&times;</span>
        <div class="video-container">
            <iframe id="videoFrame" src="" title="Hackathon video" allowfullscreen></iframe>
        </div>
        <h3 id="videoTitle"></h3>
    </div>
</div>

<section id="sponsors" class="sponsors-section">
    <div class="reveal">
    <h2 style="text-align:left;">Our <span>partners</span></h2>
    <div class="sponsor-logos">
        {% for sponsor in site.data.sponsors.partners %}
        <img src="{{ sponsor.logo | relative_url }}" alt="{{ sponsor.alt }}"{% if sponsor.url and sponsor.url != '#' %} onclick="window.open('{{ sponsor.url }}', '_blank')" style="cursor: pointer;"{% endif %}>
        {% endfor %}
    </div>
    </div>
</section>

<section id="faq" class="faq-section-home">
    <div class="reveal">
    <h2>Frequently asked <span>questions</span></h2>
    {% for faq in site.data.faq.questions %}
    <div class="faq-item faq-open">
        <h3 class="faq-question-visible">{{ faq.question }}</h3>
        <div class="faq-answer-visible">
            <p>{{ faq.answer }}</p>
        </div>
    </div>
    {% endfor %}
    </div>
</section>
