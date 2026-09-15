<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />

  <title>ThunderDoesDev | Backend Developer & IT Technician</title>

  <meta
    name="description"
    content="ThunderDoesDev — Backend Developer, Certified IT Technician, Discord Developer and Infrastructure Builder from Australia."
  />

  <meta name="theme-color" content="#00ffff" />

  <style>
    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
    }

    :root {
      --bg: #05070b;
      --bg-secondary: #0a0f18;
      --card: rgba(13, 17, 23, 0.78);
      --card-solid: #0d1117;
      --cyan: #00ffff;
      --cyan-soft: #5cfaff;
      --blue: #0077ff;
      --purple: #7c3aed;
      --green: #00ff9c;
      --red: #ff4d67;
      --yellow: #facc15;
      --text: #f5f7fa;
      --muted: #8b949e;
      --border: rgba(0, 255, 255, 0.18);
      --shadow: 0 0 30px rgba(0, 255, 255, 0.09);
      --font:
        Inter,
        system-ui,
        -apple-system,
        BlinkMacSystemFont,
        "Segoe UI",
        sans-serif;
      --mono:
        "SFMono-Regular",
        Consolas,
        "Liberation Mono",
        Menlo,
        monospace;
    }

    html {
      scroll-behavior: smooth;
    }

    body {
      min-height: 100vh;
      background:
        radial-gradient(
          circle at 10% 10%,
          rgba(0, 255, 255, 0.08),
          transparent 30%
        ),
        radial-gradient(
          circle at 90% 20%,
          rgba(124, 58, 237, 0.1),
          transparent 30%
        ),
        radial-gradient(
          circle at 50% 90%,
          rgba(0, 119, 255, 0.08),
          transparent 30%
        ),
        var(--bg);

      color: var(--text);
      font-family: var(--font);
      line-height: 1.6;
      overflow-x: hidden;
    }

    body::before {
      content: "";
      position: fixed;
      inset: 0;
      pointer-events: none;
      opacity: 0.1;
      z-index: 999;
      background-image:
        linear-gradient(rgba(255,255,255,0.02) 1px, transparent 1px),
        linear-gradient(90deg, rgba(255,255,255,0.02) 1px, transparent 1px);
      background-size: 40px 40px;
    }

    a {
      color: inherit;
      text-decoration: none;
    }

    img {
      max-width: 100%;
    }

    .container {
      width: min(1200px, calc(100% - 32px));
      margin: 0 auto;
    }

    .section {
      padding: 100px 0;
      position: relative;
    }

    .section-title {
      font-size: clamp(2rem, 5vw, 3.5rem);
      margin-bottom: 16px;
      letter-spacing: -0.04em;
    }

    .section-title span {
      color: var(--cyan);
      text-shadow: 0 0 18px rgba(0, 255, 255, 0.35);
    }

    .section-subtitle {
      color: var(--muted);
      max-width: 760px;
      margin-bottom: 40px;
      font-size: 1.05rem;
    }

    .gradient-text {
      background: linear-gradient(
        90deg,
        var(--cyan),
        var(--blue),
        var(--purple)
      );
      -webkit-background-clip: text;
      background-clip: text;
      color: transparent;
    }

    /* =========================
       NAV
    ========================== */

    nav {
      position: fixed;
      top: 0;
      left: 0;
      right: 0;
      z-index: 1000;
      background: rgba(5, 7, 11, 0.72);
      border-bottom: 1px solid rgba(255,255,255,0.05);
      backdrop-filter: blur(18px);
    }

    .nav-inner {
      width: min(1200px, calc(100% - 32px));
      margin: 0 auto;
      min-height: 72px;
      display: flex;
      align-items: center;
      justify-content: space-between;
      gap: 20px;
    }

    .brand {
      font-family: var(--mono);
      font-weight: 800;
      font-size: 1.1rem;
      letter-spacing: 0.05em;
      color: var(--cyan);
    }

    .nav-links {
      display: flex;
      align-items: center;
      gap: 24px;
      color: #c9d1d9;
      font-size: 0.95rem;
    }

    .nav-links a {
      transition: 0.2s ease;
    }

    .nav-links a:hover {
      color: var(--cyan);
    }

    .nav-button {
      border: 1px solid rgba(0,255,255,0.35);
      padding: 9px 15px;
      border-radius: 10px;
      color: var(--cyan) !important;
      background: rgba(0,255,255,0.05);
    }

    /* =========================
       HERO
    ========================== */

    .hero {
      min-height: 100vh;
      display: flex;
      align-items: center;
      padding: 130px 0 70px;
      position: relative;
    }

    .hero-grid {
      display: grid;
      grid-template-columns: 1.1fr 0.9fr;
      gap: 60px;
      align-items: center;
    }

    .eyebrow {
      display: inline-flex;
      align-items: center;
      gap: 10px;
      padding: 8px 14px;
      border: 1px solid var(--border);
      background: rgba(0,255,255,0.04);
      color: var(--cyan);
      border-radius: 999px;
      font-family: var(--mono);
      font-size: 0.85rem;
      margin-bottom: 22px;
    }

    .online-dot {
      width: 8px;
      height: 8px;
      background: var(--green);
      border-radius: 50%;
      box-shadow: 0 0 12px var(--green);
      animation: pulse 1.5s infinite;
    }

    @keyframes pulse {
      0%, 100% {
        opacity: 1;
      }
      50% {
        opacity: 0.35;
      }
    }

    h1 {
      font-size: clamp(4rem, 10vw, 8rem);
      line-height: 0.9;
      letter-spacing: -0.07em;
      margin-bottom: 24px;
      font-weight: 900;
    }

    .hero-description {
      max-width: 760px;
      color: #b7c0ca;
      font-size: clamp(1rem, 2vw, 1.18rem);
      margin-bottom: 34px;
    }

    .hero-description strong {
      color: #fff;
    }

    .typing-wrap {
      margin: 28px 0 34px;
      min-height: 34px;
      font-family: var(--mono);
      font-size: clamp(1rem, 2.5vw, 1.25rem);
      color: var(--cyan);
    }

    .typing-prefix {
      color: var(--green);
      margin-right: 8px;
    }

    .cursor {
      display: inline-block;
      width: 9px;
      height: 1.2em;
      background: var(--cyan);
      vertical-align: middle;
      margin-left: 4px;
      animation: blink 0.85s infinite;
    }

    @keyframes blink {
      50% {
        opacity: 0;
      }
    }

    .hero-actions {
      display: flex;
      flex-wrap: wrap;
      gap: 12px;
    }

    .button {
      display: inline-flex;
      align-items: center;
      justify-content: center;
      gap: 9px;
      padding: 13px 18px;
      border-radius: 12px;
      font-weight: 700;
      border: 1px solid transparent;
      transition:
        transform 0.2s ease,
        border-color 0.2s ease,
        box-shadow 0.2s ease,
        background 0.2s ease;
    }

    .button:hover {
      transform: translateY(-2px);
    }

    .button-primary {
      color: #001014;
      background: linear-gradient(90deg, var(--cyan), #50e9ff);
      box-shadow: 0 0 25px rgba(0,255,255,0.2);
    }

    .button-secondary {
      color: #fff;
      background: rgba(255,255,255,0.04);
      border-color: rgba(255,255,255,0.1);
    }

    .button-secondary:hover {
      border-color: var(--cyan);
      box-shadow: 0 0 20px rgba(0,255,255,0.08);
    }

    /* =========================
       TERMINAL
    ========================== */

    .terminal {
      background: rgba(3, 7, 12, 0.88);
      border: 1px solid rgba(0,255,255,0.18);
      border-radius: 18px;
      overflow: hidden;
      box-shadow:
        0 30px 70px rgba(0,0,0,0.45),
        0 0 40px rgba(0,255,255,0.07);
      transform: perspective(1200px) rotateY(-3deg);
    }

    .terminal-bar {
      display: flex;
      align-items: center;
      gap: 8px;
      padding: 14px 16px;
      background: rgba(255,255,255,0.035);
      border-bottom: 1px solid rgba(255,255,255,0.05);
    }

    .terminal-dot {
      width: 12px;
      height: 12px;
      border-radius: 50%;
    }

    .dot-red { background: #ff5f56; }
    .dot-yellow { background: #ffbd2e; }
    .dot-green { background: #27c93f; }

    .terminal-title {
      margin-left: auto;
      margin-right: auto;
      font-family: var(--mono);
      color: #7d8590;
      font-size: 0.8rem;
      transform: translateX(-18px);
    }

    .terminal-body {
      padding: 24px;
      font-family: var(--mono);
      font-size: 0.9rem;
      min-height: 360px;
      color: #d4d7dc;
    }

    .prompt {
      color: var(--cyan);
    }

    .command {
      color: #fff;
    }

    .output {
      color: var(--muted);
      margin: 3px 0 14px;
    }

    .success {
      color: var(--green);
    }

    .warning {
      color: var(--yellow);
    }

    /* =========================
       CARDS
    ========================== */

    .grid {
      display: grid;
      gap: 24px;
    }

    .grid-2 {
      grid-template-columns: repeat(2, minmax(0, 1fr));
    }

    .grid-3 {
      grid-template-columns: repeat(3, minmax(0, 1fr));
    }

    .card {
      position: relative;
      border: 1px solid rgba(255,255,255,0.07);
      background:
        linear-gradient(
          145deg,
          rgba(255,255,255,0.04),
          rgba(255,255,255,0.015)
        );
      border-radius: 18px;
      padding: 28px;
      overflow: hidden;
      transition:
        transform 0.25s ease,
        border-color 0.25s ease,
        box-shadow 0.25s ease;
    }

    .card::before {
      content: "";
      position: absolute;
      width: 140px;
      height: 140px;
      background: var(--cyan);
      filter: blur(100px);
      opacity: 0.05;
      right: -50px;
      top: -50px;
      pointer-events: none;
    }

    .card:hover {
      transform: translateY(-5px);
      border-color: rgba(0,255,255,0.25);
      box-shadow: var(--shadow);
    }

    .card-icon {
      font-size: 2rem;
      margin-bottom: 16px;
    }

    .card h3 {
      font-size: 1.35rem;
      margin-bottom: 10px;
    }

    .card p {
      color: var(--muted);
    }

    /* =========================
       TECH STACK
    ========================== */

    .stack-group {
      margin-top: 34px;
    }

    .stack-group h3 {
      color: #fff;
      margin-bottom: 16px;
      font-size: 1.05rem;
      font-family: var(--mono);
    }

    .badges {
      display: flex;
      flex-wrap: wrap;
      gap: 10px;
    }

    .badge {
      display: inline-flex;
      align-items: center;
      gap: 8px;
      padding: 10px 14px;
      border-radius: 10px;
      background: rgba(13,17,23,0.9);
      border: 1px solid rgba(0,255,255,0.13);
      color: #dbe2e8;
      font-size: 0.92rem;
      font-weight: 650;
      transition: 0.2s ease;
    }

    .badge:hover {
      color: var(--cyan);
      border-color: rgba(0,255,255,0.35);
      transform: translateY(-2px);
    }

    /* =========================
       PROJECTS
    ========================== */

    .project {
      min-height: 320px;
      display: flex;
      flex-direction: column;
    }

    .project-top {
      display: flex;
      justify-content: space-between;
      gap: 16px;
      margin-bottom: 12px;
    }

    .project-name {
      font-size: 1.5rem;
      font-weight: 800;
    }

    .project-tag {
      font-family: var(--mono);
      font-size: 0.75rem;
      color: var(--cyan);
      border: 1px solid rgba(0,255,255,0.2);
      border-radius: 999px;
      padding: 6px 10px;
      height: fit-content;
      white-space: nowrap;
    }

    .project p {
      margin-bottom: 20px;
    }

    .project ul {
      padding-left: 18px;
      color: #aeb7c1;
      margin-bottom: 22px;
    }

    .project-stack {
      margin-top: auto;
      display: flex;
      gap: 8px;
      flex-wrap: wrap;
    }

    .mini-tag {
      padding: 6px 9px;
      border-radius: 8px;
      background: rgba(0,119,255,0.08);
      color: #81c7ff;
      font-size: 0.78rem;
      font-family: var(--mono);
    }

    /* =========================
       ARCHITECTURE
    ========================== */

    .architecture {
      background: #05080d;
      border: 1px solid rgba(0,255,255,0.15);
      border-radius: 18px;
      padding: 28px;
      overflow-x: auto;
      box-shadow: inset 0 0 30px rgba(0,255,255,0.02);
    }

    .architecture pre {
      color: #d5dde5;
      font-family: var(--mono);
      font-size: clamp(0.68rem, 1.35vw, 0.95rem);
      line-height: 1.5;
      min-width: 720px;
    }

    .architecture .cyan {
      color: var(--cyan);
    }

    /* =========================
       PHILOSOPHY
    ========================== */

    .compare-table {
      width: 100%;
      border-collapse: collapse;
      overflow: hidden;
      border-radius: 16px;
      border: 1px solid rgba(255,255,255,0.08);
    }

    .compare-table th,
    .compare-table td {
      padding: 16px 20px;
      text-align: left;
      border-bottom: 1px solid rgba(255,255,255,0.05);
    }

    .compare-table th {
      background: rgba(255,255,255,0.04);
      font-family: var(--mono);
      color: var(--cyan);
    }

    .compare-table td {
      color: #aeb7c1;
    }

    /* =========================
       STATS
    ========================== */

    .stats-grid {
      display: grid;
      grid-template-columns: repeat(3, 1fr);
      gap: 18px;
      margin-top: 32px;
    }

    .stat {
      text-align: center;
      padding: 26px 18px;
      border-radius: 16px;
      border: 1px solid rgba(0,255,255,0.13);
      background: rgba(13,17,23,0.65);
    }

    .stat-value {
      display: block;
      font-size: 2rem;
      font-weight: 900;
      color: var(--cyan);
    }

    .stat-label {
      color: var(--muted);
      font-size: 0.9rem;
    }

    .github-images {
      display: grid;
      grid-template-columns: repeat(2, minmax(0, 1fr));
      gap: 18px;
      margin-top: 30px;
    }

    .github-images img {
      width: 100%;
      border-radius: 14px;
    }

    /* =========================
       CONTACT
    ========================== */

    .contact-box {
      padding: 50px;
      text-align: center;
      border: 1px solid rgba(0,255,255,0.18);
      border-radius: 24px;
      background:
        radial-gradient(
          circle at center,
          rgba(0,255,255,0.07),
          transparent 55%
        ),
        rgba(13,17,23,0.55);
    }

    .contact-box h2 {
      font-size: clamp(2rem, 6vw, 4rem);
      margin-bottom: 14px;
    }

    .contact-box p {
      color: var(--muted);
      max-width: 680px;
      margin: 0 auto 30px;
    }

    /* =========================
       FOOTER
    ========================== */

    footer {
      padding: 40px 0 50px;
      text-align: center;
      border-top: 1px solid rgba(255,255,255,0.05);
      color: var(--muted);
      font-size: 0.9rem;
    }

    footer strong {
      color: var(--cyan);
    }

    /* =========================
       MOBILE
    ========================== */

    @media (max-width: 900px) {
      .hero-grid,
      .grid-2,
      .grid-3,
      .github-images {
        grid-template-columns: 1fr;
      }

      .hero {
        min-height: auto;
      }

      .terminal {
        transform: none;
      }

      .nav-links a:not(.nav-button) {
        display: none;
      }

      .stats-grid {
        grid-template-columns: 1fr;
      }
    }

    @media (max-width: 600px) {
      .section {
        padding: 75px 0;
      }

      .nav-inner {
        min-height: 64px;
      }

      .brand {
        font-size: 0.9rem;
      }

      h1 {
        font-size: 4rem;
      }

      .hero-actions {
        flex-direction: column;
      }

      .button {
        width: 100%;
      }

      .terminal-body {
        font-size: 0.76rem;
        padding: 18px;
      }

      .card {
        padding: 22px;
      }

      .contact-box {
        padding: 34px 20px;
      }
    }
  </style>
</head>

<body>

  <!-- =========================
       NAVIGATION
  ========================== -->

  <nav>
    <div class="nav-inner">
      <a href="#home" class="brand">
        thunder@dev:~$
      </a>

      <div class="nav-links">
        <a href="#about">About</a>
        <a href="#stack">Stack</a>
        <a href="#projects">Projects</a>
        <a href="#infra">Infrastructure</a>
        <a href="#stats">GitHub</a>
        <a href="#contact" class="nav-button">Connect</a>
      </div>
    </div>
  </nav>

  <!-- =========================
       HERO
  ========================== -->

  <header class="hero" id="home">
    <div class="container hero-grid">

      <div>
        <div class="eyebrow">
          <span class="online-dot"></span>
          SYSTEM ONLINE
        </div>

        <h1 class="gradient-text">THUNDER</h1>

        <div class="typing-wrap">
          <span class="typing-prefix">&gt;</span>
          <span id="typing"></span>
          <span class="cursor"></span>
        </div>

        <p class="hero-description">
          I'm <strong>Thunder</strong>, a self-taught
          <strong>backend developer</strong> and
          <strong>certified IT Technician</strong> from Australia.
          I build APIs, Discord systems, web platforms, automation,
          Linux infrastructure and self-hosted services.
        </p>

        <div class="hero-actions">
          <a
            href="https://thunderdoesdev.gg"
            class="button button-primary"
            target="_blank"
            rel="noopener"
          >
            Visit Website
          </a>

          <a
            href="https://github.com/ThunderDoesDev"
            class="button button-secondary"
            target="_blank"
            rel="noopener"
          >
            GitHub
          </a>

          <a
            href="https://discord.gg/thunderdoesdev"
            class="button button-secondary"
            target="_blank"
            rel="noopener"
          >
            Discord
          </a>
        </div>
      </div>

      <div class="terminal">
        <div class="terminal-bar">
          <span class="terminal-dot dot-red"></span>
          <span class="terminal-dot dot-yellow"></span>
          <span class="terminal-dot dot-green"></span>

          <span class="terminal-title">
            thunder@production
          </span>
        </div>

        <div class="terminal-body">
          <div>
            <span class="prompt">thunder@dev:~$</span>
            <span class="command"> whoami</span>
          </div>

          <div class="output">
            Thunder<br>
            Backend Developer<br>
            Certified IT Technician
          </div>

          <div>
            <span class="prompt">thunder@dev:~$</span>
            <span class="command"> cat skills.txt</span>
          </div>

          <div class="output">
            backend_development<br>
            discord_systems<br>
            rest_apis<br>
            linux_infrastructure<br>
            nginx<br>
            mysql<br>
            cloudflare<br>
            automation<br>
            self_hosting
          </div>

          <div>
            <span class="prompt">thunder@dev:~$</span>
            <span class="command"> systemctl status thunder</span>
          </div>

          <div class="output">
            <span class="success">● active (running)</span><br>
            uptime: 10+ years<br>
            coffee.service:
            <span class="warning">required</span>
          </div>

          <div>
            <span class="prompt">thunder@dev:~$</span>
            <span class="command"> _</span>
          </div>
        </div>
      </div>

    </div>
  </header>

  <!-- =========================
       ABOUT
  ========================== -->

  <section class="section" id="about">
    <div class="container">

      <h2 class="section-title">
        SYSTEM://<span>ABOUT</span>
      </h2>

      <p class="section-subtitle">
        I don't just want an application to work. I want to understand the
        entire system keeping it alive.
      </p>

      <div class="grid grid-2">

        <article class="card">
          <div class="card-icon">⚡</div>

          <h3>Who I Am</h3>

          <p>
            I'm a 32-year-old self-taught backend developer from Australia
            with more than a decade of experience around technology and
            development.
          </p>

          <br>

          <p>
            My background started heavily around Discord bot development
            before expanding into complete backend platforms, servers,
            networking, APIs, databases and production infrastructure.
          </p>
        </article>

        <article class="card">
          <div class="card-icon">🛠️</div>

          <h3>Certified IT Technician</h3>

          <p>
            I hold a Certificate III in Information Technology, giving me a
            professional IT foundation alongside my development experience.
          </p>

          <br>

          <p>
            I enjoy working across both software and infrastructure instead
            of treating them as completely separate worlds.
          </p>
        </article>

        <article class="card">
          <div class="card-icon">🤖</div>

          <h3>Discord Development</h3>

          <p>
            Discord development has been one of my longest-running areas of
            experience, covering bots, automation, integrations,
            administration systems and server tooling.
          </p>
        </article>

        <article class="card">
          <div class="card-icon">🖥️</div>

          <h3>Infrastructure</h3>

          <p>
            I regularly work with Ubuntu servers, NGINX, Cloudflare,
            DNS, SSL/TLS, MySQL, Git deployments, firewalls, backups and
            self-hosted services.
          </p>
        </article>

      </div>
    </div>
  </section>

  <!-- =========================
       STACK
  ========================== -->

  <section class="section" id="stack">
    <div class="container">

      <h2 class="section-title">
        TECH://<span>STACK</span>
      </h2>

      <p class="section-subtitle">
        The languages, platforms and infrastructure I regularly build with.
      </p>

      <div class="stack-group">
        <h3>&gt; languages</h3>

        <div class="badges">
          <span class="badge">🐍 Python</span>
          <span class="badge">🟨 JavaScript</span>
          <span class="badge">#️⃣ C#</span>
          <span class="badge">🐘 PHP</span>
          <span class="badge">🌐 HTML5</span>
          <span class="badge">🎨 CSS3</span>
        </div>
      </div>

      <div class="stack-group">
        <h3>&gt; backend_and_web</h3>

        <div class="badges">
          <span class="badge">🟢 Node.js</span>
          <span class="badge">▲ Next.js</span>
          <span class="badge">🔌 REST APIs</span>
          <span class="badge">🔐 JWT</span>
        </div>
      </div>

      <div class="stack-group">
        <h3>&gt; databases</h3>

        <div class="badges">
          <span class="badge">🗄️ MySQL</span>
        </div>
      </div>

      <div class="stack-group">
        <h3>&gt; infrastructure</h3>

        <div class="badges">
          <span class="badge">🐧 Linux</span>
          <span class="badge">🟠 Ubuntu</span>
          <span class="badge">🟩 NGINX</span>
          <span class="badge">☁️ Cloudflare</span>
          <span class="badge">🔒 Let's Encrypt</span>
          <span class="badge">📨 Postfix</span>
          <span class="badge">📬 Dovecot</span>
        </div>
      </div>

      <div class="stack-group">
        <h3>&gt; tools</h3>

        <div class="badges">
          <span class="badge">🌿 Git</span>
          <span class="badge">🐙 GitHub</span>
          <span class="badge">💻 VS Code</span>
          <span class="badge">⌨️ Cursor</span>
          <span class="badge">🤖 Discord</span>
        </div>
      </div>

    </div>
  </section>

  <!-- =========================
       PROJECTS
  ========================== -->

  <section class="section" id="projects">
    <div class="container">

      <h2 class="section-title">
        PROJECTS://<span>ACTIVE</span>
      </h2>

      <p class="section-subtitle">
        Some of the platforms and systems I'm actively developing.
      </p>

      <div class="grid grid-2">

        <article class="card project">
          <div class="project-top">
            <div class="project-name">🎬 ThunderFlix</div>
            <span class="project-tag">ACTIVE</span>
          </div>

          <p>
            A custom streaming platform built around multiple services,
            backend APIs, account features and a flexible source system.
          </p>

          <ul>
            <li>Movies, TV and anime</li>
            <li>User authentication</li>
            <li>Multiple profiles</li>
            <li>Kids profiles</li>
            <li>Continue Watching</li>
            <li>Watchlists and favourites</li>
            <li>Multiple streaming sources</li>
            <li>Developer and admin services</li>
          </ul>

          <div class="project-stack">
            <span class="mini-tag">Next.js</span>
            <span class="mini-tag">Node.js</span>
            <span class="mini-tag">MySQL</span>
            <span class="mini-tag">Tailwind</span>
          </div>
        </article>

        <article class="card project">
          <div class="project-top">
            <div class="project-name">⚡ Aeraxis Development</div>
            <span class="project-tag">TEAM</span>
          </div>

          <p>
            A development ecosystem focused on modern applications,
            backend services, infrastructure and developer tooling.
          </p>

          <ul>
            <li>Backend development</li>
            <li>Web development</li>
            <li>APIs</li>
            <li>Discord systems</li>
            <li>Infrastructure</li>
            <li>Developer tools</li>
          </ul>

          <div class="project-stack">
            <span class="mini-tag">aeraxis.dev</span>
            <span class="mini-tag">Backend</span>
            <span class="mini-tag">Infrastructure</span>
          </div>
        </article>

        <article class="card project">
          <div class="project-top">
            <div class="project-name">🌐 SurgeCDN</div>
            <span class="project-tag">INFRA</span>
          </div>

          <p>
            Developer-focused infrastructure, APIs and reusable services
            designed to avoid rebuilding the same systems repeatedly.
          </p>

          <ul>
            <li>API services</li>
            <li>Discord bot</li>
            <li>Developer integrations</li>
            <li>Infrastructure tooling</li>
            <li>Automation</li>
          </ul>

          <div class="project-stack">
            <span class="mini-tag">CDN</span>
            <span class="mini-tag">API</span>
            <span class="mini-tag">Automation</span>
          </div>
        </article>

        <article class="card project">
          <div class="project-top">
            <div class="project-name">🤖 Nexus</div>
            <span class="project-tag">DISCORD</span>
          </div>

          <p>
            An advanced Discord toolkit designed for developers,
            communities and server owners.
          </p>

          <ul>
            <li>Moderation</li>
            <li>Automation</li>
            <li>Server management</li>
            <li>Integrations</li>
            <li>Developer utilities</li>
            <li>Community tooling</li>
          </ul>

          <div class="project-stack">
            <span class="mini-tag">Discord</span>
            <span class="mini-tag">Automation</span>
            <span class="mini-tag">Developer Tools</span>
          </div>
        </article>

      </div>
    </div>
  </section>

  <!-- =========================
       INFRASTRUCTURE
  ========================== -->

  <section class="section" id="infra">
    <div class="container">

      <h2 class="section-title">
        INFRA://<span>ARCHITECTURE</span>
      </h2>

      <p class="section-subtitle">
        The application is only one layer. I like understanding everything
        from DNS through to the database.
      </p>

      <div class="architecture">
<pre>
                               ┌─────────────────┐
                               │     INTERNET    │
                               └────────┬────────┘
                                        │
                                        ▼
                         ┌───────────────────────────┐
                         │        CLOUDFLARE         │
                         │ DNS • Proxy • Security    │
                         │ SSL • Routing             │
                         └─────────────┬─────────────┘
                                       │
                                       ▼
                         ┌───────────────────────────┐
                         │           NGINX           │
                         │       Reverse Proxy       │
                         └─────────────┬─────────────┘
                                       │
                  ┌────────────────────┼────────────────────┐
                  │                    │                    │
                  ▼                    ▼                    ▼
        ┌────────────────┐   ┌────────────────┐   ┌────────────────┐
        │    NEXT.JS     │   │    NODE API    │   │    SERVICES    │
        │  WEB PLATFORM  │   │ BACKEND LOGIC  │   │ BOTS / WORKERS │
        └───────┬────────┘   └───────┬────────┘   └───────┬────────┘
                │                    │                    │
                └────────────────────┼────────────────────┘
                                     │
                                     ▼
                           ┌──────────────────┐
                           │      MYSQL       │
                           │    DATA LAYER    │
                           └──────────────────┘
</pre>
      </div>

      <div class="grid grid-3" style="margin-top: 28px;">

        <div class="card">
          <h3>Server Management</h3>
          <p>
            Ubuntu VPS administration, SSH deployments, backups,
            networking and firewall configuration.
          </p>
        </div>

        <div class="card">
          <h3>Reverse Proxy</h3>
          <p>
            Multi-domain NGINX configurations, SSL termination and routing
            traffic to backend services.
          </p>
        </div>

        <div class="card">
          <h3>DNS & Security</h3>
          <p>
            Cloudflare DNS, proxying, SSL/TLS, domain management and
            production configuration.
          </p>
        </div>

      </div>
    </div>
  </section>

  <!-- =========================
       PHILOSOPHY
  ========================== -->

  <section class="section">
    <div class="container">

      <h2 class="section-title">
        THUNDER://<span>PHILOSOPHY</span>
      </h2>

      <p class="section-subtitle">
        Build it. Break it. Debug it. Understand it. Improve it. Deploy it.
      </p>

      <table class="compare-table">
        <thead>
          <tr>
            <th>OLD MINDSET</th>
            <th>THUNDER MINDSET</th>
          </tr>
        </thead>

        <tbody>
          <tr>
            <td>"It works on my machine."</td>
            <td>Make it work in production.</td>
          </tr>

          <tr>
            <td>Copy a config.</td>
            <td>Understand the config.</td>
          </tr>

          <tr>
            <td>Restart the service.</td>
            <td>Find the root cause.</td>
          </tr>

          <tr>
            <td>Repeat tasks manually.</td>
            <td>Automate them.</td>
          </tr>

          <tr>
            <td>Ignore the infrastructure.</td>
            <td>Understand every layer.</td>
          </tr>

          <tr>
            <td>Deploy and forget.</td>
            <td>Maintain and improve.</td>
          </tr>

          <tr>
            <td>Blame DNS.</td>
            <td>Okay... sometimes still blame DNS.</td>
          </tr>
        </tbody>
      </table>

    </div>
  </section>

  <!-- =========================
       GITHUB
  ========================== -->

  <section class="section" id="stats">
    <div class="container">

      <h2 class="section-title">
        GITHUB://<span>STATS</span>
      </h2>

      <p class="section-subtitle">
        Development activity from my GitHub profile.
      </p>

      <div class="github-images">

        <img
          src="https://github-readme-stats.vercel.app/api?username=ThunderDoesDev&show_icons=true&theme=transparent&hide_border=true&title_color=00FFFF&text_color=FFFFFF&icon_color=7C3AED"
          alt="Thunder GitHub statistics"
        />

        <img
          src="https://github-readme-stats.vercel.app/api/top-langs/?username=ThunderDoesDev&layout=compact&theme=transparent&hide_border=true&title_color=00FFFF&text_color=FFFFFF"
          alt="Thunder most used GitHub languages"
        />

      </div>

      <div class="stats-grid">
        <div class="stat">
          <span class="stat-value">10+</span>
          <span class="stat-label">Years Around Technology</span>
        </div>

        <div class="stat">
          <span class="stat-value">∞</span>
          <span class="stat-label">SSH Sessions</span>
        </div>

        <div class="stat">
          <span class="stat-value">24/7</span>
          <span class="stat-label">Building Something</span>
        </div>
      </div>

    </div>
  </section>

  <!-- =========================
       CURRENT FOCUS
  ========================== -->

  <section class="section">
    <div class="container">

      <h2 class="section-title">
        CURRENT://<span>FOCUS</span>
      </h2>

      <div class="grid grid-3">

        <div class="card">
          <div class="card-icon">⚙️</div>
          <h3>Backend Architecture</h3>
          <p>
            Improving service structure, API design and maintainability.
          </p>
        </div>

        <div class="card">
          <div class="card-icon">🖥️</div>
          <h3>Infrastructure</h3>
          <p>
            Building stronger production and self-hosted environments.
          </p>
        </div>

        <div class="card">
          <div class="card-icon">🤖</div>
          <h3>Automation</h3>
          <p>
            Replacing repetitive manual workflows with reliable systems.
          </p>
        </div>

        <div class="card">
          <div class="card-icon">🏗️</div>
          <h3>System Design</h3>
          <p>
            Designing systems that stay maintainable as they grow.
          </p>
        </div>

        <div class="card">
          <div class="card-icon">🔐</div>
          <h3>Security</h3>
          <p>
            Improving infrastructure, authentication and application security.
          </p>
        </div>

        <div class="card">
          <div class="card-icon">📡</div>
          <h3>Self Hosting</h3>
          <p>
            Running and understanding more of my own infrastructure.
          </p>
        </div>

      </div>
    </div>
  </section>

  <!-- =========================
       CONTACT
  ========================== -->

  <section class="section" id="contact">
    <div class="container">

      <div class="contact-box">

        <h2>
          Let's <span class="gradient-text">Build Something.</span>
        </h2>

        <p>
          Interested in backend development, Discord systems,
          infrastructure, automation or self-hosting?
          You can find me through the links below.
        </p>

        <div class="hero-actions" style="justify-content: center;">

          <a
            href="https://thunderdoesdev.gg"
            target="_blank"
            rel="noopener"
            class="button button-primary"
          >
            thunderdoesdev.gg
          </a>

          <a
            href="https://discord.gg/thunderdoesdev"
            target="_blank"
            rel="noopener"
            class="button button-secondary"
          >
            Discord
          </a>

          <a
            href="mailto:contact@thunderdoesdev.gg"
            class="button button-secondary"
          >
            Email Me
          </a>

          <a
            href="https://github.com/ThunderDoesDev"
            target="_blank"
            rel="noopener"
            class="button button-secondary"
          >
            GitHub
          </a>

        </div>
      </div>

    </div>
  </section>

  <!-- =========================
       FOOTER
  ========================== -->

  <footer>
    <div class="container">
      <p>
        <strong>THUNDERDOESDEV</strong>
        · Backend Development · Discord · Infrastructure · Self Hosting
      </p>

      <p style="margin-top: 8px;">
        Powered by code, Linux, caffeine and too many SSH sessions. ⚡
      </p>
    </div>
  </footer>

  <!-- =========================
       JAVASCRIPT
  ========================== -->

  <script>
    const lines = [
      "Backend Developer & Certified IT Technician",
      "Building APIs, platforms & infrastructure",
      "Discord bots • Self-hosting • Automation",
      "Linux • NGINX • MySQL • Cloudflare",
      "If I can build it myself, I probably will. ⚡"
    ];

    const typingElement = document.getElementById("typing");

    let lineIndex = 0;
    let charIndex = 0;
    let deleting = false;

    const typeSpeed = 45;
    const deleteSpeed = 25;
    const pauseTime = 1400;

    function typeLoop() {
      const currentLine = lines[lineIndex];

      if (!deleting) {
        typingElement.textContent =
          currentLine.substring(0, charIndex + 1);

        charIndex++;

        if (charIndex === currentLine.length) {
          deleting = true;

          setTimeout(typeLoop, pauseTime);
          return;
        }

        setTimeout(typeLoop, typeSpeed);
      } else {
        typingElement.textContent =
          currentLine.substring(0, charIndex - 1);

        charIndex--;

        if (charIndex === 0) {
          deleting = false;
          lineIndex = (lineIndex + 1) % lines.length;

          setTimeout(typeLoop, 350);
          return;
        }

        setTimeout(typeLoop, deleteSpeed);
      }
    }

    typeLoop();

    // Smooth active nav highlighting
    const sections = document.querySelectorAll("section[id], header[id]");
    const navLinks = document.querySelectorAll(".nav-links a");

    window.addEventListener("scroll", () => {
      let current = "";

      sections.forEach(section => {
        const sectionTop = section.offsetTop - 150;

        if (window.scrollY >= sectionTop) {
          current = section.getAttribute("id");
        }
      });

      navLinks.forEach(link => {
        const href = link.getAttribute("href");

        if (!href || !href.startsWith("#")) return;

        if (href === `#${current}`) {
          link.style.color = "#00ffff";
        } else if (!link.classList.contains("nav-button")) {
          link.style.color = "";
        }
      });
    });
  </script>

</body>
</html>