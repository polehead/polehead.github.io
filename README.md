<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Chelsea vs Man City | PL Stats Predictor — Title Race Special</title>
<link rel="preconnect" href="https://fonts.googleapis.com">
<link href="https://fonts.googleapis.com/css2?family=Space+Grotesk:wght@400;500;600;700&family=Inter:wght@300;400;500;600&display=swap" rel="stylesheet">
<style>
/* ══════════════════════════════════════════
   DESIGN TOKENS
══════════════════════════════════════════ */
:root {
  --bg:        #04060f;
  --bg-2:      #080c19;
  --bg-3:      #0e1324;
  --bg-4:      #141a2e;
  --bg-5:      #1a2138;
  --border:    rgba(255,255,255,0.07);
  --border-m:  rgba(255,255,255,0.13);
  --text:      #c2ccdf;
  --muted:     #4c5574;
  --hi:        #8895b8;
  /* Chelsea */
  --che-b:     #034694;
  --che-g:     #ffffff;
  --che-l:     rgba(3,70,148,0.22);
  /* Man City */
  --mci-b:     #6cabdd;
  --mci-g:     #1c2c5b;
  --mci-l:     rgba(108,171,221,0.16);
  /* stat colours */
  --lo:        #0fd9a2;
  --md:        #f7c948;
  --hi-c:      #f55929;
  /* Arsenal result accent */
  --arsenal:   #ef0107;
  /* danger */
  --danger:    #ef4444;
  --warn:      #f59e0b;
  --gold:      #f5c842;
  --rad:       12px;
}

*, *::before, *::after { margin:0; padding:0; box-sizing:border-box; }
html { scroll-behavior:smooth; }
body {
  font-family:'Inter',sans-serif;
  background:var(--bg);
  color:var(--text);
  font-size:14px;
  line-height:1.55;
  -webkit-font-smoothing:antialiased;
}

/* ══════════════════════════════════════════
   ANIMATIONS
══════════════════════════════════════════ */
@keyframes fadeUp   { from { opacity:0; transform:translateY(22px); } to { opacity:1; transform:translateY(0); } }
@keyframes popIn    { from { transform:scale(0.7); opacity:0; }       to { transform:scale(1); opacity:1; } }
@keyframes pulseRed { 0%,100% { box-shadow:0 0 0 0 rgba(239,68,68,0); } 60% { box-shadow:0 0 0 8px rgba(239,68,68,0.2); } }
@keyframes shimmer  { 0% { background-position:-200% center; } 100% { background-position:200% center; } }
@keyframes countUp  { from { opacity:0; transform:scale(0.8); } to { opacity:1; transform:scale(1); } }
.au1 { animation:fadeUp .5s ease both; }
.au2 { animation:fadeUp .5s .1s ease both; }
.au3 { animation:fadeUp .5s .2s ease both; }
.pop { animation:popIn .5s cubic-bezier(.34,1.56,.64,1) both; }
.pop2 { animation:popIn .5s .12s cubic-bezier(.34,1.56,.64,1) both; }

/* ══════════════════════════════════════════
   BREAKING NEWS BANNER
══════════════════════════════════════════ */
.breaking {
  background:linear-gradient(135deg,rgba(239,1,7,.18),rgba(239,1,7,.08));
  border-bottom:2px solid rgba(239,1,7,.5);
  padding:10px 16px;
  display:flex;align-items:center;gap:10px;
  animation:pulseRed 2.5s ease-in-out infinite;
}
.brk-icon { font-size:18px; flex-shrink:0; }
.brk-text { font-size:12.5px; line-height:1.5; }
.brk-text strong { color:#ff6b6b; font-weight:700; }
.brk-text em { color:#fca5a5; font-style:normal; }

/* ══════════════════════════════════════════
   SITE HEADER
══════════════════════════════════════════ */
.site-header {
  background:linear-gradient(170deg, var(--che-l) 0%, var(--bg-2) 45%, var(--mci-l) 100%);
  border-bottom:1px solid var(--border-m);
  padding:22px 16px 18px;
  text-align:center;
  position:relative; overflow:hidden;
}
.site-header::before {
  content:''; position:absolute; inset:0;
  background:radial-gradient(ellipse 80% 250% at 50% -10%, rgba(108,171,221,.06), transparent 65%);
  pointer-events:none;
}
.pl-badge {
  display:inline-flex; align-items:center; gap:7px;
  font-family:'Space Grotesk',sans-serif; font-size:10px; font-weight:700;
  letter-spacing:2px; text-transform:uppercase;
  color:var(--gold); background:rgba(245,200,66,.08);
  border:1px solid rgba(245,200,66,.28); padding:4px 13px; border-radius:20px;
  margin-bottom:11px;
}
.site-header h1 {
  font-family:'Space Grotesk',sans-serif;
  font-size:26px; font-weight:700; color:#fff;
  text-transform:uppercase; letter-spacing:.5px; line-height:1.1;
}
.site-header .sub { font-size:12px; color:var(--muted); margin-top:5px; }

/* Title race context strip */
.gap-strip {
  display:flex; justify-content:center; align-items:center; gap:16px;
  flex-wrap:wrap; margin-top:14px;
}
.gap-pill {
  display:flex; align-items:center; gap:7px;
  font-family:'Space Grotesk',sans-serif; font-size:11px; font-weight:600;
  padding:6px 13px; border-radius:8px; border:1px solid;
}
.gp-ars { background:rgba(239,1,7,.1); border-color:rgba(239,1,7,.25); color:#ff7070; }
.gp-city { background:rgba(108,171,221,.1); border-color:rgba(108,171,221,.28); color:var(--mci-b); }
.gp-gap { background:rgba(245,200,66,.08); border-color:rgba(245,200,66,.25); color:var(--gold); }
.gp-pts { font-family:'Space Grotesk',sans-serif; font-size:16px; font-weight:700; }

/* ══════════════════════════════════════════
   HERO
══════════════════════════════════════════ */
.hero-wrap {
  background:linear-gradient(135deg, rgba(3,70,148,.15) 0%, var(--bg-2) 45%, rgba(108,171,221,.12) 100%);
  border-bottom:1px solid var(--border-m);
  padding:24px 16px 20px;
  position:relative; overflow:hidden;
}
.hero-wrap::before {
  content:''; position:absolute; inset:0;
  background:radial-gradient(ellipse 60% 80% at 50% 50%, rgba(255,255,255,.02), transparent 70%);
  pointer-events:none;
}
.hero-inner {
  max-width:540px; margin:0 auto;
  display:flex; align-items:center; justify-content:space-between; gap:12px;
}
.h-team { display:flex; flex-direction:column; align-items:center; gap:8px; flex:1; }
.badge-ring {
  width:74px; height:74px; border-radius:50%;
  border:1.5px solid var(--border-m);
  background:rgba(255,255,255,.04);
  display:flex; align-items:center; justify-content:center; overflow:hidden;
  filter:drop-shadow(0 4px 20px rgba(0,0,0,.7));
  transition:transform .35s cubic-bezier(.34,1.56,.64,1), filter .3s;
  cursor:default; flex-shrink:0;
}
.badge-ring:hover { transform:scale(1.09) rotate(-2deg); filter:drop-shadow(0 6px 28px rgba(0,0,0,.85)); }
.badge-ring img { width:52px; height:52px; object-fit:contain; }
.h-name {
  font-family:'Space Grotesk',sans-serif; font-size:13px; font-weight:700;
  letter-spacing:.3px; text-transform:uppercase; text-align:center; color:#fff; line-height:1.2;
}
.h-pos { font-size:9px; color:var(--muted); text-transform:uppercase; letter-spacing:.5px; text-align:center; }
.vs-col { display:flex; flex-direction:column; align-items:center; gap:5px; flex-shrink:0; }
.vs-txt { font-family:'Space Grotesk',sans-serif; font-size:24px; font-weight:700; color:rgba(255,255,255,.1); letter-spacing:3px; }
.ko-tag { font-family:'Space Grotesk',sans-serif; font-size:9px; font-weight:700; letter-spacing:1.5px; color:var(--gold); background:rgba(245,200,66,.1); border:1px solid rgba(245,200,66,.25); padding:2px 8px; border-radius:4px; }
.venue-txt { font-size:9px; color:var(--muted); text-align:center; line-height:1.5; }

/* Title Race urgency bar */
.urgency-bar {
  background:linear-gradient(135deg,rgba(245,200,66,.12),rgba(108,171,221,.08));
  border:1px solid rgba(245,200,66,.25); border-radius:9px;
  padding:12px 16px; margin-top:16px; max-width:560px; margin-left:auto; margin-right:auto;
  text-align:center; font-size:12px; line-height:1.6;
}
.urgency-bar strong { color:var(--gold); font-weight:700; }
.urgency-bar em { color:var(--mci-b); font-style:normal; }

/* ══════════════════════════════════════════
   SCORE PREDICTION — prominent section
══════════════════════════════════════════ */
.score-box {
  background:linear-gradient(135deg, var(--bg-3) 0%, var(--bg-4) 100%);
  border:1px solid var(--border-m); border-radius:var(--rad);
  padding:18px 16px; margin-bottom:14px;
  display:flex; flex-direction:column; gap:14px;
  transition:border-color .3s;
}
.score-box:hover { border-color:rgba(108,171,221,.35); }
.score-box-title {
  font-family:'Space Grotesk',sans-serif; font-size:11px; font-weight:700;
  letter-spacing:2px; text-transform:uppercase; color:var(--muted);
  text-align:center; margin-bottom:2px;
}
.scores-row { display:flex; gap:12px; justify-content:center; flex-wrap:wrap; }
.score-card {
  background:var(--bg-5); border:1px solid var(--border); border-radius:9px;
  padding:14px 20px; text-align:center; flex:1; min-width:120px; max-width:200px;
  transition:border-color .3s, transform .3s;
}
.score-card:hover { border-color:rgba(108,171,221,.4); transform:translateY(-2px); }
.score-label { font-size:9px; font-family:'Space Grotesk',sans-serif; font-weight:700; letter-spacing:1.5px; text-transform:uppercase; color:var(--muted); margin-bottom:8px; }
.score-value {
  font-family:'Space Grotesk',sans-serif; font-size:34px; font-weight:700; color:#fff;
  letter-spacing:4px; line-height:1;
}
.score-prob { font-size:10px; color:var(--muted); margin-top:6px; }
.score-best { border-color:rgba(108,171,221,.4); background:linear-gradient(135deg,rgba(108,171,221,.08),var(--bg-5)); }
.score-best .score-label { color:var(--mci-b); }
.score-notes { font-size:11.5px; color:var(--hi); line-height:1.6; }
.score-notes strong { color:var(--gold); }

/* ══════════════════════════════════════════
   PAGE & GRID
══════════════════════════════════════════ */
.page { max-width:700px; margin:0 auto; padding:18px 14px 56px; }

/* card */
.card {
  background:var(--bg-2); border:1px solid var(--border);
  border-radius:var(--rad); overflow:hidden; margin-bottom:14px;
  opacity:0; transform:translateY(14px);
  transition:opacity .5s ease, transform .5s ease, border-color .3s;
}
.card.vis { opacity:1; transform:translateY(0); }
.card:hover { border-color:var(--border-m); }
.card-hd {
  padding:12px 16px 10px; border-bottom:1px solid var(--border);
  display:flex; align-items:center; gap:8px;
}
.hd-dot { width:5px; height:5px; border-radius:50%; flex-shrink:0; }
.hd-title {
  font-family:'Space Grotesk',sans-serif; font-size:10px; font-weight:700;
  letter-spacing:2px; text-transform:uppercase; color:var(--muted); flex:1;
}
.hd-tag { font-size:9px; font-weight:700; letter-spacing:.8px; text-transform:uppercase; padding:2px 8px; border-radius:3px; border:1px solid; }
.card-body { padding:14px 16px; }

/* callout */
.callout {
  background:rgba(255,255,255,.022); border:1px solid var(--border-m);
  border-radius:8px; padding:12px 14px; font-size:12.5px; line-height:1.7; color:var(--hi);
}
.callout strong { color:var(--gold); font-weight:700; }

/* form cols */
.form-cols { display:flex; flex-direction:column; gap:12px; }
.fcol {}
.team-lab {
  display:inline-flex; align-items:center; gap:5px;
  font-size:9.5px; font-weight:700; letter-spacing:1px; text-transform:uppercase;
  padding:2px 8px 2px 4px; border-radius:4px; margin-bottom:7px; border:1px solid;
}
.lab-che { background:rgba(3,70,148,.12); color:#70a8ff; border-color:rgba(3,70,148,.3); }
.lab-mci { background:rgba(108,171,221,.1); color:var(--mci-b); border-color:rgba(108,171,221,.28); }
.tl-img { width:13px; height:13px; object-fit:contain; border-radius:50%; }

.match-list { display:flex; flex-direction:column; gap:3px; }
.mr {
  display:grid; grid-template-columns:6px 44px 1fr auto;
  align-items:center; gap:8px;
  background:var(--bg-3); border:1px solid var(--border);
  border-radius:6px; padding:6px 9px; transition:background .2s;
}
.mr:hover { background:var(--bg-4); }
.rd { width:6px; height:6px; border-radius:50%; }
.rd.W { background:var(--lo); box-shadow:0 0 5px rgba(15,217,162,.4); }
.rd.D { background:var(--md); }
.rd.L { background:var(--hi-c); box-shadow:0 0 5px rgba(245,89,41,.4); }
.ms { font-family:'Space Grotesk',sans-serif; font-size:14px; font-weight:700; color:#fff; text-align:center; }
.mo { font-size:11.5px; color:var(--text); font-weight:500; overflow:hidden; text-overflow:ellipsis; white-space:nowrap; }
.mc { font-size:9px; color:var(--muted); text-transform:uppercase; letter-spacing:.3px; text-align:right; white-space:nowrap; }
.cup-note { font-size:8.5px; color:var(--gold); font-style:italic; }
.f-leg { display:flex; gap:11px; flex-wrap:wrap; margin-top:8px; }
.fl { display:flex; align-items:center; gap:4px; font-size:10.5px; color:var(--muted); }
.fl-dot { width:6px; height:6px; border-radius:50%; }

/* avg grid */
.avg-pair { display:flex; flex-direction:column; gap:11px; }
.a-grp {}
.a-lbl { font-family:'Space Grotesk',sans-serif; font-size:9.5px; font-weight:700; letter-spacing:1.2px; text-transform:uppercase; margin-bottom:7px; }
.avg-grid { display:grid; grid-template-columns:repeat(4,1fr); gap:5px; }
.ac {
  background:var(--bg-3); border:1px solid var(--border); border-radius:8px;
  padding:9px 5px 7px; text-align:center;
  transition:border-color .2s, transform .2s;
}
.ac:hover { border-color:var(--border-m); transform:translateY(-1px); }
.ac .val { font-family:'Space Grotesk',sans-serif; font-size:19px; font-weight:700; color:#fff; line-height:1; }
.ac .lbl { font-size:8.5px; color:var(--muted); margin-top:2px; text-transform:uppercase; letter-spacing:.4px; line-height:1.3; }

/* h2h */
.h2h-bar {
  background:var(--bg-3); border:1px solid var(--border); border-radius:8px;
  padding:12px 10px; display:flex; align-items:center; justify-content:space-between; gap:4px;
}
.hs { text-align:center; flex:1; }
.hn { font-family:'Space Grotesk',sans-serif; font-size:26px; font-weight:700; line-height:1; }
.hl { font-size:9px; color:var(--muted); text-transform:uppercase; letter-spacing:.6px; margin-top:2px; }
.hdv { width:1px; height:34px; background:var(--border); flex-shrink:0; }
.h2h-rows { display:flex; flex-direction:column; gap:3px; margin-top:10px; }
.h2h-r {
  display:grid; grid-template-columns:1fr auto 1fr;
  align-items:center; gap:8px;
  background:var(--bg-4); border:1px solid var(--border); border-radius:6px;
  padding:6px 9px; transition:background .2s;
}
.h2h-r:hover { background:var(--bg-5); }
.rh { font-size:11.5px; font-weight:600; color:var(--text); text-align:left; white-space:nowrap; overflow:hidden; text-overflow:ellipsis; }
.rs { font-family:'Space Grotesk',sans-serif; font-size:14px; font-weight:700; color:#fff; text-align:center; white-space:nowrap; }
.ra { font-size:11.5px; font-weight:600; color:var(--text); text-align:right; white-space:nowrap; overflow:hidden; text-overflow:ellipsis; }
.rsub { font-size:9px; color:var(--muted); text-transform:uppercase; letter-spacing:.3px; grid-column:1/-1; text-align:center; margin-top:-2px; }
.h2h-winner-tag { font-size:8.5px; background:rgba(108,171,221,.15); color:var(--mci-b); padding:1px 5px; border-radius:3px; white-space:nowrap; }

/* pred table */
.pred-leg { display:flex; gap:14px; flex-wrap:wrap; margin-bottom:13px; }
.pli { display:flex; align-items:center; gap:5px; font-size:10.5px; color:var(--muted); }
.pld { width:7px; height:7px; border-radius:50%; }
.pw { overflow-x:auto; -webkit-overflow-scrolling:touch; }
.pt { width:100%; border-collapse:collapse; table-layout:fixed; min-width:290px; }
.pt col.cm { width:28%; }
.pt col.cl { width:16%; }
.pt col.cn { width:16%; }
.pt col.ch { width:16%; }
.pt col.cb { width:24%; }
.pt thead th {
  font-family:'Space Grotesk',sans-serif; font-size:9px; font-weight:700;
  letter-spacing:1.5px; text-transform:uppercase; color:var(--muted);
  padding:0 0 9px; text-align:left; white-space:nowrap; overflow:hidden;
}
.pt thead th:not(:first-child) { text-align:center; }
.pt thead th.th-m { color:var(--md); }
.pt tbody td { padding:7px 3px; border-bottom:1px solid rgba(255,255,255,.035); vertical-align:middle; overflow:hidden; }
.pt tbody tr:last-child td { border-bottom:none; }
.pt tbody tr:hover td { background:rgba(255,255,255,.02); }
.pt tbody td.cmc { color:var(--hi); font-size:12.5px; padding-left:0; font-weight:500; }
.pt tbody td:not(.cmc) { text-align:center; }
.lv { font-family:'Space Grotesk',sans-serif; font-size:17px; font-weight:700; color:var(--lo); line-height:1; }
.mv { font-family:'Space Grotesk',sans-serif; font-size:17px; font-weight:700; color:var(--md); line-height:1; }
.hv { font-family:'Space Grotesk',sans-serif; font-size:17px; font-weight:700; color:var(--hi-c); line-height:1; }

/* animated bar */
.bw { width:85%; max-width:92px; height:5px; background:rgba(255,255,255,.06); border-radius:3px; overflow:hidden; margin:0 auto; display:block; }
.bf { display:block; height:100%; border-radius:3px; width:0; transition:width 1.3s cubic-bezier(.25,.46,.45,.94); }
.bf-che { background:linear-gradient(90deg, #034694, #6cabdd); }

/* yellow cards */
.yc-grid { display:flex; flex-direction:column; gap:7px; }
.yc-row {
  display:flex; align-items:flex-start; gap:9px;
  background:var(--bg-3); border:1px solid var(--border); border-radius:8px;
  padding:9px 11px; transition:border-color .25s, transform .25s;
}
.yc-row:hover { border-color:rgba(255,224,51,.2); transform:translateX(3px); }
.yc-icon { font-size:16px; flex-shrink:0; margin-top:1px; }
.yc-info { flex:1; min-width:0; }
.yc-name { font-size:12.5px; font-weight:700; color:#fff; }
.yc-club { font-size:9px; font-family:'Space Grotesk',sans-serif; letter-spacing:.7px; text-transform:uppercase; }
.yc-reason { font-size:11px; color:var(--muted); margin-top:2px; line-height:1.45; }
.yc-risk {
  font-family:'Space Grotesk',sans-serif; font-size:9px; font-weight:700;
  letter-spacing:1px; text-transform:uppercase; padding:2px 8px; border-radius:4px; flex-shrink:0; align-self:center;
}
.risk-h { background:rgba(245,89,41,.13); color:var(--hi-c); border:1px solid rgba(245,89,41,.28); }
.risk-m { background:rgba(247,201,72,.1); color:var(--md); border:1px solid rgba(247,201,72,.25); }

/* notes */
.note { margin-bottom:9px; font-size:12.5px; line-height:1.65; color:var(--hi); }
.note:last-child { margin-bottom:0; }
.note strong { color:var(--gold); font-weight:700; }

/* footer */
footer { text-align:center; padding:18px 14px; font-size:11.5px; color:rgba(76,85,116,.4); border-top:1px solid var(--border); }

/* ═══ TABLET 640px+ ═══ */
@media(min-width:640px){
  body { font-size:15px; }
  .page { max-width:920px; padding:22px 24px 62px; }
  .site-header { padding:26px 24px 22px; }
  .site-header h1 { font-size:32px; }
  .hero-wrap { padding:28px 24px 22px; }
  .hero-inner { max-width:620px; }
  .badge-ring { width:86px; height:86px; }
  .badge-ring img { width:62px; height:62px; }
  .h-name { font-size:15px; }
  .vs-txt { font-size:30px; }
  .card-hd { padding:13px 20px 11px; }
  .card-body { padding:16px 20px; }
  .form-cols { flex-direction:row; gap:16px; }
  .fcol { flex:1; min-width:0; }
  .avg-pair { flex-direction:row; gap:16px; }
  .a-grp { flex:1; }
  .ac .val { font-size:21px; }
  .hn { font-size:30px; }
  .lv,.mv,.hv { font-size:20px; }
  .pt tbody td { padding:8px 4px; }
  .bw { max-width:110px; height:5px; }
  .callout { font-size:13.5px; }
  .note { font-size:13.5px; }
  .score-value { font-size:42px; }
}

/* ═══ DESKTOP 1040px+ ═══ */
@media(min-width:1040px){
  .page { max-width:1380px; padding:28px 40px 70px; }
  .site-header { padding:28px 40px 24px; }
  .site-header h1 { font-size:38px; }
  .hero-wrap { padding:28px 40px 22px; }
  .hero-inner { max-width:680px; }
  .badge-ring { width:94px; height:94px; }
  .badge-ring img { width:68px; height:68px; }
  /* two-column layout */
  .dg { display:grid; grid-template-columns:1fr 1fr; gap:20px; align-items:start; }
  .dg .fw { grid-column:1/-1; }
  .card-hd { padding:14px 22px 12px; }
  .card-body { padding:18px 22px; }
  .ac .val { font-size:23px; }
  .lv,.mv,.hv { font-size:21px; }
  .hn { font-size:32px; }
  .bw { max-width:100px; }
}

/* ═══ WIDE 1360px+ ═══ */
@media(min-width:1360px){
  .page { max-width:1520px; padding:32px 60px 78px; }
  .site-header { padding:30px 60px 24px; }
  .hero-wrap { padding:30px 60px 22px; }
  .hero-inner { max-width:750px; }
  .dg { gap:26px; }
}
</style>
</head>
<body>

<!-- ══════════ BREAKING NEWS ══════════ -->
<div class="breaking au1">
  <div class="brk-icon">🚨</div>
  <div class="brk-text">
    <strong>RESULT — Arsenal 1–2 Bournemouth (Sat 11 Apr, 12:30 BST).</strong>
    <em> Kroupi (17') put Bournemouth ahead, Gyökeres pen (35') levelled, then Alex Scott (74') won it. Arsenal booed off at the Emirates. Arsenal remain on 70 pts from 32 games. Man City CAN cut the gap to SIX POINTS with a win today — title race blown wide open.</em>
  </div>
</div>

<!-- ══════════ SITE HEADER ══════════ -->
<header class="site-header au2">
  <div class="pl-badge">Premier League · Matchweek 32 · Super Sunday · 12 April 2026</div>
  <h1>Tam Bilbo Analytics</h1>
  <p class="sub">· Stamford Bridge &nbsp;·&nbsp; 4:30pm BST &nbsp;·&nbsp; Ref: Chris Kavanagh &nbsp;·</p>

  <div class="gap-strip">
    <div class="gap-pill gp-ars"><span>Arsenal</span><span class="gp-pts" style="color:#ff7070">70 pts</span><span style="font-size:9px;color:#fca5a5">32 gms</span></div>
    <div class="gap-pill gp-gap">→ <span style="font-size:8px">WIN TODAY CLOSES GAP TO</span> <span class="gp-pts">6 pts</span></div>
    <div class="gap-pill gp-city"><span>Man City</span><span class="gp-pts" style="color:var(--mci-b)">61 pts</span><span style="font-size:9px;color:rgba(108,171,221,.7)">31 gms · GiH</span></div>
  </div>
</header>

<!-- ══════════ HERO ══════════ -->
<div class="hero-wrap au3">
  <div class="hero-inner">

    <!-- CHELSEA -->
    <div class="h-team">
      <div class="badge-ring pop">
        <img src="https://upload.wikimedia.org/wikipedia/en/thumb/c/cc/Chelsea_FC.svg/120px-Chelsea_FC.svg.png"
             alt="Chelsea FC"
             onerror="this.parentElement.innerHTML='<svg viewBox=&quot;0 0 60 60&quot; style=&quot;width:52px;height:52px&quot;><circle cx=&quot;30&quot; cy=&quot;30&quot; r=&quot;28&quot; fill=&quot;#034694&quot;/><text x=&quot;30&quot; y=&quot;35&quot; text-anchor=&quot;middle&quot; font-size=&quot;11&quot; fill=&quot;#fff&quot; font-weight=&quot;bold&quot;>CFC</text></svg>'">
      </div>
      <div class="h-name">Chelsea FC</div>
      <div class="h-pos">6th · 48 pts<br>UEFA Champion League Race</div>
    </div>

    <div class="vs-col">
      <div class="vs-txt">VS</div>
      <div class="ko-tag">4:30 BST</div>
      <div class="venue-txt">Stamford Bridge<br>London · Sun 12 Apr</div>
    </div>

    <!-- MAN CITY -->
    <div class="h-team">
      <div class="badge-ring pop2">
        <img src="https://upload.wikimedia.org/wikipedia/en/thumb/e/eb/Manchester_City_FC_badge.svg/120px-Manchester_City_FC_badge.svg.png"
             alt="Manchester City"
             onerror="this.parentElement.innerHTML='<svg viewBox=&quot;0 0 60 60&quot; style=&quot;width:52px;height:52px&quot;><circle cx=&quot;30&quot; cy=&quot;30&quot; r=&quot;28&quot; fill=&quot;#1c2c5b&quot;/><text x=&quot;30&quot; y=&quot;35&quot; text-anchor=&quot;middle&quot; font-size=&quot;11&quot; fill=&quot;#6cabdd&quot; font-weight=&quot;bold&quot;>MCFC</text></svg>'">
      </div>
      <div class="h-name">Manchester City</div>
      <div class="h-pos">2nd · 61 pts · Game in Hand<br>Title Rivals</div>
    </div>

  </div>

  <div class="urgency-bar">
    <strong>Arsenal just lost to Bournemouth.</strong> A City win closes the gap to <em>6 points</em> with a crucial Etihad head-to-head next Sunday (Apr 19). Guardiola's April PL win rate: <strong>79%</strong>. This is <strong>the</strong> match of the weekend.
  </div>
</div>

<!-- ══════════ PAGE CONTENT ══════════ -->
<div class="page">
<div class="dg">

  <!-- ── SCORE PREDICTIONS ── -->
  <div class="score-box fw">
    <div class="score-box-title">📊 Score Predictions — Based on All Data &amp; Weighted Context</div>
    <div class="scores-row">
      <div class="score-card">
        <div class="score-label">Half-Time</div>
        <div class="score-value" style="color:#6cabdd">0 – 1</div>
        <div class="score-prob" style="color:var(--mci-b)">Man City · Most Likely</div>
      </div>
      <div class="score-card score-best">
        <div class="score-label">Full-Time Best Pick</div>
        <div class="score-value" style="color:#6cabdd">1 – 2</div>
        <div class="score-prob" style="color:var(--mci-b)">Man City win · ~32% probability</div>
      </div>
      <div class="score-card">
        <div class="score-label">Alternative</div>
        <div class="score-value" style="color:var(--md)">1 – 1</div>
        <div class="score-prob">Draw · ~24% probability</div>
      </div>
    </div>
    <div class="score-notes">
      <strong>Why City win is the weighted pick:</strong> City are unbeaten in 12 consecutive meetings with Chelsea (W7 D5). Chelsea have not beaten City since the 2021 Champions League final. Arsenal's loss today gives City maximum motivation — Guardiola's side win 79% of April PL games. Chelsea are without Enzo Fernández (suspended — their most creative line-breaker). City won 3 of the last 4 PL visits to Stamford Bridge. However, Chelsea need a win for UCL qualification and both teams play beautiful football — 1–1 is the draw risk to consider. The low H2H goal average (1.4 per game in last 5) suggests a tight match, with City's quality eventually telling. <strong>HT 0–1 reflects City's typical fast start (scored before HT in 4 of last 5 UCL/PL games).</strong>
    </div>
  </div>

  <!-- ── CONTEXT ── -->
  <div class="card fw">
    <div class="card-hd">
      <div class="hd-dot" style="background:var(--gold)"></div>
      <div class="hd-title">Match Context</div>
      <div class="hd-tag" style="color:var(--gold);border-color:rgba(245,200,66,.28);background:rgba(245,200,66,.07)">Title Race Decider · Arsenal -2 Today</div>
    </div>
    <div class="card-body">
      <div class="callout">
        <strong>Arsenal just lost.</strong> Everything changes. City can close to within 6 points with a game in hand and then face Arsenal directly at the Etihad next Sunday — making tonight effectively a title race six-pointer by proxy. Chelsea sit 6th on 48 pts, two points above Brentford/Everton in the European qualification scrap. Both teams desperately need three points for completely different reasons. Chelsea without the suspended <strong>Enzo Fernández</strong> (their top chance creator — 41 line-breaking passes, the most in the PL). City without Rubén Dias (injury) but with Rodri back. Ref Kavanagh has issued <strong>86 yellows in 23 PL games (3.7/game)</strong> — expect cards to flow. Chelsea have had at least 2 players booked in each of their last 6 games.
      </div>
    </div>
  </div>

  <!-- ── LAST 5 FORM ── -->
  <div class="card fw">
    <div class="card-hd">
      <div class="hd-dot" style="background:#70a8ff"></div>
      <div class="hd-title">Last 5 Matches — All Competitions</div>
    </div>
    <div class="card-body">
      <div class="form-cols">

        <!-- CHELSEA -->
        <div class="fcol">
          <div class="team-lab lab-che">
            <img class="tl-img" src="https://upload.wikimedia.org/wikipedia/en/thumb/c/cc/Chelsea_FC.svg/120px-Chelsea_FC.svg.png" alt="">
            Chelsea
          </div>
          <div class="match-list">
            <div class="mr"><div class="rd W"></div><div class="ms">7–0</div><div class="mo">Port Vale</div><div class="mc">FAC QF <span class="cup-note">Apr 5</span></div></div>
            <div class="mr"><div class="rd L"></div><div class="ms">0–3</div><div class="mo">Everton</div><div class="mc">PL · Away</div></div>
            <div class="mr"><div class="rd L"></div><div class="ms">0–1</div><div class="mo">Newcastle</div><div class="mc">PL · Home</div></div>
            <div class="mr"><div class="rd L"></div><div class="ms">0–3</div><div class="mo">PSG</div><div class="mc">UCL wait... wait</div></div>
            <div class="mr"><div class="rd D"></div><div class="ms">2–2</div><div class="mo">Leeds United</div><div class="mc">PL · Home</div></div>
          </div>
          <p style="font-size:10px;color:var(--muted);margin-top:7px;">W1 D1 L3 in last 5 · PL: W1 D2 L3 in last 6 · One win in 6 PL games</p>
        </div>

        <!-- MAN CITY -->
        <div class="fcol">
          <div class="team-lab lab-mci">
            <img class="tl-img" src="https://upload.wikimedia.org/wikipedia/en/thumb/e/eb/Manchester_City_FC_badge.svg/120px-Manchester_City_FC_badge.svg.png" alt="">
            Manchester City
          </div>
          <div class="match-list">
            <div class="mr"><div class="rd W"></div><div class="ms">4–0</div><div class="mo">Liverpool</div><div class="mc">FAC QF <span class="cup-note">Apr 5</span></div></div>
            <div class="mr"><div class="rd D"></div><div class="ms">1–1</div><div class="mo">West Ham</div><div class="mc">PL · Away</div></div>
            <div class="mr"><div class="rd D"></div><div class="ms">2–2</div><div class="mo">Nott'm Forest</div><div class="mc">PL · Home</div></div>
            <div class="mr"><div class="rd W"></div><div class="ms">2–0</div><div class="mo">Arsenal</div><div class="mc">EFL Cup Final <span class="cup-note">🏆</span></div></div>
            <div class="mr"><div class="rd W"></div><div class="ms">3–1</div><div class="mo">Brighton</div><div class="mc">PL · Home</div></div>
          </div>
          <p style="font-size:10px;color:var(--muted);margin-top:7px;">W3 D2 in last 5 · Unbeaten in last 8 PL · Won Carabao Cup vs Arsenal</p>
        </div>

      </div>
      <div class="f-leg">
        <div class="fl"><div class="fl-dot" style="background:var(--lo)"></div>Win</div>
        <div class="fl"><div class="fl-dot" style="background:var(--md)"></div>Draw</div>
        <div class="fl"><div class="fl-dot" style="background:var(--hi-c)"></div>Loss</div>
      </div>
    </div>
  </div>

  <!-- ── SEASON AVERAGES ── -->
  <div class="card fw">
    <div class="card-hd">
      <div class="hd-dot" style="background:#a78bfa"></div>
      <div class="hd-title">Season Averages per Match — Last 10 Games (All Comps)</div>
    </div>
    <div class="card-body">
      <div class="avg-pair">
        <div class="a-grp">
          <div class="a-lbl" style="color:#70a8ff">Chelsea — Last 10</div>
          <div class="avg-grid">
            <div class="ac"><div class="val">13.5</div><div class="lbl">Shots</div></div>
            <div class="ac"><div class="val">4.3</div><div class="lbl">SOT</div></div>
            <div class="ac"><div class="val">6.9</div><div class="lbl">Corners</div></div>
            <div class="ac"><div class="val">10.5</div><div class="lbl">Fouls</div></div>
          </div>
          <div class="avg-grid" style="margin-top:5px">
            <div class="ac"><div class="val">62%</div><div class="lbl">Possession</div></div>
            <div class="ac"><div class="val">1.9</div><div class="lbl">Goals/Gm</div></div>
            <div class="ac"><div class="val">3.7</div><div class="lbl">Corners vs</div></div>
            <div class="ac"><div class="val">7</div><div class="lbl">Red cards season</div></div>
          </div>
        </div>
        <div class="a-grp">
          <div class="a-lbl" style="color:var(--mci-b)">Man City — Last 10</div>
          <div class="avg-grid">
            <div class="ac"><div class="val">15.7</div><div class="lbl">Shots</div></div>
            <div class="ac"><div class="val">4.9</div><div class="lbl">SOT</div></div>
            <div class="ac"><div class="val">5.7</div><div class="lbl">Corners</div></div>
            <div class="ac"><div class="val">9.0</div><div class="lbl">Fouls</div></div>
          </div>
          <div class="avg-grid" style="margin-top:5px">
            <div class="ac"><div class="val">63%</div><div class="lbl">Possession</div></div>
            <div class="ac"><div class="val">1.6</div><div class="lbl">Goals/Gm</div></div>
            <div class="ac"><div class="val">3.3</div><div class="lbl">Corners vs</div></div>
            <div class="ac"><div class="val">79%</div><div class="lbl">April PL wins</div></div>
          </div>
        </div>
      </div>
    </div>
  </div>

  <!-- ── H2H ── -->
  <div class="card fw">
    <div class="card-hd">
      <div class="hd-dot" style="background:var(--hi-c)"></div>
      <div class="hd-title">Head to Head — Last 5 Meetings (All Comps)</div>
    </div>
    <div class="card-body">
      <div class="h2h-bar">
        <div class="hs"><div class="hn" style="color:#70a8ff">0</div><div class="hl">Chelsea Wins</div></div>
        <div class="hdv"></div>
        <div class="hs"><div class="hn" style="color:var(--md)">2</div><div class="hl">Draws</div></div>
        <div class="hdv"></div>
        <div class="hs"><div class="hn" style="color:var(--mci-b)">3</div><div class="hl">City Wins</div></div>
        <div class="hdv"></div>
        <div class="hs"><div class="hn">1.4</div><div class="hl">Avg Goals/Gm</div></div>
      </div>
      <p style="font-size:10.5px;color:var(--muted);margin-top:8px;margin-bottom:8px;">Chelsea have not beaten Man City in any competition since the 2021 Champions League Final (12 meetings ago). Chelsea have scored ≤1 goal in 12 of their last 13 meetings.</p>
      <div class="h2h-rows">
        <div class="h2h-r">
          <div class="rh">Man City</div>
          <div class="rs">1–1 &nbsp;<span class="h2h-winner-tag">D</span></div>
          <div class="ra">Chelsea</div>
          <div class="rsub">PL · Etihad · Jan 4, 2026 (Reijnders 42', Fernandez pen 94')</div>
        </div>
        <div class="h2h-r">
          <div class="rh">Man City</div>
          <div class="rs">3–1 &nbsp;<span class="h2h-winner-tag">City W</span></div>
          <div class="ra">Chelsea</div>
          <div class="rsub">PL · Etihad · Jan 25, 2025</div>
        </div>
        <div class="h2h-r">
          <div class="rh">Chelsea</div>
          <div class="rs">0–2 &nbsp;<span class="h2h-winner-tag">City W</span></div>
          <div class="ra">Man City</div>
          <div class="rsub">PL · Stamford Bridge · Aug 18, 2024</div>
        </div>
        <div class="h2h-r">
          <div class="rh">Man City</div>
          <div class="rs">1–0 &nbsp;<span class="h2h-winner-tag">City W</span></div>
          <div class="ra">Chelsea</div>
          <div class="rsub">FA Cup SF · Wembley · Apr 20, 2024</div>
        </div>
        <div class="h2h-r">
          <div class="rh">Man City</div>
          <div class="rs">1–1 &nbsp;<span class="h2h-winner-tag">D</span></div>
          <div class="ra">Chelsea</div>
          <div class="rsub">PL · Etihad · Feb 17, 2024</div>
        </div>
      </div>
      <p style="font-size:10.5px;color:var(--muted);margin-top:9px;">Chelsea's last home PL win vs City: January 2020 (Frank Lampard era). City won 3 of their last 4 at Stamford Bridge.</p>
    </div>
  </div>

  <!-- ── STAT PREDICTIONS ── -->
  <div class="card fw" id="pred-card">
    <div class="card-hd">
      <div class="hd-dot" style="background:var(--lo)"></div>
      <div class="hd-title">📊 Weighted Predictions — Chelsea vs Man City (Both Teams)</div>
    </div>
    <div class="card-body">
      <div class="pred-leg">
        <div class="pli"><div class="pld" style="background:var(--lo)"></div><span style="color:var(--lo);font-weight:700">Low</span> = floor</div>
        <div class="pli"><div class="pld" style="background:var(--md)"></div><span style="color:var(--md);font-weight:700">Median</span> = weighted expected</div>
        <div class="pli"><div class="pld" style="background:var(--hi-c)"></div><span style="color:var(--hi-c);font-weight:700">High</span> = ceiling</div>
      </div>
      <div class="pw">
      <table class="pt">
        <colgroup><col class="cm"><col class="cl"><col class="cn"><col class="ch"><col class="cb"></colgroup>
        <thead>
          <tr>
            <th>Metric</th>
            <th style="color:var(--lo)">Low</th>
            <th class="th-m">Median</th>
            <th style="color:var(--hi-c)">High</th>
            <th style="text-align:center;color:var(--muted)">Intensity</th>
          </tr>
        </thead>
        <tbody>
          <tr><td class="cmc">Corners</td>        <td><span class="lv">8</span></td><td><span class="mv">11</span></td><td><span class="hv">15</span></td><td><div class="bw"><div class="bf bf-che" data-pct="64"></div></div></td></tr>
          <tr><td class="cmc">Total Shots</td>    <td><span class="lv">20</span></td><td><span class="mv">26</span></td><td><span class="hv">36</span></td><td><div class="bw"><div class="bf bf-che" data-pct="70"></div></div></td></tr>
          <tr><td class="cmc">Shots on Target</td><td><span class="lv">6</span></td><td><span class="mv">9</span></td><td><span class="hv">14</span></td><td><div class="bw"><div class="bf bf-che" data-pct="62"></div></div></td></tr>
          <tr><td class="cmc">Fouls</td>          <td><span class="lv">15</span></td><td><span class="mv">22</span></td><td><span class="hv">32</span></td><td><div class="bw"><div class="bf bf-che" data-pct="66"></div></div></td></tr>
          <tr><td class="cmc">Throw-ins</td>      <td><span class="lv">32</span></td><td><span class="mv">44</span></td><td><span class="hv">58</span></td><td><div class="bw"><div class="bf bf-che" data-pct="64"></div></div></td></tr>
          <tr><td class="cmc">Goal Kicks</td>     <td><span class="lv">14</span></td><td><span class="mv">20</span></td><td><span class="hv">28</span></td><td><div class="bw"><div class="bf bf-che" data-pct="58"></div></div></td></tr>
          <tr><td class="cmc">Tackles</td>        <td><span class="lv">22</span></td><td><span class="mv">30</span></td><td><span class="hv">40</span></td><td><div class="bw"><div class="bf bf-che" data-pct="68"></div></div></td></tr>
          <tr><td class="cmc">Offsides</td>       <td><span class="lv">3</span></td><td><span class="mv">5</span></td><td><span class="hv">9</span></td><td><div class="bw"><div class="bf bf-che" data-pct="46"></div></div></td></tr>
        </tbody>
      </table>
      </div>
    </div>
  </div>

  <!-- ── YELLOW CARDS ── -->
  <div class="card fw">
    <div class="card-hd">
      <div class="hd-dot" style="background:#ffe033"></div>
      <div class="hd-title">🟨 Yellow Card Risk Players</div>
      <div class="hd-tag" style="color:var(--md);border-color:rgba(247,201,72,.28);background:rgba(247,201,72,.08)">Kavanagh avg 3.7 cards/game</div>
    </div>
    <div class="card-body">
      <div class="yc-grid">

        <div class="yc-row">
          <div class="yc-icon">🟨</div>
          <div class="yc-info">
            <div class="yc-name">Moisés Caicedo <span class="yc-club" style="color:#70a8ff">Chelsea · DM</span></div>
            <div class="yc-reason">Chelsea's most combative midfielder — without Enzo Fernandez, Caicedo bears the full burden of controlling City's midfield. He will be forced to foul to break up City's possession cycles. Already on 6 PL yellows this season. Will face Rodri and Reijnders in a crucial midfield battle.</div>
          </div>
          <div class="yc-risk risk-h">HIGH</div>
        </div>

        <div class="yc-row">
          <div class="yc-icon">🟨</div>
          <div class="yc-info">
            <div class="yc-name">Rodri <span class="yc-club" style="color:var(--mci-b)">Man City · DM</span></div>
            <div class="yc-reason">Back from long-term injury and building match sharpness. Will be playing a dominant role but is still not at full sharpness. High-stakes games after Arsenal's result will trigger intense reactions. His comeback means he over-commits in tackles to prove fitness. 3 bookings already since January return.</div>
          </div>
          <div class="yc-risk risk-h">HIGH</div>
        </div>

        <div class="yc-row">
          <div class="yc-icon">🟨</div>
          <div class="yc-info">
            <div class="yc-name">Roméo Lavia <span class="yc-club" style="color:#70a8ff">Chelsea · DM</span></div>
            <div class="yc-reason">Likely to play the No.6 role without Fernandez. Physically capable but up against City's quality pressing midfield. His reactive defensive instincts in a game where Chelsea will struggle to control possession make a booking likely. Chelsea "2.13 yellow cards per game at home."</div>
          </div>
          <div class="yc-risk risk-h">HIGH</div>
        </div>

        <div class="yc-row">
          <div class="yc-icon">🟨</div>
          <div class="yc-info">
            <div class="yc-name">Marc Cucurella <span class="yc-club" style="color:#70a8ff">Chelsea · LB</span></div>
            <div class="yc-reason">Aggressive left-back who clashes with wide forwards. Against City's right-side threats (Semenyo, Nunes), Cucurella will make physical challenges. He has a history of late tackles and Kavanagh won't hesitate — 4 PL yellows already.</div>
          </div>
          <div class="yc-risk risk-m">MED</div>
        </div>

        <div class="yc-row">
          <div class="yc-icon">🟨</div>
          <div class="yc-info">
            <div class="yc-name">Rayan Cherki <span class="yc-club" style="color:var(--mci-b)">Man City · MF</span></div>
            <div class="yc-reason">City's most creative player (8 assists) who dribbles through tight spaces and draws fouls. But he also fouls when possession is lost. In a high-intensity title-defining game, his reactions and protests could attract Kavanagh's attention. Kavanagh has 4 red cards this season — all to away teams.</div>
          </div>
          <div class="yc-risk risk-m">MED</div>
        </div>

        <div class="yc-row">
          <div class="yc-icon">🟨</div>
          <div class="yc-info">
            <div class="yc-name">Abdukodir Khusanov <span class="yc-club" style="color:var(--mci-b)">Man City · CB</span></div>
            <div class="yc-reason">Young centre-back who will face Chelsea's pressing high and will need to deal with João Pedro's pace and physicality. Has committed tactical fouls in high-stakes games. If Chelsea get in behind City's backline, Khusanov's instinct may be to foul.</div>
          </div>
          <div class="yc-risk risk-m">MED</div>
        </div>

      </div>
    </div>
  </div>

  <!-- ── ANALYTICAL NOTES ── -->
  <div class="card fw">
    <div class="card-hd">
      <div class="hd-dot" style="background:#60a5fa"></div>
      <div class="hd-title">Analytical Notes — Weighting Factors</div>
    </div>
    <div class="card-body">

      <div class="note"><strong>🔴 Arsenal's Loss — The Defining Context:</strong> Arsenal losing to Bournemouth is the single biggest context factor in this entire prediction set. It transforms Chelsea vs City from a routine mid-table-vs-title-contender clash into a genuine title six-pointer. Guardiola's April record (79% wins) combined with maximum motivation makes City the weighted favourite despite Chelsea's home advantage. City also face Arsenal at the Etihad next Sunday — a win today sets up a potential 3-point gap entering that direct head-to-head.</div>

      <div class="note"><strong>Corners (8–11–15):</strong> Chelsea average 6.9 corners/game at home, City 5.7 away. Combined baseline ~12.6 but H2H meetings are consistently tight possession contests that reduce corner frequency. H2H average has been around 9–11 corners. Chelsea had over 4.5 corners in their last 5 home games. Median of 11 is well-anchored. High end if Chelsea dominate periods of the match chasing a goal.</div>

      <div class="note"><strong>Total Shots (20–26–36):</strong> Chelsea 13.5/game; City 15.7/game. Combined baseline ~29. Both teams are elite possession sides — when two high-possession teams meet, the combined shot count is often lower than the sum of individual averages (less territory exchange = fewer shooting opportunities per team). H2H Jan 4 produced a tighter game. City avg 14.7 shots in recent PL, Chelsea 13.74 for full season. Median of 26 reflects a tight, controlled game.</div>

      <div class="note"><strong>SOT (6–9–14):</strong> Chelsea 4.3 SOT/game, City 4.9/game. Combined baseline ~9.2. Chelsea's Robert Sanchez vs City's Donnarumma — both quality keepers. Without Enzo Fernandez, Chelsea's shot creation is reduced. H2H Jan 4: Chelsea had only 4 shots total per some reports. Median of 9 is conservative but well-supported. High end requires Chelsea to open up at home.</div>

      <div class="note"><strong>Fouls (15–22–32):</strong> Chelsea 10.5 fouls/game; City only 9.0 (Guardiola's teams rarely foul). Combined baseline ~19.5. The high-stakes nature and Chelsea's physicality (7 red cards this season) pushes the median to 22. Kavanagh averages 3.7 yellows/game and has given all 4 red cards to away teams this season — City's away players are a card risk. Chelsea home average 2.13 yellows/game.</div>

      <div class="note"><strong>Throw-ins (32–44–58):</strong> Both teams contest wide areas intensely. Cucurella vs City's right side, City's left side vs Chelsea's right. PL average ~44. No major deviation expected — median of 44 sits at the league average. High end if City's pressing creates rapid wide transitions.</div>

      <div class="note"><strong>Goal Kicks (14–20–28):</strong> Both teams press high, forcing goal kicks from the opponent. City allow only 3.3 corners against per game, suggesting opponents' keepers restart frequently (cleared balls = corners vs goal kicks reduced by City's shape). Chelsea allow 3.7 against. Both keepers will restart under press. Median of 20 is standard for a high-press tactical encounter.</div>

      <div class="note"><strong>Tackles (22–30–40):</strong> Both teams are possession sides with relatively low tackle counts for PL teams. Chelsea ~13/game, City ~12/game = ~25 combined baseline. The title race intensity pushes this up. Without Fernandez, Chelsea's midfield will need to tackle more to win the ball. Median of 30 is above season average to reflect the high stakes.</div>

      <div class="note"><strong>Offsides (3–5–9):</strong> Both teams have pace runners who challenge defensive lines. Haaland (City) is a perpetual offside risk. João Pedro and Pedro Neto (Chelsea) run in behind. Both teams play high defensive lines. Combined season average ~4.5 per game in H2H-type games. Median of 5 is well-grounded.</div>

      <div class="note"><strong>Score Rationale — Full-Time 1–2 City:</strong> City's H2H dominance (12 meetings unbeaten), Arsenal's result providing maximum motivation, Chelsea without their key creator Enzo Fernandez, and Guardiola's 79% April win rate all point to a City victory. Chelsea will likely get a goal given their home threat and City's leaky recent form (drew West Ham and Forest). But City's quality should ultimately prevail. The key variable: Chelsea 1-0 would represent a genuine title-swing moment — their European qualification pressure, the atmosphere at Stamford Bridge, and their history of dropping points from winning positions (15 dropped this season, 13 at Stamford Bridge) suggests they won't keep a clean sheet.</div>

    </div>
  </div>

</div><!-- /dg -->
</div><!-- /page -->

<footer>
  <strong>Team Bilbo Statistical Analysis</strong><br>Predictions are statistical estimates based on actual data, H2H and contextual factors including Arsenal's loss to Bournemouth on Saturday. <strong>Not financial advice.</strong><br> · 12 April 2026 ·

<script>
(function(){
  'use strict';

  /* scroll reveal cards */
  var cards = document.querySelectorAll('.card');
  if('IntersectionObserver' in window){
    var obs = new IntersectionObserver(function(entries){
      entries.forEach(function(e){
        if(e.isIntersecting){ e.target.classList.add('vis'); obs.unobserve(e.target); }
      });
    },{threshold:0.06});
    cards.forEach(function(c){ obs.observe(c); });
  } else {
    cards.forEach(function(c){ c.classList.add('vis'); });
  }

  /* bar fill animation */
  var predCard = document.getElementById('pred-card');
  if(predCard && 'IntersectionObserver' in window){
    var bObs = new IntersectionObserver(function(entries){
      entries.forEach(function(e){
        if(e.isIntersecting){
          setTimeout(function(){
            predCard.querySelectorAll('.bf[data-pct]').forEach(function(b){
              b.style.width = b.getAttribute('data-pct') + '%';
            });
          }, 200);
          bObs.unobserve(e.target);
        }
      });
    },{threshold:0.2});
    bObs.observe(predCard);
  } else {
    setTimeout(function(){
      document.querySelectorAll('.bf[data-pct]').forEach(function(b){
        b.style.width = b.getAttribute('data-pct') + '%';
      });
    }, 600);
  }

  /* count-up on stat cells */
  var acObs = new IntersectionObserver(function(entries){
    entries.forEach(function(e){
      if(e.isIntersecting){
        var v = e.target.querySelector('.val');
        if(v && !v.dataset.done){
          v.dataset.done = '1';
          var raw = v.textContent.trim();
          var isPct = raw.indexOf('%') !== -1;
          var num = parseFloat(raw.replace('%',''));
          if(!isNaN(num)){
            var cur = 0, dur = 800, step = num/(dur/16);
            var t = setInterval(function(){
              cur += step;
              if(cur >= num){ cur = num; clearInterval(t); }
              var d = (String(num).indexOf('.') !== -1) ? cur.toFixed(1) : Math.round(cur);
              v.textContent = d + (isPct ? '%' : '');
            }, 16);
          }
        }
        acObs.unobserve(e.target);
      }
    });
  },{threshold:0.7});
  document.querySelectorAll('.ac').forEach(function(el){ acObs.observe(el); });

})();
</script>
</body>
</html>
