<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8" />
<meta name="viewport" content="width=device-width, initial-scale=1.0"/>
<title>GitHub Profile README Preview</title>
<style>
  @import url('https://fonts.googleapis.com/css2?family=JetBrains+Mono:wght@400;600;700&family=Inter:wght@300;400;500;600&display=swap');

  :root {
    --bg:       #0d1117;
    --surface:  #161b22;
    --border:   #21262d;
    --muted:    #484f58;
    --text:     #c9d1d9;
    --bright:   #e6edf3;
    --accent:   #58a6ff;
    --green:    #3fb950;
    --purple:   #bc8cff;
    --orange:   #f0883e;
    --pink:     #f778ba;
  }

  * { box-sizing: border-box; margin: 0; padding: 0; }

  body {
    background: #010409;
    display: flex;
    justify-content: center;
    padding: 2rem 1rem 4rem;
    font-family: 'Inter', sans-serif;
    color: var(--text);
    min-height: 100vh;
  }

  .readme {
    width: 100%;
    max-width: 780px;
    background: var(--bg);
    border: 1px solid var(--border);
    border-radius: 6px;
    padding: 2rem 2rem 2.5rem;
    line-height: 1.6;
  }

  /* ── HERO ─────────────────────────────────────── */
  .hero {
    border-bottom: 1px solid var(--border);
    padding-bottom: 1.5rem;
    margin-bottom: 1.5rem;
  }

  .typewriter {
    font-family: 'JetBrains Mono', monospace;
    font-size: 0.8rem;
    color: var(--green);
    margin-bottom: 0.75rem;
    letter-spacing: 0.04em;
  }

  .hero h1 {
    font-size: 1.9rem;
    font-weight: 600;
    color: var(--bright);
    line-height: 1.2;
    margin-bottom: 0.5rem;
  }

  .hero h1 span.accent { color: var(--accent); }
  .hero h1 span.wave {
    display: inline-block;
    animation: wave 2s ease-in-out infinite;
    transform-origin: 70% 70%;
  }
  @keyframes wave {
    0%,100%{ transform: rotate(0deg); }
    20%{ transform: rotate(20deg); }
    40%{ transform: rotate(-8deg); }
    60%{ transform: rotate(12deg); }
    80%{ transform: rotate(-4deg); }
  }

  .hero .tagline {
    font-size: 0.92rem;
    color: var(--text);
    max-width: 560px;
    margin-bottom: 1rem;
  }

  .badges {
    display: flex;
    flex-wrap: wrap;
    gap: 0.45rem;
    margin-top: 0.75rem;
  }
  .badge {
    display: inline-flex;
    align-items: center;
    gap: 0.35rem;
    font-family: 'JetBrains Mono', monospace;
    font-size: 0.72rem;
    padding: 0.25rem 0.65rem;
    border-radius: 100px;
    border: 1px solid;
    font-weight: 600;
    letter-spacing: 0.02em;
  }
  .badge.blue   { color: var(--accent);  border-color: rgba(88,166,255,0.3);  background: rgba(88,166,255,0.08); }
  .badge.green  { color: var(--green);   border-color: rgba(63,185,80,0.3);   background: rgba(63,185,80,0.08); }
  .badge.purple { color: var(--purple);  border-color: rgba(188,140,255,0.3); background: rgba(188,140,255,0.08); }
  .badge.orange { color: var(--orange);  border-color: rgba(240,136,62,0.3);  background: rgba(240,136,62,0.08); }

  /* ── SECTION ──────────────────────────────────── */
  .section {
    margin-bottom: 1.6rem;
  }
  .section-label {
    font-family: 'JetBrains Mono', monospace;
    font-size: 0.7rem;
    color: var(--muted);
    letter-spacing: 0.12em;
    text-transform: uppercase;
    margin-bottom: 0.75rem;
    display: flex;
    align-items: center;
    gap: 0.5rem;
  }
  .section-label::after {
    content: '';
    flex: 1;
    height: 1px;
    background: var(--border);
  }

  /* ── ABOUT ────────────────────────────────────── */
  .about-grid {
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: 0.5rem 1.5rem;
  }
  .about-item {
    font-size: 0.88rem;
    display: flex;
    align-items: baseline;
    gap: 0.4rem;
  }
  .about-item .icon { font-size: 0.95rem; }
  .about-item strong { color: var(--bright); font-weight: 500; }
  .about-item a {
    color: var(--accent);
    text-decoration: none;
  }
  .about-item a:hover { text-decoration: underline; }

  /* ── STACK ────────────────────────────────────── */
  .stack-group { margin-bottom: 0.9rem; }
  .stack-group-title {
    font-size: 0.75rem;
    color: var(--muted);
    margin-bottom: 0.4rem;
    font-weight: 500;
  }
  .pill-row {
    display: flex;
    flex-wrap: wrap;
    gap: 0.4rem;
  }
  .pill {
    font-family: 'JetBrains Mono', monospace;
    font-size: 0.72rem;
    padding: 0.2rem 0.6rem;
    border-radius: 4px;
    background: var(--surface);
    border: 1px solid var(--border);
    color: var(--text);
  }
  .pill:hover { border-color: var(--accent); color: var(--bright); cursor: default; }

  /* ── PROJECTS ─────────────────────────────────── */
  .projects-grid {
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: 0.75rem;
  }
  .project-card {
    background: var(--surface);
    border: 1px solid var(--border);
    border-radius: 6px;
    padding: 0.85rem 1rem;
    transition: border-color 0.15s;
    cursor: default;
  }
  .project-card:hover { border-color: var(--accent); }
  .project-card .proj-title {
    font-size: 0.88rem;
    font-weight: 600;
    color: var(--accent);
    margin-bottom: 0.3rem;
    display: flex;
    align-items: center;
    gap: 0.35rem;
  }
  .project-card .proj-desc {
    font-size: 0.8rem;
    color: var(--text);
    margin-bottom: 0.55rem;
    line-height: 1.5;
  }
  .project-card .proj-tags {
    display: flex;
    flex-wrap: wrap;
    gap: 0.3rem;
  }
  .proj-tag {
    font-family: 'JetBrains Mono', monospace;
    font-size: 0.65rem;
    color: var(--muted);
    background: var(--bg);
    border: 1px solid var(--border);
    padding: 0.12rem 0.45rem;
    border-radius: 3px;
  }

  /* ── STATS ────────────────────────────────────── */
  .stats-row {
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: 0.75rem;
  }
  .stat-card {
    background: var(--surface);
    border: 1px solid var(--border);
    border-radius: 6px;
    padding: 0.85rem 1rem;
    font-size: 0.82rem;
  }
  .stat-card .stat-title {
    color: var(--muted);
    font-size: 0.72rem;
    margin-bottom: 0.55rem;
    font-weight: 600;
    text-transform: uppercase;
    letter-spacing: 0.05em;
  }
  .lang-bar-row {
    display: flex;
    align-items: center;
    gap: 0.5rem;
    margin-bottom: 0.3rem;
  }
  .lang-name {
    font-family: 'JetBrains Mono', monospace;
    font-size: 0.72rem;
    width: 72px;
    flex-shrink: 0;
    color: var(--bright);
  }
  .lang-bar-bg {
    flex: 1;
    height: 6px;
    background: var(--border);
    border-radius: 3px;
    overflow: hidden;
  }
  .lang-bar-fill {
    height: 100%;
    border-radius: 3px;
  }
  .lang-pct {
    font-family: 'JetBrains Mono', monospace;
    font-size: 0.68rem;
    color: var(--muted);
    width: 30px;
    text-align: right;
    flex-shrink: 0;
  }

  .streak-item {
    display: flex;
    justify-content: space-between;
    align-items: baseline;
    margin-bottom: 0.3rem;
  }
  .streak-label { font-size: 0.78rem; color: var(--muted); }
  .streak-value {
    font-family: 'JetBrains Mono', monospace;
    font-size: 0.82rem;
    color: var(--bright);
    font-weight: 600;
  }
  .streak-value.green { color: var(--green); }
  .streak-value.orange { color: var(--orange); }

  /* ── CONNECT ──────────────────────────────────── */
  .connect-row {
    display: flex;
    flex-wrap: wrap;
    gap: 0.5rem;
  }
  .connect-btn {
    display: inline-flex;
    align-items: center;
    gap: 0.4rem;
    font-size: 0.8rem;
    padding: 0.4rem 0.85rem;
    border-radius: 6px;
    border: 1px solid var(--border);
    background: var(--surface);
    color: var(--text);
    text-decoration: none;
    font-family: 'Inter', sans-serif;
    transition: border-color 0.15s, color 0.15s;
    cursor: pointer;
  }
  .connect-btn:hover { border-color: var(--accent); color: var(--bright); }

  /* ── FOOTER ───────────────────────────────────── */
  .footer {
    margin-top: 1.5rem;
    padding-top: 1rem;
    border-top: 1px solid var(--border);
    font-family: 'JetBrains Mono', monospace;
    font-size: 0.72rem;
    color: var(--muted);
    display: flex;
    align-items: center;
    justify-content: space-between;
    flex-wrap: wrap;
    gap: 0.5rem;
  }
  .footer-dot { color: var(--green); margin: 0 0.3rem; }

  /* ── COPY BUTTON ──────────────────────────────── */
  .copy-area {
    margin-top: 2rem;
    background: var(--surface);
    border: 1px solid var(--border);
    border-radius: 6px;
    overflow: hidden;
  }
  .copy-header {
    display: flex;
    align-items: center;
    justify-content: space-between;
    padding: 0.6rem 1rem;
    border-bottom: 1px solid var(--border);
    background: var(--bg);
  }
  .copy-header span {
    font-family: 'JetBrains Mono', monospace;
    font-size: 0.72rem;
    color: var(--muted);
  }
  .copy-btn {
    font-family: 'JetBrains Mono', monospace;
    font-size: 0.72rem;
    padding: 0.2rem 0.7rem;
    border-radius: 4px;
    border: 1px solid var(--border);
    background: var(--surface);
    color: var(--accent);
    cursor: pointer;
    transition: background 0.15s;
  }
  .copy-btn:hover { background: rgba(88,166,255,0.1); }
  .code-block {
    padding: 1rem;
    font-family: 'JetBrains Mono', monospace;
    font-size: 0.72rem;
    color: var(--text);
    white-space: pre-wrap;
    word-break: break-all;
    max-height: 260px;
    overflow-y: auto;
    line-height: 1.7;
  }

  @media (max-width: 560px) {
    .about-grid, .projects-grid, .stats-row { grid-template-columns: 1fr; }
    .readme { padding: 1.25rem; }
  }
</style>
</head>
<body>
<div class="readme">

  <!-- HERO -->
  <div class="hero">
    <div class="typewriter">$ whoami</div>
    <h1><span class="wave">👋</span> Hi, I'm <span class="accent">Michael Andrei Jugado</span></h1>
    <p class="tagline">
      Current Computer Science Student in the University of St. La Salle, building systems that scale, hold up under load, and make sense to the next developer.
    </p>
    <div class="badges">
      <span class="badge blue">🎓 Computer Science @ USLS-Bacolod</span>
      <span class="badge green">🟢 Open to Internships · 2025</span>
      <span class="badge purple">⚡ Currently learning: System Design</span>
      <span class="badge orange">📍 Bacolod, PH</span>
    </div>
  </div>

  <!-- ABOUT -->
  <div class="section">
    <div class="section-label">About</div>
    <div class="about-grid">
      <div class="about-item"><span class="icon">🔭</span> Working on <strong>a full-stack learning module system</strong></div>
      <div class="about-item"><span class="icon">🌱</span> Studying <strong>Web Development and LLMs</strong></div>
      <div class="about-item"><span class="icon">👯</span> Open to collaborate on <strong>open-source projects</strong></div>
      <div class="about-item"><span class="icon">🤔</span> Exploring <strong>backend architecture patterns</strong></div>
      <div class="about-item"><span class="icon">💬</span> Ask me about <strong>Python, Java, or React</strong></div>
      <div class="about-item"><span class="icon">📫</span> Reach me at <a href="mailto:jugadomichael@gmail.com">jugadomichael@gmail.com</a></div>
    </div>
  </div>

  <!-- TECH STACK -->
  <div class="section">
    <div class="section-label">Tech Stack</div>
    <div class="stack-group">
      <div class="stack-group-title">Languages</div>
      <div class="pill-row">
        <span class="pill">Python</span>
        <span class="pill">Java</span>
        <span class="pill">JavaScript</span>
        <span class="pill">TypeScript</span>
        <span class="pill">C++</span>
        <span class="pill">C#</span>
        <span class="pill">SQL</span>
        <span class="pill">Bash</span>
      </div>
    </div>
    <div class="stack-group">
      <div class="stack-group-title">Frameworks & Libraries</div>
      <div class="pill-row">
        <span class="pill">React</span>
        <span class="pill">Node.js</span>
        <span class="pill">Express</span>
        <span class="pill">Spring Boot</span>
        <span class="pill">FastAPI</span>
        <span class="pill">Tailwind CSS</span>
      </div>
    </div>
    <div class="stack-group">
      <div class="stack-group-title">Tools & Platforms</div>
      <div class="pill-row">
        <span class="pill">Git</span>
        <span class="pill">Docker</span>
        <span class="pill">PostgreSQL</span>
        <span class="pill">MongoDB</span>
        <span class="pill">Convex</span>
        <span class="pill">Clerk</span>
        <span class="pill">VS Code</span>
        <span class="pill">AWS (learning)</span>
        <span class="pill">Azure (learning)</span>
      </div>
    </div>
  </div>

  <!-- PROJECTS -->
  <div class="section">
    <div class="section-label">Featured Projects</div>
    <div class="projects-grid">
      <div class="project-card">
        <div class="proj-title">📋 Learning Module System</div>
        <div class="proj-desc">Full-stack learning module system for new employees.</div>
        <div class="proj-tags">
          <span class="proj-tag">React</span>
          <span class="proj-tag">Next.js</span>
          <span class="proj-tag">Shadcn/ui</span>
          <span class="proj-tag">Clerk</span>
          <span class="proj-tag">Convex</span>
          <span class="proj-tag">Vercel</span>
        </div>
      </div>
    </div>
  </div>

  <!-- STATS -->
  <div class="section">
    <div class="section-label">Stats</div>
    <div class="stats-row">
      <div class="stat-card">
        <div class="stat-title">Top Languages</div>
        <div class="lang-bar-row">
          <span class="lang-name">Python</span>
          <div class="lang-bar-bg"><div class="lang-bar-fill" style="width:72%;background:#3572A5;"></div></div>
          <span class="lang-pct">72%</span>
        </div>
        <div class="lang-bar-row">
          <span class="lang-name">JavaScript</span>
          <div class="lang-bar-bg"><div class="lang-bar-fill" style="width:55%;background:#f1e05a;"></div></div>
          <span class="lang-pct">55%</span>
        </div>
        <div class="lang-bar-row">
          <span class="lang-name">Java</span>
          <div class="lang-bar-bg"><div class="lang-bar-fill" style="width:40%;background:#b07219;"></div></div>
          <span class="lang-pct">40%</span>
        </div>
        <div class="lang-bar-row">
          <span class="lang-name">TypeScript</span>
          <div class="lang-bar-bg"><div class="lang-bar-fill" style="width:28%;background:#2b7489;"></div></div>
          <span class="lang-pct">28%</span>
        </div>
        <div class="lang-bar-row">
          <span class="lang-name">C</span>
          <div class="lang-bar-bg"><div class="lang-bar-fill" style="width:18%;background:#555;"></div></div>
          <span class="lang-pct">18%</span>
        </div>
      </div>
      <div class="stat-card">
        <div class="stat-title">Activity</div>
        <div class="streak-item">
          <span class="streak-label">Total Commits (2024)</span>
          <span class="streak-value green">847</span>
        </div>
        <div class="streak-item">
          <span class="streak-label">Current Streak</span>
          <span class="streak-value orange">🔥 14 days</span>
        </div>
        <div class="streak-item">
          <span class="streak-label">Public Repos</span>
          <span class="streak-value">23</span>
        </div>
        <div class="streak-item">
          <span class="streak-label">Pull Requests</span>
          <span class="streak-value">38</span>
        </div>
        <div class="streak-item">
          <span class="streak-label">Issues Closed</span>
          <span class="streak-value">61</span>
        </div>
      </div>
    </div>
  </div>

  <!-- CONNECT -->
  <div class="section">
    <div class="section-label">Connect</div>
    <div class="connect-row">
      <a class="connect-btn" href="https://www.linkedin.com/in/m-a-jugado/">💼 LinkedIn</a>
      <a class="connect-btn" href="#">🌐 Portfolio(TBA)</a>
      <a class="connect-btn" href="https://www.facebook.com/michaelandrei.jugado/">🐦 Facebook</a>
      <a class="connect-btn" href="#">📄 Resume (TBA)</a>
      <a class="connect-btn" href="jugadomichael@gmail.com">✉️ Email</a>
    </div>
  </div>

  <!-- FOOTER -->
  <div class="footer">
    <span>last updated: June 2025</span>
    <span>
      views: <span style="color:var(--green)">∞</span>
      <span class="footer-dot">·</span>
      made with <span style="color:#f778ba">♥</span> and too much caffeine
    </span>
  </div>

</div>

<!-- MARKDOWN SOURCE -->
<div style="max-width:780px;margin:1.5rem auto 0;">
  <div class="copy-area">
    <div class="copy-header">
      <span>README.md — paste this into your GitHub profile repo</span>
      <button class="copy-btn" onclick="copyMarkdown()">Copy</button>
    </div>
    <div class="code-block" id="md-source"></div>
  </div>
</div>

<script>
const md = `<!-- Banner / Typing SVG (replace with https://readme-typing-svg.herokuapp.com) -->
<h1 align="center">
  Hi 👋, I'm Alex Rivera
</h1>

<p align="center">
  CS student · aspiring Software Engineer · side-project enthusiast
</p>

<p align="center">
  <img src="https://komarev.com/ghpvc/?username=alexrivera&label=Profile+Views&color=0e75b6&style=flat" alt="profile views" />
  <img src="https://img.shields.io/badge/Open%20to-Internships%202025-3fb950?style=flat&logo=github" />
  <img src="https://img.shields.io/badge/Currently%20Learning-System%20Design-bc8cff?style=flat" />
</p>

---

## 👾 About Me

- 🎓 Studying **Computer Science** @ State University
- 🔭 Currently building **TaskFlow** — a real-time full-stack Kanban board
- 🌱 Deep-diving into **Distributed Systems**, **DSA**, and **System Design**
- 👯 Looking to collaborate on **open-source projects**
- 💬 Ask me about **Python, Java, or React**
- 📫 Reach me at **alex@example.com**
- ⚡ Fun fact: I debug with \`console.log\` unironically

---

## 🛠️ Tech Stack

**Languages**
\`Python\` \`Java\` \`JavaScript\` \`TypeScript\` \`C\` \`SQL\` \`Bash\`

**Frameworks & Libraries**
\`React\` \`Node.js\` \`Express\` \`Spring Boot\` \`FastAPI\` \`Tailwind CSS\`

**Tools & Platforms**
\`Git\` \`Docker\` \`PostgreSQL\` \`MongoDB\` \`Linux\` \`VS Code\` \`AWS (learning)\`

---

## 🚀 Featured Projects

| Project | Description | Stack |
|---------|-------------|-------|
| [📋 TaskFlow](https://github.com/alexrivera/taskflow) | Full-stack Kanban with real-time drag-and-drop & JWT auth | React, Node, PostgreSQL |
| [🔍 AlgoViz](https://github.com/alexrivera/algoviz) | Interactive sorting & graph algorithm visualizer | TypeScript, React, Canvas |
| [🤖 StudyBot](https://github.com/alexrivera/studybot) | Discord flashcard quiz bot used by 3 study groups | Python, discord.py, SQLite |
| [🌐 PortfolioOS](https://github.com/alexrivera/portfolioos) | Portfolio styled as a desktop OS with terminal easter egg | React, Framer Motion |

---

## 📊 GitHub Stats

<p align="center">
  <img src="https://github-readme-stats.vercel.app/api?username=alexrivera&show_icons=true&theme=github_dark&hide_border=true" height="150"/>
  <img src="https://github-readme-stats.vercel.app/api/top-langs/?username=alexrivera&layout=compact&theme=github_dark&hide_border=true" height="150"/>
</p>

<p align="center">
  <img src="https://github-readme-streak-stats.herokuapp.com/?user=alexrivera&theme=github-dark-blue&hide_border=true" />
</p>

---

## 🤝 Connect With Me

[![LinkedIn](https://img.shields.io/badge/LinkedIn-0077B5?style=for-the-badge&logo=linkedin&logoColor=white)](https://linkedin.com/in/alexrivera)
[![Portfolio](https://img.shields.io/badge/Portfolio-000000?style=for-the-badge&logo=vercel&logoColor=white)](https://alexrivera.dev)
[![Twitter](https://img.shields.io/badge/Twitter-1DA1F2?style=for-the-badge&logo=twitter&logoColor=white)](https://twitter.com/alexrivera)
[![Resume](https://img.shields.io/badge/Resume-PDF-red?style=for-the-badge&logo=adobeacrobatreader&logoColor=white)](https://alexrivera.dev/resume.pdf)

---

<p align="center">
  <i>Last updated: June 2025 · Made with ♥ and too much caffeine</i>
</p>`;

document.getElementById('md-source').textContent = md;

function copyMarkdown() {
  navigator.clipboard.writeText(md).then(() => {
    const btn = document.querySelector('.copy-btn');
    btn.textContent = 'Copied!';
    btn.style.color = 'var(--green)';
    setTimeout(() => { btn.textContent = 'Copy'; btn.style.color = ''; }, 2000);
  });
}
</script>
</body>
</html>
