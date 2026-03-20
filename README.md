<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8" />
<meta name="viewport" content="width=device-width, initial-scale=1.0"/>
<title>Shiva Prasad Chenchala — Portfolio</title>
<link href="https://fonts.googleapis.com/css2?family=Space+Mono:ital,wght@0,400;0,700;1,400&family=Syne:wght@400;600;700;800&family=DM+Sans:wght@300;400;500;600&display=swap" rel="stylesheet"/>
<style>
  :root {
    --bg: #f5f2ee;
    --bg2: #ede9e3;
    --bg3: #e4dfd7;
    --surface: #ffffff;
    --surface2: #f9f7f4;
    --border: #d6cfc5;
    --text: #1a1714;
    --text2: #4a4540;
    --text3: #7a7068;
    --accent: #c0392b;
    --accent2: #e74c3c;
    --teal: #16a085;
    --teal2: #1abc9c;
    --gold: #d4a017;
    --gold2: #f1c40f;
    --tag-bg: #ede9e3;
    --tag-text: #4a4540;
    --card-shadow: 0 2px 20px rgba(0,0,0,0.08), 0 1px 4px rgba(0,0,0,0.04);
    --card-shadow-hover: 0 8px 40px rgba(0,0,0,0.14), 0 2px 8px rgba(0,0,0,0.08);
    --code-bg: #1a1714;
    --code-text: #f5f2ee;
  }
  [data-theme="dark"] {
    --bg: #0d0f14;
    --bg2: #131720;
    --bg3: #1a1f2e;
    --surface: #171c28;
    --surface2: #1e2435;
    --border: #2a3148;
    --text: #e8eaf0;
    --text2: #a8b0c8;
    --text3: #6a7290;
    --accent: #e74c3c;
    --accent2: #ff6b5b;
    --teal: #1abc9c;
    --teal2: #2ecc71;
    --gold: #f1c40f;
    --gold2: #f39c12;
    --tag-bg: #1e2435;
    --tag-text: #a8b0c8;
    --card-shadow: 0 2px 20px rgba(0,0,0,0.4), 0 1px 4px rgba(0,0,0,0.2);
    --card-shadow-hover: 0 8px 40px rgba(0,0,0,0.6), 0 2px 8px rgba(0,0,0,0.3);
    --code-bg: #0d0f14;
    --code-text: #e8eaf0;
  }

  *, *::before, *::after { box-sizing: border-box; margin: 0; padding: 0; }

  html { scroll-behavior: smooth; }

  body {
    font-family: 'DM Sans', sans-serif;
    background: var(--bg);
    color: var(--text);
    transition: background 0.4s, color 0.4s;
    min-height: 100vh;
    overflow-x: hidden;
  }

  /* ── THEME TOGGLE ── */
  .theme-toggle {
    position: fixed;
    top: 20px; right: 20px;
    z-index: 100;
    background: var(--surface);
    border: 1.5px solid var(--border);
    border-radius: 50px;
    padding: 8px 16px;
    cursor: pointer;
    display: flex; align-items: center; gap: 8px;
    font-family: 'Space Mono', monospace;
    font-size: 12px;
    color: var(--text2);
    box-shadow: var(--card-shadow);
    transition: all 0.3s;
  }
  .theme-toggle:hover { box-shadow: var(--card-shadow-hover); }
  .toggle-dot {
    width: 18px; height: 18px;
    border-radius: 50%;
    background: linear-gradient(135deg, var(--accent), var(--teal));
    transition: all 0.3s;
  }

  /* ── LAYOUT ── */
  .container { max-width: 900px; margin: 0 auto; padding: 60px 24px 80px; }

  /* ── HERO ── */
  .hero {
    padding: 60px 48px;
    background: var(--surface);
    border: 1.5px solid var(--border);
    border-radius: 4px;
    margin-bottom: 32px;
    position: relative;
    overflow: hidden;
    box-shadow: var(--card-shadow);
  }
  .hero::before {
    content: '';
    position: absolute;
    top: 0; left: 0; right: 0; height: 4px;
    background: linear-gradient(90deg, var(--accent), var(--gold), var(--teal));
  }
  .hero-grid { display: grid; grid-template-columns: 1fr auto; gap: 32px; align-items: start; }
  .hero-label {
    font-family: 'Space Mono', monospace;
    font-size: 11px;
    letter-spacing: 0.18em;
    text-transform: uppercase;
    color: var(--teal);
    margin-bottom: 12px;
    display: flex; align-items: center; gap: 8px;
  }
  .hero-label::before { content: '//'; color: var(--text3); }
  .hero-name {
    font-family: 'Syne', sans-serif;
    font-size: clamp(32px, 5vw, 52px);
    font-weight: 800;
    line-height: 1.05;
    letter-spacing: -0.03em;
    color: var(--text);
    margin-bottom: 8px;
  }
  .hero-name span { color: var(--accent); }
  .hero-role {
    font-family: 'Space Mono', monospace;
    font-size: 14px;
    color: var(--text3);
    margin-bottom: 24px;
  }
  .hero-role strong { color: var(--teal); font-weight: 400; }
  .hero-badges { display: flex; flex-wrap: wrap; gap: 8px; margin-bottom: 28px; }
  .badge {
    font-family: 'Space Mono', monospace;
    font-size: 11px;
    padding: 5px 12px;
    border-radius: 3px;
    border: 1.5px solid;
    transition: all 0.2s;
  }
  .badge-red { border-color: var(--accent); color: var(--accent); background: transparent; }
  .badge-teal { border-color: var(--teal); color: var(--teal); background: transparent; }
  .badge-gold { border-color: var(--gold); color: var(--gold); background: transparent; }
  .badge:hover { background: currentColor; }
  .badge:hover span { color: var(--bg); }
  .badge span { transition: color 0.2s; }
  .hero-links { display: flex; flex-wrap: wrap; gap: 10px; }
  .hero-link {
    display: inline-flex; align-items: center; gap: 6px;
    font-family: 'Space Mono', monospace;
    font-size: 11px;
    color: var(--text2);
    text-decoration: none;
    padding: 6px 12px;
    background: var(--bg2);
    border: 1px solid var(--border);
    border-radius: 3px;
    transition: all 0.2s;
  }
  .hero-link:hover { color: var(--text); border-color: var(--teal); background: var(--bg3); }
  .hero-right { text-align: right; }
  .status-pill {
    display: inline-flex; align-items: center; gap: 6px;
    background: var(--bg2);
    border: 1px solid var(--border);
    border-radius: 50px;
    padding: 8px 14px;
    font-family: 'Space Mono', monospace;
    font-size: 11px;
    color: var(--text2);
    white-space: nowrap;
  }
  .status-dot {
    width: 8px; height: 8px; border-radius: 50%;
    background: #2ecc71;
    box-shadow: 0 0 0 2px rgba(46,204,113,0.3);
    animation: pulse 2s infinite;
  }
  @keyframes pulse {
    0%, 100% { box-shadow: 0 0 0 2px rgba(46,204,113,0.3); }
    50% { box-shadow: 0 0 0 5px rgba(46,204,113,0.1); }
  }
  .trophy-block {
    margin-top: 16px;
    background: var(--bg2);
    border: 1px solid var(--gold);
    border-radius: 3px;
    padding: 12px 14px;
    text-align: left;
  }
  .trophy-label {
    font-family: 'Space Mono', monospace;
    font-size: 10px;
    color: var(--gold);
    letter-spacing: 0.1em;
    text-transform: uppercase;
    margin-bottom: 4px;
  }
  .trophy-text {
    font-size: 12px;
    color: var(--text2);
    line-height: 1.5;
  }

  /* ── SECTION HEADER ── */
  .section-header {
    display: flex; align-items: center; gap: 12px;
    margin-bottom: 20px;
  }
  .section-header h2 {
    font-family: 'Syne', sans-serif;
    font-size: 13px;
    font-weight: 700;
    letter-spacing: 0.15em;
    text-transform: uppercase;
    color: var(--text3);
  }
  .section-line {
    flex: 1; height: 1px;
    background: var(--border);
  }
  .section-num {
    font-family: 'Space Mono', monospace;
    font-size: 11px;
    color: var(--accent);
  }

  /* ── CODE BLOCK (About) ── */
  .about-code {
    background: var(--code-bg);
    border-radius: 4px;
    overflow: hidden;
    margin-bottom: 32px;
    box-shadow: var(--card-shadow);
    border: 1px solid var(--border);
  }
  .code-bar {
    background: #2a2520;
    padding: 10px 16px;
    display: flex; align-items: center; gap: 8px;
  }
  [data-theme="dark"] .code-bar { background: #1a1f2e; }
  .code-dot { width: 10px; height: 10px; border-radius: 50%; }
  .code-filename {
    font-family: 'Space Mono', monospace;
    font-size: 11px;
    color: #7a7068;
    margin-left: 4px;
  }
  [data-theme="dark"] .code-filename { color: #6a7290; }
  pre {
    padding: 24px;
    font-family: 'Space Mono', monospace;
    font-size: 13px;
    line-height: 1.7;
    color: var(--code-text);
    overflow-x: auto;
  }
  .c-key { color: #4dd0e1; }
  .c-str { color: #a5d6a7; }
  .c-arr { color: #ffcc80; }
  .c-brace { color: #ef9a9a; }
  .c-comment { color: #546e7a; font-style: italic; }

  /* ── TECH GRID ── */
  .tech-section { margin-bottom: 32px; }
  .tech-group { margin-bottom: 20px; }
  .tech-group-label {
    font-family: 'Space Mono', monospace;
    font-size: 10px;
    letter-spacing: 0.15em;
    text-transform: uppercase;
    color: var(--text3);
    margin-bottom: 10px;
    display: flex; align-items: center; gap: 8px;
  }
  .tech-group-label::after { content: ''; flex: 1; height: 1px; background: var(--border); }
  .tech-tags { display: flex; flex-wrap: wrap; gap: 8px; }
  .tech-tag {
    font-family: 'Space Mono', monospace;
    font-size: 11px;
    padding: 6px 12px;
    background: var(--tag-bg);
    color: var(--tag-text);
    border-radius: 3px;
    border: 1px solid var(--border);
    transition: all 0.2s;
    cursor: default;
  }
  .tech-tag:hover {
    background: var(--surface);
    border-color: var(--teal);
    color: var(--teal);
    transform: translateY(-1px);
    box-shadow: 0 4px 12px rgba(26,188,156,0.15);
  }

  /* ── PROJECTS ── */
  .projects-grid { display: grid; grid-template-columns: 1fr 1fr; gap: 16px; margin-bottom: 32px; }
  @media (max-width: 620px) { .projects-grid { grid-template-columns: 1fr; } }

  .project-card {
    background: var(--surface);
    border: 1.5px solid var(--border);
    border-radius: 4px;
    padding: 24px;
    transition: all 0.3s;
    box-shadow: var(--card-shadow);
    position: relative;
    overflow: hidden;
  }
  .project-card::after {
    content: '';
    position: absolute;
    bottom: 0; left: 0; right: 0; height: 2px;
    transform: scaleX(0);
    transition: transform 0.3s;
    transform-origin: left;
  }
  .project-card.p-red::after { background: var(--accent); }
  .project-card.p-teal::after { background: var(--teal); }
  .project-card.p-gold::after { background: var(--gold); }
  .project-card:hover { box-shadow: var(--card-shadow-hover); transform: translateY(-2px); border-color: var(--border); }
  .project-card:hover::after { transform: scaleX(1); }

  .project-icon { font-size: 28px; margin-bottom: 12px; }
  .project-title {
    font-family: 'Syne', sans-serif;
    font-size: 16px;
    font-weight: 700;
    color: var(--text);
    margin-bottom: 4px;
  }
  .project-winner {
    display: inline-flex; align-items: center; gap: 4px;
    font-family: 'Space Mono', monospace;
    font-size: 10px;
    color: var(--gold);
    border: 1px solid var(--gold);
    border-radius: 50px;
    padding: 2px 8px;
    margin-bottom: 10px;
    vertical-align: middle;
    margin-left: 8px;
  }
  .project-desc {
    font-size: 13px;
    color: var(--text2);
    line-height: 1.6;
    margin-bottom: 14px;
  }
  .project-highlights { margin-bottom: 14px; }
  .project-highlight {
    font-family: 'Space Mono', monospace;
    font-size: 11px;
    color: var(--text3);
    padding: 3px 0;
    display: flex; align-items: flex-start; gap: 8px;
  }
  .project-highlight::before { content: '→'; color: var(--teal); flex-shrink: 0; }
  .project-stack { display: flex; flex-wrap: wrap; gap: 6px; }
  .stack-tag {
    font-family: 'Space Mono', monospace;
    font-size: 10px;
    padding: 3px 8px;
    background: var(--bg2);
    border: 1px solid var(--border);
    border-radius: 2px;
    color: var(--text3);
  }

  /* ── NEXT/LEARNING ── */
  .next-card {
    background: var(--surface);
    border: 1.5px solid var(--border);
    border-radius: 4px;
    padding: 24px;
    box-shadow: var(--card-shadow);
  }
  .next-title {
    font-family: 'Syne', sans-serif;
    font-size: 16px;
    font-weight: 700;
    color: var(--text);
    margin-bottom: 16px;
    display: flex; align-items: center; gap: 8px;
  }
  .next-title::before { content: '⟳'; color: var(--teal); }
  .next-items { display: flex; flex-direction: column; gap: 10px; }
  .next-item {
    display: flex; align-items: center; gap: 12px;
    font-size: 13px;
    color: var(--text2);
  }
  .next-item-icon {
    width: 28px; height: 28px; border-radius: 4px;
    background: var(--bg2);
    border: 1px solid var(--border);
    display: flex; align-items: center; justify-content: center;
    font-size: 14px;
    flex-shrink: 0;
  }

  /* ── CONTACT ── */
  .contact-card {
    background: var(--surface);
    border: 1.5px solid var(--border);
    border-radius: 4px;
    padding: 32px 40px;
    text-align: center;
    box-shadow: var(--card-shadow);
    position: relative;
    overflow: hidden;
    margin-bottom: 32px;
  }
  .contact-card::before {
    content: '';
    position: absolute;
    top: 0; left: 0; right: 0; height: 3px;
    background: linear-gradient(90deg, var(--teal), var(--accent), var(--gold));
  }
  .contact-headline {
    font-family: 'Syne', sans-serif;
    font-size: 22px;
    font-weight: 800;
    color: var(--text);
    margin-bottom: 8px;
  }
  .contact-sub {
    font-size: 14px;
    color: var(--text2);
    margin-bottom: 24px;
    max-width: 420px;
    margin-left: auto; margin-right: auto;
    line-height: 1.6;
  }
  .contact-links { display: flex; justify-content: center; flex-wrap: wrap; gap: 10px; }
  .contact-link {
    display: inline-flex; align-items: center; gap: 8px;
    font-family: 'Space Mono', monospace;
    font-size: 12px;
    text-decoration: none;
    padding: 10px 20px;
    border-radius: 3px;
    border: 1.5px solid;
    transition: all 0.2s;
    font-weight: 700;
  }
  .cl-teal { color: var(--teal); border-color: var(--teal); }
  .cl-teal:hover { background: var(--teal); color: var(--bg); }
  .cl-red { color: var(--accent); border-color: var(--accent); }
  .cl-red:hover { background: var(--accent); color: #fff; }
  .cl-dark { color: var(--text2); border-color: var(--border); }
  .cl-dark:hover { background: var(--text); color: var(--bg); }

  /* ── FOOTER ── */
  .footer {
    text-align: center;
    font-family: 'Space Mono', monospace;
    font-size: 11px;
    color: var(--text3);
    padding-top: 24px;
    border-top: 1px solid var(--border);
  }

  /* ── DIVIDER ── */
  .divider { height: 1px; background: var(--border); margin: 32px 0; }

  @media (max-width: 640px) {
    .hero { padding: 32px 24px; }
    .hero-grid { grid-template-columns: 1fr; }
    .hero-right { text-align: left; }
    .contact-card { padding: 24px 20px; }
  }
</style>
</head>
<body>

<button class="theme-toggle" onclick="toggleTheme()" aria-label="Toggle theme">
  <div class="toggle-dot"></div>
  <span id="theme-label">Light</span>
</button>

<div class="container">

  <!-- ── HERO ── -->
  <section class="hero">
    <div class="hero-grid">
      <div>
        <div class="hero-label">MERN Stack Developer</div>
        <h1 class="hero-name">Shiva Prasad<br/><span>Chenchala</span></h1>
        <p class="hero-role">Hyderabad, India &nbsp;·&nbsp; <strong>Open to full-time roles</strong></p>
        <div class="hero-badges">
          <div class="badge badge-teal"><span>React + Node.js</span></div>
          <div class="badge badge-red"><span>AI / LLM Integration</span></div>
          <div class="badge badge-gold"><span>Hackathon Winner 🏆</span></div>
        </div>
        <div class="hero-links">
          <a href="https://github.com/Shiva-Prasad83" class="hero-link" target="_blank">
            <svg width="12" height="12" viewBox="0 0 16 16" fill="currentColor"><path d="M8 0C3.58 0 0 3.58 0 8c0 3.54 2.29 6.53 5.47 7.59.4.07.55-.17.55-.38 0-.19-.01-.82-.01-1.49-2.01.37-2.53-.49-2.69-.94-.09-.23-.48-.94-.82-1.13-.28-.15-.68-.52-.01-.53.63-.01 1.08.58 1.23.82.72 1.21 1.87.87 2.33.66.07-.52.28-.87.51-1.07-1.78-.2-3.64-.89-3.64-3.95 0-.87.31-1.59.82-2.15-.08-.2-.36-1.02.08-2.12 0 0 .67-.21 2.2.82.64-.18 1.32-.27 2-.27.68 0 1.36.09 2 .27 1.53-1.04 2.2-.82 2.2-.82.44 1.1.16 1.92.08 2.12.51.56.82 1.27.82 2.15 0 3.07-1.87 3.75-3.65 3.95.29.25.54.73.54 1.48 0 1.07-.01 1.93-.01 2.2 0 .21.15.46.55.38A8.013 8.013 0 0016 8c0-4.42-3.58-8-8-8z"/></svg>
            GitHub
          </a>
          <a href="https://linkedin.com/in/Shiva-Prasad" class="hero-link" target="_blank">
            <svg width="12" height="12" viewBox="0 0 24 24" fill="currentColor"><path d="M20.447 20.452h-3.554v-5.569c0-1.328-.027-3.037-1.852-3.037-1.853 0-2.136 1.445-2.136 2.939v5.667H9.351V9h3.414v1.561h.046c.477-.9 1.637-1.85 3.37-1.85 3.601 0 4.267 2.37 4.267 5.455v6.286zM5.337 7.433c-1.144 0-2.063-.926-2.063-2.065 0-1.138.92-2.063 2.063-2.063 1.14 0 2.064.925 2.064 2.063 0 1.139-.925 2.065-2.064 2.065zm1.782 13.019H3.555V9h3.564v11.452zM22.225 0H1.771C.792 0 0 .774 0 1.729v20.542C0 23.227.792 24 1.771 24h20.451C23.2 24 24 23.227 24 22.271V1.729C24 .774 23.2 0 22.222 0h.003z"/></svg>
            LinkedIn
          </a>
          <a href="mailto:shivaprasad.ch83@gmail.com" class="hero-link">
            <svg width="12" height="12" viewBox="0 0 24 24" fill="currentColor"><path d="M20 4H4c-1.1 0-2 .9-2 2v12c0 1.1.9 2 2 2h16c1.1 0 2-.9 2-2V6c0-1.1-.9-2-2-2zm0 4l-8 5-8-5V6l8 5 8-5v2z"/></svg>
            Email
          </a>
          <a href="tel:+918374329825" class="hero-link">
            <svg width="12" height="12" viewBox="0 0 24 24" fill="currentColor"><path d="M6.62 10.79c1.44 2.83 3.76 5.14 6.59 6.59l2.2-2.2c.27-.27.67-.36 1.02-.24 1.12.37 2.33.57 3.57.57.55 0 1 .45 1 1V20c0 .55-.45 1-1 1-9.39 0-17-7.61-17-17 0-.55.45-1 1-1h3.5c.55 0 1 .45 1 1 0 1.25.2 2.45.57 3.57.11.35.03.74-.25 1.02l-2.2 2.2z"/></svg>
            +91 8374329825
          </a>
        </div>
      </div>
      <div class="hero-right">
        <div class="status-pill">
          <div class="status-dot"></div>
          Available for hire
        </div>
        <div class="trophy-block">
          <div class="trophy-label">🏆 Hackathon Winner</div>
          <div class="trophy-text">AccioJob React Hackathon<br/>AI Object Recognition System</div>
        </div>
      </div>
    </div>
  </section>

  <!-- ── ABOUT ── -->
  <div class="section-header">
    <span class="section-num">01</span>
    <h2>About</h2>
    <div class="section-line"></div>
  </div>

  <div class="about-code">
    <div class="code-bar">
      <div class="code-dot" style="background:#ff5f56"></div>
      <div class="code-dot" style="background:#ffbd2e"></div>
      <div class="code-dot" style="background:#27c93f"></div>
      <span class="code-filename">about.js</span>
    </div>
    <pre><span class="c-comment">// B.Sc Computer Science — Osmania University, 2025</span>
<span class="c-key">const</span> shivaPrasad = {
  <span class="c-key">role</span>        : <span class="c-str">"MERN Stack Developer"</span>,
  <span class="c-key">location</span>    : <span class="c-str">"Hyderabad, India 🇮🇳"</span>,
  <span class="c-key">passion</span>     : <span class="c-arr">["Full-Stack Apps", "AI Integration", "Clean Code"]</span>,
  <span class="c-key">currentFocus</span>: <span class="c-str">"Production-ready apps · React + Node.js + AI APIs"</span>,
  <span class="c-key">openTo</span>      : <span class="c-str">"Full-time roles / Internships / Collaborations"</span>,
  <span class="c-key">funFact</span>     : <span class="c-str">"Won a React Hackathon with an AI Object Recognition System 🏆"</span>
<span class="c-brace">}</span></pre>
  </div>

  <!-- ── TECH STACK ── -->
  <div class="section-header">
    <span class="section-num">02</span>
    <h2>Tech Stack</h2>
    <div class="section-line"></div>
  </div>

  <div class="tech-section">
    <div class="tech-group">
      <div class="tech-group-label">Frontend</div>
      <div class="tech-tags">
        <span class="tech-tag">React.js</span>
        <span class="tech-tag">JavaScript ES6+</span>
        <span class="tech-tag">HTML5</span>
        <span class="tech-tag">Tailwind CSS</span>
        <span class="tech-tag">Vite</span>
        <span class="tech-tag">React Router</span>
      </div>
    </div>
    <div class="tech-group">
      <div class="tech-group-label">State Management</div>
      <div class="tech-tags">
        <span class="tech-tag">Redux Toolkit</span>
        <span class="tech-tag">Context API</span>
      </div>
    </div>
    <div class="tech-group">
      <div class="tech-group-label">Backend</div>
      <div class="tech-tags">
        <span class="tech-tag">Node.js</span>
        <span class="tech-tag">Express.js</span>
        <span class="tech-tag">REST APIs</span>
        <span class="tech-tag">JWT Auth</span>
        <span class="tech-tag">bcrypt</span>
      </div>
    </div>
    <div class="tech-group">
      <div class="tech-group-label">AI / LLM</div>
      <div class="tech-tags">
        <span class="tech-tag">Google Gemini API</span>
        <span class="tech-tag">Groq API (Llama-3)</span>
      </div>
    </div>
    <div class="tech-group">
      <div class="tech-group-label">Database</div>
      <div class="tech-tags">
        <span class="tech-tag">MongoDB</span>
        <span class="tech-tag">Mongoose</span>
        <span class="tech-tag">MongoDB Compass</span>
      </div>
    </div>
    <div class="tech-group">
      <div class="tech-group-label">Dev Tools</div>
      <div class="tech-tags">
        <span class="tech-tag">Git</span>
        <span class="tech-tag">GitHub</span>
        <span class="tech-tag">Postman</span>
        <span class="tech-tag">Vercel</span>
        <span class="tech-tag">Render</span>
      </div>
    </div>
  </div>

  <!-- ── PROJECTS ── -->
  <div class="section-header">
    <span class="section-num">03</span>
    <h2>Featured Projects</h2>
    <div class="section-line"></div>
  </div>

  <div class="projects-grid">

    <div class="project-card p-gold">
      <div class="project-icon">🎯</div>
      <div>
        <span class="project-title">Smart Camera</span>
        <span class="project-winner">🏆 Winner</span>
      </div>
      <p class="project-desc">Real-time AI-powered web app that captures live video frames and identifies objects using multimodal AI.</p>
      <div class="project-highlights">
        <div class="project-highlight">Web Camera API for live video streaming & frame capture</div>
        <div class="project-highlight">Base64 image encoding for backend AI processing</div>
        <div class="project-highlight">Google Gemini multimodal API for object detection</div>
        <div class="project-highlight">React.js interface for real-time results display</div>
      </div>
      <div class="project-stack">
        <span class="stack-tag">React</span>
        <span class="stack-tag">Node.js</span>
        <span class="stack-tag">Express.js</span>
        <span class="stack-tag">Gemini API</span>
      </div>
    </div>

    <div class="project-card p-teal">
      <div class="project-icon">🧾</div>
      <div class="project-title">Resume ATS Analyzer</div>
      <p class="project-desc">AI-powered Chrome Extension that scores resumes against job descriptions and gives actionable feedback.</p>
      <div class="project-highlights">
        <div class="project-highlight">Groq LLM (Llama-3) for semantic resume analysis</div>
        <div class="project-highlight">PDF parsing with Multer & PDF Parser</div>
        <div class="project-highlight">ATS score + missing keywords & skill suggestions</div>
        <div class="project-highlight">Structured AI prompting via Node.js/Express backend</div>
      </div>
      <div class="project-stack">
        <span class="stack-tag">Node.js</span>
        <span class="stack-tag">Groq API</span>
        <span class="stack-tag">Multer</span>
        <span class="stack-tag">Chrome Ext</span>
      </div>
    </div>

    <div class="project-card p-red">
      <div class="project-icon">✅</div>
      <div class="project-title">Task Manager App</div>
      <p class="project-desc">Full-stack task management application with secure JWT authentication and protected routes.</p>
      <div class="project-highlights">
        <div class="project-highlight">JWT authentication + bcrypt password hashing</div>
        <div class="project-highlight">MongoDB + Mongoose schemas for data storage</div>
        <div class="project-highlight">Custom middleware for route protection</div>
        <div class="project-highlight">RESTful CRUD APIs for complete task management</div>
      </div>
      <div class="project-stack">
        <span class="stack-tag">React</span>
        <span class="stack-tag">Tailwind</span>
        <span class="stack-tag">MongoDB</span>
        <span class="stack-tag">JWT</span>
      </div>
    </div>

    <div class="next-card">
      <div class="next-title">What's Next</div>
      <div class="next-items">
        <div class="next-item">
          <div class="next-item-icon">🔷</div>
          TypeScript for type-safe development
        </div>
        <div class="next-item">
          <div class="next-item-icon">☁️</div>
          Cloud deployments — AWS / GCP
        </div>
        <div class="next-item">
          <div class="next-item-icon">🧪</div>
          Testing with Jest & React Testing Library
        </div>
        <div class="next-item">
          <div class="next-item-icon">📦</div>
          Microservices & Docker basics
        </div>
      </div>
    </div>

  </div>

  <!-- ── CONTACT ── -->
  <div class="section-header">
    <span class="section-num">04</span>
    <h2>Let's Connect</h2>
    <div class="section-line"></div>
  </div>

  <div class="contact-card">
    <div class="contact-headline">Open to Opportunities</div>
    <p class="contact-sub">Actively looking for full-time roles and collaborative projects in full-stack development. If you have an exciting opportunity or just want to say hi — my inbox is open!</p>
    <div class="contact-links">
      <a href="https://linkedin.com/in/Shiva-Prasad" class="contact-link cl-teal" target="_blank">Connect on LinkedIn</a>
      <a href="mailto:shivaprasad.ch83@gmail.com" class="contact-link cl-red">Send an Email</a>
      <a href="https://github.com/Shiva-Prasad83" class="contact-link cl-dark" target="_blank">Follow on GitHub</a>
    </div>
  </div>

  <div class="footer">
    <span>Built with ♥ — Shiva Prasad Chenchala · 2025</span>
  </div>

</div>

<script>
  // Detect OS preference on load
  const prefersDark = window.matchMedia('(prefers-color-scheme: dark)').matches;
  let dark = prefersDark;
  applyTheme();

  function applyTheme() {
    document.documentElement.setAttribute('data-theme', dark ? 'dark' : 'light');
    document.getElementById('theme-label').textContent = dark ? 'Dark' : 'Light';
  }

  function toggleTheme() {
    dark = !dark;
    applyTheme();
  }
</script>
</body>
</html>
