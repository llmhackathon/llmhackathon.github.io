---
layout: page
title: 2025 Awards
permalink: /awards/
---

<style>
.awards-wrapper {
    display: flex;
    flex-direction: column;
    gap: 48px;
}

.awards-intro {
    font-size: 1rem;
    line-height: 1.7;
    color: #1e293b;
    background: linear-gradient(135deg, rgba(37, 99, 235, 0.1) 0%, rgba(14, 165, 233, 0.14) 100%);
    border: 1px solid rgba(148, 163, 184, 0.18);
    border-radius: 20px;
    padding: 32px;
    box-shadow: 0 20px 55px rgba(15, 23, 42, 0.12);
}

.awards-section h2 {
    font-size: 1.8rem;
    margin-bottom: 12px;
}

.awards-section p.section-copy {
    color: #475569;
    margin-bottom: 28px;
    max-width: 760px;
}

.award-grid {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
    gap: 24px;
}

.award-card {
    background: #ffffff;
    border-radius: 18px;
    border: 1px solid rgba(226, 232, 240, 0.9);
    padding: 28px;
    box-shadow: 0 16px 44px rgba(15, 23, 42, 0.1);
    display: flex;
    flex-direction: column;
    gap: 16px;
    position: relative;
}

.award-card::before {
    content: "";
    position: absolute;
    inset: 0;
    border-radius: 18px;
    padding: 1px;
    background: linear-gradient(135deg, rgba(37, 99, 235, 0.35), rgba(14, 165, 233, 0.2));
    -webkit-mask: linear-gradient(#fff 0 0) content-box, linear-gradient(#fff 0 0);
    -webkit-mask-composite: xor;
    mask-composite: exclude;
    opacity: 0;
    transition: opacity 0.3s ease;
}

.award-card:hover::before {
    opacity: 1;
}

.award-rank {
    text-transform: uppercase;
    letter-spacing: 0.12em;
    font-size: 0.85rem;
    font-weight: 700;
    color: #1d4ed8;
}

.award-card h3 {
    margin: 0;
    font-size: 1.35rem;
    color: #0f172a;
}

.award-team {
    font-size: 0.95rem;
    color: #475569;
}

.award-description {
    font-size: 0.95rem;
    color: #334155;
    line-height: 1.65;
}

.award-footer {
    margin-top: auto;
}

.award-button {
    display: inline-flex;
    align-items: center;
    justify-content: center;
    gap: 8px;
    padding: 12px 22px;
    border-radius: 999px;
    background: linear-gradient(120deg, #2563eb, #0ea5e9);
    color: #fff;
    font-weight: 600;
    font-size: 0.95rem;
    text-decoration: none;
    box-shadow: 0 18px 36px rgba(37, 99, 235, 0.25);
    transition: transform 0.25s ease, box-shadow 0.25s ease, filter 0.25s ease;
}

.award-button:hover {
    transform: translateY(-2px);
    box-shadow: 0 24px 56px rgba(14, 165, 233, 0.35);
    filter: brightness(1.03);
}

.award-button svg {
    width: 16px;
    height: 16px;
}

.visionary-card {
    background: #fff;
    border: 1px solid rgba(226, 232, 240, 0.9);
    border-radius: 18px;
    padding: 28px;
    box-shadow: 0 16px 44px rgba(15, 23, 42, 0.1);
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
    color: #334155;
}

@media (max-width: 768px) {
    .awards-intro {
        padding: 24px;
    }

    .award-grid {
        grid-template-columns: 1fr;
    }

    .visionary-card ul {
        columns: 1;
    }
}
</style>

<div class="awards-wrapper">
    <div class="awards-intro">
        Congratulations to the Lila Prize winning teams for top-scoring overall projects! Please take a moment to celebrate the teams below, explore their project descriptions, and watch their demos. We will be posting these to the website and contacting teams shortly.
    </div>

    <section class="awards-section" aria-label="Lila Prize Winners">
        <h2>Lila Prize Winners</h2>
        <div class="award-grid">
            <article class="award-card">
                <span class="award-rank">1st place</span>
                <h3>Materials Design Group</h3>
                <p class="award-team">Ryan Nduma, Hyunsoo Park, Kinga Mastej &mdash; Imperial College London</p>
                <p class="award-description">SKY is an LLM-powered synthesis exploration agent for inorganic materials. It performs composition and structure similarity searches on the Materials Project, retrieves neighbor synthesis recipes with metadata, and surfaces property and structure summaries. An LLM fuses those neighbors into target-specific protocols with confidence scores, parameter deltas, and citations, producing both readable summaries and JSON outputs to accelerate hypothesis generation when direct recipes do not exist.</p>
                <div class="award-footer">
                    <a class="award-button" href="https://youtu.be/ffLqLH87yLo" target="_blank" rel="noopener">
                        <svg viewBox="0 0 24 24" fill="currentColor" aria-hidden="true">
                            <path d="M10 16.5V7.5L16 12L10 16.5M5 3H19C20.1 3 21 3.9 21 5V19C21 20.1 20.1 21 19 21H5C3.9 21 3 20.1 3 19V5C3 3.9 3.9 3 5 3Z" />
                        </svg>
                        Watch demo
                    </a>
                </div>
            </article>
            <article class="award-card">
                <span class="award-rank">2nd place</span>
                <h3>Triple_As</h3>
                <p class="award-team">Abbas Adamu Abdullahi, Aminu Rabiu Doguwa, Abubakar Shuaibu Dahiru, Ahmad Dalhatu Abbas, Mauliady Satria, Sara Uribe Garcia &mdash; KFUPM, Dhahran</p>
                <p class="award-description">Triple_As delivers a learning platform that gives students clarity and confidence while offering institutions a scalable solution. It includes progress analytics to track improvement, an AI study-material generator for personalized flashcards and guides, and an award-winning interface that saves learners time.</p>
                <div class="award-footer">
                    <a class="award-button" href="https://youtu.be/s1nscrTJIa8" target="_blank" rel="noopener">
                        <svg viewBox="0 0 24 24" fill="currentColor" aria-hidden="true">
                            <path d="M10 16.5V7.5L16 12L10 16.5M5 3H19C20.1 3 21 3.9 21 5V19C21 20.1 20.1 21 19 21H5C3.9 21 3 20.1 3 19V5C3 3.9 3.9 3 5 3Z" />
                        </svg>
                        Watch demo
                    </a>
                </div>
            </article>
            <article class="award-card">
                <span class="award-rank">3rd place</span>
                <h3>MixSense</h3>
                <p class="award-team">Jesus Diaz Sanchez, Katharina Jaeger, Kevin Greenman, Lucia Vina Lopez, Magdalena Lederbauer, Mrigi Munjal, Sathya Edamadaka, Tatem Rios</p>
                <p class="award-description">MixSense built an autonomous LLM agent for analytical chemistry that performs quantitative structure elucidation from 1H NMR, rapidly identifying compounds in mixtures and predicting flavor profiles. The workflow spans product prediction, spectrum simulation, deconvolution, quantification, and flavor reporting directly from raw data.</p>
                <div class="award-footer">
                    <a class="award-button" href="https://www.linkedin.com/posts/jesus-diaz-sanchez-b7603a188_excited-to-share-our-project-from-the-llm-activity-7372418093496774656-B3FF?utm_source=share&amp;utm_medium=member_desktop&amp;rcm=ACoAACwkvQoB4NVBr6w6GYdn4jEEjFx5pYoR20o" target="_blank" rel="noopener">
                        <svg viewBox="0 0 24 24" fill="currentColor" aria-hidden="true">
                            <path d="M10 16.5V7.5L16 12L10 16.5M5 3H19C20.1 3 21 3.9 21 5V19C21 20.1 20.1 21 19 21H5C3.9 21 3 20.1 3 19V5C3 3.9 3.9 3 5 3Z" />
                        </svg>
                        Watch demo
                    </a>
                </div>
            </article>
            <article class="award-card">
                <span class="award-rank">4th place</span>
                <h3>CrystaLenz</h3>
                <p class="award-team">Mohammad Javad Raei</p>
                <p class="award-description">CrystaLenz is an end-to-end XRD analysis pipeline that handles heterogeneous file formats and noisy signals. It provides robust peak detection, Voigt profile fitting, and size and strain extraction with Scherrer and Williamson-Hall methods, streamlining crystallography workflows.</p>
                <div class="award-footer">
                    <a class="award-button" href="https://youtu.be/uNsnd1BLsTs" target="_blank" rel="noopener">
                        <svg viewBox="0 0 24 24" fill="currentColor" aria-hidden="true">
                            <path d="M10 16.5V7.5L16 12L10 16.5M5 3H19C20.1 3 21 3.9 21 5V19C21 20.1 20.1 21 19 21H5C3.9 21 3 20.1 3 19V5C3 3.9 3.9 3 5 3Z" />
                        </svg>
                        Watch demo
                    </a>
                </div>
            </article>
            <article class="award-card">
                <span class="award-rank">5th place</span>
                <h3>ACME (Autonomous Critical Materials Extraction)</h3>
                <p class="award-team">Hassan Harb, Hossam Farag, Rakesh Kamath, Adwaith Ravichandran, Tugba Isik, Cailin Buchanan, Suman Kumari, Sungil Hong, Yunkai Sun, Mustafa Unal, Shi Li &mdash; Argonne National Laboratory</p>
                <p class="award-description">ACME built an autonomous closed-loop discovery platform that integrates AI-driven reasoning with experimental automation. User prompts are refined into candidate molecules, filtered through conformer searches and quantum calculations, and routed to automated lab execution, with results cycling back for continuous improvement.</p>
                <div class="award-footer">
                    <a class="award-button" href="https://www.youtube.com/watch?v=bMx332SAWv4" target="_blank" rel="noopener">
                        <svg viewBox="0 0 24 24" fill="currentColor" aria-hidden="true">
                            <path d="M10 16.5V7.5L16 12L10 16.5M5 3H19C20.1 3 21 3.9 21 5V19C21 20.1 20.1 21 19 21H5C3.9 21 3 20.1 3 19V5C3 3.9 3.9 3 5 3Z" />
                        </svg>
                        Watch demo
                    </a>
                </div>
            </article>
        </div>
    </section>

    <section class="awards-section" aria-label="Abstrax Prizes">
        <h2>Abstrax Prizes</h2>
        <div class="award-grid">
            <article class="award-card">
                <h3>SmeLLMap</h3>
                <p class="award-team">Justice Lu &mdash; Duke University</p>
                <p class="award-description">SmeLLMap integrates ESM2 language models with structure prediction to study receptor-odor relationships. By combining sequence-derived features and AlphaFold cavities, the team trained CNNs that deliver near-perfect odor recognition performance across ten categories (AUC above 0.95).</p>
                <div class="award-footer">
                    <a class="award-button" href="https://www.linkedin.com/posts/justice-lu-1842a395_turning-smell-from-a-mystery-into-a-map-activity-7372304796038471680-fpC4?utm_source=share&amp;utm_medium=member_desktop&amp;rcm=ACoAABQnZzQBxyKA1uEUp0LCBt9_rfQ-WVQiOc8" target="_blank" rel="noopener">
                        <svg viewBox="0 0 24 24" fill="currentColor" aria-hidden="true">
                            <path d="M10 16.5V7.5L16 12L10 16.5M5 3H19C20.1 3 21 3.9 21 5V19C21 20.1 20.1 21 19 21H5C3.9 21 3 20.1 3 19V5C3 3.9 3.9 3 5 3Z" />
                        </svg>
                        Watch demo
                    </a>
                </div>
            </article>
            <article class="award-card">
                <h3>ATOMS Lab</h3>
                <p class="award-team">Alexander Haibel, Fariha Agbere, Shashane Anderson, Kevin Ishimwe, Colin Jones, Oscar Matemb, Izzy Shahmoradi, Samiha Sharlin, Ejike Ugwuanyi, Muhammed Usman, Tyler Josephson</p>
                <p class="award-description">ATOMS Lab built a framework for analogical prompting with LLMs to predict properties, prompting models to reason through exemplars before answering. The team curated materials and scent datasets to explore analogical reasoning for both structural properties and fragrance scores.</p>
                <div class="award-footer">
                    <a class="award-button" href="https://youtu.be/Fboa8sOo3w0" target="_blank" rel="noopener">
                        <svg viewBox="0 0 24 24" fill="currentColor" aria-hidden="true">
                            <path d="M10 16.5V7.5L16 12L10 16.5M5 3H19C20.1 3 21 3.9 21 5V19C21 20.1 20.1 21 19 21H5C3.9 21 3 20.1 3 19V5C3 3.9 3.9 3 5 3Z" />
                        </svg>
                        Watch demo
                    </a>
                </div>
            </article>
            <article class="award-card">
                <h3>ChromatographyMiner</h3>
                <p class="award-team">Md Habibur Rahman &mdash; Purdue University</p>
                <p class="award-description">ChromatographyMiner unifies GCxGC-MS analysis within a single Streamlit application, spanning raw data ingestion, peak detection, spectral matching, and LLM-powered explanations. The toolkit integrates MoNA libraries, deduplication, and visualization to support analytical chemistry workflows.</p>
                <div class="award-footer">
                    <a class="award-button" href="https://www.youtube.com/watch?v=EUzJ4XTkCG4" target="_blank" rel="noopener">
                        <svg viewBox="0 0 24 24" fill="currentColor" aria-hidden="true">
                            <path d="M10 16.5V7.5L16 12L10 16.5M5 3H19C20.1 3 21 3.9 21 5V19C21 20.1 20.1 21 19 21H5C3.9 21 3 20.1 3 19V5C3 3.9 3.9 3 5 3Z" />
                        </svg>
                        Watch demo
                    </a>
                </div>
            </article>
        </div>
    </section>

    <section class="awards-section" aria-label="2025 Visionary Awards">
        <h2>2025 Visionary Awards</h2>
        <p class="section-copy">These teams were recognized by the judges for exceptional scores, novelty, or innovative approaches. They will be invited to a special session of the hackathon showcase, and all participating teams will still be welcomed.</p>
        <div class="visionary-card">
            <ul>
                <li>ARIA</li>
                <li>AssemblAI</li>
                <li>AtomBridge</li>
                <li>AtomicShorts</li>
                <li>Best Team</li>
                <li>CafChem</li>
                <li>Catalyze</li>
                <li>Clueless-scientist</li>
                <li>DFTPilot</li>
                <li>ExpAlign</li>
                <li>H2-Guardians</li>
                <li>JH_sqr</li>
                <li>L.A.R.A</li>
                <li>LARA-HPC: A LAnguage model-powered Research Assistant for HPC</li>
                <li>LIAC's AdsKRK and DynaAgent</li>
                <li>LLM4ConProp</li>
                <li>Material AI Agent Team</li>
                <li>MatSci LapLab</li>
                <li>MCP4SDL</li>
                <li>MIDAS</li>
                <li>MINT LLM</li>
                <li>MJS</li>
                <li>MuMMIE</li>
                <li>Parse Patrol</li>
                <li>PolyNexus</li>
                <li>PolyPredictor</li>
                <li>Ragalicious</li>
                <li>RedoxFlow</li>
                <li>SciForge</li>
                <li>Team Datalab - Guillemot</li>
                <li>Team_Tc</li>
            </ul>
        </div>
    </section>
</div>
