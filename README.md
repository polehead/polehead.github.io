<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>
      Premier League MW33 Sunday · Statistical Predictor · 19 April 2026
    </title>
    <link rel="preconnect" href="https://fonts.googleapis.com" />
    <link
      href="https://fonts.googleapis.com/css2?family=Oswald:wght@400;500;600;700&family=Source+Sans+3:wght@300;400;500;600;700&display=swap"
      rel="stylesheet"
    />
    <style>
      /* ═══════════════════════════════════════════
   TOKENS
═══════════════════════════════════════════ */
      :root {
        --bg: #06090f;
        --surf: #0c1018;
        --card: #111520;
        --raised: #181e2c;
        --lift: #1f2638;
        --border: rgba(255, 255, 255, 0.07);
        --bm: rgba(255, 255, 255, 0.12);
        --text: #bcc8de;
        --muted: #3e4d66;
        --label: #7a8daa;
        --bright: #dce7f5;
        --pl-purple: #37003c;
        --pl-green: #00ff85;
        --lo: #12dba6;
        --med: #f6c840;
        --hi: #f54d2a;
        --yel: #ffe84a;
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
        font-family: "Sora", sans-serif;
        background: var(--bg);
        color: var(--text);
        font-size: 14px;
        line-height: 1.55;
        -webkit-font-smoothing: antialiased;
        overflow-x: hidden; /* Prevent horizontal jitter */
      }

      /* Heading font shorthand */
      .f-head {
        font-family: "Oswald", sans-serif;
      }

      /* ═══ ANIMATIONS ═══ */
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
      @keyframes countIn {
        from {
          opacity: 0;
          transform: scale(0.7);
        }
        to {
          opacity: 1;
          transform: scale(1);
        }
      }
      @keyframes barGrow {
        from {
          width: 0 !important;
        }
      }
      @keyframes pulse {
        0%,
        100% {
          opacity: 0.5;
        }
        50% {
          opacity: 1;
        }
      }
      @keyframes shimmer {
        0% {
          background-position: -400px 0;
        }
        100% {
          background-position: 400px 0;
        }
      }

      /* ═══ PAGE HEADER ═══ */
      .ph {
        background: linear-gradient(
          160deg,
          #05081a 0%,
          #0e0333 50%,
          #05081a 100%
        );
        border-bottom: 2px solid rgba(55, 0, 60, 0.9);
        padding: 22px 20px 18px;
        text-align: center;
        position: relative;
        overflow: hidden;
      }
      .ph::after {
        content: "";
        position: absolute;
        inset: 0;
        background: radial-gradient(
          ellipse 130% 60% at 50% -20%,
          rgba(0, 255, 133, 0.07),
          transparent 65%
        );
        pointer-events: none;
      }
      .ph-badge {
        display: inline-flex;
        align-items: center;
        gap: 8px;
        font-family: "Oswald", sans-serif;
        font-size: 10px;
        font-weight: 500;
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
      .ph h1 {
        font-family: "Oswald", sans-serif;
        font-size: clamp(22px, 4vw, 36px);
        font-weight: 700;
        color: #fff;
        letter-spacing: 0.5px;
        line-height: 1.05;
        position: relative;
      }
      .ph h1 em {
        color: var(--pl-green);
        font-style: normal;
      }
      .ph .sub {
        font-size: 12px;
        color: var(--muted);
        margin-top: 6px;
        position: relative;
      }

      /* Nav */
      .ph-nav {
        display: flex;
        flex-wrap: wrap;
        justify-content: center;
        gap: 7px;
        margin-top: 14px;
        position: relative;
      }
      .nav-btn {
        font-family: "Oswald", sans-serif;
        font-size: 10px;
        font-weight: 500;
        letter-spacing: 1px;
        text-transform: uppercase;
        padding: 4px 12px;
        border-radius: 4px;
        border: 1px solid;
        text-decoration: none;
        transition: all 0.2s;
        white-space: nowrap;
      }

      /* Significance banners */
      .sig-strip {
        padding: 9px 20px;
        text-align: center;
        font-size: 11.5px;
        font-weight: 600;
        display: flex;
        align-items: center;
        justify-content: center;
        gap: 8px;
      }

      /* ═══ MATCH CARD ═══ */
      .mc {
        max-width: 1300px;
        margin: 20px auto;
        padding: 0 14px;
        animation: fadeUp 0.5s ease both;
      }
      .mc:nth-child(1) {
        animation-delay: 0.05s;
      }
      .mc:nth-child(2) {
        animation-delay: 0.1s;
      }
      .mc:nth-child(3) {
        animation-delay: 0.15s;
      }
      .mc:nth-child(4) {
        animation-delay: 0.2s;
      }

      .card {
        background: var(--card);
        border: 1px solid var(--border);
        border-radius: 12px;
        overflow: hidden;
        box-shadow: 0 6px 40px rgba(0, 0, 0, 0.45);
        transition: border-color 0.3s;
      }
      .card:hover {
        border-color: var(--bm);
      }

      /* Colour top bar */
      .c-bar {
        height: 4px;
        width: 100%;
      }

      /* ═══ HERO SECTION ═══ */
      .hero {
        padding: 20px 20px 16px;
        display: flex;
        flex-direction: column;
        align-items: center;
        gap: 10px;
        position: relative;
      }
      .hero-meta {
        display: flex;
        gap: 8px;
        align-items: center;
        flex-wrap: wrap;
        justify-content: center;
      }
      .chip {
        font-size: 9.5px;
        font-weight: 700;
        letter-spacing: 1.5px;
        text-transform: uppercase;
        padding: 3px 9px;
        border-radius: 3px;
        border: 1px solid;
      }
      .teams-row {
        display: grid;
        grid-template-columns: 1fr auto 1fr;
        align-items: center;
        gap: 14px;
        width: 100%;
        max-width: 520px;
      }
      .team-col {
        display: flex;
        flex-direction: column;
        align-items: center;
        gap: 6px;
      }
      .badge {
        width: 68px;
        height: 68px;
        border-radius: 50%;
        background: rgba(255, 255, 255, 0.03);
        border: 1px solid var(--bm);
        display: flex;
        align-items: center;
        justify-content: center;
        overflow: hidden;
        transition: transform 0.3s cubic-bezier(0.34, 1.56, 0.64, 1);
        flex-shrink: 0;
      }
      .badge:hover {
        transform: scale(1.1) rotate(4deg);
      }
      .badge img {
        width: 48px;
        height: 48px;
        object-fit: contain;
      }
      .t-name {
        font-family: "Oswald", sans-serif;
        font-size: 13px;
        font-weight: 600;
        text-align: center;
        color: #fff;
        text-transform: uppercase;
        letter-spacing: 0.5px;
      }
      .t-meta {
        font-size: 9.5px;
        color: var(--muted);
        text-align: center;
        line-height: 1.45;
      }
      .vs-col {
        display: flex;
        flex-direction: column;
        align-items: center;
        gap: 4px;
      }
      .vs {
        font-family: "Oswald", sans-serif;
        font-size: 20px;
        font-weight: 700;
        color: rgba(255, 255, 255, 0.09);
        letter-spacing: 2px;
      }
      .ko {
        font-family: "Oswald", sans-serif;
        font-size: 9.5px;
        font-weight: 600;
        letter-spacing: 1.5px;
        color: var(--med);
        background: rgba(246, 200, 64, 0.09);
        border: 1px solid rgba(246, 200, 64, 0.25);
        padding: 2px 8px;
        border-radius: 3px;
      }
      .venue {
        font-size: 8.5px;
        color: var(--muted);
        text-align: center;
        line-height: 1.5;
      }

      /* ═══ GRID LAYOUT ═══ */
      .cg {
        display: grid;
        grid-template-columns: 1fr;
        gap: 0;
      }
      @media (min-width: 860px) {
        .cg {
          grid-template-columns: 1fr 1fr;
        }
        .cg .fw {
          grid-column: 1/-1;
        }
      }

      /* Section block */
      .sb {
        padding: 15px 20px;
        border-top: 1px solid var(--border);
      }
      .sb:nth-child(even) {
        background: rgba(255, 255, 255, 0.015);
      }
      .stitle {
        font-family: "Oswald", sans-serif;
        font-size: 9.5px;
        font-weight: 600;
        letter-spacing: 2px;
        text-transform: uppercase;
        color: var(--muted);
        margin-bottom: 11px;
        display: flex;
        align-items: center;
        gap: 8px;
      }
      .stitle::after {
        content: "";
        flex: 1;
        height: 1px;
        background: var(--border);
      }

      /* Motivation box */
      .mot-box {
        background: rgba(255, 255, 255, 0.03);
        border: 1px solid var(--bm);
        border-radius: 8px;
        padding: 11px 14px;
        font-size: 12.5px;
        line-height: 1.7;
        color: var(--label);
      }
      .mot-box strong {
        color: var(--med);
        font-weight: 700;
      }
      .mot-box .hi-alert {
        display: inline-flex;
        align-items: center;
        gap: 5px;
        padding: 1px 7px;
        border-radius: 3px;
        font-size: 10.5px;
        font-weight: 700;
        background: rgba(245, 77, 42, 0.14);
        border: 1px solid rgba(245, 77, 42, 0.3);
        color: #ff7755;
      }
      .mot-box .hi-info {
        display: inline-flex;
        align-items: center;
        gap: 5px;
        padding: 1px 7px;
        border-radius: 3px;
        font-size: 10.5px;
        font-weight: 700;
        background: rgba(0, 255, 133, 0.08);
        border: 1px solid rgba(0, 255, 133, 0.2);
        color: #00cc70;
      }

      /* Form table */
      .form-cols {
        display: grid;
        grid-template-columns: 1fr 1fr;
        gap: 12px;
      }
      .form-team {
        font-family: "Oswald", sans-serif;
        font-size: 10px;
        font-weight: 600;
        letter-spacing: 1px;
        text-transform: uppercase;
        margin-bottom: 7px;
        display: flex;
        align-items: center;
        gap: 6px;
      }
      .form-ti {
        width: 14px;
        height: 14px;
        object-fit: contain;
        border-radius: 50%;
        background: rgba(255, 255, 255, 0.04);
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
        background: var(--raised);
        border-radius: 5px;
        padding: 5px 8px;
        transition: background 0.2s;
      }
      .fr:hover {
        background: var(--lift);
      }
      .rd {
        width: 7px;
        height: 7px;
        border-radius: 50%;
      }
      .rd.W {
        background: var(--lo);
        box-shadow: 0 0 4px rgba(18, 219, 166, 0.4);
      }
      .rd.D {
        background: var(--med);
      }
      .rd.L {
        background: var(--hi);
        box-shadow: 0 0 4px rgba(245, 77, 42, 0.4);
      }
      .fs {
        font-family: "Oswald", sans-serif;
        font-size: 13px;
        font-weight: 600;
        color: #fff;
        text-align: center;
      }
      .fo {
        font-size: 11.5px;
        color: var(--text);
        overflow: hidden;
        text-overflow: ellipsis;
        white-space: nowrap;
      }
      .fc {
        font-size: 9px;
        color: var(--muted);
        text-align: right;
        text-transform: uppercase;
        letter-spacing: 0.3px;
      }
      .tag-sm {
        font-size: 7.5px;
        padding: 1px 4px;
        border-radius: 2px;
        background: rgba(246, 200, 64, 0.1);
        color: var(--med);
        font-family: "Oswald", sans-serif;
        font-weight: 600;
        letter-spacing: 0.5px;
        border: 1px solid rgba(246, 200, 64, 0.2);
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

      /* H2H */
      .h2h-bar {
        background: var(--raised);
        border-radius: 7px;
        padding: 10px;
        display: flex;
        align-items: center;
        justify-content: space-between;
        gap: 4px;
        margin-bottom: 10px;
      }
      .hs {
        text-align: center;
        flex: 1;
      }
      .hn {
        font-family: "Oswald", sans-serif;
        font-size: 26px;
        font-weight: 700;
        line-height: 1;
      }
      .hl {
        font-size: 9px;
        color: var(--muted);
        text-transform: uppercase;
        letter-spacing: 0.5px;
        margin-top: 2px;
      }
      .hv-div {
        width: 1px;
        height: 28px;
        background: var(--border);
        flex-shrink: 0;
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
        background: var(--raised);
        border-radius: 5px;
        padding: 5px 8px;
        transition: background 0.2s;
      }
      .h2h-r:hover {
        background: var(--lift);
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
        font-family: "Oswald", sans-serif;
        font-size: 14px;
        font-weight: 700;
        color: #fff;
        text-align: center;
        background: rgba(255, 255, 255, 0.05);
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
        text-transform: uppercase;
        letter-spacing: 0.3px;
      }

      /* Season Avgs */
      .avgs-pair {
        display: grid;
        grid-template-columns: 1fr 1fr;
        gap: 10px;
      }
      .avg-team-lbl {
        font-family: "Oswald", sans-serif;
        font-size: 9.5px;
        font-weight: 600;
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
        background: var(--raised);
        border-radius: 6px;
        padding: 7px 4px;
        text-align: center;
        transition:
          background 0.2s,
          transform 0.2s;
      }
      .ac:hover {
        background: var(--lift);
        transform: translateY(-1px);
      }
      .av {
        font-family: "Oswald", sans-serif;
        font-size: 18px;
        font-weight: 600;
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

      /* Prediction Table */
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
      .pt {
        width: 100%;
        border-collapse: collapse;
        min-width: 480px;
        table-layout: fixed;
      }
      .pt col.cn {
        width: 28%;
      }
      .pt col.ch {
        width: 16%;
      }
      .pt col.cm {
        width: 16%;
      }
      .pt col.cl {
        width: 16%;
      }
      .pt col.cb {
        width: 24%;
      }
      .pt thead th {
        font-family: "Oswald", sans-serif;
        font-size: 8.5px;
        font-weight: 600;
        letter-spacing: 1.5px;
        text-transform: uppercase;
        color: var(--muted);
        padding: 0 6px 8px;
        text-align: left;
      }
      .pt thead th.tc {
        text-align: center;
      }
      .pt tbody td {
        padding: 6px 6px;
        border-bottom: 1px solid rgba(255, 255, 255, 0.03);
        vertical-align: middle;
      }
      .pt tbody tr:last-child td {
        border-bottom: none;
      }
      .pt tbody tr:hover td {
        background: rgba(255, 255, 255, 0.02);
      }
      .pt td.tn {
        color: var(--label);
        font-weight: 600;
        font-size: 12px;
      }
      .pt td.tv {
        text-align: center;
      }
      .lv {
        font-family: "Oswald", sans-serif;
        font-size: 16px;
        font-weight: 600;
        color: var(--lo);
      }
      .mv {
        font-family: "Oswald", sans-serif;
        font-size: 16px;
        font-weight: 700;
        color: var(--med);
      }
      .hv {
        font-family: "Oswald", sans-serif;
        font-size: 16px;
        font-weight: 600;
        color: var(--hi);
      }

      /* Range bar */
      .rb-wrap {
        display: flex;
        align-items: center;
        gap: 6px;
      }
      .rb-track {
        flex: 1;
        height: 5px;
        background: rgba(255, 255, 255, 0.07);
        border-radius: 3px;
        overflow: hidden;
      }
      .rb-fill {
        height: 100%;
        border-radius: 3px;
        width: 0;
        transition: width 1.2s cubic-bezier(0.25, 0.46, 0.45, 0.94);
      }

      /* Team split */
      .ts-cell {
        display: flex;
        flex-direction: column;
        align-items: center;
        gap: 1px;
      }
      .ts-v {
        font-family: "Oswald", sans-serif;
        font-size: 14px;
        font-weight: 600;
        line-height: 1;
      }
      .ts-l {
        font-size: 8px;
        color: var(--muted);
        text-transform: uppercase;
        letter-spacing: 0.3px;
      }

      /* Score box */
      .score-zone {
        border-radius: 10px;
        padding: 15px;
        background: linear-gradient(
          135deg,
          rgba(255, 255, 255, 0.04),
          rgba(255, 255, 255, 0.01)
        );
        border: 1px solid var(--bm);
        display: flex;
        flex-direction: column;
        gap: 11px;
      }
      .sz-head {
        font-family: "Oswald", sans-serif;
        font-size: 9px;
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
        background: var(--raised);
        border: 1px solid var(--border);
        border-radius: 8px;
        padding: 11px 8px;
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
          var(--raised)
        );
      }
      .sbox-lbl {
        font-size: 8.5px;
        text-transform: uppercase;
        letter-spacing: 1px;
        color: var(--muted);
      }
      .sbox-score {
        font-family: "Oswald", sans-serif;
        font-size: 28px;
        font-weight: 700;
        color: #fff;
        letter-spacing: 2px;
        margin: 3px 0;
      }
      .sbox-score.feat-s {
        color: var(--med);
      }
      .sbox-prob {
        font-size: 9px;
        color: var(--muted);
      }
      .sz-note {
        font-size: 12px;
        color: var(--label);
        line-height: 1.65;
        border-top: 1px solid var(--border);
        padding-top: 9px;
      }
      .sz-note strong {
        color: var(--med);
        font-weight: 700;
      }

      /* Yellow cards */
      .yc-list {
        display: flex;
        flex-direction: column;
        gap: 6px;
      }
      .yc {
        display: flex;
        align-items: flex-start;
        gap: 9px;
        background: var(--raised);
        border: 1px solid var(--border);
        border-radius: 7px;
        padding: 8px 11px;
        transition:
          border-color 0.2s,
          transform 0.2s;
      }
      .yc:hover {
        border-color: rgba(255, 232, 74, 0.2);
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
      .yc-c {
        font-family: "Oswald", sans-serif;
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
        font-family: "Oswald", sans-serif;
        font-size: 8.5px;
        font-weight: 600;
        letter-spacing: 1px;
        text-transform: uppercase;
        padding: 2px 7px;
        border-radius: 3px;
        flex-shrink: 0;
        align-self: center;
        border: 1px solid;
      }
      .rh {
        color: var(--hi);
        border-color: rgba(245, 77, 42, 0.3);
        background: rgba(245, 77, 42, 0.1);
      }
      .rm {
        color: var(--med);
        border-color: rgba(246, 200, 64, 0.3);
        background: rgba(246, 200, 64, 0.08);
      }

      /* Footer */
      footer {
        text-align: center;
        padding: 20px 16px;
        font-size: 10px;
        color: var(--muted);
        border-top: 1px solid var(--border);
      }

      /* ═══════════════════════════════════════════
   RESPONSIVE
═══════════════════════════════════════════ */
      @media (min-width: 768px) {
        .badge { width: 80px; height: 80px; }
        .badge img { width: 56px; height: 56px; }
        .sb { padding: 18px 24px; }
      }

      /* ── Mobile ≤ 600px ── */
      @media (max-width: 600px) {
        body { font-size: 13px; }

        /* Page header */
        .ph { padding: 16px 12px 14px; }
        .ph h1 { font-size: 20px; }
        .ph .sub { font-size: 10.5px; }
        .ph-badge { font-size: 8px; letter-spacing: 1.5px; padding: 3px 8px; }
        .ph-nav { gap: 4px; margin-top: 10px; }
        .nav-btn { font-size: 8.5px; padding: 4px 8px; letter-spacing: 0.6px; }

        /* Significance strip */
        .sig-strip { font-size: 10px; padding: 7px 12px; }

        /* Match card wrapper */
        .mc { padding: 0 8px; margin: 14px auto; }
        .card { border-radius: 10px; }

        /* Hero — teams row */
        .hero { padding: 14px 12px 12px; gap: 8px; }
        .teams-row { gap: 8px; max-width: 100%; }
        .badge { width: 50px; height: 50px; }
        .badge img { width: 34px; height: 34px; }
        .t-name { font-size: 10.5px; }
        .t-meta { font-size: 8.5px; }
        .vs { font-size: 16px; }
        .ko { font-size: 8.5px; padding: 2px 6px; }
        .venue { font-size: 7.5px; }
        .chip { font-size: 7.5px; padding: 2px 6px; letter-spacing: 0.8px; }

        /* Section blocks */
        .sb { padding: 12px; }

        /* Motivation box */
        .mot-box { font-size: 11.5px; padding: 10px 12px; line-height: 1.6; }

        /* Form grid → stack */
        .form-cols { grid-template-columns: 1fr; gap: 14px; }
        .fr {
          grid-template-columns: 7px 38px 1fr 44px;
          gap: 4px; padding: 4px 6px;
        }
        .fs { font-size: 12px; }
        .fo { font-size: 10px; }
        .fc { font-size: 8px; }
        .form-team { font-size: 9px; }

        /* H2H */
        .h2h-bar { padding: 8px 6px; }
        .hn { font-size: 20px; }
        .hl { font-size: 8px; }
        .h2h-r { grid-template-columns: 1fr 48px 1fr; gap: 3px; padding: 5px 6px; }
        .rh, .ra { font-size: 10px; }
        .rs { font-size: 12px; }

        /* Averages → stack */
        .avgs-pair { grid-template-columns: 1fr; gap: 14px; }
        .avg-cells { grid-template-columns: repeat(3, 1fr); gap: 3px; }
        .av { font-size: 15px; }
        .al { font-size: 7px; }
        .ac { padding: 6px 3px; }

        /* ── Predictions table → mobile card layout ── */
        .pt { min-width: 0; }
        .pt thead { display: none; }
        .pt tbody tr {
          display: grid;
          grid-template-columns: 1fr 1fr;
          gap: 4px 8px;
          background: var(--raised);
          border-radius: 8px;
          padding: 10px 10px 8px;
          margin-bottom: 6px;
          border: 1px solid var(--border);
        }
        .pt tbody td { padding: 2px 0; border-bottom: none; }
        .pt td.tn {
          grid-column: 1 / -1;
          font-size: 10px; letter-spacing: 1px; text-transform: uppercase;
          color: var(--muted); font-weight: 700;
          padding-bottom: 2px;
          border-bottom: 1px solid var(--border);
          margin-bottom: 2px;
        }
        .pt td.tv { text-align: left; }
        .pt td.tv .ts-cell { flex-direction: row; align-items: center; gap: 6px; }
        .pt td.tv .ts-v { font-size: 14px; }
        .pt td.tv .ts-l { font-size: 8px; }
        .lv, .mv, .hv { font-size: 14px; }
        /* Range bar column spans full width */
        .pt td:last-child {
          grid-column: 1 / -1;
          padding: 4px 0 0;
        }
        .rb-wrap { gap: 4px; }

        /* Pred intro key */
        .pt-intro { gap: 8px; margin-bottom: 8px; }
        .pt-key { font-size: 9px; }

        /* Score prediction */
        .s-boxes { flex-direction: column; gap: 8px; }
        .sbox { max-width: 100%; min-width: 0; }
        .sbox-score { font-size: 24px; }
        .sbox-lbl { font-size: 8px; }
        .sbox-prob { font-size: 8.5px; }
        .score-zone { padding: 12px; border-radius: 8px; }
        .sz-note { font-size: 11px; line-height: 1.55; }

        /* Yellow cards */
        .yc { padding: 7px 9px; gap: 7px; }
        .yc-n { font-size: 11.5px; }
        .yc-r { font-size: 10px; }
        .risk { font-size: 7.5px; padding: 2px 5px; }
        .yc-ico { font-size: 13px; }
        .yc-c { font-size: 8px; }
      }

      /* ── Extra small ≤ 380px ── */
      @media (max-width: 380px) {
        .ph h1 { font-size: 17px; }
        .ph-badge { font-size: 7px; padding: 2px 6px; }
        .nav-btn { font-size: 7.5px; padding: 3px 6px; }
        .badge { width: 42px; height: 42px; }
        .badge img { width: 28px; height: 28px; }
        .t-name { font-size: 9.5px; }
        .teams-row { gap: 4px; }
        .sbox { padding: 10px 6px; }
        .sbox-score { font-size: 20px; }
        .fr { grid-template-columns: 7px 34px 1fr 38px; gap: 3px; padding: 3px 5px; }
        .fs { font-size: 11px; }
        .fo { font-size: 9px; }
      }
    </style>
  </head>
  <body>
    <!-- ═══ PAGE HEADER ═══ -->
    <header class="ph">
      <div class="ph-badge">
        ⚽ Premier League · Matchweek 33 · Sunday 19 April 2026
      </div>
      <h1 class="f-head">Sunday <em>Stats Predictor</em></h1>
      <p class="sub">
        4-match deep-dive · Form trends · Season averages · H2H · Weighted stat
        ranges · Score forecasts · Motivation analysis
      </p>
      <nav class="ph-nav">
        <a
          href="#m1"
          class="nav-btn"
          style="
            color: #95bfe5;
            border-color: rgba(149, 191, 229, 0.3);
            background: rgba(149, 191, 229, 0.07);
          "
          >Aston Villa v Sunderland</a
        >
        <a
          href="#m2"
          class="nav-btn"
          style="
            color: #274488;
            border-color: rgba(39, 68, 136, 0.4);
            background: rgba(39, 68, 136, 0.1);
          "
          >Everton v Liverpool</a
        >
        <a
          href="#m3"
          class="nav-btn"
          style="
            color: #e8003d;
            border-color: rgba(232, 0, 61, 0.35);
            background: rgba(232, 0, 61, 0.08);
          "
          >Forest v Burnley</a
        >
        <a
          href="#m4"
          class="nav-btn"
          style="
            color: #6cabdd;
            border-color: rgba(108, 171, 221, 0.35);
            background: rgba(108, 171, 221, 0.08);
          "
          >🏆 Man City v Arsenal</a
        >
      </nav>
    </header>

    <!-- ════════════════════════════════════════════
     MATCH 1 · ASTON VILLA vs SUNDERLAND
════════════════════════════════════════════ -->
    <div class="mc" id="m1">
      <div class="card">
        <div
          class="c-bar"
          style="background: linear-gradient(90deg, #95bfe5 50%, #eb172b 50%)"
        ></div>

        <div class="hero">
          <div class="hero-meta">
            <span
              class="chip"
              style="
                color: #95bfe5;
                border-color: rgba(149, 191, 229, 0.3);
                background: rgba(149, 191, 229, 0.08);
              "
              >14:00 BST · Villa Park</span
            >
            <span
              class="chip"
              style="
                color: var(--pl-green);
                border-color: rgba(0, 255, 133, 0.25);
                background: rgba(0, 255, 133, 0.06);
              "
              >UCL Qualification Race</span
            >
            <span
              class="chip"
              style="
                color: var(--med);
                border-color: rgba(246, 200, 64, 0.25);
                background: rgba(246, 200, 64, 0.06);
              "
              >Sunderland: European ambitions</span
            >
          </div>
          <div class="teams-row">
            <div class="team-col">
              <div class="badge">
                <img
                  src="https://cdn.brandfetch.io/idFPmd025E/theme/dark/logo.svg?c=1bxid64Mup7aczewSAYMX&t=1668077974118"
                  alt="Aston Villa"
                />
              </div>
              <div class="t-name" style="color: #95bfe5">Aston Villa</div>
              <div class="t-meta">
                4th · ~54 pts<br />Europa League Semi-final
              </div>
            </div>
            <div class="vs-col">
              <div class="vs">VS</div>
              <div class="ko">14:00</div>
              <div class="venue">
                Villa Park · Birmingham<br />~42,640 capacity
              </div>
            </div>
            <div class="team-col">
              <div class="badge">
                <img
                  src="https://cdn.brandfetch.io/idMQ7TtI1j/theme/light/logo.svg?c=1bxid64Mup7aczewSAYMX&t=1772760463945"
                  alt="Sunderland"
                />
              </div>
              <div class="t-name" style="color: #eb172b">Sunderland AFC</div>
              <div class="t-meta">
                10th · ~43 pts<br />1st season back in PL
              </div>
            </div>
          </div>
        </div>

        <div class="cg">
          <!-- Motivation / Context -->
          <div class="sb fw">
            <div class="stitle">Motivation & Match Significance</div>
            <div class="mot-box">
              <span class="hi-info">HIGH STAKES BOTH SIDES</span> Villa (4th,
              ~54pts) are fighting on two fronts — 7 pts clear in the UCL race
              and in the Europa League semi-final vs Nottingham Forest. Emery
              just engineered a stunning
              <strong>7-1 aggregate demolition of Bologna</strong> on Thursday.
              Sunderland (10th, ~43pts) are just 2pts outside the European
              places and consecutive wins over Newcastle and Tottenham have made
              them genuine contenders.
              <strong
                >Win for Sunderland = they enter the top six
                conversation</strong
              >. Both teams need this. Villa: Kamara (knee, out) and Alysson
              (out). Sunderland: Ballard, Mundle, Traore, Angulo, Ta Bi all out.
            </div>
          </div>

          <!-- Last 5 -->
          <div class="sb">
            <div class="stitle">Last 5 Matches</div>
            <div class="form-cols">
              <div>
                <div class="form-team" style="color: #95bfe5">
                  <img
                    class="form-ti"
                    src="https://cdn.brandfetch.io/idFPmd025E/theme/dark/logo.svg?c=1bxid64Mup7aczewSAYMX&t=1668077974118"
                    alt=""
                  />Aston Villa
                </div>
                <div class="fr-list">
                  <div class="fr">
                    <div class="rd W"></div>
                    <div class="fs">4–0</div>
                    <div class="fo">Bologna</div>
                    <div class="fc">UEL <span class="tag-sm">Semi-F</span></div>
                  </div>
                  <div class="fr">
                    <div class="rd D"></div>
                    <div class="fs">1–1</div>
                    <div class="fo">Nott'm Forest</div>
                    <div class="fc">PL Away</div>
                  </div>
                  <div class="fr">
                    <div class="rd W"></div>
                    <div class="fs">2–0</div>
                    <div class="fo">West Ham</div>
                    <div class="fc">PL Home</div>
                  </div>
                  <div class="fr">
                    <div class="rd W"></div>
                    <div class="fs">3–1</div>
                    <div class="fo">Bologna (Leg 1)</div>
                    <div class="fc">UEL</div>
                  </div>
                  <div class="fr">
                    <div class="rd W"></div>
                    <div class="fs">2–0</div>
                    <div class="fo">Lille</div>
                    <div class="fc">UEL</div>
                  </div>
                </div>
              </div>
              <div>
                <div class="form-team" style="color: #eb172b">
                  <img
                    class="form-ti"
                    src="https://cdn.brandfetch.io/idMQ7TtI1j/theme/light/logo.svg?c=1bxid64Mup7aczewSAYMX&t=1772760463945"
                    alt=""
                  />Sunderland
                </div>
                <div class="fr-list">
                  <div class="fr">
                    <div class="rd W"></div>
                    <div class="fs">1–0</div>
                    <div class="fo">Tottenham</div>
                    <div class="fc">PL Home</div>
                  </div>
                  <div class="fr">
                    <div class="rd W"></div>
                    <div class="fs">2–1</div>
                    <div class="fo">Newcastle</div>
                    <div class="fc">PL Away</div>
                  </div>
                  <div class="fr">
                    <div class="rd D"></div>
                    <div class="fs">1–1</div>
                    <div class="fo">Aston Villa (Sep)</div>
                    <div class="fc">PL Home</div>
                  </div>
                  <div class="fr">
                    <div class="rd W"></div>
                    <div class="fs">2–0</div>
                    <div class="fo">Everton</div>
                    <div class="fc">PL Away</div>
                  </div>
                  <div class="fr">
                    <div class="rd L"></div>
                    <div class="fs">0–1</div>
                    <div class="fo">Liverpool</div>
                    <div class="fc">PL Away</div>
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
          </div>

          <!-- H2H -->
          <div class="sb">
            <div class="stitle">H2H – Last 5 PL Meetings</div>
            <div class="h2h-bar">
              <div class="hs">
                <div class="hn" style="color: #95bfe5">3</div>
                <div class="hl">Villa W</div>
              </div>
              <div class="hv-div"></div>
              <div class="hs">
                <div class="hn" style="color: var(--med)">2</div>
                <div class="hl">Draws</div>
              </div>
              <div class="hv-div"></div>
              <div class="hs">
                <div class="hn" style="color: #eb172b">0</div>
                <div class="hl">Sunderland W</div>
              </div>
              <div class="hv-div"></div>
              <div class="hs">
                <div class="hn">2.4</div>
                <div class="hl">Avg Goals</div>
              </div>
            </div>
            <div class="h2h-rows">
              <div class="h2h-r">
                <div class="rh">Sunderland</div>
                <div class="rs">1–1</div>
                <div class="ra">Aston Villa</div>
                <div class="rx">PL Sep 2025 (this season)</div>
              </div>
              <div class="h2h-r">
                <div class="rh">Aston Villa</div>
                <div class="rs">3–1</div>
                <div class="ra">Sunderland</div>
                <div class="rx">Champ'ship playoff final 2019</div>
              </div>
              <div class="h2h-r">
                <div class="rh">Aston Villa</div>
                <div class="rs">1–0</div>
                <div class="ra">Sunderland</div>
                <div class="rx">PL 2016 (last top-flight prior)</div>
              </div>
              <div class="h2h-r">
                <div class="rh">Aston Villa</div>
                <div class="rs">2–1</div>
                <div class="ra">Sunderland</div>
                <div class="rx">PL 2015</div>
              </div>
              <div class="h2h-r">
                <div class="rh">Sunderland</div>
                <div class="rs">0–0</div>
                <div class="ra">Aston Villa</div>
                <div class="rx">PL 2015</div>
              </div>
            </div>
            <p style="font-size: 10px; color: var(--muted); margin-top: 8px">
              Villa unbeaten in 12 of last 13 all-comps vs Sunderland. 20 goals
              in last 6 H2H. 5 of last 6 over 2.5 goals.
            </p>
          </div>

          <!-- Season Avgs -->
          <div class="sb">
            <div class="stitle">Season Averages – PL 25/26</div>
            <div class="avgs-pair">
              <div>
                <div
                  class="avg-team-lbl"
                  style="
                    color: #fff;
                    background: rgba(149, 191, 229, 0.15);
                    border: 1px solid rgba(149, 191, 229, 0.3);
                  "
                >
                  Aston Villa
                </div>
                <div class="avg-cells">
                  <div class="ac">
                    <div class="av">15.2</div>
                    <div class="al">Shots</div>
                  </div>
                  <div class="ac">
                    <div class="av">5.1</div>
                    <div class="al">SOT</div>
                  </div>
                  <div class="ac">
                    <div class="av">5.8</div>
                    <div class="al">Corners</div>
                  </div>
                  <div class="ac">
                    <div class="av">11.2</div>
                    <div class="al">Fouls</div>
                  </div>
                  <div class="ac">
                    <div class="av">1.62</div>
                    <div class="al">Gls/Gm</div>
                  </div>
                  <div class="ac">
                    <div class="av">54</div>
                    <div class="al">Points</div>
                  </div>
                </div>
              </div>
              <div>
                <div
                  class="avg-team-lbl"
                  style="
                    color: #fff;
                    background: rgba(235, 23, 43, 0.15);
                    border: 1px solid rgba(235, 23, 43, 0.3);
                  "
                >
                  Sunderland
                </div>
                <div class="avg-cells">
                  <div class="ac">
                    <div class="av">10.2</div>
                    <div class="al">Shots</div>
                  </div>
                  <div class="ac">
                    <div class="av">3.0</div>
                    <div class="al">SOT</div>
                  </div>
                  <div class="ac">
                    <div class="av">3.4</div>
                    <div class="al">Corners</div>
                  </div>
                  <div class="ac">
                    <div class="av">12.8</div>
                    <div class="al">Fouls</div>
                  </div>
                  <div class="ac">
                    <div class="av">1.00</div>
                    <div class="al">Gls/Gm</div>
                  </div>
                  <div class="ac">
                    <div class="av">43</div>
                    <div class="al">Points</div>
                  </div>
                </div>
              </div>
            </div>
          </div>

          <!-- Predictions -->
          <div class="sb fw" id="p1">
            <div class="stitle">Weighted Stat Predictions</div>
            <div class="pt-intro">
              <div class="pt-key">
                <div class="pt-kd" style="background: var(--lo)"></div>
                <span style="color: var(--lo); font-weight: 700">Low</span>
              </div>
              <div class="pt-key">
                <div class="pt-kd" style="background: var(--med)"></div>
                <span style="color: var(--med); font-weight: 700">Median</span>
              </div>
              <div class="pt-key">
                <div class="pt-kd" style="background: var(--hi)"></div>
                <span style="color: var(--hi); font-weight: 700">High</span>
              </div>
            </div>
            <div class="ptw">
              <table class="pt">
                <colgroup>
                  <col class="cn" />
                  <col class="ch" />
                  <col class="cm" />
                  <col class="cl" />
                  <col class="cb" />
                </colgroup>
                <thead>
                  <tr>
                    <th>Metric</th>
                    <th class="tc" style="color: #95bfe5">Villa</th>
                    <th class="tc" style="color: #eb172b">Sund</th>
                    <th class="tc">Total Range</th>
                    <th class="tc" style="color: var(--muted)">Intensity</th>
                  </tr>
                </thead>
                <tbody>
                  <tr>
                    <td class="tn">Corners</td>
                    <td class="tv">
                      <div class="ts-cell">
                        <span class="ts-v" style="color: #95bfe5">5</span
                        ><span class="ts-l">med</span>
                      </div>
                    </td>
                    <td class="tv">
                      <div class="ts-cell">
                        <span class="ts-v" style="color: #eb172b">3</span
                        ><span class="ts-l">med</span>
                      </div>
                    </td>
                    <td class="tv">
                      <span class="lv">6</span> <span class="mv">8</span>
                      <span class="hv">13</span>
                    </td>
                    <td>
                      <div class="rb-wrap">
                        <div class="rb-track">
                          <div
                            class="rb-fill"
                            data-w="58"
                            style="
                              background: linear-gradient(
                                90deg,
                                #95bfe5,
                                #eb172b
                              );
                            "
                          ></div>
                        </div>
                      </div>
                    </td>
                  </tr>
                  <tr>
                    <td class="tn">Shots</td>
                    <td class="tv">
                      <div class="ts-cell">
                        <span class="ts-v" style="color: #95bfe5">16</span
                        ><span class="ts-l">med</span>
                      </div>
                    </td>
                    <td class="tv">
                      <div class="ts-cell">
                        <span class="ts-v" style="color: #eb172b">9</span
                        ><span class="ts-l">med</span>
                      </div>
                    </td>
                    <td class="tv">
                      <span class="lv">18</span> <span class="mv">25</span>
                      <span class="hv">34</span>
                    </td>
                    <td>
                      <div class="rb-wrap">
                        <div class="rb-track">
                          <div
                            class="rb-fill"
                            data-w="68"
                            style="
                              background: linear-gradient(
                                90deg,
                                #95bfe5,
                                #eb172b
                              );
                            "
                          ></div>
                        </div>
                      </div>
                    </td>
                  </tr>
                  <tr>
                    <td class="tn">Shots on Target</td>
                    <td class="tv">
                      <div class="ts-cell">
                        <span class="ts-v" style="color: #95bfe5">5</span
                        ><span class="ts-l">med</span>
                      </div>
                    </td>
                    <td class="tv">
                      <div class="ts-cell">
                        <span class="ts-v" style="color: #eb172b">3</span
                        ><span class="ts-l">med</span>
                      </div>
                    </td>
                    <td class="tv">
                      <span class="lv">6</span> <span class="mv">9</span>
                      <span class="hv">15</span>
                    </td>
                    <td>
                      <div class="rb-wrap">
                        <div class="rb-track">
                          <div
                            class="rb-fill"
                            data-w="60"
                            style="
                              background: linear-gradient(
                                90deg,
                                #95bfe5,
                                #eb172b
                              );
                            "
                          ></div>
                        </div>
                      </div>
                    </td>
                  </tr>
                  <tr>
                    <td class="tn">Fouls</td>
                    <td class="tv">
                      <div class="ts-cell">
                        <span class="ts-v" style="color: #95bfe5">11</span
                        ><span class="ts-l">med</span>
                      </div>
                    </td>
                    <td class="tv">
                      <div class="ts-cell">
                        <span class="ts-v" style="color: #eb172b">13</span
                        ><span class="ts-l">med</span>
                      </div>
                    </td>
                    <td class="tv">
                      <span class="lv">16</span> <span class="mv">24</span>
                      <span class="hv">33</span>
                    </td>
                    <td>
                      <div class="rb-wrap">
                        <div class="rb-track">
                          <div
                            class="rb-fill"
                            data-w="62"
                            style="
                              background: linear-gradient(
                                90deg,
                                #95bfe5,
                                #eb172b
                              );
                            "
                          ></div>
                        </div>
                      </div>
                    </td>
                  </tr>
                  <tr>
                    <td class="tn">Throw-ins</td>
                    <td class="tv">
                      <div class="ts-cell">
                        <span class="ts-v" style="color: #95bfe5">20</span
                        ><span class="ts-l">med</span>
                      </div>
                    </td>
                    <td class="tv">
                      <div class="ts-cell">
                        <span class="ts-v" style="color: #eb172b">18</span
                        ><span class="ts-l">med</span>
                      </div>
                    </td>
                    <td class="tv">
                      <span class="lv">28</span> <span class="mv">38</span>
                      <span class="hv">52</span>
                    </td>
                    <td>
                      <div class="rb-wrap">
                        <div class="rb-track">
                          <div
                            class="rb-fill"
                            data-w="64"
                            style="
                              background: linear-gradient(
                                90deg,
                                #95bfe5,
                                #eb172b
                              );
                            "
                          ></div>
                        </div>
                      </div>
                    </td>
                  </tr>
                  <tr>
                    <td class="tn">Goal Kicks</td>
                    <td class="tv">
                      <div class="ts-cell">
                        <span class="ts-v" style="color: #95bfe5">9</span
                        ><span class="ts-l">med</span>
                      </div>
                    </td>
                    <td class="tv">
                      <div class="ts-cell">
                        <span class="ts-v" style="color: #eb172b">11</span
                        ><span class="ts-l">med</span>
                      </div>
                    </td>
                    <td class="tv">
                      <span class="lv">14</span> <span class="mv">20</span>
                      <span class="hv">28</span>
                    </td>
                    <td>
                      <div class="rb-wrap">
                        <div class="rb-track">
                          <div
                            class="rb-fill"
                            data-w="56"
                            style="
                              background: linear-gradient(
                                90deg,
                                #95bfe5,
                                #eb172b
                              );
                            "
                          ></div>
                        </div>
                      </div>
                    </td>
                  </tr>
                  <tr>
                    <td class="tn">Tackles</td>
                    <td class="tv">
                      <div class="ts-cell">
                        <span class="ts-v" style="color: #95bfe5">14</span
                        ><span class="ts-l">med</span>
                      </div>
                    </td>
                    <td class="tv">
                      <div class="ts-cell">
                        <span class="ts-v" style="color: #eb172b">16</span
                        ><span class="ts-l">med</span>
                      </div>
                    </td>
                    <td class="tv">
                      <span class="lv">22</span> <span class="mv">30</span>
                      <span class="hv">42</span>
                    </td>
                    <td>
                      <div class="rb-wrap">
                        <div class="rb-track">
                          <div
                            class="rb-fill"
                            data-w="68"
                            style="
                              background: linear-gradient(
                                90deg,
                                #95bfe5,
                                #eb172b
                              );
                            "
                          ></div>
                        </div>
                      </div>
                    </td>
                  </tr>
                </tbody>
              </table>
            </div>
          </div>

          <!-- Score -->
          <div class="sb">
            <div class="stitle">Score Prediction</div>
            <div class="score-zone">
              <div class="sz-head">Aston Villa vs Sunderland</div>
              <div class="s-boxes">
                <div class="sbox">
                  <div class="sbox-lbl">Half-Time</div>
                  <div class="sbox-score">1–0</div>
                  <div class="sbox-prob">Villa ~44%</div>
                </div>
                <div class="sbox feat">
                  <div class="sbox-lbl">Full-Time ★</div>
                  <div class="sbox-score feat-s">2–1</div>
                  <div class="sbox-prob">Villa win ~32%</div>
                </div>
                <div class="sbox">
                  <div class="sbox-lbl">Alt: Draw</div>
                  <div class="sbox-score">1–1</div>
                  <div class="sbox-prob">~24% — Sunderland resilient</div>
                </div>
              </div>
              <div class="sz-note">
                <strong>Why Villa 2-1:</strong> Villa have won 3 of last 6 H2H
                home games at Villa Park with none of those ending in Sunderland
                away wins. Post-Bologna Europa League high gives Villa huge
                momentum, and Ollie Watkins (100th Villa goal vs Bologna) will
                carry that form. Sunderland's away record (just 10 goals in 16
                away games) is a concern, but their 3 consecutive away points
                and their fighting spirit from the Tottenham win suggests they
                won't just concede. McGinn (5 goal contributions in 6 home PL
                games) is the key Villa creator.
              </div>
            </div>
          </div>

          <!-- Yellow Cards -->
          <div class="sb">
            <div class="stitle">🟨 Yellow Card Risks</div>
            <div class="yc-list">
              <div class="yc">
                <div class="yc-ico">🟨</div>
                <div class="yc-inf">
                  <div class="yc-n">
                    Amadou Onana
                    <span class="yc-c" style="color: #95bfe5">Villa · DM</span>
                  </div>
                  <div class="yc-r">
                    Aggressive DM with 6 PL bookings. Faces Granit Xhaka's
                    physical challenge in midfield — two combative players in
                    direct duel.
                  </div>
                </div>
                <div class="risk rh">HIGH</div>
              </div>
              <div class="yc">
                <div class="yc-ico">🟨</div>
                <div class="yc-inf">
                  <div class="yc-n">
                    Granit Xhaka
                    <span class="yc-c" style="color: #eb172b"
                      >Sunderland · MF</span
                    >
                  </div>
                  <div class="yc-r">
                    12 career PL yellows in just his first season at Sunderland.
                    Renowned for tactical fouling. Faces Villa's press with
                    urgency.
                  </div>
                </div>
                <div class="risk rh">HIGH</div>
              </div>
              <div class="yc">
                <div class="yc-ico">🟨</div>
                <div class="yc-inf">
                  <div class="yc-n">
                    Noah Sadiki
                    <span class="yc-c" style="color: #eb172b"
                      >Sunderland · DM</span
                    >
                  </div>
                  <div class="yc-r">
                    Faces Watkins and Rogers in a physical battle — Sadiki fouls
                    to prevent transitions. 5 yellows this season.
                  </div>
                </div>
                <div class="risk rm">MED</div>
              </div>
              <div class="yc">
                <div class="yc-ico">🟨</div>
                <div class="yc-inf">
                  <div class="yc-n">
                    Youri Tielemans
                    <span class="yc-c" style="color: #95bfe5">Villa · MF</span>
                  </div>
                  <div class="yc-r">
                    Controlling presence who occasionally fouls to disrupt
                    Sunderland's counter-attacks. 4 PL yellows this season.
                  </div>
                </div>
                <div class="risk rm">MED</div>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>

    <!-- ════════════════════════════════════════════
     MATCH 2 · EVERTON vs LIVERPOOL
════════════════════════════════════════════ -->
    <div class="mc" id="m2">
      <!-- Significance strip -->
      <div
        class="sig-strip"
        style="
          background: linear-gradient(
            90deg,
            rgba(39, 68, 136, 0.15),
            rgba(200, 16, 46, 0.08)
          );
          border-bottom: 1px solid rgba(39, 68, 136, 0.2);
        "
      >
        <span style="font-size: 13px">🏟️</span>
        <span
          style="
            color: var(--bright);
            font-family: &quot;Oswald&quot;, sans-serif;
            font-weight: 600;
            letter-spacing: 0.5px;
          "
          >HISTORIC — FIRST MERSEYSIDE DERBY AT HILL DICKINSON STADIUM</span
        >
        <span style="font-size: 13px">🔥</span>
      </div>
      <div class="card">
        <div
          class="c-bar"
          style="background: linear-gradient(90deg, #274488 50%, #c8102e 50%)"
        ></div>

        <div class="hero">
          <div class="hero-meta">
            <span
              class="chip"
              style="
                color: #274488;
                border-color: rgba(39, 68, 136, 0.4);
                background: rgba(39, 68, 136, 0.1);
              "
              >14:00 BST · Hill Dickinson Stadium</span
            >
            <span
              class="chip"
              style="
                color: var(--hi);
                border-color: rgba(245, 77, 42, 0.3);
                background: rgba(245, 77, 42, 0.08);
              "
              >⚡ European Qualification — Both Sides</span
            >
            <span
              class="chip"
              style="color: #888; border-color: rgba(255, 255, 255, 0.15)"
              >Opta: EFC 37.3% · Draw 26.4% · LFC 36.3%</span
            >
          </div>
          <div class="teams-row">
            <div class="team-col">
              <div class="badge">
                <img
                  src="https://cdn.brandfetch.io/evertonfc.com/w/200/h/200"
                  onerror="
                    this.onerror = null;
                    this.src =
                      'https://upload.wikimedia.org/wikipedia/en/thumb/7/7c/Everton_FC_logo.svg/120px-Everton_FC_logo.svg.png';
                  "
                  alt="Everton"
                />
              </div>
              <div class="t-name" style="color: #274488">Everton FC</div>
              <div class="t-meta">
                8th · ~47 pts<br />W3 D1 L1 last 5 · Chasing Europe
              </div>
            </div>
            <div class="vs-col">
              <div class="vs">VS</div>
              <div class="ko">14:00</div>
              <div class="venue">
                Hill Dickinson Stadium<br />Merseyside Derby — Historic Occasion
              </div>
            </div>
            <div class="team-col">
              <div class="badge">
                <img
                  src="https://cdn.brandfetch.io/liverpoolfc.com/w/200/h/200"
                  onerror="
                    this.onerror = null;
                    this.src =
                      'https://upload.wikimedia.org/wikipedia/en/thumb/0/0c/Liverpool_FC.svg/120px-Liverpool_FC.svg.png';
                  "
                  alt="Liverpool"
                />
              </div>
              <div class="t-name" style="color: #c8102e">Liverpool FC</div>
              <div class="t-meta">
                5th · ~52 pts<br />L4 of last 5 all comps
              </div>
            </div>
          </div>
        </div>

        <div class="cg">
          <div class="sb fw">
            <div class="stitle">Motivation & Match Significance</div>
            <div class="mot-box">
              <span class="hi-alert">⚡ UNEVEN STAKES</span>
              <strong>Everton (47pts, 8th):</strong> desperately need to win to
              stay in the European race — only 5pts behind Liverpool in 5th.
              This is also the
              <strong
                >first ever Merseyside Derby at Hill Dickinson Stadium</strong
              >, bringing enormous emotional weight. Moyes' side are flying (W2
              home with clean sheets vs Burnley & Chelsea).
              <strong>Liverpool (52pts, 5th):</strong> humiliated 0-2 by PSG (CL
              exit 0-4 agg), lost 4 of last 5 in all competitions. Ekitike out
              for the season (Achilles). Alisson still injured — Mamardashvili
              starts. <strong>Salah's final Merseyside Derby</strong> before his
              summer departure adds narrative. Liverpool are in crisis of form
              but still a goal machine when clicking. Opta almost can't split
              them — <strong>this is genuinely a 50/50 contest</strong>.
            </div>
          </div>

          <div class="sb">
            <div class="stitle">Last 5 Matches</div>
            <div class="form-cols">
              <div>
                <div class="form-team" style="color: #274488">
                  <img
                    class="form-ti"
                    src="https://upload.wikimedia.org/wikipedia/en/thumb/7/7c/Everton_FC_logo.svg/120px-Everton_FC_logo.svg.png"
                    alt=""
                  />Everton
                </div>
                <div class="fr-list">
                  <div class="fr">
                    <div class="rd D"></div>
                    <div class="fs">2–2</div>
                    <div class="fo">Brentford</div>
                    <div class="fc">
                      PL Away <span class="tag-sm">91' EQ</span>
                    </div>
                  </div>
                  <div class="fr">
                    <div class="rd W"></div>
                    <div class="fs">3–0</div>
                    <div class="fo">Chelsea</div>
                    <div class="fc">PL Home</div>
                  </div>
                  <div class="fr">
                    <div class="rd W"></div>
                    <div class="fs">2–0</div>
                    <div class="fo">Burnley</div>
                    <div class="fc">PL Home</div>
                  </div>
                  <div class="fr">
                    <div class="rd W"></div>
                    <div class="fs">3–2</div>
                    <div class="fo">Newcastle</div>
                    <div class="fc">PL Away</div>
                  </div>
                  <div class="fr">
                    <div class="rd W"></div>
                    <div class="fs">2–0</div>
                    <div class="fo">Sunderland</div>
                    <div class="fc">PL Away</div>
                  </div>
                </div>
              </div>
              <div>
                <div class="form-team" style="color: #c8102e">
                  <img
                    class="form-ti"
                    src="https://upload.wikimedia.org/wikipedia/en/thumb/0/0c/Liverpool_FC.svg/120px-Liverpool_FC.svg.png"
                    alt=""
                  />Liverpool
                </div>
                <div class="fr-list">
                  <div class="fr">
                    <div class="rd L"></div>
                    <div class="fs">0–2</div>
                    <div class="fo">PSG</div>
                    <div class="fc">UCL <span class="tag-sm">Elim</span></div>
                  </div>
                  <div class="fr">
                    <div class="rd W"></div>
                    <div class="fs">2–0</div>
                    <div class="fo">Fulham</div>
                    <div class="fc">PL Home</div>
                  </div>
                  <div class="fr">
                    <div class="rd L"></div>
                    <div class="fs">1–2</div>
                    <div class="fo">Brighton</div>
                    <div class="fc">PL Away</div>
                  </div>
                  <div class="fr">
                    <div class="rd L"></div>
                    <div class="fs">0–4</div>
                    <div class="fo">Man City</div>
                    <div class="fc">FAC</div>
                  </div>
                  <div class="fr">
                    <div class="rd L"></div>
                    <div class="fs">0–2</div>
                    <div class="fo">PSG (Leg 1)</div>
                    <div class="fc">UCL</div>
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
          </div>

          <div class="sb">
            <div class="stitle">H2H – Last 5 Merseyside Derbies</div>
            <div class="h2h-bar">
              <div class="hs">
                <div class="hn" style="color: #274488">1</div>
                <div class="hl">Everton W</div>
              </div>
              <div class="hv-div"></div>
              <div class="hs">
                <div class="hn" style="color: var(--med)">3</div>
                <div class="hl">Draws</div>
              </div>
              <div class="hv-div"></div>
              <div class="hs">
                <div class="hn" style="color: #c8102e">1</div>
                <div class="hl">Liverpool W</div>
              </div>
              <div class="hv-div"></div>
              <div class="hs">
                <div class="hn">2.0</div>
                <div class="hl">Avg Goals</div>
              </div>
            </div>
            <div class="h2h-rows">
              <div class="h2h-r">
                <div class="rh">Liverpool</div>
                <div class="rs">2–1</div>
                <div class="ra">Everton</div>
                <div class="rx">PL Sep 2025 (Anfield)</div>
              </div>
              <div class="h2h-r">
                <div class="rh">Everton</div>
                <div class="rs">2–2</div>
                <div class="ra">Liverpool</div>
                <div class="rx">PL May 2025 — Tarkowski 90+5' eq</div>
              </div>
              <div class="h2h-r">
                <div class="rh">Liverpool</div>
                <div class="rs">2–0</div>
                <div class="ra">Everton</div>
                <div class="rx">PL Feb 2025 (Anfield)</div>
              </div>
              <div class="h2h-r">
                <div class="rh">Everton</div>
                <div class="rs">0–0</div>
                <div class="ra">Liverpool</div>
                <div class="rx">PL Oct 2024</div>
              </div>
              <div class="h2h-r">
                <div class="rh">Everton</div>
                <div class="rs">2–0</div>
                <div class="ra">Liverpool</div>
                <div class="rx">PL Feb 2024 (Last Goodison)</div>
              </div>
            </div>
            <p style="font-size: 10px; color: var(--muted); margin-top: 8px">
              6 of last 8 at Everton ended in draws. 4 of last 19 derbies had
              over 3 goals. Liverpool lost 4 away PL games in a row. Everton
              unbeaten in 3 consecutive home H2H.
            </p>
          </div>

          <div class="sb">
            <div class="stitle">Season Averages – PL 25/26</div>
            <div class="avgs-pair">
              <div>
                <div
                  class="avg-team-lbl"
                  style="
                    color: #fff;
                    background: rgba(39, 68, 136, 0.2);
                    border: 1px solid rgba(39, 68, 136, 0.35);
                  "
                >
                  Everton
                </div>
                <div class="avg-cells">
                  <div class="ac">
                    <div class="av">12.4</div>
                    <div class="al">Shots</div>
                  </div>
                  <div class="ac">
                    <div class="av">4.1</div>
                    <div class="al">SOT</div>
                  </div>
                  <div class="ac">
                    <div class="av">4.6</div>
                    <div class="al">Corners</div>
                  </div>
                  <div class="ac">
                    <div class="av">11.8</div>
                    <div class="al">Fouls</div>
                  </div>
                  <div class="ac">
                    <div class="av">1.44</div>
                    <div class="al">Gls/Gm</div>
                  </div>
                  <div class="ac">
                    <div class="av">47</div>
                    <div class="al">Points</div>
                  </div>
                </div>
              </div>
              <div>
                <div
                  class="avg-team-lbl"
                  style="
                    color: #fff;
                    background: rgba(200, 16, 46, 0.15);
                    border: 1px solid rgba(200, 16, 46, 0.3);
                  "
                >
                  Liverpool
                </div>
                <div class="avg-cells">
                  <div class="ac">
                    <div class="av">16.8</div>
                    <div class="al">Shots</div>
                  </div>
                  <div class="ac">
                    <div class="av">5.8</div>
                    <div class="al">SOT</div>
                  </div>
                  <div class="ac">
                    <div class="av">6.0</div>
                    <div class="al">Corners</div>
                  </div>
                  <div class="ac">
                    <div class="av">10.6</div>
                    <div class="al">Fouls</div>
                  </div>
                  <div class="ac">
                    <div class="av">1.56</div>
                    <div class="al">Gls/Gm</div>
                  </div>
                  <div class="ac">
                    <div class="av">52</div>
                    <div class="al">Points</div>
                  </div>
                </div>
              </div>
            </div>
          </div>

          <div class="sb fw" id="p2">
            <div class="stitle">Weighted Stat Predictions</div>
            <div class="pt-intro">
              <div class="pt-key">
                <div class="pt-kd" style="background: var(--lo)"></div>
                <span style="color: var(--lo); font-weight: 700">Low</span>
              </div>
              <div class="pt-key">
                <div class="pt-kd" style="background: var(--med)"></div>
                <span style="color: var(--med); font-weight: 700">Median</span>
              </div>
              <div class="pt-key">
                <div class="pt-kd" style="background: var(--hi)"></div>
                <span style="color: var(--hi); font-weight: 700">High</span>
              </div>
            </div>
            <div class="ptw">
              <table class="pt">
                <colgroup>
                  <col class="cn" />
                  <col class="ch" />
                  <col class="cm" />
                  <col class="cl" />
                  <col class="cb" />
                </colgroup>
                <thead>
                  <tr>
                    <th>Metric</th>
                    <th class="tc" style="color: #274488">EFC</th>
                    <th class="tc" style="color: #c8102e">LFC</th>
                    <th class="tc">Total Range</th>
                    <th class="tc" style="color: var(--muted)">Intensity</th>
                  </tr>
                </thead>
                <tbody>
                  <tr>
                    <td class="tn">Corners</td>
                    <td class="tv">
                      <div class="ts-cell">
                        <span class="ts-v" style="color: #274488">4</span
                        ><span class="ts-l">med</span>
                      </div>
                    </td>
                    <td class="tv">
                      <div class="ts-cell">
                        <span class="ts-v" style="color: #c8102e">6</span
                        ><span class="ts-l">med</span>
                      </div>
                    </td>
                    <td class="tv">
                      <span class="lv">7</span> <span class="mv">10</span>
                      <span class="hv">15</span>
                    </td>
                    <td>
                      <div class="rb-wrap">
                        <div class="rb-track">
                          <div
                            class="rb-fill"
                            data-w="65"
                            style="
                              background: linear-gradient(
                                90deg,
                                #274488,
                                #c8102e
                              );
                            "
                          ></div>
                        </div>
                      </div>
                    </td>
                  </tr>
                  <tr>
                    <td class="tn">Shots</td>
                    <td class="tv">
                      <div class="ts-cell">
                        <span class="ts-v" style="color: #274488">11</span
                        ><span class="ts-l">med</span>
                      </div>
                    </td>
                    <td class="tv">
                      <div class="ts-cell">
                        <span class="ts-v" style="color: #c8102e">14</span
                        ><span class="ts-l">med</span>
                      </div>
                    </td>
                    <td class="tv">
                      <span class="lv">18</span> <span class="mv">25</span>
                      <span class="hv">35</span>
                    </td>
                    <td>
                      <div class="rb-wrap">
                        <div class="rb-track">
                          <div
                            class="rb-fill"
                            data-w="70"
                            style="
                              background: linear-gradient(
                                90deg,
                                #274488,
                                #c8102e
                              );
                            "
                          ></div>
                        </div>
                      </div>
                    </td>
                  </tr>
                  <tr>
                    <td class="tn">Shots on Target</td>
                    <td class="tv">
                      <div class="ts-cell">
                        <span class="ts-v" style="color: #274488">4</span
                        ><span class="ts-l">med</span>
                      </div>
                    </td>
                    <td class="tv">
                      <div class="ts-cell">
                        <span class="ts-v" style="color: #c8102e">5</span
                        ><span class="ts-l">med</span>
                      </div>
                    </td>
                    <td class="tv">
                      <span class="lv">6</span> <span class="mv">9</span>
                      <span class="hv">15</span>
                    </td>
                    <td>
                      <div class="rb-wrap">
                        <div class="rb-track">
                          <div
                            class="rb-fill"
                            data-w="62"
                            style="
                              background: linear-gradient(
                                90deg,
                                #274488,
                                #c8102e
                              );
                            "
                          ></div>
                        </div>
                      </div>
                    </td>
                  </tr>
                  <tr>
                    <td class="tn">Fouls</td>
                    <td class="tv">
                      <div class="ts-cell">
                        <span class="ts-v" style="color: #274488">13</span
                        ><span class="ts-l">med</span>
                      </div>
                    </td>
                    <td class="tv">
                      <div class="ts-cell">
                        <span class="ts-v" style="color: #c8102e">11</span
                        ><span class="ts-l">med</span>
                      </div>
                    </td>
                    <td class="tv">
                      <span class="lv">18</span> <span class="mv">24</span>
                      <span class="hv">36</span>
                    </td>
                    <td>
                      <div class="rb-wrap">
                        <div class="rb-track">
                          <div
                            class="rb-fill"
                            data-w="72"
                            style="
                              background: linear-gradient(
                                90deg,
                                #274488,
                                #c8102e
                              );
                            "
                          ></div>
                        </div>
                      </div>
                    </td>
                  </tr>
                  <tr>
                    <td class="tn">Throw-ins</td>
                    <td class="tv">
                      <div class="ts-cell">
                        <span class="ts-v" style="color: #274488">20</span
                        ><span class="ts-l">med</span>
                      </div>
                    </td>
                    <td class="tv">
                      <div class="ts-cell">
                        <span class="ts-v" style="color: #c8102e">20</span
                        ><span class="ts-l">med</span>
                      </div>
                    </td>
                    <td class="tv">
                      <span class="lv">32</span> <span class="mv">40</span>
                      <span class="hv">56</span>
                    </td>
                    <td>
                      <div class="rb-wrap">
                        <div class="rb-track">
                          <div
                            class="rb-fill"
                            data-w="68"
                            style="
                              background: linear-gradient(
                                90deg,
                                #274488,
                                #c8102e
                              );
                            "
                          ></div>
                        </div>
                      </div>
                    </td>
                  </tr>
                  <tr>
                    <td class="tn">Goal Kicks</td>
                    <td class="tv">
                      <div class="ts-cell">
                        <span class="ts-v" style="color: #274488">11</span
                        ><span class="ts-l">med</span>
                      </div>
                    </td>
                    <td class="tv">
                      <div class="ts-cell">
                        <span class="ts-v" style="color: #c8102e">9</span
                        ><span class="ts-l">med</span>
                      </div>
                    </td>
                    <td class="tv">
                      <span class="lv">14</span> <span class="mv">20</span>
                      <span class="hv">28</span>
                    </td>
                    <td>
                      <div class="rb-wrap">
                        <div class="rb-track">
                          <div
                            class="rb-fill"
                            data-w="58"
                            style="
                              background: linear-gradient(
                                90deg,
                                #274488,
                                #c8102e
                              );
                            "
                          ></div>
                        </div>
                      </div>
                    </td>
                  </tr>
                  <tr>
                    <td class="tn">Tackles</td>
                    <td class="tv">
                      <div class="ts-cell">
                        <span class="ts-v" style="color: #274488">16</span
                        ><span class="ts-l">med</span>
                      </div>
                    </td>
                    <td class="tv">
                      <div class="ts-cell">
                        <span class="ts-v" style="color: #c8102e">14</span
                        ><span class="ts-l">med</span>
                      </div>
                    </td>
                    <td class="tv">
                      <span class="lv">22</span> <span class="mv">30</span>
                      <span class="hv">44</span>
                    </td>
                    <td>
                      <div class="rb-wrap">
                        <div class="rb-track">
                          <div
                            class="rb-fill"
                            data-w="75"
                            style="
                              background: linear-gradient(
                                90deg,
                                #274488,
                                #c8102e
                              );
                            "
                          ></div>
                        </div>
                      </div>
                    </td>
                  </tr>
                </tbody>
              </table>
            </div>
          </div>

          <div class="sb">
            <div class="stitle">Score Prediction</div>
            <div class="score-zone">
              <div class="sz-head">
                Everton vs Liverpool · First Derby at Hill Dickinson
              </div>
              <div class="s-boxes">
                <div class="sbox">
                  <div class="sbox-lbl">Half-Time</div>
                  <div class="sbox-score">0–0</div>
                  <div class="sbox-prob">~38% — Derby caution</div>
                </div>
                <div class="sbox feat">
                  <div class="sbox-lbl">Full-Time ★</div>
                  <div class="sbox-score feat-s">1–1</div>
                  <div class="sbox-prob">Draw ~36% — 6 of last 8 at EFC</div>
                </div>
                <div class="sbox">
                  <div class="sbox-lbl">Upset Pick</div>
                  <div class="sbox-score">1–0</div>
                  <div class="sbox-prob">Everton ~26% — Beto form</div>
                </div>
              </div>
              <div class="sz-note">
                <strong>Why 1-1:</strong> 6 of the last 8 Merseyside derbies at
                Everton ended in draws. 4 of the last 19 derbies had over 3
                goals — this is a low-scoring fixture by nature. Everton's form
                is excellent (W3 D1 last 4) but Liverpool's quality (Salah,
                Wirtz, Mac Allister) prevents a clean Everton win in most
                scenarios. Liverpool's terrible away form (L4 in a row) and
                psychological fallout from PSG elimination opens the door for
                Everton. <strong>Beto has 4 goals in last 5</strong> — Liverpool
                must watch him. Salah's final derby goodbye narrative could
                ignite him. The emotional weight of the new stadium's first
                derby makes this unpredictable — the draw is most probable but
                Everton winning is very plausible.
              </div>
            </div>
          </div>

          <div class="sb">
            <div class="stitle">🟨 Yellow Card Risks</div>
            <div class="yc-list">
              <div class="yc">
                <div class="yc-ico">🟨</div>
                <div class="yc-inf">
                  <div class="yc-n">
                    Idrissa Gueye
                    <span class="yc-c" style="color: #274488"
                      >Everton · DM</span
                    >
                  </div>
                  <div class="yc-r">
                    Everton's hard-tackling DM with 7 PL yellows. Will face
                    Wirtz and Salah, dragging him into desperate challenges.
                    Derby intensity amplifies his foul count.
                  </div>
                </div>
                <div class="risk rh">HIGH</div>
              </div>
              <div class="yc">
                <div class="yc-ico">🟨</div>
                <div class="yc-inf">
                  <div class="yc-n">
                    Ryan Gravenberch
                    <span class="yc-c" style="color: #c8102e"
                      >Liverpool · MF</span
                    >
                  </div>
                  <div class="yc-r">
                    Under pressure all season. Will face Everton's physical
                    press and be forced into desperate fouls. 5 PL bookings, a
                    further booking risks ban.
                  </div>
                </div>
                <div class="risk rh">HIGH</div>
              </div>
              <div class="yc">
                <div class="yc-ico">🟨</div>
                <div class="yc-inf">
                  <div class="yc-n">
                    Ibrahima Konaté
                    <span class="yc-c" style="color: #c8102e"
                      >Liverpool · CB</span
                    >
                  </div>
                  <div class="yc-r">
                    Booked in 4 of his last 6 games across all competitions.
                    Faces Beto — a physical striker with pace. One mistimed
                    challenge could mean a card against the in-form Portuguese
                    striker.
                  </div>
                </div>
                <div class="risk rh">HIGH</div>
              </div>
              <div class="yc">
                <div class="yc-ico">🟨</div>
                <div class="yc-inf">
                  <div class="yc-n">
                    James Garner
                    <span class="yc-c" style="color: #274488"
                      >Everton · MF</span
                    >
                  </div>
                  <div class="yc-r">
                    In excellent form but commits tactical fouls to disrupt
                    Liverpool's flow. 3 goal contributions in last 5 — also
                    threatens but earns yellows in aggressive pressing phases.
                  </div>
                </div>
                <div class="risk rm">MED</div>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>

    <!-- ════════════════════════════════════════════
     MATCH 3 · NOTTINGHAM FOREST vs BURNLEY
════════════════════════════════════════════ -->
    <div class="mc" id="m3">
      <div
        class="sig-strip"
        style="
          background: linear-gradient(
            90deg,
            rgba(232, 0, 61, 0.12),
            rgba(110, 59, 31, 0.1)
          );
          border-bottom: 1px solid rgba(232, 0, 61, 0.2);
        "
      >
        <span style="font-size: 13px">🚨</span>
        <span
          style="
            color: #ff5050;
            font-family: &quot;Oswald&quot;, sans-serif;
            font-weight: 600;
            letter-spacing: 0.5px;
          "
          >RELEGATION SIX-POINTER · Burnley could be relegated THIS
          WEEKEND</span
        >
        <span style="font-size: 13px">⬇️</span>
      </div>
      <div class="card">
        <div
          class="c-bar"
          style="background: linear-gradient(90deg, #e8003d 50%, #6e3b1f 50%)"
        ></div>

        <div class="hero">
          <div class="hero-meta">
            <span
              class="chip"
              style="
                color: #e8003d;
                border-color: rgba(232, 0, 61, 0.35);
                background: rgba(232, 0, 61, 0.09);
              "
              >14:00 BST · City Ground</span
            >
            <span
              class="chip"
              style="
                color: #f5a623;
                border-color: rgba(245, 166, 35, 0.3);
                background: rgba(245, 166, 35, 0.07);
              "
              >Forest 3pts above drop · EL Semi-final</span
            >
            <span
              class="chip"
              style="
                color: #ff3333;
                border-color: rgba(255, 51, 51, 0.3);
                background: rgba(255, 51, 51, 0.07);
              "
              >Burnley 12pts from safety</span
            >
          </div>
          <div class="teams-row">
            <div class="team-col">
              <div class="badge">
                <img
                  src="https://cdn.brandfetch.io/nottinghamforest.co.uk/w/200/h/200"
                  onerror="
                    this.onerror = null;
                    this.src =
                      'https://upload.wikimedia.org/wikipedia/en/thumb/e/e5/Nottingham_Forest_F.C._logo.svg/120px-Nottingham_Forest_F.C._logo.svg.png';
                  "
                  alt="Forest"
                />
              </div>
              <div class="t-name" style="color: #e8003d">Nottingham Forest</div>
              <div class="t-meta">
                16th · ~33 pts<br />UEL Semi-final vs Villa
              </div>
            </div>
            <div class="vs-col">
              <div class="vs">VS</div>
              <div class="ko">14:00</div>
              <div class="venue">
                City Ground · Nottingham<br />~30,400 capacity
              </div>
            </div>
            <div class="team-col">
              <div class="badge">
                <img
                  src="https://cdn.brandfetch.io/idATU8hDrd/theme/dark/logo.svg?c=1bxid64Mup7aczewSAYMX&t=1668077989078"
                  alt="Burnley"
                />
              </div>
              <div class="t-name" style="color: #6e3b1f">Burnley FC</div>
              <div class="t-meta">
                19th · 20 pts<br />Winless last 7 PL · Near-relegated
              </div>
            </div>
          </div>
        </div>

        <div class="cg">
          <div class="sb fw">
            <div class="stitle">Motivation & Match Significance</div>
            <div class="mot-box">
              <span class="hi-alert">RELEGATION WATCH</span> Forest (33pts,
              16th) sit just 3pts above the drop after an extraordinary season —
              3 managers fired, now in the
              <strong>Europa League semi-final vs Aston Villa</strong>. A Forest
              win is essentially must-have for their safety. Burnley (20pts,
              19th) are
              <strong>12pts from safety with only 15 more available</strong> —
              mathematically, they need to win virtually every remaining game.
              <strong
                >Burnley have 0 away wins in their last 10 PL road trips</strong
              >
              and scored just 9.3 shots per game (fewest in the league). Forest:
              Wood/Murillo/Hudson-Odoi all fitness checks after Porto win
              Thursday. Burnley: Cullen (ACL, out), Laurent (suspended), Beyer,
              Roberts, Amdouni, Mejbri all out.
              <strong
                >Heavily mismatched motivation — Forest are European
                semi-finalists, Burnley are nearly down.</strong
              >
            </div>
          </div>

          <div class="sb">
            <div class="stitle">Last 5 Matches</div>
            <div class="form-cols">
              <div>
                <div class="form-team" style="color: #e8003d">
                  <img
                    class="form-ti"
                    src="https://upload.wikimedia.org/wikipedia/en/thumb/e/e5/Nottingham_Forest_F.C._logo.svg/120px-Nottingham_Forest_F.C._logo.svg.png"
                    alt=""
                  />Forest
                </div>
                <div class="fr-list">
                  <div class="fr">
                    <div class="rd W"></div>
                    <div class="fs">1–0</div>
                    <div class="fo">Porto</div>
                    <div class="fc">UEL <span class="tag-sm">Semi-F</span></div>
                  </div>
                  <div class="fr">
                    <div class="rd D"></div>
                    <div class="fs">1–1</div>
                    <div class="fo">Aston Villa</div>
                    <div class="fc">PL Home</div>
                  </div>
                  <div class="fr">
                    <div class="rd W"></div>
                    <div class="fs">3–0</div>
                    <div class="fo">Tottenham</div>
                    <div class="fc">PL Away</div>
                  </div>
                  <div class="fr">
                    <div class="rd D"></div>
                    <div class="fs">2–2</div>
                    <div class="fo">Man City</div>
                    <div class="fc">PL Away</div>
                  </div>
                  <div class="fr">
                    <div class="rd W"></div>
                    <div class="fs">2–1</div>
                    <div class="fo">Porto (Leg 1)</div>
                    <div class="fc">UEL</div>
                  </div>
                </div>
              </div>
              <div>
                <div class="form-team" style="color: #6e3b1f">
                  <img
                    class="form-ti"
                    src="https://cdn.brandfetch.io/idATU8hDrd/theme/dark/logo.svg?c=1bxid64Mup7aczewSAYMX&t=1668077989078"
                    alt=""
                  />Burnley
                </div>
                <div class="fr-list">
                  <div class="fr">
                    <div class="rd L"></div>
                    <div class="fs">0–2</div>
                    <div class="fo">Brighton</div>
                    <div class="fc">PL Home</div>
                  </div>
                  <div class="fr">
                    <div class="rd L"></div>
                    <div class="fs">0–2</div>
                    <div class="fo">Everton</div>
                    <div class="fc">PL Away</div>
                  </div>
                  <div class="fr">
                    <div class="rd D"></div>
                    <div class="fs">0–0</div>
                    <div class="fo">Bournemouth</div>
                    <div class="fc">PL Home</div>
                  </div>
                  <div class="fr">
                    <div class="rd L"></div>
                    <div class="fs">3–4</div>
                    <div class="fo">Brentford</div>
                    <div class="fc">PL Away</div>
                  </div>
                  <div class="fr">
                    <div class="rd L"></div>
                    <div class="fs">0–1</div>
                    <div class="fo">Burnley (agg)</div>
                    <div class="fc">PL Away</div>
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
          </div>

          <div class="sb">
            <div class="stitle">H2H – Last 5 Meetings</div>
            <div class="h2h-bar">
              <div class="hs">
                <div class="hn" style="color: #e8003d">1</div>
                <div class="hl">Forest W</div>
              </div>
              <div class="hv-div"></div>
              <div class="hs">
                <div class="hn" style="color: var(--med)">3</div>
                <div class="hl">Draws</div>
              </div>
              <div class="hv-div"></div>
              <div class="hs">
                <div class="hn" style="color: #6e3b1f">1</div>
                <div class="hl">Burnley W</div>
              </div>
              <div class="hv-div"></div>
              <div class="hs">
                <div class="hn">2.2</div>
                <div class="hl">Avg Goals</div>
              </div>
            </div>
            <div class="h2h-rows">
              <div class="h2h-r">
                <div class="rh">Burnley</div>
                <div class="rs">1–1</div>
                <div class="ra">Forest</div>
                <div class="rx">PL Oct 2025 (this season)</div>
              </div>
              <div class="h2h-r">
                <div class="rh">Forest</div>
                <div class="rs">1–1</div>
                <div class="ra">Burnley</div>
                <div class="rx">PL Jan 2025</div>
              </div>
              <div class="h2h-r">
                <div class="rh">Forest</div>
                <div class="rs">2–0</div>
                <div class="ra">Burnley</div>
                <div class="rx">PL Apr 2024</div>
              </div>
              <div class="h2h-r">
                <div class="rh">Burnley</div>
                <div class="rs">2–2</div>
                <div class="ra">Forest</div>
                <div class="rx">PL Nov 2023</div>
              </div>
              <div class="h2h-r">
                <div class="rh">Forest</div>
                <div class="rs">1–1</div>
                <div class="ra">Burnley</div>
                <div class="rx">PL Aug 2023</div>
              </div>
            </div>
            <p style="font-size: 10px; color: var(--muted); margin-top: 8px">
              1-1 is the most common result in Forest-Burnley H2H (happened 8
              times overall). Both teams scored in 8 of last 10 meetings. Forest
              unbeaten in last 3 H2H.
            </p>
          </div>

          <div class="sb">
            <div class="stitle">Season Averages – PL 25/26</div>
            <div class="avgs-pair">
              <div>
                <div
                  class="avg-team-lbl"
                  style="
                    color: #fff;
                    background: rgba(232, 0, 61, 0.15);
                    border: 1px solid rgba(232, 0, 61, 0.3);
                  "
                >
                  Nott'm Forest
                </div>
                <div class="avg-cells">
                  <div class="ac">
                    <div class="av">12.1</div>
                    <div class="al">Shots</div>
                  </div>
                  <div class="ac">
                    <div class="av">3.9</div>
                    <div class="al">SOT</div>
                  </div>
                  <div class="ac">
                    <div class="av">4.8</div>
                    <div class="al">Corners</div>
                  </div>
                  <div class="ac">
                    <div class="av">11.6</div>
                    <div class="al">Fouls</div>
                  </div>
                  <div class="ac">
                    <div class="av">1.03</div>
                    <div class="al">Gls/Gm</div>
                  </div>
                  <div class="ac">
                    <div class="av">33</div>
                    <div class="al">Points</div>
                  </div>
                </div>
              </div>
              <div>
                <div
                  class="avg-team-lbl"
                  style="
                    color: #fff;
                    background: rgba(110, 59, 31, 0.25);
                    border: 1px solid rgba(110, 59, 31, 0.4);
                  "
                >
                  Burnley
                </div>
                <div class="avg-cells">
                  <div class="ac">
                    <div class="av">9.3</div>
                    <div class="al">Shots</div>
                  </div>
                  <div class="ac">
                    <div class="av">2.8</div>
                    <div class="al">SOT</div>
                  </div>
                  <div class="ac">
                    <div class="av">3.9</div>
                    <div class="al">Corners</div>
                  </div>
                  <div class="ac">
                    <div class="av">13.1</div>
                    <div class="al">Fouls</div>
                  </div>
                  <div class="ac">
                    <div class="av">0.69</div>
                    <div class="al">Gls/Gm</div>
                  </div>
                  <div class="ac">
                    <div class="av">20</div>
                    <div class="al">Points</div>
                  </div>
                </div>
              </div>
            </div>
          </div>

          <div class="sb fw" id="p3">
            <div class="stitle">Weighted Stat Predictions</div>
            <div class="pt-intro">
              <div class="pt-key">
                <div class="pt-kd" style="background: var(--lo)"></div>
                <span style="color: var(--lo); font-weight: 700">Low</span>
              </div>
              <div class="pt-key">
                <div class="pt-kd" style="background: var(--med)"></div>
                <span style="color: var(--med); font-weight: 700">Median</span>
              </div>
              <div class="pt-key">
                <div class="pt-kd" style="background: var(--hi)"></div>
                <span style="color: var(--hi); font-weight: 700">High</span>
              </div>
            </div>
            <div class="ptw">
              <table class="pt">
                <colgroup>
                  <col class="cn" />
                  <col class="ch" />
                  <col class="cm" />
                  <col class="cl" />
                  <col class="cb" />
                </colgroup>
                <thead>
                  <tr>
                    <th>Metric</th>
                    <th class="tc" style="color: #e8003d">FOR</th>
                    <th class="tc" style="color: #6e3b1f">BUR</th>
                    <th class="tc">Total Range</th>
                    <th class="tc" style="color: var(--muted)">Intensity</th>
                  </tr>
                </thead>
                <tbody>
                  <tr>
                    <td class="tn">Corners</td>
                    <td class="tv">
                      <div class="ts-cell">
                        <span class="ts-v" style="color: #e8003d">5</span
                        ><span class="ts-l">med</span>
                      </div>
                    </td>
                    <td class="tv">
                      <div class="ts-cell">
                        <span class="ts-v" style="color: #6e3b1f">4</span
                        ><span class="ts-l">med</span>
                      </div>
                    </td>
                    <td class="tv">
                      <span class="lv">6</span> <span class="mv">9</span>
                      <span class="hv">14</span>
                    </td>
                    <td>
                      <div class="rb-wrap">
                        <div class="rb-track">
                          <div
                            class="rb-fill"
                            data-w="58"
                            style="
                              background: linear-gradient(
                                90deg,
                                #e8003d,
                                #6e3b1f
                              );
                            "
                          ></div>
                        </div>
                      </div>
                    </td>
                  </tr>
                  <tr>
                    <td class="tn">Shots</td>
                    <td class="tv">
                      <div class="ts-cell">
                        <span class="ts-v" style="color: #e8003d">14</span
                        ><span class="ts-l">med</span>
                      </div>
                    </td>
                    <td class="tv">
                      <div class="ts-cell">
                        <span class="ts-v" style="color: #6e3b1f">8</span
                        ><span class="ts-l">med</span>
                      </div>
                    </td>
                    <td class="tv">
                      <span class="lv">16</span> <span class="mv">22</span>
                      <span class="hv">30</span>
                    </td>
                    <td>
                      <div class="rb-wrap">
                        <div class="rb-track">
                          <div
                            class="rb-fill"
                            data-w="64"
                            style="
                              background: linear-gradient(
                                90deg,
                                #e8003d,
                                #6e3b1f
                              );
                            "
                          ></div>
                        </div>
                      </div>
                    </td>
                  </tr>
                  <tr>
                    <td class="tn">Shots on Target</td>
                    <td class="tv">
                      <div class="ts-cell">
                        <span class="ts-v" style="color: #e8003d">5</span
                        ><span class="ts-l">med</span>
                      </div>
                    </td>
                    <td class="tv">
                      <div class="ts-cell">
                        <span class="ts-v" style="color: #6e3b1f">2</span
                        ><span class="ts-l">med</span>
                      </div>
                    </td>
                    <td class="tv">
                      <span class="lv">5</span> <span class="mv">8</span>
                      <span class="hv">14</span>
                    </td>
                    <td>
                      <div class="rb-wrap">
                        <div class="rb-track">
                          <div
                            class="rb-fill"
                            data-w="56"
                            style="
                              background: linear-gradient(
                                90deg,
                                #e8003d,
                                #6e3b1f
                              );
                            "
                          ></div>
                        </div>
                      </div>
                    </td>
                  </tr>
                  <tr>
                    <td class="tn">Fouls</td>
                    <td class="tv">
                      <div class="ts-cell">
                        <span class="ts-v" style="color: #e8003d">12</span
                        ><span class="ts-l">med</span>
                      </div>
                    </td>
                    <td class="tv">
                      <div class="ts-cell">
                        <span class="ts-v" style="color: #6e3b1f">14</span
                        ><span class="ts-l">med</span>
                      </div>
                    </td>
                    <td class="tv">
                      <span class="lv">18</span> <span class="mv">26</span>
                      <span class="hv">38</span>
                    </td>
                    <td>
                      <div class="rb-wrap">
                        <div class="rb-track">
                          <div
                            class="rb-fill"
                            data-w="74"
                            style="
                              background: linear-gradient(
                                90deg,
                                #e8003d,
                                #6e3b1f
                              );
                            "
                          ></div>
                        </div>
                      </div>
                    </td>
                  </tr>
                  <tr>
                    <td class="tn">Throw-ins</td>
                    <td class="tv">
                      <div class="ts-cell">
                        <span class="ts-v" style="color: #e8003d">19</span
                        ><span class="ts-l">med</span>
                      </div>
                    </td>
                    <td class="tv">
                      <div class="ts-cell">
                        <span class="ts-v" style="color: #6e3b1f">19</span
                        ><span class="ts-l">med</span>
                      </div>
                    </td>
                    <td class="tv">
                      <span class="lv">30</span> <span class="mv">38</span>
                      <span class="hv">52</span>
                    </td>
                    <td>
                      <div class="rb-wrap">
                        <div class="rb-track">
                          <div
                            class="rb-fill"
                            data-w="60"
                            style="
                              background: linear-gradient(
                                90deg,
                                #e8003d,
                                #6e3b1f
                              );
                            "
                          ></div>
                        </div>
                      </div>
                    </td>
                  </tr>
                  <tr>
                    <td class="tn">Goal Kicks</td>
                    <td class="tv">
                      <div class="ts-cell">
                        <span class="ts-v" style="color: #e8003d">10</span
                        ><span class="ts-l">med</span>
                      </div>
                    </td>
                    <td class="tv">
                      <div class="ts-cell">
                        <span class="ts-v" style="color: #6e3b1f">12</span
                        ><span class="ts-l">med</span>
                      </div>
                    </td>
                    <td class="tv">
                      <span class="lv">15</span> <span class="mv">22</span>
                      <span class="hv">32</span>
                    </td>
                    <td>
                      <div class="rb-wrap">
                        <div class="rb-track">
                          <div
                            class="rb-fill"
                            data-w="66"
                            style="
                              background: linear-gradient(
                                90deg,
                                #e8003d,
                                #6e3b1f
                              );
                            "
                          ></div>
                        </div>
                      </div>
                    </td>
                  </tr>
                  <tr>
                    <td class="tn">Tackles</td>
                    <td class="tv">
                      <div class="ts-cell">
                        <span class="ts-v" style="color: #e8003d">15</span
                        ><span class="ts-l">med</span>
                      </div>
                    </td>
                    <td class="tv">
                      <div class="ts-cell">
                        <span class="ts-v" style="color: #6e3b1f">18</span
                        ><span class="ts-l">med</span>
                      </div>
                    </td>
                    <td class="tv">
                      <span class="lv">24</span> <span class="mv">33</span>
                      <span class="hv">48</span>
                    </td>
                    <td>
                      <div class="rb-wrap">
                        <div class="rb-track">
                          <div
                            class="rb-fill"
                            data-w="76"
                            style="
                              background: linear-gradient(
                                90deg,
                                #e8003d,
                                #6e3b1f
                              );
                            "
                          ></div>
                        </div>
                      </div>
                    </td>
                  </tr>
                </tbody>
              </table>
            </div>
          </div>

          <div class="sb">
            <div class="stitle">Score Prediction</div>
            <div class="score-zone">
              <div class="sz-head">Nottingham Forest vs Burnley</div>
              <div class="s-boxes">
                <div class="sbox">
                  <div class="sbox-lbl">Half-Time</div>
                  <div class="sbox-score">1–0</div>
                  <div class="sbox-prob">Forest ~42%</div>
                </div>
                <div class="sbox feat">
                  <div class="sbox-lbl">Full-Time ★</div>
                  <div class="sbox-score feat-s">2–0</div>
                  <div class="sbox-prob">Forest clean sheet ~33%</div>
                </div>
                <div class="sbox">
                  <div class="sbox-lbl">Alt: BTTS</div>
                  <div class="sbox-score">2–1</div>
                  <div class="sbox-prob">~24% — 8 of last 10 H2H BTTS</div>
                </div>
              </div>
              <div class="sz-note">
                <strong>Why Forest 2-0:</strong> Forest on a 6-game unbeaten
                run, boosted by Porto Europa League win Thursday. City Ground
                atmosphere will be supercharged. Burnley have 0 away wins in
                last 10 PL trips and scored fewest shots of any PL team. Burnley
                can't afford to concede early — but Forest press relentlessly
                and Gibbs-White is in the form of his career. The 1-1 H2H
                history is notable but Burnley's current state means their past
                performance doesn't translate — they've scored in just 25% of
                away games recently.
              </div>
            </div>
          </div>

          <div class="sb">
            <div class="stitle">🟨 Yellow Card Risks</div>
            <div class="yc-list">
              <div class="yc">
                <div class="yc-ico">🟨</div>
                <div class="yc-inf">
                  <div class="yc-n">
                    James Ward-Prowse
                    <span class="yc-c" style="color: #6e3b1f"
                      >Burnley · MF</span
                    >
                  </div>
                  <div class="yc-r">
                    Burnley's midfield pivot who fouls to break transitions.
                    Desperate play in a must-win context creates reckless
                    challenges. 7 PL yellows this season.
                  </div>
                </div>
                <div class="risk rh">HIGH</div>
              </div>
              <div class="yc">
                <div class="yc-ico">🟨</div>
                <div class="yc-inf">
                  <div class="yc-n">
                    Ibrahim Sangaré
                    <span class="yc-c" style="color: #e8003d">Forest · DM</span>
                  </div>
                  <div class="yc-r">
                    Aggressive DM in a 6-game unbeaten run. Faces Burnley's
                    desperate pressing — Sangaré will foul to protect territory
                    and commit tactical bookings.
                  </div>
                </div>
                <div class="risk rh">HIGH</div>
              </div>
              <div class="yc">
                <div class="yc-ico">🟨</div>
                <div class="yc-inf">
                  <div class="yc-n">
                    Florentino Luís
                    <span class="yc-c" style="color: #6e3b1f"
                      >Burnley · DM</span
                    >
                  </div>
                  <div class="yc-r">
                    Physical holding midfielder who tackles hard when Burnley's
                    defence is under pressure. Faces Gibbs-White's darting runs
                    through the lines.
                  </div>
                </div>
                <div class="risk rm">MED</div>
              </div>
              <div class="yc">
                <div class="yc-ico">🟨</div>
                <div class="yc-inf">
                  <div class="yc-n">
                    Ola Aina
                    <span class="yc-c" style="color: #e8003d">Forest · RB</span>
                  </div>
                  <div class="yc-r">
                    Adventurous fullback who gets caught out of position and
                    fouls on the counter. 4 PL yellows this season, faces
                    Burnley's desperate wide play.
                  </div>
                </div>
                <div class="risk rm">MED</div>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>

    <!-- ════════════════════════════════════════════
     MATCH 4 · MAN CITY vs ARSENAL — TITLE DECIDER
════════════════════════════════════════════ -->
    <div class="mc" id="m4">
      <div
        class="sig-strip"
        style="
          background: linear-gradient(
            90deg,
            rgba(108, 171, 221, 0.18),
            rgba(239, 1, 7, 0.12)
          );
          border-bottom: 1px solid rgba(108, 171, 221, 0.25);
        "
      >
        <span style="font-size: 15px">🏆</span>
        <span
          style="
            color: #fff;
            font-family: &quot;Oswald&quot;, sans-serif;
            font-weight: 700;
            letter-spacing: 1px;
            font-size: 13px;
          "
          >PREMIER LEAGUE TITLE DECIDER · Arsenal 1st (70pts) vs Man City 2nd
          (64pts, game in hand)</span
        >
        <span style="font-size: 15px">🏆</span>
      </div>
      <div class="card">
        <div
          class="c-bar"
          style="background: linear-gradient(90deg, #6cabdd 50%, #ef0107 50%)"
        ></div>

        <div class="hero">
          <div class="hero-meta">
            <span
              class="chip"
              style="
                color: #6cabdd;
                border-color: rgba(108, 171, 221, 0.35);
                background: rgba(108, 171, 221, 0.1);
              "
              >16:30 BST · Etihad Stadium</span
            >
            <span
              class="chip"
              style="
                color: #ffe84a;
                border-color: rgba(255, 232, 74, 0.3);
                background: rgba(255, 232, 74, 0.07);
              "
              >⚡ TITLE RACE — City can close to 3pts</span
            >
            <span
              class="chip"
              style="
                color: var(--pl-green);
                border-color: rgba(0, 255, 133, 0.25);
                background: rgba(0, 255, 133, 0.07);
              "
              >Arsenal: Win = near-certain title</span
            >
          </div>
          <div class="teams-row">
            <div class="team-col">
              <div class="badge">
                <img
                  src="https://cdn.brandfetch.io/mancity.com/w/200/h/200"
                  onerror="
                    this.onerror = null;
                    this.src =
                      'https://upload.wikimedia.org/wikipedia/en/thumb/e/eb/Manchester_City_FC_badge.svg/120px-Manchester_City_FC_badge.svg.png';
                  "
                  alt="Man City"
                />
              </div>
              <div class="t-name" style="color: #6cabdd">Manchester City</div>
              <div class="t-meta">
                2nd · 64 pts (game in hand)<br />W9 straight all comps
              </div>
            </div>
            <div class="vs-col">
              <div class="vs">VS</div>
              <div class="ko">16:30</div>
              <div class="venue">
                Etihad Stadium · Manchester<br />55,097 capacity
              </div>
            </div>
            <div class="team-col">
              <div class="badge">
                <img
                  src="https://cdn.brandfetch.io/arsenal.com/w/200/h/200"
                  onerror="
                    this.onerror = null;
                    this.src =
                      'https://upload.wikimedia.org/wikipedia/en/thumb/5/53/Arsenal_FC.svg/120px-Arsenal_FC.svg.png';
                  "
                  alt="Arsenal"
                />
              </div>
              <div class="t-name" style="color: #ef0107">Arsenal FC</div>
              <div class="t-meta">
                1st · 70 pts (21W-7D-4L)<br />Unbeaten 8 PL away games
              </div>
            </div>
          </div>
        </div>

        <div class="cg">
          <div class="sb fw">
            <div class="stitle">Motivation & Significance — MAXIMUM STAKES</div>
            <div class="mot-box">
              <span class="hi-alert">TITLE DEFINING</span>
              <strong
                >A Man City win = closes to 3pts with game in hand = City become
                favourites</strong
              >. An Arsenal win = near-certain title. A draw largely benefits
              Arsenal. This is the most important PL game of the season. City
              are unbeaten in last 14 PL home games, W9 all comps in a row (beat
              Arsenal EFL Cup 2-0, Liverpool 4-0 FAC, Chelsea 3-0 PL). Arsenal
              are wobbling —
              <strong>just 1 win in last 5 PL, only 3 goals in that run</strong
              >, lost to Bournemouth 2-1 last home game. Arsenal won't win at
              the Etihad since January 2015. Arsenal injuries crisis:
              <strong
                >Odegaard (out), Saka (doubtful), Merino (out), Calafiori
                (doubtful), Timber (doubtful), Madueke (knee)</strong
              >. City injuries: Dias (out), Gvardiol (out), Stones/O'Reilly
              (doubts). Haaland: 22 PL goals, 4 goals in last 2 home games.
              Opta: City 37.7%, Draw 26.4%, Arsenal 35.8% — impossibly tight.
            </div>
          </div>

          <div class="sb">
            <div class="stitle">Last 5–10 Matches — Form Trends</div>
            <div class="form-cols">
              <div>
                <div class="form-team" style="color: #6cabdd">
                  <img
                    class="form-ti"
                    src="https://upload.wikimedia.org/wikipedia/en/thumb/e/eb/Manchester_City_FC_badge.svg/120px-Manchester_City_FC_badge.svg.png"
                    alt=""
                  />Man City
                </div>
                <div class="fr-list">
                  <div class="fr">
                    <div class="rd W"></div>
                    <div class="fs">3–0</div>
                    <div class="fo">Chelsea</div>
                    <div class="fc">PL Away</div>
                  </div>
                  <div class="fr">
                    <div class="rd W"></div>
                    <div class="fs">4–0</div>
                    <div class="fo">Liverpool</div>
                    <div class="fc">FAC</div>
                  </div>
                  <div class="fr">
                    <div class="rd W"></div>
                    <div class="fs">2–0</div>
                    <div class="fo">Arsenal</div>
                    <div class="fc">EFL Cup Final</div>
                  </div>
                  <div class="fr">
                    <div class="rd D"></div>
                    <div class="fs">2–2</div>
                    <div class="fo">Nott'm Forest</div>
                    <div class="fc">PL Away</div>
                  </div>
                  <div class="fr">
                    <div class="rd W"></div>
                    <div class="fs">5–0</div>
                    <div class="fo">St Pauli</div>
                    <div class="fc">Friendly</div>
                  </div>
                </div>
              </div>
              <div>
                <div class="form-team" style="color: #ef0107">
                  <img
                    class="form-ti"
                    src="https://upload.wikimedia.org/wikipedia/en/thumb/5/53/Arsenal_FC.svg/120px-Arsenal_FC.svg.png"
                    alt=""
                  />Arsenal
                </div>
                <div class="fr-list">
                  <div class="fr">
                    <div class="rd D"></div>
                    <div class="fs">0–0</div>
                    <div class="fo">Sporting CP</div>
                    <div class="fc">UCL <span class="tag-sm">Semi-F</span></div>
                  </div>
                  <div class="fr">
                    <div class="rd L"></div>
                    <div class="fs">1–2</div>
                    <div class="fo">Bournemouth</div>
                    <div class="fc">PL Home</div>
                  </div>
                  <div class="fr">
                    <div class="rd W"></div>
                    <div class="fs">2–0</div>
                    <div class="fo">Fulham</div>
                    <div class="fc">PL Home</div>
                  </div>
                  <div class="fr">
                    <div class="rd L"></div>
                    <div class="fs">1–2</div>
                    <div class="fo">Brighton</div>
                    <div class="fc">PL Away</div>
                  </div>
                  <div class="fr">
                    <div class="rd L"></div>
                    <div class="fs">1–2</div>
                    <div class="fo">Southampton</div>
                    <div class="fc">FAC Away</div>
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
          </div>

          <div class="sb">
            <div class="stitle">H2H – Last 5 PL Meetings</div>
            <div class="h2h-bar">
              <div class="hs">
                <div class="hn" style="color: #6cabdd">2</div>
                <div class="hl">City W</div>
              </div>
              <div class="hv-div"></div>
              <div class="hs">
                <div class="hn" style="color: var(--med)">2</div>
                <div class="hl">Draws</div>
              </div>
              <div class="hv-div"></div>
              <div class="hs">
                <div class="hn" style="color: #ef0107">1</div>
                <div class="hl">Arsenal W</div>
              </div>
              <div class="hv-div"></div>
              <div class="hs">
                <div class="hn">2.8</div>
                <div class="hl">Avg Goals</div>
              </div>
            </div>
            <div class="h2h-rows">
              <div class="h2h-r">
                <div class="rh">Arsenal</div>
                <div class="rs">1–1</div>
                <div class="ra">Man City</div>
                <div class="rx">
                  PL Sep 2025 — Martinelli 90+' (this season)
                </div>
              </div>
              <div class="h2h-r">
                <div class="rh">Man City</div>
                <div class="rs">2–0</div>
                <div class="ra">Arsenal</div>
                <div class="rx">EFL Cup Final 2026 (O'Reilly ×2)</div>
              </div>
              <div class="h2h-r">
                <div class="rh">Arsenal</div>
                <div class="rs">2–2</div>
                <div class="ra">Man City</div>
                <div class="rx">PL Mar 2025 — Stones 98' (Trossard red)</div>
              </div>
              <div class="h2h-r">
                <div class="rh">Man City</div>
                <div class="rs">4–1</div>
                <div class="ra">Arsenal</div>
                <div class="rx">PL Apr 2024 (title blow)</div>
              </div>
              <div class="h2h-r">
                <div class="rh">Man City</div>
                <div class="rs">0–1</div>
                <div class="ra">Arsenal</div>
                <div class="rx">PL Jan 2024 — Arsenal last Etihad win</div>
              </div>
            </div>
            <p style="font-size: 10px; color: var(--muted); margin-top: 8px">
              City unbeaten in last 10 PL home games vs Arsenal (W7 D3). Both
              teams scored in last 5 H2H. Arsenal last won at Etihad: Jan 2015.
              BTTS in 4 of last 5 PL meetings.
            </p>
          </div>

          <div class="sb">
            <div class="stitle">Season Averages – PL 25/26</div>
            <div class="avgs-pair">
              <div>
                <div
                  class="avg-team-lbl"
                  style="
                    color: #fff;
                    background: rgba(108, 171, 221, 0.2);
                    border: 1px solid rgba(108, 171, 221, 0.35);
                  "
                >
                  Man City
                </div>
                <div class="avg-cells">
                  <div class="ac">
                    <div class="av">18.4</div>
                    <div class="al">Shots</div>
                  </div>
                  <div class="ac">
                    <div class="av">6.8</div>
                    <div class="al">SOT</div>
                  </div>
                  <div class="ac">
                    <div class="av">5.8</div>
                    <div class="al">Corners</div>
                  </div>
                  <div class="ac">
                    <div class="av">11.1</div>
                    <div class="al">Fouls</div>
                  </div>
                  <div class="ac">
                    <div class="av">2.06</div>
                    <div class="al">Gls/Gm</div>
                  </div>
                  <div class="ac">
                    <div class="av">64</div>
                    <div class="al">Points</div>
                  </div>
                </div>
              </div>
              <div>
                <div
                  class="avg-team-lbl"
                  style="
                    color: #fff;
                    background: rgba(239, 1, 7, 0.15);
                    border: 1px solid rgba(239, 1, 7, 0.3);
                  "
                >
                  Arsenal
                </div>
                <div class="avg-cells">
                  <div class="ac">
                    <div class="av">15.6</div>
                    <div class="al">Shots</div>
                  </div>
                  <div class="ac">
                    <div class="av">5.4</div>
                    <div class="al">SOT</div>
                  </div>
                  <div class="ac">
                    <div class="av">6.2</div>
                    <div class="al">Corners</div>
                  </div>
                  <div class="ac">
                    <div class="av">10.8</div>
                    <div class="al">Fouls</div>
                  </div>
                  <div class="ac">
                    <div class="av">1.88</div>
                    <div class="al">Gls/Gm</div>
                  </div>
                  <div class="ac">
                    <div class="av">70</div>
                    <div class="al">Points</div>
                  </div>
                </div>
              </div>
            </div>
            <p style="font-size: 10px; color: var(--muted); margin-top: 8px">
              City avg 105 Bundesliga goals equivalent output. Haaland: 22 PL
              goals. Arsenal unbeaten in 8 PL away games. Arsenal scored just 3
              goals in last 5 PL. City unbeaten last 14 PL home.
            </p>
          </div>

          <div class="sb fw" id="p4">
            <div class="stitle">
              Weighted Stat Predictions — Title Decider Context
            </div>
            <div class="pt-intro">
              <div class="pt-key">
                <div class="pt-kd" style="background: var(--lo)"></div>
                <span style="color: var(--lo); font-weight: 700">Low</span>
              </div>
              <div class="pt-key">
                <div class="pt-kd" style="background: var(--med)"></div>
                <span style="color: var(--med); font-weight: 700">Median</span>
              </div>
              <div class="pt-key">
                <div class="pt-kd" style="background: var(--hi)"></div>
                <span style="color: var(--hi); font-weight: 700">High</span>
              </div>
            </div>
            <div class="ptw">
              <table class="pt">
                <colgroup>
                  <col class="cn" />
                  <col class="ch" />
                  <col class="cm" />
                  <col class="cl" />
                  <col class="cb" />
                </colgroup>
                <thead>
                  <tr>
                    <th>Metric</th>
                    <th class="tc" style="color: #6cabdd">MCI</th>
                    <th class="tc" style="color: #ef0107">ARS</th>
                    <th class="tc">Total Range</th>
                    <th class="tc" style="color: var(--muted)">Intensity</th>
                  </tr>
                </thead>
                <tbody>
                  <tr>
                    <td class="tn">Corners</td>
                    <td class="tv">
                      <div class="ts-cell">
                        <span class="ts-v" style="color: #6cabdd">6</span
                        ><span class="ts-l">med</span>
                      </div>
                    </td>
                    <td class="tv">
                      <div class="ts-cell">
                        <span class="ts-v" style="color: #ef0107">6</span
                        ><span class="ts-l">med</span>
                      </div>
                    </td>
                    <td class="tv">
                      <span class="lv">8</span> <span class="mv">12</span>
                      <span class="hv">18</span>
                    </td>
                    <td>
                      <div class="rb-wrap">
                        <div class="rb-track">
                          <div
                            class="rb-fill"
                            data-w="74"
                            style="
                              background: linear-gradient(
                                90deg,
                                #6cabdd,
                                #ef0107
                              );
                            "
                          ></div>
                        </div>
                      </div>
                    </td>
                  </tr>
                  <tr>
                    <td class="tn">Shots</td>
                    <td class="tv">
                      <div class="ts-cell">
                        <span class="ts-v" style="color: #6cabdd">18</span
                        ><span class="ts-l">med</span>
                      </div>
                    </td>
                    <td class="tv">
                      <div class="ts-cell">
                        <span class="ts-v" style="color: #ef0107">12</span
                        ><span class="ts-l">med</span>
                      </div>
                    </td>
                    <td class="tv">
                      <span class="lv">22</span> <span class="mv">30</span>
                      <span class="hv">42</span>
                    </td>
                    <td>
                      <div class="rb-wrap">
                        <div class="rb-track">
                          <div
                            class="rb-fill"
                            data-w="80"
                            style="
                              background: linear-gradient(
                                90deg,
                                #6cabdd,
                                #ef0107
                              );
                            "
                          ></div>
                        </div>
                      </div>
                    </td>
                  </tr>
                  <tr>
                    <td class="tn">Shots on Target</td>
                    <td class="tv">
                      <div class="ts-cell">
                        <span class="ts-v" style="color: #6cabdd">7</span
                        ><span class="ts-l">med</span>
                      </div>
                    </td>
                    <td class="tv">
                      <div class="ts-cell">
                        <span class="ts-v" style="color: #ef0107">5</span
                        ><span class="ts-l">med</span>
                      </div>
                    </td>
                    <td class="tv">
                      <span class="lv">7</span> <span class="mv">12</span>
                      <span class="hv">20</span>
                    </td>
                    <td>
                      <div class="rb-wrap">
                        <div class="rb-track">
                          <div
                            class="rb-fill"
                            data-w="76"
                            style="
                              background: linear-gradient(
                                90deg,
                                #6cabdd,
                                #ef0107
                              );
                            "
                          ></div>
                        </div>
                      </div>
                    </td>
                  </tr>
                  <tr>
                    <td class="tn">Fouls</td>
                    <td class="tv">
                      <div class="ts-cell">
                        <span class="ts-v" style="color: #6cabdd">11</span
                        ><span class="ts-l">med</span>
                      </div>
                    </td>
                    <td class="tv">
                      <div class="ts-cell">
                        <span class="ts-v" style="color: #ef0107">12</span
                        ><span class="ts-l">med</span>
                      </div>
                    </td>
                    <td class="tv">
                      <span class="lv">16</span> <span class="mv">23</span>
                      <span class="hv">34</span>
                    </td>
                    <td>
                      <div class="rb-wrap">
                        <div class="rb-track">
                          <div
                            class="rb-fill"
                            data-w="70"
                            style="
                              background: linear-gradient(
                                90deg,
                                #6cabdd,
                                #ef0107
                              );
                            "
                          ></div>
                        </div>
                      </div>
                    </td>
                  </tr>
                  <tr>
                    <td class="tn">Throw-ins</td>
                    <td class="tv">
                      <div class="ts-cell">
                        <span class="ts-v" style="color: #6cabdd">20</span
                        ><span class="ts-l">med</span>
                      </div>
                    </td>
                    <td class="tv">
                      <div class="ts-cell">
                        <span class="ts-v" style="color: #ef0107">18</span
                        ><span class="ts-l">med</span>
                      </div>
                    </td>
                    <td class="tv">
                      <span class="lv">30</span> <span class="mv">38</span>
                      <span class="hv">52</span>
                    </td>
                    <td>
                      <div class="rb-wrap">
                        <div class="rb-track">
                          <div
                            class="rb-fill"
                            data-w="66"
                            style="
                              background: linear-gradient(
                                90deg,
                                #6cabdd,
                                #ef0107
                              );
                            "
                          ></div>
                        </div>
                      </div>
                    </td>
                  </tr>
                  <tr>
                    <td class="tn">Goal Kicks</td>
                    <td class="tv">
                      <div class="ts-cell">
                        <span class="ts-v" style="color: #6cabdd">9</span
                        ><span class="ts-l">med</span>
                      </div>
                    </td>
                    <td class="tv">
                      <div class="ts-cell">
                        <span class="ts-v" style="color: #ef0107">11</span
                        ><span class="ts-l">med</span>
                      </div>
                    </td>
                    <td class="tv">
                      <span class="lv">14</span> <span class="mv">20</span>
                      <span class="hv">30</span>
                    </td>
                    <td>
                      <div class="rb-wrap">
                        <div class="rb-track">
                          <div
                            class="rb-fill"
                            data-w="64"
                            style="
                              background: linear-gradient(
                                90deg,
                                #6cabdd,
                                #ef0107
                              );
                            "
                          ></div>
                        </div>
                      </div>
                    </td>
                  </tr>
                  <tr>
                    <td class="tn">Tackles</td>
                    <td class="tv">
                      <div class="ts-cell">
                        <span class="ts-v" style="color: #6cabdd">14</span
                        ><span class="ts-l">med</span>
                      </div>
                    </td>
                    <td class="tv">
                      <div class="ts-cell">
                        <span class="ts-v" style="color: #ef0107">16</span
                        ><span class="ts-l">med</span>
                      </div>
                    </td>
                    <td class="tv">
                      <span class="lv">22</span> <span class="mv">30</span>
                      <span class="hv">42</span>
                    </td>
                    <td>
                      <div class="rb-wrap">
                        <div class="rb-track">
                          <div
                            class="rb-fill"
                            data-w="72"
                            style="
                              background: linear-gradient(
                                90deg,
                                #6cabdd,
                                #ef0107
                              );
                            "
                          ></div>
                        </div>
                      </div>
                    </td>
                  </tr>
                </tbody>
              </table>
            </div>
          </div>

          <div class="sb">
            <div class="stitle">Score Prediction — The Title Showdown</div>
            <div class="score-zone">
              <div class="sz-head">
                Manchester City vs Arsenal · Etihad Stadium
              </div>
              <div class="s-boxes">
                <div class="sbox">
                  <div class="sbox-lbl">Half-Time</div>
                  <div class="sbox-score">1–0</div>
                  <div class="sbox-prob">City ~38% — Haaland home</div>
                </div>
                <div class="sbox feat">
                  <div class="sbox-lbl">Full-Time ★ Best Pick</div>
                  <div class="sbox-score feat-s">1–1</div>
                  <div class="sbox-prob">Draw ~34% — Title narrative</div>
                </div>
                <div class="sbox">
                  <div class="sbox-lbl">Alt: City Win</div>
                  <div class="sbox-score">2–1</div>
                  <div class="sbox-prob">~28% — City favourites</div>
                </div>
              </div>
              <div class="sz-note">
                <strong>Why 1-1 Draw:</strong> This has been the most common
                outcome in recent high-stakes Arsenal-City meetings — the Sep
                2025 PL draw (1-1 Martinelli 90') and the 2-2 from last season
                both ended level after extraordinary drama. Arsenal won't attack
                open-faced at the Etihad given their form — Arteta will set up
                to be hard to beat and nick a goal on the counter. A 6-point
                lead with a game in hand means
                <strong
                  >Arsenal's best outcome in risk-adjusted terms is a
                  draw</strong
                >. City need to win to genuinely threaten and will attack from
                minute one. Haaland (4 goals in last 2 home games) is the main
                threat. Arsenal injuries mean they lack creativity without Saka
                and Odegaard.
                <strong
                  >BTTS in 4 of last 5 H2H — both teams will score.</strong
                >
              </div>
            </div>
          </div>

          <div class="sb">
            <div class="stitle">🟨 Yellow Card Risks</div>
            <div class="yc-list">
              <div class="yc">
                <div class="yc-ico">🟨</div>
                <div class="yc-inf">
                  <div class="yc-n">
                    Rodri
                    <span class="yc-c" style="color: #6cabdd"
                      >Man City · DM</span
                    >
                  </div>
                  <div class="yc-r">
                    Title decider intensity — Rodri fouls frequently to break
                    Arsenal's rare midfield breaks. Faces Rice and Zubimendi in
                    a battle of the pivot players. Already 6 PL yellows this
                    season.
                  </div>
                </div>
                <div class="risk rh">HIGH</div>
              </div>
              <div class="yc">
                <div class="yc-ico">🟨</div>
                <div class="yc-inf">
                  <div class="yc-n">
                    Declan Rice
                    <span class="yc-c" style="color: #ef0107"
                      >Arsenal · DM</span
                    >
                  </div>
                  <div class="yc-r">
                    Arsenal's midfield shield who will be under extreme pressure
                    from City's attacking press. Facing Bernardo Silva and
                    Cherki's movement — a desperate foul is near-inevitable in a
                    game of this magnitude.
                  </div>
                </div>
                <div class="risk rh">HIGH</div>
              </div>
              <div class="yc">
                <div class="yc-ico">🟨</div>
                <div class="yc-inf">
                  <div class="yc-n">
                    Martin Zubimendi
                    <span class="yc-c" style="color: #ef0107"
                      >Arsenal · MF</span
                    >
                  </div>
                  <div class="yc-r">
                    Both Zubimendi and Nørgaard are on booking warning for the
                    UCL semi-final, meaning any bookings here don't affect
                    European play — but Zubimendi's aggressive ball-winning
                    style in such a high-stakes atmosphere makes him a
                    near-certainty for a foul.
                  </div>
                </div>
                <div class="risk rh">HIGH</div>
              </div>
              <div class="yc">
                <div class="yc-ico">🟨</div>
                <div class="yc-inf">
                  <div class="yc-n">
                    Rayan Cherki
                    <span class="yc-c" style="color: #6cabdd"
                      >Man City · AM</span
                    >
                  </div>
                  <div class="yc-r">
                    Exuberant 21-year-old who presses relentlessly and gets
                    frustrated when fouled. City's most dynamic player this
                    month — also earns yellows for over-enthusiastic pressing. 1
                    assist every 138 minutes in PL.
                  </div>
                </div>
                <div class="risk rm">MED</div>
              </div>
              <div class="yc">
                <div class="yc-ico">🟨</div>
                <div class="yc-inf">
                  <div class="yc-n">
                    William Saliba
                    <span class="yc-c" style="color: #ef0107"
                      >Arsenal · CB</span
                    >
                  </div>
                  <div class="yc-r">
                    Faces Haaland in a battle that could define the title race.
                    Saliba vs Haaland is the key individual duel — one mistimed
                    challenge against the Norwegian scoring machine = booking.
                    The stakes make this fight explosive.
                  </div>
                </div>
                <div class="risk rm">MED</div>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>

    <!-- FOOTER -->

    <footer
      style="
        text-align: center;
        padding: 24px 16px;
        font-family: &quot;Inter&quot;, sans-serif;
        font-size: 11px;
        color: var(--muted);
        border-top: 1px solid var(--border);
      "
    >
      <p>
        <strong>Team Bilbo Statistical Analysis</strong><br />
        Predictions are statistical estimates based on historical profiles and
        Premier League dynamics.<br />
      </p>
      <p style="margin-top: 4px">
        · Premier League Matchweek 33 · 19/04/2026 · Statistical predictions are
        weighted estimates ·
      </p>
      <p style="margin-top: 4px; color: #f5522a" />
        <strong>NOT FINANCIAL ADVICE</strong>.
      </p>
    </footer>

    <script>
      // Bar fill animation
      (function () {
        const fills = document.querySelectorAll(".rb-fill[data-w]");
        if (!("IntersectionObserver" in window)) {
          fills.forEach(
            (f) => (f.style.width = f.getAttribute("data-w") + "%"),
          );
          return;
        }
        const obs = new IntersectionObserver(
          (entries) => {
            entries.forEach((e) => {
              if (e.isIntersecting) {
                const el = e.target;
                setTimeout(() => {
                  el.style.width = el.getAttribute("data-w") + "%";
                }, 200);
                obs.unobserve(el);
              }
            });
          },
          { threshold: 0.3 },
        );
        fills.forEach((f) => obs.observe(f));
      })();

      // Count-up for avg cells
      (function () {
        const cells = document.querySelectorAll(".ac .av");
        if (!("IntersectionObserver" in window)) return;
        const obs = new IntersectionObserver(
          (entries) => {
            entries.forEach((e) => {
              if (e.isIntersecting) {
                const el = e.target;
                const raw = el.textContent.trim();
                const num = parseFloat(raw);
                if (!isNaN(num) && !el.dataset.done) {
                  el.dataset.done = "1";
                  let cur = 0,
                    step = num / (700 / 16);
                  const t = setInterval(() => {
                    cur += step;
                    if (cur >= num) {
                      cur = num;
                      clearInterval(t);
                    }
                    el.textContent = raw.includes(".")
                      ? cur.toFixed(1)
                      : Math.round(cur);
                  }, 16);
                }
                obs.unobserve(el);
              }
            });
          },
          { threshold: 0.8 },
        );
        cells.forEach((c) => obs.observe(c));
      })();
    </script>
