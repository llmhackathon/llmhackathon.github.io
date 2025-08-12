---
layout: site-location
title: "Berlin"
description: "Details about the Berlin site for the LLM Hackathon. Find venue information, local schedule, and specific instructions for participants in Berlin."
keywords: "Berlin Hackathon, Center for Materials Science Berlin, LLM Event Berlin, In-person Hackathon Site"
additional_css: |
  .content-section a {
      color: #2563eb;
      text-decoration: underline;
      transition: color 0.2s;
  }
  .content-section a:hover {
      color: #1d4ed8;
  }
---

## Welcome to the Berlin Hub

<div class="event-intro" style="margin-bottom: 24px;">
    <p>
        The Berlin in-person event will be held at the <strong>Center for Materials Science Berlin (CSMB)</strong>.
    </p>
    <p>
        We will have a motivated group of people ready to hack, a brainstorming and teaming session to kick things off, some environments with compute to play around, and of course, pizza 🍕.
    </p>
    <p style="margin-top: 12px;">
        <strong>Note:</strong> Places are limited—register early to secure your spot!
    </p>
</div>

<div class="organizer" style="display: flex; align-items: center; gap: 16px; margin: 8px 0 24px; flex-wrap: wrap;">
    <img src="{{ '/sites/FAIRmat_logo.svg' | relative_url }}" alt="FAIRmat logo" style="height: 42px; width: auto;" />
    <p style="margin: 0;">
        This Berlin site is <strong>organized by</strong> <a href="https://www.fairmat-nfdi.eu/fairmat" target="_blank" rel="noopener">FAIRmat</a>.
    </p>
</div>

## Event Details

**Date:** {{ site.event.dates }}  
**Location:** Center for Materials Science Berlin (CSMB)  
**Venue:** Fritz-Haber-Institut der MPG, Faradayweg 4-6, 14195 Berlin  

## Schedule

### Day 1 - {{ site.event.dates | split: '-' | first | strip }}
- **10:00 AM:** Welcome & Coffee
- **10:30 AM:** Project brainstorming and team formation
- **12:00 PM:** Lunch break
- **1:00 PM:** Hacking begins
- **6:00 PM:** Dinner & networking

### Day 2 - {{ site.event.dates | split: '-' | last | strip }}
- **9:00 AM:** Coffee & continued hacking
- **12:00 PM:** Lunch break
- **1:00 PM:** Final push
- **4:00 PM:** Project presentations
- **5:00 PM:** Results & closing

## What's Provided

- High-speed internet and workspace
- Coffee, lunch, and snacks
- Access to computational resources
- Local mentorship and support
- Networking opportunities

## Getting There

The venue is easily accessible by public transport:
- **S-Bahn:** S1 to "Sundgauer Straße" (10-minute walk)
- **Bus:** Route 115 to "Hittorfstraße" (5-minute walk)

## Contact

For Berlin-specific questions, please reach out to the local organizers or join our [Slack community]({{ site.links.slack }}).