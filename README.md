<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>
      Professional Strategy Analytics
    </title>
    <link rel="preconnect" href="https://fonts.googleapis.com" />
    <link
      href="https://fonts.googleapis.com/css2?family=Barlow+Condensed:ital,wght@0,300;0,400;0,600;0,700;0,800;0,900;1,700&family=Barlow:wght@300;400;500;600;700&display=swap"
      rel="stylesheet" />
    <style>
      /* ════════════════════════════════
   TOKENS
════════════════════════════════ */
      :root {
        --bg: #04060c;
        --bg1: #080b16;
        --bg2: #0d1020;
        --bg3: #12172a;
        --bg4: #181e34;
        --bg5: #1e263f;
        --wire: rgba(255, 255, 255, 0.07);
        --wire2: rgba(255, 255, 255, 0.14);
        --txt: #c0cde4;
        --dim: #47567a;
        --lbl: #7d93b8;
        --hi: #e8f1ff;

        /* Stat bands */
        --lo: #0ed9a0;
        --med: #f7ca38;
        --hot: #f5512a;

        /* PL */
        --pl-dk: #37003c;
        --pl-gr: #00ff85;

        /* Match 1 – Bournemouth / Leeds */
        --bou: #da020e;
        --bou-l: rgba(218, 2, 14, 0.18);
        --lut: #ffcd00;
        --lut-l: rgba(255, 205, 0, 0.14);

        /* Match 2 – Burnley / Man City */
        --bur: #6e3b1f;
        --bur2: #cc5500;
        --bur-l: rgba(110, 59, 31, 0.18);
        --mci: #6cabdd;
        --mci-l: rgba(108, 171, 221, 0.16);
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
      .f-bc {
        font-family: 'Barlow Condensed', sans-serif;
      }

      /* ════ ANIMATIONS ════ */
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
      @keyframes popBadge {
        from {
          transform: scale(5) rotate(-10deg);
          opacity: 0;
        }
        to {
          transform: scale(1) rotate(0);
          opacity: 1;
        }
      }
      @keyframes barIn {
        from {
          width: 0 !important;
        }
      }
      @keyframes glow {
        0%,
        100% {
          opacity: 0.45;
        }
        50% {
          opacity: 0.9;
        }
      }
      @keyframes scan {
        0% {
          background-position: 0 -100%;
        }
        100% {
          background-position: 0 300%;
        }
      }

      /* ════ SCANLINE TEXTURE ════ */
      body::before {
        content: '';
        position: fixed;
        inset: 0;
        z-index: 0;
        pointer-events: none;
        background: repeating-linear-gradient(
          0deg,
          transparent,
          transparent 2px,
          rgba(255, 255, 255, 0.013) 2px,
          rgba(255, 255, 255, 0.013) 3px
        );
      }

      /* ════ PAGE HEADER ════ */
      .ph {
        position: relative;
        z-index: 1;
        background: linear-gradient(
          160deg,
          #040616 0%,
          #0a0025 55%,
          #040616 100%
        );
        border-bottom: 2px solid rgba(55, 0, 60, 0.9);
        padding: 22px 20px 18px;
        text-align: center;
        overflow: hidden;
      }
      .ph::after {
        content: '';
        position: absolute;
        inset: 0;
        pointer-events: none;
        background: radial-gradient(
          ellipse 110% 55% at 50% -15%,
          rgba(0, 255, 133, 0.08),
          transparent 62%
        );
      }
      .ph-kicker {
        display: inline-flex;
        align-items: center;
        gap: 7px;
        font-family: 'Barlow Condensed', sans-serif;
        font-size: 11px;
        font-weight: 700;
        letter-spacing: 2.5px;
        text-transform: uppercase;
        color: var(--pl-gr);
        background: rgba(0, 255, 133, 0.08);
        border: 1px solid rgba(0, 255, 133, 0.28);
        border-radius: 20px;
        padding: 4px 15px;
        margin-bottom: 10px;
        position: relative;
      }
      .ph h1 {
        font-family: 'Barlow Condensed', sans-serif;
        font-size: clamp(26px, 5vw, 52px);
        font-weight: 900;
        color: #fff;
        letter-spacing: 1px;
        line-height: 1;
        position: relative;
        text-transform: uppercase;
      }
      .ph h1 em {
        color: var(--pl-gr);
        font-style: normal;
      }
      .ph-sub {
        font-size: 12px;
        color: var(--dim);
        margin-top: 6px;
        position: relative;
      }

      /* nav pills */
      .ph-nav {
        display: flex;
        flex-wrap: wrap;
        justify-content: center;
        gap: 7px;
        margin-top: 14px;
        position: relative;
      }
      .pn {
        font-family: 'Barlow Condensed', sans-serif;
        font-size: 10px;
        font-weight: 700;
        letter-spacing: 1.5px;
        text-transform: uppercase;
        text-decoration: none;
        padding: 4px 13px;
        border-radius: 4px;
        border: 1px solid;
        transition: all 0.2s;
      }

      /* ════ SECTION DIVIDER ════ */
      .match-divider {
        position: relative;
        z-index: 1;
        padding: 14px 20px 10px;
        text-align: center;
        display: flex;
        align-items: center;
        justify-content: center;
        gap: 10px;
        font-family: 'Barlow Condensed', sans-serif;
        font-size: 11px;
        font-weight: 700;
        letter-spacing: 3px;
        text-transform: uppercase;
      }
      .md-line {
        flex: 1;
        max-width: 180px;
        height: 1px;
      }

      /* ════ WRAP ════ */
      .wrap {
        position: relative;
        z-index: 1;
        max-width: 1300px;
        margin: 0 auto;
        padding: 0 14px 72px;
      }

      /* ════ MATCH HERO ════ */
      .mhero {
        border-radius: 14px;
        overflow: hidden;
        margin-top: 18px;
        box-shadow: 0 12px 60px rgba(0, 0, 0, 0.55);
        animation: fadeUp 0.5s ease both;
      }
      .mhero-inner {
        padding: 26px 22px 22px;
        display: flex;
        flex-direction: column;
        align-items: center;
        gap: 13px;
      }
      .meta-chips {
        display: flex;
        gap: 7px;
        flex-wrap: wrap;
        justify-content: center;
      }
      .chip {
        font-family: 'Barlow Condensed', sans-serif;
        font-size: 10px;
        font-weight: 700;
        letter-spacing: 1.5px;
        text-transform: uppercase;
        padding: 3px 10px;
        border-radius: 4px;
        border: 1px solid;
      }

      /* Motivation row */
      .mot {
        display: flex;
        align-items: center;
        gap: 9px;
        width: 100%;
        max-width: 600px;
        background: rgba(255, 255, 255, 0.03);
        border: 1px solid var(--wire);
        border-radius: 8px;
        padding: 9px 14px;
      }
      .mot-tag {
        font-family: 'Barlow Condensed', sans-serif;
        font-size: 9px;
        font-weight: 700;
        letter-spacing: 1.5px;
        text-transform: uppercase;
        color: var(--dim);
        white-space: nowrap;
      }
      .mot-bar {
        flex: 1;
        height: 6px;
        background: rgba(255, 255, 255, 0.07);
        border-radius: 3px;
        overflow: hidden;
      }
      .mot-fill {
        height: 100%;
        border-radius: 3px;
        transition: width 1s ease 0.5s;
      }
      .mot-pct {
        font-family: 'Barlow Condensed', sans-serif;
        font-size: 13px;
        font-weight: 800;
        white-space: nowrap;
      }

      /* Teams */
      .teams {
        display: grid;
        grid-template-columns: 1fr auto 1fr;
        align-items: center;
        gap: 14px;
        width: 100%;
        max-width: 580px;
      }
      .tc {
        display: flex;
        flex-direction: column;
        align-items: center;
        gap: 7px;
      }
      .badge {
        width: 80px;
        height: 80px;
        border-radius: 50%;
        background: rgba(255, 255, 255, 0.04);
        border: 1.5px solid var(--wire2);
        display: flex;
        align-items: center;
        justify-content: center;
        overflow: hidden;
        transition: transform 0.35s cubic-bezier(0.34, 1.56, 0.64, 1);
        animation: popBadge 0.5s cubic-bezier(0.34, 1.56, 0.64, 1) both;
        flex-shrink: 0;
      }
      .badge:hover {
        transform: scale(1.1) rotate(5deg);
      }
      .badge img {
        width: 58px;
        height: 58px;
        object-fit: contain;
      }
      .tname {
        font-family: 'Barlow Condensed', sans-serif;
        font-size: 14px;
        font-weight: 800;
        text-transform: uppercase;
        letter-spacing: 0.5px;
        text-align: center;
        color: #fff;
      }
      .tmeta {
        font-size: 9.5px;
        color: var(--dim);
        text-align: center;
        line-height: 1.5;
      }
      .vs-c {
        display: flex;
        flex-direction: column;
        align-items: center;
        gap: 5px;
      }
      .vs {
        font-family: 'Barlow Condensed', sans-serif;
        font-size: 22px;
        font-weight: 900;
        color: rgba(255, 255, 255, 0.09);
        letter-spacing: 3px;
      }
      .ko {
        font-family: 'Barlow Condensed', sans-serif;
        font-size: 10px;
        font-weight: 700;
        letter-spacing: 1.5px;
        color: var(--med);
        background: rgba(247, 202, 56, 0.09);
        border: 1px solid rgba(247, 202, 56, 0.28);
        padding: 2px 9px;
        border-radius: 4px;
      }
      .venue {
        font-size: 8.5px;
        color: var(--dim);
        text-align: center;
        line-height: 1.55;
      }

      /* Odds */
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
        min-width: 88px;
        max-width: 145px;
        background: var(--bg2);
        border: 1px solid var(--wire);
        border-radius: 9px;
        padding: 10px 8px;
        text-align: center;
        transition:
          border-color 0.2s,
          transform 0.25s;
      }
      .odds-box:hover {
        transform: translateY(-2px);
        border-color: var(--wire2);
      }
      .ob-val {
        background: linear-gradient(
          135deg,
          rgba(247, 202, 56, 0.08),
          var(--bg2)
        ) !important;
        border-color: rgba(247, 202, 56, 0.35) !important;
      }
      .ob-lbl {
        font-size: 9px;
        text-transform: uppercase;
        letter-spacing: 1px;
        color: var(--dim);
      }
      .ob-odds {
        font-family: 'Barlow Condensed', sans-serif;
        font-size: 23px;
        font-weight: 800;
        color: #fff;
        margin: 3px 0 1px;
        line-height: 1;
      }
      .ob-impl {
        font-size: 9.5px;
        color: var(--lbl);
      }

      /* ════ CONTENT GRID ════ */
      .cgrid {
        display: grid;
        grid-template-columns: 1fr;
        gap: 14px;
        margin-top: 16px;
      }
      @media (min-width: 860px) {
        .cgrid {
          grid-template-columns: 1fr 1fr;
        }
        .span2 {
          grid-column: 1/-1;
        }
      }

      /* ════ CARD ════ */
      .card {
        background: var(--bg1);
        border: 1px solid var(--wire);
        border-radius: 11px;
        overflow: hidden;
        box-shadow: 0 4px 28px rgba(0, 0, 0, 0.4);
        transition: border-color 0.3s;
        animation: fadeUp 0.5s ease both;
      }
      .card:hover {
        border-color: var(--wire2);
      }
      .card-hd {
        padding: 10px 17px 8px;
        border-bottom: 1px solid var(--wire);
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
      .hd-t {
        font-family: 'Barlow Condensed', sans-serif;
        font-size: 10px;
        font-weight: 700;
        letter-spacing: 2px;
        text-transform: uppercase;
        color: var(--dim);
        flex: 1;
      }
      .hd-tag {
        font-size: 8.5px;
        font-weight: 700;
        letter-spacing: 0.8px;
        text-transform: uppercase;
        padding: 2px 8px;
        border-radius: 3px;
        border: 1px solid;
        white-space: nowrap;
      }
      .cb {
        padding: 13px 17px;
      }

      /* Context */
      .ctx {
        background: rgba(255, 255, 255, 0.025);
        border: 1px solid var(--wire2);
        border-radius: 8px;
        padding: 12px 14px;
        font-size: 12.5px;
        line-height: 1.75;
        color: var(--lbl);
      }
      .ctx strong {
        color: var(--med);
        font-weight: 700;
      }
      .kbadge {
        display: inline-flex;
        align-items: center;
        font-size: 10px;
        font-weight: 700;
        letter-spacing: 0.8px;
        text-transform: uppercase;
        padding: 1px 7px;
        border-radius: 3px;
        border: 1px solid;
        margin-right: 3px;
      }
      .kw {
        color: #ff5f3f;
        border-color: rgba(255, 95, 63, 0.35);
        background: rgba(255, 95, 63, 0.1);
      }
      .kg {
        color: #00ff85;
        border-color: rgba(0, 255, 133, 0.3);
        background: rgba(0, 255, 133, 0.08);
      }
      .km {
        color: var(--med);
        border-color: rgba(247, 202, 56, 0.3);
        background: rgba(247, 202, 56, 0.07);
      }

      /* Form */
      .form-cols {
        display: grid;
        grid-template-columns: 1fr 1fr;
        gap: 12px;
      }
      .ftl {
        display: flex;
        align-items: center;
        gap: 6px;
        font-family: 'Barlow Condensed', sans-serif;
        font-size: 10px;
        font-weight: 700;
        letter-spacing: 1px;
        text-transform: uppercase;
        margin-bottom: 7px;
      }
      .fti {
        width: 16px;
        height: 16px;
        object-fit: contain;
        border-radius: 50%;
        background: rgba(255, 255, 255, 0.05);
      }
      .frlist {
        display: flex;
        flex-direction: column;
        gap: 3px;
      }
      .fr {
        display: grid;
        grid-template-columns: 8px 44px 1fr 58px;
        align-items: center;
        gap: 6px;
        background: var(--bg2);
        border: 1px solid var(--wire);
        border-radius: 5px;
        padding: 5px 8px;
        transition: background 0.2s;
      }
      .fr:hover {
        background: var(--bg3);
      }
      .rd {
        width: 8px;
        height: 8px;
        border-radius: 50%;
      }
      .rd.W {
        background: var(--lo);
        box-shadow: 0 0 5px rgba(14, 217, 160, 0.45);
      }
      .rd.D {
        background: var(--med);
      }
      .rd.L {
        background: var(--hot);
        box-shadow: 0 0 5px rgba(245, 81, 42, 0.45);
      }
      .fsc {
        font-family: 'Barlow Condensed', sans-serif;
        font-size: 14px;
        font-weight: 700;
        color: #fff;
        text-align: center;
      }
      .fopp {
        font-size: 11.5px;
        color: var(--txt);
        overflow: hidden;
        text-overflow: ellipsis;
        white-space: nowrap;
      }
      .fcp {
        font-size: 9px;
        color: var(--dim);
        text-align: right;
        text-transform: uppercase;
        letter-spacing: 0.3px;
        white-space: nowrap;
      }
      .ftg {
        font-size: 7.5px;
        padding: 1px 4px;
        border-radius: 2px;
        background: rgba(247, 202, 56, 0.1);
        color: var(--med);
        font-family: 'Barlow Condensed', sans-serif;
        font-weight: 700;
        border: 1px solid rgba(247, 202, 56, 0.25);
      }
      .fleg {
        display: flex;
        gap: 10px;
        margin-top: 8px;
      }
      .fli {
        display: flex;
        align-items: center;
        gap: 4px;
        font-size: 10px;
        color: var(--dim);
      }
      .fld {
        width: 6px;
        height: 6px;
        border-radius: 50%;
      }

      /* H2H */
      .h2h-sum {
        display: grid;
        grid-template-columns: repeat(4, 1fr);
        gap: 4px;
        margin-bottom: 10px;
      }
      .hs {
        background: var(--bg2);
        border-radius: 7px;
        padding: 10px 5px;
        text-align: center;
        border: 1px solid var(--wire);
      }
      .hn {
        font-family: 'Barlow Condensed', sans-serif;
        font-size: 26px;
        font-weight: 800;
        line-height: 1;
      }
      .hl {
        font-size: 8.5px;
        color: var(--dim);
        text-transform: uppercase;
        letter-spacing: 0.5px;
        margin-top: 2px;
      }
      .h2hr-list {
        display: flex;
        flex-direction: column;
        gap: 3px;
      }
      .h2hr {
        display: grid;
        grid-template-columns: 1fr 60px 1fr;
        align-items: center;
        gap: 6px;
        background: var(--bg2);
        border-radius: 5px;
        padding: 5px 8px;
        border: 1px solid var(--wire);
        transition: background 0.2s;
      }
      .h2hr:hover {
        background: var(--bg3);
      }
      .rh {
        font-size: 11px;
        font-weight: 600;
        color: var(--txt);
        text-align: right;
        white-space: nowrap;
        overflow: hidden;
        text-overflow: ellipsis;
      }
      .rs {
        font-family: 'Barlow Condensed', sans-serif;
        font-size: 14px;
        font-weight: 700;
        color: #fff;
        text-align: center;
        background: rgba(255, 255, 255, 0.06);
        border-radius: 3px;
        padding: 1px 3px;
      }
      .ra {
        font-size: 11px;
        font-weight: 600;
        color: var(--txt);
        text-align: left;
        white-space: nowrap;
        overflow: hidden;
        text-overflow: ellipsis;
      }
      .rx {
        font-size: 8.5px;
        color: var(--dim);
        text-align: center;
        grid-column: 1/-1;
        margin-top: -2px;
        letter-spacing: 0.3px;
        text-transform: uppercase;
      }

      /* Avg cells */
      .avgs-pair {
        display: grid;
        grid-template-columns: 1fr 1fr;
        gap: 10px;
      }
      .avlbl {
        font-family: 'Barlow Condensed', sans-serif;
        font-size: 10px;
        font-weight: 700;
        letter-spacing: 1px;
        text-transform: uppercase;
        margin-bottom: 7px;
        padding: 2px 8px;
        border-radius: 3px;
        display: inline-block;
      }
      .acells {
        display: grid;
        grid-template-columns: repeat(3, 1fr);
        gap: 4px;
      }
      .ac {
        background: var(--bg2);
        border-radius: 6px;
        padding: 8px 4px;
        text-align: center;
        border: 1px solid var(--wire);
        transition:
          background 0.2s,
          transform 0.2s;
      }
      .ac:hover {
        background: var(--bg3);
        transform: translateY(-1px);
      }
      .av {
        font-family: 'Barlow Condensed', sans-serif;
        font-size: 18px;
        font-weight: 800;
        color: #fff;
        line-height: 1;
      }
      .al {
        font-size: 7.5px;
        color: var(--dim);
        margin-top: 2px;
        text-transform: uppercase;
        letter-spacing: 0.4px;
        line-height: 1.3;
      }

      /* xG row */
      .xg-row {
        display: flex;
        flex-wrap: wrap;
        gap: 8px;
        margin-top: 10px;
        background: linear-gradient(
          135deg,
          rgba(14, 217, 160, 0.07),
          rgba(14, 217, 160, 0.02)
        );
        border: 1px solid rgba(14, 217, 160, 0.22);
        border-radius: 7px;
        padding: 10px 12px;
      }
      .xgi {
        flex: 1;
        min-width: 75px;
        text-align: center;
      }
      .xgv {
        font-family: 'Barlow Condensed', sans-serif;
        font-size: 22px;
        font-weight: 800;
        line-height: 1;
      }
      .xgl {
        font-size: 8px;
        color: var(--dim);
        text-transform: uppercase;
        letter-spacing: 0.5px;
        margin-top: 2px;
      }

      /* Prediction table */
      .pt-keys {
        display: flex;
        gap: 12px;
        flex-wrap: wrap;
        margin-bottom: 10px;
      }
      .ptk {
        display: flex;
        align-items: center;
        gap: 5px;
        font-size: 10px;
        color: var(--dim);
      }
      .ptkd {
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
      .ptw::-webkit-scrollbar-thumb {
        background: var(--wire2);
        border-radius: 2px;
      }

      .ptbl {
        width: 100%;
        border-collapse: collapse;
        min-width: 540px;
      }
      .ptbl thead th {
        font-family: 'Barlow Condensed', sans-serif;
        font-size: 9px;
        font-weight: 700;
        letter-spacing: 1.5px;
        text-transform: uppercase;
        color: var(--dim);
        padding: 0 6px 10px;
        text-align: left;
        white-space: nowrap;
      }
      .ptbl thead th.tc {
        text-align: center;
      }
      .ptbl tbody td {
        padding: 7px 6px;
        border-bottom: 1px solid rgba(255, 255, 255, 0.03);
        vertical-align: middle;
      }
      .ptbl tbody tr:last-child td {
        border-bottom: none;
      }
      .ptbl tbody tr:hover td {
        background: rgba(255, 255, 255, 0.02);
      }
      .ptbl td.tn {
        color: var(--lbl);
        font-weight: 600;
        font-size: 12.5px;
        white-space: nowrap;
      }
      .ptbl td.tv {
        text-align: center;
      }

      .tsc {
        display: flex;
        flex-direction: column;
        align-items: center;
        gap: 1px;
      }
      .tsv {
        font-family: 'Barlow Condensed', sans-serif;
        font-size: 15px;
        font-weight: 700;
        line-height: 1;
      }
      .tsl {
        font-size: 7.5px;
        color: var(--dim);
        text-transform: uppercase;
        letter-spacing: 0.3px;
      }

      .vlo {
        font-family: 'Barlow Condensed', sans-serif;
        font-size: 16px;
        font-weight: 700;
        color: var(--lo);
      }
      .vmd {
        font-family: 'Barlow Condensed', sans-serif;
        font-size: 18px;
        font-weight: 800;
        color: var(--med);
      }
      .vhi {
        font-family: 'Barlow Condensed', sans-serif;
        font-size: 16px;
        font-weight: 700;
        color: var(--hot);
      }

      .rb {
        flex: 1;
        min-width: 80px;
        height: 5px;
        background: rgba(255, 255, 255, 0.07);
        border-radius: 3px;
        overflow: hidden;
      }
      .rbf {
        height: 100%;
        border-radius: 3px;
        width: 0;
        transition: width 1.3s cubic-bezier(0.25, 0.46, 0.45, 0.94);
      }

      /* Score */
      .sz {
        border-radius: 10px;
        padding: 16px;
        background: linear-gradient(
          135deg,
          rgba(255, 255, 255, 0.04),
          rgba(255, 255, 255, 0.01)
        );
        border: 1px solid var(--wire2);
        display: flex;
        flex-direction: column;
        gap: 12px;
      }
      .szh {
        font-family: 'Barlow Condensed', sans-serif;
        font-size: 9.5px;
        font-weight: 700;
        letter-spacing: 2.5px;
        text-transform: uppercase;
        color: var(--dim);
        text-align: center;
      }
      .sboxes {
        display: flex;
        gap: 8px;
        justify-content: center;
        flex-wrap: wrap;
      }
      .sbox {
        flex: 1;
        min-width: 100px;
        max-width: 158px;
        background: var(--bg2);
        border: 1px solid var(--wire);
        border-radius: 9px;
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
        border-color: rgba(247, 202, 56, 0.42);
        background: linear-gradient(
          135deg,
          rgba(247, 202, 56, 0.08),
          var(--bg2)
        );
      }
      .sbl {
        font-size: 8.5px;
        text-transform: uppercase;
        letter-spacing: 1px;
        color: var(--dim);
      }
      .sbs {
        font-family: 'Barlow Condensed', sans-serif;
        font-size: 30px;
        font-weight: 800;
        color: #fff;
        letter-spacing: 2px;
        margin: 4px 0;
        line-height: 1;
      }
      .sbs.feat {
        color: var(--med);
      }
      .sbp {
        font-size: 9.5px;
        color: var(--dim);
      }
      .sz-note {
        font-size: 12px;
        color: var(--lbl);
        line-height: 1.7;
        border-top: 1px solid var(--wire);
        padding-top: 10px;
      }
      .sz-note strong {
        color: var(--med);
        font-weight: 700;
      }
      .safe-box {
        background: linear-gradient(
          135deg,
          rgba(14, 217, 160, 0.07),
          rgba(14, 217, 160, 0.02)
        );
        border: 1px solid rgba(14, 217, 160, 0.25);
        border-radius: 7px;
        padding: 10px 12px;
        font-size: 12px;
        color: var(--lbl);
        line-height: 1.7;
      }
      .safe-box strong {
        color: var(--lo);
        font-weight: 700;
      }

      /* Yellow cards */
      .ycl {
        display: flex;
        flex-direction: column;
        gap: 6px;
      }
      .yc {
        display: flex;
        align-items: flex-start;
        gap: 9px;
        background: var(--bg2);
        border: 1px solid var(--wire);
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
      .yci {
        font-size: 15px;
        flex-shrink: 0;
        padding-top: 1px;
      }
      .ycinf {
        flex: 1;
        min-width: 0;
      }
      .ycn {
        font-size: 12.5px;
        font-weight: 700;
        color: #fff;
      }
      .ycc {
        font-family: 'Barlow Condensed', sans-serif;
        font-size: 9px;
        letter-spacing: 0.7px;
        text-transform: uppercase;
        margin-left: 5px;
      }
      .ycr {
        font-size: 11px;
        color: var(--dim);
        margin-top: 2px;
        line-height: 1.5;
      }
      .rb-tag {
        font-family: 'Barlow Condensed', sans-serif;
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
      .r-hi {
        color: var(--hot);
        border-color: rgba(245, 81, 42, 0.3);
        background: rgba(245, 81, 42, 0.1);
      }
      .r-md {
        color: var(--med);
        border-color: rgba(247, 202, 56, 0.3);
        background: rgba(247, 202, 56, 0.08);
      }

      /* Bet grid */
      .betg {
        display: grid;
        grid-template-columns: 1fr 1fr;
        gap: 8px;
        margin-bottom: 12px;
      }
      .bc {
        background: var(--bg2);
        border: 1px solid var(--wire);
        border-radius: 8px;
        padding: 11px 12px;
        transition: border-color 0.2s;
      }
      .bc:hover {
        border-color: var(--wire2);
      }
      .bc.bv {
        border-color: rgba(247, 202, 56, 0.38);
        background: linear-gradient(
          135deg,
          rgba(247, 202, 56, 0.07),
          var(--bg2)
        );
      }
      .bc.bw {
        border-color: rgba(245, 81, 42, 0.3);
        background: rgba(245, 81, 42, 0.06);
      }
      .bcm {
        font-size: 9px;
        text-transform: uppercase;
        letter-spacing: 1px;
        color: var(--dim);
        margin-bottom: 3px;
      }
      .bcl {
        font-family: 'Barlow Condensed', sans-serif;
        font-size: 18px;
        font-weight: 800;
        color: #fff;
        line-height: 1;
      }
      .bcl.yv {
        color: var(--med);
      }
      .bcl.gv {
        color: var(--lo);
      }
      .bcl.rv {
        color: var(--hot);
      }
      .bcr {
        font-size: 11px;
        color: var(--lbl);
        margin-top: 4px;
        line-height: 1.5;
      }
      .bn {
        font-size: 12px;
        color: var(--lbl);
        line-height: 1.7;
      }
      .bn strong {
        color: var(--med);
      }

      /* Sub-note */
      .sn {
        font-size: 10.5px;
        color: var(--dim);
        margin-top: 8px;
        line-height: 1.55;
      }
      .sn strong {
        color: var(--med);
      }

      /* Inline note boxes */
      .inb {
        background: var(--bg2);
        border-radius: 6px;
        padding: 10px 12px;
        border: 1px solid var(--wire);
        font-size: 12px;
        color: var(--lbl);
        line-height: 1.7;
        margin-bottom: 7px;
      }
      .inb:last-child {
        margin-bottom: 0;
      }
      .inb strong {
        color: var(--med);
      }

      /* ════ RESPONSIVE ════ */
      @media (min-width: 640px) {
        body {
          font-size: 15px;
        }
        .badge {
          width: 88px;
          height: 88px;
        }
        .badge img {
          width: 66px;
          height: 66px;
        }
        .tname {
          font-size: 15px;
        }
        .cb {
          padding: 15px 20px;
        }
        .card-hd {
          padding: 11px 20px 9px;
        }
      }
      @media (min-width: 1100px) {
        .cb {
          padding: 16px 22px;
        }
        .card-hd {
          padding: 12px 22px 10px;
        }
        .betg {
          grid-template-columns: repeat(4, 1fr);
        }
      }
      @media (max-width: 400px) {
        .form-cols,
        .avgs-pair {
          grid-template-columns: 1fr;
        }
        .h2h-sum {
          grid-template-columns: repeat(2, 1fr);
        }
      }
    </style>
  </head>
  <body>
    <!-- ═══════ PAGE HEADER ═══════ -->
    <header class="ph">
      <div class="ph-kicker">
      Team Bilbo Analytics
      </div>
      <h1 class="f-bc">Data-Driven <em>Matchday Analytics</em></h1>
      <p class="ph-sub">
        Bournemouth vs Leeds United &nbsp;·&nbsp; Burnley vs Manchester City
        &nbsp;·&nbsp; 20:00
      </p>
      <nav class="ph-nav">
        <a
          href="#m1"
          class="pn"
          style="
            color: #da020e;
            border-color: rgba(218, 2, 14, 0.4);
            background: rgba(218, 2, 14, 0.1);
          "
          >Bournemouth vs Leeds</a
        >
        <a
          href="#m2"
          class="pn"
          style="
            color: #6cabdd;
            border-color: rgba(108, 171, 221, 0.35);
            background: rgba(108, 171, 221, 0.1);
          "
          >🏆 Burnley vs Man City</a
        >
      </nav>
    </header>

    <div class="wrap">
      <!-- ─────────────────────────────────────
     MATCH 1 · BOURNEMOUTH vs LEEDS
───────────────────────────────────────── -->
      <div class="match-divider" id="m1" style="color: #da020e">
        <div
          class="md-line"
          style="
            background: linear-gradient(
              90deg,
              transparent,
              rgba(218, 2, 14, 0.5)
            );
          "></div>
        MATCH 1 · VITALITY STADIUM · 20:00
        <div
          class="md-line"
          style="
            background: linear-gradient(
              90deg,
              rgba(218, 2, 14, 0.5),
              transparent
            );
          "></div>
      </div>

      <div
        class="mhero"
        style="
          background: linear-gradient(
            135deg,
            var(--bou-l) 0%,
            var(--bg1) 50%,
            var(--lut-l) 100%
          );
          border: 1px solid rgba(255, 255, 255, 0.08);
        ">
        <div class="mhero-inner">
          <div class="meta-chips">
            <span
              class="chip"
              style="
                color: #da020e;
                border-color: rgba(218, 2, 14, 0.4);
                background: rgba(218, 2, 14, 0.09);
              "
              >Vitality Stadium · Bournemouth</span
            >
            <span
              class="chip"
              style="
                color: var(--pl-gr);
                border-color: rgba(0, 255, 133, 0.28);
                background: rgba(0, 255, 133, 0.07);
              "
              >Bournemouth: European push</span
            >
            <span
              class="chip"
              style="
                color: #ffcd00;
                border-color: rgba(255, 205, 0, 0.3);
                background: rgba(255, 205, 0, 0.07);
              "
              >Leeds: FA Cup SF eyeing Saturday</span
            >
          </div>
          <div class="mot" style="max-width: 600px; width: 100%">
            <span class="mot-tag">🏠 Bou</span>
            <div class="mot-bar">
              <div
                class="mot-fill"
                id="m1-bou"
                style="
                  width: 0;
                  background: linear-gradient(90deg, var(--bou), #ff4d5f);
                "></div>
            </div>
            <span class="mot-pct" style="color: #ef3a4a">72%</span>
            <span
              style="
                font-size: 9px;
                color: var(--dim);
                padding: 0 7px;
                white-space: nowrap;
              "
              >MOTIVATION</span
            >
            <div class="mot-bar">
              <div
                class="mot-fill"
                id="m1-lut"
                style="
                  width: 0;
                  background: linear-gradient(90deg, #b89a00, var(--lut));
                "></div>
            </div>
            <span class="mot-pct" style="color: var(--lut)">61%</span>
            <span class="mot-tag">Leeds ✈️</span>
          </div>
          <div class="teams">
            <div class="tc">
              <div class="badge" style="animation-delay: 0.05s">
                <img
                  src="https://images.gc.afcbournemouthservices.co.uk/fit-in/170x170/e430db60-34ca-11ef-a088-db17c0a14148.png"
                  alt="BOU"
                  style="background: transparent" />
              </div>
              <div class="tname" style="color: #ef3a4a">AFC Bournemouth</div>
              <div class="tmeta">
                8th · 48 pts<br />13-gm PL unbeaten run<br />4 consecutive home
                draws
              </div>
            </div>
            <div class="vs-c">
              <div class="vs">V</div>
              <div class="ko">20:00</div>
              <div class="venue">
                Vitality Stadium<br />Ref: Michael Salisbury<br />~11,300
                capacity
              </div>
            </div>
            <div class="tc">
              <div class="badge" style="animation-delay: 0.12s">
                <img
                  src="https://contentfulproxy.stadion.io/phva2knh4vy5/59uDDesQq19p5lVzfe45BY/a89feaa950427ef005c9d028e925bef0/Full_colour_crest.png?fm=webp&fit=pad&f=center&w=144&h=144&q=100"
                  alt="LEE"
                  style="background: transparent" />
              </div>
              <div class="tname" style="color: var(--lut)">Leeds United</div>
              <div class="tmeta">
                15th · 39 pts · W3 last 3 PL<br />Unbeaten 5 away · 8pts clear
                of drop<br />⚽ FA Cup SF vs Chelsea Sat
              </div>
            </div>
          </div>
          <div class="odds-row">
            <div class="odds-box ob-val">
              <div class="ob-lbl">★ Bournemouth</div>
              <div class="ob-odds" style="color: #ef3a4a">8/11</div>
              <div class="ob-impl">~58% implied</div>
            </div>
            <div class="odds-box">
              <div class="ob-lbl">Draw</div>
              <div class="ob-odds" style="color: var(--med)">12/5</div>
              <div class="ob-impl">~29% implied</div>
            </div>
            <div class="odds-box">
              <div class="ob-lbl">Leeds Win</div>
              <div class="ob-odds" style="color: var(--lut)">7/2</div>
              <div class="ob-impl">~22% implied</div>
            </div>
            <div
              class="odds-box"
              style="
                border-color: rgba(14, 217, 160, 0.3);
                background: linear-gradient(
                  135deg,
                  rgba(14, 217, 160, 0.06),
                  var(--bg2)
                );
              ">
              <div class="ob-lbl">BTTS Yes</div>
              <div class="ob-odds" style="color: var(--lo)">2/3</div>
              <div class="ob-impl">~60% implied</div>
            </div>
          </div>
        </div>
      </div>

      <!-- Grid cards M1 -->
      <div class="cgrid">
        <!-- Context -->
        <div class="card span2" style="animation-delay: 0.06s">
          <div class="card-hd">
            <div class="hd-dot" style="background: var(--med)"></div>
            <div class="hd-t">Match Context · Stakes · Key Storylines</div>
            <div
              class="hd-tag"
              style="
                color: var(--med);
                border-color: rgba(247, 202, 56, 0.3);
                background: rgba(247, 202, 56, 0.07);
              ">
              FA Cup distraction risk
            </div>
          </div>
          <div class="cb">
            <div class="ctx">
              <span
                class="kbadge"
                style="
                  color: #ef3a4a;
                  border-color: rgba(218, 2, 14, 0.4);
                  background: rgba(218, 2, 14, 0.1);
                "
                >Bournemouth</span
              >
              8th, 48pts — in the thick of the European qualification race
              alongside Chelsea, Brighton, and Brentford. Their
              <strong>13-game PL unbeaten run</strong> (W6 D7) is
              club-record-breaking. However, the home form tells a more cautious
              story: <strong>4 consecutive home draws</strong> and just
              <strong>2 home wins from their last 11 PL home games</strong>.
              Their last home win was January. Iraola's final season means
              European football would be a fairytale send-off — high motivation
              to break the home draw streak. Key absences:
              <strong
                >Kluivert (knee — out), Cook (thigh — doubt), Soler (thigh —
                doubt)</strong
              >.<br /><br />
              <span
                class="kbadge"
                style="
                  color: var(--lut);
                  border-color: rgba(255, 205, 0, 0.35);
                  background: rgba(255, 205, 0, 0.08);
                "
                >Leeds United</span
              >
              15th, 39pts —
              <strong>8 points clear of the relegation zone</strong> and
              near-safe. Farke's side won W3 last 3 PL games (Man Utd 2-1,
              Wolves 3-0, Everton draw) and are
              <strong>unbeaten in 5 consecutive away trips</strong>. The
              critical context:
              <strong
                >FA Cup semi-final vs Chelsea at Wembley on Saturday</strong
              >. Farke may rotate to protect key players — Joe Rodon,
              Calvert-Lewin, and Aaronson could all be managed or rested. Anton
              Stach and Dan James (long-term) are out. Leeds rank 18th in PL
              away form all season but their recent road form (unbeaten 5) is
              vastly better than their seasonal average. <br /><br /><span
                class="kbadge km"
                >⚠ Key Stat</span
              >
              Bournemouth have <strong>never won</strong> any of their 5 PL
              games vs promoted sides this season (D4 L1). Leeds were promoted.
              Bournemouth average 1.44 goals/home and 1.06 conceded — BTTS in
              <strong>63% of matches</strong>.
            </div>
          </div>
        </div>

        <!-- Last 5 Form M1 -->
        <div class="card" style="animation-delay: 0.09s">
          <div class="card-hd">
            <div class="hd-dot" style="background: #ef3a4a"></div>
            <div class="hd-t">Last 5 Matches</div>
          </div>
          <div class="cb">
            <div class="form-cols">
              <div>
                <div class="ftl" style="color: #ef3a4a">
                  <img
                    class="fti"
                    src="https://upload.wikimedia.org/wikipedia/en/thumb/e/e5/AFC_Bournemouth_%282013%29.svg/120px-AFC_Bournemouth_%282013%29.svg.png"
                    alt=""
                    style="background: transparent" />Bournemouth
                </div>
                <div class="frlist">
                  <div class="fr">
                    <div class="rd W"></div>
                    <div class="fsc">2–1</div>
                    <div class="fopp">Newcastle</div>
                    <div class="fcp">PL Away</div>
                  </div>
                  <div class="fr">
                    <div class="rd W"></div>
                    <div class="fsc">2–1</div>
                    <div class="fopp">Arsenal</div>
                    <div class="fcp">PL Away</div>
                  </div>
                  <div class="fr">
                    <div class="rd D"></div>
                    <div class="fsc">0–0</div>
                    <div class="fopp">Bournemouth vs Leeds</div>
                    <div class="fcp">Sep 2025</div>
                  </div>
                  <div class="fr">
                    <div class="rd D"></div>
                    <div class="fsc">1–1</div>
                    <div class="fopp">Southampton</div>
                    <div class="fcp">PL Home</div>
                  </div>
                  <div class="fr">
                    <div class="rd D"></div>
                    <div class="fsc">1–1</div>
                    <div class="fopp">Brentford</div>
                    <div class="fcp">PL Home</div>
                  </div>
                </div>
              </div>
              <div>
                <div class="ftl" style="color: var(--lut)">
                  <img
                    class="fti"
                    src="https://upload.wikimedia.org/wikipedia/en/thumb/5/54/Leeds_United_F.C._logo.svg/120px-Leeds_United_F.C._logo.svg.png"
                    alt=""
                    style="background: transparent" />Leeds United
                </div>
                <div class="frlist">
                  <div class="fr">
                    <div class="rd W"></div>
                    <div class="fsc">3–0</div>
                    <div class="fopp">Wolves</div>
                    <div class="fcp">PL Home</div>
                  </div>
                  <div class="fr">
                    <div class="rd W"></div>
                    <div class="fsc">2–1</div>
                    <div class="fopp">Man United</div>
                    <div class="fcp">PL Away</div>
                  </div>
                  <div class="fr">
                    <div class="rd D"></div>
                    <div class="fsc">0–0</div>
                    <div class="fopp">Crystal Palace</div>
                    <div class="fcp">PL Away</div>
                  </div>
                  <div class="fr">
                    <div class="rd D"></div>
                    <div class="fsc">1–1</div>
                    <div class="fopp">Aston Villa</div>
                    <div class="fcp">PL Away</div>
                  </div>
                  <div class="fr">
                    <div class="rd W"></div>
                    <div class="fsc">W Pens</div>
                    <div class="fopp">West Ham</div>
                    <div class="fcp">FAC <span class="ftg">SF place</span></div>
                  </div>
                </div>
              </div>
            </div>
            <div class="fleg">
              <div class="fli">
                <div class="fld" style="background: var(--lo)"></div>
                Win
              </div>
              <div class="fli">
                <div class="fld" style="background: var(--med)"></div>
                Draw
              </div>
              <div class="fli">
                <div class="fld" style="background: var(--hot)"></div>
                Loss
              </div>
            </div>
            <div class="sn">
              <strong>Trend:</strong> Bournemouth: W2 D7 in last 9 — high draw
              rate. Leeds: W3 D3 last 6, unbeaten 5 away — excellent road form
              recently. Leeds conceded only 2 goals in last 5 games.
            </div>
          </div>
        </div>

        <!-- H2H M1 -->
        <div class="card" style="animation-delay: 0.11s">
          <div class="card-hd">
            <div class="hd-dot" style="background: var(--hot)"></div>
            <div class="hd-t">Head to Head — Last 5 Meetings</div>
            <div
              class="hd-tag"
              style="
                color: var(--lo);
                border-color: rgba(14, 217, 160, 0.3);
                background: rgba(14, 217, 160, 0.07);
              ">
              O2.5 in last 4 H2H at Vitality
            </div>
          </div>
          <div class="cb">
            <div class="h2h-sum">
              <div class="hs">
                <div class="hn" style="color: #ef3a4a">1</div>
                <div class="hl">Bou W</div>
              </div>
              <div class="hs">
                <div class="hn" style="color: var(--med)">1</div>
                <div class="hl">Draws</div>
              </div>
              <div class="hs">
                <div class="hn" style="color: var(--lut)">3</div>
                <div class="hl">Leeds W</div>
              </div>
              <div class="hs">
                <div class="hn">2.8</div>
                <div class="hl">Avg Goals</div>
              </div>
            </div>
            <div class="h2hr-list">
              <div class="h2hr">
                <div class="rh">Leeds</div>
                <div class="rs">2–2</div>
                <div class="ra">Bournemouth</div>
                <div class="rx">PL Sep 2025 — Kroupi 93' equaliser</div>
              </div>
              <div class="h2hr">
                <div class="rh">Leeds</div>
                <div class="rs">4–1</div>
                <div class="ra">Bournemouth</div>
                <div class="rx">
                  PL Apr 2023 — Vitality (BOU's last PL trip before promo)
                </div>
              </div>
              <div class="h2hr">
                <div class="rh">Leeds</div>
                <div class="rs">1–0</div>
                <div class="ra">Bournemouth</div>
                <div class="rx">PL Oct 2022 (Elland Rd)</div>
              </div>
              <div class="h2hr">
                <div class="rh">Bournemouth</div>
                <div class="rs">1–0</div>
                <div class="ra">Leeds</div>
                <div class="rx">PL Feb 2023 (Vitality)</div>
              </div>
              <div class="h2hr">
                <div class="rh">Leeds</div>
                <div class="rs">4–0</div>
                <div class="ra">Bournemouth</div>
                <div class="rx">PL Aug 2022 (Elland Rd)</div>
              </div>
            </div>
            <div class="sn">
              Leeds hold <strong>historical dominance</strong> (11-2 overall).
              But Leeds have never conceded &lt;2 at Vitality in 4 H2H visits
              (O2.5 every time). Farke has 2W 2D 3L vs Bournemouth as manager.
              BOU have NOT won at home vs promoted teams all season (D4 L1).
            </div>
          </div>
        </div>

        <!-- Season Avgs M1 -->
        <div class="card" style="animation-delay: 0.13s">
          <div class="card-hd">
            <div class="hd-dot" style="background: #a78bfa"></div>
            <div class="hd-t">Season Averages — PL 2025/26</div>
          </div>
          <div class="cb">
            <div class="avgs-pair">
              <div>
                <div
                  class="avlbl"
                  style="
                    color: #fff;
                    background: rgba(218, 2, 14, 0.18);
                    border: 1px solid rgba(218, 2, 14, 0.35);
                  ">
                  Bournemouth
                </div>
                <div class="acells">
                  <div class="ac">
                    <div class="av">13.8</div>
                    <div class="al">Shots/gm</div>
                  </div>
                  <div class="ac">
                    <div class="av">4.7</div>
                    <div class="al">SOT/gm</div>
                  </div>
                  <div class="ac">
                    <div class="av">5.5</div>
                    <div class="al">Corners/home</div>
                  </div>
                  <div class="ac">
                    <div class="av">11.2</div>
                    <div class="al">Fouls</div>
                  </div>
                  <div class="ac">
                    <div class="av">1.44</div>
                    <div class="al">Gls/home</div>
                  </div>
                  <div class="ac">
                    <div class="av">58%</div>
                    <div class="al">BTTS rate</div>
                  </div>
                </div>
              </div>
              <div>
                <div
                  class="avlbl"
                  style="
                    color: #1a1400;
                    background: rgba(255, 205, 0, 0.85);
                    border: 1px solid rgba(255, 205, 0, 0.5);
                  ">
                  Leeds United
                </div>
                <div class="acells">
                  <div class="ac">
                    <div class="av">12.5</div>
                    <div class="al">Shots/gm</div>
                  </div>
                  <div class="ac">
                    <div class="av">3.5</div>
                    <div class="al">SOT/gm</div>
                  </div>
                  <div class="ac">
                    <div class="av">4.2</div>
                    <div class="al">Corners/away</div>
                  </div>
                  <div class="ac">
                    <div class="av">10.9</div>
                    <div class="al">Fouls won</div>
                  </div>
                  <div class="ac">
                    <div class="av">11</div>
                    <div class="al">Calvert-Lewin goals</div>
                  </div>
                  <div class="ac">
                    <div class="av">3</div>
                    <div class="al">CS last 5</div>
                  </div>
                </div>
              </div>
            </div>
            <div class="xg-row">
              <div class="xgi">
                <div class="xgv" style="color: #ef3a4a">1.44</div>
                <div class="xgl">Bou xG/home</div>
              </div>
              <div class="xgi">
                <div class="xgv" style="color: #ff9980">1.50</div>
                <div class="xgl">Bou xGA/gm</div>
              </div>
              <div class="xgi">
                <div class="xgv" style="color: var(--lut)">1.06</div>
                <div class="xgl">Leeds xG/away</div>
              </div>
              <div class="xgi">
                <div class="xgv" style="color: #ffe47a">0.94</div>
                <div class="xgl">Leeds goals/away</div>
              </div>
              <div class="xgi">
                <div class="xgv" style="color: var(--lo)">2</div>
                <div class="xgl">Leeds goals conceded last 5</div>
              </div>
            </div>
            <div class="sn">
              Bournemouth avg 100 goals in 33 PL games (3.03/gm combined). Leeds
              have kept 3 clean sheets in last 5 — their defensive improvement
              is real. Bournemouth have failed to score in 2 of last 5 home PL
              games.
            </div>
          </div>
        </div>

        <!-- Home/Away splits M1 -->
        <div class="card" style="animation-delay: 0.15s">
          <div class="card-hd">
            <div class="hd-dot" style="background: var(--lo)"></div>
            <div class="hd-t">Home / Away Performance Splits</div>
          </div>
          <div class="cb">
            <div class="avgs-pair">
              <div>
                <div
                  class="avlbl"
                  style="
                    color: #fff;
                    background: rgba(218, 2, 14, 0.18);
                    border: 1px solid rgba(218, 2, 14, 0.35);
                  ">
                  Bou @ Home
                </div>
                <div class="acells">
                  <div class="ac">
                    <div class="av">6</div>
                    <div class="al">PL Home W</div>
                  </div>
                  <div class="ac">
                    <div class="av">8</div>
                    <div class="al">Home draws</div>
                  </div>
                  <div class="ac">
                    <div class="av">2</div>
                    <div class="al">Home L</div>
                  </div>
                  <div class="ac">
                    <div class="av">4</div>
                    <div class="al">Consec draws</div>
                  </div>
                  <div class="ac">
                    <div class="av">Jan</div>
                    <div class="al">Last home win</div>
                  </div>
                  <div class="ac">
                    <div class="av">1.63</div>
                    <div class="al">Pts/gm home</div>
                  </div>
                </div>
              </div>
              <div>
                <div
                  class="avlbl"
                  style="
                    color: #1a1400;
                    background: rgba(255, 205, 0, 0.85);
                    border: 1px solid rgba(255, 205, 0, 0.5);
                  ">
                  Leeds Away
                </div>
                <div class="acells">
                  <div class="ac">
                    <div class="av">1</div>
                    <div class="al">Away L last 12</div>
                  </div>
                  <div class="ac">
                    <div class="av">5</div>
                    <div class="al">Away unbeaten</div>
                  </div>
                  <div class="ac">
                    <div class="av">0.81</div>
                    <div class="al">Pts/gm away</div>
                  </div>
                  <div class="ac">
                    <div class="av">29</div>
                    <div class="al">Away goals conc</div>
                  </div>
                  <div class="ac">
                    <div class="av">2</div>
                    <div class="al">Away CS (season)</div>
                  </div>
                  <div class="ac">
                    <div class="av">18th</div>
                    <div class="al">Away form rank</div>
                  </div>
                </div>
              </div>
            </div>
            <div class="sn">
              Leeds are 18th in PL away form all season but their recent run (1
              defeat in 12 all comps away) shows a dramatic turnaround.
              Bournemouth's home draw problem is a major factor — they have
              momentum in away games but not at the Vitality. The FA Cup SF on
              Saturday creates rotation pressure for Farke.
            </div>
          </div>
        </div>

        <!-- Prediction Table M1 -->
        <div class="card span2" style="animation-delay: 0.17s">
          <div class="card-hd">
            <div class="hd-dot" style="background: var(--lo)"></div>
            <div class="hd-t">
              Weighted Stat Predictions — Bournemouth vs Leeds
            </div>
          </div>
          <div class="cb">
            <div class="pt-keys">
              <div class="ptk">
                <div class="ptkd" style="background: var(--lo)"></div>
                <span style="color: var(--lo); font-weight: 700">Low</span>
              </div>
              <div class="ptk">
                <div class="ptkd" style="background: var(--med)"></div>
                <span style="color: var(--med); font-weight: 700">Median</span>
              </div>
              <div class="ptk">
                <div class="ptkd" style="background: var(--hot)"></div>
                <span style="color: var(--hot); font-weight: 700">High</span>
              </div>
              <div
                class="ptk"
                style="margin-left: auto; font-size: 10px; color: var(--dim)">
                Ref: Michael Salisbury
              </div>
            </div>
            <div class="ptw">
              <table class="ptbl">
                <colgroup>
                  <col style="width: 22%" />
                  <col style="width: 13%" />
                  <col style="width: 13%" />
                  <col style="width: 10%" />
                  <col style="width: 12%" />
                  <col style="width: 10%" />
                  <col style="width: 20%" />
                </colgroup>
                <thead>
                  <tr>
                    <th>Metric</th>
                    <th class="tv" style="color: #ef3a4a; text-align: center">
                      Bou
                    </th>
                    <th
                      class="tv"
                      style="color: var(--lut); text-align: center">
                      Leeds
                    </th>
                    <th class="tv" style="color: var(--lo); text-align: center">
                      Low
                    </th>
                    <th
                      class="tv"
                      style="color: var(--med); text-align: center">
                      Median
                    </th>
                    <th
                      class="tv"
                      style="color: var(--hot); text-align: center">
                      High
                    </th>
                    <th
                      class="tv"
                      style="color: var(--dim); text-align: center">
                      Bar
                    </th>
                  </tr>
                </thead>
                <tbody>
                  <tr>
                    <td class="tn">🔲 Corners</td>
                    <td class="tv">
                      <div class="tsc">
                        <span class="tsv" style="color: #ef3a4a">5</span
                        ><span class="tsl">med</span>
                      </div>
                    </td>
                    <td class="tv">
                      <div class="tsc">
                        <span class="tsv" style="color: var(--lut)">4</span
                        ><span class="tsl">med</span>
                      </div>
                    </td>
                    <td class="tv"><span class="vlo">7</span></td>
                    <td class="tv"><span class="vmd">9</span></td>
                    <td class="tv"><span class="vhi">14</span></td>
                    <td>
                      <div class="rb">
                        <div
                          class="rbf"
                          data-p="58"
                          style="
                            background: linear-gradient(
                              90deg,
                              var(--bou),
                              var(--lut)
                            );
                          "></div>
                      </div>
                    </td>
                  </tr>
                  <tr>
                    <td class="tn">📊 Total Shots</td>
                    <td class="tv">
                      <div class="tsc">
                        <span class="tsv" style="color: #ef3a4a">14</span
                        ><span class="tsl">med</span>
                      </div>
                    </td>
                    <td class="tv">
                      <div class="tsc">
                        <span class="tsv" style="color: var(--lut)">10</span
                        ><span class="tsl">med</span>
                      </div>
                    </td>
                    <td class="tv"><span class="vlo">18</span></td>
                    <td class="tv"><span class="vmd">24</span></td>
                    <td class="tv"><span class="vhi">32</span></td>
                    <td>
                      <div class="rb">
                        <div
                          class="rbf"
                          data-p="68"
                          style="
                            background: linear-gradient(
                              90deg,
                              var(--bou),
                              var(--lut)
                            );
                          "></div>
                      </div>
                    </td>
                  </tr>
                  <tr>
                    <td class="tn">🎯 Shots on Target</td>
                    <td class="tv">
                      <div class="tsc">
                        <span class="tsv" style="color: #ef3a4a">5</span
                        ><span class="tsl">med</span>
                      </div>
                    </td>
                    <td class="tv">
                      <div class="tsc">
                        <span class="tsv" style="color: var(--lut)">3</span
                        ><span class="tsl">med</span>
                      </div>
                    </td>
                    <td class="tv"><span class="vlo">5</span></td>
                    <td class="tv"><span class="vmd">8</span></td>
                    <td class="tv"><span class="vhi">13</span></td>
                    <td>
                      <div class="rb">
                        <div
                          class="rbf"
                          data-p="58"
                          style="
                            background: linear-gradient(
                              90deg,
                              var(--bou),
                              var(--lut)
                            );
                          "></div>
                      </div>
                    </td>
                  </tr>
                  <tr>
                    <td class="tn">⚠️ Fouls</td>
                    <td class="tv">
                      <div class="tsc">
                        <span class="tsv" style="color: #ef3a4a">11</span
                        ><span class="tsl">med</span>
                      </div>
                    </td>
                    <td class="tv">
                      <div class="tsc">
                        <span class="tsv" style="color: var(--lut)">13</span
                        ><span class="tsl">med</span>
                      </div>
                    </td>
                    <td class="tv"><span class="vlo">16</span></td>
                    <td class="tv"><span class="vmd">24</span></td>
                    <td class="tv"><span class="vhi">34</span></td>
                    <td>
                      <div class="rb">
                        <div
                          class="rbf"
                          data-p="70"
                          style="
                            background: linear-gradient(
                              90deg,
                              var(--bou),
                              var(--lut)
                            );
                          "></div>
                      </div>
                    </td>
                  </tr>
                  <tr>
                    <td class="tn">↗️ Throw-ins</td>
                    <td class="tv">
                      <div class="tsc">
                        <span class="tsv" style="color: #ef3a4a">20</span
                        ><span class="tsl">med</span>
                      </div>
                    </td>
                    <td class="tv">
                      <div class="tsc">
                        <span class="tsv" style="color: var(--lut)">18</span
                        ><span class="tsl">med</span>
                      </div>
                    </td>
                    <td class="tv"><span class="vlo">28</span></td>
                    <td class="tv"><span class="vmd">38</span></td>
                    <td class="tv"><span class="vhi">52</span></td>
                    <td>
                      <div class="rb">
                        <div
                          class="rbf"
                          data-p="62"
                          style="
                            background: linear-gradient(
                              90deg,
                              var(--bou),
                              var(--lut)
                            );
                          "></div>
                      </div>
                    </td>
                  </tr>
                  <tr>
                    <td class="tn">🥅 Goal Kicks</td>
                    <td class="tv">
                      <div class="tsc">
                        <span class="tsv" style="color: #ef3a4a">10</span
                        ><span class="tsl">med</span>
                      </div>
                    </td>
                    <td class="tv">
                      <div class="tsc">
                        <span class="tsv" style="color: var(--lut)">11</span
                        ><span class="tsl">med</span>
                      </div>
                    </td>
                    <td class="tv"><span class="vlo">14</span></td>
                    <td class="tv"><span class="vmd">21</span></td>
                    <td class="tv"><span class="vhi">30</span></td>
                    <td>
                      <div class="rb">
                        <div
                          class="rbf"
                          data-p="60"
                          style="
                            background: linear-gradient(
                              90deg,
                              var(--bou),
                              var(--lut)
                            );
                          "></div>
                      </div>
                    </td>
                  </tr>
                  <tr>
                    <td class="tn">⚔️ Tackles</td>
                    <td class="tv">
                      <div class="tsc">
                        <span class="tsv" style="color: #ef3a4a">14</span
                        ><span class="tsl">med</span>
                      </div>
                    </td>
                    <td class="tv">
                      <div class="tsc">
                        <span class="tsv" style="color: var(--lut)">16</span
                        ><span class="tsl">med</span>
                      </div>
                    </td>
                    <td class="tv"><span class="vlo">22</span></td>
                    <td class="tv"><span class="vmd">30</span></td>
                    <td class="tv"><span class="vhi">42</span></td>
                    <td>
                      <div class="rb">
                        <div
                          class="rbf"
                          data-p="66"
                          style="
                            background: linear-gradient(
                              90deg,
                              var(--bou),
                              var(--lut)
                            );
                          "></div>
                      </div>
                    </td>
                  </tr>
                </tbody>
              </table>
            </div>
            <div class="sn" style="margin-top: 10px">
              <strong>Key weightings:</strong> Fouls elevated by Leeds' physical
              3-4-2-1, Ampadu's combative style (8 yellows) and Salisbury's
              involvement in physical games. Corners moderate — Bournemouth avg
              5.5/home vs Leeds' solid defensive shape; Leeds concede corners
              generously. Tackles high as both teams press from compact
              formations.
            </div>
          </div>
        </div>

        <!-- Score M1 -->
        <div class="card" style="animation-delay: 0.19s">
          <div class="card-hd">
            <div class="hd-dot" style="background: var(--med)"></div>
            <div class="hd-t">Score Prediction</div>
          </div>
          <div class="cb">
            <div class="sz">
              <div class="szh">
                Bournemouth vs Leeds United · Vitality Stadium
              </div>
              <div class="sboxes">
                <div class="sbox">
                  <div class="sbl">Half-Time</div>
                  <div class="sbs">0–0</div>
                  <div class="sbp">~34% — tight first half</div>
                </div>
                <div class="sbox feat">
                  <div class="sbl">Full-Time ★</div>
                  <div class="sbs feat">1–1</div>
                  <div class="sbp">Draw ~30% — best value</div>
                </div>
                <div class="sbox">
                  <div class="sbl">Alt: Bou Win</div>
                  <div class="sbs">1–0</div>
                  <div class="sbp">~28% — Bou home edge</div>
                </div>
              </div>
              <div class="sz-note">
                <strong>Why 1-1 Draw:</strong> Bournemouth have drawn 4
                consecutive home games and have
                <strong>never beaten a promoted side at home</strong> all season
                (D4 L1). Leeds are unbeaten in their last 5 away trips and have
                only conceded twice in 5 games — their defensive improvement is
                genuine. Farke's FA Cup focus means some rotation is possible,
                but Leeds' shape away from home (3-4-2-1) is designed for
                exactly this type of tight away point. Both teams have scored in
                all recent H2H — BTTS is the safest statistical conclusion.
                Calvert-Lewin (11 goals, 0.43/90) is the key threat; Evanilson
                and Kroupi carry Bournemouth's attacking threat with Kluivert
                absent.
              </div>
              <div class="safe-box">
                <strong
                  >🛡 Safe Pick — BTTS Yes (2/3) + Over 2.5 Goals (4/5):</strong
                >
                Over 2.5 goals in Bournemouth's last 3 PL games and last 4 H2H
                at Vitality. BTTS in 63% of all Bournemouth's games this season.
                Leeds have scored in last 3 PL games (Wolves, Man Utd, Everton).
                Both teams' recent attacking form strongly supports goals at
                both ends. Best combined value: BTTS Yes as the single safest
                bet at 2/3.
              </div>
            </div>
          </div>
        </div>

        <!-- Yellow Cards M1 -->
        <div class="card" style="animation-delay: 0.21s">
          <div class="card-hd">
            <div class="hd-dot" style="background: #ffe84a"></div>
            <div class="hd-t">🟨 Yellow Card Risk Players</div>
            <div
              class="hd-tag"
              style="
                color: var(--med);
                border-color: rgba(247, 202, 56, 0.3);
                background: rgba(247, 202, 56, 0.07);
              ">
              Ref: Michael Salisbury
            </div>
          </div>
          <div class="cb">
            <div class="ycl">
              <div class="yc">
                <div class="yci">🟨</div>
                <div class="ycinf">
                  <div class="ycn">
                    Ethan Ampadu
                    <span class="ycc" style="color: var(--lut)"
                      >Leeds · DM</span
                    >
                  </div>
                  <div class="ycr">
                    8 PL yellow cards this season — Leeds' midfield enforcer.
                    Faces Bournemouth's energetic press and wide overloads. Will
                    foul to disrupt Iraola's pressing game. The most likely
                    booking on the pitch.
                  </div>
                </div>
                <div class="rb-tag r-hi">HIGH</div>
              </div>
              <div class="yc">
                <div class="yci">🟨</div>
                <div class="ycinf">
                  <div class="ycn">
                    Marcos Senesi
                    <span class="ycc" style="color: #ef3a4a"
                      >Bournemouth · CB</span
                    >
                  </div>
                  <div class="ycr">
                    Bournemouth's CB who tackles aggressively against physical
                    strikers. Faces Calvert-Lewin — a constant aerial threat who
                    draws fouls. Senesi's high card frequency noted in stats
                    previews.
                  </div>
                </div>
                <div class="rb-tag r-hi">HIGH</div>
              </div>
              <div class="yc">
                <div class="yci">🟨</div>
                <div class="ycinf">
                  <div class="ycn">
                    Ryan Christie
                    <span class="ycc" style="color: #ef3a4a"
                      >Bournemouth · CM</span
                    >
                  </div>
                  <div class="ycr">
                    Combative central midfielder who fouls when Leeds' quick
                    transitions catch Bournemouth out. 5 PL yellows this season;
                    physical CM in direct duels with Tanaka and Aaronson.
                  </div>
                </div>
                <div class="rb-tag r-md">MED</div>
              </div>
              <div class="yc">
                <div class="yci">🟨</div>
                <div class="ycinf">
                  <div class="ycn">
                    Álex Jiménez
                    <span class="ycc" style="color: #ef3a4a"
                      >Bournemouth · RB</span
                    >
                  </div>
                  <div class="ycr">
                    High-frequency card recipient among Bournemouth's defensive
                    line. Faces Leeds' wing-back overlaps — Gudmundsson and
                    Bogle create space that Jiménez defends with physicality.
                  </div>
                </div>
                <div class="rb-tag r-md">MED</div>
              </div>
            </div>
          </div>
        </div>

        <!-- Betting M1 -->
        <div class="card span2" style="animation-delay: 0.23s">
          <div class="card-hd">
            <div class="hd-dot" style="background: var(--lo)"></div>
            <div class="hd-t">📈 Betting Market Analysis · Value Picks</div>
          </div>
          <div class="cb">
            <div class="betg">
              <div class="bc bv">
                <div class="bcm">★ Best Value</div>
                <div class="bcl yv">BTTS Yes 2/3</div>
                <div class="bcr">
                  63% of Bou games BTTS. Last 4 H2H at Vitality all O2.5. Leeds
                  scored last 3. Both teams attacking. Statistically strongest
                  selection.
                </div>
              </div>
              <div class="bc bv">
                <div class="bcm">★ Goals Play</div>
                <div class="bcl gv">Over 2.5 Goals 4/5</div>
                <div class="bcr">
                  O2.5 in Bou's last 3 PL games. Last 4 H2H at Vitality featured
                  3+ goals. Leeds scored 5 goals in last 2 PL. Goals are highly
                  probable here.
                </div>
              </div>
              <div class="bc">
                <div class="bcm">Result Market</div>
                <div class="bcl">Draw 12/5</div>
                <div class="bcr">
                  4 consecutive home draws for Bou. Leeds unbeaten 5 away. Never
                  beaten promoted sides at home. Value in draw given Bou's home
                  draw trend.
                </div>
              </div>
              <div class="bc">
                <div class="bcm">Prop: Goals</div>
                <div class="bcl yv">Over 3.5 Goals 2/1</div>
                <div class="bcr">
                  O3.5 in 3 consecutive H2H at Vitality. Value bet at 2/1 given
                  historical pattern, though Leeds defensive improvement tempers
                  upside.
                </div>
              </div>
              <div class="bc bw">
                <div class="bcm">⚠ Avoid</div>
                <div class="bcl rv">Leeds Win 7/2</div>
                <div class="bcr">
                  Despite their good away form, Leeds playing Wednesday ahead of
                  FA Cup SF Saturday. Even if Farke rotates slightly, 7/2
                  underestimates Bournemouth's home strength and European
                  motivation.
                </div>
              </div>
              <div class="bc">
                <div class="bcm">Prop: Scorer</div>
                <div class="bcl">Calvert-Lewin Anytime</div>
                <div class="bcr">
                  11 goals this season, 0.43 per 90. Will target Senesi
                  aerially. Bournemouth concede 1.06/home. Good value as the
                  most clinical striker in this game.
                </div>
              </div>
              <div class="bc">
                <div class="bcm">Prop: Cards</div>
                <div class="bcl yv">Ampadu to be Booked</div>
                <div class="bcr">
                  8 PL yellows already. Faces Bournemouth's aggressive midfield
                  press. Salisbury is card-aware. Very high historical rate
                  makes this the standout card bet.
                </div>
              </div>
              <div class="bc">
                <div class="bcm">Corners</div>
                <div class="bcl">Over 8.5 Corners</div>
                <div class="bcr">
                  Bou avg 5.5/home corners. Leeds average 4.2/away. Combined 9.7
                  mean exceeds the 8.5 line regularly in their H2H. Slight value
                  at standard prices.
                </div>
              </div>
            </div>
            <div class="bn">
              <strong>Overall:</strong> This is a genuinely competitive London
              derby equivalent of mid-table intrigue. Bournemouth's home draw
              streak (4 games) shows they can't dominate at Vitality right now,
              and Leeds are legitimately solid on the road.
              <strong>BTTS Yes is the single strongest statistical pick</strong>
              backed by 63% of Bournemouth games featuring both teams scoring,
              last 4 H2H at this ground going O2.5, and both teams' recent
              goal-scoring form. Over 2.5 at 4/5 compounds this nicely. The
              <strong>draw at 12/5 offers value</strong> for those wanting a
              result market bet — it's statistically likely given Bournemouth's
              home trend and Leeds' away solidity. Smart play: 60% BTTS Yes, 30%
              O2.5 Goals, 10% Draw.
            </div>
          </div>
        </div>
      </div>
      <!-- end M1 grid -->

      <!-- ─────────────────────────────────────
     MATCH 2 · BURNLEY vs MAN CITY
───────────────────────────────────────── -->
      <div
        class="match-divider"
        id="m2"
        style="color: var(--mci); margin-top: 20px">
        <div
          class="md-line"
          style="
            background: linear-gradient(
              90deg,
              transparent,
              rgba(108, 171, 221, 0.55)
            );
          "></div>
        🏆 MATCH 2 · TURF MOOR · 20:00 · TITLE RACE + RELEGATION CONFIRMED?
        <div
          class="md-line"
          style="
            background: linear-gradient(
              90deg,
              rgba(108, 171, 221, 0.55),
              transparent
            );
          "></div>
      </div>

      <div
        class="mhero"
        style="
          background: linear-gradient(
            135deg,
            var(--bur-l) 0%,
            var(--bg1) 50%,
            var(--mci-l) 100%
          );
          border: 1px solid rgba(255, 255, 255, 0.09);
          margin-top: 0;
        ">
        <div class="mhero-inner">
          <div class="meta-chips">
            <span
              class="chip"
              style="
                color: var(--mci);
                border-color: rgba(108, 171, 221, 0.4);
                background: rgba(108, 171, 221, 0.1);
              "
              >Turf Moor · Burnley</span
            >
            <span
              class="chip"
              style="
                color: #ff9933;
                border-color: rgba(255, 153, 51, 0.3);
                background: rgba(255, 153, 51, 0.07);
              "
              >🚨 Burnley relegated if they lose</span
            >
            <span
              class="chip"
              style="
                color: var(--pl-gr);
                border-color: rgba(0, 255, 133, 0.28);
                background: rgba(0, 255, 133, 0.07);
              "
              >🏆 City can go TOP if win by 2+</span
            >
          </div>
          <div class="mot" style="max-width: 600px; width: 100%">
            <span class="mot-tag">🏠 Burnley</span>
            <div class="mot-bar">
              <div
                class="mot-fill"
                id="m2-bur"
                style="
                  width: 0;
                  background: linear-gradient(90deg, var(--bur), var(--bur2));
                "></div>
            </div>
            <span class="mot-pct" style="color: #cc7733">55%</span>
            <span
              style="
                font-size: 9px;
                color: var(--dim);
                padding: 0 7px;
                white-space: nowrap;
              "
              >MOTIVATION</span
            >
            <div class="mot-bar">
              <div
                class="mot-fill"
                id="m2-mci"
                style="
                  width: 0;
                  background: linear-gradient(90deg, #4a90d0, var(--mci));
                "></div>
            </div>
            <span class="mot-pct" style="color: var(--mci)">97%</span>
            <span class="mot-tag">Man City 🏆</span>
          </div>
          <div class="teams">
            <div class="tc">
              <div class="badge" style="animation-delay: 0.05s">
                <img
                  src="https://cdn.brandfetch.io/idATU8hDrd/theme/dark/logo.svg?c=1bxid64Mup7aczewSAYMX&t=1668077989078"
                  alt="BUR"
                  style="background: transparent" />
              </div>
              <div class="tname" style="color: #cc7733">Burnley FC</div>
              <div class="tmeta">0 home wins in 12 games<br />Relegated
                if they lose
              </div>
            </div>
            <div class="vs-c">
              <div class="vs">V</div>
              <div class="ko">20:00</div>
              <div class="venue">
                Turf Moor · Burnley<br />Ref: Andy Madley<br />~21,944 capacity
              </div>
            </div>
            <div class="tc">
              <div class="badge" style="animation-delay: 0.12s">
                <img
                  src="https://cdn.brandfetch.io/idNRR8KZnO/theme/dark/logo.svg?c=1bxid64Mup7aczewSAYMX&t=1668077960626"
                  alt="MCI"
                  style="background: transparent" />
              </div>
              <div class="tname" style="color: var(--mci)">Manchester City</div>
              <div class="tmeta">Win 2+ goals go TOP of PL<br />10-game PL unbeaten run
              </div>
            </div>
          </div>
          <div class="odds-row">
            <div class="odds-box">
              <div class="ob-lbl">Burnley Win</div>
              <div class="ob-odds" style="color: #cc7733">17/1</div>
              <div class="ob-impl">~6% implied</div>
            </div>
            <div class="odds-box">
              <div class="ob-lbl">Draw</div>
              <div class="ob-odds" style="color: var(--med)">8/1</div>
              <div class="ob-impl">~11% implied</div>
            </div>
            <div class="odds-box ob-val">
              <div class="ob-lbl">★ City Win</div>
              <div class="ob-odds" style="color: var(--mci)">1/6</div>
              <div class="ob-impl">~86% implied</div>
            </div>
            <div class="odds-box ob-val">
              <div class="ob-lbl">★ Over 3.5 Goals</div>
              <div class="ob-odds" style="color: var(--lo)">19/20</div>
              <div class="ob-impl">~51% implied · Value</div>
            </div>
          </div>
        </div>
      </div>

      <!-- Grid cards M2 -->
      <div class="cgrid" style="margin-top: 16px">
        <!-- Context M2 -->
        <div class="card span2" style="animation-delay: 0.07s">
          <div class="card-hd">
            <div class="hd-dot" style="background: var(--mci)"></div>
            <div class="hd-t">
              Match Context · Maximum Stakes Both Ends of the Table
            </div>
            <div
              class="hd-tag"
              style="
                color: var(--hot);
                border-color: rgba(245, 81, 42, 0.3);
                background: rgba(245, 81, 42, 0.09);
              ">
              MAXIMUM MISMATCH
            </div>
          </div>
          <div class="cb">
            <div class="ctx">
              <span
                class="kbadge"
                style="
                  color: var(--mci);
                  border-color: rgba(108, 171, 221, 0.4);
                  background: rgba(108, 171, 221, 0.1);
                "
                >Man City</span
              >
              2nd, 67pts —
              <strong>3 points behind Arsenal with a game in hand</strong>. A
              win by 2+ goals sends City to the TOP of the PL for the first time
              since August. Guardiola's men have won 4 straight in all
              competitions — Liverpool (4-0 FAC), Chelsea (3-0 PL), Arsenal (EFL
              Cup Final 2-0), Arsenal (PL 2-1) — scoring
              <strong
                >11 goals in those 4 games while conceding just once</strong
              >. City are unbeaten in
              <strong>29 consecutive PL games against promoted sides</strong>
              and in their last
              <strong>14 straight meetings vs Burnley</strong> (45-6 aggregate).
              Rodri (calf — out), Gvardiol (leg — out), Dias (thigh — out) are
              the notable absences but City's depth means their starting XI
              remains elite.
              <strong>Goal difference could decide the title</strong> —
              Guardiola will push for a large win.<br /><br />
              <span
                class="kbadge"
                style="
                  color: #cc7733;
                  border-color: rgba(204, 85, 0, 0.4);
                  background: rgba(204, 85, 0, 0.1);
                "
                >Burnley</span
              >
              19th, 20pts — <strong>relegated if they lose tonight</strong>.
              They've had 1 PL win in their last 24 games, 0 home wins in 12,
              and 3 consecutive defeats including a 4-1 hammering at Nottingham
              Forest on Sunday. Their squad is decimated:
              <strong
                >Cullen (ACL — season), Mejbri, Beyer, Roberts, Amdouni</strong
              >
              all out; <strong>Tuanzebe (heel — doubt)</strong>. Burnley have
              the worst defence in the PL (67 goals conceded) and the
              <strong>league's lowest xG</strong>. Their only realistic plan is
              a siege mentality with a 5-3-2 formation — but that has repeatedly
              failed against top sides. Flemming (9 PL goals) is their only
              genuine attacking threat.
              <span class="kbadge kw">⚠ RELEGATION CONFIRMED if City win</span>
            </div>
          </div>
        </div>

        <!-- Last 5 M2 -->
        <div class="card" style="animation-delay: 0.1s">
          <div class="card-hd">
            <div class="hd-dot" style="background: var(--mci)"></div>
            <div class="hd-t">Last 5 Matches — All Competitions</div>
          </div>
          <div class="cb">
            <div class="form-cols">
              <div>
                <div class="ftl" style="color: #cc7733">
                  <img
                    class="fti"
                    src="https://cdn.brandfetch.io/idATU8hDrd/theme/dark/logo.svg?c=1bxid64Mup7aczewSAYMX&t=1668077989078"
                    alt="BUR"
                    style="background: transparent"
                    alt=""
                    style="background: transparent" />Burnley
                </div>
                <div class="frlist">
                  <div class="fr">
                    <div class="rd L"></div>
                    <div class="fsc">1–4</div>
                    <div class="fopp">Nottm Forest</div>
                    <div class="fcp">PL Away</div>
                  </div>
                  <div class="fr">
                    <div class="rd L"></div>
                    <div class="fsc">0–2</div>
                    <div class="fopp">Brighton</div>
                    <div class="fcp">PL Home</div>
                  </div>
                  <div class="fr">
                    <div class="rd L"></div>
                    <div class="fsc">1–3</div>
                    <div class="fopp">Fulham</div>
                    <div class="fcp">PL Away</div>
                  </div>
                  <div class="fr">
                    <div class="rd D"></div>
                    <div class="fsc">0–0</div>
                    <div class="fopp">Bournemouth</div>
                    <div class="fcp">PL Home</div>
                  </div>
                  <div class="fr">
                    <div class="rd L"></div>
                    <div class="fsc">3–4</div>
                    <div class="fopp">Brentford</div>
                    <div class="fcp">PL Away</div>
                  </div>
                </div>
              </div>
              <div>
                <div class="ftl" style="color: var(--mci)">
                  <img
                    class="fti"
                    src="https://upload.wikimedia.org/wikipedia/en/thumb/e/eb/Manchester_City_FC_badge.svg/120px-Manchester_City_FC_badge.svg.png"
                    alt=""
                    style="background: transparent" />Man City
                </div>
                <div class="frlist">
                  <div class="fr">
                    <div class="rd W"></div>
                    <div class="fsc">2–1</div>
                    <div class="fopp">Arsenal</div>
                    <div class="fcp">
                      PL Home <span class="ftg">Title D</span>
                    </div>
                  </div>
                  <div class="fr">
                    <div class="rd W"></div>
                    <div class="fsc">3–0</div>
                    <div class="fopp">Chelsea</div>
                    <div class="fcp">PL Away</div>
                  </div>
                  <div class="fr">
                    <div class="rd W"></div>
                    <div class="fsc">2–0</div>
                    <div class="fopp">Arsenal</div>
                    <div class="fcp">EFL Cup Final</div>
                  </div>
                  <div class="fr">
                    <div class="rd W"></div>
                    <div class="fsc">4–0</div>
                    <div class="fopp">Liverpool</div>
                    <div class="fcp">FAC</div>
                  </div>
                  <div class="fr">
                    <div class="rd W"></div>
                    <div class="fsc">5–1</div>
                    <div class="fopp">Burnley</div>
                    <div class="fcp">PL Home (Sep 25)</div>
                  </div>
                </div>
              </div>
            </div>
            <div class="fleg">
              <div class="fli">
                <div class="fld" style="background: var(--lo)"></div>
                Win
              </div>
              <div class="fli">
                <div class="fld" style="background: var(--med)"></div>
                Draw
              </div>
              <div class="fli">
                <div class="fld" style="background: var(--hot)"></div>
                Loss
              </div>
            </div>
            <div class="sn">
              <strong>Contrast:</strong> City W4 straight, 11 goals scored, 1
              conceded. Burnley L3, D1, L1 in last 5 — 3 goals scored, 13
              conceded. City's last visit here in the reverse fixture produced a
              5-1 win with Haaland scoring a brace. City unbeaten in April since
              2021 (W30, D3 from 33 April games).
            </div>
          </div>
        </div>

        <!-- H2H M2 -->
        <div class="card" style="animation-delay: 0.12s">
          <div class="card-hd">
            <div class="hd-dot" style="background: var(--hot)"></div>
            <div class="hd-t">Head to Head — Last 5 Meetings</div>
            <div
              class="hd-tag"
              style="
                color: var(--hot);
                border-color: rgba(245, 81, 42, 0.3);
                background: rgba(245, 81, 42, 0.09);
              ">
              City W14 straight · 45-6 aggregate
            </div>
          </div>
          <div class="cb">
            <div class="h2h-sum">
              <div class="hs">
                <div class="hn" style="color: #cc7733">0</div>
                <div class="hl">Burnley W</div>
              </div>
              <div class="hs">
                <div class="hn" style="color: var(--med)">0</div>
                <div class="hl">Draws</div>
              </div>
              <div class="hs">
                <div class="hn" style="color: var(--mci)">5</div>
                <div class="hl">City W</div>
              </div>
              <div class="hs">
                <div class="hn">4.2</div>
                <div class="hl">Avg Goals</div>
              </div>
            </div>
            <div class="h2hr-list">
              <div class="h2hr">
                <div class="rh">Man City</div>
                <div class="rs">5–1</div>
                <div class="ra">Burnley</div>
                <div class="rx">PL Sep 2025 (Etihad) — Haaland brace</div>
              </div>
              <div class="h2hr">
                <div class="rh">Burnley</div>
                <div class="rs">0–3</div>
                <div class="ra">Man City</div>
                <div class="rx">PL Feb 2024 (Turf Moor)</div>
              </div>
              <div class="h2hr">
                <div class="rh">Burnley</div>
                <div class="rs">0–2</div>
                <div class="ra">Man City</div>
                <div class="rx">PL Oct 2023 (Turf Moor)</div>
              </div>
              <div class="h2hr">
                <div class="rh">Man City</div>
                <div class="rs">3–0</div>
                <div class="ra">Burnley</div>
                <div class="rx">PL Apr 2023 (Etihad)</div>
              </div>
              <div class="h2hr">
                <div class="rh">Burnley</div>
                <div class="rs">0–1</div>
                <div class="ra">Man City</div>
                <div class="rx">PL Feb 2023 (Turf Moor)</div>
              </div>
            </div>
            <div class="sn">
              City led at HT in ALL 5 of the last 5 meetings. City have scored
              2+ goals in each of the <strong>last 11 H2H</strong>. 14
              consecutive wins overall vs Burnley (51-3 aggregate). Burnley have
              not won vs City since 2016. The last two meetings at Turf Moor
              ended <strong>0-2 and 0-3</strong>. 3 of last 4 H2H produced 4+
              goals.
            </div>
          </div>
        </div>

        <!-- Season Avgs M2 -->
        <div class="card" style="animation-delay: 0.14s">
          <div class="card-hd">
            <div class="hd-dot" style="background: #a78bfa"></div>
            <div class="hd-t">Season Averages — PL 2025/26</div>
          </div>
          <div class="cb">
            <div class="avgs-pair">
              <div>
                <div
                  class="avlbl"
                  style="
                    color: #fff;
                    background: rgba(110, 59, 31, 0.25);
                    border: 1px solid rgba(204, 85, 0, 0.4);
                  ">
                  Burnley
                </div>
                <div class="acells">
                  <div class="ac">
                    <div class="av">9.9</div>
                    <div class="al">Shots/gm</div>
                  </div>
                  <div class="ac">
                    <div class="av">3.0</div>
                    <div class="al">SOT/gm</div>
                  </div>
                  <div class="ac">
                    <div class="av">4.4</div>
                    <div class="al">Corners/gm</div>
                  </div>
                  <div class="ac">
                    <div class="av">13.5</div>
                    <div class="al">Fouls/gm</div>
                  </div>
                  <div class="ac">
                    <div class="av">0.94</div>
                    <div class="al">Gls/home</div>
                  </div>
                  <div class="ac">
                    <div class="av">4</div>
                    <div class="al">Clean sheets</div>
                  </div>
                </div>
              </div>
              <div>
                <div
                  class="avlbl"
                  style="
                    color: #fff;
                    background: rgba(108, 171, 221, 0.18);
                    border: 1px solid rgba(108, 171, 221, 0.4);
                  ">
                  Man City
                </div>
                <div class="acells">
                  <div class="ac">
                    <div class="av">16.1</div>
                    <div class="al">Shots away</div>
                  </div>
                  <div class="ac">
                    <div class="av">5.5</div>
                    <div class="al">SOT away</div>
                  </div>
                  <div class="ac">
                    <div class="av">6.5</div>
                    <div class="al">Corners/gm</div>
                  </div>
                  <div class="ac">
                    <div class="av">9.5</div>
                    <div class="al">Fouls/gm</div>
                  </div>
                  <div class="ac">
                    <div class="av">2.0</div>
                    <div class="al">Gls/away</div>
                  </div>
                  <div class="ac">
                    <div class="av">23</div>
                    <div class="al">Haaland goals</div>
                  </div>
                </div>
              </div>
            </div>
            <div class="xg-row">
              <div class="xgi">
                <div class="xgv" style="color: #cc7733">0.94</div>
                <div class="xgl">Burnley xG/home</div>
              </div>
              <div class="xgi">
                <div class="xgv" style="color: var(--hot)">1.6</div>
                <div class="xgl">Burnley goals conceded/home</div>
              </div>
              <div class="xgi">
                <div class="xgv" style="color: var(--mci)">1.36</div>
                <div class="xgl">City xG vs Arsenal</div>
              </div>
              <div class="xgi">
                <div class="xgv" style="color: var(--lo)">2.0</div>
                <div class="xgl">City gls/away gm</div>
              </div>
              <div class="xgi">
                <div class="xgv" style="color: var(--med)">7</div>
                <div class="xgl">Haaland goals vs Burnley (3 starts)</div>
              </div>
            </div>
            <div class="sn">
              Burnley have the <strong>worst defence</strong> in PL (67 goals
              conceded, 25 at Turf Moor). City concede just 0.8 goals/away game
              (2nd best PL). Burnley have the
              <strong>lowest xG in the league</strong>. Dubravka has 114 saves —
              most in the PL by +16, showing how much he has had to do to keep
              Burnley even at 67 conceded.
            </div>
          </div>
        </div>

        <!-- Home/Away M2 -->
        <div class="card" style="animation-delay: 0.16s">
          <div class="card-hd">
            <div class="hd-dot" style="background: var(--lo)"></div>
            <div class="hd-t">Home / Away Performance Splits</div>
          </div>
          <div class="cb">
            <div class="avgs-pair">
              <div>
                <div
                  class="avlbl"
                  style="
                    color: #fff;
                    background: rgba(110, 59, 31, 0.25);
                    border: 1px solid rgba(204, 85, 0, 0.4);
                  ">
                  Burnley @ Home
                </div>
                <div class="acells">
                  <div class="ac">
                    <div class="av">2</div>
                    <div class="al">PL Home W</div>
                  </div>
                  <div class="ac">
                    <div class="av">12</div>
                    <div class="al">Home winless streak</div>
                  </div>
                  <div class="ac">
                    <div class="av">25</div>
                    <div class="al">Goals conceded home</div>
                  </div>
                  <div class="ac">
                    <div class="av">0.69</div>
                    <div class="al">Pts/home gm</div>
                  </div>
                  <div class="ac">
                    <div class="av">Oct</div>
                    <div class="al">Last home win</div>
                  </div>
                  <div class="ac">
                    <div class="av">4</div>
                    <div class="al">Home draws</div>
                  </div>
                </div>
              </div>
              <div>
                <div
                  class="avlbl"
                  style="
                    color: #fff;
                    background: rgba(108, 171, 221, 0.18);
                    border: 1px solid rgba(108, 171, 221, 0.4);
                  ">
                  City Away
                </div>
                <div class="acells">
                  <div class="ac">
                    <div class="av">21</div>
                    <div class="al">Away pts since Dec</div>
                  </div>
                  <div class="ac">
                    <div class="av">1.06</div>
                    <div class="al">Goals conceded away</div>
                  </div>
                  <div class="ac">
                    <div class="av">1.75</div>
                    <div class="al">Pts/away gm</div>
                  </div>
                  <div class="ac">
                    <div class="av">29</div>
                    <div class="al">Unbeaten vs promoted</div>
                  </div>
                  <div class="ac">
                    <div class="av">14</div>
                    <div class="al">Consec wins vs BUR</div>
                  </div>
                  <div class="ac">
                    <div class="av">W30</div>
                    <div class="al">April record (33 gms)</div>
                  </div>
                </div>
              </div>
            </div>
            <div class="sn">
              City have collected
              <strong>21 away points since December</strong> — more than any
              other PL team. They are unbeaten in 29 consecutive league games vs
              promoted sides. Burnley have
              <strong>not won at Turf Moor since October</strong>. City unbeaten
              in April since 2021 — a remarkable streak of 30 wins and 3 draws
              from 33 April games.
            </div>
          </div>
        </div>

        <!-- Prediction Table M2 -->
        <div class="card span2" style="animation-delay: 0.18s">
          <div class="card-hd">
            <div class="hd-dot" style="background: var(--mci)"></div>
            <div class="hd-t">
              Weighted Stat Predictions — Burnley vs Man City
            </div>
          </div>
          <div class="cb">
            <div class="pt-keys">
              <div class="ptk">
                <div class="ptkd" style="background: var(--lo)"></div>
                <span style="color: var(--lo); font-weight: 700">Low</span>
              </div>
              <div class="ptk">
                <div class="ptkd" style="background: var(--med)"></div>
                <span style="color: var(--med); font-weight: 700">Median</span>
              </div>
              <div class="ptk">
                <div class="ptkd" style="background: var(--hot)"></div>
                <span style="color: var(--hot); font-weight: 700">High</span>
              </div>
              <div
                class="ptk"
                style="margin-left: auto; font-size: 10px; color: var(--dim)">
                Ref: Andy Madley · City GD matters for title
              </div>
            </div>
            <div class="ptw">
              <table class="ptbl">
                <colgroup>
                  <col style="width: 22%" />
                  <col style="width: 13%" />
                  <col style="width: 13%" />
                  <col style="width: 10%" />
                  <col style="width: 12%" />
                  <col style="width: 10%" />
                  <col style="width: 20%" />
                </colgroup>
                <thead>
                  <th>Metric</th>
                  <th class="tv" style="color: #cc7733;text-align: center;">Burnley</th>
                  <th class="tv" style="color: var(--mci);text-align: center;">City</th>
                  <th class="tv" style="color: var(--lo);text-align: center;">Low</th>
                  <th class="tv" style="color: var(--med);text-align: center;">Median</th>
                  <th class="tv" style="color: var(--hot);text-align: center;">High</th>
                  <th class="tv" style="color: var(--dim);text-align: center;">Bar</th>
                </thead>
                <tbody>
                  <tr>
                    <td class="tn">🔲 Corners</td>
                    <td class="tv">
                      <div class="tsc">
                        <span class="tsv" style="color: #cc7733">3</span
                        ><span class="tsl">med</span>
                      </div>
                    </td>
                    <td class="tv">
                      <div class="tsc">
                        <span class="tsv" style="color: var(--mci)">7</span
                        ><span class="tsl">med</span>
                      </div>
                    </td>
                    <td class="tv"><span class="vlo">7</span></td>
                    <td class="tv"><span class="vmd">10</span></td>
                    <td class="tv"><span class="vhi">16</span></td>
                    <td>
                      <div class="rb">
                        <div
                          class="rbf"
                          data-p="64"
                          style="
                            background: linear-gradient(
                              90deg,
                              var(--bur2),
                              var(--mci)
                            );
                          "></div>
                      </div>
                    </td>
                  </tr>
                  <tr>
                    <td class="tn">📊 Total Shots</td>
                    <td class="tv">
                      <div class="tsc">
                        <span class="tsv" style="color: #cc7733">8</span
                        ><span class="tsl">med</span>
                      </div>
                    </td>
                    <td class="tv">
                      <div class="tsc">
                        <span class="tsv" style="color: var(--mci)">18</span
                        ><span class="tsl">med</span>
                      </div>
                    </td>
                    <td class="tv"><span class="vlo">20</span></td>
                    <td class="tv"><span class="vmd">26</span></td>
                    <td class="tv"><span class="vhi">38</span></td>
                    <td>
                      <div class="rb">
                        <div
                          class="rbf"
                          data-p="78"
                          style="
                            background: linear-gradient(
                              90deg,
                              var(--bur2),
                              var(--mci)
                            );
                          "></div>
                      </div>
                    </td>
                  </tr>
                  <tr>
                    <td class="tn">🎯 Shots on Target</td>
                    <td class="tv">
                      <div class="tsc">
                        <span class="tsv" style="color: #cc7733">3</span
                        ><span class="tsl">med</span>
                      </div>
                    </td>
                    <td class="tv">
                      <div class="tsc">
                        <span class="tsv" style="color: var(--mci)">7</span
                        ><span class="tsl">med</span>
                      </div>
                    </td>
                    <td class="tv"><span class="vlo">6</span></td>
                    <td class="tv"><span class="vmd">10</span></td>
                    <td class="tv"><span class="vhi">18</span></td>
                    <td>
                      <div class="rb">
                        <div
                          class="rbf"
                          data-p="74"
                          style="
                            background: linear-gradient(
                              90deg,
                              var(--bur2),
                              var(--mci)
                            );
                          "></div>
                      </div>
                    </td>
                  </tr>
                  <tr>
                    <td class="tn">⚠️ Fouls</td>
                    <td class="tv">
                      <div class="tsc">
                        <span class="tsv" style="color: #cc7733">14</span
                        ><span class="tsl">med</span>
                      </div>
                    </td>
                    <td class="tv">
                      <div class="tsc">
                        <span class="tsv" style="color: var(--mci)">10</span
                        ><span class="tsl">med</span>
                      </div>
                    </td>
                    <td class="tv"><span class="vlo">16</span></td>
                    <td class="tv"><span class="vmd">24</span></td>
                    <td class="tv"><span class="vhi">36</span></td>
                    <td>
                      <div class="rb">
                        <div
                          class="rbf"
                          data-p="72"
                          style="
                            background: linear-gradient(
                              90deg,
                              var(--bur2),
                              var(--mci)
                            );
                          "></div>
                      </div>
                    </td>
                  </tr>
                  <tr>
                    <td class="tn">↗️ Throw-ins</td>
                    <td class="tv">
                      <div class="tsc">
                        <span class="tsv" style="color: #cc7733">19</span
                        ><span class="tsl">med</span>
                      </div>
                    </td>
                    <td class="tv">
                      <div class="tsc">
                        <span class="tsv" style="color: var(--mci)">20</span
                        ><span class="tsl">med</span>
                      </div>
                    </td>
                    <td class="tv"><span class="vlo">28</span></td>
                    <td class="tv"><span class="vmd">39</span></td>
                    <td class="tv"><span class="vhi">54</span></td>
                    <td>
                      <div class="rb">
                        <div
                          class="rbf"
                          data-p="64"
                          style="
                            background: linear-gradient(
                              90deg,
                              var(--bur2),
                              var(--mci)
                            );
                          "></div>
                      </div>
                    </td>
                  </tr>
                  <tr>
                    <td class="tn">🥅 Goal Kicks</td>
                    <td class="tv">
                      <div class="tsc">
                        <span class="tsv" style="color: #cc7733">12</span
                        ><span class="tsl">med</span>
                      </div>
                    </td>
                    <td class="tv">
                      <div class="tsc">
                        <span class="tsv" style="color: var(--mci)">8</span
                        ><span class="tsl">med</span>
                      </div>
                    </td>
                    <td class="tv"><span class="vlo">14</span></td>
                    <td class="tv"><span class="vmd">20</span></td>
                    <td class="tv"><span class="vhi">28</span></td>
                    <td>
                      <div class="rb">
                        <div
                          class="rbf"
                          data-p="60"
                          style="
                            background: linear-gradient(
                              90deg,
                              var(--bur2),
                              var(--mci)
                            );
                          "></div>
                      </div>
                    </td>
                  </tr>
                  <tr>
                    <td class="tn">⚔️ Tackles</td>
                    <td class="tv">
                      <div class="tsc">
                        <span class="tsv" style="color: #cc7733">18</span
                        ><span class="tsl">med</span>
                      </div>
                    </td>
                    <td class="tv">
                      <div class="tsc">
                        <span class="tsv" style="color: var(--mci)">14</span
                        ><span class="tsl">med</span>
                      </div>
                    </td>
                    <td class="tv"><span class="vlo">22</span></td>
                    <td class="tv"><span class="vmd">32</span></td>
                    <td class="tv"><span class="vhi">46</span></td>
                    <td>
                      <div class="rb">
                        <div
                          class="rbf"
                          data-p="68"
                          style="
                            background: linear-gradient(
                              90deg,
                              var(--bur2),
                              var(--mci)
                            );
                          "></div>
                      </div>
                    </td>
                  </tr>
                </tbody>
              </table>
            </div>
            <div class="sn" style="margin-top: 10px">
              <strong>Key weightings:</strong> City dominant in shots/SOT
              (massive asymmetry — avg 16.1 away vs Burnley's 9.9). Burnley earn
              corners in 7 straight games (avg 4.4). City avg 6.5 corners/gm.
              Tackles elevated by Burnley's desperate defensive work. Fouls up
              from Burnley's increasingly desperate defending as goals flow.
              Burnley concede an avg 5.4 corners/gm. Goal kicks high for Burnley
              from Dubravka's distribution.
            </div>
          </div>
        </div>

        <!-- Score M2 -->
        <div class="card" style="animation-delay: 0.2s">
          <div class="card-hd">
            <div class="hd-dot" style="background: var(--med)"></div>
            <div class="hd-t">Score Prediction · Title Race Context</div>
          </div>
          <div class="cb">
            <div class="sz">
              <div class="szh">Burnley vs Manchester City · Turf Moor</div>
              <div class="sboxes">
                <div class="sbox">
                  <div class="sbl">Half-Time</div>
                  <div class="sbs">0–2</div>
                  <div class="sbp">City lead ~52%</div>
                </div>
                <div class="sbox feat">
                  <div class="sbl">Full-Time ★ Best Pick</div>
                  <div class="sbs feat">0–4</div>
                  <div class="sbp">City ~24% — GD matters</div>
                </div>
                <div class="sbox">
                  <div class="sbl">Alt: City 3-1</div>
                  <div class="sbs">1–3</div>
                  <div class="sbp">BTTS ~28% · Burnley scored last 2 H2H</div>
                </div>
              </div>
              <div class="sz-note">
                <strong>Why 0-4 City:</strong> City have won by 4+ goals in the
                reverse fixture (5-1). They need goals for goal difference — if
                this title goes to the wire, every single goal counts. Guardiola
                will not take his foot off the gas. Haaland has scored in all 3
                starts vs Burnley (7 goals). City led at HT in ALL of the last 5
                H2H. Burnley's home record is catastrophic (0 wins in 12, 25
                goals conceded). Their missing squad players (Cullen, Mejbri,
                Beyer, Roberts, Amdouni) leave them woefully short in quality.
                However, Burnley have scored in their last 2 H2H meetings — a
                Flemming goal to make it respectable is plausible but unlikely
                to significantly change the outcome. City's title-race
                desperation for goals makes 4+ the highest probability
                large-margin outcome.
              </div>
              <div class="safe-box">
                <strong
                  >🛡 Safe Picks — City Win (-3 Handicap, 11/4) + Over 3.5 Goals
                  (19/20):</strong
                >
                City have won by more than one goal vs Burnley in each of their
                past <strong>11 meetings</strong>. Over 3.5 goals in 3 of last 4
                H2H. City scoring 11 goals in last 4 games. Burnley the worst
                defence in the league. For maximum value:
                <strong>Haaland anytime scorer</strong> (~1/3) is near-certain
                given 7 goals in 3 starts vs Burnley. The -3 handicap at 11/4 is
                the sophisticated play for those seeking enhanced value beyond
                1/6 on City win alone.
              </div>
            </div>
          </div>
        </div>

        <!-- Yellow Cards M2 -->
        <div class="card" style="animation-delay: 0.22s">
          <div class="card-hd">
            <div class="hd-dot" style="background: #ffe84a"></div>
            <div class="hd-t">🟨 Yellow Card Risk Players</div>
            <div
              class="hd-tag"
              style="
                color: var(--med);
                border-color: rgba(247, 202, 56, 0.3);
                background: rgba(247, 202, 56, 0.07);
              ">
              Ref: Andy Madley
            </div>
          </div>
          <div class="cb">
            <div class="ycl">
              <div class="yc">
                <div class="yci">🟨</div>
                <div class="ycinf">
                  <div class="ycn">
                    James Ward-Prowse
                    <span class="ycc" style="color: #cc7733">Burnley · CM</span>
                  </div>
                  <div class="ycr">
                    7 PL yellows this season. Burnley's midfield anchor who will
                    foul desperately to break City's relentless attacks. Faces
                    Cherki and Doku's quick transitions — professional fouls
                    inevitable. Also earns bookings from protest/reaction to
                    decisions.
                  </div>
                </div>
                <div class="rb-tag r-hi">HIGH</div>
              </div>
              <div class="yc">
                <div class="yci">🟨</div>
                <div class="ycinf">
                  <div class="ycn">
                    Florentino Luís
                    <span class="ycc" style="color: #cc7733">Burnley · DM</span>
                  </div>
                  <div class="ycr">
                    Physical DM who tackles recklessly when outpaced. Faces
                    City's relentless 4-2-3-1 movement — will be dragged into
                    lunging challenges when City breaks at speed through the
                    lines.
                  </div>
                </div>
                <div class="rb-tag r-hi">HIGH</div>
              </div>
              <div class="yc">
                <div class="yci">🟨</div>
                <div class="ycinf">
                  <div class="ycn">
                    Lesley Ugochukwu
                    <span class="ycc" style="color: #cc7733">Burnley · CM</span>
                  </div>
                  <div class="ycr">
                    Young CM who gives away fouls through over-aggression. With
                    Burnley being gradually torn apart by City's pressing,
                    Ugochukwu will foul early and often to slow the game.
                    Burnley's card-prone midfield generally spikes yellows in
                    the 76-90 minute phase as frustration builds.
                  </div>
                </div>
                <div class="rb-tag r-md">MED</div>
              </div>
              <div class="yc">
                <div class="yci">🟨</div>
                <div class="ycinf">
                  <div class="ycn">
                    Nico González
                    <span class="ycc" style="color: var(--mci)"
                      >Man City · CM</span
                    >
                  </div>
                  <div class="ycr">
                    With Rodri out, González takes over the holding role. He
                    commits tactical fouls when City are on the break and need
                    to keep the ball safe. Earns yellow from Burnley's
                    desperation pressing in the second half when they're chasing
                    the game.
                  </div>
                </div>
                <div class="rb-tag r-md">MED</div>
              </div>
            </div>
          </div>
        </div>

        <!-- Betting M2 -->
        <div class="card span2" style="animation-delay: 0.24s">
          <div class="card-hd">
            <div class="hd-dot" style="background: var(--lo)"></div>
            <div class="hd-t">
              📈 Betting Market Analysis · City Value Picks · Title Race Context
            </div>
          </div>
          <div class="cb">
            <div class="betg">
              <div class="bc bv">
                <div class="bcm">★ Best Value</div>
                <div class="bcl gv">Over 3.5 Goals 19/20</div>
                <div class="bcr">
                  3 of last 4 H2H produced 4+ goals. City scored 11 in 4 games.
                  Burnley worst defence. City's GD title-race incentive. 39% of
                  Burnley matches hit O3.5 this season.
                </div>
              </div>
              <div class="bc bv">
                <div class="bcm">★ Handicap</div>
                <div class="bcl yv">City -3 Handicap 11/4</div>
                <div class="bcr">
                  City have won by more than 1 goal in each of the last 11 H2H
                  meetings. Won reverse fixture 5-1. Title GD pressure means
                  Guardiola won't hold back. Beats the short 1/6 City Win odds.
                </div>
              </div>
              <div class="bc bv">
                <div class="bcm">★ Prop Best Bet</div>
                <div class="bcl yv">Haaland Anytime ~1/3</div>
                <div class="bcr">
                  7 goals in 3 starts vs Burnley (one every 36 mins). 23 PL
                  goals this season. Burnley have conceded 25 at Turf Moor.
                  Near-certainty at these odds.
                </div>
              </div>
              <div class="bc bv">
                <div class="bcm">★ Prop Enhanced</div>
                <div class="bcl yv">Haaland 2+ Goals 15/8</div>
                <div class="bcr">
                  Scored brace in reverse fixture (5-1). City title ambitions
                  mean playing time for Haaland. He's scored in every H2H start.
                  15/8 is strong value given his Burnley record.
                </div>
              </div>
              <div class="bc">
                <div class="bcm">Corners</div>
                <div class="bcl">Over 9.5 Corners</div>
                <div class="bcr">
                  City avg 6.5/gm (3rd highest PL). Burnley's 2.5 corner line
                  covered 7 straight. City concede 3.9 corners. Combined median
                  10 exceeds the line. Recommended by Covers analysts.
                </div>
              </div>
              <div class="bc">
                <div class="bcm">Correct Score</div>
                <div class="bcl">City 4-0</div>
                <div class="bcr">
                  At 9/1 per Football Whispers. City won the reverse 5-1, last
                  Turf Moor visit was 3-0 and 2-0. A clean sheet from City is
                  very plausible given Burnley's lack of cutting edge.
                </div>
              </div>
              <div class="bc bw">
                <div class="bcm">⚠ Avoid</div>
                <div class="bcl rv">Under 2.5 Goals</div>
                <div class="bcr">
                  Only makes sense if City rotate heavily. Even with Rodri out,
                  City's depth is extraordinary. Under 2.5 has no value
                  whatsoever — City scored 2+ in ALL 11 recent H2H.
                </div>
              </div>
              <div class="bc">
                <div class="bcm">Scorer Prop</div>
                <div class="bcl">Rayan Cherki Assist</div>
                <div class="bcr">
                  10 assists in the PL this season (joint-highest). Sets up
                  Haaland consistently. In this type of dominant performance,
                  Cherki's playmaking is central. Good value as assist provider.
                </div>
              </div>
            </div>
            <div class="bn">
              <strong>Overall Assessment:</strong> This is one of the most
              mismatched fixtures in Premier League history — a title-chasing,
              in-form juggernaut against a near-relegated side at their worst.
              The 1/6 for City Win is too short to bet directly.
              <strong
                >The intelligent plays are: Over 3.5 Goals (19/20 — genuine
                value with 3 of 4 H2H hitting O4 goals), the -3 City handicap at
                11/4 (backed by 11 straight wins by 2+), and Haaland 2+ Goals at
                15/8 (7 goals in 3 starts vs Burnley)</strong
              >. For maximum EV in a single bet:
              <strong>Man City Win + Over 3.5 Goals combined</strong> (available
              around 6/5 on most platforms). Burnley's relegation confirmation
              is virtually certain tonight — the question is only the margin.
              Recommended allocation: 40% O3.5 Goals, 35% City -3 handicap, 25%
              Haaland 2+ goals.
            </div>
          </div>
        </div>

        <!-- Analyst Notes M2 -->
        <div class="card span2" style="animation-delay: 0.26s">
          <div class="card-hd">
            <div class="hd-dot" style="background: var(--mci)"></div>
            <div class="hd-t">Analyst Notes · Key Matchup Factors</div>
          </div>
          <div class="cb">
            <div class="inb">
              <strong>Goal Difference as a Title Weapon:</strong> If both Man
              City and Arsenal win all their remaining games, the Premier League
              title will be decided on goal difference. Arsenal currently have a
              +1 goal difference advantage over City. Every goal matters —
              Guardiola will almost certainly instruct his team to attack
              relentlessly and not ease off. This effectively turns a routine
              away win into a maximum-goal-scoring exercise against a side with
              the league's worst defence.
            </div>
            <div class="inb">
              <strong>Erling Haaland's Burnley Fixation:</strong> 7 goals in 3
              starts vs Burnley means he scores once every 36 minutes against
              them. He netted a brace in the reverse fixture. Now at 23 PL goals
              and chasing his third consecutive Golden Boot, Burnley represents
              the kind of fixture where he could add 2-3 more. He's missed 2
              open-play goals in 2026 suggesting his finishing is at an elite
              level right now.
            </div>
            <div class="inb">
              <strong>Burnley's Last Stand:</strong> Scott Parker's side have
              been admirable in parts — Dubravka's 114 saves (most in PL by
              +16), Flemming's 9 goals, their fighting spirit shown in draws vs
              Chelsea and Liverpool. But the injuries at this precise moment
              (Cullen, Mejbri, Beyer, Roberts, Amdouni all out) mean Parker
              fields a depleted squad against the best team in Europe this
              month. Dignified farewell is the most realistic outcome tonight.
            </div>
            <div class="inb">
              <strong>City's Rodri Absence Context:</strong> Without Rodri
              (calf), City will deploy Nico González and Bernardo Silva or
              Reijnders in the double pivot. Against Burnley this barely matters
              — their pressing and defensive shape can absorb any loss of
              Rodri's composure. The absence is more concerning for future title
              deciders vs Arsenal than for tonight's match.
            </div>
          </div>
        </div>
      </div>
      <!-- end M2 grid -->
    </div>
    <!-- end wrap -->

    <footer
      style="
        text-align: center;
        padding: 20px 16px;
        font-size: 10px;
        color: var(--dim);
        border-top: 1px solid var(--wire);
        position: relative;
        z-index: 1;
      ">
      <p><strong>Professional Strategy Analytics</strong></p>
      <p style="margin-top: 2px">
        Premier League Matchweek 34 · Wednesday 22 April 2026 · Statistical predictions are weighted
        estimates.<br>
        <strong style="color: var(--hot); font-size: 12px; text-transform: uppercase;"
          >Gamble responsibly. 18+. This is not financial advice.</strong
        >
      </p>
    </footer>

    <script>
      ;(function () {
        'use strict'

        /* Motivation bars */
        setTimeout(() => {
          ;[
            ['m1-bou', 72],
            ['m1-lut', 61],
            ['m2-bur', 55],
            ['m2-mci', 97],
          ].forEach(([id, pct], i) => {
            setTimeout(() => {
              const el = document.getElementById(id)
              if (el) {
                el.style.transition = 'width 1.1s ease'
                el.style.width = pct + '%'
              }
            }, i * 80)
          })
        }, 400)

        /* Prediction bars */
        const fills = document.querySelectorAll('.rbf[data-p]')
        if ('IntersectionObserver' in window) {
          const io = new IntersectionObserver(
            entries => {
              entries.forEach(e => {
                if (e.isIntersecting) {
                  setTimeout(() => {
                    e.target.style.width = e.target.getAttribute('data-p') + '%'
                  }, 200)
                  io.unobserve(e.target)
                }
              })
            },
            { threshold: 0.2 },
          )
          fills.forEach(f => io.observe(f))
        } else {
          fills.forEach(f => (f.style.width = f.getAttribute('data-p') + '%'))
        }

        /* Count-up for avg cells */
        const avs = document.querySelectorAll('.ac .av')
        if ('IntersectionObserver' in window) {
          const io2 = new IntersectionObserver(
            entries => {
              entries.forEach(e => {
                if (e.isIntersecting) {
                  const el = e.target
                  const raw = el.textContent.trim()
                  if (!el.dataset.done) {
                    el.dataset.done = '1'
                    const isPct = raw.includes('%')
                    const num = parseFloat(raw)
                    if (!isNaN(num)) {
                      let c = 0,
                        step = num / (700 / 16)
                      const t = setInterval(() => {
                        c += step
                        if (c >= num) {
                          c = num
                          clearInterval(t)
                        }
                        el.textContent =
                          (raw.includes('.') ? c.toFixed(1) : Math.round(c)) +
                          (isPct ? '%' : '')
                      }, 16)
                    }
                  }
                  io2.unobserve(el)
                }
              })
            },
            { threshold: 0.8 },
          )
          avs.forEach(a => io2.observe(a))
        }

        /* Badge hover delay stagger */
        document.querySelectorAll('.badge').forEach((b, i) => {
          b.style.animationDelay = 0.06 + i * 0.1 + 's'
        })
      })()
    </script>
