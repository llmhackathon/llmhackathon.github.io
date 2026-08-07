---
layout: page
title: "Hackathon Sites"
description: "Explore all the physical locations for the OSI Hackathon and learn how to host your own site."
keywords: "Hackathon Locations, Hackathon Hosting, London, Toronto, Sydney, On-site Hackathon, Venue Information"
---

<div class="sites-nav-actions">
    <a href="#locations" class="cta-button">See Locations</a>
    <a href="#hosting" class="secondary-cta secondary-cta--light">Host a Site</a>
</div>

<div id="locations" style="scroll-margin-top: 100px;">
    <h2>Our <span>Locations</span></h2>

    <div class="important-links" style="text-align: center;">
        <h3 style="margin-top: 0; font-size: 1.2rem;">Registration Requirements</h3>
        <p style="margin: 0 auto 8px;">
            <strong>All participants:</strong> Register for the main hackathon using the button in the navigation bar.
        </p>
        <p style="margin: 0 auto;">
            <strong>In-person participants:</strong> Also register for your specific site below if site-specific registration is available.
        </p>
    </div>

    <!-- North America -->
    <h3 class="region-heading">North America</h3>
    <div class="resource-grid">
        {% assign north_america_sites = site.data.sites.locations | where: "region", "North America" %}
        {% for site in north_america_sites %}
        <div class="resource-card site-card">
            <a href="/sites/{{ site.slug }}/" class="site-card-link">
                <h4>{{ site.name }}</h4>
                <p>{{ site.institution }}</p>
                <p><i class="fas fa-envelope" aria-hidden="true"></i> {{ site.organizer_name }}<br>[{{ site.organizer_email }}]</p>
            </a>
            <div class="site-card-footer">
                {% if site.registration_link %}
                <a href="{{ site.registration_link }}" target="_blank" rel="noopener" class="cta-button site-register-btn">Site Registration</a>
                {% else %}
                <span class="site-register-btn site-register-btn--disabled">E-mail Contact for Details</span>
                {% endif %}
            </div>
        </div>
        {% endfor %}
    </div>

    <!-- Europe -->
    <h3 class="region-heading">Europe</h3>
    <div class="resource-grid">
        {% assign europe_sites = site.data.sites.locations | where: "region", "Europe" %}
        {% for site in europe_sites %}
        <div class="resource-card site-card">
            <a href="/sites/{{ site.slug }}/" class="site-card-link">
                <h4>{{ site.name }}</h4>
                <p>{{ site.institution }}</p>
                <p><i class="fas fa-envelope" aria-hidden="true"></i> {{ site.organizer_name }}<br>[{{ site.organizer_email }}]</p>
            </a>
            <div class="site-card-footer">
                {% if site.registration_link %}
                <a href="{{ site.registration_link }}" target="_blank" rel="noopener" class="cta-button site-register-btn">Site Registration</a>
                {% else %}
                <span class="site-register-btn site-register-btn--disabled">Registration TBD</span>
                {% endif %}
            </div>
        </div>
        {% endfor %}
    </div>

    <!-- Asia-Pacific -->
    <h3 class="region-heading">Asia-Pacific</h3>
    <div class="resource-grid">
        {% assign asia_pacific_sites = site.data.sites.locations | where: "region", "Asia-Pacific" %}
        {% for site in asia_pacific_sites %}
        <div class="resource-card site-card">
            <a href="/sites/{{ site.slug }}/" class="site-card-link">
                <h4>{{ site.name }}</h4>
                <p>{{ site.institution }}</p>
                <p><i class="fas fa-envelope" aria-hidden="true"></i> {{ site.organizer_name }}<br>[{{ site.organizer_email }}]</p>
            </a>
            <div class="site-card-footer">
                {% if site.registration_link %}
                <a href="{{ site.registration_link }}" target="_blank" rel="noopener" class="cta-button site-register-btn">Site Registration</a>
                {% else %}
                <span class="site-register-btn site-register-btn--disabled">Registration TBD</span>
                {% endif %}
            </div>
        </div>
        {% endfor %}
    </div>
</div>

<div id="hosting" class="hosting-section" style="scroll-margin-top: 100px;">
    <h2>Host a <span>local site</span></h2>
    <p class="hosting-lede">Help us grow our community by operating your own "node" of the hackathon!</p>
    <p style="text-align: center;">
        <a href="https://forms.gle/nF832hR774W4hC2F6" class="cta-button" target="_blank" rel="noopener">Register a Site</a>
    </p>

    <!-- Steps to Host a Site -->
    <h3 class="region-heading">Steps to Host a Site</h3>
    <div class="hosting-steps">
        {% for step in site.data.sites.hosting.steps %}
        <div class="hosting-step">
            <div class="hosting-step-number">{{ step.number }}</div>
            <h4>{{ step.title }}</h4>
            <p>{{ step.description }}</p>
        </div>
        {% endfor %}
    </div>

    <!-- Site Requirements -->
    <h3 class="region-heading">Site Requirements</h3>
    <div class="hosting-requirements">
        <div class="hosting-panel">
            <h4><i class="fas fa-check-circle" aria-hidden="true"></i> Essential Requirements</h4>
            <ul class="hosting-list">
                {% for requirement in site.data.sites.hosting.essential_requirements %}
                <li>
                    <i class="{{ requirement.icon }}" aria-hidden="true"></i>
                    <span><strong>{{ requirement.title }}:</strong> {{ requirement.description }}</span>
                </li>
                {% endfor %}
            </ul>
        </div>
        <div class="hosting-panel">
            <h4><i class="fas fa-star" aria-hidden="true"></i> Optional Extras</h4>
            <ul class="hosting-list">
                {% for extra in site.data.sites.hosting.optional_extras %}
                <li>
                    <i class="{{ extra.icon }}" aria-hidden="true"></i>
                    <span><strong>{{ extra.title }}:</strong> {{ extra.description }}</span>
                </li>
                {% endfor %}
            </ul>
        </div>
    </div>

    <!-- What You Can Expect From Us -->
    <h3 class="region-heading">What You Can Expect From Us</h3>
    <div class="hosting-support">
        {% for support in site.data.sites.hosting.support_provided %}
        <div class="hosting-support-item">
            <i class="{{ support.icon }}" aria-hidden="true"></i>
            <h4>{{ support.title }}</h4>
            <p>{{ support.description }}</p>
        </div>
        {% endfor %}
    </div>

    <p class="hosting-disclaimer">
        <strong>By registering or operating a local hackathon site, you acknowledge and accept full responsibility to follow local regulations, and for the safety, conduct, and well-being of participants at your venue. The central organizing committee assumes no liability for injuries, property damage, or other losses that may occur during your local event.</strong>
    </p>
</div>
