<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<meta name="description" content="Team Bilbo Statistical Analytics: Premier League Matchweek Predictions">
<title>Premier League Stats Predictor | Team Bilbo Analytics</title>
<link rel="preconnect" href="https://fonts.googleapis.com">
<link href="https://fonts.googleapis.com/css2?family=Outfit:wght@300;400;600;800;900&family=Inter:wght@400;500;600;700&display=swap" rel="stylesheet">
<style>
/* ══════════════════════════════════
   ROOT TOKENS & BASE
══════════════════════════════════ */
:root {
  --bg:          #0a0a0c;
  --bg2:         #131318;
  --bg3:         #1c1c24;
  --bg4:         #262630;
  --bg5:         #2f2f3d;
  --border:      rgba(255,255,255,.08);
  --bm:          rgba(255,255,255,.15);
  --text:        #e2e8f0;
  --muted:       #94a3b8;
  --hi:          #cbd5e1;
  
  /* Premier League Branding */
  --pl-purple:   #3d195b;
  --pl-pink:     #e91e63;
  --pl-green:    #00ff85;
  
  /* Team Colors */
  --bre-r: #E30613; --bre-l: rgba(227, 6, 19, 0.2);
  --ful-w: #ffffff; --ful-l: rgba(255, 255, 255, 0.15);
  --lee-y: #FFCD00; --lee-l: rgba(255, 205, 0, 0.2);
  --wol-o: #FDB913; --wol-l: rgba(253, 185, 19, 0.2);
  --new-b: #ffffff; --new-l: rgba(255, 255, 255, 0.15);
  --bou-r: #B50E12; --bou-l: rgba(181, 14, 18, 0.2);
  --tot-n: #132257; --tot-l: rgba(19, 34, 87, 0.4);
  --bha-b: #0057B8; --bha-l: rgba(0, 87, 184, 0.2);
  --che-b: #034694; --che-l: rgba(3, 70, 148, 0.2);
  --mun-r: #DA291C; --mun-l: rgba(218, 41, 28, 0.2);

  /* Stat Colors */
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

/* ══════ HEADER & NAV ══════ */
.site-header {
  background:linear-gradient(170deg, var(--pl-purple) 0%, var(--bg2) 60%, rgba(0,255,133,.05) 100%);
  border-bottom:1px solid rgba(233,30,99,.3);
  text-align:center; padding:20px 14px;
  position:relative; z-index:10;
}
.pl-chip {
  display:inline-flex; align-items:center; gap:8px;
  font-family:'Outfit',sans-serif; font-size:10px; font-weight:800;
  letter-spacing:1.5px; text-transform:uppercase;
  color:var(--pl-green); background:rgba(0,255,133,.1);
  border:1px solid rgba(0,255,133,.3);
  padding:4px 12px; border-radius:20px; margin-bottom:10px;
}
.site-header h1 {
  font-family:'Outfit',sans-serif; font-size:22px; font-weight:900; 
  letter-spacing:0.5px; text-transform:uppercase; color:#fff; line-height:1.2;
}
.site-header .sub { font-size:12px; color:var(--muted); margin-top:6px; }

.match-nav {
  display:flex; gap:8px; overflow-x:auto; padding:12px 14px;
  background:var(--bg2); border-bottom:1px solid var(--border);
  -webkit-overflow-scrolling:touch; scrollbar-width:none;
}
.match-nav::-webkit-scrollbar { display:none; }
.mn-btn {
  white-space:nowrap; font-family:'Outfit',sans-serif; font-size:10px; font-weight:700;
  letter-spacing:1px; text-transform:uppercase; text-decoration:none;
  color:var(--hi); background:var(--bg3); border:1px solid var(--border);
  padding:6px 12px; border-radius:6px; flex-shrink:0;
}
.mn-btn:active, .mn-btn:focus { background:var(--bg4); border-color:var(--bm); }

/* ══════ MATCH HERO ══════ */
.match-hero { padding:20px 14px; border-bottom:1px solid var(--bm); position:relative; }
.hero-inner { display:flex; align-items:center; justify-content:space-between; gap:8px; max-width: 100%; margin:0 auto; }
.h-team { display:flex; flex-direction:column; align-items:center; gap:6px; flex:1; }
.badge-wrap {
  width:60px; height:60px; border-radius:50%;
  border:1.5px solid var(--bm); background:rgba(255,255,255,.08);
  display:flex; align-items:center; justify-content:center; overflow:hidden;
  filter:drop-shadow(0 4px 12px rgba(0,0,0,.4));
}
.badge-wrap img { width:40px; height:40px; object-fit:contain; }
.h-name { font-family:'Outfit',sans-serif; font-size:13px; font-weight:800; text-transform:uppercase; text-align:center; color:#fff; line-height:1.1; }

.vs-col { display:flex; flex-direction:column; align-items:center; gap:4px; flex-shrink:0; }
.vs-txt { font-family:'Outfit',sans-serif; font-size:18px; font-weight:900; color:rgba(255,255,255,.15); letter-spacing:2px; }
.ko-chip {
  font-family:'Outfit',sans-serif; font-size:9px; font-weight:800; letter-spacing:1px;
  color:#fff; background:var(--bg4); border:1px solid var(--bm);
  padding:2px 8px; border-radius:4px; text-transform: uppercase;
}

/* ══════ SCORE BOX ══════ */
.score-box { background:linear-gradient(135deg,var(--bg3),var(--bg4)); border:1px solid var(--bm); border-radius:12px; padding:16px 14px; margin-bottom:16px; }
.sb-title { font-family:'Outfit',sans-serif; font-size:11px; font-weight:800; letter-spacing:1.5px; text-transform:uppercase; color:var(--hi); text-align:center; margin-bottom:14px; border-bottom: 1px solid var(--border); padding-bottom: 10px; }
.scores-row { display:flex; gap:8px; justify-content:center; flex-wrap:wrap; }
.sc { background:var(--bg5); border:1px solid var(--border); border-radius:8px; padding:12px; text-align:center; flex:1; min-width:100px; }
.sc-label { font-family:'Outfit',sans-serif; font-size:9px; font-weight:700; letter-spacing:1px; text-transform:uppercase; color:var(--muted); margin-bottom:6px; }
.sc-value { font-family:'Outfit',sans-serif; font-size:28px; font-weight:900; letter-spacing:2px; line-height:1; color:#fff; }
.sc-prob { font-size:9px; color:var(--muted); margin-top:6px; font-weight: 500; }
.sc-best { border-color:var(--pl-pink); background:linear-gradient(135deg,rgba(233,30,99,.08),var(--bg5)); }
.sc-best .sc-label { color:var(--pl-pink); }
.sb-notes { font-size:12px; color:var(--hi); line-height:1.6; margin-top:14px; padding: 10px; background: rgba(0,0,0,0.2); border-radius: 8px; }
.sb-notes strong { color:#fff; font-weight:700; }

/* ══════ PAGE & CARDS ══════ */
.page { width:100%; max-width:1200px; margin:0 auto; padding:16px 12px 40px; }
.card { background:var(--bg2); border:1px solid var(--border); border-radius:12px; overflow:hidden; margin-bottom:16px; }
.card-hd { padding:12px 14px; border-bottom:1px solid var(--border); display:flex; align-items:center; gap:8px; background: rgba(255,255,255,0.02); }
.hd-dot { width:6px; height:6px; border-radius:50%; flex-shrink:0; }
.hd-title { font-family:'Outfit',sans-serif; font-size:11px; font-weight:800; letter-spacing:1px; text-transform:uppercase; color:var(--muted); flex:1; }
.card-body { padding:14px; }

/* Form cols */
.form-cols { display:flex; flex-direction:column; gap:16px; }
.team-lab { display:inline-flex; align-items:center; gap:6px; font-size:10px; font-weight:700; letter-spacing:1px; text-transform:uppercase; padding:4px 8px; border-radius:6px; margin-bottom:8px; border:1px solid; color:#fff;}
.match-list { display:flex; flex-direction:column; gap:4px; }
.mr { display:grid; grid-template-columns:8px 40px 1fr auto; align-items:center; gap:8px; background:var(--bg3); border:1px solid var(--border); border-radius:6px; padding:6px 10px; }
.rd { width:8px; height:8px; border-radius:50%; }
.rd.W { background:var(--lo); box-shadow:0 0 6px rgba(15,217,162,.4); }
.rd.D { background:var(--md); }
.rd.L { background:var(--hic); box-shadow:0 0 6px rgba(245,89,41,.4); }
.ms { font-family:'Outfit',sans-serif; font-size:13px; font-weight:800; color:#fff; text-align:center; }
.mo { font-size:11px; color:var(--text); font-weight:500; white-space:nowrap; overflow:hidden; text-overflow:ellipsis; }
.mc { font-size:9px; color:var(--muted); text-align:right; text-transform:uppercase; letter-spacing:0.5px; }

/* ══════ PREDICTION TABLES (MOBILE-FIRST) ══════ */
.table-wrapper { width: 100%; margin: 0; padding: 0; }
.pt { width: 100%; min-width: 100%; border-collapse: collapse; table-layout: fixed; word-wrap: break-word; }

/* Specific Column Widths to Ensure Fit */
.pt thead th:nth-child(1), .pt tbody td:nth-child(1) { width: 28%; }
.pt thead th:nth-child(2), .pt tbody td:nth-child(2) { width: 17%; }
.pt thead th:nth-child(3), .pt tbody td:nth-child(3) { width: 38%; }
.pt thead th:nth-child(4), .pt tbody td:nth-child(4) { width: 17%; }

.pt thead th {
  font-family: 'Outfit', sans-serif; font-size: 9px; font-weight: 800;
  letter-spacing: 0.5px; text-transform: uppercase; color: var(--muted);
  padding: 0 2px 8px; text-align: center; border-bottom: 1px solid var(--border);
}
.pt thead th:first-child { text-align: left; padding-left: 4px; }
.pt tbody td { padding: 10px 2px; border-bottom: 1px solid rgba(255,255,255,.04); vertical-align: middle; text-align: center; }
.pt tbody td.cmc { color: var(--hi); font-size: 11px; font-weight: 600; padding-left: 4px; text-align: left; line-height: 1.2; }

.lv { font-family: 'Outfit', sans-serif; font-size: 13px; font-weight: 800; color: var(--lo); }
.mv { font-family: 'Outfit', sans-serif; font-size: 15px; font-weight: 900; color: var(--md); }
.hv { font-family: 'Outfit', sans-serif; font-size: 13px; font-weight: 800; color: var(--hic); }

/* Vertically Stacked Splits for Narrow Screens */
.split-stats { display: flex; flex-direction: column; gap: 3px; align-items: center; font-family: 'Inter', sans-serif; font-size: 8.5px; color: var(--muted); margin-top: 5px; font-weight: 500; }
.split-stats span { display: inline-block; padding: 2px 4px; background: var(--bg4); border-radius: 4px; border: 1px solid var(--border); white-space: nowrap; }

/* Yellow Cards */
.yc-grid { display:flex; flex-direction:column; gap:8px; }
.yc-row { display:flex; align-items:flex-start; gap:10px; background:var(--bg3); border:1px solid var(--border); border-radius:8px; padding:10px 12px; }
.yc-icon { font-size:18px; flex-shrink:0; margin-top:2px; }
.yc-info { flex:1; min-width:0; }
.yc-name { font-size:13px; font-weight:700; color:#fff; }
.yc-club { font-size:9px; font-family:'Outfit',sans-serif; letter-spacing:0.5px; text-transform:uppercase; margin-left:4px; font-weight: 800; color:var(--muted); }
.yc-reason { font-size:11px; color:var(--muted); margin-top:4px; line-height:1.4; }
.yc-risk { font-family:'Outfit',sans-serif; font-size:9px; font-weight:800; letter-spacing:1px; text-transform:uppercase; padding:3px 8px; border-radius:4px; flex-shrink:0; align-self:center; }
.risk-h { background:rgba(245,89,41,.15); color:var(--hic); border:1px solid rgba(245,89,41,.3); }
.risk-m { background:rgba(247,201,72,.15); color:var(--md); border:1px solid rgba(247,201,72,.3); }

/* ══════ DESKTOP ENHANCEMENTS ══════ */
@media(min-width: 768px) {
  .site-header { padding: 32px 20px 24px; }
  .site-header h1 { font-size: 32px; }
  .match-nav { justify-content:center; padding:16px; }
  .match-hero { padding: 24px 20px; }
  .hero-inner { max-width: 720px; gap: 16px; }
  .badge-wrap { width: 80px; height: 80px; border-width: 2px; }
  .badge-wrap img { width: 56px; height: 56px; }
  .h-name { font-size: 16px; }
  .vs-txt { font-size: 24px; }
  .page { padding: 24px 20px 60px; }
  .dg { display: grid; grid-template-columns: 1fr 1fr; gap: 24px; align-items: start; }
  .fw { grid-column: 1 / -1; }
  .form-cols { flex-direction: row; }
  .fcol { flex: 1; min-width: 0; }
  
  /* Revert table limits for desktop */
  .pt { table-layout: auto; }
  .pt thead th:nth-child(1), .pt tbody td:nth-child(1) { width: auto; }
  .pt thead th:nth-child(2), .pt tbody td:nth-child(2) { width: auto; }
  .pt thead th:nth-child(3), .pt tbody td:nth-child(3) { width: auto; }
  .pt thead th:nth-child(4), .pt tbody td:nth-child(4) { width: auto; }

  .pt thead th { font-size: 11px; padding: 0 8px 12px; letter-spacing: 1px; }
  .pt tbody td { padding: 12px 10px; }
  .pt tbody td.cmc { font-size: 13px; }
  .lv, .hv { font-size: 16px; }
  .mv { font-size: 18px; }
  
  .split-stats { flex-direction: row; justify-content: center; gap: 8px; font-size: 10px; margin-top: 6px; }
  .split-stats span { padding: 2px 8px; }
}
</style>
</head>
<body>

<header class="site-header">
  <div class="pl-chip">Premier League · Matchweek Special</div>
  <h1>Team Bilbo Analytics</h1>
  <p class="sub">Form · Season Averages · H2H · Weighted Stat Projections · Score Forecasts</p>
</header>

<nav class="match-nav">
  <a href="#m1" class="mn-btn">BRE vs FUL</a>
  <a href="#m2" class="mn-btn">LEE vs WOL</a>
  <a href="#m3" class="mn-btn">NEW vs BOU</a>
  <a href="#m4" class="mn-btn">TOT vs BHA</a>
  <a href="#m5" class="mn-btn">CHE vs MUN</a>
</nav>

<div class="page">

  <div id="m1" style="background:linear-gradient(135deg, var(--bre-l) 0%, var(--bg2) 50%, var(--ful-l) 100%); border-radius:12px; overflow:hidden; margin-bottom:24px; border:1px solid var(--border);">
    <div class="match-hero">
      <div class="hero-inner">
        <div class="h-team">
          <div class="badge-wrap"><img src="https://upload.wikimedia.org/wikipedia/en/thumb/2/2a/Brentford_FC_crest.svg/120px-Brentford_FC_crest.svg.png" alt="Brentford" style="background: transparent;"></div>
          <div class="h-name">Brentford</div>
        </div>
        <div class="vs-col"><div class="vs-txt">VS</div><div class="ko-chip">Gtech Stadium</div></div>
        <div class="h-team">
          <div class="badge-wrap" style=";"><img src="https://upload.wikimedia.org/wikipedia/en/thumb/e/eb/Fulham_FC_%28shield%29.svg/120px-Fulham_FC_%28shield%29.svg.png" alt="Fulham" style="background: transparent;"></div>
          <div class="h-name">Fulham</div>
        </div>
      </div>
    </div>
    
    <div class="card-body" style="padding-top:0;">
      <div class="score-box fw" style="margin-top:16px;">
        <div class="sb-title">West London Derby Prediction</div>
        <div class="scores-row">
          <div class="sc"><div class="sc-label">Half-Time</div><div class="sc-value" style="color:var(--md)">0 – 0</div><div class="sc-prob">Tight, physical</div></div>
          <div class="sc sc-best"><div class="sc-label">Full-Time</div><div class="sc-value" style="color:var(--pl-pink)">1 – 1</div><div class="sc-prob">Draw · 45% Prob</div></div>
        </div>
        <div class="sb-notes"><strong>Rationale:</strong> Derbies at the Gtech are fiercely contested. Brentford rely on set-pieces while Fulham aim to control possession through the middle. Neither side wants to lose this fixture, pointing toward a low-scoring draw.</div>
      </div>

      <div class="dg">
        <div class="card fw">
          <div class="card-hd"><div class="hd-title">Form & H2H (Last 5)</div></div>
          <div class="card-body form-cols">
            <div class="fcol">
              <div class="team-lab" style="background:var(--bre-l); border-color:var(--bre-r);">Brentford</div>
              <div class="match-list">
                <div class="mr"><div class="rd W"></div><div class="ms">2–1</div><div class="mo">Everton</div><div class="mc">PL</div></div>
                <div class="mr"><div class="rd D"></div><div class="ms">1–1</div><div class="mo">Aston Villa</div><div class="mc">PL</div></div>
                <div class="mr"><div class="rd L"></div><div class="ms">0–2</div><div class="mo">Arsenal</div><div class="mc">PL</div></div>
                <div class="mr"><div class="rd W"></div><div class="ms">3–0</div><div class="mo">Luton</div><div class="mc">PL</div></div>
                <div class="mr"><div class="rd D"></div><div class="ms">2–2</div><div class="mo">Chelsea</div><div class="mc">PL</div></div>
              </div>
            </div>
            <div class="fcol">
              <div class="team-lab" style="background:var(--ful-l); border-color:var(--ful-w);">Fulham</div>
              <div class="match-list">
                <div class="mr"><div class="rd W"></div><div class="ms">1–0</div><div class="mo">Nott'm Forest</div><div class="mc">PL</div></div>
                <div class="mr"><div class="rd L"></div><div class="ms">1–3</div><div class="mo">Liverpool</div><div class="mc">PL</div></div>
                <div class="mr"><div class="rd W"></div><div class="ms">2–1</div><div class="mo">West Ham</div><div class="mc">PL</div></div>
                <div class="mr"><div class="rd L"></div><div class="ms">0–1</div><div class="mo">Newcastle</div><div class="mc">PL</div></div>
                <div class="mr"><div class="rd D"></div><div class="ms">1–1</div><div class="mo">Crystal Palace</div><div class="mc">PL</div></div>
              </div>
            </div>
          </div>
          <div style="padding:0 14px 14px; font-size:11px; color:var(--hi);"><strong>H2H:</strong> FUL 0-3 BRE, BRE 3-2 FUL, FUL 3-2 BRE, BRE 1-2 FUL, FUL 1-1 BRE.</div>
        </div>

        <div class="card fw">
          <div class="card-hd"><div class="hd-title">Weighted Stat Projections</div></div>
          <div class="card-body" style="padding:0;">
            <div class="table-wrapper"><table class="pt">
              <thead><tr><th>Metric</th><th>Low</th><th class="th-m">Median</th><th>High</th></tr></thead>
              <tbody>
                <tr><td class="cmc">Corners</td><td>8</td><td><span class="mv">10</span> <div class="split-stats"><span>BRE: 5</span><span>FUL: 5</span></div></td><td>13</td></tr>
                <tr><td class="cmc">Shots</td><td>20</td><td><span class="mv">24</span> <div class="split-stats"><span>BRE: 13</span><span>FUL: 11</span></div></td><td>29</td></tr>
                <tr><td class="cmc">Shots on Target</td><td>6</td><td><span class="mv">9</span> <div class="split-stats"><span>BRE: 5</span><span>FUL: 4</span></div></td><td>12</td></tr>
                <tr><td class="cmc">Fouls</td><td>18</td><td><span class="mv">22</span> <div class="split-stats"><span>BRE: 11</span><span>FUL: 11</span></div></td><td>27</td></tr>
                <tr><td class="cmc">Throw-ins</td><td>34</td><td><span class="mv">40</span> <div class="split-stats"><span>BRE: 20</span><span>FUL: 20</span></div></td><td>48</td></tr>
                <tr><td class="cmc">Goal Kicks</td><td>12</td><td><span class="mv">16</span> <div class="split-stats"><span>BRE: 8</span><span>FUL: 8</span></div></td><td>22</td></tr>
                <tr><td class="cmc">Tackles</td><td>28</td><td><span class="mv">34</span> <div class="split-stats"><span>BRE: 16</span><span>FUL: 18</span></div></td><td>42</td></tr>
              </tbody>
            </table></div>
          </div>
        </div>

        <div class="card fw">
          <div class="card-hd"><div class="hd-title">🟨 Card Risks</div></div>
          <div class="card-body yc-grid">
            <div class="yc-row"><div class="yc-icon">🟨</div><div class="yc-info"><div class="yc-name">Christian Nørgaard</div><div class="yc-club">BRE · DM</div><div class="yc-reason">Breaks up Fulham's transition. High derby tackle rate.</div></div><div class="yc-risk risk-h">HIGH</div></div>
            <div class="yc-row"><div class="yc-icon">🟨</div><div class="yc-info"><div class="yc-name">João Palhinha</div><div class="yc-club">FUL · DM</div><div class="yc-reason">League leader in tackles. Will combat physical Brentford midfield.</div></div><div class="yc-risk risk-h">HIGH</div></div>
          </div>
        </div>
      </div>
    </div>
  </div>


  <div id="m2" style="background:linear-gradient(135deg, var(--lee-l) 0%, var(--bg2) 50%, var(--wol-l) 100%); border-radius:12px; overflow:hidden; margin-bottom:24px; border:1px solid var(--border);">
    <div class="match-hero">
      <div class="hero-inner">
        <div class="h-team">
          <div class="badge-wrap" style=""><img src="https://upload.wikimedia.org/wikipedia/en/thumb/5/54/Leeds_United_F.C._logo.svg/120px-Leeds_United_F.C._logo.svg.png" alt="Leeds" style="background: transparent;"></div>
          <div class="h-name">Leeds Utd</div>
        </div>
        <div class="vs-col"><div class="vs-txt">VS</div><div class="ko-chip">Elland Road</div></div>
        <div class="h-team">
          <div class="badge-wrap"><img src="https://upload.wikimedia.org/wikipedia/en/thumb/f/fc/Wolverhampton_Wanderers.svg/120px-Wolverhampton_Wanderers.svg.png" alt="Wolves" style="background: transparent;"></div>
          <div class="h-name">Wolves</div>
        </div>
      </div>
    </div>
    
    <div class="card-body" style="padding-top:0;">
      <div class="score-box fw" style="margin-top:16px;">
        <div class="sb-title">Mid-Table Clash Prediction</div>
        <div class="scores-row">
          <div class="sc"><div class="sc-label">Half-Time</div><div class="sc-value" style="color:var(--md)">1 – 1</div><div class="sc-prob">Open start</div></div>
          <div class="sc sc-best"><div class="sc-label">Full-Time</div><div class="sc-value" style="color:var(--lo)">2 – 1</div><div class="sc-prob">Leeds edge it</div></div>
        </div>
        <div class="sb-notes"><strong>Rationale:</strong> Elland Road pushes Leeds to attack, leaving them vulnerable to Wolves' counter. High pace, lots of transitions, but Leeds' home intensity should outlast Wolves.</div>
      </div>

      <div class="dg">
        <div class="card fw">
          <div class="card-hd"><div class="hd-title">Form & H2H (Last 5)</div></div>
          <div class="card-body form-cols">
            <div class="fcol">
              <div class="team-lab" style="background:var(--lee-l); border-color:var(--lee-y);">Leeds</div>
              <div class="match-list">
                <div class="mr"><div class="rd L"></div><div class="ms">0–2</div><div class="mo">Man City</div><div class="mc">PL</div></div>
                <div class="mr"><div class="rd W"></div><div class="ms">1–0</div><div class="mo">Burnley</div><div class="mc">PL</div></div>
                <div class="mr"><div class="rd D"></div><div class="ms">2–2</div><div class="mo">West Ham</div><div class="mc">PL</div></div>
                <div class="mr"><div class="rd W"></div><div class="ms">3–1</div><div class="mo">Sheff Utd</div><div class="mc">PL</div></div>
                <div class="mr"><div class="rd L"></div><div class="ms">1–4</div><div class="mo">Arsenal</div><div class="mc">PL</div></div>
              </div>
            </div>
            <div class="fcol">
              <div class="team-lab" style="background:var(--wol-l); border-color:var(--wol-o);">Wolves</div>
              <div class="match-list">
                <div class="mr"><div class="rd D"></div><div class="ms">1–1</div><div class="mo">Crystal Palace</div><div class="mc">PL</div></div>
                <div class="mr"><div class="rd L"></div><div class="ms">0–1</div><div class="mo">Bournemouth</div><div class="mc">PL</div></div>
                <div class="mr"><div class="rd W"></div><div class="ms">2–0</div><div class="mo">Everton</div><div class="mc">PL</div></div>
                <div class="mr"><div class="rd L"></div><div class="ms">1–2</div><div class="mo">Aston Villa</div><div class="mc">PL</div></div>
                <div class="mr"><div class="rd D"></div><div class="ms">0–0</div><div class="mo">Brighton</div><div class="mc">PL</div></div>
              </div>
            </div>
          </div>
          <div style="padding:0 14px 14px; font-size:11px; color:var(--hi);"><strong>H2H:</strong> WOL 1-2 LEE, WOL 2-4 LEE, LEE 2-1 WOL, WOL 2-3 LEE, LEE 1-1 WOL.</div>
        </div>

        <div class="card fw">
          <div class="card-hd"><div class="hd-title">Weighted Stat Projections</div></div>
          <div class="card-body" style="padding:0;">
            <div class="table-wrapper"><table class="pt">
              <thead><tr><th>Metric</th><th>Low</th><th class="th-m">Median</th><th>High</th></tr></thead>
              <tbody>
                <tr><td class="cmc">Corners</td><td>9</td><td><span class="mv">11</span> <div class="split-stats"><span>LEE: 6</span><span>WOL: 5</span></div></td><td>15</td></tr>
                <tr><td class="cmc">Shots</td><td>22</td><td><span class="mv">27</span> <div class="split-stats"><span>LEE: 15</span><span>WOL: 12</span></div></td><td>33</td></tr>
                <tr><td class="cmc">Shots on Target</td><td>7</td><td><span class="mv">10</span> <div class="split-stats"><span>LEE: 6</span><span>WOL: 4</span></div></td><td>14</td></tr>
                <tr><td class="cmc">Fouls</td><td>21</td><td><span class="mv">25</span> <div class="split-stats"><span>LEE: 13</span><span>WOL: 12</span></div></td><td>31</td></tr>
                <tr><td class="cmc">Throw-ins</td><td>36</td><td><span class="mv">42</span> <div class="split-stats"><span>LEE: 22</span><span>WOL: 20</span></div></td><td>50</td></tr>
                <tr><td class="cmc">Goal Kicks</td><td>14</td><td><span class="mv">18</span> <div class="split-stats"><span>LEE: 8</span><span>WOL: 10</span></div></td><td>24</td></tr>
                <tr><td class="cmc">Tackles</td><td>30</td><td><span class="mv">36</span> <div class="split-stats"><span>LEE: 19</span><span>WOL: 17</span></div></td><td>44</td></tr>
              </tbody>
            </table></div>
          </div>
        </div>

        <div class="card fw">
          <div class="card-hd"><div class="hd-title">🟨 Card Risks</div></div>
          <div class="card-body yc-grid">
            <div class="yc-row"><div class="yc-icon">🟨</div><div class="yc-info"><div class="yc-name">Ethan Ampadu</div><div class="yc-club">LEE · DM</div><div class="yc-reason">Tasked with stopping Wolves counter. Very physical.</div></div><div class="yc-risk risk-h">HIGH</div></div>
            <div class="yc-row"><div class="yc-icon">🟨</div><div class="yc-info"><div class="yc-name">Mario Lemina</div><div class="yc-club">WOL · CM</div><div class="yc-reason">Combative central figure; prone to accumulation fouls.</div></div><div class="yc-risk risk-h">HIGH</div></div>
          </div>
        </div>
      </div>
    </div>
  </div>


  <div id="m3" style="background:linear-gradient(135deg, var(--new-l) 0%, var(--bg2) 50%, var(--bou-l) 100%); border-radius:12px; overflow:hidden; margin-bottom:24px; border:1px solid var(--border);">
    <div class="match-hero">
      <div class="hero-inner">
        <div class="h-team">
          <div class="badge-wrap"><img src="https://upload.wikimedia.org/wikipedia/en/thumb/5/56/Newcastle_United_Logo.svg/120px-Newcastle_United_Logo.svg.png" alt="Newcastle" style="background: transparent;"></div>
          <div class="h-name">Newcastle</div>
        </div>
        <div class="vs-col"><div class="vs-txt">VS</div><div class="ko-chip">St James' Park</div></div>
        <div class="h-team">
          <div class="badge-wrap"><img src="https://upload.wikimedia.org/wikipedia/en/thumb/e/e5/AFC_Bournemouth_%282013%29.svg/120px-AFC_Bournemouth_%282013%29.svg.png" alt="Bournemouth" style="background: transparent;"></div>
          <div class="h-name">Bournemouth</div>
        </div>
      </div>
    </div>
    
    <div class="card-body" style="padding-top:0;">
      <div class="score-box fw" style="margin-top:16px;">
        <div class="sb-title">European Push Prediction</div>
        <div class="scores-row">
          <div class="sc"><div class="sc-label">Half-Time</div><div class="sc-value" style="color:var(--lo)">1 – 0</div><div class="sc-prob">Toon army push</div></div>
          <div class="sc sc-best"><div class="sc-label">Full-Time</div><div class="sc-value" style="color:var(--pl-pink)">3 – 1</div><div class="sc-prob">Home dominance</div></div>
        </div>
        <div class="sb-notes"><strong>Rationale:</strong> Newcastle at home are formidable. Bournemouth play an attacking system which will leave space for Gordon and Isak. High shot volume expected for the hosts.</div>
      </div>

      <div class="dg">
        <div class="card fw">
          <div class="card-hd"><div class="hd-title">Form & H2H (Last 5)</div></div>
          <div class="card-body form-cols">
            <div class="fcol">
              <div class="team-lab" style="background:var(--new-l); border-color:var(--new-b); color:#fff;">Newcastle</div>
              <div class="match-list">
                <div class="mr"><div class="rd W"></div><div class="ms">2–0</div><div class="mo">Fulham</div><div class="mc">PL</div></div>
                <div class="mr"><div class="rd D"></div><div class="ms">1–1</div><div class="mo">Spurs</div><div class="mc">PL</div></div>
                <div class="mr"><div class="rd W"></div><div class="ms">3–0</div><div class="mo">Wolves</div><div class="mc">PL</div></div>
                <div class="mr"><div class="rd L"></div><div class="ms">1–3</div><div class="mo">Man Utd</div><div class="mc">PL</div></div>
                <div class="mr"><div class="rd W"></div><div class="ms">2–1</div><div class="mo">Brentford</div><div class="mc">PL</div></div>
              </div>
            </div>
            <div class="fcol">
              <div class="team-lab" style="background:var(--bou-l); border-color:var(--bou-r);">Bournemouth</div>
              <div class="match-list">
                <div class="mr"><div class="rd W"></div><div class="ms">1–0</div><div class="mo">Wolves</div><div class="mc">PL</div></div>
                <div class="mr"><div class="rd L"></div><div class="ms">0–2</div><div class="mo">Chelsea</div><div class="mc">PL</div></div>
                <div class="mr"><div class="rd D"></div><div class="ms">2–2</div><div class="mo">Brighton</div><div class="mc">PL</div></div>
                <div class="mr"><div class="rd L"></div><div class="ms">1–2</div><div class="mo">Aston Villa</div><div class="mc">PL</div></div>
                <div class="mr"><div class="rd W"></div><div class="ms">3–1</div><div class="mo">Sheff Utd</div><div class="mc">PL</div></div>
              </div>
            </div>
          </div>
          <div style="padding:0 14px 14px; font-size:11px; color:var(--hi);"><strong>H2H:</strong> BOU 2-0 NEW, NEW 2-2 BOU, BOU 1-1 NEW, NEW 1-0 BOU, NEW 1-1 BOU.</div>
        </div>

        <div class="card fw">
          <div class="card-hd"><div class="hd-title">Weighted Stat Projections</div></div>
          <div class="card-body" style="padding:0;">
            <div class="table-wrapper"><table class="pt">
              <thead><tr><th>Metric</th><th>Low</th><th class="th-m">Median</th><th>High</th></tr></thead>
              <tbody>
                <tr><td class="cmc">Corners</td><td>9</td><td><span class="mv">12</span> <div class="split-stats"><span>NEW: 8</span><span>BOU: 4</span></div></td><td>16</td></tr>
                <tr><td class="cmc">Shots</td><td>24</td><td><span class="mv">30</span> <div class="split-stats"><span>NEW: 18</span><span>BOU: 12</span></div></td><td>38</td></tr>
                <tr><td class="cmc">Shots on Target</td><td>8</td><td><span class="mv">11</span> <div class="split-stats"><span>NEW: 7</span><span>BOU: 4</span></div></td><td>15</td></tr>
                <tr><td class="cmc">Fouls</td><td>19</td><td><span class="mv">23</span> <div class="split-stats"><span>NEW: 11</span><span>BOU: 12</span></div></td><td>29</td></tr>
                <tr><td class="cmc">Throw-ins</td><td>32</td><td><span class="mv">38</span> <div class="split-stats"><span>NEW: 19</span><span>BOU: 19</span></div></td><td>46</td></tr>
                <tr><td class="cmc">Goal Kicks</td><td>13</td><td><span class="mv">17</span> <div class="split-stats"><span>NEW: 6</span><span>BOU: 11</span></div></td><td>23</td></tr>
                <tr><td class="cmc">Tackles</td><td>26</td><td><span class="mv">33</span> <div class="split-stats"><span>NEW: 16</span><span>BOU: 17</span></div></td><td>41</td></tr>
              </tbody>
            </table></div>
          </div>
        </div>

        <div class="card fw">
          <div class="card-hd"><div class="hd-title">🟨 Card Risks</div></div>
          <div class="card-body yc-grid">
            <div class="yc-row"><div class="yc-icon">🟨</div><div class="yc-info"><div class="yc-name">Bruno Guimarães</div><div class="yc-club">NEW · CM</div><div class="yc-reason">High involvement, tactical fouls, often clashes with refs.</div></div><div class="yc-risk risk-h">HIGH</div></div>
            <div class="yc-row"><div class="yc-icon">🟨</div><div class="yc-info"><div class="yc-name">Lewis Cook</div><div class="yc-club">BOU · CM</div><div class="yc-reason">Will be overrun centrally; forced to make stopping challenges.</div></div><div class="yc-risk risk-m">MED</div></div>
          </div>
        </div>
      </div>
    </div>
  </div>


  <div id="m4" style="background:linear-gradient(135deg, var(--tot-l) 0%, var(--bg2) 50%, var(--bha-l) 100%); border-radius:12px; overflow:hidden; margin-bottom:24px; border:1px solid var(--border);">
    <div class="match-hero">
      <div class="hero-inner">
        <div class="h-team">
          <div class="badge-wrap"><img src="https://cdn.brandfetch.io/id0hQSdBIF/theme/dark/logo.svg?c=1bxid64Mup7aczewSAYMX&t=1668069471694" alt="Spurs" style="background: transparent;"></div>
          <div class="h-name">Tottenham</div>
        </div>
        <div class="vs-col"><div class="vs-txt">VS</div><div class="ko-chip">Spurs Stadium</div></div>
        <div class="h-team">
          <div class="badge-wrap"><img src="https://upload.wikimedia.org/wikipedia/en/thumb/f/fd/Brighton_%26_Hove_Albion_logo.svg/120px-Brighton_%26_Hove_Albion_logo.svg.png" alt="Brighton" style="background: transparent;"></div>
          <div class="h-name">Brighton</div>
        </div>
      </div>
    </div>
    
    <div class="card-body" style="padding-top:0;">
      <div class="score-box fw" style="margin-top:16px;">
        <div class="sb-title">High-Line Chaos Prediction</div>
        <div class="scores-row">
          <div class="sc"><div class="sc-label">Half-Time</div><div class="sc-value" style="color:var(--md)">1 – 1</div><div class="sc-prob">End-to-end play</div></div>
          <div class="sc sc-best"><div class="sc-label">Full-Time</div><div class="sc-value" style="color:var(--pl-pink)">3 – 2</div><div class="sc-prob">Spurs outscore</div></div>
        </div>
        <div class="sb-notes"><strong>Rationale:</strong> Both Postecoglou and Hürzeler play aggressive, high-line football. Expect offside traps broken, transition chaos, and a very high shot volume. Spurs' home advantage should clinch it.</div>
      </div>

      <div class="dg">
        <div class="card fw">
          <div class="card-hd"><div class="hd-title">Form & H2H (Last 5)</div></div>
          <div class="card-body form-cols">
            <div class="fcol">
              <div class="team-lab" style="background:var(--tot-l); border-color:var(--tot-n);">Spurs</div>
              <div class="match-list">
                <div class="mr"><div class="rd D"></div><div class="ms">1–1</div><div class="mo">Newcastle</div><div class="mc">PL</div></div>
                <div class="mr"><div class="rd W"></div><div class="ms">2–0</div><div class="mo">Nott'm Forest</div><div class="mc">PL</div></div>
                <div class="mr"><div class="rd L"></div><div class="ms">1–2</div><div class="mo">Aston Villa</div><div class="mc">PL</div></div>
                <div class="mr"><div class="rd W"></div><div class="ms">3–1</div><div class="mo">Crystal Palace</div><div class="mc">PL</div></div>
                <div class="mr"><div class="rd L"></div><div class="ms">2–4</div><div class="mo">Liverpool</div><div class="mc">PL</div></div>
              </div>
            </div>
            <div class="fcol">
              <div class="team-lab" style="background:var(--bha-l); border-color:var(--bha-b);">Brighton</div>
              <div class="match-list">
                <div class="mr"><div class="rd D"></div><div class="ms">2–2</div><div class="mo">Bournemouth</div><div class="mc">PL</div></div>
                <div class="mr"><div class="rd L"></div><div class="ms">0–3</div><div class="mo">Arsenal</div><div class="mc">PL</div></div>
                <div class="mr"><div class="rd W"></div><div class="ms">1–0</div><div class="mo">Brentford</div><div class="mc">PL</div></div>
                <div class="mr"><div class="rd D"></div><div class="ms">1–1</div><div class="mo">Fulham</div><div class="mc">PL</div></div>
                <div class="mr"><div class="rd L"></div><div class="ms">1–2</div><div class="mo">Chelsea</div><div class="mc">PL</div></div>
              </div>
            </div>
          </div>
          <div style="padding:0 14px 14px; font-size:11px; color:var(--hi);"><strong>H2H:</strong> TOT 2-1 BHA, BHA 4-2 TOT, TOT 2-1 BHA, BHA 0-1 TOT, TOT 0-1 BHA.</div>
        </div>

        <div class="card fw">
          <div class="card-hd"><div class="hd-title">Weighted Stat Projections</div></div>
          <div class="card-body" style="padding:0;">
            <div class="table-wrapper"><table class="pt">
              <thead><tr><th>Metric</th><th>Low</th><th class="th-m">Median</th><th>High</th></tr></thead>
              <tbody>
                <tr><td class="cmc">Corners</td><td>9</td><td><span class="mv">12</span> <div class="split-stats"><span>TOT: 7</span><span>BHA: 5</span></div></td><td>16</td></tr>
                <tr><td class="cmc">Shots</td><td>26</td><td><span class="mv">33</span> <div class="split-stats"><span>TOT: 18</span><span>BHA: 15</span></div></td><td>42</td></tr>
                <tr><td class="cmc">Shots on Target</td><td>9</td><td><span class="mv">12</span> <div class="split-stats"><span>TOT: 7</span><span>BHA: 5</span></div></td><td>18</td></tr>
                <tr><td class="cmc">Fouls</td><td>18</td><td><span class="mv">24</span> <div class="split-stats"><span>TOT: 12</span><span>BHA: 12</span></div></td><td>30</td></tr>
                <tr><td class="cmc">Throw-ins</td><td>30</td><td><span class="mv">36</span> <div class="split-stats"><span>TOT: 18</span><span>BHA: 18</span></div></td><td>44</td></tr>
                <tr><td class="cmc">Goal Kicks</td><td>15</td><td><span class="mv">20</span> <div class="split-stats"><span>TOT: 9</span><span>BHA: 11</span></div></td><td>26</td></tr>
                <tr><td class="cmc">Tackles</td><td>30</td><td><span class="mv">38</span> <div class="split-stats"><span>TOT: 20</span><span>BHA: 18</span></div></td><td>48</td></tr>
              </tbody>
            </table></div>
          </div>
        </div>

        <div class="card fw">
          <div class="card-hd"><div class="hd-title">🟨 Card Risks</div></div>
          <div class="card-body yc-grid">
            <div class="yc-row"><div class="yc-icon">🟨</div><div class="yc-info"><div class="yc-name">Cristian Romero</div><div class="yc-club">TOT · CB</div><div class="yc-reason">High line exposes him to footraces. Physical enforcer.</div></div><div class="yc-risk risk-h">HIGH</div></div>
            <div class="yc-row"><div class="yc-icon">🟨</div><div class="yc-info"><div class="yc-name">Lewis Dunk</div><div class="yc-club">BHA · CB</div><div class="yc-reason">Will face Son/Kulusevski pace. Tactical fouls likely.</div></div><div class="yc-risk risk-m">MED</div></div>
          </div>
        </div>
      </div>
    </div>
  </div>


  <div id="m5" style="background:linear-gradient(135deg, var(--che-l) 0%, var(--bg2) 50%, var(--mun-l) 100%); border-radius:12px; overflow:hidden; margin-bottom:24px; border:1px solid var(--border);">
    <div class="match-hero">
      <div class="hero-inner">
        <div class="h-team">
          <div class="badge-wrap"><img src="https://upload.wikimedia.org/wikipedia/en/thumb/c/cc/Chelsea_FC.svg/120px-Chelsea_FC.svg.png" alt="Chelsea" style="background: transparent;"></div>
          <div class="h-name">Chelsea</div>
        </div>
        <div class="vs-col"><div class="vs-txt">VS</div><div class="ko-chip">Stamford Bridge</div></div>
        <div class="h-team">
          <div class="badge-wrap"><img src="https://upload.wikimedia.org/wikipedia/en/thumb/7/7a/Manchester_United_FC_crest.svg/120px-Manchester_United_FC_crest.svg.png" alt="Man Utd" style="background: transparent;"></div>
          <div class="h-name">Man Utd</div>
        </div>
      </div>
    </div>
    
    <div class="card-body" style="padding-top:0;">
      <div class="score-box fw" style="margin-top:16px;">
        <div class="sb-title">Heavyweight Rivalry Prediction</div>
        <div class="scores-row">
          <div class="sc"><div class="sc-label">Half-Time</div><div class="sc-value" style="color:var(--md)">1 – 1</div><div class="sc-prob">Transition heavy</div></div>
          <div class="sc sc-best"><div class="sc-label">Full-Time</div><div class="sc-value" style="color:var(--pl-pink)">2 – 2</div><div class="sc-prob">Entertaining Draw</div></div>
        </div>
        <div class="sb-notes"><strong>Rationale:</strong> Both sides possess elite attacking talent but structural midfield flaws. Historically this fixture produces drama, penalties, and late goals. A high-scoring draw fits the data profiles perfectly.</div>
      </div>

      <div class="dg">
        <div class="card fw">
          <div class="card-hd"><div class="hd-title">Form & H2H (Last 5)</div></div>
          <div class="card-body form-cols">
            <div class="fcol">
              <div class="team-lab" style="background:var(--che-l); border-color:var(--che-b);">Chelsea</div>
              <div class="match-list">
                <div class="mr"><div class="rd W"></div><div class="ms">2–0</div><div class="mo">Bournemouth</div><div class="mc">PL</div></div>
                <div class="mr"><div class="rd W"></div><div class="ms">2–1</div><div class="mo">Brighton</div><div class="mc">PL</div></div>
                <div class="mr"><div class="rd L"></div><div class="ms">0–2</div><div class="mo">Man City</div><div class="mc">PL</div></div>
                <div class="mr"><div class="rd D"></div><div class="ms">2–2</div><div class="mo">Brentford</div><div class="mc">PL</div></div>
                <div class="mr"><div class="rd W"></div><div class="ms">3–1</div><div class="mo">Everton</div><div class="mc">PL</div></div>
              </div>
            </div>
            <div class="fcol">
              <div class="team-lab" style="background:var(--mun-l); border-color:var(--mun-r);">Man Utd</div>
              <div class="match-list">
                <div class="mr"><div class="rd L"></div><div class="ms">1–3</div><div class="mo">Arsenal</div><div class="mc">PL</div></div>
                <div class="mr"><div class="rd W"></div><div class="ms">3–1</div><div class="mo">Newcastle</div><div class="mc">PL</div></div>
                <div class="mr"><div class="rd D"></div><div class="ms">1–1</div><div class="mo">Liverpool</div><div class="mc">PL</div></div>
                <div class="mr"><div class="rd W"></div><div class="ms">2–0</div><div class="mo">West Ham</div><div class="mc">PL</div></div>
                <div class="mr"><div class="rd L"></div><div class="ms">0–1</div><div class="mo">Crystal Palace</div><div class="mc">PL</div></div>
              </div>
            </div>
          </div>
          <div style="padding:0 14px 14px; font-size:11px; color:var(--hi);"><strong>H2H:</strong> MUN 2-1 CHE, CHE 4-3 MUN, MUN 4-1 CHE, CHE 1-1 MUN, MUN 1-1 CHE.</div>
        </div>

        <div class="card fw">
          <div class="card-hd"><div class="hd-title">Weighted Stat Projections</div></div>
          <div class="card-body" style="padding:0;">
            <div class="table-wrapper"><table class="pt">
              <thead><tr><th>Metric</th><th>Low</th><th class="th-m">Median</th><th>High</th></tr></thead>
              <tbody>
                <tr><td class="cmc">Corners</td><td>10</td><td><span class="mv">13</span> <div class="split-stats"><span>CHE: 7</span><span>MUN: 6</span></div></td><td>17</td></tr>
                <tr><td class="cmc">Shots</td><td>26</td><td><span class="mv">32</span> <div class="split-stats"><span>CHE: 17</span><span>MUN: 15</span></div></td><td>42</td></tr>
                <tr><td class="cmc">Shots on Target</td><td>9</td><td><span class="mv">12</span> <div class="split-stats"><span>CHE: 6</span><span>MUN: 6</span></div></td><td>17</td></tr>
                <tr><td class="cmc">Fouls</td><td>22</td><td><span class="mv">27</span> <div class="split-stats"><span>CHE: 13</span><span>MUN: 14</span></div></td><td>34</td></tr>
                <tr><td class="cmc">Throw-ins</td><td>32</td><td><span class="mv">38</span> <div class="split-stats"><span>CHE: 19</span><span>MUN: 19</span></div></td><td>46</td></tr>
                <tr><td class="cmc">Goal Kicks</td><td>15</td><td><span class="mv">19</span> <div class="split-stats"><span>CHE: 9</span><span>MUN: 10</span></div></td><td>26</td></tr>
                <tr><td class="cmc">Tackles</td><td>32</td><td><span class="mv">40</span> <div class="split-stats"><span>CHE: 20</span><span>MUN: 20</span></div></td><td>50</td></tr>
              </tbody>
            </table></div>
          </div>
        </div>

        <div class="card fw">
          <div class="card-hd"><div class="hd-title">🟨 Card Risks</div></div>
          <div class="card-body yc-grid">
            <div class="yc-row"><div class="yc-icon">🟨</div><div class="yc-info"><div class="yc-name">Moisés Caicedo</div><div class="yc-club">CHE · DM</div><div class="yc-reason">Central battle against Mainoo/Fernandes. Extremely combative.</div></div><div class="yc-risk risk-h">HIGH</div></div>
            <div class="yc-row"><div class="yc-icon">🟨</div><div class="yc-info"><div class="yc-name">Bruno Fernandes</div><div class="yc-club">MUN · AM</div><div class="yc-reason">Dissent, tactical fouls. Emotionally charged in big six clashes.</div></div><div class="yc-risk risk-h">HIGH</div></div>
            <div class="yc-row"><div class="yc-icon">🟨</div><div class="yc-info"><div class="yc-name">Marc Cucurella</div><div class="yc-club">CHE · LB</div><div class="yc-reason">Aggressive defending against Garnacho/Antony pace.</div></div><div class="yc-risk risk-m">MED</div></div>
          </div>
        </div>
      </div>
    </div>
  </div>


</div> <footer style="text-align: center; padding: 24px 16px; font-family:'Inter',sans-serif; font-size: 11px; color: var(--muted); border-top: 1px solid var(--border);">
  <strong>Team Bilbo Statistical Analysis</strong><br>
  Predictions are statistical estimates based on historical profiles and Premier League dynamics.<br>
  · Generated 2026 · Not Financial Advice ·
</footer>

<script>
(function(){
  'use strict';
  var cards=document.querySelectorAll('.card');
  if('IntersectionObserver' in window){
    var obs=new IntersectionObserver(function(e){
      e.forEach(function(entry){if(entry.isIntersecting){entry.target.classList.add('vis');obs.unobserve(entry.target);}});
    },{threshold:0.05});
    cards.forEach(function(c){obs.observe(c);});
  } else{cards.forEach(function(c){c.classList.add('vis');});}
})();
</script>
