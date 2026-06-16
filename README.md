<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8"/>
<meta name="viewport" content="width=device-width, initial-scale=1.0"/>
<title>GitHub Profile – Michael Andrei Jugado</title>
<style>
@import url('https://fonts.googleapis.com/css2?family=JetBrains+Mono:wght@400;500;700&family=Inter:wght@300;400;500;600;700&display=swap');
:root{
  --bg:#0d1117;--surface:#161b22;--border:#21262d;--muted:#484f58;
  --text:#c9d1d9;--bright:#e6edf3;--accent:#58a6ff;--green:#3fb950;
  --purple:#bc8cff;--orange:#f0883e;--pink:#f778ba;--teal:#39d3c3;
}
*{box-sizing:border-box;margin:0;padding:0;}
body{background:#010409;display:flex;flex-direction:column;align-items:center;padding:2rem 1rem 4rem;font-family:'Inter',sans-serif;color:var(--text);min-height:100vh;}
.readme{width:100%;max-width:800px;background:var(--bg);border:1px solid var(--border);border-radius:6px;padding:2rem 2.25rem 2.5rem;line-height:1.65;}

/* HERO */
.hero{padding-bottom:1.6rem;margin-bottom:1.6rem;border-bottom:1px solid var(--border);}
.prompt{font-family:'JetBrains Mono',monospace;font-size:0.73rem;color:var(--muted);margin-bottom:0.6rem;letter-spacing:0.06em;}
.prompt span{color:var(--green);}
.hero h1{font-size:2rem;font-weight:700;color:var(--bright);line-height:1.15;margin-bottom:0.6rem;}
.hero h1 em{font-style:normal;color:var(--accent);}
.wave{display:inline-block;animation:wave 2.2s ease-in-out infinite;transform-origin:70% 70%;}
@keyframes wave{0%,100%{transform:rotate(0deg);}20%{transform:rotate(18deg);}40%{transform:rotate(-6deg);}60%{transform:rotate(12deg);}80%{transform:rotate(-3deg);}}
.hero-sub{font-size:0.93rem;color:var(--text);max-width:640px;line-height:1.7;margin-bottom:1.1rem;}
.hero-sub strong{color:var(--bright);font-weight:600;}
.mission{background:linear-gradient(90deg,rgba(88,166,255,0.08) 0%,rgba(57,211,195,0.06) 100%);border:1px solid rgba(88,166,255,0.2);border-left:3px solid var(--accent);border-radius:0 6px 6px 0;padding:0.7rem 1rem;margin-bottom:1.1rem;font-size:0.85rem;color:var(--text);font-style:italic;}
.mission strong{color:var(--accent);font-style:normal;}
.badges{display:flex;flex-wrap:wrap;gap:0.4rem;}
.badge{display:inline-flex;align-items:center;gap:0.3rem;font-family:'JetBrains Mono',monospace;font-size:0.7rem;padding:0.22rem 0.6rem;border-radius:100px;border:1px solid;font-weight:600;letter-spacing:0.01em;white-space:nowrap;}
.badge.blue{color:var(--accent);border-color:rgba(88,166,255,0.3);background:rgba(88,166,255,0.07);}
.badge.green{color:var(--green);border-color:rgba(63,185,80,0.3);background:rgba(63,185,80,0.07);}
.badge.teal{color:var(--teal);border-color:rgba(57,211,195,0.3);background:rgba(57,211,195,0.07);}
.badge.purple{color:var(--purple);border-color:rgba(188,140,255,0.3);background:rgba(188,140,255,0.07);}

/* SECTIONS */
.sec{margin-bottom:1.75rem;}
.sec-label{font-family:'JetBrains Mono',monospace;font-size:0.68rem;color:var(--muted);letter-spacing:0.14em;text-transform:uppercase;margin-bottom:0.85rem;display:flex;align-items:center;gap:0.5rem;}
.sec-label::after{content:'';flex:1;height:1px;background:var(--border);}

/* ABOUT */
.about-grid{display:grid;grid-template-columns:1fr 1fr;gap:0.55rem 1.5rem;}
.ai{font-size:0.87rem;display:flex;align-items:baseline;gap:0.4rem;}
.ai strong{color:var(--bright);font-weight:500;}
.ai a{color:var(--accent);text-decoration:none;}
.ai a:hover{text-decoration:underline;}

/* FOCUS */
.focus-grid{display:grid;grid-template-columns:repeat(3,1fr);gap:0.65rem;}
.focus-card{background:var(--surface);border:1px solid var(--border);border-radius:6px;padding:0.85rem 0.9rem;}
.fc-icon{font-size:1.3rem;margin-bottom:0.4rem;}
.fc-title{font-size:0.82rem;font-weight:600;color:var(--bright);margin-bottom:0.25rem;}
.fc-desc{font-size:0.75rem;color:var(--muted);line-height:1.5;}

/* STACK */
.stack-group{margin-bottom:0.85rem;}
.sg-title{font-size:0.74rem;color:var(--muted);margin-bottom:0.4rem;font-weight:500;}
.pill-row{display:flex;flex-wrap:wrap;gap:0.35rem;}
.pill{font-family:'JetBrains Mono',monospace;font-size:0.7rem;padding:0.2rem 0.55rem;border-radius:4px;background:var(--surface);border:1px solid var(--border);color:var(--text);transition:border-color .12s,color .12s;cursor:default;}
.pill:hover{border-color:var(--accent);color:var(--bright);}

/* PROJECTS */
.proj-grid{display:grid;grid-template-columns:1fr 1fr;gap:0.7rem;}
.proj-card{background:var(--surface);border:1px solid var(--border);border-radius:6px;padding:0.9rem 1rem;transition:border-color .15s;cursor:default;}
.proj-card:hover{border-color:var(--accent);}
.pt{font-size:0.87rem;font-weight:600;color:var(--accent);margin-bottom:0.3rem;}
.pd{font-size:0.79rem;color:var(--text);margin-bottom:0.55rem;line-height:1.5;}
.ptags{display:flex;flex-wrap:wrap;gap:0.28rem;}
.ptag{font-family:'JetBrains Mono',monospace;font-size:0.64rem;color:var(--muted);background:var(--bg);border:1px solid var(--border);padding:0.1rem 0.42rem;border-radius:3px;}

/* ROADMAP */
.lp-grid{display:grid;grid-template-columns:repeat(3,1fr);gap:0.65rem;}
.lp-card{background:var(--surface);border:1px solid var(--border);border-radius:6px;padding:0.8rem 0.9rem;}
.lp-status{font-family:'JetBrains Mono',monospace;font-size:0.62rem;padding:0.15rem 0.5rem;border-radius:100px;margin-bottom:0.4rem;display:inline-block;font-weight:700;letter-spacing:0.04em;}
.lp-status.done{background:rgba(63,185,80,0.12);color:var(--green);border:1px solid rgba(63,185,80,0.25);}
.lp-status.now{background:rgba(88,166,255,0.12);color:var(--accent);border:1px solid rgba(88,166,255,0.25);}
.lp-status.next{background:rgba(72,79,88,0.2);color:var(--muted);border:1px solid var(--border);}
.lp-title{font-size:0.82rem;font-weight:600;color:var(--bright);margin-bottom:0.2rem;}
.lp-desc{font-size:0.73rem;color:var(--muted);line-height:1.4;}

/* STATS */
.stats-row{display:grid;grid-template-columns:1fr 1fr;gap:0.7rem;}
.stat-card{background:var(--surface);border:1px solid var(--border);border-radius:6px;padding:0.85rem 1rem;}
.stat-title{font-size:0.68rem;color:var(--muted);font-weight:600;text-transform:uppercase;letter-spacing:0.06em;margin-bottom:0.6rem;}
.lbr{display:flex;align-items:center;gap:0.5rem;margin-bottom:0.32rem;}
.lname{font-family:'JetBrains Mono',monospace;font-size:0.7rem;width:76px;flex-shrink:0;color:var(--bright);}
.lbg{flex:1;height:6px;background:var(--border);border-radius:3px;overflow:hidden;}
.lbf{height:100%;border-radius:3px;}
.lpct{font-family:'JetBrains Mono',monospace;font-size:0.65rem;color:var(--muted);width:30px;text-align:right;flex-shrink:0;}
.si{display:flex;justify-content:space-between;align-items:baseline;margin-bottom:0.3rem;}
.sl{font-size:0.78rem;color:var(--muted);}
.sv{font-family:'JetBrains Mono',monospace;font-size:0.82rem;color:var(--bright);font-weight:600;}
.sv.green{color:var(--green);}.sv.orange{color:var(--orange);}

/* CONNECT */
.connect-row{display:flex;flex-wrap:wrap;gap:0.45rem;}
.cbtn{display:inline-flex;align-items:center;gap:0.38rem;font-size:0.8rem;padding:0.38rem 0.82rem;border-radius:6px;border:1px solid var(--border);background:var(--surface);color:var(--text);text-decoration:none;transition:border-color .13s,color .13s;cursor:pointer;}
.cbtn:hover{border-color:var(--accent);color:var(--bright);}

/* FOOTER */
.readme-footer{margin-top:1.5rem;padding-top:1rem;border-top:1px solid var(--border);font-family:'JetBrains Mono',monospace;font-size:0.7rem;color:var(--muted);display:flex;justify-content:space-between;align-items:center;flex-wrap:wrap;gap:0.4rem;}

/* COPY */
.copy-wrap{width:100%;max-width:800px;margin-top:1.5rem;}
.copy-area{background:var(--surface);border:1px solid var(--border);border-radius:6px;overflow:hidden;}
.copy-hdr{display:flex;align-items:center;justify-content:space-between;padding:0.55rem 1rem;border-bottom:1px solid var(--border);background:var(--bg);}
.copy-hdr span{font-family:'JetBrains Mono',monospace;font-size:0.7rem;color:var(--muted);}
.copy-btn{font-family:'JetBrains Mono',monospace;font-size:0.7rem;padding:0.2rem 0.7rem;border-radius:4px;border:1px solid var(--border);background:var(--surface);color:var(--accent);cursor:pointer;}
.copy-btn:hover{background:rgba(88,166,255,0.1);}
.code-block{padding:1rem;font-family:'JetBrains Mono',monospace;font-size:0.7rem;color:var(--text);white-space:pre-wrap;word-break:break-all;max-height:300px;overflow-y:auto;line-height:1.7;}

@media(max-width:580px){
  .about-grid,.proj-grid,.stats-row,.focus-grid,.lp-grid{grid-template-columns:1fr;}
  .readme{padding:1.25rem;}
  .hero h1{font-size:1.5rem;}
}
</style>
</head>
<body>

<div class="readme">

  <!-- HERO -->
  <div class="hero">
    <div class="prompt"><span>~/usls-cs $</span> cat profile.md</div>
    <h1><span class="wave">👋</span> Hi, I'm <em>Michael Andrei Jugado</em></h1>
    <p class="hero-sub">
      <strong>Computer Science student at the University of St. La Salle</strong>, Bacolod.
      I'm on a deliberate path toward software engineering — writing code that doesn't just run today,
      but <strong>scales, holds up under load, and makes sense to the next developer who touches it</strong>.
    </p>
    <div class="mission">
      <strong>Mission:</strong> Graduate as a competent software engineer who produces scalable systems —
      clean APIs, resilient backends, and software that can grow without collapsing under its own weight.
    </div>
    <div class="badges">
      <span class="badge blue">🎓 BS Computer Science · USLS Bacolod</span>
      <span class="badge green">🟢 Open to Internships · 2025</span>
      <span class="badge teal">⚙️ Building scalable systems</span>
      <span class="badge purple">📍 Bacolod City, PH</span>
    </div>
  </div>

  <!-- ABOUT -->
  <div class="sec">
    <div class="sec-label">About</div>
    <div class="about-grid">
      <div class="ai">🔭 Building <strong>a full-stack learning module system</strong></div>
      <div class="ai">🌱 Studying <strong>System Design, Web Dev & LLMs</strong></div>
      <div class="ai">🏫 Student at <strong>University of St. La Salle, Bacolod</strong></div>
      <div class="ai">🤝 Open to <strong>open-source collaboration</strong></div>
      <div class="ai">⚙️ Interested in <strong>backend architecture & scalable APIs</strong></div>
      <div class="ai">💬 Ask me about <strong>Python, Java, or React</strong></div>
      <div class="ai">📫 Email: <a href="mailto:jugadomichael@gmail.com">jugadomichael@gmail.com</a></div>
      <div class="ai">⚡ Believe that <strong>competence compounds — ship, learn, improve</strong></div>
    </div>
  </div>

  <!-- ENGINEERING FOCUS -->
  <div class="sec">
    <div class="sec-label">Engineering Focus</div>
    <div class="focus-grid">
      <div class="focus-card">
        <div class="fc-icon">🏗️</div>
        <div class="fc-title">Scalable Backends</div>
        <div class="fc-desc">REST & async APIs built for growth — rate limiting, pagination, and graceful degradation under pressure.</div>
      </div>
      <div class="focus-card">
        <div class="fc-icon">🗄️</div>
        <div class="fc-title">Database Design</div>
        <div class="fc-desc">Schema modeling, indexing strategies, and knowing when SQL, NoSQL, or a cache is the right call.</div>
      </div>
      <div class="focus-card">
        <div class="fc-icon">🤖</div>
        <div class="fc-title">LLM Integration</div>
        <div class="fc-desc">Exploring how large language models slot into real products — prompt design, retrieval, and practical constraints.</div>
      </div>
    </div>
  </div>

  <!-- TECH STACK -->
  <div class="sec">
    <div class="sec-label">Tech Stack</div>
    <div class="stack-group">
      <div class="sg-title">Languages</div>
      <div class="pill-row">
        <span class="pill">Python</span><span class="pill">Java</span><span class="pill">JavaScript</span>
        <span class="pill">TypeScript</span><span class="pill">C++</span><span class="pill">C#</span>
        <span class="pill">SQL</span><span class="pill">Bash</span>
      </div>
    </div>
    <div class="stack-group">
      <div class="sg-title">Frameworks & Libraries</div>
      <div class="pill-row">
        <span class="pill">React</span><span class="pill">Next.js</span><span class="pill">Node.js</span>
        <span class="pill">Express</span><span class="pill">Spring Boot</span><span class="pill">FastAPI</span>
        <span class="pill">Tailwind CSS</span><span class="pill">Shadcn/ui</span>
      </div>
    </div>
    <div class="stack-group">
      <div class="sg-title">Tools & Platforms</div>
      <div class="pill-row">
        <span class="pill">Git</span><span class="pill">Docker</span><span class="pill">PostgreSQL</span>
        <span class="pill">MongoDB</span><span class="pill">Convex</span><span class="pill">Clerk</span>
        <span class="pill">Vercel</span><span class="pill">VS Code</span>
        <span class="pill">AWS (learning)</span><span class="pill">Azure (learning)</span>
      </div>
    </div>
  </div>

  <!-- PROJECTS -->
  <div class="sec">
    <div class="sec-label">Featured Projects</div>
    <div class="proj-grid">
      <div class="proj-card">
        <div class="pt">📋 Learning Module System</div>
        <div class="pd">Full-stack onboarding platform for new employees — structured learning paths, progress tracking, and role-based access control.</div>
        <div class="ptags">
          <span class="ptag">Next.js</span><span class="ptag">React</span><span class="ptag">Shadcn/ui</span>
          <span class="ptag">Clerk</span><span class="ptag">Convex</span><span class="ptag">Vercel</span>
        </div>
      </div>
      <div class="proj-card">
        <div class="pt">🚧 More on the way</div>
        <div class="pd">Currently designing a backend-heavy project to put system design concepts into practice. Watch this space.</div>
        <div class="ptags">
          <span class="ptag">In Progress</span>
        </div>
      </div>
    </div>
  </div>

  <!-- LEARNING ROADMAP -->
  <div class="sec">
    <div class="sec-label">Learning Roadmap</div>
    <div class="lp-grid">
      <div class="lp-card">
        <div class="lp-status done">✓ Done</div>
        <div class="lp-title">Web Development</div>
        <div class="lp-desc">React, Next.js, REST APIs, full-stack deployment pipelines.</div>
      </div>
      <div class="lp-card">
        <div class="lp-status done">✓ Done</div>
        <div class="lp-title">Data Structures & Algorithms</div>
        <div class="lp-desc">Trees, graphs, dynamic programming, complexity analysis.</div>
      </div>
      <div class="lp-card">
        <div class="lp-status now">→ Now</div>
        <div class="lp-title">System Design</div>
        <div class="lp-desc">CAP theorem, load balancing, caching layers, horizontal scaling patterns.</div>
      </div>
      <div class="lp-card">
        <div class="lp-status now">→ Now</div>
        <div class="lp-title">LLMs in Production</div>
        <div class="lp-desc">Prompt engineering, RAG pipelines, and integrating AI into real systems.</div>
      </div>
      <div class="lp-card">
        <div class="lp-status next">↑ Next</div>
        <div class="lp-title">Cloud Infrastructure</div>
        <div class="lp-desc">AWS & Azure core services, containers, CI/CD at scale.</div>
      </div>
      <div class="lp-card">
        <div class="lp-status next">↑ Next</div>
        <div class="lp-title">Distributed Systems</div>
        <div class="lp-desc">Consensus, replication, eventual consistency, fault tolerance.</div>
      </div>
    </div>
  </div>

  <!-- STATS -->
  <div class="sec">
    <div class="sec-label">Stats</div>
    <div class="stats-row">
      <div class="stat-card">
        <div class="stat-title">Top Languages</div>
        <div class="lbr"><span class="lname">Python</span><div class="lbg"><div class="lbf" style="width:72%;background:#3572A5;"></div></div><span class="lpct">72%</span></div>
        <div class="lbr"><span class="lname">JavaScript</span><div class="lbg"><div class="lbf" style="width:55%;background:#f1e05a;"></div></div><span class="lpct">55%</span></div>
        <div class="lbr"><span class="lname">Java</span><div class="lbg"><div class="lbf" style="width:40%;background:#b07219;"></div></div><span class="lpct">40%</span></div>
        <div class="lbr"><span class="lname">TypeScript</span><div class="lbg"><div class="lbf" style="width:28%;background:#2b7489;"></div></div><span class="lpct">28%</span></div>
        <div class="lbr"><span class="lname">C++</span><div class="lbg"><div class="lbf" style="width:16%;background:#f34b7d;"></div></div><span class="lpct">16%</span></div>
      </div>
      <div class="stat-card">
        <div class="stat-title">Activity</div>
        <div class="si"><span class="sl">Total Commits (2024)</span><span class="sv green">847</span></div>
        <div class="si"><span class="sl">Current Streak</span><span class="sv orange">🔥 14 days</span></div>
        <div class="si"><span class="sl">Public Repos</span><span class="sv">23</span></div>
        <div class="si"><span class="sl">Pull Requests</span><span class="sv">38</span></div>
        <div class="si"><span class="sl">Issues Closed</span><span class="sv">61</span></div>
      </div>
    </div>
  </div>

  <!-- CONNECT -->
  <div class="sec">
    <div class="sec-label">Connect</div>
    <div class="connect-row">
      <a class="cbtn" href="https://www.linkedin.com/in/m-a-jugado/" target="_blank">💼 LinkedIn</a>
      <a class="cbtn" href="https://www.facebook.com/michaelandrei.jugado/" target="_blank">🔵 Facebook</a>
      <a class="cbtn" href="mailto:jugadomichael@gmail.com">✉️ jugadomichael@gmail.com</a>
      <a class="cbtn" href="#">🌐 Portfolio (TBA)</a>
      <a class="cbtn" href="#">📄 Resume (TBA)</a>
    </div>
  </div>

  <div class="readme-footer">
    <span>USLS · Bacolod City, PH · BS Computer Science</span>
    <span>building toward software engineering, one system at a time</span>
  </div>

</div>

<!-- MARKDOWN -->
<div class="copy-wrap">
  <div class="copy-area">
    <div class="copy-hdr">
      <span>README.md — paste into your michaelandreijugado/michaelandreijugado repo</span>
      <button class="copy-btn" onclick="copyMd()">Copy</button>
    </div>
    <div class="code-block" id="mdsrc"></div>
  </div>
</div>

<script>
const md = `<!-- GitHub Profile README — Michael Andrei Jugado -->

<h1 align="center">Hi 👋, I'm Michael Andrei Jugado</h1>

<p align="center">
  Computer Science student at the <strong>University of St. La Salle</strong>, Bacolod City.<br/>
  Building toward software engineering — not just code that runs, but systems that scale.
</p>

<p align="center">
  <img src="https://komarev.com/ghpvc/?username=yourgithubusername&label=Profile+Views&color=0e75b6&style=flat" />
  <img src="https://img.shields.io/badge/BS%20CS-USLS%20Bacolod-58a6ff?style=flat" />
  <img src="https://img.shields.io/badge/Open%20to-Internships%202025-3fb950?style=flat" />
  <img src="https://img.shields.io/badge/Focus-Scalable%20Systems-39d3c3?style=flat" />
</p>

---

> **Mission:** Graduate as a competent software engineer who produces scalable systems —
> clean APIs, resilient backends, and software that can grow without collapsing under its own weight.

---

## 👾 About Me

- 🎓 Studying **Computer Science** at the **University of St. La Salle**, Bacolod City, PH
- 🔭 Currently building a **full-stack learning module system** for employee onboarding
- 🌱 Deep-diving into **System Design, Web Development & LLMs**
- ⚙️ Interested in **backend architecture, scalable APIs, and AI integration**
- 🤝 Open to collaborate on **open-source projects**
- 💬 Ask me about **Python, Java, or React**
- 📫 Reach me at **jugadomichael@gmail.com**
- ⚡ I believe that competence compounds — ship, learn, improve

---

## 🏗️ Engineering Focus

| Area | What I Practice |
|------|-----------------|
| **Scalable Backends** | REST & async APIs with rate limiting, pagination, and graceful degradation |
| **Database Design** | Schema modeling, indexing strategies, SQL vs NoSQL tradeoffs |
| **LLM Integration** | Prompt engineering, RAG pipelines, integrating AI into real products |

---

## 🛠️ Tech Stack

**Languages**
\`Python\` \`Java\` \`JavaScript\` \`TypeScript\` \`C++\` \`C#\` \`SQL\` \`Bash\`

**Frameworks & Libraries**
\`React\` \`Next.js\` \`Node.js\` \`Express\` \`Spring Boot\` \`FastAPI\` \`Tailwind CSS\` \`Shadcn/ui\`

**Tools & Platforms**
\`Git\` \`Docker\` \`PostgreSQL\` \`MongoDB\` \`Convex\` \`Clerk\` \`Vercel\` \`VS Code\` \`AWS (learning)\` \`Azure (learning)\`

---

## 🚀 Featured Projects

| Project | Description | Stack |
|---------|-------------|-------|
| [📋 Learning Module System](https://github.com/yourgithubusername/learning-module-system) | Full-stack onboarding platform for new employees with structured learning paths and role-based access | Next.js, React, Shadcn/ui, Clerk, Convex, Vercel |

*More projects incoming — currently designing a backend-heavy system to put system design concepts into practice.*

---

## 📍 Learning Roadmap

| Status | Topic |
|--------|-------|
| ✅ Done | Web Development — React, Next.js, REST APIs, full-stack deployment |
| ✅ Done | Data Structures & Algorithms — trees, graphs, DP, complexity |
| 🔵 Now  | System Design — CAP theorem, load balancing, caching, horizontal scaling |
| 🔵 Now  | LLMs in Production — prompt engineering, RAG, AI integration |
| ⬜ Next | Cloud Infrastructure — AWS & Azure core services, containers, CI/CD |
| ⬜ Next | Distributed Systems — consensus, replication, eventual consistency |

---

## 📊 GitHub Stats

<p align="center">
  <img src="https://github-readme-stats.vercel.app/api?username=yourgithubusername&show_icons=true&theme=github_dark&hide_border=true" height="150"/>
  <img src="https://github-readme-stats.vercel.app/api/top-langs/?username=yourgithubusername&layout=compact&theme=github_dark&hide_border=true" height="150"/>
</p>

<p align="center">
  <img src="https://github-readme-streak-stats.herokuapp.com/?user=yourgithubusername&theme=github-dark-blue&hide_border=true"/>
</p>

---

## 🤝 Connect

[![LinkedIn](https://img.shields.io/badge/LinkedIn-0077B5?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/m-a-jugado/)
[![Facebook](https://img.shields.io/badge/Facebook-1877F2?style=for-the-badge&logo=facebook&logoColor=white)](https://www.facebook.com/michaelandrei.jugado/)
[![Email](https://img.shields.io/badge/Gmail-EA4335?style=for-the-badge&logo=gmail&logoColor=white)](mailto:jugadomichael@gmail.com)
[![Portfolio](https://img.shields.io/badge/Portfolio-000000?style=for-the-badge&logo=vercel&logoColor=white)](https://yourportfolio.dev)
[![Resume](https://img.shields.io/badge/Resume-PDF-red?style=for-the-badge&logo=adobeacrobatreader&logoColor=white)](https://yourportfolio.dev/resume.pdf)

---

<p align="center">
  <i>USLS · Bacolod City, PH · building toward software engineering, one system at a time</i>
</p>`;

document.getElementById('mdsrc').textContent = md;
function copyMd(){
  navigator.clipboard.writeText(md).then(()=>{
    const b=document.querySelector('.copy-btn');
    b.textContent='Copied!';b.style.color='var(--green)';
    setTimeout(()=>{b.textContent='Copy';b.style.color='';},2000);
  });
}
</script>
</body>
</html>
