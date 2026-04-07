<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>UCL QF Stats Predictor | Sporting v Arsenal · Real Madrid v Bayern</title>
<link rel="preconnect" href="https://fonts.googleapis.com">
<link href="https://fonts.googleapis.com/css2?family=Bebas+Neue&family=Mulish:wght@300;400;600;700;800&display=swap" rel="stylesheet">
<style>
/* ═══════════════════════════════════════════════
   DESIGN TOKENS
═══════════════════════════════════════════════ */
:root {
  /* base */
  --bg:       #07080d;
  --bg-2:     #0d0f18;
  --bg-3:     #131620;
  --bg-4:     #191d2c;
  --bg-5:     #1f2438;
  --border:   rgba(255,255,255,0.06);
  --border-m: rgba(255,255,255,0.11);
  --text:     #d8dced;
  --muted:    #636b84;
  --hi:       #9daac4;
  /* UCL accent */
  --ucl:      #1a48b8;
  --ucl-b:    #0f2d7a;
  --ucl-star: #c8a84b;
  /* Sporting */
  --scp-g:    #006630;
  --scp-l:    #ffcc00;
  /* Arsenal */
  --ars-r:    #db0007;
  --ars-g:    #ffffff;
  /* Real Madrid */
  --rma-w:    #fafafa;
  --rma-g:    #c4a84f;
  /* Bayern */
  --bay-r:    #dc052d;
  --bay-b:    #0066b2;
  /* stat colours */
  --low:      #34d399;
  --med:      #f9c74f;
  --high:     #ff6b35;
  --radius:   12px;
}

*, *::before, *::after { margin:0; padding:0; box-sizing:border-box; }
html { scroll-behavior:smooth; }
body {
  font-family:'Mulish',sans-serif;
  background:var(--bg);
  color:var(--text);
  min-height:100vh;
  font-size:14px;
  line-height:1.55;
  -webkit-font-smoothing:antialiased;
}

/* ═══════════════════════════════════════════════
   SITE HEADER
═══════════════════════════════════════════════ */
.site-header {
  background: linear-gradient(160deg, var(--ucl-b) 0%, var(--bg-2) 60%);
  border-bottom:1px solid rgba(200,168,75,0.2);
  padding:22px 16px 20px;
  text-align:center;
  position:relative;
  overflow:hidden;
}
.site-header::before {
  content:'';
  position:absolute; inset:0;
  background: radial-gradient(ellipse 70% 200% at 50% -30%, rgba(200,168,75,0.1), transparent 65%);
  pointer-events:none;
}
/* UCL star strip */
.star-strip {
  display:flex; justify-content:center; align-items:center; gap:6px;
  margin-bottom:10px; position:relative;
}
.star-strip::before, .star-strip::after {
  content:''; flex:1; max-width:60px; height:1px;
  background:linear-gradient(90deg, transparent, var(--ucl-star));
}
.star-strip::after {
  background:linear-gradient(90deg, var(--ucl-star), transparent);
}
.ucl-tag {
  font-family:'Bebas Neue',sans-serif;
  font-size:11px; letter-spacing:3px; text-transform:uppercase;
  color:var(--ucl-star); padding:2px 10px;
  border:1px solid rgba(200,168,75,0.35); border-radius:3px;
}
.site-header h1 {
  font-family:'Bebas Neue',sans-serif;
  font-size:28px; letter-spacing:2px; color:#fff;
  text-transform:uppercase; line-height:1.1;
}
.site-header .tagline {
  font-size:11.5px; color:var(--muted); margin-top:5px;
}

/* ═══════════════════════════════════════════════
   MATCH HERO BANNERS
═══════════════════════════════════════════════ */
.match-hero {
  padding:22px 16px 18px;
  position:relative; overflow:hidden;
  border-bottom:1px solid var(--border-m);
}
.match-hero.scp-ars {
  background: linear-gradient(135deg, rgba(0,102,48,0.18) 0%, var(--bg-2) 40%, rgba(219,0,7,0.12) 100%);
}
.match-hero.rma-bay {
  background: linear-gradient(135deg, rgba(196,168,79,0.12) 0%, var(--bg-2) 40%, rgba(220,5,45,0.12) 100%);
}
.match-hero::before {
  content:''; position:absolute; inset:0;
  background: radial-gradient(ellipse 60% 100% at 50% 50%, rgba(26,72,184,0.05), transparent 70%);
  pointer-events:none;
}

.hero-inner {
  max-width:560px; margin:0 auto;
  display:flex; align-items:center; justify-content:space-between; gap:10px;
}
.hero-team {
  display:flex; flex-direction:column; align-items:center; gap:7px; flex:1;
}
.badge-ring {
  width:72px; height:72px;
  display:flex; align-items:center; justify-content:center;
  border-radius:50%;
  border:1px solid var(--border-m);
  background:rgba(255,255,255,0.04);
  filter:drop-shadow(0 4px 16px rgba(0,0,0,0.6));
  transition:transform .3s ease;
  flex-shrink:0;
}
.badge-ring:hover { transform:scale(1.07); }
.badge-ring svg { width:52px; height:52px; }
.hero-name {
  font-family:'Bebas Neue',sans-serif; font-size:14px; letter-spacing:1px;
  text-transform:uppercase; text-align:center; color:#fff; line-height:1.2;
}
.hero-pos { font-size:9.5px; color:var(--muted); text-transform:uppercase; letter-spacing:0.6px; }

.vs-block { display:flex; flex-direction:column; align-items:center; gap:4px; flex-shrink:0; }
.vs-text {
  font-family:'Bebas Neue',sans-serif; font-size:26px;
  color:rgba(255,255,255,0.12); letter-spacing:2px;
}
.vs-meta { font-size:9.5px; color:var(--muted); text-align:center; line-height:1.5; }
.vs-leg {
  font-family:'Bebas Neue',sans-serif; font-size:10px; letter-spacing:1.5px;
  color:var(--ucl-star); background:rgba(200,168,75,0.1);
  border:1px solid rgba(200,168,75,0.25); padding:1px 7px; border-radius:3px;
}

/* ═══════════════════════════════════════════════
   PAGE + LAYOUT
═══════════════════════════════════════════════ */
.page { max-width:700px; margin:0 auto; padding:20px 14px 56px; }

/* ─── SECTION CARD ─── */
.card {
  background:var(--bg-2); border:1px solid var(--border);
  border-radius:var(--radius); overflow:hidden; margin-bottom:16px;
}
.card-hd {
  padding:13px 18px 11px; border-bottom:1px solid var(--border);
  display:flex; align-items:center; gap:8px;
}
.card-hd-dot { width:5px; height:5px; border-radius:50%; flex-shrink:0; }
.card-hd-title {
  font-family:'Bebas Neue',sans-serif; font-size:11px; letter-spacing:2px;
  text-transform:uppercase; color:var(--muted); flex:1;
}
.card-hd-badge {
  font-size:9px; letter-spacing:0.8px; text-transform:uppercase;
  padding:2px 7px; border-radius:3px; border:1px solid;
}
.card-body { padding:16px 18px; }

/* ─── CALLOUT ─── */
.callout {
  background:rgba(255,255,255,0.025);
  border:1px solid var(--border-m);
  border-radius:8px; padding:13px 15px;
  font-size:13px; line-height:1.7; color:var(--hi);
}
.callout strong { color:var(--ucl-star); font-weight:700; }

/* ─── FORM GRID ─── */
.form-grid { display:flex; flex-direction:column; gap:14px; }
.form-col { }

.team-pill {
  display:inline-flex; align-items:center; gap:6px;
  font-size:9.5px; font-family:'Bebas Neue',sans-serif;
  letter-spacing:1.2px; text-transform:uppercase;
  padding:3px 8px 3px 5px; border-radius:4px; margin-bottom:8px; border:1px solid;
}
.pill-scp { background:rgba(0,102,48,0.13); color:#4dbb7a; border-color:rgba(0,102,48,0.3); }
.pill-ars { background:rgba(219,0,7,0.12); color:#f47070; border-color:rgba(219,0,7,0.28); }
.pill-rma { background:rgba(196,168,79,0.12); color:#e0c97a; border-color:rgba(196,168,79,0.28); }
.pill-bay { background:rgba(220,5,45,0.12); color:#f4606a; border-color:rgba(220,5,45,0.28); }
.tp-badge { width:14px; height:14px; flex-shrink:0; }

.match-list { display:flex; flex-direction:column; gap:4px; }
.mr {
  display:grid; grid-template-columns:7px 46px 1fr auto;
  align-items:center; gap:9px;
  background:var(--bg-3); border:1px solid var(--border);
  border-radius:6px; padding:7px 10px;
}
.rd { width:7px; height:7px; border-radius:50%; }
.rd.W { background:var(--low); box-shadow:0 0 5px rgba(52,211,153,0.45); }
.rd.D { background:var(--med); }
.rd.L { background:var(--high); box-shadow:0 0 5px rgba(255,107,53,0.4); }
.ms { font-family:'Bebas Neue',sans-serif; font-size:15px; font-weight:400; color:#fff; text-align:center; }
.mo { font-size:12px; color:var(--text); font-weight:600; overflow:hidden; text-overflow:ellipsis; white-space:nowrap; }
.mc { font-size:9.5px; color:var(--muted); text-transform:uppercase; letter-spacing:0.4px; text-align:right; white-space:nowrap; }

.f-legend { display:flex; gap:12px; flex-wrap:wrap; margin-top:10px; }
.fl { display:flex; align-items:center; gap:4px; font-size:10.5px; color:var(--muted); }
.fl-dot { width:7px; height:7px; border-radius:50%; }

/* ─── SEASON AVERAGES ─── */
.avg-pair { display:flex; flex-direction:column; gap:12px; }
.avg-grp { }
.avg-grp-lbl {
  font-family:'Bebas Neue',sans-serif; font-size:10px; letter-spacing:1.2px;
  text-transform:uppercase; margin-bottom:7px;
}
.avg-grid {
  display:grid; grid-template-columns:repeat(4,1fr); gap:6px;
}
.ac {
  background:var(--bg-3); border:1px solid var(--border); border-radius:8px;
  padding:10px 6px 8px; text-align:center;
}
.ac .v { font-family:'Bebas Neue',sans-serif; font-size:22px; color:#fff; line-height:1; }
.ac .l { font-size:9px; color:var(--muted); margin-top:3px; text-transform:uppercase; letter-spacing:0.5px; line-height:1.3; }

/* ─── H2H STRIP ─── */
.h2h-strip {
  background:var(--bg-3); border:1px solid var(--border); border-radius:8px;
  padding:13px 10px; display:flex; align-items:center; justify-content:space-between; gap:4px;
}
.hs { text-align:center; flex:1; }
.hn { font-family:'Bebas Neue',sans-serif; font-size:28px; line-height:1; }
.hl { font-size:9px; color:var(--muted); text-transform:uppercase; letter-spacing:0.6px; margin-top:3px; }
.hd { width:1px; height:36px; background:var(--border); flex-shrink:0; }

.h2h-list { display:flex; flex-direction:column; gap:4px; margin-top:12px; }
.h2h-row {
  display:grid; grid-template-columns:1fr auto 1fr;
  align-items:center; gap:8px;
  background:var(--bg-4); border:1px solid var(--border); border-radius:6px;
  padding:7px 10px;
}
.h2h-home { font-size:12px; font-weight:600; color:var(--text); text-align:left; white-space:nowrap; overflow:hidden; text-overflow:ellipsis; }
.h2h-sc { font-family:'Bebas Neue',sans-serif; font-size:15px; color:#fff; text-align:center; white-space:nowrap; }
.h2h-away { font-size:12px; font-weight:600; color:var(--text); text-align:right; white-space:nowrap; overflow:hidden; text-overflow:ellipsis; }
.h2h-sub { font-size:9px; color:var(--muted); text-transform:uppercase; letter-spacing:0.4px; grid-column:1/-1; text-align:center; margin-top:-2px; }

/* ─── PREDICTION TABLE ─── */
.pred-legend { display:flex; gap:14px; flex-wrap:wrap; margin-bottom:13px; }
.pli { display:flex; align-items:center; gap:5px; font-size:11px; color:var(--muted); }
.pld { width:8px; height:8px; border-radius:50%; }

.pred-wrap { overflow-x:auto; -webkit-overflow-scrolling:touch; }
.pred-table {
  width:100%; border-collapse:collapse;
  table-layout:fixed; min-width:320px;
}
.pred-table col.cm { width:32%; }
.pred-table col.cl { width:16%; }
.pred-table col.cn { width:16%; }
.pred-table col.ch { width:16%; }
.pred-table col.cb { width:20%; }

.pred-table thead th {
  font-family:'Bebas Neue',sans-serif; font-size:10px; letter-spacing:1.5px;
  text-transform:uppercase; color:var(--muted);
  padding:0 0 10px; text-align:left; white-space:nowrap; overflow:hidden;
}
.pred-table thead th:not(:first-child) { text-align:center; }
.pred-table thead th.th-med { color:var(--med); }

.pred-table tbody td {
  padding:8px 3px; border-bottom:1px solid rgba(255,255,255,0.03);
  vertical-align:middle; overflow:hidden;
}
.pred-table tbody tr:last-child td { border-bottom:none; }
.pred-table tbody td.cm-cell { color:var(--hi); font-size:12.5px; padding-left:0; }
.pred-table tbody td:not(.cm-cell) { text-align:center; }

.lv { font-family:'Bebas Neue',sans-serif; font-size:19px; color:var(--low); line-height:1; }
.mv { font-family:'Bebas Neue',sans-serif; font-size:19px; color:var(--med); line-height:1; }
.hv { font-family:'Bebas Neue',sans-serif; font-size:19px; color:var(--high); line-height:1; }

.bar-w { width:80%; max-width:90px; height:5px; background:rgba(255,255,255,0.06); border-radius:3px; overflow:hidden; margin:0 auto; display:block; }
.bar-f { display:block; height:100%; border-radius:3px; }
.bar-scp-ars { background:linear-gradient(90deg,var(--low),var(--high)); }
.bar-rma-bay { background:linear-gradient(90deg,#f9c74f,var(--high)); }

/* ─── MATCH DIVIDER ─── */
.match-divider {
  text-align:center; padding:22px 0 10px; position:relative;
}
.match-divider::before {
  content:''; position:absolute; left:0; right:0; top:50%;
  height:1px; background:var(--border);
}
.match-divider-inner {
  display:inline-flex; align-items:center; gap:10px;
  background:var(--bg); padding:0 14px; position:relative;
  font-family:'Bebas Neue',sans-serif; font-size:10px; letter-spacing:3px;
  text-transform:uppercase; color:var(--ucl-star);
}
.ucl-star-icon { font-size:12px; }

/* ─── FOOTER ─── */
footer {
  text-align:center; padding:18px 14px;
  font-size:10.5px; color:rgba(99,107,132,0.45);
  border-top:1px solid var(--border);
}

/* ════════════════════════════════════
   TABLET 640px+
═══════════════════════════════════ */
@media(min-width:640px){
  body { font-size:15px; }
  .page { max-width:920px; padding:26px 24px 64px; }
  .site-header { padding:28px 24px 24px; }
  .site-header h1 { font-size:34px; }
  .match-hero { padding:28px 24px 22px; }
  .hero-inner { max-width:640px; }
  .badge-ring { width:84px; height:84px; }
  .badge-ring svg { width:60px; height:60px; }
  .hero-name { font-size:16px; }
  .vs-text { font-size:32px; }
  .card-hd { padding:14px 22px 12px; }
  .card-body { padding:18px 22px; }
  .form-grid { flex-direction:row; gap:16px; }
  .form-col { flex:1; min-width:0; }
  .avg-pair { flex-direction:row; gap:16px; }
  .avg-grp { flex:1; }
  .ac .v { font-size:24px; }
  .hn { font-size:34px; }
  .lv,.mv,.hv { font-size:22px; }
  .pred-table tbody td { padding:9px 5px; }
  .bar-w { max-width:110px; height:6px; }
  .callout { font-size:14px; }
}

/* ════════════════════════════════════
   DESKTOP 1060px+
═══════════════════════════════════ */
@media(min-width:1060px){
  .page { max-width:1380px; padding:32px 40px 72px; }
  .site-header { padding:30px 40px 26px; }
  .site-header h1 { font-size:40px; }
  .match-hero { padding:30px 40px 24px; }
  .hero-inner { max-width:700px; }
  .badge-ring { width:92px; height:92px; }
  .badge-ring svg { width:66px; height:66px; }
  .hero-name { font-size:17px; }

  /* two-column content grid */
  .match-grid {
    display:grid; grid-template-columns:1fr 1fr; gap:22px; align-items:start;
  }
  .match-grid .fw { grid-column:1/-1; }

  .card-hd { padding:15px 24px 13px; }
  .card-body { padding:20px 24px; }
  .ac .v { font-size:26px; }
  .lv,.mv,.hv { font-size:23px; }
  .hn { font-size:36px; }
  .pred-table col.cm { width:30%; }
  .bar-w { max-width:100px; }
}

/* ════════════════════════════════════
   WIDE 1380px+
═══════════════════════════════════ */
@media(min-width:1380px){
  .page { max-width:1520px; padding:36px 60px 80px; }
  .site-header { padding:32px 60px 26px; }
  .site-header h1 { font-size:46px; }
  .match-hero { padding:32px 60px 26px; }
  .hero-inner { max-width:780px; }
  .match-grid { gap:28px; }
}
</style>
</head>
<body>

<!-- ══════════════ SITE HEADER ══════════════ -->
<header class="site-header">
  <div class="star-strip">
    <div class="ucl-tag">★ UEFA Champions League · Quarter-Finals · First Leg · 7 April 2026 ★</div>
  </div>
  <h1>Team Bilbo Champions League Stats Predictor</h1>
  <p class="tagline">Last 5 form &nbsp;·&nbsp; Season averages &nbsp;·&nbsp; Head-to-head &nbsp;·&nbsp; Low / Median / High predictions</p>
</header>

<!-- ══════════════════════════════════════════════
     MATCH 1 HERO: SPORTING CP vs ARSENAL
═══════════════════════════════════════════════ -->
<div class="match-hero scp-ars">
  <div class="hero-inner">
    <!-- SPORTING CP -->
    <div class="hero-team">
      <div class="badge-ring">
        <svg viewBox="0 0 100 100" xmlns="http://www.w3.org/2000/svg">
          <!-- Green main shield -->
          <circle cx="50" cy="50" r="46" fill="#006630"/>
          <circle cx="50" cy="50" r="46" fill="none" stroke="#ffcc00" stroke-width="2"/>
          <!-- Inner white ring -->
          <circle cx="50" cy="50" r="36" fill="none" stroke="rgba(255,255,255,0.15)" stroke-width="1"/>
          <!-- Lion silhouette (simplified) -->
          <!-- Body -->
          <ellipse cx="50" cy="56" rx="16" ry="12" fill="#ffcc00"/>
          <!-- Head -->
          <circle cx="50" cy="38" r="11" fill="#ffcc00"/>
          <!-- Mane suggestion -->
          <circle cx="50" cy="38" r="14" fill="none" stroke="#c8960a" stroke-width="3"/>
          <!-- Eyes -->
          <circle cx="46" cy="36" r="2" fill="#006630"/>
          <circle cx="54" cy="36" r="2" fill="#006630"/>
          <!-- Crown suggestion -->
          <path d="M40 28 L43 22 L47 27 L50 21 L53 27 L57 22 L60 28 Z" fill="#c8960a"/>
          <!-- SPORTING text -->
          <text x="50" y="88" text-anchor="middle" font-family="Arial,sans-serif" font-size="8" font-weight="bold" fill="#ffcc00" letter-spacing="1.5">SPORTING</text>
        </svg>
      </div>
      <div class="hero-name">Sporting CP</div>
      <div class="hero-pos">Liga NOS · 2nd · Home</div>
    </div>

    <div class="vs-block">
      <div class="vs-text">VS</div>
      <div class="vs-leg">1st Leg</div>
      <div class="vs-meta">Estádio José Alvalade<br>Lisbon · 7 Apr · 8pm CET</div>
    </div>

    <!-- ARSENAL -->
    <div class="hero-team">
      <div class="badge-ring">
        <svg viewBox="0 0 100 100" xmlns="http://www.w3.org/2000/svg">
          <circle cx="50" cy="50" r="46" fill="#db0007"/>
          <circle cx="50" cy="50" r="46" fill="none" stroke="rgba(255,255,255,0.2)" stroke-width="1.5"/>
          <!-- Cannon barrel (simplified) -->
          <rect x="22" y="44" width="56" height="12" rx="6" fill="#ffffff"/>
          <!-- Cannon wheels -->
          <circle cx="36" cy="62" r="10" fill="none" stroke="#ffffff" stroke-width="3"/>
          <circle cx="36" cy="62" r="4" fill="#ffffff"/>
          <circle cx="64" cy="62" r="10" fill="none" stroke="#ffffff" stroke-width="3"/>
          <circle cx="64" cy="62" r="4" fill="#ffffff"/>
          <!-- Cannon top rim -->
          <rect x="20" y="40" width="12" height="8" rx="3" fill="#ffffff"/>
          <!-- ARSENAL -->
          <text x="50" y="30" text-anchor="middle" font-family="Arial,sans-serif" font-size="9" font-weight="bold" fill="#ffffff" letter-spacing="2">ARSENAL</text>
        </svg>
      </div>
      <div class="hero-name">Arsenal</div>
      <div class="hero-pos">PL Leaders · 1st · Away</div>
    </div>
  </div>
</div>

<!-- ══════════════════════════════════════════════
     MATCH 1 CONTENT
═══════════════════════════════════════════════ -->
<div class="page">
<div class="match-grid">

  <!-- CONTEXT -->
  <div class="card fw">
    <div class="card-hd">
      <div class="card-hd-dot" style="background:var(--ucl-star)"></div>
      <div class="card-hd-title">Match Context — Sporting CP vs Arsenal</div>
      <div class="card-hd-badge" style="color:var(--ucl-star);border-color:rgba(200,168,75,0.3);background:rgba(200,168,75,0.07)">UCL QF Leg 1</div>
    </div>
    <div class="card-body">
      <div class="callout">
        Viktor Gyökeres <strong>returns to his former club</strong> as Arsenal travel to Lisbon for the first leg. Sporting are in outstanding home form — <strong>unbeaten in 17 straight home games</strong>, winning all five UCL home fixtures this season (scoring 16 goals in those five). Arsenal are unbeaten in all 10 of their UCL games this season, boasting the lowest xG against (0.75), goals conceded (0.5) and shots on target faced (2.7) in the competition. However, Arsenal have <strong>never won away vs Portuguese opposition in knockout European football</strong>. Sporting captain Hjulmand is <strong>suspended</strong>; Arsenal are without Saka, Timber, Eze and Merino, but Gabriel, Rice and Trossard return from FA Cup rotation. Arsenal suffered back-to-back domestic cup defeats entering this tie — Arteta's side hungry to respond on Europe's biggest stage.
      </div>
    </div>
  </div>

  <!-- LAST 5 FORM -->
  <div class="card fw">
    <div class="card-hd">
      <div class="card-hd-dot" style="background:#4dbb7a"></div>
      <div class="card-hd-title">Last 5 Matches — All Competitions</div>
    </div>
    <div class="card-body">
      <div class="form-grid">
        <!-- SPORTING -->
        <div class="form-col">
          <div class="team-pill pill-scp">
            <svg class="tp-badge" viewBox="0 0 100 100"><circle cx="50" cy="50" r="46" fill="#006630"/><circle cx="50" cy="38" r="11" fill="#ffcc00"/></svg>
            Sporting CP
          </div>
          <div class="match-list">
            <div class="mr"><div class="rd W"></div><div class="ms">4–2</div><div class="mo">Santa Clara</div><div class="mc">Liga · Home</div></div>
            <div class="mr"><div class="rd W"></div><div class="ms">5–0</div><div class="mo">Bodø/Glimt</div><div class="mc">UCL R16 · Home</div></div>
            <div class="mr"><div class="rd L"></div><div class="ms">0–3</div><div class="mo">Bodø/Glimt</div><div class="mc">UCL R16 · Away</div></div>
            <div class="mr"><div class="rd W"></div><div class="ms">4–1</div><div class="mo">Famalicão</div><div class="mc">Liga · Home</div></div>
            <div class="mr"><div class="rd W"></div><div class="ms">3–0</div><div class="mo">Casa Pia</div><div class="mc">Liga · Away</div></div>
          </div>
        </div>
        <!-- ARSENAL -->
        <div class="form-col">
          <div class="team-pill pill-ars">
            <svg class="tp-badge" viewBox="0 0 100 100"><circle cx="50" cy="50" r="46" fill="#db0007"/><rect x="20" y="44" width="60" height="12" rx="6" fill="#fff"/></svg>
            Arsenal
          </div>
          <div class="match-list">
            <div class="mr"><div class="rd L"></div><div class="ms">1–2</div><div class="mo">Southampton</div><div class="mc">FA Cup · Away</div></div>
            <div class="mr"><div class="rd L"></div><div class="ms">0–2</div><div class="mo">Manchester City</div><div class="mc">EFL Final · Neutral</div></div>
            <div class="mr"><div class="rd W"></div><div class="ms">2–0</div><div class="mo">Bayer Leverkusen</div><div class="mc">UCL R16 · Home</div></div>
            <div class="mr"><div class="rd W"></div><div class="ms">4–0</div><div class="mo">Wigan Athletic</div><div class="mc">FA Cup · Home</div></div>
            <div class="mr"><div class="rd W"></div><div class="ms">2–1</div><div class="mo">Chelsea</div><div class="mc">PL · Home</div></div>
          </div>
        </div>
      </div>
      <div class="f-legend">
        <div class="fl"><div class="fl-dot" style="background:var(--low)"></div>Win</div>
        <div class="fl"><div class="fl-dot" style="background:var(--med)"></div>Draw</div>
        <div class="fl"><div class="fl-dot" style="background:var(--high)"></div>Loss</div>
      </div>
    </div>
  </div>

  <!-- SEASON AVERAGES -->
  <div class="card fw">
    <div class="card-hd">
      <div class="card-hd-dot" style="background:#a78bfa"></div>
      <div class="card-hd-title">Season Averages per Match</div>
    </div>
    <div class="card-body">
      <div class="avg-pair">
        <div class="avg-grp">
          <div class="avg-grp-lbl" style="color:#4dbb7a">Sporting CP — Liga NOS + UCL 25/26</div>
          <div class="avg-grid">
            <div class="ac"><div class="v">17.9</div><div class="l">Shots</div></div>
            <div class="ac"><div class="v">7.0</div><div class="l">SOT</div></div>
            <div class="ac"><div class="v">6.5</div><div class="l">Corners</div></div>
            <div class="ac"><div class="v">11.2</div><div class="l">Fouls</div></div>
          </div>
          <div class="avg-grid" style="margin-top:6px">
            <div class="ac"><div class="v">55%</div><div class="l">Possess.</div></div>
            <div class="ac"><div class="v">16</div><div class="l">Corners vs Bodø</div></div>
            <div class="ac"><div class="v">38</div><div class="l">Shots vs Bodø</div></div>
            <div class="ac"><div class="v">17</div><div class="l">H. Games Won</div></div>
          </div>
        </div>
        <div class="avg-grp">
          <div class="avg-grp-lbl" style="color:#f47070">Arsenal — PL + UCL 25/26</div>
          <div class="avg-grid">
            <div class="ac"><div class="v">14.7</div><div class="l">Shots</div></div>
            <div class="ac"><div class="v">5.0</div><div class="l">SOT</div></div>
            <div class="ac"><div class="v">5.8</div><div class="l">Corners</div></div>
            <div class="ac"><div class="v">9.8</div><div class="l">Fouls</div></div>
          </div>
          <div class="avg-grid" style="margin-top:6px">
            <div class="ac"><div class="v">59%</div><div class="l">Possess.</div></div>
            <div class="ac"><div class="v">0.5</div><div class="l">UCL GA/Gm</div></div>
            <div class="ac"><div class="v">2.7</div><div class="l">UCL SOT vs /Gm</div></div>
            <div class="ac"><div class="v">10</div><div class="l">UCL Unbeaten</div></div>
          </div>
        </div>
      </div>
    </div>
  </div>

  <!-- H2H -->
  <div class="card fw">
    <div class="card-hd">
      <div class="card-hd-dot" style="background:var(--high)"></div>
      <div class="card-hd-title">Head to Head — Last 5 Meetings (All UEFA Comps)</div>
    </div>
    <div class="card-body">
      <div class="h2h-strip">
        <div class="hs"><div class="hn" style="color:#4dbb7a">0</div><div class="hl">Sporting Wins</div></div>
        <div class="hd"></div>
        <div class="hs"><div class="hn" style="color:var(--med)">3</div><div class="hl">Draws</div></div>
        <div class="hd"></div>
        <div class="hs"><div class="hn" style="color:#f47070">2</div><div class="hl">Arsenal Wins</div></div>
        <div class="hd"></div>
        <div class="hs"><div class="hn">7</div><div class="hl">Total Meetings</div></div>
      </div>
      <div class="h2h-list">
        <div class="h2h-row">
          <div class="h2h-home">Arsenal</div><div class="h2h-sc">5 – 1</div><div class="h2h-away">Sporting CP</div>
          <div class="h2h-sub">UCL League Phase · Nov 2024 (Alvalade)</div>
        </div>
        <div class="h2h-row">
          <div class="h2h-home">Arsenal</div><div class="h2h-sc">1 – 1</div><div class="h2h-away">Sporting CP</div>
          <div class="h2h-sub">UCL League Phase · Sep 2024 (Emirates)</div>
        </div>
        <div class="h2h-row">
          <div class="h2h-home">Arsenal</div><div class="h2h-sc">1 – 1*</div><div class="h2h-away">Sporting CP</div>
          <div class="h2h-sub">UEL R16 · Mar 2023 · *Sporting won on pens 5–3</div>
        </div>
        <div class="h2h-row">
          <div class="h2h-home">Sporting CP</div><div class="h2h-sc">0 – 1</div><div class="h2h-away">Arsenal</div>
          <div class="h2h-sub">UEL R16 1st Leg · Mar 2023 (Alvalade)</div>
        </div>
        <div class="h2h-row">
          <div class="h2h-home">Sporting CP</div><div class="h2h-sc">0 – 1</div><div class="h2h-away">Arsenal</div>
          <div class="h2h-sub">UEL Group Stage · Oct 2022 (Alvalade)</div>
        </div>
      </div>
      <p style="font-size:11px;color:var(--muted);margin-top:10px;">Sporting have <em>never beaten Arsenal in 90 minutes</em> across 7 meetings (W0 D4 L3). Arsenal's Nov 2024 5–1 demolition was at this very ground. But Sporting's home form in 2026 is unrecognisable from then.</p>
    </div>
  </div>

  <!-- PREDICTIONS SCP vs ARS -->
  <div class="card fw">
    <div class="card-hd">
      <div class="card-hd-dot" style="background:var(--low)"></div>
      <div class="card-hd-title">📊 Predicted Ranges — Sporting CP vs Arsenal (Both Teams Combined)</div>
    </div>
    <div class="card-body">
      <div class="pred-legend">
        <div class="pli"><div class="pld" style="background:var(--low)"></div><span style="color:var(--low);font-weight:700">Low</span> = conservative floor</div>
        <div class="pli"><div class="pld" style="background:var(--med)"></div><span style="color:var(--med);font-weight:700">Median</span> = average-based expected</div>
        <div class="pli"><div class="pld" style="background:var(--high)"></div><span style="color:var(--high);font-weight:700">High</span> = ceiling</div>
      </div>
      <div class="pred-wrap">
      <table class="pred-table">
        <colgroup>
          <col class="cm"><col class="cl"><col class="cn"><col class="ch"><col class="cb">
        </colgroup>
        <thead>
          <tr>
            <th>Metric</th>
            <th style="color:var(--low)">Low</th>
            <th class="th-med">Median</th>
            <th style="color:var(--high)">High</th>
            <th style="text-align:center;color:var(--muted)">Intensity</th>
          </tr>
        </thead>
        <tbody>
          <tr><td class="cm-cell">Corners</td><td><span class="lv">9</span></td><td><span class="mv">11</span></td><td><span class="hv">16</span></td><td><div class="bar-w"><div class="bar-f bar-scp-ars" style="width:66%"></div></div></td></tr>
          <tr><td class="cm-cell">Total Shots</td><td><span class="lv">22</span></td><td><span class="mv">28</span></td><td><span class="hv">38</span></td><td><div class="bar-w"><div class="bar-f bar-scp-ars" style="width:74%"></div></div></td></tr>
          <tr><td class="cm-cell">Shots on Target</td><td><span class="lv">7</span></td><td><span class="mv">11</span></td><td><span class="hv">16</span></td><td><div class="bar-w"><div class="bar-f bar-scp-ars" style="width:64%"></div></div></td></tr>
          <tr><td class="cm-cell">Fouls</td><td><span class="lv">18</span></td><td><span class="mv">23</span></td><td><span class="hv">32</span></td><td><div class="bar-w"><div class="bar-f bar-scp-ars" style="width:60%"></div></div></td></tr>
          <tr><td class="cm-cell">Throw-ins</td><td><span class="lv">38</span></td><td><span class="mv">47</span></td><td><span class="hv">60</span></td><td><div class="bar-w"><div class="bar-f bar-scp-ars" style="width:70%"></div></div></td></tr>
          <tr><td class="cm-cell">Goal Kicks</td><td><span class="lv">15</span></td><td><span class="mv">20</span></td><td><span class="hv">28</span></td><td><div class="bar-w"><div class="bar-f bar-scp-ars" style="width:58%"></div></div></td></tr>
          <tr><td class="cm-cell">Tackles</td><td><span class="lv">28</span></td><td><span class="mv">34</span></td><td><span class="hv">46</span></td><td><div class="bar-w"><div class="bar-f bar-scp-ars" style="width:68%"></div></div></td></tr>
          <tr><td class="cm-cell">Offsides</td><td><span class="lv">3</span></td><td><span class="mv">5</span></td><td><span class="hv">9</span></td><td><div class="bar-w"><div class="bar-f bar-scp-ars" style="width:48%"></div></div></td></tr>
        </tbody>
      </table>
      </div>
    </div>
  </div>

  <!-- NOTES SCP vs ARS -->
  <div class="card fw">
    <div class="card-hd">
      <div class="card-hd-dot" style="background:#60a5fa"></div>
      <div class="card-hd-title">Analytical Notes — Sporting vs Arsenal</div>
    </div>
    <div class="card-body">
      <div class="callout">
        <strong>Corners (9–11–16):</strong> Sporting are a set-piece machine — they earned 16 corners in a single UCL game vs Bodø/Glimt. Arsenal allow very few (2.7 shots on target against per UCL game) suggesting a disciplined structure. Median of 11 blends Sporting's aggressive attacking wing play (6.5 corners/game) with Arsenal's ability to limit territory when organised. High end is very plausible on Sporting's home patch.<br><br>
        <strong>Total Shots (22–28–38):</strong> Sporting average 17.9 shots/game at home in Liga NOS, while Arsenal generate ~14.7 away. Combined season baseline is ~29 but away UCL games are typically tighter; Arsenal also suppress opponent attack better than any UCL side. The 38 ceiling reflects Sporting's extreme home pressing scenario (they literally fired 38 shots at Bodø/Glimt). Median of 28 is realistic for a high-tempo first leg.<br><br>
        <strong>Shots on Target (7–11–16):</strong> Arsenal have the best defensive record in UCL (2.7 SOT against per game). Their defensive organisation will suppress the high end. Median of 11 combines Sporting's 7.0 own SOT with Arsenal's ~4–5 away. High end reflects a game where Arsenal get into trouble early and Sporting keep Raya busy.<br><br>
        <strong>Fouls (18–23–32):</strong> Arsenal average 9.8 fouls/game; Sporting ~11.2. The absence of Hjulmand in Sporting's midfield may actually reduce fouls (he's their most-carded midfielder). But UCL quarter-final intensity drives the median above the season average. High end if the referee is permissive and the game is physical.<br><br>
        <strong>Throw-ins (38–47–60):</strong> Both teams press wide channels intensely. Sporting's aggressive full-back play and Arsenal's overlapping system create frequent boundary breaks. UCL QF games typically see 45–55 throw-ins; Sporting's home environment and high pressing tempo push the ceiling.<br><br>
        <strong>Goal Kicks (15–20–28):</strong> Arsenal concede very few shots, meaning David Raya won't be heavily tested — his goal kicks will be fewer. Rui Silva (Sporting) will launch long balls under Arsenal's high press. High end if Arsenal park deep in second-half defensive phases.<br><br>
        <strong>Tackles (28–34–46):</strong> Sporting's pressing system is tackle-intensive; Arsenal without Merino may expose a slightly less dominant midfield. UCL context drives both teams to contest every duel. Median of 34 reflects both teams' combined season tackle averages (~16–18 each).<br><br>
        <strong>Offsides (3–5–9):</strong> Arsenal run a high defensive line (the source of their UCL success). Sporting's pacey forwards — Catamo, Trincão, Luis Suárez — will test it repeatedly. Gyökeres knows Sporting's runs intimately from the other side. Median of 5 is standard UCL fare; high end if Arsenal's line catches Sporting in behind several times.
      </div>
    </div>
  </div>

</div><!-- /match-grid -->

<!-- ══════════════════════════════════════════════
     DIVIDER
═══════════════════════════════════════════════ -->
<div class="match-divider">
  <div class="match-divider-inner">
    <span class="ucl-star-icon">★</span>
    Second Quarter-Final
    <span class="ucl-star-icon">★</span>
  </div>
</div>

<!-- ══════════════════════════════════════════════
     MATCH 2 HERO: REAL MADRID vs BAYERN MUNICH
═══════════════════════════════════════════════ -->
</div><!-- close .page -->

<div class="match-hero rma-bay">
  <div class="hero-inner">
    <!-- REAL MADRID -->
    <div class="hero-team">
      <div class="badge-ring">
        <svg viewBox="0 0 100 100" xmlns="http://www.w3.org/2000/svg">
          <!-- White/gold base circle -->
          <circle cx="50" cy="50" r="46" fill="#1e2a5e"/>
          <circle cx="50" cy="50" r="46" fill="none" stroke="#c4a84f" stroke-width="2.5"/>
          <!-- Crown top detail -->
          <path d="M30 28 L33 20 L38 26 L43 18 L48 25 L50 17 L52 25 L57 18 L62 26 L67 20 L70 28 Z" fill="#c4a84f"/>
          <!-- RM initials or shield-like emblem -->
          <circle cx="50" cy="55" r="22" fill="rgba(255,255,255,0.06)" stroke="rgba(196,168,79,0.3)" stroke-width="1"/>
          <!-- R M text -->
          <text x="50" y="60" text-anchor="middle" font-family="Georgia,serif" font-size="16" font-weight="bold" fill="#c4a84f" letter-spacing="2">RM</text>
          <text x="50" y="86" text-anchor="middle" font-family="Arial,sans-serif" font-size="7.5" font-weight="bold" fill="#c4a84f" letter-spacing="1.5">REAL MADRID</text>
        </svg>
      </div>
      <div class="hero-name">Real Madrid</div>
      <div class="hero-pos">La Liga · 2nd · Home</div>
    </div>

    <div class="vs-block">
      <div class="vs-text">VS</div>
      <div class="vs-leg">1st Leg</div>
      <div class="vs-meta">Santiago Bernabéu<br>Madrid · 7 Apr · 9pm CET</div>
    </div>

    <!-- BAYERN MUNICH -->
    <div class="hero-team">
      <div class="badge-ring">
        <svg viewBox="0 0 100 100" xmlns="http://www.w3.org/2000/svg">
          <!-- Outer ring -->
          <circle cx="50" cy="50" r="46" fill="#dc052d"/>
          <circle cx="50" cy="50" r="46" fill="none" stroke="rgba(255,255,255,0.25)" stroke-width="2"/>
          <!-- Classic Bayern checker pattern (simplified) -->
          <circle cx="50" cy="50" r="34" fill="#fff"/>
          <!-- Four quadrants in Bayern blue/white checker -->
          <path d="M50 16 A34 34 0 0 1 84 50 L50 50 Z" fill="#0066b2"/>
          <path d="M84 50 A34 34 0 0 1 50 84 L50 50 Z" fill="#fff"/>
          <path d="M50 84 A34 34 0 0 1 16 50 L50 50 Z" fill="#0066b2"/>
          <path d="M16 50 A34 34 0 0 1 50 16 L50 50 Z" fill="#fff"/>
          <!-- Inner circle -->
          <circle cx="50" cy="50" r="16" fill="#dc052d"/>
          <text x="50" y="54" text-anchor="middle" font-family="Arial,sans-serif" font-size="8" font-weight="bold" fill="#fff" letter-spacing="0.5">FCB</text>
          <text x="50" y="90" text-anchor="middle" font-family="Arial,sans-serif" font-size="7.5" font-weight="bold" fill="#fff" letter-spacing="1">MÜNCHEN</text>
        </svg>
      </div>
      <div class="hero-name">Bayern Munich</div>
      <div class="hero-pos">Bundesliga · 1st · Away</div>
    </div>
  </div>
</div>

<div class="page">
<div class="match-grid">

  <!-- CONTEXT -->
  <div class="card fw">
    <div class="card-hd">
      <div class="card-hd-dot" style="background:var(--ucl-star)"></div>
      <div class="card-hd-title">Match Context — Real Madrid vs Bayern Munich</div>
      <div class="card-hd-badge" style="color:var(--ucl-star);border-color:rgba(200,168,75,0.3);background:rgba(200,168,75,0.07)">UCL QF Leg 1 · Record 29th Meeting</div>
    </div>
    <div class="card-body">
      <div class="callout">
        The <strong>most-played fixture in UEFA competition history</strong> — 29th encounter. Real Madrid eliminated Manchester City 5–1 on aggregate; Bayern demolished Atalanta 10–2 over two legs. Madrid are unbeaten in their last <strong>nine European meetings with Bayern (W7 D2)</strong> and have progressed from all three previous UCL QF ties. Bayern's Vincent Kompany believes this is the best Bayern squad in years — Harry Kane has scored <strong>48 goals in 40 appearances</strong> this season and targets a return from an ankle issue. Real Madrid's Courtois is out for six weeks; Lunin starts. Rodrygo is also absent. Bellingham is working back from a hamstring injury. Bayern missing Ulreich. Mbappé leads UCL scoring with <strong>13 goals in 9 matches</strong>. Referee: Michael Oliver.
      </div>
    </div>
  </div>

  <!-- LAST 5 FORM -->
  <div class="card fw">
    <div class="card-hd">
      <div class="card-hd-dot" style="background:var(--ucl-star)"></div>
      <div class="card-hd-title">Last 5 Matches — All Competitions</div>
    </div>
    <div class="card-body">
      <div class="form-grid">
        <!-- REAL MADRID -->
        <div class="form-col">
          <div class="team-pill pill-rma">
            <svg class="tp-badge" viewBox="0 0 100 100"><circle cx="50" cy="50" r="46" fill="#1e2a5e"/><text x="50" y="55" text-anchor="middle" font-size="20" font-weight="bold" fill="#c4a84f">RM</text></svg>
            Real Madrid
          </div>
          <div class="match-list">
            <div class="mr"><div class="rd W"></div><div class="ms">3–2</div><div class="mo">Atlético Madrid</div><div class="mc">La Liga · Home</div></div>
            <div class="mr"><div class="rd W"></div><div class="ms">3–0</div><div class="mo">Man City</div><div class="mc">UCL R16 · Away</div></div>
            <div class="mr"><div class="rd W"></div><div class="ms">2–0</div><div class="mo">Man City</div><div class="mc">UCL R16 · Home</div></div>
            <div class="mr"><div class="rd L"></div><div class="ms">0–1</div><div class="mo">Getafe</div><div class="mc">La Liga · Away</div></div>
            <div class="mr"><div class="rd W"></div><div class="ms">2–1</div><div class="mo">Rayo Vallecano</div><div class="mc">La Liga · Home</div></div>
          </div>
        </div>
        <!-- BAYERN -->
        <div class="form-col">
          <div class="team-pill pill-bay">
            <svg class="tp-badge" viewBox="0 0 100 100"><circle cx="50" cy="50" r="46" fill="#dc052d"/><circle cx="50" cy="50" r="28" fill="#fff"/><path d="M50 22 A28 28 0 0 1 78 50 L50 50 Z" fill="#0066b2"/><path d="M50 78 A28 28 0 0 1 22 50 L50 50 Z" fill="#0066b2"/></svg>
            Bayern Munich
          </div>
          <div class="match-list">
            <div class="mr"><div class="rd W"></div><div class="ms">3–2</div><div class="mo">Freiburg</div><div class="mc">Bundesliga · Away</div></div>
            <div class="mr"><div class="rd W"></div><div class="ms">4–1</div><div class="mo">Atalanta</div><div class="mc">UCL R16 · Away</div></div>
            <div class="mr"><div class="rd W"></div><div class="ms">6–1</div><div class="mo">Atalanta</div><div class="mc">UCL R16 · Home</div></div>
            <div class="mr"><div class="rd W"></div><div class="ms">4–1</div><div class="mo">B. Mönchengladbach</div><div class="mc">Bundesliga · Home</div></div>
            <div class="mr"><div class="rd W"></div><div class="ms">3–1</div><div class="mo">Union Berlin</div><div class="mc">Bundesliga · Home</div></div>
          </div>
        </div>
      </div>
      <div class="f-legend">
        <div class="fl"><div class="fl-dot" style="background:var(--low)"></div>Win</div>
        <div class="fl"><div class="fl-dot" style="background:var(--med)"></div>Draw</div>
        <div class="fl"><div class="fl-dot" style="background:var(--high)"></div>Loss</div>
      </div>
    </div>
  </div>

  <!-- SEASON AVERAGES -->
  <div class="card fw">
    <div class="card-hd">
      <div class="card-hd-dot" style="background:#a78bfa"></div>
      <div class="card-hd-title">Season Averages per Match — UCL 2025/26</div>
    </div>
    <div class="card-body">
      <div class="avg-pair">
        <div class="avg-grp">
          <div class="avg-grp-lbl" style="color:#e0c97a">Real Madrid — UCL this season</div>
          <div class="avg-grid">
            <div class="ac"><div class="v">17.7</div><div class="l">Shots</div></div>
            <div class="ac"><div class="v">6.9</div><div class="l">SOT</div></div>
            <div class="ac"><div class="v">5.3</div><div class="l">Corners</div></div>
            <div class="ac"><div class="v">2.4</div><div class="l">Goals / Gm</div></div>
          </div>
          <div class="avg-grid" style="margin-top:6px">
            <div class="ac"><div class="v">57%</div><div class="l">Possess.</div></div>
            <div class="ac"><div class="v">29</div><div class="l">UCL Goals</div></div>
            <div class="ac"><div class="v">14</div><div class="l">UCL GA</div></div>
            <div class="ac"><div class="v">4.6</div><div class="l">Opp. Corners</div></div>
          </div>
        </div>
        <div class="avg-grp">
          <div class="avg-grp-lbl" style="color:#f4606a">Bayern Munich — UCL this season</div>
          <div class="avg-grid">
            <div class="ac"><div class="v">18.9</div><div class="l">Shots</div></div>
            <div class="ac"><div class="v">8.2</div><div class="l">SOT</div></div>
            <div class="ac"><div class="v">6.3</div><div class="l">Corners</div></div>
            <div class="ac"><div class="v">3.2</div><div class="l">Goals / Gm</div></div>
          </div>
          <div class="avg-grid" style="margin-top:6px">
            <div class="ac"><div class="v">64%</div><div class="l">Possess.</div></div>
            <div class="ac"><div class="v">32</div><div class="l">UCL Goals</div></div>
            <div class="ac"><div class="v">10</div><div class="l">UCL GA</div></div>
            <div class="ac"><div class="v">2.8</div><div class="l">Opp. Corners</div></div>
          </div>
        </div>
      </div>
    </div>
  </div>

  <!-- H2H -->
  <div class="card fw">
    <div class="card-hd">
      <div class="card-hd-dot" style="background:var(--high)"></div>
      <div class="card-hd-title">Head to Head — Last 5 Meetings (UCL)</div>
    </div>
    <div class="card-body">
      <div class="h2h-strip">
        <div class="hs"><div class="hn" style="color:#e0c97a">4</div><div class="hl">Madrid Wins</div></div>
        <div class="hd"></div>
        <div class="hs"><div class="hn" style="color:var(--med)">0</div><div class="hl">Draws</div></div>
        <div class="hd"></div>
        <div class="hs"><div class="hn" style="color:#f4606a">1</div><div class="hl">Bayern Wins</div></div>
        <div class="hd"></div>
        <div class="hs"><div class="hn">3+</div><div class="hl">Goals in 7/7 Mtgs</div></div>
      </div>
      <div class="h2h-list">
        <div class="h2h-row">
          <div class="h2h-home">Real Madrid</div><div class="h2h-sc">2 – 1</div><div class="h2h-away">Bayern Munich</div>
          <div class="h2h-sub">UCL Semi-Final 2nd Leg · May 2024 (Bernabéu)</div>
        </div>
        <div class="h2h-row">
          <div class="h2h-home">Bayern Munich</div><div class="h2h-sc">2 – 2</div><div class="h2h-away">Real Madrid</div>
          <div class="h2h-sub">UCL Semi-Final 1st Leg · Apr 2024 (Allianz Arena)</div>
        </div>
        <div class="h2h-row">
          <div class="h2h-home">Real Madrid</div><div class="h2h-sc">4 – 0</div><div class="h2h-away">Bayern Munich</div>
          <div class="h2h-sub">UCL Semi-Final 2nd Leg · May 2018 (Bernabéu)</div>
        </div>
        <div class="h2h-row">
          <div class="h2h-home">Bayern Munich</div><div class="h2h-sc">2 – 1</div><div class="h2h-away">Real Madrid</div>
          <div class="h2h-sub">UCL Semi-Final 1st Leg · Apr 2018 (Allianz Arena)</div>
        </div>
        <div class="h2h-row">
          <div class="h2h-home">Real Madrid</div><div class="h2h-sc">3 – 2</div><div class="h2h-away">Bayern Munich</div>
          <div class="h2h-sub">UCL QF 2nd Leg · Apr 2017 (Bernabéu)</div>
        </div>
      </div>
      <p style="font-size:11px;color:var(--muted);margin-top:10px;">Madrid unbeaten in last 9 UEFA meetings (W7 D2). Over 2.5 goals in all of the last 7 encounters. Madrid have won all three previous UCL QF ties between the clubs. Over 11 corners in 6 of the last 7 meetings.</p>
    </div>
  </div>

  <!-- PREDICTIONS RMA vs BAY -->
  <div class="card fw">
    <div class="card-hd">
      <div class="card-hd-dot" style="background:var(--low)"></div>
      <div class="card-hd-title">📊 Predicted Ranges — Real Madrid vs Bayern Munich (Both Teams Combined)</div>
    </div>
    <div class="card-body">
      <div class="pred-legend">
        <div class="pli"><div class="pld" style="background:var(--low)"></div><span style="color:var(--low);font-weight:700">Low</span> = conservative floor</div>
        <div class="pli"><div class="pld" style="background:var(--med)"></div><span style="color:var(--med);font-weight:700">Median</span> = average-based expected</div>
        <div class="pli"><div class="pld" style="background:var(--high)"></div><span style="color:var(--high);font-weight:700">High</span> = ceiling</div>
      </div>
      <div class="pred-wrap">
      <table class="pred-table">
        <colgroup>
          <col class="cm"><col class="cl"><col class="cn"><col class="ch"><col class="cb">
        </colgroup>
        <thead>
          <tr>
            <th>Metric</th>
            <th style="color:var(--low)">Low</th>
            <th class="th-med">Median</th>
            <th style="color:var(--high)">High</th>
            <th style="text-align:center;color:var(--muted)">Intensity</th>
          </tr>
        </thead>
        <tbody>
          <tr><td class="cm-cell">Corners</td><td><span class="lv">9</span></td><td><span class="mv">12</span></td><td><span class="hv">17</span></td><td><div class="bar-w"><div class="bar-f bar-rma-bay" style="width:72%"></div></div></td></tr>
          <tr><td class="cm-cell">Total Shots</td><td><span class="lv">24</span></td><td><span class="mv">33</span></td><td><span class="hv">44</span></td><td><div class="bar-w"><div class="bar-f bar-rma-bay" style="width:82%"></div></div></td></tr>
          <tr><td class="cm-cell">Shots on Target</td><td><span class="lv">10</span></td><td><span class="mv">14</span></td><td><span class="hv">21</span></td><td><div class="bar-w"><div class="bar-f bar-rma-bay" style="width:76%"></div></div></td></tr>
          <tr><td class="cm-cell">Fouls</td><td><span class="lv">18</span></td><td><span class="mv">24</span></td><td><span class="hv">34</span></td><td><div class="bar-w"><div class="bar-f bar-rma-bay" style="width:62%"></div></div></td></tr>
          <tr><td class="cm-cell">Throw-ins</td><td><span class="lv">40</span></td><td><span class="mv">51</span></td><td><span class="hv">66</span></td><td><div class="bar-w"><div class="bar-f bar-rma-bay" style="width:78%"></div></div></td></tr>
          <tr><td class="cm-cell">Goal Kicks</td><td><span class="lv">16</span></td><td><span class="mv">22</span></td><td><span class="hv">32</span></td><td><div class="bar-w"><div class="bar-f bar-rma-bay" style="width:64%"></div></div></td></tr>
          <tr><td class="cm-cell">Tackles</td><td><span class="lv">26</span></td><td><span class="mv">32</span></td><td><span class="hv">46</span></td><td><div class="bar-w"><div class="bar-f bar-rma-bay" style="width:70%"></div></div></td></tr>
          <tr><td class="cm-cell">Offsides</td><td><span class="lv">4</span></td><td><span class="mv">7</span></td><td><span class="hv">12</span></td><td><div class="bar-w"><div class="bar-f bar-rma-bay" style="width:62%"></div></div></td></tr>
        </tbody>
      </table>
      </div>
    </div>
  </div>

  <!-- NOTES RMA vs BAY -->
  <div class="card fw">
    <div class="card-hd">
      <div class="card-hd-dot" style="background:#60a5fa"></div>
      <div class="card-hd-title">Analytical Notes — Real Madrid vs Bayern Munich</div>
    </div>
    <div class="card-body">
      <div class="callout">
        <strong>Corners (9–12–17):</strong> Real Madrid earn 5.3 corners/UCL game; Bayern average 6.3. Combined season baseline is 11.6 — H2H data confirms over 11 corners in 6 of the last 7 meetings. Madrid's disciplined defensive structure limits opponent corners (only 4.6 allowed per UCL game). High end reflects Bayern's wing overloads with Olise, Gnabry and Díaz targeting the Bernabéu flanks. Median of 12 aligns perfectly with historical trends.<br><br>
        <strong>Total Shots (24–33–44):</strong> This is the highest-volume match of the four QFs. Real shoot 17.7 and Bayern 18.9 per UCL game — combined that's 36.6 as a baseline. Away teams typically shoot 80–90% of their home volume, giving ~32–33. Bayern had 38 shots in their 6–1 first leg vs Atalanta. The high end of 44 is plausible at the Bernabéu if the game opens up. Median of 33 reflects both teams' elite UCL firepower.<br><br>
        <strong>Shots on Target (10–14–21):</strong> Bayern lead the UCL with 8.2 SOT/game; Real produce 6.9. Combined baseline: 15.1 — but Lunin replacing Courtois may affect the goalkeeping quality without reducing shot counts. The 2023/24 semi-final 2nd leg produced 17 combined SOT. Median of 14 is grounded in season averages; ceiling of 21 reflects both goalkeepers being heavily tested.<br><br>
        <strong>Fouls (18–24–34):</strong> Both teams average 10–11 fouls per game, giving a combined ~22 baseline. UCL QF high-stakes context, an English referee (Michael Oliver) who averages 3.96 yellow cards per game, and Bayern's intense pressing style push the median to 24. High end if Bayern's aggressive transition press draws repeated fouls from Madrid's fullbacks. Bayern's Carreras already has 4 UCL yellow cards this season — a flashpoint.<br><br>
        <strong>Throw-ins (40–51–66):</strong> Both teams play wide with attacking fullbacks and wingers who drive down the flanks — Vinicius, Mbappé, Olise, Díaz all operate in wide areas. The Bernabéu's atmosphere creates intense pressure in wide zones, and Bayern's counter-pressing game creates frequent out-of-bounds situations. Median of 51 reflects a high-tempo, wide-play-dominated UCL quarter-final.<br><br>
        <strong>Goal Kicks (16–22–32):</strong> Bayern's high press (64% possession) will force Lunin to launch regularly. Real's own press will test Neuer. In UCL games with high pressing intensity, both goalkeepers field frequent restarts. The absence of Courtois (replaced by Lunin) may actually produce slightly more goal kicks as Lunin reads the press differently. High end if Bayern pin Madrid back in extended periods.<br><br>
        <strong>Tackles (26–32–46):</strong> Real Madrid average ~14–15 tackles/game; Bayern ~15–16. Combined baseline is ~30. The UCL QF context — with both teams knowing every duel matters — pushes the median to 32. The high end reflects a particularly combative mid-field battle between Tchouaméni/Valverde and Kimmich/Pavlović. Over 2.5 goals in all seven meetings historically, suggesting an open, contested game.<br><br>
        <strong>Offsides (4–7–12):</strong> This is the highest offside range of the four QF matches. Madrid's high defensive line meets Bayern's forward runs from Olise, Gnabry and Kane; while Bayern's line meets Mbappé and Vinícius' sprint capacity. Recent UCL meetings between high-pressing sides regularly produce 6–9 combined offsides. Median of 7 is well-grounded in both teams' line management styles; ceiling of 12 if both coaches aggressively set high lines.
      </div>
    </div>
  </div>

</div><!-- /match-grid -->
</div><!-- /page -->

<footer>
  <strong>Team Bilbo Statistical Analysis</strong><br>Predictions are statistical estimates based on actual data, H2H analysis and contextual factors. <strong>Not financial advice.</strong><br>· 7 April 2026 · 
</footer>
</body>
</html>
