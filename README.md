<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>UCL QF 2nd Legs · Arsenal vs Sporting · Bayern vs Real Madrid</title>
<link rel="preconnect" href="https://fonts.googleapis.com">
<link href="https://fonts.googleapis.com/css2?family=Montserrat:wght@400;500;600;700;800;900&family=Lato:wght@300;400;700&display=swap" rel="stylesheet">
<style>
/* ══════════════════════════════════
   ROOT TOKENS
══════════════════════════════════ */
:root {
  --bg:          #02030e;
  --bg2:         #060814;
  --bg3:         #0b0d1f;
  --bg4:         #10122a;
  --bg5:         #161932;
  --border:      rgba(255,255,255,.07);
  --bm:          rgba(255,255,255,.13);
  --text:        #c0cbdf;
  --muted:       #46506e;
  --hi:          #7f8dae;
  /* UCL */
  --ucl:         #001489;
  --ucl-l:       #4a6cf7;
  --ucl-gold:    #c9a830;
  --ucl-gs:      rgba(201,168,48,.16);
  /* Arsenal */
  --ars-r:       #ef0107;
  --ars-g:       #9b2335;
  --ars-l:       rgba(239,1,7,.18);
  /* Sporting */
  --scp-g:       #007a33;
  --scp-y:       #f5d03d;
  --scp-l:       rgba(0,122,51,.18);
  /* Bayern */
  --bay-r:       #dc052d;
  --bay-b:       #0066b2;
  --bay-l:       rgba(220,5,45,.18);
  /* Real Madrid */
  --rma-w:       #f0f0f0;
  --rma-g:       #c9a830;
  --rma-l:       rgba(201,168,48,.12);
  /* stats */
  --lo:          #0fd9a2;
  --md:          #f7c948;
  --hic:         #f55929;
}

*, *::before, *::after { margin:0; padding:0; box-sizing:border-box; }
html { scroll-behavior:smooth; }
body {
  font-family:'Lato', sans-serif;
  background:var(--bg);
  color:var(--text);
  font-size:14px;
  line-height:1.6;
  -webkit-font-smoothing:antialiased;
  overflow-x:hidden;
}

/* ══════ ANIMATIONS ══════ */
@keyframes fadeUp    { from{opacity:0;transform:translateY(22px)}   to{opacity:1;transform:translateY(0)} }
@keyframes popBadge  { from{transform:scale(.6)rotate(-8deg);opacity:0} to{transform:scale(1)rotate(0);opacity:1} }
@keyframes starRot   { from{transform:rotate(0)} to{transform:rotate(360deg)} }
@keyframes shimmer   { 0%{background-position:-200% center} 100%{background-position:200% center} }
@keyframes glow      { 0%,100%{opacity:.5} 50%{opacity:1} }
@keyframes barFill   { from{width:0 !important} }

/* ══════ STAR BG ══════ */
.star-bg {
  position:fixed; inset:0; pointer-events:none; z-index:0;
  background:
    radial-gradient(ellipse 70% 50% at 20% 15%, rgba(0,20,137,.07), transparent 65%),
    radial-gradient(ellipse 50% 40% at 80% 75%, rgba(201,168,48,.04), transparent 60%);
}

/* ══════ SITE HEADER ══════ */
.site-header {
  position:relative; z-index:2;
  background:linear-gradient(170deg, rgba(0,20,137,.15) 0%, var(--bg2) 50%, rgba(201,168,48,.06) 100%);
  border-bottom:1px solid rgba(0,20,137,.35);
  text-align:center;
  padding:22px 16px 18px;
  overflow:hidden;
}
.site-header::after {
  content:'★';
  font-size:110px; opacity:.025;
  position:absolute; left:50%; top:50%; transform:translate(-50%,-50%);
  animation:starRot 35s linear infinite; pointer-events:none;
}
.ucl-chip {
  display:inline-flex; align-items:center; gap:8px;
  font-family:'Montserrat',sans-serif; font-size:10px; font-weight:800;
  letter-spacing:2.5px; text-transform:uppercase;
  color:var(--ucl-gold); background:var(--ucl-gs);
  border:1px solid rgba(201,168,48,.35);
  padding:4px 14px; border-radius:20px; margin-bottom:11px;
}
.site-header h1 {
  font-family:'Montserrat',sans-serif;
  font-size:24px; font-weight:900; letter-spacing:1px;
  text-transform:uppercase; color:#fff; line-height:1.1;
}
.site-header .sub { font-size:12px; color:var(--muted); margin-top:5px; }
.match-nav {
  display:flex; justify-content:center; gap:8px; flex-wrap:wrap; margin-top:13px;
}
.mn-btn {
  font-family:'Montserrat',sans-serif; font-size:9.5px; font-weight:700;
  letter-spacing:1.2px; text-transform:uppercase;
  padding:5px 13px; border-radius:6px; border:1px solid;
  text-decoration:none; transition:all .2s;
}
.mn-ars { color:var(--ars-r); border-color:rgba(239,1,7,.3); background:rgba(239,1,7,.06); }
.mn-ars:hover { background:rgba(239,1,7,.14); }
.mn-bay { color:var(--bay-r); border-color:rgba(220,5,45,.3); background:rgba(220,5,45,.06); }
.mn-bay:hover { background:rgba(220,5,45,.14); }

/* ══════ TIE STATUS ══════ */
.tie-status {
  padding:12px 16px;
  display:flex; align-items:flex-start; gap:10px;
}
.ts-ars { background:linear-gradient(135deg,rgba(239,1,7,.1),rgba(239,1,7,.03)); border-bottom:1px solid rgba(239,1,7,.18); }
.ts-bay { background:linear-gradient(135deg,rgba(220,5,45,.1),rgba(220,5,45,.03)); border-bottom:1px solid rgba(220,5,45,.18); }
.ts-icon { font-size:20px; flex-shrink:0; margin-top:1px; animation:glow 2s ease-in-out infinite; }
.ts-text { font-size:12px; line-height:1.65; color:var(--hi); }
.ts-text strong { font-weight:700; }
.ts-agg {
  display:inline-block; font-family:'Montserrat',sans-serif;
  font-size:17px; font-weight:900; letter-spacing:1px;
}

/* ══════ MATCH HERO ══════ */
.match-hero {
  padding:24px 16px 20px;
  border-bottom:1px solid var(--bm);
  position:relative; overflow:hidden;
}
.mh-ars { background:linear-gradient(135deg, var(--ars-l) 0%, var(--bg2) 45%, var(--scp-l) 100%); }
.mh-bay { background:linear-gradient(135deg, var(--bay-l) 0%, var(--bg2) 45%, var(--rma-l) 100%); }
.hero-glow {
  position:absolute; inset:0;
  background:radial-gradient(ellipse 60% 70% at 50% 50%, rgba(0,20,137,.04), transparent 70%);
  pointer-events:none;
}
.hero-inner {
  max-width:540px; margin:0 auto;
  display:flex; align-items:center; justify-content:space-between; gap:12px;
}
.h-team { display:flex; flex-direction:column; align-items:center; gap:8px; flex:1; }
.badge-wrap {
  width:76px; height:76px; border-radius:50%;
  border:1.5px solid var(--bm); background:rgba(255,255,255,.04);
  display:flex; align-items:center; justify-content:center; overflow:hidden;
  filter:drop-shadow(0 4px 22px rgba(0,0,0,.75));
  animation:popBadge .5s cubic-bezier(.34,1.56,.64,1) both;
  transition:transform .3s cubic-bezier(.34,1.56,.64,1); flex-shrink:0; cursor:default;
}
.badge-wrap:hover { transform:scale(1.1) rotate(3deg); }
.badge-wrap img { width:54px; height:54px; object-fit:contain; }
.h-name {
  font-family:'Montserrat',sans-serif; font-size:13px; font-weight:800;
  text-transform:uppercase; text-align:center; color:#fff; line-height:1.2; letter-spacing:.5px;
}
.h-pos { font-size:9px; color:var(--muted); text-transform:uppercase; letter-spacing:.5px; text-align:center; }
.vs-col { display:flex; flex-direction:column; align-items:center; gap:5px; flex-shrink:0; }
.vs-txt { font-family:'Montserrat',sans-serif; font-size:22px; font-weight:900; color:rgba(255,255,255,.1); letter-spacing:3px; }
.ko-chip {
  font-family:'Montserrat',sans-serif; font-size:8.5px; font-weight:800; letter-spacing:1.5px;
  color:var(--ucl-gold); background:var(--ucl-gs); border:1px solid rgba(201,168,48,.3);
  padding:2px 8px; border-radius:4px;
}
.venue-txt { font-size:9px; color:var(--muted); text-align:center; line-height:1.5; }

/* ══════ SCORE BOX ══════ */
.score-box {
  background:linear-gradient(135deg,var(--bg3),var(--bg4));
  border:1px solid var(--bm); border-radius:10px;
  padding:17px 16px; margin-bottom:12px;
}
.sb-title {
  font-family:'Montserrat',sans-serif; font-size:10px; font-weight:800;
  letter-spacing:2.5px; text-transform:uppercase; color:var(--muted);
  text-align:center; margin-bottom:14px;
}
.scores-row { display:flex; gap:10px; justify-content:center; flex-wrap:wrap; }
.sc {
  background:var(--bg5); border:1px solid var(--border); border-radius:8px;
  padding:13px 17px; text-align:center; flex:1; min-width:108px; max-width:185px;
  transition:border-color .3s, transform .3s;
}
.sc:hover { transform:translateY(-2px); }
.sc-label { font-family:'Montserrat',sans-serif; font-size:8.5px; font-weight:700; letter-spacing:1.5px; text-transform:uppercase; color:var(--muted); margin-bottom:8px; }
.sc-value { font-family:'Montserrat',sans-serif; font-size:34px; font-weight:900; letter-spacing:4px; line-height:1; color:#fff; }
.sc-prob { font-size:9px; color:var(--muted); margin-top:5px; }
.sc-best { border-color:rgba(201,168,48,.4); background:linear-gradient(135deg,rgba(201,168,48,.08),var(--bg5)); }
.sc-best .sc-label { color:var(--ucl-gold); }
.sb-notes { font-size:12px; color:var(--hi); line-height:1.65; margin-top:12px; }
.sb-notes strong { color:var(--md); font-weight:700; }

/* ══════ PAGE ══════ */
.page { max-width:720px; margin:0 auto; padding:18px 14px 56px; position:relative; z-index:1; }

/* section divider */
.s-div {
  text-align:center; padding:24px 0 12px; position:relative;
}
.s-div::before {
  content:''; position:absolute; left:0; right:0; top:50%; height:1px;
  background:linear-gradient(90deg,transparent,rgba(0,20,137,.35),rgba(201,168,48,.35),rgba(0,20,137,.35),transparent);
}
.s-div-in {
  display:inline-flex; align-items:center; gap:9px;
  background:var(--bg); padding:0 14px; position:relative;
  font-family:'Montserrat',sans-serif; font-size:9.5px; font-weight:800;
  letter-spacing:2.5px; text-transform:uppercase; color:var(--ucl-l);
}

/* card */
.card {
  background:var(--bg2); border:1px solid var(--border);
  border-radius:10px; overflow:hidden; margin-bottom:12px;
  opacity:0; transform:translateY(14px);
  transition:opacity .5s ease, transform .5s ease, border-color .3s;
}
.card.vis { opacity:1; transform:translateY(0); }
.card:hover { border-color:var(--bm); }
.card-hd {
  padding:11px 16px 9px; border-bottom:1px solid var(--border);
  display:flex; align-items:center; gap:8px;
}
.hd-dot { width:5px; height:5px; border-radius:50%; flex-shrink:0; }
.hd-title {
  font-family:'Montserrat',sans-serif; font-size:9.5px; font-weight:800;
  letter-spacing:2px; text-transform:uppercase; color:var(--muted); flex:1;
}
.hd-tag { font-size:8.5px; font-weight:700; letter-spacing:.8px; text-transform:uppercase; padding:2px 7px; border-radius:3px; border:1px solid; }
.card-body { padding:14px 16px; }

/* callout */
.callout { background:rgba(255,255,255,.022); border:1px solid var(--bm); border-radius:8px; padding:12px 14px; font-size:12.5px; line-height:1.7; color:var(--hi); }
.callout strong { color:var(--md); font-weight:700; }

/* form cols */
.form-cols { display:flex; flex-direction:column; gap:12px; }
.fcol {}
.team-lab {
  display:inline-flex; align-items:center; gap:5px;
  font-size:9px; font-weight:700; letter-spacing:1px; text-transform:uppercase;
  padding:2px 8px 2px 4px; border-radius:4px; margin-bottom:7px; border:1px solid;
}
.lab-ars { background:rgba(239,1,7,.1); color:#ff7a7a; border-color:rgba(239,1,7,.28); }
.lab-scp { background:rgba(0,122,51,.1); color:#6dda8e; border-color:rgba(0,122,51,.28); }
.lab-bay { background:rgba(220,5,45,.1); color:#ff7a7a; border-color:rgba(220,5,45,.28); }
.lab-rma { background:rgba(201,168,48,.1); color:var(--ucl-gold); border-color:rgba(201,168,48,.28); }
.tl-img { width:13px; height:13px; object-fit:contain; }

.match-list { display:flex; flex-direction:column; gap:3px; }
.mr {
  display:grid; grid-template-columns:6px 44px 1fr auto;
  align-items:center; gap:8px;
  background:var(--bg3); border:1px solid var(--border);
  border-radius:6px; padding:6px 9px; transition:background .2s;
}
.mr:hover { background:var(--bg4); }
.rd { width:6px; height:6px; border-radius:50%; }
.rd.W { background:var(--lo); box-shadow:0 0 5px rgba(15,217,162,.4); }
.rd.D { background:var(--md); }
.rd.L { background:var(--hic); box-shadow:0 0 5px rgba(245,89,41,.4); }
.ms { font-family:'Montserrat',sans-serif; font-size:13px; font-weight:800; color:#fff; text-align:center; }
.mo { font-size:11.5px; color:var(--text); font-weight:500; overflow:hidden; text-overflow:ellipsis; white-space:nowrap; }
.mc { font-size:9px; color:var(--muted); text-align:right; white-space:nowrap; text-transform:uppercase; letter-spacing:.3px; }
.tag-ucl { font-size:8px; padding:1px 5px; border-radius:3px; background:var(--ucl-gs); color:var(--ucl-gold); border:1px solid rgba(201,168,48,.25); font-family:'Montserrat',sans-serif; font-weight:700; letter-spacing:.5px; }
.f-leg { display:flex; gap:11px; flex-wrap:wrap; margin-top:8px; }
.fl { display:flex; align-items:center; gap:4px; font-size:10px; color:var(--muted); }
.fl-dot { width:6px; height:6px; border-radius:50%; }

/* avg */
.avg-pair { display:flex; flex-direction:column; gap:12px; }
.a-grp {}
.a-lbl { font-family:'Montserrat',sans-serif; font-size:9.5px; font-weight:800; letter-spacing:1.5px; text-transform:uppercase; margin-bottom:7px; }
.avg-g { display:grid; grid-template-columns:repeat(4,1fr); gap:5px; }
.ac {
  background:var(--bg3); border:1px solid var(--border); border-radius:7px;
  padding:9px 5px 7px; text-align:center; transition:border-color .2s, transform .2s;
}
.ac:hover { border-color:var(--bm); transform:translateY(-1px); }
.ac .val { font-family:'Montserrat',sans-serif; font-size:19px; font-weight:900; color:#fff; line-height:1; }
.ac .lbl { font-size:8px; color:var(--muted); margin-top:3px; text-transform:uppercase; letter-spacing:.4px; line-height:1.3; }

/* h2h */
.h2h-bar {
  background:var(--bg3); border:1px solid var(--border); border-radius:7px;
  padding:11px 10px; display:flex; align-items:center; justify-content:space-between; gap:4px;
}
.hs { text-align:center; flex:1; }
.hn { font-family:'Montserrat',sans-serif; font-size:27px; font-weight:900; line-height:1; }
.hl { font-size:9px; color:var(--muted); text-transform:uppercase; letter-spacing:.6px; margin-top:2px; }
.hdv { width:1px; height:32px; background:var(--border); flex-shrink:0; }
.h2h-rows { display:flex; flex-direction:column; gap:3px; margin-top:10px; }
.h2h-r {
  display:grid; grid-template-columns:1fr auto 1fr; align-items:center; gap:8px;
  background:var(--bg4); border:1px solid var(--border); border-radius:6px;
  padding:6px 9px; transition:background .2s;
}
.h2h-r:hover { background:var(--bg5); }
.rh { font-size:11.5px; font-weight:700; color:var(--text); text-align:left; white-space:nowrap; overflow:hidden; text-overflow:ellipsis; }
.rs { font-family:'Montserrat',sans-serif; font-size:14px; font-weight:900; color:#fff; text-align:center; white-space:nowrap; }
.ra { font-size:11.5px; font-weight:700; color:var(--text); text-align:right; white-space:nowrap; overflow:hidden; text-overflow:ellipsis; }
.rsub { font-size:8.5px; color:var(--muted); letter-spacing:.3px; grid-column:1/-1; text-align:center; margin-top:-2px; text-transform:uppercase; }

/* PRED TABLE */
.pred-leg { display:flex; gap:13px; flex-wrap:wrap; margin-bottom:12px; }
.pli { display:flex; align-items:center; gap:5px; font-size:10.5px; color:var(--muted); }
.pld { width:7px; height:7px; border-radius:50%; }
.pw { overflow-x:auto; -webkit-overflow-scrolling:touch; }
.pt { width:100%; border-collapse:collapse; table-layout:fixed; min-width:285px; }
.pt col.cm{width:29%} .pt col.cl{width:16%} .pt col.cn{width:16%} .pt col.ch{width:16%} .pt col.cb{width:23%}
.pt thead th {
  font-family:'Montserrat',sans-serif; font-size:8.5px; font-weight:800;
  letter-spacing:1.5px; text-transform:uppercase; color:var(--muted);
  padding:0 0 9px; text-align:left; white-space:nowrap;
}
.pt thead th:not(:first-child) { text-align:center; }
.pt thead th.th-m { color:var(--md); }
.pt tbody td { padding:7px 3px; border-bottom:1px solid rgba(255,255,255,.03); vertical-align:middle; overflow:hidden; }
.pt tbody tr:last-child td { border-bottom:none; }
.pt tbody tr:hover td { background:rgba(255,255,255,.02); }
.pt tbody td.cmc { color:var(--hi); font-size:12px; padding-left:0; font-weight:500; }
.pt tbody td:not(.cmc) { text-align:center; }
.lv { font-family:'Montserrat',sans-serif; font-size:17px; font-weight:900; color:var(--lo); line-height:1; }
.mv { font-family:'Montserrat',sans-serif; font-size:17px; font-weight:900; color:var(--md); line-height:1; }
.hv { font-family:'Montserrat',sans-serif; font-size:17px; font-weight:900; color:var(--hic); line-height:1; }
.bw { width:85%; max-width:88px; height:5px; background:rgba(255,255,255,.06); border-radius:3px; overflow:hidden; margin:0 auto; display:block; }
.bf { display:block; height:100%; border-radius:3px; width:0; transition:width 1.3s cubic-bezier(.25,.46,.45,.94); }
.bf-ars { background:linear-gradient(90deg,var(--ars-r),#ff7a7a); }
.bf-bay { background:linear-gradient(90deg,var(--bay-r),#0066b2); }

/* YELLOW CARDS */
.yc-grid { display:flex; flex-direction:column; gap:7px; }
.yc-row {
  display:flex; align-items:flex-start; gap:9px;
  background:var(--bg3); border:1px solid var(--border); border-radius:8px;
  padding:9px 11px; transition:border-color .25s, transform .25s;
}
.yc-row:hover { border-color:rgba(255,224,51,.2); transform:translateX(3px); }
.yc-icon { font-size:16px; flex-shrink:0; margin-top:1px; }
.yc-info { flex:1; min-width:0; }
.yc-name { font-size:12.5px; font-weight:700; color:#fff; }
.yc-club { font-size:9px; font-family:'Montserrat',sans-serif; letter-spacing:.7px; text-transform:uppercase; margin-left:5px; }
.yc-reason { font-size:11px; color:var(--muted); margin-top:2px; line-height:1.45; }
.yc-risk {
  font-family:'Montserrat',sans-serif; font-size:8.5px; font-weight:800;
  letter-spacing:1px; text-transform:uppercase; padding:2px 8px;
  border-radius:4px; flex-shrink:0; align-self:center;
}
.risk-h { background:rgba(245,89,41,.14); color:var(--hic); border:1px solid rgba(245,89,41,.28); }
.risk-m { background:rgba(247,201,72,.1); color:var(--md); border:1px solid rgba(247,201,72,.25); }

/* NOTES */
.note { margin-bottom:9px; font-size:12.5px; line-height:1.65; color:var(--hi); }
.note:last-child { margin-bottom:0; }
.note strong { color:var(--md); font-weight:700; }

/* FOOTER */
footer { text-align: center;
            padding: 18px 14px;
            font-size: 11.5px;
            color: var(--muted);
            border-top: 1px solid var(--border); position:relative; z-index:1; }

/* ════ RESPONSIVE ════ */
@media(min-width:640px){
  body{font-size:15px;}
  .page{max-width:940px; padding:22px 24px 62px;}
  .site-header{padding:26px 24px 22px;} .site-header h1{font-size:30px;}
  .match-hero{padding:28px 24px 22px;} .hero-inner{max-width:620px;}
  .badge-wrap{width:84px;height:84px;} .badge-wrap img{width:60px;height:60px;}
  .h-name{font-size:14px;}
  .form-cols{flex-direction:row;gap:16px;} .fcol{flex:1;min-width:0;}
  .avg-pair{flex-direction:row;gap:16px;} .a-grp{flex:1;}
  .ac .val{font-size:21px;} .hn{font-size:30px;} .lv,.mv,.hv{font-size:20px;}
  .bw{max-width:110px;} .card-hd{padding:12px 20px 10px;} .card-body{padding:16px 20px;}
  .sc-value{font-size:40px;}
}
@media(min-width:1040px){
  .page{max-width:1380px; padding:28px 40px 68px;}
  .site-header{padding:28px 40px 24px;} .site-header h1{font-size:36px;}
  .match-hero{padding:28px 40px 22px;} .hero-inner{max-width:680px;}
  .badge-wrap{width:92px;height:92px;} .badge-wrap img{width:66px;height:66px;}
  .dg{display:grid;grid-template-columns:1fr 1fr;gap:20px;align-items:start;}
  .dg .fw{grid-column:1/-1;}
  .card-hd{padding:13px 22px 11px;} .card-body{padding:17px 22px;}
  .ac .val{font-size:22px;} .lv,.mv,.hv{font-size:21px;} .hn{font-size:32px;}
  .bw{max-width:96px;}
}
@media(min-width:1360px){
  .page{max-width:1540px;padding:32px 60px 76px;}
  .site-header{padding:30px 60px 24px;} .match-hero{padding:30px 60px 22px;} .dg{gap:26px;}
}
</style>
</head>
<body>
<div class="star-bg"></div>

<!-- ═══ HEADER ═══ -->
<header class="site-header">
  <div class="ucl-chip">★ UEFA Champions League ★<br>· Quarter-Final Second Legs ·</div>
  <h1>TEAM BILBO Stats Predictor</h1>
  <p class="sub">Arsenal vs Sporting CP &nbsp;·&nbsp; Bayern Munich vs Real Madrid &nbsp;·&nbsp; Form · Averages · H2H · Weighted Predictions · Score Forecasts</p>
  <nav class="match-nav">
    <a href="#ars" class="mn-btn mn-ars">🔴 Arsenal vs Sporting CP · Emirates · 20:00</a>
    <a href="#bay" class="mn-btn mn-bay">🔴 Bayern Munich vs Real Madrid · Allianz Arena · 20:00</a>
  </nav>
</header>

<!-- ══════════════════════════════
     MATCH 1 — ARSENAL vs SPORTING
══════════════════════════════════ -->

<div class="tie-status ts-ars" id="ars">
  <div class="ts-icon">🔴</div>
  <div class="ts-text">
    <strong>TIE STATUS — Arsenal lead 1–0 on aggregate.</strong> First leg: Sporting 0–1 Arsenal (Havertz 90+1'). Arsenal had 1 goal disallowed (VAR). Raya made 5 saves. First-leg stats: Sporting 11 shots / 5 SOT · Arsenal 8 shots / 4 SOT · 7 corners total (3 SCP, 4 ARS). Maxi Araújo committed 7 fouls. Arsenal need a draw or any win. Sporting must win by 2+ goals in 90 minutes or score once to force extra time. <span class="ts-agg" style="color:#ff7a7a">AGG: ARS 1–0</span>
  </div>
</div>

<div class="match-hero mh-ars">
  <div class="hero-glow"></div>
  <div class="hero-inner">
    <div class="h-team">
      <div class="badge-wrap">
        <img src="https://upload.wikimedia.org/wikipedia/en/thumb/5/53/Arsenal_FC.svg/120px-Arsenal_FC.svg.png" alt="Arsenal" style="background-color: #15151b;">
      </div>
      <div class="h-name">Arsenal FC</div>
      <div class="h-pos">🔴 PL Leaders · 70 pts · 1–0 up</div>
    </div>
    <div class="vs-col">
      <div class="vs-txt">VS</div>
      <div class="ko-chip">20:00</div>
      <div class="venue-txt">Emirates Stadium · London<br>Ref: François Letexier (FRA)</div>
    </div>
    <div class="h-team">
      <div class="badge-wrap" style="animation-delay:.14s">
        <img src="https://cdn.brandfetch.io/idNWw1XaNT/theme/dark/logo.svg?c=1bxid64Mup7aczewSAYMX&t=1775243816231" alt="Sporting CP" style="background-color: #15151b;">
      </div>
      <div class="h-name">Sporting CP</div>
      <div class="h-pos">🟢 Primeira Liga · 1–0 down · Need 2 goals</div>
    </div>
  </div>
</div>

<div class="page">
<div class="dg">

  <!-- SCORE PRED -->
  <div class="score-box fw">
    <div class="sb-title">📊 Score Prediction — Arsenal vs Sporting CP</div>
    <div class="scores-row">
      <div class="sc">
        <div class="sc-label">Half-Time</div>
        <div class="sc-value" style="color:#ff7a7a">1 – 0</div>
        <div class="sc-prob">Arsenal · ~42% probability</div>
      </div>
      <div class="sc sc-best">
        <div class="sc-label">Full-Time Best Pick</div>
        <div class="sc-value" style="color:#ff7a7a">2 – 0</div>
        <div class="sc-prob">Arsenal advance 3–0 on agg · ~30%</div>
      </div>
      <div class="sc" style="border-color:rgba(0,122,51,.4);">
        <div class="sc-label">Upset Watch</div>
        <div class="sc-value" style="color:#6dda8e">2 – 1</div>
        <div class="sc-prob">Arsenal progress 2–1 agg · ~22%</div>
      </div>
    </div>
    <div class="sb-notes">
      <strong>Why Arsenal 2–0:</strong> Arsenal are unbeaten in 11 UCL games this season and have won 19 of 20 two-legged European ties when winning the first leg away. At the Emirates they've kept 16 clean sheets in their last 22 European home games. Gyökeres scored 97 goals in 102 Sporting appearances — his return to the Emirates could be pivotal, but Arsenal's structure is built to control Sporting's counter-attack. Arsenal have scored after the break in 10 of their last 11 UCL games. Morten Hjulmand returns from suspension for Sporting — a crucial difference. Arsenal lost to Bournemouth last Saturday, adding emotional pressure to perform. <strong>A comfortable 2-0 is the weighted outcome</strong> — Arsenal control, clean sheet, two-goal advance. Letexier has issued only 18 yellows in 7 UCL games — a relatively lenient referee who lets the game breathe.
    </div>
  </div>

  <!-- CONTEXT -->
  <div class="card fw">
    <div class="card-hd">
      <div class="hd-dot" style="background:var(--md)"></div>
      <div class="hd-title">Match Context & Team News</div>
      <div class="hd-tag" style="color:var(--ucl-gold);border-color:rgba(201,168,48,.28);background:var(--ucl-gs)">UCL QF 2nd Leg · Havertz 90+1' Leg 1</div>
    </div>
    <div class="card-body">
      <div class="callout">
        Arsenal's title hopes took a blow with Saturday's 2-1 home loss to Bournemouth — their 3rd defeat in 4 games. However, at the Emirates in Europe they are a different team entirely — 11 UCL wins from 11 this season, <strong>16 clean sheets in their last 22 home European games</strong>. Progression to consecutive UCL semis for the first time ever is at stake. Sporting's firepower without Gyökeres (now at Arsenal) has been filled by <strong>Luís Suárez (37 goals this season, 5 in UCL)</strong>. Key Arsenal doubts: Saka, Timber, Odegaard, Rice, Calafiori — all fitness checks. <strong>Hjulmand returns from suspension</strong> — massive for Sporting (he was absent in Leg 1). Sporting without: Ioannidis (ligament), Luis Guilherme (ankle), Fresneda (physical). First leg: Arsenal had a Zubimendi goal disallowed for offside. Sporting haven't won away in UCL knockout stage since 1970 (Sept).
      </div>
    </div>
  </div>

  <!-- FORM -->
  <div class="card fw">
    <div class="card-hd">
      <div class="hd-dot" style="background:var(--ars-r)"></div>
      <div class="hd-title">Last 5 Matches — All Competitions</div>
    </div>
    <div class="card-body">
      <div class="form-cols">
        <div class="fcol">
          <div class="team-lab lab-ars">
            <img class="tl-img" src="https://upload.wikimedia.org/wikipedia/en/thumb/5/53/Arsenal_FC.svg/120px-Arsenal_FC.svg.png" alt="">Arsenal style="background-color: #15151b;"
          </div>
          <div class="match-list">
            <div class="mr"><div class="rd L"></div><div class="ms">1–2</div><div class="mo">Bournemouth</div><div class="mc">PL · Home <span class="tag-ucl">Sat</span></div></div>
            <div class="mr"><div class="rd W"></div><div class="ms">1–0</div><div class="mo">Sporting (Leg 1)</div><div class="mc">UCL QF <span class="tag-ucl">Havertz 90+1'</span></div></div>
            <div class="mr"><div class="rd L"></div><div class="ms">1–2</div><div class="mo">Southampton</div><div class="mc">FAC · Away</div></div>
            <div class="mr"><div class="rd L"></div><div class="ms">0–2</div><div class="mo">Man City</div><div class="mc">EFL Cup Final</div></div>
            <div class="mr"><div class="rd W"></div><div class="ms">2–0</div><div class="mo">Everton</div><div class="mc">PL · Home</div></div>
          </div>
        </div>
        <div class="fcol">
          <div class="team-lab lab-scp">
            <img class="tl-img" src="https://upload.wikimedia.org/wikipedia/en/thumb/5/5f/Sporting_CP_logo.svg/120px-Sporting_CP_logo.svg.png" alt="" style="background-color: #15151b;">Sporting CP
          </div>
          <div class="match-list">
            <div class="mr"><div class="rd W"></div><div class="ms">1–0</div><div class="mo">Estrela Amadora</div><div class="mc">Liga · Away</div></div>
            <div class="mr"><div class="rd L"></div><div class="ms">0–1</div><div class="mo">Arsenal (Leg 1)</div><div class="mc">UCL QF <span class="tag-ucl">Hjulmand absent</span></div></div>
            <div class="mr"><div class="rd W"></div><div class="ms">5–3</div><div class="mo">Bodø/Glimt (agg)</div><div class="mc">UCL R16 <span class="tag-ucl">came back 3-0</span></div></div>
            <div class="mr"><div class="rd W"></div><div class="ms">W</div><div class="mo">Liga (×2)</div><div class="mc">Primeira Liga</div></div>
            <div class="mr"><div class="rd W"></div><div class="ms">2–1</div><div class="mo">PSG (UCL)</div><div class="mc">UCL League Phase</div></div>
          </div>
        </div>
      </div>
      <div class="f-leg"><div class="fl"><div class="fl-dot" style="background:var(--lo)"></div>Win</div><div class="fl"><div class="fl-dot" style="background:var(--md)"></div>Draw</div><div class="fl"><div class="fl-dot" style="background:var(--hic)"></div>Loss</div></div>
    </div>
  </div>

  <!-- SEASON AVERAGES -->
  <div class="card fw">
    <div class="card-hd">
      <div class="hd-dot" style="background:#a78bfa"></div>
      <div class="hd-title">Season Averages — UCL &amp; All Comps</div>
    </div>
    <div class="card-body">
      <div class="avg-pair">
        <div class="a-grp">
          <div class="a-lbl" style="color:#ff7a7a">Arsenal — UCL leaders (5 conceded in 11 gms)</div>
          <div class="avg-g">
            <div class="ac"><div class="val">14.7</div><div class="lbl">Shots</div></div>
            <div class="ac"><div class="val">5.0</div><div class="lbl">SOT</div></div>
            <div class="ac"><div class="val">6.2</div><div class="lbl">Corners</div></div>
            <div class="ac"><div class="val">10.5</div><div class="lbl">Fouls</div></div>
          </div>
          <p style="font-size:10px;color:var(--muted);margin-top:6px;">UCL: 27 goals scored, 5 conceded in 11 games. Home UCL: unbeaten, 16 clean sheets in last 22. Gyökeres: 6 UCL goals, back at his old club.</p>
        </div>
        <div class="a-grp">
          <div class="a-lbl" style="color:#6dda8e">Sporting CP</div>
          <div class="avg-g">
            <div class="ac"><div class="val">13.4</div><div class="lbl">Shots</div></div>
            <div class="ac"><div class="val">4.6</div><div class="lbl">SOT</div></div>
            <div class="ac"><div class="val">5.8</div><div class="lbl">Corners</div></div>
            <div class="ac"><div class="val">11.2</div><div class="lbl">Fouls</div></div>
          </div>
          <p style="font-size:10px;color:var(--muted);margin-top:6px;">Suárez: 37 goals all comps, 5 UCL. Trincão: 4 UCL goals. Won 9/10 two-leg ties vs English clubs. Only 2 wins in last 14 vs English opposition in European competition.</p>
        </div>
      </div>
    </div>
  </div>

  <!-- H2H -->
  <div class="card fw">
    <div class="card-hd">
      <div class="hd-dot" style="background:var(--hic)"></div>
      <div class="hd-title">H2H — Last 5 Meetings (All Comps)</div>
    </div>
    <div class="card-body">
      <div class="h2h-bar">
        <div class="hs"><div class="hn" style="color:#ff7a7a">3</div><div class="hl">Arsenal</div></div>
        <div class="hdv"></div>
        <div class="hs"><div class="hn" style="color:var(--md)">2</div><div class="hl">Draws</div></div>
        <div class="hdv"></div>
        <div class="hs"><div class="hn" style="color:#6dda8e">0</div><div class="hl">Sporting</div></div>
        <div class="hdv"></div>
        <div class="hs"><div class="hn">1.4</div><div class="hl">Avg Goals</div></div>
      </div>
      <p style="font-size:10.5px;color:var(--muted);margin-top:8px;margin-bottom:8px;">Arsenal have never been beaten by Sporting in European competition (W4 D4 all-time). In two previous meetings at the Emirates, both ended in draws (0-0 and 1-1 in UEL 2022-23). Sporting knocked Arsenal out on penalties in 2023 after two goalless/draw legs.</p>
      <div class="h2h-rows">
        <div class="h2h-r"><div class="rh">Sporting</div><div class="rs">0–1</div><div class="ra">Arsenal</div><div class="rsub">UCL QF Leg 1 · Lisbon · Apr 7, 2026</div></div>
        <div class="h2h-r"><div class="rh">Arsenal</div><div class="rs">1–1</div><div class="ra">Sporting</div><div class="rsub">UEL R16 Leg 2 · Emirates · Mar 2023 (SCP won pens)</div></div>
        <div class="h2h-r"><div class="rh">Sporting</div><div class="rs">1–1</div><div class="ra">Arsenal</div><div class="rsub">UEL R16 Leg 1 · Lisbon · Mar 2023 (SCP won pens)</div></div>
        <div class="h2h-r"><div class="rh">Arsenal</div><div class="rs">0–0</div><div class="ra">Sporting</div><div class="rsub">UCL League Phase · Emirates · Oct 2024</div></div>
        <div class="h2h-r"><div class="rh">Arsenal</div><div class="rs">5–1</div><div class="ra">Sporting</div><div class="rsub">UCL League Phase · Lisbon · Jan 2025</div></div>
      </div>
    </div>
  </div>

  <!-- STAT PREDICTIONS -->
  <div class="card fw" id="pred-ars">
    <div class="card-hd">
      <div class="hd-dot" style="background:var(--lo)"></div>
      <div class="hd-title">📊 Weighted Stat Predictions — Arsenal vs Sporting CP</div>
    </div>
    <div class="card-body">
      <div class="pred-leg">
        <div class="pli"><div class="pld" style="background:var(--lo)"></div><span style="color:var(--lo);font-weight:700">Low</span></div>
        <div class="pli"><div class="pld" style="background:var(--md)"></div><span style="color:var(--md);font-weight:700">Median</span></div>
        <div class="pli"><div class="pld" style="background:var(--hic)"></div><span style="color:var(--hic);font-weight:700">High</span></div>
      </div>
      <div class="pw"><table class="pt">
        <colgroup><col class="cm"><col class="cl"><col class="cn"><col class="ch"><col class="cb"></colgroup>
        <thead><tr><th>Metric</th><th style="color:var(--lo)">Low</th><th class="th-m">Median</th><th style="color:var(--hic)">High</th><th style="text-align:center;color:var(--muted)">Intensity</th></tr></thead>
        <tbody>
          <tr><td class="cmc">Corners</td><td><span class="lv">7</span></td><td><span class="mv">10</span></td><td><span class="hv">15</span></td><td><div class="bw"><div class="bf bf-ars" data-pct="66"></div></div></td></tr>
          <tr><td class="cmc">Total Shots</td><td><span class="lv">18</span></td><td><span class="mv">25</span></td><td><span class="hv">35</span></td><td><div class="bw"><div class="bf bf-ars" data-pct="72"></div></div></td></tr>
          <tr><td class="cmc">Shots on Target</td><td><span class="lv">6</span></td><td><span class="mv">9</span></td><td><span class="hv">14</span></td><td><div class="bw"><div class="bf bf-ars" data-pct="62"></div></div></td></tr>
          <tr><td class="cmc">Fouls</td><td><span class="lv">16</span></td><td><span class="mv">22</span></td><td><span class="hv">32</span></td><td><div class="bw"><div class="bf bf-ars" data-pct="60"></div></div></td></tr>
          <tr><td class="cmc">Throw-ins</td><td><span class="lv">34</span></td><td><span class="mv">46</span></td><td><span class="hv">60</span></td><td><div class="bw"><div class="bf bf-ars" data-pct="68"></div></div></td></tr>
          <tr><td class="cmc">Goal Kicks</td><td><span class="lv">14</span></td><td><span class="mv">20</span></td><td><span class="hv">28</span></td><td><div class="bw"><div class="bf bf-ars" data-pct="58"></div></div></td></tr>
          <tr><td class="cmc">Tackles</td><td><span class="lv">24</span></td><td><span class="mv">34</span></td><td><span class="hv">46</span></td><td><div class="bw"><div class="bf bf-ars" data-pct="74"></div></div></td></tr>
          <tr><td class="cmc">Offsides</td><td><span class="lv">3</span></td><td><span class="mv">6</span></td><td><span class="hv">11</span></td><td><div class="bw"><div class="bf bf-ars" data-pct="52"></div></div></td></tr>
        </tbody>
      </table></div>
    </div>
  </div>

  <!-- YELLOW CARDS -->
  <div class="card fw">
    <div class="card-hd">
      <div class="hd-dot" style="background:#ffe033"></div>
      <div class="hd-title">🟨 Yellow Card Risk Players</div>
      <div class="hd-tag" style="color:var(--md);border-color:rgba(247,201,72,.28);background:rgba(247,201,72,.07)">Letexier · lenient · 18 yellows in 7 UCL games · Semi-final ban risk</div>
    </div>
    <div class="card-body"><div class="yc-grid">
      <div class="yc-row"><div class="yc-icon">🟨</div><div class="yc-info">
        <div class="yc-name">Maxi Araújo <span class="yc-club" style="color:#6dda8e">Sporting · LB</span></div>
        <div class="yc-reason">Committed 7 fouls in the first leg — the most by any player in either UCL QF first leg. Will again be tasked with stopping Arsenal's right-side threats. Against an Emirates crowd expecting an Arsenal performance, Araújo will struggle to contain Madueke and the wide attacks without fouling. He's already on thin ice with referees after Leg 1.</div>
      </div><div class="yc-risk risk-h">HIGH</div></div>

      <div class="yc-row"><div class="yc-icon">🟨</div><div class="yc-info">
        <div class="yc-name">Morten Hjulmand <span class="yc-club" style="color:#6dda8e">Sporting · DM</span></div>
        <div class="yc-reason">Returns from suspension with the knowledge that Sporting must win by 2+ goals. Hjulmand's aggressive ball-winning will be needed immediately — but against Arsenal's UCL-dominant midfield he'll be pushed into desperate challenges. One poor timing against Rice or Nørgaard in front of Letexier could mean a second-leg booking that affects Sporting's semi-final (if they progress).</div>
      </div><div class="yc-risk risk-h">HIGH</div></div>

      <div class="yc-row"><div class="yc-icon">🟨</div><div class="yc-info">
        <div class="yc-name">Declan Rice <span class="yc-club" style="color:#ff7a7a">Arsenal · MF</span></div>
        <div class="yc-reason">Rice is expected back from his knock. He will be the engine of Arsenal's control but in a game where Arsenal are protecting a lead and Sporting are pushing desperately, Rice will commit holding fouls to break up transitions. Against Hjulmand's physicality, their midfield battle is one of the most combustible on the pitch.</div>
      </div><div class="yc-risk risk-m">MED</div></div>

      <div class="yc-row"><div class="yc-icon">🟨</div><div class="yc-info">
        <div class="yc-name">Ousmane Diomandé <span class="yc-club" style="color:#6dda8e">Sporting · CB</span></div>
        <div class="yc-reason">The dominant CB split Arsenal's defence for Araújo's great first-leg chance and Raya's save. Will face Gyökeres for 90 minutes — a bruising personal battle. If Arsenal break quickly in the second half and Diomandé lunges to stop a counter, a yellow is very likely. Physical defender playing aggressive high line.</div>
      </div><div class="yc-risk risk-m">MED</div></div>
    </div></div>
  </div>

  <!-- NOTES -->
  <div class="card fw">
    <div class="card-hd"><div class="hd-dot" style="background:#60a5fa"></div><div class="hd-title">Analytical Notes — Arsenal vs Sporting</div></div>
    <div class="card-body">
      <div class="note"><strong>Corners (7–10–15):</strong> Arsenal average 6.2 corners/game; Sporting 5.8 away. Combined ~12 baseline but this is a second leg where Sporting need to attack — yet Arsenal are also one of the best attacking corner teams in Europe. Leg 1 had 7 corners total. The Emirates generates more corners than most grounds when Arsenal are in control. High end of 15 if Sporting push heavily in the second half and Arsenal exploit their defensive vulnerability through set pieces.</div>
      <div class="note"><strong>Tackles (24–34–46):</strong> Sporting need to win — Hjulmand returns and will drive their pressing game. Arsenal's midfield (Rice, Nørgaard/Zubimendi) will win the ball back aggressively to preserve the aggregate. Combined baseline ~22/game, but the high stakes and Sporting's physical approach (7 fouls from Araújo alone in Leg 1) inflates this. Referee Letexier has been lenient — both sides might push the physical limits.</div>
      <div class="note"><strong>Fouls (16–22–32):</strong> Letexier has issued only 18 yellows in 7 UCL games — the 2nd most lenient UCL referee this season. He encourages physical play without constant interruptions. Sporting will need to foul to stop Arsenal on the break; Arsenal will foul tactically. First leg had 7 total fouls. Emirates games tend to have lower foul counts than away legs. Median of 22 reflects Sporting needing to press and foul but Letexier allowing the game to flow.</div>
      <div class="note"><strong>Offsides (3–6–11):</strong> Gyökeres will make multiple runs beyond Sporting's backline. Arsenal play a high line defensively, creating offside traps for Suárez and Trincão. Sporting will also try to spring counters behind Arsenal's defence. Arsenal's UCL average offside count is elevated when playing at home against pressing teams. Leg 1 had several offside moments (Zubimendi's disallowed goal). Median of 6 is well-grounded.</div>
    </div>
  </div>

</div><!-- /dg -->
<div class="s-div"><div class="s-div-in">★ Match 2 · UCL QF ★</div></div>

<!-- ════════════════════════════════
     MATCH 2 — BAYERN vs REAL MADRID
════════════════════════════════ -->
</div><!-- /page -->

<div class="tie-status ts-bay" id="bay">
  <div class="ts-icon">🔥</div>
  <div class="ts-text">
    <strong>TIE STATUS — Bayern lead 2–1 on aggregate.</strong> First leg: Real Madrid 1–2 Bayern (Díaz 41', Kane 46', Mbappé 74'). Bayern led 2–0 by half-time. Both teams had 20 shots each. 11 corners for Bayern (wasted all). Tchouaméni suspended (3rd yellow). Courtois and Rodrygo injured. Mbappé facial injury concern. Bayern's first win at Bernabéu in 14 years. <span class="ts-agg" style="color:#ff7a7a">AGG: BAY 2–1</span>
  </div>
</div>

<div class="match-hero mh-bay">
  <div class="hero-glow"></div>
  <div class="hero-inner">
    <div class="h-team">
      <div class="badge-wrap">
        <img src="https://upload.wikimedia.org/wikipedia/commons/thumb/1/1b/FC_Bayern_M%C3%BCnchen_logo_%282017%29.svg/120px-FC_Bayern_M%C3%BCnchen_logo_%282017%29.svg.png" alt="Bayern Munich" style="background-color: #15151b;">
      </div>
      <div class="h-name">Bayern Munich</div>
      <div class="h-pos">🔴 Bundesliga leaders · 2–1 up · Allianz home</div>
    </div>
    <div class="vs-col">
      <div class="vs-txt">VS</div>
      <div class="ko-chip">20:00</div>
      <div class="venue-txt">Allianz Arena · Munich, Germany<br>Ref: Slavko Vinčić (SVN)</div>
    </div>
    <div class="h-team">
      <div class="badge-wrap" style="animation-delay:.14s">
        <img src="https://upload.wikimedia.org/wikipedia/en/thumb/5/56/Real_Madrid_CF.svg/120px-Real_Madrid_CF.svg.png" alt="Real Madrid" style="background-color: #15151b;">
      </div>
      <div class="h-name">Real Madrid</div>
      <div class="h-pos">⚪ 15× European Champions · 1–2 down · Need 1 goal (no reply)</div>
    </div>
  </div>
</div>

<div class="page">
<div class="dg">

  <!-- SCORE PRED -->
  <div class="score-box fw">
    <div class="sb-title">📊 Score Prediction — Bayern Munich vs Real Madrid</div>
    <div class="scores-row">
      <div class="sc">
        <div class="sc-label">Half-Time</div>
        <div class="sc-value" style="color:#ff7a7a">1 – 0</div>
        <div class="sc-prob">Bayern · ~38% probability</div>
      </div>
      <div class="sc sc-best">
        <div class="sc-label">Full-Time Best Pick</div>
        <div class="sc-value" style="color:#ff7a7a">2 – 1</div>
        <div class="sc-prob">Bayern advance 4–2 on agg · ~27%</div>
      </div>
      <div class="sc" style="border-color:rgba(201,168,48,.4);">
        <div class="sc-label">Madrid Magic</div>
        <div class="sc-value" style="color:var(--ucl-gold)">1 – 2</div>
        <div class="sc-prob">Real Madrid AET/Pens · ~18%</div>
      </div>
    </div>
    <div class="sb-notes">
      <strong>Why Bayern 2–1 / advance:</strong> Bayern have won all 5 UCL home games this season, scoring 3+ goals in 4 of them. They lead Germany's scoring record with 105 Bundesliga goals. Came from 3-3 draw vs Freiburg in the Bundesliga last weekend. Real need a goal without Bayern reply — but at the Allianz Arena, in front of 75,000 partisan fans, Bayern are overwhelming favourites. Opta gives Bayern 56.9%. However, <strong>this is Real Madrid</strong>. They have 14 UCL titles and Mbappé, who is close to Ronaldo's single-season UCL goals record (17) — and scored in Leg 1. Both teams had 20 shots each in Madrid: this should be another high-octane, high-shot encounter. Both teams scored in all 7 of their last European meetings. <strong>Vinčić is strict — expect 5+ yellows.</strong>
    </div>
  </div>

  <!-- CONTEXT -->
  <div class="card fw">
    <div class="card-hd">
      <div class="hd-dot" style="background:var(--md)"></div>
      <div class="hd-title">Match Context &amp; Team News</div>
      <div class="hd-tag" style="color:var(--ucl-gold);border-color:rgba(201,168,48,.28);background:var(--ucl-gs)">UCL QF 2nd Leg · Kane Returns · Mbappé Doubt</div>
    </div>
    <div class="card-body">
      <div class="callout">
        Bayern are on a <strong>14-game unbeaten run</strong>, 12 of which were wins. They smashed St. Pauli 5-0 last weekend (breaking the all-time Bundesliga season goals record). This is Bayern's first UCL semi-final appearance since 2023-24. Real Madrid are without <strong>Tchouaméni (suspended)</strong>, <strong>Courtois</strong> and <strong>Rodrygo</strong> (both injured). Mbappé has a facial injury from training — his fitness is the biggest single question mark for the tie. Interim manager Álvaro Arbeloa took over from Xabi Alonso mid-season after poor results. Real have only advanced in the UCL semi-finals 33 times — the record — and will not lie down. The first leg's <strong>20 shots each</strong> shows how open this tie is. Neuer made 9 saves in Leg 1 — Madrid created numerous chances. Vinicius Jr made 17 runs in behind Bayern in the first leg — the most by any player vs Bayern this UCL season.
      </div>
    </div>
  </div>

  <!-- FORM -->
  <div class="card fw">
    <div class="card-hd">
      <div class="hd-dot" style="background:var(--bay-r)"></div>
      <div class="hd-title">Last 5 Matches — All Competitions</div>
    </div>
    <div class="card-body">
      <div class="form-cols">
        <div class="fcol">
          <div class="team-lab lab-bay">
            <img class="tl-img" src="https://upload.wikimedia.org/wikipedia/en/thumb/1/1f/FC_Bayern_M%C3%BCnchen_logo_%282002%E2%80%932017%29.svg/120px-FC_Bayern_M%C3%BCnchen_logo_%282002%E2%80%932017%29.svg.png" alt="" style="background-color: #15151b;">Bayern Munich
          </div>
          <div class="match-list">
            <div class="mr"><div class="rd W"></div><div class="ms">5–0</div><div class="mo">St. Pauli</div><div class="mc">Bundesliga <span class="tag-ucl">record 105 goals</span></div></div>
            <div class="mr"><div class="rd W"></div><div class="ms">2–1</div><div class="mo">Real Madrid (Leg 1)</div><div class="mc">UCL QF <span class="tag-ucl">1st away win Bern 14yr</span></div></div>
            <div class="mr"><div class="rd W"></div><div class="ms">3–2</div><div class="mo">Freiburg</div><div class="mc">Bundesliga <span class="tag-ucl">comeback 2–0 down</span></div></div>
            <div class="mr"><div class="rd W"></div><div class="ms">5–2</div><div class="mo">Tottenham (agg)</div><div class="mc">UCL R16</div></div>
            <div class="mr"><div class="rd W"></div><div class="ms">4–1</div><div class="mo">Bundesliga</div><div class="mc">Bundesliga</div></div>
          </div>
        </div>
        <div class="fcol">
          <div class="team-lab lab-rma">
            <img class="tl-img" src="https://upload.wikimedia.org/wikipedia/en/thumb/5/56/Real_Madrid_CF.svg/120px-Real_Madrid_CF.svg.png" alt="" style="background-color: #15151b;">Real Madrid
          </div>
          <div class="match-list">
            <div class="mr"><div class="rd L"></div><div class="ms">1–2</div><div class="mo">Bayern (Leg 1)</div><div class="mc">UCL QF <span class="tag-ucl">Mbappé 74'</span></div></div>
            <div class="mr"><div class="rd L"></div><div class="ms">1–2</div><div class="mo">Mallorca</div><div class="mc">La Liga · Away</div></div>
            <div class="mr"><div class="rd W"></div><div class="ms">5–1</div><div class="mo">Man City (agg)</div><div class="mc">UCL R16 <span class="tag-ucl">UCL DNA</span></div></div>
            <div class="mr"><div class="rd D"></div><div class="ms">1–1</div><div class="mo">La Liga</div><div class="mc">La Liga</div></div>
            <div class="mr"><div class="rd L"></div><div class="ms">1–2</div><div class="mo">La Liga</div><div class="mc">La Liga</div></div>
          </div>
        </div>
      </div>
      <div class="f-leg"><div class="fl"><div class="fl-dot" style="background:var(--lo)"></div>Win</div><div class="fl"><div class="fl-dot" style="background:var(--md)"></div>Draw</div><div class="fl"><div class="fl-dot" style="background:var(--hic)"></div>Loss</div></div>
    </div>
  </div>

  <!-- SEASON AVGS -->
  <div class="card fw">
    <div class="card-hd">
      <div class="hd-dot" style="background:#a78bfa"></div>
      <div class="hd-title">Season Averages — UCL &amp; All Comps</div>
    </div>
    <div class="card-body">
      <div class="avg-pair">
        <div class="a-grp">
          <div class="a-lbl" style="color:#ff7a7a">Bayern Munich — 105 Bundesliga goals (record)</div>
          <div class="avg-g">
            <div class="ac"><div class="val">19.2</div><div class="lbl">Shots</div></div>
            <div class="ac"><div class="val">7.1</div><div class="lbl">SOT</div></div>
            <div class="ac"><div class="val">5.8</div><div class="lbl">UCL Home Corners</div></div>
            <div class="ac"><div class="val">11.3</div><div class="lbl">Fouls</div></div>
          </div>
          <p style="font-size:10px;color:var(--muted);margin-top:6px;">Kane: 49 goals in all comps this season. Scored in last 4 UCL games vs Real Madrid. UCL: 34 goals in 11 games. Won all 5 UCL home games (3+ goals in 4). Unbeaten last 14 all comps.</p>
        </div>
        <div class="a-grp">
          <div class="a-lbl" style="color:var(--ucl-gold)">Real Madrid — 15× UCL Champions</div>
          <div class="avg-g">
            <div class="ac"><div class="val">16.8</div><div class="lbl">Shots</div></div>
            <div class="ac"><div class="val">5.4</div><div class="lbl">SOT</div></div>
            <div class="ac"><div class="val">5.1</div><div class="lbl">Corners</div></div>
            <div class="ac"><div class="val">12.1</div><div class="lbl">Fouls</div></div>
          </div>
          <p style="font-size:10px;color:var(--muted);margin-top:6px;">Mbappé: 14 UCL goals. 3 away wins in last 4 at Allianz Arena. Vinicius: 150 runs in behind in UCL (most of any player). BTTS in last 7 H2H UCL meetings.</p>
        </div>
      </div>
    </div>
  </div>

  <!-- H2H -->
  <div class="card fw">
    <div class="card-hd">
      <div class="hd-dot" style="background:var(--hic)"></div>
      <div class="hd-title">H2H — Last 5 Meetings (UCL)</div>
    </div>
    <div class="card-body">
      <div class="h2h-bar">
        <div class="hs"><div class="hn" style="color:#ff7a7a">2</div><div class="hl">Bayern</div></div>
        <div class="hdv"></div>
        <div class="hs"><div class="hn" style="color:var(--md)">1</div><div class="hl">Draws</div></div>
        <div class="hdv"></div>
        <div class="hs"><div class="hn" style="color:var(--ucl-gold)">2</div><div class="hl">Real Madrid</div></div>
        <div class="hdv"></div>
        <div class="hs"><div class="hn">2.8</div><div class="hl">Avg Goals</div></div>
      </div>
      <p style="font-size:10.5px;color:var(--muted);margin-top:8px;margin-bottom:8px;">The most-played fixture in UCL/European Cup history — 29 meetings total (Real lead all-time 13-12). BTTS in all 7 recent UCL encounters. Bayern had previously gone 10 games without a UCL win vs Real (D2 L7). Leg 1 had 20 shots each — the most open QF first leg this season.</p>
      <div class="h2h-rows">
        <div class="h2h-r"><div class="rh">Real Madrid</div><div class="rs">1–2</div><div class="ra">Bayern</div><div class="rsub">UCL QF Leg 1 · Bernabéu · Apr 7, 2026</div></div>
        <div class="h2h-r"><div class="rh">Bayern</div><div class="rs">2–1</div><div class="ra">Real Madrid</div><div class="rsub">UCL SF Leg 2 · Allianz · Apr 2024 (Madrid progressed 4-3 agg)</div></div>
        <div class="h2h-r"><div class="rh">Real Madrid</div><div class="rs">2–1</div><div class="ra">Bayern</div><div class="rsub">UCL SF Leg 1 · Bernabéu · May 2024 (Joselu 88', 90')</div></div>
        <div class="h2h-r"><div class="rh">Bayern</div><div class="rs">3–0</div><div class="ra">Real Madrid</div><div class="rsub">UCL QF Leg 2 · Allianz Arena · Apr 2018</div></div>
        <div class="h2h-r"><div class="rh">Real Madrid</div><div class="rs">2–1</div><div class="ra">Bayern</div><div class="rsub">UCL QF Leg 1 · Bernabéu · Apr 2018 (Madrid KO on 3-3 agg)</div></div>
      </div>
    </div>
  </div>

  <!-- STAT PREDICTIONS BAYERN -->
  <div class="card fw" id="pred-bay">
    <div class="card-hd">
      <div class="hd-dot" style="background:var(--lo)"></div>
      <div class="hd-title">📊 Weighted Stat Predictions — Bayern Munich vs Real Madrid</div>
    </div>
    <div class="card-body">
      <div class="pred-leg">
        <div class="pli"><div class="pld" style="background:var(--lo)"></div><span style="color:var(--lo);font-weight:700">Low</span></div>
        <div class="pli"><div class="pld" style="background:var(--md)"></div><span style="color:var(--md);font-weight:700">Median</span></div>
        <div class="pli"><div class="pld" style="background:var(--hic)"></div><span style="color:var(--hic);font-weight:700">High</span></div>
      </div>
      <div class="pw"><table class="pt">
        <colgroup><col class="cm"><col class="cl"><col class="cn"><col class="ch"><col class="cb"></colgroup>
        <thead><tr><th>Metric</th><th style="color:var(--lo)">Low</th><th class="th-m">Median</th><th style="color:var(--hic)">High</th><th style="text-align:center;color:var(--muted)">Intensity</th></tr></thead>
        <tbody>
          <tr><td class="cmc">Corners</td><td><span class="lv">8</span></td><td><span class="mv">12</span></td><td><span class="hv">18</span></td><td><div class="bw"><div class="bf bf-bay" data-pct="74"></div></div></td></tr>
          <tr><td class="cmc">Total Shots</td><td><span class="lv">24</span></td><td><span class="mv">34</span></td><td><span class="hv">48</span></td><td><div class="bw"><div class="bf bf-bay" data-pct="90"></div></div></td></tr>
          <tr><td class="cmc">Shots on Target</td><td><span class="lv">9</span></td><td><span class="mv">14</span></td><td><span class="hv">22</span></td><td><div class="bw"><div class="bf bf-bay" data-pct="84"></div></div></td></tr>
          <tr><td class="cmc">Fouls</td><td><span class="lv">20</span></td><td><span class="mv">28</span></td><td><span class="hv">40</span></td><td><div class="bw"><div class="bf bf-bay" data-pct="80"></div></div></td></tr>
          <tr><td class="cmc">Throw-ins</td><td><span class="lv">36</span></td><td><span class="mv">52</span></td><td><span class="hv">68</span></td><td><div class="bw"><div class="bf bf-bay" data-pct="84"></div></div></td></tr>
          <tr><td class="cmc">Goal Kicks</td><td><span class="lv">16</span></td><td><span class="mv">24</span></td><td><span class="hv">36</span></td><td><div class="bw"><div class="bf bf-bay" data-pct="76"></div></div></td></tr>
          <tr><td class="cmc">Tackles</td><td><span class="lv">28</span></td><td><span class="mv">40</span></td><td><span class="hv">56</span></td><td><div class="bw"><div class="bf bf-bay" data-pct="88"></div></div></td></tr>
          <tr><td class="cmc">Offsides</td><td><span class="lv">4</span></td><td><span class="mv">8</span></td><td><span class="hv">14</span></td><td><div class="bw"><div class="bf bf-bay" data-pct="64"></div></div></td></tr>
        </tbody>
      </table></div>
    </div>
  </div>

  <!-- YELLOW CARDS BAYERN -->
  <div class="card fw">
    <div class="card-hd">
      <div class="hd-dot" style="background:#ffe033"></div>
      <div class="hd-title">🟨 Yellow Card Risk Players — Bayern vs Real Madrid</div>
      <div class="hd-tag" style="color:var(--md);border-color:rgba(247,201,72,.28);background:rgba(247,201,72,.07)">Vinčić strict · 5 yellows in Leg 1 · Expect 5–7 cards</div>
    </div>
    <div class="card-body"><div class="yc-grid">
      <div class="yc-row"><div class="yc-icon">🟨</div><div class="yc-info">
        <div class="yc-name">Federico Valverde <span class="yc-club" style="color:var(--ucl-gold)">Real Madrid · MF</span></div>
        <div class="yc-reason">The Uruguayan will be Real's engine in a match where they must attack relentlessly. Without Tchouaméni, Valverde carries double the defensive load while also needing to support the attack. He was booked in the second half of Leg 1 after growing frustrated. Against Bayern's structured midfield pressing, a desperate foul or impulsive reaction is almost guaranteed.</div>
      </div><div class="yc-risk risk-h">HIGH</div></div>

      <div class="yc-row"><div class="yc-icon">🟨</div><div class="yc-info">
        <div class="yc-name">Joshua Kimmich <span class="yc-club" style="color:#ff7a7a">Bayern · DM</span></div>
        <div class="yc-reason">Kimmich leads Bayern's pressing from the base and makes more defensive line-breaking passes than any player in the UCL this season. Against Mbappé and Vinicius in a high-intensity Allianz atmosphere, he will be forced to commit physical fouls to break up Madrid's counter-attacks. Multiple bookings already this UCL campaign.</div>
      </div><div class="yc-risk risk-h">HIGH</div></div>

      <div class="yc-row"><div class="yc-icon">🟨</div><div class="yc-info">
        <div class="yc-name">Vinicius Júnior <span class="yc-club" style="color:var(--ucl-gold)">Real Madrid · FW</span></div>
        <div class="yc-reason">Led the Allianz on a constant one-on-one battle in Leg 1. With Vinčić strict on simulation and diving, Vinicius' demonstrative reactions when fouled risk a yellow for simulation. He was booked for complaining in Leg 1. In a match where he needs to be the main creative force, his emotional responses to constant Allianz press could generate a second booking.</div>
      </div><div class="yc-risk risk-h">HIGH</div></div>

      <div class="yc-row"><div class="yc-icon">🟨</div><div class="yc-info">
        <div class="yc-name">Aleksandar Pavlović <span class="yc-club" style="color:#ff7a7a">Bayern · MF</span></div>
        <div class="yc-reason">The 21-year-old played a stellar role in Leg 1. Will again be tasked with shutting down Madrid's attacking transitions. His combative style is already on Vinčić's radar after his physical performance in Madrid. A second-leg intensity spike + first 20 minutes' aggression = prime booking territory.</div>
      </div><div class="yc-risk risk-m">MED</div></div>

      <div class="yc-row"><div class="yc-icon">🟨</div><div class="yc-info">
        <div class="yc-name">Kylian Mbappé <span class="yc-club" style="color:var(--ucl-gold)">Real Madrid · FW</span></div>
        <div class="yc-reason">If Mbappé plays through his facial injury, he may be more reactive to physical challenges, drawing fouls aggressively. He's pursuing Ronaldo's single-season UCL goals record (17). The emotional intensity of potentially being eliminated at this stage could see him lash out when tackled by Bayern's physical defence. Vinčić monitors his reactions closely.</div>
      </div><div class="yc-risk risk-m">MED</div></div>
    </div></div>
  </div>

  <!-- NOTES BAYERN -->
  <div class="card fw">
    <div class="card-hd"><div class="hd-dot" style="background:#60a5fa"></div><div class="hd-title">Analytical Notes — Bayern Munich vs Real Madrid</div></div>
    <div class="card-body">
      <div class="note"><strong>Total Shots (24–34–48) — Highest of All Four QF Second Legs:</strong> The first leg had 20 shots each — 40 total. In the second leg, with Real needing to attack (they need a goal without reply), the shot count rises even further. Bayern average 19.2 shots/game at home in the UCL. Real average 16.8 on the road. Combined baseline ~36. Bayern attacked relentlessly in Leg 1 but wasted 11 corners. The Allianz atmosphere supercharges Bayern's attacking output. High end of 48 if Real go behind and open up completely.</div>
      <div class="note"><strong>Tackles (28–40–56) — Joint-Highest with Atletico-Barcelona:</strong> Both teams press aggressively and transition at pace. In Leg 1, Real's right-back Carreras was exposed 12+ times by Olise — tackles to stop those runs are inevitable. Real without Tchouaméni means their midfield defensive cover is reduced, leading to more physical challenges from Valverde and Camavinga. Bayern's pressing game generates ball-winning duels from every position. Over 40 tackles has been recorded in 3 of the last 5 UCL meetings between these clubs.</div>
      <div class="note"><strong>Corners (8–12–18):</strong> Bayern had 11 corners in Leg 1 — and converted none. That efficiency deficit means the coaching staff will prioritise corner delivery in the second leg. At home in the UCL, Bayern average 5.8 corners/game. Real's attacking shape when chasing a goal means they press high and concede corners frequently. The high end of 18 is achievable if Bayern dominate territory in the second half.</div>
      <div class="note"><strong>Fouls (20–28–40):</strong> Vinčić averaged 4.5+ cards per game throughout the first leg and will be firm in Munich. Both teams' aggressive defensive shapes create constant foul situations. Leg 1 had 5 yellow cards total. The second leg at a partisan Allianz Arena, with Real Madrid needing to take risks, creates even more foul opportunities. First leg: Vinicius alone drew 8 fouls. Median of 28 reflects this elevated baseline.</div>
      <div class="note"><strong>Offsides (4–8–14) — Highest of All Four Second Legs:</strong> This game features the two highest "runs in behind" operators in the entire UCL tournament. Vinicius leads the UCL with 150 runs in behind (76 in knockout stages alone). Kane and Olise make constant runs into Trent's space. Both teams play extremely high defensive lines, creating constant offside traps. First leg had 6 offsides. Second leg urgency increases the frequency of line-breaking runs and traps.</div>
    </div>
  </div>

</div><!-- /dg -->
</div><!-- /page -->

<footer>
        <strong>Team Bilbo Statistical Analysis</strong><br>Predictions are statistical estimates based on historical profiles and Champions League knockout dynamics. <strong>Not financial advice.</strong><br> · April 2026 ·
    </footer>

<script>
(function(){
  'use strict';

  /* Card reveal */
  var cards=document.querySelectorAll('.card');
  if('IntersectionObserver' in window){
    var obs=new IntersectionObserver(function(e){
      e.forEach(function(entry){if(entry.isIntersecting){entry.target.classList.add('vis');obs.unobserve(entry.target);}});
    },{threshold:0.06});
    cards.forEach(function(c){obs.observe(c);});
  } else{cards.forEach(function(c){c.classList.add('vis');});}

  /* Bar animations */
  ['pred-ars','pred-bay'].forEach(function(id){
    var el=document.getElementById(id);if(!el)return;
    var fired=false;
    var bObs=new IntersectionObserver(function(entries){
      entries.forEach(function(e){
        if(e.isIntersecting && !fired){
          fired=true;
          setTimeout(function(){
            el.querySelectorAll('.bf[data-pct]').forEach(function(b){
              b.style.width=b.getAttribute('data-pct')+'%';
            });
          },200);
          bObs.unobserve(e.target);
        }
      });
    },{threshold:0.2});
    bObs.observe(el);
  });

  /* Count-up */
  var acObs=new IntersectionObserver(function(entries){
    entries.forEach(function(e){
      if(e.isIntersecting){
        var v=e.target.querySelector('.val');
        if(v && !v.dataset.done){
          v.dataset.done='1';
          var raw=v.textContent.trim();
          var isPct=raw.indexOf('%')!==-1;
          var num=parseFloat(raw.replace('%',''));
          if(!isNaN(num)){
            var cur=0,dur=850,step=num/(dur/16);
            var t=setInterval(function(){
              cur+=step;
              if(cur>=num){cur=num;clearInterval(t);}
              var d=(String(num).indexOf('.')!==-1)?cur.toFixed(1):Math.round(cur);
              v.textContent=d+(isPct?'%':'');
            },16);
          }
        }
        acObs.unobserve(e.target);
      }
    });
  },{threshold:0.7});
  document.querySelectorAll('.ac').forEach(function(el){acObs.observe(el);});
})();
</script>
