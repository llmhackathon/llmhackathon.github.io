---
layout: page
title: Submissions
permalink: /submissions/
---

<style>
/* Search and Filter Section */
.search-filter-section {
    background: white;
    border-radius: 16px;
    padding: 30px;
    margin-bottom: 30px;
    box-shadow: 0 4px 20px rgba(0, 0, 0, 0.08);
    border: 1px solid #e8f0fe;
}

.search-box-container {
    position: relative;
    margin-bottom: 24px;
}

.search-icon {
    position: absolute;
    left: 18px;
    top: 50%;
    transform: translateY(-50%);
    width: 20px;
    height: 20px;
    color: #6b7280;
    pointer-events: none;
}

#search-input {
    width: 100%;
    padding: 16px 50px 16px 50px;
    font-size: 1rem;
    border: 2px solid #e5e7eb;
    border-radius: 12px;
    transition: all 0.3s ease;
    background: #fafbfc;
}

#search-input:focus {
    outline: none;
    border-color: #027ff7;
    background: white;
    box-shadow: 0 0 0 4px rgba(2, 127, 247, 0.1);
}

#search-input::placeholder {
    color: #9ca3af;
}

.clear-search-btn {
    position: absolute;
    right: 18px;
    top: 50%;
    transform: translateY(-50%);
    background: none;
    border: none;
    cursor: pointer;
    color: #9ca3af;
    font-size: 20px;
    padding: 4px 8px;
    display: none;
    transition: color 0.2s ease;
}

.clear-search-btn:hover {
    color: #374151;
}

.clear-search-btn.visible {
    display: block;
}

.filters-container {
    display: flex;
    gap: 12px;
    flex-wrap: wrap;
    align-items: center;
    margin-bottom: 16px;
}

.filter-group {
    position: relative;
    flex: 1;
    min-width: 200px;
}

.filter-group label {
    display: block;
    font-size: 0.85rem;
    font-weight: 600;
    color: #374151;
    margin-bottom: 6px;
    text-transform: uppercase;
    letter-spacing: 0.5px;
}

.filter-group select {
    width: 100%;
    padding: 10px 16px;
    font-size: 0.9rem;
    border: 2px solid #e5e7eb;
    border-radius: 8px;
    background: white;
    cursor: pointer;
    transition: all 0.2s ease;
    appearance: none;
    background-image: url("data:image/svg+xml,%3Csvg xmlns='http://www.w3.org/2000/svg' width='12' height='12' viewBox='0 0 12 12'%3E%3Cpath fill='%236b7280' d='M6 9L1 4h10z'/%3E%3C/svg%3E");
    background-repeat: no-repeat;
    background-position: right 12px center;
    padding-right: 36px;
}

.filter-group select:focus {
    outline: none;
    border-color: #027ff7;
    box-shadow: 0 0 0 3px rgba(2, 127, 247, 0.1);
}

.filter-group select:hover {
    border-color: #cbd5e1;
}

.active-filters {
    display: flex;
    gap: 8px;
    flex-wrap: wrap;
    align-items: center;
    min-height: 32px;
}

.active-filter-chip {
    display: inline-flex;
    align-items: center;
    gap: 6px;
    background: linear-gradient(135deg, #027ff7, #0259ce);
    color: white;
    padding: 6px 12px;
    border-radius: 20px;
    font-size: 0.85rem;
    font-weight: 600;
    animation: slideIn 0.3s ease;
}

.active-filter-chip .remove-filter {
    background: rgba(255, 255, 255, 0.25);
    border: none;
    color: white;
    width: 18px;
    height: 18px;
    border-radius: 50%;
    cursor: pointer;
    display: flex;
    align-items: center;
    justify-content: center;
    font-size: 14px;
    line-height: 1;
    transition: background 0.2s ease;
}

.active-filter-chip .remove-filter:hover {
    background: rgba(255, 255, 255, 0.4);
}

.clear-all-filters {
    background: #f3f4f6;
    color: #374151;
    border: none;
    padding: 6px 14px;
    border-radius: 20px;
    font-size: 0.85rem;
    font-weight: 600;
    cursor: pointer;
    transition: all 0.2s ease;
}

.clear-all-filters:hover {
    background: #e5e7eb;
    color: #111827;
}

@keyframes slideIn {
    from {
        opacity: 0;
        transform: translateY(-10px);
    }
    to {
        opacity: 1;
        transform: translateY(0);
    }
}

.results-info {
    display: flex;
    justify-content: space-between;
    align-items: center;
    padding: 16px 0;
    margin-bottom: 16px;
    border-bottom: 2px solid #e5e7eb;
}

.results-count {
    font-size: 1rem;
    color: #374151;
    font-weight: 600;
}

.results-count .count-number {
    color: #027ff7;
    font-size: 1.25rem;
    font-weight: 700;
}

.sort-group {
    display: flex;
    align-items: center;
    gap: 10px;
}

.sort-group label {
    font-size: 0.9rem;
    color: #6b7280;
    font-weight: 500;
}

.sort-group select {
    padding: 8px 32px 8px 12px;
    font-size: 0.9rem;
    border: 2px solid #e5e7eb;
    border-radius: 8px;
    background: white;
    cursor: pointer;
    transition: all 0.2s ease;
    appearance: none;
    background-image: url("data:image/svg+xml,%3Csvg xmlns='http://www.w3.org/2000/svg' width='12' height='12' viewBox='0 0 12 12'%3E%3Cpath fill='%236b7280' d='M6 9L1 4h10z'/%3E%3C/svg%3E");
    background-repeat: no-repeat;
    background-position: right 10px center;
}

.sort-group select:focus {
    outline: none;
    border-color: #027ff7;
}

.no-results {
    text-align: center;
    padding: 60px 20px;
    color: #6b7280;
}

.no-results-icon {
    font-size: 4rem;
    margin-bottom: 16px;
    opacity: 0.3;
}

.no-results h3 {
    font-size: 1.5rem;
    color: #374151;
    margin-bottom: 8px;
}

.no-results p {
    font-size: 1rem;
    color: #6b7280;
}

/* Page Header */
.submissions-header {
    display: flex;
    justify-content: space-between;
    align-items: center;
    margin-bottom: 30px;
    padding: 24px 30px;
    background: linear-gradient(135deg, #f8fbff 0%, #e6f2ff 100%);
    border-radius: 16px;
    border: 1px solid #e0efff;
    flex-wrap: wrap;
    gap: 20px;
}

.submissions-stats {
    display: flex;
    gap: 24px;
    flex-wrap: wrap;
    flex: 1;
}

.stat-item {
    text-align: center;
    padding: 12px 20px;
    background: white;
    border-radius: 10px;
    box-shadow: 0 2px 8px rgba(0, 0, 0, 0.06);
    border: 1px solid #e2e2e2;
    min-width: 140px;
}

.stat-number {
    font-size: 1.75rem;
    font-weight: 700;
    color: #027ff7;
    margin-bottom: 4px;
}

.stat-label {
    font-size: 0.8rem;
    color: #666;
    font-weight: 500;
    text-transform: uppercase;
    letter-spacing: 0.5px;
}

.header-awards-button {
    display: inline-flex;
    align-items: center;
    gap: 10px;
    background: linear-gradient(120deg, #2563eb, #0ea5e9);
    color: white;
    padding: 14px 28px;
    border-radius: 999px;
    font-weight: 600;
    font-size: 0.95rem;
    text-decoration: none;
    box-shadow: 0 8px 24px rgba(37, 99, 235, 0.3);
    transition: transform 0.25s ease, box-shadow 0.25s ease, filter 0.25s ease;
    white-space: nowrap;
}

.header-awards-button:hover {
    transform: translateY(-2px);
    box-shadow: 0 12px 32px rgba(14, 165, 233, 0.4);
    filter: brightness(1.05);
    color: white;
    text-decoration: none;
}

.header-awards-button svg {
    width: 18px;
    height: 18px;
}

/* Submission Cards */
.submission-card {
    background: linear-gradient(to bottom, #ffffff 0%, #fafbfc 100%);
    border: 1px solid #e8f0fe;
    border-radius: 20px;
    padding: 35px;
    margin-bottom: 32px;
    box-shadow: 0 4px 20px rgba(0, 0, 0, 0.05), 0 1px 3px rgba(0, 0, 0, 0.05);
    transition: all 0.35s cubic-bezier(0.4, 0, 0.2, 1);
    position: relative;
    overflow: hidden;
    animation: fadeInUp 0.5s ease forwards;
    opacity: 0;
}

@keyframes fadeInUp {
    from {
        opacity: 0;
        transform: translateY(20px);
    }
    to {
        opacity: 1;
        transform: translateY(0);
    }
}

.submission-card::before {
    content: '';
    position: absolute;
    top: 0;
    left: 0;
    right: 0;
    height: 5px;
    background: linear-gradient(90deg, #027ff7, #0ea5e9, #6366f1);
    border-radius: 20px 20px 0 0;
}

.submission-card:hover {
    transform: translateY(-6px);
    box-shadow: 0 20px 60px rgba(2, 127, 247, 0.15), 0 8px 24px rgba(0, 0, 0, 0.1);
    border-color: #027ff7;
    background: #ffffff;
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
    min-width: fit-content;
}

/* Base chip styling - clean monochromatic approach */
.chip {
    background: #f8fafc;
    color: #475569;
    padding: 6px 14px;
    border-radius: 20px;
    font-size: 0.8rem;
    font-weight: 600;
    border: 1px solid #e2e8f0;
    transition: all 0.3s ease;
    text-transform: capitalize;
    white-space: nowrap;
}

.chip:hover {
    transform: translateY(-1px);
    background: #f1f5f9;
    border-color: #cbd5e1;
    box-shadow: 0 4px 12px rgba(71, 85, 105, 0.15);
}

/* Primary Category Badge */
.primary-category {
    background: linear-gradient(135deg, #8b5cf6 0%, #7c3aed 100%);
    color: white;
    padding: 8px 16px;
    border-radius: 24px;
    font-size: 0.85rem;
    font-weight: 700;
    text-transform: uppercase;
    letter-spacing: 0.5px;
    display: inline-block;
    margin-bottom: 15px;
    border: 1px solid #a855f7;
    box-shadow: 0 2px 8px rgba(139, 92, 246, 0.3);
    text-decoration: none;
}

.primary-category:hover {
    transform: translateY(-1px);
    box-shadow: 0 4px 12px rgba(139, 92, 246, 0.4);
}

/* Enhanced chip variants with subtle visual differentiation */
.chip.domain-area {
    background: #eff6ff;
    color: #1e40af;
    border-color: #dbeafe;
    position: relative;
}

.chip.domain-area::before {
    content: '';
    position: absolute;
    left: 4px;
    top: 50%;
    transform: translateY(-50%);
    width: 4px;
    height: 4px;
    background: #3b82f6;
    border-radius: 50%;
}

.chip.domain-area:hover {
    background: #dbeafe;
    color: #1d4ed8;
}

.chip.modality {
    background: #f0f9ff;
    color: #0284c7;
    border-color: #e0f2fe;
    position: relative;
}

.chip.modality::before {
    content: '';
    position: absolute;
    left: 4px;
    top: 50%;
    transform: translateY(-50%);
    width: 4px;
    height: 4px;
    background: #0ea5e9;
    border-radius: 50%;
}

.chip.modality:hover {
    background: #e0f2fe;
    color: #0369a1;
}

.chip.model {
    background: #f9fafb;
    color: #374151;
    border-color: #d1d5db;
    font-weight: 700;
}

.chip.model:hover {
    background: #f3f4f6;
    color: #111827;
    border-color: #9ca3af;
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
        padding: 24px;
        margin-bottom: 24px;
        border-radius: 16px;
    }
    
    .submissions-header {
        padding: 20px;
        flex-direction: column;
        align-items: stretch;
    }
    
    .submissions-stats {
        gap: 10px;
        justify-content: center;
    }
    
    .stat-item {
        padding: 10px 16px;
        min-width: 100px;
        flex: 1;
    }
    
    .stat-number {
        font-size: 1.5rem;
    }
    
    .stat-label {
        font-size: 0.7rem;
    }
    
    .header-awards-button {
        width: 100%;
        justify-content: center;
        padding: 12px 24px;
        font-size: 0.9rem;
    }
    
    .submission-links {
        gap: 8px;
    }
    
    .submission-links .btn {
        padding: 10px 18px;
        font-size: 13px;
    }
    
    .search-filter-section {
        padding: 20px;
    }
    
    .filters-container {
        flex-direction: column;
    }
    
    .filter-group {
        min-width: 100%;
    }
    
    .results-info {
        flex-direction: column;
        gap: 12px;
        align-items: flex-start;
    }
    
    .chips-container {
        flex-wrap: wrap;
    }
    
    .submission-card h3 {
        font-size: 1.25rem;
    }
}

@media (max-width: 480px) {
    .submissions-stats {
        flex-direction: column;
    }
    
    .stat-item {
        width: 100%;
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
        <div class="submissions-stats">
            <div class="stat-item">
                <div class="stat-number" id="total-submissions">-</div>
                <div class="stat-label">Submissions</div>
            </div>
            <div class="stat-item">
                <div class="stat-number" id="unique-models">-</div>
                <div class="stat-label">AI Models</div>
            </div>
            <div class="stat-item">
                <div class="stat-number" id="unique-categories">-</div>
                <div class="stat-label">Categories</div>
            </div>
        </div>
        <a class="header-awards-button" href="{{ '/awards/' | relative_url }}">
            <svg viewBox="0 0 24 24" fill="currentColor" aria-hidden="true">
                <path d="M17 3V5H21V7C21 10.31 18.31 13 15 13C13.48 13 12.09 12.45 11 11.56C9.91 12.45 8.52 13 7 13C3.69 13 1 10.31 1 7V5H5V3H17M5 7H3C3 9.21 4.79 11 7 11C8.68 11 10.1 9.95 10.66 8.5H5V7M19 7H13.34C13.9 8.95 15.32 10 17 10C19.21 10 21 8.21 21 6H19V7M13 15.91C14.25 16.57 16.19 17 18 17V19C16.37 19 14.4 18.5 13 17.68V21H9V17.68C7.6 18.5 5.63 19 4 19V17C5.81 17 7.75 16.57 9 15.91V15H13V15.91Z" />
            </svg>
            View Awards
        </a>
    </div>
    
    <!-- Search and Filter Section -->
    <div class="search-filter-section">
        <div class="search-box-container">
            <svg class="search-icon" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2">
                <circle cx="11" cy="11" r="8"></circle>
                <path d="m21 21-4.35-4.35"></path>
            </svg>
            <input type="text" id="search-input" placeholder="Search by team name, members, or description...">
            <button class="clear-search-btn" id="clear-search">×</button>
        </div>
        
        <div class="filters-container">
            <div class="filter-group">
                <label for="category-filter">Category</label>
                <select id="category-filter">
                    <option value="">All Categories</option>
                </select>
            </div>
            <div class="filter-group">
                <label for="domain-filter">Domain Area</label>
                <select id="domain-filter">
                    <option value="">All Domains</option>
                </select>
            </div>
            <div class="filter-group">
                <label for="award-filter">Award Status</label>
                <select id="award-filter">
                    <option value="">All Submissions</option>
                    <option value="awarded">Award Winners Only</option>
                    <option value="not-awarded">Non-Award Winners</option>
                </select>
            </div>
        </div>
        
        <div class="active-filters" id="active-filters"></div>
    </div>
    
    <!-- Results Info -->
    <div class="results-info" id="results-info" style="display: none;">
        <div class="results-count">
            Showing <span class="count-number" id="results-count">0</span> of <span id="total-count">0</span> submissions
        </div>
        <div class="sort-group">
            <label for="sort-select">Sort by:</label>
            <select id="sort-select">
                <option value="default">Default</option>
                <option value="name-asc">Team Name (A-Z)</option>
                <option value="name-desc">Team Name (Z-A)</option>
            </select>
        </div>
    </div>
    
    <div id="submissions-container" class="loading">
        Loading submissions...
    </div>
</div>

<script>
document.addEventListener('DOMContentLoaded', function() {
    let allSubmissions = [];
    let filteredSubmissions = [];
    
    // Async indexes for faster filtering
    let categoryIndex = new Map();
    let domainIndex = new Map();
    
    // State for filters
    const filters = {
        search: '',
        category: '',
        domain: '',
        award: ''
    };
    
    fetch('/assets/data/submissions.json')
        .then(response => response.json())
        .then(data => {
            allSubmissions = data;
            filteredSubmissions = data;
            
            // Calculate statistics
            const totalSubmissions = data.length;
            const allModels = data.flatMap(s => s.models_used ? s.models_used.split(',').map(m => m.trim()) : []);
            const uniqueModels = [...new Set(allModels)].length;
            const allCategories = data.map(s => s.primary_category).filter(Boolean);
            const uniqueCategories = [...new Set(allCategories)].length;

            // Update stats
            document.getElementById('total-submissions').textContent = totalSubmissions;
            document.getElementById('unique-models').textContent = uniqueModels;
            document.getElementById('unique-categories').textContent = uniqueCategories;
            document.getElementById('total-count').textContent = totalSubmissions;
            
            // Populate filter dropdowns
            populateFilters(data);
            
            // Build indexes asynchronously
            buildIndexes(data);
            
            // Initial render
            renderSubmissions(filteredSubmissions);
            
            // Set up event listeners
            setupEventListeners();
        })
        .catch(error => {
            const container = document.getElementById('submissions-container');
            container.innerHTML = '<div style="text-align: center; color: #dc2626; padding: 40px;">Error loading submissions. Please try again later.</div>';
        });
    
    // Build search indexes asynchronously for faster filtering
    function buildIndexes(data) {
        // Use setTimeout to make it async and not block rendering
        setTimeout(() => {
            // Build category index
            data.forEach((submission, index) => {
                if (submission.primary_category) {
                    if (!categoryIndex.has(submission.primary_category)) {
                        categoryIndex.set(submission.primary_category, []);
                    }
                    categoryIndex.get(submission.primary_category).push(index);
                }
                
                // Build domain index
                if (submission.facets && submission.facets.domain_area) {
                    submission.facets.domain_area.forEach(domain => {
                        if (!domainIndex.has(domain)) {
                            domainIndex.set(domain, []);
                        }
                        domainIndex.get(domain).push(index);
                    });
                }
            });
            console.log('Search indexes built: Category entries:', categoryIndex.size, 'Domain entries:', domainIndex.size);
        }, 0);
    }
    
    function populateFilters(data) {
        // Populate categories
        const categories = [...new Set(data.map(s => s.primary_category).filter(Boolean))].sort();
        const categorySelect = document.getElementById('category-filter');
        categories.forEach(cat => {
            const option = document.createElement('option');
            option.value = cat;
            option.textContent = formatCategoryName(cat);
            categorySelect.appendChild(option);
        });
        
        // Populate domains
        const domains = [...new Set(data.flatMap(s => s.facets?.domain_area || []))].sort();
        const domainSelect = document.getElementById('domain-filter');
        domains.forEach(domain => {
            const option = document.createElement('option');
            option.value = domain;
            option.textContent = domain.replace(/_/g, ' ').replace(/\b\w/g, l => l.toUpperCase());
            domainSelect.appendChild(option);
        });
    }
    
    function setupEventListeners() {
        // Search input
        const searchInput = document.getElementById('search-input');
        const clearSearchBtn = document.getElementById('clear-search');
        
        searchInput.addEventListener('input', (e) => {
            filters.search = e.target.value.toLowerCase();
            clearSearchBtn.classList.toggle('visible', e.target.value.length > 0);
            applyFilters();
        });
        
        clearSearchBtn.addEventListener('click', () => {
            searchInput.value = '';
            filters.search = '';
            clearSearchBtn.classList.remove('visible');
            applyFilters();
        });
        
        // Filter dropdowns
        document.getElementById('category-filter').addEventListener('change', (e) => {
            filters.category = e.target.value;
            applyFilters();
        });
        
        document.getElementById('domain-filter').addEventListener('change', (e) => {
            filters.domain = e.target.value;
            applyFilters();
        });
        
        document.getElementById('award-filter').addEventListener('change', (e) => {
            filters.award = e.target.value;
            applyFilters();
        });
        
        // Sort
        document.getElementById('sort-select').addEventListener('change', (e) => {
            sortSubmissions(e.target.value);
        });
    }
    
    function applyFilters() {
        // Use indexes when available for faster filtering
        let candidateIndices = null;
        
        // Start with category filter using index if available
        if (filters.category) {
            candidateIndices = categoryIndex.has(filters.category) 
                ? new Set(categoryIndex.get(filters.category))
                : new Set();
        }
        
        // Apply domain filter using index if available
        if (filters.domain) {
            const domainIndices = domainIndex.has(filters.domain)
                ? new Set(domainIndex.get(filters.domain))
                : new Set();
            
            if (candidateIndices === null) {
                candidateIndices = domainIndices;
            } else {
                // Intersection of category and domain
                candidateIndices = new Set([...candidateIndices].filter(x => domainIndices.has(x)));
            }
        }
        
        // If we have candidate indices from indexed filters, use them
        const candidates = candidateIndices !== null
            ? [...candidateIndices].map(i => allSubmissions[i])
            : allSubmissions;
        
        // Apply search and award filters
        filteredSubmissions = candidates.filter(submission => {
            if (filters.search) {
                const searchLower = filters.search;
                const matchesSearch = 
                    submission.team_name.toLowerCase().includes(searchLower) ||
                    submission.team_members.toLowerCase().includes(searchLower) ||
                    submission.description.toLowerCase().includes(searchLower) ||
                    (submission.project_novelty && submission.project_novelty.toLowerCase().includes(searchLower));
                
                if (!matchesSearch) return false;
            }
            
            // Apply award filter
            if (filters.award) {
                if (filters.award === 'awarded' && !submission.award) {
                    return false;
                } else if (filters.award === 'not-awarded' && submission.award) {
                    return false;
                }
            }
            
            return true;
        });
        
        updateActiveFilters();
        renderSubmissions(filteredSubmissions);
    }
    
    function updateActiveFilters() {
        const activeFiltersContainer = document.getElementById('active-filters');
        activeFiltersContainer.innerHTML = '';
        
        let hasFilters = false;
        
        if (filters.search) {
            hasFilters = true;
            addFilterChip('Search: "' + filters.search + '"', 'search');
        }
        
        if (filters.category) {
            hasFilters = true;
            addFilterChip('Category: ' + formatCategoryName(filters.category), 'category');
        }
        
        if (filters.domain) {
            hasFilters = true;
            addFilterChip('Domain: ' + filters.domain.replace(/_/g, ' '), 'domain');
        }
        
        if (filters.award) {
            hasFilters = true;
            const awardLabel = filters.award === 'awarded' ? 'Award Winners Only' : 'Non-Award Winners';
            addFilterChip('Award: ' + awardLabel, 'award');
        }
        
        if (hasFilters) {
            const clearAllBtn = document.createElement('button');
            clearAllBtn.className = 'clear-all-filters';
            clearAllBtn.textContent = 'Clear All';
            clearAllBtn.onclick = clearAllFilters;
            activeFiltersContainer.appendChild(clearAllBtn);
        }
    }
    
    function addFilterChip(text, filterType) {
        const activeFiltersContainer = document.getElementById('active-filters');
        const chip = document.createElement('div');
        chip.className = 'active-filter-chip';
        chip.innerHTML = `
            ${text}
            <button class="remove-filter" onclick="removeFilter('${filterType}')">×</button>
        `;
        activeFiltersContainer.appendChild(chip);
    }
    
    window.removeFilter = function(filterType) {
        filters[filterType] = '';
        
        // Reset the corresponding UI element
        if (filterType === 'search') {
            document.getElementById('search-input').value = '';
            document.getElementById('clear-search').classList.remove('visible');
        } else if (filterType === 'category') {
            document.getElementById('category-filter').value = '';
        } else if (filterType === 'domain') {
            document.getElementById('domain-filter').value = '';
        } else if (filterType === 'award') {
            document.getElementById('award-filter').value = '';
        }
        
        applyFilters();
    };
    
    function clearAllFilters() {
        filters.search = '';
        filters.category = '';
        filters.domain = '';
        filters.award = '';
        
        document.getElementById('search-input').value = '';
        document.getElementById('clear-search').classList.remove('visible');
        document.getElementById('category-filter').value = '';
        document.getElementById('domain-filter').value = '';
        document.getElementById('award-filter').value = '';
        
        applyFilters();
    }
    
    function sortSubmissions(sortBy) {
        if (sortBy === 'name-asc') {
            filteredSubmissions.sort((a, b) => a.team_name.localeCompare(b.team_name));
        } else if (sortBy === 'name-desc') {
            filteredSubmissions.sort((a, b) => b.team_name.localeCompare(a.team_name));
        } else {
            // Reset to original order
            filteredSubmissions = allSubmissions.filter(s => filteredSubmissions.includes(s));
        }
        renderSubmissions(filteredSubmissions);
    }
    
    function renderSubmissions(submissions) {
        const container = document.getElementById('submissions-container');
        const resultsInfo = document.getElementById('results-info');
        const resultsCount = document.getElementById('results-count');
        
        // Update results count
        resultsCount.textContent = submissions.length;
        resultsInfo.style.display = 'flex';
        
        // Clear container
        container.className = '';
        container.innerHTML = '';
        
        if (submissions.length === 0) {
            container.innerHTML = `
                <div class="no-results">
                    <div class="no-results-icon">🔍</div>
                    <h3>No submissions found</h3>
                    <p>Try adjusting your search or filters</p>
                </div>
            `;
            return;
        }

        submissions.forEach((submission, index) => {
                const card = document.createElement('div');
                card.className = 'submission-card';
                card.style.animationDelay = `${index * 0.05}s`;

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
                
                // Helper function to format category names
                function formatCategoryName(category) {
                    return category.replace(/_/g, ' ').replace(/\b\w/g, l => l.toUpperCase());
                }

                // Create award badge
                let awardBadge = '';
                if (submission.award) {
                    awardBadge = `<div class="award-badge">${submission.award}</div>`;
                }

                // Create primary category badge
                let primaryCategoryBadge = '';
                if (submission.primary_category) {
                    primaryCategoryBadge = `<div class="primary-category">${formatCategoryName(submission.primary_category)}</div>`;
                }

                // Create domain area chips
                let domainAreaChips = '';
                if (submission.facets && submission.facets.domain_area) {
                    domainAreaChips = submission.facets.domain_area.map(domain => 
                        `<span class="chip domain-area">${domain.replace(/_/g, ' ')}</span>`
                    ).join('');
                }

                // Create modality chips
                let modalityChips = '';
                if (submission.facets && submission.facets.modality) {
                    modalityChips = submission.facets.modality.map(modality => 
                        `<span class="chip modality">${modality.replace(/_/g, ' ')}</span>`
                    ).join('');
                }

                // Create model chips
                let modelsUsedChips = '';
                if(submission.models_used){
                    modelsUsedChips = submission.models_used.split(',').map(model => 
                        `<span class="chip model">${model.trim()}</span>`
                    ).join('');
                }


                card.innerHTML = `
                    ${embedContent}
                    ${awardBadge}
                    ${primaryCategoryBadge}
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
                    ${domainAreaChips ? `<div class="chips-container">
                        <div class="chips-label">Domain Areas:</div>
                        ${domainAreaChips}
                    </div>` : ''}
                    ${modalityChips ? `<div class="chips-container">
                        <div class="chips-label">Modalities:</div>
                        ${modalityChips}
                    </div>` : ''}
                    ${modelsUsedChips ? `<div class="chips-container">
                        <div class="chips-label">AI Models:</div>
                        ${modelsUsedChips}
                    </div>` : ''}
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

            // Load Twitter widgets if needed
            if (document.querySelector('.twitter-tweet')) {
                const script = document.createElement('script');
                script.src = 'https://platform.twitter.com/widgets.js';
                script.charset = 'utf-8';
                script.async = true;
                document.body.appendChild(script);
            }
    }
    
    // Helper function to format category names
    function formatCategoryName(category) {
        return category.replace(/_/g, ' ').replace(/\b\w/g, l => l.toUpperCase());
    }
});
</script>
