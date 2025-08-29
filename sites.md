---
layout: page
title: "Hackathon Sites"
description: "Explore all the physical locations for the LLM Hackathon and learn how to host your own site."
keywords: "Hackathon Locations, Hackathon Hosting, London, Toronto, Sydney, On-site Hackathon, Venue Information"
---

<div style="text-align: center; margin-top: 2rem; display: flex; justify-content: center; gap: 1rem;">
    <a href="#locations" class="cta-button">See Locations</a>
    <a href="#hosting" class="cta-button">Host a Site</a>
</div>

<section id="locations" class="content-section" style="padding-top: 5rem; scroll-margin-top: 100px;">
    <h2 style="text-align: center; font-size: 2.5rem; margin-bottom: 2rem;">Our <span>Locations</span></h2>
    
    <div style="background: #f8fafc; border: 1px solid #e2e8f0; border-radius: 8px; padding: 1.5rem; margin-bottom: 2rem; text-align: center;">
        <h3 style="color: #1a365d; margin-bottom: 1rem; font-size: 1.2rem;">Registration Requirements</h3>
        <p style="color: #4a5568; margin-bottom: 0.5rem;">
            <strong>All participants:</strong> Register for the main hackathon using the button in the navigation bar.
        </p>
        <p style="color: #4a5568; margin: 0;">
            <strong>In-person participants:</strong> Also register for your specific site below if site-specific registration is available.
        </p>
    </div>
    
    <!-- North America -->
    <h3 style="text-align: center; font-size: 2rem; margin: 3rem 0 1.5rem; color: #2563eb;">North America</h3>
    <div class="resource-grid">
        {% assign north_america_sites = site.data.sites.locations | where: "region", "North America" %}
        {% for site in north_america_sites %}
        <div class="resource-card location-card" style="text-decoration: none; display: block;">
            <a href="/sites/{{ site.slug }}/" style="text-decoration: none; color: inherit;">
                <h4>{{ site.name }}</h4>
                <p>{{ site.institution }}</p>
                <p><i class="fas fa-envelope"></i> {{ site.organizer_name }}<br>[{{ site.organizer_email }}]</p>
            </a>
            <div style="margin-top: 1rem; padding-top: 1rem; border-top: 1px solid #e2e8f0;">
                {% if site.registration_link %}
                <a href="{{ site.registration_link }}" target="_blank" rel="noopener" class="cta-button" style="font-size: 0.9rem; padding: 0.5rem 1rem; background: linear-gradient(to right, #027ff7, #0259ce); color: white; text-decoration: none;">Site Registration</a>
                {% else %}
                <span class="cta-button" style="font-size: 0.9rem; padding: 0.5rem 1rem; background: #e2e8f0; color: #718096; cursor: not-allowed;">E-mail Contact for Details</span>
                {% endif %}
            </div>
        </div>
        {% endfor %}
    </div>

    <!-- Europe -->
    <h3 style="text-align: center; font-size: 2rem; margin: 3rem 0 1.5rem; color: #2563eb;">Europe</h3>
    <div class="resource-grid">
        {% assign europe_sites = site.data.sites.locations | where: "region", "Europe" %}
        {% for site in europe_sites %}
        <div class="resource-card location-card" style="text-decoration: none; display: block;">
            <a href="/sites/{{ site.slug }}/" style="text-decoration: none; color: inherit;">
                <h4>{{ site.name }}</h4>
                <p>{{ site.institution }}</p>
                <p><i class="fas fa-envelope"></i> {{ site.organizer_name }}<br>[{{ site.organizer_email }}]</p>
            </a>
            <div style="margin-top: 1rem; padding-top: 1rem; border-top: 1px solid #e2e8f0;">
                {% if site.registration_link %}
                <a href="{{ site.registration_link }}" target="_blank" rel="noopener" class="cta-button" style="font-size: 0.9rem; padding: 0.5rem 1rem; background: linear-gradient(to right, #027ff7, #0259ce); color: white; text-decoration: none;">Site Registration</a>
                {% else %}
                <span class="cta-button" style="font-size: 0.9rem; padding: 0.5rem 1rem; background: #e2e8f0; color: #718096; cursor: not-allowed;">Registration TBD</span>
                {% endif %}
            </div>
        </div>
        {% endfor %}
    </div>

    <!-- Asia-Pacific -->
    <h3 style="text-align: center; font-size: 2rem; margin: 3rem 0 1.5rem; color: #2563eb;">Asia-Pacific</h3>
    <div class="resource-grid">
        {% assign asia_pacific_sites = site.data.sites.locations | where: "region", "Asia-Pacific" %}
        {% for site in asia_pacific_sites %}
        <div class="resource-card location-card" style="text-decoration: none; display: block;">
            <a href="/sites/{{ site.slug }}/" style="text-decoration: none; color: inherit;">
                <h4>{{ site.name }}</h4>
                <p>{{ site.institution }}</p>
                <p><i class="fas fa-envelope"></i> {{ site.organizer_name }}<br>[{{ site.organizer_email }}]</p>
            </a>
            <div style="margin-top: 1rem; padding-top: 1rem; border-top: 1px solid #e2e8f0;">
                {% if site.registration_link %}
                <a href="{{ site.registration_link }}" target="_blank" rel="noopener" class="cta-button" style="font-size: 0.9rem; padding: 0.5rem 1rem; background: linear-gradient(to right, #027ff7, #0259ce); color: white; text-decoration: none;">Site Registration</a>
                {% else %}
                <span class="cta-button" style="font-size: 0.9rem; padding: 0.5rem 1rem; background: #e2e8f0; color: #718096; cursor: not-allowed;">Registration TBD</span>
                {% endif %}
            </div>
        </div>
        {% endfor %}
    </div>

</section>

<section id="hosting" class="bg-gradient-to-br from-blue-50 to-indigo-100 py-16"
    style="margin-top: 5rem; scroll-margin-top: 100px;">
    <div class="max-w-6xl mx-auto px-6">
        <div class="text-center mb-12">
            <h2 class="text-4xl font-bold text-gray-900 mb-4">Host a Local Site for the 3rd LLM Hackathon</h2>
            <p class="text-xl text-gray-700 max-w-3xl mx-auto">
                Help us grow our community by operating your own "node" of the hackathon!
            </p>
            <div style="text-align: center; margin-top: 2rem;">
                <a href="https://forms.gle/nF832hR774W4hC2F6" class="cta-button" target="_blank" rel="noopener">Register a Site</a>
            </div>
            <div class="mt-6 border-t-2 border-indigo-300 w-24 mx-auto"></div>
        </div>

        <!-- Steps to Host a Site -->
        <div class="mb-16">
            <h3 class="text-3xl font-bold text-gray-900 mb-8 text-center">Steps to Host a Site</h3>
            <div class="grid md:grid-cols-2 lg:grid-cols-4 gap-6">
                {% for step in site.data.sites.hosting.steps %}
                <div class="bg-white rounded-xl p-6 shadow-lg hover:shadow-xl transition-shadow">
                    <div class="text-3xl font-bold text-indigo-600 mb-4">{{ step.number }}</div>
                    <h4 class="text-xl font-semibold text-gray-900 mb-3">{{ step.title }}</h4>
                    <p class="text-gray-600">{{ step.description }}</p>
                </div>
                {% endfor %}
            </div>
        </div>

        <!-- Site Requirements -->
        <div class="mb-16">
            <h3 class="text-3xl font-bold text-gray-900 mb-8 text-center">Site Requirements</h3>
            <div class="grid md:grid-cols-2 gap-8">
                <div class="bg-white rounded-xl p-8 shadow-lg">
                    <h4 class="text-2xl font-bold text-gray-900 mb-6 flex items-center">
                        <i class="fas fa-check-circle text-green-500 mr-3"></i>
                        Essential Requirements
                    </h4>
                    <ul class="space-y-4 text-gray-700">
                        {% for requirement in site.data.sites.hosting.essential_requirements %}
                        <li class="flex items-start">
                            <i class="{{ requirement.icon }} text-blue-500 mr-3 mt-1"></i>
                            <span><strong>{{ requirement.title }}:</strong> {{ requirement.description }}</span>
                        </li>
                        {% endfor %}
                    </ul>
                </div>
                <div class="bg-white rounded-xl p-8 shadow-lg">
                    <h4 class="text-2xl font-bold text-gray-900 mb-6 flex items-center">
                        <i class="fas fa-star text-yellow-500 mr-3"></i>
                        Optional Extras
                    </h4>
                    <ul class="space-y-4 text-gray-700">
                        {% for extra in site.data.sites.hosting.optional_extras %}
                        <li class="flex items-start">
                            <i class="{{ extra.icon }} text-yellow-500 mr-3 mt-1"></i>
                            <span><strong>{{ extra.title }}:</strong> {{ extra.description }}</span>
                        </li>
                        {% endfor %}
                    </ul>
                </div>
            </div>
        </div>

        <!-- What You Can Expect From Us -->
        <div class="bg-white rounded-xl p-8 shadow-lg">
            <h3 class="text-3xl font-bold text-gray-900 mb-6 text-center">What You Can Expect From Us</h3>
            <div class="grid md:grid-cols-2 lg:grid-cols-4 gap-6">
                {% for support in site.data.sites.hosting.support_provided %}
                <div class="text-center">
                    <i class="{{ support.icon }} text-4xl text-blue-500 mb-4"></i>
                    <h4 class="text-lg font-semibold text-gray-900 mb-2">{{ support.title }}</h4>
                    <p class="text-gray-600">{{ support.description }}</p>
                </div>
                {% endfor %}
            </div>
           
        </div>
        <p style="margin-top: 2rem; text-align: center;">
                <strong>By registering or operating a local hackathon site, you acknowledge and accept full responsibility to follow local regulations, and for the safety, conduct, and well-being of participants at your venue. The central organizing committee assumes no liability for injuries, property damage, or other losses that may occur during your local event.</strong>
            </p>

    </div>

</section>
