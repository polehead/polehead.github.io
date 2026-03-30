<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width,initial-scale=1.0" />
    <title>WC2026 Predictions</title>
    <link
      href="https://fonts.googleapis.com/css2?family=Inter:wght@300;400;500;600;700;800;900&family=JetBrains+Mono:wght@400;500;600&display=swap"
      rel="stylesheet"
    />
    <style>
      /* ══ TOKENS ══ */
      :root {
        --bg: #07080d;
        --bg2: #0c0e17;
        --card: #111320;
        --card2: #161929;
        --border: #1c2035;
        --border2: #262c44;
        --fg: #eef0f8;
        --fg2: #7c84a8;
        --fg3: #5e6069;
        --gold: #f0c040;
        --gold-d: rgba(240, 192, 64, 0.12);
        --cyan: #22d3ee;
        --cyan-d: rgba(34, 211, 238, 0.11);
        --green: #4ade80;
        --green-d: rgba(74, 222, 128, 0.11);
        --red: #f87171;
        --red-d: rgba(248, 113, 113, 0.11);
        --orange: #fb923c;
        --orange-d: rgba(251, 146, 60, 0.11);
        --purple: #a78bfa;
        --purple-d: rgba(167, 139, 250, 0.11);
        --pink: #f472b6;
        --pink-d: rgba(244, 114, 182, 0.11);
        --r: 10px;
        --rsm: 6px;
        --rxs: 4px;
        --px: 14px;
      }

      *,
      *::before,
      *::after {
        box-sizing: border-box;
        margin: 0;
        padding: 0;
      }

      html {
        font-size: 14px;
        scroll-behavior: smooth;
        -webkit-text-size-adjust: 100%;
      }

      body {
        background: var(--bg);
        color: var(--fg);
        font-family: "Inter", sans-serif;
        line-height: 1.5;
        min-height: 100vh;
        overflow-x: hidden;
        background-image:
          radial-gradient(
            ellipse 80% 50% at 20% 0%,
            rgba(34, 211, 238, 0.04) 0%,
            transparent 55%
          ),
          radial-gradient(
            ellipse 80% 50% at 80% 100%,
            rgba(240, 192, 64, 0.03) 0%,
            transparent 55%
          );
      }

      .rev {
        opacity: 0;
        transform: translateY(12px);
        transition:
          opacity 0.45s ease,
          transform 0.45s ease;
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
        background: rgba(7, 8, 13, 0.93);
        backdrop-filter: blur(14px);
        border-bottom: 1px solid var(--border);
      }

      .hdr-inner {
        max-width: 1080px;
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
        background: var(--gold);
        box-shadow: 0 0 7px rgba(240, 192, 64, 0.6);
        animation: blink 1.8s ease-in-out infinite;
      }

      @keyframes blink {
        0%,
        100% {
          opacity: 1;
        }

        50% {
          opacity: 0.2;
        }
      }

      .hdr-info {
        font-family: "JetBrains Mono", monospace;
        font-size: 11px;
        letter-spacing: 0.1em;
        text-transform: uppercase;
        color: var(--fg3);
      }

      .hdr-count {
        font-family: "JetBrains Mono", monospace;
        font-size: 11px;
        letter-spacing: 0.08em;
        color: var(--cyan);
        margin-left: auto;
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
        max-width: 1080px;
        margin: 0 auto;
      }

      .hero-eye {
        font-family: "JetBrains Mono", monospace;
        font-size: 11px;
        letter-spacing: 0.18em;
        text-transform: uppercase;
        color: var(--cyan);
        margin-bottom: 10px;
        display: flex;
        align-items: center;
        gap: 10px;
      }

      .hero-eye::before {
        content: "";
        width: 18px;
        height: 1px;
        background: var(--cyan);
        flex-shrink: 0;
      }

      .hero-h1 {
        font-size: clamp(34px, 8.5vw, 80px);
        font-weight: 900;
        line-height: 0.9;
        letter-spacing: -0.03em;
        margin-bottom: 8px;
      }

      .hero-h1 span {
        color: var(--gold);
      }

      .hero-sub {
        font-family: "JetBrains Mono", monospace;
        font-size: 11px;
        letter-spacing: 0.14em;
        text-transform: uppercase;
        color: var(--fg3);
        margin-bottom: 18px;
      }

      .fixture-grid {
        display: grid;
        grid-template-columns: repeat(2, 1fr);
        gap: 6px;
        margin-bottom: 16px;
      }

      @media (min-width: 480px) {
        .fixture-grid {
          grid-template-columns: repeat(3, 1fr);
        }
      }

      @media (min-width: 640px) {
        .fixture-grid {
          grid-template-columns: repeat(5, 1fr);
        }
      }

      .fg-item {
        background: var(--card);
        border: 1px solid var(--border);
        border-radius: var(--rsm);
        padding: 7px 10px;
        display: flex;
        flex-direction: column;
        gap: 2px;
      }

      .fgi-ko {
        font-family: "JetBrains Mono", monospace;
        font-size: 10px;
        letter-spacing: 0.1em;
        text-transform: uppercase;
        color: var(--fg3);
      }

      .fgi-match {
        font-size: 13px;
        font-weight: 700;
        color: var(--fg);
        line-height: 1.3;
      }

      .fgi-conf {
        font-family: "JetBrains Mono", monospace;
        font-size: 10px;
        text-transform: uppercase;
      }

      @media (min-width: 480px) {
        .hero {
          padding: 34px 20px 38px;
        }
      }

      @media (min-width: 768px) {
        .hero {
          padding: 42px 28px 46px;
        }
      }

      /* ══ LEGEND ══ */
      .legend {
        display: flex;
        gap: 14px;
        flex-wrap: wrap;
        margin-bottom: 14px;
        padding: 10px var(--px);
        background: var(--card);
        border: 1px solid var(--border);
        border-radius: var(--rsm);
      }

      .leg {
        display: flex;
        align-items: center;
        gap: 5px;
        font-family: "JetBrains Mono", monospace;
        font-size: 10px;
        letter-spacing: 0.1em;
        text-transform: uppercase;
        color: var(--fg3);
      }

      .leg-d {
        width: 12px;
        height: 3px;
        border-radius: 2px;
        flex-shrink: 0;
      }

      @media (min-width: 480px) {
        .legend {
          padding: 10px 20px;
        }
      }

      /* ══ WRAP ══ */
      .wrap {
        max-width: 1080px;
        margin: 0 auto;
        padding: 18px var(--px) 80px;
      }

      @media (min-width: 480px) {
        .wrap {
          padding: 22px 20px 88px;
        }
      }

      @media (min-width: 768px) {
        .wrap {
          padding: 28px 28px 96px;
        }
      }

      /* ══ PATH DIVIDER ══ */
      .path-hdr {
        display: flex;
        align-items: center;
        gap: 10px;
        margin-bottom: 12px;
        margin-top: 6px;
        font-family: "JetBrains Mono", monospace;
        font-size: 12px;
        letter-spacing: 0.2em;
        text-transform: uppercase;
      }

      .path-hdr::after {
        content: "";
        flex: 1;
        height: 1px;
        background: var(--border);
      }

      .ph-a {
        color: var(--cyan);
      }

      .ph-b {
        color: var(--green);
      }

      .ph-c {
        color: var(--orange);
      }

      .ph-d {
        color: var(--purple);
      }

      .ph-ic {
        color: var(--pink);
      }

      .ph-ic2 {
        color: var(--gold);
      }

      /* ══ FIXTURE CARD ══ */
      .fc {
        background: var(--card);
        border: 1px solid var(--border);
        border-radius: var(--r);
        overflow: hidden;
        margin-bottom: 10px;
        transition:
          border-color 0.18s,
          box-shadow 0.18s;
      }

      .fc:hover {
        border-color: var(--border2);
        box-shadow: 0 3px 20px rgba(0, 0, 0, 0.45);
      }

      /* ko row */
      .fc-ko {
        display: flex;
        align-items: center;
        justify-content: space-between;
        padding: 7px var(--px);
        background: var(--bg2);
        border-bottom: 1px solid var(--border);
        gap: 8px;
      }

      .ko-t {
        font-family: "JetBrains Mono", monospace;
        font-size: 11px;
        letter-spacing: 0.1em;
        text-transform: uppercase;
        font-weight: 600;
      }

      .ko-venue {
        font-family: "JetBrains Mono", monospace;
        font-size: 11px;
        color: var(--fg3);
        text-overflow: ellipsis;
        overflow: hidden;
        white-space: nowrap;
      }

      .ko-badge {
        font-family: "JetBrains Mono", monospace;
        font-size: 10px;
        font-weight: 700;
        padding: 4px 10px;
        border-radius: var(--rxs);
        border: 1px solid;
        white-space: nowrap;
        flex-shrink: 0;
      }

      .kb-hi {
        color: var(--orange);
        border-color: rgba(233, 121, 30, 0.5);
        background: var(--orange-d);
      }

      .kb-med {
        color: var(--cyan);
        border-color: rgba(34, 211, 238, 0.35);
        background: var(--cyan-d);
      }

      .kb-ic {
        color: var(--pink);
        border-color: rgba(244, 114, 182, 0.35);
        background: var(--pink-d);
      }

      @media (min-width: 480px) {
        .fc-ko {
          padding: 7px 16px;
        }
      }

      /* teams */
      .fc-top {
        display: grid;
        grid-template-columns: 1fr auto 1fr;
        padding: 14px 10px 12px;
        gap: 6px;
        padding: 14px 10px 12px;
      }

      /* both home and away: flag above name, centered */
      .fc-team {
        display: flex;
        flex-direction: column;
        align-items: center;
        text-align: center;
        gap: 6px;
      }

      .fc-team.away {
        flex-direction: column;
        text-align: center;
      }

      .fc-badge {
        width: 40px;
        height: 40px;
        flex-shrink: 0;
      }

      .fc-badge img {
        width: 100%;
        height: 100%;
        object-fit: contain;
        filter: drop-shadow(0 1px 3px rgba(0, 0, 0, 0.5));
      }

      .fc-info {
        display: flex;
        flex-direction: column;
      }

      .fc-team.away .fc-info {
        align-items: center;
      }

      .fc-club {
        font-size: 16px;
        font-weight: 700;
        letter-spacing: -0.01em;
        color: var(--fg);
        line-height: 1.1;
      }

      .fc-meta {
        font-family: "JetBrains Mono", monospace;
        font-size: 10px;
        letter-spacing: 0.03em;
        text-transform: uppercase;
        color: var(--fg3);
        margin-top: 3px;
      }

      .form-r {
        display: flex;
        gap: 3px;
        margin-top: 5px;
      }

      .form-r.rv {
        justify-content: flex-end;
      }

      .fb {
        width: 18px;
        height: 18px;
        border-radius: 3px;
        display: flex;
        align-items: center;
        justify-content: center;
        font-family: "JetBrains Mono", monospace;
        font-size: 12px;
        font-weight: 600;
        flex-shrink: 0;
      }

      .fw {
        background: rgba(74, 222, 128, 0.18);
        color: var(--green);
        border: 1px solid rgba(74, 222, 128, 0.35);
      }

      .fd {
        background: rgba(255, 255, 255, 0.06);
        color: rgba(255, 255, 255, 0.28);
        border: 1px solid rgba(255, 255, 255, 0.1);
      }

      .fl {
        background: rgba(248, 113, 113, 0.18);
        color: var(--red);
        border: 1px solid rgba(248, 113, 113, 0.3);
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
        font-size: 12px;
        letter-spacing: 0.16em;
        text-transform: uppercase;
        text-decoration: overline;

        color: var(--fg3);
      }

      .fc-pred {
        font-size: clamp(28px, 7vw, 40px);
        font-weight: 900;
        letter-spacing: 0.02em;
        line-height: 1;
        color: var(--gold);
        white-space: nowrap;
      }

      .fc-odds {
        font-family: "JetBrains Mono", monospace;
        font-size: 11px;
        color: var(--fg3);
        text-align: center;
        text-decoration: underline;
      }

      @media (min-width: 480px) {
        .fc-top {
          padding: 16px 16px 14px;
          gap: 12px;
        }

        .fc-badge {
          width: 40px;
          height: 40px;
        }
      }

      @media (min-width: 768px) {
        .fc-top {
          padding: 18px 20px 16px;
          gap: 16px;
        }

        .fc-club {
          font-size: 18px;
          text-transform: uppercase;
        }

        .fc-badge {
          width: 48px;
          height: 48px;
        }
      }

      /* prob bar */
      .fc-prob {
        padding: 8px var(--px);
        border-top: 1px solid var(--border);
        background: rgba(255, 255, 255, 0.01);
      }

      .prob-labs {
        display: flex;
        justify-content: space-between;
        margin-bottom: 3px;
      }

      .prob-lab {
        font-family: "JetBrains Mono", monospace;
        font-size: 10px;
        letter-spacing: 0.08em;
        text-transform: uppercase;
        color: var(--fg3);
      }

      .prob-bar {
        display: flex;
        height: 3px;
        border-radius: 2px;
        overflow: hidden;
        gap: 1px;
        margin-bottom: 4px;
      }

      .pb-h {
        background: var(--cyan);
      }

      .pb-d {
        background: var(--border);
      }

      .pb-a {
        background: var(--gold);
      }

      .prob-pcts {
        display: flex;
        justify-content: space-between;
      }

      .pp {
        font-family: "Inter", sans-serif;
        font-size: 15px;
        font-weight: 800;
        line-height: 1;
      }

      .pp-h {
        color: var(--cyan);
      }

      .pp-d {
        color: var(--fg3);
      }

      .pp-a {
        color: var(--gold);
      }

      @media (min-width: 480px) {
        .fc-prob {
          padding: 8px 16px;
        }
      }

      /* ══ STAT GRID ══ */
      .sg {
        border-top: 1px solid var(--border);
        display: grid;
        grid-template-columns: 1fr;
        gap: 0;
      }

      @media (min-width: 580px) {
        .sg {
          grid-template-columns: 1fr 1fr;
        }
      }

      @media (min-width: 900px) {
        .sg {
          grid-template-columns: repeat(4, 1fr);
        }
      }

      .sc {
        padding: 10px var(--px);
        border-bottom: 1px solid var(--border);
        display: flex;
        flex-direction: column;
        gap: 4px;
      }

      @media (min-width: 580px) {
        .sc {
          border-right: 1px solid var(--border);
          padding: 10px 12px;
        }

        .sc:nth-child(2n) {
          border-right: none;
        }
      }

      @media (min-width: 900px) {
        .sc:nth-child(2n) {
          border-right: 1px solid var(--border);
        }

        .sc:nth-child(4n) {
          border-right: none;
        }
      }

      .sc-name {
        font-family: "JetBrains Mono", monospace;
        font-size: 11px;
        letter-spacing: 0.12em;
        text-transform: uppercase;
        color: var(--fg3);
      }

      .sc-nums {
        display: flex;
        align-items: center;
        gap: 5px;
      }

      .sc-lo {
        font-family: "JetBrains Mono", monospace;
        font-size: 12px;
        font-weight: 600;
        color: var(--cyan);
      }

      .sc-sep {
        font-family: "JetBrains Mono", monospace;
        font-size: 11px;
        color: var(--fg3);
      }

      .sc-med {
        font-size: 18px;
        font-weight: 800;
        color: var(--gold);
        letter-spacing: -0.01em;
        margin: 0 2px;
      }

      .sc-hi {
        font-family: "JetBrains Mono", monospace;
        font-size: 12px;
        font-weight: 600;
        color: var(--orange);
      }

      .sc-bar {
        height: 3px;

        border-radius: 2px;
        background: rgba(255, 255, 255, 0.05);
        overflow: hidden;
        position: relative;
      }

      .scb-lo {
        position: absolute;
        left: 0;
        top: 0;
        height: 100%;
        border-radius: 2px;
        background: var(--cyan);
        opacity: 0.7;
      }

      .scb-hi {
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
        font-size: 12px;
        color: var(--fg3);
        line-height: 1.5;
      }

      .sc-conf {
        font-family: "JetBrains Mono", monospace;
        font-size: 12px;
        font-weight: 700;
        padding: 2px 7px;
        border-radius: var(--rxs);
        border: 1px solid;
        display: inline-block;
        margin-top: 1px;
        width: fit-content;
      }

      .conf-hi {
        color: var(--green);
        border-color: rgba(74, 222, 128, 0.35);
        background: var(--green-d);
      }

      .conf-md {
        color: var(--gold);
        border-color: rgba(240, 192, 64, 0.35);
        background: var(--gold-d);
      }

      .conf-lo {
        color: var(--fg3);
        border-color: var(--border2);
        background: rgba(255, 255, 255, 0.02);
      }

      /* ══ CONTEXT STRIP ══ */
      .fc-ctx {
        padding: 9px var(--px);
        border-top: 1px solid var(--border);
        background: rgba(240, 192, 64, 0.02);
        display: flex;
        align-items: flex-start;
        gap: 7px;
      }

      .fc-ctx-icon {
        color: var(--gold);
        font-size: 11px;
        flex-shrink: 0;
        margin-top: 1px;
      }

      .fc-ctx-text {
        font-size: 13px;
        color: var(--fg2);
        line-height: 1.7;
      }

      .fc-ctx-text strong {
        color: var(--fg);
        font-weight: 600;
      }

      .cc-g {
        color: var(--gold);
        font-weight: 600;
      }

      .cc-c {
        color: var(--cyan);
        font-weight: 600;
      }

      .cc-r {
        color: var(--red);
        font-weight: 600;
      }

      .cc-o {
        color: var(--orange);
        font-weight: 600;
      }

      .cc-gr {
        color: var(--green);
        font-weight: 600;
      }

      @media (min-width: 480px) {
        .fc-ctx {
          padding: 9px 16px;
        }
      }

      @media (min-width: 768px) {
        .fc-ctx-text {
          font-size: 12px;
        }
      }

      /* ══ CONF ROW ══ */
      .fc-conf {
        padding: 8px var(--px);
        border-top: 1px solid var(--border);
        background: rgba(255, 255, 255, 0.01);
        display: flex;
        align-items: center;
        gap: 8px;
        flex-wrap: wrap;
      }

      .conf-badge {
        display: inline-flex;
        align-items: center;
        gap: 5px;
        font-family: "JetBrains Mono", monospace;
        font-size: 11px;
        font-weight: 700;
        padding: 5px 12px;
        border-radius: var(--rxs);
        border: 1px solid;
        white-space: nowrap;
        flex-shrink: 0;
      }

      .cb-hi {
        color: var(--green);
        border-color: rgba(74, 222, 128, 0.4);
        background: var(--green-d);
      }

      .cb-md {
        color: var(--orange);
        border-color: rgba(251, 146, 60, 0.4);
        background: var(--orange-d);
      }

      .cb-lo {
        color: var(--red);
        border-color: rgba(248, 113, 113, 0.35);
        background: var(--red-d);
      }

      .conf-dot {
        width: 6px;
        height: 6px;
        border-radius: 50%;
        flex-shrink: 0;
      }

      .cd-hi {
        background: var(--green);
      }

      .cd-md {
        background: var(--orange);
      }

      .cd-lo {
        background: var(--red);
      }

      .conf-reason {
        font-family: "JetBrains Mono", monospace;
        font-size: 11px;
        color: var(--fg2);
        line-height: 1.5;
      }

      @media (min-width: 480px) {
        .fc-conf {
          padding: 8px 16px;
        }
      }

      /* ══ FOOTER ══ */
      footer {
        border-top: 1px solid var(--border);
        padding: 16px var(--px);
        max-width: 1080px;
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
        font-size: 12px;
        font-weight: 600;
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

      /* ══ MOBILE: flags above names + font clarity ══ */
      .form-r,
      .form-r.rv {
        justify-content: center;
      }
      .sc-lo,
      .sc-hi {
        font-size: 13px;
      }
      @media (min-width: 480px) {
        html {
          font-size: 18px;
        }
        .fc-top {
          grid-template-columns: 1fr auto 1fr;
          padding: 14px var(--px) 12px;
          gap: 8px;
        }
        .fc-team {
          flex-direction: column;
          align-items: center;
          text-align: center;
          gap: 8px;
        }
        .fc-team.away .fc-info {
          align-items: center;
        }
        .fc-badge {
          width: 36px;
          height: 36px;
        }
        .fc-club {
          font-size: clamp(14px, 3.5vw, 19px);
        }
        .fc-meta {
          font-size: 10px;
          letter-spacing: 0.05em;
        }
        .fc-pred-lbl {
          font-size: 12px;
        }
        .fc-pred {
          font-size: clamp(26px, 6.5vw, 38px);
        }
        .fc-odds {
          font-size: 10px;
        }
        .ko-t {
          font-size: 12px;
        }
        .ko-venue {
          font-size: 12px;
        }
        .ko-badge {
          font-size: 12px;
          padding: 3px 8px;
        }
        .prob-lab {
          font-size: 7px;
        }
        .pp {
          font-size: 14px;
        }
        .sc-name {
          font-size: 8px;
        }
        .sc-med {
          font-size: 16px;
        }
        .sc-sep {
          font-size: 12px;
        }
        .sc-ctx {
          font-size: 12px;
          line-height: 1.4;
        }
        .sc-conf {
          font-size: 12px;
          padding: 1px 5px;
        }
        .fc-ctx-text {
          font-size: 12px;
          line-height: 1.65;
        }
        .fc-ctx-icon {
          font-size: 12px;
        }
        .conf-badge {
          font-size: 12px;
          padding: 4px 10px;
        }
        .conf-reason {
          font-size: 12px;
          line-height: 1.4;
        }
        .fb {
          width: 16px;
          height: 16px;
          font-size: 8px;
        }
        .hero-eye {
          font-size: 12px;
        }
        .hero-sub {
          font-size: 12px;
        }
        .hdr-brand {
          font-size: 14px;
        }
        .hdr-info {
          font-size: 12px;
        }
        .hdr-count {
          font-size: 10px;
        }
        .path-hdr {
          font-size: 12px;
        }
        .leg {
          font-size: 8px;
        }
        .fgi-ko {
          font-size: 10px;
        }
        .fgi-match {
          font-size: 11px;
        }
        .fgi-conf {
          font-size: 8px;
        }
        .ft-l {
          font-size: 12px;
        }
        .ft-r {
          font-size: 11px;
        }
      }
    </style>
  </head>

  <body>
    <header class="site-hdr">
      <div class="hdr-inner">
        <div class="hdr-brand">
          <div class="dot"></div>
          WC2026 Intel
        </div>
        <div class="hdr-info">Playoff semi-finals · 26 Mar 2026</div>
        <div class="hdr-count">5 fixtures</div>
      </div>
    </header>

    <!-- HERO -->
    <section class="hero rev">
      <div class="hero-inner">
        <div class="hero-eye">World Cup 2026 Qualifier Play-offs</div>
        <h1 class="hero-h1">Thursday<br /><span>26 March</span></h1>
        <p class="hero-sub">
          5 High-Stakes Qualifier / Friendly Predictions · Best / Median / Worst
          stat ranges
        </p>
        <div class="fixture-grid">
          <div class="fg-item">
            <div class="fgi-ko">19:45 · Path A</div>
            <div class="fgi-match">Bosnia vs Italy</div>
          </div>
          <div class="fg-item">
            <div class="fgi-ko">20:45 · Path D</div>
            <div class="fgi-match">Czechia vs Denmark</div>
          </div>
          <div class="fg-item">
            <div class="fgi-ko">20:45 · Path C</div>
            <div class="fgi-match">Kosovo vs Türkiye</div>
          </div>
          <div class="fg-item">
            <div class="fgi-ko">20:45 · Path B</div>
            <div class="fgi-match">Sweden vs Poland</div>
          </div>
          <div class="fg-item">
            <div class="fgi-ko">19:45 · Friendly</div>
            <div class="fgi-match">England vs Japan</div>
          </div>
        </div>
        <div
          style="
            font-family: &quot;JetBrains Mono&quot;, monospace;
            font-size: 12px;
            color: var(--fg3);
            letter-spacing: 0.08em;
          "
        >
          STAT KEY: <span style="color: var(--cyan)">LOW</span> = Best-case
          defensive/controlled scenario ·
          <span style="color: var(--gold)">MED</span> = Most likely ·
          <span style="color: var(--orange)">HIGH</span> = High-intensity
          worst/best case
        </div>
      </div>
    </section>

    <div class="wrap">
      <div class="legend rev">
        <div class="leg">
          <div class="leg-d" style="background: var(--cyan)"></div>
          Best case / lowest
        </div>
        <div class="leg">
          <div class="leg-d" style="background: var(--gold)"></div>
          Median expected
        </div>
        <div class="leg">
          <div class="leg-d" style="background: var(--orange)"></div>
          Worst case / highest
        </div>
      </div>

      <div class="path-hdr rev">
        <span class="ph-a"
          >Path A Play-off — Bosnia-Herzegovina vs Italy · 19:45 CET · Bilino
          Polje Stadium</span
        >
      </div>
      <div class="fc rev">
        <div class="fc-ko">
          <div>
            <span class="ko-t" style="color: var(--cyan)">19:45 CET</span>
            <span class="ko-venue">Bilino Polje Stadium</span>
          </div>
          <span class="ko-badge kb-hi">⚡ High stakes</span>
        </div>
        <div class="fc-top">
          <div class="fc-team">
            <div class="fc-badge">
              <img
                src="https://flagcdn.com/w160/ba.png"
                alt="Bosnia"
                loading="lazy"
                style="background-color: #111320"
              />
            </div>
            <div class="fc-info">
              <div class="fc-club">Bosnia</div>
              <div class="fc-meta">FIFA 75 · 8.8 corners/g</div>
              <div class="form-r">
                <div class="fb fw">W</div>
                <div class="fb fd">D</div>
                <div class="fb fw">W</div>
                <div class="fb fl">L</div>
                <div class="fb fd">D</div>
              </div>
            </div>
          </div>
          <div class="fc-mid">
            <div class="fc-pred-lbl">Predicted</div>
            <div class="fc-pred">0–2</div>
            <div class="fc-odds">ITA 4/9 · BOS 6/1</div>
          </div>
          <div class="fc-team away">
            <div class="fc-badge">
              <img
                src="https://flagcdn.com/w160/it.png"
                alt="Italy"
                loading="lazy"
                style="background-color: #111320"
              />
            </div>
            <div class="fc-info">
              <div class="fc-club">Italy</div>
              <div class="fc-meta">FIFA 9 · Spalletti logic</div>
              <div class="form-r rv">
                <div class="fb fw">W</div>
                <div class="fb fw">W</div>
                <div class="fb fw">W</div>
                <div class="fb fw">W</div>
                <div class="fb fl">L</div>
              </div>
            </div>
          </div>
        </div>
        <div class="fc-prob">
          <div class="prob-labs">
            <span class="prob-lab">BOS</span
            ><span class="prob-lab">Draw/AET</span
            ><span class="prob-lab">ITA</span>
          </div>
          <div class="prob-bar">
            <div class="pb-h" style="flex: 10"></div>
            <div class="pb-d" style="flex: 20"></div>
            <div class="pb-a" style="flex: 70"></div>
          </div>
          <div class="prob-pcts">
            <span class="pp pp-h">10%</span><span class="pp pp-d">20%</span
            ><span class="pp pp-a">70%</span>
          </div>
        </div>
        <div class="sg">
          <div class="sc">
            <div class="sc-name">Corners</div>
            <div class="sc-nums">
              <span class="sc-lo">7</span><span class="sc-sep">·</span
              ><span class="sc-med">10</span><span class="sc-sep">·</span
              ><span class="sc-hi">14</span>
            </div>
            <div class="sc-bar">
              <div class="scb-lo" style="width: 25%"></div>
              <div class="scb-hi" style="width: 57%"></div>
            </div>
            <div class="sc-ctx">
              Both avg ~8.8 in their leagues. Italy dominates poss.
            </div>
            <span class="sc-conf conf-hi">Hi</span>
          </div>
          <div class="sc">
            <div class="sc-name">Shots on Target</div>
            <div class="sc-nums">
              <span class="sc-lo">5</span><span class="sc-sep">·</span
              ><span class="sc-med">8</span><span class="sc-sep">·</span
              ><span class="sc-hi">12</span>
            </div>
            <div class="sc-bar">
              <div class="scb-lo" style="width: 20%"></div>
              <div class="scb-hi" style="width: 53%"></div>
            </div>
            <div class="sc-ctx">Italy 6+ SoT avg. Bosnia concedes shots.</div>
            <span class="sc-conf conf-hi">Hi</span>
          </div>
          <div class="sc">
            <div class="sc-name">Total Shots</div>
            <div class="sc-nums">
              <span class="sc-lo">18</span><span class="sc-sep">·</span
              ><span class="sc-med">25</span><span class="sc-sep">·</span
              ><span class="sc-hi">31</span>
            </div>
            <div class="sc-bar">
              <div class="scb-lo" style="width: 29%"></div>
              <div class="scb-hi" style="width: 64%"></div>
            </div>
            <div class="sc-ctx">
              High volume expected from Italy pushing for early goal.
            </div>
            <span class="sc-conf conf-hi">Hi</span>
          </div>
          <div class="sc">
            <div class="sc-name">Yellow Cards</div>
            <div class="sc-nums">
              <span class="sc-lo">3</span><span class="sc-sep">·</span
              ><span class="sc-med">5</span><span class="sc-sep">·</span
              ><span class="sc-hi">8</span>
            </div>
            <div class="sc-bar">
              <div class="scb-lo" style="width: 18%"></div>
              <div class="scb-hi" style="width: 50%"></div>
            </div>
            <div class="sc-ctx">
              Serie A / Bosnian league avg is 4+. High stakes play-off.
            </div>
            <span class="sc-conf conf-hi">Hi</span>
          </div>
          <div class="sc">
            <div class="sc-name">Red Cards</div>
            <div class="sc-nums">
              <span class="sc-lo">0</span><span class="sc-sep">·</span
              ><span class="sc-med">0</span><span class="sc-sep">·</span
              ><span class="sc-hi">1</span>
            </div>
            <div class="sc-bar">
              <div class="scb-lo" style="width: 0%"></div>
              <div class="scb-hi" style="width: 0%"></div>
            </div>
            <div class="sc-ctx">
              Tense qualifier, but mostly tactical fouls expected.
            </div>
            <span class="sc-conf conf-lo">Lo</span>
          </div>
          <div class="sc">
            <div class="sc-name">Fouls</div>
            <div class="sc-nums">
              <span class="sc-lo">22</span><span class="sc-sep">·</span
              ><span class="sc-med">27</span><span class="sc-sep">·</span
              ><span class="sc-hi">34</span>
            </div>
            <div class="sc-bar">
              <div class="scb-lo" style="width: 32%"></div>
              <div class="scb-hi" style="width: 63%"></div>
            </div>
            <div class="sc-ctx">
              Bosnia avg 29 fouls/g combined. Match will be interrupted often.
            </div>
            <span class="sc-conf conf-md">Med</span>
          </div>
          <div class="sc">
            <div class="sc-name">Tackles</div>
            <div class="sc-nums">
              <span class="sc-lo">25</span><span class="sc-sep">·</span
              ><span class="sc-med">32</span><span class="sc-sep">·</span
              ><span class="sc-hi">40</span>
            </div>
            <div class="sc-bar">
              <div class="scb-lo" style="width: 31%"></div>
              <div class="scb-hi" style="width: 64%"></div>
            </div>
            <div class="sc-ctx">
              Intense midfield battle. Barella and Tonali active.
            </div>
            <span class="sc-conf conf-md">Med</span>
          </div>
          <div class="sc">
            <div class="sc-name">Throw-ins</div>
            <div class="sc-nums">
              <span class="sc-lo">30</span><span class="sc-sep">·</span
              ><span class="sc-med">38</span><span class="sc-sep">·</span
              ><span class="sc-hi">48</span>
            </div>
            <div class="sc-bar">
              <div class="scb-lo" style="width: 31%"></div>
              <div class="scb-hi" style="width: 63%"></div>
            </div>
            <div class="sc-ctx">
              Wide play expected, typical for Italy's wingbacks.
            </div>
            <span class="sc-conf conf-md">Med</span>
          </div>
          <div class="sc">
            <div class="sc-name">Goal Kicks</div>
            <div class="sc-nums">
              <span class="sc-lo">13</span><span class="sc-sep">·</span
              ><span class="sc-med">18</span><span class="sc-sep">·</span
              ><span class="sc-hi">24</span>
            </div>
            <div class="sc-bar">
              <div class="scb-lo" style="width: 27%"></div>
              <div class="scb-hi" style="width: 60%"></div>
            </div>
            <div class="sc-ctx">
              Many missed attempts from long range likely.
            </div>
            <span class="sc-conf conf-lo">Lo</span>
          </div>
        </div>
        <div class="fc-ctx">
          <span class="fc-ctx-icon">◆</span>
          <p class="fc-ctx-text">
            <strong>Italy never loses this match on paper</strong>. Bosnia is
            missing some historical key figures at their peak, although playing
            at home in Bilino Polje is daunting. Italy's H2H dominance (4W 1D
            1L) and far superior underlying metrics. Expect Italy to control the
            ball.
          </p>
        </div>
        <div class="fc-conf">
          <span class="conf-badge cb-hi"
            ><span class="conf-dot cd-hi"></span>HIGH confidence</span
          >
          <span class="conf-reason"
            >Italy 70% win prob · Dominant squad depth</span
          >
        </div>
      </div>

      <div class="path-hdr rev">
        <span class="ph-a"
          >Path D Play-off — Czech Republic vs Denmark · 20:45 CET · epet
          ARENA</span
        >
      </div>
      <div class="fc rev">
        <div class="fc-ko">
          <div>
            <span class="ko-t" style="color: var(--cyan)">20:45 CET</span>
            <span class="ko-venue">epet ARENA</span>
          </div>
          <span class="ko-badge kb-hi">⚡ High stakes</span>
        </div>
        <div class="fc-top">
          <div class="fc-team">
            <div class="fc-badge">
              <img
                src="https://flagcdn.com/w160/cz.png"
                alt="Czechia"
                loading="lazy"
                style="background-color: #111320"
              />
            </div>
            <div class="fc-info">
              <div class="fc-club">Czechia</div>
              <div class="fc-meta">FIFA 39 · Unbeaten home 18g</div>
              <div class="form-r">
                <div class="fb fd">D</div>
                <div class="fb fw">W</div>
                <div class="fb fw">W</div>
                <div class="fb fl">L</div>
                <div class="fb fd">D</div>
              </div>
            </div>
          </div>
          <div class="fc-mid">
            <div class="fc-pred-lbl">Predicted</div>
            <div class="fc-pred">1–2</div>
            <div class="fc-odds">CZE 2/1 · DEN 13/10</div>
          </div>
          <div class="fc-team away">
            <div class="fc-badge">
              <img
                src="https://flagcdn.com/w160/dk.png"
                alt="Denmark"
                loading="lazy"
                style="background-color: #111320"
              />
            </div>
            <div class="fc-info">
              <div class="fc-club">Denmark</div>
              <div class="fc-meta">FIFA 21 · Attacking style</div>
              <div class="form-r rv">
                <div class="fb fw">W</div>
                <div class="fb fl">L</div>
                <div class="fb fd">D</div>
                <div class="fb fw">W</div>
                <div class="fb fw">W</div>
              </div>
            </div>
          </div>
        </div>
        <div class="fc-prob">
          <div class="prob-labs">
            <span class="prob-lab">CZE</span
            ><span class="prob-lab">Draw/AET</span
            ><span class="prob-lab">DEN</span>
          </div>
          <div class="prob-bar">
            <div class="pb-h" style="flex: 35"></div>
            <div class="pb-d" style="flex: 25"></div>
            <div class="pb-a" style="flex: 40"></div>
          </div>
          <div class="prob-pcts">
            <span class="pp pp-h">35%</span><span class="pp pp-d">25%</span
            ><span class="pp pp-a">40%</span>
          </div>
        </div>
        <div class="sg">
          <div class="sc">
            <div class="sc-name">Corners</div>
            <div class="sc-nums">
              <span class="sc-lo">8</span><span class="sc-sep">·</span
              ><span class="sc-med">11</span><span class="sc-sep">·</span
              ><span class="sc-hi">15</span>
            </div>
            <div class="sc-bar">
              <div class="scb-lo" style="width: 26%"></div>
              <div class="scb-hi" style="width: 58%"></div>
            </div>
            <div class="sc-ctx">
              Denmark heavily relies on width and crosses.
            </div>
            <span class="sc-conf conf-hi">Hi</span>
          </div>
          <div class="sc">
            <div class="sc-name">Shots on Target</div>
            <div class="sc-nums">
              <span class="sc-lo">6</span><span class="sc-sep">·</span
              ><span class="sc-med">9</span><span class="sc-sep">·</span
              ><span class="sc-hi">13</span>
            </div>
            <div class="sc-bar">
              <div class="scb-lo" style="width: 23%"></div>
              <div class="scb-hi" style="width: 55%"></div>
            </div>
            <div class="sc-ctx">
              Denmark scores ~3/g recently. Czechia solid at home.
            </div>
            <span class="sc-conf conf-md">Med</span>
          </div>
          <div class="sc">
            <div class="sc-name">Total Shots</div>
            <div class="sc-nums">
              <span class="sc-lo">18</span><span class="sc-sep">·</span
              ><span class="sc-med">24</span><span class="sc-sep">·</span
              ><span class="sc-hi">32</span>
            </div>
            <div class="sc-bar">
              <div class="scb-lo" style="width: 28%"></div>
              <div class="scb-hi" style="width: 60%"></div>
            </div>
            <div class="sc-ctx">Open game if an early goal is scored.</div>
            <span class="sc-conf conf-md">Med</span>
          </div>
          <div class="sc">
            <div class="sc-name">Yellow Cards</div>
            <div class="sc-nums">
              <span class="sc-lo">2</span><span class="sc-sep">·</span
              ><span class="sc-med">4</span><span class="sc-sep">·</span
              ><span class="sc-hi">7</span>
            </div>
            <div class="sc-bar">
              <div class="scb-lo" style="width: 14%"></div>
              <div class="scb-hi" style="width: 45%"></div>
            </div>
            <div class="sc-ctx">
              Neither team historically overly aggressive. Mostly tactical.
            </div>
            <span class="sc-conf conf-md">Med</span>
          </div>
          <div class="sc">
            <div class="sc-name">Red Cards</div>
            <div class="sc-nums">
              <span class="sc-lo">0</span><span class="sc-sep">·</span
              ><span class="sc-med">0</span><span class="sc-sep">·</span
              ><span class="sc-hi">1</span>
            </div>
            <div class="sc-bar">
              <div class="scb-lo" style="width: 0%"></div>
              <div class="scb-hi" style="width: 0%"></div>
            </div>
            <div class="sc-ctx">Low probability of a send-off.</div>
            <span class="sc-conf conf-lo">Lo</span>
          </div>
          <div class="sc">
            <div class="sc-name">Fouls</div>
            <div class="sc-nums">
              <span class="sc-lo">18</span><span class="sc-sep">·</span
              ><span class="sc-med">23</span><span class="sc-sep">·</span
              ><span class="sc-hi">29</span>
            </div>
            <div class="sc-bar">
              <div class="scb-lo" style="width: 31%"></div>
              <div class="scb-hi" style="width: 63%"></div>
            </div>
            <div class="sc-ctx">
              Structured European play style. Less chaotic than Balkan derbies.
            </div>
            <span class="sc-conf conf-md">Med</span>
          </div>
          <div class="sc">
            <div class="sc-name">Tackles</div>
            <div class="sc-nums">
              <span class="sc-lo">24</span><span class="sc-sep">·</span
              ><span class="sc-med">30</span><span class="sc-sep">·</span
              ><span class="sc-hi">38</span>
            </div>
            <div class="sc-bar">
              <div class="scb-lo" style="width: 31%"></div>
              <div class="scb-hi" style="width: 63%"></div>
            </div>
            <div class="sc-ctx">Middle of the park battles.</div>
            <span class="sc-conf conf-md">Med</span>
          </div>
          <div class="sc">
            <div class="sc-name">Throw-ins</div>
            <div class="sc-nums">
              <span class="sc-lo">32</span><span class="sc-sep">·</span
              ><span class="sc-med">40</span><span class="sc-sep">·</span
              ><span class="sc-hi">50</span>
            </div>
            <div class="sc-bar">
              <div class="scb-lo" style="width: 32%"></div>
              <div class="scb-hi" style="width: 64%"></div>
            </div>
            <div class="sc-ctx">
              Pacey wingers on both sides pushing to the byline.
            </div>
            <span class="sc-conf conf-md">Med</span>
          </div>
          <div class="sc">
            <div class="sc-name">Goal Kicks</div>
            <div class="sc-nums">
              <span class="sc-lo">14</span><span class="sc-sep">·</span
              ><span class="sc-med">19</span><span class="sc-sep">·</span
              ><span class="sc-hi">25</span>
            </div>
            <div class="sc-bar">
              <div class="scb-lo" style="width: 28%"></div>
              <div class="scb-hi" style="width: 60%"></div>
            </div>
            <div class="sc-ctx">Standard expected range.</div>
            <span class="sc-conf conf-lo">Lo</span>
          </div>
        </div>
        <div class="fc-ctx">
          <span class="fc-ctx-icon">◆</span>
          <p class="fc-ctx-text">
            <strong>Huge tactical battle</strong>. Czech Republic are undefeated
            in 18 home games, making epet ARENA a fortress. Denmark, however,
            carries serious firepower. The Danes knocked Czechia out of Euro
            2020 (2-1). BTTS is highly likely. We expect a narrow Danish
            victory.
          </p>
        </div>
        <div class="fc-conf">
          <span class="conf-badge cb-md"
            ><span class="conf-dot cd-md"></span>MED confidence</span
          >
          <span class="conf-reason"
            >Tight match · Danish quality slight edge</span
          >
        </div>
      </div>

      <div class="path-hdr rev">
        <span class="ph-a"
          >Path C Play-off — Kosovo vs Turkey · 20:45 CET · Fadil Vokrri
          Stadium</span
        >
      </div>
      <div class="fc rev">
        <div class="fc-ko">
          <div>
            <span class="ko-t" style="color: var(--cyan)">20:45 CET</span>
            <span class="ko-venue">Fadil Vokrri Stadium</span>
          </div>
          <span class="ko-badge kb-hi">⚡ High stakes</span>
        </div>
        <div class="fc-top">
          <div class="fc-team">
            <div class="fc-badge">
              <img
                src="https://flagcdn.com/w160/xk.png"
                alt="Kosovo"
                loading="lazy"
                style="background-color: #111320"
              />
            </div>
            <div class="fc-info">
              <div class="fc-club">Kosovo</div>
              <div class="fc-meta">FIFA 100+ · 4-3 win int SF</div>
              <div class="form-r">
                <div class="fb fw">W</div>
                <div class="fb fd">D</div>
                <div class="fb fw">W</div>
                <div class="fb fw">W</div>
                <div class="fb fd">D</div>
              </div>
            </div>
          </div>
          <div class="fc-mid">
            <div class="fc-pred-lbl">Predicted</div>
            <div class="fc-pred">1–3</div>
            <div class="fc-odds">KOS 3/1 · TUR 5/6</div>
          </div>
          <div class="fc-team away">
            <div class="fc-badge">
              <img
                src="https://flagcdn.com/w160/tr.png"
                alt="Türkiye"
                loading="lazy"
                style="background-color: #111320"
              />
            </div>
            <div class="fc-info">
              <div class="fc-club">Türkiye</div>
              <div class="fc-meta">FIFA ~35 · Won all 3 H2H</div>
              <div class="form-r rv">
                <div class="fb fw">W</div>
                <div class="fb fd">D</div>
                <div class="fb fw">W</div>
                <div class="fb fw">W</div>
                <div class="fb fw">W</div>
              </div>
            </div>
          </div>
        </div>
        <div class="fc-prob">
          <div class="prob-labs">
            <span class="prob-lab">KOS</span
            ><span class="prob-lab">Draw/AET</span
            ><span class="prob-lab">TUR</span>
          </div>
          <div class="prob-bar">
            <div class="pb-h" style="flex: 20"></div>
            <div class="pb-d" style="flex: 20"></div>
            <div class="pb-a" style="flex: 60"></div>
          </div>
          <div class="prob-pcts">
            <span class="pp pp-h">20%</span><span class="pp pp-d">20%</span
            ><span class="pp pp-a">60%</span>
          </div>
        </div>
        <div class="sg">
          <div class="sc">
            <div class="sc-name">Corners</div>
            <div class="sc-nums">
              <span class="sc-lo">7</span><span class="sc-sep">·</span
              ><span class="sc-med">10</span><span class="sc-sep">·</span
              ><span class="sc-hi">13</span>
            </div>
            <div class="sc-bar">
              <div class="scb-lo" style="width: 26%"></div>
              <div class="scb-hi" style="width: 61%"></div>
            </div>
            <div class="sc-ctx">
              Turkey will play expansive passing. Kosovo will counter.
            </div>
            <span class="sc-conf conf-md">Med</span>
          </div>
          <div class="sc">
            <div class="sc-name">Shots on Target</div>
            <div class="sc-nums">
              <span class="sc-lo">7</span><span class="sc-sep">·</span
              ><span class="sc-med">11</span><span class="sc-sep">·</span
              ><span class="sc-hi">15</span>
            </div>
            <div class="sc-bar">
              <div class="scb-lo" style="width: 23%"></div>
              <div class="scb-hi" style="width: 58%"></div>
            </div>
            <div class="sc-ctx">
              Both teams scored well in semis. Defenses have gaps.
            </div>
            <span class="sc-conf conf-hi">Hi</span>
          </div>
          <div class="sc">
            <div class="sc-name">Total Shots</div>
            <div class="sc-nums">
              <span class="sc-lo">20</span><span class="sc-sep">·</span
              ><span class="sc-med">28</span><span class="sc-sep">·</span
              ><span class="sc-hi">36</span>
            </div>
            <div class="sc-bar">
              <div class="scb-lo" style="width: 27%"></div>
              <div class="scb-hi" style="width: 62%"></div>
            </div>
            <div class="sc-ctx">
              Open, chaotic game likely. Kosovo pushed by passionate crowd.
            </div>
            <span class="sc-conf conf-hi">Hi</span>
          </div>
          <div class="sc">
            <div class="sc-name">Yellow Cards</div>
            <div class="sc-nums">
              <span class="sc-lo">4</span><span class="sc-sep">·</span
              ><span class="sc-med">6</span><span class="sc-sep">·</span
              ><span class="sc-hi">9</span>
            </div>
            <div class="sc-bar">
              <div class="scb-lo" style="width: 22%"></div>
              <div class="scb-hi" style="width: 53%"></div>
            </div>
            <div class="sc-ctx">
              Eastern European derby energy. High emotion, likely cards.
            </div>
            <span class="sc-conf conf-hi">Hi</span>
          </div>
          <div class="sc">
            <div class="sc-name">Red Cards</div>
            <div class="sc-nums">
              <span class="sc-lo">0</span><span class="sc-sep">·</span
              ><span class="sc-med">0</span><span class="sc-sep">·</span
              ><span class="sc-hi">1</span>
            </div>
            <div class="sc-bar">
              <div class="scb-lo" style="width: 0%"></div>
              <div class="scb-hi" style="width: 0%"></div>
            </div>
            <div class="sc-ctx">
              Decent chance of double yellows if game gets out of hand.
            </div>
            <span class="sc-conf conf-md">Med</span>
          </div>
          <div class="sc">
            <div class="sc-name">Fouls</div>
            <div class="sc-nums">
              <span class="sc-lo">25</span><span class="sc-sep">·</span
              ><span class="sc-med">30</span><span class="sc-sep">·</span
              ><span class="sc-hi">38</span>
            </div>
            <div class="sc-bar">
              <div class="scb-lo" style="width: 32%"></div>
              <div class="scb-hi" style="width: 63%"></div>
            </div>
            <div class="sc-ctx">
              Lots of disruptive play to break Turkey's rhythm.
            </div>
            <span class="sc-conf conf-hi">Hi</span>
          </div>
          <div class="sc">
            <div class="sc-name">Tackles</div>
            <div class="sc-nums">
              <span class="sc-lo">28</span><span class="sc-sep">·</span
              ><span class="sc-med">35</span><span class="sc-sep">·</span
              ><span class="sc-hi">44</span>
            </div>
            <div class="sc-bar">
              <div class="scb-lo" style="width: 31%"></div>
              <div class="scb-hi" style="width: 63%"></div>
            </div>
            <div class="sc-ctx">Kosovo will need to dig in defensively.</div>
            <span class="sc-conf conf-hi">Hi</span>
          </div>
          <div class="sc">
            <div class="sc-name">Throw-ins</div>
            <div class="sc-nums">
              <span class="sc-lo">35</span><span class="sc-sep">·</span
              ><span class="sc-med">42</span><span class="sc-sep">·</span
              ><span class="sc-hi">55</span>
            </div>
            <div class="sc-bar">
              <div class="scb-lo" style="width: 31%"></div>
              <div class="scb-hi" style="width: 61%"></div>
            </div>
            <div class="sc-ctx">
              Fast transitions resulting in clearances out over touchlines.
            </div>
            <span class="sc-conf conf-hi">Hi</span>
          </div>
          <div class="sc">
            <div class="sc-name">Goal Kicks</div>
            <div class="sc-nums">
              <span class="sc-lo">15</span><span class="sc-sep">·</span
              ><span class="sc-med">20</span><span class="sc-sep">·</span
              ><span class="sc-hi">26</span>
            </div>
            <div class="sc-bar">
              <div class="scb-lo" style="width: 28%"></div>
              <div class="scb-hi" style="width: 61%"></div>
            </div>
            <div class="sc-ctx">A lot of chaotic final third action.</div>
            <span class="sc-conf conf-md">Med</span>
          </div>
        </div>
        <div class="fc-ctx">
          <span class="fc-ctx-icon">◆</span>
          <p class="fc-ctx-text">
            <strong>Turkey are heavily favored</strong>. In 3 historical
            meetings, Turkey has 3 wins with a 12-2 aggregate goals tally.
            Kosovo will rely on home crowd emotion at Fadil Vokrri. An early
            Turkish goal could open the floodgates. Expect high event stats.
          </p>
        </div>
        <div class="fc-conf">
          <span class="conf-badge cb-hi"
            ><span class="conf-dot cd-hi"></span>HIGH confidence</span
          >
          <span class="conf-reason">Turkey 3-0 H2H · Stronger generation</span>
        </div>
      </div>

      <div class="path-hdr rev">
        <span class="ph-a"
          >WC Qualification Play-off — Sweden vs Poland · 20:45 CET · Strawberry
          Arena</span
        >
      </div>
      <div class="fc rev">
        <div class="fc-ko">
          <div>
            <span class="ko-t" style="color: var(--cyan)">20:45 CET</span>
            <span class="ko-venue">Strawberry Arena</span>
          </div>
          <span class="ko-badge kb-hi">⚡ High stakes</span>
        </div>
        <div class="fc-top">
          <div class="fc-team">
            <div class="fc-badge">
              <img
                src="https://flagcdn.com/w160/se.png"
                alt="Sweden"
                loading="lazy"
                style="background-color: #111320"
              />
            </div>
            <div class="fc-info">
              <div class="fc-club">Sweden</div>
              <div class="fc-meta">FIFA ~23 · Gyökeres on fire</div>
              <div class="form-r">
                <div class="fb fw">W</div>
                <div class="fb fd">D</div>
                <div class="fb fl">L</div>
                <div class="fb fl">L</div>
                <div class="fb fl">L</div>
              </div>
            </div>
          </div>
          <div class="fc-mid">
            <div class="fc-pred-lbl">Predicted</div>
            <div class="fc-pred">2–1</div>
            <div class="fc-odds">SWE 6/5 · POL 2/1</div>
          </div>
          <div class="fc-team away">
            <div class="fc-badge">
              <img
                src="https://flagcdn.com/w160/pl.png"
                alt="Poland"
                loading="lazy"
                style="background-color: #111320"
              />
            </div>
            <div class="fc-info">
              <div class="fc-club">Poland</div>
              <div class="fc-meta">FIFA ~30 · Lewandowski veteran</div>
              <div class="form-r rv">
                <div class="fb fw">W</div>
                <div class="fb fw">W</div>
                <div class="fb fd">D</div>
                <div class="fb fw">W</div>
                <div class="fb fw">W</div>
              </div>
            </div>
          </div>
        </div>
        <div class="fc-prob">
          <div class="prob-labs">
            <span class="prob-lab">SWE</span
            ><span class="prob-lab">Draw/AET</span
            ><span class="prob-lab">POL</span>
          </div>
          <div class="prob-bar">
            <div class="pb-h" style="flex: 45"></div>
            <div class="pb-d" style="flex: 25"></div>
            <div class="pb-a" style="flex: 30"></div>
          </div>
          <div class="prob-pcts">
            <span class="pp pp-h">45%</span><span class="pp pp-d">25%</span
            ><span class="pp pp-a">30%</span>
          </div>
        </div>
        <div class="sg">
          <div class="sc">
            <div class="sc-name">Corners</div>
            <div class="sc-nums">
              <span class="sc-lo">8</span><span class="sc-sep">·</span
              ><span class="sc-med">11</span><span class="sc-sep">·</span
              ><span class="sc-hi">15</span>
            </div>
            <div class="sc-bar">
              <div class="scb-lo" style="width: 26%"></div>
              <div class="scb-hi" style="width: 58%"></div>
            </div>
            <div class="sc-ctx">
              Sweden plays wide, especially at home. Poland physically strong.
            </div>
            <span class="sc-conf conf-md">Med</span>
          </div>
          <div class="sc">
            <div class="sc-name">Shots on Target</div>
            <div class="sc-nums">
              <span class="sc-lo">6</span><span class="sc-sep">·</span
              ><span class="sc-med">9</span><span class="sc-sep">·</span
              ><span class="sc-hi">13</span>
            </div>
            <div class="sc-bar">
              <div class="scb-lo" style="width: 23%"></div>
              <div class="scb-hi" style="width: 55%"></div>
            </div>
            <div class="sc-ctx">
              Gyökeres vs Lewandowski. Quality finishers present.
            </div>
            <span class="sc-conf conf-md">Med</span>
          </div>
          <div class="sc">
            <div class="sc-name">Total Shots</div>
            <div class="sc-nums">
              <span class="sc-lo">18</span><span class="sc-sep">·</span
              ><span class="sc-med">24</span><span class="sc-sep">·</span
              ><span class="sc-hi">30</span>
            </div>
            <div class="sc-bar">
              <div class="scb-lo" style="width: 30%"></div>
              <div class="scb-hi" style="width: 64%"></div>
            </div>
            <div class="sc-ctx">Tactical first half, opening up late.</div>
            <span class="sc-conf conf-md">Med</span>
          </div>
          <div class="sc">
            <div class="sc-name">Yellow Cards</div>
            <div class="sc-nums">
              <span class="sc-lo">3</span><span class="sc-sep">·</span
              ><span class="sc-med">5</span><span class="sc-sep">·</span
              ><span class="sc-hi">8</span>
            </div>
            <div class="sc-bar">
              <div class="scb-lo" style="width: 18%"></div>
              <div class="scb-hi" style="width: 50%"></div>
            </div>
            <div class="sc-ctx">
              Physical match but fair. Likely to cluster in 2nd half.
            </div>
            <span class="sc-conf conf-md">Med</span>
          </div>
          <div class="sc">
            <div class="sc-name">Red Cards</div>
            <div class="sc-nums">
              <span class="sc-lo">0</span><span class="sc-sep">·</span
              ><span class="sc-med">0</span><span class="sc-sep">·</span
              ><span class="sc-hi">1</span>
            </div>
            <div class="sc-bar">
              <div class="scb-lo" style="width: 0%"></div>
              <div class="scb-hi" style="width: 0%"></div>
            </div>
            <div class="sc-ctx">Low probability.</div>
            <span class="sc-conf conf-lo">Lo</span>
          </div>
          <div class="sc">
            <div class="sc-name">Fouls</div>
            <div class="sc-nums">
              <span class="sc-lo">20</span><span class="sc-sep">·</span
              ><span class="sc-med">26</span><span class="sc-sep">·</span
              ><span class="sc-hi">32</span>
            </div>
            <div class="sc-bar">
              <div class="scb-lo" style="width: 31%"></div>
              <div class="scb-hi" style="width: 65%"></div>
            </div>
            <div class="sc-ctx">
              Averaging around 13 per team in past meetings.
            </div>
            <span class="sc-conf conf-md">Med</span>
          </div>
          <div class="sc">
            <div class="sc-name">Tackles</div>
            <div class="sc-nums">
              <span class="sc-lo">25</span><span class="sc-sep">·</span
              ><span class="sc-med">31</span><span class="sc-sep">·</span
              ><span class="sc-hi">39</span>
            </div>
            <div class="sc-bar">
              <div class="scb-lo" style="width: 32%"></div>
              <div class="scb-hi" style="width: 63%"></div>
            </div>
            <div class="sc-ctx">Midfield stability is key for both.</div>
            <span class="sc-conf conf-md">Med</span>
          </div>
          <div class="sc">
            <div class="sc-name">Throw-ins</div>
            <div class="sc-nums">
              <span class="sc-lo">30</span><span class="sc-sep">·</span
              ><span class="sc-med">38</span><span class="sc-sep">·</span
              ><span class="sc-hi">45</span>
            </div>
            <div class="sc-bar">
              <div class="scb-lo" style="width: 33%"></div>
              <div class="scb-hi" style="width: 67%"></div>
            </div>
            <div class="sc-ctx">
              Tight tactical play could push the ball wide.
            </div>
            <span class="sc-conf conf-md">Med</span>
          </div>
          <div class="sc">
            <div class="sc-name">Goal Kicks</div>
            <div class="sc-nums">
              <span class="sc-lo">14</span><span class="sc-sep">·</span
              ><span class="sc-med">18</span><span class="sc-sep">·</span
              ><span class="sc-hi">24</span>
            </div>
            <div class="sc-bar">
              <div class="scb-lo" style="width: 29%"></div>
              <div class="scb-hi" style="width: 60%"></div>
            </div>
            <div class="sc-ctx">Standard numbers.</div>
            <span class="sc-conf conf-lo">Lo</span>
          </div>
        </div>
        <div class="fc-ctx">
          <span class="fc-ctx-icon">◆</span>
          <p class="fc-ctx-text">
            <strong>Familiar foes in playoffs</strong>. Poland beat Sweden 2-0
            to reach the 2022 World Cup. Sweden won 3-2 at Euro 2020. This match
            goes back and forth. Sweden playing at home with Viktor Gyökeres in
            peak form gives them a slight edge.
          </p>
        </div>
        <div class="fc-conf">
          <span class="conf-badge cb-md"
            ><span class="conf-dot cd-md"></span>MED confidence</span
          >
          <span class="conf-reason">Home advantage critical · Tight H2H</span>
        </div>
      </div>

      <div class="path-hdr rev">
        <span class="ph-a"
          >International Friendly — England vs Japan · 19:45 BST · Wembley
          Stadium</span
        >
      </div>
      <div class="fc rev">
        <div class="fc-ko">
          <div>
            <span class="ko-t" style="color: var(--cyan)">19:45 BST</span>
            <span class="ko-venue">Wembley Stadium</span>
          </div>
          <span class="ko-badge kb-hi">⚡ High stakes</span>
        </div>
        <div class="fc-top">
          <div class="fc-team">
            <div class="fc-badge">
              <img
                src="https://flagcdn.com/w160/gb-eng.png"
                alt="England"
                loading="lazy"
                style="background-color: #111320"
              />
            </div>
            <div class="fc-info">
              <div class="fc-club">England</div>
              <div class="fc-meta">FIFA 3 · Undefeated H2H</div>
              <div class="form-r">
                <div class="fb fd">D</div>
                <div class="fb fw">W</div>
                <div class="fb fw">W</div>
                <div class="fb fw">W</div>
                <div class="fb fw">W</div>
              </div>
            </div>
          </div>
          <div class="fc-mid">
            <div class="fc-pred-lbl">Predicted</div>
            <div class="fc-pred">2–0</div>
            <div class="fc-odds">ENG 1/2 · JPN 5/1</div>
          </div>
          <div class="fc-team away">
            <div class="fc-badge">
              <img
                src="https://flagcdn.com/w160/jp.png"
                alt="Japan"
                loading="lazy"
                style="background-color: #111320"
              />
            </div>
            <div class="fc-info">
              <div class="fc-club">Japan</div>
              <div class="fc-meta">FIFA ~17 · Technical, fast</div>
              <div class="form-r rv">
                <div class="fb fw">W</div>
                <div class="fb fw">W</div>
                <div class="fb fw">W</div>
                <div class="fb fd">D</div>
                <div class="fb fl">L</div>
              </div>
            </div>
          </div>
        </div>
        <div class="fc-prob">
          <div class="prob-labs">
            <span class="prob-lab">ENG</span
            ><span class="prob-lab">Draw/AET</span
            ><span class="prob-lab">JPN</span>
          </div>
          <div class="prob-bar">
            <div class="pb-h" style="flex: 60"></div>
            <div class="pb-d" style="flex: 25"></div>
            <div class="pb-a" style="flex: 15"></div>
          </div>
          <div class="prob-pcts">
            <span class="pp pp-h">60%</span><span class="pp pp-d">25%</span
            ><span class="pp pp-a">15%</span>
          </div>
        </div>
        <div class="sg">
          <div class="sc">
            <div class="sc-name">Corners</div>
            <div class="sc-nums">
              <span class="sc-lo">6</span><span class="sc-sep">·</span
              ><span class="sc-med">9</span><span class="sc-sep">·</span
              ><span class="sc-hi">12</span>
            </div>
            <div class="sc-bar">
              <div class="scb-lo" style="width: 25%"></div>
              <div class="scb-hi" style="width: 60%"></div>
            </div>
            <div class="sc-ctx">
              Friendlies usually see lower intensity and fewer set pieces.
            </div>
            <span class="sc-conf conf-lo">Lo</span>
          </div>
          <div class="sc">
            <div class="sc-name">Shots on Target</div>
            <div class="sc-nums">
              <span class="sc-lo">7</span><span class="sc-sep">·</span
              ><span class="sc-med">10</span><span class="sc-sep">·</span
              ><span class="sc-hi">14</span>
            </div>
            <div class="sc-bar">
              <div class="scb-lo" style="width: 25%"></div>
              <div class="scb-hi" style="width: 57%"></div>
            </div>
            <div class="sc-ctx">
              England attacks at home. Japan counters effectively.
            </div>
            <span class="sc-conf conf-md">Med</span>
          </div>
          <div class="sc">
            <div class="sc-name">Total Shots</div>
            <div class="sc-nums">
              <span class="sc-lo">17</span><span class="sc-sep">·</span
              ><span class="sc-med">23</span><span class="sc-sep">·</span
              ><span class="sc-hi">29</span>
            </div>
            <div class="sc-bar">
              <div class="scb-lo" style="width: 29%"></div>
              <div class="scb-hi" style="width: 63%"></div>
            </div>
            <div class="sc-ctx">
              Relaxed pace could mean more long-range, speculative efforts.
            </div>
            <span class="sc-conf conf-lo">Lo</span>
          </div>
          <div class="sc">
            <div class="sc-name">Yellow Cards</div>
            <div class="sc-nums">
              <span class="sc-lo">1</span><span class="sc-sep">·</span
              ><span class="sc-med">3</span><span class="sc-sep">·</span
              ><span class="sc-hi">5</span>
            </div>
            <div class="sc-bar">
              <div class="scb-lo" style="width: 10%"></div>
              <div class="scb-hi" style="width: 48%"></div>
            </div>
            <div class="sc-ctx">
              Friendly. Referees lenient. Very low disciplinary expectation.
            </div>
            <span class="sc-conf conf-lo">Lo</span>
          </div>
          <div class="sc">
            <div class="sc-name">Red Cards</div>
            <div class="sc-nums">
              <span class="sc-lo">0</span><span class="sc-sep">·</span
              ><span class="sc-med">0</span><span class="sc-sep">·</span
              ><span class="sc-hi">0</span>
            </div>
            <div class="sc-bar">
              <div class="scb-lo" style="width: 30%"></div>
              <div class="scb-hi" style="width: 70%"></div>
            </div>
            <div class="sc-ctx">Almost zero chance in a friendly format.</div>
            <span class="sc-conf conf-lo">Lo</span>
          </div>
          <div class="sc">
            <div class="sc-name">Fouls</div>
            <div class="sc-nums">
              <span class="sc-lo">14</span><span class="sc-sep">·</span
              ><span class="sc-med">19</span><span class="sc-sep">·</span
              ><span class="sc-hi">24</span>
            </div>
            <div class="sc-bar">
              <div class="scb-lo" style="width: 29%"></div>
              <div class="scb-hi" style="width: 63%"></div>
            </div>
            <div class="sc-ctx">
              Teams will avoid injuries. Low physical engagement.
            </div>
            <span class="sc-conf conf-lo">Lo</span>
          </div>
          <div class="sc">
            <div class="sc-name">Tackles</div>
            <div class="sc-nums">
              <span class="sc-lo">20</span><span class="sc-sep">·</span
              ><span class="sc-med">26</span><span class="sc-sep">·</span
              ><span class="sc-hi">32</span>
            </div>
            <div class="sc-bar">
              <div class="scb-lo" style="width: 31%"></div>
              <div class="scb-hi" style="width: 65%"></div>
            </div>
            <div class="sc-ctx">Space will be allowed.</div>
            <span class="sc-conf conf-lo">Lo</span>
          </div>
          <div class="sc">
            <div class="sc-name">Throw-ins</div>
            <div class="sc-nums">
              <span class="sc-lo">28</span><span class="sc-sep">·</span
              ><span class="sc-med">35</span><span class="sc-sep">·</span
              ><span class="sc-hi">42</span>
            </div>
            <div class="sc-bar">
              <div class="scb-lo" style="width: 33%"></div>
              <div class="scb-hi" style="width: 66%"></div>
            </div>
            <div class="sc-ctx">Lower tempo possession.</div>
            <span class="sc-conf conf-lo">Lo</span>
          </div>
          <div class="sc">
            <div class="sc-name">Goal Kicks</div>
            <div class="sc-nums">
              <span class="sc-lo">13</span><span class="sc-sep">·</span
              ><span class="sc-med">16</span><span class="sc-sep">·</span
              ><span class="sc-hi">21</span>
            </div>
            <div class="sc-bar">
              <div class="scb-lo" style="width: 30%"></div>
              <div class="scb-hi" style="width: 60%"></div>
            </div>
            <div class="sc-ctx">
              Possession will be recycled rather than forced out.
            </div>
            <span class="sc-conf conf-lo">Lo</span>
          </div>
        </div>
        <div class="fc-ctx">
          <span class="fc-ctx-icon">◆</span>
          <p class="fc-ctx-text">
            <strong>England warm-up feature</strong>. England has 2 wins and 1
            draw all-time vs Japan. As this is a friendly, intensity will be far
            lower than the play-offs. Expect heavy rotation from England. Stats
            like cards and fouls should be targeted heavily under the median
            line.
          </p>
        </div>
        <div class="fc-conf">
          <span class="conf-badge cb-md"
            ><span class="conf-dot cd-md"></span>MED confidence</span
          >
          <span class="conf-reason"
            >Friendly match variance · Lower stakes</span
          >
        </div>
      </div>
    </div>
    <!-- /wrap -->

    <footer>
      <div class="ft-l">
        <strong>Team Bilbo Statistical Analysis</strong> WORLD CUP 2026
        QUALIFIER PLAYOFFS · THURSDAY 26 MARCH 2026<br />
        8 UEFA semi-finals · 2 FIFA intercontinental semi-finals<br />
        · Predictions based on Qualifying campaign data, with ·
        <span class="sc-lo">Worst</span> · <span class="sc-med">Median</span> ·
        <span class="sc-hi">Best</span> ranges ·
      </div>
      <div class="ft-r">WC2026 · 5 fixtures</div>
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
          { threshold: 0.04, rootMargin: "0px 0px -10px 0px" },
        );
        els.forEach((el) => ob.observe(el));
      })();
    </script>
  </body>
</html>
