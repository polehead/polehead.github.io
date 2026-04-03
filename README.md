<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>EFL Championship Matchday Analysis — 3 April 2026</title>
<link href="https://fonts.googleapis.com/css2?family=Barlow+Condensed:wght@400;600;700;800&family=Barlow:wght@300;400;500;600&family=Space+Mono:wght@400;700&display=swap" rel="stylesheet">
<style>
  :root {
    --bg: #0d1117;
    --surface: #161b22;
    --card: #1c2128;
    --border: rgba(255,255,255,0.07);
    --accent: #f0c040;
    --accent2: #58a6ff;
    --green: #3fb950;
    --red: #f85149;
    --orange: #fb8500;
    --purple: #bc8cff;
    --text: #e6edf3;
    --muted: #7d8590;
    --win: #3fb950;
    --draw: #f0c040;
    --loss: #f85149;
    /* Team colours */
    --charlton: #cc0000;
    --bristol-city: #c8102e;
    --leicester: #003090;
    --preston: #1d4f91;
    --norwich: #00a650;
    --portsmouth: #001489;
    --oxford: #ffd700;
    --hull: #f18a00;
    --qpr: #1d5ba1;
    --watford: #fbee23;
    --shef-utd: #ee2737;
    --swansea: #ffffff;
    --stoke: #e03a3e;
    --shef-wed: #3d6cbf;
    --westbrom: #122f67;
    --wrexham: #dc143c;
    --coventry: #68c6f0;
    --derby: #231f20;
  }

  *, *::before, *::after { box-sizing: border-box; margin: 0; padding: 0; }
  html { scroll-behavior: smooth; }

  body {
    background: var(--bg);
    color: var(--text);
    font-family: 'Barlow', sans-serif;
    font-size: 14px;
    line-height: 1.5;
  }

  /* NAV */
  .top-nav {
    background: var(--surface);
    border-bottom: 2px solid var(--accent);
    padding: 0 24px;
    position: sticky;
    top: 0;
    z-index: 100;
    display: flex;
    align-items: center;
    gap: 0;
    overflow-x: auto;
    scrollbar-width: none;
  }
  .top-nav::-webkit-scrollbar { display: none; }
  .nav-brand {
    font-family: 'Barlow Condensed', sans-serif;
    font-size: 16px;
    font-weight: 800;
    letter-spacing: 1px;
    color: var(--accent);
    padding: 12px 20px 12px 0;
    white-space: nowrap;
    border-right: 1px solid var(--border);
    margin-right: 8px;
  }
  .nav-link {
    font-family: 'Space Mono', monospace;
    font-size: 9px;
    letter-spacing: 1px;
    color: var(--muted);
    padding: 12px 10px;
    text-decoration: none;
    white-space: nowrap;
    transition: color 0.2s;
    border-bottom: 2px solid transparent;
  }
  .nav-link:hover { color: var(--text); border-bottom-color: var(--accent); }

  /* HERO */
  .hero {
    background: linear-gradient(180deg, #0d1117 0%, #1a1f2e 100%);
    border-bottom: 1px solid var(--border);
    padding: 40px 24px 32px;
    text-align: center;
    position: relative;
    overflow: hidden;
  }
  .hero::before {
    content: 'EFL';
    position: absolute;
    font-family: 'Barlow Condensed', sans-serif;
    font-size: 300px;
    font-weight: 800;
    color: rgba(255,255,255,0.02);
    top: 50%; left: 50%;
    transform: translate(-50%, -50%);
    pointer-events: none;
    letter-spacing: -10px;
  }
  .hero-badge {
    display: inline-block;
    background: var(--accent);
    color: #000;
    font-family: 'Space Mono', monospace;
    font-size: 10px;
    font-weight: 700;
    letter-spacing: 2px;
    padding: 5px 14px;
    border-radius: 2px;
    margin-bottom: 16px;
    text-transform: uppercase;
  }
  .hero h1 {
    font-family: 'Barlow Condensed', sans-serif;
    font-size: clamp(36px, 6vw, 72px);
    font-weight: 800;
    letter-spacing: 2px;
    text-transform: uppercase;
    line-height: 1;
    color: #fff;
    margin-bottom: 8px;
  }
  .hero-sub {
    font-family: 'Space Mono', monospace;
    font-size: 12px;
    color: var(--muted);
    letter-spacing: 1px;
  }
  .hero-stats {
    display: flex;
    justify-content: center;
    gap: 32px;
    margin-top: 24px;
    flex-wrap: wrap;
  }
  .hero-stat { text-align: center; }
  .hero-stat-val {
    font-family: 'Barlow Condensed', sans-serif;
    font-size: 28px;
    font-weight: 700;
    color: var(--accent);
    line-height: 1;
  }
  .hero-stat-label {
    font-size: 11px;
    color: var(--muted);
    font-family: 'Space Mono', monospace;
    letter-spacing: 0.5px;
    margin-top: 2px;
  }

  /* MATCH CARD */
  .matches-wrapper {
    max-width: 1200px;
    margin: 0 auto;
    padding: 24px 16px 60px;
    display: grid;
    gap: 24px;
  }

  .match-card {
    background: var(--card);
    border: 1px solid var(--border);
    border-radius: 10px;
    overflow: hidden;
    position: relative;
  }

  .match-card-header {
    display: grid;
    grid-template-columns: 1fr auto 1fr;
    align-items: center;
    padding: 20px 24px 16px;
    gap: 12px;
    border-bottom: 1px solid var(--border);
    position: relative;
  }

  .match-card-header::before {
    content: '';
    position: absolute;
    top: 0; left: 0; right: 0;
    height: 3px;
  }

  .team-block { display: flex; flex-direction: column; gap: 4px; }
  .team-block.right { align-items: flex-end; text-align: right; }
  .team-name {
    font-family: 'Barlow Condensed', sans-serif;
    font-size: clamp(18px, 2.5vw, 26px);
    font-weight: 800;
    letter-spacing: 0.5px;
    text-transform: uppercase;
    line-height: 1;
    color: #fff;
  }
  .team-pos {
    font-family: 'Space Mono', monospace;
    font-size: 10px;
    color: var(--muted);
    letter-spacing: 0.5px;
  }
  .team-pts { font-weight: 600; }
  .team-form { display: flex; gap: 3px; margin-top: 4px; }
  .team-block.right .team-form { justify-content: flex-end; }
  .fd {
    width: 18px; height: 18px;
    border-radius: 3px;
    display: flex; align-items: center; justify-content: center;
    font-size: 9px; font-weight: 700;
    font-family: 'Space Mono', monospace;
  }
  .fw { background: rgba(63,185,80,0.25); color: var(--win); }
  .fd2 { background: rgba(240,192,64,0.25); color: var(--draw); }
  .fl { background: rgba(248,81,73,0.25); color: var(--loss); }

  .vs-center { text-align: center; }
  .vs-text {
    font-family: 'Barlow Condensed', sans-serif;
    font-size: 32px;
    font-weight: 800;
    color: rgba(255,255,255,0.1);
    line-height: 1;
  }
  .match-info {
    font-family: 'Space Mono', monospace;
    font-size: 9px;
    color: var(--muted);
    letter-spacing: 1px;
    margin-top: 2px;
    white-space: nowrap;
  }
  .match-num-badge {
    position: absolute;
    top: 0; right: 0;
    background: rgba(255,255,255,0.04);
    font-family: 'Barlow Condensed', sans-serif;
    font-size: 11px;
    font-weight: 700;
    color: var(--muted);
    letter-spacing: 1px;
    padding: 3px 8px;
    border-bottom-left-radius: 6px;
  }

  /* CARD BODY */
  .card-body {
    padding: 0;
    display: grid;
    grid-template-columns: 1fr 1fr 1fr;
    border-bottom: 1px solid var(--border);
  }
  @media(max-width: 700px) {
    .card-body { grid-template-columns: 1fr; }
  }
  .section-col {
    padding: 16px 20px;
    border-right: 1px solid var(--border);
  }
  .section-col:last-child { border-right: none; }
  .section-title {
    font-family: 'Space Mono', monospace;
    font-size: 9px;
    letter-spacing: 2px;
    color: var(--accent);
    text-transform: uppercase;
    margin-bottom: 10px;
    display: flex;
    align-items: center;
    gap: 6px;
  }
  .section-title::after {
    content: '';
    flex: 1;
    height: 1px;
    background: var(--border);
  }

  .form-entry {
    display: flex;
    justify-content: space-between;
    align-items: center;
    padding: 5px 0;
    border-bottom: 1px solid rgba(255,255,255,0.03);
    gap: 8px;
    font-size: 12px;
  }
  .form-entry:last-child { border-bottom: none; }
  .fe-opp { color: var(--text); flex: 1; white-space: nowrap; overflow: hidden; text-overflow: ellipsis; }
  .fe-comp { color: var(--muted); font-size: 10px; font-family: 'Space Mono', monospace; }
  .fe-result {
    font-family: 'Space Mono', monospace;
    font-size: 10px;
    font-weight: 700;
    padding: 2px 6px;
    border-radius: 3px;
    white-space: nowrap;
  }
  .r-w { background: rgba(63,185,80,0.2); color: var(--win); }
  .r-d { background: rgba(240,192,64,0.2); color: var(--draw); }
  .r-l { background: rgba(248,81,73,0.2); color: var(--loss); }

  .h2h-entry {
    display: flex;
    justify-content: space-between;
    padding: 5px 0;
    border-bottom: 1px solid rgba(255,255,255,0.03);
    font-size: 11px;
    align-items: center;
    gap: 6px;
  }
  .h2h-entry:last-child { border-bottom: none; }
  .h2h-date { color: var(--muted); font-family: 'Space Mono', monospace; font-size: 9px; white-space: nowrap; }
  .h2h-score {
    font-family: 'Space Mono', monospace;
    font-weight: 700;
    font-size: 12px;
    padding: 2px 8px;
    border-radius: 3px;
    background: rgba(255,255,255,0.06);
    white-space: nowrap;
  }
  .h2h-winner { font-size: 10px; color: var(--muted); flex: 1; text-align: center; }

  /* SEASON STATS */
  .stats-grid {
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: 8px;
    padding: 16px 20px;
    border-bottom: 1px solid var(--border);
  }
  .stat-compare { display: flex; flex-direction: column; gap: 3px; }
  .stat-c-label {
    font-size: 10px;
    color: var(--muted);
    font-family: 'Space Mono', monospace;
    letter-spacing: 0.5px;
  }
  .stat-c-row { display: flex; align-items: center; gap: 6px; }
  .stat-c-val {
    font-family: 'Space Mono', monospace;
    font-size: 11px;
    font-weight: 700;
    min-width: 28px;
    text-align: right;
  }
  .stat-c-bar-wrap {
    flex: 1;
    height: 4px;
    background: rgba(255,255,255,0.06);
    border-radius: 2px;
    overflow: hidden;
  }
  .stat-c-bar { height: 100%; border-radius: 2px; }
  .bar-home { background: linear-gradient(90deg, var(--accent2), rgba(88,166,255,0.5)); }
  .bar-away { background: linear-gradient(90deg, var(--orange), rgba(251,133,0,0.5)); }

  /* PREDICTION */
  .pred-box {
    padding: 16px 20px;
    background: linear-gradient(135deg, rgba(240,192,64,0.06) 0%, rgba(0,0,0,0) 100%);
  }
  .pred-scoreline-row {
    display: flex;
    align-items: center;
    justify-content: space-between;
    gap: 12px;
    margin-bottom: 16px;
  }
  .pred-team { font-family: 'Barlow Condensed', sans-serif; font-size: 15px; font-weight: 700; color: #fff; text-transform: uppercase; letter-spacing: 0.5px; flex: 1; }
  .pred-team.right { text-align: right; }
  .pred-score-badge {
    font-family: 'Barlow Condensed', sans-serif;
    font-size: 36px;
    font-weight: 800;
    color: var(--accent);
    letter-spacing: 4px;
    padding: 4px 16px;
    background: rgba(240,192,64,0.1);
    border: 1px solid rgba(240,192,64,0.3);
    border-radius: 6px;
    line-height: 1;
  }
  .pred-metrics {
    display: grid;
    grid-template-columns: repeat(3, 1fr);
    gap: 8px;
    margin-bottom: 12px;
  }
  @media(max-width: 500px) { .pred-metrics { grid-template-columns: repeat(2, 1fr); } }
  .pred-metric {
    background: rgba(0,0,0,0.3);
    border: 1px solid rgba(255,255,255,0.06);
    border-radius: 6px;
    padding: 10px 12px;
    text-align: center;
  }
  .pm-label {
    font-family: 'Space Mono', monospace;
    font-size: 8px;
    letter-spacing: 1.5px;
    color: var(--muted);
    text-transform: uppercase;
    margin-bottom: 5px;
  }
  .pm-val {
    font-family: 'Barlow Condensed', sans-serif;
    font-size: 22px;
    font-weight: 700;
    line-height: 1;
  }
  .pm-range {
    font-family: 'Space Mono', monospace;
    font-size: 9px;
    color: var(--muted);
    margin-top: 3px;
  }
  .pm-red-risk {
    display: flex;
    align-items: center;
    gap: 6px;
    margin-top: 4px;
  }
  .risk-track {
    flex: 1;
    height: 4px;
    background: rgba(255,255,255,0.06);
    border-radius: 2px;
    overflow: hidden;
  }
  .risk-fill { height: 100%; border-radius: 2px; background: linear-gradient(90deg, var(--red), rgba(248,81,73,0.5)); }
  .risk-pct { font-family: 'Space Mono', monospace; font-size: 9px; color: var(--muted); }

  .pred-analysis {
    font-size: 12px;
    color: var(--muted);
    line-height: 1.6;
    padding-top: 10px;
    border-top: 1px solid rgba(255,255,255,0.05);
  }
  .pred-analysis strong { color: var(--text); }

  .verdict-tag {
    display: inline-block;
    font-family: 'Barlow Condensed', sans-serif;
    font-size: 13px;
    font-weight: 700;
    letter-spacing: 1px;
    padding: 3px 10px;
    border-radius: 3px;
    margin-right: 6px;
    vertical-align: middle;
  }
  .vt-home { background: rgba(63,185,80,0.2); color: var(--win); border: 1px solid rgba(63,185,80,0.4); }
  .vt-away { background: rgba(248,81,73,0.2); color: var(--loss); border: 1px solid rgba(248,81,73,0.4); }
  .vt-draw { background: rgba(240,192,64,0.2); color: var(--draw); border: 1px solid rgba(240,192,64,0.4); }

  /* RELEGATION / PROMOTION BANNERS */
  .banner-tag {
    display: inline-block;
    font-size: 9px;
    font-family: 'Space Mono', monospace;
    letter-spacing: 1px;
    padding: 2px 7px;
    border-radius: 3px;
    margin-left: 6px;
    vertical-align: middle;
  }
  .bt-relegation { background: rgba(248,81,73,0.2); color: var(--red); border: 1px solid rgba(248,81,73,0.3); }
  .bt-promotion { background: rgba(63,185,80,0.2); color: var(--win); border: 1px solid rgba(63,185,80,0.3); }
  .bt-playoff { background: rgba(88,166,255,0.2); color: var(--accent2); border: 1px solid rgba(88,166,255,0.3); }
  .bt-newboy { background: rgba(188,140,255,0.2); color: var(--purple); border: 1px solid rgba(188,140,255,0.3); }

  /* SUMMARY TABLE */
  .summary-section {
    max-width: 1200px;
    margin: 0 auto 60px;
    padding: 0 16px;
  }
  .summary-title {
    font-family: 'Barlow Condensed', sans-serif;
    font-size: 28px;
    font-weight: 800;
    text-transform: uppercase;
    letter-spacing: 2px;
    color: var(--accent);
    margin-bottom: 16px;
  }
  .summary-table { width: 100%; border-collapse: collapse; font-size: 12px; overflow-x: auto; display: block; }
  .summary-table th {
    font-family: 'Space Mono', monospace;
    font-size: 9px;
    letter-spacing: 1.5px;
    color: var(--muted);
    text-transform: uppercase;
    padding: 10px 12px;
    text-align: center;
    border-bottom: 2px solid rgba(240,192,64,0.4);
    background: var(--surface);
    white-space: nowrap;
  }
  .summary-table th:first-child { text-align: left; }
  .summary-table td {
    padding: 10px 12px;
    border-bottom: 1px solid rgba(255,255,255,0.04);
    text-align: center;
    white-space: nowrap;
  }
  .summary-table td:first-child { text-align: left; font-weight: 600; }
  .summary-table tr:hover td { background: rgba(255,255,255,0.02); }
  .match-label-cell { font-family: 'Barlow Condensed', sans-serif; font-size: 14px; letter-spacing: 0.5px; }
  .pred-score-cell {
    font-family: 'Barlow Condensed', sans-serif;
    font-size: 18px;
    font-weight: 700;
    color: var(--accent);
  }

  /* FOOTER */
  .footer {
    text-align: center;
    padding: 24px;
    font-family: 'Space Mono', monospace;
    font-size: 10px;
    color: var(--muted);
    letter-spacing: 0.5px;
    border-top: 1px solid var(--border);
  }

  /* COLOUR ACCENT BARS */
  .accent-charlton::before { background: linear-gradient(90deg, var(--charlton), rgba(204,0,0,0.3)); }
  .accent-leicester::before { background: linear-gradient(90deg, var(--leicester), rgba(0,48,144,0.3)); }
  .accent-norwich::before { background: linear-gradient(90deg, var(--norwich), rgba(0,166,80,0.3)); }
  .accent-oxford::before { background: linear-gradient(90deg, #1a3c5e, rgba(26,60,94,0.3)); }
  .accent-qpr::before { background: linear-gradient(90deg, var(--qpr), rgba(29,91,161,0.3)); }
  .accent-shefutd::before { background: linear-gradient(90deg, var(--shef-utd), rgba(238,39,55,0.3)); }
  .accent-stoke::before { background: linear-gradient(90deg, var(--stoke), rgba(224,58,62,0.3)); }
  .accent-westbrom::before { background: linear-gradient(90deg, var(--westbrom), rgba(18,47,103,0.3)); }
  .accent-coventry::before { background: linear-gradient(90deg, #1a78c2, rgba(26,120,194,0.3)); }

  .section-sub {
    font-size: 11px;
    color: var(--muted);
    margin-top: 6px;
    font-style: italic;
  }

  .pm-val.goals { color: var(--accent); }
  .pm-val.corners { color: var(--accent2); }
  .pm-val.yellow { color: var(--orange); }
  .pm-val.shots { color: var(--purple); }
  .pm-val.sot { color: var(--green); }
  .pm-val.red { color: var(--red); }

  .injury-note {
    font-size: 11px;
    color: var(--muted);
    background: rgba(248,81,73,0.06);
    border: 1px solid rgba(248,81,73,0.15);
    border-radius: 4px;
    padding: 6px 10px;
    margin-top: 8px;
    line-height: 1.5;
  }
  .injury-note strong { color: var(--red); }

  /* ======================== MOBILE-FIRST RESPONSIVE ======================== */

  /* Fluid base font — scales from 15px at 320px to 16px at 1200px */
  body {
    font-size: clamp(15px, 1.4vw + 10px, 16px);
  }

  /* ---------- NAV (mobile) ---------- */
  @media (max-width: 700px) {
    .top-nav {
      padding: 0 12px;
      gap: 0;
    }
    .nav-brand {
      font-size: clamp(14px, 3.5vw, 18px);
      padding: 10px 12px 10px 0;
      margin-right: 4px;
    }
    .nav-link {
      font-size: clamp(10px, 2.5vw, 12px);
      padding: 14px 10px;
      min-height: 44px;
      display: flex;
      align-items: center;
    }
  }

  /* ---------- HERO (mobile) ---------- */
  @media (max-width: 700px) {
    .hero {
      padding: 28px 16px 24px;
    }
    .hero-badge {
      font-size: clamp(9px, 2.5vw, 11px);
      padding: 5px 12px;
    }
    .hero-sub {
      font-size: clamp(11px, 2.8vw, 13px);
    }
    .hero-stats {
      gap: 16px 24px;
    }
    .hero-stat-val {
      font-size: clamp(24px, 6vw, 32px);
    }
    .hero-stat-label {
      font-size: clamp(10px, 2.5vw, 12px);
    }
  }

  /* ---------- MATCH CARD HEADER (mobile) ---------- */
  @media (max-width: 600px) {
    .match-card-header {
      grid-template-columns: 1fr;
      grid-template-rows: auto auto auto;
      text-align: center;
      padding: 16px 14px 14px;
      gap: 10px;
    }
    .team-block,
    .team-block.right {
      align-items: center;
      text-align: center;
    }
    .team-block.right .team-form,
    .team-form {
      justify-content: center;
    }
    .team-name {
      font-size: clamp(20px, 5vw, 28px);
    }
    .team-pos {
      font-size: clamp(11px, 2.8vw, 13px);
    }
    .fd {
      width: 22px;
      height: 22px;
      font-size: clamp(10px, 2.5vw, 11px);
    }
    .vs-text {
      font-size: 24px;
    }
    .match-info {
      font-size: clamp(10px, 2.8vw, 12px);
    }
    .match-num-badge {
      font-size: clamp(10px, 2.5vw, 12px);
      padding: 4px 10px;
    }
    .banner-tag {
      font-size: clamp(8px, 2vw, 10px);
      padding: 2px 6px;
      display: block;
      margin: 4px auto 0;
      width: fit-content;
    }
  }

  /* ---------- CARD BODY — FORM, H2H, SECTIONS (mobile) ---------- */
  @media (max-width: 700px) {
    .section-col {
      padding: 14px 16px;
      border-right: none;
      border-bottom: 1px solid var(--border);
    }
    .section-col:last-child {
      border-bottom: none;
    }
    .section-title {
      font-size: clamp(10px, 2.8vw, 12px);
      letter-spacing: 1.5px;
      margin-bottom: 10px;
    }
    .form-entry {
      font-size: clamp(13px, 3.5vw, 15px);
      padding: 7px 0;
    }
    .fe-comp {
      font-size: clamp(10px, 2.5vw, 12px);
    }
    .fe-result {
      font-size: clamp(11px, 2.8vw, 13px);
      padding: 3px 8px;
    }
    .section-sub {
      font-size: clamp(12px, 3vw, 14px);
      line-height: 1.5;
      margin-top: 8px;
    }
    .h2h-entry {
      font-size: clamp(12px, 3vw, 14px);
      padding: 7px 0;
      flex-wrap: wrap;
      gap: 4px 8px;
    }
    .h2h-date {
      font-size: clamp(10px, 2.5vw, 12px);
    }
    .h2h-score {
      font-size: clamp(13px, 3.2vw, 15px);
      padding: 3px 10px;
    }
    .h2h-winner {
      font-size: clamp(11px, 2.8vw, 13px);
    }
    .injury-note {
      font-size: clamp(12px, 3vw, 14px);
      padding: 8px 12px;
      line-height: 1.6;
    }
  }

  /* ---------- STATS GRID (mobile) ---------- */
  @media (max-width: 700px) {
    .stats-grid {
      grid-template-columns: 1fr;
      gap: 12px;
      padding: 16px;
    }
    .stat-c-label {
      font-size: clamp(11px, 2.8vw, 13px);
      margin-bottom: 4px;
    }
    .stat-c-val {
      font-size: clamp(12px, 3vw, 14px);
      min-width: 34px;
    }
    .stat-c-bar-wrap {
      height: 6px;
    }
    .stat-c-row span[style*="font-size:9px"],
    .stat-c-row span[style*="font-family:'Space Mono'"] {
      font-size: clamp(10px, 2.5vw, 12px) !important;
    }
  }

  /* ---------- PREDICTION BOX (mobile) ---------- */
  @media (max-width: 600px) {
    .pred-box {
      padding: 16px 14px;
    }
    .pred-scoreline-row {
      flex-direction: column;
      align-items: center;
      gap: 8px;
      margin-bottom: 14px;
    }
    .pred-team,
    .pred-team.right {
      text-align: center;
      font-size: clamp(14px, 3.8vw, 18px);
    }
    .pred-score-badge {
      font-size: clamp(30px, 8vw, 40px);
      padding: 6px 20px;
    }
    .pred-metrics {
      grid-template-columns: repeat(2, 1fr);
      gap: 10px;
    }
    .pm-label {
      font-size: clamp(9px, 2.4vw, 11px);
    }
    .pm-val {
      font-size: clamp(20px, 5vw, 26px);
    }
    .pm-range {
      font-size: clamp(10px, 2.5vw, 12px);
    }
    .risk-pct {
      font-size: clamp(10px, 2.5vw, 12px);
    }
    .risk-track {
      height: 5px;
    }
    .pred-analysis {
      font-size: clamp(13px, 3.2vw, 15px);
      line-height: 1.7;
    }
    .verdict-tag {
      font-size: clamp(11px, 2.8vw, 14px);
      padding: 3px 8px;
      display: block;
      margin: 4px auto 0;
      width: fit-content;
    }
  }

  /* ---------- SUMMARY SECTION (mobile) ---------- */
  @media (max-width: 700px) {
    .summary-section {
      padding: 0 10px;
    }
    .summary-title {
      font-size: clamp(22px, 5vw, 30px);
    }
    .summary-table {
      font-size: clamp(12px, 3vw, 14px);
    }
    .summary-table th {
      font-size: clamp(8px, 2.2vw, 10px);
      padding: 8px 6px;
    }
    .summary-table td {
      padding: 8px 6px;
    }
    .match-label-cell {
      font-size: clamp(12px, 3vw, 14px) !important;
    }
    .pred-score-cell {
      font-size: clamp(16px, 4vw, 20px) !important;
    }
  }

  /* ---------- KEY STORYLINES BOX (mobile) ---------- */
  @media (max-width: 700px) {
    .summary-section > div[style*="margin-top:16px"] {
      font-size: clamp(13px, 3.2vw, 15px) !important;
      line-height: 1.8 !important;
      padding: 12px 14px !important;
    }
  }

  /* ---------- FOOTER (mobile) ---------- */
  @media (max-width: 700px) {
    .footer {
      font-size: clamp(11px, 2.8vw, 13px);
      padding: 20px 16px;
      line-height: 1.6;
    }
  }

  /* ---------- ULTRA-SMALL SCREENS (≤380px) ---------- */
  @media (max-width: 380px) {
    .pred-metrics {
      grid-template-columns: 1fr;
    }
    .hero-stats {
      flex-direction: column;
      gap: 12px;
    }
    .team-name {
      font-size: 18px;
    }
  }
</style>
</head>
<body>

<!-- NAV -->
<div class="top-nav">
  <div class="nav-brand">⚽ CHAMP. ANALYSIS</div>
  <a class="nav-link" href="#m1">Charlton v Bristol</a>
  <a class="nav-link" href="#m2">Leicester v Preston</a>
  <a class="nav-link" href="#m3">Norwich v Portsmouth</a>
  <a class="nav-link" href="#m4">Oxford v Hull</a>
  <a class="nav-link" href="#m5">QPR v Watford</a>
  <a class="nav-link" href="#m6">Sheff Utd v Swansea</a>
  <a class="nav-link" href="#m7">Stoke v Sheff Wed</a>
  <a class="nav-link" href="#m8">West Brom v Wrexham</a>
  <a class="nav-link" href="#m9">Coventry v Derby</a>
  <a class="nav-link" href="#summary">Summary</a>
</div>

<!-- HERO -->
<div class="hero">
  <div class="hero-badge">GOOD FRIDAY · 3 APRIL 2026 · MATCHDAY 40</div>
  <h1>EFL Championship<br>Match Analysis</h1>
  <p class="hero-sub">9 FIXTURES · PREDICTIONS · STATS · HEAD TO HEAD</p>
  <div class="hero-stats">
    <div class="hero-stat">
      <div class="hero-stat-val">2.59</div>
      <div class="hero-stat-label">Avg Goals/Game</div>
    </div>
    <div class="hero-stat">
      <div class="hero-stat-val">9</div>
      <div class="hero-stat-label">Fixtures Today</div>
    </div>
    <div class="hero-stat">
      <div class="hero-stat-val">7</div>
      <div class="hero-stat-label">Games Remaining</div>
    </div>
    <div class="hero-stat">
      <div class="hero-stat-val">417</div>
      <div class="hero-stat-label">Matches Played</div>
    </div>
    <div class="hero-stat">
      <div class="hero-stat-val">80pts</div>
      <div class="hero-stat-label">Coventry Lead</div>
    </div>
    <div class="hero-stat">
      <div class="hero-stat-val">-18</div>
      <div class="hero-stat-label">Sheff Wed Deduction</div>
    </div>
  </div>
</div>

<div class="matches-wrapper">

<!-- ===================== MATCH 1: CHARLTON v BRISTOL CITY ===================== -->
<div class="match-card accent-charlton" id="m1">
  <div class="match-card-header">
    <div class="match-num-badge">MATCH 1</div>
    <div class="team-block">
      <div class="team-name">Charlton Athletic</div>
      <div class="team-pos">18th · 48pts · <span style="color:var(--red)">GD −10</span></div>
      <div class="team-form">
        <div class="fd fw">W</div><div class="fd fw">W</div><div class="fd fd2">D</div><div class="fd fl">L</div><div class="fd fl">L</div>
      </div>
    </div>
    <div class="vs-center">
      <div class="vs-text">VS</div>
      <div class="match-info">THE VALLEY · 15:00</div>
    </div>
    <div class="team-block right">
      <div class="team-name">Bristol City</div>
      <div class="team-pos">16th · 51pts · GD −1</div>
      <div class="team-form">
        <div class="fd fl">L</div><div class="fd fl">L</div><div class="fd fl">L</div><div class="fd fl">L</div><div class="fd fw">W</div>
      </div>
    </div>
  </div>

  <div class="card-body">
    <div class="section-col">
      <div class="section-title">Charlton — Last 10</div>
      <div class="form-entry"><span class="fe-opp">vs Birmingham (A)</span><span class="fe-comp">Ch</span><span class="fe-result r-w">1-0 W</span></div>
      <div class="form-entry"><span class="fe-opp">vs Middlesbrough (H)</span><span class="fe-comp">Ch</span><span class="fe-result r-w">1-0 W</span></div>
      <div class="form-entry"><span class="fe-opp">vs Derby County (H)</span><span class="fe-comp">Ch</span><span class="fe-result fd2">1-1 D</span></div>
      <div class="form-entry"><span class="fe-opp">vs Stoke City (A)</span><span class="fe-comp">Ch</span><span class="fe-result fd2">0-0 D</span></div>
      <div class="form-entry"><span class="fe-opp">vs Leicester City (A)</span><span class="fe-comp">Ch</span><span class="fe-result fd2">1-1 D</span></div>
      <div class="form-entry"><span class="fe-opp">vs Oxford United (H)</span><span class="fe-comp">Ch</span><span class="fe-result r-l">0-1 L</span></div>
      <div class="form-entry"><span class="fe-opp">vs Wrexham (A)</span><span class="fe-comp">Ch</span><span class="fe-result r-l">0-1 L</span></div>
      <div class="form-entry"><span class="fe-opp">vs Watford (H)</span><span class="fe-comp">Ch</span><span class="fe-result fd2">1-1 D</span></div>
      <div class="form-entry"><span class="fe-opp">vs Portsmouth (A)</span><span class="fe-comp">Ch</span><span class="fe-result r-w">2-1 W</span></div>
      <div class="form-entry"><span class="fe-opp">vs Norwich City (H)</span><span class="fe-comp">Ch</span><span class="fe-result r-l">0-1 L</span></div>
      <div class="section-sub">Under 2.5 goals in last 7 games. 13 clean sheets all season. 36 goals from 39 games.</div>
    </div>
    <div class="section-col">
      <div class="section-title">Bristol City — Last 10</div>
      <div class="form-entry"><span class="fe-opp">vs Swansea City (H)</span><span class="fe-comp">Ch</span><span class="fe-result r-w">2-1 W</span></div>
      <div class="form-entry"><span class="fe-opp">vs Hull City (A)</span><span class="fe-comp">Ch</span><span class="fe-result r-l">1-3 L</span></div>
      <div class="form-entry"><span class="fe-opp">vs Wrexham (A)</span><span class="fe-comp">Ch</span><span class="fe-result fd2">2-2 D</span></div>
      <div class="form-entry"><span class="fe-opp">vs Derby County (A) ★</span><span class="fe-comp">Ch</span><span class="fe-result r-l">0-5 L</span></div>
      <div class="form-entry"><span class="fe-opp">vs Norwich City (H)</span><span class="fe-comp">Ch</span><span class="fe-result r-l">0-1 L</span></div>
      <div class="form-entry"><span class="fe-opp">vs QPR (A)</span><span class="fe-comp">Ch</span><span class="fe-result r-l">1-2 L</span></div>
      <div class="form-entry"><span class="fe-opp">vs Ipswich Town (H)</span><span class="fe-comp">Ch</span><span class="fe-result r-l">0-2 L</span></div>
      <div class="form-entry"><span class="fe-opp">vs Watford (A)</span><span class="fe-comp">Ch</span><span class="fe-result r-l">1-2 L</span></div>
      <div class="form-entry"><span class="fe-opp">vs Southampton (A)</span><span class="fe-comp">Ch</span><span class="fe-result r-w">2-1 W</span></div>
      <div class="form-entry"><span class="fe-opp">vs West Brom (H)</span><span class="fe-comp">Ch</span><span class="fe-result r-l">0-1 L</span></div>
      <div class="section-sub">Struber sacked. Roy Hodgson (78) caretaker. 5 wins in 8 (play-off push collapsed). 486 shots, 155 on target.</div>
    </div>
    <div class="section-col">
      <div class="section-title">H2H — Last 5</div>
      <div class="h2h-entry"><span class="h2h-date">Jan 2026</span><span style="font-size:11px;">Charlton</span><span class="h2h-score">0–0</span><span>Bristol City</span></div>
      <div class="h2h-entry"><span class="h2h-date">Sep 2025</span><span style="font-size:11px;">Bristol City</span><span class="h2h-score">2–1</span><span>Charlton</span></div>
      <div class="h2h-entry"><span class="h2h-date">2023/24</span><span style="font-size:11px;">Charlton</span><span class="h2h-score">1–2</span><span>Bristol City</span></div>
      <div class="h2h-entry"><span class="h2h-date">2023/24</span><span style="font-size:11px;">Bristol City</span><span class="h2h-score">3–0</span><span>Charlton</span></div>
      <div class="h2h-entry"><span class="h2h-date">2022/23</span><span style="font-size:11px;">Charlton</span><span class="h2h-score">0–0</span><span>Bristol City</span></div>
      <div class="section-sub" style="margin-top:8px;">Bristol City won 7 of last 19 overall. Last league meet: 0-0 draw. Low-scoring head-to-heads.</div>
      <div class="injury-note"><strong>Injuries:</strong> Charlton — Reece Burke (muscle), Matt Godden (knee), Harvey Knibbs (ankle), Josh Edwards (ankle). Bristol City — under new caretaker Roy Hodgson. Five losses in last six.</div>
    </div>
  </div>

  <div class="stats-grid">
    <div class="stat-compare">
      <div class="stat-c-label">Goals Scored/Game</div>
      <div class="stat-c-row">
        <span class="stat-c-val" style="color:var(--accent2)">0.92</span>
        <div class="stat-c-bar-wrap"><div class="stat-c-bar bar-home" style="width:45%"></div></div>
        <span style="font-size:9px;color:var(--muted);font-family:'Space Mono'">HOME</span>
      </div>
      <div class="stat-c-row">
        <span class="stat-c-val" style="color:var(--orange)">1.26</span>
        <div class="stat-c-bar-wrap"><div class="stat-c-bar bar-away" style="width:63%"></div></div>
        <span style="font-size:9px;color:var(--muted);font-family:'Space Mono'">AWAY</span>
      </div>
    </div>
    <div class="stat-compare">
      <div class="stat-c-label">Shots on Target/Game</div>
      <div class="stat-c-row">
        <span class="stat-c-val" style="color:var(--accent2)">3.2</span>
        <div class="stat-c-bar-wrap"><div class="stat-c-bar bar-home" style="width:50%"></div></div>
        <span style="font-size:9px;color:var(--muted);font-family:'Space Mono'">CHARLTON</span>
      </div>
      <div class="stat-c-row">
        <span class="stat-c-val" style="color:var(--orange)">3.9</span>
        <div class="stat-c-bar-wrap"><div class="stat-c-bar bar-away" style="width:60%"></div></div>
        <span style="font-size:9px;color:var(--muted);font-family:'Space Mono'">BRISTOL</span>
      </div>
    </div>
    <div class="stat-compare">
      <div class="stat-c-label">Total Shots/Game</div>
      <div class="stat-c-row">
        <span class="stat-c-val" style="color:var(--accent2)">~12</span>
        <div class="stat-c-bar-wrap"><div class="stat-c-bar bar-home" style="width:55%"></div></div>
        <span style="font-size:9px;color:var(--muted);font-family:'Space Mono'">CHARLTON</span>
      </div>
      <div class="stat-c-row">
        <span class="stat-c-val" style="color:var(--orange)">12.5</span>
        <div class="stat-c-bar-wrap"><div class="stat-c-bar bar-away" style="width:57%"></div></div>
        <span style="font-size:9px;color:var(--muted);font-family:'Space Mono'">BRISTOL</span>
      </div>
    </div>
    <div class="stat-compare">
      <div class="stat-c-label">Yellow Cards/Game</div>
      <div class="stat-c-row">
        <span class="stat-c-val" style="color:var(--orange)">2.2</span>
        <div class="stat-c-bar-wrap"><div class="stat-c-bar bar-home" style="width:70%"></div></div>
        <span style="font-size:9px;color:var(--muted);font-family:'Space Mono'">CHARLTON (85 total)</span>
      </div>
      <div class="stat-c-row">
        <span class="stat-c-val" style="color:var(--orange)">1.7</span>
        <div class="stat-c-bar-wrap"><div class="stat-c-bar bar-away" style="width:55%"></div></div>
        <span style="font-size:9px;color:var(--muted);font-family:'Space Mono'">BRISTOL</span>
      </div>
    </div>
  </div>

  <div class="pred-box">
    <div class="section-title">📊 Prediction</div>
    <div class="pred-scoreline-row">
      <div class="pred-team">Charlton <span class="verdict-tag vt-home">HOME WIN</span></div>
      <div class="pred-score-badge">1 – 0</div>
      <div class="pred-team right">Bristol City</div>
    </div>
    <div class="pred-metrics">
      <div class="pred-metric">
        <div class="pm-label">Goals</div>
        <div class="pm-val goals">1–2</div>
        <div class="pm-range">Likely &lt;2.5</div>
      </div>
      <div class="pred-metric">
        <div class="pm-label">Corners</div>
        <div class="pm-val corners">8–11</div>
        <div class="pm-range">Range</div>
      </div>
      <div class="pred-metric">
        <div class="pm-label">Yellow Cards</div>
        <div class="pm-val yellow">3–5</div>
        <div class="pm-range">Charlton physical</div>
      </div>
      <div class="pred-metric">
        <div class="pm-label">Shots on Target</div>
        <div class="pm-val sot">5–9</div>
        <div class="pm-range">Low output</div>
      </div>
      <div class="pred-metric">
        <div class="pm-label">Total Shots</div>
        <div class="pm-val shots">18–25</div>
        <div class="pm-range">Both limited</div>
      </div>
      <div class="pred-metric">
        <div class="pm-label">Red Card Risk</div>
        <div class="pm-val red">LOW</div>
        <div class="pm-range pm-red-risk"><div class="risk-track"><div class="risk-fill" style="width:12%"></div></div><span class="risk-pct">~12%</span></div>
      </div>
    </div>
    <div class="pred-analysis"><strong>Analysis:</strong> This looks a classic mid-table Championship scrape. <strong>Under 2.5 goals in Charlton's last 7 and Bristol City's last 4</strong> points to a tight match. Charlton have home advantage and 13 clean sheets this season but struggle to score (36 in 39). Bristol City's play-off charge has completely collapsed — 5 losses in 6 under Struber before he was sacked. Roy Hodgson's caretaker debut is unlikely to produce a dramatic transformation overnight. A narrow Charlton home win fits the pattern, with set-pieces likely decisive (Miles Leaburn key).</div>
  </div>
</div>

<!-- ===================== MATCH 2: LEICESTER v PRESTON ===================== -->
<div class="match-card accent-leicester" id="m2">
  <div class="match-card-header">
    <div class="match-num-badge">MATCH 2</div>
    <div class="team-block">
      <div class="team-name">Leicester City <span class="banner-tag bt-relegation">RELEGATION ZONE</span></div>
      <div class="team-pos">22nd · 39pts · <span style="color:var(--red)">GD −8</span> · −6pt deduction</div>
      <div class="team-form">
        <div class="fd fd2">D</div><div class="fd fl">L</div><div class="fd fw">W</div><div class="fd fd2">D</div><div class="fd fl">L</div>
      </div>
    </div>
    <div class="vs-center">
      <div class="vs-text">VS</div>
      <div class="match-info">KING POWER · 15:00</div>
    </div>
    <div class="team-block right">
      <div class="team-name">Preston North End</div>
      <div class="team-pos">13th · 52pts · GD −4</div>
      <div class="team-form">
        <div class="fd fw">W</div><div class="fd fl">L</div><div class="fd fl">L</div><div class="fd fl">L</div><div class="fd fl">L</div>
      </div>
    </div>
  </div>

  <div class="card-body">
    <div class="section-col">
      <div class="section-title">Leicester — Last 10</div>
      <div class="form-entry"><span class="fe-opp">vs Bristol City (A)</span><span class="fe-comp">Ch</span><span class="fe-result r-w">2-0 W</span></div>
      <div class="form-entry"><span class="fe-opp">vs QPR (H)</span><span class="fe-comp">Ch</span><span class="fe-result r-l">1-3 L</span></div>
      <div class="form-entry"><span class="fe-opp">vs West Brom (A)</span><span class="fe-comp">Ch</span><span class="fe-result fd2">1-1 D</span></div>
      <div class="form-entry"><span class="fe-opp">vs Charlton (H)</span><span class="fe-comp">Ch</span><span class="fe-result fd2">1-1 D</span></div>
      <div class="form-entry"><span class="fe-opp">vs Southampton (A)</span><span class="fe-comp">Ch</span><span class="fe-result r-l">0-2 L</span></div>
      <div class="form-entry"><span class="fe-opp">vs Coventry City (H)</span><span class="fe-comp">Ch</span><span class="fe-result r-l">0-2 L</span></div>
      <div class="form-entry"><span class="fe-opp">vs Millwall (A)</span><span class="fe-comp">Ch</span><span class="fe-result fd2">1-1 D</span></div>
      <div class="form-entry"><span class="fe-opp">vs Blackburn (H)</span><span class="fe-comp">Ch</span><span class="fe-result r-w">2-1 W</span></div>
      <div class="form-entry"><span class="fe-opp">vs Hull City (A)</span><span class="fe-comp">Ch</span><span class="fe-result r-l">0-1 L</span></div>
      <div class="form-entry"><span class="fe-opp">vs Watford (A)</span><span class="fe-comp">Ch</span><span class="fe-result fd2">0-0 D</span></div>
      <div class="section-sub">1 win in last 13. Conceded in 15 of last 16 home games. Over 8.5 corners in last 10 games.</div>
    </div>
    <div class="section-col">
      <div class="section-title">Preston — Last 10</div>
      <div class="form-entry"><span class="fe-opp">vs Norwich City (A)</span><span class="fe-comp">Ch</span><span class="fe-result r-l">0-2 L</span></div>
      <div class="form-entry"><span class="fe-opp">vs Swansea (H)</span><span class="fe-comp">Ch</span><span class="fe-result r-l">0-2 L</span></div>
      <div class="form-entry"><span class="fe-opp">vs Birmingham (A)</span><span class="fe-comp">Ch</span><span class="fe-result r-l">0-1 L</span></div>
      <div class="form-entry"><span class="fe-opp">vs Coventry (H)</span><span class="fe-comp">Ch</span><span class="fe-result r-l">0-3 L</span></div>
      <div class="form-entry"><span class="fe-opp">vs Oxford (A)</span><span class="fe-comp">Ch</span><span class="fe-result r-l">1-2 L</span></div>
      <div class="form-entry"><span class="fe-opp">vs Derby (H)</span><span class="fe-comp">Ch</span><span class="fe-result fd2">1-1 D</span></div>
      <div class="form-entry"><span class="fe-opp">vs QPR (A)</span><span class="fe-comp">Ch</span><span class="fe-result r-l">1-2 L</span></div>
      <div class="form-entry"><span class="fe-opp">vs Charlton (H)</span><span class="fe-comp">Ch</span><span class="fe-result r-w">2-0 W</span></div>
      <div class="form-entry"><span class="fe-opp">vs Middlesbrough (A)</span><span class="fe-comp">Ch</span><span class="fe-result r-l">0-1 L</span></div>
      <div class="form-entry"><span class="fe-opp">vs Stoke City (H)</span><span class="fe-comp">Ch</span><span class="fe-result r-w">3-1 W</span></div>
      <div class="section-sub">Won 1 of last 8. But beat Stoke 3-1 last time. Mid-table comfort, nothing to play for. 45 goals, 49 conceded.</div>
    </div>
    <div class="section-col">
      <div class="section-title">H2H — Last 5</div>
      <div class="h2h-entry"><span class="h2h-date">Aug 2025</span><span>Preston</span><span class="h2h-score" style="color:var(--red)">2–1</span><span>Leicester</span></div>
      <div class="h2h-entry"><span class="h2h-date">Apr 2024</span><span>Leicester</span><span class="h2h-score" style="color:var(--win)">2–0</span><span>Preston</span></div>
      <div class="h2h-entry"><span class="h2h-date">Dec 2023</span><span>Preston</span><span class="h2h-score" style="color:var(--draw)">1–1</span><span>Leicester</span></div>
      <div class="h2h-entry"><span class="h2h-date">Nov 2022</span><span>Leicester</span><span class="h2h-score" style="color:var(--win)">4–0</span><span>Preston</span></div>
      <div class="h2h-entry"><span class="h2h-date">Apr 2022</span><span>Preston</span><span class="h2h-score" style="color:var(--draw)">1–1</span><span>Leicester</span></div>
      <div class="section-sub">Preston lead all-time (32–17 in 66 meetings). Leicester won 4 of last 6 H2H in Championship. Goalscoring in recent H2Hs.</div>
      <div class="injury-note"><strong>Injuries:</strong> Leicester — Vestergaard, Begovic, Ramsey (doubt), Souttar, Kristiansen all out. Jordan James (Wales injury) doubt. Preston — Jamal Lewis, Lewis Gibson, Callum Lang, Alistair McCann out.</div>
    </div>
  </div>

  <div class="stats-grid">
    <div class="stat-compare">
      <div class="stat-c-label">Goals Scored/Game</div>
      <div class="stat-c-row"><span class="stat-c-val" style="color:var(--accent2)">1.31</span><div class="stat-c-bar-wrap"><div class="stat-c-bar bar-home" style="width:60%"></div></div><span style="font-size:9px;color:var(--muted);font-family:'Space Mono'">LEIC</span></div>
      <div class="stat-c-row"><span class="stat-c-val" style="color:var(--orange)">1.15</span><div class="stat-c-bar-wrap"><div class="stat-c-bar bar-away" style="width:53%"></div></div><span style="font-size:9px;color:var(--muted);font-family:'Space Mono'">PNE</span></div>
    </div>
    <div class="stat-compare">
      <div class="stat-c-label">Goals Conceded/Game</div>
      <div class="stat-c-row"><span class="stat-c-val" style="color:var(--red)">1.69</span><div class="stat-c-bar-wrap"><div class="stat-c-bar" style="width:75%;background:var(--red)"></div></div><span style="font-size:9px;color:var(--muted);font-family:'Space Mono'">LEIC</span></div>
      <div class="stat-c-row"><span class="stat-c-val" style="color:var(--red)">1.26</span><div class="stat-c-bar-wrap"><div class="stat-c-bar" style="width:58%;background:var(--red)"></div></div><span style="font-size:9px;color:var(--muted);font-family:'Space Mono'">PNE</span></div>
    </div>
    <div class="stat-compare">
      <div class="stat-c-label">Shots on Target/Game</div>
      <div class="stat-c-row"><span class="stat-c-val" style="color:var(--accent2)">~4.5</span><div class="stat-c-bar-wrap"><div class="stat-c-bar bar-home" style="width:60%"></div></div><span style="font-size:9px;color:var(--muted);font-family:'Space Mono'">LEIC</span></div>
      <div class="stat-c-row"><span class="stat-c-val" style="color:var(--orange)">~3.8</span><div class="stat-c-bar-wrap"><div class="stat-c-bar bar-away" style="width:50%"></div></div><span style="font-size:9px;color:var(--muted);font-family:'Space Mono'">PNE</span></div>
    </div>
    <div class="stat-compare">
      <div class="stat-c-label">Home Possession</div>
      <div class="stat-c-row"><span class="stat-c-val" style="color:var(--accent2)">51%</span><div class="stat-c-bar-wrap"><div class="stat-c-bar bar-home" style="width:51%"></div></div><span style="font-size:9px;color:var(--muted);font-family:'Space Mono'">LEIC</span></div>
      <div class="stat-c-row"><span class="stat-c-val" style="color:var(--orange)">~47%</span><div class="stat-c-bar-wrap"><div class="stat-c-bar bar-away" style="width:47%"></div></div><span style="font-size:9px;color:var(--muted);font-family:'Space Mono'">PNE</span></div>
    </div>
  </div>
  <div class="pred-box">
    <div class="section-title">📊 Prediction</div>
    <div class="pred-scoreline-row">
      <div class="pred-team">Leicester <span class="verdict-tag vt-home">HOME WIN</span></div>
      <div class="pred-score-badge">2 – 1</div>
      <div class="pred-team right">Preston</div>
    </div>
    <div class="pred-metrics">
      <div class="pred-metric"><div class="pm-label">Goals</div><div class="pm-val goals">2–3</div><div class="pm-range">BTTS likely</div></div>
      <div class="pred-metric"><div class="pm-label">Corners</div><div class="pm-val corners">9–13</div><div class="pm-range">Leicester dominate</div></div>
      <div class="pred-metric"><div class="pm-label">Yellow Cards</div><div class="pm-val yellow">3–5</div><div class="pm-range">Feisty relegation clash</div></div>
      <div class="pred-metric"><div class="pm-label">Shots on Target</div><div class="pm-val sot">7–12</div><div class="pm-range">Leicester push forward</div></div>
      <div class="pred-metric"><div class="pm-label">Total Shots</div><div class="pm-val shots">22–30</div><div class="pm-range">High Leicester volume</div></div>
      <div class="pred-metric"><div class="pm-label">Red Card Risk</div><div class="pm-val red">LOW</div><div class="pm-range pm-red-risk"><div class="risk-track"><div class="risk-fill" style="width:15%"></div></div><span class="risk-pct">~15%</span></div></div>
    </div>
    <div class="pred-analysis"><strong>Analysis:</strong> <strong>Survival six-pointer</strong> for Leicester — they must win. Preston are mid-table and have nothing to play for, but arrive in decent form after beating Stoke 3-1. Leicester's desperation will drive them forward but their defence remains porous (conceded in 15 of last 16 home games). Daka and Fatawu are their key weapons. Preston's away record is poor (winless in 6 on road). Leicester's home urgency should prevail in a 2-1 win, but BTTS is near-certain given both teams' defensive leakiness.</div>
  </div>
</div>

<!-- ===================== MATCH 3: NORWICH v PORTSMOUTH ===================== -->
<div class="match-card accent-norwich" id="m3">
  <div class="match-card-header">
    <div class="match-num-badge">MATCH 3</div>
    <div class="team-block">
      <div class="team-name">Norwich City</div>
      <div class="team-pos">~8th · ~53pts · Good form</div>
      <div class="team-form">
        <div class="fd fw">W</div><div class="fd fw">W</div><div class="fd fw">W</div><div class="fd fd2">D</div><div class="fd fw">W</div>
      </div>
    </div>
    <div class="vs-center">
      <div class="vs-text">VS</div>
      <div class="match-info">CARROW ROAD · 15:00</div>
    </div>
    <div class="team-block right">
      <div class="team-name">Portsmouth <span class="banner-tag bt-relegation">DANGER ZONE</span></div>
      <div class="team-pos">21st · ~40pts · 1pt from last 18</div>
      <div class="team-form">
        <div class="fd fl">L</div><div class="fd fl">L</div><div class="fd fl">L</div><div class="fd fl">L</div><div class="fd fl">L</div>
      </div>
    </div>
  </div>
  <div class="card-body">
    <div class="section-col">
      <div class="section-title">Norwich — Last 10</div>
      <div class="form-entry"><span class="fe-opp">vs West Brom (A) ★</span><span class="fe-comp">Ch</span><span class="fe-result r-w">5-0 W</span></div>
      <div class="form-entry"><span class="fe-opp">vs Southampton (H)</span><span class="fe-comp">Ch</span><span class="fe-result fd2">2-2 D</span></div>
      <div class="form-entry"><span class="fe-opp">vs Coventry (A)</span><span class="fe-comp">Ch</span><span class="fe-result r-l">0-2 L</span></div>
      <div class="form-entry"><span class="fe-opp">vs Portsmouth (H)</span><span class="fe-comp">Ch</span><span class="fe-result r-w">3-0 W</span></div>
      <div class="form-entry"><span class="fe-opp">vs Preston (H)</span><span class="fe-comp">Ch</span><span class="fe-result r-w">2-0 W</span></div>
      <div class="form-entry"><span class="fe-opp">vs Swansea (A)</span><span class="fe-comp">Ch</span><span class="fe-result r-w">2-1 W</span></div>
      <div class="form-entry"><span class="fe-opp">vs Leicester (A)</span><span class="fe-comp">Ch</span><span class="fe-result fd2">1-1 D</span></div>
      <div class="form-entry"><span class="fe-opp">vs Hull City (H)</span><span class="fe-comp">Ch</span><span class="fe-result r-w">2-0 W</span></div>
      <div class="form-entry"><span class="fe-opp">vs Watford (A)</span><span class="fe-comp">Ch</span><span class="fe-result r-w">2-1 W</span></div>
      <div class="form-entry"><span class="fe-opp">vs Charlton (A)</span><span class="fe-comp">Ch</span><span class="fe-result r-w">1-0 W</span></div>
      <div class="section-sub">Excellent home record. Philippe Clement era — settled system. Scored 2+ in 7 of last 10. Top scorers: Armstrong, McLean.</div>
    </div>
    <div class="section-col">
      <div class="section-title">Portsmouth — Last 10</div>
      <div class="form-entry"><span class="fe-opp">vs QPR (A) ★</span><span class="fe-comp">Ch</span><span class="fe-result r-l">1-6 L</span></div>
      <div class="form-entry"><span class="fe-opp">vs Derby (H)</span><span class="fe-comp">Ch</span><span class="fe-result r-l">0-1 L</span></div>
      <div class="form-entry"><span class="fe-opp">vs Blackburn (H)</span><span class="fe-comp">Ch</span><span class="fe-result r-l">1-2 L</span></div>
      <div class="form-entry"><span class="fe-opp">vs Birmingham (A)</span><span class="fe-comp">Ch</span><span class="fe-result r-l">0-2 L</span></div>
      <div class="form-entry"><span class="fe-opp">vs Leicester (A)</span><span class="fe-comp">Ch</span><span class="fe-result r-l">1-2 L</span></div>
      <div class="form-entry"><span class="fe-opp">vs Charlton (H)</span><span class="fe-comp">Ch</span><span class="fe-result r-l">1-2 L</span></div>
      <div class="form-entry"><span class="fe-opp">vs Hull (A)</span><span class="fe-comp">Ch</span><span class="fe-result r-l">0-2 L</span></div>
      <div class="form-entry"><span class="fe-opp">vs Oxford (H)</span><span class="fe-comp">Ch</span><span class="fe-result fd2">1-1 D</span></div>
      <div class="form-entry"><span class="fe-opp">vs Ipswich (A)</span><span class="fe-comp">Ch</span><span class="fe-result r-l">0-3 L</span></div>
      <div class="form-entry"><span class="fe-opp">vs Middlesbrough (H)</span><span class="fe-comp">Ch</span><span class="fe-result r-l">0-1 L</span></div>
      <div class="section-sub">1pt from last 18 available. Outshot QPR 20-8 but lost 6-1. Deep crisis — worst away record in division.</div>
    </div>
    <div class="section-col">
      <div class="section-title">H2H — Last 5</div>
      <div class="h2h-entry"><span class="h2h-date">Jan 2026</span><span>Norwich</span><span class="h2h-score" style="color:var(--win)">3–0</span><span>Portsmouth</span></div>
      <div class="h2h-entry"><span class="h2h-date">Sep 2025</span><span>Portsmouth</span><span class="h2h-score" style="color:var(--draw)">0–0</span><span>Norwich</span></div>
      <div class="h2h-entry"><span class="h2h-date">2024/25</span><span>Norwich</span><span class="h2h-score" style="color:var(--win)">2–1</span><span>Portsmouth</span></div>
      <div class="h2h-entry"><span class="h2h-date">2024/25</span><span>Portsmouth</span><span class="h2h-score" style="color:var(--draw)">1–1</span><span>Norwich</span></div>
      <div class="h2h-entry"><span class="h2h-date">2023/24</span><span>Norwich</span><span class="h2h-score" style="color:var(--win)">3–1</span><span>Portsmouth</span></div>
      <div class="section-sub">Norwich beat Portsmouth 3-0 earlier this season. Norfolk side dominant in recent H2H. Portsmouth also lost at Charlton this season.</div>
      <div class="injury-note"><strong>Key:</strong> Portsmouth already played 20 shots vs QPR but lost 6-1. Finishing crisis and morale rock bottom. Only 1pt from last 18.</div>
    </div>
  </div>
  <div class="stats-grid">
    <div class="stat-compare"><div class="stat-c-label">Goals/Game</div><div class="stat-c-row"><span class="stat-c-val" style="color:var(--win)">1.7</span><div class="stat-c-bar-wrap"><div class="stat-c-bar bar-home" style="width:70%"></div></div><span style="font-size:9px;color:var(--muted);font-family:'Space Mono'">NORWICH</span></div><div class="stat-c-row"><span class="stat-c-val" style="color:var(--red)">0.9</span><div class="stat-c-bar-wrap"><div class="stat-c-bar" style="width:35%;background:var(--red)"></div></div><span style="font-size:9px;color:var(--muted);font-family:'Space Mono'">POMPEY</span></div></div>
    <div class="stat-compare"><div class="stat-c-label">Conceded/Game</div><div class="stat-c-row"><span class="stat-c-val" style="color:var(--accent2)">0.9</span><div class="stat-c-bar-wrap"><div class="stat-c-bar bar-home" style="width:35%"></div></div><span style="font-size:9px;color:var(--muted);font-family:'Space Mono'">NORWICH</span></div><div class="stat-c-row"><span class="stat-c-val" style="color:var(--red)">2.1</span><div class="stat-c-bar-wrap"><div class="stat-c-bar" style="width:80%;background:var(--red)"></div></div><span style="font-size:9px;color:var(--muted);font-family:'Space Mono'">POMPEY</span></div></div>
    <div class="stat-compare"><div class="stat-c-label">Shots on Target/Game</div><div class="stat-c-row"><span class="stat-c-val" style="color:var(--win)">~5.5</span><div class="stat-c-bar-wrap"><div class="stat-c-bar bar-home" style="width:65%"></div></div><span style="font-size:9px;color:var(--muted);font-family:'Space Mono'">NORWICH</span></div><div class="stat-c-row"><span class="stat-c-val" style="color:var(--red)">~4.0</span><div class="stat-c-bar-wrap"><div class="stat-c-bar" style="width:50%;background:var(--orange)"></div></div><span style="font-size:9px;color:var(--muted);font-family:'Space Mono'">POMPEY</span></div></div>
    <div class="stat-compare"><div class="stat-c-label">Win Rate</div><div class="stat-c-row"><span class="stat-c-val" style="color:var(--win)">52%</span><div class="stat-c-bar-wrap"><div class="stat-c-bar bar-home" style="width:52%"></div></div><span style="font-size:9px;color:var(--muted);font-family:'Space Mono'">NORWICH</span></div><div class="stat-c-row"><span class="stat-c-val" style="color:var(--red)">17%</span><div class="stat-c-bar-wrap"><div class="stat-c-bar" style="width:17%;background:var(--red)"></div></div><span style="font-size:9px;color:var(--muted);font-family:'Space Mono'">POMPEY</span></div></div>
  </div>
  <div class="pred-box">
    <div class="section-title">📊 Prediction</div>
    <div class="pred-scoreline-row">
      <div class="pred-team">Norwich City <span class="verdict-tag vt-home">STRONG HOME</span></div>
      <div class="pred-score-badge">3 – 0</div>
      <div class="pred-team right">Portsmouth</div>
    </div>
    <div class="pred-metrics">
      <div class="pred-metric"><div class="pm-label">Goals</div><div class="pm-val goals">2–4</div><div class="pm-range">Norwich cruise</div></div>
      <div class="pred-metric"><div class="pm-label">Corners</div><div class="pm-val corners">10–14</div><div class="pm-range">Norwich dominate</div></div>
      <div class="pred-metric"><div class="pm-label">Yellow Cards</div><div class="pm-val yellow">2–4</div><div class="pm-range">Pompey frustration</div></div>
      <div class="pred-metric"><div class="pm-label">Shots on Target</div><div class="pm-val sot">8–13</div><div class="pm-range">Norwich attack-heavy</div></div>
      <div class="pred-metric"><div class="pm-label">Total Shots</div><div class="pm-val shots">24–32</div><div class="pm-range">High Norwich volume</div></div>
      <div class="pred-metric"><div class="pm-label">Red Card Risk</div><div class="pm-val red">LOW</div><div class="pm-range pm-red-risk"><div class="risk-track"><div class="risk-fill" style="width:10%"></div></div><span class="risk-pct">~10%</span></div></div>
    </div>
    <div class="pred-analysis"><strong>Analysis:</strong> This is the most one-sided fixture of the day. <strong>Norwich already beat Portsmouth 3-0 at Carrow Road earlier this season</strong>. Pompey have taken just 1 point from their last 18 available — their morale and confidence is at rock bottom. They conceded 6 at QPR while actually creating chances (20 shots). Norwich's attack is firing with McLean, Armstrong and Slimane in good form. A comfortable, high-scoring Norwich win expected.</div>
  </div>
</div>

<!-- ===================== MATCH 4: OXFORD v HULL ===================== -->
<div class="match-card accent-oxford" id="m4">
  <div class="match-card-header">
    <div class="match-num-badge">MATCH 4</div>
    <div class="team-block">
      <div class="team-name">Oxford United <span class="banner-tag bt-relegation">NEAR ZONE</span></div>
      <div class="team-pos">~20th · ~44pts · Bloomfield mgr</div>
      <div class="team-form">
        <div class="fd fl">L</div><div class="fd fl">L</div><div class="fd fw">W</div><div class="fd fl">L</div><div class="fd fl">L</div>
      </div>
    </div>
    <div class="vs-center">
      <div class="vs-text">VS</div>
      <div class="match-info">KASSAM STADIUM · 15:00</div>
    </div>
    <div class="team-block right">
      <div class="team-name">Hull City <span class="banner-tag bt-playoff">PLAY-OFF HUNT</span></div>
      <div class="team-pos">5th · 60pts · +8 GD</div>
      <div class="team-form">
        <div class="fd fw">W</div><div class="fd fl">L</div><div class="fd fw">W</div><div class="fd fw">W</div><div class="fd fw">W</div>
      </div>
    </div>
  </div>
  <div class="card-body">
    <div class="section-col">
      <div class="section-title">Oxford — Last 10</div>
      <div class="form-entry"><span class="fe-opp">vs West Brom (H)</span><span class="fe-comp">Ch</span><span class="fe-result r-w">2-1 W</span></div>
      <div class="form-entry"><span class="fe-opp">vs Coventry (A)</span><span class="fe-comp">Ch</span><span class="fe-result r-l">0-3 L</span></div>
      <div class="form-entry"><span class="fe-opp">vs Blackburn (H)</span><span class="fe-comp">Ch</span><span class="fe-result r-l">0-2 L</span></div>
      <div class="form-entry"><span class="fe-opp">vs Middlesbrough (A)</span><span class="fe-comp">Ch</span><span class="fe-result r-l">1-2 L</span></div>
      <div class="form-entry"><span class="fe-opp">vs Portsmouth (A)</span><span class="fe-comp">Ch</span><span class="fe-result fd2">1-1 D</span></div>
      <div class="form-entry"><span class="fe-opp">vs Derby (H)</span><span class="fe-comp">Ch</span><span class="fe-result r-l">0-2 L</span></div>
      <div class="form-entry"><span class="fe-opp">vs Charlton (A)</span><span class="fe-comp">Ch</span><span class="fe-result r-w">1-0 W</span></div>
      <div class="form-entry"><span class="fe-opp">vs Preston (H)</span><span class="fe-comp">Ch</span><span class="fe-result r-w">2-1 W</span></div>
      <div class="form-entry"><span class="fe-opp">vs Sheffield Wed (H)</span><span class="fe-comp">Ch</span><span class="fe-result r-w">3-0 W</span></div>
      <div class="form-entry"><span class="fe-opp">vs Southampton (H)</span><span class="fe-comp">Ch</span><span class="fe-result r-l">0-2 L</span></div>
      <div class="section-sub">New manager Matt Bloomfield (Jan). Kassam Stadium tight — small ground (12,500). Inconsistent but capable upsets.</div>
    </div>
    <div class="section-col">
      <div class="section-title">Hull City — Last 10</div>
      <div class="form-entry"><span class="fe-opp">vs West Brom (A)</span><span class="fe-comp">Ch</span><span class="fe-result r-l">0-3 L</span></div>
      <div class="form-entry"><span class="fe-opp">vs Bristol City (H)</span><span class="fe-comp">Ch</span><span class="fe-result r-w">3-1 W</span></div>
      <div class="form-entry"><span class="fe-opp">vs Watford (H)</span><span class="fe-comp">Ch</span><span class="fe-result r-w">2-0 W</span></div>
      <div class="form-entry"><span class="fe-opp">vs Millwall (A)</span><span class="fe-comp">Ch</span><span class="fe-result r-l">0-1 L</span></div>
      <div class="form-entry"><span class="fe-opp">vs QPR (H)</span><span class="fe-comp">Ch</span><span class="fe-result r-w">3-1 W</span></div>
      <div class="form-entry"><span class="fe-opp">vs Norwich (A)</span><span class="fe-comp">Ch</span><span class="fe-result r-l">0-2 L</span></div>
      <div class="form-entry"><span class="fe-opp">vs Derby (A)</span><span class="fe-comp">Ch</span><span class="fe-result r-w">2-1 W</span></div>
      <div class="form-entry"><span class="fe-opp">vs Ipswich (H)</span><span class="fe-comp">Ch</span><span class="fe-result r-l">0-2 L</span></div>
      <div class="form-entry"><span class="fe-opp">vs Swansea (A)</span><span class="fe-comp">Ch</span><span class="fe-result r-w">2-1 W</span></div>
      <div class="form-entry"><span class="fe-opp">vs Sheff Wed (A)</span><span class="fe-comp">Ch</span><span class="fe-result r-w">3-1 W</span></div>
      <div class="section-sub">56 goals scored this season — 3rd highest in division. Jakirović solid manager. Top scorer Vipotnik. 5th place, genuine play-off threat.</div>
    </div>
    <div class="section-col">
      <div class="section-title">H2H — Last 5</div>
      <div class="h2h-entry"><span class="h2h-date">Nov 2025</span><span>Oxford</span><span class="h2h-score" style="color:var(--draw)">1–1</span><span>Hull</span></div>
      <div class="h2h-entry"><span class="h2h-date">Feb 2025</span><span>Hull</span><span class="h2h-score" style="color:var(--win)">2–0</span><span>Oxford</span></div>
      <div class="h2h-entry"><span class="h2h-date">Oct 2024</span><span>Oxford</span><span class="h2h-score" style="color:var(--draw)">0–0</span><span>Hull</span></div>
      <div class="h2h-entry"><span class="h2h-date">2024/25</span><span>Hull</span><span class="h2h-score" style="color:var(--win)">3–0</span><span>Oxford</span></div>
      <div class="h2h-entry"><span class="h2h-date">2023/24</span><span>Oxford</span><span class="h2h-score" style="color:var(--draw)">1–1</span><span>Hull</span></div>
      <div class="section-sub">Hull dominant in H2H. Drew 1-1 at Kassam earlier this season. Hull beat Oxford heavily in recent meetings.</div>
      <div class="injury-note"><strong>Context:</strong> Oxford's Kassam Stadium (12,500 capacity) can be a tough atmosphere but Hull's quality shines through. Oxford beat West Brom 2-1 last time showing they can still cause upsets.</div>
    </div>
  </div>
  <div class="stats-grid">
    <div class="stat-compare"><div class="stat-c-label">Goals Scored</div><div class="stat-c-row"><span class="stat-c-val" style="color:var(--accent2)">~38</span><div class="stat-c-bar-wrap"><div class="stat-c-bar bar-home" style="width:48%"></div></div><span style="font-size:9px;color:var(--muted);font-family:'Space Mono'">OXFORD</span></div><div class="stat-c-row"><span class="stat-c-val" style="color:var(--win)">56</span><div class="stat-c-bar-wrap"><div class="stat-c-bar" style="width:70%;background:var(--win)"></div></div><span style="font-size:9px;color:var(--muted);font-family:'Space Mono'">HULL</span></div></div>
    <div class="stat-compare"><div class="stat-c-label">Goals Conceded</div><div class="stat-c-row"><span class="stat-c-val" style="color:var(--red)">~55</span><div class="stat-c-bar-wrap"><div class="stat-c-bar" style="width:75%;background:var(--red)"></div></div><span style="font-size:9px;color:var(--muted);font-family:'Space Mono'">OXFORD</span></div><div class="stat-c-row"><span class="stat-c-val" style="color:var(--orange)">48</span><div class="stat-c-bar-wrap"><div class="stat-c-bar" style="width:60%;background:var(--orange)"></div></div><span style="font-size:9px;color:var(--muted);font-family:'Space Mono'">HULL</span></div></div>
    <div class="stat-compare"><div class="stat-c-label">League Position</div><div class="stat-c-row"><span class="stat-c-val" style="color:var(--red)">20th</span><div class="stat-c-bar-wrap"><div class="stat-c-bar" style="width:20%;background:var(--red)"></div></div><span style="font-size:9px;color:var(--muted);font-family:'Space Mono'">OXFORD</span></div><div class="stat-c-row"><span class="stat-c-val" style="color:var(--win)">5th</span><div class="stat-c-bar-wrap"><div class="stat-c-bar" style="width:85%;background:var(--win)"></div></div><span style="font-size:9px;color:var(--muted);font-family:'Space Mono'">HULL</span></div></div>
    <div class="stat-compare"><div class="stat-c-label">Win Rate</div><div class="stat-c-row"><span class="stat-c-val" style="color:var(--orange)">28%</span><div class="stat-c-bar-wrap"><div class="stat-c-bar bar-home" style="width:28%"></div></div><span style="font-size:9px;color:var(--muted);font-family:'Space Mono'">OXFORD</span></div><div class="stat-c-row"><span class="stat-c-val" style="color:var(--win)">47%</span><div class="stat-c-bar-wrap"><div class="stat-c-bar" style="width:47%;background:var(--win)"></div></div><span style="font-size:9px;color:var(--muted);font-family:'Space Mono'">HULL</span></div></div>
  </div>
  <div class="pred-box">
    <div class="section-title">📊 Prediction</div>
    <div class="pred-scoreline-row">
      <div class="pred-team">Oxford Utd</div>
      <div class="pred-score-badge">1 – 2</div>
      <div class="pred-team right">Hull City <span class="verdict-tag vt-away">AWAY WIN</span></div>
    </div>
    <div class="pred-metrics">
      <div class="pred-metric"><div class="pm-label">Goals</div><div class="pm-val goals">2–4</div><div class="pm-range">Open game</div></div>
      <div class="pred-metric"><div class="pm-label">Corners</div><div class="pm-val corners">9–13</div><div class="pm-range">Hull dominate</div></div>
      <div class="pred-metric"><div class="pm-label">Yellow Cards</div><div class="pm-val yellow">3–5</div><div class="pm-range">Physical contest</div></div>
      <div class="pred-metric"><div class="pm-label">Shots on Target</div><div class="pm-val sot">7–12</div><div class="pm-range">Hull push</div></div>
      <div class="pred-metric"><div class="pm-label">Total Shots</div><div class="pm-val shots">22–30</div><div class="pm-range">Both active</div></div>
      <div class="pred-metric"><div class="pm-label">Red Card Risk</div><div class="pm-val red">LOW</div><div class="pm-range pm-red-risk"><div class="risk-track"><div class="risk-fill" style="width:13%"></div></div><span class="risk-pct">~13%</span></div></div>
    </div>
    <div class="pred-analysis"><strong>Analysis:</strong> Hull City need points in the play-off race and arrive with 60 points and genuine quality. They beat Oxford 3-0 and 2-0 in recent H2H. Oxford are struggling but do have a tight, difficult ground. Expect Hull to win but the Kassam's atmosphere could make it scrappy. Vipotnik and the Hull attack should see them over the line.</div>
  </div>
</div>

<!-- ===================== MATCH 5: QPR v WATFORD ===================== -->
<div class="match-card accent-qpr" id="m5">
  <div class="match-card-header">
    <div class="match-num-badge">MATCH 5</div>
    <div class="team-block">
      <div class="team-name">Queens Park Rangers</div>
      <div class="team-pos">~10th · ~49pts · Stéphan mgr</div>
      <div class="team-form">
        <div class="fd fw">W</div><div class="fd fw">W</div><div class="fd fl">L</div><div class="fd fw">W</div><div class="fd fw">W</div>
      </div>
    </div>
    <div class="vs-center">
      <div class="vs-text">VS</div>
      <div class="match-info">LOFTUS ROAD · 15:00</div>
    </div>
    <div class="team-block right">
      <div class="team-name">Watford</div>
      <div class="team-pos">~14th · ~46pts · Still mgr</div>
      <div class="team-form">
        <div class="fd fd2">D</div><div class="fd fw">W</div><div class="fd fl">L</div><span style="font-size:11px;color:var(--muted)"> (recent)</span>
      </div>
    </div>
  </div>
  <div class="card-body">
    <div class="section-col">
      <div class="section-title">QPR — Last 10</div>
      <div class="form-entry"><span class="fe-opp">vs Portsmouth (H) ★</span><span class="fe-comp">Ch</span><span class="fe-result r-w">6-1 W</span></div>
      <div class="form-entry"><span class="fe-opp">vs Hull City (A)</span><span class="fe-comp">Ch</span><span class="fe-result r-l">1-3 L</span></div>
      <div class="form-entry"><span class="fe-opp">vs Leicester (A)</span><span class="fe-comp">Ch</span><span class="fe-result r-w">3-1 W</span></div>
      <div class="form-entry"><span class="fe-opp">vs Swansea (H)</span><span class="fe-comp">Ch</span><span class="fe-result r-w">2-0 W</span></div>
      <div class="form-entry"><span class="fe-opp">vs Birmingham (H)</span><span class="fe-comp">Ch</span><span class="fe-result fd2">1-1 D</span></div>
      <div class="form-entry"><span class="fe-opp">vs Bristol City (H)</span><span class="fe-comp">Ch</span><span class="fe-result r-w">2-1 W</span></div>
      <div class="form-entry"><span class="fe-opp">vs Preston (H)</span><span class="fe-comp">Ch</span><span class="fe-result r-w">2-1 W</span></div>
      <div class="form-entry"><span class="fe-opp">vs Derby (A)</span><span class="fe-comp">Ch</span><span class="fe-result r-l">0-2 L</span></div>
      <div class="form-entry"><span class="fe-opp">vs West Brom (H)</span><span class="fe-comp">Ch</span><span class="fe-result r-w">2-0 W</span></div>
      <div class="form-entry"><span class="fe-opp">vs Stoke (A)</span><span class="fe-comp">Ch</span><span class="fe-result fd2">1-1 D</span></div>
      <div class="section-sub">6-1 vs Portsmouth was season highlight! Strong home form at Loftus Road. Stéphan has QPR playing good football.</div>
    </div>
    <div class="section-col">
      <div class="section-title">Watford — Last 10</div>
      <div class="form-entry"><span class="fe-opp">vs Leicester (H)</span><span class="fe-comp">Ch</span><span class="fe-result fd2">0-0 D</span></div>
      <div class="form-entry"><span class="fe-opp">vs Wrexham (H)</span><span class="fe-comp">Ch</span><span class="fe-result r-w">3-1 W</span></div>
      <div class="form-entry"><span class="fe-opp">vs Southampton (A)</span><span class="fe-comp">Ch</span><span class="fe-result r-l">0-2 L</span></div>
      <div class="form-entry"><span class="fe-opp">vs Millwall (H)</span><span class="fe-comp">Ch</span><span class="fe-result fd2">1-1 D</span></div>
      <div class="form-entry"><span class="fe-opp">vs Hull (A)</span><span class="fe-comp">Ch</span><span class="fe-result r-l">0-2 L</span></div>
      <div class="form-entry"><span class="fe-opp">vs Coventry (H)</span><span class="fe-comp">Ch</span><span class="fe-result r-l">1-2 L</span></div>
      <div class="form-entry"><span class="fe-opp">vs Norwich (H)</span><span class="fe-comp">Ch</span><span class="fe-result r-l">1-2 L</span></div>
      <div class="form-entry"><span class="fe-opp">vs Ipswich (A)</span><span class="fe-comp">Ch</span><span class="fe-result r-l">1-3 L</span></div>
      <div class="form-entry"><span class="fe-opp">vs Charlton (A)</span><span class="fe-comp">Ch</span><span class="fe-result fd2">1-1 D</span></div>
      <div class="form-entry"><span class="fe-opp">vs Bristol City (H)</span><span class="fe-comp">Ch</span><span class="fe-result r-w">2-1 W</span></div>
      <div class="section-sub">Edward Still replaced Gracia. Mid-table comfort. Still building under new manager. Inconsistent results.</div>
    </div>
    <div class="section-col">
      <div class="section-title">H2H — Last 5</div>
      <div class="h2h-entry"><span class="h2h-date">Aug 2025</span><span>Watford</span><span class="h2h-score" style="color:var(--win)">2–0</span><span>QPR</span></div>
      <div class="h2h-entry"><span class="h2h-date">2024/25</span><span>QPR</span><span class="h2h-score" style="color:var(--draw)">1–1</span><span>Watford</span></div>
      <div class="h2h-entry"><span class="h2h-date">2024/25</span><span>Watford</span><span class="h2h-score" style="color:var(--win)">2–1</span><span>QPR</span></div>
      <div class="h2h-entry"><span class="h2h-date">2023/24</span><span>QPR</span><span class="h2h-score" style="color:var(--win)">2–1</span><span>Watford</span></div>
      <div class="h2h-entry"><span class="h2h-date">2023/24</span><span>Watford</span><span class="h2h-score" style="color:var(--draw)">0–0</span><span>QPR</span></div>
      <div class="section-sub">Watford won reverse fixture 2-0. Recent H2H tight. QPR's Coventry 7-1 home moment shows Loftus Road can explode. QPR in better form.</div>
      <div class="injury-note"><strong>Context:</strong> QPR destroyed Portsmouth 6-1. This QPR side has moments of real quality. Watford under new manager Still stabilising but away form has been poor.</div>
    </div>
  </div>
  <div class="stats-grid">
    <div class="stat-compare"><div class="stat-c-label">Goals/Game (Season)</div><div class="stat-c-row"><span class="stat-c-val" style="color:var(--accent2)">1.5</span><div class="stat-c-bar-wrap"><div class="stat-c-bar bar-home" style="width:65%"></div></div><span style="font-size:9px;color:var(--muted);font-family:'Space Mono'">QPR</span></div><div class="stat-c-row"><span class="stat-c-val" style="color:var(--orange)">1.2</span><div class="stat-c-bar-wrap"><div class="stat-c-bar bar-away" style="width:52%"></div></div><span style="font-size:9px;color:var(--muted);font-family:'Space Mono'">WATFORD</span></div></div>
    <div class="stat-compare"><div class="stat-c-label">Home vs Away Edge</div><div class="stat-c-row"><span class="stat-c-val" style="color:var(--win)">Strong</span><div class="stat-c-bar-wrap"><div class="stat-c-bar bar-home" style="width:75%"></div></div><span style="font-size:9px;color:var(--muted);font-family:'Space Mono'">QPR HOME</span></div><div class="stat-c-row"><span class="stat-c-val" style="color:var(--red)">Weak away</span><div class="stat-c-bar-wrap"><div class="stat-c-bar" style="width:30%;background:var(--red)"></div></div><span style="font-size:9px;color:var(--muted);font-family:'Space Mono'">WATFORD AWAY</span></div></div>
    <div class="stat-compare"><div class="stat-c-label">Shots on Target/Game</div><div class="stat-c-row"><span class="stat-c-val" style="color:var(--accent2)">~5.0</span><div class="stat-c-bar-wrap"><div class="stat-c-bar bar-home" style="width:62%"></div></div><span style="font-size:9px;color:var(--muted);font-family:'Space Mono'">QPR</span></div><div class="stat-c-row"><span class="stat-c-val" style="color:var(--orange)">~4.0</span><div class="stat-c-bar-wrap"><div class="stat-c-bar bar-away" style="width:50%"></div></div><span style="font-size:9px;color:var(--muted);font-family:'Space Mono'">WATFORD</span></div></div>
    <div class="stat-compare"><div class="stat-c-label">League Form (last 5)</div><div class="stat-c-row"><span class="stat-c-val" style="color:var(--win)">WWLWW</span><div class="stat-c-bar-wrap"><div class="stat-c-bar bar-home" style="width:80%"></div></div><span style="font-size:9px;color:var(--muted);font-family:'Space Mono'">QPR</span></div><div class="stat-c-row"><span class="stat-c-val" style="color:var(--orange)">DWLDD</span><div class="stat-c-bar-wrap"><div class="stat-c-bar bar-away" style="width:40%"></div></div><span style="font-size:9px;color:var(--muted);font-family:'Space Mono'">WATFORD</span></div></div>
  </div>
  <div class="pred-box">
    <div class="section-title">📊 Prediction</div>
    <div class="pred-scoreline-row">
      <div class="pred-team">QPR <span class="verdict-tag vt-home">HOME WIN</span></div>
      <div class="pred-score-badge">2 – 1</div>
      <div class="pred-team right">Watford</div>
    </div>
    <div class="pred-metrics">
      <div class="pred-metric"><div class="pm-label">Goals</div><div class="pm-val goals">2–3</div><div class="pm-range">BTTS possible</div></div>
      <div class="pred-metric"><div class="pm-label">Corners</div><div class="pm-val corners">9–13</div><div class="pm-range">Both competitive</div></div>
      <div class="pred-metric"><div class="pm-label">Yellow Cards</div><div class="pm-val yellow">3–5</div><div class="pm-range">Midfield battle</div></div>
      <div class="pred-metric"><div class="pm-label">Shots on Target</div><div class="pm-val sot">7–11</div><div class="pm-range">QPR edge</div></div>
      <div class="pred-metric"><div class="pm-label">Total Shots</div><div class="pm-val shots">22–30</div><div class="pm-range">Both attack-minded</div></div>
      <div class="pred-metric"><div class="pm-label">Red Card Risk</div><div class="pm-val red">LOW</div><div class="pm-range pm-red-risk"><div class="risk-track"><div class="risk-fill" style="width:12%"></div></div><span class="risk-pct">~12%</span></div></div>
    </div>
    <div class="pred-analysis"><strong>Analysis:</strong> QPR's brilliant 6-1 win over Portsmouth shows their attacking capability and confidence at Loftus Road. Watford are mid-table but have lost 4 of their last 6 away games. The reverse fixture went Watford's way 2-0 but QPR's current form and home advantage makes them favourites here. Expect an entertaining game with QPR edging it.</div>
  </div>
</div>

<!-- ===================== MATCH 6: SHEFFIELD UNITED v SWANSEA ===================== -->
<div class="match-card accent-shefutd" id="m6">
  <div class="match-card-header">
    <div class="match-num-badge">MATCH 6</div>
    <div class="team-block">
      <div class="team-name">Sheffield United</div>
      <div class="team-pos">~11th · ~50pts · Wilder mgr</div>
      <div class="team-form">
        <div class="fd fl">L</div><div class="fd fd2">D</div><div class="fd fd2">D</div><div class="fd fl">L</div><div class="fd fw">W</div>
      </div>
    </div>
    <div class="vs-center">
      <div class="vs-text">VS</div>
      <div class="match-info">BRAMALL LANE · 15:00</div>
    </div>
    <div class="team-block right">
      <div class="team-name">Swansea City</div>
      <div class="team-pos">~9th · ~51pts · Matos mgr</div>
      <div class="team-form">
        <div class="fd fl">L</div><div class="fd fl">L</div><div class="fd fw">W</div><div class="fd fw">W</div><div class="fd fw">W</div>
      </div>
    </div>
  </div>
  <div class="card-body">
    <div class="section-col">
      <div class="section-title">Sheff United — Last 10</div>
      <div class="form-entry"><span class="fe-opp">vs Wrexham (H)</span><span class="fe-comp">Ch</span><span class="fe-result r-l">1-2 L</span></div>
      <div class="form-entry"><span class="fe-opp">vs Watford (A)</span><span class="fe-comp">Ch</span><span class="fe-result fd2">1-1 D</span></div>
      <div class="form-entry"><span class="fe-opp">vs Southampton (H)</span><span class="fe-comp">Ch</span><span class="fe-result fd2">1-1 D</span></div>
      <div class="form-entry"><span class="fe-opp">vs Derby (H)</span><span class="fe-comp">Ch</span><span class="fe-result r-l">1-2 L</span></div>
      <div class="form-entry"><span class="fe-opp">vs Norwich (A)</span><span class="fe-comp">Ch</span><span class="fe-result fd2">1-1 D</span></div>
      <div class="form-entry"><span class="fe-opp">vs Millwall (H)</span><span class="fe-comp">Ch</span><span class="fe-result r-w">2-0 W</span></div>
      <div class="form-entry"><span class="fe-opp">vs Wrexham (A)</span><span class="fe-comp">Ch</span><span class="fe-result r-l">3-5 L ★</span></div>
      <div class="form-entry"><span class="fe-opp">vs Middlesbrough (A)</span><span class="fe-comp">Ch</span><span class="fe-result r-l">0-2 L</span></div>
      <div class="form-entry"><span class="fe-opp">vs Derby (A)</span><span class="fe-comp">Ch</span><span class="fe-result r-w">2-1 W</span></div>
      <div class="form-entry"><span class="fe-opp">vs Blackburn (A)</span><span class="fe-comp">Ch</span><span class="fe-result r-w">3-1 W</span></div>
      <div class="section-sub">4 games without a win. 9 games without a Bramall Lane clean sheet. Both teams scored in all of those 9 games at home. Scored in 10 consecutive games.</div>
    </div>
    <div class="section-col">
      <div class="section-title">Swansea City — Last 10</div>
      <div class="form-entry"><span class="fe-opp">vs Coventry (H)</span><span class="fe-comp">Ch</span><span class="fe-result r-l">0-3 L</span></div>
      <div class="form-entry"><span class="fe-opp">vs Birmingham (A)</span><span class="fe-comp">Ch</span><span class="fe-result r-l">0-1 L</span></div>
      <div class="form-entry"><span class="fe-opp">vs Middlesbrough (H)</span><span class="fe-comp">Ch</span><span class="fe-result r-w">2-0 W</span></div>
      <div class="form-entry"><span class="fe-opp">vs Wrexham (A)</span><span class="fe-comp">Ch</span><span class="fe-result r-l">1-2 L</span></div>
      <div class="form-entry"><span class="fe-opp">vs Preston (A)</span><span class="fe-comp">Ch</span><span class="fe-result r-w">2-0 W</span></div>
      <div class="form-entry"><span class="fe-opp">vs Hull (H)</span><span class="fe-comp">Ch</span><span class="fe-result r-l">1-2 L</span></div>
      <div class="form-entry"><span class="fe-opp">vs Norwich (H)</span><span class="fe-comp">Ch</span><span class="fe-result r-l">1-2 L</span></div>
      <div class="form-entry"><span class="fe-opp">vs Oxford (H)</span><span class="fe-comp">Ch</span><span class="fe-result r-w">2-1 W</span></div>
      <div class="form-entry"><span class="fe-opp">vs Stoke (A)</span><span class="fe-comp">Ch</span><span class="fe-result fd2">1-1 D</span></div>
      <div class="form-entry"><span class="fe-opp">vs Sheffield Utd (H)</span><span class="fe-comp">Ch</span><span class="fe-result r-w">1-0 W</span></div>
      <div class="section-sub">Swansea won last H2H 1-0. Lost 3-0 to Coventry — conceded 3 in 11 mins. Vipotnik (16 goals, top scorer) key. Back-to-back defeats.</div>
    </div>
    <div class="section-col">
      <div class="section-title">H2H — Last 5</div>
      <div class="h2h-entry"><span class="h2h-date">Oct 2025</span><span>Swansea</span><span class="h2h-score" style="color:var(--win)">1–0</span><span>Sheff Utd</span></div>
      <div class="h2h-entry"><span class="h2h-date">2024/25</span><span>Sheff Utd</span><span class="h2h-score" style="color:var(--win)">2–1</span><span>Swansea</span></div>
      <div class="h2h-entry"><span class="h2h-date">2024/25</span><span>Swansea</span><span class="h2h-score" style="color:var(--draw)">1–1</span><span>Sheff Utd</span></div>
      <div class="h2h-entry"><span class="h2h-date">2023/24</span><span>Sheff Utd</span><span class="h2h-score" style="color:var(--win)">3–2</span><span>Swansea</span></div>
      <div class="h2h-entry"><span class="h2h-date">2022/23</span><span>Swansea</span><span class="h2h-score" style="color:var(--draw)">0–0</span><span>Sheff Utd</span></div>
      <div class="section-sub">Swansea won last H2H 1-0. Both teams have scored in Bramall Lane's last 9 home games. BTTS near-certainty at Bramall Lane.</div>
      <div class="injury-note"><strong>Key facts:</strong> Sheffield United have 9 games without a home clean sheet — both teams scored in all of them. 100% BTTS at Bramall Lane in that run. Expect goals here.</div>
    </div>
  </div>
  <div class="stats-grid">
    <div class="stat-compare"><div class="stat-c-label">Home Clean Sheet Rate</div><div class="stat-c-row"><span class="stat-c-val" style="color:var(--red)">20%</span><div class="stat-c-bar-wrap"><div class="stat-c-bar" style="width:20%;background:var(--red)"></div></div><span style="font-size:9px;color:var(--muted);font-family:'Space Mono'">SHEF UTD</span></div><div class="stat-c-row"><span class="stat-c-val" style="color:var(--accent2)">25%</span><div class="stat-c-bar-wrap"><div class="stat-c-bar bar-away" style="width:25%"></div></div><span style="font-size:9px;color:var(--muted);font-family:'Space Mono'">SWANSEA</span></div></div>
    <div class="stat-compare"><div class="stat-c-label">Goals Scored/Game</div><div class="stat-c-row"><span class="stat-c-val" style="color:var(--accent2)">1.4</span><div class="stat-c-bar-wrap"><div class="stat-c-bar bar-home" style="width:60%"></div></div><span style="font-size:9px;color:var(--muted);font-family:'Space Mono'">SHEF UTD</span></div><div class="stat-c-row"><span class="stat-c-val" style="color:var(--orange)">1.3</span><div class="stat-c-bar-wrap"><div class="stat-c-bar bar-away" style="width:55%"></div></div><span style="font-size:9px;color:var(--muted);font-family:'Space Mono'">SWANSEA</span></div></div>
    <div class="stat-compare"><div class="stat-c-label">Top Scorer</div><div class="stat-c-row"><span class="stat-c-val" style="color:var(--accent2)" style="font-size:10px">Bamford</span><div class="stat-c-bar-wrap"><div class="stat-c-bar bar-home" style="width:55%"></div></div><span style="font-size:9px;color:var(--muted);font-family:'Space Mono'">SUF</span></div><div class="stat-c-row"><span class="stat-c-val" style="color:var(--win)" style="font-size:10px">Vipotnik</span><div class="stat-c-bar-wrap"><div class="stat-c-bar" style="width:80%;background:var(--win)"></div></div><span style="font-size:9px;color:var(--muted);font-family:'Space Mono'">16 GOALS</span></div></div>
    <div class="stat-compare"><div class="stat-c-label">League Form (last 5)</div><div class="stat-c-row"><span class="stat-c-val" style="color:var(--orange)">LDDLW</span><div class="stat-c-bar-wrap"><div class="stat-c-bar bar-home" style="width:35%"></div></div><span style="font-size:9px;color:var(--muted);font-family:'Space Mono'">SHEF UTD</span></div><div class="stat-c-row"><span class="stat-c-val" style="color:var(--red)">LLWWW</span><div class="stat-c-bar-wrap"><div class="stat-c-bar bar-away" style="width:45%"></div></div><span style="font-size:9px;color:var(--muted);font-family:'Space Mono'">SWANSEA</span></div></div>
  </div>
  <div class="pred-box">
    <div class="section-title">📊 Prediction</div>
    <div class="pred-scoreline-row">
      <div class="pred-team">Sheff United</div>
      <div class="pred-score-badge">2 – 2</div>
      <div class="pred-team right">Swansea <span class="verdict-tag vt-draw">DRAW</span></div>
    </div>
    <div class="pred-metrics">
      <div class="pred-metric"><div class="pm-label">Goals</div><div class="pm-val goals">2–4</div><div class="pm-range">BTTS near-certain</div></div>
      <div class="pred-metric"><div class="pm-label">Corners</div><div class="pm-val corners">9–13</div><div class="pm-range">Both attack</div></div>
      <div class="pred-metric"><div class="pm-label">Yellow Cards</div><div class="pm-val yellow">3–6</div><div class="pm-range">Derby intensity</div></div>
      <div class="pred-metric"><div class="pm-label">Shots on Target</div><div class="pm-val sot">8–13</div><div class="pm-range">Open game</div></div>
      <div class="pred-metric"><div class="pm-label">Total Shots</div><div class="pm-val shots">24–32</div><div class="pm-range">High</div></div>
      <div class="pred-metric"><div class="pm-label">Red Card Risk</div><div class="pm-val red">MODERATE</div><div class="pm-range pm-red-risk"><div class="risk-track"><div class="risk-fill" style="width:22%"></div></div><span class="risk-pct">~22%</span></div></div>
    </div>
    <div class="pred-analysis"><strong>Analysis:</strong> <strong>BTTS is virtually guaranteed</strong> — Bramall Lane has seen both teams score in 9 consecutive home games. Sheff United have scored in 10 straight games. Swansea have Vipotnik (16 goals, league top scorer) who always poses a threat. Both teams need a win but have been inconsistent. This looks like a high-octane, action-packed draw with goals flowing both ways.</div>
  </div>
</div>

<!-- ===================== MATCH 7: STOKE v SHEFFIELD WEDNESDAY ===================== -->
<div class="match-card accent-stoke" id="m7">
  <div class="match-card-header">
    <div class="match-num-badge">MATCH 7</div>
    <div class="team-block">
      <div class="team-name">Stoke City</div>
      <div class="team-pos">~15th · ~45pts · Robins mgr</div>
      <div class="team-form">
        <div class="fd fl">L</div><div class="fd fd2">D</div><div class="fd fw">W</div><div class="fd fd2">D</div><div class="fd fw">W</div>
      </div>
    </div>
    <div class="vs-center">
      <div class="vs-text">VS</div>
      <div class="match-info">BET365 STADIUM · 15:00</div>
    </div>
    <div class="team-block right">
      <div class="team-name">Sheffield Wednesday <span class="banner-tag bt-relegation">RELEGATED −18pts</span></div>
      <div class="team-pos">24th · ~14pts · 29-game winless</div>
      <div class="team-form">
        <div class="fd fl">L</div><div class="fd fl">L</div><div class="fd fl">L</div><div class="fd fl">L</div><div class="fd fl">L</div>
      </div>
    </div>
  </div>
  <div class="card-body">
    <div class="section-col">
      <div class="section-title">Stoke City — Last 10</div>
      <div class="form-entry"><span class="fe-opp">vs Preston (A)</span><span class="fe-comp">Ch</span><span class="fe-result r-l">1-3 L</span></div>
      <div class="form-entry"><span class="fe-opp">vs Blackburn (H)</span><span class="fe-comp">Ch</span><span class="fe-result fd2">0-0 D</span></div>
      <div class="form-entry"><span class="fe-opp">vs Birmingham (H)</span><span class="fe-comp">Ch</span><span class="fe-result r-w">2-1 W</span></div>
      <div class="form-entry"><span class="fe-opp">vs QPR (H)</span><span class="fe-comp">Ch</span><span class="fe-result fd2">1-1 D</span></div>
      <div class="form-entry"><span class="fe-opp">vs Watford (H)</span><span class="fe-comp">Ch</span><span class="fe-result r-w">2-0 W</span></div>
      <div class="form-entry"><span class="fe-opp">vs Middlesbrough (A)</span><span class="fe-comp">Ch</span><span class="fe-result r-l">1-2 L</span></div>
      <div class="form-entry"><span class="fe-opp">vs Derby (A)</span><span class="fe-comp">Ch</span><span class="fe-result r-l">0-1 L</span></div>
      <div class="form-entry"><span class="fe-opp">vs Hull (A)</span><span class="fe-comp">Ch</span><span class="fe-result r-l">1-2 L</span></div>
      <div class="form-entry"><span class="fe-opp">vs Charlton (H)</span><span class="fe-comp">Ch</span><span class="fe-result fd2">0-0 D</span></div>
      <div class="form-entry"><span class="fe-opp">vs Swansea (H)</span><span class="fe-comp">Ch</span><span class="fe-result fd2">1-1 D</span></div>
      <div class="section-sub">Inconsistent but solid at home. Mark Robins era. Decent enough form to be safe. No great attacking flair but defensive resilience at home.</div>
    </div>
    <div class="section-col">
      <div class="section-title">Sheffield Wednesday — Last 10</div>
      <div class="form-entry"><span class="fe-opp">vs Hull (H)</span><span class="fe-comp">Ch</span><span class="fe-result r-l">1-3 L</span></div>
      <div class="form-entry"><span class="fe-opp">vs Blackburn (A)</span><span class="fe-comp">Ch</span><span class="fe-result r-l">1-2 L</span></div>
      <div class="form-entry"><span class="fe-opp">vs Ipswich (H)</span><span class="fe-comp">Ch</span><span class="fe-result r-l">0-1 L</span></div>
      <div class="form-entry"><span class="fe-opp">vs Oxford (A)</span><span class="fe-comp">Ch</span><span class="fe-result r-l">0-3 L</span></div>
      <div class="form-entry"><span class="fe-opp">vs Middlesbrough (H)</span><span class="fe-comp">Ch</span><span class="fe-result r-l">0-1 L</span></div>
      <div class="form-entry"><span class="fe-opp">vs Southampton (A)</span><span class="fe-comp">Ch</span><span class="fe-result r-l">0-2 L</span></div>
      <div class="form-entry"><span class="fe-opp">vs Coventry (H) ★</span><span class="fe-comp">Ch</span><span class="fe-result r-l">0-5 L</span></div>
      <div class="form-entry"><span class="fe-opp">vs Sheffield Utd (H)</span><span class="fe-comp">Ch</span><span class="fe-result r-l">0-3 L</span></div>
      <div class="form-entry"><span class="fe-opp">vs Derby (H)</span><span class="fe-comp">Ch</span><span class="fe-result r-l">1-2 L</span></div>
      <div class="form-entry"><span class="fe-opp">vs Watford (H)</span><span class="fe-comp">Ch</span><span class="fe-result r-l">1-2 L</span></div>
      <div class="section-sub"><strong>Worst record in EFL history this season.</strong> 29-game winless run. -18pts deduction (admin + payment breaches). RELEGATED. Lowest morale in the division. 12-game losing streak at one point.</div>
    </div>
    <div class="section-col">
      <div class="section-title">H2H — Last 5</div>
      <div class="h2h-entry"><span class="h2h-date">Nov 2025</span><span>Stoke</span><span class="h2h-score" style="color:var(--win)">3–1</span><span>Sheff Wed</span></div>
      <div class="h2h-entry"><span class="h2h-date">Mar 2025</span><span>Sheff Wed</span><span class="h2h-score" style="color:var(--win)">2–0</span><span>Stoke</span></div>
      <div class="h2h-entry"><span class="h2h-date">Nov 2024</span><span>Stoke</span><span class="h2h-score" style="color:var(--win)">2–1</span><span>Sheff Wed</span></div>
      <div class="h2h-entry"><span class="h2h-date">2023/24</span><span>Sheff Wed</span><span class="h2h-score" style="color:var(--draw)">1–1</span><span>Stoke</span></div>
      <div class="h2h-entry"><span class="h2h-date">2023/24</span><span>Stoke</span><span class="h2h-score" style="color:var(--win)">3–0</span><span>Sheff Wed</span></div>
      <div class="section-sub">Stoke beat Wednesday 3-1 in the reverse earlier this season. Wednesday haven't won in 29 games. Their season is over — zero motivation.</div>
      <div class="injury-note"><strong>Context:</strong> Wednesday are already relegated. This is a dead rubber for them. Financial chaos, administration, 29-game winless run. Lowest average attendance (7,081 at one home game). Stoke should cruise.</div>
    </div>
  </div>
  <div class="stats-grid">
    <div class="stat-compare"><div class="stat-c-label">Goals Scored (Season)</div><div class="stat-c-row"><span class="stat-c-val" style="color:var(--accent2)">~44</span><div class="stat-c-bar-wrap"><div class="stat-c-bar bar-home" style="width:56%"></div></div><span style="font-size:9px;color:var(--muted);font-family:'Space Mono'">STOKE</span></div><div class="stat-c-row"><span class="stat-c-val" style="color:var(--red)">~25</span><div class="stat-c-bar-wrap"><div class="stat-c-bar" style="width:30%;background:var(--red)"></div></div><span style="font-size:9px;color:var(--muted);font-family:'Space Mono'">SHEF WED</span></div></div>
    <div class="stat-compare"><div class="stat-c-label">Goals Conceded (Season)</div><div class="stat-c-row"><span class="stat-c-val" style="color:var(--orange)">~49</span><div class="stat-c-bar-wrap"><div class="stat-c-bar bar-home" style="width:57%"></div></div><span style="font-size:9px;color:var(--muted);font-family:'Space Mono'">STOKE</span></div><div class="stat-c-row"><span class="stat-c-val" style="color:var(--red)">~75+</span><div class="stat-c-bar-wrap"><div class="stat-c-bar" style="width:90%;background:var(--red)"></div></div><span style="font-size:9px;color:var(--muted);font-family:'Space Mono'">SHEF WED</span></div></div>
    <div class="stat-compare"><div class="stat-c-label">Wins (Season)</div><div class="stat-c-row"><span class="stat-c-val" style="color:var(--accent2)">~12</span><div class="stat-c-bar-wrap"><div class="stat-c-bar bar-home" style="width:60%"></div></div><span style="font-size:9px;color:var(--muted);font-family:'Space Mono'">STOKE</span></div><div class="stat-c-row"><span class="stat-c-val" style="color:var(--red)">2</span><div class="stat-c-bar-wrap"><div class="stat-c-bar" style="width:8%;background:var(--red)"></div></div><span style="font-size:9px;color:var(--muted);font-family:'Space Mono'">SHEF WED</span></div></div>
    <div class="stat-compare"><div class="stat-c-label">Points (adj.)</div><div class="stat-c-row"><span class="stat-c-val" style="color:var(--accent2)">~45</span><div class="stat-c-bar-wrap"><div class="stat-c-bar bar-home" style="width:50%"></div></div><span style="font-size:9px;color:var(--muted);font-family:'Space Mono'">STOKE</span></div><div class="stat-c-row"><span class="stat-c-val" style="color:var(--red)">~14</span><div class="stat-c-bar-wrap"><div class="stat-c-bar" style="width:15%;background:var(--red)"></div></div><span style="font-size:9px;color:var(--muted);font-family:'Space Mono'">SHEF WED (−18)</span></div></div>
  </div>
  <div class="pred-box">
    <div class="section-title">📊 Prediction</div>
    <div class="pred-scoreline-row">
      <div class="pred-team">Stoke City <span class="verdict-tag vt-home">STRONG HOME</span></div>
      <div class="pred-score-badge">3 – 0</div>
      <div class="pred-team right">Sheffield Wednesday</div>
    </div>
    <div class="pred-metrics">
      <div class="pred-metric"><div class="pm-label">Goals</div><div class="pm-val goals">2–4</div><div class="pm-range">Stoke clinical</div></div>
      <div class="pred-metric"><div class="pm-label">Corners</div><div class="pm-val corners">10–14</div><div class="pm-range">Stoke dominate</div></div>
      <div class="pred-metric"><div class="pm-label">Yellow Cards</div><div class="pm-val yellow">2–4</div><div class="pm-range">Wednesday may frustrate</div></div>
      <div class="pred-metric"><div class="pm-label">Shots on Target</div><div class="pm-val sot">8–13</div><div class="pm-range">Stoke pressure</div></div>
      <div class="pred-metric"><div class="pm-label">Total Shots</div><div class="pm-val shots">22–30</div><div class="pm-range">Stoke volume</div></div>
      <div class="pred-metric"><div class="pm-label">Red Card Risk</div><div class="pm-val red">MODERATE</div><div class="pm-range pm-red-risk"><div class="risk-track"><div class="risk-fill" style="width:20%"></div></div><span class="risk-pct">~20%</span></div></div>
    </div>
    <div class="pred-analysis"><strong>Analysis:</strong> The Championship's most one-sided fixture. Sheffield Wednesday are <strong>already relegated</strong> with a 29-game winless run and an -18pt deduction due to administration. They've conceded at least 2 in most away games this season (lost 0-5 at home to Coventry). Stoke beat them 3-1 earlier this season. A comfortable Stoke win is expected. The red card risk is moderate because Wednesday may resort to cynical fouls in frustration. Highest likelihood of a clean sheet for Stoke all day.</div>
  </div>
</div>

<!-- ===================== MATCH 8: WEST BROM v WREXHAM ===================== -->
<div class="match-card accent-westbrom" id="m8">
  <div class="match-card-header">
    <div class="match-num-badge">MATCH 8</div>
    <div class="team-block">
      <div class="team-name">West Brom <span class="banner-tag bt-relegation">SURVIVAL FIGHT</span></div>
      <div class="team-pos">~21st · 43pts · Morrison mgr</div>
      <div class="team-form">
        <div class="fd fw">W</div><div class="fd fw">W</div><div class="fd fd2">D</div><div class="fd fd2">D</div><div class="fd fl">L</div>
      </div>
    </div>
    <div class="vs-center">
      <div class="vs-text">VS</div>
      <div class="match-info">THE HAWTHORNS · 15:00</div>
    </div>
    <div class="team-block right">
      <div class="team-name">Wrexham <span class="banner-tag bt-playoff">PLAY-OFF HUNT</span> <span class="banner-tag bt-newboy">PROMOTED</span></div>
      <div class="team-pos">7th · 57pts · Parkinson mgr</div>
      <div class="team-form">
        <div class="fd fw">W</div><div class="fd fl">L</div><div class="fd fw">W</div><div class="fd fl">L</div><div class="fd fl">L</div>
      </div>
    </div>
  </div>
  <div class="card-body">
    <div class="section-col">
      <div class="section-title">West Brom — Last 10</div>
      <div class="form-entry"><span class="fe-opp">vs Bristol City (A)</span><span class="fe-comp">Ch</span><span class="fe-result r-w">1-0 W</span></div>
      <div class="form-entry"><span class="fe-opp">vs Hull City (H)</span><span class="fe-comp">Ch</span><span class="fe-result r-w">3-0 W</span></div>
      <div class="form-entry"><span class="fe-opp">vs Southampton (H)</span><span class="fe-comp">Ch</span><span class="fe-result fd2">1-1 D</span></div>
      <div class="form-entry"><span class="fe-opp">vs Sheffield Utd (A)</span><span class="fe-comp">Ch</span><span class="fe-result fd2">1-1 D</span></div>
      <div class="form-entry"><span class="fe-opp">vs Oxford (A)</span><span class="fe-comp">Ch</span><span class="fe-result r-l">1-2 L</span></div>
      <div class="form-entry"><span class="fe-opp">vs Blackburn (H)</span><span class="fe-comp">Ch</span><span class="fe-result r-l">0-2 L</span></div>
      <div class="form-entry"><span class="fe-opp">vs Swansea (A)</span><span class="fe-comp">Ch</span><span class="fe-result fd2">1-1 D</span></div>
      <div class="form-entry"><span class="fe-opp">vs Norwich ★</span><span class="fe-comp">Ch</span><span class="fe-result r-l">0-5 L</span></div>
      <div class="form-entry"><span class="fe-opp">vs Coventry (A)</span><span class="fe-comp">Ch</span><span class="fe-result r-l">0-3 L</span></div>
      <div class="form-entry"><span class="fe-opp">vs Charlton (A)</span><span class="fe-comp">Ch</span><span class="fe-result fd2">1-1 D</span></div>
      <div class="section-sub">Manager change in Jan (Morrison after Ramsay). Unbeaten in last 4. Beat Hull 3-0, Bristol 1-0 back-to-back wins. 4pts clear of drop.</div>
    </div>
    <div class="section-col">
      <div class="section-title">Wrexham — Last 10</div>
      <div class="form-entry"><span class="fe-opp">vs Sheffield Utd (A)</span><span class="fe-comp">Ch</span><span class="fe-result r-w">2-1 W</span></div>
      <div class="form-entry"><span class="fe-opp">vs Watford (A)</span><span class="fe-comp">Ch</span><span class="fe-result r-l">1-3 L</span></div>
      <div class="form-entry"><span class="fe-opp">vs Charlton (H)</span><span class="fe-comp">Ch</span><span class="fe-result r-w">1-0 W</span></div>
      <div class="form-entry"><span class="fe-opp">vs Bristol City (A)</span><span class="fe-comp">Ch</span><span class="fe-result fd2">2-2 D</span></div>
      <div class="form-entry"><span class="fe-opp">vs Swansea (H)</span><span class="fe-comp">Ch</span><span class="fe-result r-w">2-1 W</span></div>
      <div class="form-entry"><span class="fe-opp">vs Millwall (A)</span><span class="fe-comp">Ch</span><span class="fe-result fd2">1-1 D</span></div>
      <div class="form-entry"><span class="fe-opp">vs Ipswich ★</span><span class="fe-comp">Ch</span><span class="fe-result r-w">5-3 W</span></div>
      <div class="form-entry"><span class="fe-opp">vs Sheffield Utd ★</span><span class="fe-comp">Ch</span><span class="fe-result r-l">3-5 L</span></div>
      <div class="form-entry"><span class="fe-opp">vs Birmingham (H)</span><span class="fe-comp">Ch</span><span class="fe-result r-w">3-2 W</span></div>
      <div class="form-entry"><span class="fe-opp">vs Derby (A)</span><span class="fe-comp">Ch</span><span class="fe-result r-l">0-2 L</span></div>
      <div class="section-sub">Promoted side punching above weight! 7th place. 54 goals (highest scoring mid-table). Windass, Smith, Brooks key. Unbeaten in 10 of last 13. Road record: W6, D1 in last 8 away games.</div>
    </div>
    <div class="section-col">
      <div class="section-title">H2H — Last 5</div>
      <div class="h2h-entry"><span class="h2h-date">Aug 2025</span><span>Wrexham</span><span class="h2h-score" style="color:var(--red)">2–3</span><span>West Brom</span></div>
      <div class="h2h-entry"><span class="h2h-date">FA Cup 1930</span><span>WBA</span><span class="h2h-score">W</span><span>Wrexham</span></div>
      <div class="h2h-entry" style="opacity:0.4"><span class="h2h-date">Historical</span><span colspan="3" style="font-size:10px;color:var(--muted)">Very limited modern H2H</span></div>
      <div class="section-sub" style="margin-top:8px;">Only 3 meetings ever. West Brom won the August 2025 Championship game 3-2 at Wrexham. Very limited H2H history. First season these clubs meet at The Hawthorns in the Championship.</div>
      <div class="injury-note"><strong>Key Stakes:</strong> West Brom desperately need points to stay up (4pts above relegation). Wrexham need points for a top-6 finish in their debut Championship season. Both teams have high motivation. Potentially the match of the day at The Hawthorns.</div>
    </div>
  </div>
  <div class="stats-grid">
    <div class="stat-compare"><div class="stat-c-label">Goals/Game</div><div class="stat-c-row"><span class="stat-c-val" style="color:var(--accent2)">1.1</span><div class="stat-c-bar-wrap"><div class="stat-c-bar bar-home" style="width:47%"></div></div><span style="font-size:9px;color:var(--muted);font-family:'Space Mono'">WEST BROM</span></div><div class="stat-c-row"><span class="stat-c-val" style="color:var(--orange)">1.4</span><div class="stat-c-bar-wrap"><div class="stat-c-bar bar-away" style="width:60%"></div></div><span style="font-size:9px;color:var(--muted);font-family:'Space Mono'">WREXHAM</span></div></div>
    <div class="stat-compare"><div class="stat-c-label">Recent Form (last 4)</div><div class="stat-c-row"><span class="stat-c-val" style="color:var(--win)">WWDD</span><div class="stat-c-bar-wrap"><div class="stat-c-bar bar-home" style="width:80%"></div></div><span style="font-size:9px;color:var(--muted);font-family:'Space Mono'">WBA</span></div><div class="stat-c-row"><span class="stat-c-val" style="color:var(--orange)">WLWL</span><div class="stat-c-bar-wrap"><div class="stat-c-bar bar-away" style="width:50%"></div></div><span style="font-size:9px;color:var(--muted);font-family:'Space Mono'">WREXHAM</span></div></div>
    <div class="stat-compare"><div class="stat-c-label">Away Record (Wrexham)</div><div class="stat-c-row"><span class="stat-c-val" style="color:var(--win)">W6,D1</span><div class="stat-c-bar-wrap"><div class="stat-c-bar" style="width:75%;background:var(--win)"></div></div><span style="font-size:9px;color:var(--muted);font-family:'Space Mono'">LAST 8 AWAY</span></div></div>
    <div class="stat-compare"><div class="stat-c-label">Goals Scored (Season)</div><div class="stat-c-row"><span class="stat-c-val" style="color:var(--accent2)">~43</span><div class="stat-c-bar-wrap"><div class="stat-c-bar bar-home" style="width:54%"></div></div><span style="font-size:9px;color:var(--muted);font-family:'Space Mono'">WBA</span></div><div class="stat-c-row"><span class="stat-c-val" style="color:var(--orange)">54</span><div class="stat-c-bar-wrap"><div class="stat-c-bar bar-away" style="width:68%"></div></div><span style="font-size:9px;color:var(--muted);font-family:'Space Mono'">WREXHAM</span></div></div>
  </div>
  <div class="pred-box">
    <div class="section-title">📊 Prediction</div>
    <div class="pred-scoreline-row">
      <div class="pred-team">West Brom</div>
      <div class="pred-score-badge">1 – 1</div>
      <div class="pred-team right">Wrexham <span class="verdict-tag vt-draw">DRAW</span></div>
    </div>
    <div class="pred-metrics">
      <div class="pred-metric"><div class="pm-label">Goals</div><div class="pm-val goals">2–3</div><div class="pm-range">BTTS</div></div>
      <div class="pred-metric"><div class="pm-label">Corners</div><div class="pm-val corners">10–14</div><div class="pm-range">Both create</div></div>
      <div class="pred-metric"><div class="pm-label">Yellow Cards</div><div class="pm-val yellow">4–6</div><div class="pm-range">High stakes, physical</div></div>
      <div class="pred-metric"><div class="pm-label">Shots on Target</div><div class="pm-val sot">8–13</div><div class="pm-range">High quality</div></div>
      <div class="pred-metric"><div class="pm-label">Total Shots</div><div class="pm-val shots">24–32</div><div class="pm-range">Both attack-minded</div></div>
      <div class="pred-metric"><div class="pm-label">Red Card Risk</div><div class="pm-val red">MODERATE</div><div class="pm-range pm-red-risk"><div class="risk-track"><div class="risk-fill" style="width:25%"></div></div><span class="risk-pct">~25%</span></div></div>
    </div>
    <div class="pred-analysis"><strong>Analysis:</strong> <strong>The Game of the Day</strong> — relegation vs promotion aspirations. West Brom have found some form under Morrison (unbeaten in 4) but Wrexham's road record is exceptional (W6, D1 in last 8 away). Both teams will attack, both need points. The high stakes and contrasting situations make this fiercely contested. A draw is the most likely outcome in what should be an entertaining, end-to-end contest. Red card risk elevated due to the pressure on both sides.</div>
  </div>
</div>

<!-- ===================== MATCH 9: COVENTRY v DERBY ===================== -->
<div class="match-card accent-coventry" id="m9">
  <div class="match-card-header">
    <div class="match-num-badge">MATCH 9</div>
    <div class="team-block">
      <div class="team-name">Coventry City <span class="banner-tag bt-promotion">CHAMPIONS</span></div>
      <div class="team-pos">1st · 80pts · Lampard mgr</div>
      <div class="team-form">
        <div class="fd fw">W</div><div class="fd fw">W</div><div class="fd fw">W</div><div class="fd fw">W</div><div class="fd fw">W</div>
      </div>
    </div>
    <div class="vs-center">
      <div class="vs-text">VS</div>
      <div class="match-info">CBS ARENA · 21:00</div>
    </div>
    <div class="team-block right">
      <div class="team-name">Derby County</div>
      <div class="team-pos">~8th · ~53pts · Eustace mgr</div>
      <div class="team-form">
        <div class="fd fw">W</div><div class="fd fw">W</div><div class="fd fw">W</div><div class="fd fl">L</div><div class="fd fw">W</div>
      </div>
    </div>
  </div>
  <div class="card-body">
    <div class="section-col">
      <div class="section-title">Coventry — Last 10</div>
      <div class="form-entry"><span class="fe-opp">vs Swansea (A)</span><span class="fe-comp">Ch</span><span class="fe-result r-w">3-0 W</span></div>
      <div class="form-entry"><span class="fe-opp">vs Birmingham ★ (A)</span><span class="fe-comp">Ch</span><span class="fe-result r-w">0-5 W</span></div>
      <div class="form-entry"><span class="fe-opp">vs Oxford (H)</span><span class="fe-comp">Ch</span><span class="fe-result r-w">3-0 W</span></div>
      <div class="form-entry"><span class="fe-opp">vs Preston (A)</span><span class="fe-comp">Ch</span><span class="fe-result r-w">3-0 W</span></div>
      <div class="form-entry"><span class="fe-opp">vs Leicester (A)</span><span class="fe-comp">Ch</span><span class="fe-result r-w">2-0 W</span></div>
      <div class="form-entry"><span class="fe-opp">vs Millwall (H)</span><span class="fe-comp">Ch</span><span class="fe-result fd2">1-1 D</span></div>
      <div class="form-entry"><span class="fe-opp">vs Sheffield Wed ★ (A)</span><span class="fe-comp">Ch</span><span class="fe-result r-w">0-5 W</span></div>
      <div class="form-entry"><span class="fe-opp">vs QPR (H) ★</span><span class="fe-comp">Ch</span><span class="fe-result r-w">7-1 W</span></div>
      <div class="form-entry"><span class="fe-opp">vs Watford (A)</span><span class="fe-comp">Ch</span><span class="fe-result r-w">2-1 W</span></div>
      <div class="form-entry"><span class="fe-opp">vs Middlesbrough (A)</span><span class="fe-comp">Ch</span><span class="fe-result fd2">1-1 D</span></div>
      <div class="section-sub">72 goals scored (most in division). 6-game winning run. <strong>Champions</strong>. Lampard's 4-3-3 devastating in attack. Grimes orchestrates. Average goals scored: 2.1/game.</div>
    </div>
    <div class="section-col">
      <div class="section-title">Derby County — Last 10</div>
      <div class="form-entry"><span class="fe-opp">vs Birmingham (H)</span><span class="fe-comp">Ch</span><span class="fe-result r-w">1-0 W</span></div>
      <div class="form-entry"><span class="fe-opp">vs QPR (H)</span><span class="fe-comp">Ch</span><span class="fe-result r-w">2-0 W</span></div>
      <div class="form-entry"><span class="fe-opp">vs Sheffield Utd (A)</span><span class="fe-comp">Ch</span><span class="fe-result r-w">2-1 W</span></div>
      <div class="form-entry"><span class="fe-opp">vs Middlesbrough (A)</span><span class="fe-comp">Ch</span><span class="fe-result fd2">1-1 D</span></div>
      <div class="form-entry"><span class="fe-opp">vs Portsmouth (A)</span><span class="fe-comp">Ch</span><span class="fe-result r-w">1-0 W</span></div>
      <div class="form-entry"><span class="fe-opp">vs Blackburn (A)</span><span class="fe-comp">Ch</span><span class="fe-result r-l">0-3 L</span></div>
      <div class="form-entry"><span class="fe-opp">vs Charlton (A)</span><span class="fe-comp">Ch</span><span class="fe-result fd2">1-1 D</span></div>
      <div class="form-entry"><span class="fe-opp">vs Wrexham (H)</span><span class="fe-comp">Ch</span><span class="fe-result r-w">2-0 W</span></div>
      <div class="form-entry"><span class="fe-opp">vs Bristol City (A) ★</span><span class="fe-comp">Ch</span><span class="fe-result r-w">5-0 W</span></div>
      <div class="form-entry"><span class="fe-opp">vs Preston (A)</span><span class="fe-comp">Ch</span><span class="fe-result fd2">1-1 D</span></div>
      <div class="section-sub">Excellent recent form — only 1 loss in last 10. Beat Bristol 5-0. Eustace building something good. Comfortable mid-table to play-off chase position.</div>
    </div>
    <div class="section-col">
      <div class="section-title">H2H — Last 5</div>
      <div class="h2h-entry"><span class="h2h-date">Aug 2025 ★</span><span>Derby</span><span class="h2h-score" style="color:var(--red)">3–5</span><span>Coventry</span></div>
      <div class="h2h-entry"><span class="h2h-date">Jan 2025</span><span>Coventry</span><span class="h2h-score" style="color:var(--win)">2–0</span><span>Derby</span></div>
      <div class="h2h-entry"><span class="h2h-date">Sep 2024</span><span>Derby</span><span class="h2h-score" style="color:var(--draw)">1–1</span><span>Coventry</span></div>
      <div class="h2h-entry"><span class="h2h-date">Jan 2024</span><span>Coventry</span><span class="h2h-score" style="color:var(--win)">3–1</span><span>Derby</span></div>
      <div class="h2h-entry"><span class="h2h-date">2023/24</span><span>Derby</span><span class="h2h-score" style="color:var(--win)">2–1</span><span>Coventry</span></div>
      <div class="section-sub">Derby 3-5 Coventry in August was a 8-goal thriller. Both teams can score freely. Coventry dominate recent H2H but Derby are competitive. 4+ goals in last H2H.</div>
      <div class="injury-note"><strong>Context:</strong> Late kick-off (9pm). Coventry are CHAMPIONS and can cruise here. Derby are in good form but face the league's best team. This could be a goal-fest given both teams' offensive capabilities.</div>
    </div>
  </div>
  <div class="stats-grid">
    <div class="stat-compare"><div class="stat-c-label">Goals Scored (Season)</div><div class="stat-c-row"><span class="stat-c-val" style="color:var(--win)">72</span><div class="stat-c-bar-wrap"><div class="stat-c-bar" style="width:90%;background:var(--win)"></div></div><span style="font-size:9px;color:var(--muted);font-family:'Space Mono'">COVENTRY</span></div><div class="stat-c-row"><span class="stat-c-val" style="color:var(--accent2)">~54</span><div class="stat-c-bar-wrap"><div class="stat-c-bar bar-away" style="width:68%"></div></div><span style="font-size:9px;color:var(--muted);font-family:'Space Mono'">DERBY</span></div></div>
    <div class="stat-compare"><div class="stat-c-label">Goals Conceded</div><div class="stat-c-row"><span class="stat-c-val" style="color:var(--green)">38</span><div class="stat-c-bar-wrap"><div class="stat-c-bar bar-home" style="width:48%"></div></div><span style="font-size:9px;color:var(--muted);font-family:'Space Mono'">COVENTRY</span></div><div class="stat-c-row"><span class="stat-c-val" style="color:var(--orange)">~50</span><div class="stat-c-bar-wrap"><div class="stat-c-bar bar-away" style="width:63%"></div></div><span style="font-size:9px;color:var(--muted);font-family:'Space Mono'">DERBY</span></div></div>
    <div class="stat-compare"><div class="stat-c-label">Longest Unbeaten Run</div><div class="stat-c-row"><span class="stat-c-val" style="color:var(--win)">12 games</span><div class="stat-c-bar-wrap"><div class="stat-c-bar" style="width:90%;background:var(--win)"></div></div><span style="font-size:9px;color:var(--muted);font-family:'Space Mono'">COVENTRY</span></div><div class="stat-c-row"><span class="stat-c-val" style="color:var(--accent2)">~6 games</span><div class="stat-c-bar-wrap"><div class="stat-c-bar bar-away" style="width:50%"></div></div><span style="font-size:9px;color:var(--muted);font-family:'Space Mono'">DERBY</span></div></div>
    <div class="stat-compare"><div class="stat-c-label">Wins (Season)</div><div class="stat-c-row"><span class="stat-c-val" style="color:var(--win)">21</span><div class="stat-c-bar-wrap"><div class="stat-c-bar" style="width:88%;background:var(--win)"></div></div><span style="font-size:9px;color:var(--muted);font-family:'Space Mono'">COVENTRY</span></div><div class="stat-c-row"><span class="stat-c-val" style="color:var(--accent2)">~15</span><div class="stat-c-bar-wrap"><div class="stat-c-bar bar-away" style="width:60%"></div></div><span style="font-size:9px;color:var(--muted);font-family:'Space Mono'">DERBY</span></div></div>
  </div>
  <div class="pred-box">
    <div class="section-title">📊 Prediction</div>
    <div class="pred-scoreline-row">
      <div class="pred-team">Coventry <span class="verdict-tag vt-home">CHAMPIONS</span></div>
      <div class="pred-score-badge">3 – 1</div>
      <div class="pred-team right">Derby County</div>
    </div>
    <div class="pred-metrics">
      <div class="pred-metric"><div class="pm-label">Goals</div><div class="pm-val goals">3–5</div><div class="pm-range">High scoring</div></div>
      <div class="pred-metric"><div class="pm-label">Corners</div><div class="pm-val corners">11–15</div><div class="pm-range">Coventry dominate</div></div>
      <div class="pred-metric"><div class="pm-label">Yellow Cards</div><div class="pm-val yellow">3–5</div><div class="pm-range">Competitive still</div></div>
      <div class="pred-metric"><div class="pm-label">Shots on Target</div><div class="pm-val sot">10–16</div><div class="pm-range">Coventry attack fest</div></div>
      <div class="pred-metric"><div class="pm-label">Total Shots</div><div class="pm-val shots">28–38</div><div class="pm-range">Highest volume today</div></div>
      <div class="pred-metric"><div class="pm-label">Red Card Risk</div><div class="pm-val red">LOW</div><div class="pm-range pm-red-risk"><div class="risk-track"><div class="risk-fill" style="width:14%"></div></div><span class="risk-pct">~14%</span></div></div>
    </div>
    <div class="pred-analysis"><strong>Analysis:</strong> <strong>Champions vs the form team</strong> — both teams have been outstanding in recent weeks. The August fixture went Derby 3-5 Coventry, signalling goals are expected. Coventry have scored 72 in 35 games (2.1/game) — the best attack in the division by far. Frank Lampard's 4-3-3 will be unleashed in this late-night CBS Arena encounter. Derby are no pushover (beat Bristol 5-0!) but Coventry's overall quality should prevail. This is the night's <strong>best bet for Over 3.5 goals</strong>.</div>
  </div>
</div>

</div><!-- end matches-wrapper -->

<!-- SUMMARY TABLE -->
<div class="summary-section" id="summary">
  <div class="summary-title">⚡All Predictions at a Glance</div>
  <div style="overflow-x:auto;">
    <table class="summary-table">
      <thead>
        <tr>
          <th>Match</th>
          <th>Score</th>
          <th>Goals</th>
          <th>Corners</th>
          <th>Yellows</th>
          <th>SoT</th>
          <th>Total Shots</th>
          <th>Red Risk</th>
          <th>Verdict</th>
        </tr>
      </thead>
      <tbody>
        <tr>
          <td class="match-label-cell">Charlton vs Bristol City</td>
          <td class="pred-score-cell">1 – 0</td>
          <td>1–2</td>
          <td>8–11</td>
          <td>3–5</td>
          <td>5–9</td>
          <td>18–25</td>
          <td style="color:var(--green)">Low ~12%</td>
          <td><span class="verdict-tag vt-home">Charlton</span></td>
        </tr>
        <tr>
          <td class="match-label-cell">Leicester vs Preston</td>
          <td class="pred-score-cell">2 – 1</td>
          <td>2–3</td>
          <td>9–13</td>
          <td>3–5</td>
          <td>7–12</td>
          <td>22–30</td>
          <td style="color:var(--green)">Low ~15%</td>
          <td><span class="verdict-tag vt-home">Leicester</span></td>
        </tr>
        <tr>
          <td class="match-label-cell">Norwich vs Portsmouth</td>
          <td class="pred-score-cell">3 – 0</td>
          <td>2–4</td>
          <td>10–14</td>
          <td>2–4</td>
          <td>8–13</td>
          <td>24–32</td>
          <td style="color:var(--green)">Low ~10%</td>
          <td><span class="verdict-tag vt-home">Norwich</span></td>
        </tr>
        <tr>
          <td class="match-label-cell">Oxford vs Hull City</td>
          <td class="pred-score-cell">1 – 2</td>
          <td>2–4</td>
          <td>9–13</td>
          <td>3–5</td>
          <td>7–12</td>
          <td>22–30</td>
          <td style="color:var(--green)">Low ~13%</td>
          <td><span class="verdict-tag vt-away">Hull City</span></td>
        </tr>
        <tr>
          <td class="match-label-cell">QPR vs Watford</td>
          <td class="pred-score-cell">2 – 1</td>
          <td>2–3</td>
          <td>9–13</td>
          <td>3–5</td>
          <td>7–11</td>
          <td>22–30</td>
          <td style="color:var(--green)">Low ~12%</td>
          <td><span class="verdict-tag vt-home">QPR</span></td>
        </tr>
        <tr>
          <td class="match-label-cell">Sheffield Utd vs Swansea</td>
          <td class="pred-score-cell">2 – 2</td>
          <td>2–4</td>
          <td>9–13</td>
          <td>3–6</td>
          <td>8–13</td>
          <td>24–32</td>
          <td style="color:var(--orange)">Mod ~22%</td>
          <td><span class="verdict-tag vt-draw">Draw</span></td>
        </tr>
        <tr>
          <td class="match-label-cell">Stoke vs Sheffield Wednesday</td>
          <td class="pred-score-cell">3 – 0</td>
          <td>2–4</td>
          <td>10–14</td>
          <td>2–4</td>
          <td>8–13</td>
          <td>22–30</td>
          <td style="color:var(--orange)">Mod ~20%</td>
          <td><span class="verdict-tag vt-home">Stoke</span></td>
        </tr>
        <tr>
          <td class="match-label-cell">West Brom vs Wrexham</td>
          <td class="pred-score-cell">1 – 1</td>
          <td>2–3</td>
          <td>10–14</td>
          <td>4–6</td>
          <td>8–13</td>
          <td>24–32</td>
          <td style="color:var(--orange)">Mod ~25%</td>
          <td><span class="verdict-tag vt-draw">Draw</span></td>
        </tr>
        <tr>
          <td class="match-label-cell">Coventry vs Derby County</td>
          <td class="pred-score-cell">3 – 1</td>
          <td>3–5</td>
          <td>11–15</td>
          <td>3–5</td>
          <td>10–16</td>
          <td>28–38</td>
          <td style="color:var(--green)">Low ~14%</td>
          <td><span class="verdict-tag vt-home">Coventry</span></td>
        </tr>
      </tbody>
    </table>
  </div>
  <div style="margin-top:16px;padding:14px 16px;background:var(--surface);border:1px solid var(--border);border-radius:8px;font-size:12px;line-height:1.7;color:var(--muted);">
    <strong style="color:var(--accent);">📋 Key Storylines Today:</strong> 
    <strong style="color:var(--text);">Leicester vs Preston</strong> is the day's most desperate fixture (Leicester must win to escape relegation) · 
    <strong style="color:var(--text);">West Brom vs Wrexham</strong> is the most entertaining match on paper (relegation vs play-off push) · 
    <strong style="color:var(--text);">Coventry vs Derby</strong> offers the best Over 3.5 goals value (champions, 72 goals, previous 5-3 H2H) · 
    <strong style="color:var(--text);">Sheffield United vs Swansea</strong> is the best BTTS bet (9 consecutive Bramall Lane both-scored) · 
    <strong style="color:var(--text);">Stoke vs Sheffield Wednesday</strong> is the safest home win (Wednesday relegated, 29 winless). Season avg: <strong style="color:var(--accent);">2.59 goals/match</strong>.
  </div>
</div>

<div class="footer">
  <div><strong>Team Bilbo Statistical Analysis</strong><br>EFL CHAMPIONSHIP MATCHDAY 40 · GOOD FRIDAY, 3 APRIL 2026</div>
  <div style="margin-top:4px;">Analysis based on verified Championship data, season averages and team news as of April 3, 2026. <strong>All predictions are probabilistic estimates only</strong>.</div>
</div>

</body>
</html>
