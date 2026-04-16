<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0, maximum-scale=1.0, user-scalable=no">
<meta name="description" content="Team Bilbo Statistical Analytics: UEFA Europa League Quarter-Finals Second Leg Predictions">
<title>UEL QF 2nd Legs · Aston Villa vs Bologna · Nott'm Forest vs Porto</title>
<link rel="preconnect" href="https://fonts.googleapis.com">
<link href="https://fonts.googleapis.com/css2?family=Outfit:wght@300;400;600;800;900&family=Inter:wght@400;500;600;700&display=swap" rel="stylesheet">
<style>
/* ══════════════════════════════════
   ROOT TOKENS & BASE
══════════════════════════════════ */
:root {
  --bg:          #0a0a0a;
  --bg2:         #121212;
  --bg3:         #1a1a1a;
  --bg4:         #242424;
  --bg5:         #2a2a2a;
  --border:      rgba(255,255,255,.08);
  --bm:          rgba(255,255,255,.15);
  --text:        #e0e0e0;
  --muted:       #888888;
  --hi:          #b0b0b0;
  
  /* UEL Branding */
  --uel-orange:  #F68E00;
  --uel-dark:    #1a1005;
  --uel-gs:      rgba(246, 142, 0, 0.12);
  
  /* Aston Villa */
  --avl-clr:     #670E36;
  --avl-blu:     #95BFE5;
  --avl-l:       rgba(103, 14, 54, 0.25);
  
  /* Bologna */
  --bol-r:       #A21A22;
  --bol-b:       #16214A;
  --bol-l:       rgba(162, 26, 34, 0.25);
  
  /* Nottingham Forest */
  --nfo-r:       #E53233;
  --nfo-l:       rgba(229, 50, 51, 0.25);
  
  /* FC Porto */
  --fcp-b:       #00428C;
  --fcp-l:       rgba(0, 66, 140, 0.25);

  /* stats */
  --lo:          #0fd9a2;
  --md:          #f7c948;
  --hic:         #f55929;
}

*, *::before, *::after { margin:0; padding:0; box-sizing:border-box; }
html { scroll-behavior:smooth; -webkit-text-size-adjust: 100%; }
body {
  font-family:'Inter', sans-serif;
  background:var(--bg);
  color:var(--text);
  font-size:14px;
  line-height:1.5;
  -webkit-font-smoothing:antialiased;
  overflow-x:hidden;
}

/* ══════ ANIMATIONS ══════ */
@keyframes glow { 0%,100%{opacity:.6} 50%{opacity:1} }
@keyframes popBadge { from{transform:scale(.6)rotate(-8deg);opacity:0} to{transform:scale(1)rotate(0);opacity:1} }

/* ══════ SITE HEADER ══════ */
.site-header {
  position:relative; z-index:2;
  background:linear-gradient(170deg, var(--uel-dark) 0%, var(--bg2) 50%, rgba(246,142,0,.05) 100%);
  border-bottom:1px solid rgba(246,142,0,.35);
  text-align:center;
  padding:20px 14px;
}
.uel-chip {
  display:inline-flex; align-items:center; gap:8px;
  font-family:'Outfit',sans-serif; font-size:10px; font-weight:800;
  letter-spacing:1.5px; text-transform:uppercase;
  color:var(--uel-orange); background:var(--uel-gs);
  border:1px solid rgba(246,142,0,.35);
  padding:4px 12px; border-radius:20px; margin-bottom:10px;
}
.site-header h1 {
  font-family:'Outfit',sans-serif; font-size:22px; font-weight:900; 
  letter-spacing:0.5px; text-transform:uppercase; color:#fff; line-height:1.2;
}
.site-header .sub { font-size:12px; color:var(--muted); margin-top:6px; }

/* ══════ TIE STATUS ══════ */
.tie-status {
  padding:14px 16px;
  display:flex; align-items:flex-start; gap:10px;
  border-bottom: 1px solid var(--border);
}
.ts-1 { background:linear-gradient(135deg,rgba(103,14,54,.15),var(--bg2)); border-bottom-color:rgba(103,14,54,.3); }
.ts-2 { background:linear-gradient(135deg,rgba(229,50,51,.15),var(--bg2)); border-bottom-color:rgba(229,50,51,.3); }
.ts-icon { font-size:20px; flex-shrink:0; margin-top:2px; animation:glow 2s ease-in-out infinite; }
.ts-text { font-size:12px; line-height:1.6; color:var(--hi); }
.ts-text strong { font-weight:700; color: #fff; }
.ts-agg { display:block; font-family:'Outfit',sans-serif; font-size:16px; font-weight:900; letter-spacing:1px; margin-top: 6px; }

/* ══════ MATCH HERO (MOBILE FIRST) ══════ */
.match-hero {
  padding:20px 14px; border-bottom:1px solid var(--bm);
}
.mh-1 { background:linear-gradient(135deg, var(--avl-l) 0%, var(--bg2) 50%, var(--bol-l) 100%); }
.mh-2 { background:linear-gradient(135deg, var(--nfo-l) 0%, var(--bg2) 50%, var(--fcp-l) 100%); }
.hero-inner {
  display:flex; align-items:center; justify-content:space-between; gap:8px;
  max-width: 100%; margin:0 auto;
}
.h-team { display:flex; flex-direction:column; align-items:center; gap:6px; flex:1; }
.badge-wrap {
  width:60px; height:60px; border-radius:50%;
  border:1.5px solid var(--bm); background:rgba(255,255,255,.08);
  display:flex; align-items:center; justify-content:center; overflow:hidden;
  filter:drop-shadow(0 4px 12px rgba(0,0,0,.4));
  animation:popBadge .5s cubic-bezier(.34,1.56,.64,1) both;
}
.badge-wrap img { width:40px; height:40px; object-fit:contain; }
.h-name { font-family:'Outfit',sans-serif; font-size:13px; font-weight:800; text-transform:uppercase; text-align:center; color:#fff; line-height:1.1; }
.h-pos { font-size:9px; color:var(--muted); text-transform:uppercase; letter-spacing:0.5px; text-align:center; font-weight: 600; }

.vs-col { display:flex; flex-direction:column; align-items:center; gap:4px; flex-shrink:0; }
.vs-txt { font-family:'Outfit',sans-serif; font-size:18px; font-weight:900; color:rgba(255,255,255,.15); letter-spacing:2px; }
.ko-chip {
  font-family:'Outfit',sans-serif; font-size:9px; font-weight:800; letter-spacing:1px;
  color:var(--uel-orange); background:var(--uel-gs); border:1px solid rgba(246,142,0,.3);
  padding:2px 8px; border-radius:4px; text-transform: uppercase;
}
.venue-txt { font-size:9px; color:var(--muted); text-align:center; line-height:1.3; font-weight: 500; }

/* ══════ SCORE BOX ══════ */
.score-box {
  background:linear-gradient(135deg,var(--bg3),var(--bg4));
  border:1px solid var(--bm); border-radius:12px;
  padding:16px 14px; margin-bottom:16px;
}
.sb-title {
  font-family:'Outfit',sans-serif; font-size:11px; font-weight:800;
  letter-spacing:1.5px; text-transform:uppercase; color:var(--hi);
  text-align:center; margin-bottom:14px; border-bottom: 1px solid var(--border); padding-bottom: 10px;
}
.scores-row { display:flex; gap:8px; justify-content:center; flex-wrap:wrap; }
.sc {
  background:var(--bg5); border:1px solid var(--border); border-radius:8px;
  padding:12px; text-align:center; flex:1; min-width:100px;
}
.sc-label { font-family:'Outfit',sans-serif; font-size:9px; font-weight:700; letter-spacing:1px; text-transform:uppercase; color:var(--muted); margin-bottom:6px; }
.sc-value { font-family:'Outfit',sans-serif; font-size:28px; font-weight:900; letter-spacing:2px; line-height:1; color:#fff; }
.sc-prob { font-size:9px; color:var(--muted); margin-top:6px; font-weight: 500; }
.sc-best { border-color:rgba(246,142,0,.4); background:linear-gradient(135deg,rgba(246,142,0,.08),var(--bg5)); }
.sc-best .sc-label { color:var(--uel-orange); }
.sb-notes { font-size:12px; color:var(--hi); line-height:1.6; margin-top:14px; padding: 10px; background: rgba(0,0,0,0.2); border-radius: 8px; }
.sb-notes strong { color:var(--md); font-weight:700; }

/* ══════ PAGE & CARDS ══════ */
.page { width:100%; max-width:1200px; margin:0 auto; padding:16px 12px 40px; }

.card {
  background:var(--bg2); border:1px solid var(--border);
  border-radius:12px; overflow:hidden; margin-bottom:16px;
  opacity:0; transform:translateY(14px);
  transition:opacity .5s ease, transform .5s ease;
}
.card.vis { opacity:1; transform:translateY(0); }
.card-hd {
  padding:12px 14px; border-bottom:1px solid var(--border);
  display:flex; align-items:center; gap:8px; background: rgba(255,255,255,0.02);
}
.hd-dot { width:6px; height:6px; border-radius:50%; flex-shrink:0; }
.hd-title { font-family:'Outfit',sans-serif; font-size:11px; font-weight:800; letter-spacing:1px; text-transform:uppercase; color:var(--muted); flex:1; }
.card-body { padding:14px; }

/* Form cols (Stack on mobile, side-by-side on desktop) */
.form-cols { display:flex; flex-direction:column; gap:16px; }
.team-lab {
  display:inline-flex; align-items:center; gap:6px;
  font-size:10px; font-weight:700; letter-spacing:1px; text-transform:uppercase;
  padding:4px 8px; border-radius:6px; margin-bottom:8px; border:1px solid;
}
.lab-avl { background:var(--avl-l); color:#fff; border-color:var(--avl-clr); }
.lab-bol { background:var(--bol-l); color:#fff; border-color:var(--bol-r); }
.lab-nfo { background:var(--nfo-l); color:#fff; border-color:var(--nfo-r); }
.lab-fcp { background:var(--fcp-l); color:#fff; border-color:var(--fcp-b); }
.tl-img { width:14px; height:14px; object-fit:contain; }

.match-list { display:flex; flex-direction:column; gap:4px; }
.mr {
  display:grid; grid-template-columns:8px 40px 1fr auto;
  align-items:center; gap:8px; background:var(--bg3); border:1px solid var(--border);
  border-radius:6px; padding:6px 10px;
}
.rd { width:8px; height:8px; border-radius:50%; }
.rd.W { background:var(--lo); box-shadow:0 0 6px rgba(15,217,162,.4); }
.rd.D { background:var(--md); }
.rd.L { background:var(--hic); box-shadow:0 0 6px rgba(245,89,41,.4); }
.ms { font-family:'Outfit',sans-serif; font-size:13px; font-weight:800; color:#fff; text-align:center; }
.mo { font-size:11px; color:var(--text); font-weight:500; white-space:nowrap; overflow:hidden; text-overflow:ellipsis; }
.mc { font-size:9px; color:var(--muted); text-align:right; text-transform:uppercase; letter-spacing:0.5px; }

/* Averages Grid */
.avg-pair { display:flex; flex-direction:column; gap:16px; }
.a-lbl { font-family:'Outfit',sans-serif; font-size:10px; font-weight:800; letter-spacing:1px; text-transform:uppercase; margin-bottom:8px; }
.avg-g { display:grid; grid-template-columns:repeat(4,1fr); gap:6px; }
.ac { background:var(--bg3); border:1px solid var(--border); border-radius:6px; padding:10px 4px 8px; text-align:center; }
.ac .val { font-family:'Outfit',sans-serif; font-size:18px; font-weight:900; color:#fff; line-height:1; }
.ac .lbl { font-size:8px; color:var(--muted); margin-top:4px; text-transform:uppercase; letter-spacing:0.5px; line-height:1.2; font-weight: 600; }

/* Prediction Table - Mobile Scroll Wrapper */
.table-wrapper {
  width: 100%;
  overflow-x: auto;
  -webkit-overflow-scrolling: touch;
  margin: 0 -14px;
  padding: 0 14px 10px;
}
.pt { width:100%; min-width: 480px; border-collapse:collapse; table-layout:auto; }
.pt thead th {
  font-family:'Outfit',sans-serif; font-size:9px; font-weight:800;
  letter-spacing:1px; text-transform:uppercase; color:var(--muted);
  padding:0 8px 10px; text-align:center; border-bottom: 1px solid var(--border);
}
.pt thead th:first-child { text-align:left; padding-left: 0; }
.pt tbody td { padding:10px 8px; border-bottom:1px solid rgba(255,255,255,.04); vertical-align:middle; text-align:center; }
.pt tbody td.cmc { color:var(--hi); font-size:12px; font-weight:600; padding-left:0; text-align:left; }

.lv { font-family:'Outfit',sans-serif; font-size:15px; font-weight:800; color:var(--lo); }
.mv { font-family:'Outfit',sans-serif; font-size:17px; font-weight:900; color:var(--md); }
.hv { font-family:'Outfit',sans-serif; font-size:15px; font-weight:800; color:var(--hic); }

.split-stats {
  display: flex; flex-direction: column; gap: 4px; align-items: center;
  font-family: 'Inter', sans-serif; font-size: 9px; color: var(--muted);
  margin-top: 6px; font-weight: 500;
}
.split-stats span { display: inline-block; padding: 2px 4px; background: var(--bg4); border-radius: 4px; border: 1px solid var(--border); white-space: nowrap; }

/* Yellow Cards */
.yc-grid { display:flex; flex-direction:column; gap:8px; }
.yc-row {
  display:flex; align-items:flex-start; gap:10px;
  background:var(--bg3); border:1px solid var(--border); border-radius:8px;
  padding:10px 12px;
}
.yc-icon { font-size:18px; flex-shrink:0; margin-top:2px; }
.yc-info { flex:1; min-width:0; }
.yc-name { font-size:13px; font-weight:700; color:#fff; }
.yc-club { font-size:9px; font-family:'Outfit',sans-serif; letter-spacing:0.5px; text-transform:uppercase; margin-left:4px; font-weight: 800; }
.yc-reason { font-size:11px; color:var(--muted); margin-top:4px; line-height:1.4; }
.yc-risk {
  font-family:'Outfit',sans-serif; font-size:9px; font-weight:800;
  letter-spacing:1px; text-transform:uppercase; padding:3px 8px;
  border-radius:4px; flex-shrink:0; align-self:center;
}
.risk-h { background:rgba(245,89,41,.15); color:var(--hic); border:1px solid rgba(245,89,41,.3); }
.risk-m { background:rgba(247,201,72,.15); color:var(--md); border:1px solid rgba(247,201,72,.3); }

/* DIVIDER */
.s-div { text-align:center; padding:24px 0 12px; position:relative; }
.s-div::before { content:''; position:absolute; left:0; right:0; top:50%; height:1px; background:linear-gradient(90deg,transparent,rgba(246,142,0,.4),transparent); }
.s-div-in {
  display:inline-flex; align-items:center; gap:8px;
  background:var(--bg); padding:0 12px; position:relative;
  font-family:'Outfit',sans-serif; font-size:10px; font-weight:900;
  letter-spacing:2px; text-transform:uppercase; color:var(--uel-orange);
}

/* ══════ DESKTOP ENHANCEMENTS ══════ */
@media(min-width: 768px) {
  .site-header { padding: 32px 20px 24px; }
  .site-header h1 { font-size: 32px; }
  .match-hero { padding: 32px 20px; }
  .hero-inner { max-width: 720px; gap: 16px; }
  .badge-wrap { width: 84px; height: 84px; border-width: 2px; }
  .badge-wrap img { width: 60px; height: 60px; }
  .h-name { font-size: 16px; }
  .vs-txt { font-size: 28px; }
  .ko-chip { font-size: 11px; padding: 4px 12px; }

  .page { padding: 24px 20px 60px; }
  .dg { display: grid; grid-template-columns: 1fr 1fr; gap: 24px; align-items: start; }
  .fw { grid-column: 1 / -1; }
  
  .form-cols, .avg-pair { flex-direction: row; }
  .fcol, .a-grp { flex: 1; min-width: 0; }
  
  .sb-title { font-size: 13px; }
  .sc { padding: 18px; }
  .sc-label { font-size: 11px; }
  .sc-value { font-size: 42px; }
  
  .table-wrapper { margin: 0; padding: 0; overflow-x: visible; }
  .pt { min-width: 100%; }
  .pt thead th { font-size: 11px; padding-bottom: 12px; }
  .pt tbody td { padding: 14px 12px; }
  .cmc { font-size: 14px; }
  .split-stats { flex-direction: row; justify-content: center; gap: 8px; font-size: 11px; }
  .split-stats span { padding: 2px 6px; }
  
  .yc-name { font-size: 15px; }
  .yc-club { font-size: 11px; }
  .yc-reason { font-size: 13px; }
  .yc-risk { font-size: 11px; padding: 4px 12px; }
}

@media(min-width: 1024px) {
  .page { max-width: 1100px; }
  .ac .val { font-size: 24px; }
  .ac .lbl { font-size: 10px; }
}
</style>
</head>
<body>

<header class="site-header">
  <div class="uel-chip">UEFA Europa League</div>
  <h1>Team Bilbo Analytics</h1>
  <p class="sub">Quarter-Finals 2nd Leg · Form · Averages · H2H · Weighted Stats</p>
</header>

<div class="tie-status ts-1">
  <div class="ts-icon">🔥</div>
  <div class="ts-text">
    <strong>TIE STATUS — Aston Villa lead 3–1 on aggregate.</strong> First leg: Bologna 1–3 Aston Villa. Villa secured a vital away win in Italy, giving them a comfortable cushion. Bologna must win by 3 goals at Villa Park to advance in 90 mins, or win by 2 to force Extra Time. High stakes as Unai Emery targets another European semi-final.
    <span class="ts-agg" style="color:var(--avl-blu)">AGG: AVL 3–1 BOL</span>
  </div>
</div>

<div class="match-hero mh-1">
  <div class="hero-inner">
    <div class="h-team">
      <div class="badge-wrap">
        <img src="https://cdn.brandfetch.io/idFPmd025E/theme/dark/logo.svg?c=1bxid64Mup7aczewSAYMX&t=1668077974118" alt="Aston Villa">
      </div>
      <div class="h-name">Aston Villa</div>
      <div class="h-pos">Premier League · Home</div>
    </div>
    <div class="vs-col">
      <div class="vs-txt">VS</div>
      <div class="ko-chip">20:00</div>
      <div class="venue-txt">Villa Park, Birmingham</div>
    </div>
    <div class="h-team">
      <div class="badge-wrap">
        <img src="https://cdn.brandfetch.io/idv07tl3PU/theme/dark/logo.svg?c=1bxid64Mup7aczewSAYMX&t=1775434500476" alt="Bologna">
      </div>
      <div class="h-name">Bologna FC</div>
      <div class="h-pos">Serie A · Needs 2+ Goals</div>
    </div>
  </div>
</div>

<div class="page">
  <div class="dg">
    
    <div class="score-box fw">
      <div class="sb-title">Score Prediction — Aston Villa vs Bologna</div>
      <div class="scores-row">
        <div class="sc">
          <div class="sc-label">Half-Time</div>
          <div class="sc-value" style="color:var(--avl-blu)">1 – 0</div>
          <div class="sc-prob">Villa control early</div>
        </div>
        <div class="sc sc-best">
          <div class="sc-label">Full-Time Best Pick</div>
          <div class="sc-value" style="color:var(--avl-blu)">2 – 0</div>
          <div class="sc-prob">Villa win (Agg 5-1)</div>
        </div>
        <div class="sc">
          <div class="sc-label">Alternative</div>
          <div class="sc-value" style="color:var(--md)">1 – 1</div>
          <div class="sc-prob">Draw (Agg 4-2)</div>
        </div>
      </div>
      <div class="sb-notes">
        <strong>Rationale:</strong> Unai Emery is a master of two-legged European ties. Holding a 3-1 lead, Villa can sit slightly deeper, absorb Bologna's pressure, and strike on the counter using Watkins and Bailey. Bologna has struggled to score multiple goals away from home in Europe this season. We project a disciplined 2-0 home victory.
      </div>
    </div>

    <div class="card fw">
      <div class="card-hd"><div class="hd-dot" style="background:var(--md)"></div><div class="hd-title">Last 5 Matches (All Comps)</div></div>
      <div class="card-body">
        <div class="form-cols">
          <div class="fcol">
            <div class="team-lab lab-avl"><img class="tl-img" src="https://cdn.brandfetch.io/avfc.co.uk/icon" alt="" onerror="this.style.display='none'"> Aston Villa</div>
            <div class="match-list">
              <div class="mr"><div class="rd W"></div><div class="ms">3–1</div><div class="mo">Brentford</div><div class="mc">PL</div></div>
              <div class="mr"><div class="rd L"></div><div class="ms">1–2</div><div class="mo">Chelsea</div><div class="mc">PL</div></div>
              <div class="mr"><div class="rd W"></div><div class="ms">3–1</div><div class="mo">Bologna (Leg 1)</div><div class="mc">UEL</div></div>
              <div class="mr"><div class="rd D"></div><div class="ms">1–1</div><div class="mo">West Ham</div><div class="mc">PL</div></div>
              <div class="mr"><div class="rd W"></div><div class="ms">2–0</div><div class="mo">Ajax</div><div class="mc">UEL</div></div>
            </div>
          </div>
          <div class="fcol">
            <div class="team-lab lab-bol"><img class="tl-img" src="https://cdn.brandfetch.io/bolognafc.it/icon" alt="" onerror="this.style.display='none'"> Bologna</div>
            <div class="match-list">
              <div class="mr"><div class="rd L"></div><div class="ms">0–1</div><div class="mo">Juventus</div><div class="mc">Serie A</div></div>
              <div class="mr"><div class="rd D"></div><div class="ms">0–0</div><div class="mo">Torino</div><div class="mc">Serie A</div></div>
              <div class="mr"><div class="rd L"></div><div class="ms">1–3</div><div class="mo">Aston Villa (Leg 1)</div><div class="mc">UEL</div></div>
              <div class="mr"><div class="rd W"></div><div class="ms">3–0</div><div class="mo">Frosinone</div><div class="mc">Serie A</div></div>
              <div class="mr"><div class="rd W"></div><div class="ms">2–1</div><div class="mo">Feyenoord</div><div class="mc">UEL</div></div>
            </div>
          </div>
        </div>
      </div>
    </div>

    <div class="card">
      <div class="card-hd"><div class="hd-dot" style="background:#a78bfa"></div><div class="hd-title">Season Averages & H2H</div></div>
      <div class="card-body">
        <div class="avg-pair">
          <div class="a-grp">
            <div class="a-lbl" style="color:var(--avl-blu)">Aston Villa (Last 10)</div>
            <div class="avg-g">
              <div class="ac"><div class="val">14.2</div><div class="lbl">Shots</div></div>
              <div class="ac"><div class="val">5.8</div><div class="lbl">Corners</div></div>
              <div class="ac"><div class="val">10.1</div><div class="lbl">Fouls</div></div>
              <div class="ac"><div class="val">1.9</div><div class="lbl">Gls/Gm</div></div>
            </div>
          </div>
          <div class="a-grp">
            <div class="a-lbl" style="color:var(--bol-r)">Bologna (Last 10)</div>
            <div class="avg-g">
              <div class="ac"><div class="val">12.5</div><div class="lbl">Shots</div></div>
              <div class="ac"><div class="val">4.6</div><div class="lbl">Corners</div></div>
              <div class="ac"><div class="val">12.8</div><div class="lbl">Fouls</div></div>
              <div class="ac"><div class="val">1.2</div><div class="lbl">Gls/Gm</div></div>
            </div>
          </div>
        </div>
        <div style="margin-top:20px; border-top:1px solid var(--border); padding-top:16px;">
          <div class="a-lbl">Recent Head-to-Head</div>
          <div class="match-list" style="margin-top:8px;">
            <div class="mr" style="grid-template-columns:1fr auto 1fr;"><div class="mo">Bologna</div><div class="ms">1–3</div><div class="mc" style="text-align: left;">A. Villa</div><div style="grid-column:1/-1; text-align:center; font-size:10px; color:var(--muted)">UEL QF L1 · April 2026</div></div>
            <div class="mr" style="grid-template-columns:1fr auto 1fr;"><div class="mo">A. Villa</div><div class="ms">2–0</div><div class="mc" style="text-align: left;">Bologna</div><div style="grid-column:1/-1; text-align:center; font-size:10px; color:var(--muted)">UCL League Ph · Oct 2024</div></div>
            <div class="mr" style="grid-template-columns:1fr auto 1fr;"><div class="mo">Bologna</div><div class="ms">1–1</div><div class="mc" style="text-align: left;">A. Villa</div><div style="grid-column:1/-1; text-align:center; font-size:10px; color:var(--muted)">Pre-season · Aug 2021</div></div>
          </div>
        </div>
      </div>
    </div>

    <div class="card fw">
      <div class="card-hd"><div class="hd-dot" style="background:var(--lo)"></div><div class="hd-title">📊 Weighted Stat Predictions</div></div>
      <div class="card-body" style="padding-left: 0; padding-right: 0;">
        <div style="font-size:11px; color:var(--muted); margin-bottom:12px; padding: 0 14px; text-align: center;">
          <strong>Median:</strong> Match Total <em>(Home Split / Away Split)</em>
        </div>
        <div class="table-wrapper">
          <table class="pt">
            <thead>
              <tr>
                <th style="padding-left: 14px;">Metric</th>
                <th>Low Total</th>
                <th class="th-m">Median <span>(AVL / BOL)</span></th>
                <th>High Total</th>
                <th>Volatility</th>
              </tr>
            </thead>
            <tbody>
              <tr>
                <td class="cmc" style="padding-left: 14px;">Corners</td>
                <td><span class="lv">8</span></td>
                <td><span class="mv">10</span> <div class="split-stats"><span>AVL: 6</span> <span>BOL: 4</span></div></td>
                <td><span class="hv">13</span></td>
                <td style="color:var(--muted); font-size:10px;">Average</td>
              </tr>
              <tr>
                <td class="cmc" style="padding-left: 14px;">Total Shots</td>
                <td><span class="lv">20</span></td>
                <td><span class="mv">26</span> <div class="split-stats"><span>AVL: 14</span> <span>BOL: 12</span></div></td>
                <td><span class="hv">32</span></td>
                <td style="color:var(--hic); font-size:10px;">High</td>
              </tr>
              <tr>
                <td class="cmc" style="padding-left: 14px;">Shots on Target</td>
                <td><span class="lv">7</span></td>
                <td><span class="mv">9</span> <div class="split-stats"><span>AVL: 5</span> <span>BOL: 4</span></div></td>
                <td><span class="hv">13</span></td>
                <td style="color:var(--muted); font-size:10px;">Average</td>
              </tr>
              <tr>
                <td class="cmc" style="padding-left: 14px;">Fouls</td>
                <td><span class="lv">19</span></td>
                <td><span class="mv">24</span> <div class="split-stats"><span>AVL: 10</span> <span>BOL: 14</span></div></td>
                <td><span class="hv">30</span></td>
                <td style="color:var(--md); font-size:10px;">Moderate</td>
              </tr>
              <tr>
                <td class="cmc" style="padding-left: 14px;">Throw-ins</td>
                <td><span class="lv">32</span></td>
                <td><span class="mv">38</span> <div class="split-stats"><span>AVL: 18</span> <span>BOL: 20</span></div></td>
                <td><span class="hv">46</span></td>
                <td style="color:var(--muted); font-size:10px;">Average</td>
              </tr>
              <tr>
                <td class="cmc" style="padding-left: 14px;">Goal Kicks</td>
                <td><span class="lv">12</span></td>
                <td><span class="mv">16</span> <div class="split-stats"><span>AVL: 9</span> <span>BOL: 7</span></div></td>
                <td><span class="hv">21</span></td>
                <td style="color:var(--muted); font-size:10px;">Average</td>
              </tr>
              <tr>
                <td class="cmc" style="padding-left: 14px;">Tackles</td>
                <td><span class="lv">26</span></td>
                <td><span class="mv">32</span> <div class="split-stats"><span>AVL: 15</span> <span>BOL: 17</span></div></td>
                <td><span class="hv">38</span></td>
                <td style="color:var(--md); font-size:10px;">Moderate</td>
              </tr>
              <tr>
                <td class="cmc" style="padding-left: 14px;">Offsides</td>
                <td><span class="lv">2</span></td>
                <td><span class="mv">4</span> <div class="split-stats"><span>AVL: 2</span> <span>BOL: 2</span></div></td>
                <td><span class="hv">7</span></td>
                <td style="color:var(--lo); font-size:10px;">Low</td>
              </tr>
            </tbody>
          </table>
        </div>
      </div>
    </div>

    <div class="card fw">
      <div class="card-hd"><div class="hd-dot" style="background:var(--md)"></div><div class="hd-title">🟨 Yellow Card Risk Players</div></div>
      <div class="card-body">
        <div class="yc-grid">
          <div class="yc-row">
            <div class="yc-icon">🟨</div>
            <div class="yc-info">
              <div class="yc-name">Remo Freuler <span class="yc-club" style="color:var(--bol-r)">Bologna · CM</span></div>
              <div class="yc-reason">Tasked with breaking up Villa's transitions. Very prone to tactical fouls in high-stakes European away ties.</div>
            </div>
            <div class="yc-risk risk-h">HIGH</div>
          </div>
          <div class="yc-row">
            <div class="yc-icon">🟨</div>
            <div class="yc-info">
              <div class="yc-name">Douglas Luiz <span class="yc-club" style="color:var(--avl-blu)">Aston Villa · CM</span></div>
              <div class="yc-reason">Anchors the midfield. Will engage in physical duels to maintain Villa's control. Often booked for late challenges.</div>
            </div>
            <div class="yc-risk risk-h">HIGH</div>
          </div>
          <div class="yc-row">
            <div class="yc-icon">🟨</div>
            <div class="yc-info">
              <div class="yc-name">Stefan Posch <span class="yc-club" style="color:var(--bol-r)">Bologna · RB</span></div>
              <div class="yc-reason">Will face immense pressure from Villa's left flank (McGinn/Diaby). Defensive overload increases booking risk.</div>
            </div>
            <div class="yc-risk risk-m">MED</div>
          </div>
        </div>
      </div>
    </div>

  </div> <div class="s-div"><div class="s-div-in">★ Match 2 · UEL QF ★</div></div>

  <div class="tie-status ts-2">
    <div class="ts-icon">⚔️</div>
    <div class="ts-text">
      <strong>TIE STATUS — Aggregate tied 1–1.</strong> First leg: Porto 1–1 Nott'm Forest. Forest secured a fantastic draw at the Estádio do Dragão. The tie is perfectly poised. Porto has immense European pedigree, but the City Ground under the lights is a formidable fortress. Winner takes all.
      <span class="ts-agg" style="color:var(--nfo-r)">AGG: NFO 1–1 POR</span>
    </div>
  </div>

  <div class="match-hero mh-2">
    <div class="hero-inner">
      <div class="h-team">
        <div class="badge-wrap">
          <img src="https://cdn.brandfetch.io/idwmZKybXP/theme/dark/logo.svg?c=1bxid64Mup7aczewSAYMX&t=1773431229883" alt="Nott'm Forest">
        </div>
        <div class="h-name">Nott'm Forest</div>
        <div class="h-pos">Premier League · Home</div>
      </div>
      <div class="vs-col">
        <div class="vs-txt">VS</div>
        <div class="ko-chip">20:00</div>
        <div class="venue-txt">The City Ground, Nott'm</div>
      </div>
      <div class="h-team">
        <div class="badge-wrap">
          <img src="https://cdn.brandfetch.io/idu4toElqn/theme/light/logo.svg?c=1bxid64Mup7aczewSAYMX&t=1760228783193" alt="Porto">
        </div>
        <div class="h-name">FC Porto</div>
        <div class="h-pos">Primeira Liga · Agg Tied</div>
      </div>
    </div>
  </div>

  <div class="dg">
    
    <div class="score-box fw">
      <div class="sb-title">Score Prediction — Nott'm Forest vs FC Porto</div>
      <div class="scores-row">
        <div class="sc">
          <div class="sc-label">Half-Time</div>
          <div class="sc-value" style="color:var(--md)">0 – 0</div>
          <div class="sc-prob">Tense, physical start</div>
        </div>
        <div class="sc sc-best">
          <div class="sc-label">Full-Time Best Pick</div>
          <div class="sc-value" style="color:var(--nfo-r)">2 – 1</div>
          <div class="sc-prob">Forest win late/AET</div>
        </div>
        <div class="sc">
          <div class="sc-label">Porto Experience</div>
          <div class="sc-value" style="color:var(--fcp-b)">0 – 1</div>
          <div class="sc-prob">Porto steal it</div>
        </div>
      </div>
      <div class="sb-notes">
        <strong>Rationale:</strong> The City Ground atmosphere will be electric. Forest play a high-energy, direct style at home. Porto are seasoned European knockout specialists, expertly killing momentum and forcing fouls. This will be an ugly, tight game. We predict a 1-1 draw in 90 mins, with Forest edging it 2-1 in Extra Time driven by the home crowd.
      </div>
    </div>

    <div class="card fw">
      <div class="card-hd"><div class="hd-dot" style="background:var(--md)"></div><div class="hd-title">Last 5 Matches (All Comps)</div></div>
      <div class="card-body">
        <div class="form-cols">
          <div class="fcol">
            <div class="team-lab lab-nfo"><img class="tl-img" src="https://cdn.brandfetch.io/nottinghamforest.co.uk/icon" alt="" onerror="this.style.display='none'"> Nott'm Forest</div>
            <div class="match-list">
              <div class="mr"><div class="rd D"></div><div class="ms">1–1</div><div class="mo">Crystal Palace</div><div class="mc">PL</div></div>
              <div class="mr"><div class="rd W"></div><div class="ms">2–0</div><div class="mo">Everton</div><div class="mc">PL</div></div>
              <div class="mr"><div class="rd D"></div><div class="ms">1–1</div><div class="mo">Porto (Leg 1)</div><div class="mc">UEL</div></div>
              <div class="mr"><div class="rd L"></div><div class="ms">1–3</div><div class="mo">Arsenal</div><div class="mc">PL</div></div>
              <div class="mr"><div class="rd W"></div><div class="ms">2–1</div><div class="mo">Lille</div><div class="mc">UEL</div></div>
            </div>
          </div>
          <div class="fcol">
            <div class="team-lab lab-fcp"><img class="tl-img" src="https://cdn.brandfetch.io/fcporto.pt/icon" alt="" onerror="this.style.display='none'"> FC Porto</div>
            <div class="match-list">
              <div class="mr"><div class="rd W"></div><div class="ms">2–0</div><div class="mo">Boavista</div><div class="mc">Liga</div></div>
              <div class="mr"><div class="rd D"></div><div class="ms">1–1</div><div class="mo">Nott'm Forest (L1)</div><div class="mc">UEL</div></div>
              <div class="mr"><div class="rd W"></div><div class="ms">3–1</div><div class="mo">Braga</div><div class="mc">Liga</div></div>
              <div class="mr"><div class="rd L"></div><div class="ms">0–1</div><div class="mo">Benfica</div><div class="mc">Liga</div></div>
              <div class="mr"><div class="rd W"></div><div class="ms">2–0</div><div class="mo">Lazio</div><div class="mc">UEL</div></div>
            </div>
          </div>
        </div>
      </div>
    </div>

    <div class="card">
      <div class="card-hd"><div class="hd-dot" style="background:#a78bfa"></div><div class="hd-title">Season Averages & H2H</div></div>
      <div class="card-body">
        <div class="avg-pair">
          <div class="a-grp">
            <div class="a-lbl" style="color:var(--nfo-r)">Forest (Last 10)</div>
            <div class="avg-g">
              <div class="ac"><div class="val">11.8</div><div class="lbl">Shots</div></div>
              <div class="ac"><div class="val">4.5</div><div class="lbl">Corners</div></div>
              <div class="ac"><div class="val">11.2</div><div class="lbl">Fouls</div></div>
              <div class="ac"><div class="val">1.4</div><div class="lbl">Gls/Gm</div></div>
            </div>
          </div>
          <div class="a-grp">
            <div class="a-lbl" style="color:var(--fcp-b)">Porto (Last 10)</div>
            <div class="avg-g">
              <div class="ac"><div class="val">15.2</div><div class="lbl">Shots</div></div>
              <div class="ac"><div class="val">6.1</div><div class="lbl">Corners</div></div>
              <div class="ac"><div class="val">14.5</div><div class="lbl">Fouls</div></div>
              <div class="ac"><div class="val">1.8</div><div class="lbl">Gls/Gm</div></div>
            </div>
          </div>
        </div>
        <div style="margin-top:20px; border-top:1px solid var(--border); padding-top:16px;">
          <div class="a-lbl">Recent Head-to-Head</div>
          <div class="match-list" style="margin-top:8px;">
            <div class="mr" style="grid-template-columns:1fr auto 1fr;"><div class="mo">Porto</div><div class="ms">1–1</div><div class="mc" style="text-align: left;">N. Forest</div><div style="grid-column:1/-1; text-align:center; font-size:10px; color:var(--muted)">UEL QF L1 · April 2026</div></div>
            <div class="mr" style="grid-template-columns:1fr auto 1fr;"><div class="mo">N. Forest</div><div class="ms">0–1</div><div class="mc" style="text-align: left;">Porto</div><div style="grid-column:1/-1; text-align:center; font-size:10px; color:var(--muted)">Club Friendly · Jul 2024</div></div>
            <div class="mr" style="grid-template-columns:1fr auto 1fr;"><div class="mo">Porto</div><div class="ms">2–0</div><div class="mc" style="text-align: left;">N. Forest</div><div style="grid-column:1/-1; text-align:center; font-size:10px; color:var(--muted)">Club Friendly · Jul 2022</div></div>
          </div>
        </div>
      </div>
    </div>

    <div class="card fw">
      <div class="card-hd"><div class="hd-dot" style="background:var(--lo)"></div><div class="hd-title">📊 Weighted Stat Predictions</div></div>
      <div class="card-body" style="padding-left: 0; padding-right: 0;">
        <div style="font-size:11px; color:var(--muted); margin-bottom:12px; padding: 0 14px; text-align: center;">
          <strong>Median:</strong> Match Total <em>(Home Split / Away Split)</em>
        </div>
        <div class="table-wrapper">
          <table class="pt">
            <thead>
              <tr>
                <th style="padding-left: 14px;">Metric</th>
                <th>Low Total</th>
                <th class="th-m">Median <span>(NFO / POR)</span></th>
                <th>High Total</th>
                <th>Volatility</th>
              </tr>
            </thead>
            <tbody>
              <tr>
                <td class="cmc" style="padding-left: 14px;">Corners</td>
                <td><span class="lv">8</span></td>
                <td><span class="mv">11</span> <div class="split-stats"><span>NFO: 5</span> <span>POR: 6</span></div></td>
                <td><span class="hv">14</span></td>
                <td style="color:var(--muted); font-size:10px;">Average</td>
              </tr>
              <tr>
                <td class="cmc" style="padding-left: 14px;">Total Shots</td>
                <td><span class="lv">22</span></td>
                <td><span class="mv">28</span> <div class="split-stats"><span>NFO: 13</span> <span>POR: 15</span></div></td>
                <td><span class="hv">36</span></td>
                <td style="color:var(--muted); font-size:10px;">Average</td>
              </tr>
              <tr>
                <td class="cmc" style="padding-left: 14px;">Shots on Target</td>
                <td><span class="lv">7</span></td>
                <td><span class="mv">10</span> <div class="split-stats"><span>NFO: 5</span> <span>POR: 5</span></div></td>
                <td><span class="hv">15</span></td>
                <td style="color:var(--muted); font-size:10px;">Average</td>
              </tr>
              <tr>
                <td class="cmc" style="padding-left: 14px;">Fouls</td>
                <td><span class="lv">24</span></td>
                <td><span class="mv">28</span> <div class="split-stats"><span>NFO: 12</span> <span>POR: 16</span></div></td>
                <td><span class="hv">34</span></td>
                <td style="color:var(--hic); font-size:10px;">High (Porto dark arts)</td>
              </tr>
              <tr>
                <td class="cmc" style="padding-left: 14px;">Throw-ins</td>
                <td><span class="lv">36</span></td>
                <td><span class="mv">42</span> <div class="split-stats"><span>NFO: 21</span> <span>POR: 21</span></div></td>
                <td><span class="hv">50</span></td>
                <td style="color:var(--md); font-size:10px;">Moderate</td>
              </tr>
              <tr>
                <td class="cmc" style="padding-left: 14px;">Goal Kicks</td>
                <td><span class="lv">14</span></td>
                <td><span class="mv">18</span> <div class="split-stats"><span>NFO: 10</span> <span>POR: 8</span></div></td>
                <td><span class="hv">24</span></td>
                <td style="color:var(--muted); font-size:10px;">Average</td>
              </tr>
              <tr>
                <td class="cmc" style="padding-left: 14px;">Tackles</td>
                <td><span class="lv">30</span></td>
                <td><span class="mv">38</span> <div class="split-stats"><span>NFO: 20</span> <span>POR: 18</span></div></td>
                <td><span class="hv">46</span></td>
                <td style="color:var(--hic); font-size:10px;">High (Disruptive)</td>
              </tr>
              <tr>
                <td class="cmc" style="padding-left: 14px;">Offsides</td>
                <td><span class="lv">3</span></td>
                <td><span class="mv">5</span> <div class="split-stats"><span>NFO: 2</span> <span>POR: 3</span></div></td>
                <td><span class="hv">8</span></td>
                <td style="color:var(--lo); font-size:10px;">Low</td>
              </tr>
            </tbody>
          </table>
        </div>
      </div>
    </div>

    <div class="card fw">
      <div class="card-hd"><div class="hd-dot" style="background:var(--md)"></div><div class="hd-title">🟨 Yellow Card Risk Players</div></div>
      <div class="card-body">
        <div class="yc-grid">
          <div class="yc-row">
            <div class="yc-icon">🟨</div>
            <div class="yc-info">
              <div class="yc-name">Alan Varela <span class="yc-club" style="color:var(--fcp-b)">Porto · DM</span></div>
              <div class="yc-reason">The enforcer in Porto's midfield. Will be required to break up Forest's transitions. Very high card potential away from home.</div>
            </div>
            <div class="yc-risk risk-h">HIGH</div>
          </div>
          <div class="yc-row">
            <div class="yc-icon">🟨</div>
            <div class="yc-info">
              <div class="yc-name">Ryan Yates <span class="yc-club" style="color:var(--nfo-r)">Nott'm Forest · CM</span></div>
              <div class="yc-reason">Forest's aggressive ball-winner. Emotionally charged by the home crowd, he will not back out of any tackles against Porto's technical players.</div>
            </div>
            <div class="yc-risk risk-h">HIGH</div>
          </div>
          <div class="yc-row">
            <div class="yc-icon">🟨</div>
            <div class="yc-info">
              <div class="yc-name">Porto Central Defenders <span class="yc-club" style="color:var(--fcp-b)">Porto · CBs</span></div>
              <div class="yc-reason">Porto's defense employs gamesmanship and tactical fouling perfectly. Time-wasting or dissent bookings are extremely likely in the second half.</div>
            </div>
            <div class="yc-risk risk-m">MED</div>
          </div>
        </div>
      </div>
    </div>

  </div> </div> <footer style="text-align: center; padding: 24px 16px; font-family:'Inter',sans-serif; font-size: 11px; color: var(--muted); border-top: 1px solid var(--border);">
  <strong>Team Bilbo Statistical Analysis</strong><br>
  Predictions are statistical estimates based on historical profiles and UEFA Europa League knockout dynamics.<br>
  · April 2026 · Not Financial Advice ·
</footer>

<script>
(function(){
  'use strict';

  /* Card reveal */
  var cards=document.querySelectorAll('.card');
  if('IntersectionObserver' in window){
    var obs=new IntersectionObserver(function(e){
      e.forEach(function(entry){if(entry.isIntersecting){entry.target.classList.add('vis');obs.unobserve(entry.target);}});
    },{threshold:0.05});
    cards.forEach(function(c){obs.observe(c);});
  } else{cards.forEach(function(c){c.classList.add('vis');});}

  /* Count-up */
  var acObs=new IntersectionObserver(function(entries){
    entries.forEach(function(e){
      if(e.isIntersecting){
        var v=e.target.querySelector('.val');
        if(v && !v.dataset.done){
          v.dataset.done='1';
          var raw=v.textContent.trim();
          var num=parseFloat(raw.replace('%',''));
          if(!isNaN(num)){
            var cur=0,dur=850,step=num/(dur/16);
            var t=setInterval(function(){
              cur+=step;
              if(cur>=num){cur=num;clearInterval(t);}
              var d=(String(num).indexOf('.')!==-1)?cur.toFixed(1):Math.round(cur);
              v.textContent=d+(raw.indexOf('%')!==-1?'%':'');
            },16);
          }
        }
        acObs.unobserve(e.target);
      }
    });
  },{threshold:0.5});
  document.querySelectorAll('.ac').forEach(function(el){acObs.observe(el);});
})();
</script>
