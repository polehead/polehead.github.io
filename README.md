<html lang="en">

<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Matchday Analytics · PL Predictor · 22 April 2026</title>
  <link rel="preconnect" href="https://fonts.googleapis.com">
  <link
    href="https://fonts.googleapis.com/css2?family=Exo+2:wght@300;400;500;600;700;800;900&family=Inter:wght@300;400;500;600&display=swap"
    rel="stylesheet">
  <style>
    :root {
      --bou-primary: #b50e12;
      --bou-secondary: #000000;
      --lee-primary: #1d428a;
      --lee-secondary: #ffcd00;
      --bur-primary: #6c1d45;
      --bur-secondary: #99c5e7;
      --mci-primary: #6cabdd;
      --mci-secondary: #1c2c5b;

      /* Match specific lights */
      --bou-light: rgba(181, 14, 18, 0.15);
      --lee-light: rgba(29, 66, 138, 0.15);
      --bur-light: rgba(108, 29, 69, 0.15);
      --mci-light: rgba(108, 171, 221, 0.15);

      /* UI */
      --bg: #06080f;
      --bg2: #0b0e1c;
      --bg3: #111628;
      --bg4: #171e32;
      --bg5: #1d263d;
      --border: rgba(255, 255, 255, 0.07);
      --border2: rgba(255, 255, 255, 0.13);
      --text: #c2cde4;
      --muted: #4a5a7a;
      --label: #8093b5;
      --white: #fff;

      /* Stat colours */
      --green: #0fd9a2;
      --amber: #f7c948;
      --red: #f5522a;
      --purple: #a78bfa;

      /* PL */
      --pl-purple: #37003c;
      --pl-green: #00ff85;
    }

    *,
    *::before,
    *::after {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
    }

    html {
      scroll-behavior: smooth;
    }

    body {
      font-family: 'Inter', sans-serif;
      background: var(--bg);
      color: var(--text);
      font-size: 14px;
      line-height: 1.55;
      -webkit-font-smoothing: antialiased;
      overflow-x: hidden;
    }

    /* ─── ANIMATIONS ─── */
    @keyframes fadeUp {
      from {
        opacity: 0;
        transform: translateY(20px);
      }

      to {
        opacity: 1;
        transform: translateY(0);
      }
    }

    @keyframes popIn {
      from {
        transform: scale(5) rotate(-10deg);
        opacity: 0;
      }

      to {
        transform: scale(1) rotate(360);
        opacity: 1;
      }
    }

    /* ─── BACKGROUND ─── */
    .bg-layer {
      position: fixed;
      inset: 0;
      z-index: 0;
      pointer-events: none;
      background:
        radial-gradient(ellipse 70% 50% at 15% 10%, rgba(0, 87, 184, .07), transparent 60%),
        radial-gradient(ellipse 60% 45% at 85% 80%, rgba(3, 70, 148, .06), transparent 60%),
        repeating-linear-gradient(0deg, transparent, transparent 55px, rgba(255, 255, 255, .012) 55px, rgba(255, 255, 255, .012) 56px),
        repeating-linear-gradient(90deg, transparent, transparent 55px, rgba(255, 255, 255, .012) 55px, rgba(255, 255, 255, .012) 56px);
    }

    /* ─── PAGE HEADER ─── */
    .page-hd {
      background: linear-gradient(150deg, #050820 0%, #070022 55%, #050820 100%);
      border-bottom: 2px solid rgba(55, 0, 60, .8);
      padding: 20px 20px 16px;
      text-align: center;
      position: relative;
      overflow: hidden;
    }

    .page-hd::before {
      content: '';
      position: absolute;
      inset: 0;
      background: radial-gradient(ellipse 110% 60% at 50% -10%, rgba(0, 255, 133, .07), transparent 65%);
    }

    .pl-badge {
      display: inline-flex;
      align-items: center;
      gap: 7px;
      font-family: 'Exo 2', sans-serif;
      font-size: 10px;
      font-weight: 700;
      letter-spacing: 2.5px;
      text-transform: uppercase;
      color: var(--pl-green);
      background: rgba(0, 255, 133, .08);
      border: 1px solid rgba(0, 255, 133, .25);
      padding: 4px 14px;
      border-radius: 20px;
      margin-bottom: 10px;
      position: relative;
    }

    .page-hd h1 {
      font-family: 'Exo 2', sans-serif;
      font-size: clamp(22px, 4.5vw, 40px);
      font-weight: 900;
      letter-spacing: .5px;
      color: #fff;
      line-height: 1.05;
      position: relative;
    }

    .page-hd h1 span {
      color: var(--pl-green);
    }

    .page-hd .sub {
      font-size: 11.5px;
      color: var(--muted);
      margin-top: 5px;
      position: relative;
    }

    /* ─── MAIN CONTAINER ─── */
    .wrap {
      position: relative;
      z-index: 1;
      max-width: 1260px;
      margin: 0 auto;
      padding: 0 14px 64px;
    }

    /* ─── HERO MATCH CARD ─── */
    .hero-card {
      border-radius: 16px;
      border: 1px solid var(--border2);
      overflow: hidden;
      margin-top: 30px;
      box-shadow: 0 12px 60px rgba(0, 0, 0, .55);
      animation: fadeUp .55s ease both;
    }

    .bou-lee-bg {
      background: linear-gradient(135deg, var(--bou-light) 0%, var(--bg2) 45%, var(--lee-light) 100%);
    }

    .bur-mci-bg {
      background: linear-gradient(135deg, var(--bur-light) 0%, var(--bg2) 45%, var(--mci-light) 100%);
    }

    .hero-inner {
      padding: 28px 22px 22px;
      display: flex;
      flex-direction: column;
      align-items: center;
      gap: 14px;
    }

    .hero-meta {
      display: flex;
      gap: 8px;
      flex-wrap: wrap;
      justify-content: center;
    }

    .hm-chip {
      font-family: 'Exo 2', sans-serif;
      font-size: 9.5px;
      font-weight: 700;
      letter-spacing: 1.5px;
      text-transform: uppercase;
      padding: 3px 10px;
      border-radius: 4px;
      border: 1px solid;
    }

    .teams-row {
      display: grid;
      grid-template-columns: 1fr auto 1fr;
      align-items: center;
      gap: 16px;
      width: 100%;
      max-width: 580px;
    }

    .team-col {
      display: flex;
      flex-direction: column;
      align-items: center;
      gap: 8px;
    }

    .badge-ring {
      width: 82px;
      height: 82px;
      background: rgba(255, 255, 255, .04);
      border: 1.5px solid var(--border2);
      border-radius: 50%;
      display: flex;
      align-items: center;
      justify-content: center;
      overflow: hidden;
      transition: transform .35s cubic-bezier(.34, 1.56, .64, 1);
      animation: popIn .55s cubic-bezier(.34, 1.56, .64, 1) both;
    }

    .badge-ring:hover {
      transform: scale(1.12) rotate(5deg);
    }

    .badge-ring img {
      width: 60px;
      height: 60px;
      object-fit: contain;
    }

    .team-name {
      font-family: 'Exo 2', sans-serif;
      font-size: 14px;
      font-weight: 800;
      text-transform: uppercase;
      letter-spacing: .5px;
      text-align: center;
      color: #fff;
    }

    .team-meta {
      font-size: 9.5px;
      color: var(--muted);
      text-align: center;
      line-height: 1.5;
    }

    .vs-col {
      display: flex;
      flex-direction: column;
      align-items: center;
      gap: 5px;
    }

    .vs-txt {
      font-family: 'Exo 2', sans-serif;
      font-size: 22px;
      font-weight: 900;
      color: rgba(255, 255, 255, .08);
      letter-spacing: 3px;
    }

    .ko-tag {
      font-family: 'Exo 2', sans-serif;
      font-size: 10px;
      font-weight: 700;
      letter-spacing: 1.5px;
      color: var(--amber);
      background: rgba(247, 201, 72, .09);
      border: 1px solid rgba(247, 201, 72, .28);
      padding: 2px 8px;
      border-radius: 4px;
    }

    .mot-row {
      display: flex;
      align-items: center;
      gap: 10px;
      width: 100%;
      max-width: 580px;
      background: rgba(255, 255, 255, .03);
      border: 1px solid var(--border);
      border-radius: 8px;
      padding: 10px 14px;
    }

    .mot-lbl {
      font-family: 'Exo 2', sans-serif;
      font-size: 9px;
      font-weight: 700;
      letter-spacing: 1.2px;
      text-transform: uppercase;
      color: var(--muted);
    }

    .mot-track {
      flex: 1;
      height: 6px;
      background: rgba(255, 255, 255, .07);
      border-radius: 3px;
      overflow: hidden;
    }

    .mot-bar {
      height: 100%;
      border-radius: 3px;
      transition: width 1s ease .4s;
      width: 0;
    }

    .mot-val {
      font-family: 'Exo 2', sans-serif;
      font-size: 13px;
      font-weight: 800;
    }

    .odds-row {
      display: flex;
      gap: 8px;
      flex-wrap: wrap;
      justify-content: center;
      width: 100%;
      max-width: 520px;
    }

    .odds-box {
      flex: 1;
      min-width: 90px;
      max-width: 145px;
      background: var(--bg3);
      border: 1px solid var(--border);
      border-radius: 9px;
      padding: 11px 8px;
      text-align: center;
      transition: border-color .25s, transform .25s;
    }

    .odds-box:hover {
      transform: translateY(-2px);
      border-color: var(--border2);
    }

    .ob-lbl {
      font-size: 9px;
      text-transform: uppercase;
      letter-spacing: 1px;
      color: var(--muted);
    }

    .ob-odds {
      font-family: 'Exo 2', sans-serif;
      font-size: 23px;
      font-weight: 800;
      color: #fff;
      margin: 3px 0;
      line-height: 1;
    }

    .ob-impl {
      font-size: 9.5px;
      color: var(--label);
    }

    .ob-val {
      border-color: rgba(247, 201, 72, .38) !important;
      background: linear-gradient(135deg, rgba(247, 201, 72, .07), var(--bg3)) !important;
    }

    /* ─── GRID & CARDS ─── */
    .grid {
      display: grid;
      grid-template-columns: 1fr;
      gap: 16px;
      margin-top: 20px;
    }

    @media(min-width:860px) {
      .grid {
        grid-template-columns: 1fr 1fr;
      }

      .span2 {
        grid-column: 1 / -1;
      }
    }

    .card {
      background: var(--bg2);
      border: 1px solid var(--border);
      border-radius: 12px;
      overflow: hidden;
      box-shadow: 0 4px 28px rgba(0, 0, 0, .35);
      animation: fadeUp .5s ease both;
    }

    .card-hd {
      padding: 11px 18px 9px;
      border-bottom: 1px solid var(--border);
      display: flex;
      align-items: center;
      gap: 8px;
    }

    .hd-dot {
      width: 5px;
      height: 5px;
      border-radius: 50%;
    }

    .hd-title {
      font-family: 'Exo 2', sans-serif;
      font-size: 9.5px;
      font-weight: 700;
      letter-spacing: 2px;
      text-transform: uppercase;
      color: var(--muted);
      flex: 1;
    }

    .card-body {
      padding: 14px 18px;
    }

    /* ─── MODULES ─── */
    .ctx {
      background: rgba(255, 255, 255, .025);
      border: 1px solid var(--border2);
      border-radius: 8px;
      padding: 12px 14px;
      font-size: 12.5px;
      line-height: 1.75;
      color: var(--label);
    }

    .ctx strong {
      color: var(--amber);
      font-weight: 700;
    }

    .inline-note {
      background: var(--bg3);
      border-radius: 6px;
      padding: 10px 12px;
      border: 1px solid var(--border);
      font-size: 12px;
      color: var(--label);
      line-height: 1.7;
      margin-bottom: 12px;
      border-left: 3px solid var(--amber);
    }

    .inline-note strong {
      color: #fff;
    }

    .xg-row {
      display: flex;
      flex-wrap: wrap;
      gap: 8px;
      margin-top: 10px;
      margin-bottom: 15px;
      background: linear-gradient(135deg, rgba(15, 217, 162, .06), rgba(15, 217, 162, .02));
      border: 1px solid rgba(15, 217, 162, .22);
      border-radius: 7px;
      padding: 10px 12px;
    }

    .xg-item {
      flex: 1;
      min-width: 80px;
      text-align: center;
    }

    .xg-v {
      font-family: 'Exo 2', sans-serif;
      font-size: 22px;
      font-weight: 800;
      line-height: 1;
    }

    .xg-l {
      font-size: 8px;
      color: var(--muted);
      text-transform: uppercase;
      letter-spacing: .5px;
      margin-top: 2px;
    }

    .score-zone {
      border-radius: 10px;
      padding: 16px;
      background: linear-gradient(135deg, rgba(255, 255, 255, .04), rgba(255, 255, 255, .01));
      border: 1px solid var(--border2);
      display: flex;
      flex-direction: column;
      gap: 12px;
    }

    .sz-head {
      font-family: 'Exo 2', sans-serif;
      font-size: 9.5px;
      font-weight: 700;
      letter-spacing: 2.5px;
      text-transform: uppercase;
      color: var(--muted);
      text-align: center;
    }

    .s-boxes {
      display: flex;
      gap: 8px;
      justify-content: center;
      flex-wrap: wrap;
    }

    .sbox {
      flex: 1;
      min-width: 108px;
      max-width: 160px;
      background: var(--bg3);
      border: 1px solid var(--border);
      border-radius: 9px;
      padding: 12px 8px;
      text-align: center;
    }

    .sbox.feat {
      border-color: rgba(247, 201, 72, .4);
      background: linear-gradient(135deg, rgba(247, 201, 72, .07), var(--bg3));
    }

    .sb-lbl {
      font-size: 8.5px;
      text-transform: uppercase;
      letter-spacing: 1px;
      color: var(--muted);
    }

    .sb-score {
      font-family: 'Exo 2', sans-serif;
      font-size: 30px;
      font-weight: 900;
      color: #fff;
      letter-spacing: 2px;
      margin: 4px 0;
      line-height: 1;
    }

    .sb-prob {
      font-size: 9.5px;
      color: var(--muted);
    }

    .safe-box {
      background: linear-gradient(135deg, rgba(15, 217, 162, .07), rgba(15, 217, 162, .02));
      border: 1px solid rgba(15, 217, 162, .25);
      border-radius: 7px;
      padding: 10px 12px;
      font-size: 12px;
      color: var(--label);
      line-height: 1.7;
      margin-top: 10px;
    }

    .safe-box strong {
      color: var(--green);
      font-weight: 700;
    }

    .pred-table {
      width: 100%;
      border-collapse: collapse;
      border-radius: 6px;
    }

    .pred-table th {
      font-family: 'Exo 2', sans-serif;
      font-size: 10px;
      font-weight: 700;
      letter-spacing: 1px;
      text-transform: uppercase;
      color: var(--muted);
      padding: 0 6px 10px;
      text-align: left;
      border-bottom: 1px solid var(--border);
    }

    .pred-table td {
      padding: 9px 6px;
      border-bottom: 1px solid rgba(255, 255, 255, .03);
      font-size: 12px;
      color: var(--label);
      font-weight: 600;
    }

    .pred-table td.tv {
      text-align: center;
      font-family: 'Exo 2', sans-serif;
      font-size: 14px;
      font-weight: 700;
    }

    .val-low {
      color: var(--text);
      opacity: 0.7;
    }

    .val-exp {
      color: var(--amber);
      font-size: 16px !important;
    }

    .val-high {
      color: var(--text);
      opacity: 0.7;
    }

    .yc-list {
      display: flex;
      flex-direction: column;
      gap: 7px;
    }

    .yc-row {
      display: flex;
      align-items: flex-start;
      gap: 10px;
      background: var(--bg3);
      border: 1px solid var(--border);
      border-radius: 8px;
      padding: 9px 11px;
    }

    .yc-name {
      font-size: 12.5px;
      font-weight: 700;
      color: #fff;
    }

    .yc-club {
      font-family: 'Exo 2', sans-serif;
      font-size: 9px;
      letter-spacing: .7px;
      text-transform: uppercase;
      margin-left: 5px;
      color: var(--muted);
    }

    .yc-reason {
      font-size: 11px;
      color: var(--muted);
      margin-top: 2px;
    }

    .bet-grid {
      display: grid;
      grid-template-columns: 1fr 1fr;
      gap: 8px;
      margin-bottom: 12px;
    }

    .bet-cell {
      background: var(--bg3);
      border: 1px solid var(--border);
      border-radius: 8px;
      padding: 11px 13px;
    }

    .bet-cell.bval {
      border-color: rgba(247, 201, 72, .38);
      background: linear-gradient(135deg, rgba(247, 201, 72, .07), var(--bg3));
    }

    .bc-mkt {
      font-size: 9px;
      text-transform: uppercase;
      letter-spacing: 1px;
      color: var(--muted);
      margin-bottom: 3px;
    }

    .bc-line {
      font-family: 'Exo 2', sans-serif;
      font-size: 18px;
      font-weight: 800;
      color: #fff;
      line-height: 1;
    }
  </style>
</head>

<body>
  <div class="bg-layer"></div>

  <header class="page-hd">
    <div class="pl-badge">
      <svg width="10" height="10" viewBox="0 0 1 1" fill="none" xmlns="http://www.w3.org/2000/svg">
  <path
    d="M0.773542 0.613333L1 0.5L0.773542 0.386667L0.853542 0.146458L0.613333 0.226458L0.5 0L0.386667 0.226458L0.146458 0.146458L0.226458 0.386667L0 0.5L0.226458 0.613333L0.146458 0.853542L0.386667 0.773542L0.5 1L0.613333 0.773542L0.853542 0.853542L0.773542 0.613333Z"
    fill="#00ff85"
  />
</svg>
      Team Bilbo Analytics
      <svg width="10" height="10" viewBox="0 0 1 1" fill="none" xmlns="http://www.w3.org/2000/svg">
  <path
    d="M0.773542 0.613333L1 0.5L0.773542 0.386667L0.853542 0.146458L0.613333 0.226458L0.5 0L0.386667 0.226458L0.146458 0.146458L0.226458 0.386667L0 0.5L0.226458 0.613333L0.146458 0.853542L0.386667 0.773542L0.5 1L0.613333 0.773542L0.853542 0.853542L0.773542 0.613333Z"
    fill="#00ff85"
  />
    </div>
    <h1>Data-Driven <span>Matchday</span> Analytics</h1>
    <p class="sub">Prop Variance Modeling & Referee Impact · 22 April 2026</p>
  </header>

  <div class="wrap">

    <div class="hero-card bou-lee-bg">
      <div class="hero-inner">
        <div class="hero-meta">
          <span class="hm-chip" style="color: var(--pl-green); border-color: rgba(120, 78, 124, 0.3);">Matchday 34</span>
        </div>

        <div class="teams-row">
          <div class="team-col">
            <div class="badge-ring"><img
                src="https://images.gc.afcbournemouthservices.co.uk/fit-in/170x170/e430db60-34ca-11ef-a088-db17c0a14148.png"
                alt="BOU" style="background: transparent;"></div>
            <div class="team-name">Bournemouth</div>
            <div class="team-meta">9th Place (48 pts)<br>Home</div>
          </div>
          <div class="vs-col">
            <span class="ko-tag">22:00</span>
            <span class="vs-txt">V</span>
          </div>
          <div class="team-col">
            <div class="badge-ring"><img
                src="https://contentfulproxy.stadion.io/phva2knh4vy5/59uDDesQq19p5lVzfe45BY/a89feaa950427ef005c9d028e925bef0/Full_colour_crest.png?fm=webp&fit=pad&f=center&w=144&h=144&q=100"
                alt="LEE" style="background: transparent;"></div>
            <div class="team-name">Leeds United</div>
            <div class="team-meta">15th Place (39 pts)<br>Away</div>
          </div>
        </div>

        <div class="mot-row">
          <span class="mot-lbl">Motivation Index</span>
          <div class="mot-track">
            <div class="mot-bar" style="background: var(--bou-primary);" data-p="85" id="mot-bou1"></div>
          </div>
          <span class="mot-val" style="color: #fff;">85%</span>
          <span style="color:var(--muted); font-size:10px; margin: 0 5px;">|</span>
          <span class="mot-val" style="color: #fff;">65%</span>
          <div class="mot-track">
            <div class="mot-bar" style="background: var(--lee-primary); float: right;" data-p="65" id="mot-lee1"></div>
          </div>
        </div>
      </div>
    </div>

    <div class="grid">
      <div class="card">
        <div class="card-hd">
          <div class="hd-dot" style="background: var(--amber);"></div>
          <div class="hd-title">Context & Lineup Strength</div>
        </div>
        <div class="card-body">
          <div class="ctx" style="margin-bottom: 12px;">
            Bournemouth sit comfortably in 9th, holding a <strong>13-game unbeaten home run</strong>. They generate a
            high volume of set-pieces at the Vitality. Leeds United (39 pts) are safe from the drop and lean heavily on
            direct play and wing-back crossing, making them dangerous but structurally open on the counter.
          </div>
          <div
            style="font-size: 11px; color: var(--muted); text-transform: uppercase; letter-spacing: 1px; margin-bottom: 6px;">
            Injuries / Suspensions</div>
          <ul style="font-size: 12px; color: var(--label); padding-left: 15px; line-height: 1.6; margin-bottom: 15px;">
            <li><strong style="color:#fff;">BOU:</strong> Justin Kluivert (Out - Hamstring), Lewis Cook (Doubtful).</li>
            <li><strong style="color:#fff;">LEE:</strong> No major suspensions; potential rotation for Karl Darlow in
              goal.</li>
          </ul>

          <div class="inline-note">
            <strong>Referee Profile: Anthony Taylor</strong><br>
            Averages 21.5 fouls and 4.2 yellows per match this season. Known to let physical play go but strict on
            tactical fouls, increasing the likelihood of cards for transition-stopping tackles on the counter.
          </div>
        </div>
      </div>

      <div class="card">
        <div class="card-hd">
          <div class="hd-dot" style="background: var(--purple);"></div>
          <div class="hd-title">Prop Variance Model (Match Totals)</div>
        </div>
        <div class="card-body">
          <div class="xg-row">
            <div class="xg-item">
              <div class="xg-v">1.67</div>
              <div class="xg-l">BOU xG / 90</div>
            </div>
            <div class="xg-item">
              <div class="xg-v">1.22</div>
              <div class="xg-l">LEE xG / 90</div>
            </div>
          </div>
          <table class="pred-table">
            <thead>
              <tr>
                <th>Match Metric</th>
                <th style="text-align:center;">Low Var.</th>
                <th style="text-align:center; color: var(--amber);">Expected</th>
                <th style="text-align:center;">High Var.</th>
              </tr>
            </thead>
            <tbody>
              <tr>
                <td>Tackles Attempted</td>
                <td class="tv val-low">25</td>
                <td class="tv val-exp">34</td>
                <td class="tv val-high">42</td>
              </tr>
              <tr>
                <td>Corners</td>
                <td class="tv val-low">8</td>
                <td class="tv val-exp">10.5</td>
                <td class="tv val-high">14</td>
              </tr>
              <tr>
                <td>Total Shots</td>
                <td class="tv val-low">20</td>
                <td class="tv val-exp">26</td>
                <td class="tv val-high">32</td>
              </tr>
              <tr>
                <td>Shots on Target</td>
                <td class="tv val-low">6</td>
                <td class="tv val-exp">9</td>
                <td class="tv val-high">13</td>
              </tr>
              <tr>
                <td>Fouls Committed</td>
                <td class="tv val-low">18</td>
                <td class="tv val-exp">23</td>
                <td class="tv val-high">28</td>
              </tr>
              <tr>
                <td>Throw-ins</td>
                <td class="tv val-low">30</td>
                <td class="tv val-exp">38</td>
                <td class="tv val-high">45</td>
              </tr>
              <tr>
                <td>Goal Kicks</td>
                <td class="tv val-low">11</td>
                <td class="tv val-exp">15</td>
                <td class="tv val-high">19</td>
              </tr>
            </tbody>
          </table>
          <div style="font-size: 10px; color: var(--muted); text-align: right; margin-top: 8px;">*Data mapped via
            <a href="https://github.com/polehead">💀</a></div>
        </div>
      </div>

      <div class="card span2">
        <div class="card-hd">
          <div class="hd-dot" style="background: var(--green);"></div>
          <div class="hd-title">Algorithmic Score Modeling & Betting Angles</div>
        </div>
        <div class="card-body">
          <div class="score-zone">
            <div class="sz-head">Expected Result Variance</div>
            <div class="s-boxes">
              <div class="sbox">
                <div class="sb-lbl">Low Variance</div>
                <div class="sb-score">1 - 0</div>
                <div class="sb-prob">Scrappy Midfield Battle</div>
              </div>
              <div class="sbox feat">
                <div class="sb-lbl" style="color: var(--amber);">Median Expectation</div>
                <div class="sb-score feat-s">2 - 2</div>
                <div class="sb-prob">High Transition Play</div>
              </div>
              <div class="sbox">
                <div class="sb-lbl">High Variance</div>
                <div class="sb-score">4 - 3</div>
                <div class="sb-prob">Defensive Collapse</div>
              </div>
            </div>
            <div class="safe-box">
              <strong>Safe Prediction: BOU 2 - 1 LEE</strong><br>
              Bournemouth's home dominance combined with Leeds' leaky away defense heavily favors a home win. Expect
              Leeds to force a high volume of <strong>goal kicks (Expected 15)</strong> from Bournemouth due to
              inaccurate direct crossing.
            </div>
          </div>

          <div style="display: grid; grid-template-columns: 1fr 1fr; gap: 16px; margin-top: 16px;">
            <div>
              <div
                style="font-size: 11px; color: var(--muted); text-transform: uppercase; letter-spacing: 1px; margin-bottom: 8px;">
                Card Market Targets (Ref Impacted)</div>
              <div class="yc-list">
                <div class="yc-row">
                  <div class="yc-info">
                    <div class="yc-name">Marcos Senesi <span class="yc-club">BOU</span></div>
                    <div class="yc-reason">High volume of tactical fouls. Taylor heavily penalizes disruption of
                      counters.</div>
                  </div>
                </div>
                <div class="yc-row">
                  <div class="yc-info">
                    <div class="yc-name">Ethan Ampadu <span class="yc-club">LEE</span></div>
                    <div class="yc-reason">Tasked with breaking up transition in central areas. High tackle volume
                      expected.</div>
                  </div>
                </div>
              </div>
            </div>
            <div>
              <div
                style="font-size: 11px; color: var(--muted); text-transform: uppercase; letter-spacing: 1px; margin-bottom: 8px;">
                Betting Patterns & Value</div>
              <div class="bet-grid" style="grid-template-columns: 1fr;">
                <div class="bet-cell bval">
                  <div class="bc-mkt">Bet365 Popular Accumulator</div>
                  <div class="bc-line" style="color: var(--amber);">BOU Win + Over 2.5 Goals</div>
                  <div class="bc-rsn">Priced at 2.45 (29/20) - Backed heavily by form data.</div>
                </div>
                <div class="bet-cell">
                  <div class="bc-mkt">Prop Builder Value</div>
                  <div class="bc-line">Over 14.5 Goal Kicks</div>
                  <div class="bc-rsn">Priced at 5/6. Leeds' direct play skews goal kicks heavily.</div>
                </div>
              </div>
            </div>
          </div>

        </div>
      </div>
    </div>


    <div class="hero-card bur-mci-bg" style="margin-top: 50px;">
      <div class="hero-inner">
        <div class="hero-meta">
          <span class="hm-chip" style="color: var(--pl-green); border-color: rgba(0,255,133,.3);">Matchday 34</span>
        </div>

        <div class="teams-row">
          <div class="team-col">
            <div class="badge-ring"><img
                src="https://cdn.brandfetch.io/idATU8hDrd/theme/dark/logo.svg?c=1bxid64Mup7aczewSAYMX&t=1668077989078"
                alt="BUR" style="background: transparent;"></div>
            <div class="team-name">Burnley</div>
            <div class="team-meta">19th Place (20 pts)<br>Home</div>
          </div>
          <div class="vs-col">
            <span class="ko-tag">20:00</span>
            <span class="vs-txt">V</span>
          </div>
          <div class="team-col">
            <div class="badge-ring"><img
                src="https://cdn.brandfetch.io/idNRR8KZnO/theme/dark/logo.svg?c=1bxid64Mup7aczewSAYMX&t=1668077960626"
                alt="MCI" style="background: transparent;"></div>
            <div class="team-name">Man City</div>
            <div class="team-meta">2nd Place (67 pts)<br>Away</div>
          </div>
        </div>

        <div class="mot-row">
          <span class="mot-lbl">Motivation Index</span>
          <div class="mot-track">
            <div class="mot-bar" style="background: var(--bur-primary);" data-p="95" id="mot-bur2"></div>
          </div>
          <span class="mot-val" style="color: #fff;">95%</span>
          <span style="color:var(--muted); font-size:10px; margin: 0 5px;">|</span>
          <span class="mot-val" style="color: #fff;">98%</span>
          <div class="mot-track">
            <div class="mot-bar" style="background: var(--mci-primary); float: right;" data-p="98" id="mot-mci2"></div>
          </div>
        </div>
      </div>
    </div>

    <div class="grid">
      <div class="card">
        <div class="card-hd">
          <div class="hd-dot" style="background: var(--amber);"></div>
          <div class="hd-title">Context & Lineup Strength</div>
        </div>
        <div class="card-body">
          <div class="ctx" style="margin-bottom: 12px;">
            An extreme mismatch in stakes. Manchester City are chasing the title in a tight race; goal difference is
            paramount. Burnley are staring down relegation with the <strong>worst defensive record in the
              division</strong>. City's sheer quality makes this a hostile environment for the desperate hosts.
          </div>
          <div
            style="font-size: 11px; color: var(--muted); text-transform: uppercase; letter-spacing: 1px; margin-bottom: 6px;">
            Injuries / Suspensions</div>
          <ul style="font-size: 12px; color: var(--label); padding-left: 15px; line-height: 1.6; margin-bottom: 15px;">
            <li><strong style="color:#fff;">BUR:</strong> Depleted defensive line. Awaiting late fitness test on Jordan
              Beyer.</li>
            <li><strong style="color:#fff;">MCI:</strong> Fully fit squad rotation expected. Erling Haaland expected to
              start.</li>
          </ul>

          <div class="inline-note"
            style="border-color: rgba(108, 171, 221, 0.4); border-left: 3px solid var(--mci-primary);">
            <strong>Referee Profile: Michael Oliver</strong><br>
            Averages 20.1 fouls and 3.8 yellows per match. Oliver has a lower foul threshold but balances card
            distribution evenly. Expect a free-flowing game benefiting City's possession, keeping total match fouls on
            the lower side.
          </div>
        </div>
      </div>

      <div class="card">
        <div class="card-hd">
          <div class="hd-dot" style="background: var(--purple);"></div>
          <div class="hd-title">Prop Variance Model (Match Totals)</div>
        </div>
        <div class="card-body">
          <div class="xg-row">
            <div class="xg-item">
              <div class="xg-v">0.82</div>
              <div class="xg-l">BUR xG / 90</div>
            </div>
            <div class="xg-item">
              <div class="xg-v">2.45</div>
              <div class="xg-l">MCI xG / 90</div>
            </div>
          </div>
          <table class="pred-table">
            <thead>
              <tr>
                <th>Match Metric</th>
                <th style="text-align:center;">Low Var.</th>
                <th style="text-align:center; color: var(--amber);">Expected</th>
                <th style="text-align:center;">High Var.</th>
              </tr>
            </thead>
            <tbody>
              <tr>
                <td>Tackles Attempted</td>
                <td class="tv val-low">28</td>
                <td class="tv val-exp">36</td>
                <td class="tv val-high">44</td>
              </tr>
              <tr>
                <td>Corners</td>
                <td class="tv val-low">6</td>
                <td class="tv val-exp">9.5</td>
                <td class="tv val-high">13</td>
              </tr>
              <tr>
                <td>Total Shots</td>
                <td class="tv val-low">16</td>
                <td class="tv val-exp">23</td>
                <td class="tv val-high">29</td>
              </tr>
              <tr>
                <td>Shots on Target</td>
                <td class="tv val-low">5</td>
                <td class="tv val-exp">9</td>
                <td class="tv val-high">14</td>
              </tr>
              <tr>
                <td>Fouls Committed</td>
                <td class="tv val-low">14</td>
                <td class="tv val-exp">19</td>
                <td class="tv val-high">24</td>
              </tr>
              <tr>
                <td>Throw-ins</td>
                <td class="tv val-low">24</td>
                <td class="tv val-exp">31</td>
                <td class="tv val-high">38</td>
              </tr>
              <tr>
                <td>Goal Kicks</td>
                <td class="tv val-low">9</td>
                <td class="tv val-exp">13</td>
                <td class="tv val-high">18</td>
              </tr>
            </tbody>
          </table>
          <div style="font-size: 10px; color: var(--muted); text-align: right; margin-top: 8px;">*Data mapped via <a href="https://github.com/polehead">💀</a></div>
        </div>
      </div>

      <div class="card span2">
        <div class="card-hd">
          <div class="hd-dot" style="background: var(--green);"></div>
          <div class="hd-title">Algorithmic Score Modeling & Betting Angles</div>
        </div>
        <div class="card-body">
          <div class="score-zone">
            <div class="sz-head">Expected Result Variance</div>
            <div class="s-boxes">
              <div class="sbox">
                <div class="sb-lbl">Low Variance</div>
                <div class="sb-score">0 - 1</div>
                <div class="sb-prob">BUR Low Block Holds</div>
              </div>
              <div class="sbox feat"
                style="border-color: rgba(108, 171, 221, 0.4); background: linear-gradient(135deg, rgba(108, 171, 221, .07), var(--bg3));">
                <div class="sb-lbl" style="color: var(--mci-primary);">Median Expectation</div>
                <div class="sb-score feat-s" style="color: var(--mci-primary);">0 - 2</div>
                <div class="sb-prob">City Control Tempo</div>
              </div>
              <div class="sbox">
                <div class="sb-lbl">High Variance</div>
                <div class="sb-score">1 - 5</div>
                <div class="sb-prob">Haaland Exploitation</div>
              </div>
            </div>
            <div class="safe-box">
              <strong>Safe Prediction: BUR 0 - 3 MCI</strong><br>
              City's relentless attack forces immense pressure. We project Burnley to account for the majority of the
              <strong>Expected 13 Goal Kicks</strong> due to City's high volume of shots missing the target or being
              deflected out.
            </div>
          </div>

          <div style="display: grid; grid-template-columns: 1fr 1fr; gap: 16px; margin-top: 16px;">
            <div>
              <div
                style="font-size: 11px; color: var(--muted); text-transform: uppercase; letter-spacing: 1px; margin-bottom: 8px;">
                Card Market Targets (Ref Impacted)</div>
              <div class="yc-list">
                <div class="yc-row">
                  <div class="yc-info">
                    <div class="yc-name">Josh Cullen <span class="yc-club">BUR</span></div>
                    <div class="yc-reason">High defensive midfield volume vs Doku/Foden. Will reach high tackle counts.
                    </div>
                  </div>
                </div>
                <div class="yc-row">
                  <div class="yc-info">
                    <div class="yc-name">Maxime Esteve <span class="yc-club">BUR</span></div>
                    <div class="yc-reason">Will be isolated and forced into desperate challenges. Oliver won't hesitate
                      to card lunging tackles.</div>
                  </div>
                </div>
              </div>
            </div>
            <div>
              <div
                style="font-size: 11px; color: var(--muted); text-transform: uppercase; letter-spacing: 1px; margin-bottom: 8px;">
                Betting Patterns & Value</div>
              <div class="bet-grid" style="grid-template-columns: 1fr;">
                <div class="bet-cell bval">
                  <div class="bc-mkt">Asian Handicap</div>
                  <div class="bc-line" style="color: var(--amber);">MCI -2.5</div>
                  <div class="bc-rsn">Priced at 11/8. Heavy market action on goal diff.</div>
                </div>
                <div class="bet-cell">
                  <div class="bc-mkt">Prop Builder Value</div>
                  <div class="bc-line">BUR Over 8.5 Goal Kicks</div>
                  <div class="bc-rsn">Priced at 1/1. Relies on City's sheer shot volume.</div>
                </div>
              </div>
            </div>
          </div>

        </div>
      </div>
    </div>

  </div>

  <footer
    style="text-align:center;padding:20px 16px;font-size:10px;color:var(--muted);border-top:1px solid var(--border);position:relative;z-index:1">
    <p><strong>Professional Strategy Analytics</strong><br /></p>
    <p style="margin-top: 4px;">
      Statistical predictions are weighted estimates based on historical data and form analysis.<br />
      <strong style="color: var(--red); text-decoration: underline;">ALWAYS GAMBLE RESPONSIBLY, THIS IS NOT FINANCIAL
        ADVICE</strong>
    </p>
  </footer>

  <script>
    (function () {
      'use strict';
      setTimeout(() => {
        const bou = document.getElementById('mot-bou1');
        const lee = document.getElementById('mot-lee1');
        const bur = document.getElementById('mot-bur2');
        const mci = document.getElementById('mot-mci2');
        if (bou) { bou.style.transition = 'width 1.1s ease'; bou.style.width = bou.getAttribute('data-p') + '%'; }
        if (lee) { setTimeout(() => { lee.style.transition = 'width 1.1s ease'; lee.style.width = lee.getAttribute('data-p') + '%'; }, 150); }
        if (bur) { setTimeout(() => { bur.style.transition = 'width 1.1s ease'; bur.style.width = bur.getAttribute('data-p') + '%'; }, 300); }
        if (mci) { setTimeout(() => { mci.style.transition = 'width 1.1s ease'; mci.style.width = mci.getAttribute('data-p') + '%'; }, 450); }
      }, 400);

      document.querySelectorAll('.badge-ring').forEach((b, i) => {
        b.style.animationDelay = (0.19 + i * 0.1) + 's';
      });
    })();
  </script>
</body>

</html>
