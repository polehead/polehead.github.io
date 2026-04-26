<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta
      name="viewport"
      content="width=device-width, initial-scale=1.0, maximum-scale=5.0, minimum-scale=1.0" />
    <title>PL, UCL, UEL & FA Cup Predictions – 24 Apr–3 May 2026</title>
    <meta
      name="description"
      content="Data-driven Premier League, Champions League, Europa League & FA Cup predictions for 24 April–3 May 2026 with referee analysis" />
    <link
      href="https://fonts.googleapis.com/css2?family=Inter:wght@300;400;500;600;700;800;900&display=swap"
      rel="stylesheet" />
    <style>
      *,
      *::before,
      *::after {
        margin: 0;
        padding: 0;
        box-sizing: border-box;
      }

      html {
        overflow-x: hidden;
        max-width: 100vw;
        scroll-behavior: smooth;
        -webkit-text-size-adjust: 100%;
        -ms-text-size-adjust: 100%;
      }

      :root {
        --bg: #0a0e1a;
        --card: #111827;
        --card2: #1a2236;
        --text: #e2e8f0;
        --dim: #94a3b8;
        --accent: #6366f1;
        --glow: rgba(99, 102, 241, 0.15);
        --pl-green: #00ff85;
        --muted: #64748b;
      }

      body {
        font-family: 'Sora', sans-serif;
        background: var(--bg);
        color: var(--text);
        font-size: 14px;
        line-height: 1.55;
        -webkit-font-smoothing: antialiased;
        overflow-x: hidden; /* Prevent horizontal jitter */
      }

      .hero {
        text-align: center;
        padding: 40px 20px 20px;
        background: linear-gradient(
          135deg,
          #0f172a 0%,
          #1e1b4b 50%,
          #0f172a 100%
        );
        border-bottom: 1px solid rgba(99, 102, 241, 0.2);
      }

      .hero h1 {
        font-size: clamp(1.4rem, 4vw, 2.2rem);
        font-weight: 800;
        background: linear-gradient(135deg, #818cf8, #c084fc, #f472b6);
        -webkit-background-clip: text;
        -webkit-text-fill-color: transparent;
        margin-bottom: 6px;
      }

      .hero p {
        color: var(--dim);
        font-size: 0.85rem;
      }

      .hero .badge {
        display: inline-block;
        background: transparent;
        color: #818cf8;
        padding: 4px 12px;
        border-radius: 20px;
        font-size: 0.7rem;
        font-weight: 600;
        margin-top: 8px;
        letter-spacing: 0.5px;
      }

      /* ─── PAGE HEADER ─── */
      .page-hd {
        background: linear-gradient(
          150deg,
          #050820 0%,
          #070022 55%,
          #050820 100%
        );
        border-bottom: 2px solid rgba(55, 0, 60, 0.8);
        padding: 20px 20px 16px;
        text-align: center;
        position: relative;
        overflow: hidden;
      }

      .page-hd::before {
        content: '';
        position: absolute;
        inset: 0;
        background: radial-gradient(
          ellipse 110% 60% at 50% -10%,
          rgba(0, 255, 133, 0.07),
          transparent 65%
        );
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
        background: rgba(0, 255, 133, 0.08);
        border: 1px solid rgba(0, 255, 133, 0.25);
        padding: 4px 14px;
        border-radius: 20px;
        margin-bottom: 10px;
        position: relative;
      }

      .page-hd h1 {
        font-family: 'Exo 2', sans-serif;
        font-size: clamp(22px, 4.5vw, 40px);
        font-weight: 900;
        letter-spacing: 0.5px;
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
      h2 img {
        width: 100%;
        height: auto;
      }

      .container {
        max-width: 1200px;
        margin: 0 auto;
        padding: 20px 16px;
        width: 100%;
        overflow-x: hidden;
      }

      .match-card {
        background: var(--card);
        border-radius: 16px;
        margin-bottom: 28px;
        overflow: hidden;
        border: 1px solid rgba(255, 255, 255, 0.06);
        box-shadow: 0 4px 24px rgba(0, 0, 0, 0.3);
        max-width: 100%;
      }

      .match-header {
        display: flex;
        align-items: center;
        justify-content: center;
        gap: 12px;
        padding: 20px;
        position: relative;
        overflow: hidden;
      }

      .match-header::before {
        content: '';
        position: absolute;
        inset: 0;
        opacity: 0.12;
      }

      .team-info {
        display: flex;
        flex-direction: column;
        align-items: center;
        gap: 6px;
        flex: 1;
        max-width: 180px;
      }

      .team-info img {
        width: 52px;
        height: 52px;
        object-fit: contain;
        filter: drop-shadow(0 2px 8px rgba(0, 0, 0, 0.3));
      }

      .team-info .name {
        font-weight: 700;
        font-size: 0.85rem;
        text-align: center;
        text-transform: uppercase;
      }

      .team-info .pos {
        font-size: 0.65rem;
        color: var(--dim);
      }

      .vs {
        font-weight: 800;
        font-size: 1.1rem;
        color: #6366f1;
        text-shadow: 0 0 20px rgba(99, 102, 241, 0.4);
      }

      .match-meta {
        display: flex;
        justify-content: center;
        gap: 16px;
        padding: 0 20px 12px;
        flex-wrap: wrap;
      }

      .match-meta span {
        font-size: 0.65rem;
        color: var(--dim);
        display: flex;
        align-items: center;
        gap: 4px;
      }

      .tabs {
        display: flex;
        gap: 4px;
        padding: 0 12px;
        overflow-x: auto;
        -webkit-overflow-scrolling: touch;
        scrollbar-width: none;
      }

      .tabs::-webkit-scrollbar {
        display: none;
      }

      .tab {
        padding: 7px 14px;
        font-size: 0.7rem;
        font-weight: 600;
        border: none;
        background: transparent;
        color: var(--dim);
        cursor: pointer;
        border-radius: 8px 8px 0 0;
        white-space: nowrap;
        transition: 0.2s;
      }

      .tab.active {
        background: var(--card2);
        color: #818cf8;
      }

      .tab-content {
        display: none;
        padding: 16px;
        background: var(--card2);
        border-radius: 0 0 12px 12px;
        margin: 0 12px 12px;
      }

      .tab-content.active {
        display: block;
      }

      table {
        width: 100%;
        border-collapse: collapse;
        font-size: 0.72rem;
      }

      th {
        text-align: left;
        padding: 6px 8px;
        color: var(--dim);
        font-weight: 600;
        border-bottom: 1px solid rgba(255, 255, 255, 0.06);
        font-size: 0.65rem;
        text-transform: uppercase;
        letter-spacing: 0.5px;
        white-space: nowrap;
      }

      td {
        padding: 6px 8px;
        border-bottom: 1px solid rgba(255, 255, 255, 0.03);
        white-space: nowrap;
      }

      .bar-wrap {
        height: 6px;
        background: rgba(255, 255, 255, 0.06);
        border-radius: 3px;
        overflow: hidden;
        min-width: 60px;
      }

      .bar {
        height: 100%;
        border-radius: 3px;
        transition: width 1s ease;
      }

      .odds-grid {
        display: grid;
        grid-template-columns: repeat(3, 1fr);
        gap: 8px;
        margin: 8px 0;
      }

      .odds-box {
        text-align: center;
        padding: 10px 6px;
        background: rgba(255, 255, 255, 0.03);
        border-radius: 8px;
        border: 1px solid rgba(255, 255, 255, 0.05);
      }

      .odds-box .label {
        font-size: 0.6rem;
        color: var(--dim);
        margin-bottom: 4px;
      }

      .odds-box .val {
        font-size: 0.95rem;
        font-weight: 700;
        color: #818cf8;
      }

      .score-pred {
        display: flex;
        align-items: center;
        justify-content: center;
        gap: 16px;
        padding: 16px;
        margin: 8px 0;
        background: rgba(99, 102, 241, 0.06);
        border-radius: 10px;
        border: 1px solid rgba(99, 102, 241, 0.15);
      }

      .score-pred .sc {
        font-size: 1.8rem;
        font-weight: 800;
      }

      .score-pred .lbl {
        font-size: 0.6rem;
        color: var(--dim);
        text-transform: uppercase;
        letter-spacing: 1px;
      }

      .player-chip {
        display: inline-flex;
        align-items: center;
        gap: 4px;
        padding: 3px 10px;
        margin: 2px;
        background: rgba(255, 255, 255, 0.04);
        border-radius: 12px;
        font-size: 0.68rem;
        border: 1px solid rgba(255, 255, 255, 0.06);
      }

      .player-chip .pct {
        color: #fbbf24;
        font-weight: 600;
        font-size: 0.6rem;
      }

      .ref-card {
        display: flex;
        align-items: center;
        gap: 12px;
        padding: 12px;
        background: rgba(255, 255, 255, 0.03);
        border-radius: 10px;
        border: 1px solid rgba(255, 255, 255, 0.06);
        margin: 8px 0;
      }

      .ref-card .ref-icon {
        width: 40px;
        height: 40px;
        border-radius: 50%;
        background: linear-gradient(135deg, #6366f1, #8b5cf6);
        display: flex;
        align-items: center;
        justify-content: center;
        font-size: 1.1rem;
        flex-shrink: 0;
      }

      .ref-card .ref-info {
        flex: 1;
      }

      .ref-card .ref-name {
        font-weight: 700;
        font-size: 0.8rem;
        color: #e2e8f0;
      }

      .ref-card .ref-role {
        font-size: 0.6rem;
        color: var(--dim);
      }

      .ref-stats {
        display: grid;
        grid-template-columns: repeat(3, 1fr);
        gap: 6px;
        margin: 8px 0;
      }

      .ref-stat {
        text-align: center;
        padding: 8px 4px;
        background: rgba(255, 255, 255, 0.03);
        border-radius: 8px;
        border: 1px solid rgba(255, 255, 255, 0.05);
      }

      .ref-stat .rs-val {
        font-size: 1rem;
        font-weight: 800;
        color: #f472b6;
      }

      .ref-stat .rs-lbl {
        font-size: 0.55rem;
        color: var(--dim);
        text-transform: uppercase;
        letter-spacing: 0.5px;
      }

      .ref-impact {
        padding: 8px 10px;
        margin: 6px 0;
        background: rgba(244, 114, 182, 0.05);
        border-left: 3px solid #f472b6;
        border-radius: 0 8px 8px 0;
        font-size: 0.68rem;
        color: #f9a8d4;
      }

      .section-title {
        font-size: 0.75rem;
        font-weight: 700;
        color: #818cf8;
        margin: 12px 0 6px;
        text-transform: uppercase;
        letter-spacing: 0.5px;
      }

      .h2h-item {
        display: flex;
        justify-content: space-between;
        padding: 4px 0;
        font-size: 0.7rem;
        border-bottom: 1px solid rgba(255, 255, 255, 0.03);
      }

      .h2h-item .date {
        color: var(--dim);
      }

      .motivation {
        padding: 10px;
        margin: 8px 0;
        background: rgba(251, 191, 36, 0.05);
        border-left: 3px solid #fbbf24;
        border-radius: 0 8px 8px 0;
        font-size: 0.7rem;
        color: #fbbf24;
      }

      .form-dots {
        display: flex;
        gap: 3px;
        justify-content: center;
        margin: 4px 0;
      }

      .form-dot {
        width: 18px;
        height: 18px;
        border-radius: 4px;
        display: flex;
        align-items: center;
        justify-content: center;
        font-size: 0.55rem;
        font-weight: 700;
        color: #fff;
      }

      .form-dot.W {
        background: #22c55e;
      }

      .form-dot.D {
        background: #eab308;
      }

      .form-dot.L {
        background: #ef4444;
      }

      .stat-row {
        display: flex;
        align-items: center;
        gap: 8px;
        padding: 4px 0;
      }

      .stat-row .lbl {
        flex: 0 0 80px;
        font-size: 0.68rem;
        color: var(--dim);
        text-align: right;
      }

      .stat-row .vals {
        flex: 1;
        display: flex;
        align-items: center;
        gap: 6px;
      }

      .stat-row .v {
        font-size: 0.72rem;
        font-weight: 600;
        min-width: 28px;
        text-align: center;
      }

      .disclaimer {
        text-align: center;
        padding: 30px 20px;
        color: var(--dim);
        font-size: 0.65rem;
        border-top: 1px solid rgba(255, 255, 255, 0.05);
        margin-top: 20px;
      }

      /* ─── Scrollable table wrapper ─── */
      .table-scroll {
        overflow-x: auto;
        -webkit-overflow-scrolling: touch;
        margin: 0;
        padding: 0;
        max-width: 100%;
      }

      .table-scroll table {
        min-width: 480px;
      }

      /* ─── TABLET ─── */
      @media (max-width: 768px) {
        body {
          padding: 12px;
        }

        .container {
          padding: 12px 8px;
        }

        .match-header {
          gap: 10px;
          padding: 16px;
        }

        .team-info {
          max-width: 150px;
        }

        .team-info img {
          width: 46px;
          height: 46px;
        }
        .team-info .name {
          font-size: 0.8rem;
        }
        .team-info .name {
          font-size: 0.62rem;
        }

        .team-info .pos {
          font-size: 0.58rem;
        }
        .match-meta span {
          font-size: 0.6rem;
        }
        table {
          font-size: 0.7rem;
        }
        th {
          font-size: 0.7rem;
        }

        .tab-content {
          padding: 12px;
          margin: 0 8px 10px;
        }
      }

      /* ─── MOBILE ─── */
      @media (max-width: 480px) {
        body {
          padding: 6px;
        }

        .container {
          padding: 8px 4px;
        }
        h2 img {
          width: 100%;
          height: auto;
        }
        .page-hd {
          padding: 16px 12px 12px;
        }

        .page-hd h1 {
          font-size: clamp(18px, 5vw, 28px);
        }

        .match-card {
          margin-bottom: 20px;
          border-radius: 12px;
        }

        .match-header {
          flex-wrap: wrap;
          gap: 6px;
          padding: 12px 8px;
        }

        .team-info {
          max-width: 120px;
        }

        .team-info img {
          width: 36px;
          height: 36px;
        }

        .team-info .name {
          font-size: 0.62rem;
        }

        .team-info .pos {
          font-size: 0.58rem;
        }

        .vs {
          font-size: 0.8rem;
        }

        .match-meta {
          gap: 8px;
          padding: 0 10px 10px;
        }

        .match-meta span {
          font-size: 0.6rem;
        }

        .tabs {
          gap: 2px;
          padding: 0 6px;
        }

        .tab {
          padding: 6px 8px;
          font-size: 0.7rem;
        }

        .tab-content {
          padding: 8px;
          margin: 0 4px 6px;
        }

        table {
          font-size: 0.65rem;
        }

        th,
        td {
          padding: 2px 2px;
        }

        th {
          font-size: 0.55rem;
        }

        .odds-grid {
          gap: 4px;
        }

        .odds-box {
          padding: 8px 4px;
        }

        .odds-box .label {
          font-size: 0.55rem;
        }

        .odds-box .val {
          font-size: 0.82rem;
        }

        .score-pred {
          gap: 12px;
          padding: 12px 8px;
        }

        .score-pred .sc {
          font-size: 1.3rem;
        }

        .player-chip {
          padding: 3px 7px;
          font-size: 0.62rem;
        }

        .motivation {
          font-size: 0.65rem;
          padding: 8px;
        }

        .form-dot {
          width: 16px;
          height: 16px;
          font-size: 0.6rem;
        }

        .section-title {
          font-size: 0.68rem;
        }

        .h2h-item {
          font-size: 0.63rem;
        }

        .disclaimer {
          padding: 20px 12px;
          font-size: 0.6rem;
        }

        .hero {
          padding: 28px 12px 14px;
        }
      }

      /* ─── VERY SMALL DEVICES ─── */
      @media (max-width: 360px) {
        body {
          padding: 4px;
        }

        .team-info img {
          width: 30px;
          height: 30px;
        }

        .team-info .name {
          font-size: 0.65rem;
        }

        .tab {
          padding: 5px 6px;
          font-size: 0.55rem;
        }

        .tab-content {
          padding: 6px;
          margin: 0 2px 4px;
        }

        table {
          font-size: 0.58rem;
        }

        th,
        td {
          padding: 3px 3px;
        }

        .score-pred .sc {
          font-size: 1.1rem;
        }
      }
    </style>
  </head>

  <body>
    <header class="page-hd">
      <div class="pl-badge">Team Bilbo Analytics</div>
      <h2>Premier League, UCL &amp; UEL Predictions</h2>
      <p class="sub">
        Fixture Analysis &amp; Predictive Modeling · 24 April–3 May 2026
      </p>
    </header>
    <div class="container" id="app"></div>
    <div
      class="disclaimer"
      style="
        text-align: center;
        padding: 20px 16px;
        font-size: 10px;
        color: var(--dim);
        border-top: 1px solid var(--accent);
        position: relative;
        z-index: 1;
      ">
      <p><strong>Professional Strategy Analytics</strong><br /></p>
      <p style="margin-top: 4px">
        Statistical predictions are weighted estimates based on historical data
        and form analysis.<br /><br />
        <strong style="color: #ce4a5b"
          >ALWAYS GAMBLE RESPONSIBLY, THIS IS NOT FINANCIAL ADVICE</strong
        >
      </p>
    </div>

    <script>
      const M = [
        {
          home: {
            name: 'Man Utd',
            short: 'MUN',
            pos: '3rd (58pts)',
            badge:
              'https://static.files.bbci.co.uk/core/website/assets/static/sport/football/manchester-united.80807495b5.svg',
            color: '#DA291C',
            color2: '#FBE122',
            form: ['W', 'L', 'D', 'W', 'L'],
            xg: 1.58,
            xga: 1.22,
            cornPG: 6.0,
            shotsPG: 14.2,
            sotPG: 4.8,
            foulsPG: 10.6,
            throwsPG: 20.2,
            gkPG: 4.4,
            tacklePG: 17.0,
            offsidePG: 1.56,
            injuries: [
              'L. Mart\u00ednez (suspended)',
              'M. de Ligt (back, season)',
              'P. Dorgu (hamstring)',
              'M. Mount (muscle)',
              'L. Yoro (knock, doubtful)',
            ],
            cardPlayers: [
              { n: 'M. Ugarte', c: 9, pct: '46%' },
              { n: 'K. Mainoo', c: 6, pct: '34%' },
              { n: 'D. Dalot', c: 5, pct: '30%' },
              { n: 'H. Maguire', c: 5, pct: '28%' },
            ],
          },
          away: {
            name: 'Brentford',
            short: 'BRE',
            pos: '9th (48pts)',
            badge:
              'https://static.files.bbci.co.uk/core/website/assets/static/sport/football/brentford.aa0256ca6b.svg',
            color: '#e30613',
            color2: '#FFB81C',
            form: ['D', 'D', 'D', 'D', 'D'],
            xg: 1.18,
            xga: 1.24,
            cornPG: 4.82,
            shotsPG: 10.6,
            sotPG: 3.4,
            foulsPG: 10.4,
            throwsPG: 19.8,
            gkPG: 5.2,
            tacklePG: 17.4,
            offsidePG: 1.44,
            injuries: [
              'F. Carvalho (ACL, season)',
              'A. Milambo (ACL, season)',
              'J. Dasilva (knee)',
              'K. Furo (groin)',
              'J. Henderson (fitness)',
              'V. Janelt (fitness)',
              'R. Henry (fitness)',
            ],
            cardPlayers: [
              { n: 'C. N\u00f8rgaard', c: 7, pct: '40%' },
              { n: 'Y. Wissa', c: 5, pct: '32%' },
              { n: 'M. Damsgaard', c: 5, pct: '30%' },
              { n: 'V. Jorgensen', c: 4, pct: '26%' },
            ],
          },
          ko: '20:00',
          venue: 'Old Trafford',
          matchday: 'Matchday 34 \u00b7 Mon 27 Apr',
          referee: {
            name: 'Tony Harrington',
            games: 22,
            ycPG: 3.82,
            foulsPG: 20.45,
            rcTotal: 1,
            pensPG: 0.18,
            impact:
              'Harrington averages 3.82 yellows/game \u2014 above average. Expect cards in midfield battles. Man Utd\u2019s Ugarte and Mainoo are frequent offenders.',
          },
          h2h: [
            'MUN 2-0 BRE (Sep 25)',
            'BRE 1-1 MUN (May 25)',
            'MUN 2-1 BRE (Oct 24)',
            'BRE 2-2 MUN (Mar 24)',
            'MUN 1-0 BRE (Oct 23)',
          ],
          odds: { h: '4/7', d: '3/1', a: '9/2' },
          motivation:
            '\ud83c\udfc6 Man Utd 3rd on 58pts, chasing top-2 for direct CL entry. Beat Chelsea 1-0 away but lost 1-2 at home to Leeds. Brentford on FIVE consecutive draws \u2014 the ultimate stalemate team. Mart\u00ednez suspended, Yoro doubtful.',
          stats: {
            corners: { low: 7, med: 11, high: 15, safe: 10, h: 6, a: 5 },
            shots: { low: 18, med: 25, high: 32, safe: 24, h: 14, a: 11 },
            sot: { low: 5, med: 8, high: 12, safe: 8, h: 5, a: 4 },
            fouls: { low: 15, med: 21, high: 27, safe: 20, h: 11, a: 10 },
            throws: { low: 32, med: 40, high: 48, safe: 39, h: 20, a: 20 },
            gk: { low: 5, med: 10, high: 14, safe: 9, h: 4, a: 5 },
            tackles: { low: 26, med: 34, high: 42, safe: 33, h: 17, a: 17 },
            offsides: { low: 1, med: 3, high: 5, safe: 3, h: 2, a: 1 },
          },
          htScore: '1-0',
          ftScore: '2-0',
          htConf: '48%',
          ftConf: '40%',
          boldScore: '2-1',
        },

        {
          home: {
            name: 'PSG',
            short: 'PSG',
            pos: '1st (Ligue 1)',
            badge:
              'https://static.files.bbci.co.uk/core/website/assets/static/sport/football/paris-st-germain.9fc63d41ab.svg',
            color: '#004170',
            color2: '#DA291C',
            form: ['W', 'L', 'W', 'W', 'W'],
            xg: 2.11,
            xga: 0.95,
            cornPG: 6.21,
            shotsPG: 17.9,
            sotPG: 6.2,
            foulsPG: 9.66,
            throwsPG: 18.4,
            gkPG: 3.4,
            tacklePG: 16.8,
            offsidePG: 2.72,
            injuries: [
              'Vitinha (heel, doubtful)',
              'N. Mendes (fitness, doubtful)',
              'Q. Ndjantou (injury)',
            ],
            cardPlayers: [
              { n: 'W. Zaire-Emery', c: 7, pct: '42%' },
              { n: 'F. Ruiz', c: 6, pct: '36%' },
              { n: 'Marquinhos', c: 5, pct: '32%' },
              { n: 'A. Hakimi', c: 4, pct: '26%' },
            ],
          },
          away: {
            name: 'Bayern Munich',
            short: 'BAY',
            pos: '1st (Bundesliga)',
            badge:
              'https://static.files.bbci.co.uk/core/website/assets/static/sport/football/bayern-munich.4ea824a8bf.svg',
            color: '#DC052D',
            color2: '#0066B2',
            form: ['W', 'W', 'W', 'W', 'D'],
            xg: 2.9,
            xga: 0.88,
            cornPG: 6.3,
            shotsPG: 19.5,
            sotPG: 7.1,
            foulsPG: 9.2,
            throwsPG: 17.8,
            gkPG: 3.2,
            tacklePG: 16.2,
            offsidePG: 1.7,
            injuries: [
              'S. Gnabry (thigh, out)',
              'T. Bischof (injury)',
              'W. Mike (injury)',
              'D. Santos (injury)',
              'S. Ulreich (injury)',
            ],
            cardPlayers: [
              { n: 'J. Kimmich', c: 8, pct: '44%' },
              { n: 'A. Laimer', c: 6, pct: '36%' },
              { n: 'D. Upamecano', c: 6, pct: '34%' },
              { n: 'L. Goretzka', c: 5, pct: '28%' },
            ],
          },
          ko: '20:00',
          venue: 'Parc des Princes',
          matchday: 'UCL Semi-Final 1st Leg \u00b7 Tue 28 Apr',
          referee: {
            name: 'Fran\u00e7ois Letexier',
            games: 12,
            ycPG: 3.58,
            foulsPG: 22.1,
            rcTotal: 0,
            pensPG: 0.25,
            impact:
              'Letexier is a strict but fair UEFA official. High foul count (22.1/game) means he lets play build before whistling. Expect a tense, tactical affair.',
          },
          h2h: [
            'PSG 1-0 BAY (UCL SF 24)',
            'BAY 1-0 PSG (UCL SF 24)',
            'PSG 0-2 BAY (UCL R16 23)',
            'BAY 2-0 PSG (UCL R16 23)',
            'PSG 0-1 BAY (UCL F 20)',
          ],
          odds: { h: '6/4', d: '12/5', a: '7/4' },
          motivation:
            '\ud83c\udfc6 UCL SEMI-FINAL! PSG defending champions, beat Liverpool 4-0 agg in QF. Bayern unbeaten in 18, beat Real Madrid in QF. Kane has 53 GOALS this season. Kompany suspended for 1st leg. Vitinha doubtful \u2014 huge loss for PSG midfield.',
          stats: {
            corners: { low: 8, med: 12, high: 17, safe: 12, h: 6, a: 6 },
            shots: { low: 28, med: 37, high: 46, safe: 35, h: 18, a: 19 },
            sot: { low: 8, med: 13, high: 18, safe: 12, h: 6, a: 7 },
            fouls: { low: 13, med: 19, high: 25, safe: 18, h: 10, a: 9 },
            throws: { low: 28, med: 36, high: 44, safe: 35, h: 18, a: 18 },
            gk: { low: 3, med: 7, high: 11, safe: 6, h: 3, a: 3 },
            tackles: { low: 24, med: 33, high: 42, safe: 32, h: 16, a: 17 },
            offsides: { low: 2, med: 4, high: 7, safe: 4, h: 3, a: 2 },
          },
          htScore: '0-0',
          ftScore: '1-1',
          htConf: '52%',
          ftConf: '35%',
          boldScore: '2-2',
        },

        {
          home: {
            name: 'Atl\u00e9tico Madrid',
            short: 'ATM',
            pos: '3rd (La Liga)',
            badge:
              'https://static.files.bbci.co.uk/core/website/assets/static/sport/football/atletico-madrid.8b14f6d5e1.svg',
            color: '#272E61',
            color2: '#CE3524',
            form: ['W', 'D', 'W', 'W', 'L'],
            xg: 1.55,
            xga: 0.92,
            cornPG: 6.48,
            shotsPG: 13.4,
            sotPG: 4.5,
            foulsPG: 11.34,
            throwsPG: 19.6,
            gkPG: 4.8,
            tacklePG: 18.2,
            offsidePG: 2.06,
            injuries: ['T. Lemar (knee, season)', 'C. Azpilicueta (calf)'],
            cardPlayers: [
              { n: 'R. de Paul', c: 10, pct: '52%' },
              { n: 'Koke', c: 8, pct: '44%' },
              { n: 'J. Gallagher', c: 7, pct: '38%' },
              { n: 'J. Gim\u00e9nez', c: 6, pct: '34%' },
            ],
          },
          away: {
            name: 'Arsenal',
            short: 'ARS',
            pos: '1st (73pts)',
            badge:
              'https://static.files.bbci.co.uk/core/website/assets/static/sport/football/arsenal.5be7ff54ce.svg',
            color: '#EF0107',
            color2: '#063672',
            form: ['W', 'W', 'W', 'L', 'L'],
            xg: 1.72,
            xga: 0.75,
            cornPG: 6.2,
            shotsPG: 13.6,
            sotPG: 5.5,
            foulsPG: 9.5,
            throwsPG: 19.4,
            gkPG: 3.8,
            tacklePG: 17.9,
            offsidePG: 1.5,
            injuries: [
              'B. Saka (Achilles, doubtful)',
              'J. Timber (out)',
              'T. Tomiyasu (knee, season)',
              'R. Nelson (knee, season)',
              'E. Nwaneri (knock)',
            ],
            cardPlayers: [
              { n: 'D. Rice', c: 8, pct: '44%' },
              { n: 'W. Saliba', c: 6, pct: '34%' },
              { n: 'G. Jesus', c: 5, pct: '28%' },
              { n: 'K. Havertz', c: 5, pct: '26%' },
            ],
          },
          ko: '20:00',
          venue: 'Civitas Metropolitano',
          matchday: 'UCL Semi-Final 1st Leg \u00b7 Wed 29 Apr',
          referee: {
            name: 'Danny Makkelie',
            games: 14,
            ycPG: 4.0,
            foulsPG: 21.5,
            rcTotal: 2,
            pensPG: 0.29,
            impact:
              'Makkelie is a card-heavy referee (4.0 YC/game). In Atl\u00e9tico\u2019s physical pressing game, expect 4-5 yellows minimum. De Paul averages a card every 2 games.',
          },
          h2h: [
            'ARS 4-0 ATM (UCL Oct 25)',
            'ATM 1-0 ARS (UEL SF 18)',
            'ARS 1-1 ATM (UEL SF 18)',
          ],
          odds: { h: '11/8', d: '23/10', a: '2/1' },
          motivation:
            '\ud83c\udfc6 UCL SEMI-FINAL! Arsenal thrashed Atl\u00e9tico 4-0 in the group stage this season. Simeone\u2019s side will park the bus at home for revenge. Arsenal top of PL but back-to-back league losses \u2014 rotation risk. Saka doubtful is massive.',
          stats: {
            corners: { low: 8, med: 13, high: 18, safe: 12, h: 7, a: 6 },
            shots: { low: 18, med: 27, high: 36, safe: 25, h: 13, a: 14 },
            sot: { low: 5, med: 10, high: 15, safe: 9, h: 5, a: 5 },
            fouls: { low: 16, med: 21, high: 27, safe: 21, h: 12, a: 9 },
            throws: { low: 30, med: 39, high: 48, safe: 38, h: 20, a: 19 },
            gk: { low: 5, med: 9, high: 13, safe: 8, h: 5, a: 4 },
            tackles: { low: 28, med: 36, high: 44, safe: 35, h: 18, a: 18 },
            offsides: { low: 2, med: 4, high: 6, safe: 4, h: 2, a: 2 },
          },
          htScore: '0-0',
          ftScore: '1-1',
          htConf: '55%',
          ftConf: '32%',
          boldScore: '0-2',
        },

        {
          home: {
            name: "Nott'm Forest",
            short: 'NFO',
            pos: '16th (39pts)',
            badge:
              'https://cdn.brandfetch.io/idwmZKybXP/theme/dark/logo.svg?c=1bxid64Mup7aczewSAYMX&t=1773431229883',
            color: '#E53233',
            color2: '#fff',
            form: ['W', 'W', 'W', 'D', 'D'],
            xg: 1.16,
            xga: 1.28,
            cornPG: 4.5,
            shotsPG: 11.5,
            sotPG: 4.8,
            foulsPG: 11.3,
            throwsPG: 19.8,
            gkPG: 5.1,
            tacklePG: 17.5,
            offsidePG: 1.59,
            injuries: [
              'C. Hudson-Odoi (surgery, season)',
              'Murillo (muscle)',
              'W. Boly (knee)',
              'N. Savona (knee)',
            ],
            cardPlayers: [
              { n: 'E. Anderson', c: 6, pct: '38%' },
              { n: 'N. Milenkovi\u0107', c: 6, pct: '36%' },
              { n: 'R. Yates', c: 5, pct: '30%' },
              { n: 'N. Williams', c: 4, pct: '26%' },
            ],
          },
          away: {
            name: 'Aston Villa',
            short: 'AVL',
            pos: '5th (58pts)',
            badge:
              'https://cdn.brandfetch.io/idFPmd025E/theme/dark/logo.svg?c=1bxid64Mup7aczewSAYMX&t=1668077974118',
            color: '#670E36',
            color2: '#95BFE5',
            form: ['W', 'W', 'D', 'W', 'W'],
            xg: 1.27,
            xga: 1.43,
            cornPG: 5.24,
            shotsPG: 12.8,
            sotPG: 4.1,
            foulsPG: 10.2,
            throwsPG: 20.5,
            gkPG: 4.8,
            tacklePG: 17.2,
            offsidePG: 1.06,
            injuries: [
              'B. Kamara (knee, season)',
              'A. Onana (small pain, doubtful)',
            ],
            cardPlayers: [
              { n: 'M. Cash', c: 6, pct: '38%' },
              { n: 'E. Buend\u00eda', c: 5, pct: '34%' },
              { n: 'L. Bogarde', c: 5, pct: '32%' },
              { n: 'L. Bailey', c: 4, pct: '28%' },
            ],
          },
          ko: '20:00',
          venue: 'City Ground',
          matchday: 'UEL Semi-Final 1st Leg \u00b7 Thu 30 Apr',
          referee: {
            name: 'Jes\u00fas Gil Manzano',
            games: 16,
            ycPG: 4.5,
            foulsPG: 22.8,
            rcTotal: 2,
            pensPG: 0.31,
            impact:
              'Gil Manzano is VERY card-heavy (4.5 YC/game). Spanish referees tend to call more fouls \u2014 expect a stop-start game. Perfect conditions for Simeone-style football to creep in.',
          },
          h2h: [
            'AVL 3-1 NFO (PL Sep 25)',
            'NFO 2-1 AVL (PL Apr 25)',
            'AVL 1-2 NFO (PL Nov 24)',
            'NFO 1-1 AVL (PL Feb 24)',
            'AVL 4-2 NFO (PL Sep 23)',
          ],
          odds: { h: '13/8', d: '5/2', a: '8/5' },
          motivation:
            '\ud83c\udfc6 UEL SEMI-FINAL! English derby at the City Ground. Forest just demolished Sunderland 5-0 in the PL \u2014 confidence sky-high. Villa chasing top-4 AND Europa glory but Onana doubtful. Forest\u2019s European run is their best since 1980.',
          stats: {
            corners: { low: 6, med: 10, high: 14, safe: 9, h: 5, a: 5 },
            shots: { low: 16, med: 24, high: 32, safe: 23, h: 12, a: 12 },
            sot: { low: 5, med: 9, high: 13, safe: 8, h: 5, a: 4 },
            fouls: { low: 16, med: 22, high: 28, safe: 21, h: 11, a: 11 },
            throws: { low: 32, med: 40, high: 48, safe: 39, h: 20, a: 20 },
            gk: { low: 6, med: 10, high: 14, safe: 9, h: 5, a: 5 },
            tackles: { low: 26, med: 35, high: 44, safe: 34, h: 17, a: 18 },
            offsides: { low: 1, med: 3, high: 5, safe: 3, h: 2, a: 1 },
          },
          htScore: '0-0',
          ftScore: '1-1',
          htConf: '50%',
          ftConf: '30%',
          boldScore: '2-1',
        },

        {
          home: {
            name: 'Sp. Braga',
            short: 'BRA',
            pos: '4th (Liga Portugal)',
            badge:
              'https://static.files.bbci.co.uk/core/website/assets/static/sport/football/sporting-braga.cc49939cfa.svg',
            color: '#C8102E',
            color2: '#fff',
            form: ['W', 'W', 'D', 'L', 'W'],
            xg: 1.42,
            xga: 1.1,
            cornPG: 5.4,
            shotsPG: 13.2,
            sotPG: 4.6,
            foulsPG: 12.8,
            throwsPG: 20.6,
            gkPG: 5.0,
            tacklePG: 18.0,
            offsidePG: 2.9,
            injuries: [
              'S. Niakat\u00e9 (Achilles, season)',
              'D. Rodrigues (ankle)',
            ],
            cardPlayers: [
              { n: 'R. Horta', c: 7, pct: '40%' },
              { n: 'A. El Ouazzani', c: 6, pct: '34%' },
              { n: 'J. Source', c: 5, pct: '30%' },
              { n: 'Rodrigo Zalazar', c: 5, pct: '28%' },
            ],
          },
          away: {
            name: 'Freiburg',
            short: 'FRE',
            pos: '5th (Bundesliga)',
            badge:
              'https://static.files.bbci.co.uk/core/website/assets/static/sport/football/freiburg.913d385d12.svg',
            color: '#E2001A',
            color2: '#000',
            form: ['W', 'D', 'W', 'L', 'W'],
            xg: 1.38,
            xga: 1.15,
            cornPG: 4.8,
            shotsPG: 12.4,
            sotPG: 4.2,
            foulsPG: 11.6,
            throwsPG: 19.2,
            gkPG: 4.6,
            tacklePG: 17.6,
            offsidePG: 1.6,
            injuries: ['No major absences reported'],
            cardPlayers: [
              { n: 'M. Eggestein', c: 7, pct: '42%' },
              { n: 'P. Lienhart', c: 6, pct: '36%' },
              { n: 'L. K\u00fcbler', c: 5, pct: '30%' },
              { n: 'V. Grifo', c: 4, pct: '26%' },
            ],
          },
          ko: '20:00',
          venue: 'Est\u00e1dio Municipal de Braga',
          matchday: 'UEL Semi-Final 1st Leg \u00b7 Thu 30 Apr',
          referee: {
            name: 'Slavko Vin\u010di\u0107',
            games: 18,
            ycPG: 3.9,
            foulsPG: 21.2,
            rcTotal: 1,
            pensPG: 0.22,
            impact:
              'Vin\u010di\u0107 is an experienced Slovenian referee. Consistent card rate. Portuguese teams tend to foul more at home \u2014 expect Braga to test boundaries.',
          },
          h2h: ['No previous meetings'],
          odds: { h: '5/4', d: '12/5', a: '2/1' },
          motivation:
            '\ud83c\udfc6 UEL SEMI-FINAL! Braga in their FIRST EVER European semi-final. Freiburg went to extra-time vs Stuttgart in DFB-Pokal 3 days earlier \u2014 fatigue factor. Braga have home advantage and electric atmosphere. Both teams pragmatic.',
          stats: {
            corners: { low: 6, med: 10, high: 14, safe: 10, h: 5, a: 5 },
            shots: { low: 18, med: 26, high: 34, safe: 24, h: 13, a: 12 },
            sot: { low: 5, med: 9, high: 13, safe: 8, h: 5, a: 4 },
            fouls: { low: 18, med: 24, high: 31, safe: 24, h: 13, a: 12 },
            throws: { low: 32, med: 40, high: 48, safe: 39, h: 21, a: 19 },
            gk: { low: 5, med: 10, high: 14, safe: 9, h: 5, a: 5 },
            tackles: { low: 28, med: 36, high: 44, safe: 35, h: 18, a: 18 },
            offsides: { low: 2, med: 4, high: 7, safe: 4, h: 3, a: 2 },
          },
          htScore: '1-0',
          ftScore: '2-1',
          htConf: '42%',
          ftConf: '35%',
          boldScore: '2-0',
        },

        {
          home: {
            name: 'Leeds Utd',
            short: 'LEE',
            pos: '15th (40pts)',
            badge:
              'https://contentfulproxy.stadion.io/phva2knh4vy5/59uDDesQq19p5lVzfe45BY/a89feaa950427ef005c9d028e925bef0/Full_colour_crest.png?fm=webp&fit=pad&f=center&w=144&h=144&q=100',
            color: '#FFCD00',
            color2: '#1D428A',
            form: ['D', 'W', 'W', 'D', 'W'],
            xg: 1.32,
            xga: 1.24,
            cornPG: 4.8,
            shotsPG: 11.8,
            sotPG: 4.2,
            foulsPG: 11.8,
            throwsPG: 21.4,
            gkPG: 5.4,
            tacklePG: 18.2,
            offsidePG: 1.56,
            injuries: [
              'I. Gruev (meniscus, season)',
              'J. Bogle (foot, doubtful)',
              'J. Rodon (ankle, doubtful)',
            ],
            cardPlayers: [
              { n: 'E. Ampadu', c: 8, pct: '44%' },
              { n: 'W. Gnonto', c: 6, pct: '34%' },
              { n: 'D. James', c: 5, pct: '30%' },
              { n: 'J. Rothwell', c: 4, pct: '26%' },
            ],
          },
          away: {
            name: 'Burnley',
            short: 'BUR',
            pos: '19th (20pts)',
            badge:
              'https://static.files.bbci.co.uk/core/website/assets/static/sport/football/burnley.03819b9eba.svg',
            color: '#6C1D45',
            color2: '#99D6EA',
            form: ['L', 'L', 'L', 'D', 'L'],
            xg: 0.72,
            xga: 1.86,
            cornPG: 3.2,
            shotsPG: 8.4,
            sotPG: 2.6,
            foulsPG: 12.4,
            throwsPG: 19.6,
            gkPG: 6.2,
            tacklePG: 16.8,
            offsidePG: 1.59,
            injuries: [
              'J. Cullen (ACL, season)',
              'Z. Amdouni (ACL)',
              'H. Mejbri (hamstring)',
              'J. Beyer (knee)',
              'C. Roberts (Achilles)',
              'M. Tresor (ankle)',
            ],
            cardPlayers: [
              { n: 'J. Brownhill', c: 7, pct: '42%' },
              { n: 'L. Koleosho', c: 5, pct: '30%' },
              { n: 'D. Muric', c: 4, pct: '26%' },
              { n: 'M. Kompany Jr', c: 4, pct: '24%' },
            ],
          },
          ko: '20:00',
          venue: 'Elland Road',
          matchday: 'Matchday 36 \u00b7 Fri 1 May',
          referee: {
            name: 'Robert Jones',
            games: 19,
            ycPG: 3.42,
            foulsPG: 19.8,
            rcTotal: 0,
            pensPG: 0.16,
            impact:
              'Jones is a lenient referee. Low card rate (3.42/game). Should let the game flow \u2014 good for Leeds\u2019 attacking style.',
          },
          h2h: [
            'BUR 0-2 LEE (Sep 25)',
            'LEE 1-1 BUR (May 25)',
            'BUR 2-1 LEE (Jan 25)',
            'LEE 4-0 BUR (Sep 24)',
            'BUR 0-0 LEE (Mar 24)',
          ],
          odds: { h: '2/5', d: '7/2', a: '7/1' },
          motivation:
            '\u26a0\ufe0f Burnley already RELEGATED. Leeds safe in 15th but want strong finish after FA Cup semi-final run. Burnley have 6 key injuries \u2014 bare-bones squad. Leeds won 3 of last 5 vs Burnley.',
          stats: {
            corners: { low: 5, med: 8, high: 12, safe: 8, h: 5, a: 3 },
            shots: { low: 14, med: 20, high: 26, safe: 19, h: 12, a: 8 },
            sot: { low: 4, med: 7, high: 10, safe: 6, h: 4, a: 3 },
            fouls: { low: 18, med: 24, high: 30, safe: 23, h: 12, a: 12 },
            throws: { low: 32, med: 41, high: 49, safe: 40, h: 21, a: 20 },
            gk: { low: 6, med: 12, high: 17, safe: 11, h: 5, a: 6 },
            tackles: { low: 26, med: 35, high: 44, safe: 34, h: 18, a: 17 },
            offsides: { low: 1, med: 3, high: 5, safe: 3, h: 2, a: 2 },
          },
          htScore: '1-0',
          ftScore: '2-0',
          htConf: '52%',
          ftConf: '45%',
          boldScore: '3-0',
        },

        {
          home: {
            name: 'Brentford',
            short: 'BRE',
            pos: '9th (48pts)',
            badge:
              'https://cdn.brandfetch.io/idXs8Qu2W6/theme/dark/logo.svg?c=1bxid64Mup7aczewSAYMX&t=1775048371985',
            color: '#e30613',
            color2: '#FFB81C',
            form: ['D', 'D', 'D', 'D', 'D'],
            xg: 1.18,
            xga: 1.24,
            cornPG: 4.82,
            shotsPG: 10.6,
            sotPG: 3.4,
            foulsPG: 10.4,
            throwsPG: 19.8,
            gkPG: 5.2,
            tacklePG: 17.4,
            offsidePG: 1.44,
            injuries: [
              'F. Carvalho (ACL, season)',
              'A. Milambo (ACL, season)',
              'J. Dasilva (knee)',
            ],
            cardPlayers: [
              { n: 'C. N\u00f8rgaard', c: 7, pct: '40%' },
              { n: 'Y. Wissa', c: 5, pct: '32%' },
              { n: 'M. Damsgaard', c: 5, pct: '30%' },
              { n: 'V. Jorgensen', c: 4, pct: '26%' },
            ],
          },
          away: {
            name: 'West Ham',
            short: 'WHU',
            pos: '17th (36pts)',
            badge:
              'https://cdn.brandfetch.io/idioDWtJyw/theme/dark/logo.svg?c=1bxid64Mup7aczewSAYMX&t=1668077966418',
            color: '#7A263A',
            color2: '#1BB1E7',
            form: ['D', 'W', 'L', 'L', 'D'],
            xg: 1.12,
            xga: 1.56,
            cornPG: 4.6,
            shotsPG: 9.0,
            sotPG: 3.4,
            foulsPG: 11.3,
            throwsPG: 20.1,
            gkPG: 5.6,
            tacklePG: 16.2,
            offsidePG: 1.85,
            injuries: ['Fully fit squad reported'],
            cardPlayers: [
              { n: 'L. Paquet\u00e1', c: 7, pct: '44%' },
              { n: 'M. Fernandes', c: 7, pct: '40%' },
              { n: 'T. Sou\u010dek', c: 5, pct: '32%' },
              { n: 'K. Mavropanos', c: 4, pct: '28%' },
            ],
          },
          ko: '15:00',
          venue: 'Gtech Community Stadium',
          matchday: 'Matchday 36 \u00b7 Sat 2 May',
          referee: {
            name: 'John Brooks',
            games: 20,
            ycPG: 3.35,
            foulsPG: 20.1,
            rcTotal: 0,
            pensPG: 0.2,
            impact:
              'Brooks is a relaxed referee \u2014 below average cards. West Ham\u2019s desperation could lead to fouls but he won\u2019t over-officiate.',
          },
          h2h: [
            'WHU 1-0 BRE (Sep 25)',
            'BRE 3-2 WHU (Apr 25)',
            'WHU 0-0 BRE (Dec 24)',
            'BRE 1-1 WHU (Feb 24)',
            'WHU 3-2 BRE (Sep 23)',
          ],
          odds: { h: '11/10', d: '5/2', a: '5/2' },
          motivation:
            '\ud83d\udd25 RELEGATION SIX-POINTER for West Ham! 17th on 36pts, just 2pts above safety. Brentford\u2019s FIVE consecutive draws make them draw specialists. West Ham need a win desperately \u2014 full commitment expected.',
          stats: {
            corners: { low: 5, med: 9, high: 13, safe: 9, h: 5, a: 4 },
            shots: { low: 14, med: 20, high: 26, safe: 19, h: 11, a: 9 },
            sot: { low: 4, med: 7, high: 10, safe: 6, h: 3, a: 4 },
            fouls: { low: 15, med: 22, high: 28, safe: 21, h: 10, a: 12 },
            throws: { low: 32, med: 40, high: 47, safe: 39, h: 20, a: 20 },
            gk: { low: 6, med: 11, high: 15, safe: 10, h: 5, a: 6 },
            tackles: { low: 26, med: 34, high: 42, safe: 33, h: 17, a: 17 },
            offsides: { low: 1, med: 3, high: 5, safe: 3, h: 1, a: 2 },
          },
          htScore: '0-0',
          ftScore: '1-1',
          htConf: '48%',
          ftConf: '38%',
          boldScore: '2-2',
        },

        {
          home: {
            name: 'Newcastle',
            short: 'NEW',
            pos: '14th (42pts)',
            badge:
              'https://static.files.bbci.co.uk/core/website/assets/static/sport/football/newcastle-united.7daf913814.svg',
            color: '#898787',
            color2: '#fff',
            form: ['L', 'L', 'L', 'L', 'W'],
            xg: 1.35,
            xga: 1.38,
            cornPG: 3.6,
            shotsPG: 10.8,
            sotPG: 4.6,
            foulsPG: 11.2,
            throwsPG: 20.6,
            gkPG: 5.0,
            tacklePG: 17.3,
            offsidePG: 1.29,
            injuries: [
              'A. Gordon (hip)',
              'T. Livramento (leg)',
              'F. Sch\u00e4r (muscle)',
              'Joelinton (suspended)',
            ],
            cardPlayers: [
              { n: 'B. Guimar\u00e3es', c: 6, pct: '38%' },
              { n: 'S. Longstaff', c: 6, pct: '36%' },
              { n: 'D. Burn', c: 5, pct: '30%' },
              { n: 'T. Trippier', c: 4, pct: '26%' },
            ],
          },
          away: {
            name: 'Brighton',
            short: 'BHA',
            pos: '6th (50pts)',
            badge:
              'https://static.files.bbci.co.uk/core/website/assets/static/sport/football/brighton-and-hove-albion.4522a78440.svg',
            color: '#0057B8',
            color2: '#FFCD00',
            form: ['W', 'W', 'D', 'L', 'W'],
            xg: 1.62,
            xga: 1.08,
            cornPG: 5.6,
            shotsPG: 14.2,
            sotPG: 5.0,
            foulsPG: 10.8,
            throwsPG: 19.8,
            gkPG: 4.4,
            tacklePG: 17.0,
            offsidePG: 1.74,
            injuries: [
              'A. Webster (knee)',
              'S. Tzimas (injury)',
              'L. Dunk (suspended)',
              'J. Milner (knock, doubtful)',
            ],
            cardPlayers: [
              { n: 'C. Baleba', c: 7, pct: '40%' },
              { n: 'J. Minteh', c: 5, pct: '32%' },
              { n: 'B. Ayari', c: 5, pct: '30%' },
              { n: 'J. van Hecke', c: 4, pct: '26%' },
            ],
          },
          ko: '15:00',
          venue: "St James' Park",
          matchday: 'Matchday 36 \u00b7 Sat 2 May',
          referee: {
            name: 'David Coote',
            games: 21,
            ycPG: 3.95,
            foulsPG: 21.3,
            rcTotal: 2,
            pensPG: 0.24,
            impact:
              'Coote averages nearly 4 yellows/game. Newcastle\u2019s desperation could lead to rash challenges. Key match for both European aspirations.',
          },
          h2h: [
            'BHA 3-1 NEW (Sep 25)',
            'NEW 1-1 BHA (Mar 25)',
            'BHA 3-0 NEW (Nov 24)',
            'NEW 4-1 BHA (Apr 24)',
            'BHA 0-3 NEW (Sep 23)',
          ],
          odds: { h: '6/4', d: '5/2', a: '9/5' },
          motivation:
            '\ud83c\udfc6 Newcastle 14th on 42pts \u2014 need points to secure safety. Gordon OUT, Joelinton suspended. Brighton 6th chasing Europa League spot. Dunk suspended but Brighton in strong form \u2014 won 3 of last 5.',
          stats: {
            corners: { low: 5, med: 9, high: 13, safe: 9, h: 4, a: 5 },
            shots: { low: 18, med: 25, high: 32, safe: 24, h: 11, a: 14 },
            sot: { low: 6, med: 10, high: 14, safe: 9, h: 5, a: 5 },
            fouls: { low: 16, med: 22, high: 28, safe: 21, h: 11, a: 11 },
            throws: { low: 32, med: 40, high: 48, safe: 39, h: 21, a: 19 },
            gk: { low: 5, med: 9, high: 14, safe: 9, h: 5, a: 4 },
            tackles: { low: 26, med: 34, high: 42, safe: 33, h: 17, a: 17 },
            offsides: { low: 1, med: 3, high: 5, safe: 3, h: 1, a: 2 },
          },
          htScore: '0-0',
          ftScore: '0-1',
          htConf: '42%',
          ftConf: '35%',
          boldScore: '1-2',
        },

        {
          home: {
            name: 'Wolves',
            short: 'WOL',
            pos: '20th (17pts)',
            badge:
              'https://cdn.brandfetch.io/idv6uGDaMw/theme/dark/logo.svg?c=1bxid64Mup7aczewSAYMX&t=1668077974804',
            color: '#FDB913',
            color2: '#231F20',
            form: ['L', 'L', 'L', 'D', 'L'],
            xg: 0.88,
            xga: 1.62,
            cornPG: 3.0,
            shotsPG: 9.4,
            sotPG: 2.8,
            foulsPG: 13.1,
            throwsPG: 21.2,
            gkPG: 6.4,
            tacklePG: 17.8,
            offsidePG: 1.35,
            injuries: [
              'M. Mane (injury)',
              'H. Hwang (injury)',
              'Y. Mosquera (ACL, season)',
              'P. Sarabia (muscle)',
              'S. Kalajdzi\u0107 (ACL, season)',
            ],
            cardPlayers: [
              { n: 'J. Doherty', c: 7, pct: '42%' },
              { n: 'M. Lemina', c: 6, pct: '38%' },
              { n: 'A. Bellegarde', c: 5, pct: '30%' },
              { n: 'M. Nunes', c: 5, pct: '28%' },
            ],
          },
          away: {
            name: 'Sunderland',
            short: 'SUN',
            pos: '12th (46pts)',
            badge:
              'https://upload.wikimedia.org/wikipedia/en/thumb/7/77/Logo_Sunderland.svg/960px-Logo_Sunderland.svg.png',
            color: '#EB172B',
            color2: '#fff',
            form: ['L', 'L', 'W', 'W', 'L'],
            xg: 1.02,
            xga: 1.32,
            cornPG: 5.6,
            shotsPG: 14.2,
            sotPG: 4.6,
            foulsPG: 12.2,
            throwsPG: 20.4,
            gkPG: 5.5,
            tacklePG: 16.9,
            offsidePG: 1.5,
            injuries: [
              'N. Angulo (long-term)',
              'B. Traor\u00e9 (knee)',
              'J. Ta Bi (ankle)',
              'D. Ballard (ankle)',
            ],
            cardPlayers: [
              { n: 'T. Hume', c: 9, pct: '48%' },
              { n: 'D. Ballard', c: 6, pct: '34%' },
              { n: 'J. Cirkin', c: 5, pct: '30%' },
              { n: 'P. Roberts', c: 4, pct: '26%' },
            ],
          },
          ko: '15:00',
          venue: 'Molineux',
          matchday: 'Matchday 36 \u00b7 Sat 2 May',
          referee: {
            name: 'Simon Hooper',
            games: 17,
            ycPG: 3.59,
            foulsPG: 20.6,
            rcTotal: 0,
            pensPG: 0.18,
            impact:
              'Hooper is an average-pace referee. Nothing extreme in either direction. Wolves\u2019 high foul rate (13.1/game) will test him.',
          },
          h2h: [
            'SUN 2-1 WOL (Sep 25)',
            'WOL 1-1 SUN (May 25)',
            'SUN 3-0 WOL (Dec 24)',
            'WOL 0-2 SUN (Feb 24)',
            'SUN 1-0 WOL (Sep 23)',
          ],
          odds: { h: '7/4', d: '5/2', a: '7/4' },
          motivation:
            '\u26a0\ufe0f Wolves already RELEGATED, nothing to play for. Sunderland thumped 0-5 by Forest and need to bounce back. Sunderland haven\u2019t lost to Wolves in 5 meetings. Wolves at home may scrape a result but lack quality.',
          stats: {
            corners: { low: 5, med: 9, high: 13, safe: 8, h: 3, a: 5 },
            shots: { low: 16, med: 24, high: 31, safe: 22, h: 9, a: 14 },
            sot: { low: 4, med: 7, high: 11, safe: 7, h: 3, a: 5 },
            fouls: { low: 19, med: 25, high: 32, safe: 25, h: 13, a: 12 },
            throws: { low: 34, med: 42, high: 49, safe: 41, h: 21, a: 20 },
            gk: { low: 7, med: 12, high: 16, safe: 11, h: 6, a: 6 },
            tackles: { low: 26, med: 35, high: 44, safe: 34, h: 18, a: 17 },
            offsides: { low: 1, med: 3, high: 5, safe: 3, h: 1, a: 2 },
          },
          htScore: '0-1',
          ftScore: '0-2',
          htConf: '42%',
          ftConf: '38%',
          boldScore: '1-3',
        },

        {
          home: {
            name: 'Arsenal',
            short: 'ARS',
            pos: '1st (73pts)',
            badge:
              'https://cdn.brandfetch.io/ida744DnR8/theme/dark/logo.svg?c=1bxid64Mup7aczewSAYMX&t=1667609875130',
            color: '#EF0107',
            color2: '#063672',
            form: ['W', 'W', 'W', 'L', 'L'],
            xg: 1.72,
            xga: 0.75,
            cornPG: 6.2,
            shotsPG: 13.6,
            sotPG: 5.5,
            foulsPG: 9.5,
            throwsPG: 19.4,
            gkPG: 3.8,
            tacklePG: 17.9,
            offsidePG: 1.5,
            injuries: [
              'B. Saka (Achilles, doubtful)',
              'J. Timber (out)',
              'T. Tomiyasu (knee, season)',
            ],
            cardPlayers: [
              { n: 'D. Rice', c: 8, pct: '44%' },
              { n: 'W. Saliba', c: 6, pct: '34%' },
              { n: 'G. Jesus', c: 5, pct: '28%' },
              { n: 'K. Havertz', c: 5, pct: '26%' },
            ],
          },
          away: {
            name: 'Fulham',
            short: 'FUL',
            pos: '10th (48pts)',
            badge:
              'https://cdn.brandfetch.io/idJTNo1NC-/theme/dark/logo.svg?c=1bxid64Mup7aczewSAYMX&t=1774916217250',
            color: '#e2e8f0',
            color2: '#fff',
            form: ['L', 'D', 'W', 'L', 'D'],
            xg: 1.28,
            xga: 1.41,
            cornPG: 5.6,
            shotsPG: 14.0,
            sotPG: 3.61,
            foulsPG: 9.4,
            throwsPG: 19.88,
            gkPG: 5.1,
            tacklePG: 16.8,
            offsidePG: 1.59,
            injuries: [
              'K. Tete (foot)',
              'A. Iwobi (hamstring, doubtful)',
              'H. Reed (knee)',
            ],
            cardPlayers: [
              { n: 'J. Andersen', c: 7, pct: '42%' },
              { n: 'S. Luki\u0107', c: 7, pct: '40%' },
              { n: 'T. Cairney', c: 5, pct: '30%' },
              { n: 'A. Robinson', c: 4, pct: '25%' },
            ],
          },
          ko: '15:00',
          venue: 'Emirates Stadium',
          matchday: 'Matchday 36 \u00b7 Sat 2 May',
          referee: {
            name: 'Michael Oliver',
            games: 24,
            ycPG: 3.54,
            foulsPG: 20.8,
            rcTotal: 2,
            pensPG: 0.33,
            impact:
              'Oliver is the PL\u2019s most experienced referee. Fair but firm. Highest penalty rate (0.33/game) \u2014 watch for Arsenal\u2019s set-piece entries into the box.',
          },
          h2h: [
            'FUL 0-2 ARS (Sep 25)',
            'ARS 1-1 FUL (May 25)',
            'FUL 1-2 ARS (Dec 24)',
            'ARS 2-1 FUL (Apr 24)',
            'FUL 0-3 ARS (Sep 23)',
          ],
          odds: { h: '1/3', d: '9/2', a: '8/1' },
          motivation:
            '\ud83c\udfc6 TITLE RACE! Arsenal top on 73pts. Must keep winning after CL SF. Fulham have nothing to play for \u2014 mid-table comfort. Arsenal unbeaten in last 5 vs Fulham and have won 4 of last 5 at the Emirates. Saka\u2019s fitness is key.',
          stats: {
            corners: { low: 7, med: 12, high: 16, safe: 11, h: 7, a: 5 },
            shots: { low: 20, med: 28, high: 36, safe: 26, h: 14, a: 14 },
            sot: { low: 6, med: 9, high: 13, safe: 9, h: 6, a: 4 },
            fouls: { low: 13, med: 19, high: 25, safe: 18, h: 9, a: 9 },
            throws: { low: 30, med: 39, high: 48, safe: 38, h: 19, a: 20 },
            gk: { low: 4, med: 9, high: 14, safe: 8, h: 4, a: 5 },
            tackles: { low: 26, med: 35, high: 44, safe: 34, h: 18, a: 17 },
            offsides: { low: 1, med: 3, high: 5, safe: 3, h: 2, a: 2 },
          },
          htScore: '1-0',
          ftScore: '3-0',
          htConf: '55%',
          ftConf: '42%',
          boldScore: '4-1',
        },

        {
          home: {
            name: 'Bournemouth',
            short: 'BOU',
            pos: '7th (49pts)',
            badge:
              'https://static.files.bbci.co.uk/core/website/assets/static/sport/football/afc-bournemouth.3e0ae7da8e.svg',
            color: '#DA291C',
            color2: '#000',
            form: ['W', 'D', 'L', 'W', 'W'],
            xg: 1.48,
            xga: 1.12,
            cornPG: 5.2,
            shotsPG: 13.8,
            sotPG: 4.6,
            foulsPG: 10.8,
            throwsPG: 20.2,
            gkPG: 4.6,
            tacklePG: 17.4,
            offsidePG: 1.79,
            injuries: [
              'L. Cook (thigh)',
              'J. Kluivert (knee)',
              'J. Soler (thigh, doubtful)',
            ],
            cardPlayers: [
              { n: 'A. Smith', c: 7, pct: '40%' },
              { n: 'R. Christie', c: 5, pct: '32%' },
              { n: 'M. Senesi', c: 5, pct: '30%' },
              { n: 'L. Cook', c: 4, pct: '26%' },
            ],
          },
          away: {
            name: 'Crystal Palace',
            short: 'CRY',
            pos: '13th (43pts)',
            badge:
              'https://cdn.brandfetch.io/iddi0P11VR/theme/dark/logo.svg?c=1bxid64Mup7aczewSAYMX&t=1668077972554',
            color: '#1B458F',
            color2: '#C4122E',
            form: ['D', 'L', 'W', 'D', 'W'],
            xg: 1.53,
            xga: 1.29,
            cornPG: 4.2,
            shotsPG: 12.4,
            sotPG: 3.9,
            foulsPG: 11.1,
            throwsPG: 20.8,
            gkPG: 5.3,
            tacklePG: 18.6,
            offsidePG: 1.91,
            injuries: [
              'E. Nketiah (hamstring)',
              'E. Guessand (long-term)',
              'N. Clyne (illness, doubtful)',
            ],
            cardPlayers: [
              { n: 'T. Mitchell', c: 6, pct: '38%' },
              { n: 'C. Doucoure', c: 5, pct: '34%' },
              { n: 'W. Hughes', c: 5, pct: '30%' },
              { n: 'M. Gu\u00e9hi', c: 4, pct: '26%' },
            ],
          },
          ko: '15:00',
          venue: 'Vitality Stadium',
          matchday: 'Matchday 36 \u00b7 Sun 3 May',
          referee: {
            name: 'Tim Robinson',
            games: 16,
            ycPG: 3.25,
            foulsPG: 19.4,
            rcTotal: 0,
            pensPG: 0.19,
            impact:
              'Robinson is lenient and lets games flow. Low card rate benefits both attacking teams.',
          },
          h2h: [
            'CRY 1-0 BOU (Sep 25)',
            'BOU 2-1 CRY (May 25)',
            'CRY 0-0 BOU (Nov 24)',
            'BOU 1-0 CRY (Apr 24)',
            'CRY 0-2 BOU (Dec 23)',
          ],
          odds: { h: '4/5', d: '3/1', a: '7/2' },
          motivation:
            '\ud83c\udfc6 Bournemouth 7th chasing Europa League spot. Palace comfortable in mid-table. Bournemouth have won 3 of last 4 at home and are the season\u2019s surprise package. Palace have beaten Liverpool twice this season.',
          stats: {
            corners: { low: 5, med: 9, high: 14, safe: 9, h: 5, a: 4 },
            shots: { low: 18, med: 26, high: 34, safe: 25, h: 14, a: 12 },
            sot: { low: 5, med: 9, high: 12, safe: 8, h: 5, a: 4 },
            fouls: { low: 15, med: 22, high: 28, safe: 21, h: 11, a: 11 },
            throws: { low: 32, med: 41, high: 49, safe: 40, h: 20, a: 21 },
            gk: { low: 5, med: 10, high: 14, safe: 9, h: 5, a: 5 },
            tackles: { low: 28, med: 36, high: 44, safe: 35, h: 17, a: 19 },
            offsides: { low: 2, med: 4, high: 6, safe: 4, h: 2, a: 2 },
          },
          htScore: '1-0',
          ftScore: '2-0',
          htConf: '45%',
          ftConf: '40%',
          boldScore: '3-1',
        },

        {
          home: {
            name: 'Man Utd',
            short: 'MUN',
            pos: '3rd (58pts)',
            badge:
              'https://static.files.bbci.co.uk/core/website/assets/static/sport/football/manchester-united.80807495b5.svg',
            color: '#DA291C',
            color2: '#FBE122',
            form: ['W', 'L', 'D', 'W', 'L'],
            xg: 1.58,
            xga: 1.22,
            cornPG: 6.0,
            shotsPG: 14.2,
            sotPG: 4.8,
            foulsPG: 10.6,
            throwsPG: 20.2,
            gkPG: 4.4,
            tacklePG: 17.0,
            offsidePG: 1.56,
            injuries: [
              'L. Mart\u00ednez (suspended)',
              'M. de Ligt (back, season)',
              'P. Dorgu (hamstring)',
            ],
            cardPlayers: [
              { n: 'M. Ugarte', c: 9, pct: '46%' },
              { n: 'K. Mainoo', c: 6, pct: '34%' },
              { n: 'D. Dalot', c: 5, pct: '30%' },
              { n: 'H. Maguire', c: 5, pct: '28%' },
            ],
          },
          away: {
            name: 'Liverpool',
            short: 'LIV',
            pos: '4th (58pts)',
            badge:
              'https://cdn.brandfetch.io/idLw_x5PBk/w/185/h/185/theme/dark/logo.webp?c=1bxid64Mup7aczewSAYMX&t=1746516677234',
            color: '#C8102E',
            color2: '#00B2A9',
            form: ['W', 'W', 'L', 'W', 'D'],
            xg: 1.65,
            xga: 1.18,
            cornPG: 6.8,
            shotsPG: 14.6,
            sotPG: 5.2,
            foulsPG: 9.8,
            throwsPG: 21.3,
            gkPG: 4.2,
            tacklePG: 17.5,
            offsidePG: 2.0,
            injuries: [
              'Alisson (muscle)',
              'G. Mamardashvili (knee)',
              'H. Ekitike (Achilles, season)',
              'W. Endo (ankle, season)',
            ],
            cardPlayers: [
              { n: 'D. Szoboszlai', c: 7, pct: '40%' },
              { n: 'R. Gravenberch', c: 5, pct: '32%' },
              { n: 'V. van Dijk', c: 4, pct: '26%' },
              { n: 'A. Mac Allister', c: 4, pct: '24%' },
            ],
          },
          ko: '16:30',
          venue: 'Old Trafford',
          matchday: 'Matchday 36 \u00b7 Sun 3 May',
          referee: {
            name: 'Anthony Taylor',
            games: 25,
            ycPG: 3.72,
            foulsPG: 21.2,
            rcTotal: 3,
            pensPG: 0.28,
            impact:
              'Taylor is the PL\u2019s most experienced big-game referee. Above-average card rate. This rivalry ALWAYS produces cards \u2014 expect 5+ yellows.',
          },
          h2h: [
            'MUN 2-1 LIV (Oct 25)',
            'LIV 2-2 MUN (Jan 25)',
            'MUN 0-3 LIV (Sep 24)',
            'MUN 2-2 LIV (Apr 24)',
            'LIV 0-0 MUN (Dec 23)',
          ],
          odds: { h: '6/4', d: '5/2', a: '9/5' },
          motivation:
            '\ud83d\udd25 THE BIGGEST RIVALRY IN ENGLISH FOOTBALL! Both on 58pts fighting for top-4/CL spots. Man Utd beat Liverpool 2-1 at Old Trafford earlier this season. Liverpool GK crisis continues (3rd choice Woodman). Electric atmosphere guaranteed.',
          stats: {
            corners: { low: 8, med: 13, high: 17, safe: 12, h: 6, a: 7 },
            shots: { low: 22, med: 29, high: 36, safe: 28, h: 14, a: 15 },
            sot: { low: 7, med: 10, high: 14, safe: 10, h: 5, a: 5 },
            fouls: { low: 14, med: 20, high: 27, safe: 20, h: 11, a: 10 },
            throws: { low: 34, med: 42, high: 50, safe: 41, h: 20, a: 22 },
            gk: { low: 5, med: 9, high: 13, safe: 8, h: 4, a: 4 },
            tackles: { low: 28, med: 35, high: 42, safe: 34, h: 17, a: 18 },
            offsides: { low: 2, med: 4, high: 6, safe: 4, h: 2, a: 2 },
          },
          htScore: '1-1',
          ftScore: '2-2',
          htConf: '35%',
          ftConf: '28%',
          boldScore: '3-2',
        },

        {
          home: {
            name: 'Aston Villa',
            short: 'AVL',
            pos: '5th (58pts)',
            badge:
              'https://cdn.brandfetch.io/idFPmd025E/theme/dark/logo.svg?c=1bxid64Mup7aczewSAYMX&t=1668077974118',
            color: '#670E36',
            color2: '#95BFE5',
            form: ['W', 'W', 'D', 'W', 'W'],
            xg: 1.27,
            xga: 1.43,
            cornPG: 5.24,
            shotsPG: 12.8,
            sotPG: 4.1,
            foulsPG: 10.2,
            throwsPG: 20.5,
            gkPG: 4.8,
            tacklePG: 17.2,
            offsidePG: 1.06,
            injuries: [
              'B. Kamara (knee, season)',
              'A. Onana (fitness, doubtful)',
            ],
            cardPlayers: [
              { n: 'M. Cash', c: 6, pct: '38%' },
              { n: 'E. Buend\u00eda', c: 5, pct: '34%' },
              { n: 'L. Bogarde', c: 5, pct: '32%' },
              { n: 'L. Bailey', c: 4, pct: '28%' },
            ],
          },
          away: {
            name: 'Tottenham',
            short: 'TOT',
            pos: '18th (34pts)',
            badge:
              'https://cdn.brandfetch.io/id0hQSdBIF/theme/dark/logo.svg?c=1bxid64Mup7aczewSAYMX&t=1668069471694',
            color: '#3b5fdf',
            color2: '#fff',
            form: ['D', 'L', 'L', 'D', 'L'],
            xg: 1.18,
            xga: 1.48,
            cornPG: 7.2,
            shotsPG: 12.6,
            sotPG: 4.5,
            foulsPG: 10.8,
            throwsPG: 20.4,
            gkPG: 4.9,
            tacklePG: 17.1,
            offsidePG: 1.52,
            injuries: [
              'C. Romero (knee, season)',
              'W. Odobert (ACL)',
              'B. Johnson (hamstring)',
              'D. Gray (knee)',
            ],
            cardPlayers: [
              { n: 'R. Bentancur', c: 7, pct: '40%' },
              { n: 'Y. Bissouma', c: 6, pct: '36%' },
              { n: 'P. Sarr', c: 5, pct: '30%' },
              { n: 'J. van de Ven', c: 4, pct: '26%' },
            ],
          },
          ko: '15:00',
          venue: 'Villa Park',
          matchday: 'Matchday 36 \u00b7 Sun 3 May',
          referee: {
            name: 'Peter Bankes',
            games: 18,
            ycPG: 3.44,
            foulsPG: 19.6,
            rcTotal: 0,
            pensPG: 0.17,
            impact:
              'Bankes is a lenient referee. Below-average cards (3.44/game). Villa\u2019s technical superiority should be rewarded with few interruptions.',
          },
          h2h: [
            'TOT 1-2 AVL (Sep 25)',
            'AVL 3-1 TOT (May 25)',
            'TOT 0-1 AVL (Nov 24)',
            'AVL 2-0 TOT (Mar 24)',
            'TOT 1-2 AVL (Nov 23)',
          ],
          odds: { h: '1/2', d: '7/2', a: '11/2' },
          motivation:
            '\ud83c\udfc6 Villa 5th on 58pts, chasing top-4. Spurs 18th and STILL in the relegation battle (2pts behind safety). Villa have won ALL 5 of the last H2H meetings. Spurs winless away from home since January. Villa coming off UEL SF 1st leg.',
          stats: {
            corners: { low: 8, med: 12, high: 16, safe: 12, h: 5, a: 7 },
            shots: { low: 18, med: 25, high: 33, safe: 24, h: 13, a: 12 },
            sot: { low: 5, med: 9, high: 13, safe: 8, h: 4, a: 5 },
            fouls: { low: 14, med: 21, high: 28, safe: 20, h: 10, a: 11 },
            throws: { low: 32, med: 41, high: 49, safe: 40, h: 20, a: 21 },
            gk: { low: 5, med: 10, high: 14, safe: 9, h: 5, a: 5 },
            tackles: { low: 26, med: 34, high: 42, safe: 33, h: 17, a: 17 },
            offsides: { low: 1, med: 3, high: 5, safe: 3, h: 1, a: 2 },
          },
          htScore: '1-0',
          ftScore: '2-0',
          htConf: '50%',
          ftConf: '42%',
          boldScore: '3-1',
        },
      ]

      function formDots(f) {
        return f.map(r => `<span class="form-dot ${r}">${r}</span>`).join('')
      }
      function barHTML(val, max, col) {
        const w = Math.min(100, (val / max) * 100)
        return `<div class="bar-wrap"><div class="bar" style="width:${w}%;background:${col}"></div></div>`
      }

      function renderMatch(m, i) {
        const hc = m.home.color,
          ac = m.away.color
        const s = m.stats
        const statRows = [
          ['Corners', s.corners],
          ['Shots', s.shots],
          ['On Target', s.sot],
          ['Fouls', s.fouls],
          ['Throw-ins', s.throws],
          ['Goal Kicks', s.gk],
          ['Tackles', s.tackles],
          ['Offsides', s.offsides],
        ]
        let statsTable = `<table><tr><th>Metric</th><th>${m.home.short}</th><th>${m.away.short}</th><th>Total</th><th>Low</th><th>Med</th><th>High</th><th>Safe</th></tr>`
        statRows.forEach(([lbl, d]) => {
          statsTable += `<tr><td style="font-weight:600">${lbl}</td><td style="color:${hc};font-weight:600">${d.h}</td><td style="color:${ac};font-weight:600">${d.a}</td><td>${d.h + d.a}</td><td>${d.low}</td><td style="font-weight:700">${d.med}</td><td>${d.high}</td><td style="color:#22c55e;font-weight:700">${d.safe}</td></tr>`
        })
        statsTable += '</table>'

        let cardChips =
          "<div class='section-title'>" + m.home.name + '</div><div>'
        m.home.cardPlayers.forEach(p => {
          cardChips += `<span class="player-chip">🟨 ${p.n} (${p.c}) <span class="pct">${p.pct}</span></span>`
        })
        cardChips +=
          "</div><div class='section-title' style='margin-top:10px'>" +
          m.away.name +
          '</div><div>'
        m.away.cardPlayers.forEach(p => {
          cardChips += `<span class="player-chip">🟨 ${p.n} (${p.c}) <span class="pct">${p.pct}</span></span>`
        })
        cardChips += '</div>'

        let h2hHTML = ''
        m.h2h.forEach(r => {
          const p = r.split('(')
          h2hHTML += `<div class="h2h-item"><span>${p[0].trim()}</span><span class="date">${p[1]?.replace(')', '')}</span></div>`
        })

        let injHTML = `<div class="section-title">${m.home.name} Injuries</div><div style="margin-bottom:8px">`
        m.home.injuries.forEach(inj => {
          injHTML += `<span class="player-chip">🏥 ${inj}</span>`
        })
        injHTML += `</div><div class="section-title">${m.away.name} Injuries</div><div>`
        m.away.injuries.forEach(inj => {
          injHTML += `<span class="player-chip">🏥 ${inj}</span>`
        })
        injHTML += '</div>'

        const r = m.referee || {}
        const refHTML = r.name
          ? `<div class="ref-card"><div class="ref-icon">👨‍⚖️</div><div class="ref-info"><div class="ref-name">${r.name}</div><div class="ref-role">Match Referee · ${r.games} PL games this season</div></div></div>
<div class="ref-stats">
<div class="ref-stat"><div class="rs-val">${r.ycPG}</div><div class="rs-lbl">Yellows/Game</div></div>
<div class="ref-stat"><div class="rs-val">${r.foulsPG}</div><div class="rs-lbl">Fouls/Game</div></div>
<div class="ref-stat"><div class="rs-val">${r.pensPG}</div><div class="rs-lbl">Pens/Game</div></div>
</div>
<div class="ref-stats" style="grid-template-columns:1fr 1fr">
<div class="ref-stat"><div class="rs-val">${r.rcTotal}</div><div class="rs-lbl">Red Cards (Season)</div></div>
<div class="ref-stat"><div class="rs-val">${r.games}</div><div class="rs-lbl">Games Officiated</div></div>
</div>
<div class="ref-impact">⚡ ${r.impact}</div>`
          : '<div style="color:var(--dim);font-size:.7rem">Referee data not yet available</div>'

        const xgHTML = `<div style="display:grid;grid-template-columns:1fr 1fr;gap:12px;margin:8px 0">
<div style="padding:10px;background:rgba(255,255,255,.03);border-radius:8px;text-align:center">
<div style="font-size:.8rem;color:var(--hot)">xG</div>
<div style="font-size:1.2rem;font-weight:700;color:${hc}">${m.home.xg}</div>
<div style="font-size:.8rem;color:var(--dim)">xGA: ${m.home.xga}</div>
</div>
<div style="padding:10px;background:rgba(255,255,255,.03);border-radius:8px;text-align:center">
<div style="font-size:.8rem;color:var(--hot)">xG</div>
<div style="font-size:1.2rem;font-weight:700;color:${ac}">${m.away.xg}</div>
<div style="font-size:.8rem;color:var(--muted)">xGA: ${m.away.xga}</div>
</div></div>`

        const id = `m${i}`
        return `<div class="match-card">
<div class="match-header" style="background:linear-gradient(135deg,${hc}22,transparent,${ac}22)">
<div class="team-info"><img src="${m.home.badge}" style="background: transparent" alt="${m.home.name}" onerror="this.style.display='none'"><span class="name" style="color:${hc}">${m.home.name}</span><span class="pos">${m.home.pos}</span><div class="form-dots">${formDots(m.home.form)}</div></div>
<div style="text-align:center"><span class="vs">V</span><div style="font-size:.6rem;color:var(--dim);margin-top:2px">${m.ko}</div></div>
<div class="team-info"><img src="${m.away.badge}" style="background: transparent" alt="${m.away.name}" onerror="this.style.display='none'"><span class="name" style="color:${ac}">${m.away.name}</span><span class="pos">${m.away.pos}</span><div class="form-dots">${formDots(m.away.form)}</div></div>
</div>
<div class="match-meta"><span>📍 ${m.venue}</span><span>⏰ ${m.ko}</span><span>🏟️ ${m.matchday || 'Matchday 35'}</span><span>👨‍⚖️ ${m.referee ? m.referee.name : 'TBC'}</span></div>

<div class="tabs" id="tabs-${id}">
<button class="tab active" onclick="showTab('${id}',0)">📊 Stats</button>
<button class="tab" onclick="showTab('${id}',1)">🎯 Score</button>
<button class="tab" onclick="showTab('${id}',2)">🟨 Cards</button>
<button class="tab" onclick="showTab('${id}',3)">📈 xG & Form</button>
<button class="tab" onclick="showTab('${id}',4)">🔄 H2H</button>
<button class="tab" onclick="showTab('${id}',5)">💰 Odds</button>
<button class="tab" onclick="showTab('${id}',6)">🏥 Injuries</button>
<button class="tab" onclick="showTab('${id}',7)">👨‍⚖️ Referee</button>
</div>

<div class="tab-content active" id="${id}-0"><div class="table-scroll">${statsTable}</div></div>
<div class="tab-content" id="${id}-1">
<div class="score-pred">
<div style="text-align:center"><div class="lbl">Half-Time</div><div class="sc">${m.htScore}</div><div style="font-size:.6rem;color:var(--dim)">Confidence: ${m.htConf}</div></div>
<div style="width:1px;height:50px;background:rgba(255,255,255,.1)"></div>
<div style="text-align:center"><div class="lbl">Full-Time</div><div class="sc">${m.ftScore}</div><div style="font-size:.6rem;color:var(--dim)">Confidence: ${m.ftConf}</div></div>
<div style="width:1px;height:50px;background:rgba(255,255,255,.1)"></div>
<div style="text-align:center"><div class="lbl" style="background:linear-gradient(135deg,#f97316,#ef4444);-webkit-background-clip:text;-webkit-text-fill-color:transparent;font-weight:700">🔥 Bold (xG)</div><div class="sc" style="background:linear-gradient(135deg,#f97316,#ef4444);-webkit-background-clip:text;-webkit-text-fill-color:transparent">${m.boldScore}</div><div style="font-size:.6rem;color:#f97316">Based on xG/xGA</div></div>
</div>
<div class="motivation">${m.motivation}</div>
</div>
<div class="tab-content" id="${id}-2">${cardChips}</div>
<div class="tab-content" id="${id}-3">${xgHTML}
<div class="section-title">Season Averages Per Game</div>
<div class="table-scroll"><table><tr><th>Metric</th><th>${m.home.short}</th><th>${m.away.short}</th></tr>
<tr><td>Corners</td><td>${m.home.cornPG}</td><td>${m.away.cornPG}</td></tr>
<tr><td>Shots</td><td>${m.home.shotsPG}</td><td>${m.away.shotsPG}</td></tr>
<tr><td>Shots on Target</td><td>${m.home.sotPG}</td><td>${m.away.sotPG}</td></tr>
<tr><td>Fouls</td><td>${m.home.foulsPG}</td><td>${m.away.foulsPG}</td></tr>
<tr><td>Throw-ins</td><td>${m.home.throwsPG}</td><td>${m.away.throwsPG}</td></tr>
<tr><td>Tackles</td><td>${m.home.tacklePG}</td><td>${m.away.tacklePG}</td></tr>
<tr><td>Offsides</td><td>${m.home.offsidePG}</td><td>${m.away.offsidePG}</td></tr>
</table></div>
</div>
<div class="tab-content" id="${id}-4">
<div class="section-title">Last 5 Meetings</div>${h2hHTML}
</div>
<div class="tab-content" id="${id}-5">
<div class="odds-grid">
<div class="odds-box"><div class="label">${m.home.name}</div><div class="val">${m.odds.h}</div></div>
<div class="odds-box"><div class="label">Draw</div><div class="val">${m.odds.d}</div></div>
<div class="odds-box"><div class="label">${m.away.name}</div><div class="val">${m.odds.a}</div></div>
</div>
<div class="motivation">${m.motivation}</div>
</div>
<div class="tab-content" id="${id}-6">${injHTML}</div>
<div class="tab-content" id="${id}-7">${refHTML}</div>
</div>`
      }

      function showTab(id, n) {
        document
          .querySelectorAll(`#tabs-${id} .tab`)
          .forEach((t, i) => t.classList.toggle('active', i === n))
        for (let i = 0; i < 8; i++) {
          const el = document.getElementById(`${id}-${i}`)
          if (el) el.classList.toggle('active', i === n)
        }
      }

      document.getElementById('app').innerHTML = M.map((m, i) =>
        renderMatch(m, i),
      ).join('')
    </script>
