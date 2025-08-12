---
layout: page
title: "Frequently Asked Questions"
description: "Find answers to common questions about the LLM Hackathon for Applications in Materials Science & Chemistry."
keywords: "LLM Hackathon FAQ, Questions, Participation, Registration"
---

<section class="faq-section">
    {% for faq in site.data.faq.questions %}
    <div class="faq-item">
        <button class="faq-question">{{ faq.question }}</button>
        <div class="faq-answer">
            <p>{{ faq.answer }}</p>
        </div>
    </div>
    {% endfor %}
</section>