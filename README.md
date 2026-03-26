<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width,initial-scale=1.0" />
    <title>World Cup 2026 Qualifiers · 26 March 2026 · All Fixtures</title>
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
        font-size: 18px;
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
        font-size: 12px;
        letter-spacing: 0.1em;
        text-transform: uppercase;
        color: var(--fg3);
      }
      .hdr-count {
        font-family: "JetBrains Mono", monospace;
        font-size: 10px;
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
        font-size: 12px;
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
        font-size: 12px;
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
        font-size: 11px;
        font-weight: 700;
        color: var(--fg);
        line-height: 1.3;
      }
      .fgi-conf {
        font-family: "JetBrains Mono", monospace;
        font-size: 8px;
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
        font-size: 8px;
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
        font-size: 12px;
        letter-spacing: 0.1em;
        text-transform: uppercase;
        font-weight: 600;
      }
      .ko-venue {
        font-family: "JetBrains Mono", monospace;
        font-size: 12px;
        color: var(--fg3);
        text-overflow: ellipsis;
        overflow: hidden;
        white-space: nowrap;
      }
      .ko-badge {
        font-family: "JetBrains Mono", monospace;
        font-size: 12px;
        font-weight: 700;
        padding: 3px 8px;
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
        gap: 8px;
        padding: 14px var(--px) 12px;
        }
        /* both home and away: flag above name, centered */
        .fc-team {
          display: flex;
          flex-direction: column;
          align-items: center;
          text-align: center;
          gap: 8px;

      }
      .fc-team.away {
        flex-direction: column;
        text-align: center;
      }
      .fc-badge {
        width: 36px;
        height: 36px;
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
        font-size: clamp(14px, 3.5vw, 19px);
        font-weight: 700;
        letter-spacing: -0.01em;
        color: var(--fg);
        line-height: 1.1;
      }
      .fc-meta {
        font-family: "JetBrains Mono", monospace;
        font-size: 10px;
        letter-spacing: 0.05em;
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
        width: 16px;
        height: 16px;
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
        font-size: clamp(26px, 6.5vw, 38px);
        font-weight: 900;
        letter-spacing: 0.02em;
        line-height: 1;
        color: var(--gold);
        white-space: nowrap;
      }
      .fc-odds {
        font-family: "JetBrains Mono", monospace;
        font-size: 10px;
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
        font-size: 7px;
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
        font-size: 14px;
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
        font-size: 8px;
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
        font-size: 12px;
        color: var(--fg3);
      }
      .sc-med {
        font-size: 16px;
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
        line-height: 1.4;
      }
      .sc-conf {
        font-family: "JetBrains Mono", monospace;
        font-size: 11px;
        font-weight: 700;
        padding: 1px 5px;
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
        font-size: 12px;
        flex-shrink: 0;
        margin-top: 1px;
      }
      .fc-ctx-text {
        font-size: 11px;
        color: var(--fg2);
        line-height: 1.65;
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
        font-size: 12px;
        font-weight: 700;
        padding: 4px 10px;
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
        font-size: 12px;
        color: var(--fg2);
        line-height: 1.4;
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
        font-size: 12px;
        color: var(--fg3);
        letter-spacing: 0.05em;
        line-height: 2;
      }
      .ft-r {
        font-family: "JetBrains Mono", monospace;
        font-size: 11px;
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
      @media (max-width: 479px) {
        /* bump base size for the whole page */
        html {
          font-size: 14px;
        }

        /* stack the team grid so each team gets more room */
        .fc-top {
          grid-template-columns: 1fr auto 1fr;
          padding: 14px 10px 12px;
          gap: 6px;
        }
        /* both home and away: flag above name, centered */
        .fc-team {
          flex-direction: column !important;
          align-items: center !important;
          text-align: center;
          gap: 6px;
        }
        .fc-team.away .fc-info {
          align-items: center;
        }
        /* centre the form row for the away team too */
        .form-r,
        .form-r.rv {
          justify-content: center;
        }

        /* slightly larger badges so flags are legible */
        .fc-badge {
          width: 40px;
          height: 40px;
        }

        /* ── Font clarity — aggressive bumps ── */
        .fc-club {
          font-size: 16px;
        }
        .fc-meta {
          font-size: 10px;
          letter-spacing: 0.03em;
        }
        .fc-pred-lbl {
          font-size: 12px;
        }
        .fc-pred {
          font-size: clamp(28px, 7vw, 40px);
        }
        .fc-odds {
          font-size: 11px;
        }

        /* KO row */
        .ko-t {
          font-size: 11px;
        }
        .ko-venue {
          font-size: 11px;
        }
        .ko-badge {
          font-size: 10px;
          padding: 4px 10px;
        }

        /* probability bar */
        .prob-lab {
          font-size: 10px;
        }
        .pp {
          font-size: 15px;
        }

        /* stat cards */
        .sc-name {
          font-size: 11px;
        }
        .sc-lo,
        .sc-hi {
          font-size: 13px;
        }
        .sc-med {
          font-size: 18px;
        }
        .sc-sep {
          font-size: 11px;
        }
        .sc-ctx {
          font-size: 11px;
          line-height: 1.5;
        }
        .sc-conf {
          font-size: 12px;
          padding: 2px 7px;
        }

        /* context strip */
        .fc-ctx-text {
          font-size: 13px;
          line-height: 1.7;
        }
        .fc-ctx-icon {
          font-size: 11px;
        }

        /* confidence row */
        .conf-badge {
          font-size: 11px;
          padding: 5px 12px;
        }
        .conf-reason {
          font-size: 11px;
          line-height: 1.5;
        }

        /* form badges */
        .fb {
          width: 18px;
          height: 18px;
          font-size: 12px;
        }

        /* hero section */
        .hero-eye {
          font-size: 11px;
        }
        .hero-sub {
          font-size: 11px;
        }

        /* header */
        .hdr-brand {
          font-size: 14px;
        }
        .hdr-info {
          font-size: 11px;
        }
        .hdr-count {
          font-size: 11px;
        }

        /* path divider */
        .path-hdr {
          font-size: 11px;
        }

        /* legend */
        .leg {
          font-size: 10px;
        }

        /* fixture grid */
        .fgi-ko {
          font-size: 10px;
        }
        .fgi-match {
          font-size: 13px;
        }
        .fgi-conf {
          font-size: 10px;
        }

        /* footer */
        .ft-l {
          font-size: 10px;
        }
        .ft-r {
          font-size: 12px;
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
        <div class="hdr-count">10 fixtures</div>
      </div>
    </header>

    <!-- HERO -->
    <section class="hero rev">
      <div class="hero-inner">
        <div class="hero-eye">World Cup 2026 Qualifier Play-offs</div>
        <h1 class="hero-h1">Thursday<br /><span>26 March</span></h1>
        <p class="hero-sub">
          8 UEFA semi-finals · 2 FIFA intercontinental semi-finals · Best /
          Median / Worst stat ranges
        </p>
        <div class="fixture-grid">
          <div class="fg-item">
            <div class="fgi-ko">17:00 · Path C</div>
            <div class="fgi-match">Türkiye vs Romania</div>
          </div>
          <div class="fg-item">
            <div class="fgi-ko">19:45 · Path A</div>
            <div class="fgi-match">Italy vs N.Ireland</div>
          </div>
          <div class="fg-item">
            <div class="fgi-ko">19:45 · Path A</div>
            <div class="fgi-match">Wales vs Bosnia</div>
          </div>
          <div class="fg-item">
            <div class="fgi-ko">19:45 · Path B</div>
            <div class="fgi-match">Ukraine vs Sweden</div>
          </div>
          <div class="fg-item">
            <div class="fgi-ko">19:45 · Path B</div>
            <div class="fgi-match">Poland vs Albania</div>
          </div>
          <div class="fg-item">
            <div class="fgi-ko">19:45 · Path C</div>
            <div class="fgi-match">Slovakia vs Kosovo</div>
          </div>
          <div class="fg-item">
            <div class="fgi-ko">19:45 · Path D</div>
            <div class="fgi-match">Denmark vs N.Mac</div>
          </div>
          <div class="fg-item">
            <div class="fgi-ko">19:45 · Path D</div>
            <div class="fgi-match">Czechia vs Ireland</div>
          </div>
          <div class="fg-item">
            <div class="fgi-ko">03:00 · FIFA IC</div>
            <div class="fgi-match">New Cal. vs Jamaica</div>
          </div>
          <div class="fg-item">
            <div class="fgi-ko">23:00 · FIFA IC</div>
            <div class="fgi-match">Bolivia vs Suriname</div>
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

      <!-- ══════════ PATH A ══════════ -->
      <div class="path-hdr rev">
        <span class="ph-a"
          >Path A — Italy vs Northern Ireland · 19:45 GMT · Bergamo (New Balance
          Arena)</span
        >
      </div>

      <div class="fc rev">
        <div class="fc-ko">
          <div>
            <span class="ko-t" style="color: var(--cyan)">19:45 GMT</span>
            <span class="ko-venue"
              >New Balance Arena</span
            >
          </div>
          <span class="ko-badge kb-hi">⚡ High stakes</span>
        </div>
        <div class="fc-top">
          <div class="fc-team">
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
              <div class="fc-meta">
                FIFA 9 · 6.6 corners/g · 57% poss avg · Gattuso
              </div>
              <div class="form-r">
                <div class="fb fl">L</div>
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
            <div class="fc-odds">ITA 2/7 · NI 10/1</div>
          </div>
          <div class="fc-team away">
            <div class="fc-badge">
              <img
                src="https://flagcdn.com/w160/gb-nir.png"
                alt="Northern Ireland"
                loading="lazy"
                style="background-color: #111320"
              />
            </div>
            <div class="fc-info">
              <div class="fc-club">N. Ireland</div>
              <div class="fc-meta">
                FIFA 69 · 5.3 corners/g · 36.7% poss avg · O'Neill
              </div>
              <div class="form-r rv">
                <div class="fb fw">W</div>
                <div class="fb fl">L</div>
                <div class="fb fl">L</div>
                <div class="fb fw">W</div>
                <div class="fb fl">L</div>
              </div>
            </div>
          </div>
        </div>
        <div class="fc-prob">
          <div class="prob-labs">
            <span class="prob-lab">Italy</span
            ><span class="prob-lab">Draw/AET</span
            ><span class="prob-lab">N. Ireland</span>
          </div>
          <div class="prob-bar">
            <div class="pb-h" style="flex: 72"></div>
            <div class="pb-d" style="flex: 16"></div>
            <div class="pb-a" style="flex: 12"></div>
          </div>
          <div class="prob-pcts">
            <span class="pp pp-h">72%</span><span class="pp pp-d">16%</span
            ><span class="pp pp-a">12%</span>
          </div>
        </div>
        <div class="sg">
          <div class="sc">
            <div class="sc-name">Corners</div>
            <div class="sc-nums">
              <span class="sc-lo">5</span><span class="sc-sep">·</span
              ><span class="sc-med">9</span><span class="sc-sep">·</span
              ><span class="sc-hi">14</span>
            </div>
            <div class="sc-bar">
              <div class="scb-lo" style="width: 36%"></div>
              <div class="scb-hi" style="width: 72%"></div>
            </div>
            <div class="sc-ctx">
              Italy 6.6/g avg · NI suppress to U9.5 in 6/7 games · Italy 56
              corners in qual
            </div>
            <span class="sc-conf conf-hi">Hi</span>
          </div>
          <div class="sc">
            <div class="sc-name">Shots on Target</div>
            <div class="sc-nums">
              <span class="sc-lo">4</span><span class="sc-sep">·</span
              ><span class="sc-med">7</span><span class="sc-sep">·</span
              ><span class="sc-hi">11</span>
            </div>
            <div class="sc-bar">
              <div class="scb-lo" style="width: 36%"></div>
              <div class="scb-hi" style="width: 68%"></div>
            </div>
            <div class="sc-ctx">
              Italy 6.3 SoT/g · NI concede 2.3 SoT/g · NI limit big chances well
            </div>
            <span class="sc-conf conf-hi">Hi</span>
          </div>
          <div class="sc">
            <div class="sc-name">Fouls</div>
            <div class="sc-nums">
              <span class="sc-lo">16</span><span class="sc-sep">·</span
              ><span class="sc-med">22</span><span class="sc-sep">·</span
              ><span class="sc-hi">30</span>
            </div>
            <div class="sc-bar">
              <div class="scb-lo" style="width: 46%"></div>
              <div class="scb-hi" style="width: 72%"></div>
            </div>
            <div class="sc-ctx">
              NI physical — 7 fouls from Hume alone in recent qualifiers · Italy
              18.7 SH avg · high-stakes = more
            </div>
            <span class="sc-conf conf-hi">Hi</span>
          </div>
          <div class="sc">
            <div class="sc-name">Total Shots</div>
            <div class="sc-nums">
              <span class="sc-lo">14</span><span class="sc-sep">·</span
              ><span class="sc-med">22</span><span class="sc-sep">·</span
              ><span class="sc-hi">30</span>
            </div>
            <div class="sc-bar">
              <div class="scb-lo" style="width: 48%"></div>
              <div class="scb-hi" style="width: 74%"></div>
            </div>
            <div class="sc-ctx">
              Italy 18.7 att/g · NI 8.8 att/g · Italy dominant possession — NI
              likely to absorb
            </div>
            <span class="sc-conf conf-hi">Hi</span>
          </div>
          <div class="sc">
            <div class="sc-name">Throw-ins</div>
            <div class="sc-nums">
              <span class="sc-lo">28</span><span class="sc-sep">·</span
              ><span class="sc-med">36</span><span class="sc-sep">·</span
              ><span class="sc-hi">46</span>
            </div>
            <div class="sc-bar">
              <div class="scb-lo" style="width: 44%"></div>
              <div class="scb-hi" style="width: 66%"></div>
            </div>
            <div class="sc-ctx">
              NI deep block → lots of sideline play · Italy's wide attacks via
              Dimarco, Bellanova
            </div>
            <span class="sc-conf conf-md">Med</span>
          </div>
          <div class="sc">
            <div class="sc-name">Goal Kicks</div>
            <div class="sc-nums">
              <span class="sc-lo">12</span><span class="sc-sep">·</span
              ><span class="sc-med">18</span><span class="sc-sep">·</span
              ><span class="sc-hi">26</span>
            </div>
            <div class="sc-bar">
              <div class="scb-lo" style="width: 38%"></div>
              <div class="scb-hi" style="width: 62%"></div>
            </div>
            <div class="sc-ctx">
              NI GK launches long · Italy build out · Donnarumma short from back
              · NI GK = high volume
            </div>
            <span class="sc-conf conf-md">Med</span>
          </div>
          <div class="sc">
            <div class="sc-name">Tackles</div>
            <div class="sc-nums">
              <span class="sc-lo">22</span><span class="sc-sep">·</span
              ><span class="sc-med">30</span><span class="sc-sep">·</span
              ><span class="sc-hi">40</span>
            </div>
            <div class="sc-bar">
              <div class="scb-lo" style="width: 50%"></div>
              <div class="scb-hi" style="width: 74%"></div>
            </div>
            <div class="sc-ctx">
              NI 111 tackles in qual (high) · Italy press less with lead ·
              playoff desperation = peak effort
            </div>
            <span class="sc-conf conf-hi">Hi</span>
          </div>
        </div>
        <div class="fc-ctx">
          <span class="fc-ctx-icon">◆</span>
          <p class="fc-ctx-text">
            <strong>Italy have NEVER conceded vs Northern Ireland</strong> (5W
            2D — 0 goals against since 1958).
            <span class="cc-r"
              >Chiesa OUT, Scamacca OUT, Tonali/Mancini doubts</span
            >. NI missing
            <span class="cc-r">Conor Bradley AND Dan Ballard</span> — two
            starters. <span class="cc-c">Italy 2-7 to win.</span> Retegui (5g,
            4a in qual) is the key threat. NI organised but under-resourced
            going forward — only 7 goals in 6 qualifiers. Expect patient Italy
            possession, NI low block, late goals.
          </p>
        </div>
        <div class="fc-conf">
          <span class="conf-badge cb-hi"
            ><span class="conf-dot cd-hi"></span>HIGH confidence — Italy
            win</span
          >
          <span class="conf-reason"
            >Italy 72% win prob · never lost vs NI · NI missing Bradley +
            Ballard · Italy 6W in L7</span
          >
        </div>
      </div>

      <!-- ══ PATH A: WALES vs BOSNIA ══ -->
      <div class="path-hdr rev">
        <span class="ph-a"
          >Path A — Wales vs Bosnia-Herzegovina · 19:45 GMT · Cardiff City
          Stadium</span
        >
      </div>
      <div class="fc rev">
        <div class="fc-ko">
          <div>
            <span class="ko-t" style="color: var(--cyan)">19:45 GMT</span>
            <span class="ko-venue">Cardiff City Stadium</span>
          </div>
          <span class="ko-badge kb-hi">⚡ High stakes</span>
        </div>
        <div class="fc-top">
          <div class="fc-team">
            <div class="fc-badge">
              <img
                src="https://flagcdn.com/w160/gb-wls.png"
                alt="Wales"
                loading="lazy"
                style="background-color: #111320"
              />
            </div>
            <div class="fc-info">
              <div class="fc-club">Wales</div>
              <div class="fc-meta">
                FIFA 34 · 2.6 goals/g in qual · Wilson 5g · Bellamy
              </div>
              <div class="form-r">
                <div class="fb fw">W</div>
                <div class="fb fw">W</div>
                <div class="fb fd">D</div>
                <div class="fb fw">W</div>
                <div class="fb fw">W</div>
              </div>
            </div>
          </div>
          <div class="fc-mid">
            <div class="fc-pred-lbl">Predicted</div>
            <div class="fc-pred">2–1</div>
            <div class="fc-odds">WAL slight fav · evens</div>
          </div>
          <div class="fc-team away">
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
              <div class="fc-meta">
                FIFA 75 · 2.1 goals/g · Dzeko 40 (5g) · Barbarez
              </div>
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
            <span class="prob-lab">Wales</span
            ><span class="prob-lab">Draw/AET</span
            ><span class="prob-lab">Bosnia</span>
          </div>
          <div class="prob-bar">
            <div class="pb-h" style="flex: 42"></div>
            <div class="pb-d" style="flex: 28"></div>
            <div class="pb-a" style="flex: 30"></div>
          </div>
          <div class="prob-pcts">
            <span class="pp pp-h">42%</span><span class="pp pp-d">28%</span
            ><span class="pp pp-a">30%</span>
          </div>
        </div>
        <div class="sg">
          <div class="sc">
            <div class="sc-name">Corners</div>
            <div class="sc-nums">
              <span class="sc-lo">7</span><span class="sc-sep">·</span
              ><span class="sc-med">11</span><span class="sc-sep">·</span
              ><span class="sc-hi">16</span>
            </div>
            <div class="sc-bar">
              <div class="scb-lo" style="width: 44%"></div>
              <div class="scb-hi" style="width: 78%"></div>
            </div>
            <div class="sc-ctx">
              Wales 2.6 goals/g → attacking → many corners · Bosnia 0.88 GA/g
              well-organised · both attack wide
            </div>
            <span class="sc-conf conf-hi">Hi</span>
          </div>
          <div class="sc">
            <div class="sc-name">Shots on Target</div>
            <div class="sc-nums">
              <span class="sc-lo">5</span><span class="sc-sep">·</span
              ><span class="sc-med">8</span><span class="sc-sep">·</span
              ><span class="sc-hi">13</span>
            </div>
            <div class="sc-bar">
              <div class="scb-lo" style="width: 38%"></div>
              <div class="scb-hi" style="width: 68%"></div>
            </div>
            <div class="sc-ctx">
              Wales 3.8 SoT/g · Bosnia 2.3 SoT/g conceded · Wilson in
              double-digit PL goals — quality striking
            </div>
            <span class="sc-conf conf-hi">Hi</span>
          </div>
          <div class="sc">
            <div class="sc-name">Fouls</div>
            <div class="sc-nums">
              <span class="sc-lo">18</span><span class="sc-sep">·</span
              ><span class="sc-med">25</span><span class="sc-sep">·</span
              ><span class="sc-hi">34</span>
            </div>
            <div class="sc-bar">
              <div class="scb-lo" style="width: 46%"></div>
              <div class="scb-hi" style="width: 72%"></div>
            </div>
            <div class="sc-ctx">
              Katic 6 bookings at Schalke + 2 in qual · physical contest ·
              Cardiff hostile atmosphere amps up fouls
            </div>
            <span class="sc-conf conf-hi">Hi</span>
          </div>
          <div class="sc">
            <div class="sc-name">Total Shots</div>
            <div class="sc-nums">
              <span class="sc-lo">18</span><span class="sc-sep">·</span
              ><span class="sc-med">26</span><span class="sc-sep">·</span
              ><span class="sc-hi">36</span>
            </div>
            <div class="sc-bar">
              <div class="scb-lo" style="width: 50%"></div>
              <div class="scb-hi" style="width: 78%"></div>
            </div>
            <div class="sc-ctx">
              Wales 7-1 vs N.Macedonia shows high attack intent at home · Bosnia
              also not shy in front of goal
            </div>
            <span class="sc-conf conf-hi">Hi</span>
          </div>
          <div class="sc">
            <div class="sc-name">Throw-ins</div>
            <div class="sc-nums">
              <span class="sc-lo">30</span><span class="sc-sep">·</span
              ><span class="sc-med">40</span><span class="sc-sep">·</span
              ><span class="sc-hi">52</span>
            </div>
            <div class="sc-bar">
              <div class="scb-lo" style="width: 48%"></div>
              <div class="scb-hi" style="width: 72%"></div>
            </div>
            <div class="sc-ctx">
              Cardiff City Stadium wide pitch · both teams physical duels on
              touchline · high energy game
            </div>
            <span class="sc-conf conf-md">Med</span>
          </div>
          <div class="sc">
            <div class="sc-name">Goal Kicks</div>
            <div class="sc-nums">
              <span class="sc-lo">12</span><span class="sc-sep">·</span
              ><span class="sc-med">18</span><span class="sc-sep">·</span
              ><span class="sc-hi">26</span>
            </div>
            <div class="sc-bar">
              <div class="scb-lo" style="width: 38%"></div>
              <div class="scb-hi" style="width: 62%"></div>
            </div>
            <div class="sc-ctx">
              Darlow plays out from back · Vasilj long kick tendency · Bosnia
              forced back → many GKs for Vasilj
            </div>
            <span class="sc-conf conf-md">Med</span>
          </div>
          <div class="sc">
            <div class="sc-name">Tackles</div>
            <div class="sc-nums">
              <span class="sc-lo">24</span><span class="sc-sep">·</span
              ><span class="sc-med">34</span><span class="sc-sep">·</span
              ><span class="sc-hi">46</span>
            </div>
            <div class="sc-bar">
              <div class="scb-lo" style="width: 50%"></div>
              <div class="scb-hi" style="width: 78%"></div>
            </div>
            <div class="sc-ctx">
              Both physically combative · Ampadu + Dzeko midfield battle · huge
              stakes = max effort
            </div>
            <span class="sc-conf conf-hi">Hi</span>
          </div>
        </div>
        <div class="fc-ctx">
          <span class="fc-ctx-icon">◆</span>
          <p class="fc-ctx-text">
            <strong>Wales have never beaten Bosnia-Herzegovina</strong> (D2 L2
            historically).
            <span class="cc-r"
              >Ben Davies OUT (ankle), Kieffer Moore OUT (injury)</span
            >. But
            <span class="cc-c"
              >Cardiff home form: 5W in last 6 competitive home games</span
            >. Bosnia unbeaten in their last 4 away.
            <span class="cc-g"
              >Harry Wilson: 5g in 5 qualifiers, 10 PL goals, scored in last 3
              for Fulham.</span
            >
            <span class="cc-o"
              >Bosnia's playoff record: 0W in 7 attempts in 4 campaigns —
              historic psychological baggage.</span
            >
            Dzeko at 40 could be decisive or limited. Expect goals — BTTS
            likely. AET real possibility.
          </p>
        </div>
        <div class="fc-conf">
          <span class="conf-badge cb-md"
            ><span class="conf-dot cd-md"></span>MED confidence — Wales
            edge</span
          >
          <span class="conf-reason"
            >42% Wales · Bosnia never won a playoff · Cardiff fortress · but
            Bosnia excellent away record</span
          >
        </div>
      </div>

      <!-- ══ PATH B: UKRAINE vs SWEDEN ══ -->
      <div class="path-hdr rev">
        <span class="ph-b"
          >Path B — Ukraine vs Sweden · 19:45 GMT · Estadi Ciutat de
          València</span
        >
      </div>
      <div class="fc rev">
        <div class="fc-ko">
          <div>
            <span class="ko-t" style="color: var(--green)">19:45 GMT</span>
            <span class="ko-venue"
              >Estadi Ciutat de València · Neutral venue</span
            >
          </div>
          <span class="ko-badge kb-hi">⚡ Neutral venue</span>
        </div>
        <div class="fc-top">
          <div class="fc-team">
            <div class="fc-badge">
              <img
                src="https://flagcdn.com/w160/ua.png"
                alt="Ukraine"
                loading="lazy"
                style="background-color: #111320"
              />
            </div>
            <div class="fc-info">
              <div class="fc-club">Ukraine</div>
              <div class="fc-meta">
                FIFA 27 · Rebrov · 20-yr WC absence · play at neutral venues
              </div>
              <div class="form-r">
                <div class="fb fw">W</div>
                <div class="fb fw">W</div>
                <div class="fb fw">W</div>
                <div class="fb fl">L</div>
                <div class="fb fd">D</div>
              </div>
            </div>
          </div>
          <div class="fc-mid">
            <div class="fc-pred-lbl">Predicted</div>
            <div class="fc-pred">2–1</div>
            <div class="fc-odds">UKR fav · AET poss</div>
          </div>
          <div class="fc-team away">
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
              <div class="fc-meta">
                FIFA 40 · Gyokeres (Arsenal) leading · NL route
              </div>
              <div class="form-r rv">
                <div class="fb fl">L</div>
                <div class="fb fl">L</div>
                <div class="fb fl">L</div>
                <div class="fb fl">L</div>
                <div class="fb fd">D</div>
              </div>
            </div>
          </div>
        </div>
        <div class="fc-prob">
          <div class="prob-labs">
            <span class="prob-lab">Ukraine</span
            ><span class="prob-lab">Draw/AET</span
            ><span class="prob-lab">Sweden</span>
          </div>
          <div class="prob-bar">
            <div class="pb-h" style="flex: 52"></div>
            <div class="pb-d" style="flex: 26"></div>
            <div class="pb-a" style="flex: 22"></div>
          </div>
          <div class="prob-pcts">
            <span class="pp pp-h">52%</span><span class="pp pp-d">26%</span
            ><span class="pp pp-a">22%</span>
          </div>
        </div>
        <div class="sg">
          <div class="sc">
            <div class="sc-name">Corners</div>
            <div class="sc-nums">
              <span class="sc-lo">5</span><span class="sc-sep">·</span
              ><span class="sc-med">9</span><span class="sc-sep">·</span
              ><span class="sc-hi">14</span>
            </div>
            <div class="sc-bar">
              <div class="scb-lo" style="width: 36%"></div>
              <div class="scb-hi" style="width: 68%"></div>
            </div>
            <div class="sc-ctx">
              Sweden 0W in qual group · defensive → fewer corners against ·
              Ukraine attacks wide with Mudryk/Tsygankov
            </div>
            <span class="sc-conf conf-md">Med</span>
          </div>
          <div class="sc">
            <div class="sc-name">Shots on Target</div>
            <div class="sc-nums">
              <span class="sc-lo">4</span><span class="sc-sep">·</span
              ><span class="sc-med">7</span><span class="sc-sep">·</span
              ><span class="sc-hi">11</span>
            </div>
            <div class="sc-bar">
              <div class="scb-lo" style="width: 36%"></div>
              <div class="scb-hi" style="width: 66%"></div>
            </div>
            <div class="sc-ctx">
              Gyokeres 21 Arsenal goals this season · Ukraine solid defensive +
              attacking transition team
            </div>
            <span class="sc-conf conf-md">Med</span>
          </div>
          <div class="sc">
            <div class="sc-name">Fouls</div>
            <div class="sc-nums">
              <span class="sc-lo">16</span><span class="sc-sep">·</span
              ><span class="sc-med">22</span><span class="sc-sep">·</span
              ><span class="sc-hi">30</span>
            </div>
            <div class="sc-bar">
              <div class="scb-lo" style="width: 44%"></div>
              <div class="scb-hi" style="width: 68%"></div>
            </div>
            <div class="sc-ctx">
              Neutral venue removes crowd noise factor · both combative nations
              · WC desperation = physical game
            </div>
            <span class="sc-conf conf-md">Med</span>
          </div>
          <div class="sc">
            <div class="sc-name">Total Shots</div>
            <div class="sc-nums">
              <span class="sc-lo">14</span><span class="sc-sep">·</span
              ><span class="sc-med">22</span><span class="sc-sep">·</span
              ><span class="sc-hi">30</span>
            </div>
            <div class="sc-bar">
              <div class="scb-lo" style="width: 44%"></div>
              <div class="scb-hi" style="width: 72%"></div>
            </div>
            <div class="sc-ctx">
              Gyokeres + Isak for Sweden v Ukraine's Dovbyk-led attack · both
              teams can score
            </div>
            <span class="sc-conf conf-md">Med</span>
          </div>
          <div class="sc">
            <div class="sc-name">Throw-ins</div>
            <div class="sc-nums">
              <span class="sc-lo">28</span><span class="sc-sep">·</span
              ><span class="sc-med">36</span><span class="sc-sep">·</span
              ><span class="sc-hi">46</span>
            </div>
            <div class="sc-bar">
              <div class="scb-lo" style="width: 42%"></div>
              <div class="scb-hi" style="width: 64%"></div>
            </div>
            <div class="sc-ctx">
              Neutral venue pitch — Valencia stadium wide · both teams mid-block
              style = sideline battles
            </div>
            <span class="sc-conf conf-md">Med</span>
          </div>
          <div class="sc">
            <div class="sc-name">Goal Kicks</div>
            <div class="sc-nums">
              <span class="sc-lo">10</span><span class="sc-sep">·</span
              ><span class="sc-med">16</span><span class="sc-sep">·</span
              ><span class="sc-hi">24</span>
            </div>
            <div class="sc-bar">
              <div class="scb-lo" style="width: 36%"></div>
              <div class="scb-hi" style="width: 60%"></div>
            </div>
            <div class="sc-ctx">
              Both play moderate build-up · Sweden likely to launch long vs
              Ukraine press · moderate GK volume
            </div>
            <span class="sc-conf conf-lo">Low</span>
          </div>
          <div class="sc">
            <div class="sc-name">Tackles</div>
            <div class="sc-nums">
              <span class="sc-lo">22</span><span class="sc-sep">·</span
              ><span class="sc-med">30</span><span class="sc-sep">·</span
              ><span class="sc-hi">40</span>
            </div>
            <div class="sc-bar">
              <div class="scb-lo" style="width: 48%"></div>
              <div class="scb-hi" style="width: 72%"></div>
            </div>
            <div class="sc-ctx">
              Ukraine's 20-year WC absence = maximum effort · Sweden not
              motivated from Nations League route
            </div>
            <span class="sc-conf conf-md">Med</span>
          </div>
        </div>
        <div class="fc-ctx">
          <span class="fc-ctx-icon">◆</span>
          <p class="fc-ctx-text">
            <strong>Ukraine last appeared at the World Cup in 2006.</strong>
            Playing at a neutral venue in Valencia adds unpredictability.
            <span class="cc-c"
              >Sweden qualified via Nations League despite 0 wins in their
              qualifying group</span
            >
            — unusual.
            <span class="cc-g"
              >Gyokeres (Arsenal) is Sweden's superstar — 21 goals this
              season.</span
            >
            Ukraine's motivation (a war-torn nation) is uniquely high.
            <span class="cc-r">Sweden winless in qualifying was alarming</span>
            but their NL form was better. Expect Ukraine to control and win
            narrowly.
          </p>
        </div>
        <div class="fc-conf">
          <span class="conf-badge cb-md"
            ><span class="conf-dot cd-md"></span>MED confidence — Ukraine</span
          >
          <span class="conf-reason"
            >52% Ukraine · Sweden 0W in qual · Gyokeres = wildcard · neutral
            venue balances things</span
          >
        </div>
      </div>

      <!-- ══ PATH B: POLAND vs ALBANIA ══ -->
      <div class="path-hdr rev">
        <span class="ph-b"
          >Path B — Poland vs Albania · 19:45 GMT · PGE Narodowy, Warsaw</span
        >
      </div>
      <div class="fc rev">
        <div class="fc-ko">
          <div>
            <span class="ko-t" style="color: var(--green)">19:45 GMT</span>
            <span class="ko-venue"
              >PGE Narodowy</span
            >
          </div>
          <span class="ko-badge kb-hi">⚡ High stakes</span>
        </div>
        <div class="fc-top">
          <div class="fc-team">
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
              <div class="fc-meta">
                FIFA 33 · Group B 2nd · Lewandowski leads attack
              </div>
              <div class="form-r">
                <div class="fb fw">W</div>
                <div class="fb fw">W</div>
                <div class="fb fw">W</div>
                <div class="fb fd">D</div>
                <div class="fb fw">W</div>
              </div>
            </div>
          </div>
          <div class="fc-mid">
            <div class="fc-pred-lbl">Predicted</div>
            <div class="fc-pred">2–0</div>
            <div class="fc-odds">POL 1/2 fav</div>
          </div>
          <div class="fc-team away">
            <div class="fc-badge">
              <img
                src="https://flagcdn.com/w160/al.png"
                alt="Albania"
                loading="lazy"
                style="background-color: #111320"
              />
            </div>
            <div class="fc-info">
              <div class="fc-club">Albania</div>
              <div class="fc-meta">
                FIFA 61 · Group K runners-up behind England
              </div>
              <div class="form-r rv">
                <div class="fb fw">W</div>
                <div class="fb fl">L</div>
                <div class="fb fw">W</div>
                <div class="fb fw">W</div>
                <div class="fb fl">L</div>
              </div>
            </div>
          </div>
        </div>
        <div class="fc-prob">
          <div class="prob-labs">
            <span class="prob-lab">Poland</span
            ><span class="prob-lab">Draw/AET</span
            ><span class="prob-lab">Albania</span>
          </div>
          <div class="prob-bar">
            <div class="pb-h" style="flex: 62"></div>
            <div class="pb-d" style="flex: 22"></div>
            <div class="pb-a" style="flex: 16"></div>
          </div>
          <div class="prob-pcts">
            <span class="pp pp-h">62%</span><span class="pp pp-d">22%</span
            ><span class="pp pp-a">16%</span>
          </div>
        </div>
        <div class="sg">
          <div class="sc">
            <div class="sc-name">Corners</div>
            <div class="sc-nums">
              <span class="sc-lo">6</span><span class="sc-sep">·</span
              ><span class="sc-med">10</span><span class="sc-sep">·</span
              ><span class="sc-hi">15</span>
            </div>
            <div class="sc-bar">
              <div class="scb-lo" style="width: 40%"></div>
              <div class="scb-hi" style="width: 72%"></div>
            </div>
            <div class="sc-ctx">
              Poland dominant possession at home → many corners · Albania likely
              to defend deep + concede set pieces
            </div>
            <span class="sc-conf conf-hi">Hi</span>
          </div>
          <div class="sc">
            <div class="sc-name">Shots on Target</div>
            <div class="sc-nums">
              <span class="sc-lo">4</span><span class="sc-sep">·</span
              ><span class="sc-med">8</span><span class="sc-sep">·</span
              ><span class="sc-hi">12</span>
            </div>
            <div class="sc-bar">
              <div class="scb-lo" style="width: 36%"></div>
              <div class="scb-hi" style="width: 68%"></div>
            </div>
            <div class="sc-ctx">
              Lewandowski led all Poland scorers in qual · Albania conceded
              regularly vs top sides
            </div>
            <span class="sc-conf conf-hi">Hi</span>
          </div>
          <div class="sc">
            <div class="sc-name">Fouls</div>
            <div class="sc-nums">
              <span class="sc-lo">16</span><span class="sc-sep">·</span
              ><span class="sc-med">22</span><span class="sc-sep">·</span
              ><span class="sc-hi">30</span>
            </div>
            <div class="sc-bar">
              <div class="scb-lo" style="width: 44%"></div>
              <div class="scb-hi" style="width: 68%"></div>
            </div>
            <div class="sc-ctx">
              Albania foul to stop Polish fast breaks · Warsaw 58,000 crowd
              raises intensity · physical qualifier
            </div>
            <span class="sc-conf conf-hi">Hi</span>
          </div>
          <div class="sc">
            <div class="sc-name">Total Shots</div>
            <div class="sc-nums">
              <span class="sc-lo">16</span><span class="sc-sep">·</span
              ><span class="sc-med">24</span><span class="sc-sep">·</span
              ><span class="sc-hi">32</span>
            </div>
            <div class="sc-bar">
              <div class="scb-lo" style="width: 50%"></div>
              <div class="scb-hi" style="width: 76%"></div>
            </div>
            <div class="sc-ctx">
              Poland attacking depth — Lewandowski + Szymanski + Zielinski ·
              Albania defending expected
            </div>
            <span class="sc-conf conf-hi">Hi</span>
          </div>
          <div class="sc">
            <div class="sc-name">Throw-ins</div>
            <div class="sc-nums">
              <span class="sc-lo">28</span><span class="sc-sep">·</span
              ><span class="sc-med">38</span><span class="sc-sep">·</span
              ><span class="sc-hi">48</span>
            </div>
            <div class="sc-bar">
              <div class="scb-lo" style="width: 44%"></div>
              <div class="scb-hi" style="width: 66%"></div>
            </div>
            <div class="sc-ctx">
              PGE Narodowy wide pitch · Albania transition play → sideline
              battles frequent
            </div>
            <span class="sc-conf conf-md">Med</span>
          </div>
          <div class="sc">
            <div class="sc-name">Goal Kicks</div>
            <div class="sc-nums">
              <span class="sc-lo">10</span><span class="sc-sep">·</span
              ><span class="sc-med">16</span><span class="sc-sep">·</span
              ><span class="sc-hi">22</span>
            </div>
            <div class="sc-bar">
              <div class="scb-lo" style="width: 34%"></div>
              <div class="scb-hi" style="width: 58%"></div>
            </div>
            <div class="sc-ctx">
              Albania GK likely to launch long under Polish press · Poland build
              from back under Probierz
            </div>
            <span class="sc-conf conf-md">Med</span>
          </div>
          <div class="sc">
            <div class="sc-name">Tackles</div>
            <div class="sc-nums">
              <span class="sc-lo">22</span><span class="sc-sep">·</span
              ><span class="sc-med">30</span><span class="sc-sep">·</span
              ><span class="sc-hi">40</span>
            </div>
            <div class="sc-bar">
              <div class="scb-lo" style="width: 48%"></div>
              <div class="scb-hi" style="width: 72%"></div>
            </div>
            <div class="sc-ctx">
              Albania press hard on the ball · Poland physical in midfield ·
              high effort given WC stakes
            </div>
            <span class="sc-conf conf-md">Med</span>
          </div>
        </div>
        <div class="fc-ctx">
          <span class="fc-ctx-icon">◆</span>
          <p class="fc-ctx-text">
            <strong>Poland are the strong home favourites</strong> with
            Lewandowski still world-class.
            <span class="cc-g">Albania finished behind England in Group K</span>
            — decent campaign — and have pace in attack.
            <span class="cc-c">PGE Narodowy: a fortress atmosphere.</span>
            <span class="cc-r"
              >Poland suffered recent WC playoff embarrassment</span
            >
            but are experienced in these high-pressure occasions. Albania have
            Seferi and Bajrami to watch. Expect Poland control with goals.
          </p>
        </div>
        <div class="fc-conf">
          <span class="conf-badge cb-hi"
            ><span class="conf-dot cd-hi"></span>HIGH confidence — Poland
            win</span
          >
          <span class="conf-reason"
            >62% Poland · Lewandowski quality · home advantage · Albania 16% to
            win</span
          >
        </div>
      </div>

      <!-- ══ PATH C: TÜRKIYE vs ROMANIA ══ -->
      <div class="path-hdr rev">
        <span class="ph-c"
          >Path C — Türkiye vs Romania · 17:00 GMT · Vodafone Park,
          Istanbul</span
        >
      </div>
      <div class="fc rev">
        <div class="fc-ko">
          <div>
            <span class="ko-t" style="color: var(--orange)">17:00 GMT</span>
            <span class="ko-venue">Vodafone Park · Early KO</span>
          </div>
          <span class="ko-badge kb-hi">⚡ High stakes</span>
        </div>
        <div class="fc-top">
          <div class="fc-team">
            <div class="fc-badge">
              <img
                src="https://flagcdn.com/w160/tr.png"
                alt="Turkey"
                loading="lazy"
                style="background-color: #111320"
              />
            </div>
            <div class="fc-info">
              <div class="fc-club">Türkiye</div>
              <div class="fc-meta">
                FIFA 26 · Güler (R.Madrid), Yildiz (Juventus), Çalhanoglu ·
                Montella
              </div>
              <div class="form-r">
                <div class="fb fw">W</div>
                <div class="fb fw">W</div>
                <div class="fb fw">W</div>
                <div class="fb fw">W</div>
                <div class="fb fl">L</div>
              </div>
            </div>
          </div>
          <div class="fc-mid">
            <div class="fc-pred-lbl">Predicted</div>
            <div class="fc-pred">2–0</div>
            <div class="fc-odds">TUR 4/7 fav</div>
          </div>
          <div class="fc-team away">
            <div class="fc-badge">
              <img
                src="https://flagcdn.com/w160/ro.png"
                alt="Romania"
                loading="lazy"
                style="background-color: #111320"
              />
            </div>
            <div class="fc-info">
              <div class="fc-club">Romania</div>
              <div class="fc-meta">
                FIFA 47 · NL route · Lucescu 80 (coach!) · domestic-based squad
              </div>
              <div class="form-r rv">
                <div class="fb fl">L</div>
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
            <span class="prob-lab">Türkiye</span
            ><span class="prob-lab">Draw/AET</span
            ><span class="prob-lab">Romania</span>
          </div>
          <div class="prob-bar">
            <div class="pb-h" style="flex: 65"></div>
            <div class="pb-d" style="flex: 20"></div>
            <div class="pb-a" style="flex: 15"></div>
          </div>
          <div class="prob-pcts">
            <span class="pp pp-h">65%</span><span class="pp pp-d">20%</span
            ><span class="pp pp-a">15%</span>
          </div>
        </div>
        <div class="sg">
          <div class="sc">
            <div class="sc-name">Corners</div>
            <div class="sc-nums">
              <span class="sc-lo">6</span><span class="sc-sep">·</span
              ><span class="sc-med">10</span><span class="sc-sep">·</span
              ><span class="sc-hi">15</span>
            </div>
            <div class="sc-bar">
              <div class="scb-lo" style="width: 40%"></div>
              <div class="scb-hi" style="width: 72%"></div>
            </div>
            <div class="sc-ctx">
              Güler + Yildiz attack wide → Turkey generate many corners ·
              Romania defend deep = Turkey corner fest
            </div>
            <span class="sc-conf conf-hi">Hi</span>
          </div>
          <div class="sc">
            <div class="sc-name">Shots on Target</div>
            <div class="sc-nums">
              <span class="sc-lo">4</span><span class="sc-sep">·</span
              ><span class="sc-med">7</span><span class="sc-sep">·</span
              ><span class="sc-hi">12</span>
            </div>
            <div class="sc-bar">
              <div class="scb-lo" style="width: 36%"></div>
              <div class="scb-hi" style="width: 68%"></div>
            </div>
            <div class="sc-ctx">
              Turkey top attacking talent vs domestic-based Romania · Istanbul
              atmosphere 70,000 fans
            </div>
            <span class="sc-conf conf-hi">Hi</span>
          </div>
          <div class="sc">
            <div class="sc-name">Fouls</div>
            <div class="sc-nums">
              <span class="sc-lo">16</span><span class="sc-sep">·</span
              ><span class="sc-med">22</span><span class="sc-sep">·</span
              ><span class="sc-hi">32</span>
            </div>
            <div class="sc-bar">
              <div class="scb-lo" style="width: 44%"></div>
              <div class="scb-hi" style="width: 70%"></div>
            </div>
            <div class="sc-ctx">
              Turkey + Romania both physical · Romania foul to disrupt Turkey's
              quality in midfield
            </div>
            <span class="sc-conf conf-hi">Hi</span>
          </div>
          <div class="sc">
            <div class="sc-name">Total Shots</div>
            <div class="sc-nums">
              <span class="sc-lo">16</span><span class="sc-sep">·</span
              ><span class="sc-med">24</span><span class="sc-sep">·</span
              ><span class="sc-hi">32</span>
            </div>
            <div class="sc-bar">
              <div class="scb-lo" style="width: 50%"></div>
              <div class="scb-hi" style="width: 76%"></div>
            </div>
            <div class="sc-ctx">
              Turkey 2.5 goals/g in qual · Vodafone Park 70k atmospheric stadium
              · expectation = attack
            </div>
            <span class="sc-conf conf-hi">Hi</span>
          </div>
          <div class="sc">
            <div class="sc-name">Throw-ins</div>
            <div class="sc-nums">
              <span class="sc-lo">28</span><span class="sc-sep">·</span
              ><span class="sc-med">36</span><span class="sc-sep">·</span
              ><span class="sc-hi">46</span>
            </div>
            <div class="sc-bar">
              <div class="scb-lo" style="width: 42%"></div>
              <div class="scb-hi" style="width: 64%"></div>
            </div>
            <div class="sc-ctx">
              Romania forced sideways → sideline clearances frequent · Turkey
              wide attackers beaten out regularly
            </div>
            <span class="sc-conf conf-md">Med</span>
          </div>
          <div class="sc">
            <div class="sc-name">Goal Kicks</div>
            <div class="sc-nums">
              <span class="sc-lo">10</span><span class="sc-sep">·</span
              ><span class="sc-med">16</span><span class="sc-sep">·</span
              ><span class="sc-hi">24</span>
            </div>
            <div class="sc-bar">
              <div class="scb-lo" style="width: 34%"></div>
              <div class="scb-hi" style="width: 58%"></div>
            </div>
            <div class="sc-ctx">
              Romania GK likely many GKs under Turkey pressure · domestic-based
              squad less polished in build-up
            </div>
            <span class="sc-conf conf-md">Med</span>
          </div>
          <div class="sc">
            <div class="sc-name">Tackles</div>
            <div class="sc-nums">
              <span class="sc-lo">22</span><span class="sc-sep">·</span
              ><span class="sc-med">28</span><span class="sc-sep">·</span
              ><span class="sc-hi">38</span>
            </div>
            <div class="sc-bar">
              <div class="scb-lo" style="width: 46%"></div>
              <div class="scb-hi" style="width: 70%"></div>
            </div>
            <div class="sc-ctx">
              Çalhanoglu covers huge ground · Turkey midfield vs Romania's
              domestic-based midfielders
            </div>
            <span class="sc-conf conf-md">Med</span>
          </div>
        </div>
        <div class="fc-ctx">
          <span class="fc-ctx-icon">◆</span>
          <p class="fc-ctx-text">
            <strong>Turkey are overwhelming favourites.</strong>
            <span class="cc-g"
              >Güler, Yildiz, Çalhanoglu and Özcan provide world-class midfield
              quality</span
            >. Romania's 80-year-old coach Mircea Lucescu largely relies on
            SuperLiga-based players — a significant quality gap.
            <span class="cc-r"
              >Turkey alternate W/L in their last 5 H2H with Romania</span
            >
            but home advantage + talent = strong Turkey. Early KO at 17:00 GMT.
          </p>
        </div>
        <div class="fc-conf">
          <span class="conf-badge cb-hi"
            ><span class="conf-dot cd-hi"></span>HIGH confidence — Turkey
            win</span
          >
          <span class="conf-reason"
            >65% Turkey · CL talent vs SuperLiga squad · Vodafone Park
            atmosphere · Turkey 4W in last 5</span
          >
        </div>
      </div>

      <!-- ══ PATH C: SLOVAKIA vs KOSOVO ══ -->
      <div class="path-hdr rev">
        <span class="ph-c"
          >Path C — Slovakia vs Kosovo · 19:45 GMT · Národný futbalový štadión,
          Bratislava</span
        >
      </div>
      <div class="fc rev">
        <div class="fc-ko">
          <div>
            <span class="ko-t" style="color: var(--orange)">19:45 GMT</span>
            <span class="ko-venue"
              >Národný futbalový štadión</span
            >
          </div>
          <span class="ko-badge kb-hi">⚡ High stakes</span>
        </div>
        <div class="fc-top">
          <div class="fc-team">
            <div class="fc-badge">
              <img
                src="https://flagcdn.com/w160/sk.png"
                alt="Slovakia"
                loading="lazy"
                style="background-color: #111320"
              />
            </div>
            <div class="fc-info">
              <div class="fc-club">Slovakia</div>
              <div class="fc-meta">
                FIFA 46 · Dubravka · Skriniar · Lobotka · 3W at home in qual
              </div>
              <div class="form-r">
                <div class="fb fw">W</div>
                <div class="fb fw">W</div>
                <div class="fb fw">W</div>
                <div class="fb fw">W</div>
                <div class="fb fl">L</div>
              </div>
            </div>
          </div>
          <div class="fc-mid">
            <div class="fc-pred-lbl">Predicted</div>
            <div class="fc-pred">2–1</div>
            <div class="fc-odds">SVK slight fav</div>
          </div>
          <div class="fc-team away">
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
              <div class="fc-meta">
                FIFA 84 · Muriqi (Mallorca) · beat Sweden twice in qual · Foda
              </div>
              <div class="form-r rv">
                <div class="fb fw">W</div>
                <div class="fb fw">W</div>
                <div class="fb fw">W</div>
                <div class="fb fd">D</div>
                <div class="fb fw">W</div>
              </div>
            </div>
          </div>
        </div>
        <div class="fc-prob">
          <div class="prob-labs">
            <span class="prob-lab">Slovakia</span
            ><span class="prob-lab">Draw/AET</span
            ><span class="prob-lab">Kosovo</span>
          </div>
          <div class="prob-bar">
            <div class="pb-h" style="flex: 48"></div>
            <div class="pb-d" style="flex: 26"></div>
            <div class="pb-a" style="flex: 26"></div>
          </div>
          <div class="prob-pcts">
            <span class="pp pp-h">48%</span><span class="pp pp-d">26%</span
            ><span class="pp pp-a">26%</span>
          </div>
        </div>
        <div class="sg">
          <div class="sc">
            <div class="sc-name">Corners</div>
            <div class="sc-nums">
              <span class="sc-lo">6</span><span class="sc-sep">·</span
              ><span class="sc-med">10</span><span class="sc-sep">·</span
              ><span class="sc-hi">15</span>
            </div>
            <div class="sc-bar">
              <div class="scb-lo" style="width: 40%"></div>
              <div class="scb-hi" style="width: 72%"></div>
            </div>
            <div class="sc-ctx">
              Slovakia home pressure → corners · Kosovo beat Sweden H&A =
              tactically sophisticated · tight match
            </div>
            <span class="sc-conf conf-md">Med</span>
          </div>
          <div class="sc">
            <div class="sc-name">Shots on Target</div>
            <div class="sc-nums">
              <span class="sc-lo">5</span><span class="sc-sep">·</span
              ><span class="sc-med">8</span><span class="sc-sep">·</span
              ><span class="sc-hi">13</span>
            </div>
            <div class="sc-bar">
              <div class="scb-lo" style="width: 38%"></div>
              <div class="scb-hi" style="width: 68%"></div>
            </div>
            <div class="sc-ctx">
              Muriqi prolific at Mallorca this season · Kucka + Lobotka create
              for Slovakia · both teams have quality
            </div>
            <span class="sc-conf conf-md">Med</span>
          </div>
          <div class="sc">
            <div class="sc-name">Fouls</div>
            <div class="sc-nums">
              <span class="sc-lo">18</span><span class="sc-sep">·</span
              ><span class="sc-med">26</span><span class="sc-sep">·</span
              ><span class="sc-hi">36</span>
            </div>
            <div class="sc-bar">
              <div class="scb-lo" style="width: 46%"></div>
              <div class="scb-hi" style="width: 74%"></div>
            </div>
            <div class="sc-ctx">
              Kosovo's historic first WC appearance chase = maximum physicality
              · tight competitive match = most fouls on the day
            </div>
            <span class="sc-conf conf-hi">Hi</span>
          </div>
          <div class="sc">
            <div class="sc-name">Total Shots</div>
            <div class="sc-nums">
              <span class="sc-lo">16</span><span class="sc-sep">·</span
              ><span class="sc-med">24</span><span class="sc-sep">·</span
              ><span class="sc-hi">32</span>
            </div>
            <div class="sc-bar">
              <div class="scb-lo" style="width: 50%"></div>
              <div class="scb-hi" style="width: 74%"></div>
            </div>
            <div class="sc-ctx">
              Slovakia pushed for goals at home in all 3 home qualifiers ·
              Kosovo attacks boldly when away
            </div>
            <span class="sc-conf conf-md">Med</span>
          </div>
          <div class="sc">
            <div class="sc-name">Throw-ins</div>
            <div class="sc-nums">
              <span class="sc-lo">32</span><span class="sc-sep">·</span
              ><span class="sc-med">42</span><span class="sc-sep">·</span
              ><span class="sc-hi">52</span>
            </div>
            <div class="sc-bar">
              <div class="scb-lo" style="width: 48%"></div>
              <div class="scb-hi" style="width: 72%"></div>
            </div>
            <div class="sc-ctx">
              Most throw-ins predicted of any UEFA fixture — Kosovo
              counter-pressing generates sideline chaos
            </div>
            <span class="sc-conf conf-md">Med</span>
          </div>
          <div class="sc">
            <div class="sc-name">Goal Kicks</div>
            <div class="sc-nums">
              <span class="sc-lo">12</span><span class="sc-sep">·</span
              ><span class="sc-med">18</span><span class="sc-sep">·</span
              ><span class="sc-hi">26</span>
            </div>
            <div class="sc-bar">
              <div class="scb-lo" style="width: 36%"></div>
              <div class="scb-hi" style="width: 62%"></div>
            </div>
            <div class="sc-ctx">
              Dubravka (Burnley) long kick style · Kosovo GK also long · both
              teams directional play
            </div>
            <span class="sc-conf conf-lo">Low</span>
          </div>
          <div class="sc">
            <div class="sc-name">Tackles</div>
            <div class="sc-nums">
              <span class="sc-lo">26</span><span class="sc-sep">·</span
              ><span class="sc-med">36</span><span class="sc-sep">·</span
              ><span class="sc-hi">48</span>
            </div>
            <div class="sc-bar">
              <div class="scb-lo" style="width: 52%"></div>
              <div class="scb-hi" style="width: 78%"></div>
            </div>
            <div class="sc-ctx">
              Highest tackles expected of all 8 UEFA ties — Kosovo's first ever
              WC chance + Slovakia's home pride
            </div>
            <span class="sc-conf conf-hi">Hi</span>
          </div>
        </div>
        <div class="fc-ctx">
          <span class="fc-ctx-icon">◆</span>
          <p class="fc-ctx-text">
            <strong
              >Kosovo are chasing their first ever World Cup qualification as an
              independent nation.</strong
            >
            <span class="cc-g"
              >They beat Sweden home AND away in qualifying</span
            >
            — no mean feat. Muriqi is on fire at Mallorca.
            <span class="cc-c"
              >Slovakia's home record in qualifying: 3W from 3 at
              Bratislava.</span
            >
            <span class="cc-r"
              >Skriniar + Lobotka provide real Champions League pedigree.</span
            >
            This is the most unpredictable and potentially most thrilling of all
            the UEFA semi-finals — both teams can win and both want it
            desperately.
          </p>
        </div>
        <div class="fc-conf">
          <span class="conf-badge cb-lo"
            ><span class="conf-dot cd-lo"></span>LOW confidence — too
            close</span
          >
          <span class="conf-reason"
            >48% SVK · Kosovo beat Sweden twice · Muriqi = threat · genuinely
            could go either way or AET</span
          >
        </div>
      </div>

      <!-- ══ PATH D: DENMARK vs NORTH MACEDONIA ══ -->
      <div class="path-hdr rev">
        <span class="ph-d"
          >Path D — Denmark vs North Macedonia · 19:45 GMT · Parken Stadium,
          Copenhagen</span
        >
      </div>
      <div class="fc rev">
        <div class="fc-ko">
          <div>
            <span class="ko-t" style="color: var(--purple)">19:45 GMT</span>
            <span class="ko-venue"
              >Parken Stadium</span
            >
          </div>
          <span class="ko-badge kb-hi">⚡ High stakes</span>
        </div>
        <div class="fc-top">
          <div class="fc-team">
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
              <div class="fc-meta">
                FIFA 20 · Eriksen · Hojlund · Damsgaard · Riemer
              </div>
              <div class="form-r">
                <div class="fb fw">W</div>
                <div class="fb fw">W</div>
                <div class="fb fw">W</div>
                <div class="fb fl">L</div>
                <div class="fb fd">D</div>
              </div>
            </div>
          </div>
          <div class="fc-mid">
            <div class="fc-pred-lbl">Predicted</div>
            <div class="fc-pred">2–0</div>
            <div class="fc-odds">DEN strong fav</div>
          </div>
          <div class="fc-team away">
            <div class="fc-badge">
              <img
                src="https://flagcdn.com/w160/mk.png"
                alt="N. Macedonia"
                loading="lazy"
                style="background-color: #111320"
              />
            </div>
            <div class="fc-info">
              <div class="fc-club">N. Macedonia</div>
              <div class="fc-meta">
                FIFA 65 · NL route · knocked Italy out in 2022 · Bardi
              </div>
              <div class="form-r rv">
                <div class="fb fw">W</div>
                <div class="fb fw">W</div>
                <div class="fb fw">W</div>
                <div class="fb fl">L</div>
                <div class="fb fw">W</div>
              </div>
            </div>
          </div>
        </div>
        <div class="fc-prob">
          <div class="prob-labs">
            <span class="prob-lab">Denmark</span
            ><span class="prob-lab">Draw/AET</span
            ><span class="prob-lab">N. Macedonia</span>
          </div>
          <div class="prob-bar">
            <div class="pb-h" style="flex: 66"></div>
            <div class="pb-d" style="flex: 20"></div>
            <div class="pb-a" style="flex: 14"></div>
          </div>
          <div class="prob-pcts">
            <span class="pp pp-h">66%</span><span class="pp pp-d">20%</span
            ><span class="pp pp-a">14%</span>
          </div>
        </div>
        <div class="sg">
          <div class="sc">
            <div class="sc-name">Corners</div>
            <div class="sc-nums">
              <span class="sc-lo">6</span><span class="sc-sep">·</span
              ><span class="sc-med">10</span><span class="sc-sep">·</span
              ><span class="sc-hi">14</span>
            </div>
            <div class="sc-bar">
              <div class="scb-lo" style="width: 42%"></div>
              <div class="scb-hi" style="width: 70%"></div>
            </div>
            <div class="sc-ctx">
              Denmark dominant possession → corners · N.Mac defend deep under
              pressure from superior sides
            </div>
            <span class="sc-conf conf-hi">Hi</span>
          </div>
          <div class="sc">
            <div class="sc-name">Shots on Target</div>
            <div class="sc-nums">
              <span class="sc-lo">4</span><span class="sc-sep">·</span
              ><span class="sc-med">7</span><span class="sc-sep">·</span
              ><span class="sc-hi">11</span>
            </div>
            <div class="sc-bar">
              <div class="scb-lo" style="width: 36%"></div>
              <div class="scb-hi" style="width: 66%"></div>
            </div>
            <div class="sc-ctx">
              Hojlund (Man Utd) + Eriksen quality · Denmark blew automatic qual
              but talent still strong
            </div>
            <span class="sc-conf conf-hi">Hi</span>
          </div>
          <div class="sc">
            <div class="sc-name">Fouls</div>
            <div class="sc-nums">
              <span class="sc-lo">16</span><span class="sc-sep">·</span
              ><span class="sc-med">22</span><span class="sc-sep">·</span
              ><span class="sc-hi">30</span>
            </div>
            <div class="sc-bar">
              <div class="scb-lo" style="width: 44%"></div>
              <div class="scb-hi" style="width: 68%"></div>
            </div>
            <div class="sc-ctx">
              Christensen + Dorgu OUT for Denmark but N.Mac will foul to disrupt
              technically superior opponents
            </div>
            <span class="sc-conf conf-hi">Hi</span>
          </div>
          <div class="sc">
            <div class="sc-name">Total Shots</div>
            <div class="sc-nums">
              <span class="sc-lo">16</span><span class="sc-sep">·</span
              ><span class="sc-med">24</span><span class="sc-sep">·</span
              ><span class="sc-hi">30</span>
            </div>
            <div class="sc-bar">
              <div class="scb-lo" style="width: 52%"></div>
              <div class="scb-hi" style="width: 74%"></div>
            </div>
            <div class="sc-ctx">
              Denmark 24+ shots at home likely · N.Mac pace on counter could
              produce 3-4 attempts
            </div>
            <span class="sc-conf conf-hi">Hi</span>
          </div>
          <div class="sc">
            <div class="sc-name">Throw-ins</div>
            <div class="sc-nums">
              <span class="sc-lo">26</span><span class="sc-sep">·</span
              ><span class="sc-med">34</span><span class="sc-sep">·</span
              ><span class="sc-hi">44</span>
            </div>
            <div class="sc-bar">
              <div class="scb-lo" style="width: 40%"></div>
              <div class="scb-hi" style="width: 62%"></div>
            </div>
            <div class="sc-ctx">
              N.Mac defend on the wings → many out-of-plays on touchline ·
              moderate throw-in count
            </div>
            <span class="sc-conf conf-md">Med</span>
          </div>
          <div class="sc">
            <div class="sc-name">Goal Kicks</div>
            <div class="sc-nums">
              <span class="sc-lo">10</span><span class="sc-sep">·</span
              ><span class="sc-med">16</span><span class="sc-sep">·</span
              ><span class="sc-hi">22</span>
            </div>
            <div class="sc-bar">
              <div class="scb-lo" style="width: 34%"></div>
              <div class="scb-hi" style="width: 58%"></div>
            </div>
            <div class="sc-ctx">
              Denmark play out from back · N.Mac GK may be under pressure → many
              GKs for Bardi
            </div>
            <span class="sc-conf conf-md">Med</span>
          </div>
          <div class="sc">
            <div class="sc-name">Tackles</div>
            <div class="sc-nums">
              <span class="sc-lo">22</span><span class="sc-sep">·</span
              ><span class="sc-med">30</span><span class="sc-sep">·</span
              ><span class="sc-hi">40</span>
            </div>
            <div class="sc-bar">
              <div class="scb-lo" style="width: 48%"></div>
              <div class="scb-hi" style="width: 72%"></div>
            </div>
            <div class="sc-ctx">
              N.Mac 3-5-2 style = hard running + tackling · Eriksen + Hojlund
              attract tackles · intensity high
            </div>
            <span class="sc-conf conf-hi">Hi</span>
          </div>
        </div>
        <div class="fc-ctx">
          <span class="fc-ctx-icon">◆</span>
          <p class="fc-ctx-text">
            <strong
              >North Macedonia knocked Italy out of the 2022 playoff</strong
            >
            away from home — upset specialists.
            <span class="cc-r"
              >Denmark missing Christensen (CB, Barcelona) and Patrick Dorgu
              (LB, Man United)</span
            >.
            <span class="cc-c"
              >Eriksen + Hojlund (Man Utd) + Damsgaard provide Champions League
              quality.</span
            >
            Denmark blew automatic qualification by dropping points to Belarus
            in November — nerves are a real factor. N.Mac will be disciplined
            and dangerous on the counter.
          </p>
        </div>
        <div class="fc-conf">
          <span class="conf-badge cb-md"
            ><span class="conf-dot cd-md"></span>MED confidence — Denmark</span
          >
          <span class="conf-reason"
            >66% Denmark · N.Mac upset specialists · Christensen + Dorgu OUT ·
            Denmark bottled it in qual</span
          >
        </div>
      </div>

      <!-- ══ PATH D: CZECHIA vs REPUBLIC OF IRELAND ══ -->
      <div class="path-hdr rev">
        <span class="ph-d"
          >Path D — Czechia vs Republic of Ireland · 19:45 GMT · Fortuna Arena,
          Prague</span
        >
      </div>
      <div class="fc rev">
        <div class="fc-ko">
          <div>
            <span class="ko-t" style="color: var(--purple)">19:45 GMT</span>
            <span class="ko-venue">Fortuna Arena</span>
          </div>
          <span class="ko-badge kb-hi">⚡ Both 20yr WC absence</span>
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
              <div class="fc-meta">
                FIFA 44 · Soucek · Barak · Schick back from injury · Hasek
              </div>
              <div class="form-r">
                <div class="fb fw">W</div>
                <div class="fb fw">W</div>
                <div class="fb fw">W</div>
                <div class="fb fw">W</div>
                <div class="fb fl">L</div>
              </div>
            </div>
          </div>
          <div class="fc-mid">
            <div class="fc-pred-lbl">Predicted</div>
            <div class="fc-pred">1–1</div>
            <div class="fc-odds">CZE slight fav · AET likely</div>
          </div>
          <div class="fc-team away">
            <div class="fc-badge">
              <img
                src="https://flagcdn.com/w160/ie.png"
                alt="Republic of Ireland"
                loading="lazy"
                style="background-color: #111320"
              />
            </div>
            <div class="fc-info">
              <div class="fc-club">Rep. of Ireland</div>
              <div class="fc-meta">
                FIFA 62 · Parrott hat-trick vs HUN (96') · Hallgrimsson
              </div>
              <div class="form-r rv">
                <div class="fb fw">W</div>
                <div class="fb fw">W</div>
                <div class="fb fl">L</div>
                <div class="fb fd">D</div>
                <div class="fb fw">W</div>
              </div>
            </div>
          </div>
        </div>
        <div class="fc-prob">
          <div class="prob-labs">
            <span class="prob-lab">Czechia</span
            ><span class="prob-lab">Draw/AET</span
            ><span class="prob-lab">Ireland</span>
          </div>
          <div class="prob-bar">
            <div class="pb-h" style="flex: 44"></div>
            <div class="pb-d" style="flex: 28"></div>
            <div class="pb-a" style="flex: 28"></div>
          </div>
          <div class="prob-pcts">
            <span class="pp pp-h">44%</span><span class="pp pp-d">28%</span
            ><span class="pp pp-a">28%</span>
          </div>
        </div>
        <div class="sg">
          <div class="sc">
            <div class="sc-name">Corners</div>
            <div class="sc-nums">
              <span class="sc-lo">6</span><span class="sc-sep">·</span
              ><span class="sc-med">10</span><span class="sc-sep">·</span
              ><span class="sc-hi">15</span>
            </div>
            <div class="sc-bar">
              <div class="scb-lo" style="width: 40%"></div>
              <div class="scb-hi" style="width: 72%"></div>
            </div>
            <div class="sc-ctx">
              Both teams generate corners in attacking play · Ireland's
              physicality causes corners when challenging for ball
            </div>
            <span class="sc-conf conf-md">Med</span>
          </div>
          <div class="sc">
            <div class="sc-name">Shots on Target</div>
            <div class="sc-nums">
              <span class="sc-lo">4</span><span class="sc-sep">·</span
              ><span class="sc-med">7</span><span class="sc-sep">·</span
              ><span class="sc-hi">11</span>
            </div>
            <div class="sc-bar">
              <div class="scb-lo" style="width: 36%"></div>
              <div class="scb-hi" style="width: 66%"></div>
            </div>
            <div class="sc-ctx">
              Parrott + Ogbene for Ireland · Schick + Chory for Czechia · both
              compact with moments of quality
            </div>
            <span class="sc-conf conf-md">Med</span>
          </div>
          <div class="sc">
            <div class="sc-name">Fouls</div>
            <div class="sc-nums">
              <span class="sc-lo">18</span><span class="sc-sep">·</span
              ><span class="sc-med">26</span><span class="sc-sep">·</span
              ><span class="sc-hi">36</span>
            </div>
            <div class="sc-bar">
              <div class="scb-lo" style="width: 46%"></div>
              <div class="scb-hi" style="width: 72%"></div>
            </div>
            <div class="sc-ctx">
              Ireland physical in midfield (Coleman, Molumby) · first WC since
              2002 for Ireland = maximum effort
            </div>
            <span class="sc-conf conf-hi">Hi</span>
          </div>
          <div class="sc">
            <div class="sc-name">Total Shots</div>
            <div class="sc-nums">
              <span class="sc-lo">16</span><span class="sc-sep">·</span
              ><span class="sc-med">24</span><span class="sc-sep">·</span
              ><span class="sc-hi">32</span>
            </div>
            <div class="sc-bar">
              <div class="scb-lo" style="width: 50%"></div>
              <div class="scb-hi" style="width: 74%"></div>
            </div>
            <div class="sc-ctx">
              Czechia home generates shot volume · Ireland shoot on the break ·
              AET likely = extra 30 min of shots
            </div>
            <span class="sc-conf conf-md">Med</span>
          </div>
          <div class="sc">
            <div class="sc-name">Throw-ins</div>
            <div class="sc-nums">
              <span class="sc-lo">32</span><span class="sc-sep">·</span
              ><span class="sc-med">42</span><span class="sc-sep">·</span
              ><span class="sc-hi">54</span>
            </div>
            <div class="sc-bar">
              <div class="scb-lo" style="width: 48%"></div>
              <div class="scb-hi" style="width: 72%"></div>
            </div>
            <div class="sc-ctx">
              High throw-in count predicted — AET if it goes that far adds 30+
              more minutes of sideline battles
            </div>
            <span class="sc-conf conf-md">Med</span>
          </div>
          <div class="sc">
            <div class="sc-name">Goal Kicks</div>
            <div class="sc-nums">
              <span class="sc-lo">12</span><span class="sc-sep">·</span
              ><span class="sc-med">18</span><span class="sc-sep">·</span
              ><span class="sc-hi">26</span>
            </div>
            <div class="sc-bar">
              <div class="scb-lo" style="width: 38%"></div>
              <div class="scb-hi" style="width: 62%"></div>
            </div>
            <div class="sc-ctx">
              Ireland GK launches long under pressure · Czechia build short ·
              balance of GK styles
            </div>
            <span class="sc-conf conf-lo">Low</span>
          </div>
          <div class="sc">
            <div class="sc-name">Tackles</div>
            <div class="sc-nums">
              <span class="sc-lo">26</span><span class="sc-sep">·</span
              ><span class="sc-med">36</span><span class="sc-sep">·</span
              ><span class="sc-hi">50</span>
            </div>
            <div class="sc-bar">
              <div class="scb-lo" style="width: 50%"></div>
              <div class="scb-hi" style="width: 78%"></div>
            </div>
            <div class="sc-ctx">
              Most scrappy tackle count of the day if AET — Ireland's 96'
              Parrott win vs Hungary showed their spirit; expect total
              commitment
            </div>
            <span class="sc-conf conf-hi">Hi</span>
          </div>
        </div>
        <div class="fc-ctx">
          <span class="fc-ctx-icon">◆</span>
          <p class="fc-ctx-text">
            <strong
              >Two teams both chasing their first World Cup since 2002.</strong
            >
            <span class="cc-g"
              >Ireland qualified via Troy Parrott's stunning hat-trick including
              a 96th-minute winner vs Hungary</span
            >
            — the momentum is exceptional.
            <span class="cc-c"
              >Czechia: Soucek (West Ham captain), Barak, Schick (returning from
              injury) provide quality.</span
            >
            AET is the most likely outcome of all 8 UEFA fixtures here.
            <span class="cc-r"
              >Fortuna Arena Prague only holds 19,370 — a tight, partisan
              cauldron.</span
            >
            Ireland have the psychological momentum of a miracle qualification —
            don't count them out.
          </p>
        </div>
        <div class="fc-conf">
          <span class="conf-badge cb-lo"
            ><span class="conf-dot cd-lo"></span>LOW confidence — 50/50</span
          >
          <span class="conf-reason"
            >44% CZE · Ireland on incredible momentum · AET most likely of all 8
            UEFA ties · genuine toss-up</span
          >
        </div>
      </div>

      <!-- ══ FIFA IC: NEW CALEDONIA vs JAMAICA ══ -->
      <div class="path-hdr rev">
        <span class="ph-ic"
          >FIFA Intercontinental — New Caledonia vs Jamaica · 03:00 GMT Fri ·
          Guadalajara, Mexico</span
        >
      </div>
      <div class="fc rev">
        <div class="fc-ko">
          <div>
            <span class="ko-t" style="color: var(--pink)">03:00 GMT Fri</span>
            <span class="ko-venue"
              >Estadio Jalisco</span
            >
          </div>
          <span class="ko-badge kb-ic">FIFA IC playoff</span>
        </div>
        <div class="fc-top">
          <div class="fc-team">
            <div class="fc-badge">
              <img
                src="https://flagcdn.com/w160/nc.png"
                alt="New Caledonia"
                loading="lazy"
                style="background-color: #111320"
              />
            </div>
            <div class="fc-info">
              <div class="fc-club">New Caledonia</div>
              <div class="fc-meta">
                OFC route · small island nation · rare WC journey
              </div>
              <div class="form-r">
                <div class="fb fw">W</div>
                <div class="fb fw">W</div>
                <div class="fb fw">W</div>
                <div class="fb fw">W</div>
                <div class="fb fd">D</div>
              </div>
            </div>
          </div>
          <div class="fc-mid">
            <div class="fc-pred-lbl">Predicted</div>
            <div class="fc-pred">1–2</div>
            <div class="fc-odds">JAM narrow fav</div>
          </div>
          <div class="fc-team away">
            <div class="fc-badge">
              <img
                src="https://flagcdn.com/w160/jm.png"
                alt="Jamaica"
                loading="lazy"
                style="background-color: #111320"
              />
            </div>
            <div class="fc-info">
              <div class="fc-club">Jamaica</div>
              <div class="fc-meta">
                CONCACAF · already qualified · strong Caribbean squad · Liston
              </div>
              <div class="form-r rv">
                <div class="fb fw">W</div>
                <div class="fb fw">W</div>
                <div class="fb fd">D</div>
                <div class="fb fw">W</div>
                <div class="fb fl">L</div>
              </div>
            </div>
          </div>
        </div>
        <div class="fc-prob">
          <div class="prob-labs">
            <span class="prob-lab">New Caledonia</span
            ><span class="prob-lab">Draw/AET</span
            ><span class="prob-lab">Jamaica</span>
          </div>
          <div class="prob-bar">
            <div class="pb-h" style="flex: 18"></div>
            <div class="pb-d" style="flex: 22"></div>
            <div class="pb-a" style="flex: 60"></div>
          </div>
          <div class="prob-pcts">
            <span class="pp pp-h">18%</span><span class="pp pp-d">22%</span
            ><span class="pp pp-a">60%</span>
          </div>
        </div>
        <div class="sg">
          <div class="sc">
            <div class="sc-name">Corners</div>
            <div class="sc-nums">
              <span class="sc-lo">4</span><span class="sc-sep">·</span
              ><span class="sc-med">8</span><span class="sc-sep">·</span
              ><span class="sc-hi">12</span>
            </div>
            <div class="sc-bar">
              <div class="scb-lo" style="width: 34%"></div>
              <div class="scb-hi" style="width: 64%"></div>
            </div>
            <div class="sc-ctx">
              Jamaica expected to dominate · New Caledonia OFC-based defensive
              style · moderate corner count
            </div>
            <span class="sc-conf conf-lo">Low</span>
          </div>
          <div class="sc">
            <div class="sc-name">Shots on Target</div>
            <div class="sc-nums">
              <span class="sc-lo">3</span><span class="sc-sep">·</span
              ><span class="sc-med">6</span><span class="sc-sep">·</span
              ><span class="sc-hi">10</span>
            </div>
            <div class="sc-bar">
              <div class="scb-lo" style="width: 30%"></div>
              <div class="scb-hi" style="width: 62%"></div>
            </div>
            <div class="sc-ctx">
              Limited data on both teams · Jamaica CONCACAF quality vs OFC
              standard · significant level gap
            </div>
            <span class="sc-conf conf-lo">Low</span>
          </div>
          <div class="sc">
            <div class="sc-name">Fouls</div>
            <div class="sc-nums">
              <span class="sc-lo">16</span><span class="sc-sep">·</span
              ><span class="sc-med">22</span><span class="sc-sep">·</span
              ><span class="sc-hi">30</span>
            </div>
            <div class="sc-bar">
              <div class="scb-lo" style="width: 44%"></div>
              <div class="scb-hi" style="width: 66%"></div>
            </div>
            <div class="sc-ctx">
              Intercontinental playoff tension · New Caledonia likely to foul to
              disrupt Jamaica's faster players
            </div>
            <span class="sc-conf conf-lo">Low</span>
          </div>
          <div class="sc">
            <div class="sc-name">Total Shots</div>
            <div class="sc-nums">
              <span class="sc-lo">10</span><span class="sc-sep">·</span
              ><span class="sc-med">18</span><span class="sc-sep">·</span
              ><span class="sc-hi">26</span>
            </div>
            <div class="sc-bar">
              <div class="scb-lo" style="width: 40%"></div>
              <div class="scb-hi" style="width: 68%"></div>
            </div>
            <div class="sc-ctx">
              Jamaica should dominate shots · New Caledonia counter-attacks
              likely OFC-style
            </div>
            <span class="sc-conf conf-lo">Low</span>
          </div>
          <div class="sc">
            <div class="sc-name">Throw-ins</div>
            <div class="sc-nums">
              <span class="sc-lo">24</span><span class="sc-sep">·</span
              ><span class="sc-med">32</span><span class="sc-sep">·</span
              ><span class="sc-hi">42</span>
            </div>
            <div class="sc-bar">
              <div class="scb-lo" style="width: 40%"></div>
              <div class="scb-hi" style="width: 62%"></div>
            </div>
            <div class="sc-ctx">
              CONCACAF style games often have high sideline activity · Mexico
              venue neutral
            </div>
            <span class="sc-conf conf-lo">Low</span>
          </div>
          <div class="sc">
            <div class="sc-name">Goal Kicks</div>
            <div class="sc-nums">
              <span class="sc-lo">10</span><span class="sc-sep">·</span
              ><span class="sc-med">16</span><span class="sc-sep">·</span
              ><span class="sc-hi">22</span>
            </div>
            <div class="sc-bar">
              <div class="scb-lo" style="width: 34%"></div>
              <div class="scb-hi" style="width: 58%"></div>
            </div>
            <div class="sc-ctx">
              Limited data · New Caledonia may launch long · Jamaica build-up
              style from CONCACAF qual
            </div>
            <span class="sc-conf conf-lo">Low</span>
          </div>
          <div class="sc">
            <div class="sc-name">Tackles</div>
            <div class="sc-nums">
              <span class="sc-lo">18</span><span class="sc-sep">·</span
              ><span class="sc-med">26</span><span class="sc-sep">·</span
              ><span class="sc-hi">36</span>
            </div>
            <div class="sc-bar">
              <div class="scb-lo" style="width: 44%"></div>
              <div class="scb-hi" style="width: 68%"></div>
            </div>
            <div class="sc-ctx">
              New Caledonia likely to tackle hard to stay in game · Jamaica
              physical CONCACAF style
            </div>
            <span class="sc-conf conf-lo">Low</span>
          </div>
        </div>
        <div class="fc-ctx">
          <span class="fc-ctx-icon">◆</span>
          <p class="fc-ctx-text">
            <strong
              >New Caledonia are the smallest nation in the intercontinental
              playoffs.</strong
            >
            Playing at 03:00 GMT (Fri) in Guadalajara, Mexico — neutral venue.
            <span class="cc-g"
              >Jamaica have qualified for the 2026 World Cup already</span
            >
            as one of the CONCACAF third-round qualifiers (confirmed).
            <span class="cc-r">Stat confidence is LOW throughout</span> —
            limited reliable data on New Caledonia's performances vs quality
            opposition. Jamaica should win.
          </p>
        </div>
        <div class="fc-conf">
          <span class="conf-badge cb-lo"
            ><span class="conf-dot cd-lo"></span>LOW confidence — limited
            data</span
          >
          <span class="conf-reason"
            >60% Jamaica but very limited data on New Caledonia vs
            CONCACAF-level opponents</span
          >
        </div>
      </div>

      <!-- ══ FIFA IC: BOLIVIA vs SURINAME ══ -->
      <div class="path-hdr rev">
        <span class="ph-ic2"
          >FIFA Intercontinental — Bolivia vs Suriname · 23:00 GMT · Monterrey,
          Mexico</span
        >
      </div>
      <div class="fc rev">
        <div class="fc-ko">
          <div>
            <span class="ko-t" style="color: var(--gold)">23:00 GMT</span>
            <span class="ko-venue"
              >Estadio BBVA</span
            >
          </div>
          <span class="ko-badge kb-ic">FIFA IC playoff</span>
        </div>
        <div class="fc-top">
          <div class="fc-team">
            <div class="fc-badge">
              <img
                src="https://flagcdn.com/w160/bo.png"
                alt="Bolivia"
                loading="lazy"
                style="background-color: #111320"
              />
            </div>
            <div class="fc-info">
              <div class="fc-club">Bolivia</div>
              <div class="fc-meta">
                CONMEBOL · La Paz altitude team · play at sea level · Rojas
              </div>
              <div class="form-r">
                <div class="fb fw">W</div>
                <div class="fb fw">W</div>
                <div class="fb fl">L</div>
                <div class="fb fl">L</div>
                <div class="fb fd">D</div>
              </div>
            </div>
          </div>
          <div class="fc-mid">
            <div class="fc-pred-lbl">Predicted</div>
            <div class="fc-pred">2–1</div>
            <div class="fc-odds">BOL favoured</div>
          </div>
          <div class="fc-team away">
            <div class="fc-badge">
              <img
                src="https://flagcdn.com/w160/sr.png"
                alt="Suriname"
                loading="lazy"
                style="background-color: #111320"
              />
            </div>
            <div class="fc-info">
              <div class="fc-club">Suriname</div>
              <div class="fc-meta">
                CONCACAF · smallest nation in FIFA IC playoffs · debut stage
              </div>
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
            <span class="prob-lab">Bolivia</span
            ><span class="prob-lab">Draw/AET</span
            ><span class="prob-lab">Suriname</span>
          </div>
          <div class="prob-bar">
            <div class="pb-h" style="flex: 55"></div>
            <div class="pb-d" style="flex: 25"></div>
            <div class="pb-a" style="flex: 20"></div>
          </div>
          <div class="prob-pcts">
            <span class="pp pp-h">55%</span><span class="pp pp-d">25%</span
            ><span class="pp pp-a">20%</span>
          </div>
        </div>
        <div class="sg">
          <div class="sc">
            <div class="sc-name">Corners</div>
            <div class="sc-nums">
              <span class="sc-lo">4</span><span class="sc-sep">·</span
              ><span class="sc-med">8</span><span class="sc-sep">·</span
              ><span class="sc-hi">12</span>
            </div>
            <div class="sc-bar">
              <div class="scb-lo" style="width: 32%"></div>
              <div class="scb-hi" style="width: 60%"></div>
            </div>
            <div class="sc-ctx">
              Bolivia CONMEBOL pedigree → more corners at sea level · Suriname
              CONCACAF style = compact
            </div>
            <span class="sc-conf conf-lo">Low</span>
          </div>
          <div class="sc">
            <div class="sc-name">Shots on Target</div>
            <div class="sc-nums">
              <span class="sc-lo">3</span><span class="sc-sep">·</span
              ><span class="sc-med">6</span><span class="sc-sep">·</span
              ><span class="sc-hi">10</span>
            </div>
            <div class="sc-bar">
              <div class="scb-lo" style="width: 28%"></div>
              <div class="scb-hi" style="width: 58%"></div>
            </div>
            <div class="sc-ctx">
              Bolivia at sea level (not altitude) = less impactful · Suriname
              surprise potential · limited data
            </div>
            <span class="sc-conf conf-lo">Low</span>
          </div>
          <div class="sc">
            <div class="sc-name">Fouls</div>
            <div class="sc-nums">
              <span class="sc-lo">16</span><span class="sc-sep">·</span
              ><span class="sc-med">22</span><span class="sc-sep">·</span
              ><span class="sc-hi">32</span>
            </div>
            <div class="sc-bar">
              <div class="scb-lo" style="width: 42%"></div>
              <div class="scb-hi" style="width: 66%"></div>
            </div>
            <div class="sc-ctx">
              Intercontinental playoff = nervous, foul-heavy game · Suriname
              foul to level tactical gap vs Bolivia
            </div>
            <span class="sc-conf conf-lo">Low</span>
          </div>
          <div class="sc">
            <div class="sc-name">Total Shots</div>
            <div class="sc-nums">
              <span class="sc-lo">10</span><span class="sc-sep">·</span
              ><span class="sc-med">18</span><span class="sc-sep">·</span
              ><span class="sc-hi">26</span>
            </div>
            <div class="sc-bar">
              <div class="scb-lo" style="width: 38%"></div>
              <div class="scb-hi" style="width: 64%"></div>
            </div>
            <div class="sc-ctx">
              Bolivia should create more chances but Suriname historically
              dangerous · very limited data
            </div>
            <span class="sc-conf conf-lo">Low</span>
          </div>
          <div class="sc">
            <div class="sc-name">Throw-ins</div>
            <div class="sc-nums">
              <span class="sc-lo">22</span><span class="sc-sep">·</span
              ><span class="sc-med">32</span><span class="sc-sep">·</span
              ><span class="sc-hi">42</span>
            </div>
            <div class="sc-bar">
              <div class="scb-lo" style="width: 38%"></div>
              <div class="scb-hi" style="width: 60%"></div>
            </div>
            <div class="sc-ctx">
              Monterrey venue wide · both South American / Caribbean teams
              physical in sideline battles
            </div>
            <span class="sc-conf conf-lo">Low</span>
          </div>
          <div class="sc">
            <div class="sc-name">Goal Kicks</div>
            <div class="sc-nums">
              <span class="sc-lo">10</span><span class="sc-sep">·</span
              ><span class="sc-med">16</span><span class="sc-sep">·</span
              ><span class="sc-hi">22</span>
            </div>
            <div class="sc-bar">
              <div class="scb-lo" style="width: 32%"></div>
              <div class="scb-hi" style="width: 56%"></div>
            </div>
            <div class="sc-ctx">
              Bolivia tend to launch long at sea level · Suriname GK under
              pressure → many GKs possible
            </div>
            <span class="sc-conf conf-lo">Low</span>
          </div>
          <div class="sc">
            <div class="sc-name">Tackles</div>
            <div class="sc-nums">
              <span class="sc-lo">18</span><span class="sc-sep">·</span
              ><span class="sc-med">26</span><span class="sc-sep">·</span
              ><span class="sc-hi">36</span>
            </div>
            <div class="sc-bar">
              <div class="scb-lo" style="width: 42%"></div>
              <div class="scb-hi" style="width: 66%"></div>
            </div>
            <div class="sc-ctx">
              Both physically combative styles · CONMEBOL vs CONCACAF = direct,
              powerful football · high tackle count expected
            </div>
            <span class="sc-conf conf-lo">Low</span>
          </div>
        </div>
        <div class="fc-ctx">
          <span class="fc-ctx-icon">◆</span>
          <p class="fc-ctx-text">
            <strong
              >Bolivia's famous altitude advantage is neutralised at sea level
              in Monterrey.</strong
            >
            <span class="cc-r">This is a major factor</span> — Bolivia at
            altitude are almost unbeatable; at sea level they're a very
            different proposition.
            <span class="cc-g"
              >Suriname are making history just being here</span
            >
            — a tiny nation (620k people) that upset multiple CONCACAF nations
            to qualify.
            <span class="cc-r">Stat confidence is LOW throughout</span> — very
            limited data on these two nations at this level.
          </p>
        </div>
        <div class="fc-conf">
          <span class="conf-badge cb-lo"
            ><span class="conf-dot cd-lo"></span>LOW confidence — limited
            data</span
          >
          <span class="conf-reason"
            >55% Bolivia but altitude neutralised · Suriname could shock · very
            limited historical data available</span
          >
        </div>
      </div>
    </div>
    <!-- /wrap -->

    <footer>
      <div class="ft-l">
        <strong>· Team Bilbo Statistical Analysis</strong> WORLD CUP 2026
        QUALIFIER PLAYOFFS · THURSDAY 26 MARCH 2026 ·<br />
        · 8 UEFA semi-finals · 2 FIFA intercontinental semi-finals ·<br />
        · Predictions based on Qualifying campaign data, with · <span class="sc-lo">Worst</span> · <span class="sc-med">Median</span> · <span class="sc-hi">Best</span> ranges ·
      </div>
      <div class="ft-r">WC2026 · 10 fixtures</div>
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
