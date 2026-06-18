<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Luis Pimentel — GitHub Profile</title>
  <style>
    @import url('https://fonts.googleapis.com/css2?family=Space+Grotesk:wght@300;400;600;700&family=Space+Mono:ital@0;1&display=swap');

    :root {
      --bg:        #0d0d0d;
      --surface:   #141414;
      --border:    #2a2a2a;
      --accent:    #c8f25a;
      --accent2:   #7b5ea7;
      --text:      #e8e8e8;
      --muted:     #888;
      --font-main: 'Space Grotesk', sans-serif;
      --font-mono: 'Space Mono', monospace;
    }

    *, *::before, *::after { box-sizing: border-box; margin: 0; padding: 0; }

    body {
      background: var(--bg);
      color: var(--text);
      font-family: var(--font-main);
      min-height: 100vh;
      display: flex;
      justify-content: center;
      padding: 3rem 1.5rem;
    }

    .card {
      max-width: 720px;
      width: 100%;
    }

    /* ── Header ── */
    .header {
      border-bottom: 1px solid var(--border);
      padding-bottom: 2rem;
      margin-bottom: 2rem;
    }

    .eyebrow {
      font-family: var(--font-mono);
      font-size: 0.75rem;
      color: var(--accent);
      letter-spacing: 0.12em;
      text-transform: uppercase;
      margin-bottom: 1rem;
    }

    .name {
      font-size: clamp(2.2rem, 6vw, 3.5rem);
      font-weight: 700;
      line-height: 1.05;
      letter-spacing: -0.03em;
    }

    .name span {
      color: var(--accent);
    }

    .roles {
      margin-top: 1rem;
      display: flex;
      flex-wrap: wrap;
      gap: 0.5rem;
    }

    .role-tag {
      font-family: var(--font-mono);
      font-size: 0.72rem;
      padding: 0.3rem 0.75rem;
      border: 1px solid var(--border);
      border-radius: 2px;
      color: var(--muted);
      letter-spacing: 0.05em;
      transition: border-color 0.2s, color 0.2s;
      cursor: default;
    }

    .role-tag:hover {
      border-color: var(--accent);
      color: var(--accent);
    }

    /* ── Bio ── */
    .bio {
      margin-bottom: 2.5rem;
    }

    .bio p {
      font-size: 1rem;
      line-height: 1.75;
      color: #bbb;
      margin-bottom: 1rem;
    }

    .bio p:last-child { margin-bottom: 0; }

    .bio .highlight {
      color: var(--text);
      font-weight: 600;
    }

    .bio .music-line {
      font-style: italic;
      color: var(--accent);
      border-left: 2px solid var(--accent);
      padding-left: 1rem;
      margin: 1.5rem 0;
    }

    /* ── Stack ── */
    .section-label {
      font-family: var(--font-mono);
      font-size: 0.7rem;
      color: var(--muted);
      letter-spacing: 0.12em;
      text-transform: uppercase;
      margin-bottom: 1rem;
    }

    .stack {
      display: flex;
      flex-wrap: wrap;
      gap: 0.5rem;
      margin-bottom: 2.5rem;
    }

    .stack-item {
      font-family: var(--font-mono);
      font-size: 0.8rem;
      padding: 0.4rem 0.9rem;
      background: var(--surface);
      border: 1px solid var(--border);
      border-radius: 2px;
      color: var(--text);
      cursor: default;
      transition: background 0.2s, border-color 0.2s, transform 0.15s;
      user-select: none;
    }

    .stack-item:hover {
      background: #1e1e1e;
      border-color: var(--accent2);
      transform: translateY(-2px);
    }

    /* ── Counter ── */
    .counter-grid {
      display: grid;
      grid-template-columns: repeat(3, 1fr);
      gap: 1px;
      background: var(--border);
      border: 1px solid var(--border);
      margin-bottom: 2.5rem;
    }

    .counter-cell {
      background: var(--surface);
      padding: 1.25rem 1rem;
      text-align: center;
    }

    .counter-number {
      font-size: 2rem;
      font-weight: 700;
      color: var(--accent);
      font-family: var(--font-mono);
      display: block;
    }

    .counter-label {
      font-size: 0.72rem;
      color: var(--muted);
      margin-top: 0.25rem;
      letter-spacing: 0.05em;
    }

    /* ── Footer ── */
    .footer {
      border-top: 1px solid var(--border);
      padding-top: 1.5rem;
      display: flex;
      justify-content: space-between;
      align-items: center;
      flex-wrap: gap;
      gap: 1rem;
    }

    .location {
      font-family: var(--font-mono);
      font-size: 0.75rem;
      color: var(--muted);
    }

    .tagline {
      font-family: var(--font-mono);
      font-size: 0.72rem;
      color: var(--muted);
      font-style: italic;
      text-align: right;
    }

    /* ── Cursor blink on name ── */
    .cursor {
      display: inline-block;
      width: 3px;
      height: 0.85em;
      background: var(--accent);
      margin-left: 4px;
      vertical-align: middle;
      animation: blink 1s step-end infinite;
    }

    @keyframes blink {
      0%, 100% { opacity: 1; }
      50%       { opacity: 0; }
    }

    @media (max-width: 480px) {
      .counter-grid { grid-template-columns: 1fr; }
      .footer { flex-direction: column; align-items: flex-start; }
      .tagline { text-align: left; }
    }
  </style>
</head>
<body>
  <div class="card">

    <!-- Header -->
    <header class="header">
      <p class="eyebrow">// github.com/luispimentelsalcedo</p>
      <h1 class="name">Luis <span>Pimentel</span><span class="cursor"></span></h1>
      <div class="roles">
        <span class="role-tag">Audiovisual Technologist</span>
        <span class="role-tag">Sound Lecturer</span>
        <span class="role-tag">Multi-instrumentalist</span>
        <span class="role-tag">Frontend Developer in progress</span>
      </div>
    </header>

    <!-- Bio -->
    <section class="bio">
      <p>
        With a background in <span class="highlight">Audio Engineering, Audiovisual Communication and UX Design</span>,
        I have spent over a decade working in broadcasting, live events, audiovisual systems,
        higher education and technical problem solving.
      </p>
      <p class="music-line">
        Professional multi-instrumentalist — bridging the gap between sound, design and code.
      </p>
      <p>
        Currently teaching Sound at <span class="highlight">Universidad Nebrija</span> while transitioning
        into software development through JavaScript, React, Git and modern frontend technologies.
        Bringing together technical expertise, user-centred thinking and a passion for building digital products.
      </p>
      <p>
        Driven by curiosity, continuous learning and the belief that
        <span class="highlight">great technology should be both intuitive and impactful.</span>
      </p>
    </section>

    <!-- Stats -->
    <p class="section-label">// experience</p>
    <div class="counter-grid" id="counter-grid">
      <div class="counter-cell">
        <span class="counter-number" data-target="10">0</span>
        <span class="counter-label">Years in AV & Education</span>
      </div>
      <div class="counter-cell">
        <span class="counter-number" data-target="4">0</span>
        <span class="counter-label">Degrees & Masters</span>
      </div>
      <div class="counter-cell">
        <span class="counter-number" data-target="1">0</span>
        <span class="counter-label">Career pivot underway</span>
      </div>
    </div>

    <!-- Stack -->
    <p class="section-label">// current stack</p>
    <div class="stack">
      <span class="stack-item">HTML5</span>
      <span class="stack-item">CSS3</span>
      <span class="stack-item">JavaScript</span>
      <span class="stack-item">Git</span>
      <span class="stack-item">GitHub</span>
      <span class="stack-item">Flexbox</span>
      <span class="stack-item">Grid</span>
      <span class="stack-item">React → coming soon</span>
    </div>

    <!-- Footer -->
    <footer class="footer">
      <span class="location">📍 Madrid, Spain</span>
      <span class="tagline">"El buen diseño, como el buen sonido,<br>se nota cuando no se nota."</span>
    </footer>

  </div>

  <script>
    // Counter animation — counts up from 0 to data-target
    function animateCounters() {
      const counters = document.querySelectorAll('.counter-number');

      counters.forEach(function(counter) {
        const target = parseInt(counter.getAttribute('data-target'));
        const duration = 1500;
        const step = duration / target;
        let current = 0;

        const interval = setInterval(function() {
          current++;
          counter.textContent = current;

          if (current >= target) {
            counter.textContent = target + '+';
            clearInterval(interval);
          }
        }, step);
      });
    }

    // Only run when the counters are visible on screen
    const observer = new IntersectionObserver(function(entries) {
      entries.forEach(function(entry) {
        if (entry.isIntersecting) {
          animateCounters();
          observer.disconnect();
        }
      });
    });

    observer.observe(document.getElementById('counter-grid'));
  </script>

</body>
</html>
