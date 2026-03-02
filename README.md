!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>NY Mets 2026 — Queens Baseball</title>
<link href="https://fonts.googleapis.com/css2?family=Barlow+Condensed:wght@400;600;700;800;900&family=Barlow:wght@300;400;500;600&display=swap" rel="stylesheet">
<style>
:root {
  --blue: #002D72;
  --blue-dark: #001a45;
  --blue-mid: #003d99;
  --orange: #FF5910;
  --orange-dark: #cc4400;
  --white: #ffffff;
  --light: #edf1fb;
  --text: #0a1228;
  --muted: rgba(10,18,40,0.5);
  --card-shadow: 0 4px 20px rgba(0,45,114,0.08);
}

* { margin: 0; padding: 0; box-sizing: border-box; }
html { scroll-behavior: smooth; }
body { background: var(--light); color: var(--text); font-family: 'Barlow', sans-serif; overflow-x: hidden; }

/* ── NAV ── */
nav {
  position: fixed; top: 0; left: 0; right: 0; z-index: 200;
  display: flex; align-items: center; justify-content: space-between;
  padding: 0 40px; height: 64px;
  background: var(--blue);
  border-bottom: 3px solid var(--orange);
}
.nav-logo {
  display: flex; align-items: center; gap: 12px;
  font-family: 'Barlow Condensed', sans-serif;
  font-weight: 800; font-size: 1.3rem; letter-spacing: 1px;
  text-transform: uppercase; color: white; text-decoration: none;
}
.nav-badge {
  width: 36px; height: 36px; border-radius: 50%;
  background: var(--orange);
  display: flex; align-items: center; justify-content: center;
  font-size: 0.78rem; font-weight: 900; color: white;
}
.nav-links { display: flex; gap: 28px; list-style: none; }
.nav-links a {
  color: rgba(255,255,255,0.7); text-decoration: none;
  font-size: 0.75rem; letter-spacing: 2px; text-transform: uppercase;
  font-weight: 600; transition: color 0.2s;
}
.nav-links a:hover { color: var(--orange); }
.nav-ticket {
  background: var(--orange); color: white !important;
  padding: 8px 18px; border-radius: 4px;
}
.nav-ticket:hover { background: #ff7a3d !important; color: white !important; }

/* ── HERO ── */
.hero {
  background: var(--blue);
  min-height: 100vh;
  display: flex; flex-direction: column;
  align-items: center; justify-content: center;
  text-align: center; padding: 100px 24px 80px;
  position: relative; overflow: hidden;
}
.hero::before {
  content: '';
  position: absolute; inset: 0;
  background:
    radial-gradient(ellipse 70% 60% at 15% 20%, rgba(0,80,200,0.5) 0%, transparent 60%),
    radial-gradient(ellipse 50% 40% at 85% 80%, rgba(255,89,16,0.2) 0%, transparent 55%);
  pointer-events: none;
}
.hero-ring {
  position: absolute; border-radius: 50%;
  border: 1px solid rgba(255,255,255,0.06);
  animation: spin 30s linear infinite; pointer-events: none;
}
.hero-ring:nth-child(1) { width: 700px; height: 700px; }
.hero-ring:nth-child(2) { width: 480px; height: 480px; border-color: rgba(255,89,16,0.08); animation-direction: reverse; animation-duration: 22s; }
@keyframes spin { to { transform: rotate(360deg); } }

.hero-eyebrow {
  position: relative; font-size: 0.72rem; letter-spacing: 5px;
  text-transform: uppercase; color: var(--orange); font-weight: 700;
  margin-bottom: 20px; animation: fadeUp 0.8s ease both;
}
.hero-title {
  position: relative;
  font-family: 'Barlow Condensed', sans-serif; font-weight: 900;
  font-size: clamp(5rem, 16vw, 13rem); line-height: 0.88;
  text-transform: uppercase; letter-spacing: -2px;
  animation: fadeUp 0.8s ease 0.1s both; color: white;
}
.hero-title .outline { -webkit-text-stroke: 2px rgba(255,255,255,0.2); color: transparent; }
.hero-title .accent { color: var(--orange); }
.hero-subtitle {
  position: relative; margin-top: 24px; font-size: 1rem;
  color: rgba(255,255,255,0.5); letter-spacing: 2px; font-weight: 300;
  text-transform: uppercase; animation: fadeUp 0.8s ease 0.2s both;
}
.hero-cta {
  position: relative; margin-top: 40px;
  display: flex; gap: 16px; justify-content: center; flex-wrap: wrap;
  animation: fadeUp 0.8s ease 0.3s both;
}
.btn {
  padding: 14px 32px; border-radius: 4px;
  font-family: 'Barlow Condensed', sans-serif; font-size: 0.9rem;
  font-weight: 700; letter-spacing: 2px; text-transform: uppercase;
  cursor: pointer; border: none; transition: all 0.2s; text-decoration: none; display: inline-block;
}
.btn-primary { background: var(--orange); color: white; }
.btn-primary:hover { background: #ff7a3d; transform: translateY(-2px); }
.btn-ghost { background: transparent; color: white; border: 1px solid rgba(255,255,255,0.3); }
.btn-ghost:hover { border-color: white; transform: translateY(-2px); }

/* ── STAT STRIP ── */
.stat-strip {
  background: var(--orange);
  display: flex; justify-content: center; flex-wrap: wrap;
}
.stat-item {
  padding: 28px 44px; text-align: center;
  border-right: 1px solid rgba(255,255,255,0.2);
  flex: 1; min-width: 130px;
}
.stat-item:last-child { border-right: none; }
.stat-num {
  font-family: 'Barlow Condensed', sans-serif;
  font-size: 2.8rem; font-weight: 900; color: white; line-height: 1;
}
.stat-num .dim { color: rgba(0,0,0,0.2); }
.stat-label { font-size: 0.62rem; letter-spacing: 3px; text-transform: uppercase; color: rgba(255,255,255,0.75); margin-top: 6px; font-weight: 600; }

/* ── SECTION SHARED ── */
.section-wrap { max-width: 1100px; margin: 0 auto; padding: 90px 24px; }
.section-tag { font-size: 0.68rem; letter-spacing: 4px; text-transform: uppercase; color: var(--orange); font-weight: 700; margin-bottom: 10px; }
.section-title { font-family: 'Barlow Condensed', sans-serif; font-size: clamp(2rem, 5vw, 3.2rem); font-weight: 900; text-transform: uppercase; letter-spacing: -1px; line-height: 1; color: var(--blue); }
.section-title-white { color: white; }
.section-header { display: flex; align-items: flex-end; justify-content: space-between; margin-bottom: 44px; flex-wrap: wrap; gap: 16px; }

/* ── TICKER ── */
.ticker-wrap {
  background: var(--blue-dark); overflow: hidden;
  padding: 12px 0; border-top: 1px solid rgba(255,255,255,0.05);
  border-bottom: 1px solid rgba(255,255,255,0.05);
}
.ticker-track {
  display: flex; gap: 0;
  animation: ticker 28s linear infinite;
  white-space: nowrap;
}
.ticker-item {
  font-family: 'Barlow Condensed', sans-serif;
  font-size: 0.85rem; font-weight: 700; letter-spacing: 2px;
  text-transform: uppercase; color: rgba(255,255,255,0.6);
  padding: 0 40px;
}
.ticker-item .hi { color: var(--orange); }
.ticker-sep { color: rgba(255,255,255,0.15); padding: 0 10px; }
@keyframes ticker { 0% { transform: translateX(0); } 100% { transform: translateX(-50%); } }

/* ── ROSTER ── */
.roster-grid { display: grid; grid-template-columns: repeat(auto-fill, minmax(300px, 1fr)); gap: 14px; }
.player-card {
  background: white; border: 1px solid rgba(0,45,114,0.1);
  border-radius: 12px; padding: 22px 24px;
  display: flex; align-items: center; gap: 18px;
  transition: all 0.25s; box-shadow: var(--card-shadow);
}
.player-card:hover { border-color: var(--orange); transform: translateY(-3px); box-shadow: 0 14px 36px rgba(0,45,114,0.13); }
.player-num {
  font-family: 'Barlow Condensed', sans-serif; font-size: 2.8rem;
  font-weight: 900; color: rgba(0,45,114,0.1); line-height: 1;
  min-width: 60px; text-align: center; transition: color 0.25s;
}
.player-card:hover .player-num { color: var(--orange); }
.player-details { flex: 1; }
.player-name { font-family: 'Barlow Condensed', sans-serif; font-size: 1.25rem; font-weight: 800; text-transform: uppercase; color: var(--blue); line-height: 1.1; }
.player-pos { font-size: 0.73rem; color: var(--muted); margin-top: 4px; letter-spacing: 0.5px; }
.player-badge { font-size: 0.58rem; letter-spacing: 1.5px; text-transform: uppercase; padding: 4px 10px; border-radius: 20px; font-weight: 700; white-space: nowrap; }
.badge-new { background: rgba(255,89,16,0.1); color: var(--orange); border: 1px solid rgba(255,89,16,0.25); }
.badge-fav { background: rgba(0,45,114,0.08); color: var(--blue); border: 1px solid rgba(0,45,114,0.18); }

/* ── DARK BG WRAPPER ── */
.dark-section { background: var(--blue); }

/* ── SCHEDULE ── */
.schedule-wrap { display: grid; grid-template-columns: 1fr 1fr; gap: 14px; }
@media (max-width: 700px) { .schedule-wrap { grid-template-columns: 1fr; } }
.month-block { background: rgba(255,255,255,0.05); border: 1px solid rgba(255,255,255,0.08); border-radius: 12px; overflow: hidden; }
.month-head { background: rgba(255,89,16,0.8); padding: 13px 20px; font-family: 'Barlow Condensed', sans-serif; font-size: 0.95rem; font-weight: 800; text-transform: uppercase; letter-spacing: 2px; color: white; display: flex; align-items: center; gap: 10px; }
.month-dot { width: 7px; height: 7px; border-radius: 50%; background: white; }
.game-item { display: flex; align-items: center; gap: 12px; padding: 11px 20px; border-bottom: 1px solid rgba(255,255,255,0.04); transition: background 0.15s; }
.game-item:last-child { border-bottom: none; }
.game-item:hover { background: rgba(255,255,255,0.04); }
.g-date { font-family: 'Barlow Condensed', sans-serif; font-size: 0.82rem; font-weight: 700; color: rgba(255,255,255,0.45); min-width: 60px; }
.g-opp { flex: 1; font-size: 0.86rem; color: rgba(255,255,255,0.88); }
.g-tag { font-size: 0.58rem; letter-spacing: 1px; text-transform: uppercase; padding: 3px 8px; border-radius: 3px; font-weight: 700; }
.g-home { background: rgba(255,255,255,0.12); color: white; }
.g-away { background: rgba(255,255,255,0.04); color: rgba(255,255,255,0.45); }
.g-series { background: var(--orange); color: white; }

/* ── TRIVIA QUIZ ── */
.quiz-box {
  background: white; border-radius: 16px; padding: 40px;
  box-shadow: var(--card-shadow); border: 1px solid rgba(0,45,114,0.1);
  max-width: 700px; margin: 0 auto;
}
.quiz-counter { font-size: 0.7rem; letter-spacing: 3px; text-transform: uppercase; color: var(--orange); font-weight: 700; margin-bottom: 10px; }
.quiz-q { font-family: 'Barlow Condensed', sans-serif; font-size: 1.8rem; font-weight: 800; color: var(--blue); line-height: 1.2; margin-bottom: 28px; }
.quiz-options { display: grid; grid-template-columns: 1fr 1fr; gap: 12px; }
.quiz-opt {
  padding: 16px 20px; border-radius: 10px;
  border: 2px solid rgba(0,45,114,0.12);
  background: var(--light); color: var(--text);
  font-family: 'Barlow', sans-serif; font-size: 0.9rem; font-weight: 500;
  cursor: pointer; transition: all 0.2s; text-align: left;
}
.quiz-opt:hover { border-color: var(--blue); background: white; }
.quiz-opt.correct { background: #e6f9ef; border-color: #22c55e; color: #166534; }
.quiz-opt.wrong { background: #fef2f2; border-color: #ef4444; color: #991b1b; }
.quiz-result { margin-top: 20px; padding: 16px 20px; border-radius: 10px; font-weight: 600; font-size: 0.95rem; display: none; }
.quiz-result.show { display: block; }
.quiz-result.correct { background: #e6f9ef; color: #166534; }
.quiz-result.wrong { background: #fef2f2; color: #991b1b; }
.quiz-next { margin-top: 20px; display: none; }
.quiz-next.show { display: block; }
.quiz-score { font-family: 'Barlow Condensed', sans-serif; font-size: 3rem; font-weight: 900; color: var(--blue); text-align: center; margin: 16px 0; }
.quiz-score span { color: var(--orange); }

/* ── POLL ── */
.poll-box {
  background: white; border-radius: 16px; padding: 36px;
  box-shadow: var(--card-shadow); border: 1px solid rgba(0,45,114,0.1);
}
.poll-q { font-family: 'Barlow Condensed', sans-serif; font-size: 1.6rem; font-weight: 800; color: var(--blue); margin-bottom: 24px; line-height: 1.2; }
.poll-options { display: flex; flex-direction: column; gap: 12px; }
.poll-opt {
  position: relative; overflow: hidden;
  padding: 14px 18px; border-radius: 10px;
  border: 2px solid rgba(0,45,114,0.1);
  background: var(--light); cursor: pointer;
  transition: border-color 0.2s;
  font-weight: 500; font-size: 0.9rem;
}
.poll-opt:hover { border-color: var(--blue); }
.poll-bar {
  position: absolute; left: 0; top: 0; bottom: 0;
  background: rgba(0,45,114,0.08); transition: width 0.8s ease;
  width: 0%;
}
.poll-opt-text { position: relative; z-index: 1; display: flex; justify-content: space-between; align-items: center; }
.poll-pct { font-family: 'Barlow Condensed', sans-serif; font-weight: 800; font-size: 1rem; color: var(--blue); opacity: 0; transition: opacity 0.3s; }
.poll-voted .poll-pct { opacity: 1; }
.poll-voted .poll-opt { cursor: default; }
.poll-voted .poll-opt.winner { border-color: var(--orange); }
.poll-voted .poll-opt.winner .poll-bar { background: rgba(255,89,16,0.12); }

/* ── FUN FACTS ── */
.facts-grid { display: grid; grid-template-columns: repeat(3,1fr); gap: 14px; }
@media (max-width: 750px) { .facts-grid { grid-template-columns: 1fr 1fr; } }
@media (max-width: 480px) { .facts-grid { grid-template-columns: 1fr; } }
.fact-card {
  background: white; border: 1px solid rgba(0,45,114,0.1);
  border-radius: 14px; padding: 28px 24px;
  box-shadow: var(--card-shadow); transition: all 0.25s;
}
.fact-card:hover { transform: translateY(-3px); border-color: var(--orange); }
.fact-num { font-family: 'Barlow Condensed', sans-serif; font-size: 3.5rem; font-weight: 900; color: var(--orange); line-height: 1; margin-bottom: 8px; }
.fact-label { font-family: 'Barlow Condensed', sans-serif; font-size: 1rem; font-weight: 800; text-transform: uppercase; color: var(--blue); letter-spacing: 0.5px; margin-bottom: 8px; }
.fact-desc { font-size: 0.82rem; color: var(--muted); line-height: 1.6; }

/* ── BUZZ ── */
.buzz-grid { display: grid; grid-template-columns: repeat(3,1fr); gap: 14px; }
@media (max-width: 800px) { .buzz-grid { grid-template-columns: 1fr; } }
.buzz-card {
  background: rgba(255,255,255,0.05); border: 1px solid rgba(255,255,255,0.09);
  border-radius: 14px; padding: 28px; transition: all 0.25s;
}
.buzz-card:hover { background: rgba(255,255,255,0.08); transform: translateY(-3px); border-color: rgba(255,89,16,0.4); }
.buzz-icon { font-size: 2rem; margin-bottom: 14px; }
.buzz-title { font-family: 'Barlow Condensed', sans-serif; font-size: 1.15rem; font-weight: 800; text-transform: uppercase; letter-spacing: 0.5px; margin-bottom: 10px; color: white; }
.buzz-text { font-size: 0.86rem; color: rgba(255,255,255,0.55); line-height: 1.7; }

/* ── COUNTDOWN ── */
.countdown-strip {
  background: var(--orange);
  text-align: center; padding: 40px 24px;
}
.countdown-label { font-size: 0.72rem; letter-spacing: 4px; text-transform: uppercase; color: rgba(255,255,255,0.75); font-weight: 700; margin-bottom: 20px; }
.countdown-boxes { display: flex; justify-content: center; gap: 20px; flex-wrap: wrap; }
.cd-box { text-align: center; }
.cd-num { font-family: 'Barlow Condensed', sans-serif; font-size: 3.5rem; font-weight: 900; color: white; line-height: 1; background: rgba(0,0,0,0.15); padding: 12px 20px; border-radius: 8px; min-width: 80px; display: block; }
.cd-unit { font-size: 0.62rem; letter-spacing: 3px; text-transform: uppercase; color: rgba(255,255,255,0.7); font-weight: 600; margin-top: 8px; }

/* ── FOOTER ── */
footer { background: var(--blue-dark); text-align: center; padding: 60px 24px; border-top: 4px solid var(--orange); }
.footer-logo { font-family: 'Barlow Condensed', sans-serif; font-size: 4rem; font-weight: 900; text-transform: uppercase; letter-spacing: -2px; line-height: 1; margin-bottom: 16px; color: white; }
.footer-logo .accent { color: var(--orange); }
.footer-logo .outline { -webkit-text-stroke: 1px rgba(255,255,255,0.2); color: transparent; }
.footer-links { display: flex; justify-content: center; gap: 32px; margin: 24px 0; flex-wrap: wrap; }
.footer-links a { color: rgba(255,255,255,0.45); text-decoration: none; font-size: 0.75rem; letter-spacing: 2px; text-transform: uppercase; transition: color 0.2s; }
.footer-links a:hover { color: var(--orange); }
.footer-sub { font-size: 0.72rem; color: rgba(255,255,255,0.3); letter-spacing: 2px; text-transform: uppercase; }

/* ── ANIMATIONS ── */
@keyframes fadeUp { from { opacity: 0; transform: translateY(30px); } to { opacity: 1; transform: translateY(0); } }
.reveal { opacity: 0; transform: translateY(24px); transition: opacity 0.6s ease, transform 0.6s ease; }
.reveal.visible { opacity: 1; transform: translateY(0); }

@media (max-width: 600px) {
  nav { padding: 0 16px; }
  .nav-links { gap: 16px; }
  .section-wrap { padding: 70px 16px; }
  .stat-item { padding: 20px 20px; }
  .quiz-options { grid-template-columns: 1fr; }
}
</style>
</head>
<body>

<!-- NAV -->
<nav>
  <a href="#" class="nav-logo">
    <div class="nav-badge">NY</div>
    METS 2026
  </a>
  <ul class="nav-links">
    <li><a href="#roster">Roster</a></li>
    <li><a href="#schedule">Schedule</a></li>
    <li><a href="#trivia">Trivia</a></li>
    <li><a href="#facts">Facts</a></li>
    <li><a href="#buzz">Buzz</a></li>
    <li><a href="https://www.mlb.com/mets/tickets" target="_blank" class="nav-ticket">Tickets</a></li>
  </ul>
</nav>

<!-- HERO -->
<div class="hero">
  <div class="hero-ring"></div>
  <div class="hero-ring"></div>
  <div class="hero-eyebrow">New York Mets · 2026 Season · Queens, NY</div>
  <h1 class="hero-title">
    <span class="outline">LET'S</span><br>
    <span class="accent">GO</span><br>
    <span>METS</span>
  </h1>
  <p class="hero-subtitle">Citi Field · Est. 1962 · NL East</p>
  <div class="hero-cta">
    <a href="#roster" class="btn btn-primary">View Roster</a>
    <a href="#schedule" class="btn btn-ghost">2026 Schedule</a>
  </div>
</div>

<!-- STAT STRIP -->
<div class="stat-strip">
  <div class="stat-item"><div class="stat-num">83<span class="dim">–79</span></div><div class="stat-label">2025 Record</div></div>
  <div class="stat-item"><div class="stat-num">$765<span class="dim">M</span></div><div class="stat-label">Soto Contract</div></div>
  <div class="stat-item"><div class="stat-num">$126<span class="dim">M</span></div><div class="stat-label">Bichette Deal</div></div>
  <div class="stat-item"><div class="stat-num">65<span class="dim">th</span></div><div class="stat-label">Season</div></div>
  <div class="stat-item"><div class="stat-num">#<span class="dim">1</span></div><div class="stat-label">Queens Forever</div></div>
</div>

<!-- TICKER -->
<div class="ticker-wrap">
  <div class="ticker-track">
    <span class="ticker-item">🔵 Juan Soto <span class="hi">RF</span></span><span class="ticker-sep">·</span>
    <span class="ticker-item">🔵 Francisco Lindor <span class="hi">SS</span></span><span class="ticker-sep">·</span>
    <span class="ticker-item">🟠 Bo Bichette <span class="hi">NEW · $126M</span></span><span class="ticker-sep">·</span>
    <span class="ticker-item">🟠 Luis Robert Jr. <span class="hi">NEW · CF</span></span><span class="ticker-sep">·</span>
    <span class="ticker-item">🔵 Francisco Alvarez <span class="hi">C</span></span><span class="ticker-sep">·</span>
    <span class="ticker-item">🟠 Freddy Peralta <span class="hi">NEW · SP</span></span><span class="ticker-sep">·</span>
    <span class="ticker-item">🔵 Opening Day <span class="hi">Mar 26 vs PIT</span></span><span class="ticker-sep">·</span>
    <span class="ticker-item">⚡ Subway Series <span class="hi">May 12–14</span></span><span class="ticker-sep">·</span>
    <span class="ticker-item">🔵 Juan Soto <span class="hi">RF</span></span><span class="ticker-sep">·</span>
    <span class="ticker-item">🔵 Francisco Lindor <span class="hi">SS</span></span><span class="ticker-sep">·</span>
    <span class="ticker-item">🟠 Bo Bichette <span class="hi">NEW · $126M</span></span><span class="ticker-sep">·</span>
    <span class="ticker-item">🟠 Luis Robert Jr. <span class="hi">NEW · CF</span></span><span class="ticker-sep">·</span>
    <span class="ticker-item">🔵 Francisco Alvarez <span class="hi">C</span></span><span class="ticker-sep">·</span>
    <span class="ticker-item">🟠 Freddy Peralta <span class="hi">NEW · SP</span></span><span class="ticker-sep">·</span>
    <span class="ticker-item">🔵 Opening Day <span class="hi">Mar 26 vs PIT</span></span><span class="ticker-sep">·</span>
    <span class="ticker-item">⚡ Subway Series <span class="hi">May 12–14</span></span><span class="ticker-sep">·</span>
  </div>
</div>

<!-- COUNTDOWN -->
<div class="countdown-strip">
  <div class="countdown-label">Opening Day Countdown — March 26, 2026</div>
  <div class="countdown-boxes">
    <div class="cd-box"><span class="cd-num" id="cd-days">24</span><div class="cd-unit">Days</div></div>
    <div class="cd-box"><span class="cd-num" id="cd-hours">--</span><div class="cd-unit">Hours</div></div>
    <div class="cd-box"><span class="cd-num" id="cd-mins">--</span><div class="cd-unit">Minutes</div></div>
    <div class="cd-box"><span class="cd-num" id="cd-secs">--</span><div class="cd-unit">Seconds</div></div>
  </div>
</div>

<!-- ROSTER -->
<div style="background: var(--light);">
<div class="section-wrap" id="roster">
  <div class="section-header reveal">
    <div><div class="section-tag">2026 Squad</div><h2 class="section-title">The Roster</h2></div>
    <div style="font-size:0.78rem;color:var(--muted);letter-spacing:1px;">🟠 = New Addition</div>
  </div>
  <div class="roster-grid">
    <div class="player-card reveal"><div class="player-num">22</div><div class="player-details"><div class="player-name">Juan Soto</div><div class="player-pos">Right Field · Age 27 · $765M · Generational Hitter</div></div><span class="player-badge badge-fav">Fan Fav</span></div>
    <div class="player-card reveal"><div class="player-num">12</div><div class="player-details"><div class="player-name">Francisco Lindor</div><div class="player-pos">Shortstop · Age 32 · Team Captain · Gold Glover</div></div></div>
    <div class="player-card reveal"><div class="player-num">4</div><div class="player-details"><div class="player-name">Francisco Alvarez</div><div class="player-pos">Catcher · Age 24 · Future Superstar</div></div></div>
    <div class="player-card reveal"><div class="player-num">19</div><div class="player-details"><div class="player-name">Bo Bichette</div><div class="player-pos">Infield · Age 28 · $126M Deal · Proven Hitter</div></div><span class="player-badge badge-new">New</span></div>
    <div class="player-card reveal"><div class="player-num">88</div><div class="player-details"><div class="player-name">Luis Robert Jr.</div><div class="player-pos">Center Field · Age 27 · Five-Tool Weapon</div></div><span class="player-badge badge-new">New</span></div>
    <div class="player-card reveal"><div class="player-num">7</div><div class="player-details"><div class="player-name">Brett Baty</div><div class="player-pos">Third Base · Age 26 · Breakout Candidate</div></div></div>
    <div class="player-card reveal"><div class="player-num">1</div><div class="player-details"><div class="player-name">MJ Melendez</div><div class="player-pos">Left Field · Age 27 · Power Bat</div></div></div>
    <div class="player-card reveal"><div class="player-num">0</div><div class="player-details"><div class="player-name">Ronny Mauricio</div><div class="player-pos">Infield · Age 25 · Rising Prospect</div></div></div>
    <div class="player-card reveal"><div class="player-num">59</div><div class="player-details"><div class="player-name">Sean Manaea</div><div class="player-pos">SP · Age 34 · Rotation Anchor · Veteran Lefty</div></div></div>
    <div class="player-card reveal"><div class="player-num">51</div><div class="player-details"><div class="player-name">Freddy Peralta</div><div class="player-pos">SP · Age 29 · Opening Day Starter · From MIL</div></div><span class="player-badge badge-new">New</span></div>
    <div class="player-card reveal"><div class="player-num">35</div><div class="player-details"><div class="player-name">Clay Holmes</div><div class="player-pos">SP · Age 33 · Converted Sinker Machine</div></div></div>
    <div class="player-card reveal"><div class="player-num">23</div><div class="player-details"><div class="player-name">David Peterson</div><div class="player-pos">SP · Age 30 · Homegrown Queens Lefty</div></div></div>
  </div>
</div>
</div>

<!-- SCHEDULE -->
<div class="dark-section" id="schedule">
<div class="section-wrap">
  <div class="section-header reveal">
    <div><div class="section-tag">Regular Season</div><h2 class="section-title section-title-white">2026 Schedule</h2></div>
    <div style="font-size:0.75rem;color:rgba(255,255,255,0.35);letter-spacing:1px;">⚡ Subway Series &nbsp;·&nbsp; 🔥 Marquee Game</div>
  </div>
  <div class="schedule-wrap">
    <div class="month-block reveal">
      <div class="month-head"><div class="month-dot"></div>March</div>
      <div class="game-item"><span class="g-date">Mar 26</span><span class="g-opp">Pittsburgh Pirates — Opening Day 🎉</span><span class="g-tag g-home">Home</span></div>
      <div class="game-item"><span class="g-date">Mar 28</span><span class="g-opp">Pittsburgh Pirates</span><span class="g-tag g-home">Home</span></div>
      <div class="game-item"><span class="g-date">Mar 29</span><span class="g-opp">Pittsburgh Pirates</span><span class="g-tag g-home">Home</span></div>
      <div class="game-item"><span class="g-date">Mar 30</span><span class="g-opp">St. Louis Cardinals</span><span class="g-tag g-away">Away</span></div>
      <div class="game-item"><span class="g-date">Mar 31</span><span class="g-opp">St. Louis Cardinals</span><span class="g-tag g-away">Away</span></div>
    </div>
    <div class="month-block reveal">
      <div class="month-head"><div class="month-dot"></div>April — Part 1</div>
      <div class="game-item"><span class="g-date">Apr 1</span><span class="g-opp">St. Louis Cardinals</span><span class="g-tag g-away">Away</span></div>
      <div class="game-item"><span class="g-date">Apr 2–5</span><span class="g-opp">San Francisco Giants (4 games)</span><span class="g-tag g-away">Away</span></div>
      <div class="game-item"><span class="g-date">Apr 7–9</span><span class="g-opp">Arizona Diamondbacks</span><span class="g-tag g-home">Home</span></div>
      <div class="game-item"><span class="g-date">Apr 10–12</span><span class="g-opp">Athletics</span><span class="g-tag g-home">Home</span></div>
      <div class="game-item"><span class="g-date">Apr 13–15</span><span class="g-opp">Los Angeles Dodgers 🔥</span><span class="g-tag g-away">Away</span></div>
    </div>
    <div class="month-block reveal">
      <div class="month-head"><div class="month-dot"></div>April — Part 2</div>
      <div class="game-item"><span class="g-date">Apr 17–19</span><span class="g-opp">Chicago Cubs (Wrigley) 🔥</span><span class="g-tag g-away">Away</span></div>
      <div class="game-item"><span class="g-date">Apr 21–23</span><span class="g-opp">Minnesota Twins</span><span class="g-tag g-home">Home</span></div>
      <div class="game-item"><span class="g-date">Apr 24–26</span><span class="g-opp">Colorado Rockies</span><span class="g-tag g-home">Home</span></div>
      <div class="game-item"><span class="g-date">Apr 28–30</span><span class="g-opp">Washington Nationals</span><span class="g-tag g-home">Home</span></div>
    </div>
    <div class="month-block reveal">
      <div class="month-head"><div class="month-dot"></div>May</div>
      <div class="game-item"><span class="g-date">May 1–3</span><span class="g-opp">Los Angeles Angels</span><span class="g-tag g-away">Away</span></div>
      <div class="game-item"><span class="g-date">May 5–6</span><span class="g-opp">Colorado Rockies</span><span class="g-tag g-away">Away</span></div>
      <div class="game-item"><span class="g-date">May 9–10</span><span class="g-opp">Arizona Diamondbacks</span><span class="g-tag g-away">Away</span></div>
      <div class="game-item"><span class="g-date">May 12–14</span><span class="g-opp">New York Yankees ⚡</span><span class="g-tag g-series">Subway</span></div>
      <div class="game-item"><span class="g-date">May 15–17</span><span class="g-opp">Miami Marlins</span><span class="g-tag g-home">Home</span></div>
      <div class="game-item"><span class="g-date">May 19–21</span><span class="g-opp">Washington Nationals</span><span class="g-tag g-away">Away</span></div>
      <div class="game-item"><span class="g-date">May 25–27</span><span class="g-opp">Toronto Blue Jays</span><span class="g-tag g-home">Home</span></div>
      <div class="game-item"><span class="g-date">May 29–31</span><span class="g-opp">Philadelphia Phillies 🔥</span><span class="g-tag g-home">Home</span></div>
    </div>
    <div class="month-block reveal">
      <div class="month-head"><div class="month-dot"></div>June</div>
      <div class="game-item"><span class="g-date">Jun 2–3</span><span class="g-opp">Seattle Mariners</span><span class="g-tag g-away">Away</span></div>
      <div class="game-item"><span class="g-date">Jun 6–7</span><span class="g-opp">San Diego Padres</span><span class="g-tag g-away">Away</span></div>
      <div class="game-item"><span class="g-date">Jun 9–14</span><span class="g-opp">Home Stand — Citi Field</span><span class="g-tag g-home">Home</span></div>
      <div class="game-item"><span class="g-date">Jun 16–17</span><span class="g-opp">Cincinnati Reds</span><span class="g-tag g-away">Away</span></div>
      <div class="game-item"><span class="g-date">Jun 20–21</span><span class="g-opp">Philadelphia Phillies 🔥</span><span class="g-tag g-away">Away</span></div>
      <div class="game-item"><span class="g-date">Jun 22–28</span><span class="g-opp">Home Stand — Citi Field</span><span class="g-tag g-home">Home</span></div>
      <div class="game-item"><span class="g-date">Jun 30</span><span class="g-opp">Toronto Blue Jays</span><span class="g-tag g-away">Away</span></div>
    </div>
    <div class="month-block reveal" style="display:flex;align-items:center;justify-content:center;">
      <div style="text-align:center;padding:36px;">
        <div style="font-size:2.5rem;margin-bottom:12px;">🏆</div>
        <div style="font-family:'Barlow Condensed',sans-serif;font-size:1.2rem;font-weight:800;text-transform:uppercase;letter-spacing:1px;color:white;margin-bottom:8px;">July – October</div>
        <div style="font-size:0.82rem;color:rgba(255,255,255,0.35);">Second half schedule updates<br>as the season progresses</div>
      </div>
    </div>
  </div>
</div>
</div>

<!-- METS TRIVIA QUIZ -->
<div style="background: var(--light);">
<div class="section-wrap" id="trivia">
  <div class="section-header reveal">
    <div><div class="section-tag">Test Your Knowledge</div><h2 class="section-title">Mets Trivia</h2></div>
  </div>
  <div class="quiz-box reveal">
    <div class="quiz-counter" id="quiz-counter">Question 1 of 6</div>
    <div class="quiz-q" id="quiz-q">Loading...</div>
    <div class="quiz-options" id="quiz-opts"></div>
    <div class="quiz-result" id="quiz-result"></div>
    <div class="quiz-next" id="quiz-next">
      <button class="btn btn-primary" onclick="nextQuestion()">Next Question →</button>
    </div>
  </div>
</div>
</div>

<!-- FAN POLL -->
<div class="dark-section">
<div class="section-wrap" style="max-width:700px;">
  <div class="section-header reveal">
    <div><div class="section-tag">Fan Vote</div><h2 class="section-title section-title-white">Fan Poll</h2></div>
  </div>
  <div class="poll-box reveal">
    <div class="poll-q">Who will be the Mets' best player in 2026?</div>
    <div class="poll-options" id="poll-opts">
      <div class="poll-opt" onclick="vote(this, 52)"><div class="poll-bar"></div><div class="poll-opt-text"><span>Juan Soto</span><span class="poll-pct">52%</span></div></div>
      <div class="poll-opt" onclick="vote(this, 24)"><div class="poll-bar"></div><div class="poll-opt-text"><span>Francisco Alvarez</span><span class="poll-pct">24%</span></div></div>
      <div class="poll-opt" onclick="vote(this, 14)"><div class="poll-bar"></div><div class="poll-opt-text"><span>Francisco Lindor</span><span class="poll-pct">14%</span></div></div>
      <div class="poll-opt" onclick="vote(this, 10)"><div class="poll-bar"></div><div class="poll-opt-text"><span>Bo Bichette</span><span class="poll-pct">10%</span></div></div>
    </div>
  </div>
</div>
</div>

<!-- FUN FACTS -->
<div style="background: var(--light);">
<div class="section-wrap" id="facts">
  <div class="section-header reveal">
    <div><div class="section-tag">Did You Know?</div><h2 class="section-title">Mets By the Numbers</h2></div>
  </div>
  <div class="facts-grid">
    <div class="fact-card reveal"><div class="fact-num">2</div><div class="fact-label">World Series Titles</div><div class="fact-desc">1969 Miracle Mets and 1986. Both times Queens shocked the baseball world.</div></div>
    <div class="fact-card reveal"><div class="fact-num">65</div><div class="fact-label">Years of Baseball</div><div class="fact-desc">The Mets have been playing since 1962, originally at the Polo Grounds before moving to Shea Stadium and then Citi Field.</div></div>
    <div class="fact-card reveal"><div class="fact-num">41</div><div class="fact-label">Citi Field Capacity (K)</div><div class="fact-desc">Opened in 2009, Citi Field holds 41,922 fans and is one of the best ballparks in the majors.</div></div>
    <div class="fact-card reveal"><div class="fact-num">7</div><div class="fact-label">Retired Numbers</div><div class="fact-desc">Gil Hodges (14), Casey Stengel (37), Jackie Robinson (42), Tom Seaver (41), Mike Piazza (31), Jerry Koosman (36), and Dwight Gooden (16).</div></div>
    <div class="fact-card reveal"><div class="fact-num">$765M</div><div class="fact-label">Soto's Deal</div><div class="fact-desc">Juan Soto's contract is one of the largest in baseball history, cementing him as the face of the 2026 Mets.</div></div>
    <div class="fact-card reveal"><div class="fact-num">1969</div><div class="fact-label">The Miracle Year</div><div class="fact-desc">The "Miracle Mets" were 100-to-1 underdogs who shocked everyone by winning the World Series. You gotta believe.</div></div>
  </div>
</div>
</div>

<!-- BUZZ -->
<div class="dark-section">
<div class="section-wrap" id="buzz">
  <div class="section-header reveal">
    <div><div class="section-tag">2026 Storylines</div><h2 class="section-title section-title-white">Season Buzz</h2></div>
  </div>
  <div class="buzz-grid">
    <div class="buzz-card reveal"><div class="buzz-icon">💰</div><div class="buzz-title">Big Offseason Moves</div><div class="buzz-text">Steve Cohen kept spending. Bichette locked in for $126M, Peralta brought in from Milwaukee — stacking on top of Soto's $765M deal from last offseason. Built to win.</div></div>
    <div class="buzz-card reveal"><div class="buzz-icon">⚡</div><div class="buzz-title">Subway Series</div><div class="buzz-text">Yankees at Citi Field May 12–14. Three games, one city, all the bragging rights. Queens is going to be electric.</div></div>
    <div class="buzz-card reveal"><div class="buzz-icon">🔥</div><div class="buzz-title">Dodgers Showdown</div><div class="buzz-text">April 13–15 at Dodger Stadium. Soto vs. LA's back-to-back defending champions. The Mets want revenge. This is the first big statement game of the year.</div></div>
    <div class="buzz-card reveal"><div class="buzz-icon">📈</div><div class="buzz-title">Alvarez Ascending</div><div class="buzz-text">Francisco Alvarez is 24 and entering his prime. One of the most exciting young catchers in baseball, built for a monster year.</div></div>
    <div class="buzz-card reveal"><div class="buzz-icon">🎯</div><div class="buzz-title">Deep Rotation</div><div class="buzz-text">Manaea, Peralta, Holmes, Peterson — real depth in the rotation. If they stay healthy, October baseball is very much in play.</div></div>
    <div class="buzz-card reveal"><div class="buzz-icon">🏟️</div><div class="buzz-title">Opening Day Is Here</div><div class="buzz-text">March 26 vs. Pittsburgh at Citi Field. The faithful are fired up. This is the year Queens brings it all the way home.</div></div>
  </div>
</div>
</div>

<!-- FOOTER -->
<footer>
  <div class="footer-logo"><span class="accent">Let's Go </span><span class="outline">Mets</span></div>
  <div class="footer-links">
    <a href="https://www.mlb.com/mets" target="_blank">Official Site</a>
    <a href="https://www.mlb.com/mets/tickets" target="_blank">Tickets</a>
    <a href="https://www.mlb.com/mets/stats" target="_blank">Stats</a>
    <a href="https://twitter.com/mets" target="_blank">Twitter / X</a>
  </div>
  <div class="footer-sub">Blue & Orange Forever · Citi Field, Queens NY · Est. 1962</div>
</footer>

<script>
// ── COUNTDOWN ──
function updateCountdown() {
  const opening = new Date('2026-03-26T13:10:00-04:00');
  const now = new Date();
  const diff = opening - now;
  if (diff <= 0) {
    document.getElementById('cd-days').textContent = '0';
    document.getElementById('cd-hours').textContent = '00';
    document.getElementById('cd-mins').textContent = '00';
    document.getElementById('cd-secs').textContent = '00';
    return;
  }
  const days = Math.floor(diff / 86400000);
  const hours = Math.floor((diff % 86400000) / 3600000);
  const mins = Math.floor((diff % 3600000) / 60000);
  const secs = Math.floor((diff % 60000) / 1000);
  document.getElementById('cd-days').textContent = days;
  document.getElementById('cd-hours').textContent = String(hours).padStart(2,'0');
  document.getElementById('cd-mins').textContent = String(mins).padStart(2,'0');
  document.getElementById('cd-secs').textContent = String(secs).padStart(2,'0');
}
setInterval(updateCountdown, 1000);
updateCountdown();

// ── TRIVIA ──
const questions = [
  { q: "What year did the Mets win their first World Series?", opts: ["1962","1969","1973","1977"], ans: 1 },
  { q: "Who is the Mets' all-time home run leader?", opts: ["Tom Seaver","Mike Piazza","Darryl Strawberry","David Wright"], ans: 2 },
  { q: "What is the name of the Mets' current home stadium?", opts: ["Shea Stadium","Yankee Stadium","Citi Field","Oracle Park"], ans: 2 },
  { q: "Which Mets legend wore number 41 and had his jersey retired?", opts: ["Mike Piazza","Tom Seaver","Dwight Gooden","Keith Hernandez"], ans: 1 },
  { q: "How much did Juan Soto sign for with the Mets?", opts: ["$450M","$600M","$765M","$800M"], ans: 2 },
  { q: "The 'Miracle Mets' of 1969 were considered how big an underdog at the start of the season?", opts: ["10-to-1","50-to-1","100-to-1","200-to-1"], ans: 2 },
];
let current = 0, score = 0, answered = false;

function loadQuestion() {
  const q = questions[current];
  document.getElementById('quiz-counter').textContent = `Question ${current+1} of ${questions.length}`;
  document.getElementById('quiz-q').textContent = q.q;
  document.getElementById('quiz-result').className = 'quiz-result';
  document.getElementById('quiz-result').textContent = '';
  document.getElementById('quiz-next').className = 'quiz-next';
  answered = false;
  const optsEl = document.getElementById('quiz-opts');
  optsEl.innerHTML = '';
  q.opts.forEach((opt, i) => {
    const btn = document.createElement('button');
    btn.className = 'quiz-opt';
    btn.textContent = opt;
    btn.onclick = () => checkAnswer(i, btn);
    optsEl.appendChild(btn);
  });
}

function checkAnswer(idx, btn) {
  if (answered) return;
  answered = true;
  const q = questions[current];
  const resultEl = document.getElementById('quiz-result');
  const allOpts = document.querySelectorAll('.quiz-opt');
  allOpts[q.ans].classList.add('correct');
  if (idx === q.ans) {
    score++;
    resultEl.textContent = '✅ Correct! Great Mets knowledge!';
    resultEl.className = 'quiz-result show correct';
  } else {
    btn.classList.add('wrong');
    resultEl.textContent = `❌ Not quite! The answer is: ${q.opts[q.ans]}`;
    resultEl.className = 'quiz-result show wrong';
  }
  document.getElementById('quiz-next').className = current < questions.length - 1 ? 'quiz-next show' : 'quiz-next show';
  if (current === questions.length - 1) {
    document.getElementById('quiz-next').innerHTML = `<button class="btn btn-primary" onclick="showScore()">See My Score →</button>`;
  }
}

function nextQuestion() {
  current++;
  loadQuestion();
}

function showScore() {
  document.getElementById('quiz-counter').textContent = 'Quiz Complete!';
  document.getElementById('quiz-q').textContent = score >= 5 ? '🏆 You\'re a true Mets fan!' : score >= 3 ? '⚾ Not bad — keep watching!' : '📚 Time to brush up on Mets history!';
  document.getElementById('quiz-opts').innerHTML = `<div class="quiz-score">${score}<span>/${questions.length}</span></div>`;
  document.getElementById('quiz-result').className = 'quiz-result';
  document.getElementById('quiz-next').innerHTML = `<button class="btn btn-primary" onclick="restartQuiz()">Play Again</button>`;
  document.getElementById('quiz-next').className = 'quiz-next show';
}

function restartQuiz() {
  current = 0; score = 0;
  loadQuestion();
}

loadQuestion();

// ── POLL ──
function vote(el, pct) {
  const container = document.getElementById('poll-opts');
  if (container.classList.contains('poll-voted')) return;
  container.classList.add('poll-voted');
  el.classList.add('winner');
  document.querySelectorAll('.poll-opt').forEach(opt => {
    const pctVal = parseInt(opt.querySelector('.poll-pct').textContent);
    opt.querySelector('.poll-bar').style.width = pctVal + '%';
  });
}

// ── SCROLL REVEAL ──
const reveals = document.querySelectorAll('.reveal');
const observer = new IntersectionObserver((entries) => {
  entries.forEach((entry, i) => {
    if (entry.isIntersecting) {
      setTimeout(() => entry.target.classList.add('visible'), i * 50);
      observer.unobserve(entry.target);
    }
  });
}, { threshold: 0.08 });
reveals.forEach(el => observer.observe(el));
</script>
</body>
</html>
