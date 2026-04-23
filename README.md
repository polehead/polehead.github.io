<html lang="en">

<head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width,initial-scale=1" />
    <title>PL Matchday 35 Predictions – 25 Apr 2026</title>
    <meta name="description" content="Data-driven Premier League predictions for April 25 2026 fixtures" />
    <link href="https://fonts.googleapis.com/css2?family=Inter:wght@300;400;500;600;700;800;900&display=swap"
        rel="stylesheet" />
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        :root {
            --bg: #0a0e1a;
            --card: #111827;
            --card2: #1a2236;
            --text: #e2e8f0;
            --dim: #94a3b8;
            --accent: #6366f1;
            --glow: rgba(99, 102, 241, 0.15);
        }

        body {
            font-family: 'Segoe UI', Roboto, Helvetica, Arial, sans-serif;
            background: var(--bg);
            color: var(--text);
            margin: 0;
            padding: 20px;
            line-height: 1.6;
            min-height: 100vh;
            overflow-x: hidden;
        }

        .hero {
            text-align: center;
            padding: 40px 20px 20px;
            background: linear-gradient(135deg,
                    #0f172a 0%,
                    #1e1b4b 50%,
                    #0f172a 100%);
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
        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 20px 16px;
        }

        .match-card {
            background: var(--card);
            border-radius: 16px;
            margin-bottom: 28px;
            overflow: hidden;
            border: 1px solid rgba(255, 255, 255, 0.06);
            box-shadow: 0 4px 24px rgba(0, 0, 0, 0.3);
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
        }

        td {
            padding: 6px 8px;
            border-bottom: 1px solid rgba(255, 255, 255, 0.03);
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

        @media (max-width: 600px) {
            .match-header {
                flex-wrap: wrap;
                gap: 8px;
                padding: 14px;
            }

            .team-info img {
                width: 40px;
                height: 40px;
            }

            .team-info .name {
                font-size: 0.75rem;
            }

            .tab {
                padding: 6px 10px;
                font-size: 0.63rem;
            }

            .tab-content {
                padding: 10px;
                margin: 0 6px 8px;
            }

            table {
                font-size: 0.65rem;
            }

            th,
            td {
                padding: 4px 5px;
            }

            .odds-grid {
                grid-template-columns: repeat(3, 1fr);
                gap: 4px;
            }

            .score-pred .sc {
                font-size: 1.4rem;
            }
        }
    </style>
</head>

<body>
    <header class="page-hd">
    <div class="pl-badge">
      Team Bilbo Analytics
    </div>
    <h2>Premier League Predictions</h2>
    <p class="sub">Fixture Analysis & Predictive Modeling · 22 April 2026</p>
  </header>
    <div class="container" id="app"></div>
    <div class="disclaimer" style="text-align:center;padding:20px 16px;font-size:10px;color:var(--dim);border-top:1px solid var(--accent);position:relative;z-index:1">
    <p><strong>Professional Strategy Analytics</strong><br /></p>
    <p style="margin-top: 4px;">
      Statistical predictions are weighted estimates based on historical data and form analysis.<br /><br>
      <strong style="color: #fbbf24;">ALWAYS GAMBLE RESPONSIBLY, THIS IS NOT FINANCIAL
        ADVICE</strong>
    </p>
    </div>

    <script>
        const M = [
            {
                home: {
                    name: 'Fulham',
                    short: 'FUL',
                    pos: '12th (45pts)',
                    badge:
                        'https://cdn.brandfetch.io/idJTNo1NC-/theme/dark/logo.svg?c=1bxid64Mup7aczewSAYMX&t=1774916217250',
                    color: '#e2e8f0',
                    color2: '#fff',
                    form: ['L', 'D', 'L', 'D', 'W'],
                    xg: 1.28,
                    xga: 1.41,
                    cornPG: 4.79,
                    shotsPG: 11.2,
                    sotPG: 3.61,
                    foulsPG: 10.79,
                    throwsPG: 19.88,
                    gkPG: 5.1,
                    tacklePG: 16.8,
                    injuries: [
                        'K. Tete (foot)',
                        'A. Iwobi (hamstring, doubtful)',
                        'H. Reed (knee)',
                    ],
                    cardPlayers: [
                        { n: 'J. Andersen', c: 7, pct: '42%' },
                        { n: 'S. Lukić', c: 7, pct: '40%' },
                        { n: 'T. Cairney', c: 5, pct: '30%' },
                        { n: 'A. Robinson', c: 4, pct: '25%' },
                    ],
                },
                away: {
                    name: 'Aston Villa',
                    short: 'AVL',
                    pos: '4th (58pts)',
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
                    injuries: ['B. Kamara (knee, season)', 'B. Traoré (knee)'],
                    cardPlayers: [
                        { n: 'M. Cash', c: 6, pct: '38%' },
                        { n: 'E. Buendía', c: 5, pct: '34%' },
                        { n: 'L. Bogarde', c: 5, pct: '32%' },
                        { n: 'L. Bailey', c: 4, pct: '28%' },
                    ],
                },
                ko: '12:30',
                venue: 'Craven Cottage',
                ref: 'TBC',
                h2h: [
                    'AVL 3-1 FUL (Sep 25)',
                    'AVL 1-0 FUL (May 25)',
                    'FUL 1-3 AVL (Oct 24)',
                    'FUL 1-2 AVL (Feb 24)',
                    'AVL 3-1 FUL (Nov 23)',
                ],
                odds: { h: '17/10', d: '13/5', a: '8/5' },
                motivation:
                    '🏆 Villa chasing top-4 for Champions League. Fulham comfortable in mid-table but struggling — failed to score in 5 of last 6. Villa on 6-game unbeaten run with 14 goals in last 5.',
                stats: {
                    corners: { low: 7, med: 10, high: 13, safe: 9, h: 4, a: 6 },
                    shots: { low: 17, med: 23, high: 29, safe: 22, h: 10, a: 13 },
                    sot: { low: 5, med: 8, high: 11, safe: 7, h: 3, a: 5 },
                    fouls: { low: 15, med: 21, high: 27, safe: 20, h: 11, a: 10 },
                    throws: { low: 32, med: 40, high: 48, safe: 39, h: 19, a: 21 },
                    gk: { low: 6, med: 10, high: 14, safe: 9, h: 5, a: 5 },
                    tackles: { low: 26, med: 34, high: 42, safe: 33, h: 16, a: 18 },
                },
                htScore: '0-1',
                ftScore: '0-2',
                htConf: '62%',
                ftConf: '45%',
            },

            {
                home: {
                    name: 'Liverpool',
                    short: 'LIV',
                    pos: '5th (55pts)',
                    badge:
                        'https://cdn.brandfetch.io/idLw_x5PBk/w/185/h/185/theme/dark/logo.webp?c=1bxid64Mup7aczewSAYMX&t=1746516677234',
                    color: '#C8102E',
                    color2: '#00B2A9',
                    form: ['W', 'W', 'L', 'W', 'D'],
                    xg: 1.65,
                    xga: 1.18,
                    cornPG: 5.97,
                    shotsPG: 14.6,
                    sotPG: 5.2,
                    foulsPG: 9.8,
                    throwsPG: 21.3,
                    gkPG: 4.2,
                    tacklePG: 17.5,
                    injuries: [
                        'Alisson (muscle)',
                        'G. Mamardashvili (knee)',
                        'H. Ekitike (Achilles, season)',
                        'W. Endo (ankle, season)',
                        'C. Bradley (knee)',
                        'G. Leoni (ACL)',
                        'J. Gomez (knock)',
                    ],
                    cardPlayers: [
                        { n: 'D. Szoboszlai', c: 7, pct: '40%' },
                        { n: 'R. Gravenberch', c: 5, pct: '32%' },
                        { n: 'V. van Dijk', c: 4, pct: '26%' },
                        { n: 'A. Mac Allister', c: 4, pct: '24%' },
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
                    cornPG: 4.19,
                    shotsPG: 12.4,
                    sotPG: 3.9,
                    foulsPG: 11.1,
                    throwsPG: 20.8,
                    gkPG: 5.3,
                    tacklePG: 18.6,
                    injuries: ['A. Wharton (returning)'],
                    cardPlayers: [
                        { n: 'T. Mitchell', c: 6, pct: '38%' },
                        { n: 'C. Doucoure', c: 5, pct: '34%' },
                        { n: 'W. Hughes', c: 5, pct: '30%' },
                        { n: 'M. Guéhi', c: 4, pct: '26%' },
                    ],
                },
                ko: '15:00',
                venue: 'Anfield',
                ref: 'TBC',
                h2h: [
                    'CRY 2-1 LIV (Sep 25)',
                    'LIV 1-1 CRY (May 25)',
                    'CRY 0-1 LIV (Oct 24)',
                    'LIV 0-1 CRY (Apr 24)',
                    'CRY 1-2 LIV (Dec 23)',
                ],
                odds: { h: '1/2', d: '15/4', a: '6/1' },
                motivation:
                    '🎯 Liverpool need wins to stay in top-4 race. Palace won all 3 meetings this season (incl. Community Shield & Carabao Cup). Liverpool have 9 players injured — GK crisis with 3rd choice Woodman expected to start.',
                stats: {
                    corners: { low: 7, med: 10, high: 14, safe: 10, h: 6, a: 4 },
                    shots: { low: 20, med: 27, high: 33, safe: 25, h: 15, a: 12 },
                    sot: { low: 6, med: 9, high: 13, safe: 9, h: 5, a: 4 },
                    fouls: { low: 14, med: 21, high: 27, safe: 20, h: 9, a: 12 },
                    throws: { low: 34, med: 42, high: 50, safe: 41, h: 22, a: 20 },
                    gk: { low: 5, med: 9, high: 14, safe: 9, h: 4, a: 5 },
                    tackles: { low: 28, med: 36, high: 44, safe: 35, h: 17, a: 19 },
                },
                htScore: '1-0',
                ftScore: '2-1',
                htConf: '48%',
                ftConf: '38%',
            },

            {
                home: {
                    name: 'West Ham Utd',
                    short: 'WHU',
                    pos: '17th (33pts)',
                    badge:
                        'https://cdn.brandfetch.io/idioDWtJyw/theme/dark/logo.svg?c=1bxid64Mup7aczewSAYMX&t=1668077966418',
                    color: '#7A263A',
                    color2: '#1BB1E7',
                    form: ['D', 'W', 'L', 'L', 'D'],
                    xg: 1.12,
                    xga: 1.56,
                    cornPG: 5.06,
                    shotsPG: 10.8,
                    sotPG: 3.4,
                    foulsPG: 11.3,
                    throwsPG: 20.1,
                    gkPG: 5.6,
                    tacklePG: 16.2,
                    injuries: ['Fully fit squad reported'],
                    cardPlayers: [
                        { n: 'L. Paquetá', c: 7, pct: '44%' },
                        { n: 'M. Fernandes', c: 7, pct: '40%' },
                        { n: 'T. Souček', c: 5, pct: '32%' },
                        { n: 'K. Mavropanos', c: 4, pct: '28%' },
                    ],
                },
                away: {
                    name: 'Everton',
                    short: 'EVE',
                    pos: '10th (47pts)',
                    badge:
                        'https://images.gc.evertonfcservices.co.uk/fit-in/170x170/e2faca70-1941-11ef-99c3-49ef9e747bf4.png',
                    color: '#003399',
                    color2: '#fff',
                    form: ['L', 'W', 'D', 'W', 'L'],
                    xg: 1.24,
                    xga: 1.49,
                    cornPG: 4.21,
                    shotsPG: 11.6,
                    sotPG: 3.8,
                    foulsPG: 10.5,
                    throwsPG: 19.6,
                    gkPG: 5.2,
                    tacklePG: 18.4,
                    injuries: [
                        'J. Branthwaite (hamstring, season)',
                        'J. Grealish (foot, long-term)',
                    ],
                    cardPlayers: [
                        { n: 'J. Garner', c: 9, pct: '48%' },
                        { n: 'V. Mykolenko', c: 5, pct: '32%' },
                        { n: 'I. Gueye', c: 5, pct: '30%' },
                        { n: 'A. Doucouré', c: 4, pct: '26%' },
                    ],
                },
                ko: '15:00',
                venue: 'London Stadium',
                ref: 'TBC',
                h2h: [
                    'EVE 1-1 WHU (Sep 25)',
                    'EVE 1-1 WHU (Mar 25)',
                    'WHU 0-0 EVE (Nov 24)',
                    'EVE 1-3 WHU (Mar 24)',
                    'WHU 0-1 EVE (Oct 23)',
                ],
                odds: { h: '6/4', d: '23/10', a: '2/1' },
                motivation:
                    '🔥 RELEGATION BATTLE: West Ham 17th, just 2pts above the drop zone. Massive 6-pointer at home — 4-0 win vs Wolves last time showed they can perform under pressure. Everton comfortable mid-table under Moyes.',
                stats: {
                    corners: { low: 6, med: 9, high: 13, safe: 9, h: 5, a: 4 },
                    shots: { low: 16, med: 22, high: 28, safe: 21, h: 11, a: 11 },
                    sot: { low: 4, med: 7, high: 11, safe: 7, h: 3, a: 4 },
                    fouls: { low: 16, med: 22, high: 28, safe: 21, h: 12, a: 10 },
                    throws: { low: 32, med: 40, high: 47, safe: 39, h: 21, a: 19 },
                    gk: { low: 7, med: 11, high: 15, safe: 10, h: 6, a: 5 },
                    tackles: { low: 26, med: 34, high: 42, safe: 33, h: 16, a: 18 },
                },
                htScore: '1-0',
                ftScore: '2-1',
                htConf: '40%',
                ftConf: '35%',
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
                    cornPG: 3.24,
                    shotsPG: 9.4,
                    sotPG: 2.8,
                    foulsPG: 13.1,
                    throwsPG: 21.2,
                    gkPG: 6.4,
                    tacklePG: 17.8,
                    injuries: [
                        'M. Mane (injury)',
                        'H. Hwang (injury)',
                        'E. Gonzalez (injury)',
                        'S. Johnstone (injury)',
                        'J. Sá (injury)',
                        'M. Doherty (injury)',
                    ],
                    cardPlayers: [
                        { n: 'Y. Mosquera', c: 11, pct: '52%', note: 'susp.' },
                        { n: 'J. Gomes', c: 8, pct: '46%' },
                        { n: 'M. Lemina', c: 6, pct: '38%' },
                        { n: 'N. Semedo', c: 5, pct: '32%' },
                    ],
                },
                away: {
                    name: 'Tottenham',
                    short: 'TOT',
                    pos: '18th (31pts)',
                    badge:
                        'https://cdn.brandfetch.io/id0hQSdBIF/theme/dark/logo.svg?c=1bxid64Mup7aczewSAYMX&t=1668069471694',
                    color: '#1b317f',
                    color2: '#fff',
                    form: ['D', 'L', 'L', 'D', 'L'],
                    xg: 1.18,
                    xga: 1.48,
                    cornPG: 5.27,
                    shotsPG: 13.2,
                    sotPG: 4.5,
                    foulsPG: 10.8,
                    throwsPG: 20.4,
                    gkPG: 4.9,
                    tacklePG: 17.1,
                    injuries: [
                        'C. Romero (knee, season)',
                        'W. Odobert (ACL)',
                        'D. Kulusevski (knee)',
                        'M. Kudus (thigh)',
                        'G. Vicario (groin)',
                        'B. Davies (ankle)',
                        'D. Udogie (doubtful)',
                    ],
                    cardPlayers: [
                        { n: 'C. Romero', c: 11, pct: 'N/A – out' },
                        { n: 'J. Palhinha', c: 8, pct: '46%' },
                        { n: 'Y. Bissouma', c: 6, pct: '38%' },
                        { n: 'R. Bentancur', c: 5, pct: '30%' },
                    ],
                },
                ko: '15:00',
                venue: 'Molineux',
                ref: 'TBC',
                h2h: [
                    'TOT 1-1 WOL (Sep 25)',
                    'WOL 4-2 TOT (Apr 25)',
                    'TOT 2-2 WOL (Dec 24)',
                    'TOT 1-2 WOL (Feb 24)',
                    'WOL 2-1 TOT (Nov 23)',
                ],
                odds: { h: '13/4', d: '13/5', a: '1/1' },
                motivation:
                    '⚠️ RELEGATION SIX-POINTER! Wolves already relegated but Spurs are 18th — 2pts behind safety. Spurs winless in 2026. Wolves have beaten Spurs in 3 of last 5. Both teams ravaged by injuries.',
                stats: {
                    corners: { low: 5, med: 8, high: 12, safe: 8, h: 3, a: 5 },
                    shots: { low: 16, med: 23, high: 29, safe: 21, h: 9, a: 14 },
                    sot: { low: 4, med: 7, high: 11, safe: 7, h: 3, a: 5 },
                    fouls: { low: 18, med: 24, high: 30, safe: 23, h: 14, a: 10 },
                    throws: { low: 34, med: 42, high: 49, safe: 41, h: 22, a: 20 },
                    gk: { low: 7, med: 11, high: 15, safe: 11, h: 6, a: 5 },
                    tackles: { low: 28, med: 35, high: 42, safe: 34, h: 18, a: 17 },
                },
                htScore: '0-1',
                ftScore: '1-2',
                htConf: '42%',
                ftConf: '36%',
            },

            {
                home: {
                    name: 'Arsenal',
                    short: 'ARS',
                    pos: '2nd (70pts)',
                    badge:
                        'https://cdn.brandfetch.io/ida744DnR8/theme/dark/logo.svg?c=1bxid64Mup7aczewSAYMX&t=1667609875130',
                    color: '#EF0107',
                    color2: '#063672',
                    form: ['L', 'L', 'W', 'W', 'W'],
                    xg: 1.72,
                    xga: 0.75,
                    cornPG: 5.94,
                    shotsPG: 15.1,
                    sotPG: 5.5,
                    foulsPG: 9.5,
                    throwsPG: 19.4,
                    gkPG: 3.8,
                    tacklePG: 17.9,
                    injuries: [
                        'B. Saka (Achilles, doubtful)',
                        'J. Timber (out)',
                        'R. Calafiori (out)',
                        'M. Merino (out)',
                    ],
                    cardPlayers: [
                        { n: 'R. Calafiori', c: 5, pct: 'N/A – out' },
                        { n: 'J. Timber', c: 5, pct: 'N/A – out' },
                        { n: 'V. Gyökeres', c: 5, pct: '30%' },
                        { n: 'D. Rice', c: 4, pct: '28%' },
                        { n: 'T. Partey', c: 4, pct: '26%' },
                    ],
                },
                away: {
                    name: 'Newcastle Utd',
                    short: 'NEW',
                    pos: '14th (42pts)',
                    badge:
                        'https://cdn.brandfetch.io/idXUqgf3Ge/theme/dark/logo.svg?c=1bxid64Mup7aczewSAYMX&t=1771886755450s://www.newcastleunited.com/_next/image?url=https%3A%2F%2Fimages.ctfassets.net%2F9ec6988xevcz%2F2j0nCJps49kwlviuhN4AcW%2F7175da7cdd7b6fac3351c7c66749b7dd%2FBlack_on_white_414x414.png%3Fh%3D120%26w%3D120&w=256&q=75',
                    color: '#e2e8f0',
                    color2: '#fff',
                    form: ['L', 'L', 'L', 'L', 'W'],
                    xg: 1.35,
                    xga: 1.38,
                    cornPG: 6.36,
                    shotsPG: 13.4,
                    sotPG: 4.6,
                    foulsPG: 11.2,
                    throwsPG: 20.6,
                    gkPG: 5.0,
                    tacklePG: 17.3,
                    injuries: [
                        'A. Gordon (hip)',
                        'T. Livramento (leg)',
                        'F. Schär (ankle)',
                        'E. Krafth (knee)',
                    ],
                    cardPlayers: [
                        { n: 'Joelinton', c: 10, pct: '50%' },
                        { n: 'S. Longstaff', c: 6, pct: '36%' },
                        { n: 'B. Guimarães', c: 5, pct: '30%' },
                        { n: 'D. Burn', c: 4, pct: '26%' },
                    ],
                },
                ko: '17:30',
                venue: 'Emirates Stadium',
                ref: 'TBC',
                h2h: [
                    'NEW 1-2 ARS (Sep 25)',
                    'ARS 1-0 NEW (May 25)',
                    'NEW 1-0 ARS (Nov 24)',
                    'ARS 4-1 NEW (Feb 24)',
                    'NEW 1-0 ARS (Nov 23)',
                ],
                odds: { h: '1/2', d: '7/2', a: '11/2' },
                motivation:
                    '🏆 TITLE RACE! Arsenal level on points with Man City at the top. Back-to-back losses vs Bournemouth & City — must win. Saka doubtful. Newcastle lost 4 in a row but Ødegaard returned. Gordon missing.',
                stats: {
                    corners: { low: 8, med: 12, high: 16, safe: 11, h: 6, a: 6 },
                    shots: { low: 21, med: 28, high: 35, safe: 27, h: 16, a: 12 },
                    sot: { low: 6, med: 10, high: 14, safe: 9, h: 6, a: 4 },
                    fouls: { low: 14, med: 20, high: 27, safe: 20, h: 9, a: 12 },
                    throws: { low: 32, med: 40, high: 48, safe: 39, h: 19, a: 21 },
                    gk: { low: 5, med: 9, high: 13, safe: 8, h: 4, a: 5 },
                    tackles: { low: 28, med: 35, high: 43, safe: 34, h: 18, a: 17 },
                },
                htScore: '1-0',
                ftScore: '2-0',
                htConf: '52%',
                ftConf: '42%',
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

            const xgHTML = `<div style="display:grid;grid-template-columns:1fr 1fr;gap:12px;margin:8px 0">
<div style="padding:10px;background:rgba(255,255,255,.03);border-radius:8px;text-align:center">
<div style="font-size:.65rem;color:var(--dim)">${m.home.short} xG/game</div>
<div style="font-size:1.2rem;font-weight:700;color:${hc}">${m.home.xg}</div>
<div style="font-size:.6rem;color:var(--dim)">xGA: ${m.home.xga}</div>
</div>
<div style="padding:10px;background:rgba(255,255,255,.03);border-radius:8px;text-align:center">
<div style="font-size:.65rem;color:var(--dim)">${m.away.short} xG/game</div>
<div style="font-size:1.2rem;font-weight:700;color:${ac}">${m.away.xg}</div>
<div style="font-size:.6rem;color:var(--dim)">xGA: ${m.away.xga}</div>
</div></div>`

            const id = `m${i}`
            return `<div class="match-card">
<div class="match-header" style="background:linear-gradient(135deg,${hc}22,transparent,${ac}22)">
<div class="team-info"><img src="${m.home.badge}" style="background: transparent" alt="${m.home.name}" onerror="this.style.display='none'"><span class="name" style="color:${hc}">${m.home.name}</span><span class="pos">${m.home.pos}</span><div class="form-dots">${formDots(m.home.form)}</div></div>
<div style="text-align:center"><span class="vs">VS</span><div style="font-size:.6rem;color:var(--dim);margin-top:2px">${m.ko}</div></div>
<div class="team-info"><img src="${m.away.badge}" style="background: transparent" alt="${m.away.name}" onerror="this.style.display='none'"><span class="name" style="color:${ac}">${m.away.name}</span><span class="pos">${m.away.pos}</span><div class="form-dots">${formDots(m.away.form)}</div></div>
</div>
<div class="match-meta"><span>📍 ${m.venue}</span><span>⏰ ${m.ko}</span><span>🏟️ Matchday 35</span></div>

<div class="tabs" id="tabs-${id}">
<button class="tab active" onclick="showTab('${id}',0)">📊 Stats</button>
<button class="tab" onclick="showTab('${id}',1)">🎯 Score</button>
<button class="tab" onclick="showTab('${id}',2)">🟨 Cards</button>
<button class="tab" onclick="showTab('${id}',3)">📈 xG & Form</button>
<button class="tab" onclick="showTab('${id}',4)">🔄 H2H</button>
<button class="tab" onclick="showTab('${id}',5)">💰 Odds</button>
<button class="tab" onclick="showTab('${id}',6)">🏥 Injuries</button>
</div>

<div class="tab-content active" id="${id}-0">${statsTable}</div>
<div class="tab-content" id="${id}-1">
<div class="score-pred">
<div style="text-align:center"><div class="lbl">Half-Time</div><div class="sc">${m.htScore}</div><div style="font-size:.6rem;color:var(--dim)">Confidence: ${m.htConf}</div></div>
<div style="width:1px;height:50px;background:rgba(255,255,255,.1)"></div>
<div style="text-align:center"><div class="lbl">Full-Time</div><div class="sc">${m.ftScore}</div><div style="font-size:.6rem;color:var(--dim)">Confidence: ${m.ftConf}</div></div>
</div>
<div class="motivation">${m.motivation}</div>
</div>
<div class="tab-content" id="${id}-2">${cardChips}</div>
<div class="tab-content" id="${id}-3">${xgHTML}
<div class="section-title">Season Averages Per Game</div>
<table><tr><th>Metric</th><th>${m.home.short}</th><th>${m.away.short}</th></tr>
<tr><td>Corners</td><td>${m.home.cornPG}</td><td>${m.away.cornPG}</td></tr>
<tr><td>Shots</td><td>${m.home.shotsPG}</td><td>${m.away.shotsPG}</td></tr>
<tr><td>Shots on Target</td><td>${m.home.sotPG}</td><td>${m.away.sotPG}</td></tr>
<tr><td>Fouls</td><td>${m.home.foulsPG}</td><td>${m.away.foulsPG}</td></tr>
<tr><td>Throw-ins</td><td>${m.home.throwsPG}</td><td>${m.away.throwsPG}</td></tr>
<tr><td>Tackles</td><td>${m.home.tacklePG}</td><td>${m.away.tacklePG}</td></tr>
</table>
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
</div>`
        }

        function showTab(id, n) {
            document
                .querySelectorAll(`#tabs-${id} .tab`)
                .forEach((t, i) => t.classList.toggle('active', i === n))
            for (let i = 0; i < 7; i++) {
                const el = document.getElementById(`${id}-${i}`)
                if (el) el.classList.toggle('active', i === n)
            }
        }

        document.getElementById('app').innerHTML = M.map((m, i) =>
            renderMatch(m, i),
        ).join('')
    </script>
