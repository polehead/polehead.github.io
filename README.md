<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width,initial-scale=1.0" />
    <title>England vs Uruguay · WC2026 Warm-Up · 27 March 2026</title>
    <link
      href="https://fonts.googleapis.com/css2?family=Outfit:wght@300;400;500;600;700;800;900&family=JetBrains+Mono:wght@400;500;600&display=swap"
      rel="stylesheet"
    />
    <style>
      /* ══ DESIGN TOKENS ══ */
      :root {
        --bg: #050a0f;
        --bg2: #080d14;
        --card: #0c1320;
        --card2: #101829;
        --border: #152030;
        --border2: #1e2f44;
        --fg: #f0f4f8;
        --fg2: #7090b0;
        --fg3: #2a4060;

        --eng: #cf1820;
        /* England red */
        --eng-d: rgba(207, 24, 32, 0.13);
        --uru: #5bb4e4;
        /* Uruguay sky blue */
        --uru-d: rgba(91, 180, 228, 0.13);
        --gold: #f5c518;
        --gold-d: rgba(245, 197, 24, 0.12);
        --green: #30d87a;
        --green-d: rgba(48, 216, 122, 0.12);
        --orange: #ff8c42;
        --orange-d: rgba(255, 140, 66, 0.12);
        --purple: #b07aff;
        --purple-d: rgba(176, 122, 255, 0.12);
        --red: #ff5c5c;
        --red-d: rgba(255, 92, 92, 0.12);
        --sky: #38c3f8;
        --sky-d: rgba(56, 195, 248, 0.11);

        --r: 12px;
        --rsm: 8px;
        --rxs: 5px;
        --px: 15px;
      }

      *,
      *::before,
      *::after {
        box-sizing: border-box;
        margin: 0;
        padding: 0;
      }

      html {
        font-size: 18px;
        scroll-behavior: smooth;
        -webkit-text-size-adjust: 100%;
      }

      body {
        background: var(--bg);
        color: var(--fg);
        font-family: "Outfit", sans-serif;
        line-height: 1.5;
        min-height: 100vh;
        overflow-x: hidden;
        background-image:
          radial-gradient(
            ellipse 75% 45% at 5% 0%,
            rgba(207, 24, 32, 0.06) 0%,
            transparent 55%
          ),
          radial-gradient(
            ellipse 70% 45% at 95% 100%,
            rgba(91, 180, 228, 0.05) 0%,
            transparent 55%
          );
      }

      body::before {
        content: "";
        position: fixed;
        inset: 0;
        z-index: 0;
        pointer-events: none;
        opacity: 0.018;
        background-image: url("data:image/svg+xml,%3Csvg xmlns='http://www.w3.org/2000/svg' width='256' height='256'%3E%3Cfilter id='n'%3E%3CfeTurbulence type='fractalNoise' baseFrequency='.85' numOctaves='4' stitchTiles='stitch'/%3E%3C/filter%3E%3Crect width='256' height='256' filter='url(%23n)'/%3E%3C/svg%3E");
        background-size: 256px;
      }

      .rev {
        opacity: 0;
        transform: translateY(12px);
        transition:
          opacity 0.5s ease,
          transform 0.5s ease;
      }

      .rev.in {
        opacity: 1;
        transform: none;
      }

      /* ══ HEADER ══ */
      .site-hdr {
        position: sticky;
        top: 0;
        z-index: 200;
        background: rgba(5, 10, 15, 0.93);
        backdrop-filter: blur(14px);
        -webkit-backdrop-filter: blur(14px);
        border-bottom: 1px solid var(--border);
      }

      .hdr-inner {
        max-width: 1060px;
        margin: 0 auto;
        display: flex;
        align-items: center;
        gap: 10px;
        padding: 0 var(--px);
        height: 48px;
      }

      .hdr-brand {
        font-size: 14px;
        font-weight: 800;
        letter-spacing: 0.06em;
        text-transform: uppercase;
        color: var(--gold);
        display: flex;
        align-items: center;
        gap: 7px;
        flex-shrink: 0;
      }

      .dot {
        width: 7px;
        height: 7px;
        border-radius: 50%;
        background: var(--eng);
        box-shadow: 0 0 8px rgba(207, 24, 32, 0.7);
        animation: blink 1.8s ease-in-out infinite;
      }

      @keyframes blink {
        0%,
        100% {
          opacity: 1;
        }

        50% {
          opacity: 0.25;
        }
      }

      .hdr-info {
        font-family: "JetBrains Mono", monospace;
        font-size: 9px;
        letter-spacing: 0.1em;
        text-transform: uppercase;
        color: var(--fg3);
      }

      .hdr-ko {
        font-family: "JetBrains Mono", monospace;
        font-size: 10px;
        letter-spacing: 0.08em;
        color: var(--gold);
        margin-left: auto;
        flex-shrink: 0;
      }

      @media (min-width: 480px) {
        .hdr-inner {
          height: 50px;
          padding: 0 20px;
        }
      }

      @media (min-width: 768px) {
        .hdr-inner {
          height: 54px;
          padding: 0 28px;
        }
      }

      /* ══ HERO ══ */
      .hero {
        padding: 26px var(--px) 30px;
        border-bottom: 1px solid var(--border);
        background: linear-gradient(
          160deg,
          rgba(34, 211, 238, 0.04) 0%,
          transparent 45%,
          rgba(240, 192, 64, 0.03) 100%
        );
      }

      .hero-inner {
        max-width: 1060px;
        margin: 0 auto;
        position: relative;
        z-index: 1;
      }

      .hero-eyebrow {
        font-family: "JetBrains Mono", monospace;
        font-size: 10px;
        letter-spacing: 0.18em;
        text-transform: uppercase;
        color: var(--gold);
        margin-bottom: 18px;
        display: flex;
        align-items: center;
        gap: 10px;
      }

      .hero-eyebrow::before {
        content: "";
        width: 18px;
        height: 1px;
        background: var(--gold);
        flex-shrink: 0;
      }

      /* matchup block */
      .matchup {
        display: grid;
        grid-template-columns: 1fr auto 1fr;
        align-items: center;
        gap: 10px;
        margin-bottom: 0;
      }

      .mu-team {
        display: flex;
        flex-direction: column;
        align-items: center;
        text-align: center;
      }

      .mu-team.away {
        align-items: center;
        text-align: center;
      }

      .mu-badge {
        width: 56px;
        height: 56px;
        margin-bottom: 8px;
      }

      .mu-badge img {
        width: 100%;
        height: 100%;
        object-fit: contain;
        filter: drop-shadow(0 2px 8px rgba(0, 0, 0, 0.6));
      }

      .mu-name {
        font-size: clamp(30px, 8vw, 72px);
        font-weight: 900;
        letter-spacing: -0.03em;
        line-height: 0.88;
        text-transform: uppercase;
      }

      .mu-name.eng {
        color: var(--eng);
      }

      .mu-name.uru {
        color: var(--uru);
      }

      .mu-sub {
        font-family: "JetBrains Mono", monospace;
        font-size: 9px;
        letter-spacing: 0.07em;
        text-transform: uppercase;
        color: var(--fg3);
        margin-top: 5px;
      }

      .form-r {
        display: flex;
        gap: 3px;
        margin-top: 7px;
        justify-content: center;
      }

      .form-r.rv {
        justify-content: center;
      }

      .fb {
        width: 19px;
        height: 19px;
        border-radius: 3px;
        display: flex;
        align-items: center;
        justify-content: center;
        font-family: "JetBrains Mono", monospace;
        font-size: 8px;
        font-weight: 600;
        flex-shrink: 0;
      }

      .fw {
        background: rgba(48, 216, 122, 0.18);
        color: var(--green);
        border: 1px solid rgba(48, 216, 122, 0.35);
      }

      .fd {
        background: rgba(255, 255, 255, 0.06);
        color: rgba(255, 255, 255, 0.28);
        border: 1px solid rgba(255, 255, 255, 0.1);
      }

      .fl {
        background: rgba(255, 92, 92, 0.18);
        color: var(--red);
        border: 1px solid rgba(255, 92, 92, 0.3);
      }

      .mu-mid {
        display: flex;
        flex-direction: column;
        align-items: center;
        gap: 5px;
        flex-shrink: 0;
      }

      .mu-vs {
        font-family: "JetBrains Mono", monospace;
        font-size: 11px;
        letter-spacing: 0.2em;
        text-transform: uppercase;
        color: var(--fg3);
      }

      .mu-pred {
        font-size: clamp(44px, 11vw, 90px);
        font-weight: 900;
        letter-spacing: 0.02em;
        line-height: 1;
        color: var(--gold);
        white-space: nowrap;
        text-shadow: 0 0 32px rgba(245, 197, 24, 0.35);
      }

      .mu-pred-lbl {
        font-family: "JetBrains Mono", monospace;
        font-size: 8px;
        letter-spacing: 0.18em;
        text-transform: uppercase;
        color: rgba(255, 255, 255, 0.18);
        text-align: center;
      }

      @media (min-width: 480px) {
        .hero {
          padding: 36px 20px 0;
        }

        .mu-badge {
          width: 64px;
          height: 64px;
        }

        .matchup {
          gap: 16px;
        }
      }

      @media (min-width: 768px) {
        .hero {
          padding: 44px 28px 0;
        }

        .mu-badge {
          width: 72px;
          height: 72px;
        }

        .matchup {
          gap: 22px;
        }

        /* restore side alignment on desktop */
        .mu-team {
          align-items: flex-start;
          text-align: left;
        }

        .mu-team.away {
          align-items: flex-end;
          text-align: right;
        }

        .form-r {
          justify-content: flex-start;
        }

        .form-r.rv {
          justify-content: flex-end;
        }
      }

      /* strip */
      .hero-strip {
        margin-top: 20px;
        padding: 12px 0;
        border-top: 1px solid var(--border);
        display: flex;
        justify-content: space-between;
        align-items: center;
        flex-wrap: wrap;
        gap: 8px;
      }

      .hs-item {
        display: flex;
        flex-direction: column;
        gap: 1px;
        align-items: center;
      }

      .hs-v {
        font-size: 14px;
        font-weight: 700;
        color: var(--fg);
      }

      .hs-v.eng {
        color: var(--eng);
      }

      .hs-v.uru {
        color: var(--uru);
      }

      .hs-v.gold {
        color: var(--gold);
      }

      .hs-l {
        font-family: "JetBrains Mono", monospace;
        font-size: 8px;
        letter-spacing: 0.1em;
        text-transform: uppercase;
        color: var(--fg3);
      }

      /* prob bar */
      .prob-wrap {
        padding: 12px var(--px);
        border-top: 1px solid var(--border);
        background: rgba(255, 255, 255, 0.01);
      }

      .prob-wrap-inner {
        max-width: 1060px;
        margin: 0 auto;
      }

      .prob-labels {
        display: flex;
        justify-content: space-between;
        margin-bottom: 4px;
      }

      .prob-lbl {
        font-family: "JetBrains Mono", monospace;
        font-size: 8px;
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

      .pb-e {
        background: var(--eng);
      }

      .pb-d {
        background: var(--border2);
      }

      .pb-u {
        background: var(--uru);
      }

      .prob-pcts {
        display: flex;
        justify-content: space-between;
      }

      .pp {
        font-size: 18px;
        font-weight: 800;
        line-height: 1;
      }

      .pp-e {
        color: var(--eng);
      }

      .pp-d {
        color: var(--fg3);
      }

      .pp-u {
        color: var(--uru);
      }

      @media (min-width: 480px) {
        .prob-wrap {
          padding: 13px 20px;
        }

        .pp {
          font-size: 20px;
        }
      }

      @media (min-width: 768px) {
        .prob-wrap {
          padding: 14px 28px;
        }

        .pp {
          font-size: 22px;
        }
      }

      /* context pills */
      .ctx-pills {
        padding: 10px var(--px);
        border-top: 1px solid var(--border);
        background: rgba(245, 197, 24, 0.02);
      }

      .ctx-pills-inner {
        max-width: 1060px;
        margin: 0 auto;
        display: flex;
        gap: 5px;
        flex-wrap: wrap;
      }

      .cpill {
        font-family: "JetBrains Mono", monospace;
        font-size: 8px;
        letter-spacing: 0.07em;
        text-transform: uppercase;
        font-weight: 600;
        padding: 3px 8px;
        border-radius: var(--rxs);
        border: 1px solid;
      }

      .cp-g {
        color: var(--gold);
        border-color: rgba(245, 197, 24, 0.4);
        background: var(--gold-d);
      }

      .cp-e {
        color: var(--eng);
        border-color: rgba(207, 24, 32, 0.4);
        background: var(--eng-d);
      }

      .cp-u {
        color: var(--uru);
        border-color: rgba(91, 180, 228, 0.4);
        background: var(--uru-d);
      }

      .cp-gr {
        color: var(--green);
        border-color: rgba(48, 216, 122, 0.4);
        background: var(--green-d);
      }

      .cp-o {
        color: var(--orange);
        border-color: rgba(255, 140, 66, 0.4);
        background: var(--orange-d);
      }

      @media (min-width: 480px) {
        .ctx-pills {
          padding: 10px 20px;
        }
      }

      @media (min-width: 768px) {
        .ctx-pills {
          padding: 11px 28px;
        }
      }

      /* ══ WRAP ══ */
      .wrap {
        max-width: 1060px;
        margin: 0 auto;
        padding: 20px var(--px) 80px;
        position: relative;
        z-index: 1;
      }

      @media (min-width: 480px) {
        .wrap {
          padding: 26px 20px 88px;
        }
      }

      @media (min-width: 768px) {
        .wrap {
          padding: 32px 28px 96px;
        }
      }

      /* ══ SECTION LABEL ══ */
      .sec {
        display: flex;
        align-items: center;
        gap: 10px;
        margin-bottom: 12px;
        margin-top: 6px;
        font-family: "JetBrains Mono", monospace;
        font-size: 9px;
        letter-spacing: 0.2em;
        text-transform: uppercase;
      }

      .sec::after {
        content: "";
        flex: 1;
        height: 1px;
        background: var(--border);
      }

      .sec-e {
        color: var(--eng);
      }

      .sec-u {
        color: var(--uru);
      }

      .sec-g {
        color: var(--gold);
      }

      /* ══ CARDS ══ */
      .card {
        background: var(--card);
        border: 1px solid var(--border);
        border-radius: var(--r);
        overflow: hidden;
        margin-bottom: 12px;
      }

      .card:hover {
        border-color: var(--border2);
      }

      .card-hd {
        padding: 11px var(--px);
        border-bottom: 1px solid var(--border);
        background: rgba(255, 255, 255, 0.02);
        font-size: 13px;
        font-weight: 700;
        letter-spacing: 0.04em;
        text-transform: uppercase;
        color: var(--fg2);
        display: flex;
        align-items: center;
        gap: 8px;
      }

      .card-hd::before {
        content: "◆";
        font-size: 8px;
        color: var(--gold);
      }

      .card-hd.ce::before {
        color: var(--eng);
      }

      .card-hd.cu::before {
        color: var(--uru);
      }

      .card-bd {
        padding: 14px var(--px);
      }

      @media (min-width: 480px) {
        .card-hd {
          padding: 12px 20px;
        }

        .card-bd {
          padding: 15px 20px;
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

      /* ══ 2-COL ══ */
      .two-col {
        display: grid;
        grid-template-columns: 1fr;
        gap: 12px;
        margin-bottom: 12px;
      }

      @media (min-width: 640px) {
        .two-col {
          grid-template-columns: 1fr 1fr;
        }
      }

      /* ══ LAST 5 ROW ══ */
      .l5r {
        display: flex;
        align-items: center;
        gap: 8px;
        padding: 7px 0;
        border-bottom: 1px solid rgba(255, 255, 255, 0.04);
      }

      .l5r:last-child {
        border-bottom: none;
      }

      .l5-date {
        font-family: "JetBrains Mono", monospace;
        font-size: 9px;
        color: var(--fg3);
        flex-shrink: 0;
        width: 36px;
      }

      .l5-comp {
        font-family: "JetBrains Mono", monospace;
        font-size: 8px;
        color: var(--fg3);
        flex-shrink: 0;
        width: 28px;
      }

      .l5-match {
        font-size: 12px;
        color: var(--fg2);
        flex: 1;
        min-width: 0;
        overflow: hidden;
        text-overflow: ellipsis;
        white-space: nowrap;
      }

      .l5-sc {
        font-size: 14px;
        font-weight: 700;
        letter-spacing: 0.02em;
        color: var(--fg);
        white-space: nowrap;
        margin-left: 4px;
      }

      .l5-res {
        font-family: "JetBrains Mono", monospace;
        font-size: 8px;
        font-weight: 700;
        padding: 2px 6px;
        border-radius: var(--rxs);
        border: 1px solid;
        flex-shrink: 0;
      }

      .lw {
        color: var(--green);
        border-color: rgba(48, 216, 122, 0.35);
        background: var(--green-d);
      }

      .ld {
        color: var(--fg3);
        border-color: var(--border2);
        background: rgba(255, 255, 255, 0.03);
      }

      .ll {
        color: var(--red);
        border-color: rgba(255, 92, 92, 0.35);
        background: var(--red-d);
      }

      /* avg row */
      .avg-row {
        display: flex;
        gap: 5px;
        flex-wrap: wrap;
        margin-top: 11px;
      }

      .avg {
        background: rgba(255, 255, 255, 0.03);
        border: 1px solid var(--border);
        border-radius: var(--rxs);
        padding: 6px 9px;
        display: flex;
        flex-direction: column;
        align-items: center;
      }

      .avg-v {
        font-size: 17px;
        font-weight: 800;
        line-height: 1;
      }

      .avg-v.e {
        color: var(--eng);
      }

      .avg-v.u {
        color: var(--uru);
      }

      .avg-v.g {
        color: var(--gold);
      }

      .avg-l {
        font-family: "JetBrains Mono", monospace;
        font-size: 8px;
        letter-spacing: 0.09em;
        text-transform: uppercase;
        color: var(--fg3);
        margin-top: 2px;
        text-align: center;
      }

      /* ══ H2H ══ */
      .h2h-r {
        display: flex;
        align-items: center;
        gap: 7px;
        padding: 7px 0;
        border-bottom: 1px solid rgba(255, 255, 255, 0.04);
      }

      .h2h-r:last-child {
        border-bottom: none;
      }

      .h2h-date {
        font-family: "JetBrains Mono", monospace;
        font-size: 9px;
        color: var(--fg3);
        flex-shrink: 0;
        width: 40px;
      }

      .h2h-ht {
        font-size: 12px;
        font-weight: 500;
        color: var(--fg2);
        text-align: right;
        flex: 1;
      }

      .h2h-sc {
        font-size: 16px;
        font-weight: 800;
        color: var(--gold);
        white-space: nowrap;
        padding: 0 7px;
        flex-shrink: 0;
      }

      .h2h-at {
        font-size: 12px;
        font-weight: 500;
        color: var(--fg2);
        flex: 1;
      }

      .h2h-comp {
        font-family: "JetBrains Mono", monospace;
        font-size: 8px;
        color: var(--fg3);
        flex-shrink: 0;
      }

      .h2h-tag {
        font-family: "JetBrains Mono", monospace;
        font-size: 8px;
        font-weight: 700;
        padding: 2px 6px;
        border-radius: var(--rxs);
        border: 1px solid;
        white-space: nowrap;
        flex-shrink: 0;
      }

      .ht-e {
        color: var(--eng);
        border-color: rgba(207, 24, 32, 0.35);
        background: var(--eng-d);
      }

      .ht-u {
        color: var(--uru);
        border-color: rgba(91, 180, 228, 0.35);
        background: var(--uru-d);
      }

      .ht-d {
        color: var(--fg3);
        border-color: var(--border2);
        background: rgba(255, 255, 255, 0.03);
      }

      /* ══ TEAM NEWS ══ */
      .tn-grid {
        display: grid;
        grid-template-columns: 1fr;
        gap: 14px;
      }

      @media (min-width: 640px) {
        .tn-grid {
          grid-template-columns: 1fr 1fr;
        }
      }

      .tn-side {
        font-size: 11px;
        font-weight: 700;
        letter-spacing: 0.1em;
        text-transform: uppercase;
        margin-bottom: 7px;
      }

      .tn-e {
        color: var(--eng);
      }

      .tn-u {
        color: var(--uru);
      }

      .tn-xi {
        font-size: 13px;
        line-height: 1.8;
        color: var(--fg2);
      }

      .tn-xi strong {
        color: var(--fg);
        font-weight: 600;
      }

      .tn-out-lbl {
        font-family: "JetBrains Mono", monospace;
        font-size: 8px;
        letter-spacing: 0.1em;
        text-transform: uppercase;
        color: var(--red);
        margin-top: 8px;
        margin-bottom: 3px;
      }

      .tn-out-names {
        font-size: 11px;
        line-height: 1.7;
        color: var(--fg3);
      }

      .tn-alert {
        grid-column: 1/-1;
        background: rgba(245, 197, 24, 0.04);
        border: 1px solid rgba(245, 197, 24, 0.16);
        border-radius: var(--rxs);
        padding: 10px 13px;
        font-size: 12px;
        color: var(--fg2);
        line-height: 1.7;
      }

      .ta-g {
        color: var(--gold);
        font-weight: 600;
      }

      .ta-e {
        color: var(--eng);
        font-weight: 600;
      }

      .ta-u {
        color: var(--uru);
        font-weight: 600;
      }

      .ta-gr {
        color: var(--green);
        font-weight: 600;
      }

      @media (min-width: 768px) {
        .tn-xi {
          font-size: 14px;
        }

        .tn-out-names {
          font-size: 12px;
        }

        .tn-alert {
          font-size: 13px;
        }
      }

      /* ══ STAT PANEL ══ */
      .sp {
        background: var(--card);
        border: 1px solid var(--border);
        border-radius: var(--r);
        overflow: hidden;
        margin-bottom: 12px;
      }

      .sp-hd {
        padding: 13px var(--px);
        border-bottom: 1px solid var(--border);
        background: linear-gradient(
          90deg,
          rgba(207, 24, 32, 0.07) 0%,
          rgba(91, 180, 228, 0.05) 100%
        );
        display: flex;
        align-items: flex-start;
        justify-content: space-between;
        flex-wrap: wrap;
        gap: 8px;
      }

      .sp-title {
        font-size: 14px;
        font-weight: 800;
        letter-spacing: 0.06em;
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
        font-family: "JetBrains Mono", monospace;
        font-size: 9px;
        color: var(--fg3);
        margin-top: 3px;
        letter-spacing: 0.06em;
      }

      .sp-leg {
        display: flex;
        gap: 12px;
        flex-wrap: wrap;
      }

      .sleg {
        display: flex;
        align-items: center;
        gap: 5px;
        font-family: "JetBrains Mono", monospace;
        font-size: 8px;
        letter-spacing: 0.08em;
        text-transform: uppercase;
        color: var(--fg3);
      }

      .sleg-d {
        width: 12px;
        height: 3px;
        border-radius: 2px;
        flex-shrink: 0;
      }

      @media (min-width: 480px) {
        .sp-hd {
          padding: 14px 20px;
        }
      }

      @media (min-width: 768px) {
        .sp-hd {
          padding: 15px 28px;
        }
      }

      /* col headers */
      .sr-hd {
        display: none;
        grid-template-columns: 130px 1fr auto auto auto auto;
        gap: 8px;
        padding: 7px var(--px);
        border-bottom: 2px solid var(--border);
        background: rgba(255, 255, 255, 0.018);
      }

      .srh {
        font-family: "JetBrains Mono", monospace;
        font-size: 8px;
        letter-spacing: 0.12em;
        text-transform: uppercase;
        color: var(--fg3);
      }

      .srh.clo {
        color: var(--uru);
      }

      .srh.cme {
        color: var(--gold);
      }

      .srh.chi {
        color: var(--eng);
      }

      .srh.ccf {
        color: var(--green);
      }

      @media (min-width: 480px) {
        .sr-hd {
          display: grid;
          padding: 7px 20px;
          gap: 10px;
        }
      }

      @media (min-width: 768px) {
        .sr-hd {
          padding: 8px 28px;
          grid-template-columns: 155px 1fr auto auto auto auto;
          gap: 14px;
        }
      }

      /* stat rows — mobile-first card layout */
      .sr {
        display: flex;
        flex-direction: column;
        gap: 6px;
        padding: 14px var(--px);
        border-bottom: 1px solid rgba(255, 255, 255, 0.035);
        transition: background 0.15s;
      }

      .sr:last-child {
        border-bottom: none;
      }

      .sr:hover {
        background: rgba(255, 255, 255, 0.02);
      }

      .sr-top {
        display: flex;
        align-items: center;
        justify-content: space-between;
        gap: 8px;
      }

      .sr-name {
        font-size: 14px;
        font-weight: 600;
        color: var(--fg);
        white-space: nowrap;
      }

      .sr-vals {
        display: flex;
        align-items: center;
        gap: 10px;
      }

      .sr-bars {
        display: flex;
        flex-direction: column;
        gap: 3px;
        flex: 1;
        min-width: 0;
        width: fit-content;
      }

      .sr-track {
        height: 5px;
        background: rgba(255, 255, 255, 0.05);
        border-radius: 3px;
        overflow: hidden;
        position: relative;
      }

      .sr-lo-f {
        position: absolute;
        left: 0;
        top: 0;
        height: 100%;
        border-radius: 3px;
        background: var(--uru);
        opacity: 0.75;
      }

      .sr-hi-f {
        position: absolute;
        left: 0;
        top: 0;
        height: 100%;
        border-radius: 3px;
        background: var(--eng);
        opacity: 0.38;
      }

      .sr-ctx {
        font-family: "JetBrains Mono", monospace;
        font-size: 8px;
        color: var(--fg3);
        overflow: hidden;
        text-overflow: ellipsis;
        white-space: nowrap;
      }

      .sr-lo {
        font-family: "JetBrains Mono", monospace;
        font-size: 14px;
        font-weight: 600;
        color: var(--uru);
        white-space: nowrap;
        text-align: right;
      }

      .sr-me {
        font-size: 22px;
        font-weight: 900;
        color: var(--gold);
        white-space: nowrap;
        text-align: center;
        letter-spacing: -0.01em;
      }

      .sr-hi {
        font-family: "JetBrains Mono", monospace;
        font-size: 14px;
        font-weight: 600;
        color: var(--eng);
        white-space: nowrap;
        text-align: left;
      }

      .sr-cf {
        font-family: "JetBrains Mono", monospace;
        font-size: 8px;
        font-weight: 700;
        padding: 3px 7px;
        border-radius: var(--rxs);
        border: 1px solid;
        white-space: nowrap;
        width: fit-content;
      }

      .cf-hi {
        color: var(--green);
        border-color: rgba(48, 216, 122, 0.35);
        background: var(--green-d);
      }

      .cf-md {
        color: var(--gold);
        border-color: rgba(245, 197, 24, 0.35);
        background: var(--gold-d);
      }

      .cf-lo {
        color: var(--fg3);
        border-color: var(--border2);
        background: rgba(255, 255, 255, 0.02);
      }

      @media (min-width: 480px) {
        .sr {
          display: grid;
          grid-template-columns: 130px 1fr auto auto auto auto;
          align-items: center;
          flex-direction: unset;
          padding: 11px 20px;
          gap: 10px;
        }

        .sr-me {
          font-size: 21px;
        }

        .sr-name {
          font-size: 13px;
          font-weight: 500;
          color: var(--fg2);
        }

        .sr-lo {
          font-size: 13px;
        }

        .sr-hi {
          font-size: 13px;
        }
      }

      @media (min-width: 768px) {
        .sr {
          padding: 12px 28px;
          grid-template-columns: 155px 1fr auto auto auto auto;
          gap: 14px;
        }

        .sr-name {
          font-size: 14px;
        }
      }

      /* ══ CONTEXT ANALYSIS ══ */
      .ctx-note {
        font-size: 13px;
        color: var(--fg2);
        line-height: 1.75;
      }

      .ctx-note strong {
        color: var(--fg);
        font-weight: 600;
      }

      .cn-g {
        color: var(--gold);
        font-weight: 600;
      }

      .cn-e {
        color: var(--eng);
        font-weight: 600;
      }

      .cn-u {
        color: var(--uru);
        font-weight: 600;
      }

      .cn-gr {
        color: var(--green);
        font-weight: 600;
      }

      .cn-o {
        color: var(--orange);
        font-weight: 600;
      }

      @media (min-width: 768px) {
        .ctx-note {
          font-size: 14px;
        }
      }

      /* inline pills */
      .ipills {
        display: flex;
        gap: 6px;
        flex-wrap: wrap;
        margin-top: 12px;
      }

      .ip {
        font-family: "JetBrains Mono", monospace;
        font-size: 9px;
        letter-spacing: 0.07em;
        text-transform: uppercase;
        font-weight: 600;
        padding: 4px 9px;
        border-radius: var(--rxs);
        border: 1px solid;
      }

      .ip-g {
        color: var(--gold);
        border-color: rgba(245, 197, 24, 0.4);
        background: var(--gold-d);
      }

      .ip-e {
        color: var(--eng);
        border-color: rgba(207, 24, 32, 0.4);
        background: var(--eng-d);
      }

      .ip-u {
        color: var(--uru);
        border-color: rgba(91, 180, 228, 0.4);
        background: var(--uru-d);
      }

      .ip-gr {
        color: var(--green);
        border-color: rgba(48, 216, 122, 0.4);
        background: var(--green-d);
      }

      .ip-o {
        color: var(--orange);
        border-color: rgba(255, 140, 66, 0.4);
        background: var(--orange-d);
      }

      .ip-p {
        color: var(--purple);
        border-color: rgba(176, 122, 255, 0.4);
        background: var(--purple-d);
      }

      /* ══ QUICK REF ══ */
      .qr {
        display: flex;
        align-items: center;
        gap: 10px;
        padding: 7px 0;
        border-bottom: 1px solid rgba(255, 255, 255, 0.04);
      }

      .qr:last-child {
        border-bottom: none;
      }

      .qr-lbl {
        font-size: 13px;
        font-weight: 500;
        color: var(--fg2);
        flex: 1;
      }

      .qr-val {
        font-size: 17px;
        font-weight: 800;
        color: var(--gold);
        white-space: nowrap;
        letter-spacing: 0.01em;
      }

      .qr-val.big {
        font-size: 21px;
      }

      @media (min-width: 768px) {
        .qr-lbl {
          font-size: 14px;
        }
      }

      /* ══ FOOTER ══ */
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
        font-size: 18px;
        color: var(--fg3);
        letter-spacing: 0.05em;
        line-height: 2;
      }

      .ft-r {
        font-size: 14px;
        font-weight: 800;
        letter-spacing: 0.05em;
        text-transform: uppercase;
        color: var(--gold);
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

      /* ══ MOBILE OVERRIDES — everything visible & readable ══ */
      @media (max-width: 479px) {
        /* Base font bump */
        html {
          font-size: 20px;
        }

        /* Header */
        .hdr-inner {
          height: auto;
          min-height: 48px;
          padding: 8px var(--px);
          flex-wrap: wrap;
          gap: 6px;
        }
        .hdr-brand {
          font-size: 15px;
        }
        .hdr-info {
          font-size: 11px;
        }
        .hdr-ko {
          font-size: 12px;
        }

        /* Hero eyebrow */
        .hero-eyebrow {
          font-size: 12px;
        }

        /* Matchup team names and subs */
        .matchup {
          gap: 6px;
          overflow: hidden;
        }
        .mu-team {
          min-width: 0;
          overflow: hidden;
        }
        .mu-name {
          font-size: clamp(22px, 7vw, 30px);
          word-break: break-word;
          line-height: 1;
        }
        .mu-badge {
          width: 48px;
          height: 48px;
          margin-bottom: 6px;
        }
        .mu-sub {
          font-size: 11px;
        }
        .mu-vs {
          font-size: 13px;
        }
        .mu-pred {
          font-size: clamp(36px, 10vw, 52px);
        }
        .mu-pred-lbl {
          font-size: 10px;
        }

        /* Form badges */
        .fb {
          width: 24px;
          height: 24px;
          font-size: 11px;
          border-radius: 4px;
        }

        /* Hero strip — stacks nicely */
        .hero-strip {
          display: grid;
          grid-template-columns: repeat(3, 1fr);
          gap: 10px;
          padding: 14px 0;
        }
        .hs-v {
          font-size: 16px;
        }
        .hs-l {
          font-size: 10px;
        }

        /* Probability bar labels & %s */
        .prob-lbl {
          font-size: 10px;
        }
        .pp {
          font-size: 20px;
        }

        /* Context pills */
        .cpill {
          font-size: 10px;
          padding: 5px 10px;
        }

        /* Section labels */
        .sec {
          font-size: 11px;
          margin-bottom: 14px;
        }

        /* Card headers */
        .card-hd {
          font-size: 14px;
          padding: 13px var(--px);
        }
        .card-hd::before {
          font-size: 10px;
        }

        /* Last 5 rows — stack on mobile */
        .l5r {
          flex-wrap: wrap;
          gap: 6px;
          padding: 10px 0;
        }
        .l5-date {
          font-size: 12px;
          width: auto;
        }
        .l5-comp {
          font-size: 10px;
          width: auto;
        }
        .l5-match {
          font-size: 14px;
          white-space: normal;
          flex-basis: 100%;
          order: 3;
        }
        .l5-sc {
          font-size: 16px;
          margin-left: auto;
        }
        .l5-res {
          font-size: 11px;
          padding: 3px 8px;
        }

        /* Avg row */
        .avg-row {
          gap: 8px;
        }
        .avg {
          padding: 8px 12px;
        }
        .avg-v {
          font-size: 18px;
        }
        .avg-l {
          font-size: 10px;
        }

        /* H2H rows — stack for readability */
        .h2h-r {
          flex-wrap: wrap;
          gap: 6px;
          padding: 10px 0;
        }
        .h2h-date {
          font-size: 12px;
          width: auto;
        }
        .h2h-ht {
          font-size: 14px;
          text-align: left;
        }
        .h2h-sc {
          font-size: 18px;
        }
        .h2h-at {
          font-size: 14px;
        }
        .h2h-comp {
          font-size: 10px;
        }
        .h2h-tag {
          font-size: 10px;
          padding: 3px 8px;
        }

        /* Team news */
        .tn-side {
          font-size: 13px;
        }
        .tn-xi {
          font-size: 15px;
        }
        .tn-out-lbl {
          font-size: 10px;
        }
        .tn-out-names {
          font-size: 13px;
        }
        .tn-alert {
          font-size: 14px;
          padding: 12px 14px;
        }

        /* Stat panel header */
        .sp-title {
          font-size: 15px;
        }
        .sp-sub {
          font-size: 11px;
        }
        .sleg {
          font-size: 10px;
        }

        /* Stat rows — card layout on mobile */
        .sr {
          padding: 16px var(--px);
          gap: 8px;
        }
        .sr-name {
          font-size: 16px;
        }
        .sr-lo {
          font-size: 16px;
        }
        .sr-me {
          font-size: 24px;
        }
        .sr-hi {
          font-size: 16px;
        }
        .sr-ctx {
          font-size: 11px;
          white-space: normal;
          overflow: visible;
          text-overflow: unset;
          line-height: 1.5;
        }
        .sr-cf {
          font-size: 10px;
          padding: 4px 8px;
        }

        /* Context analysis text */
        .ctx-note {
          font-size: 15px;
        }

        /* Inline pills */
        .ip {
          font-size: 11px;
          padding: 5px 10px;
        }

        /* Quick ref */
        .qr-lbl {
          font-size: 15px;
        }
        .qr-val {
          font-size: 19px;
        }
        .qr-val.big {
          font-size: 23px;
        }

        /* Footer */
        .ft-l {
          font-size: 10px;
        }
        .ft-r {
          font-size: 15px;
        }
      }
    </style>
  </head>

  <body>
    <header class="site-hdr">
      <div class="hdr-inner">
        <div class="hdr-brand">
          <div class="dot"></div>
          Match Intel
        </div>
        <div class="hdr-info">WC2026 Warm-Up · Wembley</div>
        <div class="hdr-ko">Fri 27 Mar · 19:45 GMT</div>
      </div>
    </header>

    <!-- ══ HERO ══ -->
    <section class="hero rev">
      <div class="hero-inner">
        <div class="hero-eyebrow">
          International Friendly · World Cup 2026 Send-Off Series
        </div>
        <div class="matchup">
          <div class="mu-team">
            <div class="mu-badge">
              <img
                src="https://flagcdn.com/w160/gb-eng.png"
                alt="England"
                loading="lazy"
                style="background-color: #111320"
              />
            </div>
            <div class="mu-name eng">England</div>
            <div class="mu-sub">FIFA 4 · Tuchel · 22G 0GA in qual</div>
            <!-- L5: W(ALB 2-0), W(ENG 5-0 Serbia), W(ENG 3-0 Kosovo), W(ENG 2-0 ALB Wembley), L(SEN 1-3) -->
            <div class="form-r">
              <div class="fb fw">W</div>
              <div class="fb fw">W</div>
              <div class="fb fw">W</div>
              <div class="fb fw">W</div>
              <div class="fb fl">L</div>
            </div>
          </div>
          <div class="mu-mid">
            <div class="mu-vs">vs</div>
            <div class="mu-pred">2–1</div>
            <div class="mu-pred-lbl">Predicted</div>
          </div>
          <div class="mu-team away">
            <div class="mu-badge">
              <img
                src="https://flagcdn.com/w160/uy.png"
                alt="Uruguay"
                loading="lazy"
                style="background-color: #111320"
              />
            </div>
            <div class="mu-name uru">Uruguay</div>
            <div class="mu-sub">FIFA 17 · Bielsa · Copa Am. 3rd 2024</div>
            <!-- L5: L(USA 1-5), W(COL), D(ARG), W(VEN), W(ECU) -->
            <div class="form-r rv">
              <div class="fb fl">L</div>
              <div class="fb fw">W</div>
              <div class="fb fd">D</div>
              <div class="fb fw">W</div>
              <div class="fb fw">W</div>
            </div>
          </div>
        </div>

        <div class="hero-strip">
          <div class="hs-item">
            <div class="hs-v eng">1/2</div>
            <div class="hs-l">England odds</div>
          </div>
          <div class="hs-item">
            <div class="hs-v gold">16/5</div>
            <div class="hs-l">Draw odds</div>
          </div>
          <div class="hs-item">
            <div class="hs-v uru">11/2</div>
            <div class="hs-l">Uruguay odds</div>
          </div>
          <div class="hs-item">
            <div class="hs-v gold">85,000</div>
            <div class="hs-l">Wembley cap.</div>
          </div>
          <div class="hs-item">
            <div class="hs-v eng">27%</div>
            <div class="hs-l">ENG win % vs URU</div>
          </div>
          <div class="hs-item">
            <div class="hs-v">Jablonski</div>
            <div class="hs-l">Referee (GER)</div>
          </div>
        </div>
      </div>

      <div class="prob-wrap">
        <div class="prob-wrap-inner">
          <div class="prob-labels">
            <span class="prob-lbl">England</span
            ><span class="prob-lbl">Draw</span
            ><span class="prob-lbl">Uruguay</span>
          </div>
          <div class="prob-bar">
            <div class="pb-e" style="flex: 52"></div>
            <div class="pb-d" style="flex: 28"></div>
            <div class="pb-u" style="flex: 20"></div>
          </div>
          <div class="prob-pcts">
            <span class="pp pp-e">52%</span><span class="pp pp-d">28%</span
            ><span class="pp pp-u">20%</span>
          </div>
        </div>
      </div>

      <div class="ctx-pills">
        <div class="ctx-pills-inner">
          <span class="cpill cp-g">First meeting since 2014 WC</span>
          <span class="cpill cp-e">ENG 8W 0L in qualifying · 22-0</span>
          <span class="cpill cp-e">11 clean sheets in L12</span>
          <span class="cpill cp-u">URU won 2-1 · 2014 WC (Suárez x2)</span>
          <span class="cpill cp-g">Bellingham returns from injury</span>
          <span class="cpill cp-o">Kane, Saka, Rice RESTED for Japan</span>
          <span class="cpill cp-e">Wembley 85k — sell-out atmosphere</span>
          <span class="cpill cp-u">Valverde + Núñez to start</span>
          <span class="cpill cp-g">Players proving WC squad spots</span>
        </div>
      </div>
    </section>

    <div class="wrap">
      <!-- ══ LAST 5 ══ -->
      <div class="sec rev">
        <span class="sec-e">England</span>&nbsp;·&nbsp;<span class="sec-u"
          >Uruguay</span
        >&nbsp;— Last 5 Matches Each
      </div>
      <div class="two-col">
        <!-- ENGLAND L5 -->
        <div class="card rev">
          <div class="card-hd ce">England — Last 5 (All Comps)</div>
          <div class="card-bd">
            <div class="l5r">
              <span class="l5-date">Nov 25</span><span class="l5-comp">WCQ</span
              ><span class="l5-match">Albania 0-2 England (Tirana)</span
              ><span class="l5-sc">0–2</span><span class="l5-res lw">W</span>
            </div>
            <div class="l5r">
              <span class="l5-date">Sep 25</span><span class="l5-comp">WCQ</span
              ><span class="l5-match">England 5-0 Serbia (Wembley)</span
              ><span class="l5-sc">5–0</span><span class="l5-res lw">W</span>
            </div>
            <div class="l5r">
              <span class="l5-date">Jun 25</span><span class="l5-comp">FRI</span
              ><span class="l5-match">Senegal 3-1 England (Nottm Forest)</span
              ><span class="l5-sc">1–3</span><span class="l5-res ll">L</span>
            </div>
            <div class="l5r">
              <span class="l5-date">Nov 24</span><span class="l5-comp">WCQ</span
              ><span class="l5-match">England 5-0 Montenegro</span
              ><span class="l5-sc">5–0</span><span class="l5-res lw">W</span>
            </div>
            <div class="l5r">
              <span class="l5-date">Oct 24</span><span class="l5-comp">WCQ</span
              ><span class="l5-match">England 3-0 Kosovo (Wembley)</span
              ><span class="l5-sc">3–0</span><span class="l5-res lw">W</span>
            </div>
            <div class="avg-row">
              <div class="avg">
                <div class="avg-v e">8W 0L</div>
                <div class="avg-l">Qual record</div>
              </div>
              <div class="avg">
                <div class="avg-v e">22–0</div>
                <div class="avg-l">Qual GF–GA</div>
              </div>
              <div class="avg">
                <div class="avg-v e">11/12</div>
                <div class="avg-l">Clean sheets</div>
              </div>
              <div class="avg">
                <div class="avg-v g">~7–8</div>
                <div class="avg-l">Corners/g</div>
              </div>
              <div class="avg">
                <div class="avg-v g">~18</div>
                <div class="avg-l">Shots/g avg</div>
              </div>
            </div>
          </div>
        </div>

        <!-- URUGUAY L5 -->
        <div class="card rev">
          <div class="card-hd cu">Uruguay — Last 5 (All Comps)</div>
          <div class="card-bd">
            <div class="l5r">
              <span class="l5-date">Nov 25</span><span class="l5-comp">FRI</span
              ><span class="l5-match">USA 5-1 Uruguay (shock loss)</span
              ><span class="l5-sc">1–5</span><span class="l5-res ll">L</span>
            </div>
            <div class="l5r">
              <span class="l5-date">Oct 25</span><span class="l5-comp">WCQ</span
              ><span class="l5-match">Uruguay 3-0 Venezuela</span
              ><span class="l5-sc">3–0</span><span class="l5-res lw">W</span>
            </div>
            <div class="l5r">
              <span class="l5-date">Oct 25</span><span class="l5-comp">WCQ</span
              ><span class="l5-match">Ecuador 1-1 Uruguay</span
              ><span class="l5-sc">1–1</span><span class="l5-res ld">D</span>
            </div>
            <div class="l5r">
              <span class="l5-date">Sep 25</span><span class="l5-comp">WCQ</span
              ><span class="l5-match">Uruguay 2-1 Colombia</span
              ><span class="l5-sc">2–1</span><span class="l5-res lw">W</span>
            </div>
            <div class="l5r">
              <span class="l5-date">Sep 25</span><span class="l5-comp">WCQ</span
              ><span class="l5-match">Argentina 1-1 Uruguay</span
              ><span class="l5-sc">1–1</span><span class="l5-res ld">D</span>
            </div>
            <div class="avg-row">
              <div class="avg">
                <div class="avg-v u">28pts</div>
                <div class="avg-l">WCQ total</div>
              </div>
              <div class="avg">
                <div class="avg-v u">7W 7D 4L</div>
                <div class="avg-l">Qual record</div>
              </div>
              <div class="avg">
                <div class="avg-v u">4th</div>
                <div class="avg-l">CONMEBOL pos</div>
              </div>
              <div class="avg">
                <div class="avg-v g">Núñez</div>
                <div class="avg-l">5g qual top scorer</div>
              </div>
              <div class="avg">
                <div class="avg-v g">Copa Am</div>
                <div class="avg-l">3rd place 2024</div>
              </div>
            </div>
          </div>
        </div>
      </div>

      <!-- ══ H2H ══ -->
      <div class="sec rev"><span class="sec-g">Last 5 Head to Head</span></div>
      <div class="card rev">
        <div class="card-hd">England vs Uruguay — H2H History</div>
        <div class="card-bd">
          <div class="h2h-r">
            <span class="h2h-date">Jun 14</span>
            <span class="h2h-ht">Uruguay</span>
            <span class="h2h-sc">2–1</span>
            <span class="h2h-at">England</span>
            <span class="h2h-comp">WC GS</span>
            <span class="h2h-tag ht-u">URU Win</span>
          </div>
          <div class="h2h-r">
            <span class="h2h-date">Mar 06</span>
            <span class="h2h-ht">England</span>
            <span class="h2h-sc">2–1</span>
            <span class="h2h-at">Uruguay</span>
            <span class="h2h-comp">FRI</span>
            <span class="h2h-tag ht-e">ENG Win</span>
          </div>
          <div class="h2h-r">
            <span class="h2h-date">Mar 95</span>
            <span class="h2h-ht">England</span>
            <span class="h2h-sc">0–0</span>
            <span class="h2h-at">Uruguay</span>
            <span class="h2h-comp">FRI Wem</span>
            <span class="h2h-tag ht-d">Draw</span>
          </div>
          <div class="h2h-r">
            <span class="h2h-date">May 90</span>
            <span class="h2h-ht">Uruguay</span>
            <span class="h2h-sc">2–1</span>
            <span class="h2h-at">England</span>
            <span class="h2h-comp">FRI</span>
            <span class="h2h-tag ht-u">URU Win</span>
          </div>
          <div class="h2h-r">
            <span class="h2h-date">Jun 66</span>
            <span class="h2h-ht">England</span>
            <span class="h2h-sc">0–0</span>
            <span class="h2h-at">Uruguay</span>
            <span class="h2h-comp">WC GS Wem</span>
            <span class="h2h-tag ht-d">Draw</span>
          </div>
          <div class="avg-row" style="margin-top: 12px">
            <div class="avg">
              <div class="avg-v e">27%</div>
              <div class="avg-l">ENG win ratio vs URU</div>
            </div>
            <div class="avg">
              <div class="avg-v u">P11 W3 D4 L4</div>
              <div class="avg-l">England overall H2H</div>
            </div>
            <div class="avg">
              <div class="avg-v g">2× 0-0</div>
              <div class="avg-l">Goalless at Wembley</div>
            </div>
            <div class="avg">
              <div class="avg-v u">12 years</div>
              <div class="avg-l">Since last meeting</div>
            </div>
          </div>
          <p
            class="ctx-note"
            style="
              margin-top: 14px;
              padding-top: 12px;
              border-top: 1px solid var(--border);
            "
          >
            <strong
              >England's record against Uruguay is historically poor</strong
            >
            — only 27% win rate, lower only against Brazil (15%) and Romania
            (25%) among nations they've met 10+ times.
            <span class="cn-u"
              >Two of the four previous games at Wembley ended 0-0</span
            >, including the 1966 World Cup opener and the 1995 friendly.
            <span class="cn-e"
              >England are also winless in their last five games against South
              American nations</span
            >
            (W0 D3 L2) since beating Peru in 2014. The last meeting was the 2014
            World Cup, when
            <span class="cn-u">Luis Suárez scored twice</span> to knock England
            out. This is the first Wembley meeting since 1995 — 31 years between
            home encounters.
          </p>
        </div>
      </div>

      <!-- ══ TEAM NEWS ══ -->
      <div class="sec rev">
        <span class="sec-g">Team News &amp; Confirmed XIs</span>
      </div>
      <div class="card rev">
        <div class="card-hd">Confirmed Team News · Wembley Friendly</div>
        <div class="card-bd">
          <div class="tn-grid">
            <div>
              <div class="tn-side tn-e">England</div>
              <div class="tn-xi">
                <strong>Pickford</strong> (c) or Trafford<br />
                Livramento · <strong>Maguire</strong> · Guehi/Burn ·
                Lewis-Skelly<br />
                <strong>Bellingham</strong> · Wharton · Jones<br />
                Bowen · Solanke/Gordon · Rashford
              </div>
              <div class="tn-out-lbl">
                Rested for Japan (not available tonight)
              </div>
              <div class="tn-out-names">
                <span style="color: var(--orange)"
                  >Kane · Saka · Rice · Henderson (D) · Burn · Guehi · Konsa ·
                  O'Reilly · Anderson · Rogers · Gordon (some group)</span
                >
              </div>
              <div class="tn-out-lbl">Injured / unavailable</div>
              <div class="tn-out-names">
                <span style="color: var(--red)"
                  >Eze (calf — ruled out) · Maddison · Grealish ·
                  Alexander-Arnold · O.Watkins</span
                >
              </div>
            </div>
            <div>
              <div class="tn-side tn-u">Uruguay</div>
              <div class="tn-xi">
                <strong>Rochet</strong><br />
                Nández/Giménez · <strong>R.Araújo</strong> · Olivera<br />
                <strong>Ugarte</strong> · <strong>Valverde</strong> ·
                Bentancur/Ugarte<br />
                Pellistri · De Arrascaeta · M.Araújo<br />
                <strong>Darwin Núñez</strong>
              </div>
              <div class="tn-out-lbl">Injured / suspended</div>
              <div class="tn-out-names">
                <span style="color: var(--red)"
                  >Bentancur (injured) · Nández (injured) · Vecino (injured) ·
                  M.Araújo (injured) · Barbas</span
                >
              </div>
            </div>
            <div class="tn-alert">
              <span class="ta-g">KEY INTEL:</span>
              <span class="ta-e"
                >Tuchel has split his 35-man squad across two games</span
              >
              — the "strong" group faces Uruguay, the second group faces Japan.
              <span class="ta-g">Bellingham RETURNS</span> from a muscle injury
              picked up at Real Madrid — his first England appearance in months.
              <span class="ta-g">Maguire RECALLED</span> — this is his chance to
              push for a WC squad spot ahead of Burn, Guehi and Konsa.
              <span class="ta-u"
                >Ugarte (Manchester United) anchors Uruguay's midfield</span
              >
              — Racing Post note he picked up two suspensions in WCQ.
              <span class="ta-g">Valverde is the player to watch</span> — Bielsa
              may rotate him given Uruguay also play Algeria in this window.
              <span class="ta-e"
                >England's 22-0 qualifying record is extraordinary</span
              >
              — tonight is a genuine test of quality above what they faced in
              Group K.
              <span class="ta-u"
                >Núñez: 5 goals in qualifying, starts at Wembley — returns to
                English soil.</span
              >
            </div>
          </div>
        </div>
      </div>

      <!-- ══ SEASON AVERAGES ══ -->
      <div class="sec rev">
        <span class="sec-g">Season Average Statistics Comparison</span>
      </div>
      <div class="two-col">
        <div class="card rev">
          <div class="card-hd ce">England 2025-26 International Averages</div>
          <div class="card-bd">
            <div class="qr">
              <span class="qr-lbl">Goals scored / game</span
              ><span class="qr-val" style="color: var(--eng)">2.75</span>
            </div>
            <div class="qr">
              <span class="qr-lbl">Goals conceded / game</span
              ><span class="qr-val" style="color: var(--green)">0.0</span>
            </div>
            <div class="qr">
              <span class="qr-lbl">Possession average</span
              ><span class="qr-val" style="color: var(--eng)">~58%</span>
            </div>
            <div class="qr">
              <span class="qr-lbl">Corners / game (est.)</span
              ><span class="qr-val" style="color: var(--eng)">7.5</span>
            </div>
            <div class="qr">
              <span class="qr-lbl">Shots on target / game (est.)</span
              ><span class="qr-val" style="color: var(--eng)">7.2</span>
            </div>
            <div class="qr">
              <span class="qr-lbl">Clean sheets in qualifying</span
              ><span class="qr-val" style="color: var(--green)">8/8</span>
            </div>
            <div class="qr">
              <span class="qr-lbl">Win % under Tuchel</span
              ><span class="qr-val" style="color: var(--eng)">~72%</span>
            </div>
          </div>
        </div>
        <div class="card rev">
          <div class="card-hd cu">Uruguay 2025-26 International Averages</div>
          <div class="card-bd">
            <div class="qr">
              <span class="qr-lbl">Goals scored / game (WCQ)</span
              ><span class="qr-val" style="color: var(--uru)">1.67</span>
            </div>
            <div class="qr">
              <span class="qr-lbl">Goals conceded / game</span
              ><span class="qr-val" style="color: var(--uru)">1.06</span>
            </div>
            <div class="qr">
              <span class="qr-lbl">Possession average</span
              ><span class="qr-val" style="color: var(--uru)">~48%</span>
            </div>
            <div class="qr">
              <span class="qr-lbl">CONMEBOL finishing position</span
              ><span class="qr-val" style="color: var(--uru)">4th</span>
            </div>
            <div class="qr">
              <span class="qr-lbl">Núñez goals in qualifying</span
              ><span class="qr-val" style="color: var(--uru)">5</span>
            </div>
            <div class="qr">
              <span class="qr-lbl">Copa América 2024</span
              ><span class="qr-val" style="color: var(--uru)">3rd</span>
            </div>
            <div class="qr">
              <span class="qr-lbl">Bielsa win % vs ENG</span
              ><span class="qr-val" style="color: var(--uru)"
                >0% (D 2000, L 2002)</span
              >
            </div>
          </div>
        </div>
      </div>

      <!-- ══ STAT PREDICTIONS ══ -->
      <div class="sec rev">
        <span class="sec-g">Stat Predictions · All Categories</span>
      </div>
      <div class="sp rev">
        <div class="sp-hd">
          <div>
            <div class="sp-title">England vs Uruguay — Stat Ranges</div>
            <div class="sp-sub">
              Wembley · 27 Mar · Friendly context · WC squad audition factor ·
              H2H · Qualifying averages applied
            </div>
          </div>
          <div class="sp-leg">
            <div class="sleg">
              <div class="sleg-d" style="background: var(--uru)"></div>
              Lowest
            </div>
            <div class="sleg">
              <div class="sleg-d" style="background: var(--gold)"></div>
              Median
            </div>
            <div class="sleg">
              <div class="sleg-d" style="background: var(--eng)"></div>
              Highest
            </div>
          </div>
        </div>

        <div class="sr-hd">
          <span class="srh">Stat</span>
          <span class="srh">Basis</span>
          <span class="srh clo">Low</span>
          <span class="srh cme">Med</span>
          <span class="srh chi">High</span>
          <span class="srh ccf">Conf.</span>
        </div>

        <!-- CORNERS -->
        <div class="sr">
          <span class="sr-name">Corners</span>
          <div class="sr-bars">
            <div class="sr-track">
              <div class="sr-lo-f" style="width: 42%"></div>
              <div class="sr-hi-f" style="width: 76%"></div>
            </div>
            <span class="sr-ctx"
              >ENG ~7.5/g in qual · URU defend compactly under Bielsa · Wembley
              wide pitch amplifies · two 0-0 H2H at Wembley = historically few
              corners</span
            >
          </div>
          <span class="sr-lo">6</span><span class="sr-me">10</span
          ><span class="sr-hi">15</span>
          <span class="sr-cf cf-hi">Hi</span>
        </div>

        <!-- SHOTS ON TARGET -->
        <div class="sr">
          <span class="sr-name">Shots on Target</span>
          <div class="sr-bars">
            <div class="sr-track">
              <div class="sr-lo-f" style="width: 38%"></div>
              <div class="sr-hi-f" style="width: 70%"></div>
            </div>
            <span class="sr-ctx"
              >ENG 7.2 SoT/g estimated · Uruguay Rochet solid GK · warm-up =
              experimental combinations → less clinical · Bellingham + Núñez
              both quality</span
            >
          </div>
          <span class="sr-lo">4</span><span class="sr-me">8</span
          ><span class="sr-hi">13</span>
          <span class="sr-cf cf-hi">Hi</span>
        </div>

        <!-- TOTAL SHOTS -->
        <div class="sr">
          <span class="sr-name">Total Shots</span>
          <div class="sr-bars">
            <div class="sr-track">
              <div class="sr-lo-f" style="width: 48%"></div>
              <div class="sr-hi-f" style="width: 74%"></div>
            </div>
            <span class="sr-ctx"
              >ENG avg ~18/g in qual · URU ~12/g in CONMEBOL · Wembley crowd
              drives England attack · proving-yourself factor = high shot
              count</span
            >
          </div>
          <span class="sr-lo">18</span><span class="sr-me">26</span
          ><span class="sr-hi">34</span>
          <span class="sr-cf cf-hi">Hi</span>
        </div>

        <!-- FOULS -->
        <div class="sr">
          <span class="sr-name">Fouls</span>
          <div class="sr-bars">
            <div class="sr-track">
              <div class="sr-lo-f" style="width: 40%"></div>
              <div class="sr-hi-f" style="width: 64%"></div>
            </div>
            <span class="sr-ctx"
              >Friendly = typically fewer cynical fouls · BUT Ugarte suspended
              twice in WCQ = foul-happy · Bielsa presses hard = fouls in
              midfield · WC audition raises intensity</span
            >
          </div>
          <span class="sr-lo">14</span><span class="sr-me">20</span
          ><span class="sr-hi">28</span>
          <span class="sr-cf cf-md">Med</span>
        </div>

        <!-- FREE KICKS -->
        <div class="sr">
          <span class="sr-name">Free Kicks</span>
          <div class="sr-bars">
            <div class="sr-track">
              <div class="sr-lo-f" style="width: 40%"></div>
              <div class="sr-hi-f" style="width: 64%"></div>
            </div>
            <span class="sr-ctx"
              >Mirrors fouls · ENG earn FKs from Bellingham + Bowen runs · URU
              give FKs to disrupt England's flow under Bielsa press</span
            >
          </div>
          <span class="sr-lo">14</span><span class="sr-me">20</span
          ><span class="sr-hi">28</span>
          <span class="sr-cf cf-md">Med</span>
        </div>

        <!-- THROW-INS -->
        <div class="sr">
          <span class="sr-name">Throw-ins</span>
          <div class="sr-bars">
            <div class="sr-track">
              <div class="sr-lo-f" style="width: 44%"></div>
              <div class="sr-hi-f" style="width: 64%"></div>
            </div>
            <span class="sr-ctx"
              >Wembley wide pitch → above-average throw-ins · England wide play
              via Rashford + Bowen generates sideline duels · PL avg ~33/g for
              reference</span
            >
          </div>
          <span class="sr-lo">28</span><span class="sr-me">36</span
          ><span class="sr-hi">46</span>
          <span class="sr-cf cf-md">Med</span>
        </div>

        <!-- GOAL KICKS -->
        <div class="sr">
          <span class="sr-name">Goal Kicks</span>
          <div class="sr-bars">
            <div class="sr-track">
              <div class="sr-lo-f" style="width: 30%"></div>
              <div class="sr-hi-f" style="width: 54%"></div>
            </div>
            <span class="sr-ctx"
              >Pickford plays short (low GKs for ENG) · Rochet comfortable
              playing out · URU CONMEBOL style = more long balls → moderate GKs
              · low overall expected</span
            >
          </div>
          <span class="sr-lo">8</span><span class="sr-me">14</span
          ><span class="sr-hi">20</span>
          <span class="sr-cf cf-lo">Low</span>
        </div>

        <!-- TACKLES -->
        <div class="sr">
          <span class="sr-name">Tackles</span>
          <div class="sr-bars">
            <div class="sr-track">
              <div class="sr-lo-f" style="width: 46%"></div>
              <div class="sr-hi-f" style="width: 72%"></div>
            </div>
            <span class="sr-ctx"
              >WC squad audition = maximum effort on every 50/50 · Bellingham vs
              Valverde = elite midfield battle · Bielsa teams press aggressively
              = tackles · fringe players proving themselves</span
            >
          </div>
          <span class="sr-lo">22</span><span class="sr-me">30</span
          ><span class="sr-hi">42</span>
          <span class="sr-cf cf-hi">Hi</span>
        </div>

        <!-- OFFSIDES -->
        <div class="sr">
          <span class="sr-name">Offsides</span>
          <div class="sr-bars">
            <div class="sr-track">
              <div class="sr-lo-f" style="width: 28%"></div>
              <div class="sr-hi-f" style="width: 56%"></div>
            </div>
            <span class="sr-ctx"
              >Friendly = less coordinated defensive line → more offside calls ·
              ENG forwards (Bowen, Rashford, Solanke) push high · Núñez +
              Pellistri aggressive runners · both teams attack = moderate
              offsides</span
            >
          </div>
          <span class="sr-lo">2</span><span class="sr-me">5</span
          ><span class="sr-hi">9</span>
          <span class="sr-cf cf-lo">Low</span>
        </div>
      </div>

      <!-- ══ FULL ANALYSIS ══ -->
      <div class="sec rev"><span class="sec-g">Full Match Analysis</span></div>
      <div class="card rev">
        <div class="card-hd">
          Context, Key Battles &amp; Prediction Rationale
        </div>
        <div class="card-bd">
          <p class="ctx-note">
            <strong
              >A fixture with two very different narratives colliding.</strong
            >
            On paper, this is a warm-up. In practice, with the 2026 World Cup
            less than 3 months away, every player on the pitch tonight knows a
            strong performance could define whether they make Tuchel's 23-man
            squad.
            <span class="cn-g"
              >Tuchel himself described this as his final opportunity to
              finalise squad thoughts before May's selection deadline.</span
            >
            The atmosphere at a sell-out Wembley (85,000) will feel nothing like
            a friendly — the crowd expects an England performance that
            demonstrates genuine World Cup readiness.
          </p>
          <br />
          <p class="ctx-note">
            <strong>The selection intrigue shapes the stats.</strong> With Kane,
            Saka, Rice and several first-choice starters rested for the Japan
            game on March 31, tonight is an opportunity for the likes of
            <span class="cn-e"
              >Maguire (on his recall), Bowen, Solanke, Rashford and
              Bellingham</span
            >
            — who returns from injury — to make decisive statements. Players
            wanting to prove themselves means higher work-rate, more tackles,
            more pressing and more attacking ambition than a typical
            pre-tournament friendly would produce. The proving-yourself factor
            is the single biggest stat modifier in this report:
            <span class="cn-g"
              >tackles are pushed to their highest range (22–42)</span
            >, shots are elevated above normal friendly averages, and corners
            will be driven by England's attacking intent from wide areas.
          </p>
          <br />
          <p class="ctx-note">
            <strong>Uruguay under Bielsa: organised chaos.</strong>
            <span class="cn-u"
              >Bielsa's teams press relentlessly, run hard from minute 1 to 90,
              and create a high-tempo, physically exhausting environment.</span
            >
            Three midfielders — Ugarte, Valverde and De Arrascaeta — will press
            England's ball-carriers constantly. Valverde, potentially managed
            for minutes, is the highest-quality player on the pitch when fit.
            <span class="cn-u"
              >Darwin Núñez returns to England — where he spent three years at
              Liverpool</span
            >
            — and will be desperate to score against his former home country.
            Bielsa has never beaten England (D 2000 Wembley, L 2002 WC as
            Argentina manager) and will know his tactical homework faces a real
            test tonight.
          </p>
          <br />
          <p class="ctx-note">
            <strong>Why goals are expected.</strong>
            <span class="cn-e"
              >England conceded 0 goals in all 8 qualifying games</span
            >, but those came against Group K minnows (Albania, Kosovo, Serbia
            etc.). Uruguay's attacking trio — Núñez, De Arrascaeta, Pellistri —
            are a significant step up in quality. Meanwhile
            <span class="cn-u"
              >Uruguay lost 5-1 to the USA in their last friendly</span
            >
            — suggesting a defensive vulnerability on the road against quality
            opposition. England's blend of Bellingham's creativity, Rashford's
            pace and Bowen's wide quality should produce goals.
            <strong>Prediction: England 2-1 Uruguay</strong> — a quality
            contest, goals in both halves, Bellingham influential, Núñez causing
            problems throughout.
          </p>
          <div class="ipills">
            <span class="ip ip-e">ENG win — 52%</span>
            <span class="ip ip-g">BTTS YES — likely</span>
            <span class="ip ip-g">O2.5 goals possible</span>
            <span class="ip ip-e">Bellingham anytime scorer</span>
            <span class="ip ip-u">Núñez anytime scorer</span>
            <span class="ip ip-g">Tackles highest stat of the night</span>
            <span class="ip ip-g">O9.5 corners — YES</span>
            <span class="ip ip-e">ENG winless vs South America L5</span>
            <span class="ip ip-u">Valverde: manage mins expected</span>
            <span class="ip ip-o">Offsides = low confidence stat</span>
          </div>
        </div>
      </div>

      <!-- ══ QUICK REF ══ -->
      <div class="sec rev">
        <span class="sec-g">Quick Reference Summary</span>
      </div>
      <div class="card rev" style="margin-bottom: 0">
        <div class="card-hd">All Predictions at a Glance</div>
        <div class="card-bd">
          <div class="qr">
            <span class="qr-lbl">Predicted Score</span
            ><span class="qr-val big">England 2–1 Uruguay</span>
          </div>
          <div class="qr">
            <span class="qr-lbl">Total Shots (low / med / high)</span
            ><span class="qr-val">18 · 26 · 34</span>
          </div>
          <div class="qr">
            <span class="qr-lbl">Shots on Target (low / med / high)</span
            ><span class="qr-val">4 · 8 · 13</span>
          </div>
          <div class="qr">
            <span class="qr-lbl">Corners (low / med / high)</span
            ><span class="qr-val">6 · 10 · 15</span>
          </div>
          <div class="qr">
            <span class="qr-lbl">Fouls (low / med / high)</span
            ><span class="qr-val">14 · 20 · 28</span>
          </div>
          <div class="qr">
            <span class="qr-lbl">Free Kicks (low / med / high)</span
            ><span class="qr-val">14 · 20 · 28</span>
          </div>
          <div class="qr">
            <span class="qr-lbl">Throw-ins (low / med / high)</span
            ><span class="qr-val">28 · 36 · 46</span>
          </div>
          <div class="qr">
            <span class="qr-lbl">Goal Kicks (low / med / high)</span
            ><span class="qr-val">8 · 14 · 20</span>
          </div>
          <div class="qr">
            <span class="qr-lbl">Tackles (low / med / high)</span
            ><span class="qr-val">22 · 30 · 42</span>
          </div>
          <div class="qr">
            <span class="qr-lbl">Offsides (low / med / high)</span
            ><span class="qr-val">2 · 5 · 9</span>
          </div>
          <div class="qr">
            <span class="qr-lbl">BTTS probability</span
            ><span class="qr-val">~60%</span>
          </div>
          <div class="qr">
            <span class="qr-lbl">Over 2.5 goals</span
            ><span class="qr-val">~40%</span>
          </div>
          <div class="qr">
            <span class="qr-lbl">Yellow cards (combined)</span
            ><span class="qr-val">2 – 5</span>
          </div>
          <div class="qr">
            <span class="qr-lbl">England win probability</span
            ><span class="qr-val">52%</span>
          </div>
          <div class="qr">
            <span class="qr-lbl">Key battle</span
            ><span class="qr-val">Bellingham vs Valverde</span>
          </div>
          <div class="qr">
            <span class="qr-lbl">Highest stat of the night</span
            ><span class="qr-val">Tackles (30 med)</span>
          </div>
          <div class="qr">
            <span class="qr-lbl">Referee</span
            ><span class="qr-val">Sven Jablonski (GER)</span>
          </div>
        </div>
      </div>
    </div>
    <!-- /wrap -->

    <footer>
      <div class="ft-l">
        <strong>Team Bilbo Statistical Analysis</strong>
    </div>
      <div class="ft-r">Wembley · 19:45 GMT ⚽</div>
    </footer>

    <script>
      (function () {
        const els = document.querySelectorAll(".rev");
        const ob = new IntersectionObserver(
          (entries) => {
            entries.forEach((e) => {
              if (e.isIntersecting) {
                e.target.classList.add("in");
                ob.unobserve(e.target);
              }
            });
          },
          { threshold: 0.05, rootMargin: "0px 0px -12px 0px" },
        );
        els.forEach((el) => ob.observe(el));
      })();
    </script>
  </body>
</html>
