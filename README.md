<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>FA Cup QF | Match Stats Predictor</title>
<link rel="preconnect" href="https://fonts.googleapis.com">
<link href="https://fonts.googleapis.com/css2?family=Barlow+Condensed:wght@400;600;700;800&family=DM+Sans:wght@300;400;500;600&display=swap" rel="stylesheet">
<style>
  :root {
    --bg: #0a0c10;
    --bg-2: #111318;
    --bg-3: #181c24;
    --border: rgba(255,255,255,0.07);
    --text: #e8eaf0;
    --muted: #8891a4;
    --chelsea-a: #00b4d8;
    --chelsea-b: #0072b1;
    --arsenal-a: #e63946;
    --arsenal-b: #c1121f;
    --accent-gold: #f4b942;
    --low: #4ade80;
    --high: #f97316;
  }

  * { margin: 0; padding: 0; box-sizing: border-box; }

  body {
    font-family: 'DM Sans', sans-serif;
    background: var(--bg);
    color: var(--text);
    min-height: 100vh;
    font-size: 15px;
    line-height: 1.5;
  }

  /* ─── HEADER ─── */
  .site-header {
    background: var(--bg-2);
    border-bottom: 1px solid var(--border);
    padding: 18px 20px;
    text-align: center;
    position: relative;
  }
  .site-header .competition-tag {
    display: inline-block;
    background: var(--accent-gold);
    color: #000;
    font-family: 'Barlow Condensed', sans-serif;
    font-size: 11px;
    font-weight: 700;
    letter-spacing: 1.5px;
    text-transform: uppercase;
    padding: 3px 10px;
    border-radius: 2px;
    margin-bottom: 8px;
  }
  .site-header h1 {
    font-family: 'Barlow Condensed', sans-serif;
    font-size: 22px;
    font-weight: 800;
    letter-spacing: 0.5px;
    color: #fff;
    text-transform: uppercase;
  }
  .site-header .sub {
    font-size: 12px;
    color: var(--muted);
    margin-top: 4px;
  }

  /* ─── LAYOUT ─── */
  .page { max-width: 680px; margin: 0 auto; padding: 20px 16px 48px; }

  /* ─── MATCH BLOCK ─── */
  .match-block { margin-bottom: 40px; }

  .match-title-bar {
    border-radius: 10px 10px 0 0;
    padding: 16px 20px;
    display: flex;
    align-items: center;
    gap: 10px;
  }
  .match-title-bar.chelsea { background: linear-gradient(135deg, var(--chelsea-b), var(--chelsea-a)); }
  .match-title-bar.arsenal  { background: linear-gradient(135deg, var(--arsenal-b), var(--arsenal-a)); }

  .match-title-bar .badge {
    font-family: 'Barlow Condensed', sans-serif;
    font-size: 10px;
    font-weight: 700;
    letter-spacing: 1.2px;
    text-transform: uppercase;
    background: rgba(0,0,0,0.25);
    padding: 2px 8px;
    border-radius: 2px;
    white-space: nowrap;
  }
  .match-title-bar h2 {
    font-family: 'Barlow Condensed', sans-serif;
    font-size: 20px;
    font-weight: 800;
    letter-spacing: 0.3px;
    color: #fff;
    text-transform: uppercase;
    flex: 1;
  }
  .match-title-bar .meta {
    font-size: 11px;
    color: rgba(255,255,255,0.7);
    text-align: right;
    line-height: 1.4;
    white-space: nowrap;
  }

  .match-body {
    background: var(--bg-2);
    border: 1px solid var(--border);
    border-top: none;
    border-radius: 0 0 10px 10px;
    overflow: hidden;
  }

  /* ─── SECTION INSIDE MATCH ─── */
  .section {
    padding: 18px 20px;
    border-bottom: 1px solid var(--border);
  }
  .section:last-child { border-bottom: none; }

  .section-label {
    font-family: 'Barlow Condensed', sans-serif;
    font-size: 11px;
    font-weight: 700;
    letter-spacing: 1.5px;
    text-transform: uppercase;
    color: var(--muted);
    margin-bottom: 12px;
  }

  /* ─── TEAM COLUMNS ─── */
  .team-cols {
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: 12px;
  }
  .team-card {
    background: var(--bg-3);
    border: 1px solid var(--border);
    border-radius: 8px;
    padding: 12px 14px;
  }
  .team-card .team-name {
    font-family: 'Barlow Condensed', sans-serif;
    font-size: 16px;
    font-weight: 700;
    letter-spacing: 0.2px;
    text-transform: uppercase;
    color: #fff;
    margin-bottom: 6px;
  }
  .team-card .team-league {
    font-size: 10px;
    color: var(--muted);
    text-transform: uppercase;
    letter-spacing: 0.8px;
    margin-bottom: 10px;
  }

  /* ─── FORM PILLS ─── */
  .form-row {
    display: flex;
    gap: 4px;
    flex-wrap: wrap;
    margin-bottom: 6px;
  }
  .result-pill {
    display: inline-flex;
    align-items: center;
    justify-content: center;
    width: 24px;
    height: 24px;
    border-radius: 4px;
    font-size: 10px;
    font-weight: 700;
    font-family: 'Barlow Condensed', sans-serif;
  }
  .result-pill.W { background: rgba(74,222,128,0.15); color: var(--low); border: 1px solid rgba(74,222,128,0.3); }
  .result-pill.D { background: rgba(244,185,66,0.12); color: var(--accent-gold); border: 1px solid rgba(244,185,66,0.25); }
  .result-pill.L { background: rgba(249,115,22,0.12); color: var(--high); border: 1px solid rgba(249,115,22,0.3); }

  /* ─── MICRO STATS ─── */
  .mini-stats {
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: 5px;
    margin-top: 8px;
  }
  .mini-stat {
    display: flex;
    flex-direction: column;
  }
  .mini-stat .label { font-size: 10px; color: var(--muted); }
  .mini-stat .value { font-size: 14px; font-weight: 600; color: var(--text); }

  /* ─── H2H ROW ─── */
  .h2h-banner {
    background: var(--bg-3);
    border: 1px solid var(--border);
    border-radius: 8px;
    padding: 12px 16px;
    display: flex;
    align-items: center;
    justify-content: space-between;
    gap: 8px;
  }
  .h2h-stat { text-align: center; flex: 1; }
  .h2h-stat .val {
    font-family: 'Barlow Condensed', sans-serif;
    font-size: 26px;
    font-weight: 800;
    color: #fff;
    line-height: 1;
  }
  .h2h-stat .lbl { font-size: 10px; color: var(--muted); text-transform: uppercase; letter-spacing: 0.8px; margin-top: 2px; }
  .h2h-divider { width: 1px; height: 36px; background: var(--border); }

  /* ─── PREDICTION TABLE ─── */
  .pred-table { width: 100%; border-collapse: collapse; }
  .pred-table th {
    font-family: 'Barlow Condensed', sans-serif;
    font-size: 10px;
    font-weight: 700;
    letter-spacing: 1.2px;
    text-transform: uppercase;
    color: var(--muted);
    padding: 0 0 8px 0;
    text-align: left;
  }
  .pred-table th:not(:first-child) { text-align: center; }
  .pred-table td {
    padding: 7px 0;
    border-bottom: 1px solid var(--border);
    font-size: 14px;
    vertical-align: middle;
  }
  .pred-table tr:last-child td { border-bottom: none; }
  .pred-table td:first-child {
    color: var(--muted);
    font-size: 13px;
    padding-right: 12px;
  }
  .pred-table td:not(:first-child) { text-align: center; }

  .range-cell {
    display: flex;
    align-items: center;
    justify-content: center;
    gap: 6px;
    font-weight: 600;
  }
  .low-val {
    color: var(--low);
    font-family: 'Barlow Condensed', sans-serif;
    font-size: 16px;
    font-weight: 700;
  }
  .dash { color: var(--border); font-size: 12px; }
  .high-val {
    color: var(--high);
    font-family: 'Barlow Condensed', sans-serif;
    font-size: 16px;
    font-weight: 700;
  }

  /* ─── INLINE BAR ─── */
  .bar-wrap { flex: 1; height: 4px; background: rgba(255,255,255,0.08); border-radius: 2px; max-width: 80px; position: relative; overflow: hidden; }
  .bar-fill { height: 100%; background: linear-gradient(90deg, var(--low), var(--high)); border-radius: 2px; }

  /* ─── CONTEXT CALLOUT ─── */
  .callout {
    background: rgba(244,185,66,0.06);
    border: 1px solid rgba(244,185,66,0.18);
    border-radius: 8px;
    padding: 12px 14px;
    font-size: 13px;
    line-height: 1.55;
    color: rgba(232,234,240,0.85);
  }
  .callout strong { color: var(--accent-gold); }

  /* ─── FORM MATCH DETAIL ─── */
  .match-list { display: flex; flex-direction: column; gap: 6px; }
  .match-row {
    display: flex;
    align-items: center;
    gap: 8px;
    background: var(--bg-3);
    border-radius: 6px;
    padding: 8px 10px;
    font-size: 12px;
  }
  .match-row .score {
    font-family: 'Barlow Condensed', sans-serif;
    font-size: 15px;
    font-weight: 700;
    color: #fff;
    min-width: 42px;
    text-align: center;
  }
  .match-row .opponent { flex: 1; color: var(--text); font-size: 12px; }
  .match-row .comp { font-size: 10px; color: var(--muted); text-transform: uppercase; letter-spacing: 0.5px; }
  .match-row .result-dot {
    width: 8px; height: 8px; border-radius: 50%; flex-shrink: 0;
  }
  .result-dot.W { background: var(--low); }
  .result-dot.D { background: var(--accent-gold); }
  .result-dot.L { background: var(--high); }

  /* ─── LEGEND ─── */
  .legend {
    display: flex;
    gap: 16px;
    flex-wrap: wrap;
    margin-top: 4px;
  }
  .legend-item { display: flex; align-items: center; gap: 5px; font-size: 11px; color: var(--muted); }
  .legend-dot { width: 8px; height: 8px; border-radius: 50%; }

  /* ─── DIVIDER ─── */
  .divider {
    height: 1px;
    background: var(--border);
    margin: 0 20px;
  }

  /* ─── FOOTER ─── */
  footer {
    text-align: center;
    padding: 20px 16px;
    font-size: 11px;
    color: rgba(136,145,164,0.5);
    border-top: 1px solid var(--border);
  }

  /* ─── SEASON AVG ─── */
  .avg-grid {
    display: grid;
    grid-template-columns: 1fr 1fr 1fr;
    gap: 8px;
  }
  .avg-item {
    background: var(--bg-3);
    border: 1px solid var(--border);
    border-radius: 8px;
    padding: 10px 12px;
    text-align: center;
  }
  .avg-item .avg-val {
    font-family: 'Barlow Condensed', sans-serif;
    font-size: 22px;
    font-weight: 800;
    color: #fff;
    line-height: 1;
  }
  .avg-item .avg-lbl {
    font-size: 10px;
    color: var(--muted);
    margin-top: 3px;
    text-transform: uppercase;
    letter-spacing: 0.5px;
    line-height: 1.3;
  }

  .pill-label {
    display: inline-block;
    font-size: 10px;
    font-family: 'Barlow Condensed', sans-serif;
    font-weight: 700;
    letter-spacing: 0.8px;
    text-transform: uppercase;
    padding: 2px 7px;
    border-radius: 3px;
    margin-bottom: 6px;
  }
  .pill-chelsea { background: rgba(0,180,216,0.15); color: var(--chelsea-a); border: 1px solid rgba(0,180,216,0.3); }
  .pill-arsenal { background: rgba(230,57,70,0.15); color: #f06672; border: 1px solid rgba(230,57,70,0.3); }

  @media (min-width: 480px) {
    .site-header h1 { font-size: 26px; }
    .avg-grid { grid-template-columns: repeat(4, 1fr); }
    .mini-stats { grid-template-columns: repeat(3, 1fr); }
  }
</style>
</head>
<body>

<header class="site-header">
  <div class="competition-tag">FA Cup · Quarter-Finals · 4 April 2026</div>
  <h1>Team Bilbo Match Predictor</h1>
  <p class="sub">Last 5 form · Season averages · H2H · Predicted ranges</p>
</header>

<div class="page">

  <!-- ════════════════════════════════════════ -->
  <!--  MATCH 1: CHELSEA VS PORT VALE          -->
  <!-- ════════════════════════════════════════ -->
  <div class="match-block">
    <div class="match-title-bar chelsea">
      <div>
        <h2>Chelsea&nbsp;&nbsp;vs&nbsp;&nbsp;Port Vale</h2>
        <div class="meta">Stamford Bridge · 5:15pm BST</div>
      </div>
      <div class="badge">QF · Match 1</div>
    </div>

    <div class="match-body">

      <!-- CONTEXT -->
      <div class="section">
        <div class="section-label">Match Context</div>
        <div class="callout">
          A <strong>David vs Goliath</strong> cup tie — Chelsea's first meeting with Port Vale in almost a century. Chelsea are the Club World Cup champions but arrive in alarming Premier League form, losing 4 consecutive matches and failing to score in 3 straight league games. Port Vale sit <strong>14 points adrift of League One safety</strong> but are the FA Cup's great romantics, knocking out Bristol City and top-flight Sunderland. Enzo Fernández is suspended; Jorgensen, Colwill, James, Chalobah and Mudryk are out.
        </div>
      </div>

      <!-- TEAM FORMS -->
      <div class="section">
        <div class="section-label">Last 5 Matches</div>

        <!-- CHELSEA FORM -->
        <div style="margin-bottom:14px;">
          <div class="pill-label pill-chelsea">Chelsea (PL · 7th)</div>
          <div class="match-list">
            <div class="match-row"><div class="result-dot L"></div><div class="score">0–3</div><div class="opponent">Everton</div><div class="comp">PL · Away</div></div>
            <div class="match-row"><div class="result-dot L"></div><div class="score">0–3</div><div class="opponent">PSG</div><div class="comp">UCL · Home</div></div>
            <div class="match-row"><div class="result-dot L"></div><div class="score">0–1</div><div class="opponent">Newcastle Utd</div><div class="comp">PL · Home</div></div>
            <div class="match-row"><div class="result-dot L"></div><div class="score">2–5</div><div class="opponent">PSG</div><div class="comp">UCL · Away</div></div>
            <div class="match-row"><div class="result-dot W"></div><div class="score">4–2</div><div class="opponent">Wrexham</div><div class="comp">FAC · Away</div></div>
          </div>
          <div class="legend" style="margin-top:8px;">
            <div class="legend-item"><div class="legend-dot W"></div>Win</div>
            <div class="legend-item"><div class="legend-dot D"></div>Draw</div>
            <div class="legend-item"><div class="legend-dot L"></div>Loss</div>
          </div>
        </div>

        <!-- PORT VALE FORM -->
        <div>
          <div class="pill-label pill-chelsea">Port Vale (L1 · 24th)</div>
          <div class="match-list">
            <div class="match-row"><div class="result-dot L"></div><div class="score">0–4</div><div class="opponent">Wycombe</div><div class="comp">L1 · Home</div></div>
            <div class="match-row"><div class="result-dot W"></div><div class="score">1–0</div><div class="opponent">Sunderland</div><div class="comp">FAC · Home</div></div>
            <div class="match-row"><div class="result-dot D"></div><div class="score">0–0</div><div class="opponent">Leyton Orient</div><div class="comp">L1 · Away</div></div>
            <div class="match-row"><div class="result-dot D"></div><div class="score">0–0</div><div class="opponent">Stevenage</div><div class="comp">L1 · Home</div></div>
            <div class="match-row"><div class="result-dot W"></div><div class="score">1–0</div><div class="opponent">Bristol City</div><div class="comp">FAC · Away</div></div>
          </div>
        </div>
      </div>

      <!-- SEASON AVERAGES -->
      <div class="section">
        <div class="section-label">Season Averages (per match)</div>
        <div style="margin-bottom:10px">
          <div class="pill-label pill-chelsea" style="margin-bottom:8px">Chelsea — Premier League</div>
          <div class="avg-grid">
            <div class="avg-item"><div class="avg-val">13.7</div><div class="avg-lbl">Shots</div></div>
            <div class="avg-item"><div class="avg-val">4.7</div><div class="avg-lbl">SOT</div></div>
            <div class="avg-item"><div class="avg-val">5.1</div><div class="avg-lbl">Corners</div></div>
            <div class="avg-item"><div class="avg-val">10.3</div><div class="avg-lbl">Fouls</div></div>
          </div>
        </div>
        <div>
          <div class="pill-label pill-chelsea" style="margin-bottom:8px">Port Vale — League One</div>
          <div class="avg-grid">
            <div class="avg-item"><div class="avg-val">11.6</div><div class="avg-lbl">Shots</div></div>
            <div class="avg-item"><div class="avg-val">3.2</div><div class="avg-lbl">SOT</div></div>
            <div class="avg-item"><div class="avg-val">3.8</div><div class="avg-lbl">Corners</div></div>
            <div class="avg-item"><div class="avg-val">12.4</div><div class="avg-lbl">Fouls</div></div>
          </div>
        </div>
      </div>

      <!-- H2H -->
      <div class="section">
        <div class="section-label">Head-to-Head Record</div>
        <div class="h2h-banner">
          <div class="h2h-stat">
            <div class="val" style="color:var(--chelsea-a)">14</div>
            <div class="lbl">Chelsea Wins</div>
          </div>
          <div class="h2h-divider"></div>
          <div class="h2h-stat">
            <div class="val" style="color:var(--accent-gold)">3</div>
            <div class="lbl">Draws</div>
          </div>
          <div class="h2h-divider"></div>
          <div class="h2h-stat">
            <div class="val" style="color:var(--high)">3</div>
            <div class="lbl">Vale Wins</div>
          </div>
          <div class="h2h-divider"></div>
          <div class="h2h-stat">
            <div class="val">97</div>
            <div class="lbl">Yrs Since</div>
          </div>
        </div>
        <p style="font-size:11px;color:var(--muted);margin-top:8px;">All 20 meetings were Div Two league matches between 1905–1929. No FA Cup meetings ever. Last meeting: Port Vale 1–0 Chelsea, April 1929.</p>
      </div>

      <!-- PREDICTIONS -->
      <div class="section">
        <div class="section-label">📊 Predicted Ranges — Both Teams Combined</div>
        <div style="margin-bottom:10px;">
          <div class="legend" style="gap:18px">
            <div class="legend-item"><div class="legend-dot" style="background:var(--low)"></div><span style="color:var(--low);font-weight:600">Low</span>&nbsp;= minimum expected</div>
            <div class="legend-item"><div class="legend-dot" style="background:var(--high)"></div><span style="color:var(--high);font-weight:600">High</span>&nbsp;= maximum expected</div>
          </div>
        </div>
        <table class="pred-table">
          <thead>
            <tr>
              <th>Metric</th>
              <th>Low</th>
              <th></th>
              <th>High</th>
              <th>Range</th>
            </tr>
          </thead>
          <tbody>
            <tr>
              <td>Corners</td>
              <td><span class="low-val">9</span></td>
              <td><span class="dash">—</span></td>
              <td><span class="high-val">13</span></td>
              <td><div class="bar-wrap"><div class="bar-fill" style="width:65%"></div></div></td>
            </tr>
            <tr>
              <td>Total Shots</td>
              <td><span class="low-val">21</span></td>
              <td><span class="dash">—</span></td>
              <td><span class="high-val">30</span></td>
              <td><div class="bar-wrap"><div class="bar-fill" style="width:72%"></div></div></td>
            </tr>
            <tr>
              <td>Shots on Target</td>
              <td><span class="low-val">6</span></td>
              <td><span class="dash">—</span></td>
              <td><span class="high-val">11</span></td>
              <td><div class="bar-wrap"><div class="bar-fill" style="width:55%"></div></div></td>
            </tr>
            <tr>
              <td>Fouls</td>
              <td><span class="low-val">22</span></td>
              <td><span class="dash">—</span></td>
              <td><span class="high-val">32</span></td>
              <td><div class="bar-wrap"><div class="bar-fill" style="width:60%"></div></div></td>
            </tr>
            <tr>
              <td>Throw-ins</td>
              <td><span class="low-val">38</span></td>
              <td><span class="dash">—</span></td>
              <td><span class="high-val">54</span></td>
              <td><div class="bar-wrap"><div class="bar-fill" style="width:70%"></div></div></td>
            </tr>
            <tr>
              <td>Goal Kicks</td>
              <td><span class="low-val">14</span></td>
              <td><span class="dash">—</span></td>
              <td><span class="high-val">24</span></td>
              <td><div class="bar-wrap"><div class="bar-fill" style="width:58%"></div></div></td>
            </tr>
            <tr>
              <td>Tackles</td>
              <td><span class="low-val">30</span></td>
              <td><span class="dash">—</span></td>
              <td><span class="high-val">46</span></td>
              <td><div class="bar-wrap"><div class="bar-fill" style="width:65%"></div></div></td>
            </tr>
            <tr>
              <td>Offsides</td>
              <td><span class="low-val">3</span></td>
              <td><span class="dash">—</span></td>
              <td><span class="high-val">7</span></td>
              <td><div class="bar-wrap"><div class="bar-fill" style="width:40%"></div></div></td>
            </tr>
          </tbody>
        </table>
      </div>

      <!-- ANALYTICAL NOTES -->
      <div class="section">
        <div class="section-label">Analytical Notes</div>
        <div class="callout">
          <strong>Corners (9–13):</strong> Chelsea's possession-dominant style will generate 7–9 corners alone; Vale will earn very few (2–4) operating in a deep block. High end reflects Chelsea's attacking pressure not converting cleanly.<br><br>
          <strong>Shots (21–30):</strong> Chelsea expect ~18–22 shots; Port Vale's pragmatic Cup football will limit them to ~4–8. Low end if Port Vale defend exceptionally deep. Impactful given Chelsea's shocking 0 goals in 3 PL games — the attack may misfire again.<br><br>
          <strong>Fouls (22–32):</strong> Port Vale will commit the majority (12–18 fouls) breaking up Chelsea attacks as League One physicality meets Premier League pace. High end if referee allows robust challenges.<br><br>
          <strong>Throw-ins (38–54):</strong> Port Vale clearing high balls into wide areas creates throw-ins. High end likely due to Vale's counter-pressing disruptions in wide zones.<br><br>
          <strong>Goal Kicks (14–24):</strong> Port Vale GK will frequently restart with long balls; Chelsea's GK will benefit from Vale sitting very deep with few shots at goal.<br><br>
          <strong>Tackles (30–46):</strong> Vale's defensive solidity (clean sheet vs Sunderland) suggests a tackle-heavy game. High end if Vale's discipline holds under pressure.<br><br>
          <strong>Offsides (3–7):</strong> Chelsea will push attackers in behind but Vale's defensive line management is cautious. Low end probable given Vale's very deep shape.
        </div>
      </div>

    </div>
  </div>

  <!-- ════════════════════════════════════════ -->
  <!--  MATCH 2: SOUTHAMPTON VS ARSENAL        -->
  <!-- ════════════════════════════════════════ -->
  <div class="match-block">
    <div class="match-title-bar arsenal">
      <div>
        <h2>Southampton&nbsp;&nbsp;vs&nbsp;&nbsp;Arsenal</h2>
        <div class="meta">St Mary's · 8:00pm BST</div>
      </div>
      <div class="badge">QF · Match 2</div>
    </div>

    <div class="match-body">

      <!-- CONTEXT -->
      <div class="section">
        <div class="section-label">Match Context</div>
        <div class="callout">
          A much tighter affair. <strong>Southampton (Championship) are unbeaten in 14 games</strong> and upset Premier League Fulham in Round 5. Arsenal lead the Premier League by 9 points but are licking wounds from a <strong>Carabao Cup final defeat to Man City</strong>. Arsenal's squad is heavily depleted: Eze, Madueke, Timber, Merino all out; Odegaard and Havertz fitness doubts. Arteta likely to rotate. Southampton's Downes and Matsuki are suspended.
        </div>
      </div>

      <!-- FORM -->
      <div class="section">
        <div class="section-label">Last 5 Matches</div>

        <!-- SOUTHAMPTON -->
        <div style="margin-bottom:14px;">
          <div class="pill-label pill-arsenal">Southampton (Champ · 6th)</div>
          <div class="match-list">
            <div class="match-row"><div class="result-dot W"></div><div class="score">2–0</div><div class="opponent">Oxford United</div><div class="comp">Champ · Home</div></div>
            <div class="match-row"><div class="result-dot W"></div><div class="score">1–0</div><div class="opponent">Norwich City</div><div class="comp">Champ · Away</div></div>
            <div class="match-row"><div class="result-dot W"></div><div class="score">2–0</div><div class="opponent">Coventry City</div><div class="comp">Champ · Home</div></div>
            <div class="match-row"><div class="result-dot D"></div><div class="score">1–1</div><div class="opponent">West Brom</div><div class="comp">Champ · Away</div></div>
            <div class="match-row"><div class="result-dot W"></div><div class="score">1–0</div><div class="opponent">Fulham</div><div class="comp">FAC · Away</div></div>
          </div>
        </div>

        <!-- ARSENAL -->
        <div>
          <div class="pill-label pill-arsenal">Arsenal (PL · 1st)</div>
          <div class="match-list">
            <div class="match-row"><div class="result-dot L"></div><div class="score">0–2</div><div class="opponent">Manchester City</div><div class="comp">EFL Final · Wembley</div></div>
            <div class="match-row"><div class="result-dot W"></div><div class="score">2–0</div><div class="opponent">Mansfield Town</div><div class="comp">FAC · Away</div></div>
            <div class="match-row"><div class="result-dot W"></div><div class="score">4–0</div><div class="opponent">Wigan Athletic</div><div class="comp">FAC · Home</div></div>
            <div class="match-row"><div class="result-dot W"></div><div class="score">2–1</div><div class="opponent">Chelsea</div><div class="comp">PL · Home</div></div>
            <div class="match-row"><div class="result-dot W"></div><div class="score">3–0</div><div class="opponent">Crystal Palace</div><div class="comp">PL · Away</div></div>
          </div>
        </div>
      </div>

      <!-- SEASON AVERAGES -->
      <div class="section">
        <div class="section-label">Season Averages (per match)</div>
        <div style="margin-bottom:10px">
          <div class="pill-label pill-arsenal" style="margin-bottom:8px">Southampton — Championship</div>
          <div class="avg-grid">
            <div class="avg-item"><div class="avg-val">14.3</div><div class="avg-lbl">Shots</div></div>
            <div class="avg-item"><div class="avg-val">5.3</div><div class="avg-lbl">SOT</div></div>
            <div class="avg-item"><div class="avg-val">4.8</div><div class="avg-lbl">Corners</div></div>
            <div class="avg-item"><div class="avg-val">11.2</div><div class="avg-lbl">Fouls</div></div>
          </div>
        </div>
        <div>
          <div class="pill-label pill-arsenal" style="margin-bottom:8px">Arsenal — Premier League</div>
          <div class="avg-grid">
            <div class="avg-item"><div class="avg-val">14.7</div><div class="avg-lbl">Shots</div></div>
            <div class="avg-item"><div class="avg-val">5.0</div><div class="avg-lbl">SOT</div></div>
            <div class="avg-item"><div class="avg-val">5.8</div><div class="avg-lbl">Corners</div></div>
            <div class="avg-item"><div class="avg-val">9.8</div><div class="avg-lbl">Fouls</div></div>
          </div>
        </div>
      </div>

      <!-- H2H -->
      <div class="section">
        <div class="section-label">Head-to-Head (Recent)</div>
        <div class="h2h-banner">
          <div class="h2h-stat">
            <div class="val" style="color:var(--arsenal-a)">9</div>
            <div class="lbl">Arsenal Wins</div>
          </div>
          <div class="h2h-divider"></div>
          <div class="h2h-stat">
            <div class="val" style="color:var(--accent-gold)">4</div>
            <div class="lbl">Draws</div>
          </div>
          <div class="h2h-divider"></div>
          <div class="h2h-stat">
            <div class="val" style="color:var(--low)">4</div>
            <div class="lbl">Saints Wins</div>
          </div>
          <div class="h2h-divider"></div>
          <div class="h2h-stat">
            <div class="val">78.3%</div>
            <div class="lbl">Arsenal Win%</div>
          </div>
        </div>
        <p style="font-size:11px;color:var(--muted);margin-top:8px;">Last 17 meetings: Arsenal have not lost to Southampton since 2021. At St Mary's: 2 wins each + 1 draw in last 5 meetings. Arsenal won here 2–1 on the final day of 2024–25.</p>
      </div>

      <!-- PREDICTIONS -->
      <div class="section">
        <div class="section-label">📊 Predicted Ranges — Both Teams Combined</div>
        <div style="margin-bottom:10px;">
          <div class="legend" style="gap:18px">
            <div class="legend-item"><div class="legend-dot" style="background:var(--low)"></div><span style="color:var(--low);font-weight:600">Low</span>&nbsp;= minimum expected</div>
            <div class="legend-item"><div class="legend-dot" style="background:var(--high)"></div><span style="color:var(--high);font-weight:600">High</span>&nbsp;= maximum expected</div>
          </div>
        </div>
        <table class="pred-table">
          <thead>
            <tr>
              <th>Metric</th>
              <th>Low</th>
              <th></th>
              <th>High</th>
              <th>Range</th>
            </tr>
          </thead>
          <tbody>
            <tr>
              <td>Corners</td>
              <td><span class="low-val">8</span></td>
              <td><span class="dash">—</span></td>
              <td><span class="high-val">13</span></td>
              <td><div class="bar-wrap"><div class="bar-fill" style="width:60%"></div></div></td>
            </tr>
            <tr>
              <td>Total Shots</td>
              <td><span class="low-val">22</span></td>
              <td><span class="dash">—</span></td>
              <td><span class="high-val">34</span></td>
              <td><div class="bar-wrap"><div class="bar-fill" style="width:78%"></div></div></td>
            </tr>
            <tr>
              <td>Shots on Target</td>
              <td><span class="low-val">7</span></td>
              <td><span class="dash">—</span></td>
              <td><span class="high-val">13</span></td>
              <td><div class="bar-wrap"><div class="bar-fill" style="width:62%"></div></div></td>
            </tr>
            <tr>
              <td>Fouls</td>
              <td><span class="low-val">18</span></td>
              <td><span class="dash">—</span></td>
              <td><span class="high-val">28</span></td>
              <td><div class="bar-wrap"><div class="bar-fill" style="width:55%"></div></div></td>
            </tr>
            <tr>
              <td>Throw-ins</td>
              <td><span class="low-val">34</span></td>
              <td><span class="dash">—</span></td>
              <td><span class="high-val">50</span></td>
              <td><div class="bar-wrap"><div class="bar-fill" style="width:65%"></div></div></td>
            </tr>
            <tr>
              <td>Goal Kicks</td>
              <td><span class="low-val">16</span></td>
              <td><span class="dash">—</span></td>
              <td><span class="high-val">26</span></td>
              <td><div class="bar-wrap"><div class="bar-fill" style="width:60%"></div></div></td>
            </tr>
            <tr>
              <td>Tackles</td>
              <td><span class="low-val">28</span></td>
              <td><span class="dash">—</span></td>
              <td><span class="high-val">44</span></td>
              <td><div class="bar-wrap"><div class="bar-fill" style="width:62%"></div></div></td>
            </tr>
            <tr>
              <td>Offsides</td>
              <td><span class="low-val">3</span></td>
              <td><span class="dash">—</span></td>
              <td><span class="high-val">8</span></td>
              <td><div class="bar-wrap"><div class="bar-fill" style="width:50%"></div></div></td>
            </tr>
          </tbody>
        </table>
      </div>

      <!-- ANALYTICAL NOTES -->
      <div class="section">
        <div class="section-label">Analytical Notes</div>
        <div class="callout">
          <strong>Corners (8–13):</strong> Two technically strong teams will generate corners at a high rate. Arsenal earn ~5.8 per game in the PL; Southampton ~4.8 in the Championship. At St Mary's, Southampton avg 10.7 corners per match as host. High end reflects both teams pressing hard in a knockout tie.<br><br>
          <strong>Shots (22–34):</strong> Both sides are among the top shot-takers in their respective divisions. Southampton's 14-game unbeaten run includes high output at home. A competitive cup tie with both managers valuing FA Cup means neither will park the bus. High end if the game opens up in extra time.<br><br>
          <strong>Fouls (18–28):</strong> Arsenal play through tight spaces; Southampton's energetic midfield will disrupt with fouls. Lower end if the referee allows the game to flow; high end with a physical battle at St Mary's.<br><br>
          <strong>Throw-ins (34–50):</strong> Both teams press wide areas. Southampton's hard-working wide players (Fellows, Edozie) and Arsenal's full-back overlaps create frequent boundary breaks. High end if the game is end-to-end with many transitions.<br><br>
          <strong>Goal Kicks (16–26):</strong> Arsenal's high press means Southampton's keeper will launch long balls. Arsenal's makeshift defence (Mosquera, Salmon) may concede ground; both keepers will be active.<br><br>
          <strong>Tackles (28–44):</strong> Southampton's pressing system relies heavily on intense tackling. Arsenal without Merino and potentially Rice means more midfield exposure. High end if Arsenal rotate heavily and Southampton press aggressively throughout.<br><br>
          <strong>Offsides (3–8):</strong> Arsenal's high defensive line and Southampton's pacey runners (Stewart, Larin) create offside traps in both directions. Higher end than the Chelsea match given both teams' attacking intent.
        </div>
      </div>

    </div>
  </div>

  <!-- COMPARISON SUMMARY -->
  <div style="background:var(--bg-2);border:1px solid var(--border);border-radius:10px;overflow:hidden;margin-bottom:20px;">
    <div style="padding:16px 20px;background:linear-gradient(135deg,#1a1f2e,#222836);border-bottom:1px solid var(--border);">
      <div style="font-family:'Barlow Condensed',sans-serif;font-size:18px;font-weight:800;text-transform:uppercase;letter-spacing:0.3px;color:#fff;">Match Comparison Summary</div>
      <div style="font-size:12px;color:var(--muted);margin-top:2px;">Chelsea v PV vs Southampton v Arsenal</div>
    </div>
    <div style="padding:18px 20px;">
      <table class="pred-table">
        <thead>
          <tr>
            <th>Metric</th>
            <th style="color:var(--chelsea-a)">CHE vs PV</th>
            <th style="color:var(--arsenal-a)">SOU vs ARS</th>
          </tr>
        </thead>
        <tbody>
          <tr><td>Corners</td><td style="text-align:center;color:var(--text)">9–13</td><td style="text-align:center;color:var(--text)">8–13</td></tr>
          <tr><td>Total Shots</td><td style="text-align:center;color:var(--text)">21–30</td><td style="text-align:center;color:var(--text)">22–34</td></tr>
          <tr><td>Shots on Target</td><td style="text-align:center;color:var(--text)">6–11</td><td style="text-align:center;color:var(--text)">7–13</td></tr>
          <tr><td>Fouls</td><td style="text-align:center;color:var(--text)">22–32</td><td style="text-align:center;color:var(--text)">18–28</td></tr>
          <tr><td>Throw-ins</td><td style="text-align:center;color:var(--text)">38–54</td><td style="text-align:center;color:var(--text)">34–50</td></tr>
          <tr><td>Goal Kicks</td><td style="text-align:center;color:var(--text)">14–24</td><td style="text-align:center;color:var(--text)">16–26</td></tr>
          <tr><td>Tackles</td><td style="text-align:center;color:var(--text)">30–46</td><td style="text-align:center;color:var(--text)">28–44</td></tr>
          <tr><td>Offsides</td><td style="text-align:center;color:var(--text)">3–7</td><td style="text-align:center;color:var(--text)">3–8</td></tr>
        </tbody>
      </table>
      <div class="callout" style="margin-top:14px;">
        The <strong>Southampton v Arsenal</strong> tie is projected to produce more shots and a higher attacking output — both teams are in better goalscoring form and the match is far more evenly contested. <strong>Chelsea v Port Vale</strong> will likely see more fouls and throw-ins as the League One visitors disrupt Chelsea's rhythm with a rugged low block. Port Vale's extraordinary cup runs always carry a defensive structure that makes them awkward opponents.
      </div>
    </div>
  </div>

</div>

<footer>
  <strong>Team Bilbo Statistical Analysis</strong><br>Data sourced from FootyStats, WhoScored, Opta Analyst, Chelsea FC, Arsenal FC & Southampton FC official sites · <strong>Predictions are statistical estimates</strong> based on available data and contextual factors · April 4, 2026.
</footer>

</body>
</html>
