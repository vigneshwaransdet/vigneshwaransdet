
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8" />
<meta name="viewport" content="width=device-width, initial-scale=1.0"/>
<title>Vigneshwaran Baskaran — GitHub Profile</title>
<style>
  @import url('https://fonts.googleapis.com/css2?family=JetBrains+Mono:wght@400;500&family=Syne:wght@400;500;700&display=swap');

  *, *::before, *::after { box-sizing: border-box; margin: 0; padding: 0; }

  :root {
    --bg: #0d1117;
    --surface: #161b22;
    --surface2: #21262d;
    --border: #30363d;
    --text: #e6edf3;
    --muted: #8b949e;
    --green: #7ee787;
    --blue: #58a6ff;
    --purple: #a371f7;
    --orange: #f97316;
    --amber: #f59e0b;
    --red: #f78166;
    --accent: #238636;
  }

  body {
    background: var(--bg);
    color: var(--text);
    font-family: 'Syne', sans-serif;
    min-height: 100vh;
    padding: 2rem 1rem;
  }

  .container { max-width: 720px; margin: 0 auto; }

  /* Header */
  .header { text-align: center; margin-bottom: 2rem; }
  .avatar {
    width: 72px; height: 72px; border-radius: 50%;
    background: linear-gradient(135deg, #238636, #58a6ff);
    display: flex; align-items: center; justify-content: center;
    font-size: 28px; font-weight: 700; color: #fff;
    margin: 0 auto 1rem;
    border: 2px solid var(--border);
  }
  .header h1 { font-size: 24px; font-weight: 700; margin-bottom: 6px; }
  .header p { font-size: 14px; color: var(--muted); font-family: 'JetBrains Mono', monospace; }
  .pv {
    display: inline-flex; align-items: center; gap: 5px;
    background: #1f3a5f; color: #58a6ff;
    font-size: 11px; padding: 3px 10px; border-radius: 20px;
    margin-top: 10px; font-family: 'JetBrains Mono', monospace;
  }

  /* Card */
  .card {
    background: var(--surface);
    border: 1px solid var(--border);
    border-radius: 10px;
    padding: 1.25rem 1.5rem;
    margin-bottom: 1rem;
  }
  .card-title {
    font-size: 13px; font-weight: 500; color: var(--muted);
    text-transform: uppercase; letter-spacing: 0.08em;
    margin-bottom: 1rem;
    display: flex; align-items: center; gap: 6px;
  }
  .card-title::after {
    content: ''; flex: 1; height: 1px; background: var(--border);
  }

  /* About list */
  .about-list { list-style: none; display: flex; flex-direction: column; gap: 8px; }
  .about-list li {
    display: flex; align-items: flex-start; gap: 10px;
    font-size: 14px; line-height: 1.5;
  }
  .about-list li .icon { font-size: 15px; flex-shrink: 0; margin-top: 1px; }
  .about-list li strong { color: var(--green); font-weight: 500; }
  .about-list li a { color: var(--blue); text-decoration: none; }
  .about-list li a:hover { text-decoration: underline; }

  /* Connect */
  .connect-row { display: flex; gap: 10px; flex-wrap: wrap; }
  .connect-btn {
    display: inline-flex; align-items: center; gap: 7px;
    padding: 7px 16px; border-radius: 6px;
    border: 1px solid var(--border);
    background: var(--surface2);
    color: var(--text); font-size: 13px;
    text-decoration: none; font-family: 'Syne', sans-serif;
    transition: border-color 0.15s, background 0.15s;
    cursor: pointer;
  }
  .connect-btn:hover { border-color: var(--blue); background: #1f3a5f22; }

  /* Skills */
  .skill-group { margin-bottom: 1rem; }
  .skill-group:last-child { margin-bottom: 0; }
  .skill-group-label {
    font-size: 11px; color: var(--muted); font-weight: 500;
    text-transform: uppercase; letter-spacing: 0.06em;
    margin-bottom: 7px; font-family: 'JetBrains Mono', monospace;
  }
  .badges { display: flex; flex-wrap: wrap; gap: 6px; }
  .badge {
    display: inline-flex; align-items: center; gap: 5px;
    padding: 4px 10px; border-radius: 6px;
    font-size: 12px; font-weight: 500;
    border: 1px solid var(--border);
    background: var(--surface2);
    color: var(--text);
    transition: border-color 0.15s;
    font-family: 'JetBrains Mono', monospace;
  }
  .badge:hover { border-color: var(--muted); }
  .badge .dot { width: 8px; height: 8px; border-radius: 50%; }

  /* Stats */
  .stats-grid {
    display: grid;
    grid-template-columns: 1fr 1px 1fr 1px 1fr;
    align-items: center;
    gap: 0;
  }
  .stat-divider { background: var(--border); height: 60px; }
  .stat-sec { display: flex; flex-direction: column; align-items: center; gap: 4px; padding: 0 12px; }
  .stat-num { font-size: 28px; font-weight: 700; color: var(--blue); font-family: 'JetBrains Mono', monospace; }
  .stat-label { font-size: 12px; color: var(--muted); text-align: center; }
  .stat-sub { font-size: 10px; color: var(--green); text-align: center; font-family: 'JetBrains Mono', monospace; }

  /* Streak ring */
  .ring-wrap { display: flex; flex-direction: column; align-items: center; gap: 5px; }
  .ring-container { position: relative; width: 72px; height: 72px; }
  .ring-container svg { position: absolute; top: 0; left: 0; }
  .ring-inner {
    position: absolute; top: 50%; left: 50%;
    transform: translate(-50%, -50%);
    text-align: center;
  }
  .ring-num { font-size: 18px; font-weight: 700; color: var(--purple); font-family: 'JetBrains Mono', monospace; }
  .streak-lbl { font-size: 12px; font-weight: 500; color: var(--purple); }
  .streak-sub { font-size: 10px; color: var(--muted); font-family: 'JetBrains Mono', monospace; }

  /* Lang card */
  .lang-card {
    background: #0d1117;
    border: 1px solid var(--border);
    border-radius: 10px;
    padding: 1.1rem 1.25rem;
    margin-bottom: 1rem;
  }
  .lang-title { color: var(--green); font-size: 14px; font-weight: 500; margin-bottom: 12px; }
  .lang-bar { display: flex; height: 8px; border-radius: 6px; overflow: hidden; margin-bottom: 12px; gap: 2px; }
  .lang-legend { display: grid; grid-template-columns: 1fr 1fr; gap: 5px 14px; }
  .lang-item { display: flex; align-items: center; gap: 6px; font-size: 12px; color: #c9d1d9; font-family: 'JetBrains Mono', monospace; }
  .lang-dot { width: 10px; height: 10px; border-radius: 50%; flex-shrink: 0; }

  /* Update bar */
  .update-bar {
    display: flex; align-items: center; gap: 10px;
    flex-wrap: wrap; margin-top: 14px;
    padding-top: 14px; border-top: 1px solid var(--border);
  }
  .update-bar label { font-size: 12px; color: var(--muted); font-family: 'JetBrains Mono', monospace; }
  .update-bar input {
    width: 72px; padding: 5px 8px;
    background: var(--surface2); border: 1px solid var(--border);
    color: var(--text); border-radius: 6px;
    font-size: 13px; font-family: 'JetBrains Mono', monospace;
  }
  .update-bar input:focus { outline: none; border-color: var(--blue); }
  .update-bar button {
    padding: 5px 14px;
    background: var(--accent); border: none;
    color: #fff; border-radius: 6px;
    font-size: 13px; cursor: pointer;
    font-family: 'Syne', sans-serif; font-weight: 500;
  }
  .update-bar button:hover { background: #2ea043; }
</style>
</head>
<body>
<div class="container">

  <!-- Header -->
  <div class="header">
    <div class="avatar">VB</div>
    <h1>Hi 👋, I'm Vigneshwaran Baskaran</h1>
    <p>Senior SDET | 9+ Years | Selenium • Java • API Automation | CI/CD | DSA Learner</p>
    <div class="pv">👁 Profile views tracking enabled</div>
  </div>

  <!-- About -->
  <div class="card">
    <div class="card-title">About</div>
    <ul class="about-list">
      <li><span class="icon">🏢</span><span>Currently @ <strong>Gen Digital (NortonLifeLock)</strong> — Senior SDET</span></li>
      <li><span class="icon">📈</span><span>Leveling up <strong>DSA &amp; Problem Solving</strong> on LeetCode</span></li>
      <li><span class="icon">💬</span><span>Ask me about <strong>Selenium • REST Assured • Framework Design • CI/CD</strong></span></li>
      <li><span class="icon">🤝</span><span>Open to collaborate on <strong>QA Automation &amp; SDET projects</strong></span></li>
      <li><span class="icon">📫</span><span><a href="mailto:vigneshwaransdet@gmail.com">vigneshwaransdet@gmail.com</a></span></li>
      <li><span class="icon">⚡</span><span>9+ years of <strong>breaking things professionally</strong> — so users don't have to!</span></li>
    </ul>
  </div>

  <!-- Connect -->
  <div class="card">
    <div class="card-title">Connect</div>
    <div class="connect-row">
      <a href="https://www.linkedin.com/in/vigneshwaran-baskaran/" class="connect-btn" target="_blank">
        🔗 LinkedIn
      </a>
      <a href="https://leetcode.com/vigneshwaran_qaengr/" class="connect-btn" target="_blank">
        💻 LeetCode
      </a>
    </div>
  </div>

  <!-- Skills -->
  <div class="card">
    <div class="card-title">Technical Skills</div>

    <div class="skill-group">
      <div class="skill-group-label">Test Automation</div>
      <div class="badges">
        <span class="badge"><span class="dot" style="background:#43B02A;"></span>Selenium</span>
        <span class="badge"><span class="dot" style="background:#FF6C37;"></span>TestNG</span>
        <span class="badge"><span class="dot" style="background:#23D96C;"></span>Cucumber</span>
        <span class="badge"><span class="dot" style="background:#2EAD33;"></span>Playwright</span>
      </div>
    </div>

    <div class="skill-group">
      <div class="skill-group-label">API Testing</div>
      <div class="badges">
        <span class="badge"><span class="dot" style="background:#005F73;"></span>REST Assured</span>
        <span class="badge"><span class="dot" style="background:#FF6C37;"></span>Postman</span>
        <span class="badge"><span class="dot" style="background:#6A0DAD;"></span>SOAP UI</span>
      </div>
    </div>

    <div class="skill-group">
      <div class="skill-group-label">CI/CD &amp; DevOps</div>
      <div class="badges">
        <span class="badge"><span class="dot" style="background:#D24939;"></span>Jenkins</span>
        <span class="badge"><span class="dot" style="background:#888;"></span>TeamCity</span>
        <span class="badge"><span class="dot" style="background:#C71A36;"></span>Maven</span>
        <span class="badge"><span class="dot" style="background:#2496ED;"></span>Docker</span>
        <span class="badge"><span class="dot" style="background:#F05032;"></span>Git</span>
        <span class="badge"><span class="dot" style="background:#0052CC;"></span>Bitbucket</span>
        <span class="badge"><span class="dot" style="background:#e6edf3;"></span>GitHub</span>
      </div>
    </div>

    <div class="skill-group">
      <div class="skill-group-label">AI-Assisted Testing</div>
      <div class="badges">
        <span class="badge"><span class="dot" style="background:#e6edf3;"></span>GitHub Copilot</span>
        <span class="badge"><span class="dot" style="background:#6C63FF;"></span>Cursor AI</span>
      </div>
    </div>

    <div class="skill-group">
      <div class="skill-group-label">Cloud &amp; Cross-Browser</div>
      <div class="badges">
        <span class="badge"><span class="dot" style="background:#FF6C37;"></span>BrowserStack</span>
        <span class="badge"><span class="dot" style="background:#888;"></span>LambdaTest</span>
      </div>
    </div>

    <div class="skill-group">
      <div class="skill-group-label">Programming</div>
      <div class="badges">
        <span class="badge"><span class="dot" style="background:#ED8B00;"></span>Java</span>
        <span class="badge"><span class="dot" style="background:#F7DF1E;"></span>JavaScript</span>
        <span class="badge"><span class="dot" style="background:#007ACC;"></span>TypeScript</span>
      </div>
    </div>

    <div class="skill-group">
      <div class="skill-group-label">Database</div>
      <div class="badges">
        <span class="badge"><span class="dot" style="background:#4479A1;"></span>SQL</span>
      </div>
    </div>

    <div class="skill-group">
      <div class="skill-group-label">Test Management</div>
      <div class="badges">
        <span class="badge"><span class="dot" style="background:#0052CC;"></span>JIRA</span>
        <span class="badge"><span class="dot" style="background:#65C179;"></span>TestRail</span>
      </div>
    </div>
  </div>

  <!-- GitHub Stats -->
  <div class="card">
    <div class="card-title">GitHub Stats</div>

    <!-- Languages -->
    <div class="lang-card">
      <div class="lang-title">My Programming Languages</div>
      <div class="lang-bar">
        <div style="width:56.89%;background:#f97316;border-radius:6px 0 0 6px;"></div>
        <div style="width:38.57%;background:#f59e0b;"></div>
        <div style="width:2.43%;background:#8b5cf6;"></div>
        <div style="width:2.09%;background:#eab308;"></div>
        <div style="width:0.02%;background:#6b7280;border-radius:0 6px 6px 0;"></div>
      </div>
      <div class="lang-legend">
        <div class="lang-item"><div class="lang-dot" style="background:#f97316;"></div>HTML (56.89%)</div>
        <div class="lang-item"><div class="lang-dot" style="background:#f59e0b;"></div>Java (38.57%)</div>
        <div class="lang-item"><div class="lang-dot" style="background:#8b5cf6;"></div>CSS (2.43%)</div>
        <div class="lang-item"><div class="lang-dot" style="background:#eab308;"></div>JavaScript (2.09%)</div>
        <div class="lang-item"><div class="lang-dot" style="background:#6b7280;"></div>Batchfile (0.02%)</div>
      </div>
    </div>

    <!-- Streak Stats -->
    <div class="stats-grid">
      <div class="stat-sec">
        <div class="stat-num">201</div>
        <div class="stat-label">Total Contributions</div>
        <div class="stat-sub">Jul 4, 2021 – Present</div>
      </div>
      <div class="stat-divider"></div>
      <div class="stat-sec">
        <div class="ring-wrap">
          <div class="ring-container">
            <svg viewBox="0 0 72 72" width="72" height="72">
              <circle cx="36" cy="36" r="28" fill="none" stroke="#21262d" stroke-width="6"/>
              <circle id="arc" cx="36" cy="36" r="28" fill="none" stroke="#58a6ff" stroke-width="6"
                stroke-dasharray="175.93" stroke-dashoffset="175.93"
                stroke-linecap="round" transform="rotate(-90 36 36)"
                style="transition: stroke-dashoffset 0.5s ease;"/>
            </svg>
            <div class="ring-inner">
              <div style="font-size:14px;">🔥</div>
              <div class="ring-num" id="curr-num">0</div>
            </div>
          </div>
          <div class="streak-lbl">Current Streak</div>
          <div class="streak-sub" id="streak-date">May 19</div>
        </div>
      </div>
      <div class="stat-divider"></div>
      <div class="stat-sec">
        <div class="stat-num">13</div>
        <div class="stat-label">Longest Streak</div>
        <div class="stat-sub">Sep 11 – Sep 23, 2021</div>
      </div>
    </div>

    <!-- Update bar -->
    <div class="update-bar">
      <label>Update current streak:</label>
      <input type="number" id="streak-input" value="0" min="0" max="365" />
      <button onclick="applyStreak()">Apply</button>
    </div>
  </div>

</div>

<script>
  function applyStreak() {
    const v = parseInt(document.getElementById('streak-input').value) || 0;
    document.getElementById('curr-num').textContent = v;
    const circumference = 175.93;
    const offset = circumference * (1 - Math.min(v / 30, 1));
    document.getElementById('arc').style.strokeDashoffset = offset;
    const today = new Date();
    const label = today.toLocaleDateString('en-US', { month: 'short', day: 'numeric' });
    document.getElementById('streak-date').textContent = v > 0 ? 'Active – ' + label : label;
  }
</script>
</body>
</html>
