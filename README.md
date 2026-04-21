<html lang="en">

<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Brighton vs Chelsea · PL Predictor · 21 April 2026</title>
  <link rel="preconnect" href="https://fonts.googleapis.com">
  <link
    href="https://fonts.googleapis.com/css2?family=Exo+2:wght@300;400;500;600;700;800;900&family=Inter:wght@300;400;500;600&display=swap"
    rel="stylesheet">
  <style>
    :root {
      /* Brighton */
      --bha-blue: #0057B8;
      --bha-white: #FFFFFF;
      --bha-light: rgba(0, 87, 184, 0.15);

      /* Chelsea */
      --che-blue: #034694;
      --che-gold: #C8A84B;
      --che-light: rgba(3, 70, 148, 0.15);

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
      line-height: 1.6;
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
        transform: scale(.5) rotate(-8deg);
        opacity: 0;
      }

      to {
        transform: scale(1) rotate(0);
        opacity: 1;
      }
    }

    @keyframes barGrow {
      from {
        width: 0 !important;
      }
    }

    @keyframes shimmer {

      0%,
      100% {
        opacity: .6;
      }

      50% {
        opacity: 1;
      }
    }

    @keyframes spin {
      from {
        transform: rotate(0);
      }

      to {
        transform: rotate(360deg);
      }
    }

    @keyframes pulse {

      0%,
      100% {
        transform: scale(1);
      }

      50% {
        transform: scale(1.05);
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
      background: linear-gradient(135deg, var(--bha-light) 0%, var(--bg2) 45%, var(--che-light) 100%);
      border-radius: 16px;
      border: 1px solid var(--border2);
      overflow: hidden;
      margin-top: 22px;
      box-shadow: 0 12px 60px rgba(0, 0, 0, .55);
      animation: fadeUp .55s ease both;
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

    /* Teams row */
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
      flex-shrink: 0;
    }

    .badge-ring:hover {
      transform: scale(1.12) rotate(5deg);
    }

    .badge-ring img,
    .badge-ring svg {
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

    .venue-txt {
      font-size: 8.5px;
      color: var(--muted);
      text-align: center;
      line-height: 1.55;
    }

    /* Motivation bars */
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
      white-space: nowrap;
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
    }

    .mot-val {
      font-family: 'Exo 2', sans-serif;
      font-size: 13px;
      font-weight: 800;
      white-space: nowrap;
    }

    /* Odds row */
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

    .ob-val .ob-lbl {
      color: var(--amber);
    }

    /* ─── GRID ─── */
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

    /* ─── CARD ─── */
    .card {
      background: var(--bg2);
      border: 1px solid var(--border);
      border-radius: 12px;
      overflow: hidden;
      box-shadow: 0 4px 28px rgba(0, 0, 0, .35);
      transition: border-color .3s;
      animation: fadeUp .5s ease both;
    }

    .card:hover {
      border-color: var(--border2);
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
      font-family: 'Exo 2', sans-serif;
      font-size: 9.5px;
      font-weight: 700;
      letter-spacing: 2px;
      text-transform: uppercase;
      color: var(--muted);
      flex: 1;
    }

    .hd-tag {
      font-size: 8.5px;
      font-weight: 700;
      letter-spacing: .8px;
      text-transform: uppercase;
      padding: 2px 8px;
      border-radius: 4px;
      border: 1px solid;
      white-space: nowrap;
    }

    .card-body {
      padding: 14px 18px;
    }

    /* Context box */
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

    .ctx .key-badge {
      display: inline-flex;
      align-items: center;
      gap: 4px;
      font-size: 10px;
      font-weight: 700;
      letter-spacing: .7px;
      text-transform: uppercase;
      padding: 1px 7px;
      border-radius: 3px;
      border: 1px solid;
      margin-right: 2px;
    }

    .kb-bha {
      color: #60a5fa;
      border-color: rgba(0, 87, 184, .4);
      background: rgba(0, 87, 184, .12);
    }

    .kb-che {
      color: #a5c4ff;
      border-color: rgba(3, 70, 148, .4);
      background: rgba(3, 70, 148, .12);
    }

    .kb-warn {
      color: #ff5f3f;
      border-color: rgba(255, 95, 63, .35);
      background: rgba(255, 95, 63, .1);
    }

    .kb-good {
      color: #00ff85;
      border-color: rgba(0, 255, 133, .3);
      background: rgba(0, 255, 133, .08);
    }

    .kb-stat {
      color: var(--amber);
      border-color: rgba(247, 201, 72, .3);
      background: rgba(247, 201, 72, .08);
    }

    /* Form list */
    .form-cols {
      display: grid;
      grid-template-columns: 1fr 1fr;
      gap: 14px;
    }

    .form-team-lbl {
      display: flex;
      align-items: center;
      gap: 6px;
      font-family: 'Exo 2', sans-serif;
      font-size: 10px;
      font-weight: 700;
      letter-spacing: 1px;
      text-transform: uppercase;
      margin-bottom: 8px;
    }

    .form-badge-sm {
      width: 16px;
      height: 16px;
      object-fit: contain;
      border-radius: 50%;
      background: rgba(255, 255, 255, .05);
      flex-shrink: 0;
    }

    .fr-list {
      display: flex;
      flex-direction: column;
      gap: 3px;
    }

    .fr {
      display: grid;
      grid-template-columns: 8px 44px 1fr 60px;
      align-items: center;
      gap: 6px;
      background: var(--bg3);
      border: 1px solid var(--border);
      border-radius: 5px;
      padding: 5px 8px;
      transition: background .2s;
    }

    .fr:hover {
      background: var(--bg4);
    }

    .rdot {
      width: 8px;
      height: 8px;
      border-radius: 50%;
    }

    .rdot.W {
      background: var(--green);
      box-shadow: 0 0 5px rgba(15, 217, 162, .45);
    }

    .rdot.D {
      background: var(--amber);
    }

    .rdot.L {
      background: var(--red);
      box-shadow: 0 0 5px rgba(245, 82, 42, .45);
    }

    .f-sc {
      font-family: 'Exo 2', sans-serif;
      font-size: 14px;
      font-weight: 700;
      color: #fff;
      text-align: center;
    }

    .f-opp {
      font-size: 11.5px;
      color: var(--text);
      overflow: hidden;
      text-overflow: ellipsis;
      white-space: nowrap;
    }

    .f-comp {
      font-size: 9px;
      color: var(--muted);
      text-align: right;
      text-transform: uppercase;
      letter-spacing: .3px;
      white-space: nowrap;
    }

    .f-tag {
      font-size: 7.5px;
      padding: 1px 4px;
      border-radius: 2px;
      background: rgba(247, 201, 72, .1);
      color: var(--amber);
      font-family: 'Exo 2', sans-serif;
      font-weight: 700;
      border: 1px solid rgba(247, 201, 72, .25);
    }

    .form-legend {
      display: flex;
      gap: 10px;
      margin-top: 8px;
    }

    .fl {
      display: flex;
      align-items: center;
      gap: 4px;
      font-size: 10px;
      color: var(--muted);
    }

    .fld {
      width: 6px;
      height: 6px;
      border-radius: 50%;
    }

    /* H2H */
    .h2h-bar {
      display: grid;
      grid-template-columns: repeat(4, 1fr);
      gap: 4px;
      margin-bottom: 10px;
    }

    .hs {
      background: var(--bg3);
      border-radius: 7px;
      padding: 10px 5px;
      text-align: center;
      border: 1px solid var(--border);
    }

    .hn {
      font-family: 'Exo 2', sans-serif;
      font-size: 26px;
      font-weight: 800;
      line-height: 1;
    }

    .hl {
      font-size: 8.5px;
      color: var(--muted);
      text-transform: uppercase;
      letter-spacing: .5px;
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
      background: var(--bg3);
      border-radius: 5px;
      padding: 5px 8px;
      border: 1px solid var(--border);
      transition: background .2s;
    }

    .h2h-r:hover {
      background: var(--bg4);
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
      font-family: 'Exo 2', sans-serif;
      font-size: 14px;
      font-weight: 700;
      color: #fff;
      text-align: center;
      background: rgba(255, 255, 255, .06);
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
      grid-column: 1 / -1;
      margin-top: -2px;
      letter-spacing: .3px;
      text-transform: uppercase;
    }

    /* Season avgs */
    .avgs-pair {
      display: grid;
      grid-template-columns: 1fr 1fr;
      gap: 12px;
    }

    .avg-lbl {
      font-family: 'Exo 2', sans-serif;
      font-size: 9.5px;
      font-weight: 700;
      letter-spacing: 1px;
      text-transform: uppercase;
      margin-bottom: 7px;
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
      background: var(--bg3);
      border-radius: 6px;
      padding: 8px 4px;
      text-align: center;
      border: 1px solid var(--border);
      transition: background .2s, transform .2s;
    }

    .ac:hover {
      background: var(--bg4);
      transform: translateY(-1px);
    }

    .av {
      font-family: 'Exo 2', sans-serif;
      font-size: 18px;
      font-weight: 800;
      color: #fff;
      line-height: 1;
    }

    .al {
      font-size: 7.5px;
      color: var(--muted);
      margin-top: 2px;
      text-transform: uppercase;
      letter-spacing: .4px;
      line-height: 1.3;
    }

    /* xG row */
    .xg-row {
      display: flex;
      flex-wrap: wrap;
      gap: 8px;
      margin-top: 10px;
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

    /* Prediction table */
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
      background: var(--border2);
      border-radius: 2px;
    }

    .pred-table {
      width: 100%;
      border-collapse: collapse;
      min-width: 560px;
    }

    .pred-table thead th {
      font-family: 'Exo 2', sans-serif;
      font-size: 9px;
      font-weight: 700;
      letter-spacing: 1.5px;
      text-transform: uppercase;
      color: var(--muted);
      padding: 0 6px 10px;
      text-align: left;
      white-space: nowrap;
    }

    .pred-table thead th.tc {
      text-align: center;
    }

    .pred-table tbody td {
      padding: 7px 6px;
      border-bottom: 1px solid rgba(255, 255, 255, .03);
      vertical-align: middle;
    }

    .pred-table tbody tr:last-child td {
      border-bottom: none;
    }

    .pred-table tbody tr:hover td {
      background: rgba(255, 255, 255, .02);
    }

    .pred-table td.tn {
      color: var(--label);
      font-weight: 600;
      font-size: 12.5px;
      white-space: nowrap;
    }

    .pred-table td.tv {
      text-align: center;
    }

    .ts-cell {
      display: flex;
      flex-direction: column;
      align-items: center;
      gap: 1px;
    }

    .ts-v {
      font-family: 'Exo 2', sans-serif;
      font-size: 15px;
      font-weight: 700;
      line-height: 1;
    }

    .ts-l {
      font-size: 7.5px;
      color: var(--muted);
      text-transform: uppercase;
      letter-spacing: .3px;
    }

    .lv {
      font-family: 'Exo 2', sans-serif;
      font-size: 16px;
      font-weight: 700;
      color: var(--green);
    }

    .mv {
      font-family: 'Exo 2', sans-serif;
      font-size: 18px;
      font-weight: 800;
      color: var(--amber);
    }

    .hv {
      font-family: 'Exo 2', sans-serif;
      font-size: 16px;
      font-weight: 700;
      color: var(--red);
    }

    .rbar {
      flex: 1;
      min-width: 80px;
      height: 5px;
      background: rgba(255, 255, 255, .07);
      border-radius: 3px;
      overflow: hidden;
    }

    .rbf {
      height: 100%;
      border-radius: 3px;
      width: 0;
      transition: width 1.3s cubic-bezier(.25, .46, .45, .94);
    }

    /* Score cards */
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
      transition: border-color .3s, transform .3s;
    }

    .sbox:hover {
      transform: translateY(-2px);
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

    .sb-score.feat-s {
      color: var(--amber);
    }

    .sb-prob {
      font-size: 9.5px;
      color: var(--muted);
    }

    .sz-note {
      font-size: 12px;
      color: var(--label);
      line-height: 1.7;
      border-top: 1px solid var(--border);
      padding-top: 10px;
    }

    .sz-note strong {
      color: var(--amber);
      font-weight: 700;
    }

    .safe-box {
      background: linear-gradient(135deg, rgba(15, 217, 162, .07), rgba(15, 217, 162, .02));
      border: 1px solid rgba(15, 217, 162, .25);
      border-radius: 7px;
      padding: 10px 12px;
      font-size: 12px;
      color: var(--label);
      line-height: 1.7;
    }

    .safe-box strong {
      color: var(--green);
      font-weight: 700;
    }

    /* Yellow cards */
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
      transition: border-color .2s, transform .2s;
    }

    .yc-row:hover {
      border-color: rgba(255, 232, 74, .22);
      transform: translateX(2px);
    }

    .yc-ico {
      font-size: 15px;
      flex-shrink: 0;
      padding-top: 1px;
    }

    .yc-info {
      flex: 1;
      min-width: 0;
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
    }

    .yc-reason {
      font-size: 11px;
      color: var(--muted);
      margin-top: 2px;
      line-height: 1.5;
    }

    .risk-badge {
      font-family: 'Exo 2', sans-serif;
      font-size: 8.5px;
      font-weight: 700;
      letter-spacing: 1px;
      text-transform: uppercase;
      padding: 2px 8px;
      border-radius: 4px;
      flex-shrink: 0;
      align-self: center;
      border: 1px solid;
    }

    .rh {
      color: var(--red);
      border-color: rgba(245, 82, 42, .3);
      background: rgba(245, 82, 42, .1);
    }

    .rm {
      color: var(--amber);
      border-color: rgba(247, 201, 72, .3);
      background: rgba(247, 201, 72, .08);
    }

    /* Bet analysis */
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
      transition: border-color .2s;
    }

    .bet-cell:hover {
      border-color: var(--border2);
    }

    .bet-cell.bval {
      border-color: rgba(247, 201, 72, .38);
      background: linear-gradient(135deg, rgba(247, 201, 72, .07), var(--bg3));
    }

    .bet-cell.bwarn {
      border-color: rgba(245, 82, 42, .3);
      background: rgba(245, 82, 42, .06);
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

    .bc-line.vy {
      color: var(--amber);
    }

    .bc-line.vg {
      color: var(--green);
    }

    .bc-line.vr {
      color: var(--red);
    }

    .bc-rsn {
      font-size: 11px;
      color: var(--label);
      margin-top: 4px;
      line-height: 1.5;
    }

    .bet-note {
      font-size: 12px;
      color: var(--label);
      line-height: 1.7;
    }

    .bet-note strong {
      color: var(--amber);
    }

    /* Section sub-note */
    .s-note {
      font-size: 10.5px;
      color: var(--muted);
      margin-top: 8px;
      line-height: 1.55;
    }

    .s-note strong {
      color: var(--amber);
    }

    /* Inline note */
    .inline-note {
      background: var(--bg3);
      border-radius: 6px;
      padding: 10px 12px;
      border: 1px solid var(--border);
      font-size: 12px;
      color: var(--label);
      line-height: 1.7;
      margin-bottom: 7px;
    }

    .inline-note:last-child {
      margin-bottom: 0;
    }

    .inline-note strong {
      color: var(--amber);
    }

    /* ─── RESPONSIVE ─── */
    @media(min-width:640px) {
      body {
        font-size: 15px;
      }

      .badge-ring {
        width: 90px;
        height: 90px;
      }

      .badge-ring img,
      .badge-ring svg {
        width: 68px;
        height: 68px;
      }

      .team-name {
        font-size: 15px;
      }

      .card-body {
        padding: 16px 22px;
      }

      .card-hd {
        padding: 12px 22px 10px;
      }

      .form-cols {
        gap: 18px;
      }

      .av {
        font-size: 20px;
      }
    }

    @media(min-width:1100px) {
      .card-body {
        padding: 17px 24px;
      }

      .card-hd {
        padding: 13px 24px 11px;
      }

      .bet-grid {
        grid-template-columns: repeat(4, 1fr);
      }
    }

    @media(max-width:400px) {

      .form-cols,
      .avgs-pair {
        grid-template-columns: 1fr;
      }

      .h2h-bar {
        grid-template-columns: repeat(2, 1fr);
      }
    }
  </style>
</head>

<body>
  <div class="bg-layer"></div>

  <!-- PAGE HEADER -->
  <header class="page-hd">
    <div class="pl-badge"><h1><span style="color: var(--red);">Premier League</span><br> <span>Team Bilbo Analytics</span></h1></div>
    <h1><span style="color: var(--bha-blue);">BRIGHTON</span> <span style="color: var(--amber);">v</span> <span style="color: var(--che-blue);">CHELSEA</span></h1>
    <p class="sub">Statistical Match Prediction · American Express Stadium · 20:00 · Referee: Craig Pawson</p>
  </header>

  <div class="wrap">

    <!-- ═══════════ HERO ═══════════ -->
    <div class="hero-card">
      <div class="hero-inner">

        <div class="hero-meta">
          <span class="hm-chip" style="color:#60a5fa;border-color:rgba(0,87,184,.4);background:rgba(0,87,184,.12)">Amex
            Stadium · Brighton</span>
          <span class="hm-chip"
            style="color:var(--pl-green);border-color:rgba(0,255,133,.28);background:rgba(0,255,133,.07)">Brighton:
            European qualification hunt</span>
          <span class="hm-chip" style="color:#ff5f3f;border-color:rgba(255,95,63,.35);background:rgba(255,95,63,.09)">⚠
            Chelsea: 4 PL defeats · 0 goals scored</span>
        </div>

        <!-- Motivation -->
        <div class="mot-row" style="max-width:580px;width:100%">
          <span class="mot-lbl">🏠 Brighton</span>
          <div class="mot-track">
            <div class="mot-bar" id="mot-bha" style="width:0;background:linear-gradient(90deg,var(--bha-blue),#3b82f6)">
            </div>
          </div>
          <span class="mot-val" style="color:#60a5fa">87%</span>
          <span style="font-size:9px;color:var(--muted);padding:0 8px;white-space:nowrap">MOTIVATION</span>
          <div class="mot-track">
            <div class="mot-bar" id="mot-che"
              style="width:0;background:linear-gradient(90deg,var(--che-blue),var(--che-gold))"></div>
          </div>
          <span class="mot-val" style="color:#a5c4ff">82%</span>
          <span class="mot-lbl">Chelsea ✈️</span>
        </div>

        <!-- Teams -->
        <div class="teams-row">
          <div class="team-col">
            <div class="badge-ring" style="animation-delay:.05s">
              <img src="https://cdn.cdnlogo.com/logos/b/32/brighton-hove-albion.svg"
                onerror="this.onerror=null;this.src='https://upload.wikimedia.org/wikipedia/en/thumb/f/fd/Brighton_%26_Hove_Albion_logo.svg/120px-Brighton_%26_Hove_Albion_logo.svg.png'"
                alt="Brighton">
            </div>
            <div class="team-name" style="color:#60a5fa">Brighton</div>
            <div class="team-meta">9th · ~46 pts<br>Unbeaten last 7 PL<br>W3 H2H vs Chelsea in a row</div>
          </div>
          <div class="vs-col">
            <div class="vs-txt">VS</div>
            <div class="ko-tag">20:00</div>
            <div class="venue-txt">Amex Stadium · Brighton<br>~31,800 capacity<br>Tue 21 Apr 2026</div>
          </div>
          <div class="team-col">
            <div class="badge-ring" style="animation-delay:.12s">
              <img src="https://cdn.cdnlogo.com/logos/c/8/chelsea-fc.svg"
                onerror="this.onerror=null;this.src='https://upload.wikimedia.org/wikipedia/en/thumb/c/cc/Chelsea_FC.svg/120px-Chelsea_FC.svg.png'"
                alt="Chelsea">
            </div>
            <div class="team-name" style="color:#a5c4ff">Chelsea FC</div>
            <div class="team-meta">6th · ~48 pts · 1pt ahead<br>4 PL losses in a row (0 goals)<br>FA Cup SF vs Leeds on
              Sat</div>
          </div>
        </div>

        <!-- Odds -->
        <div class="odds-row">
          <div class="odds-box ob-val">
            <div class="ob-lbl">★ Brighton Win</div>
            <div class="ob-odds" style="color:#60a5fa">7/5</div>
            <div class="ob-impl">~42% implied · Value</div>
          </div>
          <div class="odds-box">
            <div class="ob-lbl">Draw</div>
            <div class="ob-odds" style="color:var(--amber)">13/5</div>
            <div class="ob-impl">~28% implied</div>
          </div>
          <div class="odds-box">
            <div class="ob-lbl">Chelsea Win</div>
            <div class="ob-odds" style="color:#a5c4ff">13/8</div>
            <div class="ob-impl">~38% implied</div>
          </div>
          <div class="odds-box"
            style="border-color:rgba(15,217,162,.3);background:linear-gradient(135deg,rgba(15,217,162,.06),var(--bg3))">
            <div class="ob-lbl">Over 2.5 Goals</div>
            <div class="ob-odds" style="color:var(--green)">10/11</div>
            <div class="ob-impl">~52% implied</div>
          </div>
        </div>

      </div>
    </div>

    <!-- ═══════════ GRID ═══════════ -->
    <div class="grid">

      <!-- CONTEXT & STAKES -->
      <div class="card span2" style="animation-delay:.06s">
        <div class="card-hd">
          <div class="hd-dot" style="background:var(--amber)"></div>
          <div class="hd-title">Match Context · Stakes · Motivation Analysis</div>
          <div class="hd-tag" style="color:var(--red);border-color:rgba(245,82,42,.3);background:rgba(245,82,42,.09)">
            European Race Both Sides</div>
        </div>
        <div class="card-body">
          <div class="ctx">
            <span class="key-badge kb-bha">Brighton</span>
            9th place, ~46 pts — just <strong>1 point below Chelsea in 6th</strong>. A Brighton win propels them above
            Chelsea and into the European places. They've won <strong>W5 from last 7 PL games</strong>, beat Liverpool
            2-1 at the Amex recently, and came back from 2-0 down at Spurs for a 2-2 draw showing resilience and spirit.
            Danny Welbeck (age 35, 12 PL goals) is enjoying one of the finest seasons of his career. Fabian Hürzeler has
            rebuilt Brighton after losing Caicedo, Saliba and Gilmour to bigger clubs. Their defensive record is
            exceptional — only City, Arsenal and Palace concede fewer. Dunk returns from suspension to anchor the back
            line.
            <br><br>
            <span class="key-badge kb-che">Chelsea</span>
            6th, ~48 pts — but <strong>only 1 point ahead of Brighton, with Europe (and potentially Champions League via
              6th if Aston Villa win UEL) on the line</strong>. Chelsea's crisis is historic. <strong>4 consecutive PL
              defeats, 0 goals scored</strong>. They haven't scored a PL goal in over 360 minutes (6+ weeks). The last
            time they suffered 5 scoreless consecutive PL defeats was <strong>1912</strong>. Their xG was 1.57 vs Man
            United with 21 shots — yet still couldn't convert. <strong>Injuries:</strong> Estevao (hamstring — out),
            Reece James (thigh), Levi Colwill (ACL — long term), Gittens (hamstring), Jorgensen (GK — injury). João
            Pedro is <strong>doubtful with a thigh issue</strong> but may feature at his former club. <span
              class="key-badge kb-stat">⚠ FA Cup SF vs Leeds on Saturday</span> — some rotation risk for Chelsea.
            <br><br>
            <span class="key-badge kb-warn">Key Stat</span> Brighton have won <strong>W3 consecutive H2H</strong> vs
            Chelsea, including a 3-1 away win at Stamford Bridge in September 2025. Chelsea have <strong>not kept a
              clean sheet in 11 consecutive PL games</strong>. Over 2.5 goals in <strong>9 of the last 10</strong>
            Brighton-Chelsea meetings. This is a must-win for both but Brighton come in with immeasurably superior
            recent form.
          </div>
        </div>
      </div>

      <!-- LAST 5 FORM -->
      <div class="card" style="animation-delay:.09s">
        <div class="card-hd">
          <div class="hd-dot" style="background:#60a5fa"></div>
          <div class="hd-title">Last 5 Matches — All Competitions</div>
        </div>
        <div class="card-body">
          <div class="form-cols">
            <div>
              <div class="form-team-lbl" style="color:#60a5fa">
                <img class="form-badge-sm"
                  src="https://upload.wikimedia.org/wikipedia/en/thumb/f/fd/Brighton_%26_Hove_Albion_logo.svg/120px-Brighton_%26_Hove_Albion_logo.svg.png"
                  alt="">
                Brighton
              </div>
              <div class="fr-list">
                <div class="fr">
                  <div class="rdot D"></div>
                  <div class="f-sc">2–2</div>
                  <div class="f-opp">Tottenham</div>
                  <div class="f-comp">PL Away</div>
                </div>
                <div class="fr">
                  <div class="rdot W"></div>
                  <div class="f-sc">1–0</div>
                  <div class="f-opp">Sunderland</div>
                  <div class="f-comp">PL Away</div>
                </div>
                <div class="fr">
                  <div class="rdot W"></div>
                  <div class="f-sc">2–1</div>
                  <div class="f-opp">Liverpool</div>
                  <div class="f-comp">PL Home</div>
                </div>
                <div class="fr">
                  <div class="rdot W"></div>
                  <div class="f-sc">2–0</div>
                  <div class="f-opp">Burnley</div>
                  <div class="f-comp">PL Away</div>
                </div>
                <div class="fr">
                  <div class="rdot L"></div>
                  <div class="f-sc">0–1</div>
                  <div class="f-opp">Arsenal</div>
                  <div class="f-comp">PL Away</div>
                </div>
              </div>
            </div>
            <div>
              <div class="form-team-lbl" style="color:#a5c4ff">
                <img class="form-badge-sm"
                  src="https://upload.wikimedia.org/wikipedia/en/thumb/c/cc/Chelsea_FC.svg/120px-Chelsea_FC.svg.png"
                  alt="">
                Chelsea
              </div>
              <div class="fr-list">
                <div class="fr">
                  <div class="rdot L"></div>
                  <div class="f-sc">0–1</div>
                  <div class="f-opp">Man United</div>
                  <div class="f-comp">PL Home</div>
                </div>
                <div class="fr">
                  <div class="rdot W"></div>
                  <div class="f-sc">7–0</div>
                  <div class="f-opp">Port Vale</div>
                  <div class="f-comp">FAC <span class="f-tag">L1 opp</span></div>
                </div>
                <div class="fr">
                  <div class="rdot L"></div>
                  <div class="f-sc">0–3</div>
                  <div class="f-opp">Everton</div>
                  <div class="f-comp">PL Away</div>
                </div>
                <div class="fr">
                  <div class="rdot L"></div>
                  <div class="f-sc">0–3</div>
                  <div class="f-opp">Man City</div>
                  <div class="f-comp">PL Away</div>
                </div>
                <div class="fr">
                  <div class="rdot L"></div>
                  <div class="f-sc">0–1</div>
                  <div class="f-opp">Newcastle</div>
                  <div class="f-comp">PL Home</div>
                </div>
              </div>
            </div>
          </div>
          <div class="form-legend">
            <div class="fl">
              <div class="fld" style="background:var(--green)"></div>Win
            </div>
            <div class="fl">
              <div class="fld" style="background:var(--amber)"></div>Draw
            </div>
            <div class="fl">
              <div class="fld" style="background:var(--red)"></div>Loss
            </div>
          </div>
          <div class="s-note"><strong>Trend:</strong> Brighton: 1 defeat in last 7 PL (vs Arsenal, 1-0). Chelsea: 4 PL
            defeats in a row, 0 goals scored, 8 goals conceded. Their only goal in 5 games was a 7-0 vs League One Port
            Vale.</div>
        </div>
      </div>

      <!-- H2H -->
      <div class="card" style="animation-delay:.11s">
        <div class="card-hd">
          <div class="hd-dot" style="background:var(--red)"></div>
          <div class="hd-title">Head to Head — Last 5 Meetings</div>
          <div class="hd-tag"
            style="color:var(--green);border-color:rgba(15,217,162,.3);background:rgba(15,217,162,.07)">O2.5 goals in 9
            of last 10 H2H</div>
        </div>
        <div class="card-body">
          <div class="h2h-bar">
            <div class="hs">
              <div class="hn" style="color:#60a5fa">3</div>
              <div class="hl">Brighton W</div>
            </div>
            <div class="hs">
              <div class="hn" style="color:var(--amber)">0</div>
              <div class="hl">Draws</div>
            </div>
            <div class="hs">
              <div class="hn" style="color:#a5c4ff">2</div>
              <div class="hl">Chelsea W</div>
            </div>
            <div class="hs">
              <div class="hn">3.6</div>
              <div class="hl">Avg Goals</div>
            </div>
          </div>
          <div class="h2h-rows">
            <div class="h2h-r">
              <div class="rh">Chelsea</div>
              <div class="rs">1–3</div>
              <div class="ra">Brighton</div>
              <div class="rx">PL Sep 2025 · Stamford Bridge (3 late goals / Chalobah red)</div>
            </div>
            <div class="h2h-r">
              <div class="rh">Brighton</div>
              <div class="rs">3–2</div>
              <div class="ra">Chelsea</div>
              <div class="rx">PL Feb 2025 · Amex Stadium</div>
            </div>
            <div class="h2h-r">
              <div class="rh">Chelsea</div>
              <div class="rs">2–1</div>
              <div class="ra">Brighton</div>
              <div class="rx">PL Oct 2024 · Stamford Bridge</div>
            </div>
            <div class="h2h-r">
              <div class="rh">Brighton</div>
              <div class="rs">2–1</div>
              <div class="ra">Chelsea</div>
              <div class="rx">FAC Feb 2025 · Stamford Bridge</div>
            </div>
            <div class="h2h-r">
              <div class="rh">Chelsea</div>
              <div class="rs">1–2</div>
              <div class="ra">Brighton</div>
              <div class="rx">PL May 2024 · Stamford Bridge</div>
            </div>
          </div>
          <div class="s-note"><strong>Key H2H facts:</strong> Brighton have won last 3 in all comps (never done league
            double over Chelsea before — first time in 2022/23). Danny Welbeck: 5 goals + 2 assists in his last 8 PL
            games vs Chelsea. Cole Palmer: 5 goals in 3 PL H2H. Brighton have scored 3 goals in each of the last two
            meetings. 9 of last 10 meetings had 3+ goals.</div>
        </div>
      </div>

      <!-- SEASON AVERAGES -->
      <div class="card" style="animation-delay:.13s">
        <div class="card-hd">
          <div class="hd-dot" style="background:var(--purple)"></div>
          <div class="hd-title">Season Averages — PL 2025/26</div>
        </div>
        <div class="card-body">
          <div class="avgs-pair">
            <div>
              <div class="avg-lbl" style="color:#fff;background:rgba(0,87,184,.18);border:1px solid rgba(0,87,184,.35)">
                Brighton</div>
              <div class="avg-cells">
                <div class="ac">
                  <div class="av">11.4</div>
                  <div class="al">Shots/gm</div>
                </div>
                <div class="ac">
                  <div class="av">4.4</div>
                  <div class="al">SOT/gm</div>
                </div>
                <div class="ac">
                  <div class="av">3.9</div>
                  <div class="al">Corners/gm</div>
                </div>
                <div class="ac">
                  <div class="av">5.6</div>
                  <div class="al">Corners vs</div>
                </div>
                <div class="ac">
                  <div class="av">1.2</div>
                  <div class="al">Gls/gm</div>
                </div>
                <div class="ac">
                  <div class="av">53%</div>
                  <div class="al">Poss</div>
                </div>
              </div>
            </div>
            <div>
              <div class="avg-lbl" style="color:#fff;background:rgba(3,70,148,.18);border:1px solid rgba(3,70,148,.35)">
                Chelsea</div>
              <div class="avg-cells">
                <div class="ac">
                  <div class="av">15.3</div>
                  <div class="al">Shots/gm</div>
                </div>
                <div class="ac">
                  <div class="av">4.2</div>
                  <div class="al">SOT/gm</div>
                </div>
                <div class="ac">
                  <div class="av">7.2</div>
                  <div class="al">Corners (away)</div>
                </div>
                <div class="ac">
                  <div class="av">3.7</div>
                  <div class="al">Corners vs</div>
                </div>
                <div class="ac">
                  <div class="av">1.4</div>
                  <div class="al">Gls/gm</div>
                </div>
                <div class="ac">
                  <div class="av">61%</div>
                  <div class="al">Poss</div>
                </div>
              </div>
            </div>
          </div>
          <div class="xg-row">
            <div class="xg-item">
              <div class="xg-v" style="color:#60a5fa">1.08</div>
              <div class="xg-l">Brighton xG/gm</div>
            </div>
            <div class="xg-item">
              <div class="xg-v" style="color:#ff9980">0.87</div>
              <div class="xg-l">Brighton xG vs Spurs</div>
            </div>
            <div class="xg-item">
              <div class="xg-v" style="color:#a5c4ff">1.57</div>
              <div class="xg-l">Chelsea xG vs Man Utd</div>
            </div>
            <div class="xg-item">
              <div class="xg-v" style="color:var(--red)">0</div>
              <div class="xg-l">Chelsea PL goals (4 gms)</div>
            </div>
            <div class="xg-item">
              <div class="xg-v" style="color:var(--green)">11</div>
              <div class="xg-l">Chelsea clean sheets ago</div>
            </div>
          </div>
          <div class="s-note"><strong>xG tells a damning story for Chelsea:</strong> They're creating chances (21 shots,
            1.57 xG vs Man Utd) but finishing has completely dried up. Brighton are efficient — xG ~1.08/game, only
            conceded 0.8 goals/game in last 10. Chelsea awarded most corners in 6 straight away PL games (7.2/gm away
            avg) — highest in the league.</div>
        </div>
      </div>

      <!-- HOME/AWAY SPLITS -->
      <div class="card" style="animation-delay:.15s">
        <div class="card-hd">
          <div class="hd-dot" style="background:var(--green)"></div>
          <div class="hd-title">Home / Away Performance Splits</div>
        </div>
        <div class="card-body">
          <div class="avgs-pair">
            <div>
              <div class="avg-lbl" style="color:#fff;background:rgba(0,87,184,.18);border:1px solid rgba(0,87,184,.35)">
                Brighton @ Home</div>
              <div class="avg-cells">
                <div class="ac">
                  <div class="av">7</div>
                  <div class="al">Home Wins</div>
                </div>
                <div class="ac">
                  <div class="av">5.0</div>
                  <div class="al">Corners/gm</div>
                </div>
                <div class="ac">
                  <div class="av">0.8</div>
                  <div class="al">Goals conceded</div>
                </div>
                <div class="ac">
                  <div class="av">2</div>
                  <div class="al">Home defeats (narrow)</div>
                </div>
                <div class="ac">
                  <div class="av">3</div>
                  <div class="al">H2H home wins vs CHE</div>
                </div>
                <div class="ac">
                  <div class="av">6</div>
                  <div class="al">Home draws</div>
                </div>
              </div>
            </div>
            <div>
              <div class="avg-lbl" style="color:#fff;background:rgba(3,70,148,.18);border:1px solid rgba(3,70,148,.35)">
                Chelsea Away</div>
              <div class="avg-cells">
                <div class="ac">
                  <div class="av">3</div>
                  <div class="al">Away Wins (since Dec)</div>
                </div>
                <div class="ac">
                  <div class="av">7.2</div>
                  <div class="al">Corners away</div>
                </div>
                <div class="ac">
                  <div class="av">1.7</div>
                  <div class="al">Goals conceded</div>
                </div>
                <div class="ac">
                  <div class="av">8</div>
                  <div class="al">Goals conceded last 2 away</div>
                </div>
                <div class="ac">
                  <div class="av">59%</div>
                  <div class="al">Poss away</div>
                </div>
                <div class="ac">
                  <div class="av">0</div>
                  <div class="al">Clean sheets (11 gms)</div>
                </div>
              </div>
            </div>
          </div>
          <div class="s-note">Brighton have conceded only <strong>2 narrow 1-0 home defeats</strong> this season — both
            one-goal losses, showing defensive solidity. Chelsea's away form has dramatically deteriorated (8 goals
            conceded in last 2 away games). Chelsea's corner volume away (7.2/gm) is the highest in the league but that
            is partly because they trail in games and press late — not necessarily a sign of dominance.</div>
        </div>
      </div>

      <!-- WEIGHTED PREDICTIONS -->
      <div class="card span2" style="animation-delay:.17s">
        <div class="card-hd">
          <div class="hd-dot" style="background:var(--green)"></div>
          <div class="hd-title">Weighted Stat Predictions — Brighton vs Chelsea</div>
        </div>
        <div class="card-body">
          <div class="pt-intro">
            <div class="pt-key">
              <div style="width:8px;height:8px;border-radius:50%;background:var(--green)"></div><span
                style="color:var(--green);font-weight:700">Low (floor)</span>
            </div>
            <div class="pt-key">
              <div style="width:8px;height:8px;border-radius:50%;background:var(--amber)"></div><span
                style="color:var(--amber);font-weight:700">Median (weighted)</span>
            </div>
            <div class="pt-key">
              <div style="width:8px;height:8px;border-radius:50%;background:var(--red)"></div><span
                style="color:var(--red);font-weight:700">High (ceiling)</span>
            </div>
          </div>
          <div class="ptw">
            <table class="pred-table">
              <colgroup>
                <col style="width:22%">
                <col style="width:14%">
                <col style="width:14%">
                <col style="width:10%">
                <col style="width:12%">
                <col style="width:10%">
                <col style="width:18%">
              </colgroup>
              <thead>
                <tr>
                  <th>Metric</th>
                  <th class="tc" style="color:#60a5fa">Brighton</th>
                  <th class="tc" style="color:#a5c4ff">Chelsea</th>
                  <th class="tc" style="color:var(--green)">Low</th>
                  <th class="tc" style="color:var(--amber)">Median</th>
                  <th class="tc" style="color:var(--red)">High</th>
                  <th class="tc" style="color:var(--muted)">Intensity Bar</th>
                </tr>
              </thead>
              <tbody>
                <tr>
                  <td class="tn">🔲 Corners</td>
                  <td class="tv">
                    <div class="ts-cell"><span class="ts-v" style="color:#60a5fa">5</span><span class="ts-l">med
                        (home)</span></div>
                  </td>
                  <td class="tv">
                    <div class="ts-cell"><span class="ts-v" style="color:#a5c4ff">6</span><span class="ts-l">med
                        (away)</span></div>
                  </td>
                  <td class="tv"><span class="lv">7</span></td>
                  <td class="tv"><span class="mv">11</span></td>
                  <td class="tv"><span class="hv">17</span></td>
                  <td>
                    <div class="rbar">
                      <div class="rbf" data-p="66" style="background:linear-gradient(90deg,#0057b8,#034694)"></div>
                    </div>
                  </td>
                </tr>
                <tr>
                  <td class="tn">📊 Total Shots</td>
                  <td class="tv">
                    <div class="ts-cell"><span class="ts-v" style="color:#60a5fa">12</span><span class="ts-l">med</span>
                    </div>
                  </td>
                  <td class="tv">
                    <div class="ts-cell"><span class="ts-v" style="color:#a5c4ff">13</span><span class="ts-l">med</span>
                    </div>
                  </td>
                  <td class="tv"><span class="lv">18</span></td>
                  <td class="tv"><span class="mv">26</span></td>
                  <td class="tv"><span class="hv">36</span></td>
                  <td>
                    <div class="rbar">
                      <div class="rbf" data-p="72" style="background:linear-gradient(90deg,#0057b8,#034694)"></div>
                    </div>
                  </td>
                </tr>
                <tr>
                  <td class="tn">🎯 SOT</td>
                  <td class="tv">
                    <div class="ts-cell"><span class="ts-v" style="color:#60a5fa">5</span><span class="ts-l">med</span>
                    </div>
                  </td>
                  <td class="tv">
                    <div class="ts-cell"><span class="ts-v" style="color:#a5c4ff">4</span><span class="ts-l">med</span>
                    </div>
                  </td>
                  <td class="tv"><span class="lv">6</span></td>
                  <td class="tv"><span class="mv">9</span></td>
                  <td class="tv"><span class="hv">15</span></td>
                  <td>
                    <div class="rbar">
                      <div class="rbf" data-p="60" style="background:linear-gradient(90deg,#0057b8,#034694)"></div>
                    </div>
                  </td>
                </tr>
                <tr>
                  <td class="tn">⚠️ Fouls</td>
                  <td class="tv">
                    <div class="ts-cell"><span class="ts-v" style="color:#60a5fa">11</span><span class="ts-l">med</span>
                    </div>
                  </td>
                  <td class="tv">
                    <div class="ts-cell"><span class="ts-v" style="color:#a5c4ff">12</span><span class="ts-l">med</span>
                    </div>
                  </td>
                  <td class="tv"><span class="lv">17</span></td>
                  <td class="tv"><span class="mv">23</span></td>
                  <td class="tv"><span class="hv">34</span></td>
                  <td>
                    <div class="rbar">
                      <div class="rbf" data-p="70" style="background:linear-gradient(90deg,#0057b8,#034694)"></div>
                    </div>
                  </td>
                </tr>
                <tr>
                  <td class="tn">↗️ Throw-ins</td>
                  <td class="tv">
                    <div class="ts-cell"><span class="ts-v" style="color:#60a5fa">20</span><span class="ts-l">med</span>
                    </div>
                  </td>
                  <td class="tv">
                    <div class="ts-cell"><span class="ts-v" style="color:#a5c4ff">19</span><span class="ts-l">med</span>
                    </div>
                  </td>
                  <td class="tv"><span class="lv">28</span></td>
                  <td class="tv"><span class="mv">39</span></td>
                  <td class="tv"><span class="hv">52</span></td>
                  <td>
                    <div class="rbar">
                      <div class="rbf" data-p="62" style="background:linear-gradient(90deg,#0057b8,#034694)"></div>
                    </div>
                  </td>
                </tr>
                <tr>
                  <td class="tn">🥅 Goal Kicks</td>
                  <td class="tv">
                    <div class="ts-cell"><span class="ts-v" style="color:#60a5fa">9</span><span class="ts-l">med</span>
                    </div>
                  </td>
                  <td class="tv">
                    <div class="ts-cell"><span class="ts-v" style="color:#a5c4ff">9</span><span class="ts-l">med</span>
                    </div>
                  </td>
                  <td class="tv"><span class="lv">13</span></td>
                  <td class="tv"><span class="mv">18</span></td>
                  <td class="tv"><span class="hv">26</span></td>
                  <td>
                    <div class="rbar">
                      <div class="rbf" data-p="56" style="background:linear-gradient(90deg,#0057b8,#034694)"></div>
                    </div>
                  </td>
                </tr>
                <tr>
                  <td class="tn">⚔️ Tackles</td>
                  <td class="tv">
                    <div class="ts-cell"><span class="ts-v" style="color:#60a5fa">14</span><span class="ts-l">med</span>
                    </div>
                  </td>
                  <td class="tv">
                    <div class="ts-cell"><span class="ts-v" style="color:#a5c4ff">14</span><span class="ts-l">med</span>
                    </div>
                  </td>
                  <td class="tv"><span class="lv">22</span></td>
                  <td class="tv"><span class="mv">28</span></td>
                  <td class="tv"><span class="hv">40</span></td>
                  <td>
                    <div class="rbar">
                      <div class="rbf" data-p="64" style="background:linear-gradient(90deg,#0057b8,#034694)"></div>
                    </div>
                  </td>
                </tr>
              </tbody>
            </table>
          </div>
          <div class="s-note" style="margin-top:10px">
            <strong>Corners note:</strong> Chelsea average 7.2 corners/game away — highest in PL — but this partially
            reflects their habit of playing from behind and pressing late. Brighton avg 5.0/gm at Amex. Combined median
            11 is elevated above both teams' averages because of Chelsea's high away corner rate.
            <strong>Fouls:</strong> Both Brighton and Chelsea are among the top 4 in the PL bookings chart — Craig
            Pawson is strict, making 23 the weighted median. <strong>Tackles:</strong> Brighton press high and Chelsea
            chase the game = both teams generating high tackle counts.
          </div>
        </div>
      </div>

      <!-- SCORE PREDICTION -->
      <div class="card" style="animation-delay:.19s">
        <div class="card-hd">
          <div class="hd-dot" style="background:var(--amber)"></div>
          <div class="hd-title">Score Prediction · Probability Analysis</div>
        </div>
        <div class="card-body">
          <div class="score-zone">
            <div class="sz-head">Brighton vs Chelsea · Amex Stadium</div>
            <div class="s-boxes">
              <div class="sbox">
                <div class="sb-lbl">Half-Time</div>
                <div class="sb-score">1–0</div>
                <div class="sb-prob">Brighton ~38%</div>
              </div>
              <div class="sbox feat">
                <div class="sb-lbl">Full-Time ★ Best Pick</div>
                <div class="sb-score feat-s">2–1</div>
                <div class="sb-prob">Brighton ~26% · Value at 7/5</div>
              </div>
              <div class="sbox">
                <div class="sb-lbl">Alt: Chelsea Score</div>
                <div class="sb-score">1–1</div>
                <div class="sb-prob">Draw ~21%</div>
              </div>
            </div>
            <div class="sz-note">
              <strong>Why Brighton 2-1:</strong> Brighton are one of the Premier League's best home teams right now —
              beat Liverpool and drew vs Spurs in recent home games. They've won W3 consecutive H2H vs Chelsea, scoring
              exactly 3 goals in each of the last two meetings. <strong>Chelsea can't stop conceding</strong> (11 games
              without a clean sheet) and their attack is misfiring — but the 9 of 10 H2H producing 3+ goals tells you
              Chelsea always contribute. Welbeck (12 PL goals, 5 vs Chelsea) is the standout danger. Cole Palmer (5
              goals in 3 PL vs Brighton) is Chelsea's only hope of breaking through. The Chelsea xG (1.57 vs Man Utd
              with 21 shots, still lost) shows they ARE creating chances — they just can't convert. <strong>Expect
                Chelsea to score once, Brighton to outscore them.</strong>
            </div>
            <div class="safe-box">
              <strong>🛡️ Safe Prediction — Brighton to Win &amp; Under 4.5 Goals (7/5)</strong><br>
              This combination is backed by: Brighton's superior form (unbeaten last 7), their 3-game winning streak vs
              Chelsea, home advantage, Chelsea's scoring drought, and both teams' tendency to play games with 2-3 goals
              (not goal fests). Brighton's 11 other league wins all featured under 3.5 goals. The Racing Post
              recommended this exact combination. <strong>BTTS Yes is also statistically strong</strong> — 8 of 9 recent
              H2H, and Chelsea's xG suggests they will eventually break through their drought.
            </div>
          </div>
        </div>
      </div>

      <!-- YELLOW CARDS -->
      <div class="card" style="animation-delay:.21s">
        <div class="card-hd">
          <div class="hd-dot" style="background:#ffe84a"></div>
          <div class="hd-title">🟨 Yellow Card Risk Players</div>
          <div class="hd-tag"
            style="color:var(--amber);border-color:rgba(247,201,72,.3);background:rgba(247,201,72,.07)">Craig Pawson —
            Strict Referee</div>
        </div>
        <div class="card-body">
          <div class="yc-list">
            <div class="yc-row">
              <div class="yc-ico">🟨</div>
              <div class="yc-info">
                <div class="yc-name">Mats Wieffer <span class="yc-club" style="color:#60a5fa">Brighton · DM</span></div>
                <div class="yc-reason">Identified by Racing Post as the standout yellow card pick. Both teams among top
                  4 in PL bookings chart. Wieffer's aggressive defensive midfield role vs Chelsea's high possession =
                  tactical fouls. He scored twice vs Spurs which shows his box-to-box involvement creates foul
                  situations.</div>
              </div>
              <div class="risk-badge rh">HIGH</div>
            </div>
            <div class="yc-row">
              <div class="yc-ico">🟨</div>
              <div class="yc-info">
                <div class="yc-name">Moisés Caicedo <span class="yc-club" style="color:#a5c4ff">Chelsea · DM</span>
                </div>
                <div class="yc-reason">Chelsea's combative DM who fouls as a tactical tool. Against a Brighton side
                  pressing intensely, Caicedo will commit holding fouls in the first half to slow Brighton's build-up.
                  He's accumulated 6 PL yellows this season and is Chelsea's most penalised player.</div>
              </div>
              <div class="risk-badge rh">HIGH</div>
            </div>
            <div class="yc-row">
              <div class="yc-ico">🟨</div>
              <div class="yc-info">
                <div class="yc-name">Marc Cucurella <span class="yc-club" style="color:#a5c4ff">Chelsea · LB</span>
                </div>
                <div class="yc-reason">Faces Yankuba Minteh (Brighton's electric right-winger) all night. Cucurella has
                  been penalised heavily this season when beaten 1v1. Chelsea's increasingly desperate play in a losing
                  position will force him into cynical challenges.</div>
              </div>
              <div class="risk-badge rm">MED</div>
            </div>
            <div class="yc-row">
              <div class="yc-ico">🟨</div>
              <div class="yc-info">
                <div class="yc-name">Ferdi Kadıoğlu <span class="yc-club" style="color:#60a5fa">Brighton · LB</span>
                </div>
                <div class="yc-reason">Brighton's left-back who competes physically against Chelsea's right-side
                  attacks. Active in duels when pressed. Brighton's physical style under Hürzeler creates bookings
                  through pressing — Kadıoğlu leads this from the back.</div>
              </div>
              <div class="risk-badge rm">MED</div>
            </div>
            <div class="yc-row">
              <div class="yc-ico">🟨</div>
              <div class="yc-info">
                <div class="yc-name">Romeo Lavia <span class="yc-club" style="color:#a5c4ff">Chelsea · DM</span></div>
                <div class="yc-reason">Chelsea's second DM who uses physicality when Chelsea are under pressure.
                  Pawson's strict standards in midfield duels means Lavia's tackling style draws cards. He and Caicedo
                  together make Chelsea's midfield very yellow-prone away from home.</div>
              </div>
              <div class="risk-badge rm">MED</div>
            </div>
          </div>
        </div>
      </div>

      <!-- BETTING ANALYSIS -->
      <div class="card span2" style="animation-delay:.23s">
        <div class="card-hd">
          <div class="hd-dot" style="background:var(--green)"></div>
          <div class="hd-title">📈 Betting Market Analysis · Value Picks · Pattern Recognition</div>
        </div>
        <div class="card-body">
          <div class="bet-grid">
            <div class="bet-cell bval">
              <div class="bc-mkt">★ Best Value Pick</div>
              <div class="bc-line vy">Brighton Win 7/5</div>
              <div class="bc-rsn">Won W3 straight H2H. Unbeaten 7 PL games. Home. Chelsea 4 PL losses in a row. Market
                42% implied — actual probability closer to 52-55%.</div>
            </div>
            <div class="bet-cell bval">
              <div class="bc-mkt">★ Combo Play</div>
              <div class="bc-line vg">Brighton Win &amp; U4.5</div>
              <div class="bc-rsn">Brighton's 11 other wins all saw under 3.5 goals. Racing Post recommended. Balances
                goal risk while capturing Brighton's dominance. ~2/1 for combo.</div>
            </div>
            <div class="bet-cell bval">
              <div class="bc-mkt">Goals Market</div>
              <div class="bc-line vg">BTTS Yes ~7/10</div>
              <div class="bc-rsn">8 of last 9 H2H both teams scored. Chelsea xG 1.57 vs Man Utd (21 shots!) — drought
                must end. Brighton concede too. Statistically near-certain.</div>
            </div>
            <div class="bet-cell">
              <div class="bc-mkt">Corners Market</div>
              <div class="bc-line vy">Chelsea Corner Handicap</div>
              <div class="bc-rsn">Chelsea avg 7.2 corners/away game — highest in PL. 10 of 11 recent games Chelsea made
                more passes from corners. Corner Match Bet +106 (Chelsea to win).</div>
            </div>
            <div class="bet-cell">
              <div class="bc-mkt">Player Props</div>
              <div class="bc-line">Welbeck To Score</div>
              <div class="bc-rsn">13/8 per Football365. 12 PL goals, 5 vs Chelsea. 7 goal involvements in 8 PL H2H
                games. Age 35 but genuinely unstoppable right now. Very strong value.</div>
            </div>
            <div class="bet-cell">
              <div class="bc-mkt">Player Props</div>
              <div class="bc-line">Cole Palmer O2.5 Shots</div>
              <div class="bc-rsn">5 goals in 3 PL vs Brighton (2 goals per game). Has O2.5 shots in 7 of last 10 PL
                games. +120 available. Despite form slump, Brighton fixture historically ignites Palmer.</div>
            </div>
            <div class="bet-cell bwarn">
              <div class="bc-mkt">⚠️ Caution</div>
              <div class="bc-line vr">Chelsea to Win</div>
              <div class="bc-rsn">13/8 looks attractive but Chelsea haven't won a PL away game since Dec. 4 scoreless
                defeats. Away vs in-form Brighton = very risky. Avoid unless high risk tolerance.</div>
            </div>
            <div class="bet-cell bwarn">
              <div class="bc-mkt">⚠️ Note</div>
              <div class="bc-line vr">Chelsea Not to Score</div>
              <div class="bc-rsn">Appealing at 4/10 given scoring drought — but their xG (1.57 vs Man Utd) and Palmer's
                H2H record vs Brighton means this is higher variance than the odds suggest.</div>
            </div>
          </div>
          <div class="bet-note">
            <strong>Overall Market Assessment:</strong> The odds have Brighton at 7/5 (~42% implied). Our weighted
            analysis places Brighton's actual win probability at <strong>52-55%</strong> based on: form differential
            (unbeaten 7 vs 4 PL losses), H2H (W3 in a row), home advantage at Amex (only 2 narrow defeats all season at
            home), Chelsea's catastrophic scoring drought (0 PL goals in 4 games), and Chelsea's key injury absences.
            <strong>The BTTS Yes market also carries exceptional statistical weight</strong> — 8 of last 9
            Brighton-Chelsea meetings saw both teams score, and Chelsea's xG data (1.57 vs Man Utd, 21 shots) shows they
            ARE creating chances and are due to score eventually. The 9 of 10 H2H producing 3+ goals supports BTTS +
            over 2.5, though Brighton's defensive record (0.8 goals conceded at home) tempers the ceiling. <strong>Smart
              bankroll allocation: 70% on Brighton Win, 20% on BTTS Yes, 10% on Welbeck to Score.</strong>
          </div>
        </div>
      </div>

      <!-- TEAM NEWS & LINEUPS -->
      <div class="card" style="animation-delay:.25s">
        <div class="card-hd">
          <div class="hd-dot" style="background:var(--red)"></div>
          <div class="hd-title">Team News · Injuries · Predicted XIs</div>
        </div>
        <div class="card-body">
          <div class="form-cols">
            <div>
              <div class="form-team-lbl" style="color:#60a5fa">Brighton (4-2-3-1)</div>
              <div style="font-size:11.5px;color:var(--label);line-height:1.75">
                <span style="color:#60a5fa">GK</span> Verbruggen<br>
                <span style="color:#60a5fa">DEF</span> Wieffer · Van Hecke · Boscagli · Kadıoğlu<br>
                <span style="color:#60a5fa">MID</span> Ayari · Gross<br>
                <span style="color:#60a5fa">ATT</span> Rutter · Hinshelwood · Minteh<br>
                <span style="color:#60a5fa">FWD</span> Welbeck
              </div>
              <div style="margin-top:10px;font-size:11px">
                <div style="color:var(--red);margin-bottom:3px;font-weight:700">❌ Out:</div>
                <div style="color:var(--muted);line-height:1.8">Gomez (knee) · Milner (minor) · March (injured) ·
                  Webster (ligament) · Tzimas (ligament)</div>
                <div style="color:var(--green);margin-top:5px;margin-bottom:3px;font-weight:700">✅ Returns:</div>
                <div style="color:var(--muted)">Lewis Dunk (back from 2-match ban) — likely to start at CB. Mitoma fit
                  (cramp only vs Spurs).</div>
              </div>
            </div>
            <div>
              <div class="form-team-lbl" style="color:#a5c4ff">Chelsea (4-2-3-1)</div>
              <div style="font-size:11.5px;color:var(--label);line-height:1.75">
                <span style="color:#a5c4ff">GK</span> Sánchez<br>
                <span style="color:#a5c4ff">DEF</span> Gusto · Fofana · Chalobah · Cucurella<br>
                <span style="color:#a5c4ff">MID</span> Lavia · Caicedo<br>
                <span style="color:#a5c4ff">ATT</span> Neto · Palmer · Garnacho<br>
                <span style="color:#a5c4ff">FWD</span> Delap (Joao Pedro if fit?)
              </div>
              <div style="margin-top:10px;font-size:11px">
                <div style="color:var(--red);margin-bottom:3px;font-weight:700">❌ Out:</div>
                <div style="color:var(--muted);line-height:1.8">Estevao (hamstring — out) · Reece James (thigh) ·
                  Colwill (ACL) · Gittens (hamstring) · Jorgensen (GK injury)</div>
                <div style="color:var(--amber);margin-top:5px;margin-bottom:3px;font-weight:700">⚠️ Doubtful:</div>
                <div style="color:var(--muted)">João Pedro (thigh) — will be assessed. Key story: returning to Amex vs
                  former club.</div>
              </div>
            </div>
          </div>
        </div>
      </div>

      <!-- ANALYST NOTES -->
      <div class="card" style="animation-delay:.27s">
        <div class="card-hd">
          <div class="hd-dot" style="background:#7ab8e0"></div>
          <div class="hd-title">Analyst Notes · Key Matchup Factors</div>
        </div>
        <div class="card-body">
          <div class="inline-note">
            <strong>Chelsea's Finishing Crisis vs Brighton's Defensive Efficiency:</strong> Chelsea have 1.57 xG vs Man
            United with 21 shots and still lost 0-1. But Brighton's expected goals against at home is only 0.8/game —
            the Seagulls are genuinely one of the best defences in the league at home. Chelsea will create chances (they
            always do) but converting them at the Amex against Verbruggen + Dunk/Van Hecke is an entirely different
            challenge.
          </div>
          <div class="inline-note">
            <strong>FA Cup Semi-Final Distraction:</strong> Chelsea face Leeds United at Wembley on Saturday. Rosenior
            has insisted this is not a distraction but some rotation is possible — Chalobah may be rested, Garnacho may
            be saved. Any rotation weakens Chelsea's already fragile attacking lineup. Brighton have no such competing
            priority.
          </div>
          <div class="inline-note">
            <strong>Danny Welbeck at 35 — Historic Form:</strong> 12 PL goals. Against Chelsea, he has 5 goals and 2
            assists in his last 8 games — West Ham are the only team he's scored more against. He's been involved in 7
            goals in just 8 PL appearances vs Chelsea overall. This is genuinely Chelsea's biggest individual threat at
            the Amex.
          </div>
          <div class="inline-note">
            <strong>Cole Palmer's Brighton Record:</strong> Despite Chelsea's slump, Palmer has 5 goals in his last 3 PL
            games vs Brighton (and 5 PL goals this season). He told the press he has "only recently started playing
            freely again." This is the one fixture where his H2H record suggests Chelsea may actually end their scoring
            drought. However, getting the ball in dangerous positions away from home against a rigid Brighton backline
            is the challenge.
          </div>
          <div class="inline-note">
            <strong>Corner Asymmetry:</strong> Chelsea average 7.2 corners/away game (PL-highest). Brighton average
            5.0/home game. This asymmetry suggests Chelsea's possession game forces corner-generating situations — but
            <strong>4 of West Ham's last 7 goals came from corners</strong>. Brighton are not immune at corners. Their
            concession rate at set-pieces is worth monitoring in the context of Chelsea's delivery quality.
          </div>
        </div>
      </div>

    </div><!-- end grid -->
  </div><!-- end wrap -->

  <footer
    style="text-align:center;padding:20px 16px;font-size:10px;color:var(--muted);border-top:1px solid var(--border);position:relative;z-index:1">
    <p><strong>Team Bilbo Statistical Analysis</strong><br /></p>
    <p style="margin-top: 4px;">
      Statistical predictions are weighted estimates based on historical data and form analysis.<br />
      <strong style="color: var(--red); text-decoration: underline;">ALWAYS GAMBLE RESPONSIBLY, THIS IS NOT FINANCIAL
        ADVICE</strong>
    </p>
  </footer>

  <script>
    (function () {
      'use strict';

      /* Motivation bar animation */
      setTimeout(() => {
        const bha = document.getElementById('mot-bha');
        const che = document.getElementById('mot-che');
        if (bha) { bha.style.transition = 'width 1.1s ease'; bha.style.width = '87%'; }
        if (che) { setTimeout(() => { che.style.transition = 'width 1.1s ease'; che.style.width = '82%'; }, 150); }
      }, 400);

      /* Prediction bar animations */
      const fills = document.querySelectorAll('.rbf[data-p]');
      if ('IntersectionObserver' in window) {
        const io = new IntersectionObserver(entries => {
          entries.forEach(e => {
            if (e.isIntersecting) {
              setTimeout(() => { e.target.style.width = e.target.getAttribute('data-p') + '%'; }, 200);
              io.unobserve(e.target);
            }
          });
        }, { threshold: .25 });
        fills.forEach(f => io.observe(f));
      } else { fills.forEach(f => f.style.width = f.getAttribute('data-p') + '%'); }

      /* Count-up animations */
      const avs = document.querySelectorAll('.ac .av');
      if ('IntersectionObserver' in window) {
        const io2 = new IntersectionObserver(entries => {
          entries.forEach(e => {
            if (e.isIntersecting) {
              const el = e.target;
              const raw = el.textContent.trim();
              if (!el.dataset.done) {
                el.dataset.done = '1';
                const isPct = raw.includes('%');
                const num = parseFloat(raw);
                if (!isNaN(num)) {
                  let c = 0, step = num / (700 / 16);
                  const t = setInterval(() => {
                    c += step;
                    if (c >= num) { c = num; clearInterval(t); }
                    el.textContent = (raw.includes('.') ? c.toFixed(1) : Math.round(c)) + (isPct ? '%' : '');
                  }, 16);
                }
              }
              io2.unobserve(el);
            }
          });
        }, { threshold: .8 });
        avs.forEach(a => io2.observe(a));
      }

      /* Badge fallback animation stagger */
      document.querySelectorAll('.badge-ring').forEach((b, i) => {
        b.style.animationDelay = (0.06 + i * 0.1) + 's';
      });
    })();
  </script>
