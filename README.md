<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>West Ham vs Leeds | FA Cup QF Stats Predictor</title>
<link rel="preconnect" href="https://fonts.googleapis.com">
<link href="https://fonts.googleapis.com/css2?family=Oswald:wght@400;500;600;700&family=Nunito+Sans:wght@300;400;600;700&display=swap" rel="stylesheet">
<style>
/* ═══════════════════════════════════
   TOKENS
═══════════════════════════════════ */
:root {
  --bg:        #0b0d11;
  --bg-2:      #12151c;
  --bg-3:      #181d27;
  --bg-4:      #1e2533;
  --border:    rgba(255,255,255,0.07);
  --border-md: rgba(255,255,255,0.11);
  --text:      #7b91d1;
  --muted:     #6e788f;
  --muted-hi:  #9ca5bc;
  /* West Ham: claret + sky blue */
  --whu-1:     #7a003c;
  --whu-2:     #b51b5e;
  --whu-3:     #00b2e3;
  --whu-glow:  rgba(181,27,94,0.18);
  /* Leeds: white + yellow + blue */
  --lut-1:     #1d428a;
  --lut-2:     #3060c0;
  --lut-3:     #ffcd00;
  --lut-glow:  rgba(48,96,192,0.18);
  /* UI */
  --gold:      #f5c842;
  --low:       #3edc8a;
  --high:      #ff7043;
  --radius:    14px;
}

*, *::before, *::after { margin:0; padding:0; box-sizing:border-box; }
html { scroll-behavior:smooth; }
body {
  font-family: 'Nunito Sans', sans-serif;
  background: var(--bg);
  color: var(--text);
  min-height: 100vh;
  font-size: 14px;
  line-height: 1.55;
  -webkit-font-smoothing: antialiased;
}

/* ═══════════════════════════════════
   GLOBAL SITE HEADER
═══════════════════════════════════ */
.site-header {
  background: var(--bg-2);
  border-bottom: 1px solid var(--border);
  padding: 20px 16px 18px;
  text-align: center;
  position: relative;
  overflow: hidden;
}
.site-header::before {
  content:'';
  position:absolute; inset:0;
  background: radial-gradient(ellipse 80% 140% at 50% -10%, rgba(245,200,66,0.06), transparent 65%);
  pointer-events:none;
}
.cup-tag {
  display:inline-block;
  background: var(--gold);
  color:#000;
  font-family:'Oswald',sans-serif;
  font-size:10px; font-weight:700; letter-spacing:2px; text-transform:uppercase;
  padding:3px 11px; border-radius:3px; margin-bottom:10px;
}
.site-header h1 {
  font-family:'Oswald',sans-serif;
  font-size:24px; font-weight:700; letter-spacing:1px;
  color:#fff; text-transform:uppercase; line-height:1.1;
}
.site-header .tagline {
  font-size:12px; color:var(--muted); margin-top:5px; letter-spacing:0.3px;
}

/* ═══════════════════════════════════
   MATCHUP HERO — BADGE + SCORE
═══════════════════════════════════ */
.matchup-hero {
  background: var(--bg-2);
  border-bottom: 1px solid var(--border);
  padding: 24px 16px 20px;
  position: relative;
  overflow: hidden;
}
.matchup-hero::before {
  content:'';
  position:absolute; inset:0;
  background: linear-gradient(135deg, var(--whu-glow) 0%, transparent 50%, var(--lut-glow) 100%);
  pointer-events:none;
}
.hero-inner {
  max-width: 600px;
  margin: 0 auto;
  display: flex;
  align-items: center;
  justify-content: space-between;
  gap: 12px;
}
.hero-team {
  display: flex;
  flex-direction: column;
  align-items: center;
  gap: 8px;
  flex: 1;
}
.badge-wrap {
  width: 72px; height: 72px;
  display: flex; align-items: center; justify-content: center;
  filter: drop-shadow(0 4px 14px rgba(0,0,0,0.5));
  transition: transform 0.3s ease;
}
.badge-wrap:hover { transform: scale(1.06); }
.badge-wrap svg { width:100%; height:100%; }
.hero-team-name {
  font-family:'Oswald',sans-serif;
  font-size:14px; font-weight:600; text-transform:uppercase;
  letter-spacing:0.8px; text-align:center; color:#fff;
  line-height: 1.2;
}
.hero-team-pos {
  font-size:10px; color:var(--muted);
  font-family:'Oswald',sans-serif; letter-spacing:0.5px;
  text-transform:uppercase;
}
.hero-vs-block {
  display: flex;
  flex-direction: column;
  align-items: center;
  gap: 4px;
  flex-shrink: 0;
}
.hero-vs {
  font-family:'Oswald',sans-serif;
  font-size:28px; font-weight:700; color:rgba(255,255,255,0.15);
  line-height:1;
}
.hero-meta {
  font-size:10px; color:var(--muted); text-align:center;
  line-height:1.5; letter-spacing:0.3px;
}

/* ═══════════════════════════════════
   PAGE LAYOUT
═══════════════════════════════════ */
.page {
  max-width: 680px;
  margin: 0 auto;
  padding: 20px 14px 56px;
}

/* ═══════════════════════════════════
   SECTION CARDS
═══════════════════════════════════ */
.card {
  background: var(--bg-2);
  border: 1px solid var(--border);
  border-radius: var(--radius);
  overflow: hidden;
  margin-bottom: 18px;
}
.card-header {
  padding: 14px 18px 12px;
  border-bottom: 1px solid var(--border);
  display: flex;
  align-items: center;
  gap: 8px;
}
.card-header-icon {
  width: 6px; height: 6px; border-radius: 50%; flex-shrink: 0;
}
.card-title {
  font-family:'Oswald',sans-serif;
  font-size:11px; font-weight:600; letter-spacing:1.8px; text-transform:uppercase;
  color:var(--muted);
  flex: 1;
}
.card-body { padding: 16px 18px; }

/* ═══════════════════════════════════
   CONTEXT CALLOUT
═══════════════════════════════════ */
.callout {
  background: rgba(255,255,255,0.025);
  border: 1px solid var(--border-md);
  border-radius: 8px;
  padding: 13px 15px;
  font-size:13px; line-height:1.7; color:var(--muted-hi);
}
.callout strong { color:var(--gold); font-weight:700; }

/* ═══════════════════════════════════
   FORM GRID — two-col on >= 500px
═══════════════════════════════════ */
.form-grid {
  display:flex; flex-direction:column; gap:14px;
}
.form-col { }

.team-form-label {
  display:inline-flex; align-items:center; gap:6px;
  font-family:'Oswald',sans-serif; font-size:11px; font-weight:600;
  letter-spacing:1px; text-transform:uppercase;
  padding:3px 8px 3px 6px; border-radius:4px; margin-bottom:9px;
}
.team-form-label.whu { background:rgba(181,27,94,0.13); color:var(--whu-2); border:1px solid rgba(181,27,94,0.25); }
.team-form-label.lut { background:rgba(48,96,192,0.13); color:#7ca4f0; border:1px solid rgba(48,96,192,0.28); }
.label-badge { width:16px; height:16px; flex-shrink:0; }

.match-list { display:flex; flex-direction:column; gap:4px; }
.match-row {
  display:grid;
  grid-template-columns: 7px 46px 1fr auto;
  align-items:center; gap:9px;
  background:var(--bg-3);
  border:1px solid var(--border);
  border-radius:7px;
  padding:8px 11px;
}
.rd { width:7px; height:7px; border-radius:50%; flex-shrink:0; }
.rd.W { background:var(--low);  box-shadow:0 0 6px rgba(62,220,138,0.45); }
.rd.D { background:var(--gold); }
.rd.L { background:var(--high); box-shadow:0 0 6px rgba(255,112,67,0.4); }
.mscore { font-family:'Oswald',sans-serif; font-size:15px; font-weight:700; color:#fff; text-align:center; }
.mopponent { font-size:12px; color:var(--text); font-weight:600; overflow:hidden; text-overflow:ellipsis; white-space:nowrap; }
.mcomp { font-size:10px; color:var(--muted); text-transform:uppercase; letter-spacing:0.4px; white-space:nowrap; text-align:right; }

.form-legend { display:flex; gap:14px; flex-wrap:wrap; margin-top:10px; }
.fl-item { display:flex; align-items:center; gap:5px; font-size:11px; color:var(--muted); }
.fl-dot { width:7px; height:7px; border-radius:50%; }

/* ═══════════════════════════════════
   SEASON AVG GRIDS
═══════════════════════════════════ */
.avg-pair { display:flex; flex-direction:column; gap:12px; }
.avg-group-label {
  font-family:'Oswald',sans-serif; font-size:10px; font-weight:600;
  letter-spacing:1px; text-transform:uppercase; margin-bottom:7px;
}
.avg-grid {
  display:grid; grid-template-columns:repeat(4, 1fr); gap:6px;
}
.avg-cell {
  background:var(--bg-3); border:1px solid var(--border); border-radius:9px;
  padding:10px 6px 8px; text-align:center;
}
.avg-cell .val { font-family:'Oswald',sans-serif; font-size:22px; font-weight:700; color:#fff; line-height:1; }
.avg-cell .lbl { font-size:9px; color:var(--muted); margin-top:3px; text-transform:uppercase; letter-spacing:0.5px; line-height:1.3; }

/* ═══════════════════════════════════
   H2H STRIP
═══════════════════════════════════ */
.h2h-strip {
  background:var(--bg-3); border:1px solid var(--border); border-radius:9px;
  padding:14px 12px; display:flex; align-items:center;
  justify-content:space-between; gap:4px;
}
.h2h-s { text-align:center; flex:1; }
.h2h-num { font-family:'Oswald',sans-serif; font-size:30px; font-weight:700; line-height:1; }
.h2h-lbl { font-size:9px; color:var(--muted); text-transform:uppercase; letter-spacing:0.7px; margin-top:3px; }
.h2h-sep { width:1px; height:40px; background:var(--border); flex-shrink:0; }

.h2h-matches { display:flex; flex-direction:column; gap:4px; margin-top:12px; }
.h2h-row {
  display:grid; grid-template-columns:1fr auto 1fr;
  align-items:center; gap:8px;
  background:var(--bg-4); border:1px solid var(--border); border-radius:6px;
  padding:7px 10px; font-size:12px;
}
.h2h-home { font-weight:600; color:var(--text); text-align:left; white-space:nowrap; overflow:hidden; text-overflow:ellipsis; }
.h2h-score-cell { font-family:'Oswald',sans-serif; font-size:15px; font-weight:700; color:#fff; text-align:center; white-space:nowrap; }
.h2h-away { font-weight:600; color:var(--text); text-align:right; white-space:nowrap; overflow:hidden; text-overflow:ellipsis; }
.h2h-comp-tag { font-size:9px; color:var(--muted); text-transform:uppercase; letter-spacing:0.5px; grid-column:1/-1; text-align:center; margin-top:-2px; }

/* ═══════════════════════════════════
   PREDICTION TABLE
═══════════════════════════════════ */
.pred-legend { display:flex; gap:16px; flex-wrap:wrap; margin-bottom:14px; }
.pl-item { display:flex; align-items:center; gap:5px; font-size:11px; color:var(--muted); }
.pl-dot { width:8px; height:8px; border-radius:50%; }

/* Scroll guard — prevents overflow on narrow viewports */
.pred-table-wrap { overflow-x:auto; -webkit-overflow-scrolling:touch; }

.pred-table {
  width:100%; border-collapse:collapse;
  table-layout:fixed;   /* critical: enforces our column widths */
  min-width:300px;      /* minimum before scroll kicks in */
}
/* Column widths — 4 columns: label | low–high | median | bar */
.pred-table col.c-metric { width:34%; }
.pred-table col.c-range  { width:28%; }
.pred-table col.c-median { width:18%; }
.pred-table col.c-bar    { width:20%; }

.pred-table thead th {
  font-family:'Oswald',sans-serif; font-size:10px; font-weight:600;
  letter-spacing:1.3px; text-transform:uppercase; color:var(--muted);
  padding:0 0 10px 0; text-align:left; white-space:nowrap; overflow:hidden;
}
.pred-table thead th.c-range-h  { text-align:center; }
.pred-table thead th.c-median-h { text-align:center; }
.pred-table thead th.c-bar-h    { text-align:center; }

.pred-table tbody td {
  padding:9px 4px; border-bottom:1px solid rgba(255,255,255,0.04);
  font-size:13px; vertical-align:middle; overflow:hidden;
}
.pred-table tbody tr:last-child td { border-bottom:none; }

/* Metric label */
.pred-table tbody td.c-metric { color:var(--muted-hi); font-size:12.5px; padding-left:0; }

/* Range cell — flex row with low/dash/high */
.pred-table tbody td.c-range { text-align:center; }
.range-inner {
  display:flex; align-items:center; justify-content:center; gap:5px;
}
.lv { font-family:'Oswald',sans-serif; font-size:18px; font-weight:700; color:var(--low); line-height:1; }
.hv { font-family:'Oswald',sans-serif; font-size:18px; font-weight:700; color:var(--high); line-height:1; }
.ds { color:rgba(255,255,255,0.18); font-size:11px; line-height:1; }

/* Median cell */
.pred-table tbody td.c-median { text-align:center; }
.med-wrap {
  display:inline-flex; flex-direction:column; align-items:center;
  gap:2px;
}
.mv {
  font-family:'Oswald',sans-serif; font-size:18px; font-weight:700;
  color:#fff; line-height:1;
}
.med-pip {
  display:block; width:18px; height:3px; border-radius:2px;
  background: linear-gradient(90deg, var(--low), var(--high));
  opacity:0.6;
}

/* Bar cell */
.pred-table tbody td.c-bar { text-align:center; }
.bar-w { width:80%; max-width:90px; height:5px; background:rgba(255,255,255,0.07); border-radius:3px; overflow:hidden; margin:0 auto; display:block; }
.bar-f { display:block; height:100%; background:linear-gradient(90deg,var(--low),var(--high)); border-radius:3px; }

/* ═══════════════════════════════════
   FOOTER
═══════════════════════════════════ */
footer {
  text-align:center; padding:18px 14px;
  font-size:10.5px; color:rgba(110,120,143,0.5);
  border-top:1px solid var(--border);
}

/* ═══════════════════════════════════
   TABLET — 640px+
═══════════════════════════════════ */
@media(min-width:640px){
  body { font-size:15px; }
  .page { max-width:880px; padding:26px 24px 64px; }

  .site-header { padding:26px 24px 22px; }
  .site-header h1 { font-size:30px; }
  .site-header .tagline { font-size:13px; }

  .matchup-hero { padding:30px 24px 26px; }
  .badge-wrap { width:88px; height:88px; }
  .hero-team-name { font-size:16px; }
  .hero-vs { font-size:36px; }
  .hero-meta { font-size:11px; }

  .card-header { padding:15px 22px 13px; }
  .card-title { font-size:11px; }
  .card-body { padding:18px 22px; }

  /* Form side-by-side */
  .form-grid { flex-direction:row; gap:18px; }
  .form-col { flex:1; min-width:0; }

  .match-row { padding:9px 13px; }
  .mscore { font-size:16px; }
  .mopponent { font-size:13px; }

  .avg-pair { flex-direction:row; gap:16px; }
  .avg-group { flex:1; }
  .avg-cell .val { font-size:24px; }

  .h2h-num { font-size:34px; }
  .lv,.hv,.mv { font-size:21px; }
  .pred-table tbody td { font-size:14px; padding:10px 6px; }
  .bar-w { max-width:110px; height:6px; }

  .callout { font-size:14px; }
}

/* ═══════════════════════════════════
   DESKTOP — 1024px+
═══════════════════════════════════ */
@media(min-width:1024px){
  .page { max-width:1100px; padding:32px 40px 72px; }

  .site-header { padding:30px 40px 26px; }
  .site-header h1 { font-size:36px; letter-spacing:1.5px; }

  .matchup-hero { padding:34px 40px 28px; }
  .hero-inner { max-width:700px; }
  .badge-wrap { width:100px; height:100px; }
  .hero-team-name { font-size:17px; }
  .hero-vs { font-size:40px; }

  /* Desktop: 2-col layout for content */
  .desktop-grid {
    display:grid;
    grid-template-columns:1fr 1fr;
    gap:22px;
    align-items:start;
  }
  /* Cards that span full width */
  .desktop-grid .full-width { grid-column:1/-1; }

  .card-header { padding:16px 24px 14px; }
  .card-body { padding:20px 24px; }

  .avg-cell .val { font-size:26px; }
  .h2h-num { font-size:38px; }
  .lv,.hv { font-size:23px; }
  .pred-table tbody td { font-size:14px; padding:10px 8px 10px 0; }
  .bar-w { max-width:110px; }

  .callout { font-size:14px; line-height:1.75; }
}

/* ═══════════════════════════════════
   WIDE — 1360px+
═══════════════════════════════════ */
@media(min-width:1360px){
  .page { max-width:1400px; padding:36px 60px 80px; }
  .site-header { padding:34px 60px 28px; }
  .site-header h1 { font-size:42px; }
  .matchup-hero { padding:36px 60px 30px; }
  .hero-inner { max-width:780px; }
  .badge-wrap { width:110px; height:110px; }
  .desktop-grid { gap:28px; }
}
</style>
</head>
<body>

<!-- ─── SITE HEADER ─── -->
<header class="site-header">
  <div class="cup-tag">⚽ Emirates FA Cup · Quarter-Finals · 5 April 2026</div>
  <h1>Team Bilbo Match Predictor</h1>
  <p class="tagline">Last 5 form &nbsp;·&nbsp; Season averages &nbsp;·&nbsp; Head-to-head &nbsp;·&nbsp; Predicted stat ranges</p>
</header>

<!-- ─── MATCHUP HERO ─── -->
<div class="matchup-hero">
  <div class="hero-inner">

    <!-- WEST HAM -->
    <div class="hero-team">
      <div class="badge-wrap">
        <!-- West Ham United SVG Badge -->
        <svg viewBox="0 0 100 120" xmlns="http://www.w3.org/2000/svg">
          <defs>
            <linearGradient id="whuShield" x1="0%" y1="0%" x2="100%" y2="100%">
              <stop offset="0%" stop-color="#8a0040"/>
              <stop offset="100%" stop-color="#b51b5e"/>
            </linearGradient>
          </defs>
          <!-- Shield shape -->
          <path d="M50 4 L96 20 L96 68 Q96 100 50 116 Q4 100 4 68 L4 20 Z"
                fill="url(#whuShield)" stroke="#c4225a" stroke-width="1.5"/>
          <!-- Claret band -->
          <path d="M50 4 L96 20 L96 68 Q96 100 50 116 Q4 100 4 68 L4 20 Z"
                fill="none" stroke="rgba(255,255,255,0.12)" stroke-width="3"/>
          <!-- Crossed hammers (simplified) -->
          <!-- Hammer 1 (left) -->
          <g transform="translate(25,35) rotate(-35,25,35)">
            <rect x="22" y="10" width="6" height="30" rx="2" fill="#00b2e3"/>
            <rect x="14" y="8" width="22" height="10" rx="3" fill="#00c8ff"/>
          </g>
          <!-- Hammer 2 (right) -->
          <g transform="translate(55,35) rotate(35,25,35)">
            <rect x="22" y="10" width="6" height="30" rx="2" fill="#00b2e3"/>
            <rect x="14" y="8" width="22" height="10" rx="3" fill="#00c8ff"/>
          </g>
          <!-- Castle / West Ham motif bar -->
          <rect x="20" y="80" width="60" height="14" rx="3" fill="rgba(255,255,255,0.08)"/>
          <text x="50" y="92" text-anchor="middle" font-family="Georgia,serif" font-size="8" font-weight="bold" fill="rgba(255,255,255,0.7)" letter-spacing="1">WEST HAM</text>
        </svg>
      </div>
      <div class="hero-team-name">West Ham<br>United</div>
      <div class="hero-team-pos">18th · 29 pts</div>
    </div>

    <!-- VS -->
    <div class="hero-vs-block">
      <div class="hero-vs">VS</div>
      <div class="hero-meta">London Stadium<br>Sun 5 Apr · 4:30pm BST<br>FA Cup Quarter-Final</div>
    </div>

    <!-- LEEDS -->
    <div class="hero-team">
      <div class="badge-wrap">
        <!-- Leeds United SVG Badge -->
        <svg viewBox="0 0 100 120" xmlns="http://www.w3.org/2000/svg">
          <defs>
            <linearGradient id="lutShield" x1="0%" y1="0%" x2="100%" y2="100%">
              <stop offset="0%" stop-color="#1a3a80"/>
              <stop offset="100%" stop-color="#2654b8"/>
            </linearGradient>
          </defs>
          <!-- Shield -->
          <path d="M50 4 L96 20 L96 68 Q96 100 50 116 Q4 100 4 68 L4 20 Z"
                fill="url(#lutShield)" stroke="#2e5cd4" stroke-width="1.5"/>
          <path d="M50 4 L96 20 L96 68 Q96 100 50 116 Q4 100 4 68 L4 20 Z"
                fill="none" stroke="rgba(255,255,255,0.1)" stroke-width="3"/>
          <!-- Leeds United peace / smiley badge circle -->
          <circle cx="50" cy="52" r="28" fill="none" stroke="#ffcd00" stroke-width="2.5"/>
          <!-- Stylised "LUFC" owl eye motif — simplified arms raised figure -->
          <!-- Body -->
          <circle cx="50" cy="50" r="10" fill="#ffcd00"/>
          <!-- Face - simple smiley eyes -->
          <circle cx="46" cy="47" r="2.5" fill="#1a3a80"/>
          <circle cx="54" cy="47" r="2.5" fill="#1a3a80"/>
          <!-- Smile -->
          <path d="M44 54 Q50 60 56 54" fill="none" stroke="#1a3a80" stroke-width="2" stroke-linecap="round"/>
          <!-- Arms raised (the famous pose) -->
          <line x1="28" y1="38" x2="42" y2="48" stroke="#ffcd00" stroke-width="3" stroke-linecap="round"/>
          <line x1="72" y1="38" x2="58" y2="48" stroke="#ffcd00" stroke-width="3" stroke-linecap="round"/>
          <!-- Legs -->
          <line x1="44" y1="60" x2="40" y2="74" stroke="#ffcd00" stroke-width="2.5" stroke-linecap="round"/>
          <line x1="56" y1="60" x2="60" y2="74" stroke="#ffcd00" stroke-width="2.5" stroke-linecap="round"/>
          <!-- Banner -->
          <rect x="18" y="80" width="64" height="14" rx="3" fill="rgba(255,205,0,0.12)"/>
          <text x="50" y="92" text-anchor="middle" font-family="Georgia,serif" font-size="8" font-weight="bold" fill="#ffcd00" letter-spacing="1">LEEDS UTD</text>
        </svg>
      </div>
      <div class="hero-team-name">Leeds<br>United</div>
      <div class="hero-team-pos">15th · 33 pts</div>
    </div>

  </div>
</div>

<!-- ─── PAGE ─── -->
<div class="page">
<div class="desktop-grid">

  <!-- ══════════════════════════════
       MATCH CONTEXT
  ═════════════════════════════════ -->
  <div class="card full-width">
    <div class="card-header">
      <div class="card-header-icon" style="background:var(--gold)"></div>
      <div class="card-title">Match Context</div>
    </div>
    <div class="card-body">
      <div class="callout">
        A <strong>Premier League relegation battle played out on the FA Cup stage.</strong> West Ham sit 18th (29pts, two points from safety) while Leeds are 15th (33pts, four points clear). A Wembley semi-final is the carrot — but both managers know what happens if they over-rotate. West Ham reached this stage via a <strong>penalty shootout against Brentford</strong> after a 2–2 draw; Leeds demolished Norwich <strong>3–0</strong>. The H2H record is balanced: 2 wins each in the last 5 meetings, with BTTS in 4 of those 5 games and over 2.5 goals in all four they've met in this current PL season cycle. <strong>Injuries:</strong> West Ham missing Fabianski &amp; Mavropanos (out), Todibo &amp; Summerville doubts. Leeds almost fully fit — Gudmundsson back from suspension, Calvert-Lewin a slight doubt.
      </div>
    </div>
  </div>

  <!-- ══════════════════════════════
       LAST 5 FORM
  ═════════════════════════════════ -->
  <div class="card full-width">
    <div class="card-header">
      <div class="card-header-icon" style="background:var(--whu-3)"></div>
      <div class="card-title">Last 5 Matches — All Competitions</div>
    </div>
    <div class="card-body">
      <div class="form-grid">

        <!-- WEST HAM -->
        <div class="form-col">
          <div class="team-form-label whu">
            <!-- Tiny WHU badge -->
            <svg class="label-badge" viewBox="0 0 100 120" xmlns="http://www.w3.org/2000/svg">
              <path d="M50 4 L96 20 L96 68 Q96 100 50 116 Q4 100 4 68 L4 20 Z" fill="#8a0040"/>
              <g transform="translate(25,35) rotate(-35,25,35)">
                <rect x="22" y="10" width="6" height="28" rx="2" fill="#00b2e3"/>
                <rect x="14" y="8" width="22" height="9" rx="2" fill="#00c8ff"/>
              </g>
              <g transform="translate(55,35) rotate(35,25,35)">
                <rect x="22" y="10" width="6" height="28" rx="2" fill="#00b2e3"/>
                <rect x="14" y="8" width="22" height="9" rx="2" fill="#00c8ff"/>
              </g>
            </svg>
            West Ham · 18th
          </div>
          <div class="match-list">
            <div class="match-row"><div class="rd L"></div><div class="mscore">0–2</div><div class="mopponent">Aston Villa</div><div class="mcomp">PL · Away</div></div>
            <div class="match-row"><div class="rd D"></div><div class="mscore">2–2</div><div class="mopponent">Brentford</div><div class="mcomp">FAC · Home</div></div>
            <div class="match-row"><div class="rd D"></div><div class="mscore">1–1</div><div class="mopponent">Manchester City</div><div class="mcomp">PL · Home</div></div>
            <div class="match-row"><div class="rd W"></div><div class="mscore">1–0</div><div class="mopponent">Fulham</div><div class="mcomp">PL · Home</div></div>
            <div class="match-row"><div class="rd L"></div><div class="mscore">2–5</div><div class="mopponent">Liverpool</div><div class="mcomp">PL · Away</div></div>
          </div>
        </div>

        <!-- LEEDS -->
        <div class="form-col">
          <div class="team-form-label lut">
            <!-- Tiny LUT badge -->
            <svg class="label-badge" viewBox="0 0 100 120" xmlns="http://www.w3.org/2000/svg">
              <path d="M50 4 L96 20 L96 68 Q96 100 50 116 Q4 100 4 68 L4 20 Z" fill="#1a3a80"/>
              <circle cx="50" cy="52" r="28" fill="none" stroke="#ffcd00" stroke-width="3"/>
              <circle cx="50" cy="50" r="10" fill="#ffcd00"/>
              <circle cx="46" cy="47" r="2.5" fill="#1a3a80"/>
              <circle cx="54" cy="47" r="2.5" fill="#1a3a80"/>
            </svg>
            Leeds · 15th
          </div>
          <div class="match-list">
            <div class="match-row"><div class="rd D"></div><div class="mscore">0–0</div><div class="mopponent">Brentford</div><div class="mcomp">PL · Home</div></div>
            <div class="match-row"><div class="rd D"></div><div class="mscore">0–0</div><div class="mopponent">Crystal Palace</div><div class="mcomp">PL · Away</div></div>
            <div class="match-row"><div class="rd L"></div><div class="mscore">0–1</div><div class="mopponent">Sunderland</div><div class="mcomp">PL · Home</div></div>
            <div class="match-row"><div class="rd W"></div><div class="mscore">3–0</div><div class="mopponent">Norwich City</div><div class="mcomp">FAC · Home</div></div>
            <div class="match-row"><div class="rd L"></div><div class="mscore">0–1</div><div class="mopponent">Manchester City</div><div class="mcomp">PL · Away</div></div>
          </div>
        </div>

      </div>
      <div class="form-legend">
        <div class="fl-item"><div class="fl-dot" style="background:var(--low)"></div>Win</div>
        <div class="fl-item"><div class="fl-dot" style="background:var(--gold)"></div>Draw</div>
        <div class="fl-item"><div class="fl-dot" style="background:var(--high)"></div>Loss</div>
      </div>
    </div>
  </div>

  <!-- ══════════════════════════════
       SEASON AVERAGES
  ═════════════════════════════════ -->
  <div class="card full-width">
    <div class="card-header">
      <div class="card-header-icon" style="background:#a78bfa"></div>
      <div class="card-title">Season Averages per Match — Premier League 25/26</div>
    </div>
    <div class="card-body">
      <div class="avg-pair">

        <div class="avg-group">
          <div class="avg-group-label" style="color:var(--whu-2)">
            <svg style="width:14px;height:14px;vertical-align:middle;margin-right:4px" viewBox="0 0 100 120" xmlns="http://www.w3.org/2000/svg">
              <path d="M50 4 L96 20 L96 68 Q96 100 50 116 Q4 100 4 68 L4 20 Z" fill="#8a0040"/>
            </svg>
            West Ham United
          </div>
          <div class="avg-grid">
            <div class="avg-cell"><div class="val">10.1</div><div class="lbl">Shots</div></div>
            <div class="avg-cell"><div class="val">3.4</div><div class="lbl">SOT</div></div>
            <div class="avg-cell"><div class="val">5.2</div><div class="lbl">Corners</div></div>
            <div class="avg-cell"><div class="val">10.8</div><div class="lbl">Fouls</div></div>
          </div>
          <div class="avg-grid" style="margin-top:6px">
            <div class="avg-cell"><div class="val">14.9</div><div class="lbl">Tackles</div></div>
            <div class="avg-cell"><div class="val">1.9</div><div class="lbl">Offsides</div></div>
            <div class="avg-cell"><div class="val">41.9%</div><div class="lbl">Possess.</div></div>
            <div class="avg-cell"><div class="val">11.5</div><div class="lbl">Corners in game</div></div>
          </div>
        </div>

        <div class="avg-group">
          <div class="avg-group-label" style="color:var(--lut-3)">
            <svg style="width:14px;height:14px;vertical-align:middle;margin-right:4px" viewBox="0 0 100 120" xmlns="http://www.w3.org/2000/svg">
              <path d="M50 4 L96 20 L96 68 Q96 100 50 116 Q4 100 4 68 L4 20 Z" fill="#1a3a80"/>
            </svg>
            Leeds United
          </div>
          <div class="avg-grid">
            <div class="avg-cell"><div class="val">12.5</div><div class="lbl">Shots</div></div>
            <div class="avg-cell"><div class="val">3.9</div><div class="lbl">SOT</div></div>
            <div class="avg-cell"><div class="val">4.1</div><div class="lbl">Corners</div></div>
            <div class="avg-cell"><div class="val">11.2</div><div class="lbl">Fouls</div></div>
          </div>
          <div class="avg-grid" style="margin-top:6px">
            <div class="avg-cell"><div class="val">15.9</div><div class="lbl">Tackles</div></div>
            <div class="avg-cell"><div class="val">2.0</div><div class="lbl">Offsides</div></div>
            <div class="avg-cell"><div class="val">53.0%</div><div class="lbl">Possess.</div></div>
            <div class="avg-cell"><div class="val">8.1</div><div class="lbl">Corners in game</div></div>
          </div>
        </div>

      </div>
    </div>
  </div>

  <!-- ══════════════════════════════
       HEAD TO HEAD
  ═════════════════════════════════ -->
  <div class="card full-width">
    <div class="card-header">
      <div class="card-header-icon" style="background:var(--high)"></div>
      <div class="card-title">Head to Head — Last 5 Meetings</div>
    </div>
    <div class="card-body">
      <div class="h2h-strip">
        <div class="h2h-s">
          <div class="h2h-num" style="color:var(--whu-2)">2</div>
          <div class="h2h-lbl">West Ham Wins</div>
        </div>
        <div class="h2h-sep"></div>
        <div class="h2h-s">
          <div class="h2h-num" style="color:var(--gold)">1</div>
          <div class="h2h-lbl">Draw</div>
        </div>
        <div class="h2h-sep"></div>
        <div class="h2h-s">
          <div class="h2h-num" style="color:#7ca4f0">2</div>
          <div class="h2h-lbl">Leeds Wins</div>
        </div>
        <div class="h2h-sep"></div>
        <div class="h2h-s">
          <div class="h2h-num">4/5</div>
          <div class="h2h-lbl">BTTS Games</div>
        </div>
      </div>

      <div class="h2h-matches" style="margin-top:14px">
        <div class="h2h-row">
          <div class="h2h-home">Leeds United</div>
          <div class="h2h-score-cell">2 – 1</div>
          <div class="h2h-away">West Ham</div>
          <div class="h2h-comp-tag">Premier League · Oct 2025</div>
        </div>
        <div class="h2h-row">
          <div class="h2h-home">West Ham</div>
          <div class="h2h-score-cell">2 – 2</div>
          <div class="h2h-away">Leeds United</div>
          <div class="h2h-comp-tag">Premier League · 2024–25</div>
        </div>
        <div class="h2h-row">
          <div class="h2h-home">West Ham</div>
          <div class="h2h-score-cell">3 – 1</div>
          <div class="h2h-away">Leeds United</div>
          <div class="h2h-comp-tag">Premier League · May 2023</div>
        </div>
        <div class="h2h-row">
          <div class="h2h-home">Leeds United</div>
          <div class="h2h-score-cell">2 – 2</div>
          <div class="h2h-away">West Ham</div>
          <div class="h2h-comp-tag">Premier League · Jan 2023</div>
        </div>
        <div class="h2h-row">
          <div class="h2h-home">West Ham</div>
          <div class="h2h-score-cell">2 – 0</div>
          <div class="h2h-away">Leeds United</div>
          <div class="h2h-comp-tag">FA Cup · Jan 2022</div>
        </div>
      </div>
      <p style="font-size:11px;color:var(--muted);margin-top:10px;">Over 2.5 goals in all five recent meetings. West Ham won the last FA Cup encounter 2–0 in Jan 2022. BTTS in 4 of the last 5 clashes — these sides score against each other freely.</p>
    </div>
  </div>

  <!-- ══════════════════════════════
       PREDICTION TABLE
  ═════════════════════════════════ -->
  <div class="card full-width">
    <div class="card-header">
      <div class="card-header-icon" style="background:var(--low)"></div>
      <div class="card-title">📊 Predicted Ranges — Both Teams Combined</div>
    </div>
    <div class="card-body">
      <div class="pred-legend">
        <div class="pl-item"><div class="pl-dot" style="background:var(--low)"></div><span style="color:var(--low);font-weight:700">Low</span>&nbsp;= minimum expected</div>
        <div class="pl-item"><div class="pl-dot" style="background:#fff;opacity:0.8"></div><span style="color:#fff;font-weight:700">Median</span>&nbsp;= average-based expected</div>
        <div class="pl-item"><div class="pl-dot" style="background:var(--high)"></div><span style="color:var(--high);font-weight:700">High</span>&nbsp;= maximum expected</div>
      </div>
      <div class="pred-table-wrap">
      <table class="pred-table">
        <colgroup>
          <col class="c-metric">
          <col class="c-range">
          <col class="c-median">
          <col class="c-bar">
        </colgroup>
        <thead>
          <tr>
            <th>Metric</th>
            <th class="c-range-h">Low &nbsp;—&nbsp; High</th>
            <th class="c-median-h">Median</th>
            <th class="c-bar-h">Intensity</th>
          </tr>
        </thead>
        <tbody>
          <tr>
            <td class="c-metric">Corners</td>
            <td class="c-range"><div class="range-inner"><span class="lv">8</span><span class="ds">—</span><span class="hv">13</span></div></td>
            <td class="c-median"><div class="med-wrap"><span class="mv">10</span><span class="med-pip"></span></div></td>
            <td class="c-bar"><div class="bar-w"><div class="bar-f" style="width:60%"></div></div></td>
          </tr>
          <tr>
            <td class="c-metric">Total Shots</td>
            <td class="c-range"><div class="range-inner"><span class="lv">18</span><span class="ds">—</span><span class="hv">30</span></div></td>
            <td class="c-median"><div class="med-wrap"><span class="mv">23</span><span class="med-pip"></span></div></td>
            <td class="c-bar"><div class="bar-w"><div class="bar-f" style="width:68%"></div></div></td>
          </tr>
          <tr>
            <td class="c-metric">Shots on Target</td>
            <td class="c-range"><div class="range-inner"><span class="lv">5</span><span class="ds">—</span><span class="hv">11</span></div></td>
            <td class="c-median"><div class="med-wrap"><span class="mv">7</span><span class="med-pip"></span></div></td>
            <td class="c-bar"><div class="bar-w"><div class="bar-f" style="width:52%"></div></div></td>
          </tr>
          <tr>
            <td class="c-metric">Fouls</td>
            <td class="c-range"><div class="range-inner"><span class="lv">19</span><span class="ds">—</span><span class="hv">30</span></div></td>
            <td class="c-median"><div class="med-wrap"><span class="mv">22</span><span class="med-pip"></span></div></td>
            <td class="c-bar"><div class="bar-w"><div class="bar-f" style="width:62%"></div></div></td>
          </tr>
          <tr>
            <td class="c-metric">Throw-ins</td>
            <td class="c-range"><div class="range-inner"><span class="lv">36</span><span class="ds">—</span><span class="hv">52</span></div></td>
            <td class="c-median"><div class="med-wrap"><span class="mv">44</span><span class="med-pip"></span></div></td>
            <td class="c-bar"><div class="bar-w"><div class="bar-f" style="width:66%"></div></div></td>
          </tr>
          <tr>
            <td class="c-metric">Goal Kicks</td>
            <td class="c-range"><div class="range-inner"><span class="lv">14</span><span class="ds">—</span><span class="hv">24</span></div></td>
            <td class="c-median"><div class="med-wrap"><span class="mv">19</span><span class="med-pip"></span></div></td>
            <td class="c-bar"><div class="bar-w"><div class="bar-f" style="width:58%"></div></div></td>
          </tr>
          <tr>
            <td class="c-metric">Tackles</td>
            <td class="c-range"><div class="range-inner"><span class="lv">28</span><span class="ds">—</span><span class="hv">46</span></div></td>
            <td class="c-median"><div class="med-wrap"><span class="mv">31</span><span class="med-pip"></span></div></td>
            <td class="c-bar"><div class="bar-w"><div class="bar-f" style="width:70%"></div></div></td>
          </tr>
          <tr>
            <td class="c-metric">Offsides</td>
            <td class="c-range"><div class="range-inner"><span class="lv">2</span><span class="ds">—</span><span class="hv">7</span></div></td>
            <td class="c-median"><div class="med-wrap"><span class="mv">4</span><span class="med-pip"></span></div></td>
            <td class="c-bar"><div class="bar-w"><div class="bar-f" style="width:44%"></div></div></td>
          </tr>
        </tbody>
      </table>
      </div>
    </div>
  </div>

  <!-- ══════════════════════════════
       ANALYTICAL NOTES
  ═════════════════════════════════ -->
  <div class="card full-width">
    <div class="card-header">
      <div class="card-header-icon" style="background:#60a5fa"></div>
      <div class="card-title">Analytical Notes</div>
    </div>
    <div class="card-body">
      <div class="callout">
        <strong>Corners (8–13):</strong> Games involving West Ham average 11.5 total corners; Leeds games average just 8.1. The divergence reflects Leeds' low-block / counter-attack tendencies under Farke (57% possession opponents often dominate corners against them). West Ham earn ~5.2 per match at home and will press forward. High end if West Ham dominate territory as expected, low end if Leeds exploit space and the game stays tight.<br><br>

        <strong>Total Shots (18–30):</strong> West Ham average only 10.1 shots per game — one of the lowest in the PL — but Leeds average 12.5. Combined that's ~22–23 as a baseline, though the high-stakes Cup context and both sides' attacks clicking pushes the ceiling. Leeds had just 4 shots on target vs Brentford and West Ham 1 vs Aston Villa — recent form caps the low end.<br><br>

        <strong>Shots on Target (5–11):</strong> Both sides rank in the lower half of the PL for SOT (West Ham 3.4/game, Leeds 3.9). The low end (5) reflects recent poor finishing form from both clubs. The high end acknowledges the knockout nature — expect more shots in search of a winner if the scores are level late on.<br><br>

        <strong>Fouls (19–30):</strong> Both teams commit around 10–11 fouls per game individually, producing a combined season average of ~22. The high-stakes, physical nature of a cup quarter-final — especially with relegation-stressed players — pushes the ceiling to 30. Low end if the referee lets the game flow; high end with a combative midfield battle between Ampadu/Stach/Longstaff vs Soucek/Fernandes.<br><br>

        <strong>Throw-ins (36–52):</strong> Leeds and West Ham both play direct football and contest wide areas. West Ham's limited possession (41.9%) means opponents launch frequent restarts against them. Leeds' 57% possession away will generate pressure in wide channels. High end if the game is physically contested with lots of transitions along both touchlines.<br><br>

        <strong>Goal Kicks (14–24):</strong> With West Ham sitting lower and launching long balls at times, and Leeds' Lucas Perri comfortable distributing under pressure, goal kicks will be frequent. High end if both GKs face sustained pressure — particularly West Ham's backup keeper. Low end if possession periods reduce the frequency of clearances over the line.<br><br>

        <strong>Tackles (28–46):</strong> Combined, West Ham (14.9/game) and Leeds (15.9/game) average ~31 tackles per match — the highest tackle rate of any of the four quarter-finals this weekend. Both teams are physically intense, fight-for-every-ball sides. Farke's pressing system and Nuno's aggressive transitions mean this will be the most tackle-dense game of the four QFs. High end if both teams press at maximum intensity throughout.<br><br>

        <strong>Offsides (2–7):</strong> Both teams have one of the lowest offside rates in the PL (West Ham 1.9, Leeds 2.0 per game). Neither team runs a consistent high-line offside trap. Low end is very plausible, especially with Leeds' recent cautious away approach. The cup context and late attacking pushes nudge the ceiling toward 7.
      </div>
    </div>
  </div>

</div><!-- /desktop-grid -->
</div><!-- /page -->

<footer>
  <strong>Team Bilbo Statistical Analysis</strong><br>Predictions are statistical estimates based on actual data and contextual analysis<br>· April 5, 2026 ·
</footer>

</body>
</html>
