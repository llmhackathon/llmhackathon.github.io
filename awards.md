---
layout: page
title: 2025 Awards
permalink: /awards/
---

<style>
.awards-wrapper {
    font-family: var(--font-display);
    display: flex;
    flex-direction: column;
    gap: 48px;
}

.awards-intro {
    font-size: 1rem;
    line-height: 1.7;
    color: var(--on-void);
    background: var(--void);
    border: 1px solid var(--line-on-void);
    border-radius: var(--radius-md);
    padding: 32px;
}

.awards-section h2 {
    font-size: 1.8rem;
    margin-bottom: 12px;
}

.awards-section p.section-copy {
    color: var(--ink-soft);
    margin-bottom: 28px;
    max-width: 760px;
}

.award-grid {
    display: grid;
    grid-template-columns: repeat(auto-fill, minmax(380px, 1fr));
    gap: 24px;
}

.award-card {
    background: var(--paper);
    border: 1px solid var(--line);
    border-radius: var(--radius-md);
    padding: 24px;
    box-shadow: 0 1px 2px rgba(20,18,35,0.08), 0 12px 32px rgba(20,18,35,0.07);
    transition: all 0.35s cubic-bezier(0.4, 0, 0.2, 1);
    position: relative;
    overflow: hidden;
    display: flex;
    flex-direction: column;
}

.award-card:hover {
    transform: translateY(-3px);
    border-color: var(--action);
}

.award-rank {
    font-family: var(--font-mono);
    font-size: 0.72rem;
    text-transform: uppercase;
    letter-spacing: 0.06em;
    color: var(--ink-gold);
    background: color-mix(in oklch, var(--gold) 18%, transparent);
    border: 1px solid color-mix(in oklch, var(--gold) 50%, transparent);
    border-radius: 999px;
    padding: 4px 12px;
    display: inline-block;
    margin-bottom: 12px;
}

.award-card h3 {
    color: var(--ink);
    margin-bottom: 12px;
    font-size: 1.25rem;
    font-weight: 700;
    position: relative;
    padding-bottom: 6px;
    line-height: 1.3;
}

.award-card h3::after {
    content: '';
    position: absolute;
    bottom: 0;
    left: 0;
    width: 50px;
    height: 2px;
    background: var(--action);
    border-radius: 2px;
}

.award-section {
    margin-bottom: 14px;
    flex: 1;
}

.award-section-title {
    font-family: var(--font-mono);
    font-weight: 600;
    color: var(--ink);
    margin-bottom: 6px;
    font-size: 0.8rem;
    text-transform: uppercase;
    letter-spacing: 0.5px;
    display: flex;
    align-items: center;
    gap: 6px;
}

.award-section-title::before {
    content: '';
    width: 3px;
    height: 12px;
    background: var(--action);
    border-radius: 2px;
}

.award-team {
    color: var(--ink-soft);
    line-height: 1.5;
    font-size: 0.875rem;
}

.award-description {
    color: var(--ink-soft);
    line-height: 1.5;
    font-size: 0.875rem;
    display: -webkit-box;
    -webkit-line-clamp: 4;
    -webkit-box-orient: vertical;
    overflow: hidden;
}

.award-links {
    margin-top: auto;
    padding-top: 16px;
    display: flex;
    gap: 10px;
    flex-wrap: wrap;
}

.award-button {
    background: var(--action);
    color: var(--cream);
    padding: 10px 18px;
    border: 0;
    border-radius: var(--radius-sm);
    font-weight: 600;
    font-size: 13px;
    text-decoration: none;
    display: inline-flex;
    align-items: center;
    gap: 6px;
    transition: all 0.3s cubic-bezier(0.4, 0, 0.2, 1);
    position: relative;
    overflow: hidden;
}

.award-button:hover {
    color: var(--cream);
    filter: brightness(1.05);
    transform: translateY(-1px);
}

.award-button svg {
    width: 14px;
    height: 14px;
}

.visionary-card {
    background: var(--paper);
    border: 1px solid var(--line);
    border-radius: var(--radius-md);
    padding: 28px;
    box-shadow: 0 1px 2px rgba(20,18,35,0.08), 0 12px 32px rgba(20,18,35,0.07);
}

.visionary-card ul {
    columns: 2;
    column-gap: 24px;
    margin: 0;
    padding: 0;
    list-style: none;
}

.visionary-card li {
    margin: 0 0 8px 0;
    font-weight: 600;
    color: var(--ink);
}

.loading {
    text-align: center;
    padding: 40px;
    color: var(--ink-soft);
    font-size: 1rem;
}

@media (max-width: 768px) {
    .awards-intro {
        padding: 24px;
    }

    .award-grid {
        grid-template-columns: 1fr;
    }
    
    .award-card {
        padding: 20px;
    }
    
    .award-card h3 {
        font-size: 1.15rem;
    }
    
    .award-description {
        -webkit-line-clamp: 5;
    }

    .visionary-card ul {
        columns: 1;
    }
}

@media (min-width: 769px) and (max-width: 1200px) {
    .award-grid {
        grid-template-columns: repeat(2, 1fr);
    }
}
</style>

<div class="awards-wrapper">
    <div class="awards-intro">
        Congratulations to the Lila Prize winning teams for top-scoring overall projects! Please take a moment to celebrate the teams below, explore their project descriptions, and watch their demos. We will be posting these to the website and contacting teams shortly.
    </div>

    <section class="awards-section" aria-label="Lila Prize Winners">
        <h2>Lila Prize Winners</h2>
        <div class="award-grid" id="lila-awards-grid">
            <div class="loading">Loading awards...</div>
        </div>
    </section>

    <section class="awards-section" aria-label="Abstrax Prizes">
        <h2>Abstrax Prizes</h2>
        <div class="award-grid" id="abstrax-awards-grid">
            <div class="loading">Loading awards...</div>
        </div>
    </section>

    <section class="awards-section" aria-label="2025 Visionary Awards">
        <h2>2025 Visionary Awards</h2>
        <p class="section-copy">These teams were recognized by the judges for exceptional scores, novelty, or innovative approaches. They will be invited to a special session of the hackathon showcase, and all participating teams will still be welcomed.</p>
        <div class="award-grid" id="visionary-awards-grid">
            <div class="loading">Loading awards...</div>
        </div>
    </section>
</div>

<script>
document.addEventListener('DOMContentLoaded', function() {
    fetch('/assets/data/submissions.json')
        .then(response => response.json())
        .then(data => {
            // Filter submissions with awards
            const awardedSubmissions = data.filter(s => s.award);
            
            // Group by award type
            const lilaWinners = awardedSubmissions
                .filter(s => s.award.startsWith('Lila Prize'))
                .sort((a, b) => {
                    // Sort by place number
                    const getPlace = (award) => {
                        const match = award.match(/(\d+)(st|nd|rd|th) Place/);
                        return match ? parseInt(match[1]) : 999;
                    };
                    return getPlace(a.award) - getPlace(b.award);
                });
            
            const abstraxWinners = awardedSubmissions
                .filter(s => s.award === 'Abstrax Prize');
            
            const visionaryWinners = awardedSubmissions
                .filter(s => s.award === 'Visionary Award')
                .sort((a, b) => a.team_name.localeCompare(b.team_name));
            
            // Render awards
            renderAwardCards(lilaWinners, 'lila-awards-grid', true);
            renderAwardCards(abstraxWinners, 'abstrax-awards-grid', false);
            renderAwardCards(visionaryWinners, 'visionary-awards-grid', false);
        })
        .catch(error => {
            console.error('Error loading awards:', error);
            document.querySelectorAll('.loading').forEach(el => {
                el.textContent = 'Error loading awards. Please try again later.';
                el.style.color = '#dc2626';
            });
        });
    
    function renderAwardCards(winners, containerId, showRank) {
        const container = document.getElementById(containerId);
        container.innerHTML = '';
        
        if (winners.length === 0) {
            container.innerHTML = '<div class="loading">No awards in this category.</div>';
            return;
        }
        
        winners.forEach((submission) => {
            const card = document.createElement('article');
            card.className = 'award-card';
            
            // Extract rank from award name
            let rankBadge = '';
            if (showRank && submission.award) {
                const rankMatch = submission.award.match(/(\d+)(st|nd|rd|th) [Pp]lace/);
                if (rankMatch) {
                    rankBadge = `<span class="award-rank">${rankMatch[1]}${rankMatch[2]} place</span>`;
                }
            } else if (!showRank) {
                rankBadge = `<span class="award-rank">${submission.award}</span>`;
            }
            
            // Build links
            let linksHtml = '<div class="award-links">';
            if (submission.submission_link) {
                linksHtml += `
                    <a class="award-button" href="${submission.submission_link}" target="_blank" rel="noopener">
                        <svg viewBox="0 0 24 24" fill="currentColor" aria-hidden="true">
                            <path d="M10 16.5V7.5L16 12L10 16.5M5 3H19C20.1 3 21 3.9 21 5V19C21 20.1 20.1 21 19 21H5C3.9 21 3 20.1 3 19V5C3 3.9 3.9 3 5 3Z" />
                        </svg>
                        Watch demo
                    </a>
                `;
            }
            if (submission.code_link) {
                linksHtml += `
                    <a class="award-button" href="${submission.code_link}" target="_blank" rel="noopener" style="background: var(--action);">
                        <svg viewBox="0 0 24 24" fill="currentColor" aria-hidden="true">
                            <path d="M12,2A10,10 0 0,0 2,12C2,16.42 4.87,20.17 8.84,21.5C9.34,21.58 9.5,21.27 9.5,21C9.5,20.77 9.5,20.14 9.5,19.31C6.73,19.91 6.14,17.97 6.14,17.97C5.68,16.81 5.03,16.5 5.03,16.5C4.12,15.88 5.1,15.9 5.1,15.9C6.1,15.97 6.63,16.93 6.63,16.93C7.5,18.45 8.97,18 9.54,17.76C9.63,17.11 9.89,16.67 10.17,16.42C7.95,16.17 5.62,15.31 5.62,11.5C5.62,10.39 6,9.5 6.65,8.79C6.55,8.54 6.2,7.5 6.75,6.15C6.75,6.15 7.59,5.88 9.5,7.17C10.29,6.95 11.15,6.84 12,6.84C12.85,6.84 13.71,6.95 14.5,7.17C16.41,5.88 17.25,6.15 17.25,6.15C17.8,7.5 17.45,8.54 17.35,8.79C18,9.5 18.38,10.39 18.38,11.5C18.38,15.32 16.04,16.16 13.81,16.41C14.17,16.72 14.5,17.33 14.5,18.26C14.5,19.6 14.5,20.68 14.5,21C14.5,21.27 14.66,21.59 15.17,21.5C19.14,20.16 22,16.42 22,12A10,10 0 0,0 12,2Z"/>
                        </svg>
                        View Code
                    </a>
                `;
            }
            linksHtml += '</div>';
            
            card.innerHTML = `
                ${rankBadge}
                <h3>${submission.team_name}</h3>
                <div class="award-section">
                    <div class="award-section-title">Team Members</div>
                    <div class="award-team">${submission.team_members}</div>
                </div>
                <div class="award-section">
                    <div class="award-section-title">Description</div>
                    <div class="award-description">${submission.description}</div>
                </div>
                ${linksHtml}
            `;
            
            container.appendChild(card);
        });
    }
});
</script>
