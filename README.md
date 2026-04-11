<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>PL Stats Predictor | April 11 2026 — 4 Matches</title>
<link rel="preconnect" href="https://fonts.googleapis.com">
<link href="https://fonts.googleapis.com/css2?family=Oswald:wght@400;500;600;700&family=Mulish:wght@300;400;500;600;700;800&display=swap" rel="stylesheet">
<style>
/* ═══════════════════════════════════
   TOKENS
═══════════════════════════════════ */
:root{
  --bg:        #060709;
  --bg-2:      #0c0e14;
  --bg-3:      #12151e;
  --bg-4:      #191d2c;
  --border:    rgba(255,255,255,0.07);
  --border-m:  rgba(255,255,255,0.13);
  --text:      #c5cde0;
  --muted:     #4e5672;
  --hi:        #8a93b0;
  /* PL purple/lion */
  --pl:        #3b0071;
  --pl-l:      #6c30e4;
  --pl-g:      #ffffff;
  /* match accent colours */
  --ars:       #ef0107; --bou:#c8102e;
  --bre:       #e30613; --eve:#003399;
  --bur:       #6c1d45; --bri:#0057b8;
  --liv:       #c8102e; --ful:#cc0000;
  /* stat palette */
  --lo:        #10d9a0;
  --md:        #f5ba32;
  --hi-c:      #f55c2a;
  --card-y:    #ffe033;
  --danger:    #ef4444;
  --warn:      #f59e0b;
}

*,*::before,*::after{margin:0;padding:0;box-sizing:border-box;}
html{scroll-behavior:smooth;}
body{
  font-family:'Mulish',sans-serif;
  background:var(--bg);
  color:var(--text);
  min-height:100vh;
  font-size:14px;
  line-height:1.55;
  -webkit-font-smoothing:antialiased;
}

/* ═══════════════════════════════════
   ANIMATIONS
═══════════════════════════════════ */
@keyframes fadeUp{from{opacity:0;transform:translateY(20px);}to{opacity:1;transform:translateY(0);}}
@keyframes scalePop{from{transform:scale(0.75);opacity:0;}to{transform:scale(1);opacity:1;}}
@keyframes pulse{0%,100%{opacity:1;}50%{opacity:.5;}}

/* ═══════════════════════════════════
   SITE HEADER
═══════════════════════════════════ */
.site-header{
  background:linear-gradient(175deg,#07070f 0%,#0f0a18 55%,#07070f 100%);
  border-bottom:2px solid rgba(108,48,228,.45);
  padding:18px 16px 16px;
  text-align:center;
  position:relative;overflow:hidden;
}
.site-header::before{
  content:'';position:absolute;inset:0;
  background:radial-gradient(ellipse 100% 300% at 50% -10%,rgba(108,48,228,.1),transparent 65%);
  pointer-events:none;
}
.pl-badge{
  display:inline-flex;align-items:center;gap:7px;
  font-family:'Oswald',sans-serif;font-size:10px;font-weight:600;
  letter-spacing:2.5px;text-transform:uppercase;
  color:var(--pl-l);background:rgba(108,48,228,.08);
  border:1px solid rgba(108,48,228,.3);padding:3px 12px;border-radius:20px;
  margin-bottom:10px;
}
.site-header h1{
  font-family:'Oswald',sans-serif;font-size:24px;font-weight:700;
  letter-spacing:.5px;color:#fff;line-height:1.1;text-transform:uppercase;
}
.site-header .sub{font-size:11.5px;color:var(--muted);margin-top:5px;}
.ko-strip{
  display:flex;flex-wrap:wrap;justify-content:center;gap:8px;margin-top:12px;
}
.ko-pill{
  display:inline-flex;align-items:center;gap:5px;
  font-family:'Oswald',sans-serif;font-size:9.5px;font-weight:600;
  letter-spacing:1px;text-transform:uppercase;
  padding:4px 11px;border-radius:20px;border:1px solid rgba(255,255,255,.1);
  color:var(--text);background:rgba(255,255,255,.04);text-decoration:none;
  transition:border-color .2s,background .2s;
}
.ko-pill:hover{border-color:rgba(108,48,228,.5);background:rgba(108,48,228,.08);}

/* ═══════════════════════════════════
   FATIGUE BANNER
═══════════════════════════════════ */
.f-banner{
  background:linear-gradient(135deg,rgba(239,68,68,.1),rgba(239,68,68,.04));
  border:1px solid rgba(239,68,68,.28);border-radius:9px;
  padding:11px 14px;display:flex;align-items:flex-start;gap:9px;margin:14px 0;
}
.f-icon{font-size:18px;flex-shrink:0;animation:pulse 2s infinite;}
.f-text{font-size:12px;color:#fca5a5;line-height:1.6;}
.f-text strong{color:var(--danger);font-weight:800;}

/* ═══════════════════════════════════
   MATCH HERO
═══════════════════════════════════ */
.match-hero{
  padding:22px 16px 18px;
  border-bottom:1px solid var(--border-m);
  position:relative;overflow:hidden;
}
.mh-ars{background:linear-gradient(135deg,rgba(239,1,7,.14) 0%,var(--bg-2) 45%,rgba(200,16,46,.1) 100%);}
.mh-bre{background:linear-gradient(135deg,rgba(227,6,19,.14) 0%,var(--bg-2) 45%,rgba(0,51,153,.12) 100%);}
.mh-bur{background:linear-gradient(135deg,rgba(108,29,69,.16) 0%,var(--bg-2) 45%,rgba(0,87,184,.12) 100%);}
.mh-liv{background:linear-gradient(135deg,rgba(200,16,46,.14) 0%,var(--bg-2) 45%,rgba(204,0,0,.1) 100%);}
.mh-glow{position:absolute;inset:0;background:radial-gradient(ellipse 70% 100% at 50% 50%,rgba(108,48,228,.04),transparent 70%);pointer-events:none;}

.hero-inner{
  max-width:520px;margin:0 auto;
  display:flex;align-items:center;justify-content:space-between;gap:10px;
}
.h-team{display:flex;flex-direction:column;align-items:center;gap:7px;flex:1;}
.badge-ring{
  width:68px;height:68px;border-radius:50%;
  border:1.5px solid var(--border-m);background:rgba(255,255,255,.04);
  display:flex;align-items:center;justify-content:center;overflow:hidden;
  filter:drop-shadow(0 4px 16px rgba(0,0,0,.65));
  animation:scalePop .5s cubic-bezier(.34,1.56,.64,1) both;
  transition:transform .3s;flex-shrink:0;
}
.badge-ring:hover{transform:scale(1.08);}
.badge-ring img{width:50px;height:50px;object-fit:contain;}
.h-name{
  font-family:'Oswald',sans-serif;font-size:12.5px;font-weight:600;
  letter-spacing:.3px;text-transform:uppercase;text-align:center;color:#fff;line-height:1.2;
}
.h-pos{font-size:9px;color:var(--muted);text-transform:uppercase;letter-spacing:.5px;}
.vs-col{display:flex;flex-direction:column;align-items:center;gap:4px;flex-shrink:0;}
.vs-txt{font-family:'Oswald',sans-serif;font-size:22px;font-weight:700;color:rgba(255,255,255,.1);letter-spacing:3px;}
.ko-tag{
  font-family:'Oswald',sans-serif;font-size:9px;font-weight:700;letter-spacing:1.5px;
  color:var(--md);background:rgba(245,186,50,.1);
  border:1px solid rgba(245,186,50,.25);padding:2px 7px;border-radius:4px;
}
.venue-txt{font-size:9px;color:var(--muted);text-align:center;line-height:1.5;}

/* ═══════════════════════════════════
   PAGE & GRID
═══════════════════════════════════ */
.page{max-width:700px;margin:0 auto;padding:16px 14px 52px;}

/* card */
.card{
  background:var(--bg-2);border:1px solid var(--border);
  border-radius:10px;overflow:hidden;margin-bottom:12px;
  transition:border-color .3s;opacity:0;transform:translateY(14px);
}
.card.visible{opacity:1;transform:translateY(0);transition:opacity .5s ease,transform .5s ease,border-color .3s;}
.card:hover{border-color:var(--border-m);}
.card-hd{
  padding:11px 16px 9px;border-bottom:1px solid var(--border);
  display:flex;align-items:center;gap:7px;
}
.hd-dot{width:5px;height:5px;border-radius:50%;flex-shrink:0;}
.hd-title{
  font-family:'Oswald',sans-serif;font-size:10px;font-weight:600;
  letter-spacing:2px;text-transform:uppercase;color:var(--muted);flex:1;
}
.hd-tag{
  font-size:8.5px;font-weight:800;letter-spacing:.8px;text-transform:uppercase;
  padding:2px 7px;border-radius:3px;border:1px solid;
}
.card-body{padding:13px 16px;}

/* callout */
.callout{
  background:rgba(255,255,255,.02);border:1px solid var(--border-m);
  border-radius:8px;padding:11px 13px;font-size:12px;line-height:1.7;color:var(--hi);
}
.callout strong{color:var(--md);font-weight:800;}

/* form cols */
.form-cols{display:flex;flex-direction:column;gap:11px;}
.fcol{}
.team-lab{
  display:inline-flex;align-items:center;gap:5px;
  font-size:9px;font-weight:800;letter-spacing:1px;text-transform:uppercase;
  padding:2px 7px 2px 4px;border-radius:4px;margin-bottom:7px;border:1px solid;
}
.tl-img{width:13px;height:13px;object-fit:contain;}
/* dynamic label colours per match */
.lab-ars{background:rgba(239,1,7,.1);color:#f07070;border-color:rgba(239,1,7,.25);}
.lab-bou{background:rgba(200,16,46,.1);color:#f07070;border-color:rgba(200,16,46,.25);}
.lab-bre{background:rgba(227,6,19,.1);color:#f07070;border-color:rgba(227,6,19,.25);}
.lab-eve{background:rgba(0,51,153,.1);color:#7aafff;border-color:rgba(0,51,153,.25);}
.lab-bur{background:rgba(108,29,69,.12);color:#d070a0;border-color:rgba(108,29,69,.28);}
.lab-bri{background:rgba(0,87,184,.1);color:#7aafff;border-color:rgba(0,87,184,.25);}
.lab-liv{background:rgba(200,16,46,.1);color:#f07070;border-color:rgba(200,16,46,.25);}
.lab-ful{background:rgba(204,0,0,.1);color:#f07070;border-color:rgba(204,0,0,.25);}

.match-list{display:flex;flex-direction:column;gap:3px;}
.mr{
  display:grid;grid-template-columns:6px 42px 1fr auto;
  align-items:center;gap:7px;
  background:var(--bg-3);border:1px solid var(--border);
  border-radius:6px;padding:6px 9px;transition:background .2s;
}
.mr:hover{background:var(--bg-4);}
.rd{width:6px;height:6px;border-radius:50%;}
.rd.W{background:var(--lo);box-shadow:0 0 5px rgba(16,217,160,.4);}
.rd.D{background:var(--md);}
.rd.L{background:var(--hi-c);box-shadow:0 0 5px rgba(245,92,42,.4);}
.ms{font-family:'Oswald',sans-serif;font-size:14px;font-weight:600;color:#fff;text-align:center;}
.mo{font-size:11.5px;color:var(--text);font-weight:500;overflow:hidden;text-overflow:ellipsis;white-space:nowrap;}
.mc{font-size:9px;color:var(--muted);text-transform:uppercase;letter-spacing:.3px;text-align:right;white-space:nowrap;}
.ucl-note{font-size:8.5px;color:var(--warn);font-style:italic;}
.f-leg{display:flex;gap:11px;flex-wrap:wrap;margin-top:8px;}
.fl{display:flex;align-items:center;gap:4px;font-size:10px;color:var(--muted);}
.fl-dot{width:6px;height:6px;border-radius:50%;}

/* avg */
.avg-pair{display:flex;flex-direction:column;gap:10px;}
.a-grp{}
.a-lbl{font-family:'Oswald',sans-serif;font-size:9px;font-weight:700;letter-spacing:1.2px;text-transform:uppercase;margin-bottom:6px;}
.avg-g{display:grid;grid-template-columns:repeat(4,1fr);gap:4px;}
.ac{
  background:var(--bg-3);border:1px solid var(--border);border-radius:7px;
  padding:8px 4px 6px;text-align:center;
  transition:border-color .2s,transform .2s;
}
.ac:hover{border-color:var(--border-m);transform:translateY(-1px);}
.ac .val{font-family:'Oswald',sans-serif;font-size:18px;font-weight:700;color:#fff;line-height:1;}
.ac .lbl{font-size:8px;color:var(--muted);margin-top:2px;text-transform:uppercase;letter-spacing:.4px;line-height:1.3;}

/* h2h */
.h2h-bar{
  background:var(--bg-3);border:1px solid var(--border);border-radius:7px;
  padding:11px 9px;display:flex;align-items:center;justify-content:space-between;gap:4px;
}
.hs{text-align:center;flex:1;}
.hn{font-family:'Oswald',sans-serif;font-size:26px;font-weight:700;line-height:1;}
.hl{font-size:8.5px;color:var(--muted);text-transform:uppercase;letter-spacing:.6px;margin-top:2px;}
.hdiv{width:1px;height:32px;background:var(--border);flex-shrink:0;}
.h2h-rows{display:flex;flex-direction:column;gap:3px;margin-top:10px;}
.h2h-r{
  display:grid;grid-template-columns:1fr auto 1fr;align-items:center;gap:7px;
  background:var(--bg-4);border:1px solid var(--border);border-radius:6px;padding:6px 9px;
  transition:background .2s;
}
.h2h-r:hover{background:#1e2238;}
.rh{font-size:11.5px;font-weight:600;color:var(--text);text-align:left;white-space:nowrap;overflow:hidden;text-overflow:ellipsis;}
.rs{font-family:'Oswald',sans-serif;font-size:14px;font-weight:700;color:#fff;text-align:center;white-space:nowrap;}
.ra{font-size:11.5px;font-weight:600;color:var(--text);text-align:right;white-space:nowrap;overflow:hidden;text-overflow:ellipsis;}
.rsub{font-size:8.5px;color:var(--muted);text-transform:uppercase;letter-spacing:.3px;grid-column:1/-1;text-align:center;margin-top:-2px;}

/* pred table */
.pred-leg{display:flex;gap:12px;flex-wrap:wrap;margin-bottom:12px;}
.pli{display:flex;align-items:center;gap:5px;font-size:10.5px;color:var(--muted);}
.pld{width:7px;height:7px;border-radius:50%;}
.pw{overflow-x:auto;-webkit-overflow-scrolling:touch;}
.pt{width:100%;border-collapse:collapse;table-layout:fixed;min-width:290px;}
.pt col.cm{width:28%;}
.pt col.cl{width:16%;}
.pt col.cn{width:16%;}
.pt col.ch{width:16%;}
.pt col.cb{width:24%;}
.pt thead th{
  font-family:'Oswald',sans-serif;font-size:9px;font-weight:700;
  letter-spacing:1.5px;text-transform:uppercase;color:var(--muted);
  padding:0 0 8px;text-align:left;white-space:nowrap;overflow:hidden;
}
.pt thead th:not(:first-child){text-align:center;}
.pt thead th.th-m{color:var(--md);}
.pt tbody td{padding:7px 3px;border-bottom:1px solid rgba(255,255,255,.03);vertical-align:middle;overflow:hidden;}
.pt tbody tr:last-child td{border-bottom:none;}
.pt tbody tr{transition:background .2s;}
.pt tbody tr:hover td{background:rgba(255,255,255,.02);}
.pt tbody td.cmc{color:var(--hi);font-size:12px;padding-left:0;font-weight:500;}
.pt tbody td:not(.cmc){text-align:center;}
.lv{font-family:'Oswald',sans-serif;font-size:17px;font-weight:700;color:var(--lo);line-height:1;}
.mv{font-family:'Oswald',sans-serif;font-size:17px;font-weight:700;color:var(--md);line-height:1;}
.hv{font-family:'Oswald',sans-serif;font-size:17px;font-weight:700;color:var(--hi-c);line-height:1;}
.bar-wrap{width:85%;max-width:90px;height:5px;background:rgba(255,255,255,.06);border-radius:3px;overflow:hidden;margin:0 auto;display:block;}
.bar-fill{display:block;height:100%;border-radius:3px;width:0;transition:width 1.2s cubic-bezier(.25,.46,.45,.94);}
.bf-1{background:linear-gradient(90deg,var(--lo),var(--hi-c));}
.bf-2{background:linear-gradient(90deg,#22d3a0,#7c3aed);}
.bf-3{background:linear-gradient(90deg,#22d3a0,#3b82f6);}
.bf-4{background:linear-gradient(90deg,#f59e0b,var(--hi-c));}

/* yellow card */
.yc-grid{display:flex;flex-direction:column;gap:7px;}
.yc-row{
  display:flex;align-items:flex-start;gap:9px;
  background:var(--bg-3);border:1px solid var(--border);border-radius:8px;
  padding:9px 11px;transition:border-color .25s,transform .25s;
}
.yc-row:hover{border-color:rgba(255,224,51,.2);transform:translateX(3px);}
.yc-icon{font-size:16px;flex-shrink:0;margin-top:1px;}
.yc-info{flex:1;min-width:0;}
.yc-name{font-size:12px;font-weight:700;color:#fff;}
.yc-club{font-size:9px;font-family:'Oswald',sans-serif;letter-spacing:.7px;text-transform:uppercase;}
.yc-reason{font-size:11px;color:var(--muted);margin-top:2px;line-height:1.45;}
.yc-risk{
  font-family:'Oswald',sans-serif;font-size:9px;font-weight:700;letter-spacing:1.2px;
  text-transform:uppercase;padding:2px 8px;border-radius:4px;flex-shrink:0;align-self:center;
}
.risk-h{background:rgba(245,92,42,.14);color:var(--hi-c);border:1px solid rgba(245,92,42,.28);}
.risk-m{background:rgba(245,186,50,.1);color:var(--md);border:1px solid rgba(245,186,50,.25);}

/* notes */
.note{margin-bottom:8px;font-size:12px;line-height:1.65;color:var(--hi);}
.note:last-child{margin-bottom:0;}
.note strong{color:var(--md);font-weight:800;}

/* section divider */
.s-div{
  text-align:center;padding:20px 0 10px;position:relative;
  margin:0 0 0;
}
.s-div::before{content:'';position:absolute;left:0;right:0;top:50%;height:1px;background:rgba(108,48,228,.2);}
.s-div-in{
  display:inline-flex;align-items:center;gap:8px;
  background:var(--bg);padding:0 12px;position:relative;
  font-family:'Oswald',sans-serif;font-size:9.5px;font-weight:700;
  letter-spacing:2.5px;text-transform:uppercase;color:var(--pl-l);
}

/* footer */
footer{text-align:center;padding:16px 14px;font-size:11px;color:rgba(78,86,114,.4);border-top:1px solid var(--border);}

/* ═══════════════════════════════════
   TABLET 640+
═══════════════════════════════════ */
@media(min-width:640px){
  body{font-size:15px;}
  .page{max-width:900px;padding:18px 22px 58px;}
  .site-header{padding:24px 22px 20px;}
  .site-header h1{font-size:30px;}
  .match-hero{padding:26px 22px 20px;}
  .hero-inner{max-width:600px;}
  .badge-ring{width:80px;height:80px;}
  .badge-ring img{width:58px;height:58px;}
  .h-name{font-size:14px;}
  .vs-txt{font-size:28px;}
  .card-hd{padding:12px 20px 10px;}
  .card-body{padding:15px 20px;}
  .form-cols{flex-direction:row;gap:14px;}
  .fcol{flex:1;min-width:0;}
  .avg-pair{flex-direction:row;gap:14px;}
  .a-grp{flex:1;}
  .ac .val{font-size:20px;}
  .hn{font-size:30px;}
  .lv,.mv,.hv{font-size:20px;}
  .pt tbody td{padding:8px 4px;}
  .bar-wrap{max-width:105px;height:5px;}
  .callout{font-size:13px;}
  .note{font-size:13px;}
}

/* ═══════════════════════════════════
   DESKTOP 1040+
═══════════════════════════════════ */
@media(min-width:1040px){
  .page{max-width:1380px;padding:26px 40px 68px;}
  .site-header{padding:26px 40px 22px;}
  .site-header h1{font-size:36px;}
  .match-hero{padding:26px 40px 20px;}
  .hero-inner{max-width:660px;}
  .badge-ring{width:88px;height:88px;}
  .badge-ring img{width:64px;height:64px;}
  .dg{display:grid;grid-template-columns:1fr 1fr;gap:18px;align-items:start;}
  .dg .fw{grid-column:1/-1;}
  .card-hd{padding:13px 22px 11px;}
  .card-body{padding:16px 22px;}
  .ac .val{font-size:22px;}
  .lv,.mv,.hv{font-size:21px;}
  .hn{font-size:32px;}
  .bar-wrap{max-width:96px;}
}

/* ═══════════════════════════════════
   WIDE 1360+
═══════════════════════════════════ */
@media(min-width:1360px){
  .page{max-width:1520px;padding:30px 60px 74px;}
  .site-header{padding:28px 60px 22px;}
  .match-hero{padding:28px 60px 22px;}
  .dg{gap:24px;}
}
</style>
</head>
<body>

<!-- ═══ SITE HEADER ═══ -->
<header class="site-header">
  <div class="pl-badge">⚽ Premier League · Matchweek 32 · Saturday 11 April 2026</div>
  <h1>Team Bilbo Premier League Stats Predictor</h1>
  <p class="sub">4-match preview &nbsp;·&nbsp; Last 5 form &nbsp;·&nbsp; Season averages &nbsp;·&nbsp; H2H &nbsp;·&nbsp; Low / Median / High predictions &nbsp;·&nbsp; Yellow card risks</p>
  <nav class="ko-strip">
    <a href="#ars" class="ko-pill">12:30 · Arsenal vs Bournemouth</a>
    <a href="#bre" class="ko-pill">15:00 · Brentford vs Everton</a>
    <a href="#bur" class="ko-pill">15:00 · Burnley vs Brighton</a>
    <a href="#liv" class="ko-pill">17:30 · Liverpool vs Fulham</a>
  </nav>
</header>

<!-- ═══════════════════════════════════════
     MATCH 1 — ARSENAL vs BOURNEMOUTH
═══════════════════════════════════════ -->
<div class="match-hero mh-ars" id="ars">
  <div class="mh-glow"></div>
  <div class="hero-inner">
    <div class="h-team">
      <div class="badge-ring">
        <img src="https://upload.wikimedia.org/wikipedia/en/thumb/5/53/Arsenal_FC.svg/120px-Arsenal_FC.svg.png" alt="Arsenal">
      </div>
      <div class="h-name">Arsenal</div>
      <div class="h-pos">1st · 70 pts · Leaders</div>
    </div>
    <div class="vs-col">
      <div class="vs-txt">VS</div>
      <div class="ko-tag">12:30 BST</div>
      <div class="venue-txt">Emirates Stadium<br>Ref: Michael Oliver</div>
    </div>
    <div class="h-team">
      <div class="badge-ring" style="animation-delay:.12s">
        <img src="https://upload.wikimedia.org/wikipedia/en/thumb/e/e5/AFC_Bournemouth_%282013%29.svg/120px-AFC_Bournemouth_%282013%29.svg.png" alt="Bournemouth">
      </div>
      <div class="h-name">Bournemouth</div>
      <div class="h-pos">13th · 42 pts</div>
    </div>
  </div>
</div>

<div class="page">
<div class="dg">

  <div class="card fw">
    <div class="card-hd"><div class="hd-dot" style="background:var(--md)"></div><div class="hd-title">Context</div><div class="hd-tag" style="color:var(--md);border-color:rgba(245,186,50,.28);background:rgba(245,186,50,.07)">Title Race · UCL Fatigue</div></div>
    <div class="card-body">
      <div class="callout">Arsenal lead by <strong>9 points</strong>, aiming for a 5th straight PL win that would extend the gap to 12 pts. However, they beat Sporting 1–0 in the <strong>UCL QF Leg 1 on Tuesday</strong> — some fatigue in the legs heading into a 12:30 kick-off. Saka and Timber both missed the UCL tie and remain doubts. Bournemouth are the <strong>PL's draw specialists</strong> (15 draws in 31 games) on an <strong>11-game unbeaten run</strong>, their joint-club record. Last 5 PL games: DDDDD — including 0–0 at West Ham, 0–0 at Burnley, 0–0 vs Brentford. Bournemouth have won 2 of their last 3 PL visits to Arsenal.
      </div>
    </div>
  </div>

  <div class="card fw">
    <div class="card-hd"><div class="hd-dot" style="background:var(--ars)"></div><div class="hd-title">Last 5 Matches — All Comps</div></div>
    <div class="card-body">
      <div class="form-cols">
        <div class="fcol">
          <div class="team-lab lab-ars"><img class="tl-img" src="https://upload.wikimedia.org/wikipedia/en/thumb/5/53/Arsenal_FC.svg/120px-Arsenal_FC.svg.png" alt="">Arsenal</div>
          <div class="match-list">
            <div class="mr"><div class="rd W"></div><div class="ms">1–0</div><div class="mo">Sporting CP</div><div class="mc">UCL QF <span class="ucl-note">Tue</span></div></div>
            <div class="mr"><div class="rd L"></div><div class="ms">1–2</div><div class="mo">Southampton</div><div class="mc">FAC · Away</div></div>
            <div class="mr"><div class="rd L"></div><div class="ms">0–2</div><div class="mo">Man City</div><div class="mc">EFL Final</div></div>
            <div class="mr"><div class="rd W"></div><div class="ms">2–0</div><div class="mo">Everton</div><div class="mc">PL · Home</div></div>
            <div class="mr"><div class="rd W"></div><div class="ms">2–0</div><div class="mo">Bayer Leverkusen</div><div class="mc">UCL R16</div></div>
          </div>
        </div>
        <div class="fcol">
          <div class="team-lab lab-bou"><img class="tl-img" src="https://upload.wikimedia.org/wikipedia/en/thumb/e/e5/AFC_Bournemouth_%282013%29.svg/120px-AFC_Bournemouth_%282013%29.svg.png" alt="">Bournemouth</div>
          <div class="match-list">
            <div class="mr"><div class="rd D"></div><div class="ms">0–0</div><div class="mo">Burnley</div><div class="mc">PL · Away</div></div>
            <div class="mr"><div class="rd D"></div><div class="ms">0–0</div><div class="mo">West Ham</div><div class="mc">PL · Away</div></div>
            <div class="mr"><div class="rd D"></div><div class="ms">0–0</div><div class="mo">Brentford</div><div class="mc">PL · Home</div></div>
            <div class="mr"><div class="rd D"></div><div class="ms">2–2</div><div class="mo">Man United</div><div class="mc">PL · Away</div></div>
            <div class="mr"><div class="rd D"></div><div class="ms">1–1</div><div class="mo">Sunderland</div><div class="mc">PL · Home</div></div>
          </div>
        </div>
      </div>
      <div class="f-leg"><div class="fl"><div class="fl-dot" style="background:var(--lo)"></div>Win</div><div class="fl"><div class="fl-dot" style="background:var(--md)"></div>Draw</div><div class="fl"><div class="fl-dot" style="background:var(--hi-c)"></div>Loss</div></div>
    </div>
  </div>

  <div class="card fw">
    <div class="card-hd"><div class="hd-dot" style="background:#a78bfa"></div><div class="hd-title">Season Averages per Match — PL 25/26</div></div>
    <div class="card-body">
      <div class="avg-pair">
        <div class="a-grp">
          <div class="a-lbl" style="color:#f07070">Arsenal</div>
          <div class="avg-g">
            <div class="ac"><div class="val">14.7</div><div class="lbl">Shots</div></div>
            <div class="ac"><div class="val">5.0</div><div class="lbl">SOT</div></div>
            <div class="ac"><div class="val">5.8</div><div class="lbl">Corners</div></div>
            <div class="ac"><div class="val">10.5</div><div class="lbl">Fouls</div></div>
          </div>
        </div>
        <div class="a-grp">
          <div class="a-lbl" style="color:#f07070">Bournemouth</div>
          <div class="avg-g">
            <div class="ac"><div class="val">11.2</div><div class="lbl">Shots</div></div>
            <div class="ac"><div class="val">3.9</div><div class="lbl">SOT</div></div>
            <div class="ac"><div class="val">4.6</div><div class="lbl">Corners</div></div>
            <div class="ac"><div class="val">11.8</div><div class="lbl">Fouls</div></div>
          </div>
        </div>
      </div>
    </div>
  </div>

  <div class="card fw">
    <div class="card-hd"><div class="hd-dot" style="background:var(--hi-c)"></div><div class="hd-title">H2H — Last 5 Meetings</div></div>
    <div class="card-body">
      <div class="h2h-bar">
        <div class="hs"><div class="hn" style="color:#f07070">3</div><div class="hl">Arsenal Wins</div></div>
        <div class="hdiv"></div>
        <div class="hs"><div class="hn" style="color:var(--md)">0</div><div class="hl">Draws</div></div>
        <div class="hdiv"></div>
        <div class="hs"><div class="hn" style="color:#f07070">2</div><div class="hl">Bou Wins</div></div>
        <div class="hdiv"></div>
        <div class="hs"><div class="hn">2.4</div><div class="hl">Avg Goals</div></div>
      </div>
      <div class="h2h-rows">
        <div class="h2h-r"><div class="rh">Bournemouth</div><div class="rs">2–3</div><div class="ra">Arsenal</div><div class="rsub">PL · Jan 2026 (last meeting)</div></div>
        <div class="h2h-r"><div class="rh">Arsenal</div><div class="rs">2–0</div><div class="ra">Bournemouth</div><div class="rsub">PL · Mar 2026</div></div>
        <div class="h2h-r"><div class="rh">Arsenal</div><div class="rs">2–1</div><div class="ra">Bournemouth</div><div class="rsub">PL · Oct 2025</div></div>
        <div class="h2h-r"><div class="rh">Bournemouth</div><div class="rs">2–1</div><div class="ra">Arsenal</div><div class="rsub">PL · Dec 2024</div></div>
        <div class="h2h-r"><div class="rh">Bournemouth</div><div class="rs">1–0</div><div class="ra">Arsenal</div><div class="rsub">PL · Feb 2024</div></div>
      </div>
    </div>
  </div>

  <div class="card fw" id="pred-ars">
    <div class="card-hd"><div class="hd-dot" style="background:var(--lo)"></div><div class="hd-title">Weighted Predictions — Arsenal vs Bournemouth</div></div>
    <div class="card-body">
      <div class="pred-leg"><div class="pli"><div class="pld" style="background:var(--lo)"></div><span style="color:var(--lo);font-weight:700">Low</span></div><div class="pli"><div class="pld" style="background:var(--md)"></div><span style="color:var(--md);font-weight:700">Median</span></div><div class="pli"><div class="pld" style="background:var(--hi-c)"></div><span style="color:var(--hi-c);font-weight:700">High</span></div></div>
      <div class="pw"><table class="pt">
        <colgroup><col class="cm"><col class="cl"><col class="cn"><col class="ch"><col class="cb"></colgroup>
        <thead><tr><th>Metric</th><th style="color:var(--lo)">Low</th><th class="th-m">Median</th><th style="color:var(--hi-c)">High</th><th style="text-align:center;color:var(--muted)">Intensity</th></tr></thead>
        <tbody>
          <tr><td class="cmc">Corners</td><td><span class="lv">7</span></td><td><span class="mv">10</span></td><td><span class="hv">14</span></td><td><div class="bar-wrap"><div class="bar-fill bf-1" data-pct="60"></div></div></td></tr>
          <tr><td class="cmc">Total Shots</td><td><span class="lv">20</span></td><td><span class="mv">26</span></td><td><span class="hv">36</span></td><td><div class="bar-wrap"><div class="bar-fill bf-1" data-pct="72"></div></div></td></tr>
          <tr><td class="cmc">Shots on Target</td><td><span class="lv">6</span></td><td><span class="mv">9</span></td><td><span class="hv">14</span></td><td><div class="bar-wrap"><div class="bar-fill bf-1" data-pct="62"></div></div></td></tr>
          <tr><td class="cmc">Fouls</td><td><span class="lv">16</span></td><td><span class="mv">22</span></td><td><span class="hv">30</span></td><td><div class="bar-wrap"><div class="bar-fill bf-1" data-pct="55"></div></div></td></tr>
          <tr><td class="cmc">Throw-ins</td><td><span class="lv">32</span></td><td><span class="mv">42</span></td><td><span class="hv">54</span></td><td><div class="bar-wrap"><div class="bar-fill bf-1" data-pct="60"></div></div></td></tr>
          <tr><td class="cmc">Goal Kicks</td><td><span class="lv">12</span></td><td><span class="mv">18</span></td><td><span class="hv">26</span></td><td><div class="bar-wrap"><div class="bar-fill bf-1" data-pct="54"></div></div></td></tr>
          <tr><td class="cmc">Tackles</td><td><span class="lv">22</span></td><td><span class="mv">30</span></td><td><span class="hv">40</span></td><td><div class="bar-wrap"><div class="bar-fill bf-1" data-pct="64"></div></div></td></tr>
          <tr><td class="cmc">Offsides</td><td><span class="lv">3</span></td><td><span class="mv">6</span></td><td><span class="hv">10</span></td><td><div class="bar-wrap"><div class="bar-fill bf-1" data-pct="52"></div></div></td></tr>
        </tbody>
      </table></div>
    </div>
  </div>

  <div class="card fw">
    <div class="card-hd"><div class="hd-dot" style="background:var(--card-y)"></div><div class="hd-title">🟨 Yellow Card Risks</div></div>
    <div class="card-body"><div class="yc-grid">
      <div class="yc-row"><div class="yc-icon">🟨</div><div class="yc-info"><div class="yc-name">Thomas Partey / Zubimendi <span class="yc-club" style="color:#f07070">Arsenal · MF</span></div><div class="yc-reason">Arsenal midfield after UCL midweek — tired legs lead to tactical fouls. Bournemouth's vertical play will draw 50-50s. Whoever plays the deeper DM role is a booking risk.</div></div><div class="yc-risk risk-h">HIGH</div></div>
      <div class="yc-row"><div class="yc-icon">🟨</div><div class="yc-info"><div class="yc-name">Ryan Christie <span class="yc-club" style="color:#f07070">Bournemouth · MF</span></div><div class="yc-reason">High-intensity midfielder with 6 PL yellows. Will compete aggressively against Arsenal's midfield. Bournemouth's press is physical; Christie leads it.</div></div><div class="yc-risk risk-h">HIGH</div></div>
      <div class="yc-row"><div class="yc-icon">🟨</div><div class="yc-info"><div class="yc-name">Lewis Cook / Adam Scott <span class="yc-club" style="color:#f07070">Bournemouth · MF</span></div><div class="yc-reason">Bournemouth have recorded 65 direct attacks — among the most in PL. Their midfield combat style will produce fouls against Arsenal's technical play at the Emirates.</div></div><div class="yc-risk risk-m">MED</div></div>
      <div class="yc-row"><div class="yc-icon">🟨</div><div class="yc-info"><div class="yc-name">Declan Rice <span class="yc-club" style="color:#f07070">Arsenal · MF</span></div><div class="yc-reason">Rice is aggressive breaking up play and has been booked multiple times this season. Against Bournemouth's physical direct attacks, his challenge timing could be off after three games in eight days.</div></div><div class="yc-risk risk-m">MED</div></div>
    </div></div>
  </div>

  <div class="card fw">
    <div class="card-hd"><div class="hd-dot" style="background:#60a5fa"></div><div class="hd-title">Notes</div></div>
    <div class="card-body">
      <div class="note"><strong>Corners (7–10–14):</strong> Arsenal avg 5.8 corners/game at home; Bournemouth have been heavily defensive away (5 straight draws, 3 goalless). Combined baseline ~10.4. Bournemouth's disciplined shape suppresses Arsenal's corner count. Median of 10 is the anchor.</div>
      <div class="note"><strong>Shots (20–26–36):</strong> Arsenal avg 14.7 at home; Bournemouth 11.2 away. Combined baseline ~26. Arsenal UCL fatigue (Tuesday, 12:30 kick-off = 65hrs rest) slightly reduces their creative output. Bournemouth's defensive identity means fewer shots from them. High end requires Arsenal to dominate from the off.</div>
      <div class="note"><strong>Fouls (16–22–30):</strong> Arsenal avg 10.5 fouls; Bournemouth 11.8. Both teams are relatively clean. Bournemouth's pressing system creates tactical foul situations. Michael Oliver (consistent, firm) keeps control. Median of 22 is well-grounded.</div>
      <div class="note"><strong>Tackles (22–30–40):</strong> Arsenal's structured pressing and Bournemouth's work-rate produce contests in midfield. Both teams have ~14-15 tackles/game. UCL fatigue may reduce Arsenal's pressing intensity — but this is a title-race game; they'll be motivated.</div>
    </div>
  </div>

</div><!-- /dg -->
<div class="s-div"><div class="s-div-in">✦ Match 2 ✦</div></div>

<!-- ═══════════════════════════════════════
     MATCH 2 — BRENTFORD vs EVERTON
═══════════════════════════════════════ -->
</div><!-- /page -->

<div class="match-hero mh-bre" id="bre">
  <div class="mh-glow"></div>
  <div class="hero-inner">
    <div class="h-team">
      <div class="badge-ring">
        <img src="https://upload.wikimedia.org/wikipedia/en/thumb/2/2a/Brentford_FC_crest.svg/120px-Brentford_FC_crest.svg.png" alt="Brentford">
      </div>
      <div class="h-name">Brentford</div>
      <div class="h-pos">7th · 46 pts</div>
    </div>
    <div class="vs-col">
      <div class="vs-txt">VS</div>
      <div class="ko-tag">15:00 BST</div>
      <div class="venue-txt">Gtech Community Stadium<br>Ref: Farai Hallam</div>
    </div>
    <div class="h-team">
      <div class="badge-ring" style="animation-delay:.12s">
        <img src="https://upload.wikimedia.org/wikipedia/en/thumb/7/7c/Everton_FC_logo.svg/120px-Everton_FC_logo.svg.png" alt="Everton">
      </div>
      <div class="h-name">Everton</div>
      <div class="h-pos">8th · 46 pts</div>
    </div>
  </div>
</div>

<div class="page">
<div class="dg">

  <div class="card fw">
    <div class="card-hd"><div class="hd-dot" style="background:var(--md)"></div><div class="hd-title">Context</div><div class="hd-tag" style="color:var(--md);border-color:rgba(245,186,50,.28);background:rgba(245,186,50,.07)">European Race · Level on Points</div></div>
    <div class="card-body">
      <div class="callout">Both teams are <strong>dead level on 46 points</strong>, separated only by goal difference. A potential European qualification battle — European slots from 5th down are very much alive. Brentford are coming off <strong>3 straight draws</strong> in the PL, while Everton are in red-hot form: <strong>W3 in last 4</strong>, including a stunning 3–0 demolition of Chelsea. Igor Thiago has 19 PL goals. Brentford beat Everton 4–2 in the reverse fixture. Referee Hallam has issued 87 yellows in 26 games this season (averages 3.35 per game) — cards expected.
      </div>
    </div>
  </div>

  <div class="card fw">
    <div class="card-hd"><div class="hd-dot" style="background:var(--bre)"></div><div class="hd-title">Last 5 Matches — All Comps</div></div>
    <div class="card-body">
      <div class="form-cols">
        <div class="fcol">
          <div class="team-lab lab-bre"><img class="tl-img" src="https://upload.wikimedia.org/wikipedia/en/thumb/2/2a/Brentford_FC_crest.svg/120px-Brentford_FC_crest.svg.png" alt="">Brentford</div>
          <div class="match-list">
            <div class="mr"><div class="rd D"></div><div class="ms">2–2</div><div class="mo">Wolves</div><div class="mc">PL · Home</div></div>
            <div class="mr"><div class="rd D"></div><div class="ms">0–0</div><div class="mo">Leeds United</div><div class="mc">PL · Away</div></div>
            <div class="mr"><div class="rd D"></div><div class="ms">0–0</div><div class="mo">Bournemouth</div><div class="mc">PL · Away</div></div>
            <div class="mr"><div class="rd W"></div><div class="ms">4–3</div><div class="mo">Burnley</div><div class="mc">PL · Away</div></div>
            <div class="mr"><div class="rd W"></div><div class="ms">2–0</div><div class="mo">Brighton</div><div class="mc">PL · Away</div></div>
          </div>
        </div>
        <div class="fcol">
          <div class="team-lab lab-eve"><img class="tl-img" src="https://upload.wikimedia.org/wikipedia/en/thumb/7/7c/Everton_FC_logo.svg/120px-Everton_FC_logo.svg.png" alt="">Everton</div>
          <div class="match-list">
            <div class="mr"><div class="rd W"></div><div class="ms">3–0</div><div class="mo">Chelsea</div><div class="mc">PL · Home</div></div>
            <div class="mr"><div class="rd W"></div><div class="ms">3–2</div><div class="mo">Newcastle</div><div class="mc">PL · Away</div></div>
            <div class="mr"><div class="rd L"></div><div class="ms">0–2</div><div class="mo">Arsenal</div><div class="mc">PL · Away</div></div>
            <div class="mr"><div class="rd W"></div><div class="ms">2–0</div><div class="mo">Burnley</div><div class="mc">PL · Away</div></div>
            <div class="mr"><div class="rd L"></div><div class="ms">2–4</div><div class="mo">Brentford</div><div class="mc">PL · Away</div></div>
          </div>
        </div>
      </div>
      <div class="f-leg"><div class="fl"><div class="fl-dot" style="background:var(--lo)"></div>Win</div><div class="fl"><div class="fl-dot" style="background:var(--md)"></div>Draw</div><div class="fl"><div class="fl-dot" style="background:var(--hi-c)"></div>Loss</div></div>
    </div>
  </div>

  <div class="card fw">
    <div class="card-hd"><div class="hd-dot" style="background:#a78bfa"></div><div class="hd-title">Season Averages per Match — PL 25/26</div></div>
    <div class="card-body">
      <div class="avg-pair">
        <div class="a-grp">
          <div class="a-lbl" style="color:#f07070">Brentford</div>
          <div class="avg-g">
            <div class="ac"><div class="val">13.2</div><div class="lbl">Shots</div></div>
            <div class="ac"><div class="val">4.4</div><div class="lbl">SOT</div></div>
            <div class="ac"><div class="val">5.4</div><div class="lbl">Corners</div></div>
            <div class="ac"><div class="val">10.6</div><div class="lbl">Fouls</div></div>
          </div>
        </div>
        <div class="a-grp">
          <div class="a-lbl" style="color:#7aafff">Everton</div>
          <div class="avg-g">
            <div class="ac"><div class="val">12.8</div><div class="lbl">Shots</div></div>
            <div class="ac"><div class="val">4.2</div><div class="lbl">SOT</div></div>
            <div class="ac"><div class="val">4.8</div><div class="lbl">Corners</div></div>
            <div class="ac"><div class="val">12.1</div><div class="lbl">Fouls</div></div>
          </div>
        </div>
      </div>
    </div>
  </div>

  <div class="card fw">
    <div class="card-hd"><div class="hd-dot" style="background:var(--hi-c)"></div><div class="hd-title">H2H — Last 5 Meetings</div></div>
    <div class="card-body">
      <div class="h2h-bar">
        <div class="hs"><div class="hn" style="color:#f07070">3</div><div class="hl">Brentford</div></div>
        <div class="hdiv"></div>
        <div class="hs"><div class="hn" style="color:var(--md)">0</div><div class="hl">Draws</div></div>
        <div class="hdiv"></div>
        <div class="hs"><div class="hn" style="color:#7aafff">2</div><div class="hl">Everton</div></div>
        <div class="hdiv"></div>
        <div class="hs"><div class="hn">3.0</div><div class="hl">Avg Goals</div></div>
      </div>
      <div class="h2h-rows">
        <div class="h2h-r"><div class="rh">Everton</div><div class="rs">2–4</div><div class="ra">Brentford</div><div class="rsub">PL · Everton's new stadium · Jan 2026</div></div>
        <div class="h2h-r"><div class="rh">Brentford</div><div class="rs">1–0</div><div class="ra">Everton</div><div class="rsub">PL · Gtech · Apr 2025</div></div>
        <div class="h2h-r"><div class="rh">Everton</div><div class="rs">1–2</div><div class="ra">Brentford</div><div class="rsub">PL · Hill Dickinson · Dec 2024</div></div>
        <div class="h2h-r"><div class="rh">Brentford</div><div class="rs">2–1</div><div class="ra">Everton</div><div class="rsub">PL · Gtech · Oct 2023</div></div>
        <div class="h2h-r"><div class="rh">Everton</div><div class="rs">3–2</div><div class="ra">Brentford</div><div class="rsub">PL · Goodison Park · Feb 2023</div></div>
      </div>
    </div>
  </div>

  <div class="card fw" id="pred-bre">
    <div class="card-hd"><div class="hd-dot" style="background:var(--lo)"></div><div class="hd-title">Weighted Predictions — Brentford vs Everton</div></div>
    <div class="card-body">
      <div class="pred-leg"><div class="pli"><div class="pld" style="background:var(--lo)"></div><span style="color:var(--lo);font-weight:700">Low</span></div><div class="pli"><div class="pld" style="background:var(--md)"></div><span style="color:var(--md);font-weight:700">Median</span></div><div class="pli"><div class="pld" style="background:var(--hi-c)"></div><span style="color:var(--hi-c);font-weight:700">High</span></div></div>
      <div class="pw"><table class="pt">
        <colgroup><col class="cm"><col class="cl"><col class="cn"><col class="ch"><col class="cb"></colgroup>
        <thead><tr><th>Metric</th><th style="color:var(--lo)">Low</th><th class="th-m">Median</th><th style="color:var(--hi-c)">High</th><th style="text-align:center;color:var(--muted)">Intensity</th></tr></thead>
        <tbody>
          <tr><td class="cmc">Corners</td><td><span class="lv">7</span></td><td><span class="mv">10</span></td><td><span class="hv">15</span></td><td><div class="bar-wrap"><div class="bar-fill bf-2" data-pct="62"></div></div></td></tr>
          <tr><td class="cmc">Total Shots</td><td><span class="lv">18</span></td><td><span class="mv">25</span></td><td><span class="hv">34</span></td><td><div class="bar-wrap"><div class="bar-fill bf-2" data-pct="70"></div></div></td></tr>
          <tr><td class="cmc">Shots on Target</td><td><span class="lv">6</span></td><td><span class="mv">9</span></td><td><span class="hv">14</span></td><td><div class="bar-wrap"><div class="bar-fill bf-2" data-pct="62"></div></div></td></tr>
          <tr><td class="cmc">Fouls</td><td><span class="lv">18</span></td><td><span class="mv">25</span></td><td><span class="hv">34</span></td><td><div class="bar-wrap"><div class="bar-fill bf-2" data-pct="72"></div></div></td></tr>
          <tr><td class="cmc">Throw-ins</td><td><span class="lv">34</span></td><td><span class="mv">44</span></td><td><span class="hv">56</span></td><td><div class="bar-wrap"><div class="bar-fill bf-2" data-pct="64"></div></div></td></tr>
          <tr><td class="cmc">Goal Kicks</td><td><span class="lv">14</span></td><td><span class="mv">20</span></td><td><span class="hv">28</span></td><td><div class="bar-wrap"><div class="bar-fill bf-2" data-pct="58"></div></div></td></tr>
          <tr><td class="cmc">Tackles</td><td><span class="lv">26</span></td><td><span class="mv">34</span></td><td><span class="hv">46</span></td><td><div class="bar-wrap"><div class="bar-fill bf-2" data-pct="76"></div></div></td></tr>
          <tr><td class="cmc">Offsides</td><td><span class="lv">2</span></td><td><span class="mv">5</span></td><td><span class="hv">9</span></td><td><div class="bar-wrap"><div class="bar-fill bf-2" data-pct="48"></div></div></td></tr>
        </tbody>
      </table></div>
    </div>
  </div>

  <div class="card fw">
    <div class="card-hd"><div class="hd-dot" style="background:var(--card-y)"></div><div class="hd-title">🟨 Yellow Card Risks</div></div>
    <div class="card-body"><div class="yc-grid">
      <div class="yc-row"><div class="yc-icon">🟨</div><div class="yc-info"><div class="yc-name">Idrissa Gueye <span class="yc-club" style="color:#7aafff">Everton · DM</span></div><div class="yc-reason">Combative defensive midfielder with 8 PL yellows this season. Against Brentford's physical counter-attack system led by Thiago, Gueye will be pressed into desperate challenges. High European stakes increase aggression.</div></div><div class="yc-risk risk-h">HIGH</div></div>
      <div class="yc-row"><div class="yc-icon">🟨</div><div class="yc-info"><div class="yc-name">Vitaly Janelt <span class="yc-club" style="color:#f07070">Brentford · MF</span></div><div class="yc-reason">Dynamic midfielder who wins the ball aggressively. Was absent recently (fitness) but expected to return. Returning players often overcook tackles in first games back. Key to stopping Everton's creative midfield.</div></div><div class="yc-risk risk-h">HIGH</div></div>
      <div class="yc-row"><div class="yc-icon">🟨</div><div class="yc-info"><div class="yc-name">Jarrad Branthwaite <span class="yc-club" style="color:#7aafff">Everton · CB</span></div><div class="yc-reason">Tall, aggressive centre-back who has been key in Everton's defensive resurgence. Will face Igor Thiago's direct running. Brentford average the most goals from counter-attacks in the PL — Branthwaite will be tested.</div></div><div class="yc-risk risk-m">MED</div></div>
      <div class="yc-row"><div class="yc-icon">🟨</div><div class="yc-info"><div class="yc-name">Nathan Collins <span class="yc-club" style="color:#f07070">Brentford · CB</span></div><div class="yc-reason">Physical, committed defender who plays on the edge. Will mark Beto closely — Everton's powerful striker generates physical duels. Referee Hallam gives cards freely.</div></div><div class="yc-risk risk-m">MED</div></div>
    </div></div>
  </div>

  <div class="card fw">
    <div class="card-hd"><div class="hd-dot" style="background:#60a5fa"></div><div class="hd-title">Notes</div></div>
    <div class="card-body">
      <div class="note"><strong>Tackles (26–34–46):</strong> This is expected to be the highest-tackle game of the four on Saturday. Both teams are physical, both have European ambitions, and Gtech Community Stadium always produces aggressive duels. Brentford 10.6 fouls/game + Everton 12.1 = 22.7 combined baseline for fouls alone. Referee Hallam averages 3.35 yellows, but the stakes will elevate the physicality.</div>
      <div class="note"><strong>Shots (18–25–34):</strong> The reverse fixture produced 6 goals (4-2 Brentford). H2H averages 3.0 goals/game. Both teams attack with intent but Brentford's defensive record at home has been excellent (17 conceded at home vs Everton's ~20 conceded away). High end if the match opens up after an early goal.</div>
      <div class="note"><strong>Corners (7–10–15):</strong> Brentford 5.4 corners earned/game; Everton 4.8. Combined ~10.2. Neither team defends corners particularly well — both are physical in the air. The compact Gtech pitch generates more corners than most PL grounds. Median of 10 is well supported.</div>
    </div>
  </div>

</div>
<div class="s-div"><div class="s-div-in">✦ Match 3 ✦</div></div>
</div>

<!-- ═══════════════════════════════════════
     MATCH 3 — BURNLEY vs BRIGHTON
═══════════════════════════════════════ -->
<div class="match-hero mh-bur" id="bur">
  <div class="mh-glow"></div>
  <div class="hero-inner">
    <div class="h-team">
      <div class="badge-ring">
        <img src="https://brandlogos.net/wp-content/uploads/2023/07/burnley_fc-logo_brandlogos.net_vh9ys.png" alt="Burnley">
      </div>
      <div class="h-name">Burnley</div>
      <div class="h-pos">19th · 20 pts · Relegation</div>
    </div>
    <div class="vs-col">
      <div class="vs-txt">VS</div>
      <div class="ko-tag">15:00 BST</div>
      <div class="venue-txt">Turf Moor, Burnley<br>Ref: Thomas Bramall</div>
    </div>
    <div class="h-team">
      <div class="badge-ring" style="animation-delay:.12s">
        <img src="https://upload.wikimedia.org/wikipedia/en/thumb/f/fd/Brighton_%26_Hove_Albion_logo.svg/120px-Brighton_%26_Hove_Albion_logo.svg.png" alt="Brighton">
      </div>
      <div class="h-name">Brighton</div>
      <div class="h-pos">10th · 43 pts · European Push</div>
    </div>
  </div>
</div>

<div class="page">
<div class="dg">

  <div class="card fw">
    <div class="card-hd"><div class="hd-dot" style="background:var(--md)"></div><div class="hd-title">Context</div><div class="hd-tag" style="color:var(--danger);border-color:rgba(239,68,68,.28);background:rgba(239,68,68,.07)">Burnley Likely Relegated</div></div>
    <div class="card-body">
      <div class="callout">Burnley have <strong>won just 1 of their last 22 Premier League games</strong>. By kick-off, they could be 12 points from safety with 7 games left — their relegation is a near-certainty. Scott Parker has vowed full commitment but the squad is depleted: Laurent (suspended), Roberts (injured), Cullen (season-ending knee), Beyer (knee). Brighton arrive in exceptional form — <strong>W4 in last 5</strong>, including a 2-1 win over Liverpool. Lewis Dunk is suspended, but Kaoru Mitoma returns from Japan duty. Referee Bramall averages <strong>4.06 yellows/game</strong> and Brighton receive 3.1 away yellows/game.
      </div>
    </div>
  </div>

  <div class="card fw">
    <div class="card-hd"><div class="hd-dot" style="background:var(--bur)"></div><div class="hd-title">Last 5 Matches — All Comps</div></div>
    <div class="card-body">
      <div class="form-cols">
        <div class="fcol">
          <div class="team-lab lab-bur"><img class="tl-img" src="https://upload.wikimedia.org/wikipedia/en/thumb/6/62/Burnley_F.C._Logo.svg/120px-Burnley_F.C._Logo.svg.png" alt="">Burnley</div>
          <div class="match-list">
            <div class="mr"><div class="rd L"></div><div class="ms">1–3</div><div class="mo">Fulham</div><div class="mc">PL · Away</div></div>
            <div class="mr"><div class="rd D"></div><div class="ms">0–0</div><div class="mo">Bournemouth</div><div class="mc">PL · Home</div></div>
            <div class="mr"><div class="rd L"></div><div class="ms">0–2</div><div class="mo">Everton</div><div class="mc">PL · Away</div></div>
            <div class="mr"><div class="rd L"></div><div class="ms">3–4</div><div class="mo">Brentford</div><div class="mc">PL · Home</div></div>
            <div class="mr"><div class="rd D"></div><div class="ms">1–1</div><div class="mo">Chelsea</div><div class="mc">PL · Away</div></div>
          </div>
        </div>
        <div class="fcol">
          <div class="team-lab lab-bri"><img class="tl-img" src="https://upload.wikimedia.org/wikipedia/en/thumb/f/fd/Brighton_%26_Hove_Albion_logo.svg/120px-Brighton_%26_Hove_Albion_logo.svg.png" alt="">Brighton</div>
          <div class="match-list">
            <div class="mr"><div class="rd W"></div><div class="ms">2–1</div><div class="mo">Liverpool</div><div class="mc">PL · Home</div></div>
            <div class="mr"><div class="rd W"></div><div class="ms">1–0</div><div class="mo">Sunderland</div><div class="mc">PL · Away</div></div>
            <div class="mr"><div class="rd W"></div><div class="ms">2–1</div><div class="mo">Nott'm Forest</div><div class="mc">PL · Home</div></div>
            <div class="mr"><div class="rd W"></div><div class="ms">2–0</div><div class="mo">Brentford</div><div class="mc">PL · Away</div></div>
            <div class="mr"><div class="rd L"></div><div class="ms">0–1</div><div class="mo">Arsenal</div><div class="mc">PL · Away</div></div>
          </div>
        </div>
      </div>
      <div class="f-leg"><div class="fl"><div class="fl-dot" style="background:var(--lo)"></div>Win</div><div class="fl"><div class="fl-dot" style="background:var(--md)"></div>Draw</div><div class="fl"><div class="fl-dot" style="background:var(--hi-c)"></div>Loss</div></div>
    </div>
  </div>

  <div class="card fw">
    <div class="card-hd"><div class="hd-dot" style="background:#a78bfa"></div><div class="hd-title">Season Averages per Match — PL 25/26</div></div>
    <div class="card-body">
      <div class="avg-pair">
        <div class="a-grp">
          <div class="a-lbl" style="color:#d070a0">Burnley</div>
          <div class="avg-g">
            <div class="ac"><div class="val">10.4</div><div class="lbl">Shots</div></div>
            <div class="ac"><div class="val">3.5</div><div class="lbl">SOT</div></div>
            <div class="ac"><div class="val">3.4</div><div class="lbl">Corners</div></div>
            <div class="ac"><div class="val">11.9</div><div class="lbl">Fouls</div></div>
          </div>
        </div>
        <div class="a-grp">
          <div class="a-lbl" style="color:#7aafff">Brighton</div>
          <div class="avg-g">
            <div class="ac"><div class="val">13.8</div><div class="lbl">Shots</div></div>
            <div class="ac"><div class="val">4.7</div><div class="lbl">SOT</div></div>
            <div class="ac"><div class="val">4.4</div><div class="lbl">Corners Away</div></div>
            <div class="ac"><div class="val">11.4</div><div class="lbl">Fouls</div></div>
          </div>
        </div>
      </div>
    </div>
  </div>

  <div class="card fw">
    <div class="card-hd"><div class="hd-dot" style="background:var(--hi-c)"></div><div class="hd-title">H2H — Last 5 Meetings</div></div>
    <div class="card-body">
      <div class="h2h-bar">
        <div class="hs"><div class="hn" style="color:#d070a0">1</div><div class="hl">Burnley</div></div>
        <div class="hdiv"></div>
        <div class="hs"><div class="hn" style="color:var(--md)">2</div><div class="hl">Draws</div></div>
        <div class="hdiv"></div>
        <div class="hs"><div class="hn" style="color:#7aafff">2</div><div class="hl">Brighton</div></div>
        <div class="hdiv"></div>
        <div class="hs"><div class="hn">2.0</div><div class="hl">Avg Goals</div></div>
      </div>
      <div class="h2h-rows">
        <div class="h2h-r"><div class="rh">Brighton</div><div class="rs">2–0</div><div class="ra">Burnley</div><div class="rsub">PL · Amex · Jan 2026</div></div>
        <div class="h2h-r"><div class="rh">Burnley</div><div class="rs">1–1</div><div class="ra">Brighton</div><div class="rsub">PL · Turf Moor · Sep 2025</div></div>
        <div class="h2h-r"><div class="rh">Burnley</div><div class="rs">1–2</div><div class="ra">Brighton</div><div class="rsub">Championship · Feb 2023</div></div>
        <div class="h2h-r"><div class="rh">Burnley</div><div class="rs">1–1</div><div class="ra">Brighton</div><div class="rsub">Championship · Oct 2022</div></div>
        <div class="h2h-r"><div class="rh">Burnley</div><div class="rs">1–0</div><div class="ra">Brighton</div><div class="rsub">PL · Turf Moor · Dec 2018</div></div>
      </div>
      <p style="font-size:10.5px;color:var(--muted);margin-top:8px;">Over 8.5 total corners in 5 consecutive H2H meetings at Turf Moor. Brighton unbeaten in last 4 visits to Burnley (W2 D2).</p>
    </div>
  </div>

  <div class="card fw" id="pred-bur">
    <div class="card-hd"><div class="hd-dot" style="background:var(--lo)"></div><div class="hd-title">Weighted Predictions — Burnley vs Brighton</div></div>
    <div class="card-body">
      <div class="pred-leg"><div class="pli"><div class="pld" style="background:var(--lo)"></div><span style="color:var(--lo);font-weight:700">Low</span></div><div class="pli"><div class="pld" style="background:var(--md)"></div><span style="color:var(--md);font-weight:700">Median</span></div><div class="pli"><div class="pld" style="background:var(--hi-c)"></div><span style="color:var(--hi-c);font-weight:700">High</span></div></div>
      <div class="pw"><table class="pt">
        <colgroup><col class="cm"><col class="cl"><col class="cn"><col class="ch"><col class="cb"></colgroup>
        <thead><tr><th>Metric</th><th style="color:var(--lo)">Low</th><th class="th-m">Median</th><th style="color:var(--hi-c)">High</th><th style="text-align:center;color:var(--muted)">Intensity</th></tr></thead>
        <tbody>
          <tr><td class="cmc">Corners</td><td><span class="lv">8</span></td><td><span class="mv">11</span></td><td><span class="hv">16</span></td><td><div class="bar-wrap"><div class="bar-fill bf-3" data-pct="66"></div></div></td></tr>
          <tr><td class="cmc">Total Shots</td><td><span class="lv">17</span></td><td><span class="mv">24</span></td><td><span class="hv">33</span></td><td><div class="bar-wrap"><div class="bar-fill bf-3" data-pct="68"></div></div></td></tr>
          <tr><td class="cmc">Shots on Target</td><td><span class="lv">5</span></td><td><span class="mv">9</span></td><td><span class="hv">14</span></td><td><div class="bar-wrap"><div class="bar-fill bf-3" data-pct="60"></div></div></td></tr>
          <tr><td class="cmc">Fouls</td><td><span class="lv">19</span></td><td><span class="mv">26</span></td><td><span class="hv">36</span></td><td><div class="bar-wrap"><div class="bar-fill bf-3" data-pct="76"></div></div></td></tr>
          <tr><td class="cmc">Throw-ins</td><td><span class="lv">36</span></td><td><span class="mv">46</span></td><td><span class="hv">58</span></td><td><div class="bar-wrap"><div class="bar-fill bf-3" data-pct="68"></div></div></td></tr>
          <tr><td class="cmc">Goal Kicks</td><td><span class="lv">15</span></td><td><span class="mv">22</span></td><td><span class="hv">30</span></td><td><div class="bar-wrap"><div class="bar-fill bf-3" data-pct="66"></div></div></td></tr>
          <tr><td class="cmc">Tackles</td><td><span class="lv">26</span></td><td><span class="mv">34</span></td><td><span class="hv">46</span></td><td><div class="bar-wrap"><div class="bar-fill bf-3" data-pct="74"></div></div></td></tr>
          <tr><td class="cmc">Offsides</td><td><span class="lv">2</span></td><td><span class="mv">5</span></td><td><span class="hv">8</span></td><td><div class="bar-wrap"><div class="bar-fill bf-3" data-pct="44"></div></div></td></tr>
        </tbody>
      </table></div>
    </div>
  </div>

  <div class="card fw">
    <div class="card-hd"><div class="hd-dot" style="background:var(--card-y)"></div><div class="hd-title">🟨 Yellow Card Risks</div></div>
    <div class="card-body"><div class="yc-grid">
      <div class="yc-row"><div class="yc-icon">🟨</div><div class="yc-info"><div class="yc-name">James Ward-Prowse <span class="yc-club" style="color:#d070a0">Burnley · MF</span></div><div class="yc-reason">Captain and organiser — will be desperately trying to marshal a depleted midfield. Against Brighton's 264 high turnovers (1st in PL), Ward-Prowse will commit fouls trying to win the ball back. Has 5 PL yellows.</div></div><div class="yc-risk risk-h">HIGH</div></div>
      <div class="yc-row"><div class="yc-icon">🟨</div><div class="yc-info"><div class="yc-name">Pascal Groß / Mats Wieffer <span class="yc-club" style="color:#7aafff">Brighton · MF</span></div><div class="yc-reason">Brighton receive 3.1 away yellows/game (highest in PL). Brighton's midfield presses aggressively and Groß/Wieffer are physical. Against a desperate Burnley side, their pressing will generate foul situations.</div></div><div class="yc-risk risk-h">HIGH</div></div>
      <div class="yc-row"><div class="yc-icon">🟨</div><div class="yc-info"><div class="yc-name">Bashir Humphreys <span class="yc-club" style="color:#d070a0">Burnley · CB</span></div><div class="yc-reason">Burnley's defence is the PL's worst (61 conceded). Humphreys will be tested by Brighton's pace and movement. One mistimed tackle stopping a counter-attack in a game Burnley desperately need to win.</div></div><div class="yc-risk risk-m">MED</div></div>
      <div class="yc-row"><div class="yc-icon">🟨</div><div class="yc-info"><div class="yc-name">Yankuba Minteh <span class="yc-club" style="color:#7aafff">Brighton · FW</span></div><div class="yc-reason">Electric winger who draws fouls regularly. His pace and directness against Burnley's makeshift full-backs will create flashpoints. 4 yellows this season for simulation and reaction fouls.</div></div><div class="yc-risk risk-m">MED</div></div>
    </div></div>
  </div>

  <div class="card fw">
    <div class="card-hd"><div class="hd-dot" style="background:#60a5fa"></div><div class="hd-title">Notes</div></div>
    <div class="card-body">
      <div class="note"><strong>Corners (8–11–16):</strong> H2H data is the anchor here — over 8.5 corners in 5 consecutive meetings at Turf Moor. Brighton avg 4.4 corners away; Burnley 3.4 at home. Combined season baseline ~7.8, but H2H trend and Burnley's desperation to attack (must risk for corners from set pieces) push the median to 11.</div>
      <div class="note"><strong>Fouls (19–26–36):</strong> This is the highest foul projection of the four games. Burnley average 11.9 fouls (2nd highest in PL); Brighton average 11.4 on the road. Combined baseline 23.3. The desperation element from Burnley (must win) and Bramall's high card average (4.06/game) drives the median to 26. Brighton's pressing system creates constant foul-opportunities. High end of 36 if Burnley become desperate in the second half.</div>
      <div class="note"><strong>Shots (17–24–33):</strong> Brighton are one of the best pressing teams in England; Burnley's defence has conceded 61 goals. Brighton avg 13.8 shots/game; Burnley 10.4. Combined ~24 baseline with Brighton's quality suppressing Burnley's attacking output. Burnley need goals so will shoot from anywhere.</div>
      <div class="note"><strong>Goal Kicks (15–22–30):</strong> Brighton's high press forces Burnley's goalkeeper (Dubravka) to launch long balls repeatedly. Burnley have conceded the first goal in 23 of 31 matches — they'll spend significant time defending from goal kicks.</div>
    </div>
  </div>

</div>
<div class="s-div"><div class="s-div-in">✦ Match 4 ✦</div></div>
</div>

<!-- ═══════════════════════════════════════
     MATCH 4 — LIVERPOOL vs FULHAM
═══════════════════════════════════════ -->
<div class="match-hero mh-liv" id="liv">
  <div class="mh-glow"></div>
  <div class="hero-inner">
    <div class="h-team">
      <div class="badge-ring">
        <img src="https://upload.wikimedia.org/wikipedia/en/thumb/0/0c/Liverpool_FC.svg/120px-Liverpool_FC.svg.png" alt="Liverpool">
      </div>
      <div class="h-name">Liverpool</div>
      <div class="h-pos">5th · 49 pts · UCL Wed</div>
    </div>
    <div class="vs-col">
      <div class="vs-txt">VS</div>
      <div class="ko-tag">17:30 BST</div>
      <div class="venue-txt">Anfield, Liverpool<br>Ref: Anthony Taylor</div>
    </div>
    <div class="h-team">
      <div class="badge-ring" style="animation-delay:.12s">
        <img src="https://upload.wikimedia.org/wikipedia/en/thumb/e/eb/Fulham_FC_%28shield%29.svg/120px-Fulham_FC_%28shield%29.svg.png" alt="Fulham">
      </div>
      <div class="h-name">Fulham</div>
      <div class="h-pos">9th · 44 pts</div>
    </div>
  </div>
</div>

<div class="page">
<div class="dg">

  <div class="f-banner fw">
    <div class="f-icon">⚡</div>
    <div class="f-text"><strong>Liverpool UCL Fatigue — Played PSG (away) on Wednesday:</strong> Liverpool lost 0–2 to PSG at Parc des Princes in the UCL QF Leg 1 on Wednesday night. That's just 3 days before Anfield hosts Fulham. Alisson (injured), Conor Bradley, Leoni and Endo are all unavailable. Slot may rotate key players with the PSG return leg in mind. All predictions weighted for a fatigued, depleted Liverpool side.</div>
  </div>

  <div class="card fw">
    <div class="card-hd"><div class="hd-dot" style="background:var(--md)"></div><div class="hd-title">Context</div><div class="hd-tag" style="color:var(--warn);border-color:rgba(245,158,11,.28);background:rgba(245,158,11,.07)">UCL Fatigue · 3 Losses In a Row</div></div>
    <div class="card-body">
      <div class="callout">Liverpool have <strong>lost 3 consecutive matches</strong>: Man City 4–0 (FA Cup), PSG 0–2 (UCL), Brighton 1–2 (PL). Van Dijk admitted the team "gave up" vs Man City. Slot needs a response at Anfield but with <strong>key absentees and European fatigue</strong>, this is a danger game. Fulham won 3–1 at Burnley last time out, have Harry Wilson on 10 goals and 6 assists, and are <strong>unbeaten in their last 3 meetings vs Liverpool</strong> (W1 D2). BTTS in all 5 recent H2H meetings. Liverpool's corner average at Anfield is 5.93/game; Fulham earn 4.1–5.1 corners away. Both teams to score is the strongest market signal.
      </div>
    </div>
  </div>

  <div class="card fw">
    <div class="card-hd"><div class="hd-dot" style="background:var(--liv)"></div><div class="hd-title">Last 5 Matches — All Comps</div></div>
    <div class="card-body">
      <div class="form-cols">
        <div class="fcol">
          <div class="team-lab lab-liv"><img class="tl-img" src="https://upload.wikimedia.org/wikipedia/en/thumb/0/0c/Liverpool_FC.svg/120px-Liverpool_FC.svg.png" alt="">Liverpool</div>
          <div class="match-list">
            <div class="mr"><div class="rd L"></div><div class="ms">0–2</div><div class="mo">PSG</div><div class="mc">UCL QF <span class="ucl-note">Wed</span></div></div>
            <div class="mr"><div class="rd L"></div><div class="ms">1–2</div><div class="mo">Brighton</div><div class="mc">PL · Away</div></div>
            <div class="mr"><div class="rd L"></div><div class="ms">0–4</div><div class="mo">Manchester City</div><div class="mc">FAC · Away</div></div>
            <div class="mr"><div class="rd W"></div><div class="ms">4–0</div><div class="mo">Galatasaray</div><div class="mc">UCL R16 · Home</div></div>
            <div class="mr"><div class="rd L"></div><div class="ms">2–1</div><div class="mo">Wolves</div><div class="mc">PL · Away</div></div>
          </div>
        </div>
        <div class="fcol">
          <div class="team-lab lab-ful"><img class="tl-img" src="https://upload.wikimedia.org/wikipedia/en/thumb/e/eb/Fulham_FC_%28shield%29.svg/120px-Fulham_FC_%28shield%29.svg.png" alt="">Fulham</div>
          <div class="match-list">
            <div class="mr"><div class="rd W"></div><div class="ms">3–1</div><div class="mo">Burnley</div><div class="mc">PL · Home</div></div>
            <div class="mr"><div class="rd W"></div><div class="ms">2–1</div><div class="mo">Brentford</div><div class="mc">PL · Away</div></div>
            <div class="mr"><div class="rd L"></div><div class="ms">0–2</div><div class="mo">Chelsea</div><div class="mc">PL · Away</div></div>
            <div class="mr"><div class="rd W"></div><div class="ms">2–1</div><div class="mo">Man United</div><div class="mc">PL · Home</div></div>
            <div class="mr"><div class="rd D"></div><div class="ms">2–2</div><div class="mo">Liverpool</div><div class="mc">PL · Away</div></div>
          </div>
        </div>
      </div>
      <div class="f-leg"><div class="fl"><div class="fl-dot" style="background:var(--lo)"></div>Win</div><div class="fl"><div class="fl-dot" style="background:var(--md)"></div>Draw</div><div class="fl"><div class="fl-dot" style="background:var(--hi-c)"></div>Loss</div></div>
    </div>
  </div>

  <div class="card fw">
    <div class="card-hd"><div class="hd-dot" style="background:#a78bfa"></div><div class="hd-title">Season Averages per Match — PL 25/26</div></div>
    <div class="card-body">
      <div class="avg-pair">
        <div class="a-grp">
          <div class="a-lbl" style="color:#f07070">Liverpool</div>
          <div class="avg-g">
            <div class="ac"><div class="val">17.7</div><div class="lbl">Shots</div></div>
            <div class="ac"><div class="val">5.6</div><div class="lbl">SOT</div></div>
            <div class="ac"><div class="val">5.9</div><div class="lbl">Corners</div></div>
            <div class="ac"><div class="val">10.4</div><div class="lbl">Fouls</div></div>
          </div>
        </div>
        <div class="a-grp">
          <div class="a-lbl" style="color:#f07070">Fulham</div>
          <div class="avg-g">
            <div class="ac"><div class="val">13.2</div><div class="lbl">Shots</div></div>
            <div class="ac"><div class="val">3.8</div><div class="lbl">SOT</div></div>
            <div class="ac"><div class="val">5.1</div><div class="lbl">Corners</div></div>
            <div class="ac"><div class="val">11.6</div><div class="lbl">Fouls</div></div>
          </div>
        </div>
      </div>
    </div>
  </div>

  <div class="card fw">
    <div class="card-hd"><div class="hd-dot" style="background:var(--hi-c)"></div><div class="hd-title">H2H — Last 5 Meetings</div></div>
    <div class="card-body">
      <div class="h2h-bar">
        <div class="hs"><div class="hn" style="color:#f07070">1</div><div class="hl">Liverpool</div></div>
        <div class="hdiv"></div>
        <div class="hs"><div class="hn" style="color:var(--md)">3</div><div class="hl">Draws</div></div>
        <div class="hdiv"></div>
        <div class="hs"><div class="hn" style="color:#f07070">1</div><div class="hl">Fulham</div></div>
        <div class="hdiv"></div>
        <div class="hs"><div class="hn">BTTS</div><div class="hl">All 5 Games</div></div>
      </div>
      <div class="h2h-rows">
        <div class="h2h-r"><div class="rh">Fulham</div><div class="rs">2–2</div><div class="ra">Liverpool</div><div class="rsub">PL · Craven Cottage · this season (Gakpo 89' / Reed 97')</div></div>
        <div class="h2h-r"><div class="rh">Liverpool</div><div class="rs">3–1</div><div class="ra">Fulham</div><div class="rsub">PL · Anfield · Apr 2025</div></div>
        <div class="h2h-r"><div class="rh">Liverpool</div><div class="rs">3–3</div><div class="ra">Fulham</div><div class="rsub">PL · Anfield · Mar 2024</div></div>
        <div class="h2h-r"><div class="rh">Fulham</div><div class="rs">2–1</div><div class="ra">Liverpool</div><div class="rsub">PL · Craven Cottage · Mar 2023</div></div>
        <div class="h2h-r"><div class="rh">Liverpool</div><div class="rs">2–2</div><div class="ra">Fulham</div><div class="rsub">PL · Anfield · Dec 2022</div></div>
      </div>
      <p style="font-size:10.5px;color:var(--muted);margin-top:8px;">BTTS in every single meeting in this run. 2+ goals in every H2H. 3+ goals in 4 of last 5. Fulham unbeaten in last 3 vs Liverpool. Raul Jimenez averages 1.86 fouls/game against Van Dijk.</p>
    </div>
  </div>

  <div class="card fw" id="pred-liv">
    <div class="card-hd"><div class="hd-dot" style="background:var(--lo)"></div><div class="hd-title">Weighted Predictions — Liverpool vs Fulham</div></div>
    <div class="card-body">
      <div class="pred-leg"><div class="pli"><div class="pld" style="background:var(--lo)"></div><span style="color:var(--lo);font-weight:700">Low</span></div><div class="pli"><div class="pld" style="background:var(--md)"></div><span style="color:var(--md);font-weight:700">Median</span></div><div class="pli"><div class="pld" style="background:var(--hi-c)"></div><span style="color:var(--hi-c);font-weight:700">High</span></div></div>
      <div class="pw"><table class="pt">
        <colgroup><col class="cm"><col class="cl"><col class="cn"><col class="ch"><col class="cb"></colgroup>
        <thead><tr><th>Metric</th><th style="color:var(--lo)">Low</th><th class="th-m">Median</th><th style="color:var(--hi-c)">High</th><th style="text-align:center;color:var(--muted)">Intensity</th></tr></thead>
        <tbody>
          <tr><td class="cmc">Corners</td><td><span class="lv">8</span></td><td><span class="mv">11</span></td><td><span class="hv">16</span></td><td><div class="bar-wrap"><div class="bar-fill bf-4" data-pct="66"></div></div></td></tr>
          <tr><td class="cmc">Total Shots</td><td><span class="lv">20</span></td><td><span class="mv">27</span></td><td><span class="hv">38</span></td><td><div class="bar-wrap"><div class="bar-fill bf-4" data-pct="74"></div></div></td></tr>
          <tr><td class="cmc">Shots on Target</td><td><span class="lv">7</span></td><td><span class="mv">10</span></td><td><span class="hv">16</span></td><td><div class="bar-wrap"><div class="bar-fill bf-4" data-pct="66"></div></div></td></tr>
          <tr><td class="cmc">Fouls</td><td><span class="lv">17</span></td><td><span class="mv">23</span></td><td><span class="hv">32</span></td><td><div class="bar-wrap"><div class="bar-fill bf-4" data-pct="60"></div></div></td></tr>
          <tr><td class="cmc">Throw-ins</td><td><span class="lv">36</span></td><td><span class="mv">48</span></td><td><span class="hv">62</span></td><td><div class="bar-wrap"><div class="bar-fill bf-4" data-pct="72"></div></div></td></tr>
          <tr><td class="cmc">Goal Kicks</td><td><span class="lv">14</span></td><td><span class="mv">21</span></td><td><span class="hv">30</span></td><td><div class="bar-wrap"><div class="bar-fill bf-4" data-pct="62"></div></div></td></tr>
          <tr><td class="cmc">Tackles</td><td><span class="lv">24</span></td><td><span class="mv">32</span></td><td><span class="hv">44</span></td><td><div class="bar-wrap"><div class="bar-fill bf-4" data-pct="68"></div></div></td></tr>
          <tr><td class="cmc">Offsides</td><td><span class="lv">3</span></td><td><span class="mv">6</span></td><td><span class="hv">11</span></td><td><div class="bar-wrap"><div class="bar-fill bf-4" data-pct="56"></div></div></td></tr>
        </tbody>
      </table></div>
    </div>
  </div>

  <div class="card fw">
    <div class="card-hd"><div class="hd-dot" style="background:var(--card-y)"></div><div class="hd-title">🟨 Yellow Card Risk Players</div></div>
    <div class="card-body"><div class="yc-grid">
      <div class="yc-row"><div class="yc-icon">🟨</div><div class="yc-info"><div class="yc-name">Raúl Jiménez <span class="yc-club" style="color:#f07070">Fulham · FW</span></div><div class="yc-reason">Averages 1.86 fouls/game — highest of any PL attacker. Has committed multiple fouls in 5 of last 10 away games. His physical duel with van Dijk will be intense — Liverpool's captain has been fouled in 2 of his last 3 Anfield appearances. Jiménez's wrestling style almost guarantees a booking.</div></div><div class="yc-risk risk-h">HIGH</div></div>
      <div class="yc-row"><div class="yc-icon">🟨</div><div class="yc-info"><div class="yc-name">Ryan Gravenberch <span class="yc-club" style="color:#f07070">Liverpool · MF</span></div><div class="yc-reason">Likely to play a high number of minutes given Endo's absence. Will be needed to win the ball back against Fulham's dynamic midfield. Fatigue from PSG midweek will make his challenges lunge-prone. 4 PL yellows this season.</div></div><div class="yc-risk risk-h">HIGH</div></div>
      <div class="yc-row"><div class="yc-icon">🟨</div><div class="yc-info"><div class="yc-name">Sander Berge <span class="yc-club" style="color:#f07070">Fulham · DM</span></div><div class="yc-reason">Tall, powerful midfielder who competes physically for everything. Will be tasked with stopping Liverpool's counter-attacking moves from midfield. Against a potentially rattled Liverpool midfield, Berge will press aggressively.</div></div><div class="yc-risk risk-h">HIGH</div></div>
      <div class="yc-row"><div class="yc-icon">🟨</div><div class="yc-info"><div class="yc-name">Virgil van Dijk <span class="yc-club" style="color:#f07070">Liverpool · CB</span></div><div class="yc-reason">Van Dijk is under personal pressure with his future at Anfield uncertain. Emotional games lead to animated responses with referees. He's been fouled repeatedly and his reactions have drawn cards. Fulham's physical attack will frustrate him.</div></div><div class="yc-risk risk-m">MED</div></div>
      <div class="yc-row"><div class="yc-icon">🟨</div><div class="yc-info"><div class="yc-name">Alex Iwobi <span class="yc-club" style="color:#f07070">Fulham · MF</span></div><div class="yc-reason">Creative engine who drives at defenders. Has been in excellent form but picks up cards for over-aggressive pressing. Will look to exploit Liverpool's tired midfield — his energy vs their fatigue creates flashpoints.</div></div><div class="yc-risk risk-m">MED</div></div>
    </div></div>
  </div>

  <div class="card fw">
    <div class="card-hd"><div class="hd-dot" style="background:#60a5fa"></div><div class="hd-title">Notes</div></div>
    <div class="card-body">
      <div class="note"><strong>Corners (8–11–16):</strong> Liverpool 5.93/game at Anfield; Fulham 5.1 corners/game. Combined ~11 baseline. Over 9.5 hit in 6 of Fulham's last 7 games — they are extremely corner-active. Liverpool avg 4.46 corners against at home. H2H average of 3+ goals in most games means open attacking play = more corners. Median of 11 is the best supported figure of all four games.</div>
      <div class="note"><strong>Shots (20–27–38):</strong> This is the highest projected shot game of the four. Liverpool avg 17.7 at home; Fulham 13.2 away — combined baseline of ~31. UCL fatigue will suppress Liverpool's numbers somewhat (they're ranked 19th for high-intensity pressures in the PL since Matchweek 6). But Anfield's atmosphere and desperation after 3 losses will also drive volume. High end of 38 if Liverpool chase the game.</div>
      <div class="note"><strong>Offsides (3–6–11):</strong> Highest offside projection of the four games. Liverpool run a high defensive line; Fulham attack with pace (Jiménez runs behind, Wilson and Chukwueze exploit channels). Combined with Liverpool's attacking offside traps on corners and free kicks, both sets of forwards will be flagged repeatedly. H2H games average 4–5 combined offsides; fatigue-driven defensive line management raises this.</div>
      <div class="note"><strong>Fouls (17–23–32):</strong> Liverpool 10.4 fouls/game + Fulham 11.6 = 22 combined baseline. UCL fatigue from Liverpool means reactive defensive fouls. Jiménez alone generates 1.86 fouls/game. Median of 23 is anchored by strong data on both sides. Taylor can be strict — cards are likely.</div>
    </div>
  </div>

</div><!-- /dg -->
</div><!-- /page -->

<footer>
  <strong>Team Bilbo Statistical Analysis</strong><br>Predictions are statistical estimates based on actual data, H2H analysis and contextual factors. <strong>Not financial advice.</strong><br>· Saturday 11 April 2026 ·
</footer>

<script>
(function(){
  'use strict';

  // Scroll-triggered card animations
  var cards = document.querySelectorAll('.card');
  if('IntersectionObserver' in window){
    var obs = new IntersectionObserver(function(entries){
      entries.forEach(function(e){
        if(e.isIntersecting){
          e.target.classList.add('visible');
          obs.unobserve(e.target);
        }
      });
    },{threshold:0.06});
    cards.forEach(function(c){ obs.observe(c); });
  } else {
    cards.forEach(function(c){ c.classList.add('visible'); });
  }

  // Bar fill animations on scroll into view
  var predCards = ['pred-ars','pred-bre','pred-bur','pred-liv'];
  predCards.forEach(function(id){
    var el = document.getElementById(id);
    if(!el) return;
    var fired = false;
    var barObs = new IntersectionObserver(function(entries){
      entries.forEach(function(e){
        if(e.isIntersecting && !fired){
          fired = true;
          setTimeout(function(){
            el.querySelectorAll('.bar-fill[data-pct]').forEach(function(bar){
              bar.style.width = bar.getAttribute('data-pct') + '%';
            });
          }, 150);
          barObs.unobserve(e.target);
        }
      });
    },{threshold:0.2});
    barObs.observe(el);
  });

  // Stat cell count-up animation
  var acObs = new IntersectionObserver(function(entries){
    entries.forEach(function(e){
      if(e.isIntersecting){
        var valEl = e.target.querySelector('.val');
        if(valEl && !valEl.dataset.counted){
          valEl.dataset.counted = '1';
          var raw = valEl.textContent.trim();
          var isPercent = raw.indexOf('%') !== -1;
          var num = parseFloat(raw.replace('%',''));
          if(!isNaN(num)){
            var start = 0, dur = 850, step = num/(dur/16);
            var timer = setInterval(function(){
              start += step;
              if(start >= num){ start = num; clearInterval(timer); }
              var disp = (String(num).indexOf('.') !== -1)
                ? start.toFixed(1)
                : Math.round(start);
              valEl.textContent = disp + (isPercent ? '%' : '');
            },16);
          }
        }
        acObs.unobserve(e.target);
      }
    });
  },{threshold:0.6});
  document.querySelectorAll('.ac').forEach(function(el){ acObs.observe(el); });

})();
</script>
</body>
</html>
