---
layout: page
title: "Agenda"
description: "Event schedule and timeline for the Open Scientific Intelligence (OSI) Hackathon — October 21–22, 2026."
keywords: "OSI Hackathon Schedule, Event Timeline, Agenda, October 2026"
---

## {{ site.event.next_edition }}

<div class="event-status-banner">
    <span class="status-dot status-dot--pending" aria-hidden="true"></span>
    <span>Dates confirmed &middot; agenda TBA</span>
</div>

The fourth edition — now the **Open Scientific Intelligence (OSI) Hackathon** — runs **Wednesday–Thursday, October 21–22, 2026**, hybrid and worldwide. Kick-off time, mentorship blocks, and the submission deadline are still being finalized. They will be published here and announced in [Slack]({{ site.links.slack }}) first. Registration is open now.

<div class="schedule-timeline">
    <div class="schedule-item">
        <div class="schedule-time">Day 1 &middot; Wed, Oct 21 &middot; TBA</div>
        <div class="schedule-details">
            <h4>Kick-off, teaming, hacking begins</h4>
            <p>Opening session, team formation across sites and virtually, then straight into building. Times to be announced.</p>
        </div>
    </div>
    <div class="schedule-item">
        <div class="schedule-time">Day 2 &middot; Thu, Oct 22 &middot; TBA</div>
        <div class="schedule-details">
            <h4>Build day and final submissions</h4>
            <p>Focused development with mentors on hand, followed by the project submission deadline. Times to be announced.</p>
        </div>
    </div>
    <div class="schedule-item">
        <div class="schedule-time">After the event &middot; TBA</div>
        <div class="schedule-details">
            <h4>Winners announced &amp; virtual showcase</h4>
            <p>Judging wraps up, awards are announced, and featured projects are invited to present. Date to be announced.</p>
        </div>
    </div>
</div>

<div class="hero-actions">
    <a rel="noopener noreferrer" target="_blank" href="{{ site.links.registration }}" class="cta-button">Register for October 21&ndash;22, 2026</a>
    <a rel="noopener noreferrer" target="_blank" href="{{ site.links.slack }}" class="secondary-cta secondary-cta--light">Get the schedule first &mdash; join Slack</a>
</div>

## What to Expect

### Day 1: Getting Started
- **Welcome & Networking**: Meet fellow participants and organizers
- **Project Brainstorming**: Explore ideas and form teams
- **Technical Setup**: Access to computational resources and data
- **Mentorship**: Connect with experienced researchers and industry professionals

### Day 2: Development & Presentation
- **Intensive Development**: Focus time for building your project
- **Final Submissions**: Complete and submit your work
- **Project Showcases**: Present your innovations to judges and peers
- **Awards Ceremony**: Recognition for outstanding contributions

## Resources Available

During the event, participants will have access to:
- High-performance computing resources
- Curated datasets across the physical sciences and mathematics
- Documentation and tutorials for LLM, agent, and scientific software APIs
- Expert mentorship and technical support
- Collaboration tools and communication channels

## Time Zones

All times listed are in Central Time (CT). International participants should note:
- **UTC**: Add 6 hours to CT times
- **GMT**: Add 6 hours to CT times  
- **EST**: Add 1 hour to CT times
- **PST**: Subtract 2 hours from CT times

For participants at international sites, local organizers will coordinate timing and provide location-specific schedules.

---

## Previous Edition: {{ site.event.dates }}

*Kept here for reference while the 2026 agenda is being defined — the 2026 schedule will follow a similar shape.*

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

### 2025 Deadlines

- **Registration Deadline**: September 11, 2025
- **Project Submission**: {{ site.event.submission_deadline }}
- **Final Presentations**: September 12, 2025
