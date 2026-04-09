<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>UEL QF Stats Predictor | Bologna·Villa · Porto·Forest · Freiburg·Celta</title>
<link rel="preconnect" href="https://fonts.googleapis.com">
<link href="https://fonts.googleapis.com/css2?family=Anton&family=Inter:wght@300;400;500;600;700&display=swap" rel="stylesheet">
<style>
/* ═══════════════════════════════════════
   TOKENS — Europa League editorial
═══════════════════════════════════════ */
:root{
  --bg:       #060608;
  --bg-2:     #0d0e13;
  --bg-3:     #13151d;
  --bg-4:     #191c28;
  --border:   rgba(255,255,255,0.07);
  --border-m: rgba(255,255,255,0.12);
  --text:     #c8cfe0;
  --muted:    #505870;
  --hi:       #8d97b8;
  /* UEL */
  --uel:      #f5582a;
  --uel-d:    #c73d16;
  --uel-g:    #ffd04a;
  /* match colours */
  --bol-r:    #cc0000;
  --vil-c:    #7b0041;
  --por-b:    #0e3799;
  --for-r:    #dd0000;
  --fre-r:    #bf1010;
  --fre-b:    #003087;
  --cel-c:    #70b2e0;
  --cel-b:    #003087;
  /* stat */
  --low:      #10d9a0;
  --med:      #f5ba32;
  --high:     #f55c2a;
  --card-y:   #ffe033;
  --r12: 10px;
}

*,*::before,*::after{margin:0;padding:0;box-sizing:border-box;}
html{scroll-behavior:smooth;}
body{
  font-family:'Inter',sans-serif;
  background:var(--bg);
  color:var(--text);
  min-height:100vh;
  font-size:14px;
  line-height:1.55;
  -webkit-font-smoothing:antialiased;
}

/* ═══ SITE HEADER ═══ */
.site-header{
  background:linear-gradient(180deg,#0d0808 0%,#110b06 60%,#06060a 100%);
  border-bottom:2px solid var(--uel);
  padding:22px 16px 18px;
  text-align:center;
  position:relative;overflow:hidden;
}
.site-header::before{
  content:'';position:absolute;inset:0;
  background:radial-gradient(ellipse 90% 250% at 50% -10%,rgba(245,88,42,0.12),transparent 70%);
  pointer-events:none;
}
.uel-tag{
  display:inline-flex;align-items:center;gap:8px;
  font-family:'Anton',sans-serif;font-size:11px;letter-spacing:3px;
  text-transform:uppercase;color:var(--uel);
  border:1px solid rgba(245,88,42,0.35);
  background:rgba(245,88,42,0.07);
  padding:4px 14px;border-radius:3px;margin-bottom:12px;
}
.site-header h1{
  font-family:'Anton',sans-serif;
  font-size:26px;letter-spacing:2px;color:#fff;
  text-transform:uppercase;line-height:1.1;
}
.site-header .sub{font-size:12px;color:var(--muted);margin-top:5px;letter-spacing:0.3px;}

/* ═══ MATCH NAV ═══ */
.match-nav{display:flex;justify-content:center;gap:8px;flex-wrap:wrap;margin-top:14px;}
.mnav{
  font-size:10px;font-weight:700;letter-spacing:0.8px;text-transform:uppercase;
  padding:5px 12px;border-radius:20px;border:1px solid rgba(245,88,42,0.3);
  color:var(--uel);background:rgba(245,88,42,0.06);text-decoration:none;
}

/* ═══ MATCH HERO ═══ */
.match-hero{
  padding:22px 16px 18px;
  border-bottom:1px solid var(--border-m);
  position:relative;overflow:hidden;
}
.mh-bol{background:linear-gradient(135deg,rgba(204,0,0,0.16) 0%,var(--bg-2) 40%,rgba(123,0,65,0.12) 100%);}
.mh-por{background:linear-gradient(135deg,rgba(14,55,153,0.18) 0%,var(--bg-2) 40%,rgba(221,0,0,0.12) 100%);}
.mh-fre{background:linear-gradient(135deg,rgba(191,16,16,0.16) 0%,var(--bg-2) 40%,rgba(112,178,224,0.12) 100%);}
.mh-glow{position:absolute;inset:0;background:radial-gradient(ellipse 60% 80% at 50% 50%,rgba(245,88,42,0.04),transparent 70%);pointer-events:none;}

.hero-row{max-width:560px;margin:0 auto;display:flex;align-items:center;justify-content:space-between;gap:10px;}
.hero-team{display:flex;flex-direction:column;align-items:center;gap:8px;flex:1;}

/* BADGE — real image from Wikimedia */
.badge-img-wrap{
  width:72px;height:72px;border-radius:50%;
  border:1px solid var(--border-m);
  background:rgba(255,255,255,0.04);
  display:flex;align-items:center;justify-content:center;
  overflow:hidden;
  filter:drop-shadow(0 4px 14px rgba(0,0,0,0.6));
  transition:transform .3s;flex-shrink:0;
}
.badge-img-wrap:hover{transform:scale(1.07);}
.badge-img-wrap img{width:52px;height:52px;object-fit:contain;}

.h-name{font-family:'Anton',sans-serif;font-size:13px;letter-spacing:0.8px;text-transform:uppercase;text-align:center;color:#fff;line-height:1.2;}
.h-pos{font-size:9px;color:var(--muted);text-transform:uppercase;letter-spacing:0.5px;}

.vs-col{display:flex;flex-direction:column;align-items:center;gap:5px;flex-shrink:0;}
.vs-big{font-family:'Anton',sans-serif;font-size:24px;color:rgba(255,255,255,0.1);letter-spacing:3px;}
.leg-tag{font-family:'Anton',sans-serif;font-size:9px;letter-spacing:2px;color:var(--uel-g);background:rgba(255,208,74,0.1);border:1px solid rgba(255,208,74,0.25);padding:2px 7px;border-radius:3px;}
.venue-txt{font-size:9px;color:var(--muted);text-align:center;line-height:1.5;}

/* ═══ PAGE ═══ */
.page{max-width:700px;margin:0 auto;padding:18px 14px 52px;}
.m-grid{display:flex;flex-direction:column;gap:0;}

/* card */
.card{background:var(--bg-2);border:1px solid var(--border);border-radius:var(--r12);overflow:hidden;margin-bottom:12px;}
.card-hd{padding:12px 16px 10px;border-bottom:1px solid var(--border);display:flex;align-items:center;gap:8px;}
.hd-dot{width:5px;height:5px;border-radius:50%;flex-shrink:0;}
.hd-title{font-family:'Anton',sans-serif;font-size:10px;letter-spacing:2px;text-transform:uppercase;color:var(--muted);flex:1;}
.hd-tag{font-size:9px;letter-spacing:0.8px;text-transform:uppercase;padding:2px 7px;border-radius:3px;border:1px solid;font-weight:700;}
.card-body{padding:14px 16px;}

/* callout */
.callout{background:rgba(255,255,255,0.022);border:1px solid var(--border-m);border-radius:8px;padding:12px 14px;font-size:12.5px;line-height:1.7;color:var(--hi);}
.callout strong{color:var(--uel-g);font-weight:700;}
.callout em{color:var(--text);font-style:normal;font-weight:600;}

/* form */
.form-cols{display:flex;flex-direction:column;gap:12px;}
.fcol{}
.team-lab{
  display:inline-flex;align-items:center;gap:5px;
  font-size:9px;font-weight:700;letter-spacing:1.2px;text-transform:uppercase;
  padding:2px 8px 2px 4px;border-radius:4px;margin-bottom:7px;border:1px solid;
}
.lab-bol{background:rgba(204,0,0,0.12);color:#f07070;border-color:rgba(204,0,0,0.28);}
.lab-vil{background:rgba(123,0,65,0.13);color:#e080b0;border-color:rgba(123,0,65,0.28);}
.lab-por{background:rgba(14,55,153,0.13);color:#7aafff;border-color:rgba(14,55,153,0.3);}
.lab-for{background:rgba(221,0,0,0.12);color:#f07070;border-color:rgba(221,0,0,0.28);}
.lab-fre{background:rgba(191,16,16,0.12);color:#f07070;border-color:rgba(191,16,16,0.28);}
.lab-cel{background:rgba(112,178,224,0.12);color:#80c8f0;border-color:rgba(112,178,224,0.28);}
.tl-img{width:14px;height:14px;object-fit:contain;}

.match-list{display:flex;flex-direction:column;gap:3px;}
.mr{
  display:grid;grid-template-columns:7px 44px 1fr auto;
  align-items:center;gap:8px;
  background:var(--bg-3);border:1px solid var(--border);
  border-radius:6px;padding:6px 9px;
}
.rd{width:7px;height:7px;border-radius:50%;}
.rd.W{background:var(--low);box-shadow:0 0 5px rgba(16,217,160,0.4);}
.rd.D{background:var(--med);}
.rd.L{background:var(--high);box-shadow:0 0 5px rgba(245,92,42,0.4);}
.ms{font-family:'Anton',sans-serif;font-size:14px;color:#fff;text-align:center;}
.mo{font-size:11.5px;color:var(--text);font-weight:600;overflow:hidden;text-overflow:ellipsis;white-space:nowrap;}
.mc{font-size:9px;color:var(--muted);text-transform:uppercase;letter-spacing:0.3px;text-align:right;white-space:nowrap;}
.uel-note{font-size:9px;color:var(--uel-g);font-style:italic;}

.f-leg{display:flex;gap:12px;flex-wrap:wrap;margin-top:8px;}
.fl{display:flex;align-items:center;gap:4px;font-size:10px;color:var(--muted);}
.fld{width:7px;height:7px;border-radius:50%;}

/* avg */
.avg-pair{display:flex;flex-direction:column;gap:10px;}
.a-grp{}
.a-grp-lbl{font-family:'Anton',sans-serif;font-size:9px;letter-spacing:1.2px;text-transform:uppercase;margin-bottom:7px;}
.avg-g{display:grid;grid-template-columns:repeat(4,1fr);gap:5px;}
.ac{background:var(--bg-3);border:1px solid var(--border);border-radius:7px;padding:8px 5px 7px;text-align:center;}
.av{font-family:'Anton',sans-serif;font-size:20px;color:#fff;line-height:1;}
.al{font-size:8.5px;color:var(--muted);margin-top:2px;text-transform:uppercase;letter-spacing:0.5px;line-height:1.3;}

/* h2h */
.h2h-bar{background:var(--bg-3);border:1px solid var(--border);border-radius:7px;padding:12px 10px;display:flex;align-items:center;justify-content:space-between;gap:4px;}
.hs{text-align:center;flex:1;}
.hn{font-family:'Anton',sans-serif;font-size:26px;line-height:1;}
.hl{font-size:8.5px;color:var(--muted);text-transform:uppercase;letter-spacing:0.6px;margin-top:3px;}
.hd{width:1px;height:34px;background:var(--border);flex-shrink:0;}

.h2h-rows{display:flex;flex-direction:column;gap:4px;margin-top:10px;}
.h2h-r{
  display:grid;grid-template-columns:1fr auto 1fr;
  align-items:center;gap:8px;
  background:var(--bg-4);border:1px solid var(--border);border-radius:5px;
  padding:6px 9px;
}
.rh{font-size:11.5px;font-weight:600;color:var(--text);text-align:left;white-space:nowrap;overflow:hidden;text-overflow:ellipsis;}
.rs{font-family:'Anton',sans-serif;font-size:14px;color:#fff;text-align:center;white-space:nowrap;}
.ra{font-size:11.5px;font-weight:600;color:var(--text);text-align:right;white-space:nowrap;overflow:hidden;text-overflow:ellipsis;}
.rsub{font-size:9px;color:var(--muted);text-transform:uppercase;letter-spacing:0.3px;grid-column:1/-1;text-align:center;margin-top:-2px;}

/* pred table */
.pred-leg{display:flex;gap:14px;flex-wrap:wrap;margin-bottom:12px;}
.pli{display:flex;align-items:center;gap:5px;font-size:10.5px;color:var(--muted);}
.pld{width:8px;height:8px;border-radius:50%;}

.pw{overflow-x:auto;-webkit-overflow-scrolling:touch;}
.pt{width:100%;border-collapse:collapse;table-layout:fixed;min-width:320px;}
.pt col.cm{width:30%;}
.pt col.cl{width:16%;}
.pt col.cn{width:16%;}
.pt col.ch{width:16%;}
.pt col.cb{width:22%;}

.pt thead th{
  font-family:'Anton',sans-serif;font-size:9.5px;letter-spacing:1.5px;
  text-transform:uppercase;color:var(--muted);
  padding:0 0 9px;text-align:left;white-space:nowrap;overflow:hidden;
}
.pt thead th:not(:first-child){text-align:center;}
.pt thead th.th-m{color:var(--med);}

.pt tbody td{
  padding:7px 3px;border-bottom:1px solid rgba(255,255,255,0.03);
  vertical-align:middle;overflow:hidden;
}
.pt tbody tr:last-child td{border-bottom:none;}
.pt tbody td.cmc{color:var(--hi);font-size:12px;padding-left:0;}
.pt tbody td:not(.cmc){text-align:center;}

.lv{font-family:'Anton',sans-serif;font-size:18px;color:var(--low);line-height:1;}
.mv{font-family:'Anton',sans-serif;font-size:18px;color:var(--med);line-height:1;}
.hv{font-family:'Anton',sans-serif;font-size:18px;color:var(--high);line-height:1;}

.bw{width:80%;max-width:88px;height:4px;background:rgba(255,255,255,0.06);border-radius:3px;overflow:hidden;margin:0 auto;display:block;}
.bf{display:block;height:100%;border-radius:3px;background:linear-gradient(90deg,var(--low),var(--high));}

/* yellow card block */
.yc-grid{display:flex;flex-direction:column;gap:7px;}
.yc-row{
  display:flex;align-items:flex-start;gap:10px;
  background:var(--bg-3);border:1px solid var(--border);
  border-radius:7px;padding:9px 11px;
}
.yc-icon{font-size:16px;flex-shrink:0;margin-top:1px;}
.yc-info{flex:1;min-width:0;}
.yc-name{font-size:12.5px;font-weight:700;color:#fff;}
.yc-reason{font-size:11px;color:var(--muted);margin-top:2px;line-height:1.4;}
.yc-risk{
  font-family:'Anton',sans-serif;font-size:9px;letter-spacing:1px;
  text-transform:uppercase;padding:2px 7px;border-radius:3px;
  flex-shrink:0;align-self:center;
}
.risk-h{background:rgba(245,92,42,0.15);color:var(--high);border:1px solid rgba(245,92,42,0.3);}
.risk-m{background:rgba(245,186,50,0.12);color:var(--med);border:1px solid rgba(245,186,50,0.28);}

/* section divider */
.s-div{text-align:center;padding:20px 0 10px;position:relative;}
.s-div::before{content:'';position:absolute;left:0;right:0;top:50%;height:1px;background:var(--uel);opacity:0.18;}
.s-div-in{
  display:inline-flex;align-items:center;gap:10px;
  background:var(--bg);padding:0 12px;position:relative;
  font-family:'Anton',sans-serif;font-size:9px;letter-spacing:3px;
  text-transform:uppercase;color:var(--uel);
}

/* notes */
.note{margin-bottom:9px;font-size:12.5px;line-height:1.65;color:var(--hi);}
.note:last-child{margin-bottom:0;}
.note strong{color:var(--uel-g);font-weight:700;}

/* footer */
footer{text-align:center;padding:16px 14px;font-size:11.5px;color:rgba(80,88,112,0.45);border-top:1px solid var(--border);}

/* ═══ TABLET 640px+ ═══ */
@media(min-width:640px){
  body{font-size:15px;}
  .page{max-width:920px;padding:22px 22px 60px;}
  .site-header{padding:26px 22px 22px;}
  .site-header h1{font-size:32px;}
  .match-hero{padding:26px 22px 20px;}
  .hero-row{max-width:620px;}
  .badge-img-wrap{width:82px;height:82px;}
  .badge-img-wrap img{width:58px;height:58px;}
  .h-name{font-size:15px;}
  .vs-big{font-size:30px;}
  .card-hd{padding:13px 20px 11px;}
  .card-body{padding:16px 20px;}
  .form-cols{flex-direction:row;gap:14px;}
  .fcol{flex:1;min-width:0;}
  .avg-pair{flex-direction:row;gap:14px;}
  .a-grp{flex:1;}
  .av{font-size:22px;}
  .hn{font-size:30px;}
  .lv,.mv,.hv{font-size:21px;}
  .pt tbody td{padding:8px 5px;}
  .bw{max-width:100px;height:5px;}
  .callout{font-size:13.5px;}
  .note{font-size:13.5px;}
}

/* ═══ DESKTOP 1060px+ ═══ */
@media(min-width:1060px){
  .page{max-width:1380px;padding:28px 40px 68px;}
  .site-header{padding:28px 40px 24px;}
  .site-header h1{font-size:38px;}
  .match-hero{padding:28px 40px 22px;}
  .hero-row{max-width:680px;}
  .badge-img-wrap{width:90px;height:90px;}
  .badge-img-wrap img{width:64px;height:64px;}
  .m-grid{display:grid;grid-template-columns:1fr 1fr;gap:20px;align-items:start;}
  .m-grid .fw{grid-column:1/-1;}
  .card-hd{padding:14px 22px 12px;}
  .card-body{padding:18px 22px;}
  .av{font-size:24px;}
  .lv,.mv,.hv{font-size:22px;}
  .hn{font-size:32px;}
  .bw{max-width:90px;}
}

/* ═══ WIDE 1380px+ ═══ */
@media(min-width:1380px){
  .page{max-width:1520px;padding:32px 60px 76px;}
  .site-header{padding:30px 60px 24px;}
  .match-hero{padding:30px 60px 22px;}
  .hero-row{max-width:760px;}
  .m-grid{gap:26px;}
}
</style>
</head>
<body>

<!-- ══════════ HEADER ══════════ -->
<header class="site-header">
  <div class="uel-tag">🔶 UEFA Europa League · Quarter-Finals 🔶<br>· 9 April 2026 ·</div>
  <p class="sub">Last 5 form &nbsp;·&nbsp; Season averages &nbsp;·&nbsp; H2H &nbsp;·&nbsp; Weighted Low / Median / High &nbsp;·&nbsp; Yellow Card risks</p>
  <div class="match-nav">
    <a href="#bol" class="mnav">Bologna vs Aston Villa</a>
    <a href="#por" class="mnav">Porto vs Nottingham Forest</a>
    <a href="#fre" class="mnav">Freiburg vs Celta Vigo</a>
  </div>
</header>

<!-- ═══════════════════════════════════════
     MATCH 1: BOLOGNA vs ASTON VILLA
═══════════════════════════════════════ -->
<div class="match-hero mh-bol" id="bol">
  <div class="mh-glow"></div>
  <div class="hero-row">

    <div class="hero-team">
      <div class="badge-img-wrap">
        <img src="https://upload.wikimedia.org/wikipedia/commons/0/0b/Soccer.svg"
             alt="Bologna FC" onerror="this.style.display='none'">
      </div>
      <div class="h-name">Bologna FC</div>
      <div class="h-pos">Serie A 8th · Home</div>
    </div>

    <div class="vs-col">
      <div class="vs-big">VS</div>
      <div class="leg-tag">1st Leg</div>
      <div class="venue-txt">Stadio Dall'Ara, Bologna<br>Thu 9 Apr · 6:45pm BST</div>
    </div>

    <div class="hero-team">
      <div class="badge-img-wrap">
        <img src="https://upload.wikimedia.org/wikipedia/commons/0/0b/Soccer.svg"
             alt="Aston Villa" onerror="this.style.display='none'">
      </div>
      <div class="h-name">Aston Villa</div>
      <div class="h-pos">PL 6th · Away</div>
    </div>

  </div>
</div>

<div class="page">
<div class="m-grid">

  <!-- CONTEXT -->
  <div class="card fw">
    <div class="card-hd">
      <div class="hd-dot" style="background:var(--uel-g)"></div>
      <div class="hd-title">Match Context</div>
      <div class="hd-tag" style="color:var(--uel-g);border-color:rgba(255,208,74,0.28);background:rgba(255,208,74,0.07)">3rd meeting in 2 seasons</div>
    </div>
    <div class="card-body">
      <div class="callout">
        Villa have beaten Bologna in <strong>both previous meetings without conceding</strong> (1–0 in EL league phase Sep 2025; 1–0 in the 2023–24 Conference League). Unai Emery — a <em>four-time Europa League winner</em> — has Villa on a <strong>7-game UEL winning streak</strong>, the longest in club history. Bologna are ranked <strong>1st in the UEL table</strong> after 11 games unbeaten, beating Roma 5–4 on aggregate in a dramatic R16 comeback. Key absences: Bologna miss GK <strong>Skorupski (hamstring)</strong> and are without Dallinga, Odgaard, Lykogiannis, Domínguez, and Vitík (suspended). Villa without Kamara and Sancho. <strong>Referee:</strong> Sandro Schärer (Switzerland) — averages 4.4 yellows/UEL game.
      </div>
    </div>
  </div>

  <!-- FORM -->
  <div class="card fw">
    <div class="card-hd">
      <div class="hd-dot" style="background:#f07070"></div>
      <div class="hd-title">Last 5 Matches — All Competitions</div>
    </div>
    <div class="card-body">
      <div class="form-cols">
        <div class="fcol">
          <div class="team-lab lab-bol">
            <img class="tl-img" src="https://upload.wikimedia.org/wikipedia/commons/0/0b/Soccer.svg" alt="">
            Bologna
          </div>
          <div class="match-list">
            <div class="mr"><div class="rd W"></div><div class="ms">2–1</div><div class="mo">Cremonese</div><div class="mc">SA · Away</div></div>
            <div class="mr"><div class="rd W"></div><div class="ms">4–3</div><div class="mo">Roma</div><div class="mc">UEL R16 · Away <span class="uel-note">AET</span></div></div>
            <div class="mr"><div class="rd D"></div><div class="ms">3–3</div><div class="mo">Roma</div><div class="mc">UEL R16 · Home</div></div>
            <div class="mr"><div class="rd W"></div><div class="ms">2–0</div><div class="mo">Lecce</div><div class="mc">SA · Home</div></div>
            <div class="mr"><div class="rd L"></div><div class="ms">0–2</div><div class="mo">AC Milan</div><div class="mc">SA · Away</div></div>
          </div>
        </div>
        <div class="fcol">
          <div class="team-lab lab-vil">
            <img class="tl-img" src="https://upload.wikimedia.org/wikipedia/commons/0/0b/Soccer.svg" alt="">
            Aston Villa
          </div>
          <div class="match-list">
            <div class="mr"><div class="rd W"></div><div class="ms">2–0</div><div class="mo">West Ham</div><div class="mc">PL · Home</div></div>
            <div class="mr"><div class="rd W"></div><div class="ms">2–0</div><div class="mo">Lille</div><div class="mc">UEL R16 · Home</div></div>
            <div class="mr"><div class="rd W"></div><div class="ms">1–0</div><div class="mo">Lille</div><div class="mc">UEL R16 · Away</div></div>
            <div class="mr"><div class="rd W"></div><div class="ms">3–1</div><div class="mo">Tottenham</div><div class="mc">PL · Away</div></div>
            <div class="mr"><div class="rd L"></div><div class="ms">0–1</div><div class="mo">Arsenal</div><div class="mc">PL · Home</div></div>
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

  <!-- AVERAGES -->
  <div class="card fw">
    <div class="card-hd">
      <div class="hd-dot" style="background:#a78bfa"></div>
      <div class="hd-title">Season Averages per Match — UEL 25/26</div>
    </div>
    <div class="card-body">
      <div class="avg-pair">
        <div class="a-grp">
          <div class="a-grp-lbl" style="color:#f07070">Bologna — Last 10 UEL/Serie A</div>
          <div class="avg-g">
            <div class="ac"><div class="av">13.8</div><div class="al">Shots</div></div>
            <div class="ac"><div class="av">4.6</div><div class="al">SOT</div></div>
            <div class="ac"><div class="av">9.2</div><div class="al">Corners/Gm <span style="font-size:7px">(home UEL)</span></div></div>
            <div class="ac"><div class="av">5.1</div><div class="al">Corners (avg)</div></div>
          </div>
          <div class="avg-g" style="margin-top:5px">
            <div class="ac"><div class="av">52%</div><div class="al">Possession</div></div>
            <div class="ac"><div class="av">1.3</div><div class="al">Goals/Gm</div></div>
            <div class="ac"><div class="av">11</div><div class="al">UEL Unbeaten</div></div>
            <div class="ac"><div class="av">5</div><div class="al">Bernardeschi Gls</div></div>
          </div>
        </div>
        <div class="a-grp">
          <div class="a-grp-lbl" style="color:#e080b0">Aston Villa — Last 10 UEL/PL</div>
          <div class="avg-g">
            <div class="ac"><div class="av">13.7</div><div class="al">Shots</div></div>
            <div class="ac"><div class="av">3.7</div><div class="al">SOT</div></div>
            <div class="ac"><div class="av">5.5</div><div class="al">Corners</div></div>
            <div class="ac"><div class="av">4.7</div><div class="al">Corners vs</div></div>
          </div>
          <div class="avg-g" style="margin-top:5px">
            <div class="ac"><div class="av">55%</div><div class="al">Possession</div></div>
            <div class="ac"><div class="av">1.0</div><div class="al">Goals/Gm</div></div>
            <div class="ac"><div class="av">7</div><div class="al">UEL Wins Streak</div></div>
            <div class="ac"><div class="av">4</div><div class="al">CS vs Italian clubs</div></div>
          </div>
        </div>
      </div>
    </div>
  </div>

  <!-- H2H -->
  <div class="card fw">
    <div class="card-hd">
      <div class="hd-dot" style="background:var(--high)"></div>
      <div class="hd-title">Head to Head — Both Previous Meetings</div>
    </div>
    <div class="card-body">
      <div class="h2h-bar">
        <div class="hs"><div class="hn" style="color:#f07070">0</div><div class="hl">Bologna Wins</div></div>
        <div class="hd"></div>
        <div class="hs"><div class="hn" style="color:var(--med)">0</div><div class="hl">Draws</div></div>
        <div class="hd"></div>
        <div class="hs"><div class="hn" style="color:#e080b0">2</div><div class="hl">Villa Wins</div></div>
        <div class="hd"></div>
        <div class="hs"><div class="hn">1.5</div><div class="hl">Avg Goals</div></div>
      </div>
      <div class="h2h-rows">
        <div class="h2h-r">
          <div class="rh">Aston Villa</div><div class="rs">1–0</div><div class="ra">Bologna</div>
          <div class="rsub">UEL League Phase · Villa Park · Sep 2025 (McGinn 13')</div>
        </div>
        <div class="h2h-r">
          <div class="rh">Aston Villa</div><div class="rs">2–0</div><div class="ra">Bologna</div>
          <div class="rsub">UECL Quarter-Final 2nd Leg · Villa Park · Apr 2024</div>
        </div>
      </div>
      <p style="font-size:11px;color:var(--muted);margin-top:8px;">Villa have kept a clean sheet in both meetings. Under 2.5 goals in both H2H games. Both sides' previous encounters have been low-scoring, tactically tight. Bologna have never beaten Villa in a competitive match.</p>
    </div>
  </div>

  <!-- PREDICTIONS -->
  <div class="card fw">
    <div class="card-hd">
      <div class="hd-dot" style="background:var(--low)"></div>
      <div class="hd-title">Weighted Predictions — Bologna vs Villa (Both Teams)</div>
    </div>
    <div class="card-body">
      <div class="pred-leg">
        <div class="pli"><div class="pld" style="background:var(--low)"></div><span style="color:var(--low);font-weight:700">Low</span></div>
        <div class="pli"><div class="pld" style="background:var(--med)"></div><span style="color:var(--med);font-weight:700">Median</span></div>
        <div class="pli"><div class="pld" style="background:var(--high)"></div><span style="color:var(--high);font-weight:700">High</span></div>
      </div>
      <div class="pw">
      <table class="pt">
        <colgroup><col class="cm"><col class="cl"><col class="cn"><col class="ch"><col class="cb"></colgroup>
        <thead><tr><th>Metric</th><th style="color:var(--low)">Low</th><th class="th-m">Median</th><th style="color:var(--high)">High</th><th style="text-align:center;color:var(--muted)">Intensity</th></tr></thead>
        <tbody>
          <tr><td class="cmc">Corners</td>        <td><span class="lv">8</span></td><td><span class="mv">11</span></td><td><span class="hv">16</span></td><td><div class="bw"><div class="bf" style="width:64%"></div></div></td></tr>
          <tr><td class="cmc">Total Shots</td>    <td><span class="lv">18</span></td><td><span class="mv">24</span></td><td><span class="hv">32</span></td><td><div class="bw"><div class="bf" style="width:62%"></div></div></td></tr>
          <tr><td class="cmc">Shots on Target</td><td><span class="lv">5</span></td><td><span class="mv">8</span></td><td><span class="hv">13</span></td><td><div class="bw"><div class="bf" style="width:54%"></div></div></td></tr>
          <tr><td class="cmc">Fouls</td>          <td><span class="lv">18</span></td><td><span class="mv">25</span></td><td><span class="hv">34</span></td><td><div class="bw"><div class="bf" style="width:68%"></div></div></td></tr>
          <tr><td class="cmc">Throw-ins</td>      <td><span class="lv">34</span></td><td><span class="mv">44</span></td><td><span class="hv">56</span></td><td><div class="bw"><div class="bf" style="width:62%"></div></div></td></tr>
          <tr><td class="cmc">Goal Kicks</td>     <td><span class="lv">14</span></td><td><span class="mv">20</span></td><td><span class="hv">28</span></td><td><div class="bw"><div class="bf" style="width:58%"></div></div></td></tr>
          <tr><td class="cmc">Tackles</td>        <td><span class="lv">24</span></td><td><span class="mv">32</span></td><td><span class="hv">44</span></td><td><div class="bw"><div class="bf" style="width:70%"></div></div></td></tr>
          <tr><td class="cmc">Offsides</td>       <td><span class="lv">2</span></td><td><span class="mv">4</span></td><td><span class="hv">8</span></td><td><div class="bw"><div class="bf" style="width:42%"></div></div></td></tr>
        </tbody>
      </table>
      </div>
    </div>
  </div>

  <!-- YELLOW CARDS -->
  <div class="card fw">
    <div class="card-hd">
      <div class="hd-dot" style="background:var(--card-y)"></div>
      <div class="hd-title">🟨 Yellow Card Risk Players</div>
    </div>
    <div class="card-body">
      <div class="yc-grid">
        <div class="yc-row">
          <div class="yc-icon">🟨</div>
          <div class="yc-info">
            <div class="yc-name">Lewis Ferguson (Bologna, MF)</div>
            <div class="yc-reason">Played all 12 UEL games, combative central midfielder averaging 1.9 fouls/game. Will be tasked with disrupting Villa's possession — crucial and aggressive role. High press triggers.</div>
          </div>
          <div class="yc-risk risk-h">HIGH</div>
        </div>
        <div class="yc-row">
          <div class="yc-icon">🟨</div>
          <div class="yc-info">
            <div class="yc-name">Nikola Moro (Bologna, MF)</div>
            <div class="yc-reason">Bologna's defensive midfielder with an aggressive playing style. 3 yellow cards in UEL this season. Will likely target breaking up Villa's build-up play early.</div>
          </div>
          <div class="yc-risk risk-h">HIGH</div>
        </div>
        <div class="yc-row">
          <div class="yc-icon">🟨</div>
          <div class="yc-info">
            <div class="yc-name">Youri Tielemans (Aston Villa, MF)</div>
            <div class="yc-reason">Engine of Villa's midfield, tends to pick up tactical fouls. Has been booked 4 times in UEL. Will be tested by Bologna's high pressing game in a tight arena.</div>
          </div>
          <div class="yc-risk risk-h">HIGH</div>
        </div>
        <div class="yc-row">
          <div class="yc-icon">🟨</div>
          <div class="yc-info">
            <div class="yc-name">Jhon Lucumí (Bologna, CB)</div>
            <div class="yc-reason">Physical centre-back who likes to step out and challenge. Without Skorupski in goal, the defence will be under pressure to protect the inexperienced Ravaglia — leading to cynical fouls.</div>
          </div>
          <div class="yc-risk risk-m">MED</div>
        </div>
        <div class="yc-row">
          <div class="yc-icon">🟨</div>
          <div class="yc-info">
            <div class="yc-name">Pau Torres (Aston Villa, CB)</div>
            <div class="yc-reason">Elegant but can be caught by pace in transition. Santiago Castro and Jonathan Rowe will test him with runs in behind — risks a booking stopping a counter-attack.</div>
          </div>
          <div class="yc-risk risk-m">MED</div>
        </div>
      </div>
    </div>
  </div>

  <!-- NOTES -->
  <div class="card fw">
    <div class="card-hd"><div class="hd-dot" style="background:#60a5fa"></div><div class="hd-title">Analytical Notes</div></div>
    <div class="card-body">
      <div class="note"><strong>Corners (8–11–16):</strong> Bologna earn an extraordinary <em>9.2 corners/game at home in UEL</em> — the highest individual home average in this competition. Villa average 5.5 corners/game and allow 4.7 against. Combined baseline ~14, but Villa's tight defensive shape tends to reduce corner opportunities against them (H2H data: both meetings settled with tight scores, few corners). Median of 11 weighted down by Villa's defensive organisation.</div>
      <div class="note"><strong>Shots (18–24–32):</strong> Bologna lead the UEL in total shots (competition-leading shot tally per WhoScored); Villa allow 11.2 attempts/game. Combined baseline ~25. H2H meetings have been tight (under 2.5 goals in both), suggesting the high end is unlikely. Weighted median of 24.</div>
      <div class="note"><strong>Fouls (18–25–34):</strong> Referee Schärer averages 4.4 yellows/UEL game — high card count expected. Matches involving Bologna average 4.3 cautions; Villa 3.8. Bologna's pressing game produces frequent fouls against them, and their depleted midfield (Vitík suspended) means extra physicality from the remaining players. Median weighted to 25.</div>
      <div class="note"><strong>Tackles (24–32–44):</strong> Bologna's high-energy pressing and Villa's technical counter-press create a high-tackle environment. Under Emery, Villa know how to win the ball back and Tielemans is aggressive in the tackle. Bologna's home urgency to upset Villa inflates this. Median of 32.</div>
    </div>
  </div>

</div><!-- /m-grid -->

<!-- ─ DIVIDER ─ -->
<div class="s-div"><div class="s-div-in">★ Match 2 ★</div></div>

</div><!-- /page -->

<!-- ═══════════════════════════════════════
     MATCH 2: PORTO vs NOTTINGHAM FOREST
═══════════════════════════════════════ -->
<div class="match-hero mh-por" id="por">
  <div class="mh-glow"></div>
  <div class="hero-row">

    <div class="hero-team">
      <div class="badge-img-wrap">
        <img src="https://upload.wikimedia.org/wikipedia/commons/0/0b/Soccer.svg"
             alt="FC Porto" onerror="this.style.display='none'">
      </div>
      <div class="h-name">FC Porto</div>
      <div class="h-pos">Primeira Liga · 1st · Home</div>
    </div>

    <div class="vs-col">
      <div class="vs-big">VS</div>
      <div class="leg-tag">1st Leg</div>
      <div class="venue-txt">Estádio do Dragão<br>Thu 9 Apr · 8pm BST</div>
    </div>

    <div class="hero-team">
      <div class="badge-img-wrap">
        <img src="https://upload.wikimedia.org/wikipedia/commons/0/0b/Soccer.svg"
             alt="Nottingham Forest" onerror="this.style.display='none'">
      </div>
      <div class="h-name">Nottm Forest</div>
      <div class="h-pos">PL 16th · 3 pts from drop · Away</div>
    </div>

  </div>
</div>

<div class="page">
<div class="m-grid">

  <!-- CONTEXT -->
  <div class="card fw">
    <div class="card-hd">
      <div class="hd-dot" style="background:var(--uel-g)"></div>
      <div class="hd-title">Match Context</div>
      <div class="hd-tag" style="color:var(--uel-g);border-color:rgba(255,208,74,0.28);background:rgba(255,208,74,0.07)">Vitor Pereira returns to Porto</div>
    </div>
    <div class="card-body">
      <div class="callout">
        <strong>Forest beat Porto 2–0 at the City Ground</strong> in the UEL group phase in October — their only previous meeting. Forest's manager Vítor Pereira managed Porto to <em>back-to-back league titles in 2012 and 2013</em> and receives a hero's welcome at the Dragão. Porto have won <strong>all five home UEL games</strong> this season (scoring in the first half of every one); Forest have lost 8 consecutive UEFA two-legged ties against Portuguese clubs. Forest arrive with heavy absentees: <strong>Elliot Anderson (suspended), Hutchinson, Boly, Cunha, Aina, Victor, Savona</strong> all out. Porto also missing top scorer Samu Aghehowa and Luuk de Jong. Porto lead the Primeira Liga by <strong>5 points with a game in hand</strong>.
      </div>
    </div>
  </div>

  <!-- FORM -->
  <div class="card fw">
    <div class="card-hd">
      <div class="hd-dot" style="background:#7aafff"></div>
      <div class="hd-title">Last 5 Matches — All Competitions</div>
    </div>
    <div class="card-body">
      <div class="form-cols">
        <div class="fcol">
          <div class="team-lab lab-por">
            <img class="tl-img" src="https://upload.wikimedia.org/wikipedia/commons/0/0b/Soccer.svg" alt="">
            FC Porto
          </div>
          <div class="match-list">
            <div class="mr"><div class="rd D"></div><div class="ms">2–2</div><div class="mo">Famalicão</div><div class="mc">PriLiga · Home</div></div>
            <div class="mr"><div class="rd W"></div><div class="ms">2–0</div><div class="mo">Stuttgart</div><div class="mc">UEL R16 · Home</div></div>
            <div class="mr"><div class="rd W"></div><div class="ms">2–1</div><div class="mo">Stuttgart</div><div class="mc">UEL R16 · Away</div></div>
            <div class="mr"><div class="rd W"></div><div class="ms">3–0</div><div class="mo">Moreirense</div><div class="mc">PriLiga · Away</div></div>
            <div class="mr"><div class="rd W"></div><div class="ms">2–1</div><div class="mo">Braga</div><div class="mc">PriLiga · Home</div></div>
          </div>
        </div>
        <div class="fcol">
          <div class="team-lab lab-for">
            <img class="tl-img" src="https://upload.wikimedia.org/wikipedia/commons/0/0b/Soccer.svg" alt="">
            Nottingham Forest
          </div>
          <div class="match-list">
            <div class="mr"><div class="rd W"></div><div class="ms">3–0</div><div class="mo">Tottenham</div><div class="mc">PL · Away</div></div>
            <div class="mr"><div class="rd W"></div><div class="ms">2–1</div><div class="mo">Midtjylland</div><div class="mc">UEL R16 · Away</div></div>
            <div class="mr"><div class="rd D"></div><div class="ms">1–1</div><div class="mo">Midtjylland</div><div class="mc">UEL R16 · Home <span class="uel-note">[pens]</span></div></div>
            <div class="mr"><div class="rd L"></div><div class="ms">0–1</div><div class="mo">Fulham</div><div class="mc">PL · Away</div></div>
            <div class="mr"><div class="rd L"></div><div class="ms">1–2</div><div class="mo">Brighton</div><div class="mc">PL · Home</div></div>
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

  <!-- AVERAGES -->
  <div class="card fw">
    <div class="card-hd">
      <div class="hd-dot" style="background:#a78bfa"></div>
      <div class="hd-title">Season Averages per Match — UEL 25/26</div>
    </div>
    <div class="card-body">
      <div class="avg-pair">
        <div class="a-grp">
          <div class="a-grp-lbl" style="color:#7aafff">FC Porto — Last 10 UEL/Liga</div>
          <div class="avg-g">
            <div class="ac"><div class="av">12.7</div><div class="al">Shots</div></div>
            <div class="ac"><div class="av">4.9</div><div class="al">SOT</div></div>
            <div class="ac"><div class="av">4.6</div><div class="al">Corners</div></div>
            <div class="ac"><div class="av">1.9</div><div class="al">Goals/Gm</div></div>
          </div>
          <div class="avg-g" style="margin-top:5px">
            <div class="ac"><div class="av">48%</div><div class="al">Possession</div></div>
            <div class="ac"><div class="av">5–0</div><div class="al">UEL Home W</div></div>
            <div class="ac"><div class="av">7</div><div class="al">UEL Unbeaten</div></div>
            <div class="ac"><div class="av">4</div><div class="al">Clean sheets</div></div>
          </div>
        </div>
        <div class="a-grp">
          <div class="a-grp-lbl" style="color:#f07070">Nottm Forest — Last 10 UEL/PL</div>
          <div class="avg-g">
            <div class="ac"><div class="av">11.4</div><div class="al">Shots</div></div>
            <div class="ac"><div class="av">4.2</div><div class="al">SOT</div></div>
            <div class="ac"><div class="av">5.7</div><div class="al">Corners<br>(away)</div></div>
            <div class="ac"><div class="av">1.4</div><div class="al">Goals/Gm</div></div>
          </div>
          <div class="avg-g" style="margin-top:5px">
            <div class="ac"><div class="av">44%</div><div class="al">Possession</div></div>
            <div class="ac"><div class="av">7</div><div class="al">Igor Jesus Gls</div></div>
            <div class="ac"><div class="av">18</div><div class="al">2-leg wins ever</div></div>
            <div class="ac"><div class="av">16th</div><div class="al">PL Position</div></div>
          </div>
        </div>
      </div>
    </div>
  </div>

  <!-- H2H -->
  <div class="card fw">
    <div class="card-hd">
      <div class="hd-dot" style="background:var(--high)"></div>
      <div class="hd-title">Head to Head — Only 1 Previous Meeting</div>
    </div>
    <div class="card-body">
      <div class="h2h-bar">
        <div class="hs"><div class="hn" style="color:#7aafff">0</div><div class="hl">Porto Wins</div></div>
        <div class="hd"></div>
        <div class="hs"><div class="hn" style="color:var(--med)">0</div><div class="hl">Draws</div></div>
        <div class="hd"></div>
        <div class="hs"><div class="hn" style="color:#f07070">1</div><div class="hl">Forest Wins</div></div>
        <div class="hd"></div>
        <div class="hs"><div class="hn">2.0</div><div class="hl">Goals</div></div>
      </div>
      <div class="h2h-rows">
        <div class="h2h-r">
          <div class="rh">Nottm Forest</div><div class="rs">2–0</div><div class="ra">FC Porto</div>
          <div class="rsub">UEL League Phase · City Ground · Oct 2025 (2 penalties)</div>
        </div>
      </div>
      <p style="font-size:11px;color:var(--muted);margin-top:8px;">Only 1 previous meeting — Forest won with two penalties in October. Porto have lost their last 8 UEFA two-legged ties against English clubs. However, Porto won the first game at the Dragão vs Forest (5–3) in a pre-season friendly, and their home UEL record this season is impeccable: W5 D0 L0.</p>
    </div>
  </div>

  <!-- PREDICTIONS -->
  <div class="card fw">
    <div class="card-hd">
      <div class="hd-dot" style="background:var(--low)"></div>
      <div class="hd-title">Weighted Predictions — Porto vs Forest (Both Teams)</div>
    </div>
    <div class="card-body">
      <div class="pred-leg">
        <div class="pli"><div class="pld" style="background:var(--low)"></div><span style="color:var(--low);font-weight:700">Low</span></div>
        <div class="pli"><div class="pld" style="background:var(--med)"></div><span style="color:var(--med);font-weight:700">Median</span></div>
        <div class="pli"><div class="pld" style="background:var(--high)"></div><span style="color:var(--high);font-weight:700">High</span></div>
      </div>
      <div class="pw">
      <table class="pt">
        <colgroup><col class="cm"><col class="cl"><col class="cn"><col class="ch"><col class="cb"></colgroup>
        <thead><tr><th>Metric</th><th style="color:var(--low)">Low</th><th class="th-m">Median</th><th style="color:var(--high)">High</th><th style="text-align:center;color:var(--muted)">Intensity</th></tr></thead>
        <tbody>
          <tr><td class="cmc">Corners</td>        <td><span class="lv">7</span></td><td><span class="mv">9</span></td><td><span class="hv">14</span></td><td><div class="bw"><div class="bf" style="width:52%"></div></div></td></tr>
          <tr><td class="cmc">Total Shots</td>    <td><span class="lv">17</span></td><td><span class="mv">23</span></td><td><span class="hv">31</span></td><td><div class="bw"><div class="bf" style="width:60%"></div></div></td></tr>
          <tr><td class="cmc">Shots on Target</td><td><span class="lv">5</span></td><td><span class="mv">9</span></td><td><span class="hv">14</span></td><td><div class="bw"><div class="bf" style="width:56%"></div></div></td></tr>
          <tr><td class="cmc">Fouls</td>          <td><span class="lv">20</span></td><td><span class="mv">27</span></td><td><span class="hv">36</span></td><td><div class="bw"><div class="bf" style="width:72%"></div></div></td></tr>
          <tr><td class="cmc">Throw-ins</td>      <td><span class="lv">32</span></td><td><span class="mv">42</span></td><td><span class="hv">54</span></td><td><div class="bw"><div class="bf" style="width:60%"></div></div></td></tr>
          <tr><td class="cmc">Goal Kicks</td>     <td><span class="lv">14</span></td><td><span class="mv">19</span></td><td><span class="hv">26</span></td><td><div class="bw"><div class="bf" style="width:54%"></div></div></td></tr>
          <tr><td class="cmc">Tackles</td>        <td><span class="lv">24</span></td><td><span class="mv">32</span></td><td><span class="hv">44</span></td><td><div class="bw"><div class="bf" style="width:68%"></div></div></td></tr>
          <tr><td class="cmc">Offsides</td>       <td><span class="lv">2</span></td><td><span class="mv">5</span></td><td><span class="hv">9</span></td><td><div class="bw"><div class="bf" style="width:46%"></div></div></td></tr>
        </tbody>
      </table>
      </div>
    </div>
  </div>

  <!-- YELLOW CARDS -->
  <div class="card fw">
    <div class="card-hd">
      <div class="hd-dot" style="background:var(--card-y)"></div>
      <div class="hd-title">🟨 Yellow Card Risk Players</div>
    </div>
    <div class="card-body">
      <div class="yc-grid">
        <div class="yc-row">
          <div class="yc-icon">🟨</div>
          <div class="yc-info">
            <div class="yc-name">Seko Fofana (Porto, MF)</div>
            <div class="yc-reason">Physical, box-to-box midfielder averaging 2.0 fouls/game. Scored 3 UEL goals this season but also accumulates cards. Porto's aggressive press generates high foul counts.</div>
          </div>
          <div class="yc-risk risk-h">HIGH</div>
        </div>
        <div class="yc-row">
          <div class="yc-icon">🟨</div>
          <div class="yc-info">
            <div class="yc-name">Ryan Yates (Nottm Forest, MF)</div>
            <div class="yc-reason">Combative central midfielder tasked with protecting Forest's high line. Porto averages 2.4 yellow cards per UEL game — Yates will be pressing hard and is a natural candidate for tactical bookings.</div>
          </div>
          <div class="yc-risk risk-h">HIGH</div>
        </div>
        <div class="yc-row">
          <div class="yc-icon">🟨</div>
          <div class="yc-info">
            <div class="yc-name">Omar Sangare (Nottm Forest, MF)</div>
            <div class="yc-reason">Powerful defensive midfielder, 5 yellows in Premier League this season. Forest's counter-press will see Sangare make high-tempo challenges against Porto's quick transitions.</div>
          </div>
          <div class="yc-risk risk-h">HIGH</div>
        </div>
        <div class="yc-row">
          <div class="yc-icon">🟨</div>
          <div class="yc-info">
            <div class="yc-name">Alberto Costa (Porto, RB)</div>
            <div class="yc-reason">Attacking right-back who gets forward aggressively and can be exposed defensively on the counter. Forest's wide threat on the left will create opportunities for tactical fouls.</div>
          </div>
          <div class="yc-risk risk-m">MED</div>
        </div>
        <div class="yc-row">
          <div class="yc-icon">🟨</div>
          <div class="yc-info">
            <div class="yc-name">Nicolás Domínguez (Nottm Forest, MF)</div>
            <div class="yc-reason">Technical midfielder in an unfamiliar away environment. Forest lacking depth in midfield without Anderson — Domínguez will have extra responsibility and may foul to protect space.</div>
          </div>
          <div class="yc-risk risk-m">MED</div>
        </div>
      </div>
    </div>
  </div>

  <!-- NOTES -->
  <div class="card fw">
    <div class="card-hd"><div class="hd-dot" style="background:#60a5fa"></div><div class="hd-title">Analytical Notes</div></div>
    <div class="card-body">
      <div class="note"><strong>Corners (7–9–14):</strong> Porto average 4.4 corners/home UEL game; Forest 5.7 on away UEL trips. Combined baseline ~10. The tactical nature of this tie (Forest will defend deep without Anderson) suppresses the corner count — the low end is very possible. Porto's data suggests under 8.5 corners in 7 of 8 Celta-style opponents (same compact shape). Median 9.</div>
      <div class="note"><strong>Fouls (20–27–36):</strong> Porto average 2.4 cautions/UEL game (highest of the three home sides tonight). Forest's makeshift midfield without Anderson will be aggressive and tactical. Porto's pressing game creates frequent fouls. Combined baseline ~28; QF intensity pushes median to 27. High end if referee is strict.</div>
      <div class="note"><strong>Shots (17–23–31):</strong> Porto average 12.7/game; Forest ~11.4 on away trips. Combined ~24. Without Samu and de Jong, Porto's attack is weaker. Forest's compact 4-5-1 will limit quality attempts. Median of 23 reflects two teams with moderate attacking output in a tight first leg. <em>Igor Jesus has scored 7 UEL goals</em> — Forest's counter-attack could produce several shots.</div>
      <div class="note"><strong>Offsides (2–5–9):</strong> Porto's high-tempo forward pressing creates offside lines. Forest will play a high defensive line under Pereira (their PL style) which risks being caught by Porto's directness. Both Borja Sainz and William Gomes are quick runners who test the line. Median of 5.</div>
    </div>
  </div>

</div><!-- /m-grid -->

<!-- ─ DIVIDER ─ -->
<div class="s-div"><div class="s-div-in">★ Match 3 ★</div></div>

</div><!-- /page -->

<!-- ═══════════════════════════════════════
     MATCH 3: FREIBURG vs CELTA VIGO
═══════════════════════════════════════ -->
<div class="match-hero mh-fre" id="fre">
  <div class="mh-glow"></div>
  <div class="hero-row">

    <div class="hero-team">
      <div class="badge-img-wrap">
        <img src="https://upload.wikimedia.org/wikipedia/commons/0/0b/Soccer.svg"
             alt="SC Freiburg" onerror="this.style.display='none'">
      </div>
      <div class="h-name">SC Freiburg</div>
      <div class="h-pos">Bundesliga 8th · Home · Historic QF</div>
    </div>

    <div class="vs-col">
      <div class="vs-big">VS</div>
      <div class="leg-tag">1st Leg</div>
      <div class="venue-txt">Europa-Park Stadion<br>Thu 9 Apr · 8pm BST</div>
    </div>

    <div class="hero-team">
      <div class="badge-img-wrap">
        <img src="https://upload.wikimedia.org/wikipedia/commons/0/0b/Soccer.svg"
             alt="Celta Vigo" onerror="this.style.display='none'">
      </div>
      <div class="h-name">RC Celta Vigo</div>
      <div class="h-pos">La Liga 6th · Away</div>
    </div>

  </div>
</div>

<div class="page">
<div class="m-grid">

  <!-- CONTEXT -->
  <div class="card fw">
    <div class="card-hd">
      <div class="hd-dot" style="background:var(--uel-g)"></div>
      <div class="hd-title">Match Context</div>
      <div class="hd-tag" style="color:var(--uel-g);border-color:rgba(255,208,74,0.28);background:rgba(255,208,74,0.07)">First ever meeting · Freiburg's first major Euro QF</div>
    </div>
    <div class="card-body">
      <div class="callout">
        <strong>First ever meeting</strong> between these clubs. Freiburg reach a major European quarter-final for the first time in their 124-year history — a remarkable achievement. They overturned a first-leg deficit to beat Genk 5–1 at home in R16. Celta's <strong>5th European QF</strong>, first since reaching the semi-final in 2017 when they beat Genk and Shakhtar before falling to Man United. Celta are the <em>joint-top scorers in UEL this season (21 goals in 10 games)</em>. Celta are unbeaten in their last <strong>8 away matches</strong> (W4 D4). Freiburg concede in every game at home (10 consecutive) but score in 24 of 25 home matches. Key absences: Freiburg missing Höler (hamstring), Koffi-Kyereh, Osterhage, Makengo, Rosenfelder. Celta missing Hugo Álvarez (ankle), Javi Rueda (suspension), Carl Starfelt (back).
      </div>
    </div>
  </div>

  <!-- FORM -->
  <div class="card fw">
    <div class="card-hd">
      <div class="hd-dot" style="background:#f07070"></div>
      <div class="hd-title">Last 5 Matches — All Competitions</div>
    </div>
    <div class="card-body">
      <div class="form-cols">
        <div class="fcol">
          <div class="team-lab lab-fre">
            <img class="tl-img" src="https://upload.wikimedia.org/wikipedia/commons/0/0b/Soccer.svg" alt="">
            SC Freiburg
          </div>
          <div class="match-list">
            <div class="mr"><div class="rd L"></div><div class="ms">2–3</div><div class="mo">Bayern Munich</div><div class="mc">Bundesliga · Home</div></div>
            <div class="mr"><div class="rd W"></div><div class="ms">5–1</div><div class="mo">Genk</div><div class="mc">UEL R16 · Home</div></div>
            <div class="mr"><div class="rd L"></div><div class="ms">0–1</div><div class="mo">Genk</div><div class="mc">UEL R16 · Away</div></div>
            <div class="mr"><div class="rd W"></div><div class="ms">2–0</div><div class="mo">Mainz</div><div class="mc">Bundesliga · Home</div></div>
            <div class="mr"><div class="rd L"></div><div class="ms">0–2</div><div class="mo">Union Berlin</div><div class="mc">Bundesliga · Away</div></div>
          </div>
        </div>
        <div class="fcol">
          <div class="team-lab lab-cel">
            <img class="tl-img" src="https://upload.wikimedia.org/wikipedia/commons/0/0b/Soccer.svg" alt="">
            Celta Vigo
          </div>
          <div class="match-list">
            <div class="mr"><div class="rd W"></div><div class="ms">3–2</div><div class="mo">Valencia</div><div class="mc">La Liga · Away</div></div>
            <div class="mr"><div class="rd W"></div><div class="ms">2–0</div><div class="mo">Lyon</div><div class="mc">UEL R16 · Away</div></div>
            <div class="mr"><div class="rd D"></div><div class="ms">1–1</div><div class="mo">Lyon</div><div class="mc">UEL R16 · Home</div></div>
            <div class="mr"><div class="rd W"></div><div class="ms">2–1</div><div class="mo">Athletic Bilbao</div><div class="mc">La Liga · Away</div></div>
            <div class="mr"><div class="rd D"></div><div class="ms">1–1</div><div class="mo">Girona</div><div class="mc">La Liga · Away</div></div>
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

  <!-- AVERAGES -->
  <div class="card fw">
    <div class="card-hd">
      <div class="hd-dot" style="background:#a78bfa"></div>
      <div class="hd-title">Season Averages per Match — UEL &amp; League 25/26</div>
    </div>
    <div class="card-body">
      <div class="avg-pair">
        <div class="a-grp">
          <div class="a-grp-lbl" style="color:#f07070">SC Freiburg — Last 10 UEL/Liga</div>
          <div class="avg-g">
            <div class="ac"><div class="av">12.4</div><div class="al">Shots</div></div>
            <div class="ac"><div class="av">4.7</div><div class="al">SOT</div></div>
            <div class="ac"><div class="av">4.7</div><div class="al">Corners</div></div>
            <div class="ac"><div class="av">1.5</div><div class="al">Goals/Gm</div></div>
          </div>
          <div class="avg-g" style="margin-top:5px">
            <div class="ac"><div class="av">45%</div><div class="al">Possession</div></div>
            <div class="ac"><div class="av">15</div><div class="al">UEL Goals</div></div>
            <div class="ac"><div class="av">6</div><div class="al">UEL GA (best)</div></div>
            <div class="ac"><div class="av">10</div><div class="al">Consecutive concede</div></div>
          </div>
        </div>
        <div class="a-grp">
          <div class="a-grp-lbl" style="color:#80c8f0">Celta Vigo — Last 10 UEL/Liga</div>
          <div class="avg-g">
            <div class="ac"><div class="av">10.7</div><div class="al">Shots</div></div>
            <div class="ac"><div class="av">5.3</div><div class="al">SOT</div></div>
            <div class="ac"><div class="av">4.2</div><div class="al">Corners</div></div>
            <div class="ac"><div class="av">1.8</div><div class="al">Goals/Gm</div></div>
          </div>
          <div class="avg-g" style="margin-top:5px">
            <div class="ac"><div class="av">48%</div><div class="al">Possession</div></div>
            <div class="ac"><div class="av">21</div><div class="al">UEL Goals</div></div>
            <div class="ac"><div class="av">8</div><div class="al">Away unbeaten</div></div>
            <div class="ac"><div class="av">18/19</div><div class="al">Matches scoring</div></div>
          </div>
        </div>
      </div>
    </div>
  </div>

  <!-- H2H -->
  <div class="card fw">
    <div class="card-hd">
      <div class="hd-dot" style="background:var(--high)"></div>
      <div class="hd-title">Head to Head — No Previous Meetings</div>
    </div>
    <div class="card-body">
      <div class="h2h-bar">
        <div class="hs"><div class="hn" style="color:#f07070">0</div><div class="hl">Freiburg</div></div>
        <div class="hd"></div>
        <div class="hs"><div class="hn" style="color:var(--med)">0</div><div class="hl">Draws</div></div>
        <div class="hd"></div>
        <div class="hs"><div class="hn" style="color:#80c8f0">0</div><div class="hl">Celta Vigo</div></div>
        <div class="hd"></div>
        <div class="hs"><div class="hn">—</div><div class="hl">First Ever</div></div>
      </div>
      <p style="font-size:11px;color:var(--muted);margin-top:12px;">These clubs have <em>never met before</em> in any competition. No H2H data available — predictions are based entirely on season form, UEL averages, home/away splits, and individual match context. Freiburg reached a European QF for the first time ever; Celta's last European QF was in 2017 when they reached the UEL semi-finals. Both have surprised European opponents this season.</p>
    </div>
  </div>

  <!-- PREDICTIONS -->
  <div class="card fw">
    <div class="card-hd">
      <div class="hd-dot" style="background:var(--low)"></div>
      <div class="hd-title">Weighted Predictions — Freiburg vs Celta (Both Teams)</div>
    </div>
    <div class="card-body">
      <div class="pred-leg">
        <div class="pli"><div class="pld" style="background:var(--low)"></div><span style="color:var(--low);font-weight:700">Low</span></div>
        <div class="pli"><div class="pld" style="background:var(--med)"></div><span style="color:var(--med);font-weight:700">Median</span></div>
        <div class="pli"><div class="pld" style="background:var(--high)"></div><span style="color:var(--high);font-weight:700">High</span></div>
      </div>
      <div class="pw">
      <table class="pt">
        <colgroup><col class="cm"><col class="cl"><col class="cn"><col class="ch"><col class="cb"></colgroup>
        <thead><tr><th>Metric</th><th style="color:var(--low)">Low</th><th class="th-m">Median</th><th style="color:var(--high)">High</th><th style="text-align:center;color:var(--muted)">Intensity</th></tr></thead>
        <tbody>
          <tr><td class="cmc">Corners</td>        <td><span class="lv">6</span></td><td><span class="mv">9</span></td><td><span class="hv">13</span></td><td><div class="bw"><div class="bf" style="width:54%"></div></div></td></tr>
          <tr><td class="cmc">Total Shots</td>    <td><span class="lv">18</span></td><td><span class="mv">24</span></td><td><span class="hv">34</span></td><td><div class="bw"><div class="bf" style="width:66%"></div></div></td></tr>
          <tr><td class="cmc">Shots on Target</td><td><span class="lv">6</span></td><td><span class="mv">10</span></td><td><span class="hv">15</span></td><td><div class="bw"><div class="bf" style="width:60%"></div></div></td></tr>
          <tr><td class="cmc">Fouls</td>          <td><span class="lv">19</span></td><td><span class="mv">26</span></td><td><span class="hv">35</span></td><td><div class="bw"><div class="bf" style="width:66%"></div></div></td></tr>
          <tr><td class="cmc">Throw-ins</td>      <td><span class="lv">34</span></td><td><span class="mv">44</span></td><td><span class="hv">58</span></td><td><div class="bw"><div class="bf" style="width:62%"></div></div></td></tr>
          <tr><td class="cmc">Goal Kicks</td>     <td><span class="lv">13</span></td><td><span class="mv">19</span></td><td><span class="hv">26</span></td><td><div class="bw"><div class="bf" style="width:58%"></div></div></td></tr>
          <tr><td class="cmc">Tackles</td>        <td><span class="lv">24</span></td><td><span class="mv">32</span></td><td><span class="hv">46</span></td><td><div class="bw"><div class="bf" style="width:70%"></div></div></td></tr>
          <tr><td class="cmc">Offsides</td>       <td><span class="lv">2</span></td><td><span class="mv">5</span></td><td><span class="hv">9</span></td><td><div class="bw"><div class="bf" style="width:46%"></div></div></td></tr>
        </tbody>
      </table>
      </div>
    </div>
  </div>

  <!-- YELLOW CARDS -->
  <div class="card fw">
    <div class="card-hd">
      <div class="hd-dot" style="background:var(--card-y)"></div>
      <div class="hd-title">🟨 Yellow Card Risk Players</div>
    </div>
    <div class="card-body">
      <div class="yc-grid">
        <div class="yc-row">
          <div class="yc-icon">🟨</div>
          <div class="yc-info">
            <div class="yc-name">Ilaix Moriba (Celta Vigo, MF)</div>
            <div class="yc-reason">Physical, combative midfielder tasked with protecting Celta's defence on the road. 4 yellows in UEL this season. Will face Freiburg's aggressive pressing and likely commit tactical fouls.</div>
          </div>
          <div class="yc-risk risk-h">HIGH</div>
        </div>
        <div class="yc-row">
          <div class="yc-icon">🟨</div>
          <div class="yc-info">
            <div class="yc-name">Maximilian Eggestein (Freiburg, MF)</div>
            <div class="yc-reason">Box-to-box midfielder, one of Freiburg's top assistors. Aggressive in the press and commits fouls when disrupting attacks. Key to breaking up Celta's counter-transitions. On 3 UEL bookings.</div>
          </div>
          <div class="yc-risk risk-h">HIGH</div>
        </div>
        <div class="yc-row">
          <div class="yc-icon">🟨</div>
          <div class="yc-info">
            <div class="yc-name">Hugo Sotelo (Celta Vigo, MF)</div>
            <div class="yc-reason">Young, energetic midfielder who covers ground aggressively. Will be asked to press high in a Freiburg home environment — high-tempo press from Freiburg will create foul opportunities. 2 UEL yellows.</div>
          </div>
          <div class="yc-risk risk-h">HIGH</div>
        </div>
        <div class="yc-row">
          <div class="yc-icon">🟨</div>
          <div class="yc-info">
            <div class="yc-name">Matthias Ginter (Freiburg, CB)</div>
            <div class="yc-reason">Experienced defender but Celta's pace runners (Swedberg, Jutglà) will test him. 3 UEL goals but also 3 bookings. In the first leg of a high-pressure QF, a cynical foul is likely.</div>
          </div>
          <div class="yc-risk risk-m">MED</div>
        </div>
        <div class="yc-row">
          <div class="yc-icon">🟨</div>
          <div class="yc-info">
            <div class="yc-name">Óscar Mingueza (Celta Vigo, RB)</div>
            <div class="yc-reason">Attacking right-back and Celta's most capped player in the squad. Gets forward constantly and can be caught out of position. 4 assists this season but prone to tactical fouls on the counter.</div>
          </div>
          <div class="yc-risk risk-m">MED</div>
        </div>
      </div>
    </div>
  </div>

  <!-- NOTES -->
  <div class="card fw">
    <div class="card-hd"><div class="hd-dot" style="background:#60a5fa"></div><div class="hd-title">Analytical Notes</div></div>
    <div class="card-body">
      <div class="note"><strong>Corners (6–9–13):</strong> Freiburg average 4.7 corners/game; Celta 4.2 on their away trips. Combined baseline ~9. However, data shows under 8.5 corners in 7 of Celta's last 8 away matches. <em>Freiburg doesn't rely heavily on set pieces despite their strong home record</em>. Median of 9 sits right at the threshold. Low end if Celta disrupt Freiburg's wide play early.</div>
      <div class="note"><strong>Shots (18–24–34):</strong> Freiburg 12.4 shots/game; Celta score in 18 of 19 games and generate ~10.7 shots away. Both teams find the net consistently (BTTS in 4 of Freiburg's last 5 home games, 4 of Celta's last 5 away). Combined baseline ~23. High end reflects both teams' attacking confidence and the first-ever encounter meaning no defensive script to fall back on. Median of 24.</div>
      <div class="note"><strong>Tackles (24–32–46):</strong> This is the most balanced tackle matchup of the three QF games. Both teams press aggressively and contest every ball. Freiburg's counter-pressing energy plus Celta's physical midfield creates the conditions for a tackle-heavy encounter. Celta's Moriba and Sotelo are physical presences; Freiburg's Eggestein and Höler (if fit) compete hard. Median of 32 is well-anchored.</div>
      <div class="note"><strong>Offsides (2–5–9):</strong> No H2H data to anchor this, but both teams use some high-line elements. Celta's strikers make runs behind defensive lines (Borja Iglesias, Williot Swedberg); Freiburg's defence can be caught by pace (they conceded in 10 consecutive home games). Median of 5 based purely on league averages for both sides.</div>
    </div>
  </div>

</div><!-- /m-grid -->
</div><!-- /page -->

<footer>
  <strong>TEAM BILBO Statistical Analysis</strong><br>Predictions are statistical estimates based on actual data, H2H analysis and contextual factors. <strong>Not financial advice.</strong><br> · April 9, 2026 ·
</footer>
</body>
</html>
