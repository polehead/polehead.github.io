<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>UCL QF 2nd Legs | Liverpool v PSG · Atlético v Barcelona · Stats Predictor</title>
<link rel="preconnect" href="https://fonts.googleapis.com">
<link href="https://fonts.googleapis.com/css2?family=Barlow+Condensed:wght@400;500;600;700;800;900&family=Barlow:wght@300;400;500;600&display=swap" rel="stylesheet">
<style>
/* ════════════════════════════════════════════
   TOKENS — UCL Midnight Steel theme
════════════════════════════════════════════ */
:root {
  --bg:       #03040d;
  --bg2:      #07091a;
  --bg3:      #0d1128;
  --bg4:      #141730;
  --bg5:      #1a2039;
  --border:   rgba(255,255,255,.07);
  --bm:       rgba(255,255,255,.13);
  --text:     #bfc9e2;
  --muted:    #454e72;
  --hi:       #818db4;
  /* UCL brand */
  --ucl:      #1b4dbe;
  --ucl-l:    #3d76ff;
  --ucl-g:    #c9a227;
  --ucl-gs:   rgba(201,162,39,.18);
  /* team colours */
  --liv-r:    #c8102e;   --liv-l:rgba(200,16,46,.2);
  --psg-n:    #004170;   --psg-r:rgba(0,65,112,.2);
  --atm-r:    #cb3524;   --atm-l:rgba(203,53,36,.18);
  --bar-b:    #a50044;   --bar-l:rgba(0,82,147,.18);
  /* stat palette */
  --lo:       #0fd9a2;
  --md:       #f7c948;
  --hic:      #f55929;
  /* danger */
  --danger:   #ef4444;
  --warn:     #f59e0b;
}

*, *::before, *::after { margin:0; padding:0; box-sizing:border-box; }
html { scroll-behavior:smooth; }
body {
  font-family:'Barlow', sans-serif;
  background:var(--bg);
  color:var(--text);
  font-size:14px;
  line-height:1.55;
  -webkit-font-smoothing:antialiased;
  overflow-x:hidden;
}

/* ════ ANIMATIONS ════ */
@keyframes fadeUp   { from{opacity:0;transform:translateY(24px)} to{opacity:1;transform:translateY(0)} }
@keyframes popBadge { from{transform:scale(.65);opacity:0}        to{transform:scale(1);opacity:1} }
@keyframes starSpin { from{transform:rotate(0)}                   to{transform:rotate(360deg)} }
@keyframes glow     { 0%,100%{opacity:.4} 50%{opacity:.9} }
@keyframes countUp  { from{opacity:0;transform:scale(.7)} to{opacity:1;transform:scale(1)} }

/* ════ STARS BG ════ */
.stars-bg {
  position:fixed;inset:0;pointer-events:none;z-index:0;
  background:
    radial-gradient(ellipse 80% 60% at 15% 20%, rgba(27,77,190,.07), transparent 60%),
    radial-gradient(ellipse 60% 50% at 80% 70%, rgba(27,77,190,.05), transparent 60%);
}

/* ════ SITE HEADER ════ */
.site-header {
  position:relative;z-index:2;
  background:linear-gradient(170deg, rgba(27,77,190,.14) 0%, var(--bg2) 50%, rgba(201,162,39,.06) 100%);
  border-bottom:1px solid rgba(27,77,190,.3);
  text-align:center;
  padding:20px 16px 18px;
  overflow:hidden;
}
.site-header::before {
  content:'⭐';font-size:90px;opacity:.03;
  position:absolute;left:50%;top:50%;transform:translate(-50%,-50%);
  animation:starSpin 30s linear infinite;pointer-events:none;
}
.ucl-badge {
  display:inline-flex;align-items:center;gap:8px;
  font-family:'Barlow Condensed',sans-serif;font-size:11px;font-weight:700;letter-spacing:2.5px;
  color:var(--ucl-g);background:var(--ucl-gs);border:1px solid rgba(201,162,39,.35);
  padding:4px 14px;border-radius:20px;margin-bottom:11px;text-transform:uppercase;
}
.site-header h1 {
  font-family:'Barlow Condensed',sans-serif;font-size:26px;font-weight:900;
  letter-spacing:2px;text-transform:uppercase;color:#fff;line-height:1.1;
}
.site-header .sub { font-size:12px;color:var(--muted);margin-top:5px; }
/* match nav */
.match-nav {
  display:flex;justify-content:center;gap:8px;flex-wrap:wrap;margin-top:13px;
}
.mnav-btn {
  font-family:'Barlow Condensed',sans-serif;font-size:10px;font-weight:700;
  letter-spacing:1.5px;text-transform:uppercase;
  padding:5px 13px;border-radius:6px;border:1px solid;
  text-decoration:none;transition:background .2s,border-color .2s;
}
.mn-liv { color:var(--liv-r);border-color:rgba(200,16,46,.3);background:rgba(200,16,46,.06); }
.mn-liv:hover { background:rgba(200,16,46,.14);border-color:rgba(200,16,46,.5); }
.mn-atm { color:#ff8c42;border-color:rgba(203,53,36,.3);background:rgba(203,53,36,.06); }
.mn-atm:hover { background:rgba(203,53,36,.14);border-color:rgba(203,53,36,.5); }

/* ════ TIE STATUS BANNER ════ */
.tie-banner {
  padding:11px 16px;
  display:flex;align-items:flex-start;gap:10px;
  border-bottom:1px solid var(--border);
}
.tb-liv { background:linear-gradient(135deg,rgba(200,16,46,.12),rgba(200,16,46,.04)); border-bottom-color:rgba(200,16,46,.2); }
.tb-atm { background:linear-gradient(135deg,rgba(203,53,36,.12),rgba(203,53,36,.04)); border-bottom-color:rgba(203,53,36,.2); }
.tb-icon { font-size:20px;flex-shrink:0;animation:glow 2s ease-in-out infinite; }
.tb-text { font-size:12px;line-height:1.6;color:var(--hi); }
.tb-text strong { font-weight:700; }
.tb-text .agg { font-family:'Barlow Condensed',sans-serif;font-size:18px;font-weight:900;letter-spacing:1px; }

/* ════ MATCH HERO ════ */
.match-hero {
  border-bottom:1px solid var(--bm);
  padding:24px 16px 20px;
  position:relative;overflow:hidden;
}
.mh-liv { background:linear-gradient(135deg,var(--liv-l) 0%,var(--bg2) 45%,var(--psg-r) 100%); }
.mh-atm { background:linear-gradient(135deg,var(--atm-l) 0%,var(--bg2) 45%,var(--bar-l) 100%); }
.mh-glow {
  position:absolute;inset:0;
  background:radial-gradient(ellipse 70% 80% at 50% 50%,rgba(27,77,190,.04),transparent 70%);
  pointer-events:none;
}
.hero-inner {
  max-width:540px;margin:0 auto;
  display:flex;align-items:center;justify-content:space-between;gap:12px;
}
.h-team { display:flex;flex-direction:column;align-items:center;gap:8px;flex:1; }
.badge-ring {
  width:76px;height:76px;border-radius:50%;
  border:1.5px solid var(--bm);background:rgba(255,255,255,.04);
  display:flex;align-items:center;justify-content:center;overflow:hidden;
  filter:drop-shadow(0 4px 20px rgba(0,0,0,.75));
  animation:popBadge .55s cubic-bezier(.34,1.56,.64,1) both;
  transition:transform .3s cubic-bezier(.34,1.56,.64,1);cursor:default;flex-shrink:0;
}
.badge-ring:hover { transform:scale(1.1) rotate(-3deg); }
.badge-ring img { width:54px;height:54px;object-fit:contain; }
.h-name {
  font-family:'Barlow Condensed',sans-serif;font-size:13px;font-weight:800;
  letter-spacing:.5px;text-transform:uppercase;text-align:center;color:#fff;line-height:1.15;
}
.h-pos { font-size:9px;color:var(--muted);text-transform:uppercase;letter-spacing:.5px;text-align:center; }
.vs-col { display:flex;flex-direction:column;align-items:center;gap:5px;flex-shrink:0; }
.vs-txt {
  font-family:'Barlow Condensed',sans-serif;font-size:24px;font-weight:900;
  color:rgba(255,255,255,.1);letter-spacing:3px;
}
.ko-tag {
  font-family:'Barlow Condensed',sans-serif;font-size:9px;font-weight:800;letter-spacing:1.5px;
  color:var(--ucl-g);background:var(--ucl-gs);border:1px solid rgba(201,162,39,.3);
  padding:2px 8px;border-radius:4px;
}
.venue-txt { font-size:9px;color:var(--muted);text-align:center;line-height:1.5; }

/* ════ PAGE ════ */
.page { max-width:700px;margin:0 auto;padding:18px 14px 56px;position:relative;z-index:1; }

/* section divider */
.sec-div {
  text-align:center;padding:22px 0 12px;position:relative;
}
.sec-div::before {
  content:'';position:absolute;left:0;right:0;top:50%;height:1px;
  background:linear-gradient(90deg,transparent,rgba(27,77,190,.3),rgba(201,162,39,.3),rgba(27,77,190,.3),transparent);
}
.sec-div-in {
  display:inline-flex;align-items:center;gap:9px;
  background:var(--bg);padding:0 14px;position:relative;
  font-family:'Barlow Condensed',sans-serif;font-size:10px;font-weight:800;
  letter-spacing:2.5px;text-transform:uppercase;color:var(--ucl-l);
}

/* card */
.card {
  background:var(--bg2);border:1px solid var(--border);
  border-radius:10px;overflow:hidden;margin-bottom:12px;
  opacity:0;transform:translateY(14px);
  transition:opacity .5s ease,transform .5s ease,border-color .3s;
}
.card.vis { opacity:1;transform:translateY(0); }
.card:hover { border-color:var(--bm); }
.card-hd {
  padding:11px 16px 9px;border-bottom:1px solid var(--border);
  display:flex;align-items:center;gap:7px;
}
.hd-dot { width:5px;height:5px;border-radius:50%;flex-shrink:0; }
.hd-title {
  font-family:'Barlow Condensed',sans-serif;font-size:10px;font-weight:700;
  letter-spacing:2px;text-transform:uppercase;color:var(--muted);flex:1;
}
.hd-tag {
  font-size:8.5px;font-weight:700;letter-spacing:.8px;text-transform:uppercase;
  padding:2px 7px;border-radius:3px;border:1px solid;
}
.card-body { padding:14px 16px; }

/* callout */
.callout {
  background:rgba(255,255,255,.022);border:1px solid var(--bm);
  border-radius:8px;padding:12px 14px;font-size:12.5px;line-height:1.7;color:var(--hi);
}
.callout strong { color:var(--md);font-weight:700; }

/* form cols */
.form-cols { display:flex;flex-direction:column;gap:12px; }
.fcol {}
.team-lab {
  display:inline-flex;align-items:center;gap:5px;
  font-size:9px;font-weight:700;letter-spacing:1px;text-transform:uppercase;
  padding:2px 8px 2px 4px;border-radius:4px;margin-bottom:7px;border:1px solid;
}
.lab-liv { background:rgba(200,16,46,.1);color:#ff7070;border-color:rgba(200,16,46,.28); }
.lab-psg { background:rgba(0,65,112,.14);color:#60a5fa;border-color:rgba(0,65,112,.35); }
.lab-atm { background:rgba(203,53,36,.1);color:#ff8c42;border-color:rgba(203,53,36,.28); }
.lab-bar { background:rgba(0,82,147,.12);color:#60a5fa;border-color:rgba(0,82,147,.3); }
.tl-img { width:13px;height:13px;object-fit:contain; }

.match-list { display:flex;flex-direction:column;gap:3px; }
.mr {
  display:grid;grid-template-columns:6px 44px 1fr auto;
  align-items:center;gap:8px;
  background:var(--bg3);border:1px solid var(--border);
  border-radius:6px;padding:6px 9px;transition:background .2s;
}
.mr:hover { background:var(--bg4); }
.rd { width:6px;height:6px;border-radius:50%; }
.rd.W { background:var(--lo);box-shadow:0 0 5px rgba(15,217,162,.4); }
.rd.D { background:var(--md); }
.rd.L { background:var(--hic);box-shadow:0 0 5px rgba(245,89,41,.4); }
.ms { font-family:'Barlow Condensed',sans-serif;font-size:14px;font-weight:800;color:#fff;text-align:center; }
.mo { font-size:11.5px;color:var(--text);font-weight:500;overflow:hidden;text-overflow:ellipsis;white-space:nowrap; }
.mc { font-size:9px;color:var(--muted);text-transform:uppercase;letter-spacing:.3px;text-align:right;white-space:nowrap; }
.ucl-pill {
  font-size:8px;font-family:'Barlow Condensed',sans-serif;font-weight:700;letter-spacing:.8px;text-transform:uppercase;
  padding:1px 5px;border-radius:3px;background:var(--ucl-gs);color:var(--ucl-g);border:1px solid rgba(201,162,39,.25);
}
.f-leg { display:flex;gap:11px;flex-wrap:wrap;margin-top:8px; }
.fl { display:flex;align-items:center;gap:4px;font-size:10px;color:var(--muted); }
.fl-dot { width:6px;height:6px;border-radius:50%; }

/* avg grid */
.avg-pair { display:flex;flex-direction:column;gap:11px; }
.a-grp {}
.a-lbl {
  font-family:'Barlow Condensed',sans-serif;font-size:10px;font-weight:700;
  letter-spacing:1.5px;text-transform:uppercase;margin-bottom:7px;
}
.avg-g { display:grid;grid-template-columns:repeat(4,1fr);gap:5px; }
.ac {
  background:var(--bg3);border:1px solid var(--border);border-radius:7px;
  padding:8px 5px 6px;text-align:center;transition:border-color .2s,transform .2s;
}
.ac:hover { border-color:var(--bm);transform:translateY(-1px); }
.ac .val { font-family:'Barlow Condensed',sans-serif;font-size:19px;font-weight:800;color:#fff;line-height:1; }
.ac .lbl { font-size:8px;color:var(--muted);margin-top:2px;text-transform:uppercase;letter-spacing:.4px;line-height:1.3; }

/* h2h bar */
.h2h-bar {
  background:var(--bg3);border:1px solid var(--border);border-radius:7px;
  padding:11px 10px;display:flex;align-items:center;justify-content:space-between;gap:4px;
}
.hs { text-align:center;flex:1; }
.hn { font-family:'Barlow Condensed',sans-serif;font-size:26px;font-weight:900;line-height:1; }
.hl { font-size:9px;color:var(--muted);text-transform:uppercase;letter-spacing:.6px;margin-top:2px; }
.hdv { width:1px;height:32px;background:var(--border);flex-shrink:0; }
.h2h-rows { display:flex;flex-direction:column;gap:3px;margin-top:10px; }
.h2h-r {
  display:grid;grid-template-columns:1fr auto 1fr;align-items:center;gap:8px;
  background:var(--bg4);border:1px solid var(--border);border-radius:6px;
  padding:6px 9px;transition:background .2s;
}
.h2h-r:hover { background:var(--bg5); }
.rh { font-size:11.5px;font-weight:600;color:var(--text);text-align:left;white-space:nowrap;overflow:hidden;text-overflow:ellipsis; }
.rs { font-family:'Barlow Condensed',sans-serif;font-size:14px;font-weight:800;color:#fff;text-align:center;white-space:nowrap; }
.ra { font-size:11.5px;font-weight:600;color:var(--text);text-align:right;white-space:nowrap;overflow:hidden;text-overflow:ellipsis; }
.rsub { font-size:8.5px;color:var(--muted);text-transform:uppercase;letter-spacing:.3px;grid-column:1/-1;text-align:center;margin-top:-2px; }

/* SCORE BOX */
.score-box {
  background:linear-gradient(135deg,var(--bg3),var(--bg4));
  border:1px solid var(--bm);border-radius:10px;padding:17px 16px;margin-bottom:12px;
}
.sb-title {
  font-family:'Barlow Condensed',sans-serif;font-size:11px;font-weight:700;
  letter-spacing:2.5px;text-transform:uppercase;color:var(--muted);text-align:center;margin-bottom:14px;
}
.scores-row { display:flex;gap:10px;justify-content:center;flex-wrap:wrap; }
.sc {
  background:var(--bg5);border:1px solid var(--border);border-radius:8px;
  padding:13px 18px;text-align:center;flex:1;min-width:110px;max-width:190px;
  transition:border-color .3s,transform .3s;
}
.sc:hover { transform:translateY(-2px); }
.sc-lbl { font-family:'Barlow Condensed',sans-serif;font-size:9px;font-weight:700;letter-spacing:1.5px;text-transform:uppercase;color:var(--muted);margin-bottom:7px; }
.sc-val { font-family:'Barlow Condensed',sans-serif;font-size:36px;font-weight:900;letter-spacing:4px;line-height:1; }
.sc-prob { font-size:9px;color:var(--muted);margin-top:5px; }
.sc-best { border-color:rgba(201,162,39,.35);background:linear-gradient(135deg,rgba(201,162,39,.08),var(--bg5)); }
.sc-best .sc-lbl { color:var(--ucl-g); }
.sb-notes { font-size:12px;color:var(--hi);line-height:1.65;margin-top:12px; }
.sb-notes strong { color:var(--md);font-weight:700; }

/* PRED TABLE */
.pred-leg { display:flex;gap:13px;flex-wrap:wrap;margin-bottom:12px; }
.pli { display:flex;align-items:center;gap:5px;font-size:10.5px;color:var(--muted); }
.pld { width:7px;height:7px;border-radius:50%; }
.pw { overflow-x:auto;-webkit-overflow-scrolling:touch; }
.pt { width:100%;border-collapse:collapse;table-layout:fixed;min-width:285px; }
.pt col.cm{width:29%}.pt col.cl{width:16%}.pt col.cn{width:16%}.pt col.ch{width:16%}.pt col.cb{width:23%}
.pt thead th {
  font-family:'Barlow Condensed',sans-serif;font-size:9px;font-weight:700;
  letter-spacing:1.5px;text-transform:uppercase;color:var(--muted);
  padding:0 0 9px;text-align:left;white-space:nowrap;
}
.pt thead th:not(:first-child) { text-align:center; }
.pt thead th.th-m { color:var(--md); }
.pt tbody td { padding:7px 3px;border-bottom:1px solid rgba(255,255,255,.03);vertical-align:middle;overflow:hidden; }
.pt tbody tr:last-child td { border-bottom:none; }
.pt tbody tr:hover td { background:rgba(255,255,255,.02); }
.pt tbody td.cmc { color:var(--hi);font-size:12px;padding-left:0;font-weight:500; }
.pt tbody td:not(.cmc) { text-align:center; }
.lv { font-family:'Barlow Condensed',sans-serif;font-size:18px;font-weight:800;color:var(--lo);line-height:1; }
.mv { font-family:'Barlow Condensed',sans-serif;font-size:18px;font-weight:800;color:var(--md);line-height:1; }
.hv { font-family:'Barlow Condensed',sans-serif;font-size:18px;font-weight:800;color:var(--hic);line-height:1; }
.bw { width:85%;max-width:88px;height:5px;background:rgba(255,255,255,.06);border-radius:3px;overflow:hidden;margin:0 auto;display:block; }
.bf { display:block;height:100%;border-radius:3px;width:0;transition:width 1.3s cubic-bezier(.25,.46,.45,.94); }
.bf-liv { background:linear-gradient(90deg,var(--liv-r),#ff6b6b); }
.bf-atm { background:linear-gradient(90deg,var(--atm-r),#f5c842); }

/* YELLOW CARDS */
.yc-grid { display:flex;flex-direction:column;gap:7px; }
.yc-row {
  display:flex;align-items:flex-start;gap:9px;
  background:var(--bg3);border:1px solid var(--border);border-radius:8px;
  padding:9px 11px;transition:border-color .25s,transform .25s;
}
.yc-row:hover { border-color:rgba(255,224,51,.2);transform:translateX(3px); }
.yc-icon { font-size:16px;flex-shrink:0;margin-top:1px; }
.yc-info { flex:1;min-width:0; }
.yc-name { font-size:12.5px;font-weight:700;color:#fff; }
.yc-club { font-size:9px;font-family:'Barlow Condensed',sans-serif;letter-spacing:.7px;text-transform:uppercase; }
.yc-reason { font-size:11px;color:var(--muted);margin-top:2px;line-height:1.45; }
.yc-risk {
  font-family:'Barlow Condensed',sans-serif;font-size:9px;font-weight:700;
  letter-spacing:1.2px;text-transform:uppercase;padding:2px 8px;border-radius:4px;flex-shrink:0;align-self:center;
}
.risk-h { background:rgba(245,89,41,.14);color:var(--hic);border:1px solid rgba(245,89,41,.28); }
.risk-m { background:rgba(247,201,72,.1);color:var(--md);border:1px solid rgba(247,201,72,.25); }

/* NOTES */
.note { margin-bottom:9px;font-size:12.5px;line-height:1.65;color:var(--hi); }
.note:last-child { margin-bottom:0; }
.note strong { color:var(--md);font-weight:700; }

/* FOOTER */
footer {
            text-align: center;
            padding: 18px 14px;
            font-size: 11.5px;
            color: var(--muted);
            border-top: 1px solid var(--border);
        }
/* ════ TABLET 640px+ ════ */
@media(min-width:640px){
  body{font-size:15px;}
  .page{max-width:920px;padding:22px 24px 62px;}
  .site-header{padding:26px 24px 22px;}
  .site-header h1{font-size:32px;}
  .match-hero{padding:28px 24px 22px;}
  .hero-inner{max-width:620px;}
  .badge-ring{width:84px;height:84px;}
  .badge-ring img{width:60px;height:60px;}
  .h-name{font-size:15px;}
  .card-hd{padding:12px 20px 10px;}
  .card-body{padding:16px 20px;}
  .form-cols{flex-direction:row;gap:16px;}
  .fcol{flex:1;min-width:0;}
  .avg-pair{flex-direction:row;gap:16px;}
  .a-grp{flex:1;}
  .ac .val{font-size:21px;}
  .hn{font-size:30px;}
  .lv,.mv,.hv{font-size:21px;}
  .bw{max-width:110px;}
  .sc-val{font-size:42px;}
}

/* ════ DESKTOP 1040px+ ════ */
@media(min-width:1040px){
  .page{max-width:1380px;padding:28px 40px 68px;}
  .site-header{padding:28px 40px 24px;}
  .site-header h1{font-size:38px;}
  .match-hero{padding:28px 40px 22px;}
  .hero-inner{max-width:680px;}
  .badge-ring{width:92px;height:92px;}
  .badge-ring img{width:66px;height:66px;}
  .dg{display:grid;grid-template-columns:1fr 1fr;gap:20px;align-items:start;}
  .dg .fw{grid-column:1/-1;}
  .card-hd{padding:13px 22px 11px;}
  .card-body{padding:17px 22px;}
  .ac .val{font-size:22px;}
  .lv,.mv,.hv{font-size:22px;}
  .hn{font-size:32px;}
  .bw{max-width:96px;}
}

/* ════ WIDE 1360px+ ════ */
@media(min-width:1360px){
  .page{max-width:1540px;padding:32px 60px 76px;}
  .site-header{padding:30px 60px 24px;}
  .match-hero{padding:30px 60px 24px;}
  .dg{gap:26px;}
}
</style>
</head>
<body>
<div class="stars-bg"></div>

<!-- ════ SITE HEADER ════ -->
<header class="site-header">
  <div class="ucl-badge">⭐ UEFA Champions League · Quarter-Finals · Second Legs · 14–15 April 2026</div>
  <h1>UCL QF Second Leg Stats Predictor</h1>
  <p class="sub">Liverpool vs PSG &nbsp;·&nbsp; Atlético Madrid vs Barcelona &nbsp;·&nbsp; Form · Season Avgs · H2H · Weighted Predictions · Score Forecasts</p>
  <nav class="match-nav">
    <a href="#liv-psg" class="mnav-btn mn-liv">🔴 Liverpool vs PSG · Anfield · 9pm BST</a>
    <a href="#atm-bar" class="mnav-btn mn-atm">🔴 Atlético vs Barcelona · Metropolitano · 9pm CET</a>
  </nav>
</header>

<!-- ══════════════════════════════════════
     MATCH 1 — LIVERPOOL vs PSG
══════════════════════════════════════ -->

<!-- Tie Status Banner -->
<div class="tie-banner tb-liv" id="liv-psg">
  <div class="tb-icon">⚡</div>
  <div class="tb-text">
    <strong>TIE STATUS — PSG lead 2–0 on aggregate.</strong> First leg: PSG 2–0 Liverpool (Doué 11', Kvaratskhelia 66'). Liverpool had <strong>0 shots on target</strong> and 26% possession in Paris. Liverpool need to win by 3+ goals to progress in 90 minutes, or 2-0 to force extra time / penalties. PSG can afford a 1-goal defeat and still advance. <span class="agg" style="color:#ff7070">AGG: PSG 2–0</span>
  </div>
</div>

<div class="match-hero mh-liv">
  <div class="mh-glow"></div>
  <div class="hero-inner">
    <div class="h-team">
      <div class="badge-ring">
        <img src="https://upload.wikimedia.org/wikipedia/en/thumb/0/0c/Liverpool_FC.svg/120px-Liverpool_FC.svg.png" alt="Liverpool">
      </div>
      <div class="h-name">Liverpool FC</div>
      <div class="h-pos">5th PL · 2–0 down · Need 3 goals</div>
    </div>
    <div class="vs-col">
      <div class="vs-txt">VS</div>
      <div class="ko-tag">9pm BST</div>
      <div class="venue-txt">Anfield · Liverpool, England<br>Ref: Maurizio Mariani (ITA)</div>
    </div>
    <div class="h-team">
      <div class="badge-ring" style="animation-delay:.14s">
        <img src="https://upload.wikimedia.org/wikipedia/en/thumb/a/a7/Paris_Saint-Germain_F.C..svg/120px-Paris_Saint-Germain_F.C..svg.png" alt="PSG">
      </div>
      <div class="h-name">Paris SG</div>
      <div class="h-pos">UCL Holders · 2–0 up · Controlled</div>
    </div>
  </div>
</div>

<div class="page">
<div class="dg">

  <!-- SCORE PREDICTION -->
  <div class="score-box fw">
    <div class="sb-title">📊 Score Prediction — Liverpool vs PSG</div>
    <div class="scores-row">
      <div class="sc">
        <div class="sc-lbl">Half-Time</div>
        <div class="sc-val" style="color:#ff7070">1 – 0</div>
        <div class="sc-prob">Liverpool · ~36% probability</div>
      </div>
      <div class="sc sc-best">
        <div class="sc-lbl">Full-Time Best Pick</div>
        <div class="sc-val" style="color:#ff7070">2 – 1</div>
        <div class="sc-prob">PSG progress 3–2 on agg · ~26%</div>
      </div>
      <div class="sc" style="border-color:rgba(0,65,112,.4)">
        <div class="sc-lbl">If Liverpool dream</div>
        <div class="sc-val" style="color:#60a5fa">3 – 0</div>
        <div class="sc-prob">Anfield magic · ~9% probability</div>
      </div>
    </div>
    <div class="sb-notes">
      <strong>Why 2–1 to Liverpool / PSG progress:</strong> Anfield will be electric and Liverpool historically attack from the first whistle in comeback nights (scored in the first half in 9 of last 10 home games). PSG, however, lead 2-0 and need only a draw — Luis Enrique will set up with one eye on protecting the aggregate. PSG won 4 consecutive away games keeping clean sheets in the last 3. Liverpool had 0 shots on target in Paris — that must improve but a full Anfield comeback requires extraordinary performance. PSG's away quality and discipline make the 3-0 required scoreline extremely unlikely. Liverpool scoring first is highly probable, but PSG will respond. <strong>The 2-1 / PSG progress (3-2 agg) is the most logical weighted outcome</strong>, balancing Anfield pressure vs PSG's superiority shown in Leg 1.
    </div>
  </div>

  <!-- CONTEXT -->
  <div class="card fw">
    <div class="card-hd">
      <div class="hd-dot" style="background:var(--md)"></div>
      <div class="hd-title">Context — Second Leg Stakes</div>
      <div class="hd-tag" style="color:var(--ucl-g);border-color:rgba(201,162,39,.28);background:var(--ucl-gs)">UCL QF 2nd Leg</div>
    </div>
    <div class="card-body">
      <div class="callout">
        Liverpool overcame a 3-0 first-leg deficit against Barcelona at Anfield in 2019 — the only time in UCL history that is remotely comparable. But PSG are the reigning champions and far better equipped than that Barca side. Luis Enrique has <strong>warned against a PSG "trap"</strong> — he saw how 2019 unfolded and will ensure his team are prepared for maximum pressure. Liverpool beat Fulham 2-0 on Saturday with Salah and Ngumoha (17yo) scoring. PSG had the weekend off after their Lens fixture was postponed. <strong>Alisson still injured</strong> — Mamardashvili starts. Barcola and Ndjantou absent for PSG. Kvaratskhelia and Nuno Mendes are both one yellow card from a potential semi-final ban — cautious in challenges. Wirtz has <strong>28 open-play chances created in this UCL</strong> — the most of any player.
      </div>
    </div>
  </div>

  <!-- FORM -->
  <div class="card fw">
    <div class="card-hd">
      <div class="hd-dot" style="background:var(--liv-r)"></div>
      <div class="hd-title">Last 5 Matches — All Competitions</div>
    </div>
    <div class="card-body">
      <div class="form-cols">
        <div class="fcol">
          <div class="team-lab lab-liv"><img class="tl-img" src="https://upload.wikimedia.org/wikipedia/en/thumb/0/0c/Liverpool_FC.svg/120px-Liverpool_FC.svg.png" alt="">Liverpool</div>
          <div class="match-list">
            <div class="mr"><div class="rd W"></div><div class="ms">2–0</div><div class="mo">Fulham</div><div class="mc">PL · Sat <span class="ucl-pill">just played</span></div></div>
            <div class="mr"><div class="rd L"></div><div class="ms">0–2</div><div class="mo">PSG (Leg 1)</div><div class="mc">UCL QF <span class="ucl-pill">0 SOT</span></div></div>
            <div class="mr"><div class="rd L"></div><div class="ms">1–2</div><div class="mo">Brighton</div><div class="mc">PL · Away</div></div>
            <div class="mr"><div class="rd L"></div><div class="ms">0–4</div><div class="mo">Man City</div><div class="mc">FAC · Away</div></div>
            <div class="mr"><div class="rd W"></div><div class="ms">4–0</div><div class="mo">Galatasaray</div><div class="mc">UCL R16</div></div>
          </div>
        </div>
        <div class="fcol">
          <div class="team-lab lab-psg"><img class="tl-img" src="https://upload.wikimedia.org/wikipedia/en/thumb/a/a7/Paris_Saint-Germain_F.C..svg/120px-Paris_Saint-Germain_F.C..svg.png" alt="">Paris SG</div>
          <div class="match-list">
            <div class="mr"><div class="rd W"></div><div class="ms">2–0</div><div class="mo">Liverpool (Leg 1)</div><div class="mc">UCL QF <span class="ucl-pill">18 shots</span></div></div>
            <div class="mr"><div class="rd W"></div><div class="ms">8–2</div><div class="mo">Chelsea (agg)</div><div class="mc">UCL R16</div></div>
            <div class="mr"><div class="rd W"></div><div class="ms">W</div><div class="mo">Ligue 1 (×2)</div><div class="mc">Ligue 1</div></div>
            <div class="mr"><div class="rd W"></div><div class="ms">W</div><div class="mo">Monaco</div><div class="mc">UCL QF prev</div></div>
            <div class="mr"><div class="rd W"></div><div class="ms">–</div><div class="mo">Weekend postponed</div><div class="mc">vs Lens · Rest</div></div>
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
      <div class="hd-title">Season Averages — UCL 2025/26 (Last 10 All Comps)</div>
    </div>
    <div class="card-body">
      <div class="avg-pair">
        <div class="a-grp">
          <div class="a-lbl" style="color:#ff7070">Liverpool</div>
          <div class="avg-g">
            <div class="ac"><div class="val">17.7</div><div class="lbl">Shots</div></div>
            <div class="ac"><div class="val">6.2</div><div class="lbl">SOT</div></div>
            <div class="ac"><div class="val">6.7</div><div class="lbl">Corners</div></div>
            <div class="ac"><div class="val">10.4</div><div class="lbl">Fouls</div></div>
          </div>
        </div>
        <div class="a-grp">
          <div class="a-lbl" style="color:#60a5fa">PSG — UCL Leading Stats</div>
          <div class="avg-g">
            <div class="ac"><div class="val">18.3</div><div class="lbl">Shots</div></div>
            <div class="ac"><div class="val">7.3</div><div class="lbl">SOT</div></div>
            <div class="ac"><div class="val">5.3</div><div class="lbl">Corners</div></div>
            <div class="ac"><div class="val">11.8</div><div class="lbl">Fouls</div></div>
          </div>
          <p style="font-size:10px;color:var(--muted);margin-top:6px;">UCL leaders: goals (36), shots (259), SOT (96), box touches (486). 67% possession avg. Won 7 of 10 UCL games. 4 clean sheets Safonov.</p>
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
        <div class="hs"><div class="hn" style="color:#ff7070">2</div><div class="hl">Liverpool</div></div>
        <div class="hdv"></div>
        <div class="hs"><div class="hn" style="color:var(--md)">0</div><div class="hl">Draws</div></div>
        <div class="hdv"></div>
        <div class="hs"><div class="hn" style="color:#60a5fa">3</div><div class="hl">PSG</div></div>
        <div class="hdv"></div>
        <div class="hs"><div class="hn">2.4</div><div class="hl">Avg Goals</div></div>
      </div>
      <p style="font-size:10.5px;color:var(--muted);margin-top:8px;margin-bottom:8px;">No draws in last 7 meetings between these two clubs. Over 9.5 corners in all 4 recent H2H meetings. Liverpool won 2 of their last 3 at Anfield vs PSG.</p>
      <div class="h2h-rows">
        <div class="h2h-r"><div class="rh">PSG</div><div class="rs">2–0</div><div class="ra">Liverpool</div><div class="rsub">UCL QF Leg 1 · Paris · Apr 8, 2026</div></div>
        <div class="h2h-r"><div class="rh">Liverpool</div><div class="rs">0–1</div><div class="ra">PSG</div><div class="rsub">UCL R16 Leg 2 · Anfield · Mar 2025 (PSG won on pens)</div></div>
        <div class="h2h-r"><div class="rh">PSG</div><div class="rs">0–1</div><div class="ra">Liverpool</div><div class="rsub">UCL R16 Leg 1 · Paris · Feb 2025 (LIV won leg)</div></div>
        <div class="h2h-r"><div class="rh">Liverpool</div><div class="rs">3–2</div><div class="ra">PSG</div><div class="rsub">UCL League Phase · Anfield · Nov 2024</div></div>
        <div class="h2h-r"><div class="rh">PSG</div><div class="rs">1–0</div><div class="ra">Liverpool</div><div class="rsub">UCL League Phase · Paris · Jan 2025</div></div>
      </div>
    </div>
  </div>

  <!-- PREDICTIONS -->
  <div class="card fw" id="pred-liv">
    <div class="card-hd">
      <div class="hd-dot" style="background:var(--lo)"></div>
      <div class="hd-title">📊 Weighted Stat Predictions — Liverpool vs PSG (2nd Leg)</div>
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
          <tr><td class="cmc">Corners</td>        <td><span class="lv">9</span></td><td><span class="mv">13</span></td><td><span class="hv">18</span></td><td><div class="bw"><div class="bf bf-liv" data-pct="78"></div></div></td></tr>
          <tr><td class="cmc">Total Shots</td>    <td><span class="lv">22</span></td><td><span class="mv">30</span></td><td><span class="hv">42</span></td><td><div class="bw"><div class="bf bf-liv" data-pct="82"></div></div></td></tr>
          <tr><td class="cmc">Shots on Target</td><td><span class="lv">7</span></td><td><span class="mv">11</span></td><td><span class="hv">17</span></td><td><div class="bw"><div class="bf bf-liv" data-pct="72"></div></div></td></tr>
          <tr><td class="cmc">Fouls</td>          <td><span class="lv">17</span></td><td><span class="mv">24</span></td><td><span class="hv">34</span></td><td><div class="bw"><div class="bf bf-liv" data-pct="68"></div></div></td></tr>
          <tr><td class="cmc">Throw-ins</td>      <td><span class="lv">36</span></td><td><span class="mv">50</span></td><td><span class="hv">66</span></td><td><div class="bw"><div class="bf bf-liv" data-pct="80"></div></div></td></tr>
          <tr><td class="cmc">Goal Kicks</td>     <td><span class="lv">14</span></td><td><span class="mv">22</span></td><td><span class="hv">32</span></td><td><div class="bw"><div class="bf bf-liv" data-pct="66"></div></div></td></tr>
          <tr><td class="cmc">Tackles</td>        <td><span class="lv">26</span></td><td><span class="mv">36</span></td><td><span class="hv">50</span></td><td><div class="bw"><div class="bf bf-liv" data-pct="82"></div></div></td></tr>
          <tr><td class="cmc">Offsides</td>       <td><span class="lv">3</span></td><td><span class="mv">7</span></td><td><span class="hv">13</span></td><td><div class="bw"><div class="bf bf-liv" data-pct="60"></div></div></td></tr>
        </tbody>
      </table></div>
    </div>
  </div>

  <!-- YELLOW CARDS LIV/PSG -->
  <div class="card fw">
    <div class="card-hd">
      <div class="hd-dot" style="background:#ffe033"></div>
      <div class="hd-title">🟨 Yellow Card Risk Players</div>
      <div class="hd-tag" style="color:var(--md);border-color:rgba(247,201,72,.28);background:rgba(247,201,72,.07)">Mariani avg 4+ cards/game · Semi-final ban at stake</div>
    </div>
    <div class="card-body"><div class="yc-grid">
      <div class="yc-row"><div class="yc-icon">🟨</div><div class="yc-info">
        <div class="yc-name">Ryan Gravenberch <span class="yc-club" style="color:#ff7070">Liverpool · MF</span></div>
        <div class="yc-reason">Liverpool need goals urgently — Gravenberch will press intensely from the first minute, making more aggressive challenges than usual. Without Endo, Gravenberch is the anchor in a midfield that must both attack and destroy. A foul on Vitinha or Neves breaking at pace = booking.</div>
      </div><div class="yc-risk risk-h">HIGH</div></div>

      <div class="yc-row"><div class="yc-icon">🟨</div><div class="yc-info">
        <div class="yc-name">João Neves <span class="yc-club" style="color:#60a5fa">PSG · MF</span></div>
        <div class="yc-reason">The Portuguese midfielder will be tasked with breaking up Liverpool's desperate attacks. As Liverpool push numbers forward in the second half, Neves' tactical fouling becomes his primary tool. Second-leg pressure and Anfield atmosphere create perfect conditions for impulsive bookings.</div>
      </div><div class="yc-risk risk-h">HIGH</div></div>

      <div class="yc-row"><div class="yc-icon">🟨</div><div class="yc-info">
        <div class="yc-name">Vitinha <span class="yc-club" style="color:#60a5fa">PSG · MF</span></div>
        <div class="yc-reason">Vitinha will be expected to time-waste and shield the ball if PSG go ahead. At Anfield with a hostile crowd, time-wasting earns yellows from Mariani. Also, his frustrated reaction to being fouled repeatedly has drawn cards before. His bookings came most frequently in high-pressure games.</div>
      </div><div class="yc-risk risk-m">MED</div></div>

      <div class="yc-row"><div class="yc-icon">🟨</div><div class="yc-info">
        <div class="yc-name">Alexis Mac Allister <span class="yc-club" style="color:#ff7070">Liverpool · MF</span></div>
        <div class="yc-reason">Liverpool's midfield will commit tactical fouls to stop PSG's counter-attacks in the first half. Mac Allister is Liverpool's most aggressive ball-winner and will stretch to halt PSG's fast breaks when Liverpool push high. One impulsive swipe at Kvaratskhelia = yellow in a heartbeat from Mariani.</div>
      </div><div class="yc-risk risk-m">MED</div></div>
    </div></div>
  </div>

  <!-- NOTES LIV -->
  <div class="card fw">
    <div class="card-hd"><div class="hd-dot" style="background:#60a5fa"></div><div class="hd-title">Analytical Notes — Liverpool vs PSG</div></div>
    <div class="card-body">
      <div class="note"><strong>Corners (9–13–18) — Highest of Any Match This Weekend:</strong> Liverpool avg 6.7 corners/game, PSG 5.3 away. Combined ~12 baseline. But this is a UCL knockout second-leg where Liverpool need goals — they'll camp in PSG's half, generating corners relentlessly. Leg 1 had only 4 total corners (3 PSG, 1 Liverpool). Anfield second legs traditionally produce 12–16 corners when Liverpool need to overturn a deficit. Over 9.5 corners has hit in all 4 recent H2H meetings. The high end of 18 accounts for a late desperate Liverpool push when needing a third goal.</div>
      <div class="note"><strong>Total Shots (22–30–42) — Also Highest of Weekend:</strong> Liverpool will throw everything forward from kick-off. PSG avg 18.3 shots/game; Liverpool avg 17.7 at home. Combined baseline ~36, but PSG will adopt a more conservative shape protecting their aggregate lead — potentially limiting their shot count to 6-10. Liverpool alone could have 18-22 shots. The high end of 42 represents a fully open game if Liverpool score early and PSG need to respond.</div>
      <div class="note"><strong>Tackles (26–36–50):</strong> Liverpool desperately winning the ball back vs PSG's composure in possession — this is a tackle-generating scenario. PSG averaged 8.9 shots against in their away UCL games, suggesting they defend compactly. Liverpool will press the PSG backline aggressively. High tackles from both teams in a frenetic Anfield atmosphere. Second-leg UCL games historically produce 15-20% more tackles than first legs.</div>
      <div class="note"><strong>Offsides (3–7–13):</strong> Highest offside projection of all four second legs this week. Liverpool need to run beyond the PSG defensive line repeatedly — Ekitiké and Wirtz will trigger offside traps constantly. Marquinhos and Pacho play a high line in the first half. PSG on the counter will also probe behind Liverpool's pressing line. 7-13 offsides is realistic for a match with this much attacking urgency.</div>
    </div>
  </div>

</div>
<div class="sec-div"><div class="sec-div-in">⭐ Match 2 · UCL QF ⭐</div></div>

<!-- ══════════════════════════════════════
     MATCH 2 — ATLÉTICO MADRID vs BARCELONA
══════════════════════════════════════ -->
</div>

<!-- Tie Status Banner -->
<div class="tie-banner tb-atm" id="atm-bar">
  <div class="tb-icon">🔥</div>
  <div class="tb-text">
    <strong>TIE STATUS — Atlético lead 2–0 on aggregate.</strong> First leg: Barcelona 0–2 Atlético (Álvarez 45'+1, Sørloth 70'). Cubarsi (red card) is suspended. <strong>6th meeting between these teams in just 10 days</strong> across La Liga and UCL. Barcelona need to win by 2+ goals in normal time. Atlético can afford a 1-goal defeat. <span class="agg" style="color:#ff8c42">AGG: ATM 2–0</span>
  </div>
</div>

<div class="match-hero mh-atm">
  <div class="mh-glow"></div>
  <div class="hero-inner">
    <div class="h-team">
      <div class="badge-ring">
        <img src="https://upload.wikimedia.org/wikipedia/en/thumb/f/f4/Atletico_Madrid_2017_logo.svg/120px-Atletico_Madrid_2017_logo.svg.png" alt="Atletico Madrid">
      </div>
      <div class="h-name">Atlético Madrid</div>
      <div class="h-pos">4th La Liga · 2–0 up · Metropolitano fortress</div>
    </div>
    <div class="vs-col">
      <div class="vs-txt">VS</div>
      <div class="ko-tag">9pm CET</div>
      <div class="venue-txt">Metropolitano · Madrid, Spain<br>Ref: Clement Turpin (FRA)</div>
    </div>
    <div class="h-team">
      <div class="badge-ring" style="animation-delay:.14s">
        <img src="https://upload.wikimedia.org/wikipedia/en/thumb/4/47/FC_Barcelona_%28crest%29.svg/120px-FC_Barcelona_%28crest%29.svg.png" alt="Barcelona">
      </div>
      <div class="h-name">FC Barcelona</div>
      <div class="h-pos">La Liga Leaders · No Cubarsi/Raphinha · Need 2 goals</div>
    </div>
  </div>
</div>

<div class="page">
<div class="dg">

  <!-- SCORE PREDICTION -->
  <div class="score-box fw">
    <div class="sb-title">📊 Score Prediction — Atlético Madrid vs Barcelona</div>
    <div class="scores-row">
      <div class="sc">
        <div class="sc-lbl">Half-Time</div>
        <div class="sc-val" style="color:#60a5fa">0 – 1</div>
        <div class="sc-prob">Barcelona · ~34% probability</div>
      </div>
      <div class="sc sc-best">
        <div class="sc-lbl">Full-Time Best Pick</div>
        <div class="sc-val" style="color:#ff8c42">1 – 2</div>
        <div class="sc-prob">Atlético progress 3–2 agg · ~24%</div>
      </div>
      <div class="sc" style="border-color:rgba(0,82,147,.4)">
        <div class="sc-lbl">Barcelona dream</div>
        <div class="sc-val" style="color:#60a5fa">0 – 2</div>
        <div class="sc-prob">AET/Pens possible · ~19%</div>
      </div>
    </div>
    <div class="sb-notes">
      <strong>Why 1–2 Barcelona / Atlético progress:</strong> Barcelona have won 5 of their last 6 at the Metropolitano. They beat Atlético 2-1 in La Liga just 10 days ago at this very ground. However, Atlético have home advantage in a tie they lead, Cubarsi (key CB) is absent, Raphinha (key creative outlet) is injured, and Simeone is a master of protecting leads on European nights. The Metropolitano on a UCL night is one of football's most hostile atmospheres. Barcelona will attack relentlessly and likely score — but Atlético's counter-attacking threat (Álvarez, Sorloth, Griezmann) means a PSG-style defensive masterclass is unrealistic. <strong>Barcelona winning the second leg 2-1 is the most likely outcome</strong>, but Atlético advancing 3-2 on aggregate is the weighted prediction.
    </div>
  </div>

  <!-- CONTEXT -->
  <div class="card fw">
    <div class="card-hd">
      <div class="hd-dot" style="background:var(--md)"></div>
      <div class="hd-title">Context — Second Leg Stakes</div>
      <div class="hd-tag" style="color:var(--md);border-color:rgba(247,201,72,.28);background:var(--ucl-gs)">UCL QF 2nd Leg · Cubarsi Suspended</div>
    </div>
    <div class="card-body">
      <div class="callout">
        This is the <strong>6th meeting between these teams in 10 days</strong> — truly extraordinary familiarity. Barcelona won La Liga matches against Atlético on Apr 4 (2-1 away at Metropolitano) and Apr 11 (4-1 vs Espanyol at Camp Nou — Yamal 1G 2A). Atlético's win in the first leg at Camp Nou was their <strong>first in 20 years</strong> there. Barcelona come in with extreme confidence despite the deficit. Key absences for Barcelona: <strong>Cubarsi</strong> (suspension — key defensive organiser), <strong>Raphinha</strong> (hamstring — creative leader), Christensen (ACL). Frenkie de Jong expected to return. Atlético: Hancko and Barrios doubtful, Giménez doubtful. Referee Turpin is known for letting the game flow — expect a physically intense, emotionally charged battle with Simeone working his touchline magic.
      </div>
    </div>
  </div>

  <!-- FORM -->
  <div class="card fw">
    <div class="card-hd">
      <div class="hd-dot" style="background:var(--atm-r)"></div>
      <div class="hd-title">Last 5 Matches — All Competitions</div>
    </div>
    <div class="card-body">
      <div class="form-cols">
        <div class="fcol">
          <div class="team-lab lab-atm"><img class="tl-img" src="https://upload.wikimedia.org/wikipedia/en/thumb/f/f4/Atletico_Madrid_2017_logo.svg/120px-Atletico_Madrid_2017_logo.svg.png" alt="">Atlético</div>
          <div class="match-list">
            <div class="mr"><div class="rd W"></div><div class="ms">2–0</div><div class="mo">Barcelona (Leg 1)</div><div class="mc">UCL QF <span class="ucl-pill">away win</span></div></div>
            <div class="mr"><div class="rd L"></div><div class="ms">1–2</div><div class="mo">Barcelona</div><div class="mc">La Liga · Away</div></div>
            <div class="mr"><div class="rd W"></div><div class="ms">7–5</div><div class="mo">Tottenham (agg)</div><div class="mc">UCL R16</div></div>
            <div class="mr"><div class="rd W"></div><div class="ms">2–1</div><div class="mo">Rashford scored</div><div class="mc">La Liga · Home</div></div>
            <div class="mr"><div class="rd D"></div><div class="ms">0–0</div><div class="mo">La Liga mid-table</div><div class="mc">La Liga</div></div>
          </div>
        </div>
        <div class="fcol">
          <div class="team-lab lab-bar"><img class="tl-img" src="https://upload.wikimedia.org/wikipedia/en/thumb/4/47/FC_Barcelona_%28crest%29.svg/120px-FC_Barcelona_%28crest%29.svg.png" alt="">Barcelona</div>
          <div class="match-list">
            <div class="mr"><div class="rd W"></div><div class="ms">4–1</div><div class="mo">Espanyol</div><div class="mc">La Liga <span class="ucl-pill">Yamal 1G2A</span></div></div>
            <div class="mr"><div class="rd L"></div><div class="ms">0–2</div><div class="mo">Atlético (Leg 1)</div><div class="mc">UCL QF <span class="ucl-pill">Cubarsi red</span></div></div>
            <div class="mr"><div class="rd W"></div><div class="ms">2–1</div><div class="mo">Atlético</div><div class="mc">La Liga · Away</div></div>
            <div class="mr"><div class="rd W"></div><div class="ms">8–3</div><div class="mo">Newcastle (agg)</div><div class="mc">UCL R16</div></div>
            <div class="mr"><div class="rd W"></div><div class="ms">2–0</div><div class="mo">La Liga</div><div class="mc">La Liga · Home</div></div>
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
      <div class="hd-title">Season Averages — UCL 2025/26 &amp; La Liga</div>
    </div>
    <div class="card-body">
      <div class="avg-pair">
        <div class="a-grp">
          <div class="a-lbl" style="color:#ff8c42">Atlético Madrid</div>
          <div class="avg-g">
            <div class="ac"><div class="val">13.1</div><div class="lbl">Shots</div></div>
            <div class="ac"><div class="val">4.8</div><div class="lbl">SOT</div></div>
            <div class="ac"><div class="val">5.2</div><div class="lbl">Corners</div></div>
            <div class="ac"><div class="val">13.4</div><div class="lbl">Fouls</div></div>
          </div>
        </div>
        <div class="a-grp">
          <div class="a-lbl" style="color:#60a5fa">Barcelona</div>
          <div class="avg-g">
            <div class="ac"><div class="val">17.4</div><div class="lbl">Shots</div></div>
            <div class="ac"><div class="val">6.3</div><div class="lbl">SOT</div></div>
            <div class="ac"><div class="val">6.8</div><div class="lbl">Corners</div></div>
            <div class="ac"><div class="val">10.6</div><div class="lbl">Fouls</div></div>
          </div>
          <p style="font-size:10px;color:var(--muted);margin-top:6px;">Barcelona beat Atlético 4x in last 5 meetings. La Liga leaders by 9pts. Won 5 of last 6 at Metropolitano. Rashford out on loan from Man Utd.</p>
        </div>
      </div>
    </div>
  </div>

  <!-- H2H ATM/BAR -->
  <div class="card fw">
    <div class="card-hd">
      <div class="hd-dot" style="background:var(--hic)"></div>
      <div class="hd-title">H2H — Last 5 Meetings (This Season Heavily Weighted)</div>
    </div>
    <div class="card-body">
      <div class="h2h-bar">
        <div class="hs"><div class="hn" style="color:#ff8c42">1</div><div class="hl">Atlético</div></div>
        <div class="hdv"></div>
        <div class="hs"><div class="hn" style="color:var(--md)">0</div><div class="hl">Draws</div></div>
        <div class="hdv"></div>
        <div class="hs"><div class="hn" style="color:#60a5fa">4</div><div class="hl">Barcelona</div></div>
        <div class="hdv"></div>
        <div class="hs"><div class="hn">3.4</div><div class="hl">Avg Goals</div></div>
      </div>
      <p style="font-size:10.5px;color:var(--muted);margin-top:8px;margin-bottom:8px;">Both teams have played each other <strong>5 times already this season</strong> — extraordinary tactical familiarity. Barcelona won the last 4. Atlético's Camp Nou win was their first there in 20 years.</p>
      <div class="h2h-rows">
        <div class="h2h-r"><div class="rh">Barcelona</div><div class="rs">0–2</div><div class="ra">Atlético</div><div class="rsub">UCL QF Leg 1 · Camp Nou · Apr 8, 2026</div></div>
        <div class="h2h-r"><div class="rh">Atlético</div><div class="rs">1–2</div><div class="ra">Barcelona</div><div class="rsub">La Liga · Metropolitano · Apr 4, 2026</div></div>
        <div class="h2h-r"><div class="rh">Barcelona</div><div class="rs">4–3</div><div class="ra">Atlético</div><div class="rsub">Copa del Rey · (over 2 legs) · Feb 2026</div></div>
        <div class="h2h-r"><div class="rh">Barcelona</div><div class="rs">3–1</div><div class="ra">Atlético</div><div class="rsub">La Liga · Camp Nou · Dec 2025</div></div>
        <div class="h2h-r"><div class="rh">Atlético</div><div class="rs">2–0</div><div class="ra">Barcelona</div><div class="rsub">Copa del Rey · Metropolitano · Jan 2026</div></div>
      </div>
    </div>
  </div>

  <!-- PREDICTIONS ATM -->
  <div class="card fw" id="pred-atm">
    <div class="card-hd">
      <div class="hd-dot" style="background:var(--lo)"></div>
      <div class="hd-title">📊 Weighted Stat Predictions — Atlético vs Barcelona (2nd Leg)</div>
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
          <tr><td class="cmc">Corners</td>        <td><span class="lv">8</span></td><td><span class="mv">12</span></td><td><span class="hv">18</span></td><td><div class="bw"><div class="bf bf-atm" data-pct="76"></div></div></td></tr>
          <tr><td class="cmc">Total Shots</td>    <td><span class="lv">22</span></td><td><span class="mv">30</span></td><td><span class="hv">44</span></td><td><div class="bw"><div class="bf bf-atm" data-pct="86"></div></div></td></tr>
          <tr><td class="cmc">Shots on Target</td><td><span class="lv">8</span></td><td><span class="mv">12</span></td><td><span class="hv">19</span></td><td><div class="bw"><div class="bf bf-atm" data-pct="78"></div></div></td></tr>
          <tr><td class="cmc">Fouls</td>          <td><span class="lv">22</span></td><td><span class="mv">30</span></td><td><span class="hv">42</span></td><td><div class="bw"><div class="bf bf-atm" data-pct="88"></div></div></td></tr>
          <tr><td class="cmc">Throw-ins</td>      <td><span class="lv">36</span></td><td><span class="mv">52</span></td><td><span class="hv">68</span></td><td><div class="bw"><div class="bf bf-atm" data-pct="86"></div></div></td></tr>
          <tr><td class="cmc">Goal Kicks</td>     <td><span class="lv">16</span></td><td><span class="mv">26</span></td><td><span class="hv">38</span></td><td><div class="bw"><div class="bf bf-atm" data-pct="78"></div></div></td></tr>
          <tr><td class="cmc">Tackles</td>        <td><span class="lv">28</span></td><td><span class="mv">40</span></td><td><span class="hv">58</span></td><td><div class="bw"><div class="bf bf-atm" data-pct="94"></div></div></td></tr>
          <tr><td class="cmc">Offsides</td>       <td><span class="lv">4</span></td><td><span class="mv">8</span></td><td><span class="hv">14</span></td><td><div class="bw"><div class="bf bf-atm" data-pct="66"></div></div></td></tr>
        </tbody>
      </table></div>
    </div>
  </div>

  <!-- YELLOW CARDS ATM/BAR -->
  <div class="card fw">
    <div class="card-hd">
      <div class="hd-dot" style="background:#ffe033"></div>
      <div class="hd-title">🟨 Yellow Card Risk Players — Atlético vs Barcelona</div>
      <div class="hd-tag" style="color:var(--md);border-color:rgba(247,201,72,.28);background:rgba(247,201,72,.07)">Turpin · 11 players on semi-final ban warning</div>
    </div>
    <div class="card-body"><div class="yc-grid">
      <div class="yc-row"><div class="yc-icon">🟨</div><div class="yc-info">
        <div class="yc-name">Koke <span class="yc-club" style="color:#ff8c42">Atlético · MF</span></div>
        <div class="yc-reason">The Atlético captain committed 4 fouls on Yamal and Pedri in the first leg — was lucky to stay on the pitch. Against a desperate Barcelona attack, Koke will again foul repeatedly to protect Atlético's aggregate advantage. He is the archetype of a tactical fouling midfielder. In the first leg he avoided a second yellow only through referee restraint.</div>
      </div><div class="yc-risk risk-h">HIGH</div></div>

      <div class="yc-row"><div class="yc-icon">🟨</div><div class="yc-info">
        <div class="yc-name">Pedri <span class="yc-club" style="color:#60a5fa">Barcelona · MF</span></div>
        <div class="yc-reason">Already on a yellow card from the first leg — one more booking means a semi-final ban. Pedri will be under intense pressure to avoid a booking while being the creative heartbeat of Barcelona's comeback bid. Against Atlético's physical midfield press, Pedri will also foul out of desperation and commit reactions that attract Turpin's attention.</div>
      </div><div class="yc-risk risk-h">HIGH</div></div>

      <div class="yc-row"><div class="yc-icon">🟨</div><div class="yc-info">
        <div class="yc-name">Giuliano Simeone <span class="yc-club" style="color:#ff8c42">Atlético · FW</span></div>
        <div class="yc-reason">The manager's son will be running aggressively at Barcelona's makeshift defence (without Cubarsi). His direct style draws physical responses. If he's fouled and reacts aggressively, or if he dives to win a free kick in a scenario where it's borderline — that draws cards both ways. Also on a booking warning for the semi-final.</div>
      </div><div class="yc-risk risk-h">HIGH</div></div>

      <div class="yc-row"><div class="yc-icon">🟨</div><div class="yc-info">
        <div class="yc-name">Marcos Llorente <span class="yc-club" style="color:#ff8c42">Atlético · MF</span></div>
        <div class="yc-reason">On a booking warning for the semi-final. With Barrios out injured, Llorente is the driving midfield force for Atlético. He'll be tasked with stopping Barcelona's creativity in the midfield transition. Against Yamal and Fermin López, a stretched challenge is almost inevitable.</div>
      </div><div class="yc-risk risk-m">MED</div></div>

      <div class="yc-row"><div class="yc-icon">🟨</div><div class="yc-info">
        <div class="yc-name">Fermín López <span class="yc-club" style="color:#60a5fa">Barcelona · MF</span></div>
        <div class="yc-reason">With Gavi and de Jong both under scrutiny, Fermin brings the aggression Barcelona needs. Will compete physically against Llorente and Koke. In his last outing vs Atletico in La Liga, Fermin received a booking. The frustration of needing 2 goals at the Metropolitano — with the crowd against them — pushes younger players towards impulsive challenges.</div>
      </div><div class="yc-risk risk-m">MED</div></div>
    </div></div>
  </div>

  <!-- NOTES ATM -->
  <div class="card fw">
    <div class="card-hd"><div class="hd-dot" style="background:#60a5fa"></div><div class="hd-title">Analytical Notes — Atlético Madrid vs Barcelona</div></div>
    <div class="card-body">
      <div class="note"><strong>Tackles (28–40–58) — Highest Combined Projection of Both Games:</strong> The sixth meeting between these teams in 10 days means maximum tactical fouling — both teams know each other inside out. Atlético avg 13.4 fouls/game + Barcelona 10.6 = 24 combined baseline for fouls. But the UCL second-leg pressure, Barcelona's desperation to score 2 goals, and Atlético's determination to defend their lead in a cauldron atmosphere pushes tackles to elite-level intensity. The H2H this season has averaged 25+ fouls in every meeting.</div>
      <div class="note"><strong>Fouls (22–30–42) — Highest Foul Projection of Both Games:</strong> Atlético under Simeone commit more tactical fouls per UCL game than almost any other team. The first leg produced 11 fouls and a sending off — but that was at Camp Nou. At the Metropolitano in a UCL knockout night, Atlético's pressing and foul-committing will be at maximum intensity. Barcelona will respond with frustration fouls. First leg had 11 fouls — 2nd leg should significantly exceed that. Koke alone could generate 4-6 fouls. High end of 42 if Barcelona grow desperate in the second half.</div>
      <div class="note"><strong>Shots on Target (8–12–19):</strong> Barcelona avg 6.3 SOT/game; Atlético 4.8. Combined baseline ~11.1. Barcelona will be in all-out attacking mode — they could have 8-12 shots on target alone needing two goals. Atlético on the counter (Álvarez, Griezmann, Lookman) are clinical — if they break twice on goal, both will likely test Joan Garcia. The xG data from the first leg showed Barcelona actually had 1.21 xG vs Atlético's 0.45 — reflecting Barcelona's superior attacking quality.</div>
      <div class="note"><strong>Corners (8–12–18):</strong> Barcelona avg 6.8 corners/game; Atlético 5.2. Combined ~12 baseline. Barcelona will be in Atlético's box repeatedly — Atlético's high block will concede corners constantly as Barcelona try to play through them. Last 5 H2H meetings have all had 9+ corners. In the Copa del Rey tie (2 legs) both games went over 11. High end of 18 is within reach if Barcelona dominate territory and Atlético defend their box resolutely.</div>
      <div class="note"><strong>Goal Kicks (16–26–38) — Highest of All Four Second-Leg Games:</strong> Atlético's defensive strategy will involve their goalkeeper (likely Musso) distributing long to Álvarez and Sorloth repeatedly. Barcelona, pressing high and conceding goal kicks as Atlético's shape doesn't play out, will generate this number from Atlético alone. Barcelona's goalkeeper (Joan Garcia) will also restart frequently when Atlético counter-press their build-up. The combination of two teams with distinct styles (one builds short, one goes long) inflates goal kicks significantly.</div>
    </div>
  </div>

</div><!-- /dg -->
</div><!-- /page -->

    <footer>
        <strong>Team Bilbo Statistical Analysis</strong><br>Predictions are statistical estimates based on historical
        profiles and Champions League knockout dynamics. <strong>Not financial advice.</strong><br> · April 2026 ·
    </footer>

<script>
(function(){
  'use strict';

  /* Card reveal */
  var cards = document.querySelectorAll('.card');
  if('IntersectionObserver' in window){
    var obs = new IntersectionObserver(function(e){
      e.forEach(function(entry){ if(entry.isIntersecting){ entry.target.classList.add('vis'); obs.unobserve(entry.target); } });
    },{threshold:0.06});
    cards.forEach(function(c){ obs.observe(c); });
  } else { cards.forEach(function(c){ c.classList.add('vis'); }); }

  /* Bar animations */
  ['pred-liv','pred-atm'].forEach(function(id){
    var el = document.getElementById(id);
    if(!el) return;
    var fired = false;
    var bObs = new IntersectionObserver(function(entries){
      entries.forEach(function(e){
        if(e.isIntersecting && !fired){
          fired = true;
          setTimeout(function(){
            el.querySelectorAll('.bar-fill[data-pct], .bf[data-pct]').forEach(function(b){
              b.style.width = b.getAttribute('data-pct') + '%';
            });
          }, 200);
          bObs.unobserve(e.target);
        }
      });
    },{threshold:0.2});
    bObs.observe(el);
  });

  /* Count-up */
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
            var cur = 0, dur = 850, step = num/(dur/16);
            var t = setInterval(function(){
              cur += step;
              if(cur >= num){ cur = num; clearInterval(t); }
              var d = (String(num).indexOf('.') !== -1) ? cur.toFixed(1) : Math.round(cur);
              v.textContent = d + (isPct ? '%' : '');
            },16);
          }
        }
        acObs.unobserve(e.target);
      }
    });
  },{threshold:0.7});
  document.querySelectorAll('.ac').forEach(function(el){ acObs.observe(el); });

})();
</script>
