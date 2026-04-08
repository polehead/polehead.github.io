<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>UCL QF Stats Predictor | PSG v Liverpool · Barcelona v Atlético</title>
<link rel="preconnect" href="https://fonts.googleapis.com">
<link href="https://fonts.googleapis.com/css2?family=Rajdhani:wght@400;500;600;700&family=Source+Sans+3:ital,wght@0,300;0,400;0,600;0,700;1,400&display=swap" rel="stylesheet">
<style>
/* ═══════════════════════════════════════
   TOKENS
═══════════════════════════════════════ */
:root {
  --bg:       #06070c;
  --bg-2:     #0c0e18;
  --bg-3:     #121525;
  --bg-4:     #181c2e;
  --bg-5:     #1e2238;
  --border:   rgba(255,255,255,0.065);
  --border-m: rgba(255,255,255,0.11);
  --text:     #cdd5e8;
  --muted:    #5e688a;
  --hi:       #97a3c0;
  /* UCL */
  --ucl:      #1840b8;
  --ucl-gold: #c9a840;
  /* PSG */
  --psg-b:    #003087;
  --psg-r:    #da291c;
  --psg-g:    #ffffff;
  /* Liverpool */
  --lfc-r:    #c8102e;
  --lfc-g:    #f6eb61;
  /* Barcelona */
  --barca-b:  #004d98;
  --barca-r:  #a50044;
  /* Atletico */
  --atm-r:    #ce3524;
  --atm-b:    #272e61;
  /* stat palette */
  --low:      #22d3a0;
  --med:      #f7c948;
  --high:     #f26430;
  --r12:      12px;
}

*, *::before, *::after { margin:0; padding:0; box-sizing:border-box; }
html { scroll-behavior:smooth; }

body {
  font-family:'Source Sans 3',sans-serif;
  background:var(--bg);
  color:var(--text);
  min-height:100vh;
  font-size:14px;
  line-height:1.55;
  -webkit-font-smoothing:antialiased;
}

/* ═══════════════════════════════════════
   SITE HEADER
═══════════════════════════════════════ */
.site-header {
  background: linear-gradient(170deg, #050814 0%, #0c1430 55%, #050814 100%);
  border-bottom: 1px solid rgba(201,168,64,0.22);
  padding: 24px 16px 20px;
  text-align: center;
  position: relative; overflow: hidden;
}
.site-header::before {
  content:''; position:absolute; inset:0;
  background: radial-gradient(ellipse 80% 220% at 50% -20%, rgba(201,168,64,0.09), transparent 65%);
  pointer-events:none;
}
.ucl-badge {
  display:inline-flex; align-items:center; gap:8px;
  font-family:'Rajdhani',sans-serif; font-size:11px; font-weight:700;
  letter-spacing:2.5px; text-transform:uppercase; color:var(--ucl-gold);
  border: 1px solid rgba(201,168,64,0.3); background:rgba(201,168,64,0.06);
  padding:4px 14px; border-radius:3px; margin-bottom:12px;
}
.site-header h1 {
  font-family:'Rajdhani',sans-serif;
  font-size:28px; font-weight:700; letter-spacing:1.5px;
  color:#fff; text-transform:uppercase; line-height:1.1;
}
.site-header .sub {
  font-size:12px; color:var(--muted); margin-top:6px; letter-spacing:0.3px;
}
.match-nav {
  display:flex; justify-content:center; gap:10px; flex-wrap:wrap; margin-top:14px;
}
.mnav-pill {
  font-family:'Rajdhani',sans-serif; font-size:11px; font-weight:600;
  letter-spacing:0.8px; text-transform:uppercase;
  padding:5px 14px; border-radius:20px; border:1px solid;
  text-decoration:none; transition:background .2s;
}
.mnav-psg  { color:#6b9fff; border-color:rgba(107,159,255,0.28); background:rgba(107,159,255,0.06); }
.mnav-barca{ color:#f47ca0; border-color:rgba(244,124,160,0.28); background:rgba(244,124,160,0.06); }

/* ═══════════════════════════════════════
   MATCH HERO
═══════════════════════════════════════ */
.match-hero {
  padding: 24px 16px 20px;
  position:relative; overflow:hidden;
  border-bottom: 1px solid var(--border-m);
}
.mh-psg  { background: linear-gradient(135deg, rgba(0,48,135,0.22) 0%, var(--bg-2) 40%, rgba(218,41,28,0.12) 100%); }
.mh-barca{ background: linear-gradient(135deg, rgba(0,77,152,0.2) 0%, var(--bg-2) 40%, rgba(165,0,68,0.18) 100%); }
.mh-glow { position:absolute; inset:0; background:radial-gradient(ellipse 60% 80% at 50% 50%, rgba(24,64,184,0.05), transparent 70%); pointer-events:none; }

.hero-row {
  max-width:580px; margin:0 auto;
  display:flex; align-items:center; justify-content:space-between; gap:12px;
}
.hero-team {
  display:flex; flex-direction:column; align-items:center; gap:8px; flex:1;
}
.club-badge {
  width:72px; height:72px;
  border-radius:50%; border:1px solid var(--border-m);
  background:rgba(255,255,255,0.03);
  display:flex; align-items:center; justify-content:center;
  filter:drop-shadow(0 4px 18px rgba(0,0,0,0.65));
  transition:transform .3s; flex-shrink:0;
}
.club-badge:hover { transform:scale(1.07); }
.club-badge svg { width:50px; height:50px; }
.h-name {
  font-family:'Rajdhani',sans-serif; font-size:14px; font-weight:700;
  letter-spacing:1px; text-transform:uppercase; text-align:center; color:#fff; line-height:1.2;
}
.h-pos { font-size:9.5px; color:var(--muted); text-transform:uppercase; letter-spacing:0.5px; }
.vs-col { display:flex; flex-direction:column; align-items:center; gap:5px; flex-shrink:0; }
.vs-big { font-family:'Rajdhani',sans-serif; font-size:26px; font-weight:700; color:rgba(255,255,255,0.1); letter-spacing:3px; }
.leg-tag { font-family:'Rajdhani',sans-serif; font-size:10px; font-weight:700; letter-spacing:2px; color:var(--ucl-gold); background:rgba(201,168,64,0.1); border:1px solid rgba(201,168,64,0.25); padding:2px 8px; border-radius:3px; }
.venue-txt { font-size:9.5px; color:var(--muted); text-align:center; line-height:1.5; }

/* ═══════════════════════════════════════
   PAGE & GRID
═══════════════════════════════════════ */
.page { max-width:700px; margin:0 auto; padding:20px 14px 56px; }

.m-grid { display:flex; flex-direction:column; gap:0; }

/* card */
.card {
  background:var(--bg-2); border:1px solid var(--border);
  border-radius:var(--r12); overflow:hidden; margin-bottom:14px;
}
.card-hd {
  padding:13px 18px 11px; border-bottom:1px solid var(--border);
  display:flex; align-items:center; gap:8px;
}
.hd-dot { width:5px; height:5px; border-radius:50%; flex-shrink:0; }
.hd-title {
  font-family:'Rajdhani',sans-serif; font-size:11px; font-weight:700;
  letter-spacing:2px; text-transform:uppercase; color:var(--muted); flex:1;
}
.hd-tag {
  font-family:'Rajdhani',sans-serif; font-size:9px; font-weight:700;
  letter-spacing:1px; text-transform:uppercase;
  padding:2px 8px; border-radius:3px; border:1px solid;
}
.card-body { padding:16px 18px; }

/* callout */
.callout {
  background:rgba(255,255,255,0.022);
  border:1px solid var(--border-m); border-radius:8px;
  padding:13px 15px; font-size:13px; line-height:1.7; color:var(--hi);
}
.callout strong { color:var(--ucl-gold); font-weight:700; }
.callout em { color:var(--text); font-style:normal; font-weight:600; }

/* form */
.form-cols { display:flex; flex-direction:column; gap:14px; }
.fcol {}
.team-lab {
  display:inline-flex; align-items:center; gap:6px;
  font-family:'Rajdhani',sans-serif; font-size:10px; font-weight:700;
  letter-spacing:1.2px; text-transform:uppercase;
  padding:3px 8px 3px 5px; border-radius:4px; margin-bottom:8px; border:1px solid;
}
.lab-s  { background:rgba(0,48,135,0.14); color:#7aafff; border-color:rgba(107,159,255,0.26); }
.lab-l  { background:rgba(200,16,46,0.13); color:#f07070; border-color:rgba(200,16,46,0.28); }
.lab-b  { background:rgba(0,77,152,0.14); color:#7ab0ff; border-color:rgba(0,77,152,0.3); }
.lab-a  { background:rgba(206,53,36,0.13); color:#f07060; border-color:rgba(206,53,36,0.28); }
.tl-badge { width:14px; height:14px; flex-shrink:0; }

.match-list { display:flex; flex-direction:column; gap:4px; }
.mr {
  display:grid; grid-template-columns:7px 46px 1fr auto;
  align-items:center; gap:9px;
  background:var(--bg-3); border:1px solid var(--border);
  border-radius:6px; padding:7px 10px;
}
.rd { width:7px; height:7px; border-radius:50%; }
.rd.W { background:var(--low);  box-shadow:0 0 5px rgba(34,211,160,0.4); }
.rd.D { background:var(--med); }
.rd.L { background:var(--high); box-shadow:0 0 5px rgba(242,100,48,0.4); }
.ms { font-family:'Rajdhani',sans-serif; font-size:15px; font-weight:700; color:#fff; text-align:center; }
.mo { font-size:12px; color:var(--text); font-weight:600; overflow:hidden; text-overflow:ellipsis; white-space:nowrap; }
.mc { font-size:9.5px; color:var(--muted); text-transform:uppercase; letter-spacing:0.4px; text-align:right; white-space:nowrap; }
.leg-note { font-size:9.5px; color:var(--ucl-gold); font-style:italic; }

.f-leg { display:flex; gap:12px; flex-wrap:wrap; margin-top:10px; }
.fl  { display:flex; align-items:center; gap:4px; font-size:10.5px; color:var(--muted); }
.fld { width:7px; height:7px; border-radius:50%; }

/* avg */
.avg-pair { display:flex; flex-direction:column; gap:12px; }
.a-grp {}
.a-grp-lbl { font-family:'Rajdhani',sans-serif; font-size:10px; font-weight:700; letter-spacing:1.2px; text-transform:uppercase; margin-bottom:7px; }
.avg-g { display:grid; grid-template-columns:repeat(4,1fr); gap:6px; }
.ac { background:var(--bg-3); border:1px solid var(--border); border-radius:8px; padding:10px 6px 8px; text-align:center; }
.av { font-family:'Rajdhani',sans-serif; font-size:22px; font-weight:700; color:#fff; line-height:1; }
.al { font-size:9px; color:var(--muted); margin-top:3px; text-transform:uppercase; letter-spacing:0.5px; line-height:1.3; }

/* h2h */
.h2h-bar {
  background:var(--bg-3); border:1px solid var(--border); border-radius:8px;
  padding:13px 10px; display:flex; align-items:center; justify-content:space-between; gap:4px;
}
.hs { text-align:center; flex:1; }
.hn { font-family:'Rajdhani',sans-serif; font-size:28px; font-weight:700; line-height:1; }
.hl { font-size:9px; color:var(--muted); text-transform:uppercase; letter-spacing:0.7px; margin-top:3px; }
.hd { width:1px; height:36px; background:var(--border); flex-shrink:0; }

.h2h-rows { display:flex; flex-direction:column; gap:4px; margin-top:12px; }
.h2h-r {
  display:grid; grid-template-columns:1fr auto 1fr;
  align-items:center; gap:8px;
  background:var(--bg-4); border:1px solid var(--border); border-radius:6px;
  padding:7px 10px;
}
.rh { font-size:12px; font-weight:600; color:var(--text); text-align:left; white-space:nowrap; overflow:hidden; text-overflow:ellipsis; }
.rs { font-family:'Rajdhani',sans-serif; font-size:15px; font-weight:700; color:#fff; text-align:center; white-space:nowrap; }
.ra { font-size:12px; font-weight:600; color:var(--text); text-align:right; white-space:nowrap; overflow:hidden; text-overflow:ellipsis; }
.rsub { font-size:9px; color:var(--muted); text-transform:uppercase; letter-spacing:0.4px; grid-column:1/-1; text-align:center; margin-top:-2px; }

/* pred table */
.pred-leg { display:flex; gap:14px; flex-wrap:wrap; margin-bottom:13px; }
.pli { display:flex; align-items:center; gap:5px; font-size:11px; color:var(--muted); }
.pld { width:8px; height:8px; border-radius:50%; }

.pw { overflow-x:auto; -webkit-overflow-scrolling:touch; }
.pt {
  width:100%; border-collapse:collapse;
  table-layout:fixed; min-width:320px;
}
.pt col.cm { width:32%; }
.pt col.cl { width:16%; }
.pt col.cn { width:16%; }
.pt col.ch { width:16%; }
.pt col.cb { width:20%; }

.pt thead th {
  font-family:'Rajdhani',sans-serif; font-size:10px; font-weight:700;
  letter-spacing:1.5px; text-transform:uppercase; color:var(--muted);
  padding:0 0 10px; text-align:left; white-space:nowrap; overflow:hidden;
}
.pt thead th:not(:first-child) { text-align:center; }
.pt thead th.th-m { color:var(--med); }

.pt tbody td {
  padding:8px 3px; border-bottom:1px solid rgba(255,255,255,0.03);
  vertical-align:middle; overflow:hidden;
}
.pt tbody tr:last-child td { border-bottom:none; }
.pt tbody td.cmc { color:var(--hi); font-size:12.5px; padding-left:0; }
.pt tbody td:not(.cmc) { text-align:center; }

.lv  { font-family:'Rajdhani',sans-serif; font-size:19px; font-weight:700; color:var(--low);  line-height:1; }
.mv  { font-family:'Rajdhani',sans-serif; font-size:19px; font-weight:700; color:var(--med);  line-height:1; }
.hv  { font-family:'Rajdhani',sans-serif; font-size:19px; font-weight:700; color:var(--high); line-height:1; }

.bw  { width:80%; max-width:90px; height:5px; background:rgba(255,255,255,0.06); border-radius:3px; overflow:hidden; margin:0 auto; display:block; }
.bf  { display:block; height:100%; border-radius:3px; }
.bf-psg   { background:linear-gradient(90deg, var(--low), var(--high)); }
.bf-barca { background:linear-gradient(90deg, #22d3a0, #f26430); }

/* section divider */
.s-div {
  text-align:center; padding:24px 0 12px; position:relative;
}
.s-div::before { content:''; position:absolute; left:0; right:0; top:50%; height:1px; background:var(--border); }
.s-div-in {
  display:inline-flex; align-items:center; gap:10px;
  background:var(--bg); padding:0 14px; position:relative;
  font-family:'Rajdhani',sans-serif; font-size:10px; font-weight:700;
  letter-spacing:3px; text-transform:uppercase; color:var(--ucl-gold);
}

/* notes */
.note-block { margin-bottom:10px; font-size:13px; line-height:1.65; color:var(--hi); }
.note-block:last-child { margin-bottom:0; }
.note-block strong { color:var(--ucl-gold); font-weight:700; }

/* footer */
footer {
  text-align:center; padding:18px 14px;
  font-size:11.5px; color:rgba(94,104,138,0.45);
  border-top:1px solid var(--border);
}

/* ═══════════════════════════════════════
   TABLET 640px+
═══════════════════════════════════════ */
@media(min-width:640px){
  body { font-size:15px; }
  .page { max-width:920px; padding:26px 24px 64px; }
  .site-header { padding:28px 24px 24px; }
  .site-header h1 { font-size:34px; }
  .match-hero { padding:28px 24px 22px; }
  .hero-row { max-width:640px; }
  .club-badge { width:84px; height:84px; }
  .club-badge svg { width:60px; height:60px; }
  .h-name { font-size:16px; }
  .vs-big { font-size:34px; }
  .card-hd { padding:14px 22px 12px; }
  .card-body { padding:18px 22px; }
  .form-cols { flex-direction:row; gap:16px; }
  .fcol { flex:1; min-width:0; }
  .avg-pair { flex-direction:row; gap:16px; }
  .a-grp { flex:1; }
  .av { font-size:24px; }
  .hn { font-size:34px; }
  .lv,.mv,.hv { font-size:22px; }
  .pt tbody td { padding:9px 5px; }
  .bw { max-width:110px; height:6px; }
  .callout { font-size:14px; }
  .note-block { font-size:14px; }
}

/* ═══════════════════════════════════════
   DESKTOP 1060px+
═══════════════════════════════════════ */
@media(min-width:1060px){
  .page { max-width:1380px; padding:32px 40px 72px; }
  .site-header { padding:30px 40px 26px; }
  .site-header h1 { font-size:40px; }
  .match-hero { padding:30px 40px 24px; }
  .hero-row { max-width:700px; }
  .club-badge { width:92px; height:92px; }
  .club-badge svg { width:66px; height:66px; }
  .h-name { font-size:17px; }
  .card-hd { padding:15px 24px 13px; }
  .card-body { padding:20px 24px; }
  .m-grid { display:grid; grid-template-columns:1fr 1fr; gap:22px; align-items:start; }
  .m-grid .fw { grid-column:1/-1; }
  .av { font-size:26px; }
  .lv,.mv,.hv { font-size:23px; }
  .hn { font-size:36px; }
  .bw { max-width:100px; }
}

/* ═══════════════════════════════════════
   WIDE 1380px+
═══════════════════════════════════════ */
@media(min-width:1380px){
  .page { max-width:1520px; padding:36px 60px 80px; }
  .site-header { padding:32px 60px 26px; }
  .site-header h1 { font-size:46px; }
  .match-hero { padding:32px 60px 26px; }
  .hero-row { max-width:780px; }
  .m-grid { gap:28px; }
}
</style>
</head>
<body>

<!-- ══════════ HEADER ══════════ -->
<header class="site-header">
  <div class="ucl-badge">★★★★★ UEFA Champions League ★★★★★<br> Quarter-Finals · First Legs · 8 April 2026 </div>
  <p class="sub">Last 5 form &nbsp;·&nbsp; Season averages &nbsp;·&nbsp; H2H &nbsp;·&nbsp; Weighted Low / Median / High predictions</p>
  <div class="match-nav">
    <a href="#psg" class="mnav-pill mnav-psg">PSG vs Liverpool · Parc des Princes</a>
    <a href="#barca" class="mnav-pill mnav-barca">Barcelona vs Atlético · Camp Nou</a>
  </div>
</header>

<!-- ══════════════════════════════
     MATCH 1 HERO: PSG vs LIVERPOOL
═══════════════════════════════════ -->
<div class="match-hero mh-psg" id="psg">
  <div class="mh-glow"></div>
  <div class="hero-row">

    <!-- PSG -->
    <div class="hero-team">
      <div class="club-badge">
        <svg viewBox="0 0 100 100" xmlns="http://www.w3.org/2000/svg">
          <circle cx="50" cy="50" r="47" fill="#003087"/>
          <circle cx="50" cy="50" r="47" fill="none" stroke="rgba(255,255,255,0.18)" stroke-width="2"/>
          <!-- Eiffel Tower silhouette -->
          <path d="M50 18 L44 38 L37 55 L30 72 L38 72 L41 60 L44 60 L44 72 L56 72 L56 60 L59 60 L62 72 L70 72 L63 55 L56 38 Z" fill="#da291c"/>
          <!-- Crown -->
          <path d="M38 18 L42 24 L46 20 L50 26 L54 20 L58 24 L62 18 L59 28 L41 28 Z" fill="#f9d900"/>
          <!-- PSG text -->
          <text x="50" y="90" text-anchor="middle" font-family="Arial,sans-serif" font-size="9" font-weight="900" fill="#fff" letter-spacing="2">PSG</text>
        </svg>
      </div>
      <div class="h-name">PSG</div>
      <div class="h-pos">Ligue 1 Leaders · Home</div>
    </div>

    <div class="vs-col">
      <div class="vs-big">VS</div>
      <div class="leg-tag">1st Leg</div>
      <div class="venue-txt">Parc des Princes<br>Paris · Wed 8 Apr · 9pm CET</div>
    </div>

    <!-- LIVERPOOL -->
    <div class="hero-team">
      <div class="club-badge">
        <svg viewBox="0 0 100 100" xmlns="http://www.w3.org/2000/svg">
          <circle cx="50" cy="50" r="47" fill="#c8102e"/>
          <circle cx="50" cy="50" r="47" fill="none" stroke="rgba(255,255,255,0.2)" stroke-width="1.5"/>
          <!-- Liver bird (simplified) -->
          <ellipse cx="50" cy="52" rx="18" ry="14" fill="#fff" opacity="0.9"/>
          <!-- Bird head -->
          <circle cx="50" cy="34" r="10" fill="#fff" opacity="0.9"/>
          <!-- Beak -->
          <path d="M58 32 L66 30 L62 36 Z" fill="#f6eb61"/>
          <!-- Eye -->
          <circle cx="54" cy="32" r="2" fill="#c8102e"/>
          <!-- Wings -->
          <path d="M32 44 Q24 36 22 28 Q32 32 36 40 Z" fill="#fff" opacity="0.8"/>
          <path d="M68 44 Q76 36 78 28 Q68 32 64 40 Z" fill="#fff" opacity="0.8"/>
          <!-- LFC text -->
          <text x="50" y="90" text-anchor="middle" font-family="Arial,sans-serif" font-size="9" font-weight="900" fill="#f6eb61" letter-spacing="2">LFC</text>
        </svg>
      </div>
      <div class="h-name">LIVERPOOL</div>
      <div class="h-pos">PL 5th · 49 pts · Away</div>
    </div>

  </div>
</div>

<!-- ═══════════════════ MATCH 1 CONTENT ═══════════════════ -->
<div class="page">
<div class="m-grid">

  <!-- CONTEXT -->
  <div class="card fw">
    <div class="card-hd">
      <div class="hd-dot" style="background:var(--ucl-gold)"></div>
      <div class="hd-title">Match Context</div>
      <div class="hd-tag" style="color:var(--ucl-gold);border-color:rgba(201,168,64,0.28);background:rgba(201,168,64,0.07)">UCL QF · Leg 1</div>
    </div>
    <div class="card-body">
      <div class="callout">
        <strong>Defending champions PSG vs a struggling Liverpool</strong> — a rematch layered with recent drama. Last season PSG eliminated Liverpool from this very round on penalties despite the Reds winning 1–0 in Paris. Now PSG are a different beast: <em>four consecutive wins, 15 goals scored</em>, and operating with frightening attacking cohesion (Dembélé, Kvaratskhelia, Doué). Liverpool are <em>fifth in the PL</em>, have lost 15 games across all competitions and were <strong>humiliated 4–0 by Manchester City</strong> in the FA Cup QF days earlier. Virgil van Dijk admitted the team "gave up" — a damning verdict. PSG are unbeaten in their last <strong>seven European meetings with English clubs</strong>. Alisson is out for Liverpool; PSG are without Barcola (ankle), Fabian Ruiz and Mayulu. Alexander Isak may return from his broken leg.
      </div>
    </div>
  </div>

  <!-- LAST 5 FORM -->
  <div class="card fw">
    <div class="card-hd">
      <div class="hd-dot" style="background:#7aafff"></div>
      <div class="hd-title">Last 5 Matches — All Competitions</div>
    </div>
    <div class="card-body">
      <div class="form-cols">

        <div class="fcol">
          <div class="team-lab lab-s">
            <svg class="tl-badge" viewBox="0 0 100 100"><circle cx="50" cy="50" r="47" fill="#003087"/><path d="M50 18 L44 38 L37 55 L30 72 L38 72 L41 60 L44 60 L44 72 L56 72 L56 60 L59 60 L62 72 L70 72 L63 55 L56 38 Z" fill="#da291c"/></svg>
            PSG &mdash; Ligue 1 1st
          </div>
          <div class="match-list">
            <div class="mr"><div class="rd W"></div><div class="ms">3–1</div><div class="mo">Toulouse</div><div class="mc">L1 · Home</div></div>
            <div class="mr"><div class="rd W"></div><div class="ms">4–2</div><div class="mo">Chelsea</div><div class="mc">UCL R16 · Away</div></div>
            <div class="mr"><div class="rd W"></div><div class="ms">4–0</div><div class="mo">Chelsea</div><div class="mc">UCL R16 · Home</div></div>
            <div class="mr"><div class="rd W"></div><div class="ms">2–0</div><div class="mo">Lens</div><div class="mc">Ligue 1 · Away</div></div>
            <div class="mr"><div class="rd W"></div><div class="ms">2–1</div><div class="mo">Monaco</div><div class="mc">UCL KO · Home</div></div>
          </div>
        </div>

        <div class="fcol">
          <div class="team-lab lab-l">
            <svg class="tl-badge" viewBox="0 0 100 100"><circle cx="50" cy="50" r="47" fill="#c8102e"/><circle cx="50" cy="36" r="12" fill="#fff" opacity="0.9"/></svg>
            Liverpool &mdash; PL 5th
          </div>
          <div class="match-list">
            <div class="mr"><div class="rd L"></div><div class="ms">0–4</div><div class="mo">Manchester City</div><div class="mc">FA Cup · Away</div></div>
            <div class="mr"><div class="rd L"></div><div class="ms">1–2</div><div class="mo">Brighton</div><div class="mc">PL · Away</div></div>
            <div class="mr"><div class="rd W"></div><div class="ms">4–0</div><div class="mo">Galatasaray</div><div class="mc">UCL R16 · Home</div></div>
            <div class="mr"><div class="rd L"></div><div class="ms">0–1</div><div class="mo">Galatasaray</div><div class="mc">UCL R16 · Away</div></div>
            <div class="mr"><div class="rd L"></div><div class="ms">1–2</div><div class="mo">Wolves</div><div class="mc">PL · Home</div></div>
          </div>
        </div>

      </div>
      <div class="f-leg">
        <div class="fl"><div class="fld" style="background:var(--low)"></div>Win</div>
        <div class="fl"><div class="fld" style="background:var(--med)"></div>Draw</div>
        <div class="fl"><div class="fld" style="background:var(--high)"></div>Loss</div>
      </div>
    </div>
  </div>

  <!-- SEASON AVERAGES -->
  <div class="card fw">
    <div class="card-hd">
      <div class="hd-dot" style="background:#a78bfa"></div>
      <div class="hd-title">Season Averages per Match</div>
    </div>
    <div class="card-body">
      <div class="avg-pair">
        <div class="a-grp">
          <div class="a-grp-lbl" style="color:#7aafff">PSG — Ligue 1 &amp; UCL 25/26</div>
          <div class="avg-g">
            <div class="ac"><div class="av">17.9</div><div class="al">Shots</div></div>
            <div class="ac"><div class="av">7.0</div><div class="al">SOT</div></div>
            <div class="ac"><div class="av">5.3</div><div class="al">Corners</div></div>
            <div class="ac"><div class="av">2.4</div><div class="al">Goals/Gm</div></div>
          </div>
          <div class="avg-g" style="margin-top:6px">
            <div class="ac"><div class="av">67%</div><div class="al">Possession</div></div>
            <div class="ac"><div class="av">8–2</div><div class="al">v Chelsea (agg)</div></div>
            <div class="ac"><div class="av">15</div><div class="al">Goals last 4</div></div>
            <div class="ac"><div class="av">41%</div><div class="al">Clean sheet %</div></div>
          </div>
        </div>
        <div class="a-grp">
          <div class="a-grp-lbl" style="color:#f07070">Liverpool — PL &amp; UCL 25/26</div>
          <div class="avg-g">
            <div class="ac"><div class="av">13.8</div><div class="al">Shots</div></div>
            <div class="ac"><div class="av">4.5</div><div class="al">SOT</div></div>
            <div class="ac"><div class="av">4.5</div><div class="al">Corners</div></div>
            <div class="ac"><div class="av">1.9</div><div class="al">Goals/Gm</div></div>
          </div>
          <div class="avg-g" style="margin-top:6px">
            <div class="ac"><div class="av">53%</div><div class="al">Possession</div></div>
            <div class="ac"><div class="av">15</div><div class="al">PL Losses</div></div>
            <div class="ac"><div class="av">5th</div><div class="al">PL Position</div></div>
            <div class="ac"><div class="av">29%</div><div class="al">Clean sheet %</div></div>
          </div>
        </div>
      </div>
    </div>
  </div>

  <!-- H2H -->
  <div class="card fw">
    <div class="card-hd">
      <div class="hd-dot" style="background:var(--high)"></div>
      <div class="hd-title">Head to Head — Last 5 Meetings (UEFA Comps)</div>
    </div>
    <div class="card-body">
      <div class="h2h-bar">
        <div class="hs"><div class="hn" style="color:#7aafff">2</div><div class="hl">PSG Wins</div></div>
        <div class="hd"></div>
        <div class="hs"><div class="hn" style="color:var(--med)">1</div><div class="hl">Draw / Pens</div></div>
        <div class="hd"></div>
        <div class="hs"><div class="hn" style="color:#f07070">2</div><div class="hl">Liverpool Wins</div></div>
        <div class="hd"></div>
        <div class="hs"><div class="hn">1–0</div><div class="hl">Avg margin</div></div>
      </div>
      <div class="h2h-rows">
        <div class="h2h-r">
          <div class="rh">Liverpool</div><div class="rs">1–1 &nbsp;<span class="leg-note">[1–4p]</span></div><div class="ra">PSG</div>
          <div class="rsub">UCL Round of 16 2nd Leg · Anfield · Mar 2025 · PSG advance</div>
        </div>
        <div class="h2h-r">
          <div class="rh">PSG</div><div class="rs">0–1</div><div class="ra">Liverpool</div>
          <div class="rsub">UCL Round of 16 1st Leg · Parc des Princes · Mar 2025</div>
        </div>
        <div class="h2h-r">
          <div class="rh">PSG</div><div class="rs">2–1</div><div class="ra">Liverpool</div>
          <div class="rsub">UCL Group Stage · Parc des Princes · Nov 2018</div>
        </div>
        <div class="h2h-r">
          <div class="rh">Liverpool</div><div class="rs">3–2</div><div class="ra">PSG</div>
          <div class="rsub">UCL Group Stage · Anfield · Sep 2018</div>
        </div>
        <div class="h2h-r">
          <div class="rh">Liverpool</div><div class="rs">2–0</div><div class="ra">PSG</div>
          <div class="rsub">UEFA Cup Winners' Cup SF · Anfield · Apr 1997</div>
        </div>
      </div>
      <p style="font-size:11px;color:var(--muted);margin-top:10px;">All six UEFA meetings settled by 1 goal or on penalties. PSG knocked Liverpool out last season despite losing the 1st leg 1–0. No goalless draws in any meeting. Liverpool have won only 1 of their last 3 competitive away games vs French clubs.</p>
    </div>
  </div>

  <!-- PREDICTIONS PSG vs LFC -->
  <div class="card fw">
    <div class="card-hd">
      <div class="hd-dot" style="background:var(--low)"></div>
      <div class="hd-title">Weighted Predictions — PSG vs Liverpool (Both Teams)</div>
    </div>
    <div class="card-body">
      <div class="pred-leg">
        <div class="pli"><div class="pld" style="background:var(--low)"></div><span style="color:var(--low);font-weight:700">Low</span> = conservative floor</div>
        <div class="pli"><div class="pld" style="background:var(--med)"></div><span style="color:var(--med);font-weight:700">Median</span> = weighted average expected</div>
        <div class="pli"><div class="pld" style="background:var(--high)"></div><span style="color:var(--high);font-weight:700">High</span> = ceiling</div>
      </div>
      <div class="pw">
      <table class="pt">
        <colgroup><col class="cm"><col class="cl"><col class="cn"><col class="ch"><col class="cb"></colgroup>
        <thead><tr><th>Metric</th><th style="color:var(--low)">Low</th><th class="th-m">Median</th><th style="color:var(--high)">High</th><th style="text-align:center;color:var(--muted)">Intensity</th></tr></thead>
        <tbody>
          <tr><td class="cmc">Corners</td>        <td><span class="lv">7</span></td><td><span class="mv">10</span></td><td><span class="hv">15</span></td><td><div class="bw"><div class="bf bf-psg" style="width:60%"></div></div></td></tr>
          <tr><td class="cmc">Total Shots</td>    <td><span class="lv">22</span></td><td><span class="mv">27</span></td><td><span class="hv">38</span></td><td><div class="bw"><div class="bf bf-psg" style="width:72%"></div></div></td></tr>
          <tr><td class="cmc">Shots on Target</td><td><span class="lv">7</span></td><td><span class="mv">11</span></td><td><span class="hv">17</span></td><td><div class="bw"><div class="bf bf-psg" style="width:66%"></div></div></td></tr>
          <tr><td class="cmc">Fouls</td>          <td><span class="lv">17</span></td><td><span class="mv">22</span></td><td><span class="hv">30</span></td><td><div class="bw"><div class="bf bf-psg" style="width:58%"></div></div></td></tr>
          <tr><td class="cmc">Throw-ins</td>      <td><span class="lv">36</span></td><td><span class="mv">46</span></td><td><span class="hv">62</span></td><td><div class="bw"><div class="bf bf-psg" style="width:68%"></div></div></td></tr>
          <tr><td class="cmc">Goal Kicks</td>     <td><span class="lv">14</span></td><td><span class="mv">19</span></td><td><span class="hv">28</span></td><td><div class="bw"><div class="bf bf-psg" style="width:56%"></div></div></td></tr>
          <tr><td class="cmc">Tackles</td>        <td><span class="lv">24</span></td><td><span class="mv">30</span></td><td><span class="hv">42</span></td><td><div class="bw"><div class="bf bf-psg" style="width:64%"></div></div></td></tr>
          <tr><td class="cmc">Offsides</td>       <td><span class="lv">3</span></td><td><span class="mv">6</span></td><td><span class="hv">11</span></td><td><div class="bw"><div class="bf bf-psg" style="width:52%"></div></div></td></tr>
        </tbody>
      </table>
      </div>
    </div>
  </div>

  <!-- NOTES PSG vs LFC -->
  <div class="card fw">
    <div class="card-hd">
      <div class="hd-dot" style="background:#60a5fa"></div>
      <div class="hd-title">Analytical Notes — Weighting Factors</div>
    </div>
    <div class="card-body">
      <div class="note-block"><strong>Corners (7–10–15):</strong> PSG earn 5.3 corners/UCL game at home; Liverpool concede territory away, earning only ~4–4.5 corners vs top opposition. Combined baseline: ~9–10. PSG's pacey wide play (Dembélé on the right, Kvaratskhelia left) will force corners throughout. The low end reflects a Liverpool that parks defensively and concedes few corners of their own; the high of 15 accounts for PSG dominance periods. <em>Weighted toward 10 given recent H2H tightness</em> — none of the last 5 meetings were free-flowing corner fests.</div>
      <div class="note-block"><strong>Total Shots (22–27–38):</strong> PSG average 17.9 shots at home; Liverpool ~13.8 away. Weighted combined baseline: 28–30, but PSG's possession dominance (67%) and Liverpool's current pressing inability suppresses the visitor's output. <em>Weighted low-end skew:</em> all 5 recent H2H meetings have been <1 goal margins; tight games produce fewer shots. High end requires a Liverpool collapse similar to their FA Cup display.</div>
      <div class="note-block"><strong>Shots on Target (7–11–17):</strong> PSG 7.0 SOT/game; Liverpool 4.5. Combined baseline ~11.5. Liverpool's chaotic high-line (exposed by Man City's runners) could gift PSG multiple clean SOT. The backup goalkeeper (Caoimhin Kelleher replacing Alisson) is a risk factor on high-pressure set pieces. <em>Median weighted at 11</em> respects the defensive nature of recent PSG–Liverpool meetings.</div>
      <div class="note-block"><strong>Fouls (17–22–30):</strong> PSG foul ~10/game in Ligue 1; Liverpool ~11–12. UCL QF pressure inflates this. Liverpool will commit tactical fouls to disrupt PSG's press-triggering build-up. Szoboszlai, Salah and Gravenberch will be physical. <em>Weighted toward 22</em> — the tactical importance of stopping PSG transitions makes this a foul-heavy tie, but neither side is gratuitously dirty.</div>
      <div class="note-block"><strong>Throw-ins (36–46–62):</strong> PSG's width-heavy system and Liverpool's wide press creates frequent boundary exits. In high-tempo Parc des Princes nights, transitions happen quickly and the ball goes out of play often. <em>Weighted toward 46</em> given the expected pace and pressing on both sides; high end if Liverpool concede ground and PSG recycle constantly in wide areas.</div>
      <div class="note-block"><strong>Goal Kicks (14–19–28):</strong> With PSG dominating possession (67%), Liverpool's goalkeeper will restart frequently under PSG's press. Kelleher (replacing Alisson) is less comfortable distributing under pressure and will resort to long clearances. PSG's Safonov faces fewer low-block attacks. <em>Weighted toward 19</em> — UCL QF average is ~20 combined; Liverpool's defensive shape inflates their contribution.</div>
      <div class="note-block"><strong>Tackles (24–30–42):</strong> PSG average ~13–14 tackles/Ligue 1 game; Liverpool ~14–15. Combined baseline: ~28–29. UCL QF intensity and Liverpool's need to win the ball back in transition (they have little other way to build) drives this up. <em>Weighted toward 30</em> — Liverpool's midfield will be especially aggressive given how far they're chasing the game tactically.</div>
      <div class="note-block"><strong>Offsides (3–6–11):</strong> PSG attack with sprint runners (Kvaratskhelia, Doué) who target the channels; Liverpool's high-line is disorganised and has been caught repeatedly this season. Combined expected: 5–6/game in UCL. <em>Weighted toward 6</em> — PSG's rapid transitions create more offside calls than a possession team; Liverpool's disorganised defensive shape means their own line isn't reliable enough to catch Dembélé consistently.</div>
    </div>
  </div>

</div><!-- /m-grid -->

<!-- ════════════ SECTION DIVIDER ════════════ -->
<div class="s-div">
  <div class="s-div-in"><span>★</span> Second Quarter-Final <span>★</span></div>
</div>

</div><!-- /page -->

<!-- ══════════════════════════════════════
     MATCH 2 HERO: BARCELONA vs ATLETICO
═══════════════════════════════════════ -->
<div class="match-hero mh-barca" id="barca">
  <div class="mh-glow"></div>
  <div class="hero-row">

    <!-- BARCELONA -->
    <div class="hero-team">
      <div class="club-badge">
        <svg viewBox="0 0 100 100" xmlns="http://www.w3.org/2000/svg">
          <circle cx="50" cy="50" r="47" fill="#004d98"/>
          <circle cx="50" cy="50" r="47" fill="none" stroke="rgba(255,255,255,0.15)" stroke-width="2"/>
          <!-- Diagonal stripe -->
          <path d="M30 20 L80 70 L80 80 L20 80 Z" fill="#a50044" opacity="0.7"/>
          <!-- Cross -->
          <rect x="44" y="18" width="12" height="64" fill="rgba(255,200,0,0.7)" rx="2"/>
          <rect x="18" y="44" width="64" height="12" fill="rgba(255,200,0,0.7)" rx="2"/>
          <!-- FCB text -->
          <text x="50" y="90" text-anchor="middle" font-family="Arial,sans-serif" font-size="9" font-weight="900" fill="#fff" letter-spacing="1.5">FCB</text>
        </svg>
      </div>
      <div class="h-name">BARCELONA</div>
      <div class="h-pos">La Liga Leaders · 7pts clear · Home</div>
    </div>

    <div class="vs-col">
      <div class="vs-big">VS</div>
      <div class="leg-tag">1st Leg</div>
      <div class="venue-txt">Spotify Camp Nou<br>Barcelona · Wed 8 Apr · 9pm CET</div>
    </div>

    <!-- ATLETICO -->
    <div class="hero-team">
      <div class="club-badge">
        <svg viewBox="0 0 100 100" xmlns="http://www.w3.org/2000/svg">
          <circle cx="50" cy="50" r="47" fill="#ce3524"/>
          <circle cx="50" cy="50" r="47" fill="none" stroke="rgba(255,255,255,0.18)" stroke-width="1.5"/>
          <!-- White and blue stripes (Atletico vertical) -->
          <rect x="20" y="18" width="11" height="64" fill="#fff" rx="1"/>
          <rect x="35" y="18" width="11" height="64" fill="#272e61" rx="1"/>
          <rect x="54" y="18" width="11" height="64" fill="#fff" rx="1"/>
          <rect x="69" y="18" width="11" height="64" fill="#272e61" rx="1"/>
          <!-- Bear & Strawberry tree (simplified circle) -->
          <circle cx="50" cy="78" r="6" fill="rgba(255,255,255,0.15)" stroke="rgba(255,255,255,0.3)" stroke-width="1"/>
          <!-- ATM text -->
          <text x="50" y="13" text-anchor="middle" font-family="Arial,sans-serif" font-size="8" font-weight="900" fill="#fff" letter-spacing="1">ATLÉTICO</text>
        </svg>
      </div>
      <div class="h-name">ATLÉTICO</div>
      <div class="h-pos">La Liga 4th · 3 losses in row · Away</div>
    </div>

  </div>
</div>

<div class="page">
<div class="m-grid">

  <!-- CONTEXT -->
  <div class="card fw">
    <div class="card-hd">
      <div class="hd-dot" style="background:var(--ucl-gold)"></div>
      <div class="hd-title">Match Context</div>
      <div class="hd-tag" style="color:var(--ucl-gold);border-color:rgba(201,168,64,0.28);background:rgba(201,168,64,0.07)">UCL QF · Leg 1 · 5th Meeting This Season</div>
    </div>
    <div class="card-body">
      <div class="callout">
        <strong>The El Clásico of the Cup</strong> — this will be the <em>fifth meeting between these sides in just two months</em>. Barcelona have won three of the four (twice in La Liga, once in Copa del Rey). Atlético won 4–0 in the Copa away leg but lost the tie overall. <strong>Barcelona just beat Atletico 2–1 in La Liga on Saturday</strong> with Lewandowski's 87th-minute winner, going 7pts clear. Atletico have lost <em>three consecutive matches</em> and carry Simeone's UCL record (W2 D2 L4) away from home this season. Barcelona stormed past Newcastle 8–3 on aggregate. Key absences: <strong>Raphinha (5 weeks, hip), Frenkie de Jong, Marc Bernal, Andreas Christensen</strong> all out for Barcelona. Atletico missing <strong>Jan Oblak</strong> (first-choice GK) and others — backup Musso expected to start.
      </div>
    </div>
  </div>

  <!-- LAST 5 FORM -->
  <div class="card fw">
    <div class="card-hd">
      <div class="hd-dot" style="background:#7ab0ff"></div>
      <div class="hd-title">Last 5 Matches — All Competitions</div>
    </div>
    <div class="card-body">
      <div class="form-cols">

        <div class="fcol">
          <div class="team-lab lab-b">
            <svg class="tl-badge" viewBox="0 0 100 100"><circle cx="50" cy="50" r="47" fill="#004d98"/><path d="M30 20 L80 70 L80 80 L20 80 Z" fill="#a50044" opacity="0.7"/></svg>
            Barcelona &mdash; La Liga 1st
          </div>
          <div class="match-list">
            <div class="mr"><div class="rd W"></div><div class="ms">2–1</div><div class="mo">Atlético Madrid</div><div class="mc">La Liga · Away</div></div>
            <div class="mr"><div class="rd W"></div><div class="ms">7–2</div><div class="mo">Newcastle Utd</div><div class="mc">UCL R16 · Home</div></div>
            <div class="mr"><div class="rd W"></div><div class="ms">3–1</div><div class="mo">Real Sociedad</div><div class="mc">La Liga · Home</div></div>
            <div class="mr"><div class="rd W"></div><div class="ms">4–1</div><div class="mo">Newcastle Utd</div><div class="mc">UCL R16 · Away</div></div>
            <div class="mr"><div class="rd D"></div><div class="ms">2–2</div><div class="mo">Girona</div><div class="mc">La Liga · Away</div></div>
          </div>
        </div>

        <div class="fcol">
          <div class="team-lab lab-a">
            <svg class="tl-badge" viewBox="0 0 100 100"><circle cx="50" cy="50" r="47" fill="#ce3524"/><rect x="22" y="22" width="10" height="56" fill="#fff" rx="1"/><rect x="37" y="22" width="10" height="56" fill="#272e61" rx="1"/></svg>
            Atletico &mdash; La Liga 4th
          </div>
          <div class="match-list">
            <div class="mr"><div class="rd L"></div><div class="ms">1–2</div><div class="mo">Barcelona</div><div class="mc">La Liga · Home</div></div>
            <div class="mr"><div class="rd L"></div><div class="ms">2–3</div><div class="mo">Real Madrid</div><div class="mc">La Liga · Away</div></div>
            <div class="mr"><div class="rd W"></div><div class="ms">3–0</div><div class="mo">Tottenham</div><div class="mc">UCL R16 · Home</div></div>
            <div class="mr"><div class="rd W"></div><div class="ms">2–3</div><div class="mo">Tottenham</div><div class="mc">UCL R16 · Away</div></div>
            <div class="mr"><div class="rd L"></div><div class="ms">0–4</div><div class="mo">Barcelona</div><div class="mc">Copa del Rey · Away</div></div>
          </div>
        </div>

      </div>
      <div class="f-leg">
        <div class="fl"><div class="fld" style="background:var(--low)"></div>Win</div>
        <div class="fl"><div class="fld" style="background:var(--med)"></div>Draw</div>
        <div class="fl"><div class="fld" style="background:var(--high)"></div>Loss</div>
      </div>
    </div>
  </div>

  <!-- SEASON AVERAGES -->
  <div class="card fw">
    <div class="card-hd">
      <div class="hd-dot" style="background:#a78bfa"></div>
      <div class="hd-title">Season Averages per Match — UCL &amp; League 25/26</div>
    </div>
    <div class="card-body">
      <div class="avg-pair">
        <div class="a-grp">
          <div class="a-grp-lbl" style="color:#7ab0ff">Barcelona — La Liga &amp; UCL</div>
          <div class="avg-g">
            <div class="ac"><div class="av">19.7</div><div class="al">Shots</div></div>
            <div class="ac"><div class="av">7.2</div><div class="al">SOT</div></div>
            <div class="ac"><div class="av">6.8</div><div class="al">Corners</div></div>
            <div class="ac"><div class="av">3.2</div><div class="al">Goals/Gm</div></div>
          </div>
          <div class="avg-g" style="margin-top:6px">
            <div class="ac"><div class="av">65%</div><div class="al">Possession</div></div>
            <div class="ac"><div class="av">30</div><div class="al">UCL Goals</div></div>
            <div class="ac"><div class="av">17</div><div class="al">UCL GA</div></div>
            <div class="ac"><div class="av">15–0</div><div class="al">Home W–L La Liga</div></div>
          </div>
        </div>
        <div class="a-grp">
          <div class="a-grp-lbl" style="color:#f07060">Atlético — La Liga &amp; UCL</div>
          <div class="avg-g">
            <div class="ac"><div class="av">14.6</div><div class="al">Shots</div></div>
            <div class="ac"><div class="av">5.6</div><div class="al">SOT</div></div>
            <div class="ac"><div class="av">4.7</div><div class="al">Corners</div></div>
            <div class="ac"><div class="av">2.6</div><div class="al">Goals/Gm</div></div>
          </div>
          <div class="avg-g" style="margin-top:6px">
            <div class="ac"><div class="av">52%</div><div class="al">Possession</div></div>
            <div class="ac"><div class="av">31</div><div class="al">UCL Goals</div></div>
            <div class="ac"><div class="av">24</div><div class="al">UCL GA</div></div>
            <div class="ac"><div class="av">702</div><div class="al">Alvarez pressures</div></div>
          </div>
        </div>
      </div>
    </div>
  </div>

  <!-- H2H -->
  <div class="card fw">
    <div class="card-hd">
      <div class="hd-dot" style="background:var(--high)"></div>
      <div class="hd-title">Head to Head — Last 5 Meetings (All Comps)</div>
    </div>
    <div class="card-body">
      <div class="h2h-bar">
        <div class="hs"><div class="hn" style="color:#7ab0ff">3</div><div class="hl">Barca Wins</div></div>
        <div class="hd"></div>
        <div class="hs"><div class="hn" style="color:var(--med)">0</div><div class="hl">Draws</div></div>
        <div class="hd"></div>
        <div class="hs"><div class="hn" style="color:#f07060">2</div><div class="hl">Atletico Wins</div></div>
        <div class="hd"></div>
        <div class="hs"><div class="hn">3.2</div><div class="hl">Avg Goals/Mtg</div></div>
      </div>
      <div class="h2h-rows">
        <div class="h2h-r">
          <div class="rh">Atlético Madrid</div><div class="rs">1–2</div><div class="ra">Barcelona</div>
          <div class="rsub">La Liga · Estadio Metropolitano · Apr 2026</div>
        </div>
        <div class="h2h-r">
          <div class="rh">Atlético Madrid</div><div class="rs">4–0</div><div class="ra">Barcelona</div>
          <div class="rsub">Copa del Rey · Metropolitano (2nd leg, Atléti advance) · Mar 2026</div>
        </div>
        <div class="h2h-r">
          <div class="rh">Barcelona</div><div class="rs">3–0</div><div class="ra">Atlético Madrid</div>
          <div class="rsub">Copa del Rey · Camp Nou (1st leg) · Feb 2026</div>
        </div>
        <div class="h2h-r">
          <div class="rh">Barcelona</div><div class="rs">4–0</div><div class="ra">Atlético Madrid</div>
          <div class="rsub">La Liga · Camp Nou · Jan 2026</div>
        </div>
        <div class="h2h-r">
          <div class="rh">Atlético Madrid</div><div class="rs">2–1</div><div class="ra">Barcelona</div>
          <div class="rsub">La Liga · Estadio Metropolitano · Nov 2025</div>
        </div>
      </div>
      <p style="font-size:11px;color:var(--muted);margin-top:10px;">Over 2.5 goals in 8 of their last 9 meetings. Over 8.5 corners in 10 consecutive head-to-heads. Barcelona are <em>unbeaten in 25 home games against Atletico</em>. Atletico have eliminated Barca in both previous UCL QF meetings (2014, 2016) but have never won a UCL away game vs Spanish opposition (L4 D1). Atlético missing Jan Oblak adds significant goalkeeper vulnerability.</p>
    </div>
  </div>

  <!-- PREDICTIONS BAR vs ATM -->
  <div class="card fw">
    <div class="card-hd">
      <div class="hd-dot" style="background:var(--low)"></div>
      <div class="hd-title">Weighted Predictions — Barcelona vs Atlético (Both Teams)</div>
    </div>
    <div class="card-body">
      <div class="pred-leg">
        <div class="pli"><div class="pld" style="background:var(--low)"></div><span style="color:var(--low);font-weight:700">Low</span> = conservative floor</div>
        <div class="pli"><div class="pld" style="background:var(--med)"></div><span style="color:var(--med);font-weight:700">Median</span> = weighted average expected</div>
        <div class="pli"><div class="pld" style="background:var(--high)"></div><span style="color:var(--high);font-weight:700">High</span> = ceiling</div>
      </div>
      <div class="pw">
      <table class="pt">
        <colgroup><col class="cm"><col class="cl"><col class="cn"><col class="ch"><col class="cb"></colgroup>
        <thead><tr><th>Metric</th><th style="color:var(--low)">Low</th><th class="th-m">Median</th><th style="color:var(--high)">High</th><th style="text-align:center;color:var(--muted)">Intensity</th></tr></thead>
        <tbody>
          <tr><td class="cmc">Corners</td>        <td><span class="lv">9</span></td><td><span class="mv">13</span></td><td><span class="hv">18</span></td><td><div class="bw"><div class="bf bf-barca" style="width:76%"></div></div></td></tr>
          <tr><td class="cmc">Total Shots</td>    <td><span class="lv">24</span></td><td><span class="mv">31</span></td><td><span class="hv">44</span></td><td><div class="bw"><div class="bf bf-barca" style="width:80%"></div></div></td></tr>
          <tr><td class="cmc">Shots on Target</td><td><span class="lv">9</span></td><td><span class="mv">13</span></td><td><span class="hv">20</span></td><td><div class="bw"><div class="bf bf-barca" style="width:74%"></div></div></td></tr>
          <tr><td class="cmc">Fouls</td>          <td><span class="lv">20</span></td><td><span class="mv">28</span></td><td><span class="hv">38</span></td><td><div class="bw"><div class="bf bf-barca" style="width:78%"></div></div></td></tr>
          <tr><td class="cmc">Throw-ins</td>      <td><span class="lv">38</span></td><td><span class="mv">50</span></td><td><span class="hv">66</span></td><td><div class="bw"><div class="bf bf-barca" style="width:76%"></div></div></td></tr>
          <tr><td class="cmc">Goal Kicks</td>     <td><span class="lv">15</span></td><td><span class="mv">22</span></td><td><span class="hv">32</span></td><td><div class="bw"><div class="bf bf-barca" style="width:68%"></div></div></td></tr>
          <tr><td class="cmc">Tackles</td>        <td><span class="lv">26</span></td><td><span class="mv">35</span></td><td><span class="hv">48</span></td><td><div class="bw"><div class="bf bf-barca" style="width:82%"></div></div></td></tr>
          <tr><td class="cmc">Offsides</td>       <td><span class="lv">4</span></td><td><span class="mv">8</span></td><td><span class="hv">14</span></td><td><div class="bw"><div class="bf bf-barca" style="width:72%"></div></div></td></tr>
        </tbody>
      </table>
      </div>
    </div>
  </div>

  <!-- NOTES BAR vs ATM -->
  <div class="card fw">
    <div class="card-hd">
      <div class="hd-dot" style="background:#60a5fa"></div>
      <div class="hd-title">Analytical Notes — Weighting Factors</div>
    </div>
    <div class="card-body">
      <div class="note-block"><strong>Corners (9–13–18):</strong> This is the highest corner median of all four QF matches. H2H data is definitive: <em>over 8.5 corners in 10 consecutive meetings</em>. Barcelona earn 6.8 corners/game, Atlético 4.7. Combined baseline: 11.5. Barcelona's narrow high-tempo possession football (Yamal on the right wing) constantly forces corners against deep defences. <em>Weighted to 13</em> — the H2H trend is the single strongest statistical anchor; the high end of 18 is possible if Barcelona dominate for long periods against a depleted Atlético defensive unit.</div>
      <div class="note-block"><strong>Total Shots (24–31–44):</strong> The highest shot projection of all four QFs. Barcelona fire 19.7 shots/game; Atlético 14.6. Combined: 34.3 baseline. Barcelona allowed Newcastle 14 shots in a 7–2 home win — both teams attack aggressively. Flick's high line invites Atlético counter-attacks. <em>Weighted to 31</em> — over 2.5 goals in 8 of 9 recent meetings strongly suggests a high-volume, open game at Camp Nou.</div>
      <div class="note-block"><strong>Shots on Target (9–13–20):</strong> Barcelona's 7.2 SOT at home + Atlético's 5.6 = 12.8 combined baseline. Without Oblak in goal, Atlético are more vulnerable to Barcelona's technical finishing. Julián Alvarez and Griezmann will create dangerous counter-attacks against Flick's high line. <em>Weighted to 13</em> — both keepers (Barcelona's Joan García and Atlético's Musso) may face heavy workloads. High end of 20 is the most plausible ceiling of all four QFs.</div>
      <div class="note-block"><strong>Fouls (20–28–38):</strong> This is the highest projected foul count of all four QFs. Atlético under Simeone are tactically physical, averaging ~13+ fouls/UCL game. Julian Alvarez alone committed 702 pressures — that intensity results in fouls. The rivalry is heated (Nico González red card on Saturday). <em>Weighted to 28</em> — a familiarity-bred intensity. Referee Istvan Kovacs averages high card counts. High end of 38 if Atlético respond to early Barcelona pressure with a cynical foul strategy.</div>
      <div class="note-block"><strong>Throw-ins (38–50–66):</strong> Camp Nou's possession-dominated games create wide-area congestion. Both teams press wide aggressively — Yamal on the right, Rashford left; Atlético's Giuliano Simeone and Lookman contest every wide duel. UCL high-intensity clashes average 46–52 throw-ins; the familiarity of these sides and the emotional temperature boost the median to 50. <em>High end of 66</em> if Simeone's press creates chaotic possession transitions throughout.</div>
      <div class="note-block"><strong>Goal Kicks (15–22–32):</strong> Barcelona's aggressive high press will force Atlético's backup keeper (Musso) to launch long balls repeatedly. Barcelona's own keeper Joan García faces Atlético's powerful counter-attacks and high-press triggers. Combined: higher than a typical UCL game. <em>Weighted to 22</em> — Atlético's long-ball counter-strategy under pressure inflates their GK contribution significantly.</div>
      <div class="note-block"><strong>Tackles (26–35–48):</strong> The highest tackle projection across all four QF matches this week. Atlético (Simeone system) average ~16–18 tackles/game; Barcelona ~14–15. Combined baseline: ~31–33. UCL QF intensity and the personal rivalry element between players who know each other intimately from four recent meetings drives this to a median of 35. <em>High of 48</em> if Atlético adopt a sit-and-disrupt approach in second half.</div>
      <div class="note-block"><strong>Offsides (4–8–14):</strong> The highest offside projection of the four QFs. Barcelona play a famously aggressive high defensive line (exposed by Newcastle for some offsides during 7–2); Atlético's pace runners — Griezmann, Sørloth, Alvarez — exploit space behind the line. In their last 4 meetings combined, there have been 28+ offsides. <em>Weighted to 8</em> — Flick's high line is a known offside trap weapon, and Atlético's direct counter-attack game will test it repeatedly throughout the night.</div>
    </div>
  </div>

</div><!-- /m-grid -->
</div><!-- /page -->

<footer>
  <strong>TEAM BILBO Statistical Analysis</strong><br>Predictions are statistical estimates based on actual data, H2H analysis and contextual factors. <strong>Not financial advice.</strong><br> · 8 April 2026 ·
</footer>
</body>
</html>
