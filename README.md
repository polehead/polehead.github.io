<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>Crystal Palace vs West Ham · PL Predictor · 20 April 2026</title>
    <link rel="preconnect" href="https://fonts.googleapis.com" />
    <link
      href="https://fonts.googleapis.com/css2?family=Rajdhani:wght@400;500;600;700&family=IBM+Plex+Sans:wght@300;400;500;600;700&display=swap"
      rel="stylesheet" />
    <style>
      /* ══════════════════════════════════════
   DESIGN TOKENS
══════════════════════════════════════ */
      :root {
        /* Palette */
        --bg: #050810;
        --s0: #0a0e1c;
        --s1: #0f1526;
        --s2: #141c30;
        --s3: #1a233a;
        --s4: #202a44;
        --border: rgba(255, 255, 255, 0.07);
        --bm: rgba(255, 255, 255, 0.13);
        --text: #bbc8de;
        --muted: #3e4f6c;
        --label: #7d90b0;
        --bright: #e2eaf7;

        /* Team colours */
        --cp-r: #c4122f;
        --cp-b: #004f9f;
        --cp-l: rgba(196, 18, 47, 0.18);
        --whu-m: #7a263a;
        --whu-b: #1bb1e7;
        --whu-l: rgba(122, 38, 58, 0.18);

        /* Stat bands */
        --lo: #10d9a2;
        --med: #f6c840;
        --hi: #f5522a;

        /* PL */
        --pl-p: #37003c;
        --pl-g: #00ff87;
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
        font-family: 'IBM Plex Sans', sans-serif;
        background: var(--bg);
        color: var(--text);
        font-size: 14px;
        line-height: 1.55;
        -webkit-font-smoothing: antialiased;
        overflow-x: hidden;
      }
      h1,
      h2,
      h3,
      .mono {
        font-family: 'Rajdhani', sans-serif;
      }

      /* ══ ANIMATIONS ══ */
      @keyframes fadeUp {
        from {
          opacity: 0;
          transform: translateY(18px);
        }
        to {
          opacity: 1;
          transform: translateY(0);
        }
      }
      @keyframes popIn {
        from {
          transform: scale(0.6) rotate(-6deg);
          opacity: 0;
        }
        to {
          transform: scale(1) rotate(0);
          opacity: 1;
        }
      }
      @keyframes glow {
        0%,
        100% {
          opacity: 0.4;
        }
        50% {
          opacity: 0.9;
        }
      }
      @keyframes barFill {
        from {
          width: 0 !important;
        }
      }
      @keyframes countUp {
        from {
          opacity: 0;
          transform: scale(0.7);
        }
        to {
          opacity: 1;
          transform: scale(1);
        }
      }
      @keyframes shimmerPulse {
        0%,
        100% {
          opacity: 0.7;
        }
        50% {
          opacity: 1;
        }
      }

      /* ══ PITCH TEXTURE BG ══ */
      .pitch-bg {
        position: fixed;
        inset: 0;
        pointer-events: none;
        z-index: 0;
        background:
          radial-gradient(
            ellipse 80% 50% at 20% 10%,
            rgba(196, 18, 47, 0.06),
            transparent 65%
          ),
          radial-gradient(
            ellipse 60% 45% at 80% 80%,
            rgba(27, 177, 231, 0.05),
            transparent 60%
          ),
          repeating-linear-gradient(
            0deg,
            transparent,
            transparent 60px,
            rgba(255, 255, 255, 0.013) 60px,
            rgba(255, 255, 255, 0.013) 61px
          ),
          repeating-linear-gradient(
            90deg,
            transparent,
            transparent 60px,
            rgba(255, 255, 255, 0.013) 60px,
            rgba(255, 255, 255, 0.013) 61px
          );
      }

      /* ══ MAIN WRAP ══ */
      .wrap {
        position: relative;
        z-index: 1;
        max-width: 1240px;
        margin: 0 auto;
        padding: 0 14px 60px;
      }

      /* ══ PAGE HEADER ══ */
      .page-header {
        background: linear-gradient(
          160deg,
          #07091a 0%,
          #0d0020 50%,
          #07091a 100%
        );
        border-bottom: 2px solid rgba(55, 0, 60, 0.85);
        padding: 22px 20px 18px;
        text-align: center;
        position: relative;
        overflow: hidden;
      }
      .page-header::after {
        content: '';
        position: absolute;
        inset: 0;
        background: radial-gradient(
          ellipse 120% 55% at 50% -15%,
          rgba(0, 255, 135, 0.06),
          transparent 60%
        );
        pointer-events: none;
      }
      .pl-chip {
        display: inline-flex;
        align-items: center;
        gap: 7px;
        font-family: 'Rajdhani', sans-serif;
        font-size: 10px;
        font-weight: 600;
        letter-spacing: 2px;
        text-transform: uppercase;
        color: var(--pl-g);
        background: rgba(0, 255, 135, 0.08);
        border: 1px solid rgba(0, 255, 135, 0.25);
        padding: 4px 13px;
        border-radius: 20px;
        margin-bottom: 10px;
        position: relative;
      }
      .page-header h1 {
        font-size: clamp(20px, 4.5vw, 38px);
        font-weight: 700;
        color: #fff;
        letter-spacing: 1px;
        line-height: 1.05;
        position: relative;
      }
      .page-header h1 span {
        color: var(--pl-g);
      }
      .page-header .sub {
        font-size: 11.5px;
        color: var(--muted);
        margin-top: 6px;
        position: relative;
      }

      /* ══ HERO MATCH ══ */
      .match-hero {
        background: linear-gradient(
          135deg,
          var(--cp-l) 0%,
          var(--s0) 45%,
          var(--whu-l) 100%
        );
        border-radius: 14px;
        overflow: hidden;
        margin-top: 22px;
        box-shadow: 0 8px 50px rgba(0, 0, 0, 0.5);
        animation: fadeUp 0.55s ease both;
      }
      .hero-inner {
        padding: 28px 24px 22px;
        display: flex;
        flex-direction: column;
        align-items: center;
        gap: 14px;
      }
      .match-meta-row {
        display: flex;
        gap: 8px;
        flex-wrap: wrap;
        justify-content: center;
      }
      .meta-chip {
        font-family: 'Rajdhani', sans-serif;
        font-size: 9.5px;
        font-weight: 600;
        letter-spacing: 1.5px;
        text-transform: uppercase;
        padding: 3px 10px;
        border-radius: 4px;
        border: 1px solid;
      }

      /* Motivation bar */
      .motivation-bar {
        width: 100%;
        max-width: 600px;
        background: rgba(255, 255, 255, 0.04);
        border: 1px solid var(--border);
        border-radius: 8px;
        padding: 10px 14px;
        display: flex;
        align-items: center;
        gap: 10px;
      }
      .mot-label {
        font-family: 'Rajdhani', sans-serif;
        font-size: 9px;
        font-weight: 600;
        letter-spacing: 1.5px;
        text-transform: uppercase;
        color: var(--muted);
        white-space: nowrap;
      }
      .mot-track {
        flex: 1;
        height: 6px;
        background: rgba(255, 255, 255, 0.07);
        border-radius: 3px;
        overflow: hidden;
      }
      .mot-fill-cp {
        height: 100%;
        border-radius: 3px;
        background: linear-gradient(90deg, var(--cp-r), var(--cp-b));
        animation: barFill 0.8s ease both 0.4s;
      }
      .mot-fill-whu {
        height: 100%;
        border-radius: 3px;
        background: linear-gradient(90deg, var(--whu-m), var(--whu-b));
        animation: barFill 0.8s ease both 0.5s;
      }
      .mot-pct {
        font-family: 'Rajdhani', sans-serif;
        font-size: 13px;
        font-weight: 700;
        white-space: nowrap;
      }

      /* Teams display */
      .teams-display {
        display: grid;
        grid-template-columns: 1fr auto 1fr;
        align-items: center;
        gap: 16px;
        width: 100%;
        max-width: 580px;
      }
      .t-side {
        display: flex;
        flex-direction: column;
        align-items: center;
        gap: 8px;
      }
      .t-badge {
        width: 78px;
        height: 78px;
        background: rgba(255, 255, 255, 0.04);
        border: 1.5px solid var(--bm);
        border-radius: 50%;
        display: flex;
        align-items: center;
        justify-content: center;
        overflow: hidden;
        transition: transform 0.3s cubic-bezier(0.34, 1.56, 0.64, 1);
        animation: popIn 0.5s cubic-bezier(0.34, 1.56, 0.64, 1) both;
        flex-shrink: 0;
      }
      .t-badge:hover {
        transform: scale(1.1) rotate(4deg);
      }
      .t-badge svg,
      .t-badge img {
        width: 58px;
        height: 58px;
        object-fit: contain;
      }
      .t-name {
        font-size: 14px;
        font-weight: 700;
        text-transform: uppercase;
        text-align: center;
        color: #fff;
        letter-spacing: 0.5px;
      }
      .t-stat {
        font-size: 9.5px;
        color: var(--muted);
        text-align: center;
        line-height: 1.5;
      }
      .ko-block {
        display: flex;
        flex-direction: column;
        align-items: center;
        gap: 5px;
      }
      .vs-txt {
        font-size: 20px;
        font-weight: 700;
        color: rgba(255, 255, 255, 0.09);
        letter-spacing: 2px;
      }
      .ko-time {
        font-family: 'Rajdhani', sans-serif;
        font-size: 10px;
        font-weight: 600;
        letter-spacing: 1.5px;
        color: var(--med);
        background: rgba(246, 200, 64, 0.09);
        border: 1px solid rgba(246, 200, 64, 0.25);
        padding: 2px 8px;
        border-radius: 3px;
      }
      .venue-txt {
        font-size: 8.5px;
        color: var(--muted);
        text-align: center;
        line-height: 1.5;
      }

      /* Odds row */
      .odds-row {
        display: flex;
        gap: 8px;
        flex-wrap: wrap;
        justify-content: center;
        width: 100%;
        max-width: 500px;
      }
      .odds-box {
        flex: 1;
        min-width: 90px;
        max-width: 140px;
        background: var(--s2);
        border: 1px solid var(--border);
        border-radius: 8px;
        padding: 10px 8px;
        text-align: center;
        transition: border-color 0.2s;
      }
      .odds-box:hover {
        border-color: var(--bm);
      }
      .o-label {
        font-size: 9px;
        text-transform: uppercase;
        letter-spacing: 1px;
        color: var(--muted);
      }
      .o-odds {
        font-family: 'Rajdhani', sans-serif;
        font-size: 22px;
        font-weight: 700;
        color: #fff;
        margin: 2px 0;
      }
      .o-implied {
        font-size: 9.5px;
        color: var(--label);
      }
      .ob-cp .o-odds {
        color: #e84060;
      }
      .ob-draw .o-odds {
        color: var(--med);
      }
      .ob-whu .o-odds {
        color: #7ab8e0;
      }
      .ob-value {
        border-color: rgba(246, 200, 64, 0.35) !important;
        background: linear-gradient(
          135deg,
          rgba(246, 200, 64, 0.07),
          var(--s2)
        );
      }
      .ob-value .o-label {
        color: var(--med);
      }

      /* ══ GRID ══ */
      .content-grid {
        display: grid;
        grid-template-columns: 1fr;
        gap: 16px;
        margin-top: 20px;
      }
      @media (min-width: 860px) {
        .content-grid {
          grid-template-columns: 1fr 1fr;
        }
        .span2 {
          grid-column: 1/-1;
        }
      }

      /* ══ CARD ══ */
      .card {
        background: var(--s1);
        border: 1px solid var(--border);
        border-radius: 12px;
        overflow: hidden;
        transition: border-color 0.3s;
        animation: fadeUp 0.5s ease both;
      }
      .card:hover {
        border-color: var(--bm);
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
        flex-shrink: 0;
      }
      .hd-title {
        font-family: 'Rajdhani', sans-serif;
        font-size: 10px;
        font-weight: 600;
        letter-spacing: 2px;
        text-transform: uppercase;
        color: var(--muted);
        flex: 1;
      }
      .hd-tag {
        font-size: 8.5px;
        font-weight: 600;
        letter-spacing: 0.8px;
        text-transform: uppercase;
        padding: 2px 7px;
        border-radius: 3px;
        border: 1px solid;
      }
      .card-body {
        padding: 14px 18px;
      }

      /* ══ CONTEXT BOX ══ */
      .ctx {
        background: rgba(255, 255, 255, 0.025);
        border: 1px solid var(--bm);
        border-radius: 8px;
        padding: 12px 14px;
        font-size: 12.5px;
        line-height: 1.7;
        color: var(--label);
      }
      .ctx strong {
        color: var(--med);
        font-weight: 700;
      }
      .ctx .badge-key {
        display: inline-flex;
        align-items: center;
        gap: 4px;
        font-size: 10px;
        font-weight: 700;
        letter-spacing: 0.7px;
        text-transform: uppercase;
        padding: 1px 7px;
        border-radius: 3px;
        border: 1px solid;
        margin-right: 3px;
      }
      .k-cp {
        color: #e84060;
        border-color: rgba(196, 18, 47, 0.35);
        background: rgba(196, 18, 47, 0.1);
      }
      .k-whu {
        color: #7ab8e0;
        border-color: rgba(122, 38, 58, 0.45);
        background: rgba(122, 38, 58, 0.15);
      }
      .k-alert {
        color: #ff5f45;
        border-color: rgba(255, 95, 69, 0.35);
        background: rgba(255, 95, 69, 0.1);
      }
      .k-good {
        color: var(--pl-g);
        border-color: rgba(0, 255, 135, 0.3);
        background: rgba(0, 255, 135, 0.08);
      }

      /* ══ FORM TABLE ══ */
      .form-cols {
        display: grid;
        grid-template-columns: 1fr 1fr;
        gap: 12px;
      }
      .form-team-lbl {
        display: flex;
        align-items: center;
        gap: 6px;
        font-family: 'Rajdhani', sans-serif;
        font-size: 10px;
        font-weight: 600;
        letter-spacing: 1px;
        text-transform: uppercase;
        margin-bottom: 7px;
      }
      .form-ti {
        width: 16px;
        height: 16px;
        object-fit: contain;
        border-radius: 50%;
        background: rgba(255, 255, 255, 0.05);
        overflow: hidden;
        flex-shrink: 0;
      }
      .fr-list {
        display: flex;
        flex-direction: column;
        gap: 3px;
      }
      .fr {
        display: grid;
        grid-template-columns: 7px 42px 1fr 58px;
        align-items: center;
        gap: 6px;
        background: var(--s2);
        border-radius: 5px;
        padding: 5px 8px;
        border: 1px solid var(--border);
        transition: background 0.2s;
      }
      .fr:hover {
        background: var(--s3);
      }
      .rdot {
        width: 7px;
        height: 7px;
        border-radius: 50%;
      }
      .rdot.W {
        background: var(--lo);
        box-shadow: 0 0 5px rgba(16, 217, 162, 0.4);
      }
      .rdot.D {
        background: var(--med);
      }
      .rdot.L {
        background: var(--hi);
        box-shadow: 0 0 5px rgba(245, 82, 42, 0.4);
      }
      .fscore {
        font-family: 'Rajdhani', sans-serif;
        font-size: 14px;
        font-weight: 700;
        color: #fff;
        text-align: center;
      }
      .fopp {
        font-size: 11.5px;
        color: var(--text);
        overflow: hidden;
        text-overflow: ellipsis;
        white-space: nowrap;
      }
      .fcomp {
        font-size: 9px;
        color: var(--muted);
        text-align: right;
        text-transform: uppercase;
        letter-spacing: 0.3px;
        white-space: nowrap;
      }
      .ftag {
        font-size: 8px;
        padding: 1px 4px;
        border-radius: 2px;
        background: rgba(246, 200, 64, 0.1);
        color: var(--med);
        font-family: 'Rajdhani', sans-serif;
        font-weight: 600;
        border: 1px solid rgba(246, 200, 64, 0.25);
      }
      .form-legend {
        display: flex;
        gap: 10px;
        margin-top: 8px;
      }
      .fl-i {
        display: flex;
        align-items: center;
        gap: 4px;
        font-size: 10px;
        color: var(--muted);
      }
      .fl-d {
        width: 6px;
        height: 6px;
        border-radius: 50%;
      }

      /* ══ H2H ══ */
      .h2h-summary {
        display: grid;
        grid-template-columns: repeat(4, 1fr);
        gap: 4px;
        margin-bottom: 10px;
      }
      .hs {
        background: var(--s2);
        border-radius: 7px;
        padding: 9px 5px;
        text-align: center;
        border: 1px solid var(--border);
      }
      .hn {
        font-family: 'Rajdhani', sans-serif;
        font-size: 25px;
        font-weight: 700;
        line-height: 1;
      }
      .hl {
        font-size: 8.5px;
        color: var(--muted);
        text-transform: uppercase;
        letter-spacing: 0.5px;
        margin-top: 2px;
      }
      .h2h-rows {
        display: flex;
        flex-direction: column;
        gap: 3px;
      }
      .h2h-r {
        display: grid;
        grid-template-columns: 1fr 60px 1fr;
        align-items: center;
        gap: 6px;
        background: var(--s2);
        border-radius: 5px;
        padding: 5px 8px;
        border: 1px solid var(--border);
        transition: background 0.2s;
      }
      .h2h-r:hover {
        background: var(--s3);
      }
      .rh {
        font-size: 11px;
        font-weight: 600;
        color: var(--text);
        text-align: right;
        white-space: nowrap;
        overflow: hidden;
        text-overflow: ellipsis;
      }
      .rs {
        font-family: 'Rajdhani', sans-serif;
        font-size: 14px;
        font-weight: 700;
        color: #fff;
        text-align: center;
        background: rgba(255, 255, 255, 0.06);
        border-radius: 3px;
        padding: 1px 2px;
      }
      .ra {
        font-size: 11px;
        font-weight: 600;
        color: var(--text);
        text-align: left;
        white-space: nowrap;
        overflow: hidden;
        text-overflow: ellipsis;
      }
      .rx {
        font-size: 8.5px;
        color: var(--muted);
        text-align: center;
        grid-column: 1/-1;
        margin-top: -2px;
        letter-spacing: 0.3px;
        text-transform: uppercase;
      }

      /* ══ AVG STATS ══ */
      .avgs-pair {
        display: grid;
        grid-template-columns: 1fr 1fr;
        gap: 10px;
      }
      .avg-team-lbl {
        font-family: 'Rajdhani', sans-serif;
        font-size: 10px;
        font-weight: 600;
        letter-spacing: 1px;
        text-transform: uppercase;
        margin-bottom: 8px;
        padding: 2px 8px;
        border-radius: 3px;
        display: inline-block;
      }
      .avg-cells {
        display: grid;
        grid-template-columns: repeat(3, 1fr);
        gap: 4px;
      }
      .ac {
        background: var(--s2);
        border-radius: 6px;
        padding: 8px 4px;
        text-align: center;
        border: 1px solid var(--border);
        transition:
          background 0.2s,
          transform 0.2s;
      }
      .ac:hover {
        background: var(--s3);
        transform: translateY(-1px);
      }
      .av {
        font-family: 'Rajdhani', sans-serif;
        font-size: 18px;
        font-weight: 700;
        color: #fff;
        line-height: 1;
      }
      .al {
        font-size: 7.5px;
        color: var(--muted);
        margin-top: 2px;
        text-transform: uppercase;
        letter-spacing: 0.4px;
        line-height: 1.3;
      }
      .xg-box {
        background: linear-gradient(
          135deg,
          rgba(16, 217, 162, 0.07),
          rgba(16, 217, 162, 0.02)
        );
        border: 1px solid rgba(16, 217, 162, 0.25);
        border-radius: 7px;
        padding: 10px 12px;
        margin-top: 10px;
        display: flex;
        gap: 8px;
        flex-wrap: wrap;
      }
      .xg-item {
        flex: 1;
        min-width: 80px;
        text-align: center;
      }
      .xg-val {
        font-family: 'Rajdhani', sans-serif;
        font-size: 22px;
        font-weight: 700;
        color: var(--lo);
        line-height: 1;
      }
      .xg-lbl {
        font-size: 8px;
        color: var(--muted);
        text-transform: uppercase;
        letter-spacing: 0.5px;
        margin-top: 2px;
      }

      /* ══ PREDICTION TABLE ══ */
      .pt-intro {
        display: flex;
        gap: 12px;
        flex-wrap: wrap;
        margin-bottom: 10px;
      }
      .pt-key {
        display: flex;
        align-items: center;
        gap: 5px;
        font-size: 10px;
        color: var(--muted);
      }
      .pt-kd {
        width: 8px;
        height: 8px;
        border-radius: 50%;
      }

      .ptw {
        overflow-x: auto;
        -webkit-overflow-scrolling: touch;
      }
      .ptw::-webkit-scrollbar {
        height: 3px;
      }
      .ptw::-webkit-scrollbar-track {
        background: transparent;
      }
      .ptw::-webkit-scrollbar-thumb {
        background: var(--bm);
        border-radius: 2px;
      }

      .pred-t {
        width: 100%;
        border-collapse: collapse;
        min-width: 540px;
      }
      .pred-t thead th {
        font-family: 'Rajdhani', sans-serif;
        font-size: 9px;
        font-weight: 600;
        letter-spacing: 1.5px;
        text-transform: uppercase;
        color: var(--muted);
        padding: 0 6px 10px;
        text-align: left;
        white-space: nowrap;
      }
      .pred-t thead th.tc {
        text-align: center;
      }
      .pred-t tbody td {
        padding: 7px 6px;
        border-bottom: 1px solid rgba(255, 255, 255, 0.04);
        vertical-align: middle;
      }
      .pred-t tbody tr:last-child td {
        border-bottom: none;
      }
      .pred-t tbody tr:hover td {
        background: rgba(255, 255, 255, 0.02);
      }
      .pred-t td.tn {
        color: var(--label);
        font-weight: 600;
        font-size: 12.5px;
        white-space: nowrap;
      }
      .pred-t td.tv {
        text-align: center;
      }

      .stat-team {
        display: flex;
        flex-direction: column;
        align-items: center;
        gap: 1px;
      }
      .st-val {
        font-family: 'Rajdhani', sans-serif;
        font-size: 15px;
        font-weight: 700;
        line-height: 1;
      }
      .st-lbl {
        font-size: 7.5px;
        color: var(--muted);
        text-transform: uppercase;
        letter-spacing: 0.3px;
      }

      .lv {
        font-family: 'Rajdhani', sans-serif;
        font-size: 16px;
        font-weight: 700;
        color: var(--lo);
      }
      .mv {
        font-family: 'Rajdhani', sans-serif;
        font-size: 18px;
        font-weight: 700;
        color: var(--med);
      }
      .hv {
        font-family: 'Rajdhani', sans-serif;
        font-size: 16px;
        font-weight: 700;
        color: var(--hi);
      }

      /* Range bar */
      .rbar-wrap {
        display: flex;
        align-items: center;
        gap: 5px;
        min-width: 90px;
      }
      .rbar-t {
        flex: 1;
        height: 5px;
        background: rgba(255, 255, 255, 0.07);
        border-radius: 3px;
        overflow: hidden;
      }
      .rbar-f {
        height: 100%;
        border-radius: 3px;
        width: 0;
        transition: width 1.2s cubic-bezier(0.25, 0.46, 0.45, 0.94);
      }

      /* ══ SCORE BOX ══ */
      .score-zone {
        border-radius: 10px;
        padding: 16px;
        background: linear-gradient(
          135deg,
          rgba(255, 255, 255, 0.04),
          rgba(255, 255, 255, 0.01)
        );
        border: 1px solid var(--bm);
        display: flex;
        flex-direction: column;
        gap: 12px;
      }
      .sz-head {
        font-family: 'Rajdhani', sans-serif;
        font-size: 9.5px;
        font-weight: 600;
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
        min-width: 100px;
        max-width: 160px;
        background: var(--s2);
        border: 1px solid var(--border);
        border-radius: 8px;
        padding: 12px 8px;
        text-align: center;
        transition:
          border-color 0.3s,
          transform 0.3s;
      }
      .sbox:hover {
        transform: translateY(-2px);
      }
      .sbox.feat {
        border-color: rgba(246, 200, 64, 0.4);
        background: linear-gradient(
          135deg,
          rgba(246, 200, 64, 0.07),
          var(--s2)
        );
      }
      .sb-lbl {
        font-size: 8.5px;
        text-transform: uppercase;
        letter-spacing: 1px;
        color: var(--muted);
      }
      .sb-score {
        font-family: 'Rajdhani', sans-serif;
        font-size: 30px;
        font-weight: 700;
        color: #fff;
        letter-spacing: 2px;
        margin: 3px 0;
      }
      .sb-score.feat-s {
        color: var(--med);
      }
      .sb-prob {
        font-size: 9.5px;
        color: var(--muted);
      }
      .sz-note {
        font-size: 12px;
        color: var(--label);
        line-height: 1.65;
        border-top: 1px solid var(--border);
        padding-top: 10px;
      }
      .sz-note strong {
        color: var(--med);
        font-weight: 700;
      }
      .safe-pick {
        background: linear-gradient(
          135deg,
          rgba(16, 217, 162, 0.07),
          rgba(16, 217, 162, 0.02)
        );
        border: 1px solid rgba(16, 217, 162, 0.25);
        border-radius: 7px;
        padding: 10px 12px;
        margin-top: 8px;
        font-size: 12px;
        color: var(--label);
        line-height: 1.65;
      }
      .safe-pick strong {
        color: var(--lo);
        font-weight: 700;
      }

      /* ══ YELLOW CARDS ══ */
      .yc-list {
        display: flex;
        flex-direction: column;
        gap: 6px;
      }
      .yc {
        display: flex;
        align-items: flex-start;
        gap: 9px;
        background: var(--s2);
        border: 1px solid var(--border);
        border-radius: 7px;
        padding: 9px 11px;
        transition:
          border-color 0.2s,
          transform 0.2s;
      }
      .yc:hover {
        border-color: rgba(255, 232, 74, 0.22);
        transform: translateX(2px);
      }
      .yc-ico {
        font-size: 14px;
        flex-shrink: 0;
        padding-top: 1px;
      }
      .yc-inf {
        flex: 1;
        min-width: 0;
      }
      .yc-n {
        font-size: 12.5px;
        font-weight: 700;
        color: #fff;
      }
      .yc-cl {
        font-family: 'Rajdhani', sans-serif;
        font-size: 9px;
        letter-spacing: 0.7px;
        text-transform: uppercase;
        margin-left: 5px;
      }
      .yc-r {
        font-size: 11px;
        color: var(--muted);
        margin-top: 2px;
        line-height: 1.45;
      }
      .risk {
        font-family: 'Rajdhani', sans-serif;
        font-size: 8.5px;
        font-weight: 700;
        letter-spacing: 1px;
        text-transform: uppercase;
        padding: 2px 8px;
        border-radius: 3px;
        flex-shrink: 0;
        align-self: center;
        border: 1px solid;
      }
      .r-h {
        color: var(--hi);
        border-color: rgba(245, 82, 42, 0.3);
        background: rgba(245, 82, 42, 0.1);
      }
      .r-m {
        color: var(--med);
        border-color: rgba(246, 200, 64, 0.3);
        background: rgba(246, 200, 64, 0.08);
      }

      /* ══ BETTING ANALYSIS ══ */
      .bet-grid {
        display: grid;
        grid-template-columns: 1fr 1fr;
        gap: 8px;
        margin-bottom: 12px;
      }
      .bet-cell {
        background: var(--s2);
        border: 1px solid var(--border);
        border-radius: 7px;
        padding: 10px 12px;
        transition: border-color 0.2s;
      }
      .bet-cell:hover {
        border-color: var(--bm);
      }
      .bet-cell.val {
        border-color: rgba(246, 200, 64, 0.35);
        background: linear-gradient(
          135deg,
          rgba(246, 200, 64, 0.06),
          var(--s2)
        );
      }
      .bc-market {
        font-size: 9px;
        text-transform: uppercase;
        letter-spacing: 1px;
        color: var(--muted);
        margin-bottom: 4px;
      }
      .bc-line {
        font-family: 'Rajdhani', sans-serif;
        font-size: 18px;
        font-weight: 700;
        color: #fff;
        line-height: 1;
      }
      .bc-line.val-txt {
        color: var(--med);
      }
      .bc-reason {
        font-size: 10.5px;
        color: var(--label);
        margin-top: 3px;
        line-height: 1.45;
      }
      .bet-note {
        font-size: 11.5px;
        color: var(--label);
        line-height: 1.65;
      }
      .bet-note strong {
        color: var(--med);
      }

      /* ══ FORM LEGEND ══ */
      .section-note {
        font-size: 10.5px;
        color: var(--muted);
        margin-top: 8px;
        line-height: 1.55;
      }

      /* ══ RESPONSIVE ══ */
      @media (min-width: 640px) {
        body {
          font-size: 15px;
        }
        .hero-inner {
          padding: 32px 32px 24px;
        }
        .card-hd {
          padding: 12px 22px 10px;
        }
        .card-body {
          padding: 16px 22px;
        }
        .t-badge {
          width: 88px;
          height: 88px;
        }
        .t-badge svg,
        .t-badge img {
          width: 66px;
          height: 66px;
        }
        .t-name {
          font-size: 15px;
        }
        .form-cols {
          gap: 16px;
        }
        .avgs-pair {
          gap: 14px;
        }
      }
      @media (min-width: 1100px) {
        .hero-inner {
          padding: 36px 40px 26px;
        }
        .card-hd {
          padding: 13px 24px 11px;
        }
        .card-body {
          padding: 17px 24px;
        }
        .avg-cells {
          grid-template-columns: repeat(3, 1fr);
        }
        .bet-grid {
          grid-template-columns: repeat(4, 1fr);
        }
      }
      @media (max-width: 400px) {
        .form-cols {
          grid-template-columns: 1fr;
        }
        .avgs-pair {
          grid-template-columns: 1fr;
        }
        .h2h-summary {
          grid-template-columns: repeat(2, 1fr);
        }
      }
    </style>
  </head>
  <body>
    <div class="pitch-bg"></div>

    <!-- PAGE HEADER -->
    <header class="page-header">
      <div class="pl-chip">
        <div class="t-name" style="color: #1bb1e7">Crystal Palace</div> <span>vs</span> <div class="t-name" style="color: #e84060">West Ham Utd</div>
      </div>
      <h1>Premier League <span>Team Bilbo Analytics</span></h1>
      <p class="sub">
        Statistical Prediction Report · Selhurst Park, London · 20:00 ·
        Referee: Darren England
      </p>
    </header>

    <div class="wrap">
      <!-- MATCH HERO -->
      <div class="match-hero">
        <div class="hero-inner">
          <!-- Match chips -->
          <div class="match-meta-row">
            <span
              class="meta-chip"
              style="
                color: #e84060;
                border-color: rgba(196, 18, 47, 0.35);
                background: rgba(196, 18, 47, 0.09);
              "
              >Selhurst Park · London</span
            >
            <span
              class="meta-chip"
              style="
                color: #7ab8e0;
                border-color: rgba(122, 38, 58, 0.45);
                background: rgba(122, 38, 58, 0.12);
              "
              >🚨 West Ham — Relegation Battle</span
            >
            <span
              class="meta-chip"
              style="
                color: var(--pl-g);
                border-color: rgba(0, 255, 135, 0.25);
                background: rgba(0, 255, 135, 0.06);
              "
              >🏆 Palace — UECL Semi-Final Glow</span
            >
          </div>

          <!-- Motivation levels -->
          <div class="motivation-bar" style="max-width: 580px; width: 100%">
            <span class="mot-label">🏠 Palace</span>
            <div class="mot-track">
              <div class="mot-fill-cp" style="width: 58%"></div>
            </div>
            <span class="mot-pct" style="color: #e84060">58%</span>
            <span style="font-size: 10px; color: var(--muted); margin: 0 6px"
              >MOTIVATION</span
            >
            <div class="mot-track">
              <div class="mot-fill-whu" style="width: 94%"></div>
            </div>
            <span class="mot-pct" style="color: #7ab8e0">94%</span>
            <span class="mot-label">WHU ⚔️</span>
          </div>

          <!-- Teams -->
          <div class="teams-display">
            <div class="t-side">
              <div class="t-badge" style="animation-delay: 0.05s">
                <img
                  src="https://cdn.brandfetch.io/iddi0P11VR/theme/dark/logo.svg?c=1bxid64Mup7aczewSAYMX&t=1668077972554"
                  alt="Crystal Palace"
                  style="background-color: transparent" />
              </div>
              <div class="t-name" style="color: #1bb1e7">Crystal Palace</div>
              <div class="t-stat">
                13th · ~35 pts · W4 D2 last 7<br />UECL Semi-Final vs Shakhtar
              </div>
            </div>
            <div class="ko-block">
              <div class="vs-txt">VS</div>
              <div class="ko-time">20:00</div>
              <div class="venue-txt">
                Selhurst Park<br />~25,486 capacity<br />Mon 20 Apr 2026
              </div>
            </div>
            <div class="t-side">
              <div class="t-badge" style="animation-delay: 0.12s">
                <img
                  src="https://cdn.brandfetch.io/idioDWtJyw/theme/dark/logo.svg?c=1bxid64Mup7aczewSAYMX&t=1668077966418"
                  alt="West Ham"
                  style="background-color: transparent" />
              </div>
              <div class="t-name" style="color: #e84060">West Ham Utd</div>
              <div class="t-stat">
                17th · ~30 pts · 1pt above drop<br />Full squad available —
                Desperate
              </div>
            </div>
          </div>

          <!-- Betting Odds -->
          <div class="odds-row">
            <div class="odds-box ob-cp">
              <div class="o-label">Palace Win</div>
              <div class="o-odds">13/10</div>
              <div class="o-implied">~43% implied</div>
            </div>
            <div class="odds-box ob-draw ob-value">
              <div class="o-label">★ Draw</div>
              <div class="o-odds">11/5</div>
              <div class="o-implied">~31% implied</div>
            </div>
            <div class="odds-box ob-whu">
              <div class="o-label">West Ham Win</div>
              <div class="o-odds">2/1</div>
              <div class="o-implied">~33% implied</div>
            </div>
            <div
              class="odds-box ob-draw"
              style="
                border-color: rgba(16, 217, 162, 0.3);
                background: linear-gradient(
                  135deg,
                  rgba(16, 217, 162, 0.06),
                  var(--s2)
                );
              ">
              <div class="o-label">Over 2.5 Goals</div>
              <div class="o-odds" style="color: var(--lo)">10/11</div>
              <div class="o-implied">~52% implied</div>
            </div>
          </div>
        </div>
      </div>

      <!-- CONTENT GRID -->
      <div class="content-grid">
        <!-- CONTEXT & MOTIVATION -->
        <div class="card span2" style="animation-delay: 0.08s">
          <div class="card-hd">
            <div class="hd-dot" style="background: var(--med)"></div>
            <div class="hd-title">
              Match Context · Motivation Analysis · Key Factors
            </div>
            <div
              class="hd-tag"
              style="
                color: var(--hi);
                border-color: rgba(245, 82, 42, 0.3);
                background: rgba(245, 82, 42, 0.09);
              ">
              Uneven Stakes
            </div>
          </div>
          <div class="card-body">
            <div class="ctx">
              <span class="badge-key k-cp">Palace</span> just celebrated in
              Florence after beating Fiorentina 4-2 on aggregate Thursday night
              —
              <strong
                >Dean Henderson was photographed dancing in the streets with
                fans until the early hours.</strong
              >
              Oliver Glasner sanctioned the celebrations. Palace are
              <strong>11 points clear of the relegation zone</strong>,
              mathematically almost safe, and their minds are firmly on the UECL
              semi-final vs Shakhtar Donetsk. Key injuries:
              <strong
                >Wharton (adductor — doubtful), Lacroix (knee — doubtful),
                Nketiah (hamstring), Doucoure (knee), Guessand (knee)</strong
              >. Palace have never won three consecutive PL meetings against
              West Ham. They are unbeaten in 6 straight home games across all
              competitions but have won just
              <strong>4 of 16 PL home games</strong> this season.

              <span
                class="badge-key k-whu"
                style="margin-top: 8px; display: inline-flex"
                >West Ham</span
              >
              are in a <strong>genuine relegation fight</strong> — just 1 point
              above the drop zone. Under Nuno Espírito Santo, they've collected
              18 points from 11 games since mid-January, one of the best runs in
              the division. They demolished Wolves 4-0 last Friday, are
              <strong>fully rested and fully fit</strong>, and arrived in London
              with everything to play for.
              <span class="badge-key k-alert">⚠️ Fatigue Factor</span> Palace
              played a high-intensity European tie Thursday, travelled home from
              Italy, and some players were partying. West Ham had a full week's
              rest. <span class="badge-key k-good">Stat Alert</span> Palace have
              conceded
              <strong>38.9% of goals from set pieces — highest in the PL</strong
              >. West Ham have scored from 4 of their last 7 corners
              (Mavropanos: 3 corner goals).
            </div>
          </div>
        </div>

        <!-- LAST 5 FORM -->
        <div class="card" style="animation-delay: 0.1s">
          <div class="card-hd">
            <div class="hd-dot" style="background: #e84060"></div>
            <div class="hd-title">Last 5 Matches — All Competitions</div>
          </div>
          <div class="card-body">
            <div class="form-cols">
              <div>
                <div class="form-team-lbl" style="color: #e84060">
                  <div class="form-ti">
                    <img
                      src="https://cdn.brandfetch.io/iddi0P11VR/theme/dark/logo.svg?c=1bxid64Mup7aczewSAYMX&t=1668077972554"
                      width="16"
                      height="16"
                      alt=""
                      style="background-color: transparent;" />
                  </div>
                  Crystal Palace
                </div>
                <div class="fr-list">
                  <div class="fr">
                    <div class="rdot L"></div>
                    <div class="fscore">1–2</div>
                    <div class="fopp">Fiorentina</div>
                    <div class="fcomp">
                      UECL <span class="ftag">progressed</span>
                    </div>
                  </div>
                  <div class="fr">
                    <div class="rdot W"></div>
                    <div class="fscore">2–1</div>
                    <div class="fopp">Newcastle Utd</div>
                    <div class="fcomp">PL Home</div>
                  </div>
                  <div class="fr">
                    <div class="rdot W"></div>
                    <div class="fscore">3–0</div>
                    <div class="fopp">Fiorentina</div>
                    <div class="fcomp">UECL Home</div>
                  </div>
                  <div class="fr">
                    <div class="rdot W"></div>
                    <div class="fscore">2–1</div>
                    <div class="fopp">Man United</div>
                    <div class="fcomp">PL Away</div>
                  </div>
                  <div class="fr">
                    <div class="rdot D"></div>
                    <div class="fscore">0–0</div>
                    <div class="fopp">AEK Larnaca</div>
                    <div class="fcomp">UECL Away</div>
                  </div>
                </div>
              </div>
              <div>
                <div class="form-team-lbl" style="color: #1bb1e7">
                  <div class="form-ti">
                    <img
                      src="https://cdn.brandfetch.io/idioDWtJyw/theme/dark/logo.svg?c=1bxid64Mup7aczewSAYMX&t=1668077966418"
                      width="16"
                      height="16"
                      alt=""
                      style="background-color: transparent;" />
                  </div>
                  West Ham Utd
                </div>
                <div class="fr-list">
                  <div class="fr">
                    <div class="rdot W"></div>
                    <div class="fscore">4–0</div>
                    <div class="fopp">Wolves</div>
                    <div class="fcomp">PL Home</div>
                  </div>
                  <div class="fr">
                    <div class="rdot D"></div>
                    <div class="fscore">1–1</div>
                    <div class="fopp">Southampton</div>
                    <div class="fcomp">PL Away</div>
                  </div>
                  <div class="fr">
                    <div class="rdot D"></div>
                    <div class="fscore">2–2</div>
                    <div class="fopp">Leicester</div>
                    <div class="fcomp">PL Home</div>
                  </div>
                  <div class="fr">
                    <div class="rdot W"></div>
                    <div class="fscore">3–1</div>
                    <div class="fopp">Arsenal</div>
                    <div class="fcomp">PL Home</div>
                  </div>
                  <div class="fr">
                    <div class="rdot D"></div>
                    <div class="fscore">1–1</div>
                    <div class="fopp">Brentford</div>
                    <div class="fcomp">PL Away</div>
                  </div>
                </div>
              </div>
            </div>
            <div class="form-legend">
              <div class="fl-i">
                <div class="fl-d" style="background: var(--lo)"></div>
                Win
              </div>
              <div class="fl-i">
                <div class="fl-d" style="background: var(--med)"></div>
                Draw
              </div>
              <div class="fl-i">
                <div class="fl-d" style="background: var(--hi)"></div>
                Loss
              </div>
            </div>
            <div class="section-note">
              Palace: W3 D1 L1 last 5 all comps (fatigue factor Thursday). West
              Ham: W2 D3 L0 last 5 · 9 goals scored in last 5 · 3 consecutive
              draws before Wolves rout.
            </div>
          </div>
        </div>

        <!-- H2H -->
        <div class="card" style="animation-delay: 0.12s">
          <div class="card-hd">
            <div class="hd-dot" style="background: #f5522a"></div>
            <div class="hd-title">Head to Head — Last 5 Meetings</div>
            <div
              class="hd-tag"
              style="
                color: var(--lo);
                border-color: rgba(16, 217, 162, 0.3);
                background: rgba(16, 217, 162, 0.07);
              ">
              BTTS in 8 of last 9 at Selhurst
            </div>
          </div>
          <div class="card-body">
            <div class="h2h-summary">
              <div class="hs">
                <div class="hn" style="color: #e84060">3</div>
                <div class="hl">Palace W</div>
              </div>
              <div class="hs">
                <div class="hn" style="color: var(--med)">1</div>
                <div class="hl">Draws</div>
              </div>
              <div class="hs">
                <div class="hn" style="color: #1bb1e7">1</div>
                <div class="hl">West Ham W</div>
              </div>
              <div class="hs">
                <div class="hn">2.6</div>
                <div class="hl">Avg Goals</div>
              </div>
            </div>
            <div class="h2h-rows">
              <div class="h2h-r">
                <div class="rh">West Ham</div>
                <div class="rs">1–2</div>
                <div class="ra">Crystal Palace</div>
                <div class="rx">PL Sep 2025 (away win for Palace)</div>
              </div>
              <div class="h2h-r">
                <div class="rh">Crystal Palace</div>
                <div class="rs">2–0</div>
                <div class="ra">West Ham</div>
                <div class="rx">PL Jan 2025 (at London Stadium)</div>
              </div>
              <div class="h2h-r">
                <div class="rh">West Ham</div>
                <div class="rs">2–0</div>
                <div class="ra">Crystal Palace</div>
                <div class="rx">PL Apr 2025 (last Selhurst meeting)</div>
              </div>
              <div class="h2h-r">
                <div class="rh">West Ham</div>
                <div class="rs">3–2</div>
                <div class="ra">Crystal Palace</div>
                <div class="rx">PL Aug 2024</div>
              </div>
              <div class="h2h-r">
                <div class="rh">Crystal Palace</div>
                <div class="rs">3–2</div>
                <div class="ra">West Ham</div>
                <div class="rx">PL Apr 2024</div>
              </div>
            </div>
            <div class="section-note">
              Palace won last 2 meetings. Never won 3 in a row vs WHU. West Ham
              won 3 of last 5 at Selhurst Park. Avg 2.6 goals per meeting. 9 of
              last 11 H2H meetings have seen both teams score.
            </div>
          </div>
        </div>

        <!-- SEASON AVERAGES -->
        <div class="card" style="animation-delay: 0.14s">
          <div class="card-hd">
            <div class="hd-dot" style="background: #a78bfa"></div>
            <div class="hd-title">Season Averages — PL 25/26</div>
          </div>
          <div class="card-body">
            <div class="avgs-pair">
              <div>
                <div
                  class="avg-team-lbl"
                  style="
                    color: #fff;
                    background: rgba(196, 18, 47, 0.15);
                    border: 1px solid rgba(196, 18, 47, 0.3);
                  ">
                  Crystal Palace
                </div>
                <div class="avg-cells">
                  <div class="ac">
                    <div class="av">11.7</div>
                    <div class="al">Shots/Gm</div>
                  </div>
                  <div class="ac">
                    <div class="av">3.7</div>
                    <div class="al">SOT/Gm</div>
                  </div>
                  <div class="ac">
                    <div class="av">4.4</div>
                    <div class="al">Corners</div>
                  </div>
                  <div class="ac">
                    <div class="av">11.0</div>
                    <div class="al">Fouls</div>
                  </div>
                  <div class="ac">
                    <div class="av">1.13</div>
                    <div class="al">Gls/Gm</div>
                  </div>
                  <div class="ac">
                    <div class="av">52%</div>
                    <div class="al">Poss</div>
                  </div>
                </div>
              </div>
              <div>
                <div
                  class="avg-team-lbl"
                  style="
                    color: #fff;
                    background: rgba(27, 177, 231, 0.1);
                    border: 1px solid rgba(27, 177, 231, 0.28);
                  ">
                  West Ham
                </div>
                <div class="avg-cells">
                  <div class="ac">
                    <div class="av">10.5</div>
                    <div class="al">Shots/Gm</div>
                  </div>
                  <div class="ac">
                    <div class="av">3.3</div>
                    <div class="al">SOT/Gm</div>
                  </div>
                  <div class="ac">
                    <div class="av">4.4</div>
                    <div class="al">Corners</div>
                  </div>
                  <div class="ac">
                    <div class="av">11.2</div>
                    <div class="al">Fouls</div>
                  </div>
                  <div class="ac">
                    <div class="av">1.26</div>
                    <div class="al">Gls/Gm</div>
                  </div>
                  <div class="ac">
                    <div class="av">41%</div>
                    <div class="al">Poss</div>
                  </div>
                </div>
              </div>
            </div>
            <div class="xg-box" style="margin-top: 10px">
              <div class="xg-item">
                <div class="xg-val" style="color: #e84060">1.08</div>
                <div class="xg-lbl">Palace xG/gm</div>
              </div>
              <div class="xg-item">
                <div class="xg-val" style="color: #ff5f45">1.37</div>
                <div class="xg-lbl">Palace xGA/gm</div>
              </div>
              <div class="xg-item">
                <div class="xg-val" style="color: #1bb1e7">1.15</div>
                <div class="xg-lbl">West Ham xG/gm</div>
              </div>
              <div class="xg-item">
                <div class="xg-val" style="color: #ff9a5c">1.42</div>
                <div class="xg-lbl">WHU xGA/gm</div>
              </div>
              <div class="xg-item">
                <div class="xg-val" style="color: var(--hi)">38.9%</div>
                <div class="xg-lbl">
                  Palace set-piece goals conceded (PL highest)
                </div>
              </div>
            </div>
          </div>
        </div>

        <!-- HOME / AWAY STATS -->
        <div class="card" style="animation-delay: 0.16s">
          <div class="card-hd">
            <div class="hd-dot" style="background: var(--lo)"></div>
            <div class="hd-title">Home / Away Performance Splits</div>
          </div>
          <div class="card-body">
            <div class="avgs-pair">
              <div>
                <div
                  class="avg-team-lbl"
                  style="
                    color: #fff;
                    background: rgba(196, 18, 47, 0.15);
                    border: 1px solid rgba(196, 18, 47, 0.3);
                  ">
                  Palace at Home
                </div>
                <div class="avg-cells">
                  <div class="ac">
                    <div class="av">4</div>
                    <div class="al">PL Home W</div>
                  </div>
                  <div class="ac">
                    <div class="av">4.8</div>
                    <div class="al">Corners/gm</div>
                  </div>
                  <div class="ac">
                    <div class="av">3.9</div>
                    <div class="al">Corners conceded</div>
                  </div>
                  <div class="ac">
                    <div class="av">1.0</div>
                    <div class="al">Goals scored</div>
                  </div>
                  <div class="ac">
                    <div class="av">7</div>
                    <div class="al">Home draws</div>
                  </div>
                  <div class="ac">
                    <div class="av">6</div>
                    <div class="al">Home unbeaten streak</div>
                  </div>
                </div>
              </div>
              <div>
                <div
                  class="avg-team-lbl"
                  style="
                    color: #fff;
                    background: rgba(27, 177, 231, 0.1);
                    border: 1px solid rgba(27, 177, 231, 0.28);
                  ">
                  West Ham Away
                </div>
                <div class="avg-cells">
                  <div class="ac">
                    <div class="av">3</div>
                    <div class="al">Away W (last 5)</div>
                  </div>
                  <div class="ac">
                    <div class="av">9.8</div>
                    <div class="al">Shots away</div>
                  </div>
                  <div class="ac">
                    <div class="av">7.0</div>
                    <div class="al">Corners conceded</div>
                  </div>
                  <div class="ac">
                    <div class="av">3.3</div>
                    <div class="al">SOT away</div>
                  </div>
                  <div class="ac">
                    <div class="av">94%</div>
                    <div class="al">Away O1.5g</div>
                  </div>
                  <div class="ac">
                    <div class="av">55%</div>
                    <div class="al">Away O2.5g</div>
                  </div>
                </div>
              </div>
            </div>
            <div class="section-note">
              West Ham have one of the worst away corner-conceding records
              (7.0/game). Palace keep it tight at the back at home (3.94 corners
              conceded/home match — 3rd best in league). Palace won just 4 of 16
              PL home games however.
            </div>
          </div>
        </div>

        <!-- PREDICTIONS TABLE -->
        <div class="card span2" style="animation-delay: 0.18s">
          <div class="card-hd">
            <div class="hd-dot" style="background: var(--lo)"></div>
            <div class="hd-title">
              Weighted Stat Predictions — Crystal Palace vs West Ham
            </div>
          </div>
          <div class="card-body">
            <div class="pt-intro">
              <div class="pt-key">
                <div class="pt-kd" style="background: var(--lo)"></div>
                <span style="color: var(--lo); font-weight: 700"
                  >Low (floor)</span
                >
              </div>
              <div class="pt-key">
                <div class="pt-kd" style="background: var(--med)"></div>
                <span style="color: var(--med); font-weight: 700"
                  >Median (weighted)</span
                >
              </div>
              <div class="pt-key">
                <div class="pt-kd" style="background: var(--hi)"></div>
                <span style="color: var(--hi); font-weight: 700"
                  >High (ceiling)</span
                >
              </div>
            </div>
            <div class="ptw">
              <table class="pred-t">
                <colgroup>
                  <col style="width: 22%" />
                  <col style="width: 15%" />
                  <col style="width: 15%" />
                  <col style="width: 12%" />
                  <col style="width: 12%" />
                  <col style="width: 12%" />
                  <col style="width: 12%" />
                </colgroup>
                <thead>
                  <tr>
                    <th>Metric</th>
                    <th class="tc" style="color: #e84060">Palace</th>
                    <th class="tc" style="color: #1bb1e7">West Ham</th>
                    <th class="tc" style="color: var(--lo)">Total Low</th>
                    <th class="tc" style="color: var(--med)">Median</th>
                    <th class="tc" style="color: var(--hi)">Total High</th>
                    <th class="tc" style="color: var(--muted)">Intensity</th>
                  </tr>
                </thead>
                <tbody>
                  <tr>
                    <td class="tn">🔲 Corners</td>
                    <td class="tv">
                      <div class="stat-team">
                        <span class="st-val" style="color: #e84060">5</span
                        ><span class="st-lbl">med</span>
                      </div>
                    </td>
                    <td class="tv">
                      <div class="stat-team">
                        <span class="st-val" style="color: #1bb1e7">5</span
                        ><span class="st-lbl">med</span>
                      </div>
                    </td>
                    <td class="tv"><span class="lv">7</span></td>
                    <td class="tv"><span class="mv">10</span></td>
                    <td class="tv"><span class="hv">15</span></td>
                    <td>
                      <div class="rbar-wrap">
                        <div class="rbar-t">
                          <div
                            class="rbar-f"
                            data-pct="62"
                            style="
                              background: linear-gradient(
                                90deg,
                                var(--lo),
                                var(--hi)
                              );
                            "></div>
                        </div>
                      </div>
                    </td>
                  </tr>
                  <tr>
                    <td class="tn">📊 Total Shots</td>
                    <td class="tv">
                      <div class="stat-team">
                        <span class="st-val" style="color: #e84060">12</span
                        ><span class="st-lbl">med</span>
                      </div>
                    </td>
                    <td class="tv">
                      <div class="stat-team">
                        <span class="st-val" style="color: #1bb1e7">10</span
                        ><span class="st-lbl">med</span>
                      </div>
                    </td>
                    <td class="tv"><span class="lv">16</span></td>
                    <td class="tv"><span class="mv">22</span></td>
                    <td class="tv"><span class="hv">30</span></td>
                    <td>
                      <div class="rbar-wrap">
                        <div class="rbar-t">
                          <div
                            class="rbar-f"
                            data-pct="68"
                            style="
                              background: linear-gradient(
                                90deg,
                                var(--lo),
                                var(--hi)
                              );
                            "></div>
                        </div>
                      </div>
                    </td>
                  </tr>
                  <tr>
                    <td class="tn">🎯 Shots on Target</td>
                    <td class="tv">
                      <div class="stat-team">
                        <span class="st-val" style="color: #e84060">4</span
                        ><span class="st-lbl">med</span>
                      </div>
                    </td>
                    <td class="tv">
                      <div class="stat-team">
                        <span class="st-val" style="color: #1bb1e7">3</span
                        ><span class="st-lbl">med</span>
                      </div>
                    </td>
                    <td class="tv"><span class="lv">5</span></td>
                    <td class="tv"><span class="mv">7</span></td>
                    <td class="tv"><span class="hv">13</span></td>
                    <td>
                      <div class="rbar-wrap">
                        <div class="rbar-t">
                          <div
                            class="rbar-f"
                            data-pct="58"
                            style="
                              background: linear-gradient(
                                90deg,
                                var(--lo),
                                var(--hi)
                              );
                            "></div>
                        </div>
                      </div>
                    </td>
                  </tr>
                  <tr>
                    <td class="tn">⚠️ Fouls</td>
                    <td class="tv">
                      <div class="stat-team">
                        <span class="st-val" style="color: #e84060">11</span
                        ><span class="st-lbl">med</span>
                      </div>
                    </td>
                    <td class="tv">
                      <div class="stat-team">
                        <span class="st-val" style="color: #1bb1e7">13</span
                        ><span class="st-lbl">med</span>
                      </div>
                    </td>
                    <td class="tv"><span class="lv">18</span></td>
                    <td class="tv"><span class="mv">24</span></td>
                    <td class="tv"><span class="hv">34</span></td>
                    <td>
                      <div class="rbar-wrap">
                        <div class="rbar-t">
                          <div
                            class="rbar-f"
                            data-pct="74"
                            style="
                              background: linear-gradient(
                                90deg,
                                var(--lo),
                                var(--hi)
                              );
                            "></div>
                        </div>
                      </div>
                    </td>
                  </tr>
                  <tr>
                    <td class="tn">↗️ Throw-ins</td>
                    <td class="tv">
                      <div class="stat-team">
                        <span class="st-val" style="color: #e84060">21</span
                        ><span class="st-lbl">med</span>
                      </div>
                    </td>
                    <td class="tv">
                      <div class="stat-team">
                        <span class="st-val" style="color: #1bb1e7">21</span
                        ><span class="st-lbl">med</span>
                      </div>
                    </td>
                    <td class="tv"><span class="lv">30</span></td>
                    <td class="tv"><span class="mv">42</span></td>
                    <td class="tv"><span class="hv">56</span></td>
                    <td>
                      <div class="rbar-wrap">
                        <div class="rbar-t">
                          <div
                            class="rbar-f"
                            data-pct="64"
                            style="
                              background: linear-gradient(
                                90deg,
                                var(--lo),
                                var(--hi)
                              );
                            "></div>
                        </div>
                      </div>
                    </td>
                  </tr>
                  <tr>
                    <td class="tn">🥅 Goal Kicks</td>
                    <td class="tv">
                      <div class="stat-team">
                        <span class="st-val" style="color: #e84060">10</span
                        ><span class="st-lbl">med</span>
                      </div>
                    </td>
                    <td class="tv">
                      <div class="stat-team">
                        <span class="st-val" style="color: #1bb1e7">11</span
                        ><span class="st-lbl">med</span>
                      </div>
                    </td>
                    <td class="tv"><span class="lv">14</span></td>
                    <td class="tv"><span class="mv">21</span></td>
                    <td class="tv"><span class="hv">28</span></td>
                    <td>
                      <div class="rbar-wrap">
                        <div class="rbar-t">
                          <div
                            class="rbar-f"
                            data-pct="60"
                            style="
                              background: linear-gradient(
                                90deg,
                                var(--lo),
                                var(--hi)
                              );
                            "></div>
                        </div>
                      </div>
                    </td>
                  </tr>
                  <tr>
                    <td class="tn">⚔️ Tackles</td>
                    <td class="tv">
                      <div class="stat-team">
                        <span class="st-val" style="color: #e84060">15</span
                        ><span class="st-lbl">med</span>
                      </div>
                    </td>
                    <td class="tv">
                      <div class="stat-team">
                        <span class="st-val" style="color: #1bb1e7">16</span
                        ><span class="st-lbl">med</span>
                      </div>
                    </td>
                    <td class="tv"><span class="lv">24</span></td>
                    <td class="tv"><span class="mv">31</span></td>
                    <td class="tv"><span class="hv">42</span></td>
                    <td>
                      <div class="rbar-wrap">
                        <div class="rbar-t">
                          <div
                            class="rbar-f"
                            data-pct="70"
                            style="
                              background: linear-gradient(
                                90deg,
                                var(--lo),
                                var(--hi)
                              );
                            "></div>
                        </div>
                      </div>
                    </td>
                  </tr>
                </tbody>
              </table>
            </div>
            <div class="section-note" style="margin-top: 10px">
              <strong style="color: var(--med)">Key weightings:</strong> Corners
              elevated as West Ham attack wide through Bowen + Summerville. West
              Ham concede most corners away (7.0/gm). Fouls elevated by Darren
              England's record (10 yellows in one recent game), West Ham
              desperation & London derby physicality. Tackles inflated by West
              Ham's counter-pressing. Goal kicks reflect West Ham's
              low-possession style + Palace building from back.
            </div>
          </div>
        </div>

        <!-- SCORE PREDICTION -->
        <div class="card" style="animation-delay: 0.2s">
          <div class="card-hd">
            <div class="hd-dot" style="background: var(--med)"></div>
            <div class="hd-title">Score Prediction · Probability Analysis</div>
          </div>
          <div class="card-body">
            <div class="score-zone">
              <div class="sz-head">Crystal Palace vs West Ham United</div>
              <div class="s-boxes">
                <div class="sbox">
                  <div class="sb-lbl">Half-Time</div>
                  <div class="sb-score">1–0</div>
                  <div class="sb-prob">Palace lead ~36%</div>
                </div>
                <div class="sbox feat">
                  <div class="sb-lbl">Full-Time ★ Best Pick</div>
                  <div class="sb-score feat-s">2–1</div>
                  <div class="sb-prob">Crystal Palace ~27%</div>
                </div>
                <div class="sbox">
                  <div class="sb-lbl">Safe / Draw Pick</div>
                  <div class="sb-score">1–1</div>
                  <div class="sb-prob">Draw ~31%</div>
                </div>
              </div>
              <div class="sz-note">
                <strong>Why Palace 2-1 (best pick):</strong> Palace are unbeaten
                in 6 home games across all competitions. Despite fatigue, the
                UECL euphoria creates a home atmosphere that motivates players.
                Mateta (10 PL goals, 48 career PL goals) is clinical in front of
                goal, with a brace vs Newcastle last Sunday showing he's on
                fire. Both teams have scored in 8 of last 9 H2H at Selhurst.
                West Ham's attacking threat through Bowen (scored in last 2 vs
                Palace) and Castellanos (5 goals since January) makes BTTS
                almost inevitable. Palace take the win thanks to home advantage
                + Mateta but it won't be comfortable. Confidence after the
                European triumph offsets the fatigue factor.
              </div>
              <div class="safe-pick">
                <strong
                  >🛡️ Safe/Betting Strategy Pick — Draw (11/5) or BTTS
                  (Yes):</strong
                >
                With Palace's fatigued squad, West Ham's freshness and
                desperation, and the H2H record showing 6 of last 8 at
                Everton-style near-even fixtures ending in draws or close games,
                the draw at 11/5 represents strong value. BTTS Yes at around
                8/11–7/10 is the most statistically backed selection given 8 of
                last 9 H2H at Selhurst Park saw both teams score, and West Ham's
                94% BTTS away record this season.
              </div>
            </div>
          </div>
        </div>

        <!-- YELLOW CARDS -->
        <div class="card" style="animation-delay: 0.22s">
          <div class="card-hd">
            <div class="hd-dot" style="background: #ffe84a"></div>
            <div class="hd-title">🟨 Yellow Card Risk Players</div>
            <div
              class="hd-tag"
              style="
                color: var(--med);
                border-color: rgba(246, 200, 64, 0.3);
                background: rgba(246, 200, 64, 0.07);
              ">
              Darren England — Very Strict (10 yellows in 1 game)
            </div>
          </div>
          <div class="card-body">
            <div class="yc-list">
              <div class="yc">
                <div class="yc-ico">🟨</div>
                <div class="yc-inf">
                  <div class="yc-n">
                    Mateus Fernandes
                    <span class="yc-cl" style="color: #1bb1e7"
                      >West Ham · CM</span
                    >
                  </div>
                  <div class="yc-r">
                    7 yellow cards since joining West Ham last summer.
                    Aggressive driving midfielder who combats in the centre.
                    Faces Palace's physical midfield in a desperation fixture
                    with England in charge.
                  </div>
                </div>
                <div class="risk r-h">HIGH</div>
              </div>
              <div class="yc">
                <div class="yc-ico">🟨</div>
                <div class="yc-inf">
                  <div class="yc-n">
                    Jefferson Lerma
                    <span class="yc-cl" style="color: #e84060"
                      >Crystal Palace · DM</span
                    >
                  </div>
                  <div class="yc-r">
                    Crystal Palace's defensive pivot with 5 PL yellows this
                    season. Will face Bowen and Summerville's direct running —
                    one mistimed tackle against a desperate West Ham attack is
                    near-certain. Darren England notices midfield fouls
                    immediately.
                  </div>
                </div>
                <div class="risk r-h">HIGH</div>
              </div>
              <div class="yc">
                <div class="yc-ico">🟨</div>
                <div class="yc-inf">
                  <div class="yc-n">
                    Konstantinos Mavropanos
                    <span class="yc-cl" style="color: #1bb1e7"
                      >West Ham · CB</span
                    >
                  </div>
                  <div class="yc-r">
                    Scored twice vs Wolves, threatens at set pieces, and fouls
                    energetically when beaten 1v1. 3 corner goals this season
                    signals his attacking aggression which sometimes leads to
                    defensive misjudgments and bookings when tracking Palace's
                    runners.
                  </div>
                </div>
                <div class="risk r-m">MED</div>
              </div>
              <div class="yc">
                <div class="yc-ico">🟨</div>
                <div class="yc-inf">
                  <div class="yc-n">
                    Lucas Paquetá
                    <span class="yc-cl" style="color: #1bb1e7"
                      >West Ham · AM</span
                    >
                  </div>
                  <div class="yc-r">
                    Disciplinary risk even in normal games. With high stakes and
                    England's strict refereeing style, Paquetá's frustration
                    when things don't go right in a relegation battle = booking.
                    His reactive fouls when losing the ball are well documented.
                  </div>
                </div>
                <div class="risk r-m">MED</div>
              </div>
              <div class="yc">
                <div class="yc-ico">🟨</div>
                <div class="yc-inf">
                  <div class="yc-n">
                    Will Hughes
                    <span class="yc-cl" style="color: #e84060"
                      >Palace · CM</span
                    >
                  </div>
                  <div class="yc-r">
                    Likely to fill the Wharton role if the midfielder is ruled
                    out. Less composed under pressure, prone to impulsive fouls
                    against physical opponents. West Ham's counter-pressing will
                    test him in open positions.
                  </div>
                </div>
                <div class="risk r-m">MED</div>
              </div>
            </div>
          </div>
        </div>

        <!-- BETTING ANALYSIS -->
        <div class="card span2" style="animation-delay: 0.24s">
          <div class="card-hd">
            <div class="hd-dot" style="background: var(--lo)"></div>
            <div class="hd-title">
              📈 Betting Market Analysis · Value Picks · Current Patterns
            </div>
          </div>
          <div class="card-body">
            <div class="bet-grid">
              <div class="bet-cell val">
                <div class="bc-market">★ Best Value</div>
                <div class="bc-line val-txt">BTTS Yes</div>
                <div class="bc-reason">
                  8 of 9 recent H2H at Selhurst. West Ham 94% BTTS away. Both
                  teams xG supports 2+ goals. ~7/10 available.
                </div>
              </div>
              <div class="bet-cell val">
                <div class="bc-market">★ Value Draw</div>
                <div class="bc-line val-txt">Draw 11/5</div>
                <div class="bc-reason">
                  Fatigue + motivation imbalance + 6 of last 8 London derbies at
                  Everton-type grounds ending close. Market slightly overrates
                  Palace.
                </div>
              </div>
              <div class="bet-cell">
                <div class="bc-market">Corners O9.5</div>
                <div class="bc-line">Over 9.5</div>
                <div class="bc-reason">
                  WHU concede 7.0 corners/away game. Bowen/Summerville draw
                  corners. WHU scored from 4 of last 7 corners. Likely O9.5
                  value.
                </div>
              </div>
              <div class="bet-cell">
                <div class="bc-market">Prop: Jarrod Bowen</div>
                <div class="bc-line">To Score +225</div>
                <div class="bc-reason">
                  Scored in last 2 vs Palace. 7 assists in 13 games in 2026.
                  Most dangerous WHU player. Value at +225 given recent Palace
                  conceding pattern.
                </div>
              </div>
              <div class="bet-cell">
                <div class="bc-market">O2.5 Goals</div>
                <div class="bc-line">10/11</div>
                <div class="bc-reason">
                  At least 3 goals in 4 of last 4 Palace games. WHU last 5 all
                  over 2.0 goals. Slight lean away — 9 of last 11 Palace home PL
                  under 3.5.
                </div>
              </div>
              <div class="bet-cell">
                <div class="bc-market">Prop: Mateta</div>
                <div class="bc-line">Anytime Scorer</div>
                <div class="bc-reason">
                  10 PL goals, 48 career PL goals (closing in on 50). Brace vs
                  Newcastle. Palace's primary goal threat with Nketiah out.
                  Strong value.
                </div>
              </div>
              <div class="bet-cell">
                <div class="bc-market">Cards O3.5</div>
                <div class="bc-line">Likely Over</div>
                <div class="bc-reason">
                  Darren England averaged 10 yellows in one recent game. London
                  derby intensity. Fernandes (7 yellows) + Lerma (5) = high card
                  ceiling. Watch O3.5.
                </div>
              </div>
              <div class="bet-cell">
                <div class="bc-market">⚠️ Risk</div>
                <div class="bc-line" style="color: var(--hi)">
                  Avoid: WHU Win
                </div>
                <div class="bc-reason">
                  2/1 looks tempting but Palace's home record at Selhurst
                  (unbeaten 6) and Mateta form makes WHU win higher variance
                  than the odds suggest.
                </div>
              </div>
            </div>
            <div class="bet-note">
              <strong>Overall Assessment:</strong> This match has a clear
              motivation imbalance — West Ham (94% motivation) vs a Palace squad
              returning from Florence celebrations (58% motivation). However,
              home advantage, Mateta's form, and the Selhurst Park atmosphere
              for a London derby partially offset that.
              <strong
                >The BTTS Yes market offers the strongest statistical
                edge</strong
              >
              given how reliably both teams score in this fixture. For match
              result, the Draw at 11/5 carries genuine value given the fatigue
              factor, West Ham's road form improvement, and statistical
              regression toward Palace's moderate home win rate (only 4W in 16
              home PL games). Market has Palace at ~43% implied — closer to
              38-40% adjusted for the Thursday fatigue factor.
              <strong
                >The safest bankroll strategy: BTTS Yes + Draw no-bet (Palace)
                combination.</strong
              >
            </div>
          </div>
        </div>

        <!-- INJURIES & LINEUPS -->
        <div class="card" style="animation-delay: 0.26s">
          <div class="card-hd">
            <div class="hd-dot" style="background: #ff5f45"></div>
            <div class="hd-title">Team News · Injuries · Predicted XIs</div>
          </div>
          <div class="card-body">
            <div class="form-cols">
              <div>
                <div class="form-team-lbl" style="color: #e84060">
                  Crystal Palace XI (4-3-3)
                </div>
                <div
                  style="
                    font-size: 11.5px;
                    color: var(--label);
                    line-height: 1.7;
                  ">
                  <span style="color: #e84060">GK</span> Henderson<br />
                  <span style="color: #e84060">DEF</span> Mitchell ·
                  Lacroix/Richards? · Kanwo · Muñoz<br />
                  <span style="color: #e84060">MID</span> Lerma ·
                  Hughes/Wharton? · Eze<br />
                  <span style="color: #e84060">FWD</span> Sarr · Mateta ·
                  Pino/Strand Larsen
                </div>
                <div style="margin-top: 10px; font-size: 11px">
                  <div
                    style="
                      color: var(--hi);
                      margin-bottom: 3px;
                      font-weight: 600;
                    ">
                    ❌ Ruled Out:
                  </div>
                  <div style="color: var(--muted); line-height: 1.8">
                    Nketiah (hamstring) · Doucoure (knee) · Guessand (knee)
                  </div>
                  <div
                    style="
                      color: var(--med);
                      margin-top: 5px;
                      margin-bottom: 3px;
                      font-weight: 600;
                    ">
                    ⚠️ Doubts (missed Thu):
                  </div>
                  <div style="color: var(--muted); line-height: 1.8">
                    Wharton (adductor) · Lacroix (knee) · Fatigue risk across
                    squad
                  </div>
                </div>
              </div>
              <div>
                <div class="form-team-lbl" style="color: #1bb1e7">
                  West Ham XI (4-2-3-1)
                </div>
                <div
                  style="
                    font-size: 11.5px;
                    color: var(--label);
                    line-height: 1.7;
                  ">
                  <span style="color: #1bb1e7">GK</span> Hermansen (Fabianski
                  maybe)<br />
                  <span style="color: #1bb1e7">DEF</span> Walker-Peters ·
                  Mavropanos · Disasi · Diouf<br />
                  <span style="color: #1bb1e7">MID</span> Fernandes · Souček<br />
                  <span style="color: #1bb1e7">ATT</span> Bowen · Pablo ·
                  Summerville<br />
                  <span style="color: #1bb1e7">FWD</span> Castellanos
                </div>
                <div style="margin-top: 10px; font-size: 11px">
                  <div
                    style="
                      color: var(--lo);
                      margin-bottom: 3px;
                      font-weight: 600;
                    ">
                    ✅ Near Full Strength:
                  </div>
                  <div style="color: var(--muted); line-height: 1.8">
                    Fabianski (back) — may be passed fit. Summerville back from
                    injury. Squad confirmed healthy by Nuno.
                  </div>
                  <div
                    style="
                      color: var(--med);
                      margin-top: 5px;
                      margin-bottom: 3px;
                      font-weight: 600;
                    ">
                    🔑 Key Threats:
                  </div>
                  <div style="color: var(--muted); line-height: 1.8">
                    Bowen (7 assists in 2026) · Castellanos (5 goals since Jan)
                    · Mavropanos (3 corner goals)
                  </div>
                </div>
              </div>
            </div>
          </div>
        </div>

        <!-- ANALYST NOTES -->
        <div class="card" style="animation-delay: 0.28s">
          <div class="card-hd">
            <div class="hd-dot" style="background: #7ab8e0"></div>
            <div class="hd-title">Analyst Notes · Key Matchup Factors</div>
          </div>
          <div class="card-body">
            <div style="display: flex; flex-direction: column; gap: 8px">
              <div
                style="
                  background: var(--s2);
                  border-radius: 6px;
                  padding: 10px 12px;
                  border: 1px solid var(--border);
                  font-size: 12px;
                  color: var(--label);
                  line-height: 1.65;
                ">
                <strong style="color: #e84060"
                  >Palace Set-Piece Vulnerability:</strong
                >
                Conceding 38.9% of goals from set pieces (PL-highest) against a
                West Ham team that's scored from 4 of their last 7 corners with
                Mavropanos heading in 3 of those is the single most
                statistically compelling factor in this match.
                <strong style="color: var(--med)"
                  >Watch the corner count carefully</strong
                >
                — this could be where the game turns.
              </div>
              <div
                style="
                  background: var(--s2);
                  border-radius: 6px;
                  padding: 10px 12px;
                  border: 1px solid var(--border);
                  font-size: 12px;
                  color: var(--label);
                  line-height: 1.65;
                ">
                <strong style="color: #1bb1e7"
                  >West Ham's Second-Half Pattern:</strong
                >
                Under Nuno, West Ham have scored 5 goals in the second half in
                their last 2 games. Palace have conceded to West Ham in the
                second half in 5 of their last 6 home PL fixtures.
                <strong style="color: var(--med)"
                  >Expect West Ham to grow into the game</strong
                >
                — backing them in second-half markets may carry value.
              </div>
              <div
                style="
                  background: var(--s2);
                  border-radius: 6px;
                  padding: 10px 12px;
                  border: 1px solid var(--border);
                  font-size: 12px;
                  color: var(--label);
                  line-height: 1.65;
                ">
                <strong style="color: var(--lo)"
                  >Conference League Focus:</strong
                >
                Palace's UECL semi-final vs Shakhtar Donetsk looms large.
                Glasner may manage minutes for key players — if Mateta is
                fatigued from Thursday, Strand Larsen could deputise. This
                rotation risk could affect Palace's attacking output
                significantly.
              </div>
              <div
                style="
                  background: var(--s2);
                  border-radius: 6px;
                  padding: 10px 12px;
                  border: 1px solid var(--border);
                  font-size: 12px;
                  color: var(--label);
                  line-height: 1.65;
                ">
                <strong style="color: var(--med)">Historical Pattern:</strong>
                Crystal Palace have scored at least 2 goals in 9 of their last
                11 H2H meetings with West Ham. West Ham have scored at least 2
                goals in 5 of their last 6 away meetings at Selhurst. Over 2.5
                goals in 7 of the last 10 H2H meetings. This is historically a
                high-scoring fixture.
              </div>
            </div>
          </div>
        </div>
      </div>
      <!-- end grid -->
    </div>
    <!-- end wrap -->

    <footer
      style="
        text-align: center;
        padding: 20px 16px;
        font-family: 'Inter', sans-serif;
        font-size: 11px;
        color: var(--muted);
        border-top: 1px solid var(--border);
        position: relative;
        z-index: 1;
      ">
      <p><strong>Team Bilbo Statistical Analysis</strong><br /></p>
      <p style="margin-top: 4px;">
        Statistical predictions are weighted estimates based on historical data and form analysis.<br />
        <strong style="color: var(--hi); text-decoration: underline;"
          >ALWAYS GAMBLE RESPONSIBLY, THIS IS NOT FINANCIAL ADVICE</strong
        >
      </p>
    </footer>

    <script>
      ;(function () {
        'use strict'

        /* Bar fill animations on scroll */
        const fills = document.querySelectorAll('.rbar-f[data-pct]')
        if ('IntersectionObserver' in window) {
          const obs = new IntersectionObserver(
            entries => {
              entries.forEach(e => {
                if (e.isIntersecting) {
                  const el = e.target
                  setTimeout(() => {
                    el.style.width = el.getAttribute('data-pct') + '%'
                  }, 200)
                  obs.unobserve(el)
                }
              })
            },
            { threshold: 0.3 },
          )
          fills.forEach(f => obs.observe(f))
        } else {
          fills.forEach(f => (f.style.width = f.getAttribute('data-pct') + '%'))
        }

        /* Motivation bars */
        setTimeout(() => {
          document
            .querySelectorAll('.mot-fill-cp, .mot-fill-whu')
            .forEach(el => {
              const target = el.style.width
              el.style.width = '0'
              setTimeout(() => {
                el.style.transition = 'width 1s ease'
                el.style.width = target
              }, 300)
            })
        }, 400)

        /* Count-up for avg stats */
        const avCells = document.querySelectorAll('.ac .av')
        if ('IntersectionObserver' in window) {
          const obs2 = new IntersectionObserver(
            entries => {
              entries.forEach(e => {
                if (e.isIntersecting) {
                  const el = e.target
                  const raw = el.textContent.trim()
                  if (!el.dataset.done) {
                    el.dataset.done = '1'
                    const isPercent = raw.includes('%')
                    const num = parseFloat(raw)
                    if (!isNaN(num)) {
                      let cur = 0
                      const step = num / (700 / 16)
                      const t = setInterval(() => {
                        cur += step
                        if (cur >= num) {
                          cur = num
                          clearInterval(t)
                        }
                        el.textContent =
                          (raw.includes('.')
                            ? cur.toFixed(1)
                            : Math.round(cur)) + (isPercent ? '%' : '')
                      }, 16)
                    }
                  }
                  obs2.unobserve(el)
                }
              })
            },
            { threshold: 0.8 },
          )
          avCells.forEach(c => obs2.observe(c))
        }

        /* Card stagger */
        document.querySelectorAll('.card').forEach((c, i) => {
          c.style.animationDelay = 0.07 + i * 0.06 + 's'
        })
      })()
    </script>
