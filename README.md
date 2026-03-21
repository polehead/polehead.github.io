<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>PL MD31 · Weekend Predictions · 21–22 March 2026</title>
    <link
      href="https://fonts.googleapis.com/css2?family=Plus+Jakarta+Sans:wght@300;400;500;600;700;800&family=JetBrains+Mono:wght@400;500;600&display=swap"
      rel="stylesheet"
    />
    <style>
      /* ══════════════════════════════════════════
   DESIGN TOKENS — Slate / Volt / Infrared
══════════════════════════════════════════ */
      :root {
        /* backgrounds */
        --bg: #0a0b10;
        --bg2: #0f1118;
        --card: #13151f;
        --card2: #181b26;
        --border: #1e2235;
        --border2: #262a3e;

        /* text */
        --fg: #eceef8;
        --fg2: #8890b0;
        --fg3: #3d4460;

        /* accent palette — neon-adjacent */
        --volt: #c8f542; /* lime green */
        --volt-dim: rgba(200, 245, 66, 0.12);
        --teal: #12e8c8;
        --teal-dim: rgba(18, 232, 200, 0.11);
        --pink: #f542a4;
        --pink-dim: rgba(245, 66, 164, 0.11);
        --orange: #ff7a28;
        --orange-dim: rgba(255, 122, 40, 0.11);
        --sky: #38b6ff;
        --sky-dim: rgba(56, 182, 255, 0.11);
        --purple: #a855f7;
        --purple-dim: rgba(168, 85, 247, 0.11);
        --red: #ff4b4b;
        --red-dim: rgba(255, 75, 75, 0.11);

        /* semantic */
        --win: #22d37a;
        --win-dim: rgba(34, 211, 122, 0.12);
        --draw: #6b7280;
        --loss: #ff4b4b;

        --r: 12px;
        --r-sm: 8px;
        --r-xs: 5px;
        --px: 16px;
      }

      *,
      *::before,
      *::after {
        box-sizing: border-box;
        margin: 0;
        padding: 0;
      }
      html {
        font-size: 16px;
        scroll-behavior: smooth;
        -webkit-text-size-adjust: 100%;
      }
      body {
        background: var(--bg);
        color: var(--fg);
        font-family: "Plus Jakarta Sans", sans-serif;
        line-height: 1.5;
        min-height: 100vh;
        overflow-x: hidden;
      }

      /* ── REVEAL ── */
      .reveal {
        opacity: 0;
        transform: translateY(14px);
        transition:
          opacity 0.5s ease,
          transform 0.5s ease;
      }
      .reveal.in {
        opacity: 1;
        transform: none;
      }

      /* ══════════════════════════════════════════
   HEADER — sticky, compact mobile-first
══════════════════════════════════════════ */
      .site-header {
        position: sticky;
        top: 0;
        z-index: 200;
        background: rgba(10, 11, 16, 0.9);
        backdrop-filter: blur(14px);
        -webkit-backdrop-filter: blur(14px);
        border-bottom: 1px solid var(--border);
      }
      .hdr {
        max-width: 1060px;
        margin: 0 auto;
        display: flex;
        align-items: center;
        gap: 10px;
        padding: 0 var(--px);
        height: 48px;
      }
      .hdr-logo {
        font-family: "JetBrains Mono", monospace;
        font-size: 15px;
        font-weight: 600;
        letter-spacing: 0.06em;
        text-transform: uppercase;
        color: var(--volt);
        flex-shrink: 0;
        display: flex;
        align-items: center;
        gap: 8px;
      }
      .live-dot {
        width: 7px;
        height: 7px;
        border-radius: 50%;
        background: var(--volt);
        box-shadow: 0 0 7px rgba(200, 245, 66, 0.6);
        animation: dot 1.8s ease-in-out infinite;
      }
      @keyframes dot {
        0%,
        100% {
          opacity: 1;
        }
        50% {
          opacity: 0.2;
        }
      }
      .hdr-sep {
        color: var(--fg3);
        font-size: 13px;
      }
      .hdr-date {
        font-family: "JetBrains Mono", monospace;
        font-size: 12px;
        letter-spacing: 0.06em;
        color: var(--fg3);
        display: none;
      }
      .hdr-count {
        font-family: "JetBrains Mono", monospace;
        font-size: 12px;
        letter-spacing: 0.06em;
        color: var(--teal);
        margin-left: auto;
        flex-shrink: 0;
      }
      @media (min-width: 480px) {
        .hdr {
          height: 50px;
          padding: 0 20px;
        }
        .hdr-date {
          display: block;
        }
      }
      @media (min-width: 768px) {
        .hdr {
          height: 52px;
          padding: 0 28px;
        }
      }

      /* ══════════════════════════════════════════
   HERO — bold type, compact mobile
══════════════════════════════════════════ */
      .hero {
        padding: 28px var(--px) 32px;
        border-bottom: 1px solid var(--border);
        background: linear-gradient(
          160deg,
          rgba(200, 245, 66, 0.04) 0%,
          transparent 50%,
          rgba(18, 232, 200, 0.03) 100%
        );
      }
      .hero-inner {
        max-width: 1060px;
        margin: 0 auto;
      }
      .hero-eyebrow {
        font-family: "JetBrains Mono", monospace;
        font-size: 12px;
        letter-spacing: 0.18em;
        text-transform: uppercase;
        color: var(--volt);
        margin-bottom: 10px;
        display: flex;
        align-items: center;
        gap: 10px;
      }
      .hero-eyebrow::before {
        content: "";
        width: 16px;
        height: 1px;
        background: var(--volt);
        flex-shrink: 0;
      }
      .hero-h1 {
        font-size: clamp(38px, 9vw, 82px);
        font-weight: 800;
        line-height: 0.92;
        letter-spacing: -0.03em;
        margin-bottom: 8px;
      }
      .hero-h1 em {
        color: var(--volt);
        font-style: normal;
      }
      .hero-sub {
        font-family: "JetBrains Mono", monospace;
        font-size: 11px;
        letter-spacing: 0.14em;
        text-transform: uppercase;
        color: var(--fg3);
        margin-bottom: 20px;
      }

      /* fixture day pills */
      .day-pills {
        display: flex;
        gap: 8px;
        flex-wrap: wrap;
      }
      .day-pill {
        display: flex;
        flex-direction: column;
        gap: 2px;
        background: var(--card);
        border: 1px solid var(--border);
        border-radius: var(--r-sm);
        padding: 8px 12px;
        min-width: 120px;
      }
      .dp-label {
        font-family: "JetBrains Mono", monospace;
        font-size: 10px;
        letter-spacing: 0.14em;
        text-transform: uppercase;
        color: var(--fg3);
      }
      .dp-count {
        font-size: 18px;
        font-weight: 700;
        color: var(--volt);
        line-height: 1;
      }
      .dp-time {
        font-family: "JetBrains Mono", monospace;
        font-size: 11px;
        color: var(--fg2);
      }

      @media (min-width: 480px) {
        .hero {
          padding: 36px 20px 40px;
        }
      }
      @media (min-width: 768px) {
        .hero {
          padding: 44px 28px 48px;
        }
      }

      /* ══════════════════════════════════════════
   WRAP
══════════════════════════════════════════ */
      .wrap {
        max-width: 1060px;
        margin: 0 auto;
        padding: 20px var(--px) 72px;
      }
      @media (min-width: 480px) {
        .wrap {
          padding: 24px 20px 80px;
        }
      }
      @media (min-width: 768px) {
        .wrap {
          padding: 32px 28px 88px;
        }
      }

      /* day section */
      .day-section {
        margin-bottom: 32px;
      }
      .day-header {
        display: flex;
        align-items: center;
        gap: 10px;
        margin-bottom: 14px;
        font-family: "JetBrains Mono", monospace;
        font-size: 11px;
        letter-spacing: 0.18em;
        text-transform: uppercase;
        color: var(--fg3);
      }
      .day-header::after {
        content: "";
        flex: 1;
        height: 1px;
        background: var(--border);
      }

      /* ══════════════════════════════════════════
   FIXTURE CARD — mobile-first
══════════════════════════════════════════ */
      .fc {
        background: var(--card);
        border: 1px solid var(--border);
        border-radius: var(--r);
        overflow: hidden;
        margin-bottom: 12px;
        transition:
          border-color 0.2s,
          box-shadow 0.2s;
      }
      .fc:hover {
        border-color: var(--border2);
        box-shadow: 0 4px 24px rgba(0, 0, 0, 0.4);
      }

      /* kick-off badge */
      .fc-ko {
        display: flex;
        align-items: center;
        justify-content: space-between;
        padding: 9px var(--px);
        background: var(--bg2);
        border-bottom: 1px solid var(--border);
      }
      .ko-time {
        font-family: "JetBrains Mono", monospace;
        font-size: 12px;
        letter-spacing: 0.12em;
        text-transform: uppercase;
        font-weight: 600;
      }
      .ko-comp {
        font-family: "JetBrains Mono", monospace;
        font-size: 10px;
        letter-spacing: 0.08em;
        text-transform: uppercase;
        color: var(--fg3);
      }
      .ko-badge {
        font-family: "JetBrains Mono", monospace;
        font-size: 10px;
        letter-spacing: 0.07em;
        text-transform: uppercase;
        font-weight: 600;
        padding: 4px 10px;
        border-radius: var(--r-xs);
        border: 1px solid;
        white-space: nowrap;
      }
      .stake-high {
        color: var(--orange);
        border-color: rgba(255, 122, 40, 0.35);
        background: var(--orange-dim);
      }
      .stake-med {
        color: var(--sky);
        border-color: rgba(56, 182, 255, 0.35);
        background: var(--sky-dim);
      }
      .stake-low {
        color: var(--fg3);
        border-color: var(--border);
        background: rgba(255, 255, 255, 0.02);
      }
      @media (min-width: 480px) {
        .fc-ko {
          padding: 9px 18px;
        }
      }

      /* teams & score */
      .fc-top {
        display: grid;
        grid-template-columns: 1fr auto 1fr;
        align-items: center;
        gap: 8px;
        padding: 18px var(--px) 16px;
      }
      .fc-team {
        display: flex;
        flex-direction: column;
        align-items: flex-start;
        gap: 6px;
      }
      .fc-team.away {
        align-items: flex-end;
        text-align: right;
      }
      .fc-team-info {
        display: flex;
        flex-direction: column;
      }
      .fc-team.away .fc-team-info {
        align-items: flex-end;
      }
      @media (min-width: 580px) {
        .fc-team {
          flex-direction: row;
          align-items: flex-start;
          gap: 10px;
        }
        .fc-team.away {
          flex-direction: row-reverse;
          align-items: flex-start;
        }
      }

      /* badge */
      .fc-badge {
        width: 40px;
        height: 40px;
        flex-shrink: 0;
        display: flex;
        align-items: center;
        justify-content: center;
      }
      .fc-badge img {
        width: 40px;
        height: 40px;
        object-fit: contain;
        filter: drop-shadow(0 1px 3px rgba(0, 0, 0, 0.5));
      }

      .fc-club {
        font-size: clamp(17px, 4vw, 24px);
        font-weight: 700;
        letter-spacing: -0.02em;
        color: var(--fg);
        line-height: 1.1;
      }
      .fc-meta {
        font-family: "JetBrains Mono", monospace;
        font-size: 10px;
        letter-spacing: 0.06em;
        text-transform: uppercase;
        color: var(--fg2);
        margin-top: 4px;
      }
      .form-row {
        display: flex;
        gap: 3px;
        margin-top: 7px;
      }
      .form-row.r {
        justify-content: flex-end;
      }
      .fb {
        width: 20px;
        height: 20px;
        border-radius: 3px;
        display: flex;
        align-items: center;
        justify-content: center;
        font-family: "JetBrains Mono", monospace;
        font-size: 9px;
        font-weight: 600;
        flex-shrink: 0;
      }
      .fw {
        background: rgba(34, 211, 122, 0.18);
        color: var(--win);
        border: 1px solid rgba(34, 211, 122, 0.35);
      }
      .fd {
        background: rgba(255, 255, 255, 0.08);
        color: rgba(255, 255, 255, 0.5);
        border: 1px solid rgba(255, 255, 255, 0.18);
      }
      .fl {
        background: rgba(255, 75, 75, 0.15);
        color: var(--red);
        border: 1px solid rgba(255, 75, 75, 0.3);
      }

      .fc-mid {
        display: flex;
        flex-direction: column;
        align-items: center;
        gap: 3px;
        flex-shrink: 0;
      }
      .fc-pred-lbl {
        font-family: "JetBrains Mono", monospace;
        font-size: 9px;
        letter-spacing: 0.16em;
        text-transform: uppercase;
        color: rgba(255, 255, 255, 0.35);
      }
      .fc-score {
        font-size: clamp(30px, 8vw, 48px);
        font-weight: 800;
        letter-spacing: 0.02em;
        line-height: 1;
        color: var(--volt);
        white-space: nowrap;
      }
      .fc-prob {
        font-family: "JetBrains Mono", monospace;
        font-size: 10px;
        letter-spacing: 0.06em;
        color: rgba(255, 255, 255, 0.45);
        text-align: center;
      }
      @media (min-width: 480px) {
        .fc-top {
          padding: 20px 18px 18px;
          gap: 12px;
        }
        .fc-badge {
          width: 44px;
          height: 44px;
        }
        .fc-badge img {
          width: 44px;
          height: 44px;
        }
      }
      @media (min-width: 768px) {
        .fc-top {
          padding: 22px 24px 20px;
          gap: 16px;
        }
        .fc-club {
          font-size: 22px;
        }
        .fc-badge {
          width: 48px;
          height: 48px;
        }
        .fc-badge img {
          width: 48px;
          height: 48px;
        }
      }

      /* probability bar */
      .fc-probs {
        display: flex;
        align-items: center;
        gap: 0;
        padding: 10px var(--px);
        border-top: 1px solid var(--border);
        background: rgba(255, 255, 255, 0.01);
      }
      .prob-segment {
        display: flex;
        flex-direction: column;
        align-items: center;
        flex: 1;
        gap: 3px;
      }
      .ps-label {
        font-family: "JetBrains Mono", monospace;
        font-size: 9px;
        letter-spacing: 0.08em;
        text-transform: uppercase;
        color: var(--fg3);
      }
      .ps-pct {
        font-size: 17px;
        font-weight: 700;
        line-height: 1;
      }
      .ps-h {
        color: var(--volt);
      }
      .ps-d {
        color: var(--fg3);
      }
      .ps-a {
        color: var(--teal);
      }
      .prob-bar-row {
        flex: 1;
        padding: 0 4px;
      }
      .prob-bar {
        display: flex;
        height: 3px;
        border-radius: 2px;
        overflow: hidden;
        gap: 1px;
        margin-bottom: 0;
      }
      .pb-h {
        background: var(--volt);
      }
      .pb-d {
        background: #1e2235;
      }
      .pb-a {
        background: var(--teal);
      }
      @media (min-width: 480px) {
        .fc-probs {
          padding: 10px 18px;
        }
      }

      /* ══════════════════════════════════════════
   STAT SECTION — expandable on mobile
══════════════════════════════════════════ */
      .fc-stats {
        border-top: 1px solid var(--border);
      }
      .stat-grid {
        display: grid;
        grid-template-columns: 1fr;
        gap: 0;
      }
      @media (min-width: 580px) {
        .stat-grid {
          grid-template-columns: 1fr 1fr;
        }
      }
      @media (min-width: 880px) {
        .stat-grid {
          grid-template-columns: 1fr 1fr 1fr 1fr;
        }
      }

      .stat-cell {
        padding: 11px var(--px);
        border-bottom: 1px solid var(--border);
        display: flex;
        flex-direction: column;
        gap: 5px;
      }
      @media (min-width: 580px) {
        .stat-cell {
          border-right: 1px solid var(--border);
          padding: 11px 14px;
        }
        .stat-cell:nth-child(2n) {
          border-right: none;
        }
      }
      @media (min-width: 880px) {
        .stat-cell:nth-child(2n) {
          border-right: 1px solid var(--border);
        }
        .stat-cell:nth-child(4n) {
          border-right: none;
        }
      }
      .sc-name {
        font-family: "JetBrains Mono", monospace;
        font-size: 10px;
        letter-spacing: 0.12em;
        text-transform: uppercase;
        color: var(--fg3);
      }
      .sc-vals {
        display: flex;
        align-items: center;
        gap: 6px;
      }
      .sc-lo {
        font-family: "JetBrains Mono", monospace;
        font-size: 15px;
        font-weight: 600;
        color: var(--teal);
      }
      .sc-sep {
        font-family: "JetBrains Mono", monospace;
        font-size: 11px;
        color: var(--fg3);
      }
      .sc-hi {
        font-family: "JetBrains Mono", monospace;
        font-size: 15px;
        font-weight: 600;
        color: var(--orange);
      }
      .sc-med {
        font-size: 22px;
        font-weight: 800;
        color: var(--volt);
        letter-spacing: -0.02em;
        line-height: 1;
        margin-left: auto;
      }
      .sc-bar {
        height: 3px;
        border-radius: 2px;
        background: rgba(255, 255, 255, 0.06);
        overflow: hidden;
        position: relative;
      }
      .sc-bar-lo {
        position: absolute;
        left: 0;
        top: 0;
        height: 100%;
        border-radius: 2px;
        background: var(--teal);
        opacity: 0.7;
      }
      .sc-bar-hi {
        position: absolute;
        left: 0;
        top: 0;
        height: 100%;
        border-radius: 2px;
        background: var(--orange);
        opacity: 0.35;
      }
      .sc-ctx {
        font-family: "JetBrains Mono", monospace;
        font-size: 10px;
        color: var(--fg3);
        line-height: 1.5;
      }

      /* ══════════════════════════════════════════
   CONTEXT STRIP
══════════════════════════════════════════ */
      .fc-context {
        padding: 10px var(--px);
        border-top: 1px solid var(--border);
        background: rgba(200, 245, 66, 0.025);
        display: flex;
        align-items: flex-start;
        gap: 8px;
      }
      .ctx-icon {
        color: var(--volt);
        font-size: 11px;
        flex-shrink: 0;
        margin-top: 1px;
      }
      .ctx-text {
        font-size: 13px;
        color: #a3aac8;
        line-height: 1.65;
      }
      .ctx-text strong {
        color: var(--fg);
        font-weight: 600;
      }
      .ctx-text .hl {
        color: var(--volt);
        font-weight: 600;
      }
      .ctx-text .hr {
        color: var(--red);
        font-weight: 600;
      }
      .ctx-text .ht {
        color: var(--teal);
        font-weight: 600;
      }
      .ctx-text .ho {
        color: var(--orange);
        font-weight: 600;
      }
      @media (min-width: 480px) {
        .fc-context {
          padding: 12px 18px;
        }
      }
      @media (min-width: 768px) {
        .ctx-text {
          font-size: 14px;
        }
      }

      /* ══════════════════════════════════════════
   LEGEND
══════════════════════════════════════════ */
      .legend {
        display: flex;
        gap: 14px;
        flex-wrap: wrap;
        padding: 12px var(--px);
        margin-bottom: 16px;
        background: var(--card);
        border: 1px solid var(--border);
        border-radius: var(--r-sm);
      }
      .leg {
        display: flex;
        align-items: center;
        gap: 6px;
      }
      .leg-dot {
        width: 12px;
        height: 3px;
        border-radius: 2px;
        flex-shrink: 0;
      }
      .leg-label {
        font-family: "JetBrains Mono", monospace;
        font-size: 10px;
        letter-spacing: 0.1em;
        text-transform: uppercase;
        color: var(--fg3);
      }
      @media (min-width: 480px) {
        .legend {
          padding: 12px 20px;
        }
      }

      /* ══════════════════════════════════════════
   BTTS / OVER PILLS
══════════════════════════════════════════ */
      .btts-row {
        display: flex;
        gap: 6px;
        flex-wrap: wrap;
        padding: 8px var(--px);
        border-top: 1px solid var(--border);
        background: rgba(255, 255, 255, 0.01);
      }
      .btts-pill {
        font-family: "JetBrains Mono", monospace;
        font-size: 10px;
        letter-spacing: 0.07em;
        text-transform: uppercase;
        font-weight: 600;
        padding: 4px 9px;
        border-radius: var(--r-xs);
        border: 1px solid;
      }
      .bp-yes {
        color: var(--win);
        border-color: rgba(34, 211, 122, 0.35);
        background: var(--win-dim);
      }
      .bp-no {
        color: var(--red);
        border-color: rgba(255, 75, 75, 0.35);
        background: var(--red-dim);
      }
      .bp-maybe {
        color: var(--orange);
        border-color: rgba(255, 122, 40, 0.35);
        background: var(--orange-dim);
      }
      .bp-info {
        color: var(--sky);
        border-color: rgba(56, 182, 255, 0.35);
        background: var(--sky-dim);
      }
      @media (min-width: 480px) {
        .btts-row {
          padding: 8px 18px;
        }
      }

      /* ══════════════════════════════════════════
   FOOTER
══════════════════════════════════════════ */
      footer {
        border-top: 1px solid var(--border);
        padding: 16px var(--px);
        max-width: 1060px;
        margin: 0 auto;
        display: flex;
        justify-content: space-between;
        align-items: center;
        flex-wrap: wrap;
        gap: 8px;
      }
      .ft-l {
        font-family: "JetBrains Mono", monospace;
        font-size: 10px;
        color: var(--fg3);
        letter-spacing: 0.05em;
        line-height: 2;
      }
      .ft-r {
        font-family: "JetBrains Mono", monospace;
        font-size: 14px;
        font-weight: 600;
        color: var(--volt);
      }
      @media (min-width: 480px) {
        footer {
          padding: 18px 20px;
        }
      }
      @media (min-width: 768px) {
        footer {
          padding: 20px 28px;
        }
      }

      /* colour class helpers */
      .c-volt {
        color: var(--volt);
      }
      .c-teal {
        color: var(--teal);
      }
      .c-pink {
        color: var(--pink);
      }
      .c-orange {
        color: var(--orange);
      }
      .c-sky {
        color: var(--sky);
      }
      .c-purple {
        color: var(--purple);
      }
    </style>
  </head>
  <body>
    <!-- HEADER -->
    <header class="site-header">
      <div class="hdr">
        <div class="hdr-logo">
          <div class="live-dot"></div>
          Match Intel
        </div>
        <span class="hdr-sep">·</span>
        <div class="hdr-date">Sat 21 – Sun 22 Mar 2026</div>
        <div class="hdr-count">Match Day 31 · 7 Fixtures</div>
      </div>
    </header>

    <!-- HERO -->
    <section class="hero">
      <div class="hero-inner reveal">
        <div class="hero-eyebrow">
          Premier League · Matchday 31 · Weekend Preview
        </div>
        <h1 class="hero-h1">Weekend<br /><em>Predictions</em></h1>
        <p class="hero-sub">
          21–22 March 2026 · Last 5 each team · Last 5 H2H · Season averages ·
          High-stakes adjustment
        </p>
        <div class="day-pills">
          <div class="day-pill">
            <div class="dp-label">Saturday 21 Mar</div>
            <div class="dp-count">4 Games</div>
            <div class="dp-time">12:30 · 15:00 · 17:30 · 20:00</div>
          </div>
          <div class="day-pill">
            <div class="dp-label">Sunday 22 Mar</div>
            <div class="dp-count">3 Games</div>
            <div class="dp-time">12:00 · 14:15 · 14:15</div>
          </div>
        </div>
      </div>
    </section>

    <div class="wrap">
      <!-- LEGEND -->
      <div class="legend reveal">
        <div class="leg">
          <div class="leg-dot" style="background: var(--teal)"></div>
          <div class="leg-label">Lowest expected</div>
        </div>
        <div class="leg">
          <div class="leg-dot" style="background: var(--volt)"></div>
          <div class="leg-label">Median expected</div>
        </div>
        <div class="leg">
          <div class="leg-dot" style="background: var(--orange)"></div>
          <div class="leg-label">Highest expected</div>
        </div>
      </div>

      <!-- ══════════════════ SATURDAY ══════════════════ -->
      <div class="day-section">
        <div class="day-header reveal">Saturday 21 March 2026</div>

        <!-- ── FIXTURE 1: Brighton vs Liverpool ── -->
        <div class="fc reveal">
          <div class="fc-ko">
            <div>
              <span class="ko-time c-volt">12:30 GMT</span>
              <span class="ko-comp"> · Amex Stadium · Brighton</span>
            </div>
            <span class="ko-badge stake-high">⚡ High stakes</span>
          </div>
          <div class="fc-top">
            <div class="fc-team">
              <div class="fc-badge">
                <img
                  src="https://crests.football-data.org/397.png"
                  alt="Brighton"
                  loading="lazy"
                  style="background-color: #13151f;"
                />
              </div>
              <div class="fc-team-info">
                <div class="fc-club">Brighton</div>
                <div class="fc-meta">12th · 40pts</div>
                <!-- L5: W(CRY 1-0), W(SUN 1-0), D(BRE), L(MUN), W(LEE) — strong home form -->
                <div class="form-row">
                  <div class="fb fw">W</div>
                  <div class="fb fw">W</div>
                  <div class="fb fd">D</div>
                  <div class="fb fl">L</div>
                  <div class="fb fw">W</div>
                </div>
              </div>
            </div>
            <div class="fc-mid">
              <div class="fc-pred-lbl">Predicted</div>
              <div class="fc-score">1–2</div>
              <div class="fc-prob">LFC adv · 43.8%</div>
            </div>
            <div class="fc-team away">
              <div class="fc-badge">
                <img
                  src="https://crests.football-data.org/64.png"
                  alt="Liverpool"
                  loading="lazy"
                  style="background-color: #13151f;"
                />
              </div>
              <div class="fc-team-info">
                <div class="fc-club">Liverpool</div>
                <div class="fc-meta">5th · 49pts</div>
                <!-- L5: D(TOT 1-1), W(NFO 1-0), W(SUN 1-0), L(Wolves 2-1), W(WHU 5-2) -->
                <div class="form-row r">
                  <div class="fb fd">D</div>
                  <div class="fb fw">W</div>
                  <div class="fb fw">W</div>
                  <div class="fb fl">L</div>
                  <div class="fb fw">W</div>
                </div>
              </div>
            </div>
          </div>
          <div class="fc-probs">
            <div class="prob-segment">
              <div class="ps-label">BRI</div>
              <div class="ps-pct ps-h">30.4%</div>
            </div>
            <div class="prob-bar-row">
              <div class="prob-bar">
                <div class="pb-h" style="flex: 30.4"></div>
                <div class="pb-d" style="flex: 25.8"></div>
                <div class="pb-a" style="flex: 43.8"></div>
              </div>
            </div>
            <div class="prob-segment">
              <div class="ps-label">Draw</div>
              <div class="ps-pct ps-d">25.8%</div>
            </div>
            <div class="prob-segment">
              <div class="ps-label">LFC</div>
              <div class="ps-pct ps-a">43.8%</div>
            </div>
          </div>
          <div class="fc-stats">
            <div class="stat-grid">
              <div class="stat-cell">
                <div class="sc-name">Corners</div>
                <div class="sc-vals">
                  <span class="sc-lo">7</span><span class="sc-sep">—</span
                  ><span class="sc-hi">13</span><span class="sc-med">10</span>
                </div>
                <div class="sc-bar">
                  <div class="sc-bar-lo" style="width: 54%"></div>
                  <div class="sc-bar-hi" style="width: 78%"></div>
                </div>
                <div class="sc-ctx">
                  BRI 3 vs SUN · LFC 3 vs TOT · H2H avg ~10 corners · LFC
                  possession → more corners
                </div>
              </div>
              <div class="stat-cell">
                <div class="sc-name">Shots on Target</div>
                <div class="sc-vals">
                  <span class="sc-lo">5</span><span class="sc-sep">—</span
                  ><span class="sc-hi">12</span><span class="sc-med">8</span>
                </div>
                <div class="sc-bar">
                  <div class="sc-bar-lo" style="width: 42%"></div>
                  <div class="sc-bar-hi" style="width: 72%"></div>
                </div>
                <div class="sc-ctx">
                  BRI 4 SoT vs SUN · LFC 3 SoT vs TOT · BRI avg 4.5/g home ·
                  BTTS 64% H2H
                </div>
              </div>
              <div class="stat-cell">
                <div class="sc-name">Fouls</div>
                <div class="sc-vals">
                  <span class="sc-lo">16</span><span class="sc-sep">—</span
                  ><span class="sc-hi">26</span><span class="sc-med">20</span>
                </div>
                <div class="sc-bar">
                  <div class="sc-bar-lo" style="width: 48%"></div>
                  <div class="sc-bar-hi" style="width: 70%"></div>
                </div>
                <div class="sc-ctx">
                  BRI 12 vs SUN · LFC 7 vs TOT combined=19 · Intense matchup
                  expected
                </div>
              </div>
              <div class="stat-cell">
                <div class="sc-name">Throw-ins</div>
                <div class="sc-vals">
                  <span class="sc-lo">28</span><span class="sc-sep">—</span
                  ><span class="sc-hi">42</span><span class="sc-med">34</span>
                </div>
                <div class="sc-bar">
                  <div class="sc-bar-lo" style="width: 46%"></div>
                  <div class="sc-bar-hi" style="width: 66%"></div>
                </div>
                <div class="sc-ctx">
                  BRI 9 TIs vs SUN (away) · LFC 24 TIs vs TOT · PL avg ~33
                </div>
              </div>
              <div class="stat-cell">
                <div class="sc-name">Goal Kicks</div>
                <div class="sc-vals">
                  <span class="sc-lo">10</span><span class="sc-sep">—</span
                  ><span class="sc-hi">20</span><span class="sc-med">15</span>
                </div>
                <div class="sc-bar">
                  <div class="sc-bar-lo" style="width: 40%"></div>
                  <div class="sc-bar-hi" style="width: 62%"></div>
                </div>
                <div class="sc-ctx">
                  BRI 12 GKs vs SUN (away) · LFC 5 GKs vs TOT · Mam plays out
                  from back
                </div>
              </div>
              <div class="stat-cell">
                <div class="sc-name">Total Shots</div>
                <div class="sc-vals">
                  <span class="sc-lo">18</span><span class="sc-sep">—</span
                  ><span class="sc-hi">30</span><span class="sc-med">24</span>
                </div>
                <div class="sc-bar">
                  <div class="sc-bar-lo" style="width: 52%"></div>
                  <div class="sc-bar-hi" style="width: 76%"></div>
                </div>
                <div class="sc-ctx">
                  BRI 11 shots vs SUN · LFC 16 shots vs TOT · H2H high-scoring
                  3.41 avg
                </div>
              </div>
              <div class="stat-cell">
                <div class="sc-name">Tackles</div>
                <div class="sc-vals">
                  <span class="sc-lo">22</span><span class="sc-sep">—</span
                  ><span class="sc-hi">34</span><span class="sc-med">27</span>
                </div>
                <div class="sc-bar">
                  <div class="sc-bar-lo" style="width: 44%"></div>
                  <div class="sc-bar-hi" style="width: 68%"></div>
                </div>
                <div class="sc-ctx">
                  Both high-press sides · BRI home intensity · Bogey fixture for
                  LFC raises stakes
                </div>
              </div>
            </div>
          </div>
          <div class="btts-row">
            <span class="btts-pill bp-yes">BTTS YES</span>
            <span class="btts-pill bp-yes">O2.5 goals</span>
            <span class="btts-pill bp-info">BRI bogey team for LFC</span>
            <span class="btts-pill bp-maybe">Salah OUT · Alisson OUT</span>
            <span class="btts-pill bp-info"
              >Minteh scored vs SUN · key threat</span
            >
            <span
              class="btts-pill"
              style="
                color: var(--orange);
                border-color: rgba(255, 122, 40, 0.4);
                background: var(--orange-dim);
              "
              >⬤ MED confidence</span
            >
          </div>
          <div class="fc-context">
            <span class="ctx-icon">◆</span>
            <p class="ctx-text">
              <span class="hl"
                >Brighton have won 3 of their last 5 PL home games</span
              >
              and name an unchanged XI from last weekend's 1-0 win at
              Sunderland, with Mitoma fit after ankle concerns. Despite
              Liverpool's superior league position, Brighton have been a
              persistent bogey team — LFC have won only 6 of their last 13
              meetings here. <strong>H2H averages 3.41 goals, BTTS 64%.</strong>
              <span class="hr"
                >Liverpool are without Mohamed Salah (muscle — scored and then
                came off vs Galatasaray) and Alisson (injury — Mamardashvili
                deputises).</span
              >
              Confirmed LFC XI: Mamardashvili; Frimpong, Konate, Van Dijk,
              Kerkez; Gravenberch, Mac Allister; Szoboszlai, Wirtz, Gakpo;
              Ekitike. BRI XI: Verbruggen; Wieffer, Van Hecke, Dunk, Kadioglu;
              Milner, Gross; Gomez, Hinshelwood, Minteh; Welbeck. Stakes: LFC
              fighting for UCL via league — must win heading into international
              break.
            </p>
          </div>
        </div>

        <!-- ── FIXTURE 2: Fulham vs Burnley ── -->
        <div class="fc reveal">
          <div class="fc-ko">
            <div>
              <span class="ko-time c-volt">15:00 GMT</span>
              <span class="ko-comp"> · Craven Cottage · London</span>
            </div>
            <span class="ko-badge stake-low">Low stakes</span>
          </div>
          <div class="fc-top">
            <div class="fc-team">
              <div class="fc-badge">
                <img
                  src="https://crests.football-data.org/63.png"
                  alt="Fulham"
                  loading="lazy"
                  style="background-color: #13151f;"
                />
              </div>
              <div class="fc-team-info">
                <div class="fc-club">Fulham</div>
                <div class="fc-meta">11th · 41pts</div>
                <div class="form-row">
                  <div class="fb fd">D</div>
                  <div class="fb fw">W</div>
                  <div class="fb fw">W</div>
                  <div class="fb fd">D</div>
                  <div class="fb fl">L</div>
                </div>
              </div>
            </div>
            <div class="fc-mid">
              <div class="fc-pred-lbl">Predicted</div>
              <div class="fc-score">2–0</div>
              <div class="fc-prob">FUL win · 63.1%</div>
            </div>
            <div class="fc-team away">
              <div class="fc-badge">
                <img
                  src="https://crests.football-data.org/328.png"
                  alt="Burnley"
                  loading="lazy"
                  style="background-color: #13151f;"
                />
              </div>
              <div class="fc-team-info">
                <div class="fc-club">Burnley</div>
                <div class="fc-meta">19th · 20pts</div>
                <div class="form-row r">
                  <div class="fb fd">D</div>
                  <div class="fb fl">L</div>
                  <div class="fb fl">L</div>
                  <div class="fb fd">D</div>
                  <div class="fb fl">L</div>
                </div>
              </div>
            </div>
          </div>
          <div class="fc-probs">
            <div class="prob-segment">
              <div class="ps-label">FUL</div>
              <div class="ps-pct ps-h">63.1%</div>
            </div>
            <div class="prob-bar-row">
              <div class="prob-bar">
                <div class="pb-h" style="flex: 63.1"></div>
                <div class="pb-d" style="flex: 20.7"></div>
                <div class="pb-a" style="flex: 16.2"></div>
              </div>
            </div>
            <div class="prob-segment">
              <div class="ps-label">Draw</div>
              <div class="ps-pct ps-d">20.7%</div>
            </div>
            <div class="prob-segment">
              <div class="ps-label">BUR</div>
              <div class="ps-pct ps-a" style="color: var(--fg3)">16.2%</div>
            </div>
          </div>
          <div class="fc-stats">
            <div class="stat-grid">
              <div class="stat-cell">
                <div class="sc-name">Corners</div>
                <div class="sc-vals">
                  <span class="sc-lo">6</span><span class="sc-sep">—</span
                  ><span class="sc-hi">12</span><span class="sc-med">9</span>
                </div>
                <div class="sc-bar">
                  <div class="sc-bar-lo" style="width: 48%"></div>
                  <div class="sc-bar-hi" style="width: 72%"></div>
                </div>
                <div class="sc-ctx">
                  FUL 4 corners vs NFO · BUR 5 corners vs BOU · FUL home avg ~6
                  · low-event expected
                </div>
              </div>
              <div class="stat-cell">
                <div class="sc-name">Shots on Target</div>
                <div class="sc-vals">
                  <span class="sc-lo">4</span><span class="sc-sep">—</span
                  ><span class="sc-hi">10</span><span class="sc-med">6</span>
                </div>
                <div class="sc-bar">
                  <div class="sc-bar-lo" style="width: 36%"></div>
                  <div class="sc-bar-hi" style="width: 62%"></div>
                </div>
                <div class="sc-ctx">
                  FUL 1 SoT vs NFO · BUR 2 SoT vs BOU · Burnley poor conversion
                  season-long
                </div>
              </div>
              <div class="stat-cell">
                <div class="sc-name">Fouls</div>
                <div class="sc-vals">
                  <span class="sc-lo">16</span><span class="sc-sep">—</span
                  ><span class="sc-hi">26</span><span class="sc-med">20</span>
                </div>
                <div class="sc-bar">
                  <div class="sc-bar-lo" style="width: 46%"></div>
                  <div class="sc-bar-hi" style="width: 68%"></div>
                </div>
                <div class="sc-ctx">
                  FUL 11 + BUR 10 fouls in their last games · BUR foul to
                  disrupt · avg ~20
                </div>
              </div>
              <div class="stat-cell">
                <div class="sc-name">Throw-ins</div>
                <div class="sc-vals">
                  <span class="sc-lo">28</span><span class="sc-sep">—</span
                  ><span class="sc-hi">44</span><span class="sc-med">36</span>
                </div>
                <div class="sc-bar">
                  <div class="sc-bar-lo" style="width: 44%"></div>
                  <div class="sc-bar-hi" style="width: 66%"></div>
                </div>
                <div class="sc-ctx">
                  FUL 21 + NFO 25 TIs · BUR 34 TIs vs BOU (massive) · Burnley
                  high TI team
                </div>
              </div>
              <div class="stat-cell">
                <div class="sc-name">Goal Kicks</div>
                <div class="sc-vals">
                  <span class="sc-lo">12</span><span class="sc-sep">—</span
                  ><span class="sc-hi">22</span><span class="sc-med">17</span>
                </div>
                <div class="sc-bar">
                  <div class="sc-bar-lo" style="width: 44%"></div>
                  <div class="sc-bar-hi" style="width: 68%"></div>
                </div>
                <div class="sc-ctx">
                  FUL 12 GKs vs NFO · BUR 17 GKs vs BOU · Burnley long-ball
                  style → many GKs
                </div>
              </div>
              <div class="stat-cell">
                <div class="sc-name">Total Shots</div>
                <div class="sc-vals">
                  <span class="sc-lo">14</span><span class="sc-sep">—</span
                  ><span class="sc-hi">24</span><span class="sc-med">19</span>
                </div>
                <div class="sc-bar">
                  <div class="sc-bar-lo" style="width: 44%"></div>
                  <div class="sc-bar-hi" style="width: 70%"></div>
                </div>
                <div class="sc-ctx">
                  FUL 6 shots vs NFO · BUR 14 shots vs BOU · FUL home avg ~13/g
                </div>
              </div>
              <div class="stat-cell">
                <div class="sc-name">Tackles</div>
                <div class="sc-vals">
                  <span class="sc-lo">20</span><span class="sc-sep">—</span
                  ><span class="sc-hi">30</span><span class="sc-med">24</span>
                </div>
                <div class="sc-bar">
                  <div class="sc-bar-lo" style="width: 42%"></div>
                  <div class="sc-bar-hi" style="width: 62%"></div>
                </div>
                <div class="sc-ctx">
                  Low-stakes relegation vs mid-table · BUR work-rate high ·
                  physical contest
                </div>
              </div>
            </div>
          </div>
          <div class="btts-row">
            <span class="btts-pill bp-no">BTTS NO</span>
            <span class="btts-pill bp-no">U2.5 likely</span>
            <span class="btts-pill bp-info">Burnley 4W from 25 away</span>
            <span
              class="btts-pill"
              style="
                color: var(--win);
                border-color: rgba(34, 211, 122, 0.4);
                background: var(--win-dim);
              "
              >⬤ HIGH confidence</span
            >
          </div>
          <div class="fc-context">
            <span class="ctx-icon">◆</span>
            <p class="ctx-text">
              <span class="ho"
                >Burnley are 19th and eight points from safety</span
              >
              — effectively playing for pride. Fulham are comfortable mid-table
              but fighting for a European Conference spot (4pts off 7th).
              <strong
                >Confirmed FUL XI: Leno; Tete, Andersen, Bassey, Robinson;
                Berge, Iwobi; Wilson, King, Bobb; Jimenez.</strong
              >
              <span class="hr"
                >BUR missing 6 players: Cullen, Amdouni, Roberts, Beyer,
                Tuanzebe (all confirmed OUT), Tresor (ankle doubt).</span
              >
              Confirmed BUR XI: Dubravka; Humphreys, Laurent, Esteve; Walker,
              Ugochukwu, Hannibal, Hartman; Anthony, Foster; Flemming. Harry
              Wilson contributed a goal and 2 assists in the 3-2 win at Turf
              Moor in December — the danger man to watch.
              <span class="hl"
                >Walker has a 90% win rate against Fulham in his career</span
              >
              — one stat worth noting for Burnley backers.
            </p>
          </div>
        </div>

        <!-- ── FIXTURE 3: Everton vs Chelsea ── -->
        <div class="fc reveal">
          <div class="fc-ko">
            <div>
              <span class="ko-time c-volt">17:30 GMT</span>
              <span class="ko-comp"> · Hill Dickinson Stadium · Liverpool</span>
            </div>
            <span class="ko-badge stake-high">⚡ High stakes</span>
          </div>
          <div class="fc-top">
            <div class="fc-team">
              <div class="fc-badge">
                <img
                  src="https://crests.football-data.org/62.png"
                  alt="Everton"
                  loading="lazy"
                  style="background-color: #13151f;"
                />
              </div>
              <div class="fc-team-info">
                <div class="fc-club">Everton</div>
                <div class="fc-meta">8th · 43pts</div>
                <div class="form-row">
                  <div class="fb fl">L</div>
                  <div class="fb fd">D</div>
                  <div class="fb fw">W</div>
                  <div class="fb fd">D</div>
                  <div class="fb fl">L</div>
                </div>
              </div>
            </div>
            <div class="fc-mid">
              <div class="fc-pred-lbl">Predicted</div>
              <div class="fc-score">1–2</div>
              <div class="fc-prob">CFC adv · 43.2%</div>
            </div>
            <div class="fc-team away">
              <div class="fc-badge">
                <img
                  src="https://crests.football-data.org/61.png"
                  alt="Chelsea"
                  loading="lazy"
                  style="background-color: #13151f;"
                />
              </div>
              <div class="fc-team-info">
                <div class="fc-club">Chelsea</div>
                <div class="fc-meta">6th · 48pts</div>
                <div class="form-row r">
                  <div class="fb fl">L</div>
                  <div class="fb fw">W</div>
                  <div class="fb fd">D</div>
                  <div class="fb fl">L</div>
                  <div class="fb fw">W</div>
                </div>
              </div>
            </div>
          </div>
          <div class="fc-probs">
            <div class="prob-segment">
              <div class="ps-label">EVE</div>
              <div class="ps-pct ps-h">28.9%</div>
            </div>
            <div class="prob-bar-row">
              <div class="prob-bar">
                <div class="pb-h" style="flex: 28.9"></div>
                <div class="pb-d" style="flex: 27.9"></div>
                <div class="pb-a" style="flex: 43.2"></div>
              </div>
            </div>
            <div class="prob-segment">
              <div class="ps-label">Draw</div>
              <div class="ps-pct ps-d">27.9%</div>
            </div>
            <div class="prob-segment">
              <div class="ps-label">CFC</div>
              <div class="ps-pct ps-a">43.2%</div>
            </div>
          </div>
          <div class="fc-stats">
            <div class="stat-grid">
              <div class="stat-cell">
                <div class="sc-name">Corners</div>
                <div class="sc-vals">
                  <span class="sc-lo">6</span><span class="sc-sep">—</span
                  ><span class="sc-hi">14</span><span class="sc-med">9</span>
                </div>
                <div class="sc-bar">
                  <div class="sc-bar-lo" style="width: 44%"></div>
                  <div class="sc-bar-hi" style="width: 74%"></div>
                </div>
                <div class="sc-ctx">
                  CFC 8 corners vs NEW · EVE 3 corners vs ARS · CFC
                  high-possession = many corners
                </div>
              </div>
              <div class="stat-cell">
                <div class="sc-name">Shots on Target</div>
                <div class="sc-vals">
                  <span class="sc-lo">5</span><span class="sc-sep">—</span
                  ><span class="sc-hi">12</span><span class="sc-med">8</span>
                </div>
                <div class="sc-bar">
                  <div class="sc-bar-lo" style="width: 40%"></div>
                  <div class="sc-bar-hi" style="width: 70%"></div>
                </div>
                <div class="sc-ctx">
                  CFC 3 SoT vs NEW (67% poss) · EVE 3 SoT vs ARS · Chelsea avg
                  5.8/g season
                </div>
              </div>
              <div class="stat-cell">
                <div class="sc-name">Fouls</div>
                <div class="sc-vals">
                  <span class="sc-lo">16</span><span class="sc-sep">—</span
                  ><span class="sc-hi">26</span><span class="sc-med">20</span>
                </div>
                <div class="sc-bar">
                  <div class="sc-bar-lo" style="width: 46%"></div>
                  <div class="sc-bar-hi" style="width: 68%"></div>
                </div>
                <div class="sc-ctx">
                  EVE 12 vs ARS · CFC 9 vs NEW · combined 21 · physical fixture
                  at Goodison
                </div>
              </div>
              <div class="stat-cell">
                <div class="sc-name">Throw-ins</div>
                <div class="sc-vals">
                  <span class="sc-lo">28</span><span class="sc-sep">—</span
                  ><span class="sc-hi">42</span><span class="sc-med">35</span>
                </div>
                <div class="sc-bar">
                  <div class="sc-bar-lo" style="width: 46%"></div>
                  <div class="sc-bar-hi" style="width: 66%"></div>
                </div>
                <div class="sc-ctx">
                  EVE 18 TIs vs ARS · CFC 22 TIs vs NEW · competitive matchup =
                  many sideline moments
                </div>
              </div>
              <div class="stat-cell">
                <div class="sc-name">Goal Kicks</div>
                <div class="sc-vals">
                  <span class="sc-lo">10</span><span class="sc-sep">—</span
                  ><span class="sc-hi">20</span><span class="sc-med">15</span>
                </div>
                <div class="sc-bar">
                  <div class="sc-bar-lo" style="width: 38%"></div>
                  <div class="sc-bar-hi" style="width: 62%"></div>
                </div>
                <div class="sc-ctx">
                  CFC 5 GKs vs NEW · EVE 12 GKs vs ARS · Pickford plays short ·
                  Jørgensen plays out
                </div>
              </div>
              <div class="stat-cell">
                <div class="sc-name">Total Shots</div>
                <div class="sc-vals">
                  <span class="sc-lo">18</span><span class="sc-sep">—</span
                  ><span class="sc-hi">32</span><span class="sc-med">24</span>
                </div>
                <div class="sc-bar">
                  <div class="sc-bar-lo" style="width: 50%"></div>
                  <div class="sc-bar-hi" style="width: 76%"></div>
                </div>
                <div class="sc-ctx">
                  CFC 21 shots vs NEW · EVE 9 shots vs ARS · CFC 20.2 shots/g
                  avg
                </div>
              </div>
              <div class="stat-cell">
                <div class="sc-name">Tackles</div>
                <div class="sc-vals">
                  <span class="sc-lo">24</span><span class="sc-sep">—</span
                  ><span class="sc-hi">36</span><span class="sc-med">28</span>
                </div>
                <div class="sc-bar">
                  <div class="sc-bar-lo" style="width: 48%"></div>
                  <div class="sc-bar-hi" style="width: 70%"></div>
                </div>
                <div class="sc-ctx">
                  Goodison atmosphere drives intensity · both need points ·
                  Caicedo + Gueye physical midfield battle
                </div>
              </div>
            </div>
          </div>
          <div class="btts-row">
            <span class="btts-pill bp-maybe">BTTS MAYBE</span>
            <span class="btts-pill bp-info">UCL race for CFC</span>
            <span class="btts-pill bp-info">Goodison atmosphere</span>
            <span class="btts-pill bp-info">Joao Pedro in form</span>
            <span
              class="btts-pill"
              style="
                color: var(--orange);
                border-color: rgba(255, 122, 40, 0.4);
                background: var(--orange-dim);
              "
              >⬤ MED confidence</span
            >
          </div>
          <div class="fc-context">
            <span class="ctx-icon">◆</span>
            <p class="ctx-text">
              <strong>Both teams need wins</strong> — Chelsea chasing UCL spot
              (6th, 48pts), Everton fighting for European football (8th).
              <span class="hr"
                >Chelsea crashed out of the Champions League 8-2 on aggregate to
                PSG this week, and Trevoh Chalobah suffered a 6-week ankle
                injury in that game. Reece James (hamstring), Jørgensen (groin
                surgery), Colwill (ACL), and Mudryk (doping ban) also
                absent.</span
              >
              <strong
                >Confirmed CFC XI: Sanchez; Acheampong, Fofana, Hato, Cucurella;
                Caicedo, Santos; Palmer, Fernandez, Garnacho/Neto; Joao
                Pedro.</strong
              >
              Pedro Neto returns from suspension.
              <span class="hl"
                >Everton: Pickford; O'Brien, Keane, Tarkowski, Mykolenko;
                Garner, Gueye; Armstrong, Dewsbury-Hall, Ndiaye; Barry.</span
              >
              Tyrique George ineligible (Chelsea loanee). This is Chelsea's
              <strong>first ever visit to the Hill Dickinson Stadium</strong> —
              a historic occasion. Caicedo vs Gueye is the midfield battle to
              watch.
            </p>
          </div>
        </div>

        <!-- ── FIXTURE 4: Leeds vs Brentford ── -->
        <div class="fc reveal">
          <div class="fc-ko">
            <div>
              <span class="ko-time c-volt">20:00 GMT</span>
              <span class="ko-comp"> · Elland Road · Leeds</span>
            </div>
            <span class="ko-badge stake-med">Mid stakes</span>
          </div>
          <div class="fc-top">
            <div class="fc-team">
              <div class="fc-badge">
                <img
                  src="https://crests.football-data.org/341.png"
                  alt="Leeds United"
                  loading="lazy"
                  style="background-color: #13151f;"
                />
              </div>
              <div class="fc-team-info">
                <div class="fc-club">Leeds</div>
                <div class="fc-meta">15th · 32pts</div>
                <div class="form-row">
                  <div class="fb fd">D</div>
                  <div class="fb fl">L</div>
                  <div class="fb fw">W</div>
                  <div class="fb fd">D</div>
                  <div class="fb fd">D</div>
                </div>
              </div>
            </div>
            <div class="fc-mid">
              <div class="fc-pred-lbl">Predicted</div>
              <div class="fc-score">1–1</div>
              <div class="fc-prob">Draw · 27.8%</div>
            </div>
            <div class="fc-team away">
              <div class="fc-badge">
                <img
                  src="https://crests.football-data.org/402.png"
                  alt="Brentford"
                  loading="lazy"
                  style="background-color: #13151f;"
                />
              </div>
              <div class="fc-team-info">
                <div class="fc-club">Brentford</div>
                <div class="fc-meta">7th · 45pts</div>
                <div class="form-row r">
                  <div class="fb fd">D</div>
                  <div class="fb fd">D</div>
                  <div class="fb fw">W</div>
                  <div class="fb fw">W</div>
                  <div class="fb fd">D</div>
                </div>
              </div>
            </div>
          </div>
          <div class="fc-probs">
            <div class="prob-segment">
              <div class="ps-label">LEE</div>
              <div class="ps-pct ps-h">38.5%</div>
            </div>
            <div class="prob-bar-row">
              <div class="prob-bar">
                <div class="pb-h" style="flex: 38.5"></div>
                <div class="pb-d" style="flex: 27.8"></div>
                <div class="pb-a" style="flex: 33.7"></div>
              </div>
            </div>
            <div class="prob-segment">
              <div class="ps-label">Draw</div>
              <div class="ps-pct ps-d">27.8%</div>
            </div>
            <div class="prob-segment">
              <div class="ps-label">BRE</div>
              <div class="ps-pct ps-a">33.7%</div>
            </div>
          </div>
          <div class="fc-stats">
            <div class="stat-grid">
              <div class="stat-cell">
                <div class="sc-name">Corners</div>
                <div class="sc-vals">
                  <span class="sc-lo">7</span><span class="sc-sep">—</span
                  ><span class="sc-hi">14</span><span class="sc-med">10</span>
                </div>
                <div class="sc-bar">
                  <div class="sc-bar-lo" style="width: 50%"></div>
                  <div class="sc-bar-hi" style="width: 76%"></div>
                </div>
                <div class="sc-ctx">
                  LEE 3 corners vs CRY (away) · BRE avg 5.06/g season · Elland
                  Road = high-tempo game
                </div>
              </div>
              <div class="stat-cell">
                <div class="sc-name">Shots on Target</div>
                <div class="sc-vals">
                  <span class="sc-lo">5</span><span class="sc-sep">—</span
                  ><span class="sc-hi">11</span><span class="sc-med">7</span>
                </div>
                <div class="sc-bar">
                  <div class="sc-bar-lo" style="width: 42%"></div>
                  <div class="sc-bar-hi" style="width: 70%"></div>
                </div>
                <div class="sc-ctx">
                  LEE 3 SoT vs CRY · BRE 4 SoT avg/g · Elland Road noise drives
                  pressing
                </div>
              </div>
              <div class="stat-cell">
                <div class="sc-name">Fouls</div>
                <div class="sc-vals">
                  <span class="sc-lo">18</span><span class="sc-sep">—</span
                  ><span class="sc-hi">28</span><span class="sc-med">22</span>
                </div>
                <div class="sc-bar">
                  <div class="sc-bar-lo" style="width: 50%"></div>
                  <div class="sc-bar-hi" style="width: 72%"></div>
                </div>
                <div class="sc-ctx">
                  LEE 11 vs CRY · BRE 10 vs BOU · LEE had 2 yellows + 1 red vs
                  CRY · combative game
                </div>
              </div>
              <div class="stat-cell">
                <div class="sc-name">Throw-ins</div>
                <div class="sc-vals">
                  <span class="sc-lo">30</span><span class="sc-sep">—</span
                  ><span class="sc-hi">46</span><span class="sc-med">38</span>
                </div>
                <div class="sc-bar">
                  <div class="sc-bar-lo" style="width: 48%"></div>
                  <div class="sc-bar-hi" style="width: 70%"></div>
                </div>
                <div class="sc-ctx">
                  LEE 23 TIs away vs CRY · BRE 22 vs BOU · Elland Road wide
                  pitch = more TIs
                </div>
              </div>
              <div class="stat-cell">
                <div class="sc-name">Goal Kicks</div>
                <div class="sc-vals">
                  <span class="sc-lo">12</span><span class="sc-sep">—</span
                  ><span class="sc-hi">22</span><span class="sc-med">17</span>
                </div>
                <div class="sc-bar">
                  <div class="sc-bar-lo" style="width: 42%"></div>
                  <div class="sc-bar-hi" style="width: 66%"></div>
                </div>
                <div class="sc-ctx">
                  LEE 7 GKs vs CRY (away) · BRE 15 GKs vs BOU · Darlow plays
                  long often
                </div>
              </div>
              <div class="stat-cell">
                <div class="sc-name">Total Shots</div>
                <div class="sc-vals">
                  <span class="sc-lo">16</span><span class="sc-sep">—</span
                  ><span class="sc-hi">28</span><span class="sc-med">22</span>
                </div>
                <div class="sc-bar">
                  <div class="sc-bar-lo" style="width: 50%"></div>
                  <div class="sc-bar-hi" style="width: 74%"></div>
                </div>
                <div class="sc-ctx">
                  LEE 8 shots vs CRY (away) · BRE 11 shots vs BOU · Elland Road
                  home avg ~14/g
                </div>
              </div>
              <div class="stat-cell">
                <div class="sc-name">Tackles</div>
                <div class="sc-vals">
                  <span class="sc-lo">24</span><span class="sc-sep">—</span
                  ><span class="sc-hi">36</span><span class="sc-med">28</span>
                </div>
                <div class="sc-bar">
                  <div class="sc-bar-lo" style="width: 50%"></div>
                  <div class="sc-bar-hi" style="width: 72%"></div>
                </div>
                <div class="sc-ctx">
                  Elland Road midfield battles legendary · Leeds press intensely
                  at home · BRE physical too
                </div>
              </div>
            </div>
          </div>
          <div class="btts-row">
            <span class="btts-pill bp-maybe">BTTS MAYBE</span>
            <span class="btts-pill bp-info">LEE 2D-0W-0L home last 3</span>
            <span class="btts-pill bp-info">Thiago vs Piroe key battle</span>
            <span
              class="btts-pill"
              style="
                color: var(--red);
                border-color: rgba(255, 75, 75, 0.35);
                background: var(--red-dim);
              "
              >⬤ LOW confidence</span
            >
          </div>
          <div class="fc-context">
            <span class="ctx-icon">◆</span>
            <p class="ctx-text">
              <strong>Elland Road will be rocking</strong> — Leeds are fighting
              for European football and Brentford are 7th looking to
              consolidate.
              <span class="ht"
                >Leeds have drawn their last 3 home PL games.</span
              >
              <span class="hr"
                >Key Leeds news: Gudmundsson SUSPENDED after his red card at
                Crystal Palace — James Justin deputises at left-back. Okafor
                returns to training but minutes will be managed.</span
              >
              <span class="hr"
                >Brentford injury crisis in defence: Henry (hamstring), Hickey
                (hamstring), Janelt (metatarsal), Dasilva (knee) all OUT.
                Damsgaard trained outside on the eve of the game — Andrews
                giving him every chance to prove fitness.</span
              >
              Brentford's Igor Thiago leads the league for off-the-ball runs.
              The 2-2 Brentford-Wolves on Monday shows Brentford can give up
              goals even against inferior opponents — their makeshift defence
              will be tested at Elland Road.
            </p>
          </div>
        </div>
      </div>
      <!-- end Saturday -->

      <!-- ══════════════════ SUNDAY ══════════════════ -->
      <div class="day-section">
        <div class="day-header reveal">Sunday 22 March 2026</div>

        <!-- ── FIXTURE 5: Newcastle vs Sunderland (THE BIG ONE) ── -->
        <div class="fc reveal">
          <div class="fc-ko">
            <div>
              <span class="ko-time c-volt">12:00 GMT</span>
              <span class="ko-comp"> · St. James' Park · Newcastle</span>
            </div>
            <span class="ko-badge stake-high">🔥 Tyne-Wear Derby</span>
          </div>
          <div class="fc-top">
            <div class="fc-team">
              <div class="fc-badge">
                <img
                  src="https://crests.football-data.org/67.png"
                  alt="Newcastle"
                  loading="lazy"
                  style="background-color: #13151f;"
                />
              </div>
              <div class="fc-team-info">
                <div class="fc-club">Newcastle</div>
                <div class="fc-meta">9th · 42pts</div>
                <div class="form-row">
                  <div class="fb fw">W</div>
                  <div class="fb fl">L</div>
                  <div class="fb fw">W</div>
                  <div class="fb fd">D</div>
                  <div class="fb fl">L</div>
                </div>
              </div>
            </div>
            <div class="fc-mid">
              <div class="fc-pred-lbl">Predicted</div>
              <div class="fc-score">1–1</div>
              <div class="fc-prob">Draw · derby</div>
            </div>
            <div class="fc-team away">
              <div class="fc-badge">
                <img
                  src="https://crests.football-data.org/71.png"
                  alt="Sunderland"
                  loading="lazy"
                  style="background-color: #13151f;"
                />
              </div>
              <div class="fc-team-info">
                <div class="fc-club">Sunderland</div>
                <div class="fc-meta">13th · 40pts</div>
                <div class="form-row r">
                  <div class="fb fl">L</div>
                  <div class="fb fw">W</div>
                  <div class="fb fl">L</div>
                  <div class="fb fd">D</div>
                  <div class="fb fd">D</div>
                </div>
              </div>
            </div>
          </div>
          <div class="fc-probs">
            <div class="prob-segment">
              <div class="ps-label">NEW</div>
              <div class="ps-pct ps-h">57.3%</div>
            </div>
            <div class="prob-bar-row">
              <div class="prob-bar">
                <div class="pb-h" style="flex: 57.3"></div>
                <div class="pb-d" style="flex: 24.1"></div>
                <div class="pb-a" style="flex: 18.6"></div>
              </div>
            </div>
            <div class="prob-segment">
              <div class="ps-label">Draw</div>
              <div class="ps-pct ps-d">24.1%</div>
            </div>
            <div class="prob-segment">
              <div class="ps-label">SUN</div>
              <div class="ps-pct ps-a" style="color: var(--fg3)">18.6%</div>
            </div>
          </div>
          <div class="fc-stats">
            <div class="stat-grid">
              <div class="stat-cell">
                <div class="sc-name">Corners</div>
                <div class="sc-vals">
                  <span class="sc-lo">4</span><span class="sc-sep">—</span
                  ><span class="sc-hi">10</span><span class="sc-med">7</span>
                </div>
                <div class="sc-bar">
                  <div class="sc-bar-lo" style="width: 32%"></div>
                  <div class="sc-bar-hi" style="width: 60%"></div>
                </div>
                <div class="sc-ctx">
                  NEW 1 corner vs CFC · SUN 7 corners vs BRI · Dec derby: very
                  low corners · defensive patterns dominate
                </div>
              </div>
              <div class="stat-cell">
                <div class="sc-name">Shots on Target</div>
                <div class="sc-vals">
                  <span class="sc-lo">3</span><span class="sc-sep">—</span
                  ><span class="sc-hi">9</span><span class="sc-med">5</span>
                </div>
                <div class="sc-bar">
                  <div class="sc-bar-lo" style="width: 28%"></div>
                  <div class="sc-bar-hi" style="width: 56%"></div>
                </div>
                <div class="sc-ctx">
                  Dec derby: 0.54 xG combined from 11 shots — 2nd lowest xG PL
                  game ever recorded! · Derby = tight
                </div>
              </div>
              <div class="stat-cell">
                <div class="sc-name">Fouls</div>
                <div class="sc-vals">
                  <span class="sc-lo">20</span><span class="sc-sep">—</span
                  ><span class="sc-hi">34</span><span class="sc-med">26</span>
                </div>
                <div class="sc-bar">
                  <div class="sc-bar-lo" style="width: 50%"></div>
                  <div class="sc-bar-hi" style="width: 76%"></div>
                </div>
                <div class="sc-ctx">
                  Derby intensity = many fouls · SUN 7 fouls vs BRI (low) but
                  derby raises that · Derby physics rules
                </div>
              </div>
              <div class="stat-cell">
                <div class="sc-name">Throw-ins</div>
                <div class="sc-vals">
                  <span class="sc-lo">30</span><span class="sc-sep">—</span
                  ><span class="sc-hi">50</span><span class="sc-med">40</span>
                </div>
                <div class="sc-bar">
                  <div class="sc-bar-lo" style="width: 48%"></div>
                  <div class="sc-bar-hi" style="width: 74%"></div>
                </div>
                <div class="sc-ctx">
                  SUN 28 TIs vs BRI · NEW 16 TIs vs CFC · Derby physical battles
                  generate sideline play · high range
                </div>
              </div>
              <div class="stat-cell">
                <div class="sc-name">Goal Kicks</div>
                <div class="sc-vals">
                  <span class="sc-lo">14</span><span class="sc-sep">—</span
                  ><span class="sc-hi">26</span><span class="sc-med">20</span>
                </div>
                <div class="sc-bar">
                  <div class="sc-bar-lo" style="width: 44%"></div>
                  <div class="sc-bar-hi" style="width: 72%"></div>
                </div>
                <div class="sc-ctx">
                  NEW 13 GKs vs CFC · SUN 5 GKs vs BRI · Ramsdale launches long
                  · high GK count when teams defend
                </div>
              </div>
              <div class="stat-cell">
                <div class="sc-name">Total Shots</div>
                <div class="sc-vals">
                  <span class="sc-lo">10</span><span class="sc-sep">—</span
                  ><span class="sc-hi">20</span><span class="sc-med">14</span>
                </div>
                <div class="sc-bar">
                  <div class="sc-bar-lo" style="width: 38%"></div>
                  <div class="sc-bar-hi" style="width: 64%"></div>
                </div>
                <div class="sc-ctx">
                  Dec derby: 11 total shots · NEW 6 shots vs CFC (very low) ·
                  Derby = defensive priority
                </div>
              </div>
              <div class="stat-cell">
                <div class="sc-name">Tackles</div>
                <div class="sc-vals">
                  <span class="sc-lo">30</span><span class="sc-sep">—</span
                  ><span class="sc-hi">48</span><span class="sc-med">38</span>
                </div>
                <div class="sc-bar">
                  <div class="sc-bar-lo" style="width: 54%"></div>
                  <div class="sc-bar-hi" style="width: 80%"></div>
                </div>
                <div class="sc-ctx">
                  Derby = maximum tackles · Xhaka vs depleted NEW midfield (no
                  Guimarães) · St James' Park atmosphere elevates every duel
                </div>
              </div>
            </div>
          </div>
          <div class="btts-row">
            <span class="btts-pill bp-no">BTTS UNLIKELY</span>
            <span class="btts-pill bp-no">U2.5 goals likely</span>
            <span class="btts-pill bp-info"
              >NEW: Guimarães · Schar · Krafth OUT</span
            >
            <span class="btts-pill bp-info"
              >SUN: Xhaka fit · Reinildo fit · Brobbey fit</span
            >
            <span class="btts-pill bp-maybe">Red card risk HIGH</span>
            <span
              class="btts-pill"
              style="
                color: var(--red);
                border-color: rgba(255, 75, 75, 0.35);
                background: var(--red-dim);
              "
              >⬤ LOW confidence</span
            >
          </div>
          <div class="fc-context">
            <span class="ctx-icon">◆</span>
            <p class="ctx-text">
              <span class="hr">The match of the weekend.</span>
              <strong
                >Newcastle are winless in their last 5 PL home derbies (D2
                L3)</strong
              >
              and Sunderland have won 7 of the last 8 fixtures between these
              sides. The December derby produced just 0.54 xG from 11 shots —
              <span class="hl"
                >the second-lowest combined xG in PL history.</span
              >
              <span class="ht"
                >Key injuries: Bruno Guimarães (hamstring — OUT), Fabian Schar
                (ankle — OUT), Emil Krafth (OUT). Sandro Tonali is a doubt after
                limping off vs Barcelona but Howe said "not as bad as first
                feared".</span
              >
              Livramento replaces Trippier at right-back.
              <span class="ho"
                >For Sunderland: Granit Xhaka AVAILABLE and expected to start.
                Reinildo available after return from knee injury. Brian Brobbey
                fit. Doubts: Ballard, Le Fee, Roefs, Mukiele.</span
              >
              Newcastle reeling from a 7-2 hammering at Barcelona midweek —
              Elanga scored twice but defensive confidence shot. Expect maximum
              intensity, few clear chances, and lots of physical duels.
            </p>
          </div>
        </div>

        <!-- ── FIXTURE 6: Aston Villa vs West Ham ── -->
        <div class="fc reveal">
          <div class="fc-ko">
            <div>
              <span class="ko-time c-volt">14:15 GMT</span>
              <span class="ko-comp"> · Villa Park · Birmingham</span>
            </div>
            <span class="ko-badge stake-med">Mid stakes</span>
          </div>
          <div class="fc-top">
            <div class="fc-team">
              <div class="fc-badge">
                <img
                  src="https://crests.football-data.org/58.png"
                  alt="Aston Villa"
                  loading="lazy"
                  style="background-color: #13151f;"
                />
              </div>
              <div class="fc-team-info">
                <div class="fc-club">Aston Villa</div>
                <div class="fc-meta">4th · 51pts</div>
                <div class="form-row">
                  <div class="fb fl">L</div>
                  <div class="fb fl">L</div>
                  <div class="fb fd">D</div>
                  <div class="fb fw">W</div>
                  <div class="fb fw">W</div>
                </div>
              </div>
            </div>
            <div class="fc-mid">
              <div class="fc-pred-lbl">Predicted</div>
              <div class="fc-score">2–0</div>
              <div class="fc-prob">AVL · 49.5%</div>
            </div>
            <div class="fc-team away">
              <div class="fc-badge">
                <img
                  src="https://crests.football-data.org/563.png"
                  alt="West Ham"
                  loading="lazy"
                  style="background-color: #13151f;"
                />
              </div>
              <div class="fc-team-info">
                <div class="fc-club">West Ham</div>
                <div class="fc-meta">18th · 29pts</div>
                <div class="form-row r">
                  <div class="fb fd">D</div>
                  <div class="fb fw">W</div>
                  <div class="fb fl">L</div>
                  <div class="fb fl">L</div>
                  <div class="fb fd">D</div>
                </div>
              </div>
            </div>
          </div>
          <div class="fc-probs">
            <div class="prob-segment">
              <div class="ps-label">AVL</div>
              <div class="ps-pct ps-h">49.5%</div>
            </div>
            <div class="prob-bar-row">
              <div class="prob-bar">
                <div class="pb-h" style="flex: 49.5"></div>
                <div class="pb-d" style="flex: 26.1"></div>
                <div class="pb-a" style="flex: 24.4"></div>
              </div>
            </div>
            <div class="prob-segment">
              <div class="ps-label">Draw</div>
              <div class="ps-pct ps-d">26.1%</div>
            </div>
            <div class="prob-segment">
              <div class="ps-label">WHU</div>
              <div class="ps-pct ps-a" style="color: var(--fg3)">24.4%</div>
            </div>
          </div>
          <div class="fc-stats">
            <div class="stat-grid">
              <div class="stat-cell">
                <div class="sc-name">Corners</div>
                <div class="sc-vals">
                  <span class="sc-lo">5</span><span class="sc-sep">—</span
                  ><span class="sc-hi">12</span><span class="sc-med">8</span>
                </div>
                <div class="sc-bar">
                  <div class="sc-bar-lo" style="width: 40%"></div>
                  <div class="sc-bar-hi" style="width: 68%"></div>
                </div>
                <div class="sc-ctx">
                  AVL 6 vs MUN · WHU 1 vs MCI (very low, 29% poss) · WHU
                  typically low corners away
                </div>
              </div>
              <div class="stat-cell">
                <div class="sc-name">Shots on Target</div>
                <div class="sc-vals">
                  <span class="sc-lo">4</span><span class="sc-sep">—</span
                  ><span class="sc-hi">10</span><span class="sc-med">7</span>
                </div>
                <div class="sc-bar">
                  <div class="sc-bar-lo" style="width: 36%"></div>
                  <div class="sc-bar-hi" style="width: 66%"></div>
                </div>
                <div class="sc-ctx">
                  AVL 2 SoT vs MUN · WHU 1 SoT vs MCI · AVL home usually more
                  clinical · Watkins threat
                </div>
              </div>
              <div class="stat-cell">
                <div class="sc-name">Fouls</div>
                <div class="sc-vals">
                  <span class="sc-lo">16</span><span class="sc-sep">—</span
                  ><span class="sc-hi">26</span><span class="sc-med">20</span>
                </div>
                <div class="sc-bar">
                  <div class="sc-bar-lo" style="width: 46%"></div>
                  <div class="sc-bar-hi" style="width: 68%"></div>
                </div>
                <div class="sc-ctx">
                  AVL 5 vs MUN · WHU 14 vs MCI · West Ham foul heavily when
                  struggling · combined avg ~20
                </div>
              </div>
              <div class="stat-cell">
                <div class="sc-name">Throw-ins</div>
                <div class="sc-vals">
                  <span class="sc-lo">22</span><span class="sc-sep">—</span
                  ><span class="sc-hi">38</span><span class="sc-med">30</span>
                </div>
                <div class="sc-bar">
                  <div class="sc-bar-lo" style="width: 40%"></div>
                  <div class="sc-bar-hi" style="width: 62%"></div>
                </div>
                <div class="sc-ctx">
                  AVL 11 TIs vs MUN · WHU 18 TIs vs MCI · Villa Park games tend
                  to be more controlled
                </div>
              </div>
              <div class="stat-cell">
                <div class="sc-name">Goal Kicks</div>
                <div class="sc-vals">
                  <span class="sc-lo">10</span><span class="sc-sep">—</span
                  ><span class="sc-hi">20</span><span class="sc-med">14</span>
                </div>
                <div class="sc-bar">
                  <div class="sc-bar-lo" style="width: 38%"></div>
                  <div class="sc-bar-hi" style="width: 62%"></div>
                </div>
                <div class="sc-ctx">
                  AVL 7 GKs vs MUN · WHU 11 GKs vs MCI · Martinez plays short ·
                  Areola launches long
                </div>
              </div>
              <div class="stat-cell">
                <div class="sc-name">Total Shots</div>
                <div class="sc-vals">
                  <span class="sc-lo">14</span><span class="sc-sep">—</span
                  ><span class="sc-hi">24</span><span class="sc-med">18</span>
                </div>
                <div class="sc-bar">
                  <div class="sc-bar-lo" style="width: 44%"></div>
                  <div class="sc-bar-hi" style="width: 68%"></div>
                </div>
                <div class="sc-ctx">
                  AVL 7 shots vs MUN (away) · WHU 1 shot vs MCI (shocking) · AVL
                  home usually 15-18 shots
                </div>
              </div>
              <div class="stat-cell">
                <div class="sc-name">Tackles</div>
                <div class="sc-vals">
                  <span class="sc-lo">20</span><span class="sc-sep">—</span
                  ><span class="sc-hi">30</span><span class="sc-med">24</span>
                </div>
                <div class="sc-bar">
                  <div class="sc-bar-lo" style="width: 42%"></div>
                  <div class="sc-bar-hi" style="width: 64%"></div>
                </div>
                <div class="sc-ctx">
                  Emery's Villa press high · WHU survival = hard work · but
                  talent gap large
                </div>
              </div>
            </div>
          </div>
          <div class="btts-row">
            <span class="btts-pill bp-no">BTTS NO</span>
            <span class="btts-pill bp-info">WHU 18th, survival fight</span>
            <span class="btts-pill bp-info">AVL UCL hunt</span>
            <span class="btts-pill bp-info">Watkins leads AVL attack</span>
            <span
              class="btts-pill"
              style="
                color: var(--win);
                border-color: rgba(34, 211, 122, 0.4);
                background: var(--win-dim);
              "
              >⬤ HIGH confidence</span
            >
          </div>
          <div class="fc-context">
            <span class="ctx-icon">◆</span>
            <p class="ctx-text">
              <strong>Villa are 4th and chasing Champions League</strong> — full
              motivation.
              <span class="hr"
                >West Ham are 18th and in a relegation battle</span
              >, but WhoScored data shows WHU have lost just 2 of their last 9
              PL games — more resilient than their position suggests.
              <span class="hr"
                >Summerville is OUT after being omitted from the Netherlands
                squad — a big loss for WHU's attack.</span
              >
              Bowen leads West Ham's forward line, supported by Wan-Bissaka
              overlapping.
              <strong
                >Confirmed AVL XI: Martinez; Cash, Konsa, Torres, Maatsen;
                Onana, Luiz; McGinn, Rogers, Sancho; Watkins.</strong
              >
              Tielemans has returned to training but is being assessed —
              Onana-Luiz start. Watkins leads AVL's attack with 12 goals.
              <span class="hl"
                >Sancho returns from UEL ineligibility and should bring
                creativity</span
              >. AVL played Thursday (UEL vs Lille) — fatigue factor versus a
              WHU side who have had a full week's rest.
            </p>
          </div>
        </div>

        <!-- ── FIXTURE 7: Tottenham vs Nottingham Forest ── -->
        <div class="fc reveal">
          <div class="fc-ko">
            <div>
              <span class="ko-time c-volt">14:15 GMT</span>
              <span class="ko-comp"> · Tottenham Hotspur Stadium · London</span>
            </div>
            <span class="ko-badge stake-high">🔥 Relegation six-pointer</span>
          </div>
          <div class="fc-top">
            <div class="fc-team">
              <div class="fc-badge">
                <img
                  src="https://crests.football-data.org/73.png"
                  alt="Tottenham"
                  loading="lazy"
                  style="background-color: #13151f;"
                />
              </div>
              <div class="fc-team-info">
                <div class="fc-club">Tottenham</div>
                <div class="fc-meta">16th · 30pts</div>
                <div class="form-row">
                  <div class="fb fd">D</div>
                  <div class="fb fl">L</div>
                  <div class="fb fl">L</div>
                  <div class="fb fl">L</div>
                  <div class="fb fl">L</div>
                </div>
              </div>
            </div>
            <div class="fc-mid">
              <div class="fc-pred-lbl">Predicted</div>
              <div class="fc-score">2–1</div>
              <div class="fc-prob">TOT · 42.1%</div>
            </div>
            <div class="fc-team away">
              <div class="fc-badge">
                <img
                  src="https://crests.football-data.org/351.png"
                  alt="Nottm Forest"
                  loading="lazy"
                  style="background-color: #13151f;"
                />
              </div>
              <div class="fc-team-info">
                <div class="fc-club">Forest</div>
                <div class="fc-meta">17th · 29pts</div>
                <div class="form-row r">
                  <div class="fb fd">D</div>
                  <div class="fb fd">D</div>
                  <div class="fb fw">W</div>
                  <div class="fb fl">L</div>
                  <div class="fb fd">D</div>
                </div>
              </div>
            </div>
          </div>
          <div class="fc-probs">
            <div class="prob-segment">
              <div class="ps-label">TOT</div>
              <div class="ps-pct ps-h">42.1%</div>
            </div>
            <div class="prob-bar-row">
              <div class="prob-bar">
                <div class="pb-h" style="flex: 42.1"></div>
                <div class="pb-d" style="flex: 27.9"></div>
                <div class="pb-a" style="flex: 30"></div>
              </div>
            </div>
            <div class="prob-segment">
              <div class="ps-label">Draw</div>
              <div class="ps-pct ps-d">27.9%</div>
            </div>
            <div class="prob-segment">
              <div class="ps-label">NFO</div>
              <div class="ps-pct ps-a">30.0%</div>
            </div>
          </div>
          <div class="fc-stats">
            <div class="stat-grid">
              <div class="stat-cell">
                <div class="sc-name">Corners</div>
                <div class="sc-vals">
                  <span class="sc-lo">5</span><span class="sc-sep">—</span
                  ><span class="sc-hi">11</span><span class="sc-med">8</span>
                </div>
                <div class="sc-bar">
                  <div class="sc-bar-lo" style="width: 40%"></div>
                  <div class="sc-bar-hi" style="width: 66%"></div>
                </div>
                <div class="sc-ctx">
                  TOT 4 corners vs LFC · NFO 5 corners vs FUL · home push
                  generates more corners for TOT
                </div>
              </div>
              <div class="stat-cell">
                <div class="sc-name">Shots on Target</div>
                <div class="sc-vals">
                  <span class="sc-lo">5</span><span class="sc-sep">—</span
                  ><span class="sc-hi">12</span><span class="sc-med">8</span>
                </div>
                <div class="sc-bar">
                  <div class="sc-bar-lo" style="width: 40%"></div>
                  <div class="sc-bar-hi" style="width: 70%"></div>
                </div>
                <div class="sc-ctx">
                  TOT 7 SoT vs LFC (impressive) · NFO 2 SoT vs FUL · Both teams
                  in survival zone = effort
                </div>
              </div>
              <div class="stat-cell">
                <div class="sc-name">Fouls</div>
                <div class="sc-vals">
                  <span class="sc-lo">18</span><span class="sc-sep">—</span
                  ><span class="sc-hi">30</span><span class="sc-med">24</span>
                </div>
                <div class="sc-bar">
                  <div class="sc-bar-lo" style="width: 48%"></div>
                  <div class="sc-bar-hi" style="width: 72%"></div>
                </div>
                <div class="sc-ctx">
                  TOT 13 fouls vs LFC · NFO 8 fouls vs FUL · survival game =
                  more fouls · Tudor teams foul lots
                </div>
              </div>
              <div class="stat-cell">
                <div class="sc-name">Throw-ins</div>
                <div class="sc-vals">
                  <span class="sc-lo">30</span><span class="sc-sep">—</span
                  ><span class="sc-hi">48</span><span class="sc-med">38</span>
                </div>
                <div class="sc-bar">
                  <div class="sc-bar-lo" style="width: 46%"></div>
                  <div class="sc-bar-hi" style="width: 68%"></div>
                </div>
                <div class="sc-ctx">
                  TOT 24 TIs vs LFC · NFO 25 TIs vs FUL · Both teams generate
                  lots of sideline duels
                </div>
              </div>
              <div class="stat-cell">
                <div class="sc-name">Goal Kicks</div>
                <div class="sc-vals">
                  <span class="sc-lo">14</span><span class="sc-sep">—</span
                  ><span class="sc-hi">26</span><span class="sc-med">20</span>
                </div>
                <div class="sc-bar">
                  <div class="sc-bar-lo" style="width: 44%"></div>
                  <div class="sc-bar-hi" style="width: 70%"></div>
                </div>
                <div class="sc-ctx">
                  TOT 16 GKs vs LFC · NFO 5 GKs vs FUL · Vicario goal kick count
                  high when defending deep
                </div>
              </div>
              <div class="stat-cell">
                <div class="sc-name">Total Shots</div>
                <div class="sc-vals">
                  <span class="sc-lo">16</span><span class="sc-sep">—</span
                  ><span class="sc-hi">28</span><span class="sc-med">22</span>
                </div>
                <div class="sc-bar">
                  <div class="sc-bar-lo" style="width: 48%"></div>
                  <div class="sc-bar-hi" style="width: 72%"></div>
                </div>
                <div class="sc-ctx">
                  TOT 12 shots vs LFC · NFO 13 shots vs FUL · Both teams have
                  high shot volumes for their league position
                </div>
              </div>
              <div class="stat-cell">
                <div class="sc-name">Tackles</div>
                <div class="sc-vals">
                  <span class="sc-lo">26</span><span class="sc-sep">—</span
                  ><span class="sc-hi">40</span><span class="sc-med">32</span>
                </div>
                <div class="sc-bar">
                  <div class="sc-bar-lo" style="width: 50%"></div>
                  <div class="sc-bar-hi" style="width: 74%"></div>
                </div>
                <div class="sc-ctx">
                  Relegation 6-pointer feel · TOT fight or sink · NFO away =
                  work-rate heavy · both sides desperate
                </div>
              </div>
            </div>
          </div>
          <div class="btts-row">
            <span class="btts-pill bp-maybe">BTTS MAYBE</span>
            <span class="btts-pill bp-maybe"
              >Van de Ven SUSP · TOT defence exposed</span
            >
            <span class="btts-pill bp-info"
              >Solanke fit · Palhinha cleared</span
            >
            <span class="btts-pill bp-info"
              >Richarlison returns from suspension</span
            >
            <span class="btts-pill bp-maybe">Yellow card fest likely</span>
            <span
              class="btts-pill"
              style="
                color: var(--red);
                border-color: rgba(255, 75, 75, 0.35);
                background: var(--red-dim);
              "
              >⬤ LOW confidence</span
            >
          </div>
          <div class="fc-context">
            <span class="ctx-icon">◆</span>
            <p class="ctx-text">
              <span class="hr">An outright relegation six-pointer</span> — Spurs
              16th (30pts), Forest 17th (29pts), West Ham 18th (29pts). Only 1
              point separates 16th and 18th.
              <strong
                >Both teams are desperate, which drives fouls, cards and tackles
                UP significantly.</strong
              >
              <br /><br />
              <span class="ht">Tottenham confirmed absences:</span>
              <strong>Micky van de Ven SUSPENDED</strong> (red card vs Crystal
              Palace) — a massive blow to Spurs' best defender. Odobert (ACL —
              season), Maddison (ACL — season), Bentancur (hamstring, out to
              May), Kudus (thigh, out to April), Davies (ankle) all OUT.
              <span class="hl"
                >Positives: Solanke returns from hip injury and is fit to start.
                Palhinha has been cleared after concussion protocols. Romero,
                Bergvall, Gallagher and Udogie all available. Richarlison
                returns from suspension and will start.</span
              >
              <br /><br />
              <span class="ht">Confirmed TOT XI:</span> Kinsky; Porro, Romero,
              Dragusin, Udogie; Palhinha, Bergvall; Gallagher, Tel, Richarlison;
              Solanke. <br /><br />
              <span class="ht">Nottingham Forest confirmed absences:</span>
              Chris Wood (knee — season), Boly (knee), Savona (knee), Cunha
              (foot). Hudson-Odoi is a doubt after sitting out training
              Thursday. Netz missed the UEL second leg at Midtjylland
              (ineligible) but is available domestically. Gibbs-White is the key
              creative force and starts.
              <span class="hl">Confirmed NFO XI:</span> Sels; Aina, Murillo,
              Morato, Williams; Sangare, Anderson; Hutchinson, Gibbs-White,
              Netz; Awoniyi. Forest lost 2-1 in Denmark on Thursday — morale and
              fitness both potential issues after European travel. Tudor's Spurs
              meanwhile had the full week to prepare — home advantage, rested
              squad (minus the injured), and a raucous Spurs Stadium crowd.
              Expect a fractious, foul-heavy, high-tackle game decided by one
              moment of quality.
            </p>
          </div>
        </div>
      </div>
      <!-- end Sunday -->

      <!-- ══════════════════════════════════════
     WEEKEND SUMMARY
══════════════════════════════════════ -->
      <div class="day-section reveal">
        <div class="day-header">Weekend Summary · All 7 Predictions</div>

        <style>
          /* ── SUMMARY TABLE ── */
          .sum-wrap {
            overflow-x: auto;
            -webkit-overflow-scrolling: touch;
            margin-bottom: 14px;
            border-radius: var(--r-sm);
          }
          .sum-table {
            width: 100%;
            border-collapse: collapse;
            min-width: 680px;
          }
          .sum-table thead th {
            font-family: "JetBrains Mono", monospace;
            font-size: 10px;
            letter-spacing: 0.1em;
            text-transform: uppercase;
            color: var(--fg3);
            background: var(--bg2);
            padding: 10px 12px;
            text-align: left;
            border-bottom: 2px solid var(--border2);
            white-space: nowrap;
          }
          .sum-table thead th:first-child {
            border-radius: var(--r-sm) 0 0 0;
          }
          .sum-table thead th:last-child {
            border-radius: 0 var(--r-sm) 0 0;
          }
          .sum-table tbody td {
            padding: 11px 12px;
            vertical-align: middle;
          }

          /* data row — no bottom border (conf-row sits below it) */
          .sum-table tbody tr.data-row td {
            border-bottom: none;
            padding-bottom: 6px;
          }

          /* confidence row spanning full width */
          .sum-table tbody tr.conf-row td {
            padding: 0 12px 12px;
            border-bottom: 1px solid var(--border);
          }
          .sum-table tbody tr.conf-row:last-child td {
            border-bottom: none;
          }
          .conf-row-inner {
            display: flex;
            align-items: center;
            gap: 10px;
            padding: 7px 12px;
            border-radius: var(--r-xs);
            background: rgba(255, 255, 255, 0.025);
            border: 1px solid var(--border);
          }

          .td-fix {
            font-size: 13px;
            font-weight: 600;
            color: var(--fg);
            white-space: nowrap;
          }
          .td-fix-sub {
            font-family: "JetBrains Mono", monospace;
            font-size: 9px;
            color: var(--fg3);
            margin-top: 2px;
            white-space: nowrap;
          }
          .td-ko {
            font-family: "JetBrains Mono", monospace;
            font-size: 11px;
            color: var(--fg2);
            white-space: nowrap;
          }
          .td-score {
            font-size: 18px;
            font-weight: 800;
            color: var(--volt);
            letter-spacing: 0.02em;
            white-space: nowrap;
          }
          .td-winner {
            font-family: "JetBrains Mono", monospace;
            font-size: 10px;
            font-weight: 600;
            padding: 3px 9px;
            border-radius: var(--r-xs);
            border: 1px solid;
            white-space: nowrap;
          }
          .tw-h {
            color: var(--volt);
            border-color: rgba(200, 245, 66, 0.35);
            background: var(--volt-dim);
          }
          .tw-a {
            color: var(--teal);
            border-color: rgba(18, 232, 200, 0.35);
            background: var(--teal-dim);
          }
          .tw-d {
            color: var(--fg3);
            border-color: var(--border2);
            background: rgba(255, 255, 255, 0.03);
          }

          /* confidence badges */
          .td-conf {
            text-align: left;
          }
          .conf-badge {
            display: inline-flex;
            align-items: center;
            gap: 5px;
            font-family: "JetBrains Mono", monospace;
            font-size: 10px;
            font-weight: 700;
            padding: 4px 10px;
            border-radius: var(--r-xs);
            border: 1px solid;
            white-space: nowrap;
            flex-shrink: 0;
          }
          .conf-high {
            color: var(--win);
            border-color: rgba(34, 211, 122, 0.4);
            background: var(--win-dim);
          }
          .conf-med {
            color: var(--orange);
            border-color: rgba(255, 122, 40, 0.4);
            background: var(--orange-dim);
          }
          .conf-low {
            color: var(--red);
            border-color: rgba(255, 75, 75, 0.35);
            background: var(--red-dim);
          }
          .conf-dot {
            width: 6px;
            height: 6px;
            border-radius: 50%;
            flex-shrink: 0;
          }
          .cd-high {
            background: var(--win);
          }
          .cd-med {
            background: var(--orange);
          }
          .cd-low {
            background: var(--red);
          }
          .conf-reason {
            font-family: "JetBrains Mono", monospace;
            font-size: 10px;
            color: var(--fg2);
            line-height: 1.4;
          }

          /* stat range cells */
          .td-range {
            white-space: nowrap;
            text-align: center;
          }
          .tr-lo {
            font-family: "JetBrains Mono", monospace;
            font-size: 11px;
            color: var(--teal);
            font-weight: 600;
          }
          .tr-sep {
            font-family: "JetBrains Mono", monospace;
            font-size: 10px;
            color: var(--fg3);
          }
          .tr-med {
            font-size: 14px;
            font-weight: 800;
            color: var(--volt);
            letter-spacing: -0.01em;
          }
          .tr-hi {
            font-family: "JetBrains Mono", monospace;
            font-size: 11px;
            color: var(--orange);
            font-weight: 600;
          }

          .td-btts {
            font-family: "JetBrains Mono", monospace;
            font-size: 10px;
            font-weight: 700;
            padding: 3px 8px;
            border-radius: var(--r-xs);
            border: 1px solid;
            white-space: nowrap;
            text-align: center;
          }
          .btts-y {
            color: var(--win);
            border-color: rgba(34, 211, 122, 0.35);
            background: var(--win-dim);
          }
          .btts-n {
            color: var(--red);
            border-color: rgba(255, 75, 75, 0.35);
            background: var(--red-dim);
          }
          .btts-m {
            color: var(--orange);
            border-color: rgba(255, 122, 40, 0.35);
            background: var(--orange-dim);
          }

          /* ── CARDS ROW ── */
          .sum-cards {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 10px;
            margin-bottom: 14px;
          }
          @media (min-width: 560px) {
            .sum-cards {
              grid-template-columns: repeat(3, 1fr);
            }
          }
          @media (min-width: 840px) {
            .sum-cards {
              grid-template-columns: repeat(4, 1fr);
            }
          }

          .sum-card {
            background: var(--card);
            border: 1px solid var(--border);
            border-radius: var(--r-sm);
            padding: 12px 14px;
            display: flex;
            flex-direction: column;
            gap: 4px;
          }
          .scard-label {
            font-family: "JetBrains Mono", monospace;
            font-size: 9px;
            letter-spacing: 0.14em;
            text-transform: uppercase;
            color: var(--fg3);
          }
          .scard-val {
            font-size: 22px;
            font-weight: 800;
            color: var(--volt);
            letter-spacing: -0.02em;
            line-height: 1;
          }
          .scard-sub {
            font-family: "JetBrains Mono", monospace;
            font-size: 10px;
            color: var(--fg2);
            line-height: 1.4;
            margin-top: 2px;
          }
          .scard-val.c-teal {
            color: var(--teal);
          }
          .scard-val.c-orange {
            color: var(--orange);
          }
          .scard-val.c-sky {
            color: var(--sky);
          }
          .scard-val.c-red {
            color: var(--red);
          }
          .scard-val.c-win {
            color: var(--win);
          }

          /* ── WATCHLIST ── */
          .watchlist {
            background: var(--card);
            border: 1px solid var(--border2);
            border-radius: var(--r);
            overflow: hidden;
          }
          .wl-head {
            padding: 12px 14px;
            border-bottom: 1px solid var(--border);
            background: rgba(200, 245, 66, 0.04);
            font-family: "JetBrains Mono", monospace;
            font-size: 10px;
            letter-spacing: 0.16em;
            text-transform: uppercase;
            color: var(--volt);
            display: flex;
            align-items: center;
            gap: 8px;
          }
          .wl-head::before {
            content: "◆";
            font-size: 8px;
          }
          .wl-items {
            display: grid;
            grid-template-columns: 1fr;
            gap: 0;
          }
          @media (min-width: 640px) {
            .wl-items {
              grid-template-columns: 1fr 1fr;
            }
          }
          .wl-item {
            padding: 12px 14px;
            border-bottom: 1px solid var(--border);
            display: flex;
            flex-direction: column;
            gap: 3px;
          }
          @media (min-width: 640px) {
            .wl-item {
              border-right: 1px solid var(--border);
            }
            .wl-item:nth-child(2n) {
              border-right: none;
            }
          }
          .wl-item:last-child,
          .wl-item:nth-last-child(2):nth-child(2n-1) {
            border-bottom: none;
          }
          .wl-tag {
            font-family: "JetBrains Mono", monospace;
            font-size: 9px;
            letter-spacing: 0.1em;
            text-transform: uppercase;
            margin-bottom: 2px;
          }
          .wl-fix {
            font-size: 13px;
            font-weight: 700;
            color: var(--fg);
          }
          .wl-note {
            font-family: "JetBrains Mono", monospace;
            font-size: 10px;
            color: var(--fg2);
            line-height: 1.5;
          }
        </style>

        <!-- AGGREGATE STAT CARDS -->
        <div class="sum-cards">
          <div class="sum-card">
            <div class="scard-label">Highest corner game</div>
            <div class="scard-val">BRI–LFC</div>
            <div class="scard-sub">
              Median 10 · max 13<br />Both attack wide
            </div>
          </div>
          <div class="sum-card">
            <div class="scard-label">Lowest corner game</div>
            <div class="scard-val c-teal">NEW–SUN</div>
            <div class="scard-sub">Median 7 · min 4<br />Derby defensive</div>
          </div>
          <div class="sum-card">
            <div class="scard-label">Highest foul game</div>
            <div class="scard-val c-orange">TOT–NFO</div>
            <div class="scard-sub">
              Median 24 · max 30<br />Relegation six-pointer
            </div>
          </div>
          <div class="sum-card">
            <div class="scard-label">Most tackles</div>
            <div class="scard-val c-red">NEW–SUN</div>
            <div class="scard-sub">
              Median 38 · max 48<br />Derby = max effort
            </div>
          </div>
          <div class="sum-card">
            <div class="scard-label">Most throw-ins</div>
            <div class="scard-val c-sky">FUL–BUR</div>
            <div class="scard-sub">
              Median 36 · max 44<br />Burnley generate lots
            </div>
          </div>
          <div class="sum-card">
            <div class="scard-label">Most goal kicks</div>
            <div class="scard-val c-orange">FUL–BUR</div>
            <div class="scard-sub">
              Median 17 · max 22<br />Burnley long-ball style
            </div>
          </div>
          <div class="sum-card">
            <div class="scard-label">Highest xGoals game</div>
            <div class="scard-val c-win">BRI–LFC</div>
            <div class="scard-sub">
              H2H avg 3.41 goals<br />BTTS 64% historical
            </div>
          </div>
          <div class="sum-card">
            <div class="scard-label">Match of weekend</div>
            <div class="scard-val c-red">NEW–SUN</div>
            <div class="scard-sub">
              Tyne-Wear Derby<br />First at SJP in 10 yrs
            </div>
          </div>
        </div>

        <!-- FULL PREDICTIONS TABLE -->
        <div class="sum-wrap">
          <table class="sum-table">
            <thead>
              <tr>
                <th>Fixture</th>
                <th>KO</th>
                <th>Predicted</th>
                <th>Winner</th>
                <th>
                  Corners<br /><span style="font-size: 9px; opacity: 0.6"
                    >lo · med · hi</span
                  >
                </th>
                <th>
                  SoT<br /><span style="font-size: 9px; opacity: 0.6"
                    >lo · med · hi</span
                  >
                </th>
                <th>
                  Fouls<br /><span style="font-size: 9px; opacity: 0.6"
                    >lo · med · hi</span
                  >
                </th>
                <th>
                  Throw-ins<br /><span style="font-size: 9px; opacity: 0.6"
                    >lo · med · hi</span
                  >
                </th>
                <th>
                  Goal Kicks<br /><span style="font-size: 9px; opacity: 0.6"
                    >lo · med · hi</span
                  >
                </th>
                <th>
                  Tackles<br /><span style="font-size: 9px; opacity: 0.6"
                    >lo · med · hi</span
                  >
                </th>
                <th>BTTS</th>
              </tr>
            </thead>
            <tbody>
              <!-- Brighton vs Liverpool -->
              <tr class="data-row">
                <td>
                  <div class="td-fix">Brighton vs Liverpool</div>
                  <div class="td-fix-sub">Sat · Amex Stadium</div>
                </td>
                <td class="td-ko">12:30</td>
                <td><div class="td-score">1–2</div></td>
                <td><span class="td-winner tw-a">LFC</span></td>
                <td class="td-range">
                  <span class="tr-lo">7</span><span class="tr-sep"> · </span
                  ><span class="tr-med">10</span><span class="tr-sep"> · </span
                  ><span class="tr-hi">13</span>
                </td>
                <td class="td-range">
                  <span class="tr-lo">5</span><span class="tr-sep"> · </span
                  ><span class="tr-med">8</span><span class="tr-sep"> · </span
                  ><span class="tr-hi">12</span>
                </td>
                <td class="td-range">
                  <span class="tr-lo">16</span><span class="tr-sep"> · </span
                  ><span class="tr-med">20</span><span class="tr-sep"> · </span
                  ><span class="tr-hi">26</span>
                </td>
                <td class="td-range">
                  <span class="tr-lo">28</span><span class="tr-sep"> · </span
                  ><span class="tr-med">34</span><span class="tr-sep"> · </span
                  ><span class="tr-hi">42</span>
                </td>
                <td class="td-range">
                  <span class="tr-lo">10</span><span class="tr-sep"> · </span
                  ><span class="tr-med">15</span><span class="tr-sep"> · </span
                  ><span class="tr-hi">20</span>
                </td>
                <td class="td-range">
                  <span class="tr-lo">22</span><span class="tr-sep"> · </span
                  ><span class="tr-med">27</span><span class="tr-sep"> · </span
                  ><span class="tr-hi">34</span>
                </td>
                <td><span class="td-btts btts-y">YES</span></td>
              </tr>
              <tr class="conf-row">
                <td colspan="11">
                  <div class="conf-row-inner">
                    <span class="conf-badge conf-med"
                      ><span class="conf-dot cd-med"></span>MED confidence</span
                    >
                    <span class="conf-reason"
                      >Salah OUT · Alisson OUT · BRI bogey team (6/13 LFC wins)
                      · Wirtz leads but LFC missing top scorer</span
                    >
                  </div>
                </td>
              </tr>

              <!-- Fulham vs Burnley -->
              <tr class="data-row">
                <td>
                  <div class="td-fix">Fulham vs Burnley</div>
                  <div class="td-fix-sub">Sat · Craven Cottage</div>
                </td>
                <td class="td-ko">15:00</td>
                <td><div class="td-score">2–0</div></td>
                <td><span class="td-winner tw-h">FUL</span></td>
                <td class="td-range">
                  <span class="tr-lo">6</span><span class="tr-sep"> · </span
                  ><span class="tr-med">9</span><span class="tr-sep"> · </span
                  ><span class="tr-hi">12</span>
                </td>
                <td class="td-range">
                  <span class="tr-lo">4</span><span class="tr-sep"> · </span
                  ><span class="tr-med">6</span><span class="tr-sep"> · </span
                  ><span class="tr-hi">10</span>
                </td>
                <td class="td-range">
                  <span class="tr-lo">16</span><span class="tr-sep"> · </span
                  ><span class="tr-med">20</span><span class="tr-sep"> · </span
                  ><span class="tr-hi">26</span>
                </td>
                <td class="td-range">
                  <span class="tr-lo">28</span><span class="tr-sep"> · </span
                  ><span class="tr-med">36</span><span class="tr-sep"> · </span
                  ><span class="tr-hi">44</span>
                </td>
                <td class="td-range">
                  <span class="tr-lo">12</span><span class="tr-sep"> · </span
                  ><span class="tr-med">17</span><span class="tr-sep"> · </span
                  ><span class="tr-hi">22</span>
                </td>
                <td class="td-range">
                  <span class="tr-lo">20</span><span class="tr-sep"> · </span
                  ><span class="tr-med">24</span><span class="tr-sep"> · </span
                  ><span class="tr-hi">30</span>
                </td>
                <td><span class="td-btts btts-n">NO</span></td>
              </tr>
              <tr class="conf-row">
                <td colspan="11">
                  <div class="conf-row-inner">
                    <span class="conf-badge conf-high"
                      ><span class="conf-dot cd-high"></span>HIGH
                      confidence</span
                    >
                    <span class="conf-reason"
                      >63.1% win prob · BUR 0W away in L5 · 1 goal away in L5 ·
                      BUR missing 6 players · dead rubber for Burnley</span
                    >
                  </div>
                </td>
              </tr>

              <!-- Everton vs Chelsea -->
              <tr class="data-row">
                <td>
                  <div class="td-fix">Everton vs Chelsea</div>
                  <div class="td-fix-sub">Sat · Hill Dickinson Stadium</div>
                </td>
                <td class="td-ko">17:30</td>
                <td><div class="td-score">1–2</div></td>
                <td><span class="td-winner tw-a">CFC</span></td>
                <td class="td-range">
                  <span class="tr-lo">6</span><span class="tr-sep"> · </span
                  ><span class="tr-med">9</span><span class="tr-sep"> · </span
                  ><span class="tr-hi">14</span>
                </td>
                <td class="td-range">
                  <span class="tr-lo">5</span><span class="tr-sep"> · </span
                  ><span class="tr-med">8</span><span class="tr-sep"> · </span
                  ><span class="tr-hi">12</span>
                </td>
                <td class="td-range">
                  <span class="tr-lo">16</span><span class="tr-sep"> · </span
                  ><span class="tr-med">20</span><span class="tr-sep"> · </span
                  ><span class="tr-hi">26</span>
                </td>
                <td class="td-range">
                  <span class="tr-lo">28</span><span class="tr-sep"> · </span
                  ><span class="tr-med">35</span><span class="tr-sep"> · </span
                  ><span class="tr-hi">42</span>
                </td>
                <td class="td-range">
                  <span class="tr-lo">10</span><span class="tr-sep"> · </span
                  ><span class="tr-med">15</span><span class="tr-sep"> · </span
                  ><span class="tr-hi">20</span>
                </td>
                <td class="td-range">
                  <span class="tr-lo">24</span><span class="tr-sep"> · </span
                  ><span class="tr-med">28</span><span class="tr-sep"> · </span
                  ><span class="tr-hi">36</span>
                </td>
                <td><span class="td-btts btts-m">MAYBE</span></td>
              </tr>
              <tr class="conf-row">
                <td colspan="11">
                  <div class="conf-row-inner">
                    <span class="conf-badge conf-med"
                      ><span class="conf-dot cd-med"></span>MED confidence</span
                    >
                    <span class="conf-reason"
                      >CFC 43.2% · Hill Dickinson atmosphere · CFC missing
                      James, Chalobah, Jørgensen · first ever CFC visit to new
                      ground</span
                    >
                  </div>
                </td>
              </tr>

              <!-- Leeds vs Brentford -->
              <tr class="data-row">
                <td>
                  <div class="td-fix">Leeds vs Brentford</div>
                  <div class="td-fix-sub">Sat · Elland Road</div>
                </td>
                <td class="td-ko">20:00</td>
                <td><div class="td-score">1–1</div></td>
                <td><span class="td-winner tw-d">Draw</span></td>
                <td class="td-range">
                  <span class="tr-lo">7</span><span class="tr-sep"> · </span
                  ><span class="tr-med">10</span><span class="tr-sep"> · </span
                  ><span class="tr-hi">14</span>
                </td>
                <td class="td-range">
                  <span class="tr-lo">5</span><span class="tr-sep"> · </span
                  ><span class="tr-med">7</span><span class="tr-sep"> · </span
                  ><span class="tr-hi">11</span>
                </td>
                <td class="td-range">
                  <span class="tr-lo">18</span><span class="tr-sep"> · </span
                  ><span class="tr-med">22</span><span class="tr-sep"> · </span
                  ><span class="tr-hi">28</span>
                </td>
                <td class="td-range">
                  <span class="tr-lo">30</span><span class="tr-sep"> · </span
                  ><span class="tr-med">38</span><span class="tr-sep"> · </span
                  ><span class="tr-hi">46</span>
                </td>
                <td class="td-range">
                  <span class="tr-lo">12</span><span class="tr-sep"> · </span
                  ><span class="tr-med">17</span><span class="tr-sep"> · </span
                  ><span class="tr-hi">22</span>
                </td>
                <td class="td-range">
                  <span class="tr-lo">24</span><span class="tr-sep"> · </span
                  ><span class="tr-med">28</span><span class="tr-sep"> · </span
                  ><span class="tr-hi">36</span>
                </td>
                <td><span class="td-btts btts-m">MAYBE</span></td>
              </tr>
              <tr class="conf-row">
                <td colspan="11">
                  <div class="conf-row-inner">
                    <span class="conf-badge conf-low"
                      ><span class="conf-dot cd-low"></span>LOW confidence</span
                    >
                    <span class="conf-reason"
                      >LEE drew last 3 home · Gudmundsson SUSP · BRE missing
                      Henry, Hickey, Janelt, Dasilva, Damsgaard doubt · both
                      depleted</span
                    >
                  </div>
                </td>
              </tr>

              <!-- Newcastle vs Sunderland -->
              <tr class="data-row" style="background: rgba(255, 122, 40, 0.04)">
                <td>
                  <div class="td-fix">Newcastle vs Sunderland</div>
                  <div class="td-fix-sub">Sun · St. James' Park 🔥 Derby</div>
                </td>
                <td class="td-ko">12:00</td>
                <td><div class="td-score">1–1</div></td>
                <td><span class="td-winner tw-d">Draw</span></td>
                <td class="td-range">
                  <span class="tr-lo">4</span><span class="tr-sep"> · </span
                  ><span class="tr-med">7</span><span class="tr-sep"> · </span
                  ><span class="tr-hi">10</span>
                </td>
                <td class="td-range">
                  <span class="tr-lo">3</span><span class="tr-sep"> · </span
                  ><span class="tr-med">5</span><span class="tr-sep"> · </span
                  ><span class="tr-hi">9</span>
                </td>
                <td class="td-range">
                  <span class="tr-lo">20</span><span class="tr-sep"> · </span
                  ><span class="tr-med">26</span><span class="tr-sep"> · </span
                  ><span class="tr-hi">34</span>
                </td>
                <td class="td-range">
                  <span class="tr-lo">30</span><span class="tr-sep"> · </span
                  ><span class="tr-med">40</span><span class="tr-sep"> · </span
                  ><span class="tr-hi">50</span>
                </td>
                <td class="td-range">
                  <span class="tr-lo">14</span><span class="tr-sep"> · </span
                  ><span class="tr-med">20</span><span class="tr-sep"> · </span
                  ><span class="tr-hi">26</span>
                </td>
                <td class="td-range">
                  <span class="tr-lo">30</span><span class="tr-sep"> · </span
                  ><span class="tr-med">38</span><span class="tr-sep"> · </span
                  ><span class="tr-hi">48</span>
                </td>
                <td><span class="td-btts btts-n">NO</span></td>
              </tr>
              <tr class="conf-row" style="background: rgba(255, 122, 40, 0.04)">
                <td colspan="11">
                  <div class="conf-row-inner">
                    <span class="conf-badge conf-low"
                      ><span class="conf-dot cd-low"></span>LOW confidence</span
                    >
                    <span class="conf-reason"
                      >NEW missing Guimarães, Schar, Krafth · Tonali doubt · SUN
                      have Xhaka + Reinildo fit · SUN won 7/8 H2H — odds
                      contradict history</span
                    >
                  </div>
                </td>
              </tr>

              <!-- Aston Villa vs West Ham -->
              <tr class="data-row">
                <td>
                  <div class="td-fix">Aston Villa vs West Ham</div>
                  <div class="td-fix-sub">Sun · Villa Park</div>
                </td>
                <td class="td-ko">14:15</td>
                <td><div class="td-score">2–0</div></td>
                <td><span class="td-winner tw-h">AVL</span></td>
                <td class="td-range">
                  <span class="tr-lo">5</span><span class="tr-sep"> · </span
                  ><span class="tr-med">8</span><span class="tr-sep"> · </span
                  ><span class="tr-hi">12</span>
                </td>
                <td class="td-range">
                  <span class="tr-lo">4</span><span class="tr-sep"> · </span
                  ><span class="tr-med">7</span><span class="tr-sep"> · </span
                  ><span class="tr-hi">10</span>
                </td>
                <td class="td-range">
                  <span class="tr-lo">16</span><span class="tr-sep"> · </span
                  ><span class="tr-med">20</span><span class="tr-sep"> · </span
                  ><span class="tr-hi">26</span>
                </td>
                <td class="td-range">
                  <span class="tr-lo">22</span><span class="tr-sep"> · </span
                  ><span class="tr-med">30</span><span class="tr-sep"> · </span
                  ><span class="tr-hi">38</span>
                </td>
                <td class="td-range">
                  <span class="tr-lo">10</span><span class="tr-sep"> · </span
                  ><span class="tr-med">14</span><span class="tr-sep"> · </span
                  ><span class="tr-hi">20</span>
                </td>
                <td class="td-range">
                  <span class="tr-lo">20</span><span class="tr-sep"> · </span
                  ><span class="tr-med">24</span><span class="tr-sep"> · </span
                  ><span class="tr-hi">30</span>
                </td>
                <td><span class="td-btts btts-n">NO</span></td>
              </tr>
              <tr class="conf-row">
                <td colspan="11">
                  <div class="conf-row-inner">
                    <span class="conf-badge conf-high"
                      ><span class="conf-dot cd-high"></span>HIGH
                      confidence</span
                    >
                    <span class="conf-reason"
                      >AVL 49.5% · WHU 1 shot vs City · Summerville OUT · WHU
                      18th freefall · AVL played Thu (UEL) — fatigue caveat but
                      quality gap decisive</span
                    >
                  </div>
                </td>
              </tr>

              <!-- Tottenham vs Nottm Forest -->
              <tr class="data-row">
                <td>
                  <div class="td-fix">Tottenham vs Nottm Forest</div>
                  <div class="td-fix-sub">Sun · Tottenham Hotspur Stadium</div>
                </td>
                <td class="td-ko">14:15</td>
                <td><div class="td-score">2–1</div></td>
                <td><span class="td-winner tw-h">TOT</span></td>
                <td class="td-range">
                  <span class="tr-lo">5</span><span class="tr-sep"> · </span
                  ><span class="tr-med">8</span><span class="tr-sep"> · </span
                  ><span class="tr-hi">11</span>
                </td>
                <td class="td-range">
                  <span class="tr-lo">5</span><span class="tr-sep"> · </span
                  ><span class="tr-med">8</span><span class="tr-sep"> · </span
                  ><span class="tr-hi">12</span>
                </td>
                <td class="td-range">
                  <span class="tr-lo">18</span><span class="tr-sep"> · </span
                  ><span class="tr-med">24</span><span class="tr-sep"> · </span
                  ><span class="tr-hi">30</span>
                </td>
                <td class="td-range">
                  <span class="tr-lo">30</span><span class="tr-sep"> · </span
                  ><span class="tr-med">38</span><span class="tr-sep"> · </span
                  ><span class="tr-hi">48</span>
                </td>
                <td class="td-range">
                  <span class="tr-lo">14</span><span class="tr-sep"> · </span
                  ><span class="tr-med">20</span><span class="tr-sep"> · </span
                  ><span class="tr-hi">26</span>
                </td>
                <td class="td-range">
                  <span class="tr-lo">26</span><span class="tr-sep"> · </span
                  ><span class="tr-med">32</span><span class="tr-sep"> · </span
                  ><span class="tr-hi">40</span>
                </td>
                <td><span class="td-btts btts-m">MAYBE</span></td>
              </tr>
              <tr class="conf-row">
                <td colspan="11">
                  <div class="conf-row-inner">
                    <span class="conf-badge conf-low"
                      ><span class="conf-dot cd-low"></span>LOW confidence</span
                    >
                    <span class="conf-reason"
                      >Van de Ven SUSP · TOT 0W in L5 · NFO lost Thu in Denmark
                      (EUL) · Wood/Boly OUT · genuine 3-way toss-up</span
                    >
                  </div>
                </td>
              </tr>
            </tbody>
          </table>
        </div>

        <!-- WATCHLIST -->
        <div class="watchlist">
          <div class="wl-head">Key Watchlist &amp; Betting Angles</div>
          <div class="wl-items">
            <div class="wl-item">
              <div class="wl-tag" style="color: var(--volt)">⚡ Best bet</div>
              <div class="wl-fix">Brighton vs Liverpool — BTTS YES</div>
              <div class="wl-note">
                H2H BTTS 64% · avg 3.41 goals · Salah OUT but Wirtz, Gakpo,
                Ekitike carry threat · BRI: Minteh, Rutter, Mitoma fit vs
                Mamardashvili in goal
              </div>
            </div>
            <div class="wl-item">
              <div class="wl-tag" style="color: var(--teal)">📐 Stat angle</div>
              <div class="wl-fix">Newcastle vs Sunderland — U2.5 goals</div>
              <div class="wl-note">
                Dec derby: 0.54 xG combined — 2nd lowest PL ever · Derby =
                defensive · both teams score rarely in these fixtures
              </div>
            </div>
            <div class="wl-item">
              <div class="wl-tag" style="color: var(--orange)">🟨 Cards</div>
              <div class="wl-fix">Tottenham vs Forest — 4+ yellows</div>
              <div class="wl-note">
                Relegation six-pointer · 1pt separates 16th &amp; 18th · Van de
                Ven SUSPENDED · Tudor + Pereira both tactically cynical · NFO
                fatigued after EUL travel
              </div>
            </div>
            <div class="wl-item">
              <div class="wl-tag" style="color: var(--sky)">📐 Corners</div>
              <div class="wl-fix">Brighton vs Liverpool — O9.5 corners</div>
              <div class="wl-note">
                Both sides attack wide · H2H avg ~10 corners · LFC possession →
                corners · BRI home avg 6+ corners
              </div>
            </div>
            <div class="wl-item">
              <div class="wl-tag" style="color: var(--purple)">
                🏟️ Stadium update
              </div>
              <div class="wl-fix">Everton now at Hill Dickinson Stadium</div>
              <div class="wl-note">
                Everton moved to new 52,888-capacity ground at Bramley-Moore
                Dock for start of 2025-26 season · No longer at Goodison Park
              </div>
            </div>
            <div class="wl-item">
              <div class="wl-tag" style="color: var(--win)">✓ Confidence</div>
              <div class="wl-fix">Fulham vs Burnley — Fulham Win</div>
              <div class="wl-note">
                FUL 63.1% win prob · Burnley 0W in last 5 away · 1 goal scored
                away in last 5 · dead rubber for Burnley
              </div>
            </div>
            <div class="wl-item">
              <div class="wl-tag" style="color: var(--win)">✓ Confidence</div>
              <div class="wl-fix">Aston Villa vs West Ham — Villa Win</div>
              <div class="wl-note">
                AVL 49.5% win prob · WHU had 1 shot vs City · Summerville OUT ·
                WHU 18th in freefall · AVL fatigue caveat (played Thu vs Lille)
                but quality gap decisive
              </div>
            </div>
            <div class="wl-item">
              <div class="wl-tag" style="color: var(--red)">⚠ Danger</div>
              <div class="wl-fix">Newcastle vs Sunderland — upset risk</div>
              <div class="wl-note">
                NEW missing Guimarães, Schar, Krafth — three first-team regulars
                OUT · Tonali groin doubt · SUN: Xhaka, Reinildo, Brobbey all fit
                · SUN won 7 of last 8 H2H
              </div>
            </div>
            <div class="wl-item">
              <div class="wl-tag" style="color: var(--purple)">
                🎯 Score pred
              </div>
              <div class="wl-fix">Predicted scores at a glance</div>
              <div class="wl-note">
                BRI 1-2 LFC · FUL 2-0 BUR · EVE 1-2 CFC · LEE 1-1 BRE · NEW 1-1
                SUN · AVL 2-0 WHU · TOT 2-1 NFO
              </div>
            </div>
          </div>
        </div>
      </div>
      <!-- end summary section -->
    </div>
    <!-- /wrap -->

    <footer>
      <div class="ft-l">
        MATCH INTEL · PREMIER LEAGUE MD31 · 21–22 MARCH 2026<br />
        <strong>Team Bilbo Statistical Analysis</strong><br />
        Sources: Actual L5 game stats · Last 5 H2H · Season averages · Confirmed
        team news.
      </div>
      <div class="ft-r">MD31 ·⚡</div>
    </footer>

    <script>
      (function () {
        const els = document.querySelectorAll(".reveal");
        const ob = new IntersectionObserver(
          (entries) => {
            entries.forEach((e) => {
              if (e.isIntersecting) {
                e.target.classList.add("in");
                ob.unobserve(e.target);
              }
            });
          },
          { threshold: 0.05, rootMargin: "0px 0px -14px 0px" },
        );
        els.forEach((el) => ob.observe(el));
      })();
    </script>
  </body>
</html>
