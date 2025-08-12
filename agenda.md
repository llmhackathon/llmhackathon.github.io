---
layout: page
title: "Agenda"
description: "Event schedule and timeline for the LLM Hackathon for Applications in Materials Science & Chemistry."
keywords: "LLM Hackathon Schedule, Event Timeline, Agenda"
---

## Event Schedule

### {{ site.event.dates }}

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

## Important Deadlines

- **Registration Deadline**: {{ site.event.dates | split: '-' | first | strip }}
- **Project Submission**: {{ site.event.submission_deadline }}
- **Final Presentations**: {{ site.event.dates | split: '-' | last | strip }}

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
- Curated datasets for materials science and chemistry
- Documentation and tutorials for LLM APIs
- Expert mentorship and technical support
- Collaboration tools and communication channels

## Time Zones

All times listed are in Central Time (CT). International participants should note:
- **UTC**: Add 6 hours to CT times
- **GMT**: Add 6 hours to CT times  
- **EST**: Add 1 hour to CT times
- **PST**: Subtract 2 hours from CT times

For participants at international sites, local organizers will coordinate timing and provide location-specific schedules.