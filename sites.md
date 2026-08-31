---
layout: page
title: "Hackathon Sites"
description: "On-site locations for the October 21–22, 2026 OSI Hackathon, the 2025 site archive, and how to host your own site."
keywords: "Hackathon Locations, Hackathon Hosting, Duke, Singapore, Toronto, Chicago, On-site Hackathon, Venue Information"
---

<div class="sites-nav-actions">
    <a href="#locations-2026" class="cta-button">2026 Sites</a>
    <a href="#hosting" class="secondary-cta secondary-cta--light">Host a Site</a>
    <a href="#locations-2025" class="secondary-cta secondary-cta--light">2025 Archive</a>
</div>

<div id="locations-2026" style="scroll-margin-top: 100px;">
    <h2>2026 <span>sites</span></h2>
    <p class="sites-edition-lede">On-site hubs for the October 21&ndash;22, 2026 edition. The map is still filling in &mdash; new sites are added here as hosts confirm.</p>

    <div class="important-links" style="text-align: center;">
        <h3 style="margin-top: 0; font-size: 1.2rem;">Registration Requirements</h3>
        <p style="margin: 0 auto 8px;">
            <strong>All participants:</strong> Register for the main hackathon using the button in the navigation bar.
        </p>
        <p style="margin: 0 auto;">
            <strong>In-person participants:</strong> Also register for your specific site below if site-specific registration is available.
        </p>
    </div>

    <h3 class="region-heading">Confirmed sites</h3>
    <div class="resource-grid site-grid--confirmed">
        {% for location in site.data.sites.locations_2026 %}
        {% assign location_url = '/sites/' | append: location.slug | append: '/' %}
        {% assign location_page = site.sites | where: "url", location_url | first %}
        <div class="resource-card site-card">
            <h4 class="site-card-title">
                {% if location_page %}<a href="{{ location_url | relative_url }}" class="site-card-title-link">{{ location.name }}</a>{% else %}{{ location.name }}{% endif %}
            </h4>
            <p class="site-card-institution">{{ location.institution }}</p>
            <div class="site-card-footer">
                {% if location.organizer_name %}
                <div class="site-card-contact">
                    <span class="site-card-label">Local organizer</span>
                    <span class="site-card-organizer">{{ location.organizer_name }}</span>
                    <a class="site-card-email" href="mailto:{{ location.organizer_email }}">{{ location.organizer_email }}</a>
                </div>
                {% endif %}
                {% if location.registration_link %}
                <a href="{{ location.registration_link }}" target="_blank" rel="noopener" class="cta-button site-register-btn">Site registration</a>
                {% else %}
                <span class="site-register-btn site-register-btn--disabled">Contact the organizer</span>
                {% endif %}
            </div>
        </div>
        {% endfor %}
    </div>

    <h3 class="region-heading">In planning for 2026</h3>
    <p class="sites-edition-lede">These locations are lining up hosts and venues. Details and site registration will appear here once they're set &mdash; if you're near one of them and want to help run it, <a href="mailto:{{ site.links.main_organizer_email }}">get in touch</a>.</p>
    <div class="resource-grid site-grid--planned">
        {% for location in site.data.sites.preliminary_2026 %}
        <div class="resource-card site-card site-card--planned">
            <span class="site-status-tag">In planning</span>
            <h4 class="site-card-title">{{ location.name }}</h4>
            {% if location.institution %}<p class="site-card-institution">{{ location.institution }}</p>{% endif %}
        </div>
        {% endfor %}
    </div>
</div>

<div id="locations-2025" class="sites-archive" style="scroll-margin-top: 100px;">
    <h2>2025 <span>sites</span> &middot; archive</h2>
    <p class="sites-edition-lede">Where the September 11&ndash;12, 2025 edition ran. Kept for the record &mdash; these sites and their registrations are closed. For 2026, see the <a href="#locations-2026">sites above</a>.</p>

    {% assign regions = "North America,Europe,Asia-Pacific" | split: "," %}
    {% for region in regions %}
    {% assign region_sites = site.data.sites.locations_2025 | where: "region", region %}
    {% if region_sites.size > 0 %}
    <h3 class="region-heading">{{ region }}</h3>
    <div class="resource-grid">
        {% for location in region_sites %}
        {% assign location_url = '/sites/' | append: location.slug | append: '/' %}
        {% assign location_page = site.sites | where: "url", location_url | first %}
        <div class="resource-card site-card site-card--archived">
            <h4 class="site-card-title">
                {% if location_page %}<a href="{{ location_url | relative_url }}" class="site-card-title-link">{{ location.name }}</a>{% else %}{{ location.name }}{% endif %}
            </h4>
            <p class="site-card-institution">{{ location.institution }}</p>
            <div class="site-card-footer">
                <div class="site-card-contact">
                    <span class="site-card-label">Local organizer</span>
                    <span class="site-card-organizer">{{ location.organizer_name }}</span>
                    <a class="site-card-email" href="mailto:{{ location.organizer_email }}">{{ location.organizer_email }}</a>
                </div>
                <span class="site-register-btn site-register-btn--disabled">2025 edition &middot; closed</span>
            </div>
        </div>
        {% endfor %}
    </div>
    {% endif %}
    {% endfor %}
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
