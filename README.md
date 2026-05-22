# Zaki Patel GitHub Profile

```html

<!DOCTYPE html>
<html>
<head>
<meta charset="UTF-8">
<style>
  @import url('https://fonts.googleapis.com/css2?family=Share+Tech+Mono&family=Rajdhani:wght@300;400;600;700&family=Orbitron:wght@400;700;900&display=swap');

  :root {
    --red: #FF003C;
    --red-glow: #FF003C44;
    --blue: #0057FF;
    --blue-dim: #0057FF33;
    --dark: #050508;
    --darker: #020204;
    --panel: #0a0a12;
    --panel2: #0f0f1a;
    --border: #1a1a2e;
    --text: #e8e8f0;
    --muted: #6060a0;
    --mono: 'Share Tech Mono', monospace;
    --display: 'Orbitron', sans-serif;
    --body: 'Rajdhani', sans-serif;
  }

  * { box-sizing: border-box; margin: 0; padding: 0; }

  body {
    background: var(--dark);
    color: var(--text);
    font-family: var(--body);
    font-size: 15px;
    line-height: 1.6;
    overflow-x: hidden;
  }

  /* SCANLINE OVERLAY */
  body::before {
    content: '';
    position: fixed;
    inset: 0;
    background: repeating-linear-gradient(
      0deg,
      transparent,
      transparent 2px,
      rgba(0,0,30,0.15) 2px,
      rgba(0,0,30,0.15) 4px
    );
    pointer-events: none;
    z-index: 1000;
  }

  .wrapper {
    max-width: 860px;
    margin: 0 auto;
    padding: 0 1.5rem 4rem;
  }

  /* ── HERO ── */
  .hero {
    position: relative;
    padding: 3.5rem 0 2rem;
    display: grid;
    grid-template-columns: 1fr auto;
    gap: 2rem;
    align-items: center;
    border-bottom: 1px solid var(--border);
    margin-bottom: 3rem;
    overflow: hidden;
  }

  .hero::before {
    content: '';
    position: absolute;
    inset: 0;
    background:
      radial-gradient(ellipse 60% 80% at 90% 50%, var(--blue-dim) 0%, transparent 70%),
      radial-gradient(ellipse 40% 60% at -10% 50%, var(--red-glow) 0%, transparent 70%);
    z-index: 0;
  }

  .hero-content { position: relative; z-index: 1; }

  .hero-badge {
    display: inline-flex;
    align-items: center;
    gap: 8px;
    font-family: var(--mono);
    font-size: 11px;
    letter-spacing: 0.15em;
    color: var(--red);
    border: 1px solid var(--red);
    padding: 4px 12px;
    border-radius: 2px;
    margin-bottom: 1.2rem;
    text-transform: uppercase;
  }

  .hero-badge::before {
    content: '';
    width: 6px; height: 6px;
    background: var(--red);
    border-radius: 50%;
    animation: pulse 1.4s ease-in-out infinite;
  }

  @keyframes pulse {
    0%,100% { opacity: 1; transform: scale(1); }
    50% { opacity: 0.4; transform: scale(0.7); }
  }

  .hero-name {
    font-family: var(--display);
    font-size: clamp(2rem, 5vw, 3.2rem);
    font-weight: 900;
    line-height: 1;
    letter-spacing: -0.02em;
    margin-bottom: 0.4rem;
    background: linear-gradient(135deg, #fff 30%, #aaa 100%);
    -webkit-background-clip: text;
    -webkit-text-fill-color: transparent;
    background-clip: text;
  }

  .hero-handle {
    font-family: var(--mono);
    font-size: 13px;
    color: var(--muted);
    margin-bottom: 1.2rem;
    letter-spacing: 0.08em;
  }

  .hero-handle span { color: var(--blue); }

  .hero-tagline {
    font-size: 1.05rem;
    color: #9090c0;
    font-weight: 400;
    max-width: 460px;
    line-height: 1.5;
  }

  .hero-tagline strong {
    color: var(--text);
    font-weight: 600;
  }

  /* Spider SVG */
  .spider-frame {
    position: relative;
    z-index: 1;
    width: 130px;
    height: 130px;
    flex-shrink: 0;
  }

  .spider-frame svg {
    animation: spiderFloat 4s ease-in-out infinite;
  }

  @keyframes spiderFloat {
    0%,100% { transform: translateY(0) rotate(-2deg); }
    50% { transform: translateY(-10px) rotate(2deg); }
  }

  /* ── YAML BLOCK ── */
  .yaml-card {
    background: var(--panel);
    border: 1px solid var(--border);
    border-radius: 4px;
    padding: 1.4rem 1.8rem;
    font-family: var(--mono);
    font-size: 12.5px;
    line-height: 2;
    position: relative;
    overflow: hidden;
    margin-bottom: 2.5rem;
  }

  .yaml-card::before {
    content: 'config.yaml';
    position: absolute;
    top: 0; left: 0;
    font-size: 10px;
    letter-spacing: 0.12em;
    color: var(--muted);
    background: var(--panel2);
    border-bottom: 1px solid var(--border);
    border-right: 1px solid var(--border);
    padding: 3px 12px;
    border-radius: 4px 0 4px 0;
  }

  .yaml-card::after {
    content: '';
    position: absolute;
    top: 0; right: 0; bottom: 0;
    width: 3px;
    background: linear-gradient(180deg, var(--red) 0%, var(--blue) 100%);
  }

  .y-key { color: #7878d0; }
  .y-val { color: #b8f0b8; }
  .y-str { color: #f0c080; }
  .y-arr { color: #80c8f0; }
  .y-comment { color: var(--muted); }
  .y-indent { display: inline-block; width: 18px; }

  /* ── SECTION TITLE ── */
  .section-head {
    display: flex;
    align-items: center;
    gap: 12px;
    margin-bottom: 1.5rem;
  }

  .section-head h2 {
    font-family: var(--display);
    font-size: 11px;
    font-weight: 700;
    letter-spacing: 0.2em;
    text-transform: uppercase;
    color: var(--muted);
  }

  .section-head::after {
    content: '';
    flex: 1;
    height: 1px;
    background: linear-gradient(90deg, var(--border) 0%, transparent 100%);
  }

  .section-num {
    font-family: var(--mono);
    font-size: 10px;
    color: var(--red);
    background: var(--red-glow);
    border: 1px solid var(--red);
    border-radius: 2px;
    padding: 1px 6px;
  }

  /* ── TECH STACK ── */
  .stack-grid {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(140px, 1fr));
    gap: 10px;
    margin-bottom: 2.5rem;
  }

  .stack-item {
    background: var(--panel);
    border: 1px solid var(--border);
    border-radius: 3px;
    padding: 12px 14px;
    display: flex;
    align-items: center;
    gap: 10px;
    transition: border-color 0.2s, background 0.2s;
    cursor: default;
    position: relative;
    overflow: hidden;
  }

  .stack-item::before {
    content: '';
    position: absolute;
    left: 0; top: 0; bottom: 0;
    width: 2px;
    background: var(--accent, var(--blue));
  }

  .stack-item:hover {
    border-color: var(--accent, var(--blue));
    background: var(--panel2);
  }

  .stack-icon {
    width: 28px; height: 28px;
    border-radius: 4px;
    display: flex; align-items: center; justify-content: center;
    font-size: 16px;
    background: var(--panel2);
    flex-shrink: 0;
  }

  .stack-info { min-width: 0; }
  .stack-name {
    font-family: var(--mono);
    font-size: 11.5px;
    color: var(--text);
    white-space: nowrap;
    overflow: hidden;
    text-overflow: ellipsis;
  }
  .stack-cat {
    font-size: 10px;
    color: var(--muted);
    text-transform: uppercase;
    letter-spacing: 0.08em;
  }

  /* ── PROJECTS ── */
  .projects-grid {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
    gap: 12px;
    margin-bottom: 2.5rem;
  }

  .project-card {
    background: var(--panel);
    border: 1px solid var(--border);
    border-radius: 4px;
    padding: 1.3rem 1.5rem;
    position: relative;
    overflow: hidden;
    transition: border-color 0.25s, transform 0.2s;
  }

  .project-card:hover {
    border-color: #2a2a4a;
    transform: translateY(-2px);
  }

  .project-card::after {
    content: '';
    position: absolute;
    bottom: 0; left: 0; right: 0;
    height: 1px;
    background: linear-gradient(90deg, transparent, var(--accent, var(--blue)), transparent);
  }

  .project-number {
    font-family: var(--mono);
    font-size: 10px;
    color: var(--muted);
    margin-bottom: 0.5rem;
    letter-spacing: 0.1em;
  }

  .project-title {
    font-family: var(--display);
    font-size: 13px;
    font-weight: 700;
    letter-spacing: 0.05em;
    margin-bottom: 0.5rem;
    color: var(--text);
  }

  .project-desc {
    font-size: 13px;
    color: #7878a0;
    line-height: 1.5;
    margin-bottom: 0.9rem;
  }

  .project-tags {
    display: flex;
    flex-wrap: wrap;
    gap: 6px;
  }

  .tag {
    font-family: var(--mono);
    font-size: 10px;
    padding: 2px 8px;
    border-radius: 2px;
    border: 1px solid;
    letter-spacing: 0.05em;
    text-transform: uppercase;
  }

  .tag-blue { color: #6090ff; border-color: #6090ff44; background: #6090ff11; }
  .tag-red  { color: #ff6080; border-color: #ff608044; background: #ff608011; }
  .tag-green{ color: #50e0a0; border-color: #50e0a044; background: #50e0a011; }
  .tag-amber{ color: #ffb060; border-color: #ffb06044; background: #ffb06011; }

  /* ── STATS ROW ── */
  .stats-row {
    display: grid;
    grid-template-columns: repeat(4, 1fr);
    gap: 10px;
    margin-bottom: 2.5rem;
  }

  .stat-box {
    background: var(--panel);
    border: 1px solid var(--border);
    border-radius: 3px;
    padding: 1.1rem 1rem;
    text-align: center;
    position: relative;
  }

  .stat-box::before {
    content: '';
    position: absolute;
    top: 0; left: 50%; transform: translateX(-50%);
    width: 40%; height: 1px;
    background: var(--accent, var(--blue));
  }

  .stat-num {
    font-family: var(--display);
    font-size: 1.6rem;
    font-weight: 900;
    background: linear-gradient(135deg, #fff, #888);
    -webkit-background-clip: text;
    -webkit-text-fill-color: transparent;
    background-clip: text;
    display: block;
    line-height: 1.2;
  }

  .stat-label {
    font-family: var(--mono);
    font-size: 10px;
    color: var(--muted);
    letter-spacing: 0.12em;
    text-transform: uppercase;
    margin-top: 2px;
  }

  /* ── CONNECT ── */
  .connect-row {
    display: flex;
    gap: 12px;
    flex-wrap: wrap;
    margin-bottom: 3rem;
  }

  .connect-btn {
    display: inline-flex;
    align-items: center;
    gap: 10px;
    padding: 10px 20px;
    border-radius: 3px;
    font-family: var(--mono);
    font-size: 12px;
    letter-spacing: 0.1em;
    text-transform: uppercase;
    text-decoration: none;
    border: 1px solid;
    transition: all 0.2s;
    cursor: pointer;
    background: transparent;
  }

  .btn-linkedin {
    color: #60a8ff;
    border-color: #60a8ff44;
  }
  .btn-linkedin:hover {
    background: #60a8ff11;
    border-color: #60a8ff;
  }

  .btn-github {
    color: var(--red);
    border-color: var(--red-glow);
  }
  .btn-github:hover {
    background: var(--red-glow);
    border-color: var(--red);
  }

  /* ── FOOTER QUOTE ── */
  .footer-quote {
    display: flex;
    align-items: center;
    gap: 16px;
    padding: 1.5rem 0;
    border-top: 1px solid var(--border);
  }

  .footer-icon {
    font-size: 2rem;
    flex-shrink: 0;
    filter: drop-shadow(0 0 12px var(--red));
    animation: spiderFloat 3s ease-in-out infinite;
  }

  .footer-text {
    font-family: var(--display);
    font-size: 14px;
    font-weight: 700;
    letter-spacing: 0.1em;
    text-transform: uppercase;
    color: var(--muted);
  }

  .footer-text span { color: var(--text); }

  /* ── TERMINAL CURSOR ── */
  .cursor {
    display: inline-block;
    width: 8px; height: 13px;
    background: var(--red);
    vertical-align: middle;
    animation: blink 1s step-end infinite;
    margin-left: 2px;
  }
  @keyframes blink { 50% { opacity: 0; } }

  /* ── WEB ANIMATION ── */
  .web-bg {
    position: absolute;
    top: -20px; right: -20px;
    opacity: 0.04;
    pointer-events: none;
  }

  /* responsive */
  @media (max-width: 560px) {
    .stats-row { grid-template-columns: repeat(2, 1fr); }
    .hero { grid-template-columns: 1fr; }
    .spider-frame { display: none; }
  }
</style>
</head>
<body>

<div class="wrapper">

  <!-- HERO -->
  <header class="hero">
    <!-- Web BG -->
    <svg class="web-bg" width="220" height="220" viewBox="0 0 220 220">
      <g stroke="white" stroke-width="0.8" fill="none">
        <line x1="110" y1="0" x2="110" y2="220"/>
        <line x1="0" y1="110" x2="220" y2="110"/>
        <line x1="0" y1="0" x2="220" y2="220"/>
        <line x1="220" y1="0" x2="0" y2="220"/>
        <circle cx="110" cy="110" r="30"/><circle cx="110" cy="110" r="60"/>
        <circle cx="110" cy="110" r="90"/><circle cx="110" cy="110" r="120"/>
      </g>
    </svg>

    <div class="hero-content">
      <div class="hero-badge">// IDENTITY_CONFIRMED</div>
      <h1 class="hero-name">ZAKI PATEL</h1>
      <p class="hero-handle">@<span>PatelZaki86</span> · Pune, India<span class="cursor"></span></p>
      <p class="hero-tagline">
        <strong>AI Engineer</strong> building agentic intelligence —
        autonomous systems, generative AI, and cloud-native infrastructure at the edge of what's possible.
      </p>
    </div>

    <!-- Spider Logo SVG -->
    <div class="spider-frame">
      <svg width="130" height="130" viewBox="0 0 100 100" fill="none">
        <!-- Web rays -->
        <g stroke="#FF003C" stroke-width="0.6" opacity="0.4">
          <line x1="50" y1="5" x2="50" y2="95"/>
          <line x1="5" y1="50" x2="95" y2="50"/>
          <line x1="15" y1="15" x2="85" y2="85"/>
          <line x1="85" y1="15" x2="15" y2="85"/>
        </g>
        <!-- Web rings -->
        <g stroke="#FF003C" stroke-width="0.5" fill="none" opacity="0.3">
          <circle cx="50" cy="50" r="15"/>
          <circle cx="50" cy="50" r="28"/>
          <circle cx="50" cy="50" r="42"/>
        </g>
        <!-- Spider body -->
        <ellipse cx="50" cy="46" rx="9" ry="11" fill="#FF003C" opacity="0.9"/>
        <ellipse cx="50" cy="60" rx="12" ry="14" fill="#CC0030" opacity="0.95"/>
        <!-- Eyes -->
        <circle cx="46" cy="43" r="2.5" fill="white" opacity="0.95"/>
        <circle cx="54" cy="43" r="2.5" fill="white" opacity="0.95"/>
        <circle cx="46.8" cy="43.5" r="1.2" fill="#0057FF"/>
        <circle cx="54.8" cy="43.5" r="1.2" fill="#0057FF"/>
        <!-- Legs -->
        <g stroke="#FF003C" stroke-width="1.2" stroke-linecap="round" opacity="0.8">
          <path d="M41 50 Q28 45 20 38"/>
          <path d="M41 54 Q27 52 18 50"/>
          <path d="M41 58 Q27 60 20 65"/>
          <path d="M41 62 Q28 70 22 78"/>
          <path d="M59 50 Q72 45 80 38"/>
          <path d="M59 54 Q73 52 82 50"/>
          <path d="M59 58 Q73 60 80 65"/>
          <path d="M59 62 Q72 70 78 78"/>
        </g>
        <!-- Chest mark -->
        <path d="M50 52 L46 60 L50 57 L54 60 Z" fill="white" opacity="0.7"/>
        <!-- Glow -->
        <circle cx="50" cy="50" r="45" stroke="#FF003C" stroke-width="0.8" fill="none" opacity="0.15"/>
      </svg>
    </div>
  </header>

  <!-- YAML -->
  <div class="yaml-card">
    <span class="y-comment"># ── identity.yaml ─────────────────────────</span><br>
    <span class="y-key">name</span>: <span class="y-str">"Zaki Patel"</span><br>
    <span class="y-key">role</span>: <span class="y-str">"AI Engineer"</span><br>
    <span class="y-key">location</span>: <span class="y-str">"India 🇮🇳"</span><br>
    <span class="y-key">focus</span>:<br>
    <span class="y-indent"></span><span class="y-arr">- </span><span class="y-val">Agentic AI Systems</span><br>
    <span class="y-indent"></span><span class="y-arr">- </span><span class="y-val">Generative AI</span><br>
    <span class="y-indent"></span><span class="y-arr">- </span><span class="y-val">Cybersecurity</span><br>
    <span class="y-key">current_mission</span>: <span class="y-str">"Building futuristic AI at civilisation scale"</span><br>
    <span class="y-key">status</span>: <span style="color:#50e090">ONLINE</span> <span class="cursor" style="width:6px;height:11px;background:#50e090"></span>
  </div>

  <!-- STATS -->
  <div class="section-head">
    <span class="section-num">01</span>
    <h2>Signal Stats</h2>
  </div>
  <div class="stats-row">
    <div class="stat-box" style="--accent: var(--red)">
      <span class="stat-num">4+</span>
      <span class="stat-label">Projects</span>
    </div>
    <div class="stat-box" style="--accent: #0057FF">
      <span class="stat-num">3</span>
      <span class="stat-label">AI Domains</span>
    </div>
    <div class="stat-box" style="--accent: #50e0a0">
      <span class="stat-num">∞</span>
      <span class="stat-label">Ambition</span>
    </div>
    <div class="stat-box" style="--accent: #ffb060">
      <span class="stat-num">1</span>
      <span class="stat-label">Mission</span>
    </div>
  </div>

  <!-- TECH STACK -->
  <div class="section-head">
    <span class="section-num">02</span>
    <h2>Tech Stack</h2>
  </div>
  <div class="stack-grid" style="margin-bottom:2.5rem">
    <div class="stack-item" style="--accent:#3776AB"><div class="stack-icon">🐍</div><div class="stack-info"><div class="stack-name">Python</div><div class="stack-cat">Core Lang</div></div></div>
    <div class="stack-item" style="--accent:#61DBFB"><div class="stack-icon">⚛️</div><div class="stack-info"><div class="stack-name">React</div><div class="stack-cat">Frontend</div></div></div>
    <div class="stack-item" style="--accent:#68A063"><div class="stack-icon">🟩</div><div class="stack-info"><div class="stack-name">Node.js</div><div class="stack-cat">Runtime</div></div></div>
    <div class="stack-item" style="--accent:#009688"><div class="stack-icon">⚡</div><div class="stack-info"><div class="stack-name">FastAPI</div><div class="stack-cat">Backend</div></div></div>
    <div class="stack-item" style="--accent:#2496ED"><div class="stack-icon">🐳</div><div class="stack-info"><div class="stack-name">Docker</div><div class="stack-cat">Containers</div></div></div>
    <div class="stack-item" style="--accent:#326CE5"><div class="stack-icon">☸️</div><div class="stack-info"><div class="stack-name">Kubernetes</div><div class="stack-cat">Orchestrate</div></div></div>
    <div class="stack-item" style="--accent:#FF9900"><div class="stack-icon">☁️</div><div class="stack-info"><div class="stack-name">AWS</div><div class="stack-cat">Cloud</div></div></div>
    <div class="stack-item" style="--accent:#4285F4"><div class="stack-icon">🌐</div><div class="stack-info"><div class="stack-name">GCP</div><div class="stack-cat">Cloud</div></div></div>
    <div class="stack-item" style="--accent:#47A248"><div class="stack-icon">🍃</div><div class="stack-info"><div class="stack-name">MongoDB</div><div class="stack-cat">Database</div></div></div>
    <div class="stack-item" style="--accent:#FF6600"><div class="stack-icon">🔶</div><div class="stack-info"><div class="stack-name">PyTorch</div><div class="stack-cat">ML Framework</div></div></div>
    <div class="stack-item" style="--accent:#FF6F00"><div class="stack-icon">🧠</div><div class="stack-info"><div class="stack-name">TensorFlow</div><div class="stack-cat">Deep Learning</div></div></div>
    <div class="stack-item" style="--accent:var(--red)"><div class="stack-icon">🔐</div><div class="stack-info"><div class="stack-name">Cybersec</div><div class="stack-cat">Security</div></div></div>
  </div>

  <!-- PROJECTS -->
  <div class="section-head">
    <span class="section-num">03</span>
    <h2>Featured Projects</h2>
  </div>
  <div class="projects-grid">
    <div class="project-card" style="--accent:#50e0a0">
      <div class="project-number">// PROJECT_001</div>
      <div class="project-title">GST RECONCILIATION AGENT</div>
      <div class="project-desc">AI-powered autonomous agent for end-to-end GST reconciliation and financial compliance automation.</div>
      <div class="project-tags">
        <span class="tag tag-green">Agentic AI</span>
        <span class="tag tag-blue">FastAPI</span>
        <span class="tag tag-amber">FinTech</span>
      </div>
    </div>
    <div class="project-card" style="--accent:#6090ff">
      <div class="project-number">// PROJECT_002</div>
      <div class="project-title">FARM ANALYTICS PLATFORM</div>
      <div class="project-desc">Predictive intelligence for agriculture — satellite data fusion, yield forecasting, soil health monitoring.</div>
      <div class="project-tags">
        <span class="tag tag-green">ML / Vision</span>
        <span class="tag tag-blue">Cloud</span>
        <span class="tag tag-amber">AgriTech</span>
      </div>
    </div>
    <div class="project-card" style="--accent:var(--red)">
      <div class="project-number">// PROJECT_003</div>
      <div class="project-title">MULTI-AGENT AI SYSTEMS</div>
      <div class="project-desc">Collaborative autonomous agent networks — task planning, tool-use, memory, emergent coordination.</div>
      <div class="project-tags">
        <span class="tag tag-red">Multi-Agent</span>
        <span class="tag tag-blue">LLM</span>
        <span class="tag tag-amber">Research</span>
      </div>
    </div>
    <div class="project-card" style="--accent:#ffb060">
      <div class="project-number">// PROJECT_004</div>
      <div class="project-title">DEVOPS AUTOMATION</div>
      <div class="project-desc">Zero-touch CI/CD pipelines, cloud-native infra provisioning, and self-healing deployment workflows.</div>
      <div class="project-tags">
        <span class="tag tag-blue">LLM's</span>
        <span class="tag tag-green">Docker</span>
        <span class="tag tag-amber">CI/CD</span>
      </div>
    </div>
  </div>

  <!-- CONNECT -->
  <div class="section-head">
    <span class="section-num">04</span>
    <h2>Connect</h2>
  </div>
  <div class="connect-row">
    <a href="https://linkedin.com" class="connect-btn btn-linkedin">
      <svg width="16" height="16" viewBox="0 0 24 24" fill="currentColor"><path d="M16 8a6 6 0 016 6v7h-4v-7a2 2 0 00-2-2 2 2 0 00-2 2v7h-4v-7a6 6 0 016-6zM2 9h4v12H2z"/><circle cx="4" cy="4" r="2"/></svg>
      linkedin
    </a>
    <a href="https://github.com/PatelZaki86" class="connect-btn btn-github">
      <svg width="16" height="16" viewBox="0 0 24 24" fill="currentColor"><path d="M12 2C6.477 2 2 6.484 2 12.017c0 4.425 2.865 8.18 6.839 9.504.5.092.682-.217.682-.483 0-.237-.008-.868-.013-1.703-2.782.605-3.369-1.343-3.369-1.343-.454-1.158-1.11-1.466-1.11-1.466-.908-.62.069-.608.069-.608 1.003.07 1.531 1.032 1.531 1.032.892 1.53 2.341 1.088 2.91.832.092-.647.35-1.088.636-1.338-2.22-.253-4.555-1.113-4.555-4.951 0-1.093.39-1.988 1.029-2.688-.103-.253-.446-1.272.098-2.65 0 0 .84-.27 2.75 1.026A9.564 9.564 0 0112 6.844c.85.004 1.705.115 2.504.337 1.909-1.296 2.747-1.027 2.747-1.027.546 1.379.202 2.398.1 2.651.64.7 1.028 1.595 1.028 2.688 0 3.848-2.339 4.695-4.566 4.943.359.309.678.92.678 1.855 0 1.338-.012 2.419-.012 2.747 0 .268.18.58.688.482A10.019 10.019 0 0022 12.017C22 6.484 17.522 2 12 2z"/></svg>
      github/PatelZaki86
    </a>
  </div>

  <!-- FOOTER -->
  <footer class="footer-quote">
    <div class="footer-icon">🕷️</div>
    <div class="footer-text"><span>"Anyone can wear the mask."</span><br>Build the future. Ship the impossible.</div>
  </footer>

</div>

</body>
</html>

```
