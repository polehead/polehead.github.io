<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>FA Cup QF | Match Stats Predictor</title>
<link rel="preconnect" href="https://fonts.googleapis.com">
<link href="https://fonts.googleapis.com/css2?family=Barlow+Condensed:wght@400;600;700;800;900&family=DM+Sans:ital,wght@0,300;0,400;0,500;0,600;1,400&display=swap" rel="stylesheet">
<style>
/* ═══════════════════════════════════════════════
   TOKENS
═══════════════════════════════════════════════ */
:root {
  --bg:           #08090d;
  --bg-2:         #0f1116;
  --bg-3:         #161a23;
  --bg-4:         #1c2130;
  --border:       rgba(255,255,255,0.07);
  --border-hi:    rgba(255,255,255,0.12);
  --text:         #dde1ec;
  --muted:        #7a839a;
  --muted-hi:     #a0a9be;
  --chelsea-a:    #00c4ee;
  --chelsea-b:    #0065a8;
  --arsenal-a:    #ef4351;
  --arsenal-b:    #b91020;
  --gold:         #f5bd45;
  --low:          #4ade80;
  --high:         #fb923c;
  --radius:       12px;
}

/* ═══════════════════════════════════════════════
   RESET & BASE
═══════════════════════════════════════════════ */
*, *::before, *::after { margin:0; padding:0; box-sizing:border-box; }
html { scroll-behavior: smooth; }
body {
  font-family: 'DM Sans', sans-serif;
  background: var(--bg);
  color: var(--text);
  min-height: 100vh;
  font-size: 14px;
  line-height: 1.55;
  -webkit-font-smoothing: antialiased;
}

/* ═══════════════════════════════════════════════
   SITE HEADER
═══════════════════════════════════════════════ */
.site-header {
  background: var(--bg-2);
  border-bottom: 1px solid var(--border);
  padding: 22px 16px 20px;
  text-align: center;
  position: relative;
  overflow: hidden;
}
.site-header::before {
  content: '';
  position: absolute;
  inset: 0;
  background: radial-gradient(ellipse 70% 120% at 50% -20%, rgba(245,189,69,0.07), transparent 70%);
  pointer-events: none;
}
.competition-tag {
  display: inline-block;
  background: var(--gold);
  color: #000;
  font-family: 'Barlow Condensed', sans-serif;
  font-size: 10px;
  font-weight: 800;
  letter-spacing: 2px;
  text-transform: uppercase;
  padding: 3px 10px;
  border-radius: 3px;
  margin-bottom: 10px;
}
.site-header h1 {
  font-family: 'Barlow Condensed', sans-serif;
  font-size: 26px;
  font-weight: 900;
  letter-spacing: 1px;
  color: #fff;
  text-transform: uppercase;
  line-height: 1.1;
}
.site-header .sub {
  font-size: 12px;
  color: var(--muted);
  margin-top: 5px;
}
.header-pills {
  display: flex;
  justify-content: center;
  gap: 8px;
  flex-wrap: wrap;
  margin-top: 14px;
}
.header-pill {
  font-family: 'Barlow Condensed', sans-serif;
  font-size: 11px;
  font-weight: 700;
  letter-spacing: 0.4px;
  text-transform: uppercase;
  padding: 5px 13px;
  border-radius: 20px;
  border: 1px solid;
}
.header-pill.chelsea { color: var(--chelsea-a); border-color: rgba(0,196,238,0.3); background: rgba(0,196,238,0.06); }
.header-pill.arsenal  { color: var(--arsenal-a); border-color: rgba(239,67,81,0.3);  background: rgba(239,67,81,0.06); }

/* ═══════════════════════════════════════════════
   PAGE — mobile-first, progressively wider
═══════════════════════════════════════════════ */
.page {
  max-width: 720px;
  margin: 0 auto;
  padding: 20px 14px 56px;
}

/* ═══════════════════════════════════════════════
   MATCH BLOCK
═══════════════════════════════════════════════ */
.match-block { margin-bottom: 32px; }

.match-title-bar {
  border-radius: var(--radius) var(--radius) 0 0;
  padding: 16px 20px;
  display: flex;
  align-items: center;
  gap: 12px;
  position: relative;
  overflow: hidden;
}
.match-title-bar.chelsea { background: linear-gradient(125deg, var(--chelsea-b), var(--chelsea-a)); }
.match-title-bar.arsenal  { background: linear-gradient(125deg, var(--arsenal-b), var(--arsenal-a)); }

.title-bar-inner { flex: 1; min-width: 0; }
.match-title-bar h2 {
  font-family: 'Barlow Condensed', sans-serif;
  font-size: 20px;
  font-weight: 900;
  letter-spacing: 0.4px;
  color: #fff;
  text-transform: uppercase;
  white-space: nowrap;
  overflow: hidden;
  text-overflow: ellipsis;
  line-height: 1.1;
}
.kickoff { font-size: 11px; color: rgba(255,255,255,0.7); margin-top: 3px; }

.match-badge { display: flex; flex-direction: column; align-items: flex-end; gap: 4px; flex-shrink: 0; }
.qf-tag {
  font-family: 'Barlow Condensed', sans-serif;
  font-size: 9px; font-weight: 800; letter-spacing: 1.5px; text-transform: uppercase;
  background: rgba(0,0,0,0.28); color: rgba(255,255,255,0.88); padding: 2px 8px; border-radius: 2px;
}
.venue-tag { font-size: 10px; color: rgba(255,255,255,0.55); }

.match-body {
  background: var(--bg-2);
  border: 1px solid var(--border);
  border-top: none;
  border-radius: 0 0 var(--radius) var(--radius);
  overflow: hidden;
}

/* ═══════════════════════════════════════════════
   SECTION
═══════════════════════════════════════════════ */
.section { padding: 18px 20px; border-bottom: 1px solid var(--border); }
.section:last-child { border-bottom: none; }

.section-label {
  font-family: 'Barlow Condensed', sans-serif;
  font-size: 10px; font-weight: 700; letter-spacing: 1.8px; text-transform: uppercase;
  color: var(--muted); margin-bottom: 14px;
  display: flex; align-items: center; gap: 8px;
}
.section-label::after { content: ''; flex: 1; height: 1px; background: var(--border); }

/* ═══════════════════════════════════════════════
   CALLOUT
═══════════════════════════════════════════════ */
.callout {
  background: rgba(255,255,255,0.03);
  border: 1px solid var(--border-hi);
  border-radius: 8px;
  padding: 13px 15px;
  font-size: 13px; line-height: 1.65; color: var(--muted-hi);
}
.callout strong { color: var(--gold); font-weight: 600; }

/* ═══════════════════════════════════════════════
   FORM
═══════════════════════════════════════════════ */
.form-teams-grid { display: flex; flex-direction: column; gap: 14px; }
.form-block { }

.pill-label {
  display: inline-block;
  font-size: 10px; font-family: 'Barlow Condensed', sans-serif;
  font-weight: 700; letter-spacing: 1px; text-transform: uppercase;
  padding: 2px 8px; border-radius: 3px; margin-bottom: 8px;
}
.pill-chelsea { background: rgba(0,196,238,0.12); color: var(--chelsea-a); border: 1px solid rgba(0,196,238,0.25); }
.pill-arsenal  { background: rgba(239,67,81,0.12);  color: #f47880;         border: 1px solid rgba(239,67,81,0.25); }

.match-list { display: flex; flex-direction: column; gap: 5px; }
.match-row {
  display: grid;
  grid-template-columns: 8px 46px 1fr auto;
  align-items: center;
  gap: 9px;
  background: var(--bg-3);
  border: 1px solid var(--border);
  border-radius: 6px;
  padding: 8px 11px;
}
.result-dot { width: 7px; height: 7px; border-radius: 50%; }
.result-dot.W { background: var(--low);  box-shadow: 0 0 5px rgba(74,222,128,0.5); }
.result-dot.D { background: var(--gold); }
.result-dot.L { background: var(--high); box-shadow: 0 0 5px rgba(251,146,60,0.4); }
.score { font-family: 'Barlow Condensed', sans-serif; font-size: 15px; font-weight: 800; color: #fff; text-align: center; }
.opponent { font-size: 12px; color: var(--text); font-weight: 500; white-space: nowrap; overflow: hidden; text-overflow: ellipsis; }
.comp { font-size: 10px; color: var(--muted); text-transform: uppercase; letter-spacing: 0.4px; text-align: right; white-space: nowrap; }

.legend { display: flex; gap: 14px; flex-wrap: wrap; margin-top: 10px; }
.legend-item { display: flex; align-items: center; gap: 5px; font-size: 11px; color: var(--muted); }
.legend-dot { width: 8px; height: 8px; border-radius: 50%; }

/* ═══════════════════════════════════════════════
   SEASON AVERAGES
═══════════════════════════════════════════════ */
.avg-group { margin-bottom: 12px; }
.avg-group:last-child { margin-bottom: 0; }
.avg-grid {
  display: grid;
  grid-template-columns: repeat(4, 1fr);
  gap: 6px;
}
.avg-item {
  background: var(--bg-3); border: 1px solid var(--border); border-radius: 8px;
  padding: 10px 8px 8px; text-align: center;
}
.avg-val { font-family: 'Barlow Condensed', sans-serif; font-size: 22px; font-weight: 800; color: #fff; line-height: 1; }
.avg-lbl { font-size: 9px; color: var(--muted); margin-top: 3px; text-transform: uppercase; letter-spacing: 0.5px; line-height: 1.3; }

/* ═══════════════════════════════════════════════
   H2H
═══════════════════════════════════════════════ */
.h2h-banner {
  background: var(--bg-3); border: 1px solid var(--border); border-radius: 8px;
  padding: 14px 12px; display: flex; align-items: center; justify-content: space-between; gap: 4px;
}
.h2h-stat { text-align: center; flex: 1; }
.h2h-val { font-family: 'Barlow Condensed', sans-serif; font-size: 28px; font-weight: 900; line-height: 1; }
.h2h-lbl { font-size: 9px; color: var(--muted); text-transform: uppercase; letter-spacing: 0.6px; margin-top: 3px; }
.h2h-div { width: 1px; height: 38px; background: var(--border); flex-shrink: 0; }

/* ═══════════════════════════════════════════════
   PREDICTION TABLE
═══════════════════════════════════════════════ */
.pred-legend { display: flex; gap: 16px; flex-wrap: wrap; margin-bottom: 12px; }
.pred-legend-item { display: flex; align-items: center; gap: 5px; font-size: 11px; color: var(--muted); }
.pred-legend-dot { width: 8px; height: 8px; border-radius: 50%; }

.pred-table { width: 100%; border-collapse: collapse; }
.pred-table thead th {
  font-family: 'Barlow Condensed', sans-serif; font-size: 10px; font-weight: 700;
  letter-spacing: 1.2px; text-transform: uppercase; color: var(--muted);
  padding: 0 4px 10px 0; text-align: left; white-space: nowrap;
}
.pred-table thead th:not(:first-child) { text-align: center; }
.pred-table tbody td {
  padding: 7px 4px 7px 0; border-bottom: 1px solid rgba(255,255,255,0.05);
  font-size: 13px; vertical-align: middle;
}
.pred-table tbody tr:last-child td { border-bottom: none; }
.pred-table tbody td:first-child { color: var(--muted-hi); font-size: 12px; }
.pred-table tbody td:not(:first-child) { text-align: center; }

.low-val  { font-family: 'Barlow Condensed', sans-serif; font-size: 19px; font-weight: 800; color: var(--low);  line-height: 1; }
.high-val { font-family: 'Barlow Condensed', sans-serif; font-size: 19px; font-weight: 800; color: var(--high); line-height: 1; }
.dash-sep { color: rgba(255,255,255,0.2); font-size: 13px; }

.bar-wrap { width: 100%; max-width: 80px; height: 5px; background: rgba(255,255,255,0.06); border-radius: 3px; overflow: hidden; margin: 0 auto; }
.bar-fill { height: 100%; background: linear-gradient(90deg, var(--low), var(--high)); border-radius: 3px; }

/* ═══════════════════════════════════════════════
   COMPARISON CARD
═══════════════════════════════════════════════ */
.comparison-card {
  background: var(--bg-2); border: 1px solid var(--border);
  border-radius: var(--radius); overflow: hidden; margin-bottom: 20px;
}
.comparison-header {
  padding: 16px 20px 14px;
  background: linear-gradient(135deg, #141826, #1e2538);
  border-bottom: 1px solid var(--border);
}
.comparison-header h3 {
  font-family: 'Barlow Condensed', sans-serif; font-size: 20px; font-weight: 800;
  text-transform: uppercase; letter-spacing: 0.5px; color: #fff; line-height: 1.1;
}
.comparison-header .comp-sub { font-size: 12px; color: var(--muted); margin-top: 3px; }
.comparison-body { padding: 18px 20px; }

.comp-table { width: 100%; border-collapse: collapse; }
.comp-table th {
  font-family: 'Barlow Condensed', sans-serif; font-size: 11px; font-weight: 700;
  letter-spacing: 1px; text-transform: uppercase; padding: 0 0 10px; white-space: nowrap;
}
.comp-table th:first-child { text-align: left; color: var(--muted); }
.comp-table th:not(:first-child) { text-align: center; min-width: 80px; }
.comp-table td { padding: 9px 0; border-bottom: 1px solid rgba(255,255,255,0.05); text-align: center; vertical-align: middle; }
.comp-table tr:last-child td { border-bottom: none; }
.comp-table td:first-child { text-align: left; color: var(--muted-hi); font-size: 13px; }
.range-val { font-family: 'Barlow Condensed', sans-serif; font-weight: 800; font-size: 17px; }

/* ═══════════════════════════════════════════════
   FOOTER
═══════════════════════════════════════════════ */
footer {
  text-align: center; padding: 20px 16px;
  font-size: 11px; color: rgba(122,131,154,0.5);
  border-top: 1px solid var(--border);
}

/* ═══════════════════════════════════════════════
   TABLET  768px+
═══════════════════════════════════════════════ */
@media (min-width: 768px) {
  body { font-size: 15px; }

  .page { max-width: 960px; padding: 28px 28px 64px; }

  .site-header { padding: 30px 28px 26px; }
  .site-header h1 { font-size: 34px; letter-spacing: 1.5px; }
  .site-header .sub { font-size: 13px; }
  .competition-tag { font-size: 11px; padding: 4px 12px; }
  .header-pill { font-size: 12px; padding: 6px 16px; }

  .match-title-bar { padding: 20px 26px; }
  .match-title-bar h2 { font-size: 26px; }
  .kickoff { font-size: 12px; }

  .section { padding: 20px 26px; }
  .section-label { font-size: 11px; margin-bottom: 16px; }

  /* Form: side by side */
  .form-teams-grid { flex-direction: row; gap: 16px; }
  .form-block { flex: 1; min-width: 0; }

  .match-row { padding: 10px 13px; gap: 11px; }
  .score { font-size: 16px; }
  .opponent { font-size: 13px; }

  .avg-grid { gap: 8px; }
  .avg-val { font-size: 26px; }
  .avg-lbl { font-size: 10px; }

  .h2h-val { font-size: 34px; }
  .h2h-lbl { font-size: 10px; }

  .low-val, .high-val { font-size: 22px; }
  .pred-table tbody td { font-size: 14px; padding: 9px 6px 9px 0; }
  .bar-wrap { max-width: 100px; height: 6px; }

  .comparison-header h3 { font-size: 22px; }
  .comp-table th:not(:first-child) { min-width: 120px; }
  .range-val { font-size: 18px; }
  .comp-table td { padding: 10px 0; }

  .callout { font-size: 14px; padding: 15px 17px; }
}

/* ═══════════════════════════════════════════════
   DESKTOP  1080px+  — Two-column match layout
═══════════════════════════════════════════════ */
@media (min-width: 1080px) {
  .page { max-width: 1380px; padding: 36px 40px 72px; }

  .site-header { padding: 34px 40px 30px; }
  .site-header h1 { font-size: 42px; letter-spacing: 2px; }
  .site-header .sub { font-size: 14px; margin-top: 6px; }
  .competition-tag { font-size: 12px; padding: 5px 14px; }
  .header-pill { font-size: 13px; padding: 6px 18px; }

  /* Matches side by side */
  .matches-grid {
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: 28px;
    align-items: start;
  }
  .match-block { margin-bottom: 0; }

  .match-title-bar { padding: 20px 26px; }
  .match-title-bar h2 { font-size: 22px; }

  .section { padding: 20px 26px; }

  /* On desktop each match column is narrower — stack form lists vertically */
  .form-teams-grid { flex-direction: column; gap: 14px; }

  .avg-val { font-size: 24px; }
  .h2h-val { font-size: 32px; }

  .low-val, .high-val { font-size: 21px; }
  .bar-wrap { max-width: 80px; }

  .comparison-wrapper { margin-top: 32px; }
  .comparison-header { padding: 18px 26px 16px; }
  .comparison-header h3 { font-size: 24px; }
  .comparison-body { padding: 20px 26px; }
  .range-val { font-size: 19px; }
  .comp-table td { padding: 11px 0; }
}

/* ═══════════════════════════════════════════════
   WIDE DESKTOP  1400px+
═══════════════════════════════════════════════ */
@media (min-width: 1400px) {
  .page { max-width: 1520px; padding: 40px 60px 80px; }
  .site-header h1 { font-size: 50px; }
  .matches-grid { gap: 36px; }
  .match-title-bar h2 { font-size: 24px; }

  /* Wide enough — show form side by side within each match column again */
  .form-teams-grid { flex-direction: row; gap: 14px; }
  .form-block { flex: 1; min-width: 0; }

  .avg-val { font-size: 26px; }
  .h2h-val { font-size: 36px; }
  .low-val, .high-val { font-size: 23px; }
  .bar-wrap { max-width: 100px; }
}
</style>
</head>
<body>

<!-- ═══════════════ HEADER ═══════════════ -->
<header class="site-header">
  <div class="competition-tag">FA Cup · Quarter-Finals · 4 April 2026</div>
  <h1>Team Bilbo Match Predictor</h1>
  <p class="sub">Last 5 form &nbsp;·&nbsp; Season averages &nbsp;·&nbsp; Head-to-head &nbsp;·&nbsp; Predicted stat ranges</p>
  <div class="header-pills">
    <span class="header-pill chelsea">Chelsea vs Port Vale · 5:15pm · Stamford Bridge</span>
    <span class="header-pill arsenal">Southampton vs Arsenal · 8:00pm · St Mary's</span>
  </div>
</header>

<div class="page">

  <!-- Two-column grid on desktop, single column on mobile/tablet -->
  <div class="matches-grid">

    <!-- ══════════════════════════════════════
         MATCH 1 — CHELSEA VS PORT VALE
    ═══════════════════════════════════════ -->
    <div class="match-block">
      <div class="match-title-bar chelsea">
        <div class="title-bar-inner">
          <h2>Chelsea &nbsp;vs&nbsp; Port Vale</h2>
          <div class="kickoff">Stamford Bridge &nbsp;·&nbsp; Saturday 4 April &nbsp;·&nbsp; 17:15</div>
        </div>
        <div class="match-badge">
          <span class="qf-tag">FA Cup QF</span>
          <span class="venue-tag">PL vs League One</span>
        </div>
      </div>

      <div class="match-body">

        <div class="section">
          <div class="section-label">Match Context</div>
          <div class="callout">
            A <strong>David vs Goliath</strong> cup tie — the first meeting in almost a century. Chelsea are Club World Cup champions but arrive in shocking form: <strong>4 consecutive defeats &amp; 3 games without a goal.</strong> Port Vale sit 14 points adrift of League One safety yet have sent Bristol City and top-flight Sunderland home already. Enzo Fernández is <strong>suspended</strong>; Jorgensen, Colwill, James, Chalobah and Mudryk are all out.
          </div>
        </div>

        <div class="section">
          <div class="section-label">Last 5 Matches</div>
          <div class="form-teams-grid">
            <div class="form-block">
              <div class="pill-label pill-chelsea">Chelsea — PL · 7th</div>
              <div class="match-list">
                <div class="match-row"><div class="result-dot L"></div><div class="score">0–3</div><div class="opponent">Everton</div><div class="comp">PL · Away</div></div>
                <div class="match-row"><div class="result-dot L"></div><div class="score">0–3</div><div class="opponent">PSG</div><div class="comp">UCL · Home</div></div>
                <div class="match-row"><div class="result-dot L"></div><div class="score">0–1</div><div class="opponent">Newcastle Utd</div><div class="comp">PL · Home</div></div>
                <div class="match-row"><div class="result-dot L"></div><div class="score">2–5</div><div class="opponent">PSG</div><div class="comp">UCL · Away</div></div>
                <div class="match-row"><div class="result-dot W"></div><div class="score">4–2</div><div class="opponent">Wrexham</div><div class="comp">FAC · Away</div></div>
              </div>
            </div>
            <div class="form-block">
              <div class="pill-label pill-chelsea">Port Vale — L1 · 24th (bottom)</div>
              <div class="match-list">
                <div class="match-row"><div class="result-dot L"></div><div class="score">0–4</div><div class="opponent">Wycombe Wndrs</div><div class="comp">L1 · Home</div></div>
                <div class="match-row"><div class="result-dot W"></div><div class="score">1–0</div><div class="opponent">Sunderland</div><div class="comp">FAC · Home</div></div>
                <div class="match-row"><div class="result-dot D"></div><div class="score">0–0</div><div class="opponent">Leyton Orient</div><div class="comp">L1 · Away</div></div>
                <div class="match-row"><div class="result-dot D"></div><div class="score">0–0</div><div class="opponent">Stevenage</div><div class="comp">L1 · Home</div></div>
                <div class="match-row"><div class="result-dot W"></div><div class="score">1–0</div><div class="opponent">Bristol City</div><div class="comp">FAC · Away</div></div>
              </div>
            </div>
          </div>
          <div class="legend">
            <div class="legend-item"><div class="legend-dot" style="background:var(--low)"></div>Win</div>
            <div class="legend-item"><div class="legend-dot" style="background:var(--gold)"></div>Draw</div>
            <div class="legend-item"><div class="legend-dot" style="background:var(--high)"></div>Loss</div>
          </div>
        </div>

        <div class="section">
          <div class="section-label">Season Averages per Match</div>
          <div class="avg-group">
            <div class="pill-label pill-chelsea" style="margin-bottom:8px">Chelsea — Premier League 25/26</div>
            <div class="avg-grid">
              <div class="avg-item"><div class="avg-val">13.7</div><div class="avg-lbl">Shots</div></div>
              <div class="avg-item"><div class="avg-val">4.7</div><div class="avg-lbl">SOT</div></div>
              <div class="avg-item"><div class="avg-val">5.1</div><div class="avg-lbl">Corners</div></div>
              <div class="avg-item"><div class="avg-val">10.3</div><div class="avg-lbl">Fouls</div></div>
            </div>
          </div>
          <div class="avg-group">
            <div class="pill-label pill-chelsea" style="margin-bottom:8px">Port Vale — League One 25/26</div>
            <div class="avg-grid">
              <div class="avg-item"><div class="avg-val">11.6</div><div class="avg-lbl">Shots</div></div>
              <div class="avg-item"><div class="avg-val">3.2</div><div class="avg-lbl">SOT</div></div>
              <div class="avg-item"><div class="avg-val">3.8</div><div class="avg-lbl">Corners</div></div>
              <div class="avg-item"><div class="avg-val">12.4</div><div class="avg-lbl">Fouls</div></div>
            </div>
          </div>
        </div>

        <div class="section">
          <div class="section-label">All-Time Head to Head</div>
          <div class="h2h-banner">
            <div class="h2h-stat"><div class="h2h-val" style="color:var(--chelsea-a)">14</div><div class="h2h-lbl">Chelsea Wins</div></div>
            <div class="h2h-div"></div>
            <div class="h2h-stat"><div class="h2h-val" style="color:var(--gold)">3</div><div class="h2h-lbl">Draws</div></div>
            <div class="h2h-div"></div>
            <div class="h2h-stat"><div class="h2h-val" style="color:var(--high)">3</div><div class="h2h-lbl">Vale Wins</div></div>
            <div class="h2h-div"></div>
            <div class="h2h-stat"><div class="h2h-val">97</div><div class="h2h-lbl">Yrs Since Last</div></div>
          </div>
          <p style="font-size:11px;color:var(--muted);margin-top:10px;">All 20 historical meetings: Div Two league fixtures 1905–1929. <em>No FA Cup meetings ever.</em> Last meeting: Port Vale 1–0 Chelsea, April 1929.</p>
        </div>

        <div class="section">
          <div class="section-label">Predicted Ranges — Both Teams Combined</div>
          <div class="pred-legend">
            <div class="pred-legend-item"><div class="pred-legend-dot" style="background:var(--low)"></div><span style="color:var(--low);font-weight:600">Low</span> = minimum expected</div>
            <div class="pred-legend-item"><div class="pred-legend-dot" style="background:var(--high)"></div><span style="color:var(--high);font-weight:600">High</span> = maximum expected</div>
          </div>
          <table class="pred-table">
            <thead><tr><th>Metric</th><th>Low</th><th></th><th>High</th><th style="text-align:center">Range</th></tr></thead>
            <tbody>
              <tr><td>Corners</td><td><span class="low-val">9</span></td><td><span class="dash-sep">—</span></td><td><span class="high-val">13</span></td><td><div class="bar-wrap"><div class="bar-fill" style="width:65%"></div></div></td></tr>
              <tr><td>Total Shots</td><td><span class="low-val">21</span></td><td><span class="dash-sep">—</span></td><td><span class="high-val">30</span></td><td><div class="bar-wrap"><div class="bar-fill" style="width:72%"></div></div></td></tr>
              <tr><td>Shots on Target</td><td><span class="low-val">6</span></td><td><span class="dash-sep">—</span></td><td><span class="high-val">11</span></td><td><div class="bar-wrap"><div class="bar-fill" style="width:55%"></div></div></td></tr>
              <tr><td>Fouls</td><td><span class="low-val">22</span></td><td><span class="dash-sep">—</span></td><td><span class="high-val">32</span></td><td><div class="bar-wrap"><div class="bar-fill" style="width:60%"></div></div></td></tr>
              <tr><td>Throw-ins</td><td><span class="low-val">38</span></td><td><span class="dash-sep">—</span></td><td><span class="high-val">54</span></td><td><div class="bar-wrap"><div class="bar-fill" style="width:70%"></div></div></td></tr>
              <tr><td>Goal Kicks</td><td><span class="low-val">14</span></td><td><span class="dash-sep">—</span></td><td><span class="high-val">24</span></td><td><div class="bar-wrap"><div class="bar-fill" style="width:58%"></div></div></td></tr>
              <tr><td>Tackles</td><td><span class="low-val">30</span></td><td><span class="dash-sep">—</span></td><td><span class="high-val">46</span></td><td><div class="bar-wrap"><div class="bar-fill" style="width:65%"></div></div></td></tr>
              <tr><td>Offsides</td><td><span class="low-val">3</span></td><td><span class="dash-sep">—</span></td><td><span class="high-val">7</span></td><td><div class="bar-wrap"><div class="bar-fill" style="width:40%"></div></div></td></tr>
            </tbody>
          </table>
        </div>

        <div class="section">
          <div class="section-label">Analytical Notes</div>
          <div class="callout">
            <strong>Corners (9–13):</strong> Chelsea's possession play generates 7–9 corners alone; Vale earn very few from a deep block.<br><br>
            <strong>Shots (21–30):</strong> Chelsea expect ~18–22; Vale's Cup pragmatism yields only ~4–8. Chelsea's alarming 3-game goalscoring drought compresses the higher end.<br><br>
            <strong>Fouls (22–32):</strong> Vale commit the majority (12–18) disrupting Chelsea attacks with League One physicality. High end if the referee allows robust challenges.<br><br>
            <strong>Throw-ins (38–54):</strong> Vale clearing long balls wide creates frequent throw-ins. High end likely given their transition-heavy defensive shape.<br><br>
            <strong>Goal Kicks (14–24):</strong> Vale's GK restarts constantly; Chelsea's keeper is less occupied given Vale's minimal attack.<br><br>
            <strong>Tackles (30–46):</strong> Vale's defensive solidity (clean sheets vs Sunderland, Bristol City) signals a tackle-heavy encounter.<br><br>
            <strong>Offsides (3–7):</strong> Vale sit very deep — low end probable. Chelsea's attackers pushing in behind are the primary source.
          </div>
        </div>

      </div>
    </div><!-- /match chelsea -->

    <!-- ══════════════════════════════════════
         MATCH 2 — SOUTHAMPTON VS ARSENAL
    ═══════════════════════════════════════ -->
    <div class="match-block">
      <div class="match-title-bar arsenal">
        <div class="title-bar-inner">
          <h2>Southampton &nbsp;vs&nbsp; Arsenal</h2>
          <div class="kickoff">St Mary's Stadium &nbsp;·&nbsp; Saturday 4 April &nbsp;·&nbsp; 20:00</div>
        </div>
        <div class="match-badge">
          <span class="qf-tag">FA Cup QF</span>
          <span class="venue-tag">Champ vs PL Leaders</span>
        </div>
      </div>

      <div class="match-body">

        <div class="section">
          <div class="section-label">Match Context</div>
          <div class="callout">
            A genuinely <strong>competitive cup tie.</strong> Southampton are <strong>unbeaten in 14 games</strong> and dumped Premier League Fulham in round 5. Arsenal lead the PL by 9 points but are deflated after losing the <strong>Carabao Cup final to Man City</strong> and are heavily depleted — Eze, Madueke, Timber and Merino all out, Odegaard a fitness doubt. Arteta likely to rotate. Southampton's Downes and Matsuki are suspended.
          </div>
        </div>

        <div class="section">
          <div class="section-label">Last 5 Matches</div>
          <div class="form-teams-grid">
            <div class="form-block">
              <div class="pill-label pill-arsenal">Southampton — Champ · 6th</div>
              <div class="match-list">
                <div class="match-row"><div class="result-dot W"></div><div class="score">2–0</div><div class="opponent">Oxford United</div><div class="comp">Champ · Home</div></div>
                <div class="match-row"><div class="result-dot W"></div><div class="score">1–0</div><div class="opponent">Norwich City</div><div class="comp">Champ · Away</div></div>
                <div class="match-row"><div class="result-dot W"></div><div class="score">2–0</div><div class="opponent">Coventry City</div><div class="comp">Champ · Home</div></div>
                <div class="match-row"><div class="result-dot D"></div><div class="score">1–1</div><div class="opponent">West Brom</div><div class="comp">Champ · Away</div></div>
                <div class="match-row"><div class="result-dot W"></div><div class="score">1–0</div><div class="opponent">Fulham</div><div class="comp">FAC · Away</div></div>
              </div>
            </div>
            <div class="form-block">
              <div class="pill-label pill-arsenal">Arsenal — PL · 1st (70pts)</div>
              <div class="match-list">
                <div class="match-row"><div class="result-dot L"></div><div class="score">0–2</div><div class="opponent">Manchester City</div><div class="comp">EFL Final</div></div>
                <div class="match-row"><div class="result-dot W"></div><div class="score">2–0</div><div class="opponent">Mansfield Town</div><div class="comp">FAC · Away</div></div>
                <div class="match-row"><div class="result-dot W"></div><div class="score">4–0</div><div class="opponent">Wigan Athletic</div><div class="comp">FAC · Home</div></div>
                <div class="match-row"><div class="result-dot W"></div><div class="score">2–1</div><div class="opponent">Chelsea</div><div class="comp">PL · Home</div></div>
                <div class="match-row"><div class="result-dot W"></div><div class="score">3–0</div><div class="opponent">Crystal Palace</div><div class="comp">PL · Away</div></div>
              </div>
            </div>
          </div>
          <div class="legend">
            <div class="legend-item"><div class="legend-dot" style="background:var(--low)"></div>Win</div>
            <div class="legend-item"><div class="legend-dot" style="background:var(--gold)"></div>Draw</div>
            <div class="legend-item"><div class="legend-dot" style="background:var(--high)"></div>Loss</div>
          </div>
        </div>

        <div class="section">
          <div class="section-label">Season Averages per Match</div>
          <div class="avg-group">
            <div class="pill-label pill-arsenal" style="margin-bottom:8px">Southampton — Championship 25/26</div>
            <div class="avg-grid">
              <div class="avg-item"><div class="avg-val">14.3</div><div class="avg-lbl">Shots</div></div>
              <div class="avg-item"><div class="avg-val">5.3</div><div class="avg-lbl">SOT</div></div>
              <div class="avg-item"><div class="avg-val">4.8</div><div class="avg-lbl">Corners</div></div>
              <div class="avg-item"><div class="avg-val">11.2</div><div class="avg-lbl">Fouls</div></div>
            </div>
          </div>
          <div class="avg-group">
            <div class="pill-label pill-arsenal" style="margin-bottom:8px">Arsenal — Premier League 25/26</div>
            <div class="avg-grid">
              <div class="avg-item"><div class="avg-val">14.7</div><div class="avg-lbl">Shots</div></div>
              <div class="avg-item"><div class="avg-val">5.0</div><div class="avg-lbl">SOT</div></div>
              <div class="avg-item"><div class="avg-val">5.8</div><div class="avg-lbl">Corners</div></div>
              <div class="avg-item"><div class="avg-val">9.8</div><div class="avg-lbl">Fouls</div></div>
            </div>
          </div>
        </div>

        <div class="section">
          <div class="section-label">Head-to-Head (Last 17 meetings)</div>
          <div class="h2h-banner">
            <div class="h2h-stat"><div class="h2h-val" style="color:var(--arsenal-a)">9</div><div class="h2h-lbl">Arsenal Wins</div></div>
            <div class="h2h-div"></div>
            <div class="h2h-stat"><div class="h2h-val" style="color:var(--gold)">4</div><div class="h2h-lbl">Draws</div></div>
            <div class="h2h-div"></div>
            <div class="h2h-stat"><div class="h2h-val" style="color:var(--low)">4</div><div class="h2h-lbl">Saints Wins</div></div>
            <div class="h2h-div"></div>
            <div class="h2h-stat"><div class="h2h-val">78%</div><div class="h2h-lbl">Arsenal Win%</div></div>
          </div>
          <p style="font-size:11px;color:var(--muted);margin-top:10px;">Arsenal unbeaten vs Southampton since 2021. At St Mary's: 2 wins each + 1 draw in last 5 meetings. Arsenal won here 2–1 on the final day of 2024–25.</p>
        </div>

        <div class="section">
          <div class="section-label">Predicted Ranges — Both Teams Combined</div>
          <div class="pred-legend">
            <div class="pred-legend-item"><div class="pred-legend-dot" style="background:var(--low)"></div><span style="color:var(--low);font-weight:600">Low</span> = minimum expected</div>
            <div class="pred-legend-item"><div class="pred-legend-dot" style="background:var(--high)"></div><span style="color:var(--high);font-weight:600">High</span> = maximum expected</div>
          </div>
          <table class="pred-table">
            <thead><tr><th>Metric</th><th>Low</th><th></th><th>High</th><th style="text-align:center">Range</th></tr></thead>
            <tbody>
              <tr><td>Corners</td><td><span class="low-val">8</span></td><td><span class="dash-sep">—</span></td><td><span class="high-val">13</span></td><td><div class="bar-wrap"><div class="bar-fill" style="width:60%"></div></div></td></tr>
              <tr><td>Total Shots</td><td><span class="low-val">22</span></td><td><span class="dash-sep">—</span></td><td><span class="high-val">34</span></td><td><div class="bar-wrap"><div class="bar-fill" style="width:78%"></div></div></td></tr>
              <tr><td>Shots on Target</td><td><span class="low-val">7</span></td><td><span class="dash-sep">—</span></td><td><span class="high-val">13</span></td><td><div class="bar-wrap"><div class="bar-fill" style="width:62%"></div></div></td></tr>
              <tr><td>Fouls</td><td><span class="low-val">18</span></td><td><span class="dash-sep">—</span></td><td><span class="high-val">28</span></td><td><div class="bar-wrap"><div class="bar-fill" style="width:55%"></div></div></td></tr>
              <tr><td>Throw-ins</td><td><span class="low-val">34</span></td><td><span class="dash-sep">—</span></td><td><span class="high-val">50</span></td><td><div class="bar-wrap"><div class="bar-fill" style="width:65%"></div></div></td></tr>
              <tr><td>Goal Kicks</td><td><span class="low-val">16</span></td><td><span class="dash-sep">—</span></td><td><span class="high-val">26</span></td><td><div class="bar-wrap"><div class="bar-fill" style="width:60%"></div></div></td></tr>
              <tr><td>Tackles</td><td><span class="low-val">28</span></td><td><span class="dash-sep">—</span></td><td><span class="high-val">44</span></td><td><div class="bar-wrap"><div class="bar-fill" style="width:62%"></div></div></td></tr>
              <tr><td>Offsides</td><td><span class="low-val">3</span></td><td><span class="dash-sep">—</span></td><td><span class="high-val">8</span></td><td><div class="bar-wrap"><div class="bar-fill" style="width:50%"></div></div></td></tr>
            </tbody>
          </table>
        </div>

        <div class="section">
          <div class="section-label">Analytical Notes</div>
          <div class="callout">
            <strong>Corners (8–13):</strong> Arsenal earn ~5.8/PL game; Southampton avg 10.7 corners/match at home. High end if the tie is open late on.<br><br>
            <strong>Shots (22–34):</strong> Both top shot-takers in their divisions. Neither side will park the bus with a Wembley semi-final at stake. High end if extra time is needed.<br><br>
            <strong>Fouls (18–28):</strong> Arsenal play through tight spaces; Southampton's energetic midfield will disrupt frequently. Lower end if the referee allows it to flow.<br><br>
            <strong>Throw-ins (34–50):</strong> Southampton's wide players (Fellows, Edozie) and Arsenal's overlapping fullbacks create frequent boundary breaks across a sold-out St Mary's.<br><br>
            <strong>Goal Kicks (16–26):</strong> Arsenal's high press means Southampton's keeper launches long balls repeatedly. Arsenal's makeshift defence invites pressure in return.<br><br>
            <strong>Tackles (28–44):</strong> Southampton's press-heavy system is tackle-intensive. Without Merino, Arsenal's midfield is exposed — high end if Arteta rotates heavily.<br><br>
            <strong>Offsides (3–8):</strong> Arsenal's high line + Southampton's pacey runners (Stewart, Larin) create traps in both directions — higher ceiling than the Chelsea match.
          </div>
        </div>

      </div>
    </div><!-- /match arsenal -->

  </div><!-- /matches-grid -->

  <!-- ═══════════════════════════════════════════
       COMPARISON SUMMARY (full-width)
  ════════════════════════════════════════════ -->
  <div class="comparison-wrapper">
    <div class="comparison-card">
      <div class="comparison-header">
        <h3>Head-to-Head Comparison</h3>
        <div class="comp-sub">Chelsea v Port Vale &nbsp;vs&nbsp; Southampton v Arsenal — all metrics side by side</div>
      </div>
      <div class="comparison-body">
        <table class="comp-table">
          <thead>
            <tr>
              <th>Metric</th>
              <th style="color:var(--chelsea-a)">CHE vs Port Vale</th>
              <th style="color:var(--arsenal-a)">SOU vs Arsenal</th>
            </tr>
          </thead>
          <tbody>
            <tr><td>Corners</td>
              <td><span class="range-val" style="color:var(--low)">9</span><span style="color:var(--muted);font-size:12px"> — </span><span class="range-val" style="color:var(--high)">13</span></td>
              <td><span class="range-val" style="color:var(--low)">8</span><span style="color:var(--muted);font-size:12px"> — </span><span class="range-val" style="color:var(--high)">13</span></td>
            </tr>
            <tr><td>Total Shots</td>
              <td><span class="range-val" style="color:var(--low)">21</span><span style="color:var(--muted);font-size:12px"> — </span><span class="range-val" style="color:var(--high)">30</span></td>
              <td><span class="range-val" style="color:var(--low)">22</span><span style="color:var(--muted);font-size:12px"> — </span><span class="range-val" style="color:var(--high)">34</span></td>
            </tr>
            <tr><td>Shots on Target</td>
              <td><span class="range-val" style="color:var(--low)">6</span><span style="color:var(--muted);font-size:12px"> — </span><span class="range-val" style="color:var(--high)">11</span></td>
              <td><span class="range-val" style="color:var(--low)">7</span><span style="color:var(--muted);font-size:12px"> — </span><span class="range-val" style="color:var(--high)">13</span></td>
            </tr>
            <tr><td>Fouls</td>
              <td><span class="range-val" style="color:var(--low)">22</span><span style="color:var(--muted);font-size:12px"> — </span><span class="range-val" style="color:var(--high)">32</span></td>
              <td><span class="range-val" style="color:var(--low)">18</span><span style="color:var(--muted);font-size:12px"> — </span><span class="range-val" style="color:var(--high)">28</span></td>
            </tr>
            <tr><td>Throw-ins</td>
              <td><span class="range-val" style="color:var(--low)">38</span><span style="color:var(--muted);font-size:12px"> — </span><span class="range-val" style="color:var(--high)">54</span></td>
              <td><span class="range-val" style="color:var(--low)">34</span><span style="color:var(--muted);font-size:12px"> — </span><span class="range-val" style="color:var(--high)">50</span></td>
            </tr>
            <tr><td>Goal Kicks</td>
              <td><span class="range-val" style="color:var(--low)">14</span><span style="color:var(--muted);font-size:12px"> — </span><span class="range-val" style="color:var(--high)">24</span></td>
              <td><span class="range-val" style="color:var(--low)">16</span><span style="color:var(--muted);font-size:12px"> — </span><span class="range-val" style="color:var(--high)">26</span></td>
            </tr>
            <tr><td>Tackles</td>
              <td><span class="range-val" style="color:var(--low)">30</span><span style="color:var(--muted);font-size:12px"> — </span><span class="range-val" style="color:var(--high)">46</span></td>
              <td><span class="range-val" style="color:var(--low)">28</span><span style="color:var(--muted);font-size:12px"> — </span><span class="range-val" style="color:var(--high)">44</span></td>
            </tr>
            <tr><td>Offsides</td>
              <td><span class="range-val" style="color:var(--low)">3</span><span style="color:var(--muted);font-size:12px"> — </span><span class="range-val" style="color:var(--high)">7</span></td>
              <td><span class="range-val" style="color:var(--low)">3</span><span style="color:var(--muted);font-size:12px"> — </span><span class="range-val" style="color:var(--high)">8</span></td>
            </tr>
          </tbody>
        </table>
        <div class="callout" style="margin-top:18px;">
          <strong>Southampton v Arsenal</strong> projects the higher shots, shots-on-target and attacking ceiling — both teams are genuinely dangerous and neither will park the bus with Wembley on the line. <strong>Chelsea v Port Vale</strong> will be the fouls and throw-ins match — Port Vale's League One physicality will disrupt Chelsea's rhythm throughout with a rugged low block, while Chelsea's extraordinary goalscoring drought (0 goals in 3 PL games) compresses the shots-on-target range for a team that should dominate.
        </div>
      </div>
    </div>
  </div>

</div><!-- /page -->

<footer>
<strong>Team Bilbo Statistical Analysis</strong><br>Data sourced from FootyStats, WhoScored, Opta Analyst, Chelsea FC, Arsenal FC & Southampton FC official sites · <strong>Predictions are statistical estimates</strong> based on available data and contextual factors · April 4, 2026.
</footer>

</body>
</html>
