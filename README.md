<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>West Ham vs Wolves | PL Match Predictor</title>
    <meta
      name="description"
      content="Data-driven match prediction for West Ham United vs Wolverhampton Wanderers - Premier League 2025/26"
    />
    <link
      href="https://fonts.googleapis.com/css2?family=Inter:wght@300;400;500;600;700;800;900&display=swap"
      rel="stylesheet"
    />
    <style>
      *,
      *::before,
      *::after {
        box-sizing: border-box;
        margin: 0;
        padding: 0;
      }
      :root {
        --bg-primary: #0a0e1a;
        --bg-card: #111827;
        --bg-card-alt: #1a2236;
        --claret: #7c2d3e;
        --claret-glow: #a8405a;
        --gold: #d4a843;
        --gold-light: #f0d078;
        --wolves-gold: #fdb913;
        --wolves-dark: #231f20;
        --text-primary: #f1f5f9;
        --text-secondary: #94a3b8;
        --text-muted: #64748b;
        --accent-blue: #3b82f6;
        --accent-green: #10b981;
        --accent-red: #ef4444;
        --accent-purple: #8b5cf6;
        --accent-orange: #f97316;
        --glass: rgba(255, 255, 255, 0.04);
        --glass-border: rgba(255, 255, 255, 0.08);
        --radius: 14px;
        --radius-sm: 8px;
      }
      html {
        scroll-behavior: smooth;
      }
      body {
        font-family: "Inter", sans-serif;
        background: var(--bg-primary);
        color: var(--text-primary);
        min-height: 100vh;
        overflow-x: hidden;
        line-height: 1.5;
      }
      body::before {
        content: "";
        position: fixed;
        inset: 0;
        background:
          radial-gradient(
            ellipse at 20% 0%,
            rgba(124, 45, 62, 0.15),
            transparent 50%
          ),
          radial-gradient(
            ellipse at 80% 0%,
            rgba(253, 185, 19, 0.1),
            transparent 50%
          );
        pointer-events: none;
        z-index: 0;
      }

      .container {
        max-width: 1100px;
        margin: 0 auto;
        padding: 0 16px;
        position: relative;
        z-index: 1;
      }

      /* HEADER */
      .match-header {
        text-align: center;
        padding: 28px 0 18px;
        animation: fadeDown 0.8s ease;
      }
      .match-meta {
        display: flex;
        align-items: center;
        justify-content: center;
        gap: 8px;
        flex-wrap: wrap;
        font-size: 0.75rem;
        color: var(--text-muted);
        text-transform: uppercase;
        letter-spacing: 1.5px;
        margin-bottom: 14px;
      }
      .meta-badge {
        background: var(--accent-red);
        color: #fff;
        padding: 3px 10px;
        border-radius: 20px;
        font-weight: 700;
        font-size: 0.65rem;
        animation: pulse 2s infinite;
      }
      .match-title {
        font-size: clamp(1rem, 4vw, 1.3rem);
        font-weight: 300;
        color: var(--text-secondary);
        margin-bottom: 6px;
        letter-spacing: 0.5px;
      }

      /* TEAMS */
      .teams-showcase {
        display: flex;
        align-items: center;
        justify-content: center;
        gap: clamp(16px, 5vw, 48px);
        padding: 18px 0 22px;
        animation: fadeUp 0.8s ease 0.2s both;
      }
      .team-block {
        display: flex;
        flex-direction: column;
        align-items: center;
        gap: 8px;
        flex: 1;
        max-width: 200px;
      }
      .team-badge {
        width: clamp(56px, 15vw, 90px);
        height: clamp(56px, 15vw, 90px);
        object-fit: contain;
        filter: drop-shadow(0 4px 20px rgba(0, 0, 0, 0.5));
        transition: transform 0.4s;
      }
      .team-badge:hover {
        transform: scale(1.12) rotate(-3deg);
      }
      .team-name {
        font-size: clamp(0.85rem, 3vw, 1.15rem);
        font-weight: 700;
        letter-spacing: 0.5px;
      }
      .team-form {
        display: flex;
        gap: 4px;
        margin-top: 4px;
      }
      .form-dot {
        width: 22px;
        height: 22px;
        border-radius: 50%;
        display: flex;
        align-items: center;
        justify-content: center;
        font-size: 0.6rem;
        font-weight: 700;
        color: #fff;
      }
      .form-W {
        background: var(--accent-green);
      }
      .form-D {
        background: var(--accent-orange);
      }
      .form-L {
        background: var(--accent-red);
      }
      .vs-divider {
        font-size: clamp(1.2rem, 4vw, 1.8rem);
        font-weight: 900;
        background: linear-gradient(
          135deg,
          var(--claret-glow),
          var(--wolves-gold)
        );
        -webkit-background-clip: text;
        -webkit-text-fill-color: transparent;
        letter-spacing: 2px;
      }
      .team-position {
        font-size: 0.7rem;
        color: var(--text-muted);
        padding: 2px 10px;
        border-radius: 20px;
        border: 1px solid var(--glass-border);
        margin-top: 2px;
      }

      /* CONTEXT ALERT */
      .context-alert {
        background: linear-gradient(
          135deg,
          rgba(239, 68, 68, 0.12),
          rgba(249, 115, 22, 0.08)
        );
        border: 1px solid rgba(239, 68, 68, 0.2);
        border-radius: var(--radius);
        padding: 14px 18px;
        margin: 0 0 24px;
        animation: fadeUp 0.8s ease 0.4s both;
      }
      .context-alert h3 {
        font-size: 0.8rem;
        color: var(--accent-orange);
        margin-bottom: 6px;
        display: flex;
        align-items: center;
        gap: 6px;
      }
      .context-alert p {
        font-size: 0.75rem;
        color: var(--text-secondary);
        line-height: 1.6;
      }

      /* NAV TABS */
      .tab-nav {
        display: flex;
        gap: 6px;
        overflow-x: auto;
        padding: 0 0 16px;
        margin-bottom: 20px;
        scrollbar-width: none;
        -ms-overflow-style: none;
        animation: fadeUp 0.8s ease 0.5s both;
      }
      .tab-nav::-webkit-scrollbar {
        display: none;
      }
      .tab-btn {
        flex-shrink: 0;
        padding: 8px 18px;
        border-radius: 24px;
        border: 1px solid var(--glass-border);
        background: var(--glass);
        color: var(--text-secondary);
        font-size: 0.75rem;
        font-weight: 600;
        cursor: pointer;
        transition: all 0.3s;
        font-family: inherit;
        white-space: nowrap;
      }
      .tab-btn.active,
      .tab-btn:hover {
        background: linear-gradient(135deg, var(--claret), var(--claret-glow));
        color: #fff;
        border-color: var(--claret-glow);
        transform: translateY(-1px);
      }

      /* SECTIONS */
      .section {
        display: none;
        animation: fadeUp 0.5s ease;
      }
      .section.active {
        display: block;
      }
      .section-title {
        font-size: clamp(0.9rem, 3vw, 1.1rem);
        font-weight: 700;
        margin-bottom: 16px;
        padding-bottom: 8px;
        border-bottom: 1px solid var(--glass-border);
        display: flex;
        align-items: center;
        gap: 8px;
      }
      .section-title span {
        font-size: 1.1em;
      }

      /* PREDICTION BARS */
      .pred-grid {
        display: grid;
        gap: 12px;
        margin-bottom: 28px;
      }
      .pred-card {
        background: var(--bg-card);
        border: 1px solid var(--glass-border);
        border-radius: var(--radius);
        padding: 16px;
        transition:
          transform 0.3s,
          box-shadow 0.3s;
      }
      .pred-card:hover {
        transform: translateY(-2px);
        box-shadow: 0 8px 30px rgba(0, 0, 0, 0.3);
      }
      .pred-label {
        font-size: 0.72rem;
        color: var(--text-muted);
        text-transform: uppercase;
        letter-spacing: 1px;
        margin-bottom: 10px;
        font-weight: 600;
      }
      .pred-values {
        display: grid;
        grid-template-columns: 1fr 1fr 1fr;
        gap: 8px;
      }
      .pred-item {
        text-align: center;
      }
      .pred-item-label {
        font-size: 0.6rem;
        color: var(--text-muted);
        text-transform: uppercase;
        letter-spacing: 0.5px;
        margin-bottom: 6px;
      }
      .bar-wrap {
        height: 8px;
        background: rgba(255, 255, 255, 0.06);
        border-radius: 4px;
        overflow: hidden;
        margin-bottom: 4px;
      }
      .bar-fill {
        height: 100%;
        border-radius: 4px;
        width: 0;
        transition: width 1.5s cubic-bezier(0.4, 0, 0.2, 1);
      }
      .bar-fill.low {
        background: linear-gradient(
          90deg,
          var(--accent-blue),
          var(--accent-purple)
        );
      }
      .bar-fill.med {
        background: linear-gradient(
          90deg,
          var(--accent-green),
          var(--accent-blue)
        );
      }
      .bar-fill.high {
        background: linear-gradient(
          90deg,
          var(--accent-orange),
          var(--accent-red)
        );
      }
      .pred-num {
        font-size: clamp(1rem, 3vw, 1.3rem);
        font-weight: 800;
      }
      .pred-num.low-c {
        color: var(--accent-blue);
      }
      .pred-num.med-c {
        color: var(--accent-green);
      }
      .pred-num.high-c {
        color: var(--accent-orange);
      }

      /* MATCH CARDS (Last 5) */
      .match-list {
        display: grid;
        gap: 8px;
        margin-bottom: 24px;
      }
      .match-row {
        display: grid;
        grid-template-columns: minmax(0, 1fr) auto minmax(0, 1fr);
        align-items: center;
        gap: 8px;
        background: var(--bg-card);
        border: 1px solid var(--glass-border);
        border-radius: var(--radius-sm);
        padding: 10px 14px;
        transition: transform 0.3s;
      }
      .match-row:hover {
        transform: translateX(4px);
      }
      .match-home {
        text-align: right;
        font-size: 0.78rem;
        font-weight: 500;
      }
      .match-away {
        text-align: left;
        font-size: 0.78rem;
        font-weight: 500;
      }
      .match-score {
        background: var(--bg-card-alt);
        padding: 4px 10px;
        border-radius: 6px;
        font-size: 0.8rem;
        font-weight: 800;
        min-width: 48px;
        text-align: center;
        white-space: nowrap;
      }
      .match-score.win {
        color: var(--accent-green);
      }
      .match-score.loss {
        color: var(--accent-red);
      }
      .match-score.draw {
        color: var(--accent-orange);
      }
      .match-date {
        font-size: 0.6rem;
        color: var(--text-muted);
        margin-top: 2px;
      }

      /* H2H */
      .h2h-card {
        background: var(--bg-card);
        border: 1px solid var(--glass-border);
        border-radius: var(--radius);
        padding: 16px;
        margin-bottom: 12px;
      }
      .h2h-header {
        display: flex;
        justify-content: space-between;
        align-items: center;
        margin-bottom: 8px;
      }
      .h2h-result {
        font-size: 0.8rem;
        font-weight: 700;
      }

      /* YELLOW CARD PREDICTION */
      .card-grid {
        display: grid;
        grid-template-columns: 1fr 1fr;
        gap: 12px;
        margin-bottom: 24px;
      }
      @media (max-width: 480px) {
        .card-grid {
          grid-template-columns: 1fr;
        }
      }
      .card-team {
        background: var(--bg-card);
        border: 1px solid var(--glass-border);
        border-radius: var(--radius);
        padding: 16px;
      }
      .card-team-header {
        font-size: 0.8rem;
        font-weight: 700;
        margin-bottom: 12px;
        display: flex;
        align-items: center;
        gap: 6px;
      }
      .player-card {
        display: flex;
        justify-content: space-between;
        align-items: center;
        padding: 8px 0;
        border-bottom: 1px solid var(--glass-border);
      }
      .player-card:last-child {
        border-bottom: none;
      }
      .player-name {
        font-size: 0.78rem;
        font-weight: 500;
      }
      .player-risk {
        font-size: 0.65rem;
        font-weight: 700;
        padding: 3px 8px;
        border-radius: 12px;
      }
      .risk-high {
        background: rgba(239, 68, 68, 0.15);
        color: var(--accent-red);
      }
      .risk-med {
        background: rgba(249, 115, 22, 0.15);
        color: var(--accent-orange);
      }
      .risk-low {
        background: rgba(59, 130, 246, 0.15);
        color: var(--accent-blue);
      }
      .player-yellows {
        font-size: 0.65rem;
        color: var(--text-muted);
      }

      /* SEASON AVG TABLE */
      .stats-table {
        width: 100%;
        border-collapse: collapse;
        margin-bottom: 24px;
        font-size: 0.78rem;
      }
      .stats-table th {
        background: var(--bg-card-alt);
        padding: 10px 12px;
        text-align: left;
        font-weight: 600;
        color: var(--text-muted);
        text-transform: uppercase;
        font-size: 0.65rem;
        letter-spacing: 1px;
        position: sticky;
        top: 0;
      }
      .stats-table td {
        padding: 10px 12px;
        border-bottom: 1px solid var(--glass-border);
      }
      .stats-table tr:hover td {
        background: rgba(255, 255, 255, 0.02);
      }
      .stats-table .team-col {
        font-weight: 600;
        white-space: nowrap;
      }
      .table-wrap {
        overflow-x: auto;
        border-radius: var(--radius);
        border: 1px solid var(--glass-border);
        margin-bottom: 24px;
      }

      /* METHODOLOGY */
      .method-box {
        background: var(--bg-card);
        border: 1px solid var(--glass-border);
        border-radius: var(--radius);
        padding: 16px;
        margin-bottom: 24px;
        font-size: 0.75rem;
        color: var(--text-secondary);
        line-height: 1.7;
      }
      .method-box h4 {
        color: var(--text-primary);
        margin-bottom: 8px;
        font-size: 0.8rem;
      }
      .weight-tag {
        display: inline-block;
        padding: 2px 8px;
        border-radius: 10px;
        font-size: 0.6rem;
        font-weight: 700;
        margin: 2px;
      }
      .w-season {
        background: rgba(59, 130, 246, 0.15);
        color: var(--accent-blue);
      }
      .w-form {
        background: rgba(16, 185, 129, 0.15);
        color: var(--accent-green);
      }
      .w-h2h {
        background: rgba(139, 92, 246, 0.15);
        color: var(--accent-purple);
      }
      .w-context {
        background: rgba(249, 115, 22, 0.15);
        color: var(--accent-orange);
      }

      /* FOOTER */
      footer {
        text-align: center;
        padding: 28px 0;
        font-size: 0.65rem;
        color: var(--text-muted);
        border-top: 1px solid var(--glass-border);
        margin-top: 20px;
      }

      /* ANIMATIONS */
      @keyframes fadeDown {
        from {
          opacity: 0;
          transform: translateY(-20px);
        }
        to {
          opacity: 1;
          transform: translateY(0);
        }
      }
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
      @keyframes pulse {
        0%,
        100% {
          opacity: 1;
        }
        50% {
          opacity: 0.6;
        }
      }

      /* TABLET */
      @media (min-width: 600px) {
        .pred-grid {
          grid-template-columns: 1fr 1fr;
        }
        .container {
          padding: 0 24px;
        }
      }
      /* DESKTOP */
      @media (min-width: 900px) {
        .pred-grid {
          grid-template-columns: 1fr 1fr;
        }
        .container {
          padding: 0 40px;
        }
        .match-list {
          grid-template-columns: 1fr 1fr;
        }
      }
    </style>
  </head>
  <body>
    <div class="container">
      <!-- HEADER -->
      <header class="match-header">
        <div class="match-meta">
          <span class="meta-badge">TEAM BILBO</span>
          <span>Premier League</span>
        </div>
        <div class="match-title">London Stadium — Matchweek 32</div>

        <div class="teams-showcase">
          <div class="team-block">
            <img
              class="team-badge"
              src="https://resources.premierleague.com/premierleague/badges/rb/t21.svg"
              alt="West Ham United"
            />
            <div class="team-name">West Ham</div>
            <div class="team-position">18th · 29 pts</div>
            <div class="team-form">
              <span class="form-dot form-L">L</span>
              <span class="form-dot form-D">D</span>
              <span class="form-dot form-W">W</span>
              <span class="form-dot form-D">D</span>
              <span class="form-dot form-L">L</span>
            </div>
          </div>
          <div class="vs-divider">VS</div>
          <div class="team-block">
            <img
              class="team-badge"
              src="https://resources.premierleague.com/premierleague/badges/rb/t39.svg"
              alt="Wolverhampton Wanderers"
            />
            <div class="team-name">Wolves</div>
            <div class="team-position">20th · 17 pts</div>
            <div class="team-form">
              <span class="form-dot form-D">D</span>
              <span class="form-dot form-W">W</span>
              <span class="form-dot form-W">W</span>
              <span class="form-dot form-L">L</span>
              <span class="form-dot form-D">D</span>
            </div>
          </div>
        </div>
      </header>

      <!-- CONTEXT -->
      <div class="context-alert">
        <h3>📊 Key Context Factors</h3>
        <p>
          <strong>Relegation six-pointer:</strong> West Ham (18th) desperately
          need a win to climb from the drop zone. Wolves (20th, 17 pts) are
          virtually down but fighting. <strong>Fatigue:</strong> West Ham played
          120 mins in Sunday's FA Cup QF vs Leeds (lost on pens 4-2). Only 4
          days' rest. <strong>H2H:</strong> Wolves have won the last 3
          competitive meetings. No draws in the last 16 PL meetings between
          these sides. <strong>Jarrod Bowen</strong> has scored in each of his
          last 3 home PL games vs Wolves.
        </p>
      </div>

      <!-- NAV -->
      <nav class="tab-nav" role="tablist">
        <button class="tab-btn active" onclick="showTab('predictions')">
          ⚡ Predictions
        </button>
        <button class="tab-btn" onclick="showTab('form')">
          ⚽ Last 5 Matches
        </button>
        <button class="tab-btn" onclick="showTab('h2h')">
          ⚔️ Head to Head
        </button>
        <button class="tab-btn" onclick="showTab('season')">
          📈 Season Averages
        </button>
        <button class="tab-btn" onclick="showTab('cards')">
          🟨 Yellow Cards
        </button>
        <button class="tab-btn" onclick="showTab('method')">
          📊 Methodology
        </button>
      </nav>

      <!-- PREDICTIONS -->
      <section id="predictions" class="section active">
        <h2 class="section-title"><span>⚡</span> Weighted Predictions</h2>
        <div class="pred-grid" id="predGrid"></div>
      </section>

      <!-- LAST 5 -->
      <section id="form" class="section">
        <h2 class="section-title">
          <span>⚽</span> West Ham — Last 5 PL Matches
        </h2>
        <div class="match-list">
          <div class="match-row">
            <div class="match-home">
              Aston Villa
              <div class="match-date">22 Mar</div>
            </div>
            <div class="match-score loss">2 - 1</div>
            <div class="match-away">West Ham</div>
          </div>
          <div class="match-row">
            <div class="match-home">
              West Ham
              <div class="match-date">14 Mar</div>
            </div>
            <div class="match-score draw">1 - 1</div>
            <div class="match-away">Man City</div>
          </div>
          <div class="match-row">
            <div class="match-home">
              Fulham
              <div class="match-date">4 Mar</div>
            </div>
            <div class="match-score win">0 - 1</div>
            <div class="match-away">West Ham</div>
          </div>
          <div class="match-row">
            <div class="match-home">
              Liverpool
              <div class="match-date">28 Feb</div>
            </div>
            <div class="match-score loss">3 - 0</div>
            <div class="match-away">West Ham</div>
          </div>
          <div class="match-row">
            <div class="match-home">
              West Ham
              <div class="match-date">10 Feb</div>
            </div>
            <div class="match-score draw">1 - 1</div>
            <div class="match-away">Man Utd</div>
          </div>
        </div>
        <h2 class="section-title" style="margin-top: 18px">
          <span>⚽</span> Wolves — Last 5 PL Matches
        </h2>
        <div class="match-list">
          <div class="match-row">
            <div class="match-home">
              Wolves
              <div class="match-date">16 Mar</div>
            </div>
            <div class="match-score draw">2 - 2</div>
            <div class="match-away">Brentford</div>
          </div>
          <div class="match-row">
            <div class="match-home">
              Wolves
              <div class="match-date">3 Mar</div>
            </div>
            <div class="match-score win">2 - 1</div>
            <div class="match-away">Liverpool</div>
          </div>
          <div class="match-row">
            <div class="match-home">
              Wolves
              <div class="match-date">27 Feb</div>
            </div>
            <div class="match-score win">2 - 0</div>
            <div class="match-away">Aston Villa</div>
          </div>
          <div class="match-row">
            <div class="match-home">
              Crystal Palace
              <div class="match-date">22 Feb</div>
            </div>
            <div class="match-score loss">1 - 0</div>
            <div class="match-away">Wolves</div>
          </div>
          <div class="match-row">
            <div class="match-home">
              Wolves
              <div class="match-date">18 Feb</div>
            </div>
            <div class="match-score draw">2 - 2</div>
            <div class="match-away">Arsenal</div>
          </div>
        </div>
      </section>

      <!-- H2H -->
      <section id="h2h" class="section">
        <h2 class="section-title"><span>⚔️</span> Last 5 Head-to-Head (PL)</h2>
        <div class="match-list">
          <div class="match-row">
            <div class="match-home">
              Wolves
              <div class="match-date">3 Jan 2026</div>
            </div>
            <div class="match-score win">3 - 0</div>
            <div class="match-away">West Ham</div>
          </div>
          <div class="match-row">
            <div class="match-home">
              Wolves
              <div class="match-date">1 Apr 2025</div>
            </div>
            <div class="match-score win">1 - 0</div>
            <div class="match-away">West Ham</div>
          </div>
          <div class="match-row">
            <div class="match-home">
              West Ham
              <div class="match-date">9 Dec 2024</div>
            </div>
            <div class="match-score win">2 - 1</div>
            <div class="match-away">Wolves</div>
          </div>
          <div class="match-row">
            <div class="match-home">
              Wolves
              <div class="match-date">6 Apr 2024</div>
            </div>
            <div class="match-score loss">1 - 2</div>
            <div class="match-away">West Ham</div>
          </div>
          <div class="match-row">
            <div class="match-home">
              West Ham
              <div class="match-date">17 Dec 2023</div>
            </div>
            <div class="match-score win">3 - 0</div>
            <div class="match-away">Wolves</div>
          </div>
        </div>
        <div class="method-box" style="margin-top: 14px">
          <h4>H2H Insights</h4>
          <p>
            ▸ Wolves have won the last
            <strong>3 competitive meetings</strong> (incl. EFL Cup 3-2 in Aug
            2025).<br />
            ▸ <strong>No draws</strong> in the last 16 PL encounters between
            these sides.<br />
            ▸ H2H avg total corners: ~9.2 | H2H avg total fouls: ~24 | H2H avg
            total cards: ~4.6
          </p>
        </div>
      </section>

      <!-- SEASON AVERAGES -->
      <section id="season" class="section">
        <h2 class="section-title">
          <span>📈</span> Season Averages (Per Game)
        </h2>
        <div class="table-wrap">
          <table class="stats-table">
            <thead>
              <tr>
                <th>Metric</th>
                <th>West Ham</th>
                <th>Wolves</th>
                <th>Combined</th>
              </tr>
            </thead>
            <tbody>
              <tr>
                <td class="team-col">Shots</td>
                <td>10.13</td>
                <td>9.23</td>
                <td>19.36</td>
              </tr>
              <tr>
                <td class="team-col">Shots on Target</td>
                <td>3.35</td>
                <td>3.26</td>
                <td>6.61</td>
              </tr>
              <tr>
                <td class="team-col">Corners</td>
                <td>5.03</td>
                <td>3.19</td>
                <td>8.22</td>
              </tr>
              <tr>
                <td class="team-col">Fouls</td>
                <td>11.00</td>
                <td>13.16</td>
                <td>24.16</td>
              </tr>
              <tr>
                <td class="team-col">Tackles</td>
                <td>17.42</td>
                <td>18.48</td>
                <td>35.90</td>
              </tr>
              <tr>
                <td class="team-col">Offsides</td>
                <td>1.90</td>
                <td>1.39</td>
                <td>3.29</td>
              </tr>
              <tr>
                <td class="team-col">Throw-ins</td>
                <td>17.87</td>
                <td>~18.5</td>
                <td>~36.4</td>
              </tr>
              <tr>
                <td class="team-col">Goal Kicks</td>
                <td>~7.8</td>
                <td>8.35</td>
                <td>~16.2</td>
              </tr>
              <tr>
                <td class="team-col">Yellow Cards</td>
                <td>1.74</td>
                <td>2.16</td>
                <td>3.90</td>
              </tr>
            </tbody>
          </table>
        </div>
      </section>

      <!-- YELLOW CARDS -->
      <section id="cards" class="section">
        <h2 class="section-title"><span>🟨</span> Yellow Card Predictions</h2>
        <div class="card-grid">
          <div
            class="card-team"
            style="border-top: 3px solid var(--claret-glow)"
          >
            <div class="card-team-header">⬣ West Ham United</div>
            <div class="player-card">
              <div>
                <div class="player-name">Mateus Fernandes</div>
                <div class="player-yellows">6 YC this season</div>
              </div>
              <span class="player-risk risk-high">HIGH 72%</span>
            </div>
            <div class="player-card">
              <div>
                <div class="player-name">Jean-Clair Todibo</div>
                <div class="player-yellows">4 YC + 1 RC this season</div>
              </div>
              <span class="player-risk risk-high">HIGH 65%</span>
            </div>
            <div class="player-card">
              <div>
                <div class="player-name">Aaron Wan-Bissaka</div>
                <div class="player-yellows">4 YC this season</div>
              </div>
              <span class="player-risk risk-med">MED 48%</span>
            </div>
            <div class="player-card">
              <div>
                <div class="player-name">Tomáš Souček</div>
                <div class="player-yellows">2 YC + 1 RC this season</div>
              </div>
              <span class="player-risk risk-med">MED 40%</span>
            </div>
            <div class="player-card">
              <div>
                <div class="player-name">Jarrod Bowen</div>
                <div class="player-yellows">Aggressive pressing</div>
              </div>
              <span class="player-risk risk-low">LOW 22%</span>
            </div>
          </div>
          <div
            class="card-team"
            style="border-top: 3px solid var(--wolves-gold)"
          >
            <div class="card-team-header">🐺 Wolverhampton Wanderers</div>
            <div class="player-card">
              <div>
                <div class="player-name">Yerson Mosquera</div>
                <div class="player-yellows">10 YC this season</div>
              </div>
              <span class="player-risk risk-high">HIGH 78%</span>
            </div>
            <div class="player-card">
              <div>
                <div class="player-name">João Gomes</div>
                <div class="player-yellows">9 YC this season</div>
              </div>
              <span class="player-risk risk-high">HIGH 74%</span>
            </div>
            <div class="player-card">
              <div>
                <div class="player-name">André</div>
                <div class="player-yellows">9 YC this season</div>
              </div>
              <span class="player-risk risk-high">HIGH 71%</span>
            </div>
            <div class="player-card">
              <div>
                <div class="player-name">Jørgen Strand Larsen</div>
                <div class="player-yellows">Physical forward</div>
              </div>
              <span class="player-risk risk-med">MED 38%</span>
            </div>
            <div class="player-card">
              <div>
                <div class="player-name">Pablo Sarabia</div>
                <div class="player-yellows">Tactical fouling</div>
              </div>
              <span class="player-risk risk-low">LOW 25%</span>
            </div>
          </div>
        </div>
        <div class="method-box">
          <h4>Card Prediction Notes</h4>
          <p>
            Probabilities factor in: season booking rate per 90, match intensity
            (relegation battle), referee tendencies in high-stakes fixtures, and
            Wolves' notably high foul count (13.16/game). West Ham's fatigue
            from extra time Sunday may lead to more late/reckless challenges.
          </p>
        </div>
      </section>

      <!-- METHODOLOGY -->
      <section id="method" class="section">
        <h2 class="section-title"><span>📊</span> Prediction Methodology</h2>
        <div class="method-box">
          <h4>Weighted Model</h4>
          <p>Predictions use a weighted average of four data layers:</p>
          <p style="margin: 10px 0">
            <span class="weight-tag w-season">SEASON AVG 25%</span>
            <span class="weight-tag w-form">LAST 5 FORM 35%</span>
            <span class="weight-tag w-h2h">H2H RECORD 20%</span>
            <span class="weight-tag w-context">CONTEXT 20%</span>
          </p>
          <p>
            <strong>Context adjustments:</strong><br />
            ▸ West Ham fatigue (+5% fouls, -5% shots, +8% goal kicks) — only 4
            days after 120-min FA Cup tie.<br />
            ▸ Relegation intensity (+10% fouls, +8% cards, +6% tackles) — both
            teams fighting for survival.<br />
            ▸ Home advantage for West Ham (+10% corners, +5% shots) — 4 PL games
            unbeaten at London Stadium.<br />
            ▸ Wolves' recent surge (W2 D2 L1 in last 5) weighted higher than
            overall season record.<br />
            ▸ No draws in last 16 H2H meetings suggests decisive match → higher
            activity metrics.
          </p>
        </div>
      </section>
    </div>

    <footer>
      <div class="container">
        <p>
          <strong>TEAM BILBO Statistical Analysis</strong><br />Predictions are
          statistical estimates based on actual data, H2H analysis and
          contextual factors.
        </p>
        <p style="margin-top: 4px">
          <strong>Not financial advice.</strong>
        </p>
      </div>
    </footer>

    <script>
      const predictions = [
        { label: "Corners (Total)", low: 7, med: 9, high: 12, max: 16 },
        { label: "Shots (Total)", low: 16, med: 20, high: 25, max: 30 },
        { label: "Shots on Target", low: 5, med: 7, high: 10, max: 14 },
        { label: "Fouls (Total)", low: 20, med: 26, high: 32, max: 38 },
        { label: "Throw-ins (Total)", low: 30, med: 37, high: 44, max: 52 },
        { label: "Goal Kicks (Total)", low: 12, med: 16, high: 21, max: 26 },
        { label: "Tackles (Total)", low: 30, med: 36, high: 42, max: 50 },
        { label: "Offsides (Total)", low: 2, med: 3, high: 5, max: 8 },
      ];

      function buildPredictions() {
        const grid = document.getElementById("predGrid");
        predictions.forEach((p, i) => {
          const card = document.createElement("div");
          card.className = "pred-card";
          card.style.animationDelay = i * 0.08 + "s";
          const lp = Math.round((p.low / p.max) * 100);
          const mp = Math.round((p.med / p.max) * 100);
          const hp = Math.round((p.high / p.max) * 100);
          card.innerHTML = `
      <div class="pred-label">${p.label}</div>
      <div class="pred-values">
        <div class="pred-item">
          <div class="pred-item-label">Low</div>
          <div class="bar-wrap"><div class="bar-fill low" data-w="${lp}"></div></div>
          <div class="pred-num low-c">${p.low}</div>
        </div>
        <div class="pred-item">
          <div class="pred-item-label">Median</div>
          <div class="bar-wrap"><div class="bar-fill med" data-w="${mp}"></div></div>
          <div class="pred-num med-c">${p.med}</div>
        </div>
        <div class="pred-item">
          <div class="pred-item-label">High</div>
          <div class="bar-wrap"><div class="bar-fill high" data-w="${hp}"></div></div>
          <div class="pred-num high-c">${p.high}</div>
        </div>
      </div>`;
          grid.appendChild(card);
        });
      }

      function animateBars() {
        document.querySelectorAll(".bar-fill[data-w]").forEach((bar, i) => {
          setTimeout(
            () => {
              bar.style.width = bar.dataset.w + "%";
            },
            200 + i * 60,
          );
        });
      }

      function showTab(id) {
        document
          .querySelectorAll(".section")
          .forEach((s) => s.classList.remove("active"));
        document
          .querySelectorAll(".tab-btn")
          .forEach((b) => b.classList.remove("active"));
        document.getElementById(id).classList.add("active");
        event.currentTarget.classList.add("active");
        if (id === "predictions") setTimeout(animateBars, 100);
      }

      // Intersection observer for scroll-triggered bar animations
      const observer = new IntersectionObserver(
        (entries) => {
          entries.forEach((e) => {
            if (e.isIntersecting) {
              animateBars();
              observer.unobserve(e.target);
            }
          });
        },
        { threshold: 0.3 },
      );

      buildPredictions();
      const predSection = document.getElementById("predGrid");
      if (predSection) observer.observe(predSection);
    </script>
  </body>
</html>
