<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>Bournemouth vs Manchester United · 20 March 2026</title>
    <link
      href="https://fonts.googleapis.com/css2?family=Syne:wght@400;600;700;800&family=IBM+Plex+Mono:wght@400;500;600&family=IBM+Plex+Sans:wght@300;400;500;600&display=swap"
      rel="stylesheet"
    />
    <style>
      /* ═══════════════════════════════════════
   TOKENS — New Colour Scheme
════════════════════════════════════════ */
      :root {
        --bg: rgba(0, 0, 0, 0.914);
        --s1: rgba(19, 18, 18, 0.914);
        --s2: rgba(11, 10, 10, 0.914);
        --s3: rgba(20, 20, 20, 0.914);
        --border: rgba(84, 88, 99, 0.5);
        --border2: rgba(84, 88, 99, 0.3);
        --fg: rgba(255, 227, 227, 1);
        --fg2: rgba(255, 227, 227, 0.7);
        --fg3: rgba(255, 227, 227, 0.4);
        --bou: rgba(189, 59, 59, 0.908); /* Bournemouth orange */
        --bou-dim: rgba(249, 110, 70, 0.13);
        --bou-glow: rgba(249, 110, 70, 0.4);
        --mun: rgba(249, 200, 70, 1); /* Man Utd yellow */
        --mun2: rgba(249, 200, 70, 1); /* Man Utd gold */
        --mun-dim: rgba(249, 200, 70, 0.12);
        --mun-glow: rgba(249, 200, 70, 0.35);
        --gold: rgba(249, 200, 70, 1);
        --gold-dim: rgba(249, 200, 70, 0.12);
        --gold-glow: rgba(249, 200, 70, 0.35);
        --teal: rgba(0, 232, 252, 1);
        --teal-dim: rgba(0, 232, 252, 0.11);
        --green: rgba(0, 232, 252, 1);
        --green-dim: rgba(0, 232, 252, 0.12);
        --red: rgba(249, 110, 70, 1);
        --red-dim: rgba(249, 110, 70, 0.12);
        --blue: rgba(0, 232, 252, 1);
        --blue-dim: rgba(0, 232, 252, 0.11);
        --r: 10px;
        --r2: 5px;
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
        scroll-behavior: smooth;
        font-size: 18px;
        -webkit-text-size-adjust: 100%;
      }
      body {
        background: var(--bg);
        color: var(--fg);
        font-family: "IBM Plex Sans", sans-serif;
        line-height: 1.6;
        min-height: 100vh;
        overflow-x: hidden;
        background-image:
          radial-gradient(
            ellipse 80% 55% at 0% 0%,
            rgba(249, 110, 70, 0.05) 0%,
            transparent 60%
          ),
          radial-gradient(
            ellipse 70% 50% at 100% 100%,
            rgba(249, 200, 70, 0.04) 0%,
            transparent 55%
          );
      }

      /* ── FILM GRAIN ── */
      body::before {
        content: "";
        position: fixed;
        inset: 0;
        z-index: 0;
        pointer-events: none;
        opacity: 0.02;
        background-image: url("data:image/svg+xml,%3Csvg xmlns='http://www.w3.org/2000/svg' width='300' height='300'%3E%3Cfilter id='n'%3E%3CfeTurbulence type='fractalNoise' baseFrequency='.85' numOctaves='4' stitchTiles='stitch'/%3E%3C/filter%3E%3Crect width='300' height='300' filter='url(%23n)'/%3E%3C/svg%3E");
        background-size: 300px;
      }

      /* ── REVEAL ── */
      .reveal {
        opacity: 0;
        transform: translateY(16px);
        transition:
          opacity 0.55s cubic-bezier(0.22, 1, 0.36, 1),
          transform 0.55s cubic-bezier(0.22, 1, 0.36, 1);
      }
      .reveal.in {
        opacity: 1;
        transform: none;
      }

      /* ── HEADER ── */
      header {
        position: sticky;
        top: 0;
        z-index: 200;
        background: rgba(12, 8, 10, 0.92);
        backdrop-filter: blur(16px);
        -webkit-backdrop-filter: blur(16px);
        border-bottom: 1px solid var(--border);
      }
      .hdr {
        max-width: 1080px;
        margin: 0 auto;
        display: flex;
        align-items: center;
        gap: 12px;
        padding: 0 var(--px);
        height: 48px;
      }
      .hdr-brand {
        font-family: "Syne", sans-serif;
        font-size: 13px;
        font-weight: 800;
        letter-spacing: 0.08em;
        text-transform: uppercase;
        color: var(--fg);
        display: flex;
        align-items: center;
        gap: 10px;
        flex-shrink: 0;
      }
      .hdr-pip {
        width: 8px;
        height: 8px;
        border-radius: 50%;
        background: var(--bou);
        box-shadow: 0 0 8px var(--bou-glow);
        animation: pip 2s ease-in-out infinite;
      }
      @keyframes pip {
        0%,
        100% {
          opacity: 1;
        }
        50% {
          opacity: 0.2;
        }
      }
      .hdr-badge {
        font-family: "IBM Plex Mono", monospace;
        font-size: 9px;
        letter-spacing: 0.12em;
        text-transform: uppercase;
        padding: 2px 8px;
        border-radius: 3px;
        border: 1px solid;
        white-space: nowrap;
      }
      .hb-pl {
        color: var(--mun2);
        border-color: rgba(245, 197, 24, 0.35);
        background: rgba(245, 197, 24, 0.08);
      }
      .hdr-ko {
        font-family: "IBM Plex Mono", monospace;
        font-size: 10px;
        letter-spacing: 0.06em;
        color: var(--fg3);
        margin-left: auto;
        flex-shrink: 0;
      }
      @media (min-width: 480px) {
        .hdr {
          height: 52px;
          padding: 0 20px;
        }
      }
      @media (min-width: 768px) {
        .hdr {
          height: 56px;
          padding: 0 28px;
        }
      }

      /* ── HERO ── */
      .hero {
        padding: 36px var(--px) 40px;
        border-bottom: 1px solid var(--border);
        position: relative;
        overflow: hidden;
      }
      .hero::after {
        content: "VS";
        position: absolute;
        right: -10px;
        top: -20px;
        font-family: "Syne", sans-serif;
        font-weight: 800;
        font-size: clamp(120px, 25vw, 240px);
        color: rgba(225, 41, 45, 0.04);
        line-height: 1;
        pointer-events: none;
        user-select: none;
        letter-spacing: -0.05em;
      }
      .hero-inner {
        max-width: 1080px;
        margin: 0 auto;
        position: relative;
        z-index: 1;
      }
      .kicker {
        font-family: "IBM Plex Mono", monospace;
        font-size: 10px;
        letter-spacing: 0.18em;
        text-transform: uppercase;
        color: var(--bou);
        margin-bottom: 14px;
        display: flex;
        align-items: center;
        gap: 12px;
      }
      .kicker::before {
        content: "";
        width: 22px;
        height: 1px;
        background: var(--bou);
        box-shadow: 0 0 6px var(--bou-glow);
        flex-shrink: 0;
      }
      .versus {
        display: flex;
        align-items: center;
        gap: 16px;
        margin-bottom: 14px;
        flex-wrap: wrap;
      }
      .team-block {
        display: flex;
        flex-direction: column;
        gap: 3px;
      }
      .team-name {
        font-family: "Syne", sans-serif;
        font-size: clamp(36px, 9vw, 90px);
        font-weight: 800;
        letter-spacing: -0.02em;
        line-height: 0.9;
      }
      .team-name.bou {
        color: var(--bou);
      }
      .team-name.mun {
        color: var(--mun2);
      }
      .team-pos {
        font-family: "IBM Plex Mono", monospace;
        font-size: 10px;
        letter-spacing: 0.08em;
        text-transform: uppercase;
        color: var(--fg3);
      }
      .vs-sep {
        font-family: "Syne", sans-serif;
        font-size: clamp(24px, 5vw, 48px);
        font-weight: 800;
        color: rgba(255, 255, 255, 0.08);
        letter-spacing: -0.03em;
        flex-shrink: 0;
        margin: 0 4px;
        align-self: center;
      }
      .hero-sub {
        font-family: "IBM Plex Mono", monospace;
        font-size: 10px;
        letter-spacing: 0.12em;
        text-transform: uppercase;
        color: var(--fg3);
        margin-bottom: 24px;
      }

      /* meta pills */
      .pill-row {
        display: flex;
        gap: 6px;
        flex-wrap: wrap;
        margin-bottom: 20px;
      }
      .pill {
        font-family: "IBM Plex Mono", monospace;
        font-size: 9px;
        letter-spacing: 0.08em;
        text-transform: uppercase;
        font-weight: 500;
        padding: 4px 9px;
        border-radius: var(--r2);
        border: 1px solid;
      }
      .p-r {
        color: var(--bou);
        border-color: rgba(225, 41, 45, 0.4);
        background: var(--bou-dim);
      }
      .p-g {
        color: var(--gold);
        border-color: rgba(245, 197, 24, 0.4);
        background: var(--gold-dim);
      }
      .p-t {
        color: var(--teal);
        border-color: rgba(45, 212, 191, 0.4);
        background: var(--teal-dim);
      }
      .p-gr {
        color: var(--green);
        border-color: rgba(74, 222, 128, 0.4);
        background: var(--green-dim);
      }
      .p-b {
        color: var(--blue);
        border-color: rgba(96, 165, 250, 0.4);
        background: var(--blue-dim);
      }
      .p-rd {
        color: var(--red);
        border-color: rgba(248, 113, 113, 0.4);
        background: var(--red-dim);
      }
      .ft-r {
        font-family: "Syne", sans-serif;
        font-size: 20px;
        font-weight: 800;
        letter-spacing: 0.04em;
        color: var(--gold);
      }
      .avg-val {
        font-family: "Syne", sans-serif;
        font-size: 20px;
        font-weight: 700;
        line-height: 1;
      }
      .sr-med {
        font-family: "Syne", sans-serif;
        font-size: 20px;
        font-weight: 700;
        color: var(--gold);
        min-width: 40px;
        text-align: center;
        white-space: nowrap;
        letter-spacing: -0.01em;
      }
      .sb-club {
        font-family: "Syne", sans-serif;
        font-size: clamp(24px, 5.5vw, 38px);
        font-weight: 800;
        letter-spacing: -0.01em;
        color: #fff;
        line-height: 1;
      }
      @media (min-width: 480px) {
        .hero {
          padding: 44px 20px 48px;
        }
      }
      @media (min-width: 768px) {
        .hero {
          padding: 52px 28px 56px;
        }
      }

      /* ── WRAP ── */
      .wrap {
        max-width: 1080px;
        margin: 0 auto;
        padding: 28px var(--px) 80px;
        position: relative;
        z-index: 1;
      }
      @media (min-width: 480px) {
        .wrap {
          padding: 36px 20px 88px;
        }
      }
      @media (min-width: 768px) {
        .wrap {
          padding: 44px 28px 96px;
        }
      }

      /* ── CARDS ── */
      .card {
        background: var(--s1);
        border: 1px solid var(--border);
        border-radius: var(--r);
        overflow: hidden;
        margin-bottom: 14px;
        transition:
          border-color 0.2s,
          box-shadow 0.2s;
      }
      .card:hover {
        border-color: var(--border2);
        box-shadow: 0 4px 28px rgba(0, 0, 0, 0.5);
      }

      /* card head */
      .card-hd {
        padding: 12px var(--px);
        border-bottom: 1px solid var(--border);
        background: rgba(255, 255, 255, 0.02);
        font-family: "IBM Plex Mono", monospace;
        font-size: 10px;
        letter-spacing: 0.14em;
        text-transform: uppercase;
        color: var(--fg3);
        display: flex;
        align-items: center;
        gap: 8px;
      }
      .card-hd::before {
        content: "◆";
        font-size: 8px;
        color: var(--gold);
      }
      .card-hd.bou-c::before {
        color: var(--bou);
      }
      .card-hd.mun-c::before {
        color: var(--mun2);
      }
      .card-bd {
        padding: 14px var(--px);
      }
      @media (min-width: 480px) {
        .card-hd {
          padding: 12px 20px;
        }
        .card-bd {
          padding: 14px 20px;
        }
      }
      @media (min-width: 768px) {
        .card-hd {
          padding: 12px 28px;
        }
        .card-bd {
          padding: 16px 28px;
        }
      }

      /* ── SCOREBOARD ── */
      .sb-top {
        display: grid;
        grid-template-columns: 1fr auto 1fr;
        align-items: center;
        gap: 8px;
        padding: 22px var(--px) 20px;
        position: relative;
        overflow: hidden;
      }
      .sb-top::before {
        content: "";
        position: absolute;
        inset: 0;
        background: linear-gradient(
          150deg,
          rgba(225, 41, 45, 0.08) 0%,
          var(--s1) 45%,
          rgba(245, 197, 24, 0.05) 100%
        );
      }
      .sb-team {
        display: flex;
        flex-direction: column;
        position: relative;
        z-index: 1;
      }
      .sb-team.r {
        align-items: flex-end;
        text-align: right;
      }
      .sb-club {
        font-family: "Syne", sans-serif;
        font-size: clamp(22px, 5vw, 34px);
        font-weight: 800;
        letter-spacing: -0.01em;
        color: #fff;
        line-height: 1;
      }
      .sb-meta {
        font-family: "IBM Plex Mono", monospace;
        font-size: 9px;
        letter-spacing: 0.07em;
        text-transform: uppercase;
        color: rgba(255, 255, 255, 0.28);
        margin-top: 4px;
      }
      .form-strip {
        display: flex;
        gap: 3px;
        margin-top: 7px;
      }
      .form-strip.r {
        justify-content: flex-end;
      }
      .fb {
        width: 18px;
        height: 18px;
        border-radius: 3px;
        display: flex;
        align-items: center;
        justify-content: center;
        font-family: "IBM Plex Mono", monospace;
        font-size: 9px;
        font-weight: 600;
        flex-shrink: 0;
      }
      .fw {
        background: rgba(74, 222, 128, 0.18);
        color: var(--green);
        border: 1px solid rgba(74, 222, 128, 0.35);
      }
      .fd {
        background: rgba(255, 255, 255, 0.07);
        color: rgba(255, 255, 255, 0.3);
        border: 1px solid rgba(255, 255, 255, 0.1);
      }
      .fl {
        background: rgba(248, 113, 113, 0.18);
        color: var(--red);
        border: 1px solid rgba(248, 113, 113, 0.3);
      }

      .sb-mid {
        display: flex;
        flex-direction: column;
        align-items: center;
        gap: 4px;
        flex-shrink: 0;
        position: relative;
        z-index: 1;
      }
      .sb-lbl {
        font-family: "IBM Plex Mono", monospace;
        font-size: 8px;
        letter-spacing: 0.18em;
        text-transform: uppercase;
        color: rgba(255, 255, 255, 0.18);
      }
      .sb-score {
        font-family: "Syne", sans-serif;
        font-size: clamp(36px, 9vw, 60px);
        font-weight: 800;
        letter-spacing: 0.02em;
        line-height: 1;
        color: var(--gold);
        text-shadow: 0 0 28px var(--gold-glow);
        white-space: nowrap;
      }
      .sb-venue {
        font-family: "IBM Plex Mono", monospace;
        font-size: 9px;
        letter-spacing: 0.08em;
        text-transform: uppercase;
        color: rgba(255, 255, 255, 0.2);
        text-align: center;
        max-width: 120px;
        line-height: 1.4;
      }
      @media (min-width: 480px) {
        .sb-top {
          padding: 24px 20px 22px;
          gap: 14px;
        }
      }
      @media (min-width: 768px) {
        .sb-top {
          padding: 28px 28px 24px;
          gap: 20px;
        }
        .sb-club {
          font-size: 32px;
        }
      }

      /* prob bar */
      .prob-strip {
        padding: 12px var(--px) 10px;
        border-top: 1px solid var(--border);
        background: rgba(255, 255, 255, 0.01);
      }
      .prob-labs {
        display: flex;
        justify-content: space-between;
        margin-bottom: 4px;
      }
      .prob-lab {
        font-family: "IBM Plex Mono", monospace;
        font-size: 9px;
        letter-spacing: 0.08em;
        text-transform: uppercase;
        color: var(--fg3);
      }
      .prob-bar {
        display: flex;
        height: 4px;
        border-radius: 2px;
        overflow: hidden;
        gap: 1px;
        margin-bottom: 5px;
      }
      .pb-h {
        background: var(--bou);
      }
      .pb-d {
        background: #2e1c24;
      }
      .pb-a {
        background: var(--mun2);
      }
      .prob-pcts {
        display: flex;
        justify-content: space-between;
      }
      .pct {
        font-family: "Syne", sans-serif;
        font-size: 20px;
        font-weight: 700;
        letter-spacing: 0.02em;
        line-height: 1;
      }
      .pc-h {
        color: var(--bou);
      }
      .pc-d {
        color: var(--fg3);
      }
      .pc-a {
        color: var(--mun2);
      }
      @media (min-width: 480px) {
        .prob-strip {
          padding: 12px 20px 10px;
        }
        .pct {
          font-size: 22px;
        }
      }
      @media (min-width: 768px) {
        .prob-strip {
          padding: 13px 28px 11px;
        }
        .pct {
          font-size: 24px;
        }
      }

      /* ── 2-COL GRID ── */
      .two-col {
        display: grid;
        grid-template-columns: 1fr;
        gap: 14px;
        margin-bottom: 14px;
      }
      @media (min-width: 620px) {
        .two-col {
          grid-template-columns: 1fr 1fr;
        }
      }

      /* ── LAST 5 TABLE ── */
      .l5-row {
        display: flex;
        align-items: center;
        gap: 8px;
        padding: 6px 0;
        border-bottom: 1px solid rgba(255, 255, 255, 0.03);
      }
      .l5-row:last-child {
        border-bottom: none;
      }
      .l5-date {
        font-family: "IBM Plex Mono", monospace;
        font-size: 10px;
        color: var(--fg3);
        flex-shrink: 0;
        width: 36px;
      }
      .l5-match {
        font-family: "IBM Plex Sans", sans-serif;
        font-size: 12px;
        color: var(--fg2);
        flex: 1;
        min-width: 0;
        white-space: nowrap;
        overflow: hidden;
        text-overflow: ellipsis;
      }
      .l5-score {
        font-family: "Syne", sans-serif;
        font-size: 14px;
        font-weight: 700;
        letter-spacing: 0.04em;
        color: var(--fg);
        white-space: nowrap;
      }
      .l5-res {
        font-family: "IBM Plex Mono", monospace;
        font-size: 10px;
        font-weight: 700;
        padding: 2px 6px;
        border-radius: 3px;
        border: 1px solid;
        flex-shrink: 0;
      }
      .lw {
        color: var(--green);
        border-color: rgba(74, 222, 128, 0.35);
        background: var(--green-dim);
      }
      .ld {
        color: var(--fg3);
        border-color: rgba(255, 255, 255, 0.12);
        background: rgba(255, 255, 255, 0.03);
      }
      .ll {
        color: var(--red);
        border-color: rgba(248, 113, 113, 0.35);
        background: var(--red-dim);
      }

      /* ── STAT ROWS (match data) ── */
      .mr {
        display: flex;
        align-items: center;
        gap: 8px;
        padding: 5px 0;
        border-bottom: 1px solid rgba(255, 255, 255, 0.03);
      }
      .mr:last-child {
        border-bottom: none;
      }
      .mr-lbl {
        font-family: "IBM Plex Sans", sans-serif;
        font-size: 12px;
        color: var(--fg2);
        flex: 1;
      }
      .mr-bar {
        width: 40px;
        height: 3px;
        background: rgba(255, 255, 255, 0.05);
        border-radius: 2px;
        overflow: hidden;
        flex-shrink: 0;
      }
      .mrb {
        height: 100%;
        border-radius: 2px;
      }
      .mrb-r {
        background: var(--bou);
      }
      .mrb-g {
        background: var(--mun2);
      }
      .mrb-t {
        background: var(--teal);
      }
      .mrb-b {
        background: var(--blue);
      }
      .mr-val {
        font-family: "IBM Plex Mono", monospace;
        font-size: 11px;
        font-weight: 600;
        color: var(--fg);
        min-width: 36px;
        text-align: right;
      }
      .mr-val.hi {
        color: var(--gold);
      }
      @media (min-width: 768px) {
        .mr-lbl {
          font-size: 13px;
        }
      }

      /* ── H2H ROW ── */
      .h2h-row {
        display: flex;
        align-items: center;
        gap: 8px;
        padding: 7px 0;
        border-bottom: 1px solid rgba(255, 255, 255, 0.03);
      }
      .h2h-row:last-child {
        border-bottom: none;
      }
      .h2h-date {
        font-family: "IBM Plex Mono", monospace;
        font-size: 10px;
        color: var(--fg3);
        flex-shrink: 0;
        width: 44px;
      }
      .h2h-ht {
        font-family: "IBM Plex Sans", sans-serif;
        font-size: 12px;
        font-weight: 500;
        color: var(--fg2);
        text-align: right;
        flex: 1;
        min-width: 0;
      }
      .h2h-sc {
        font-family: "Syne", sans-serif;
        font-size: 16px;
        font-weight: 700;
        letter-spacing: 0.04em;
        color: var(--gold);
        white-space: nowrap;
        padding: 0 8px;
        flex-shrink: 0;
      }
      .h2h-at {
        font-family: "IBM Plex Sans", sans-serif;
        font-size: 12px;
        font-weight: 500;
        color: var(--fg2);
        flex: 1;
        min-width: 0;
      }
      .h2h-tag {
        font-family: "IBM Plex Mono", monospace;
        font-size: 9px;
        font-weight: 600;
        padding: 2px 6px;
        border-radius: 3px;
        border: 1px solid;
        flex-shrink: 0;
        white-space: nowrap;
      }
      .hb {
        color: var(--bou);
        border-color: rgba(225, 41, 45, 0.35);
        background: var(--bou-dim);
      }
      .hm {
        color: var(--mun2);
        border-color: rgba(245, 197, 24, 0.35);
        background: var(--gold-dim);
      }
      .hd {
        color: var(--fg3);
        border-color: rgba(255, 255, 255, 0.12);
        background: rgba(255, 255, 255, 0.03);
      }
      @media (max-width: 619px) {
        .h2h-row {
          flex-wrap: wrap;
          gap: 6px;
        }
        .h2h-date {
          width: auto;
          flex-basis: 100%;
          opacity: 0.5;
        }
        .h2h-ht,
        .h2h-at {
          min-width: 0;
          flex: 1;
          font-size: 12px;
        }
        .h2h-ht {
          text-align: left;
        }
        .h2h-sc {
          padding: 0 4px;
        }
      }
      @media (min-width: 768px) {
        .h2h-ht,
        .h2h-at {
          font-size: 13px;
        }
        .h2h-sc {
          font-size: 18px;
        }
      }

      /* ── NOTE / CONTEXT ── */
      .note {
        font-family: "IBM Plex Sans", sans-serif;
        font-size: 12px;
        color: var(--fg2);
        line-height: 1.75;
      }
      .note strong {
        color: var(--fg);
        font-weight: 600;
      }
      .note .hg {
        color: var(--gold);
        font-weight: 600;
      }
      .note .hr {
        color: var(--bou);
        font-weight: 600;
      }
      .note .hm {
        color: var(--mun2);
        font-weight: 600;
      }
      .note .ht {
        color: var(--teal);
        font-weight: 600;
      }
      @media (min-width: 768px) {
        .note {
          font-size: 13px;
        }
      }

      /* ── TEAM NEWS ── */
      .tn-grid {
        display: grid;
        grid-template-columns: 1fr 1fr;
        gap: 14px;
      }
      .tn-side {
        font-family: "IBM Plex Mono", monospace;
        font-size: 9px;
        letter-spacing: 0.12em;
        text-transform: uppercase;
        margin-bottom: 7px;
      }
      .tn-bou {
        color: var(--bou);
      }
      .tn-mun {
        color: var(--mun2);
      }
      .tn-xi {
        font-family: "IBM Plex Sans", sans-serif;
        font-size: 12px;
        line-height: 1.8;
        color: var(--fg2);
      }
      .tn-xi strong {
        color: var(--fg);
        font-weight: 600;
      }
      .tn-out-wrap {
        margin-top: 8px;
        padding-top: 8px;
        border-top: 1px solid var(--border);
      }
      .tn-out-lbl {
        font-family: "IBM Plex Mono", monospace;
        font-size: 9px;
        letter-spacing: 0.08em;
        text-transform: uppercase;
        color: var(--red);
        margin-bottom: 3px;
      }
      .tn-out-names {
        font-family: "IBM Plex Sans", sans-serif;
        font-size: 11px;
        line-height: 1.7;
        color: var(--fg3);
      }
      .tn-alert {
        grid-column: 1/-1;
        background: rgba(245, 197, 24, 0.04);
        border: 1px solid rgba(245, 197, 24, 0.15);
        border-radius: var(--r2);
        padding: 8px 12px;
        font-family: "IBM Plex Sans", sans-serif;
        font-size: 11px;
        color: var(--fg2);
        line-height: 1.65;
      }
      .ta-g {
        color: var(--gold);
        font-weight: 600;
      }
      .ta-r {
        color: var(--bou);
        font-weight: 600;
      }
      .ta-m {
        color: var(--mun2);
        font-weight: 600;
      }
      .ta-t {
        color: var(--teal);
        font-weight: 600;
      }
      @media (max-width: 479px) {
        .tn-grid {
          grid-template-columns: 1fr;
          gap: 20px;
        }
      }
      @media (min-width: 768px) {
        .tn-xi {
          font-size: 13px;
        }
        .tn-out-names {
          font-size: 12px;
        }
        .tn-alert {
          font-size: 12px;
        }
      }

      /* ── STAT PREDICTION PANEL ── */
      .sp {
        background: var(--s1);
        border: 1px solid var(--border);
        border-radius: var(--r);
        overflow: hidden;
        margin-bottom: 14px;
      }
      .sp-hd {
        padding: 13px var(--px);
        border-bottom: 1px solid var(--border);
        background: linear-gradient(
          90deg,
          rgba(245, 197, 24, 0.06) 0%,
          transparent 100%
        );
        display: flex;
        align-items: center;
        justify-content: space-between;
        flex-wrap: wrap;
        gap: 8px;
      }
      .sp-title {
        font-family: "IBM Plex Mono", monospace;
        font-size: 10px;
        letter-spacing: 0.14em;
        text-transform: uppercase;
        color: var(--gold);
        display: flex;
        align-items: center;
        gap: 8px;
      }
      .sp-title::before {
        content: "◆";
        font-size: 8px;
      }
      .sp-sub {
        font-family: "IBM Plex Mono", monospace;
        font-size: 10px;
        color: var(--fg3);
        letter-spacing: 0.06em;
      }
      .sp-leg {
        display: flex;
        gap: 14px;
        flex-wrap: wrap;
      }
      .sl {
        display: flex;
        align-items: center;
        gap: 5px;
        font-family: "IBM Plex Mono", monospace;
        font-size: 9px;
        letter-spacing: 0.08em;
        text-transform: uppercase;
        color: var(--fg3);
      }
      .sl-dot {
        width: 12px;
        height: 3px;
        border-radius: 2px;
        flex-shrink: 0;
      }

      /* stat rows */
      .sr {
        display: grid;
        grid-template-columns: 140px 1fr auto auto auto auto;
        align-items: center;
        gap: 8px;
        padding: 11px var(--px);
        border-bottom: 1px solid rgba(255, 255, 255, 0.03);
        transition: background 0.15s;
      }
      .sr:last-child {
        border-bottom: none;
      }
      .sr:hover {
        background: rgba(255, 255, 255, 0.02);
      }
      .sr-name {
        font-family: "IBM Plex Sans", sans-serif;
        font-size: 12px;
        font-weight: 500;
        color: var(--fg2);
        white-space: normal;
        min-width: 0;
      }
      .sr-bars {
        display: flex;
        flex-direction: column;
        gap: 3px;
        flex: 1;
        min-width: 0;
      }
      .sr-track {
        height: 5px;
        background: rgba(255, 255, 255, 0.05);
        border-radius: 3px;
        overflow: hidden;
        position: relative;
      }
      .sr-lo-fill {
        position: absolute;
        left: 0;
        top: 0;
        height: 100%;
        border-radius: 3px;
        background: var(--teal);
        opacity: 0.7;
      }
      .sr-hi-fill {
        position: absolute;
        left: 0;
        top: 0;
        height: 100%;
        border-radius: 3px;
        background: var(--bou);
        opacity: 0.38;
      }
      .sr-med-fill {
        position: absolute;
        top: 0;
        height: 100%;
        border-radius: 3px;
        background: var(--gold);
        opacity: 0.55;
      }
      .sr-sub {
        font-family: "IBM Plex Mono", monospace;
        font-size: 9px;
        color: var(--fg3);
        white-space: nowrap;
        overflow: hidden;
        text-overflow: ellipsis;
      }

      .sr-lo {
        font-family: "IBM Plex Mono", monospace;
        font-size: 12px;
        font-weight: 600;
        color: var(--teal);
        min-width: 32px;
        text-align: right;
        white-space: nowrap;
      }
      .sr-med {
        font-family: "Syne", sans-serif;
        font-size: 18px;
        font-weight: 700;
        color: var(--gold);
        min-width: 40px;
        text-align: center;
        white-space: nowrap;
        letter-spacing: -0.01em;
      }
      .sr-hi {
        font-family: "IBM Plex Mono", monospace;
        font-size: 12px;
        font-weight: 600;
        color: var(--bou);
        min-width: 32px;
        text-align: left;
        white-space: nowrap;
      }

      .sr-conf {
        font-family: "IBM Plex Mono", monospace;
        font-size: 9px;
        font-weight: 600;
        padding: 2px 6px;
        border-radius: 3px;
        border: 1px solid;
        white-space: nowrap;
        flex-shrink: 0;
      }
      .sc-hi {
        color: var(--green);
        border-color: rgba(74, 222, 128, 0.35);
        background: var(--green-dim);
      }
      .sc-md {
        color: var(--gold);
        border-color: rgba(245, 197, 24, 0.35);
        background: var(--gold-dim);
      }
      .sc-lo {
        color: var(--fg3);
        border-color: rgba(255, 255, 255, 0.12);
        background: rgba(255, 255, 255, 0.03);
      }

      .sr-head-row {
        display: grid;
        grid-template-columns: 140px 1fr auto auto auto auto;
        gap: 8px;
        padding: 7px var(--px);
        border-bottom: 2px solid var(--border);
        background: rgba(255, 255, 255, 0.015);
      }
      .sr-h {
        font-family: "IBM Plex Mono", monospace;
        font-size: 9px;
        letter-spacing: 0.12em;
        text-transform: uppercase;
        color: var(--fg3);
      }
      .sr-h.c-t {
        color: var(--teal);
      }
      .sr-h.c-g {
        color: var(--gold);
      }
      .sr-h.c-r {
        color: var(--bou);
      }

      /* ── MOBILE STAT GRID ── */
      @media (max-width: 619px) {
        .sr-head-row {
          display: none;
        }
        .sr {
          display: flex;
          flex-direction: column;
          gap: 6px;
          padding: 12px var(--px);
        }
        .sr-name {
          font-size: 13px;
          font-weight: 600;
          color: var(--fg);
          white-space: normal;
        }
        .sr-name .delta {
          display: inline-flex;
          margin-left: 0;
          margin-top: 4px;
        }
        .sr-bars {
          width: 100%;
        }
        .sr .sr-lo,
        .sr .sr-med,
        .sr .sr-hi,
        .sr .sr-conf {
          display: inline-flex;
        }
        .sr::after {
          content: "";
          display: flex;
          order: 10;
        }
        /* Wrap low/med/high/conf into a row */
        .sr {
          flex-wrap: wrap;
        }
        .sr-lo,
        .sr-hi {
          font-size: 12px;
        }
        .sr-med {
          font-size: 20px;
        }
        .sr-conf {
          margin-left: auto;
        }
      }
      @media (min-width: 480px) {
        .sp-hd {
          padding: 13px 20px;
        }
      }
      @media (min-width: 620px) {
        .sr {
          padding: 11px 20px;
          gap: 10px;
        }
        .sr-head-row {
          padding: 7px 20px;
          gap: 10px;
        }
      }
      @media (min-width: 768px) {
        .sp-hd {
          padding: 14px 28px;
        }
        .sr {
          padding: 12px 28px;
          grid-template-columns: 160px 1fr auto auto auto auto;
          gap: 14px;
        }
        .sr-head-row {
          padding: 8px 28px;
          grid-template-columns: 160px 1fr auto auto auto auto;
          gap: 14px;
        }
        .sr-name {
          font-size: 13px;
        }
        .sr-med {
          font-size: 20px;
        }
      }

      .delta {
        display: inline-flex;
        align-items: center;
        gap: 3px;
        font-family: "IBM Plex Mono", monospace;
        font-size: 9px;
        font-weight: 600;
        padding: 1px 5px;
        border-radius: 3px;
        border: 1px solid;
        white-space: nowrap;
        vertical-align: middle;
        margin-left: 5px;
        margin-top: 2px;
      }
      .d-up {
        color: var(--bou);
        border-color: rgba(225, 41, 45, 0.3);
        background: var(--bou-dim);
      }
      .d-dn {
        color: var(--teal);
        border-color: rgba(45, 212, 191, 0.3);
        background: var(--teal-dim);
      }
      .d-eq {
        color: var(--fg3);
        border-color: rgba(255, 255, 255, 0.12);
        background: rgba(255, 255, 255, 0.02);
      }

      /* ── AVG BADGES ── */
      .avg-row {
        display: flex;
        gap: 6px;
        flex-wrap: wrap;
        margin-top: 12px;
      }
      .avg {
        display: flex;
        flex-direction: column;
        align-items: center;
        background: rgba(255, 255, 255, 0.03);
        border: 1px solid var(--border);
        border-radius: var(--r2);
        padding: 6px 10px;
      }
      .avg-val {
        font-family: "Syne", sans-serif;
        font-size: 18px;
        font-weight: 700;
        line-height: 1;
      }
      .avg-val.r {
        color: var(--bou);
      }
      .avg-val.g {
        color: var(--gold);
      }
      .avg-val.t {
        color: var(--teal);
      }
      .avg-val.gr {
        color: var(--green);
      }
      .avg-val.rd {
        color: var(--red);
      }
      .avg-lbl {
        font-family: "IBM Plex Mono", monospace;
        font-size: 9px;
        letter-spacing: 0.08em;
        text-transform: uppercase;
        color: var(--fg3);
        margin-top: 2px;
        text-align: center;
      }

      /* ── FOOTER ── */
      footer {
        border-top: 1px solid var(--border);
        padding: 18px var(--px);
        max-width: 1080px;
        margin: 0 auto;
        display: flex;
        justify-content: space-between;
        align-items: center;
        flex-wrap: wrap;
        gap: 10px;
        position: relative;
        z-index: 1;
      }
      .ft-l {
        font-family: "IBM Plex Mono", monospace;
        font-size: 10px;
        color: var(--fg3);
        letter-spacing: 0.05em;
        line-height: 2;
      }
      .ft-r {
        font-family: "Syne", sans-serif;
        font-size: 18px;
        font-weight: 800;
        letter-spacing: 0.04em;
        color: var(--gold);
      }
      @media (min-width: 480px) {
        footer {
          padding: 20px 20px;
        }
      }
      @media (min-width: 768px) {
        footer {
          padding: 22px 28px;
        }
      }
    </style>
  </head>
  <body>
    <header>
      <div class="hdr">
        <div class="hdr-brand">
          <div class="hdr-pip"></div>
          MATCH INTEL<span class="hdr-badge hb-pl">MD31</span>
        </div>
        <div class="hdr-ko">FRI 20 MAR 2026 · 20:00 GMT</div>
      </div>
    </header>

    <!-- ── HERO ── -->
    <section class="hero">
      <div class="hero-inner reveal">
        <div class="kicker">
          Premier League · Matchday 31 · Vitality Stadium
        </div>
        <div class="versus">
          <div class="team-block">
            <div class="team-name bou">Bournemouth</div>
            <div class="team-pos">10th · 41 pts · BOU 29.5%</div>
          </div>
          <div class="vs-sep">vs</div>
          <div class="team-block">
            <div class="team-name mun">Man Utd</div>
            <div class="team-pos">3rd · 54 pts · MUN 45.3%</div>
          </div>
        </div>
        <p class="hero-sub">
          Fri 20 Mar 2026 · 20:00 GMT · Last 5 each · Last 5 H2H · Season avgs ·
          High-stakes adjustment
        </p>
        <div class="pill-row">
          <span class="pill p-g">H2H avg 3.39 goals</span>
          <span class="pill p-gr">BTTS 61% H2H</span>
          <span class="pill p-r">BOU unbeaten L5</span>
          <span class="pill p-g">MUN 10pts L5</span>
          <span class="pill p-b">O9.5 corners 63% BOU home</span>
          <span class="pill p-t">UCL race · high stakes</span>
        </div>
      </div>
    </section>

    <div class="wrap">
      <!-- ══ SCOREBOARD ══ -->
      <div class="card reveal">
        <div class="sb-top">
          <div class="sb-team">
            <div class="sb-club">Bournemouth</div>
            <div class="sb-meta">10th · 41pts · Vitality Stadium</div>
            <!-- BOU L5 all comps: D(BUR 0-0), D(BRE 0-0), D(SUN 1-1), D(WHU 0-0), W(EVE 1-2) -->
            <div class="form-strip">
              <div class="fb fd">D</div>
              <div class="fb fd">D</div>
              <div class="fb fd">D</div>
              <div class="fb fd">D</div>
              <div class="fb fw">W</div>
            </div>
          </div>
          <div class="sb-mid">
            <div class="sb-lbl">Predicted</div>
            <div class="sb-score">1 – 2</div>
            <div class="sb-venue">Vitality Stadium<br />Bournemouth</div>
          </div>
          <div class="sb-team r">
            <div class="sb-club">Man Utd</div>
            <div class="sb-meta">3rd · 54pts · UCL race</div>
            <!-- MUN L5: W(AVL 3-1), L(NEW 2-1), W(CRY 2-1), W(EVE 1-0), D(WHU 1-1) -->
            <div class="form-strip r">
              <div class="fb fw">W</div>
              <div class="fb fl">L</div>
              <div class="fb fw">W</div>
              <div class="fb fw">W</div>
              <div class="fb fd">D</div>
            </div>
          </div>
        </div>
        <div class="prob-strip">
          <div class="prob-labs">
            <span class="prob-lab">Bournemouth</span>
            <span class="prob-lab">Draw</span>
            <span class="prob-lab">Man United</span>
          </div>
          <div class="prob-bar">
            <div class="pb-h" style="flex: 29.5"></div>
            <div class="pb-d" style="flex: 25.2"></div>
            <div class="pb-a" style="flex: 45.3"></div>
          </div>
          <div class="prob-pcts">
            <span class="pct pc-h">29.5%</span>
            <span class="pct pc-d">25.2%</span>
            <span class="pct pc-a">45.3%</span>
          </div>
        </div>
      </div>

      <!-- ══ LAST 5 + SEASON AVGS ══ -->
      <div class="two-col rg">
        <!-- BOURNEMOUTH LAST 5 -->
        <div class="card reveal">
          <div class="card-hd bou-c">Bournemouth — Last 5 PL</div>
          <div class="card-bd">
            <div class="l5-row">
              <span class="l5-date">14 Mar</span
              ><span class="l5-match">BUR 0-0 BOU</span
              ><span class="l5-score">0–0</span><span class="l5-res ld">D</span>
            </div>
            <div class="l5-row">
              <span class="l5-date">3 Mar</span
              ><span class="l5-match">BOU 0-0 BRE</span
              ><span class="l5-score">0–0</span><span class="l5-res ld">D</span>
            </div>
            <div class="l5-row">
              <span class="l5-date">28 Feb</span
              ><span class="l5-match">BOU 1-1 SUN</span
              ><span class="l5-score">1–1</span><span class="l5-res ld">D</span>
            </div>
            <div class="l5-row">
              <span class="l5-date">21 Feb</span
              ><span class="l5-match">WHU 0-0 BOU</span
              ><span class="l5-score">0–0</span><span class="l5-res ld">D</span>
            </div>
            <div class="l5-row">
              <span class="l5-date">10 Feb</span
              ><span class="l5-match">EVE 1-2 BOU</span
              ><span class="l5-score">1–2</span><span class="l5-res lw">W</span>
            </div>
            <div class="avg-row">
              <div class="avg">
                <div class="avg-val r">14.4</div>
                <div class="avg-lbl">Shots/g L5</div>
              </div>
              <div class="avg">
                <div class="avg-val t">3.0</div>
                <div class="avg-lbl">SoT/g L5</div>
              </div>
              <div class="avg">
                <div class="avg-val g">5.3</div>
                <div class="avg-lbl">Corners/g L5</div>
              </div>
              <div class="avg">
                <div class="avg-val r">10.0</div>
                <div class="avg-lbl">Fouls/g L5</div>
              </div>
              <div class="avg">
                <div class="avg-val rd">0.6</div>
                <div class="avg-lbl">GF/g L5</div>
              </div>
            </div>
          </div>
        </div>

        <!-- MAN UTD LAST 5 -->
        <div class="card reveal">
          <div class="card-hd mun-c">Man United — Last 5 PL</div>
          <div class="card-bd">
            <div class="l5-row">
              <span class="l5-date">15 Mar</span
              ><span class="l5-match">MUN 3-1 AVL</span
              ><span class="l5-score">3–1</span><span class="l5-res lw">W</span>
            </div>
            <div class="l5-row">
              <span class="l5-date">4 Mar</span
              ><span class="l5-match">NEW 2-1 MUN</span
              ><span class="l5-score">2–1</span><span class="l5-res ll">L</span>
            </div>
            <div class="l5-row">
              <span class="l5-date">1 Mar</span
              ><span class="l5-match">MUN 2-1 CRY</span
              ><span class="l5-score">2–1</span><span class="l5-res lw">W</span>
            </div>
            <div class="l5-row">
              <span class="l5-date">23 Feb</span
              ><span class="l5-match">EVE 0-1 MUN</span
              ><span class="l5-score">0–1</span><span class="l5-res lw">W</span>
            </div>
            <div class="l5-row">
              <span class="l5-date">10 Feb</span
              ><span class="l5-match">WHU 1-1 MUN</span
              ><span class="l5-score">1–1</span><span class="l5-res ld">D</span>
            </div>
            <div class="avg-row">
              <div class="avg">
                <div class="avg-val g">16.1</div>
                <div class="avg-lbl">Shots/g L5</div>
              </div>
              <div class="avg">
                <div class="avg-val g">7.7</div>
                <div class="avg-lbl">SoT/g L5</div>
              </div>
              <div class="avg">
                <div class="avg-val g">5.7</div>
                <div class="avg-lbl">Corners/g L5</div>
              </div>
              <div class="avg">
                <div class="avg-val r">12.7</div>
                <div class="avg-lbl">Fouls/g L5</div>
              </div>
              <div class="avg">
                <div class="avg-val gr">2.0</div>
                <div class="avg-lbl">GF/g L5</div>
              </div>
            </div>
          </div>
        </div>
      </div>

      <!-- ══ H2H ══ -->
      <div class="card reveal">
        <div class="card-hd">
          Last 5 Head to Head — Bournemouth vs Manchester United
        </div>
        <div class="card-bd">
          <div class="h2h-row">
            <span class="h2h-date">Dec 25</span>
            <span class="h2h-ht">Man United</span>
            <span class="h2h-sc">4–4</span>
            <span class="h2h-at">Bournemouth</span>
            <span class="h2h-tag hd">Draw</span>
          </div>
          <div class="h2h-row">
            <span class="h2h-date">Apr 25</span>
            <span class="h2h-ht">Bournemouth</span>
            <span class="h2h-sc">1–1</span>
            <span class="h2h-at">Man United</span>
            <span class="h2h-tag hd">Draw</span>
          </div>
          <div class="h2h-row">
            <span class="h2h-date">Dec 24</span>
            <span class="h2h-ht">Man United</span>
            <span class="h2h-sc">0–3</span>
            <span class="h2h-at">Bournemouth</span>
            <span class="h2h-tag hb">BOU Win</span>
          </div>
          <div class="h2h-row">
            <span class="h2h-date">Apr 24</span>
            <span class="h2h-ht">Bournemouth</span>
            <span class="h2h-sc">2–2</span>
            <span class="h2h-at">Man United</span>
            <span class="h2h-tag hd">Draw</span>
          </div>
          <div class="h2h-row">
            <span class="h2h-date">Dec 23</span>
            <span class="h2h-ht">Man United</span>
            <span class="h2h-sc">0–3</span>
            <span class="h2h-at">Bournemouth</span>
            <span class="h2h-tag hb">BOU Win</span>
          </div>
          <div class="avg-row" style="margin-top: 14px">
            <div class="avg">
              <div class="avg-val g">3.39</div>
              <div class="avg-lbl">Goals/game H2H</div>
            </div>
            <div class="avg">
              <div class="avg-val gr">61%</div>
              <div class="avg-lbl">BTTS rate</div>
            </div>
            <div class="avg">
              <div class="avg-val r">5/6</div>
              <div class="avg-lbl">O2.5 recent</div>
            </div>
            <div class="avg">
              <div class="avg-val t">2W 2D 1L</div>
              <div class="avg-lbl">BOU L5 H2H</div>
            </div>
          </div>
          <p class="note" style="margin-top: 14px">
            <span class="hg"
              >This is the highest-scoring H2H fixture in this period</span
            >
            — 4-4, 1-1, 0-3, 2-2, 0-3 across the last five. Bournemouth have
            beaten Manchester United 3-0 TWICE at Old Trafford (Dec 2023, Dec
            2024), and the last home meeting for BOU ended 1-1 (April 2025). The
            December 2025 meeting (4-4) was one of the Premier League's all-time
            rollercoaster results.
            <span class="hr"
              >Bournemouth have never beaten Man United at Vitality Stadium in
              the Premier League era</span
            >
            — their home results have been draws.
            <strong
              >High-scoring, open, physical: this fixture demands a high-event
              prediction.</strong
            >
          </p>
        </div>
      </div>

      <!-- ══ TEAM NEWS ══ -->
      <div class="card reveal">
        <div class="card-hd">Team News &amp; Expected XIs</div>
        <div class="card-bd">
          <div class="tn-grid">
            <div>
              <div class="tn-side tn-bou">Bournemouth</div>
              <div class="tn-xi">
                <strong>Petrovic</strong><br />
                Smith · Hill · Senesi · Truffert<br />
                Christie · Scott<br />
                Jimenez · Tavernier · Rayan<br />
                <strong>Evanilson</strong>
              </div>
              <div class="tn-out-wrap">
                <div class="tn-out-lbl">Out</div>
                <div class="tn-out-names">
                  Soler (injury) · Akinmboni (injury) ·
                  <span style="color: var(--bou)"
                    >Kluivert (injury — major absence)</span
                  >
                  · Cook (injury)
                </div>
              </div>
            </div>
            <div>
              <div class="tn-side tn-mun">Manchester United</div>
              <div class="tn-xi">
                <strong>Lammens</strong><br />
                Dalot · Yoro · Maguire · Shaw<br />
                Casemiro · Mainoo<br />
                <strong>Mbeumo</strong> · Fernandes · Cunha<br />
                <strong>Sesko</strong>
              </div>
              <div class="tn-out-wrap">
                <div class="tn-out-lbl">Out</div>
                <div class="tn-out-names">
                  <span style="color: var(--bou)">Mazraoui (injury)</span> ·
                  Martinez (injury) · De Ligt (injury) · Dorgu (injury) · Shaw
                  (doubt — late call)
                </div>
              </div>
            </div>
            <div class="tn-alert">
              <span class="ta-g">KEY INTEL:</span>
              <span class="ta-r">Justin Kluivert is OUT</span> — Bournemouth's
              top scorer (18 goals) missing is massive. Rayan and Jimenez will
              carry the attacking burden.
              <span class="ta-m"
                >Sesko has scored in 5 of United's last 7 games</span
              >
              under Carrick — lethal form.
              <span class="ta-g">Mbeumo leads United with 9 goals</span> and is
              a constant threat from wide right.
              <span class="ta-t"
                >United are fighting for the UCL spot (3rd place, 54pts)</span
              >
              — every point counts, maximum intensity tonight.
              <strong
                >Bournemouth's unbeaten L5 run (W1 D4) comes with a massive
                goalscoring caveat: 0 goals in last 2 games, only 3 goals in 5
                games total.</strong
              >
            </div>
          </div>
        </div>
      </div>

      <!-- ══ SEASON STAT COMPARISON ══ -->
      <div class="two-col rg" style="margin-bottom: 14px">
        <div class="card reveal">
          <div class="card-hd bou-c">BOU Season Averages (2025-26 PL)</div>
          <div class="card-bd">
            <div class="mr">
              <span class="mr-lbl">Total Shots / game</span>
              <div class="mr-bar">
                <div class="mrb mrb-r" style="width: 62%"></div>
              </div>
              <span class="mr-val hi">13.68</span>
            </div>
            <div class="mr">
              <span class="mr-lbl">Shots on Target / game</span>
              <div class="mr-bar">
                <div class="mrb mrb-r" style="width: 52%"></div>
              </div>
              <span class="mr-val hi">4.93</span>
            </div>
            <div class="mr">
              <span class="mr-lbl">Corners / game</span>
              <div class="mr-bar">
                <div class="mrb mrb-r" style="width: 54%"></div>
              </div>
              <span class="mr-val hi">5.7</span>
            </div>
            <div class="mr">
              <span class="mr-lbl">Fouls / game</span>
              <div class="mr-bar">
                <div class="mrb mrb-r" style="width: 48%"></div>
              </div>
              <span class="mr-val">10.3</span>
            </div>
            <div class="mr">
              <span class="mr-lbl">Goals scored / game</span>
              <div class="mr-bar">
                <div class="mrb mrb-r" style="width: 66%"></div>
              </div>
              <span class="mr-val hi">1.47</span>
            </div>
            <div class="mr">
              <span class="mr-lbl">Goals conceded / game</span>
              <div class="mr-bar">
                <div class="mrb mrb-b" style="width: 72%"></div>
              </div>
              <span class="mr-val">1.64</span>
            </div>
            <div class="mr">
              <span class="mr-lbl">BTTS rate (season)</span>
              <div class="mr-bar">
                <div class="mrb mrb-t" style="width: 68%"></div>
              </div>
              <span class="mr-val hi">63%</span>
            </div>
            <div class="mr">
              <span class="mr-lbl">Home corners avg</span>
              <div class="mr-bar">
                <div class="mrb mrb-r" style="width: 44%"></div>
              </div>
              <span class="mr-val">4.4</span>
            </div>
            <div class="mr">
              <span class="mr-lbl">O9.5 corners % (home)</span>
              <div class="mr-bar">
                <div class="mrb mrb-g" style="width: 63%"></div>
              </div>
              <span class="mr-val hi">63%</span>
            </div>
          </div>
        </div>
        <div class="card reveal">
          <div class="card-hd mun-c">MUN Season Averages (2025-26 PL)</div>
          <div class="card-bd">
            <div class="mr">
              <span class="mr-lbl">Total Shots / game</span>
              <div class="mr-bar">
                <div class="mrb mrb-g" style="width: 72%"></div>
              </div>
              <span class="mr-val hi">15.93</span>
            </div>
            <div class="mr">
              <span class="mr-lbl">Shots on Target / game</span>
              <div class="mr-bar">
                <div class="mrb mrb-g" style="width: 60%"></div>
              </div>
              <span class="mr-val hi">5.76</span>
            </div>
            <div class="mr">
              <span class="mr-lbl">Corners / game</span>
              <div class="mr-bar">
                <div class="mrb mrb-g" style="width: 47%"></div>
              </div>
              <span class="mr-val">4.47</span>
            </div>
            <div class="mr">
              <span class="mr-lbl">Fouls / game</span>
              <div class="mr-bar">
                <div class="mrb mrb-g" style="width: 56%"></div>
              </div>
              <span class="mr-val">11.5</span>
            </div>
            <div class="mr">
              <span class="mr-lbl">Goals scored / game</span>
              <div class="mr-bar">
                <div class="mrb mrb-g" style="width: 80%"></div>
              </div>
              <span class="mr-val hi">1.76</span>
            </div>
            <div class="mr">
              <span class="mr-lbl">Goals conceded / game</span>
              <div class="mr-bar">
                <div class="mrb mrb-b" style="width: 58%"></div>
              </div>
              <span class="mr-val">1.38</span>
            </div>
            <div class="mr">
              <span class="mr-lbl">BTTS rate (season)</span>
              <div class="mr-bar">
                <div class="mrb mrb-t" style="width: 62%"></div>
              </div>
              <span class="mr-val hi">61%</span>
            </div>
            <div class="mr">
              <span class="mr-lbl">Away corners avg</span>
              <div class="mr-bar">
                <div class="mrb mrb-g" style="width: 45%"></div>
              </div>
              <span class="mr-val">4.47</span>
            </div>
            <div class="mr">
              <span class="mr-lbl">Over 2.5 goals % season</span>
              <div class="mr-bar">
                <div class="mrb mrb-g" style="width: 59%"></div>
              </div>
              <span class="mr-val hi">59%</span>
            </div>
          </div>
        </div>
      </div>

      <!-- ══ MAIN STAT PREDICTIONS ══ -->
      <div class="sp reveal">
        <div class="sp-hd">
          <div>
            <div class="sp-title">
              Stat Predictions — Bournemouth vs Man United
            </div>
            <div class="sp-sub">
              MD31 · Fri 20 Mar · High-stakes UCL race · Based on L5 actual data
              + H2H + season avgs
            </div>
          </div>
          <div class="sp-leg">
            <div class="sl">
              <div class="sl-dot" style="background: var(--teal)"></div>
              Lowest expected
            </div>
            <div class="sl">
              <div class="sl-dot" style="background: var(--gold)"></div>
              Median
            </div>
            <div class="sl">
              <div class="sl-dot" style="background: var(--bou)"></div>
              Highest expected
            </div>
          </div>
        </div>

        <div class="sr-head-row">
          <span class="sr-h">Stat</span>
          <span class="sr-h">Data basis</span>
          <span class="sr-h c-t">Lowest</span>
          <span class="sr-h c-g">Median</span>
          <span class="sr-h c-r">Highest</span>
          <span class="sr-h">Conf.</span>
        </div>

        <!-- TOTAL SHOTS -->
        <div class="sr">
          <span class="sr-name">Total Shots</span>
          <div class="sr-bars">
            <div class="sr-track">
              <div class="sr-lo-fill" style="width: 54%"></div>
              <div class="sr-med-fill" style="left: 54%; width: 18%"></div>
              <div class="sr-hi-fill" style="width: 78%"></div>
            </div>
            <span class="sr-sub"
              >BOU 13.7/g · MUN 15.9/g · BOU home 14+ last 2 · MUN CRY: 20
              shots</span
            >
          </div>
          <span class="sr-lo">20</span>
          <span class="sr-med">26</span>
          <span class="sr-hi">34</span>
          <span class="sr-conf sc-hi">Hi</span>
        </div>

        <!-- SHOTS ON TARGET -->
        <div class="sr">
          <span class="sr-name"
            >Shots on Target<span class="delta d-up">↑ MUN clinical</span></span
          >
          <div class="sr-bars">
            <div class="sr-track">
              <div class="sr-lo-fill" style="width: 44%"></div>
              <div class="sr-med-fill" style="left: 44%; width: 16%"></div>
              <div class="sr-hi-fill" style="width: 68%"></div>
            </div>
            <span class="sr-sub"
              >BOU 4.9/g · MUN 5.8/g · MUN vs CRY: 12 SoT · Sesko peak
              form</span
            >
          </div>
          <span class="sr-lo">6</span>
          <span class="sr-med">9</span>
          <span class="sr-hi">14</span>
          <span class="sr-conf sc-hi">Hi</span>
        </div>

        <!-- CORNERS -->
        <div class="sr">
          <span class="sr-name"
            >Corners<span class="delta d-up">↑ O9.5 in 63%</span></span
          >
          <div class="sr-bars">
            <div class="sr-track">
              <div class="sr-lo-fill" style="width: 46%"></div>
              <div class="sr-med-fill" style="left: 46%; width: 18%"></div>
              <div class="sr-hi-fill" style="width: 72%"></div>
            </div>
            <span class="sr-sub"
              >BOU home 4.4 + MUN away 4.47 = ~8.9 avg · O9.5 in 63% BOU home
              games · H2H 4-4 had 9 corners</span
            >
          </div>
          <span class="sr-lo">7</span>
          <span class="sr-med">10</span>
          <span class="sr-hi">14</span>
          <span class="sr-conf sc-hi">Hi</span>
        </div>

        <!-- FOULS -->
        <div class="sr">
          <span class="sr-name">Fouls</span>
          <div class="sr-bars">
            <div class="sr-track">
              <div class="sr-lo-fill" style="width: 46%"></div>
              <div class="sr-med-fill" style="left: 46%; width: 14%"></div>
              <div class="sr-hi-fill" style="width: 68%"></div>
            </div>
            <span class="sr-sub"
              >BOU 10.3/g · MUN 11.5/g · BOU vs SUN: 15+12=27 · MUN vs NEW:
              15+14=29 · High-stakes = more</span
            >
          </div>
          <span class="sr-lo">18</span>
          <span class="sr-med">22</span>
          <span class="sr-hi">30</span>
          <span class="sr-conf sc-hi">Hi</span>
        </div>

        <!-- FREE KICKS -->
        <div class="sr">
          <span class="sr-name">Free Kicks</span>
          <div class="sr-bars">
            <div class="sr-track">
              <div class="sr-lo-fill" style="width: 46%"></div>
              <div class="sr-med-fill" style="left: 46%; width: 14%"></div>
              <div class="sr-hi-fill" style="width: 68%"></div>
            </div>
            <span class="sr-sub"
              >Mirrors fouls closely · BOU earn 12-15 FKs/g · MUN earn 11-14
              FKs/g · high-stakes competition</span
            >
          </div>
          <span class="sr-lo">18</span>
          <span class="sr-med">22</span>
          <span class="sr-hi">30</span>
          <span class="sr-conf sc-hi">Hi</span>
        </div>

        <!-- THROW-INS -->
        <div class="sr">
          <span class="sr-name"
            >Throw-ins<span class="delta d-eq">≈ PL avg</span></span
          >
          <div class="sr-bars">
            <div class="sr-track">
              <div class="sr-lo-fill" style="width: 40%"></div>
              <div class="sr-med-fill" style="left: 40%; width: 16%"></div>
              <div class="sr-hi-fill" style="width: 64%"></div>
            </div>
            <span class="sr-sub"
              >BOU vs BRE: 22+18=40 · BOU vs SUN: 18+24=42 · PL avg ~33/g · BOU
              home 19.0 TIs/g L5</span
            >
          </div>
          <span class="sr-lo">28</span>
          <span class="sr-med">36</span>
          <span class="sr-hi">46</span>
          <span class="sr-conf sc-md">Med</span>
        </div>

        <!-- GOAL KICKS -->
        <div class="sr">
          <span class="sr-name"
            >Goal Kicks<span class="delta d-dn">↓ both play out</span></span
          >
          <div class="sr-bars">
            <div class="sr-track">
              <div class="sr-lo-fill" style="width: 36%"></div>
              <div class="sr-med-fill" style="left: 36%; width: 14%"></div>
              <div class="sr-hi-fill" style="width: 58%"></div>
            </div>
            <span class="sr-sub"
              >BOU vs BUR: BOU 8 GKs · BOU vs BRE: BOU 5 GKs · MUN vs AVL: MUN 6
              GKs · both play short</span
            >
          </div>
          <span class="sr-lo">10</span>
          <span class="sr-med">16</span>
          <span class="sr-hi">22</span>
          <span class="sr-conf sc-lo">Low</span>
        </div>

        <!-- TACKLES -->
        <div class="sr">
          <span class="sr-name"
            >Tackles<span class="delta d-up">↑ high-stakes</span></span
          >
          <div class="sr-bars">
            <div class="sr-track">
              <div class="sr-lo-fill" style="width: 44%"></div>
              <div class="sr-med-fill" style="left: 44%; width: 16%"></div>
              <div class="sr-hi-fill" style="width: 68%"></div>
            </div>
            <span class="sr-sub"
              >PL avg ~16-18 tackles/team/game · MUN high-press under Carrick
              ~15-17/g · BOU 12-14/g · UCL stakes = more intensity</span
            >
          </div>
          <span class="sr-lo">24</span>
          <span class="sr-med">30</span>
          <span class="sr-hi">38</span>
          <span class="sr-conf sc-md">Med</span>
        </div>
      </div>

      <!-- ══ CONTEXT + PREDICTION ══ -->
      <div class="card reveal">
        <div class="card-hd">Full Analysis &amp; Prediction Context</div>
        <div class="card-bd">
          <p class="note">
            <strong>The goals question.</strong> This is the highest-averaging
            H2H fixture in the dataset —
            <span class="hg"
              >3.39 goals per game across 18 meetings, BTTS 61% of the time, and
              5 of the last 6 have gone Over 2.5</span
            >. Yet Bournemouth have scored just 3 goals in their last 5 games
            and are on a 4-game draw streak. Without
            <span class="hr">Kluivert (18 goals this season)</span>, their
            attacking threat is significantly reduced — Evanilson, Rayan, and
            Jimenez must step up.
            <span class="hm"
              >Man United, meanwhile, have Sesko in irresistible form (5 goals
              in 7 games)</span
            >
            and Mbeumo and Fernandes providing consistent creativity. Michael
            Carrick has turned United into the best side in the league since
            January in terms of points (13 from 7 PL games).<br /><br />
            <strong>High-stakes adjustment.</strong> With
            <span class="ht">United fighting for the UCL spot in 3rd place</span
            >, this is not a game they can afford to drop points in. They will
            be set up to win — Casemiro-Mainoo provide defensive cover for the
            back four while Fernandes, Mbeumo, and Cunha attack with freedom.
            The last time this fixture was played at Vitality (April 2025), it
            ended 1-1. Before that, BOU 2-2 MUN (April 2024).
            <span class="hg"
              >Bournemouth's Vitality H2H record vs United is D-D-D in the last
              three home meetings</span
            >
            — but United's current form is superior to any of those previous
            away visits.<br /><br />
            <strong>Stat breakdown rationale.</strong> Corners are expected to
            be high —
            <span class="hg"
              >63% of Bournemouth home games go Over 9.5 corners</span
            >. The combined average is 5.7+4.47=10.2/g, and both sides attack
            wide, generating blocked crosses that lead to corners. Fouls will be
            elevated due to the stakes and pace of the game — the Newcastle
            match (MUN away) produced 29 total fouls, and Bournemouth-Sunderland
            had 27. Tackles will be higher than a normal game — both managers
            set up to press and win the ball, and the UCL pressure elevates
            every 50-50 challenge.
            <strong
              >Predicted: Bournemouth 1-2 Manchester United. BTTS YES. Over 2.5
              goals YES. Over 9.5 corners YES.</strong
            >
          </p>
          <div class="pill-row" style="margin-top: 16px; margin-bottom: 0">
            <span class="pill p-g">MUN WIN — prediction</span>
            <span class="pill p-gr">BTTS YES</span>
            <span class="pill p-t">O2.5 goals</span>
            <span class="pill p-b">O9.5 corners</span>
            <span class="pill p-r">Kluivert out = BOU weaker</span>
            <span class="pill p-g">Sesko anytime scorer</span>
          </div>
        </div>
      </div>

      <!-- ══ SUMMARY QUICK REF ══ -->
      <div class="card reveal" style="margin-bottom: 0">
        <div class="card-hd">Quick Reference Summary</div>
        <div class="card-bd">
          <div class="mr">
            <span class="mr-lbl">Predicted Score</span>
            <div class="mr-bar">
              <div class="mrb mrb-g" style="width: 70%"></div>
            </div>
            <span class="mr-val hi">BOU 1–2 MUN</span>
          </div>
          <div class="mr">
            <span class="mr-lbl">Total Shots (low / median / high)</span>
            <div class="mr-bar">
              <div class="mrb mrb-t" style="width: 65%"></div>
            </div>
            <span class="mr-val">20 / 26 / 34</span>
          </div>
          <div class="mr">
            <span class="mr-lbl">Shots on Target (low / median / high)</span>
            <div class="mr-bar">
              <div class="mrb mrb-t" style="width: 54%"></div>
            </div>
            <span class="mr-val">6 / 9 / 14</span>
          </div>
          <div class="mr">
            <span class="mr-lbl">Corners (low / median / high)</span>
            <div class="mr-bar">
              <div class="mrb mrb-t" style="width: 60%"></div>
            </div>
            <span class="mr-val">7 / 10 / 14</span>
          </div>
          <div class="mr">
            <span class="mr-lbl">Fouls (low / median / high)</span>
            <div class="mr-bar">
              <div class="mrb mrb-t" style="width: 55%"></div>
            </div>
            <span class="mr-val">18 / 22 / 30</span>
          </div>
          <div class="mr">
            <span class="mr-lbl">Free Kicks (low / median / high)</span>
            <div class="mr-bar">
              <div class="mrb mrb-t" style="width: 55%"></div>
            </div>
            <span class="mr-val">18 / 22 / 30</span>
          </div>
          <div class="mr">
            <span class="mr-lbl">Throw-ins (low / median / high)</span>
            <div class="mr-bar">
              <div class="mrb mrb-t" style="width: 50%"></div>
            </div>
            <span class="mr-val">28 / 36 / 46</span>
          </div>
          <div class="mr">
            <span class="mr-lbl">Goal Kicks (low / median / high)</span>
            <div class="mr-bar">
              <div class="mrb mrb-t" style="width: 38%"></div>
            </div>
            <span class="mr-val">10 / 16 / 22</span>
          </div>
          <div class="mr">
            <span class="mr-lbl">Tackles (low / median / high)</span>
            <div class="mr-bar">
              <div class="mrb mrb-t" style="width: 52%"></div>
            </div>
            <span class="mr-val">24 / 30 / 38</span>
          </div>
          <div class="mr">
            <span class="mr-lbl">BTTS</span>
            <div class="mr-bar">
              <div class="mrb mrb-g" style="width: 68%"></div>
            </div>
            <span class="mr-val hi">YES — 68%</span>
          </div>
          <div class="mr">
            <span class="mr-lbl">Over 2.5 Goals</span>
            <div class="mr-bar">
              <div class="mrb mrb-g" style="width: 65%"></div>
            </div>
            <span class="mr-val hi">YES — 65%</span>
          </div>
          <div class="mr">
            <span class="mr-lbl">Yellow Cards</span>
            <div class="mr-bar">
              <div class="mrb mrb-r" style="width: 50%"></div>
            </div>
            <span class="mr-val">3–5 total</span>
          </div>
          <div class="mr">
            <span class="mr-lbl">Win Probability (MUN)</span>
            <div class="mr-bar">
              <div class="mrb mrb-g" style="width: 45%"></div>
            </div>
            <span class="mr-val hi">45.3%</span>
          </div>
        </div>
      </div>
    </div>
    <!-- /wrap -->
    <br />
    <footer>
      <div class="ft-l">
        PREMIER LEAGUE · FRI 20 MARCH 2026<br />
        Team Bilbo Statistical Analysis Sources: Actual L5 game stats · Last 5
        H2H · Season averages · Confirmed team news.
      </div>
      <div class="ft-r">· Bournemouth v Manchester United ·</div>
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
          { threshold: 0.06, rootMargin: "0px 0px -18px 0px" },
        );
        els.forEach((el) => ob.observe(el));
      })();
    </script>
  </body>
</html>
