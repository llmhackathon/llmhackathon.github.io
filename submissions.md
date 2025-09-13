---
layout: page
title: Submissions
permalink: /submissions/
---

<style>
/* Page Header */
.submissions-header {
    text-align: center;
    margin-bottom: 40px;
    padding: 40px 20px;
    background: linear-gradient(135deg, #f8fbff 0%, #e6f2ff 100%);
    border-radius: 16px;
    border: 1px solid #e0efff;
}

.submissions-stats {
    display: flex;
    justify-content: center;
    gap: 30px;
    margin-top: 20px;
    flex-wrap: wrap;
}

.stat-item {
    text-align: center;
    padding: 15px 25px;
    background: white;
    border-radius: 12px;
    box-shadow: 0 4px 12px rgba(0, 0, 0, 0.08);
    border: 1px solid #e2e2e2;
}

.stat-number {
    font-size: 2rem;
    font-weight: 700;
    color: #027ff7;
    margin-bottom: 5px;
}

.stat-label {
    font-size: 0.9rem;
    color: #666;
    font-weight: 500;
}

/* Submission Cards */
.submission-card {
    background: #ffffff;
    border: 1px solid #e8f0fe;
    border-radius: 16px;
    padding: 30px;
    margin-bottom: 40px;
    box-shadow: 0 8px 32px rgba(0, 0, 0, 0.06);
    transition: transform 0.3s ease, box-shadow 0.3s ease, border-color 0.3s ease;
    position: relative;
    overflow: hidden;
}

.submission-card::before {
    content: '';
    position: absolute;
    top: 0;
    left: 0;
    right: 0;
    height: 4px;
    background: linear-gradient(90deg, #027ff7, #0259ce, #6366f1);
    border-radius: 16px 16px 0 0;
}

.submission-card:hover {
    transform: translateY(-4px);
    box-shadow: 0 16px 48px rgba(0, 0, 0, 0.12);
    border-color: #027ff7;
}

/* Team Name */
.submission-card h3 {
    color: #1a1a1a;
    margin-bottom: 16px;
    font-size: 1.5rem;
    font-weight: 700;
    position: relative;
    padding-bottom: 8px;
}

.submission-card h3::after {
    content: '';
    position: absolute;
    bottom: 0;
    left: 0;
    width: 60px;
    height: 3px;
    background: linear-gradient(90deg, #027ff7, #6366f1);
    border-radius: 2px;
}

/* Content Sections */
.submission-section {
    margin-bottom: 20px;
}

.submission-section-title {
    font-weight: 600;
    color: #374151;
    margin-bottom: 8px;
    font-size: 0.95rem;
    text-transform: uppercase;
    letter-spacing: 0.5px;
    display: flex;
    align-items: center;
    gap: 8px;
}

.submission-section-title::before {
    content: '';
    width: 4px;
    height: 16px;
    background: #027ff7;
    border-radius: 2px;
}

.submission-content {
    color: #4b5563;
    line-height: 1.6;
    font-size: 0.95rem;
}

/* Action Links */
.submission-links {
    margin-top: 25px;
    display: flex;
    gap: 12px;
    flex-wrap: wrap;
}

.submission-links .btn {
    background: linear-gradient(135deg, #027ff7 0%, #0259ce 100%);
    color: #ffffff;
    padding: 12px 24px;
    border: 0;
    border-radius: 8px;
    font-weight: 600;
    font-size: 14px;
    text-decoration: none;
    display: inline-flex;
    align-items: center;
    gap: 8px;
    transition: all 0.3s cubic-bezier(0.4, 0, 0.2, 1);
    position: relative;
    overflow: hidden;
}

.submission-links .btn::before {
    content: '';
    position: absolute;
    top: 0;
    left: -100%;
    width: 100%;
    height: 100%;
    background: linear-gradient(90deg, transparent, rgba(255,255,255,0.2), transparent);
    transition: left 0.5s;
}

.submission-links .btn:hover::before {
    left: 100%;
}

.submission-links .btn:hover {
    color: #ffffff;
    transform: translateY(-2px);
    box-shadow: 0 8px 24px rgba(2, 127, 247, 0.4);
}

.submission-links .btn:nth-child(2) {
    background: linear-gradient(135deg, #6b7280 0%, #4b5563 100%);
}

.submission-links .btn:nth-child(2):hover {
    box-shadow: 0 8px 24px rgba(107, 114, 128, 0.4);
}

/* Chips and Tags */
.chips-container {
    margin-top: 20px;
    display: flex;
    gap: 8px;
    flex-wrap: wrap;
    align-items: center;
}

.chips-label {
    font-weight: 600;
    color: #374151;
    margin-right: 8px;
    font-size: 0.9rem;
}

.chip {
    background: linear-gradient(135deg, #e6f2ff 0%, #dbeafe 100%);
    color: #1e40af;
    padding: 6px 14px;
    border-radius: 20px;
    font-size: 0.8rem;
    font-weight: 600;
    border: 1px solid #bfdbfe;
    transition: all 0.3s ease;
    text-transform: capitalize;
}

.chip:hover {
    transform: translateY(-1px);
    box-shadow: 0 4px 12px rgba(30, 64, 175, 0.2);
}

.chip.chip-anal-chem-yes {
    background: linear-gradient(135deg, #d1fae5 0%, #a7f3d0 100%);
    color: #059669;
    border-color: #6ee7b7;
}

.chip.chip-anal-chem-no {
    background: linear-gradient(135deg, #fee2e2 0%, #fecaca 100%);
    color: #dc2626;
    border-color: #fca5a5;
}

/* Media Embeds */
.video-container {
    position: relative;
    padding-bottom: 56.25%;
    height: 0;
    overflow: hidden;
    max-width: 100%;
    background: linear-gradient(135deg, #1f2937 0%, #111827 100%);
    margin-bottom: 25px;
    border-radius: 12px;
    box-shadow: 0 8px 24px rgba(0, 0, 0, 0.15);
}

.video-container iframe {
    position: absolute;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    border-radius: 12px;
}

.linkedin-preview {
    border: 2px solid #0077b5;
    border-radius: 12px;
    background: linear-gradient(135deg, #0077b5 0%, #005885 50%, #004471 100%);
    color: white;
    padding: 24px;
    margin-bottom: 25px;
    text-decoration: none;
    display: block;
    transition: all 0.3s cubic-bezier(0.4, 0, 0.2, 1);
    position: relative;
    overflow: hidden;
}

.linkedin-preview::before {
    content: '';
    position: absolute;
    top: 0;
    left: -100%;
    width: 100%;
    height: 100%;
    background: linear-gradient(90deg, transparent, rgba(255,255,255,0.1), transparent);
    transition: left 0.6s;
}

.linkedin-preview:hover::before {
    left: 100%;
}

.linkedin-preview:hover {
    transform: translateY(-3px);
    box-shadow: 0 12px 32px rgba(0, 119, 181, 0.4);
    color: white;
    text-decoration: none;
    border-color: #0088cc;
}

.linkedin-preview-header {
    display: flex;
    align-items: center;
    margin-bottom: 12px;
}

.linkedin-preview-icon {
    width: 28px;
    height: 28px;
    margin-right: 12px;
    fill: currentColor;
    filter: drop-shadow(0 2px 4px rgba(0,0,0,0.2));
}

.linkedin-preview-text {
    font-size: 18px;
    font-weight: 700;
    text-shadow: 0 1px 2px rgba(0,0,0,0.2);
}

.twitter-embed {
    margin-bottom: 25px;
    border-radius: 12px;
    overflow: hidden;
    box-shadow: 0 4px 16px rgba(0, 0, 0, 0.1);
}

/* Responsive Design */
@media (max-width: 768px) {
    .submission-card {
        padding: 20px;
        margin-bottom: 30px;
    }
    
    .submissions-stats {
        gap: 15px;
    }
    
    .stat-item {
        padding: 12px 20px;
    }
    
    .stat-number {
        font-size: 1.5rem;
    }
    
    .submission-links {
        gap: 8px;
    }
    
    .submission-links .btn {
        padding: 10px 18px;
        font-size: 13px;
    }
}

/* Loading Animation */
.loading {
    display: flex;
    justify-content: center;
    align-items: center;
    height: 200px;
    font-size: 1.1rem;
    color: #6b7280;
}

.loading::after {
    content: '';
    width: 20px;
    height: 20px;
    margin-left: 10px;
    border: 2px solid #e5e7eb;
    border-top: 2px solid #027ff7;
    border-radius: 50%;
    animation: spin 1s linear infinite;
}

@keyframes spin {
    0% { transform: rotate(0deg); }
    100% { transform: rotate(360deg); }
}
</style>

<div class="content-section">
    <div class="submissions-header">
        <h1>2025 Hackathon Submissions</h1>
        <p>Explore the innovative projects from our community of materials scientists, chemists, and AI researchers.</p>
        <div class="submissions-stats">
            <div class="stat-item">
                <div class="stat-number" id="total-submissions">-</div>
                <div class="stat-label">Total Submissions</div>
            </div>
            <div class="stat-item">
                <div class="stat-number" id="anal-chem-relevant">-</div>
                <div class="stat-label">Analytical Chemistry</div>
            </div>
            <div class="stat-item">
                <div class="stat-number" id="unique-models">-</div>
                <div class="stat-label">AI Models Used</div>
            </div>
        </div>
    </div>
    
    <div id="submissions-container" class="loading">
        Loading submissions...
    </div>
</div>

<script>
document.addEventListener('DOMContentLoaded', function() {
    fetch('/assets/data/submissions.json')
        .then(response => response.json())
        .then(data => {
            // Calculate statistics
            const totalSubmissions = data.length;
            const analChemRelevant = data.filter(s => s.is_relevant_to_anal_chem === 'Yes').length;
            const allModels = data.flatMap(s => s.models_used ? s.models_used.split(',').map(m => m.trim()) : []);
            const uniqueModels = [...new Set(allModels)].length;

            // Update stats
            document.getElementById('total-submissions').textContent = totalSubmissions;
            document.getElementById('anal-chem-relevant').textContent = analChemRelevant;
            document.getElementById('unique-models').textContent = uniqueModels;

            // Clear loading state
            const container = document.getElementById('submissions-container');
            container.className = '';
            container.innerHTML = '';

            data.forEach(submission => {
                const card = document.createElement('div');
                card.className = 'submission-card';

                let embedContent = '';
                if (submission.submission_link) {
                    let url = submission.submission_link;
                    if (url.includes('youtube.com/watch?v=')) {
                        const videoId = new URL(url).searchParams.get('v');
                        embedContent = `<div class="video-container"><iframe src="https://www.youtube.com/embed/${videoId}" frameborder="0" allowfullscreen></iframe></div>`;
                    } else if (url.includes('youtu.be/')) {
                        const videoId = url.split('youtu.be/')[1].split('?')[0];
                        embedContent = `<div class="video-container"><iframe src="https://www.youtube.com/embed/${videoId}" frameborder="0" allowfullscreen></iframe></div>`;
                    } else if (url.includes('loom.com/share/')) {
                        const videoId = url.split('loom.com/share/')[1].split('?')[0];
                        embedContent = `<div class="video-container"><iframe src="https://www.loom.com/embed/${videoId}" frameborder="0" webkitallowfullscreen mozallowfullscreen allowfullscreen></iframe></div>`;
                    } else if (url.includes('linkedin.com/posts/') || url.includes('linkedin.com/feed/update/')) {
                        embedContent = `
                            <a href="${url}" target="_blank" rel="noopener" class="linkedin-preview">
                                <div class="linkedin-preview-header">
                                    <svg class="linkedin-preview-icon" viewBox="0 0 24 24">
                                        <path d="M20.447 20.452h-3.554v-5.569c0-1.328-.027-3.037-1.852-3.037-1.853 0-2.136 1.445-2.136 2.939v5.667H9.351V9h3.414v1.561h.046c.477-.9 1.637-1.85 3.37-1.85 3.601 0 4.267 2.37 4.267 5.455v6.286zM5.337 7.433c-1.144 0-2.063-.926-2.063-2.065 0-1.138.92-2.063 2.063-2.063 1.14 0 2.064.925 2.064 2.063 0 1.139-.925 2.065-2.064 2.065zm1.782 13.019H3.555V9h3.564v11.452zM22.225 0H1.771C.792 0 0 .774 0 1.729v20.542C0 23.227.792 24 1.771 24h20.451C23.2 24 24 23.227 24 22.271V1.729C24 .774 23.2 0 22.222 0h.003z"/>
                                    </svg>
                                    <span class="linkedin-preview-text">View LinkedIn Post</span>
                                </div>
                                <p style="margin: 0; opacity: 0.9; font-size: 14px;">Click to view this submission's LinkedIn post</p>
                            </a>
                        `;
                    } else if (url.includes('x.com/') || url.includes('twitter.com/')) {
                        embedContent = `<div class="twitter-embed"><blockquote class="twitter-tweet"><a href="${url}"></a></blockquote></div>`;
                    }
                }
                
                let modelsUsedChips = '';
                if(submission.models_used){
                    modelsUsedChips = submission.models_used.split(',').map(model => `<span class="chip">${model.trim()}</span>`).join('');
                }

                const isRelevantChip = `<span class="chip ${submission.is_relevant_to_anal_chem === 'Yes' ? 'chip-anal-chem-yes' : 'chip-anal-chem-no'}">${submission.is_relevant_to_anal_chem === 'Yes' ? 'Relevant to Analytical Chemistry' : 'Not Relevant to Analytical Chemistry'}</span>`;

                card.innerHTML = `
                    ${embedContent}
                    <h3>${submission.team_name}</h3>
                    <div class="submission-section">
                        <div class="submission-section-title">Team Members</div>
                        <div class="submission-content">${submission.team_members}</div>
                    </div>
                    <div class="submission-section">
                        <div class="submission-section-title">Description</div>
                        <div class="submission-content">${submission.description}</div>
                    </div>
                    <div class="submission-section">
                        <div class="submission-section-title">Project Novelty</div>
                        <div class="submission-content">${submission.project_novelty}</div>
                    </div>
                    <div class="chips-container">
                        <div class="chips-label">Models Used:</div>
                        ${modelsUsedChips}
                    </div>
                    <div class="chips-container">
                        ${isRelevantChip}
                    </div>
                    <div class="submission-links">
                        <a href="${submission.submission_link}" class="btn" target="_blank" rel="noopener">
                            <svg width="16" height="16" viewBox="0 0 24 24" fill="currentColor">
                                <path d="M14,3V5H17.59L7.76,14.83L9.17,16.24L19,6.41V10H21V3M19,19H5V5H12V3H5C3.89,3 3,3.9 3,5V19A2,2 0 0,0 5,21H19A2,2 0 0,0 21,19V12H19V19Z"/>
                            </svg>
                            View Submission
                        </a>
                        ${submission.code_link ? `<a href="${submission.code_link}" class="btn" target="_blank" rel="noopener">
                            <svg width="16" height="16" viewBox="0 0 24 24" fill="currentColor">
                                <path d="M12,2A10,10 0 0,0 2,12C2,16.42 4.87,20.17 8.84,21.5C9.34,21.58 9.5,21.27 9.5,21C9.5,20.77 9.5,20.14 9.5,19.31C6.73,19.91 6.14,17.97 6.14,17.97C5.68,16.81 5.03,16.5 5.03,16.5C4.12,15.88 5.1,15.9 5.1,15.9C6.1,15.97 6.63,16.93 6.63,16.93C7.5,18.45 8.97,18 9.54,17.76C9.63,17.11 9.89,16.67 10.17,16.42C7.95,16.17 5.62,15.31 5.62,11.5C5.62,10.39 6,9.5 6.65,8.79C6.55,8.54 6.2,7.5 6.75,6.15C6.75,6.15 7.59,5.88 9.5,7.17C10.29,6.95 11.15,6.84 12,6.84C12.85,6.84 13.71,6.95 14.5,7.17C16.41,5.88 17.25,6.15 17.25,6.15C17.8,7.5 17.45,8.54 17.35,8.79C18,9.5 18.38,10.39 18.38,11.5C18.38,15.32 16.04,16.16 13.81,16.41C14.17,16.72 14.5,17.33 14.5,18.26C14.5,19.6 14.5,20.68 14.5,21C14.5,21.27 14.66,21.59 15.17,21.5C19.14,20.16 22,16.42 22,12A10,10 0 0,0 12,2Z"/>
                            </svg>
                            View Code
                        </a>` : ''}
                    </div>
                `;
                container.appendChild(card);
            });

            if (document.querySelector('.twitter-tweet')) {
                const script = document.createElement('script');
                script.src = 'https://platform.twitter.com/widgets.js';
                script.charset = 'utf-8';
                script.async = true;
                document.body.appendChild(script);
            }
        })
        .catch(error => {
            const container = document.getElementById('submissions-container');
            container.innerHTML = '<div style="text-align: center; color: #dc2626; padding: 40px;">Error loading submissions. Please try again later.</div>';
        });
});
</script>
