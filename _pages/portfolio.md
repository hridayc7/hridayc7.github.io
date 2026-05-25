---
layout: archive
title: "Portfolio"
permalink: /portfolio/
author_profile: true
---

<style>
  /* Base Portfolio Styling */
  .portfolio-wrapper {
    font-family: -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, Helvetica, Arial, sans-serif;
    color: var(--pf-text-main);
    line-height: 1.6;
    margin-top: 1rem;
  }
  
  .portfolio-intro {
    font-size: 1.1rem;
    color: var(--pf-text-muted);
    margin-bottom: 2rem;
    max-width: 800px;
  }

  /* Color Palette Variables */
  :root {
    --pf-bg-card: #ffffff;
    --pf-border: #e2e8f0;
    --pf-text-main: #1e293b;
    --pf-text-muted: #64748b;
    --pf-primary: #3b82f6;
    --pf-primary-light: #eff6ff;
    --pf-research: #ecfdf5;
    --pf-research-text: #059669;
    --pf-personal: #faf5ff;
    --pf-personal-text: #7c3aed;
    --pf-tag-bg: #f1f5f9;
    --pf-tag-text: #475569;
    --pf-shadow: 0 4px 6px -1px rgba(0, 0, 0, 0.05), 0 2px 4px -1px rgba(0, 0, 0, 0.03);
    --pf-shadow-hover: 0 10px 15px -3px rgba(0, 0, 0, 0.1), 0 4px 6px -2px rgba(0, 0, 0, 0.05);
  }

  @media (prefers-color-scheme: dark) {
    :root {
      --pf-bg-card: #1e293b;
      --pf-border: #334155;
      --pf-text-main: #f8fafc;
      --pf-text-muted: #94a3b8;
      --pf-primary-light: rgba(59, 130, 246, 0.15);
      --pf-research: rgba(5, 150, 105, 0.15);
      --pf-research-text: #34d399;
      --pf-personal: rgba(124, 58, 237, 0.15);
      --pf-personal-text: #c084fc;
      --pf-tag-bg: #334155;
      --pf-tag-text: #cbd5e1;
      --pf-shadow: 0 4px 6px -1px rgba(0, 0, 0, 0.2), 0 2px 4px -1px rgba(0, 0, 0, 0.1);
      --pf-shadow-hover: 0 12px 20px -3px rgba(0, 0, 0, 0.3), 0 4px 8px -2px rgba(0, 0, 0, 0.2);
    }
  }

  /* Interactive Dashboard Index Grid */
  .dashboard-section {
    margin-bottom: 3.5rem;
  }
  
  .dashboard-header {
    font-size: 0.85rem;
    font-weight: 700;
    text-transform: uppercase;
    letter-spacing: 0.05em;
    color: var(--pf-text-muted);
    margin-bottom: 1.25rem;
    border-bottom: 2px solid var(--pf-border);
    padding-bottom: 0.5rem;
  }

  .project-grid {
    display: grid;
    grid-template-columns: repeat(auto-fill, minmax(280px, 1fr));
    gap: 1.25rem;
  }

  .index-card {
    background: var(--pf-bg-card);
    border: 1px solid var(--pf-border);
    border-radius: 12px;
    padding: 1.25rem;
    box-shadow: var(--pf-shadow);
    transition: all 0.3s cubic-bezier(0.4, 0, 0.2, 1);
    display: flex;
    flex-direction: column;
    justify-content: space-between;
    height: 100%;
    cursor: pointer;
    text-decoration: none !important;
  }

  .index-card:hover {
    transform: translateY(-4px);
    box-shadow: var(--pf-shadow-hover);
    border-color: var(--pf-primary);
  }

  .card-top {
    margin-bottom: 1rem;
  }

  .card-meta {
    display: flex;
    justify-content: space-between;
    align-items: center;
    margin-bottom: 0.75rem;
  }

  .badge {
    font-size: 0.7rem;
    font-weight: 700;
    text-transform: uppercase;
    padding: 0.2rem 0.5rem;
    border-radius: 20px;
    letter-spacing: 0.02em;
  }

  .badge-research {
    background: var(--pf-research);
    color: var(--pf-research-text);
  }

  .badge-personal {
    background: var(--pf-personal);
    color: var(--pf-personal-text);
  }

  .card-date {
    font-size: 0.75rem;
    font-weight: 600;
    color: var(--pf-text-muted);
  }

  .card-title {
    font-size: 1.15rem;
    font-weight: 700;
    color: var(--pf-text-main);
    margin: 0 0 0.5rem 0;
    line-height: 1.3;
  }

  .card-subtitle {
    font-size: 0.85rem;
    color: var(--pf-text-muted);
    margin: 0;
    display: -webkit-box;
    -webkit-line-clamp: 2;
    -webkit-box-orient: vertical;
    overflow: hidden;
    line-height: 1.4;
  }

  .card-tech-list {
    display: flex;
    flex-wrap: wrap;
    gap: 0.35rem;
    margin-top: 1rem;
  }

  .mini-tag {
    font-size: 0.65rem;
    font-weight: 600;
    background: var(--pf-tag-bg);
    color: var(--pf-tag-text);
    padding: 0.15rem 0.4rem;
    border-radius: 4px;
  }

  /* Deep Dive Showcases */
  .section-divider {
    height: 1px;
    background: var(--pf-border);
    margin: 4rem 0;
  }

  .section-title {
    font-size: 1.6rem;
    font-weight: 800;
    margin-bottom: 2rem;
    border-left: 4px solid var(--pf-primary);
    padding-left: 0.75rem;
    color: var(--pf-text-main);
  }

  .project-showcase-list {
    display: flex;
    flex-direction: column;
    gap: 3.5rem;
  }

  .project-card {
    background: var(--pf-bg-card);
    border: 1px solid var(--pf-border);
    border-radius: 16px;
    box-shadow: var(--pf-shadow);
    overflow: hidden;
    display: flex;
    flex-direction: column;
    transition: all 0.3s ease;
    scroll-margin-top: 80px; /* Offset for sticky navigation bar */
  }

  .project-card:hover {
    box-shadow: var(--pf-shadow-hover);
  }

  .project-card {
    background: var(--pf-bg-card);
    border: 1px solid var(--pf-border);
    border-radius: 16px;
    box-shadow: var(--pf-shadow);
    overflow: hidden;
    display: flex;
    flex-direction: column; /* Vertical stacked layout for all screens */
    transition: all 0.3s ease;
    scroll-margin-top: 80px; /* Offset for sticky navigation bar */
  }

  .project-media-col {
    width: 100%;
    background: var(--pf-tag-bg); /* Soft gray background instead of harsh black */
    display: flex;
    align-items: center;
    justify-content: center;
    position: relative;
    padding: 2.25rem 2.25rem 1.75rem 2.25rem;
    border-bottom: 1px solid var(--pf-border);
    transition: background 0.3s ease;
  }

  .project-info-col {
    width: 100%;
    padding: 2.25rem;
    display: flex;
    flex-direction: column;
  }

  /* Responsive Media Styling */
  .media-wrapper {
    max-width: 720px; /* Perfect visual balance on desktop, scales naturally on mobile */
    width: 100%;
    position: relative;
    overflow: hidden;
    display: flex;
    align-items: center;
    justify-content: center;
    margin: 0 auto;
  }

  .media-gif {
    width: 100%;
    height: auto;
    max-height: 400px;
    object-fit: contain;
    display: block;
    border-radius: 8px;
    box-shadow: 0 10px 25px -5px rgba(0, 0, 0, 0.15), 0 8px 10px -6px rgba(0, 0, 0, 0.15);
    border: 1px solid var(--pf-border);
  }

  .video-container {
    position: relative;
    width: 100%;
    padding-bottom: 56.25%; /* 16:9 Aspect Ratio */
    height: 0;
    overflow: hidden;
    border-radius: 8px;
    box-shadow: 0 10px 25px -5px rgba(0, 0, 0, 0.15), 0 8px 10px -6px rgba(0, 0, 0, 0.15);
    border: 1px solid var(--pf-border);
    background: #000;
  }

  .video-container iframe {
    position: absolute;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    border: 0;
  }

  /* Showcase Header and Info */
  .showcase-header {
    margin-bottom: 1.25rem;
  }

  .showcase-title-row {
    display: flex;
    justify-content: space-between;
    align-items: flex-start;
    flex-wrap: wrap;
    gap: 0.5rem;
    margin-bottom: 0.5rem;
  }

  .showcase-title {
    font-size: 1.35rem;
    font-weight: 800;
    color: var(--pf-text-main);
    margin: 0;
  }

  .showcase-achievement-badge {
    font-size: 0.75rem;
    font-weight: 700;
    background: #fef3c7;
    color: #d97706;
    border: 1px solid #fcd34d;
    padding: 0.25rem 0.6rem;
    border-radius: 6px;
    display: inline-flex;
    align-items: center;
    gap: 0.25rem;
  }

  @media (prefers-color-scheme: dark) {
    .showcase-achievement-badge {
      background: rgba(217, 119, 6, 0.15);
      color: #fbbf24;
      border-color: rgba(251, 191, 36, 0.3);
    }
  }

  .showcase-timeframe {
    font-size: 0.85rem;
    font-weight: 600;
    color: var(--pf-text-muted);
  }

  .showcase-desc {
    font-size: 0.95rem;
    color: var(--pf-text-main);
    margin-bottom: 1.5rem;
    line-height: 1.5;
  }

  .showcase-features-title {
    font-size: 0.8rem;
    font-weight: 700;
    text-transform: uppercase;
    letter-spacing: 0.05em;
    color: var(--pf-text-muted);
    margin-bottom: 0.5rem;
  }

  .showcase-features-list {
    margin: 0 0 1.5rem 0;
    padding-left: 1.25rem;
  }

  .showcase-features-list li {
    font-size: 0.9rem;
    color: var(--pf-text-main);
    margin-bottom: 0.5rem;
    line-height: 1.45;
  }

  /* Showcase Tech Footer */
  .showcase-footer {
    border-top: 1px solid var(--pf-border);
    padding-top: 1.25rem;
    margin-top: auto;
  }

  .showcase-tech-title {
    font-size: 0.8rem;
    font-weight: 700;
    text-transform: uppercase;
    letter-spacing: 0.05em;
    color: var(--pf-text-muted);
    margin-bottom: 0.5rem;
  }

  .showcase-tech-tags {
    display: flex;
    flex-wrap: wrap;
    gap: 0.4rem;
  }

  .tech-pill {
    font-size: 0.72rem;
    font-weight: 600;
    background: var(--pf-tag-bg);
    color: var(--pf-tag-text);
    padding: 0.25rem 0.6rem;
    border-radius: 6px;
    border: 1px solid var(--pf-border);
    transition: all 0.2s ease;
  }

  .tech-pill:hover {
    border-color: var(--pf-primary);
    color: var(--pf-primary);
    background: var(--pf-primary-light);
  }
</style>

<div class="portfolio-wrapper">
  <p class="portfolio-intro">
    I am deeply passionate about creating human-centered, consumer-facing AI experiences. Below is a curated selection of the research and personal engineering projects I have designed and built.
  </p>

  <!-- INTERACTIVE DASHBOARD INDEX -->
  <section class="dashboard-section">
    <div class="dashboard-header">
      <span>Project Directory &amp; Tech Matrix</span>
    </div>
    
    <div class="project-grid">
      <!-- Simulus -->
      <a href="#project-simulus" class="index-card">
        <div class="card-top">
          <div class="card-meta">
            <span class="badge badge-research">Research</span>
            <span class="card-date">Summer 2024</span>
          </div>
          <h4 class="card-title">Simulus</h4>
          <p class="card-subtitle">XR + LLM based stress-relief simulation virtual environments.</p>
        </div>
        <div class="card-tech-list">
          <span class="mini-tag">Unity</span>
          <span class="mini-tag">Meta Quest 3</span>
          <span class="mini-tag">GPT-4o</span>
        </div>
      </a>

      <!-- SoundWatch -->
      <a href="#project-soundwatch" class="index-card">
        <div class="card-top">
          <div class="card-meta">
            <span class="badge badge-research">Research</span>
            <span class="card-date">Fall 2024</span>
          </div>
          <h4 class="card-title">SoundWatch</h4>
          <p class="card-subtitle">Deep learning sound awareness for iOS and Apple Watch.</p>
        </div>
        <div class="card-tech-list">
          <span class="mini-tag">Swift</span>
          <span class="mini-tag">CoreML</span>
          <span class="mini-tag">FastAPI</span>
        </div>
      </a>

      <!-- EverArc -->
      <a href="#project-everarc" class="index-card">
        <div class="card-top">
          <div class="card-meta">
            <span class="badge badge-personal">Personal</span>
            <span class="card-date">Winter 2025</span>
          </div>
          <h4 class="card-title">EverArc</h4>
          <p class="card-subtitle">A high-craft, minimalist habit tracker app built for iOS.</p>
        </div>
        <div class="card-tech-list">
          <span class="mini-tag">SwiftUI</span>
          <span class="mini-tag">SwiftData</span>
          <span class="mini-tag">SwiftCharts</span>
        </div>
      </a>

      <!-- Words of Wisdom -->
      <a href="#project-words-of-wisdom" class="index-card">
        <div class="card-top">
          <div class="card-meta">
            <span class="badge badge-personal">Personal</span>
            <span class="card-date">Winter 2025</span>
          </div>
          <h4 class="card-title">Words of Wisdom</h4>
          <p class="card-subtitle">Augmented Reality experience for therapeutic cognitive defusion.</p>
        </div>
        <div class="card-tech-list">
          <span class="mini-tag">ARKit</span>
          <span class="mini-tag">CoreML</span>
          <span class="mini-tag">SoundAnalysis</span>
        </div>
      </a>

      <!-- OpenTitan RAG -->
      <a href="#project-opentitan-rag" class="index-card">
        <div class="card-top">
          <div class="card-meta">
            <span class="badge badge-personal">Personal</span>
            <span class="card-date">Spring 2025</span>
          </div>
          <h4 class="card-title">OpenTitan RAG</h4>
          <p class="card-subtitle">Semantic search &amp; conversational assistant for OpenTitan specs.</p>
        </div>
        <div class="card-tech-list">
          <span class="mini-tag">Claude 3</span>
          <span class="mini-tag">FAISS</span>
          <span class="mini-tag">Flask + React</span>
        </div>
      </a>
    </div>
  </section>

  <div class="section-divider"></div>

  <!-- DEEP DIVE SHOWCASES -->
  
  <h2 class="section-title" id="research-showcase">🧪 Research Projects</h2>
  
  <div class="project-showcase-list">
    <!-- Simulus Card -->
    <div id="project-simulus" class="project-card">
      <div class="project-media-col">
        <div class="media-wrapper">
          <img src="{{ '/files/demos/Simulus_Demo.gif' | relative_url }}" class="media-gif" alt="Simulus Demo">
        </div>
      </div>
      <div class="project-info-col">
        <div class="showcase-header">
          <div class="showcase-title-row">
            <h3 class="showcase-title">Simulus</h3>
            <span class="showcase-achievement-badge">🏆 CHI 2025 Honorable Mention</span>
          </div>
          <div class="showcase-timeframe">Summer 2024 <i>(May – Aug)</i></div>
        </div>
        
        <p class="showcase-desc">
          Developed in collaboration with Professor Haiyi Zhu, Anna Fang, and Alekhya Maram at Carnegie Mellon University. Simulus is an AR/VR stress-relief simulation platform on the Meta Quest 3, enabling users to practice stress management and navigate everyday high-pressure situations by interacting with smart, AI-driven virtual avatars.
        </p>

        <div class="showcase-features-title">Key Contributions</div>
        <ul class="showcase-features-list">
          <li><strong>LLM-Based Virtual Avatars</strong>: Built expressive GPT-4o-driven avatar profiles inside Unity, configuring detailed personas, conversational styles, and specialized psychological guidance templates.</li>
          <li><strong>Structured Output Dialogue State</strong>: Engineered structured JSON prompting rules to enforce consistent outputs from GPT-4o, facilitating elegant chat parsing and real-time state tracking.</li>
          <li><strong>Speech-to-Text Conversational Core</strong>: Integrated OpenAI's Whisper API in C# to achieve seamless, low-latency vocal interactions, letting users communicate naturally using their real voice.</li>
        </ul>

        <div class="showcase-footer">
          <div class="showcase-tech-title">Tech Stack</div>
          <div class="showcase-tech-tags">
            <span class="tech-pill">Unity (C#)</span>
            <span class="tech-pill">Meta Quest 3</span>
            <span class="tech-pill">Meta XR SDK</span>
            <span class="tech-pill">OpenAI GPT-4o</span>
            <span class="tech-pill">OpenAI Whisper</span>
          </div>
        </div>
      </div>
    </div>

    <!-- SoundWatch Card -->
    <div id="project-soundwatch" class="project-card">
      <div class="project-media-col">
        <div class="media-wrapper">
          <div class="video-container">
            <iframe src="https://www.youtube.com/embed/aanpbJIDB4g?si=8h4zeGKxkCLtDl5v" allowfullscreen></iframe>
          </div>
        </div>
      </div>
      <div class="project-info-col">
        <div class="showcase-header">
          <div class="showcase-title-row">
            <h3 class="showcase-title">SoundWatch</h3>
          </div>
          <div class="showcase-timeframe">Fall 2024 <i>(Aug – Dec)</i></div>
        </div>
        
        <p class="showcase-desc">
          An end-to-end deep learning sound awareness platform designed for Deaf and Hard of Hearing (DHH) individuals. The system continuously listens to environmental sounds and alerts users to critical events—such as fire alarms, sirens, microwave beeps, and doorbells—through localized watch haptics and visual notifications.
        </p>

        <div class="showcase-features-title">Key Contributions</div>
        <ul class="showcase-features-list">
          <li><strong>On-Device Sound Classification</strong>: Deployed custom audio classification neural networks locally on iOS using CoreML and Apple's SoundAnalysis framework, achieving high-accuracy detection without sacrificing user privacy.</li>
          <li><strong>watchOS Synchronization</strong>: Developed a lightweight, highly responsive watchOS companion app using Swift and WCSession to trigger custom haptic patterns matching specific hazard levels.</li>
          <li><strong>Analytics Backend &amp; Dashboard</strong>: Programmed a telemetry system with FastAPI, PostgreSQL, and React to help researchers study long-term auditory assistant usage trends securely.</li>
        </ul>

        <div class="showcase-footer">
          <div class="showcase-tech-title">Tech Stack</div>
          <div class="showcase-tech-tags">
            <span class="tech-pill">Swift</span>
            <span class="tech-pill">SwiftUI</span>
            <span class="tech-pill">CoreML</span>
            <span class="tech-pill">watchOS</span>
            <span class="tech-pill">FastAPI</span>
            <span class="tech-pill">React</span>
            <span class="tech-pill">PostgreSQL</span>
          </div>
        </div>
      </div>
    </div>
  </div>

  <div class="section-divider"></div>

  <h2 class="section-title" id="personal-showcase">🚀 Personal Projects</h2>

  <div class="project-showcase-list">
    <!-- EverArc Card -->
    <div id="project-everarc" class="project-card">
      <div class="project-media-col">
        <div class="media-wrapper">
          <div class="video-container">
            <iframe src="https://www.youtube.com/embed/6vDa7zFkcOc" allowfullscreen></iframe>
          </div>
        </div>
      </div>
      <div class="project-info-col">
        <div class="showcase-header">
          <div class="showcase-title-row">
            <h3 class="showcase-title">EverArc</h3>
          </div>
          <div class="showcase-timeframe">Winter 2025 <i>(Feb)</i></div>
        </div>
        
        <p class="showcase-desc">
          EverArc is a minimalist, highly crafted habit tracking app built for iOS. Born out of a personal frustration with bloated logging tools, EverArc focuses on minimizing friction and delivering stunning, visual rewards that help users stick to their routines.
        </p>

        <div class="showcase-features-title">Key Features</div>
        <ul class="showcase-features-list">
          <li><strong>One-Tap Seamless Logging</strong>: Combines highly responsive, physical-feeling haptic interactions with interactive completion rings to make habit tracking rewarding.</li>
          <li><strong>Native Local Data Architecture</strong>: Implemented SwiftData to orchestrate schema modeling and lightweight database operations on-device, offering instant offline loading.</li>
          <li><strong>Streak &amp; Visual Analytics</strong>: Created visual calendars and charts with SwiftCharts to track consistency, along with celebratory completion particle effects.</li>
        </ul>

        <div class="showcase-footer">
          <div class="showcase-tech-title">Tech Stack</div>
          <div class="showcase-tech-tags">
            <span class="tech-pill">SwiftUI</span>
            <span class="tech-pill">SwiftData</span>
            <span class="tech-pill">SwiftCharts</span>
            <span class="tech-pill">Haptic Engine</span>
          </div>
        </div>
      </div>
    </div>

    <!-- Words of Wisdom Card -->
    <div id="project-words-of-wisdom" class="project-card">
      <div class="project-media-col">
        <div class="media-wrapper">
          <div class="video-container">
            <iframe src="https://www.youtube.com/embed/Lc0h_Mie0o0" allowfullscreen></iframe>
          </div>
        </div>
      </div>
      <div class="project-info-col">
        <div class="showcase-header">
          <div class="showcase-title-row">
            <h3 class="showcase-title">Words of Wisdom</h3>
          </div>
          <div class="showcase-timeframe">Winter 2025 <i>(Feb)</i></div>
        </div>
        
        <p class="showcase-desc">
          An augmented reality mobile experience designed to help users manage anxious thoughts. Inspired by *Cognitive Defusion* (a core technique in Acceptance and Commitment Therapy), the app enables users to externalize negative thoughts by projecting them into physical space and peacefully letting them go.
        </p>

        <div class="showcase-features-title">Key Features</div>
        <ul class="showcase-features-list">
          <li><strong>AR Spatial Defusion</strong>: Places user-submitted negative thoughts onto floating, customizable 3D text clouds mapped in the room using ARKit.</li>
          <li><strong>Breath-Powered Cloud Dispersal</strong>: Implemented live audio classification models via CoreML to detect long exhaling sounds into the phone mic, allowing the user's physical breath to push the AR clouds away.</li>
          <li><strong>Mindfulness Logging</strong>: Uses SwiftData to track categories of thoughts and encourage positive reframing patterns over time.</li>
        </ul>

        <div class="showcase-footer">
          <div class="showcase-tech-title">Tech Stack</div>
          <div class="showcase-tech-tags">
            <span class="tech-pill">SwiftUI</span>
            <span class="tech-pill">ARKit</span>
            <span class="tech-pill">CoreML</span>
            <span class="tech-pill">SoundAnalysis</span>
            <span class="tech-pill">SwiftData</span>
          </div>
        </div>
      </div>
    </div>

    <!-- OpenTitan RAG Card -->
    <div id="project-opentitan-rag" class="project-card">
      <div class="project-media-col">
        <div class="media-wrapper">
          <div class="video-container">
            <iframe src="https://www.youtube.com/embed/MeZdiM05C2s" allowfullscreen></iframe>
          </div>
        </div>
      </div>
      <div class="project-info-col">
        <div class="showcase-header">
          <div class="showcase-title-row">
            <h3 class="showcase-title">OpenTitan RAG</h3>
          </div>
          <div class="showcase-timeframe">Spring 2025 <i>(Apr)</i></div>
        </div>
        
        <p class="showcase-desc">
          An AI-powered technical document assistant engineered specifically to parse, index, and query the open-source OpenTitan secure silicon platform documentation. It enables silicon designers and software developers to retrieve precise technical specifications through natural language questions.
        </p>

        <div class="showcase-features-title">Key Features</div>
        <ul class="showcase-features-list">
          <li><strong>High-Fidelity Document Retrieval</strong>: Implemented dense document vector databases using FAISS and Hugging Face's sentence transformers, optimizing passage-level semantic search accuracy.</li>
          <li><strong>Context-Aware Synthesis</strong>: Built multi-turn conversational agents with Claude 3 Opus and LangChain, enabling detailed hardware reasoning and direct links to official documentation sources.</li>
          <li><strong>Full-Stack Chat App</strong>: Wrapped the retrieval pipeline in a lightweight Flask API, serving a gorgeous, responsive, syntax-highlighted React chat dashboard.</li>
        </ul>

        <div class="showcase-footer">
          <div class="showcase-tech-title">Tech Stack</div>
          <div class="showcase-tech-tags">
            <span class="tech-pill">Claude 3 Opus</span>
            <span class="tech-pill">FAISS</span>
            <span class="tech-pill">LangChain</span>
            <span class="tech-pill">Sentence Transformers</span>
            <span class="tech-pill">Flask</span>
            <span class="tech-pill">React</span>
            <span class="tech-pill">PyTorch</span>
          </div>
        </div>
      </div>
    </div>
  </div>
</div>
