<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Manchester United vs Leeds United | PL Stats Predictor — Roses Rivalry</title>
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link
        href="https://fonts.googleapis.com/css2?family=Space+Grotesk:wght@400;500;600;700&family=Inter:wght@300;400;500;600&display=swap"
        rel="stylesheet">
    <style>
        /* ══════════════════════════════════════════
   DESIGN TOKENS
══════════════════════════════════════════ */
        :root {
            --bg: #04060f;
            --bg-2: #080c19;
            --bg-3: #0e1324;
            --bg-4: #141a2e;
            --bg-5: #1a2138;
            --border: rgba(255, 255, 255, 0.07);
            --border-m: rgba(255, 255, 255, 0.13);
            --text: #c2ccdf;
            --muted: #4c5574;
            --hi: #8895b8;
            /* Man Utd */
            --mun-b: #DA291C;
            --mun-g: #ffffff;
            --mun-l: rgba(218, 41, 28, 0.22);
            /* Leeds */
            --lee-b: #FFCD00;
            --lee-g: #1D428A;
            --lee-l: rgba(255, 205, 0, 0.22);
            /* stat colours */
            --lo: #0fd9a2;
            --md: #f7c948;
            --hi-c: #f55929;
            /* danger */
            --danger: #ef4444;
            --warn: #f59e0b;
            --gold: #f5c842;
            --rad: 12px;
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
        }

        /* ══════════════════════════════════════════
   ANIMATIONS
══════════════════════════════════════════ */
        @keyframes fadeUp {
            from {
                opacity: 0;
                transform: translateY(22px);
            }

            to {
                opacity: 1;
                transform: translateY(0);
            }
        }

        @keyframes popIn {
            from {
                transform: scale(0.7);
                opacity: 0;
            }

            to {
                transform: scale(1);
                opacity: 1;
            }
        }

        @keyframes pulseRed {

            0%,
            100% {
                box-shadow: 0 0 0 0 rgba(239, 68, 68, 0);
            }

            60% {
                box-shadow: 0 0 0 8px rgba(239, 68, 68, 0.2);
            }
        }

        @keyframes shimmer {
            0% {
                background-position: -200% center;
            }

            100% {
                background-position: 200% center;
            }
        }

        .au1 {
            animation: fadeUp .5s ease both;
        }

        .au2 {
            animation: fadeUp .5s .1s ease both;
        }

        .au3 {
            animation: fadeUp .5s .2s ease both;
        }

        .pop {
            animation: popIn .5s cubic-bezier(.34, 1.56, .64, 1) both;
        }

        .pop2 {
            animation: popIn .5s .12s cubic-bezier(.34, 1.56, .64, 1) both;
        }

        /* ══════════════════════════════════════════
   BREAKING NEWS BANNER
══════════════════════════════════════════ */
        .breaking {
            background: linear-gradient(135deg, rgba(255, 205, 0, .18), rgba(255, 205, 0, .08));
            border-bottom: 2px solid rgba(255, 205, 0, .5);
            padding: 10px 16px;
            display: flex;
            align-items: center;
            gap: 10px;
        }

        .brk-icon {
            font-size: 18px;
            flex-shrink: 0;
        }

        .brk-text {
            font-size: 12.5px;
            line-height: 1.5;
        }

        .brk-text strong {
            color: #FFCD00;
            font-weight: 700;
        }

        .brk-text em {
            color: #fca5a5;
            font-style: normal;
        }

        /* ══════════════════════════════════════════
   SITE HEADER
══════════════════════════════════════════ */
        .site-header {
            background: linear-gradient(170deg, var(--mun-l) 0%, var(--bg-2) 45%, var(--lee-l) 100%);
            border-bottom: 1px solid var(--border-m);
            padding: 22px 16px 18px;
            text-align: center;
            position: relative;
            overflow: hidden;
        }

        .site-header::before {
            content: '';
            position: absolute;
            inset: 0;
            background: radial-gradient(ellipse 80% 250% at 50% -10%, rgba(218, 41, 28, .06), transparent 65%);
            pointer-events: none;
        }

        .pl-badge {
            display: inline-flex;
            align-items: center;
            gap: 7px;
            font-family: 'Space Grotesk', sans-serif;
            font-size: 10px;
            font-weight: 700;
            letter-spacing: 2px;
            text-transform: uppercase;
            color: var(--gold);
            background: rgba(245, 200, 66, .08);
            border: 1px solid rgba(245, 200, 66, .28);
            padding: 4px 13px;
            border-radius: 20px;
            margin-bottom: 11px;
        }

        .site-header h1 {
            font-family: 'Space Grotesk', sans-serif;
            font-size: 26px;
            font-weight: 700;
            color: #fff;
            text-transform: uppercase;
            letter-spacing: .5px;
            line-height: 1.1;
        }

        .site-header .sub {
            font-size: 12px;
            color: var(--muted);
            margin-top: 5px;
        }

        /* Title race context strip */
        .gap-strip {
            display: flex;
            justify-content: center;
            align-items: center;
            gap: 16px;
            flex-wrap: wrap;
            margin-top: 14px;
        }

        .gap-pill {
            display: flex;
            align-items: center;
            gap: 7px;
            font-family: 'Space Grotesk', sans-serif;
            font-size: 11px;
            font-weight: 600;
            padding: 6px 13px;
            border-radius: 8px;
            border: 1px solid;
        }

        .gp-mun {
            background: rgba(218, 41, 28, .1);
            border-color: rgba(218, 41, 28, .25);
            color: #ff7070;
        }

        .gp-lee {
            background: rgba(255, 205, 0, .1);
            border-color: rgba(255, 205, 0, .28);
            color: var(--lee-b);
        }

        .gp-gap {
            background: rgba(245, 200, 66, .08);
            border-color: rgba(245, 200, 66, .25);
            color: var(--gold);
        }

        .gp-pts {
            font-family: 'Space Grotesk', sans-serif;
            font-size: 16px;
            font-weight: 700;
        }

        /* ══════════════════════════════════════════
   HERO
══════════════════════════════════════════ */
        .hero-wrap {
            background: linear-gradient(135deg, rgba(218, 41, 28, .15) 0%, var(--bg-2) 45%, rgba(255, 205, 0, .12) 100%);
            border-bottom: 1px solid var(--border-m);
            padding: 24px 16px 20px;
            position: relative;
            overflow: hidden;
        }

        .hero-wrap::before {
            content: '';
            position: absolute;
            inset: 0;
            background: radial-gradient(ellipse 60% 80% at 50% 50%, rgba(255, 255, 255, .02), transparent 70%);
            pointer-events: none;
        }

        .hero-inner {
            max-width: 540px;
            margin: 0 auto;
            display: flex;
            align-items: center;
            justify-content: space-between;
            gap: 12px;
        }

        .h-team {
            display: flex;
            flex-direction: column;
            align-items: center;
            gap: 8px;
            flex: 1;
        }

        .badge-ring {
            width: 74px;
            height: 74px;
            border-radius: 50%;
            border: 1.5px solid var(--border-m);
            background: rgba(255, 255, 255, .04);
            display: flex;
            align-items: center;
            justify-content: center;
            overflow: hidden;
            filter: drop-shadow(0 4px 20px rgba(0, 0, 0, .7));
            transition: transform .35s cubic-bezier(.34, 1.56, .64, 1), filter .3s;
            cursor: default;
            flex-shrink: 0;
        }

        .badge-ring:hover {
            transform: scale(1.09) rotate(-2deg);
            filter: drop-shadow(0 6px 28px rgba(0, 0, 0, .85));
        }

        .badge-ring img {
            width: 52px;
            height: 52px;
            object-fit: contain;
        }

        .h-name {
            font-family: 'Space Grotesk', sans-serif;
            font-size: 13px;
            font-weight: 700;
            letter-spacing: .3px;
            text-transform: uppercase;
            text-align: center;
            color: #fff;
            line-height: 1.2;
        }

        .h-pos {
            font-size: 9px;
            color: var(--muted);
            text-transform: uppercase;
            letter-spacing: .5px;
            text-align: center;
        }

        .vs-col {
            display: flex;
            flex-direction: column;
            align-items: center;
            gap: 5px;
            flex-shrink: 0;
        }

        .vs-txt {
            font-family: 'Space Grotesk', sans-serif;
            font-size: 24px;
            font-weight: 700;
            color: rgba(255, 255, 255, .1);
            letter-spacing: 3px;
        }

        .ko-tag {
            font-family: 'Space Grotesk', sans-serif;
            font-size: 9px;
            font-weight: 700;
            letter-spacing: 1.5px;
            color: var(--gold);
            background: rgba(245, 200, 66, .1);
            border: 1px solid rgba(245, 200, 66, .25);
            padding: 2px 8px;
            border-radius: 4px;
        }

        .venue-txt {
            font-size: 9px;
            color: var(--muted);
            text-align: center;
            line-height: 1.5;
        }

        /* Title Race urgency bar */
        .urgency-bar {
            background: linear-gradient(135deg, rgba(245, 200, 66, .12), rgba(218, 41, 28, .08));
            border: 1px solid rgba(245, 200, 66, .25);
            border-radius: 9px;
            padding: 12px 16px;
            margin-top: 16px;
            max-width: 560px;
            margin-left: auto;
            margin-right: auto;
            text-align: center;
            font-size: 12px;
            line-height: 1.6;
        }

        .urgency-bar strong {
            color: var(--gold);
            font-weight: 700;
        }

        .urgency-bar em {
            color: #ff7070;
            font-style: normal;
        }

        /* ══════════════════════════════════════════
   SCORE PREDICTION
══════════════════════════════════════════ */
        .score-box {
            background: linear-gradient(135deg, var(--bg-3) 0%, var(--bg-4) 100%);
            border: 1px solid var(--border-m);
            border-radius: var(--rad);
            padding: 18px 16px;
            margin-bottom: 14px;
            display: flex;
            flex-direction: column;
            gap: 14px;
            transition: border-color .3s;
        }

        .score-box:hover {
            border-color: rgba(218, 41, 28, .35);
        }

        .score-box-title {
            font-family: 'Space Grotesk', sans-serif;
            font-size: 11px;
            font-weight: 700;
            letter-spacing: 2px;
            text-transform: uppercase;
            color: var(--muted);
            text-align: center;
            margin-bottom: 2px;
        }

        .scores-row {
            display: flex;
            gap: 12px;
            justify-content: center;
            flex-wrap: wrap;
        }

        .score-card {
            background: var(--bg-5);
            border: 1px solid var(--border);
            border-radius: 9px;
            padding: 14px 20px;
            text-align: center;
            flex: 1;
            min-width: 120px;
            max-width: 200px;
            transition: border-color .3s, transform .3s;
        }

        .score-card:hover {
            border-color: rgba(218, 41, 28, .4);
            transform: translateY(-2px);
        }

        .score-label {
            font-size: 9px;
            font-family: 'Space Grotesk', sans-serif;
            font-weight: 700;
            letter-spacing: 1.5px;
            text-transform: uppercase;
            color: var(--muted);
            margin-bottom: 8px;
        }

        .score-value {
            font-family: 'Space Grotesk', sans-serif;
            font-size: 34px;
            font-weight: 700;
            color: #fff;
            letter-spacing: 4px;
            line-height: 1;
        }

        .score-prob {
            font-size: 10px;
            color: var(--muted);
            margin-top: 6px;
        }

        .score-best {
            border-color: rgba(218, 41, 28, .4);
            background: linear-gradient(135deg, rgba(218, 41, 28, .08), var(--bg-5));
        }

        .score-best .score-label {
            color: #ff7070;
        }

        .score-notes {
            font-size: 11.5px;
            color: var(--hi);
            line-height: 1.6;
        }

        .score-notes strong {
            color: var(--gold);
        }

        /* ══════════════════════════════════════════
   PAGE & GRID
══════════════════════════════════════════ */
        .page {
            max-width: 700px;
            margin: 0 auto;
            padding: 18px 14px 56px;
        }

        /* card */
        .card {
            background: var(--bg-2);
            border: 1px solid var(--border);
            border-radius: var(--rad);
            overflow: hidden;
            margin-bottom: 14px;
            opacity: 0;
            transform: translateY(14px);
            transition: opacity .5s ease, transform .5s ease, border-color .3s;
        }

        .card.vis {
            opacity: 1;
            transform: translateY(0);
        }

        .card:hover {
            border-color: var(--border-m);
        }

        .card-hd {
            padding: 12px 16px 10px;
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
            font-family: 'Space Grotesk', sans-serif;
            font-size: 10px;
            font-weight: 700;
            letter-spacing: 2px;
            text-transform: uppercase;
            color: var(--muted);
            flex: 1;
        }

        .hd-tag {
            font-size: 9px;
            font-weight: 700;
            letter-spacing: .8px;
            text-transform: uppercase;
            padding: 2px 8px;
            border-radius: 3px;
            border: 1px solid;
        }

        .card-body {
            padding: 14px 16px;
        }

        /* callout */
        .callout {
            background: rgba(255, 255, 255, .022);
            border: 1px solid var(--border-m);
            border-radius: 8px;
            padding: 12px 14px;
            font-size: 12.5px;
            line-height: 1.7;
            color: var(--hi);
        }

        .callout strong {
            color: var(--gold);
            font-weight: 700;
        }

        /* form cols */
        .form-cols {
            display: flex;
            flex-direction: column;
            gap: 12px;
        }

        .team-lab {
            display: inline-flex;
            align-items: center;
            gap: 5px;
            font-size: 9.5px;
            font-weight: 700;
            letter-spacing: 1px;
            text-transform: uppercase;
            padding: 2px 8px 2px 4px;
            border-radius: 4px;
            margin-bottom: 7px;
            border: 1px solid;
        }

        .lab-mun {
            background: rgba(218, 41, 28, .12);
            color: #ff6b6b;
            border-color: rgba(218, 41, 28, .3);
        }

        .lab-lee {
            background: rgba(255, 205, 0, .1);
            color: var(--lee-b);
            border-color: rgba(255, 205, 0, .28);
        }

        .tl-img {
            width: 13px;
            height: 13px;
            object-fit: contain;
            border-radius: 50%;
        }

        .match-list {
            display: flex;
            flex-direction: column;
            gap: 3px;
        }

        .mr {
            display: grid;
            grid-template-columns: 6px 44px 1fr auto;
            align-items: center;
            gap: 8px;
            background: var(--bg-3);
            border: 1px solid var(--border);
            border-radius: 6px;
            padding: 6px 9px;
            transition: background .2s;
        }

        .mr:hover {
            background: var(--bg-4);
        }

        .rd {
            width: 6px;
            height: 6px;
            border-radius: 50%;
        }

        .rd.W {
            background: var(--lo);
            box-shadow: 0 0 5px rgba(15, 217, 162, .4);
        }

        .rd.D {
            background: var(--md);
        }

        .rd.L {
            background: var(--hi-c);
            box-shadow: 0 0 5px rgba(245, 89, 41, .4);
        }

        .ms {
            font-family: 'Space Grotesk', sans-serif;
            font-size: 14px;
            font-weight: 700;
            color: #fff;
            text-align: center;
        }

        .mo {
            font-size: 11.5px;
            color: var(--text);
            font-weight: 500;
            overflow: hidden;
            text-overflow: ellipsis;
            white-space: nowrap;
        }

        .mc {
            font-size: 9px;
            color: var(--muted);
            text-transform: uppercase;
            letter-spacing: .3px;
            text-align: right;
            white-space: nowrap;
        }

        .cup-note {
            font-size: 8.5px;
            color: var(--gold);
            font-style: italic;
        }

        .f-leg {
            display: flex;
            gap: 11px;
            flex-wrap: wrap;
            margin-top: 8px;
        }

        .fl {
            display: flex;
            align-items: center;
            gap: 4px;
            font-size: 10.5px;
            color: var(--muted);
        }

        .fl-dot {
            width: 6px;
            height: 6px;
            border-radius: 50%;
        }

        /* avg grid */
        .avg-pair {
            display: flex;
            flex-direction: column;
            gap: 11px;
        }

        .a-lbl {
            font-family: 'Space Grotesk', sans-serif;
            font-size: 9.5px;
            font-weight: 700;
            letter-spacing: 1.2px;
            text-transform: uppercase;
            margin-bottom: 7px;
        }

        .avg-grid {
            display: grid;
            grid-template-columns: repeat(4, 1fr);
            gap: 5px;
        }

        .ac {
            background: var(--bg-3);
            border: 1px solid var(--border);
            border-radius: 8px;
            padding: 9px 5px 7px;
            text-align: center;
            transition: border-color .2s, transform .2s;
        }

        .ac:hover {
            border-color: var(--border-m);
            transform: translateY(-1px);
        }

        .ac .val {
            font-family: 'Space Grotesk', sans-serif;
            font-size: 19px;
            font-weight: 700;
            color: #fff;
            line-height: 1;
        }

        .ac .lbl {
            font-size: 8.5px;
            color: var(--muted);
            margin-top: 2px;
            text-transform: uppercase;
            letter-spacing: .4px;
            line-height: 1.3;
        }

        /* h2h */
        .h2h-bar {
            background: var(--bg-3);
            border: 1px solid var(--border);
            border-radius: 8px;
            padding: 12px 10px;
            display: flex;
            align-items: center;
            justify-content: space-between;
            gap: 4px;
        }

        .hs {
            text-align: center;
            flex: 1;
        }

        .hn {
            font-family: 'Space Grotesk', sans-serif;
            font-size: 26px;
            font-weight: 700;
            line-height: 1;
        }

        .hl {
            font-size: 9px;
            color: var(--muted);
            text-transform: uppercase;
            letter-spacing: .6px;
            margin-top: 2px;
        }

        .hdv {
            width: 1px;
            height: 34px;
            background: var(--border);
            flex-shrink: 0;
        }

        .h2h-rows {
            display: flex;
            flex-direction: column;
            gap: 3px;
            margin-top: 10px;
        }

        .h2h-r {
            display: grid;
            grid-template-columns: 1fr auto 1fr;
            align-items: center;
            gap: 8px;
            background: var(--bg-4);
            border: 1px solid var(--border);
            border-radius: 6px;
            padding: 6px 9px;
            transition: background .2s;
        }

        .h2h-r:hover {
            background: var(--bg-5);
        }

        .rh {
            font-size: 11.5px;
            font-weight: 600;
            color: var(--text);
            text-align: left;
            white-space: nowrap;
            overflow: hidden;
            text-overflow: ellipsis;
        }

        .rs {
            font-family: 'Space Grotesk', sans-serif;
            font-size: 14px;
            font-weight: 700;
            color: #fff;
            text-align: center;
            white-space: nowrap;
        }

        .ra {
            font-size: 11.5px;
            font-weight: 600;
            color: var(--text);
            text-align: right;
            white-space: nowrap;
            overflow: hidden;
            text-overflow: ellipsis;
        }

        .rsub {
            font-size: 9px;
            color: var(--muted);
            text-transform: uppercase;
            letter-spacing: .3px;
            grid-column: 1/-1;
            text-align: center;
            margin-top: -2px;
        }

        .h2h-winner-tag {
            font-size: 8.5px;
            background: rgba(218, 41, 28, .15);
            color: #ff7070;
            padding: 1px 5px;
            border-radius: 3px;
            white-space: nowrap;
        }

        /* pred table */
        .pred-leg {
            display: flex;
            gap: 14px;
            flex-wrap: wrap;
            margin-bottom: 13px;
        }

        .pli {
            display: flex;
            align-items: center;
            gap: 5px;
            font-size: 10.5px;
            color: var(--muted);
        }

        .pld {
            width: 7px;
            height: 7px;
            border-radius: 50%;
        }

        .pw {
            overflow-x: auto;
            -webkit-overflow-scrolling: touch;
        }

        .pt {
            width: 100%;
            border-collapse: collapse;
            table-layout: fixed;
            min-width: 290px;
            background-color: #080c19;
        }

        .pt col.cm {
            width: 28%;
        }

        .pt col.cl {
            width: 16%;
        }

        .pt col.cn {
            width: 16%;
        }

        .pt col.ch {
            width: 16%;
        }

        .pt col.cb {
            width: 24%;
        }

        .pt thead th {
            font-family: 'Space Grotesk', sans-serif;
            font-size: 9px;
            font-weight: 700;
            letter-spacing: 1.5px;
            text-transform: uppercase;
            color: var(--muted);
            padding: 0 0 9px;
            text-align: left;
            white-space: nowrap;
            overflow: hidden;
        }

        .pt thead th:not(:first-child) {
            text-align: center;
        }

        .pt thead th.th-m {
            color: var(--md);
        }

        .pt tbody td {
            padding: 7px 3px;
            border-bottom: 1px solid rgba(255, 255, 255, .035);
            vertical-align: middle;
            overflow: hidden;
        }

        .pt tbody tr:last-child td {
            border-bottom: none;
        }

        .pt tbody tr:hover td {
            background: rgba(255, 255, 255, .02);
        }

        .pt tbody td.cmc {
            color: var(--hi);
            font-size: 12.5px;
            padding-left: 0;
            font-weight: 500;
        }

        .pt tbody td:not(.cmc) {
            text-align: center;
        }

        .lv {
            font-family: 'Space Grotesk', sans-serif;
            font-size: 17px;
            font-weight: 700;
            color: var(--lo);
            line-height: 1;
        }

        .mv {
            font-family: 'Space Grotesk', sans-serif;
            font-size: 17px;
            font-weight: 700;
            color: var(--md);
            line-height: 1;
        }

        .hv {
            font-family: 'Space Grotesk', sans-serif;
            font-size: 17px;
            font-weight: 700;
            color: var(--hi-c);
            line-height: 1;
        }

        /* animated bar */
        .bw {
            width: 85%;
            max-width: 92px;
            height: 5px;
            background: rgba(255, 255, 255, .06);
            border-radius: 3px;
            overflow: hidden;
            margin: 0 auto;
            display: block;
        }

        .bf {
            display: block;
            height: 100%;
            border-radius: 3px;
            width: 0;
            transition: width 1.3s cubic-bezier(.25, .46, .45, .94);
        }

        .bf-mun {
            background: linear-gradient(90deg, #DA291C, #FFCD00);
        }

        /* yellow cards */
        .yc-grid {
            display: flex;
            flex-direction: column;
            gap: 7px;
        }

        .yc-row {
            display: flex;
            align-items: flex-start;
            gap: 9px;
            background: var(--bg-3);
            border: 1px solid var(--border);
            border-radius: 8px;
            padding: 9px 11px;
            transition: border-color .25s, transform .25s;
        }

        .yc-row:hover {
            border-color: rgba(255, 224, 51, .2);
            transform: translateX(3px);
        }

        .yc-icon {
            font-size: 16px;
            flex-shrink: 0;
            margin-top: 1px;
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
            font-size: 9px;
            font-family: 'Space Grotesk', sans-serif;
            letter-spacing: .7px;
            text-transform: uppercase;
        }

        .yc-reason {
            font-size: 11px;
            color: var(--muted);
            margin-top: 2px;
            line-height: 1.45;
        }

        .yc-risk {
            font-family: 'Space Grotesk', sans-serif;
            font-size: 9px;
            font-weight: 700;
            letter-spacing: 1px;
            text-transform: uppercase;
            padding: 2px 8px;
            border-radius: 4px;
            flex-shrink: 0;
            align-self: center;
        }

        .risk-h {
            background: rgba(245, 89, 41, .13);
            color: var(--hi-c);
            border: 1px solid rgba(245, 89, 41, .28);
        }

        .risk-m {
            background: rgba(247, 201, 72, .1);
            color: var(--md);
            border: 1px solid rgba(247, 201, 72, .25);
        }

        /* notes */
        .note {
            margin-bottom: 9px;
            font-size: 12.5px;
            line-height: 1.65;
            color: var(--hi);
        }

        .note:last-child {
            margin-bottom: 0;
        }

        .note strong {
            color: var(--gold);
            font-weight: 700;
        }

        /* footer */
        footer {
            text-align: center;
            padding: 18px 14px;
            font-size: 11.5px;
            color: var(--muted);
            border-top: 1px solid var(--border);
        }

        /* ═══ TABLET 640px+ ═══ */
        @media(min-width:640px) {
            body {
                font-size: 15px;
            }

            .page {
                max-width: 920px;
                padding: 22px 24px 62px;
            }

            .site-header {
                padding: 26px 24px 22px;
            }

            .site-header h1 {
                font-size: 32px;
            }

            .hero-wrap {
                padding: 28px 24px 22px;
            }

            .hero-inner {
                max-width: 620px;
            }

            .badge-ring {
                width: 86px;
                height: 86px;
            }

            .badge-ring img {
                width: 62px;
                height: 62px;
            }

            .h-name {
                font-size: 15px;
            }

            .vs-txt {
                font-size: 30px;
            }

            .card-hd {
                padding: 13px 20px 11px;
            }

            .card-body {
                padding: 16px 20px;
            }

            .form-cols {
                flex-direction: row;
                gap: 16px;
            }

            .fcol {
                flex: 1;
                min-width: 0;
            }

            .avg-pair {
                flex-direction: row;
                gap: 16px;
            }

            .a-grp {
                flex: 1;
            }

            .ac .val {
                font-size: 21px;
            }

            .hn {
                font-size: 30px;
            }

            .lv,
            .mv,
            .hv {
                font-size: 20px;
            }

            .pt tbody td {
                padding: 8px 4px;
            }

            .bw {
                max-width: 110px;
                height: 5px;
            }

            .callout {
                font-size: 13.5px;
            }

            .note {
                font-size: 13.5px;
            }

            .score-value {
                font-size: 42px;
            }
        }

        /* ═══ DESKTOP 1040px+ ═══ */
        @media(min-width:1040px) {
            .page {
                max-width: 1380px;
                padding: 28px 40px 70px;
            }

            .site-header {
                padding: 28px 40px 24px;
            }

            .site-header h1 {
                font-size: 38px;
            }

            .hero-wrap {
                padding: 28px 40px 22px;
            }

            .hero-inner {
                max-width: 680px;
            }

            .badge-ring {
                width: 94px;
                height: 94px;
            }

            .badge-ring img {
                width: 68px;
                height: 68px;
            }

            .dg {
                display: grid;
                grid-template-columns: 1fr 1fr;
                gap: 20px;
                align-items: start;
            }

            .dg .fw {
                grid-column: 1/-1;
            }

            .card-hd {
                padding: 14px 22px 12px;
            }

            .card-body {
                padding: 18px 22px;
            }

            .ac .val {
                font-size: 23px;
            }

            .lv,
            .mv,
            .hv {
                font-size: 21px;
            }

            .hn {
                font-size: 32px;
            }

            .bw {
                max-width: 100px;
            }
        }

        /* ═══ WIDE 1360px+ ═══ */
        @media(min-width:1360px) {
            .page {
                max-width: 1520px;
                padding: 32px 60px 78px;
            }

            .site-header {
                padding: 30px 60px 24px;
            }

            .hero-wrap {
                padding: 30px 60px 22px;
            }

            .hero-inner {
                max-width: 750px;
            }

            .dg {
                gap: 26px;
            }
        }
    </style>
</head>

<body>

    <div class="breaking au1">
        <div class="brk-icon">🚨</div>
        <div class="brk-text">
            <strong>CONTEXT — The Roses Rivalry Returns.</strong>
            <em> Leeds United are fighting for survival, sitting 15th on 33 points, while Michael Carrick's Manchester
                United look to cement 3rd place on 55 points. Leeds have failed to score in 4 consecutive league
                matches.</em>
        </div>
    </div>

    <header class="site-header au2">
        <div class="pl-badge">Premier League · Matchweek 32 · Monday Night Football · 13 April 2026</div>
        <h1>Team Bilbo Analytics</h1>
        <p class="sub">· Old Trafford &nbsp;·&nbsp; 8:00pm BST &nbsp;·&nbsp; Rivalry Fixture &nbsp;·</p>

        <div class="gap-strip">
            <div class="gap-pill gp-mun"><span>Man Utd</span><span class="gp-pts" style="color:#ff7070">55
                    pts</span><span style="font-size:9px;color:#fca5a5">3rd Place</span></div>
            <div class="gap-pill gp-gap">→ <span style="font-size:8px">THE ROSES RIVALRY</span> ←</div>
            <div class="gap-pill gp-lee"><span>Leeds Utd</span><span class="gp-pts" style="color:var(--lee-b)">33
                    pts</span><span style="font-size:9px;color:rgba(255,205,0,.7)">15th Place</span></div>
        </div>
    </header>

    <div class="hero-wrap au3">
        <div class="hero-inner">

            <div class="h-team">
                <div class="badge-ring pop">
                    <img src="https://upload.wikimedia.org/wikipedia/en/thumb/7/7a/Manchester_United_FC_crest.svg/120px-Manchester_United_FC_crest.svg.png"
                        alt="Manchester United F.C." style="background-color: transparent;"
                        onerror="this.parentElement.innerHTML='<svg viewBox=&quot;0 0 60 60&quot; style=&quot;width:52px;height:52px&quot;><circle cx=&quot;30&quot; cy=&quot;30&quot; r=&quot;28&quot; fill=&quot;#DA291C&quot;/><text x=&quot;30&quot; y=&quot;35&quot; text-anchor=&quot;middle&quot; font-size=&quot;11&quot; fill=&quot;#fff&quot; font-weight=&quot;bold&quot;>MUFC</text></svg>'">
                </div>
                <div class="h-name">Manchester United</div>
                <div class="h-pos">3rd · 55 pts<br>Top 4 Push</div>
            </div>

            <div class="vs-col">
                <div class="vs-txt">VS</div>
                <div class="ko-tag">20:00</div>
                <div class="venue-txt">Old Trafford<br>Manchester · Mon 13 Apr</div>
            </div>

            <div class="h-team">
                <div class="badge-ring pop2">
                    <img src="https://upload.wikimedia.org/wikipedia/en/thumb/5/54/Leeds_United_F.C._logo.svg/120px-Leeds_United_F.C._logo.svg.png"
                        alt="Leeds United" style="background-color: transparent;"
                        onerror="this.parentElement.innerHTML='<svg viewBox=&quot;0 0 60 60&quot; style=&quot;width:52px;height:52px&quot;><circle cx=&quot;30&quot; cy=&quot;30&quot; r=&quot;28&quot; fill=&quot;#FFCD00&quot;/><text x=&quot;30&quot; y=&quot;35&quot; text-anchor=&quot;middle&quot; font-size=&quot;11&quot; fill=&quot;#1D428A&quot; font-weight=&quot;bold&quot;>LUFC</text></svg>'">
                </div>
                <div class="h-name">Leeds United</div>
                <div class="h-pos">15th · 33 pts<br>Relegation Battle</div>
            </div>

        </div>

        <div class="urgency-bar">
            <strong>Contrasting fortunes.</strong> Manchester United are undefeated in their last 11 games against
            Leeds. Meanwhile, Leeds are desperate for points to stave off relegation, but haven't scored a Premier
            League goal in their last 4 outings.
        </div>
    </div>

    <div class="page">
        <div class="dg">

            <div class="score-box fw">
                <div class="score-box-title">Score Predictions — Based on Last 10 Matches & H2H</div>
                <div class="scores-row">
                    <div class="score-card">
                        <div class="score-label">Half-Time</div>
                        <div class="score-value" style="color:#ff7070">1 – 0</div>
                        <div class="score-prob" style="color:var(--mun-b)">Man Utd · Control early</div>
                    </div>
                    <div class="score-card score-best">
                        <div class="score-label">Full-Time Best Pick</div>
                        <div class="score-value" style="color:#ff7070">2 – 0</div>
                        <div class="score-prob" style="color:var(--mun-b)">Man Utd win · ~65% probability</div>
                    </div>
                    <div class="score-card">
                        <div class="score-label">Alternative</div>
                        <div class="score-value" style="color:var(--md)">1 – 1</div>
                        <div class="score-prob">Draw · ~20% probability</div>
                    </div>
                </div>
                <div class="score-notes">
                    <strong>Why Man Utd win is the weighted pick:</strong> Manchester United have not lost at home in 9
                    consecutive league games, while Leeds are winless in 12 away. Leeds' attacking struggles (0 goals in
                    4 league games) heavily factor into the predicted clean sheet for the home side. The 1-1 draw in
                    January 2026 shows Leeds can occasionally frustrate United, but Old Trafford gives Carrick's men a
                    significant edge.
                </div>
            </div>

            <div class="card fw">
                <div class="card-hd">
                    <div class="hd-dot" style="background:var(--gold)"></div>
                    <div class="hd-title">Match Context</div>
                    <div class="hd-tag"
                        style="color:var(--gold);border-color:rgba(245,200,66,.28);background:rgba(245,200,66,.07)">The
                        Roses Rivalry</div>
                </div>
                <div class="card-body">
                    <div class="callout">
                        <strong>A rivalry renewed with stakes at both ends of the table.</strong> Michael Carrick has
                        Manchester United functioning efficiently in the league, pushing for a Champions League spot.
                        They have had plenty of rest following their 2-2 draw with Bournemouth on March 21. Conversely,
                        Daniel Farke's Leeds sit dangerously close to the relegation zone in 15th. Despite an uplifting
                        penalty shoot-out win over West Ham to reach the FA Cup semi-finals recently, their league
                        survival is on the line.
                    </div>
                </div>
            </div>

            <div class="card fw">
                <div class="card-hd">
                    <div class="hd-dot" style="background:#ff7070"></div>
                    <div class="hd-title">Recent Form (Last 5 Displayed from 10-Match Sample)</div>
                </div>
                <div class="card-body">
                    <div class="form-cols">

                        <div class="fcol">
                            <div class="team-lab lab-mun">
                                <img class="tl-img"
                                    src="https://upload.wikimedia.org/wikipedia/en/thumb/7/7a/Manchester_United_FC_crest.svg/120px-Manchester_United_FC_crest.svg.png"
                                    alt="" style="background-color: transparent;">
                                Man Utd
                            </div>
                            <div class="match-list">
                                <div class="mr">
                                    <div class="rd D"></div>
                                    <div class="ms">2–2</div>
                                    <div class="mo">Bournemouth</div>
                                    <div class="mc">PL <span class="cup-note">Mar 20</span></div>
                                </div>
                                <div class="mr">
                                    <div class="rd W"></div>
                                    <div class="ms">3–1</div>
                                    <div class="mo">Aston Villa</div>
                                    <div class="mc">PL</div>
                                </div>
                                <div class="mr">
                                    <div class="rd L"></div>
                                    <div class="ms">1–2</div>
                                    <div class="mo">Newcastle</div>
                                    <div class="mc">PL</div>
                                </div>
                                <div class="mr">
                                    <div class="rd W"></div>
                                    <div class="ms">2–1</div>
                                    <div class="mo">Crystal Palace</div>
                                    <div class="mc">PL</div>
                                </div>
                                <div class="mr">
                                    <div class="rd W"></div>
                                    <div class="ms">1–0</div>
                                    <div class="mo">Everton</div>
                                    <div class="mc">PL</div>
                                </div>
                            </div>
                            <p style="font-size:10px;color:var(--muted);margin-top:7px;">Form from last 10: Mixed but
                                strong at home.</p>
                        </div>

                        <div class="fcol">
                            <div class="team-lab lab-lee">
                                <img class="tl-img"
                                    src="https://upload.wikimedia.org/wikipedia/en/thumb/5/54/Leeds_United_F.C._logo.svg/120px-Leeds_United_F.C._logo.svg.png"
                                    alt="" style="background-color: transparent;">
                                Leeds Utd
                            </div>
                            <div class="match-list">
                                <div class="mr">
                                    <div class="rd D"></div>
                                    <div class="ms">2–2</div>
                                    <div class="mo">West Ham</div>
                                    <div class="mc">FAC <span class="cup-note">Apr 5</span></div>
                                </div>
                                <div class="mr">
                                    <div class="rd D"></div>
                                    <div class="ms">0–0</div>
                                    <div class="mo">Brentford</div>
                                    <div class="mc">PL</div>
                                </div>
                                <div class="mr">
                                    <div class="rd D"></div>
                                    <div class="ms">0–0</div>
                                    <div class="mo">Crystal Palace</div>
                                    <div class="mc">PL</div>
                                </div>
                                <div class="mr">
                                    <div class="rd W"></div>
                                    <div class="ms">3–0</div>
                                    <div class="mo">Norwich</div>
                                    <div class="mc">FAC</div>
                                </div>
                                <div class="mr">
                                    <div class="rd L"></div>
                                    <div class="ms">0–1</div>
                                    <div class="mo">Sunderland</div>
                                    <div class="mc">PL</div>
                                </div>
                            </div>
                            <p style="font-size:10px;color:var(--muted);margin-top:7px;">Form from last 10: Solid in
                                cups, struggling to score in league.</p>
                        </div>

                    </div>
                    <div class="f-leg">
                        <div class="fl">
                            <div class="fl-dot" style="background:var(--lo)"></div>Win
                        </div>
                        <div class="fl">
                            <div class="fl-dot" style="background:var(--md)"></div>Draw
                        </div>
                        <div class="fl">
                            <div class="fl-dot" style="background:var(--hi-c)"></div>Loss
                        </div>
                    </div>
                </div>
            </div>

            <div class="card fw">
                <div class="card-hd">
                    <div class="hd-dot" style="background:#a78bfa"></div>
                    <div class="hd-title">Rolling Averages per Match — Last 10 Games</div>
                </div>
                <div class="card-body">
                    <div class="avg-pair">
                        <div class="a-grp">
                            <div class="a-lbl" style="color:#ff7070">Man Utd — Last 10</div>
                            <div class="avg-grid">
                                <div class="ac">
                                    <div class="val">14.5</div>
                                    <div class="lbl">Shots</div>
                                </div>
                                <div class="ac">
                                    <div class="val">5.1</div>
                                    <div class="lbl">SOT</div>
                                </div>
                                <div class="ac">
                                    <div class="val">6.2</div>
                                    <div class="lbl">Corners</div>
                                </div>
                                <div class="ac">
                                    <div class="val">11.4</div>
                                    <div class="lbl">Fouls</div>
                                </div>
                            </div>
                            <div class="avg-grid" style="margin-top:5px">
                                <div class="ac">
                                    <div class="val">58%</div>
                                    <div class="lbl">Possession</div>
                                </div>
                                <div class="ac">
                                    <div class="val">1.8</div>
                                    <div class="lbl">Goals/Gm</div>
                                </div>
                                <div class="ac">
                                    <div class="val">4.1</div>
                                    <div class="lbl">Corners vs</div>
                                </div>
                                <div class="ac">
                                    <div class="val">+13</div>
                                    <div class="lbl">Season GD</div>
                                </div>
                            </div>
                        </div>
                        <div class="a-grp">
                            <div class="a-lbl" style="color:var(--lee-b)">Leeds Utd — Last 10</div>
                            <div class="avg-grid">
                                <div class="ac">
                                    <div class="val">10.2</div>
                                    <div class="lbl">Shots</div>
                                </div>
                                <div class="ac">
                                    <div class="val">3.4</div>
                                    <div class="lbl">SOT</div>
                                </div>
                                <div class="ac">
                                    <div class="val">4.5</div>
                                    <div class="lbl">Corners</div>
                                </div>
                                <div class="ac">
                                    <div class="val">12.8</div>
                                    <div class="lbl">Fouls</div>
                                </div>
                            </div>
                            <div class="avg-grid" style="margin-top:5px">
                                <div class="ac">
                                    <div class="val">46%</div>
                                    <div class="lbl">Possession</div>
                                </div>
                                <div class="ac">
                                    <div class="val">0.7</div>
                                    <div class="lbl">Goals/Gm</div>
                                </div>
                                <div class="ac">
                                    <div class="val">5.8</div>
                                    <div class="lbl">Corners vs</div>
                                </div>
                                <div class="ac">
                                    <div class="val">-11</div>
                                    <div class="lbl">Season GD</div>
                                </div>
                            </div>
                        </div>
                    </div>
                </div>
            </div>

            <div class="card fw">
                <div class="card-hd">
                    <div class="hd-dot" style="background:var(--hi-c)"></div>
                    <div class="hd-title">Head to Head — Last 5 Meetings</div>
                </div>
                <div class="card-body">
                    <div class="h2h-bar">
                        <div class="hs">
                            <div class="hn" style="color:#ff7070">3</div>
                            <div class="hl">Man Utd Wins</div>
                        </div>
                        <div class="hdv"></div>
                        <div class="hs">
                            <div class="hn" style="color:var(--md)">2</div>
                            <div class="hl">Draws</div>
                        </div>
                        <div class="hdv"></div>
                        <div class="hs">
                            <div class="hn" style="color:var(--lee-b)">0</div>
                            <div class="hl">Leeds Wins</div>
                        </div>
                        <div class="hdv"></div>
                        <div class="hs">
                            <div class="hn">3.6</div>
                            <div class="hl">Avg Goals/Gm</div>
                        </div>
                    </div>
                    <p style="font-size:10.5px;color:var(--muted);margin-top:8px;margin-bottom:8px;">Man Utd are
                        unbeaten against Leeds in their last 11 games across all competitions. Their encounters are
                        historically high-scoring, though the last two meetings were tighter.</p>
                    <div class="h2h-rows">
                        <div class="h2h-r">
                            <div class="rh">Leeds Utd</div>
                            <div class="rs">1–1 &nbsp;<span class="h2h-winner-tag"
                                    style="background:var(--md); color:#000;">D</span></div>
                            <div class="ra">Man Utd</div>
                            <div class="rsub">PL · Elland Road · Jan 4, 2026</div>
                        </div>
                        <div class="h2h-r">
                            <div class="rh">Leeds Utd</div>
                            <div class="rs">0–2 &nbsp;<span class="h2h-winner-tag">Utd W</span></div>
                            <div class="ra">Man Utd</div>
                            <div class="rsub">PL · Elland Road · Feb 12, 2023</div>
                        </div>
                        <div class="h2h-r">
                            <div class="rh">Man Utd</div>
                            <div class="rs">2–2 &nbsp;<span class="h2h-winner-tag"
                                    style="background:var(--md); color:#000;">D</span></div>
                            <div class="ra">Leeds Utd</div>
                            <div class="rsub">PL · Old Trafford · Feb 8, 2023</div>
                        </div>
                        <div class="h2h-r">
                            <div class="rh">Leeds Utd</div>
                            <div class="rs">2–4 &nbsp;<span class="h2h-winner-tag">Utd W</span></div>
                            <div class="ra">Man Utd</div>
                            <div class="rsub">PL · Elland Road · Feb 20, 2022</div>
                        </div>
                        <div class="h2h-r">
                            <div class="rh">Man Utd</div>
                            <div class="rs">5–1 &nbsp;<span class="h2h-winner-tag">Utd W</span></div>
                            <div class="ra">Leeds Utd</div>
                            <div class="rsub">PL · Old Trafford · Aug 14, 2021</div>
                        </div>
                    </div>
                </div>
            </div>

            <div class="card fw" id="pred-card">
                <div class="card-hd">
                    <div class="hd-dot" style="background:var(--lo)"></div>
                    <div class="hd-title">Weighted Predictions — Match Aggregates (Both Teams)</div>
                </div>
                <div class="card-body">
                    <div class="pred-leg">
                        <div class="pli">
                            <div class="pld" style="background:var(--lo)"></div><span
                                style="color:var(--lo);font-weight:700">Low</span> = floor
                        </div>
                        <div class="pli">
                            <div class="pld" style="background:var(--md)"></div><span
                                style="color:var(--md);font-weight:700">Median</span> = weighted expected
                        </div>
                        <div class="pli">
                            <div class="pld" style="background:var(--hi-c)"></div><span
                                style="color:var(--hi-c);font-weight:700">High</span> = ceiling
                        </div>
                    </div>
                    <div class="pw">
                        <table class="pt">
                            <colgroup>
                                <col class="cm">
                                <col class="cl">
                                <col class="cn">
                                <col class="ch">
                                <col class="cb">
                            </colgroup>
                            <thead>
                                <tr>
                                    <th>Metric</th>
                                    <th style="color:var(--lo)">Low</th>
                                    <th class="th-m">Median</th>
                                    <th style="color:var(--hi-c)">High</th>
                                    <th style="text-align:center;color:var(--muted)">Intensity</th>
                                </tr>
                            </thead>
                            <tbody>
                                <tr>
                                    <td class="cmc">Corners</td>
                                    <td><span class="lv">8</span></td>
                                    <td><span class="mv">10</span></td>
                                    <td><span class="hv">14</span></td>
                                    <td>
                                        <div class="bw">
                                            <div class="bf bf-mun" data-pct="55"></div>
                                        </div>
                                    </td>
                                </tr>
                                <tr>
                                    <td class="cmc">Total Shots</td>
                                    <td><span class="lv">22</span></td>
                                    <td><span class="mv">25</span></td>
                                    <td><span class="hv">32</span></td>
                                    <td>
                                        <div class="bw">
                                            <div class="bf bf-mun" data-pct="65"></div>
                                        </div>
                                    </td>
                                </tr>
                                <tr>
                                    <td class="cmc">Shots on Target</td>
                                    <td><span class="lv">6</span></td>
                                    <td><span class="mv">9</span></td>
                                    <td><span class="hv">13</span></td>
                                    <td>
                                        <div class="bw">
                                            <div class="bf bf-mun" data-pct="58"></div>
                                        </div>
                                    </td>
                                </tr>
                                <tr>
                                    <td class="cmc">Fouls</td>
                                    <td><span class="lv">21</span></td>
                                    <td><span class="mv">25</span></td>
                                    <td><span class="hv">31</span></td>
                                    <td>
                                        <div class="bw">
                                            <div class="bf bf-mun" data-pct="82"></div>
                                        </div>
                                    </td>
                                </tr>
                                <tr>
                                    <td class="cmc">Throw-ins</td>
                                    <td><span class="lv">34</span></td>
                                    <td><span class="mv">40</span></td>
                                    <td><span class="hv">48</span></td>
                                    <td>
                                        <div class="bw">
                                            <div class="bf bf-mun" data-pct="68"></div>
                                        </div>
                                    </td>
                                </tr>
                                <tr>
                                    <td class="cmc">Goal Kicks</td>
                                    <td><span class="lv">13</span></td>
                                    <td><span class="mv">17</span></td>
                                    <td><span class="hv">22</span></td>
                                    <td>
                                        <div class="bw">
                                            <div class="bf bf-mun" data-pct="52"></div>
                                        </div>
                                    </td>
                                </tr>
                                <tr>
                                    <td class="cmc">Tackles</td>
                                    <td><span class="lv">28</span></td>
                                    <td><span class="mv">36</span></td>
                                    <td><span class="hv">46</span></td>
                                    <td>
                                        <div class="bw">
                                            <div class="bf bf-mun" data-pct="78"></div>
                                        </div>
                                    </td>
                                </tr>
                                <tr>
                                    <td class="cmc">Offsides</td>
                                    <td><span class="lv">2</span></td>
                                    <td><span class="mv">4</span></td>
                                    <td><span class="hv">7</span></td>
                                    <td>
                                        <div class="bw">
                                            <div class="bf bf-mun" data-pct="45"></div>
                                        </div>
                                    </td>
                                </tr>
                            </tbody>
                        </table>
                    </div>
                </div>
            </div>

            <div class="card fw">
                <div class="card-hd">
                    <div class="hd-dot" style="background:#ffe033"></div>
                    <div class="hd-title">🟨 Yellow Card Risk Players</div>
                    <div class="hd-tag"
                        style="color:var(--md);border-color:rgba(247,201,72,.28);background:rgba(247,201,72,.08)">High
                        Rivalry Tension</div>
                </div>
                <div class="card-body">
                    <div class="yc-grid">

                        <div class="yc-row">
                            <div class="yc-icon">🟨</div>
                            <div class="yc-info">
                                <div class="yc-name">Casemiro <span class="yc-club" style="color:#ff7070">Man Utd ·
                                        DM</span></div>
                                <div class="yc-reason">The midfield anchor for Michael Carrick's side. Often responsible
                                    for tactical fouls to prevent counter-attacks from deep. In a high-stakes rivalry
                                    game, he is heavily prone to committing aggressive challenges.</div>
                            </div>
                            <div class="yc-risk risk-h">HIGH</div>
                        </div>

                        <div class="yc-row">
                            <div class="yc-icon">🟨</div>
                            <div class="yc-info">
                                <div class="yc-name">Junior Firpo <span class="yc-club" style="color:var(--lee-b)">Leeds
                                        Utd · LB</span></div>
                                <div class="yc-reason">Leeds will be under pressure for long periods, and Firpo will
                                    have to deal with the tricky wide play of United's attackers. Historically
                                    accumulates cards against quick, direct wingers.</div>
                            </div>
                            <div class="yc-risk risk-h">HIGH</div>
                        </div>

                        <div class="yc-row">
                            <div class="yc-icon">🟨</div>
                            <div class="yc-info">
                                <div class="yc-name">Bruno Fernandes <span class="yc-club" style="color:#ff7070">Man Utd
                                        · CAM</span></div>
                                <div class="yc-reason">A vital cog for United's midfield control. Prone to bookings for
                                    dissent when referee decisions don't go his way. The hostility of this rivalry
                                    usually brings out his more combative side.</div>
                            </div>
                            <div class="yc-risk risk-m">MED</div>
                        </div>

                        <div class="yc-row">
                            <div class="yc-icon">🟨</div>
                            <div class="yc-info">
                                <div class="yc-name">Ethan Ampadu <span class="yc-club" style="color:var(--lee-b)">Leeds
                                        Utd · CDM/CB</span></div>
                                <div class="yc-reason">The defensive shield for Leeds who has to break up play. Playing
                                    in the center of the park against Man Utd's dynamic runners means he will likely
                                    need to make professional fouls.</div>
                            </div>
                            <div class="yc-risk risk-m">MED</div>
                        </div>

                    </div>
                </div>
            </div>

            <div class="card fw">
                <div class="card-hd">
                    <div class="hd-dot" style="background:#60a5fa"></div>
                    <div class="hd-title">Analytical Notes — Weighting Factors</div>
                </div>
                <div class="card-body">

                    <div class="note"><strong>🔴 The Relegation vs Top 4 Dynamic:</strong> Leeds come into this game
                        absolutely needing a result to climb away from 15th place on 33 points. However, their attack
                        has entirely stagnated, going four consecutive Premier League games without a goal. Manchester
                        United are comfortable in 3rd on 55 points and have turned Old Trafford back into a fortress
                        under Michael Carrick. The home win is heavily favored.</div>

                    <div class="note"><strong>Fouls & Tackles Spike:</strong> The Roses Rivalry historically inflates
                        physical metrics. With Leeds fighting for survival and this being a major derby, the median
                        projection for fouls is weighted upwards to 25. Tackles are also expected to sit around 36 as
                        Leeds will likely cede possession and try to disrupt United's rhythm.</div>

                    <div class="note"><strong>Goals & Shots:</strong> While historical encounters between these two have
                        featured high-scoring anomalies (e.g. 5-1, 4-2), Leeds' recent defensive resilience under Daniel
                        Farke (evident in their 0-0 draws with Brentford and Palace) suggests a tighter match. We
                        project Man Utd to control possession and shots (weighted median of 25 combined), but the goal
                        count to be lower than historic averages.</div>

                </div>
            </div>

        </div>
    </div>
    <footer>
        <strong>Team Bilbo Statistical Analysis</strong><br>Predictions are statistical estimates based on actual data,
        rolling 10-match trends, and contextual rivalry factors. <strong>Not financial advice.</strong><br> · 13 April
        2026 ·

        <script>
            (function () {
                'use strict';

                /* scroll reveal cards */
                var cards = document.querySelectorAll('.card');
                if ('IntersectionObserver' in window) {
                    var obs = new IntersectionObserver(function (entries) {
                        entries.forEach(function (e) {
                            if (e.isIntersecting) { e.target.classList.add('vis'); obs.unobserve(e.target); }
                        });
                    }, { threshold: 0.06 });
                    cards.forEach(function (c) { obs.observe(c); });
                } else {
                    cards.forEach(function (c) { c.classList.add('vis'); });
                }

                /* bar fill animation */
                var predCard = document.getElementById('pred-card');
                if (predCard && 'IntersectionObserver' in window) {
                    var bObs = new IntersectionObserver(function (entries) {
                        entries.forEach(function (e) {
                            if (e.isIntersecting) {
                                setTimeout(function () {
                                    predCard.querySelectorAll('.bf[data-pct]').forEach(function (b) {
                                        b.style.width = b.getAttribute('data-pct') + '%';
                                    });
                                }, 200);
                                bObs.unobserve(e.target);
                            }
                        });
                    }, { threshold: 0.2 });
                    bObs.observe(predCard);
                } else {
                    setTimeout(function () {
                        document.querySelectorAll('.bf[data-pct]').forEach(function (b) {
                            b.style.width = b.getAttribute('data-pct') + '%';
                        });
                    }, 600);
                }

                /* count-up on stat cells */
                var acObs = new IntersectionObserver(function (entries) {
                    entries.forEach(function (e) {
                        if (e.isIntersecting) {
                            var v = e.target.querySelector('.val');
                            if (v && !v.dataset.done) {
                                v.dataset.done = '1';
                                var raw = v.textContent.trim();
                                var isPct = raw.indexOf('%') !== -1;
                                var num = parseFloat(raw.replace('%', ''));
                                if (!isNaN(num)) {
                                    var cur = 0, dur = 800, step = num / (dur / 16);
                                    var t = setInterval(function () {
                                        cur += step;
                                        if (cur >= num) { cur = num; clearInterval(t); }
                                        var d = (String(num).indexOf('.') !== -1) ? cur.toFixed(1) : Math.round(cur);
                                        v.textContent = d + (isPct ? '%' : '');
                                    }, 16);
                                }
                            }
                            acObs.unobserve(e.target);
                        }
                    });
                }, { threshold: 0.7 });
                document.querySelectorAll('.ac').forEach(function (el) { acObs.observe(el); });

            })();
        </script>

