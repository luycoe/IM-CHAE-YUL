# IM-CHAE-YUL<!DOCTYPE html>
<html lang="ko">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <meta name="theme-color" content="#f7f4ed">
  <meta name="description" content="임채율의 포트폴리오. 전시와 브랜드 행사 등 공간 기반 프로젝트를 기획하고 사람과 공간을 연결합니다.">
  <title>임채율 — Space & Experience Planner</title>
  <style>
    :root {
      --bg: #f7f4ed;
      --paper: #fffdf8;
      --ink: #292b26;
      --muted: #77786e;
      --line: #dedbd1;
      --accent: #a2a98b;
      --accent-dark: #626b50;
      --soft: #e9e8dc;
      --serif: Georgia, "Times New Roman", serif;
      --sans: "Pretendard", "Apple SD Gothic Neo", "Malgun Gothic", sans-serif;
      --width: 1120px;
    }

    * { box-sizing: border-box; }

    html {
      scroll-behavior: smooth;
      scroll-padding-top: 90px;
    }

    body {
      margin: 0;
      background: var(--bg);
      color: var(--ink);
      font-family: var(--sans);
      line-height: 1.7;
      word-break: keep-all;
      -webkit-font-smoothing: antialiased;
    }

    a {
      color: inherit;
      text-decoration: none;
    }

    button, a { -webkit-tap-highlight-color: transparent; }

    button:focus-visible, a:focus-visible {
      outline: 2px solid var(--accent-dark);
      outline-offset: 4px;
    }

    .container {
      width: min(var(--width), calc(100% - 64px));
      margin-inline: auto;
    }

    .eyebrow {
      margin: 0 0 18px;
      color: var(--accent-dark);
      font-size: 11px;
      font-weight: 700;
      letter-spacing: .18em;
      text-transform: uppercase;
    }

    .section {
      padding: 112px 0;
      border-top: 1px solid var(--line);
    }

    .section-heading {
      display: flex;
      justify-content: space-between;
      align-items: end;
      gap: 28px;
      margin-bottom: 44px;
    }

    .section-heading h2 {
      margin: 0;
      font-size: clamp(32px, 4vw, 48px);
      font-weight: 500;
      letter-spacing: -.065em;
      line-height: 1.2;
    }

    .section-heading p {
      max-width: 330px;
      margin: 0;
      color: var(--muted);
      font-size: 13px;
    }

    /* Navigation */
    .header {
      position: sticky;
      top: 0;
      z-index: 10;
      background: rgba(247, 244, 237, .92);
      border-bottom: 1px solid rgba(222, 219, 209, .8);
      backdrop-filter: blur(14px);
    }

    .nav {
      min-height: 72px;
      display: flex;
      justify-content: space-between;
      align-items: center;
      gap: 24px;
    }

    .logo {
      font-size: 14px;
      font-weight: 750;
      letter-spacing: -.04em;
    }

    .nav-links {
      display: flex;
      gap: 28px;
      align-items: center;
      font-size: 12px;
      color: var(--muted);
    }

    .nav-links a:hover { color: var(--ink); }

    .nav-contact {
      padding: 9px 15px;
      border: 1px solid var(--line);
      border-radius: 99px;
      color: var(--ink);
    }

    /* Hero */
    .hero {
      min-height: 660px;
      padding: 100px 0 84px;
      display: flex;
      align-items: center;
    }

    .hero-grid {
      display: grid;
      grid-template-columns: 1.25fr .75fr;
      align-items: center;
      gap: 64px;
    }

    .hero h1 {
      margin: 0;
      font-size: clamp(58px, 9vw, 112px);
      line-height: .99;
      font-weight: 500;
      letter-spacing: -.085em;
    }

    .hero h1 span {
      display: block;
      margin-top: 12px;
      color: var(--accent-dark);
    }

    .hero-description {
      max-width: 530px;
      margin: 32px 0 0;
      font-size: clamp(15px, 1.5vw, 18px);
      line-height: 1.9;
      letter-spacing: -.035em;
    }

    .hero-meta {
      display: flex;
      flex-wrap: wrap;
      gap: 8px;
      margin-top: 28px;
    }

    .pill {
      padding: 7px 12px;
      border: 1px solid var(--line);
      border-radius: 99px;
      color: var(--muted);
      font-size: 11px;
    }

    .hero-visual {
      position: relative;
      min-height: 380px;
      display: grid;
      place-items: center;
      overflow: hidden;
      border-radius: 48% 48% 8px 8px;
      background: #e7e7d9;
    }

    .hero-visual::before {
      position: absolute;
      width: 240px;
      height: 240px;
      content: "";
      border: 1px solid rgba(98, 107, 80, .28);
      border-radius: 50%;
    }

    .hero-visual::after {
      position: absolute;
      width: 170px;
      height: 170px;
      content: "";
      border: 1px solid rgba(98, 107, 80, .35);
      border-radius: 50%;
    }

    .orbit {
      position: absolute;
      width: 310px;
      height: 130px;
      border: 1px solid rgba(98, 107, 80, .3);
      border-radius: 50%;
      transform: rotate(-35deg);
    }

    .visual-center {
      position: relative;
      z-index: 1;
      display: grid;
      place-items: center;
      width: 126px;
      height: 126px;
      border-radius: 50%;
      background: var(--accent-dark);
      color: var(--paper);
      font-family: var(--serif);
      font-size: 34px;
      letter-spacing: -.06em;
      box-shadow: 0 18px 50px rgba(48, 53, 39, .12);
    }

    .visual-note {
      position: absolute;
      z-index: 2;
      padding: 7px 12px;
      border: 1px solid rgba(98, 107, 80, .25);
      border-radius: 99px;
      background: rgba(255, 253, 248, .78);
      color: var(--accent-dark);
      font-size: 10px;
      letter-spacing: .08em;
    }

    .note-one { top: 24%; left: 8%; }
    .note-two { top: 36%; right: 5%; }
    .note-three { bottom: 22%; left: 17%; }

    .hero-bottom {
      display: flex;
      align-items: center;
      gap: 12px;
      margin-top: 38px;
      color: var(--muted);
      font-size: 11px;
      letter-spacing: .08em;
    }

    .scroll-line {
      display: inline-block;
      width: 40px;
      height: 1px;
      background: var(--accent-dark);
    }

    /* Projects */
    .projects {
      background: var(--paper);
    }

    .project-grid {
      display: grid;
      grid-template-columns: repeat(2, minmax(0, 1fr));
      gap: 44px 24px;
    }

    .project-card {
      min-width: 0;
    }

    .project-card:first-child {
      grid-column: span 2;
    }

    .project-art {
      position: relative;
      display: flex;
      min-height: 270px;
      align-items: center;
      justify-content: center;
      overflow: hidden;
      background: var(--soft);
      isolation: isolate;
    }

    .project-card:first-child .project-art {
      min-height: 390px;
    }

    .art-fair {
      background: #e6e5d9;
    }

    .fair-stage {
      position: relative;
      width: 76%;
      height: 205px;
      border: 1px solid rgba(74, 81, 59, .45);
      background: rgba(255, 253, 248, .4);
      transform: perspective(600px) rotateX(2deg);
    }

    .fair-stage::before {
      position: absolute;
      content: "";
      left: 8%;
      right: 8%;
      top: 16%;
      height: 1px;
      background: rgba(74, 81, 59, .4);
      box-shadow: 0 30px 0 rgba(74, 81, 59, .3),
                  0 60px 0 rgba(74, 81, 59, .2);
    }

    .fair-stage::after {
      position: absolute;
      content: "";
      top: 0;
      bottom: 0;
      left: 50%;
      width: 1px;
      background: rgba(74, 81, 59, .22);
    }

    .fair-block {
      position: absolute;
      z-index: 1;
      bottom: 0;
      width: 17%;
      background: #858d70;
    }

    .fair-block.one { left: 12%; height: 48%; }
    .fair-block.two { left: 36%; height: 70%; background: #c2b99f; }
    .fair-block.three { right: 12%; height: 56%; background: #697356; }

    .art-tag {
      position: absolute;
      z-index: 2;
      top: 18px;
      left: 18px;
      padding: 5px 10px;
      border: 1px solid rgba(41, 43, 38, .2);
      border-radius: 99px;
      color: var(--ink);
      font-size: 10px;
      letter-spacing: .08em;
    }

    .art-index {
      position: absolute;
      right: 20px;
      bottom: 14px;
      color: rgba(41, 43, 38, .58);
      font-family: var(--serif);
      font-size: 12px;
    }

    .art-film {
      background: #e9e0d6;
    }

    .film-frame {
      position: relative;
      display: flex;
      width: 64%;
      aspect-ratio: 4 / 3;
      align-items: center;
      justify-content: center;
      border: 1px solid rgba(81, 69, 59, .4);
      background: linear-gradient(140deg, #b8aa98, #e6d9c9 55%, #928978);
      transform: rotate(-5deg);
    }

    .film-frame::before,
    .film-frame::after {
      position: absolute;
      content: "";
      width: 14px;
      top: 0;
      bottom: 0;
      background: repeating-linear-gradient(
        to bottom,
        #e9e0d6 0 8px,
        transparent 8px 18px
      );
    }

    .film-frame::before { left: -22px; }
    .film-frame::after { right: -22px; }

    .film-sun {
      width: 90px;
      height: 90px;
      border-radius: 50%;
      background: rgba(255, 245, 222, .8);
      box-shadow: 0 0 60px rgba(255, 245, 222, .35);
    }

    .film-caption {
      position: absolute;
      bottom: 16px;
      left: 18px;
      color: #5e554a;
      font-family: var(--serif);
      font-size: 13px;
      letter-spacing: .04em;
    }

    .art-festival {
      background: #dfe5d5;
    }

    .festival-circle {
      position: absolute;
      width: 200px;
      height: 200px;
      border: 1px solid rgba(72, 91, 59, .55);
      border-radius: 50%;
    }

    .festival-circle.inner {
      width: 145px;
      height: 145px;
      border-style: dashed;
    }

    .festival-panel {
      position: relative;
      z-index: 1;
      display: flex;
      width: 115px;
      height: 155px;
      align-items: center;
      justify-content: center;
      border: 1px solid rgba(72, 91, 59, .5);
      background: #f7f4ed;
      color: #59664c;
      font-family: var(--serif);
      font-size: 28px;
      letter-spacing: -.06em;
      box-shadow: 12px 12px 0 rgba(98, 107, 80, .12);
    }

    .project-info {
      display: flex;
      justify-content: space-between;
      align-items: start;
      gap: 18px;
      padding-top: 18px;
    }

    .project-info h3 {
      margin: 0;
      font-size: 20px;
      font-weight: 600;
      letter-spacing: -.05em;
      line-height: 1.5;
    }

    .project-info p {
      margin: 7px 0 0;
      color: var(--muted);
      font-size: 12px;
    }

    .project-number {
      flex-shrink: 0;
      color: var(--accent-dark);
      font-family: var(--serif);
      font-size: 13px;
    }

    .project-description {
      max-width: 600px;
      margin: 15px 0 0;
      color: var(--muted);
      font-size: 13px;
      line-height: 1.9;
    }

    .project-tags {
      display: flex;
      flex-wrap: wrap;
      gap: 7px;
      margin-top: 16px;
    }

    .project-tags span {
      padding: 4px 9px;
      border-radius: 4px;
      background: #f0eee6;
      color: #686a5e;
      font-size: 10px;
    }

    /* About */
    .about-grid {
      display: grid;
      grid-template-columns: .8fr 1.2fr;
      gap: 90px;
    }

    .about-title {
      position: sticky;
      top: 112px;
      align-self: start;
    }

    .about-title h2 {
      margin: 0;
      font-size: clamp(36px, 5vw, 56px);
      font-weight: 500;
      letter-spacing: -.075em;
      line-height: 1.2;
    }

    .about-title h2 em {
      color: var(--accent-dark);
      font-family: var(--serif);
      font-weight: 400;
    }

    .about-copy {
      max-width: 620px;
    }

    .about-lead {
      margin: 0 0 24px;
      font-size: 21px;
      line-height: 1.8;
      letter-spacing: -.04em;
    }

    .about-copy > p:not(.about-lead) {
      color: var(--muted);
      font-size: 14px;
      line-height: 2;
    }

    .values {
      display: grid;
      grid-template-columns: repeat(3, 1fr);
      gap: 12px;
      margin-top: 34px;
    }

    .value-card {
      padding: 19px 14px;
      border: 1px solid var(--line);
      border-radius: 8px;
    }

    .value-card strong {
      display: block;
      margin-bottom: 7px;
      color: var(--accent-dark);
      font-size: 13px;
    }

    .value-card span {
      display: block;
      color: var(--muted);
      font-size: 11px;
      line-height: 1.7;
    }

    /* Experience */
    .experience {
      background: #efeee5;
    }

    .timeline {
      border-top: 1px solid #d8d7cb;
    }

    .timeline-item {
      display: grid;
      grid-template-columns: 150px 1fr 130px;
      gap: 28px;
      padding: 25px 0;
      border-bottom: 1px solid #d8d7cb;
    }

    .timeline-date {
      color: var(--accent-dark);
      font-family: var(--serif);
      font-size: 13px;
    }

    .timeline-item h3 {
      margin: 0;
      font-size: 16px;
      font-weight: 600;
      letter-spacing: -.03em;
    }

    .timeline-item p {
      margin: 6px 0 0;
      color: var(--muted);
      font-size: 12px;
    }

    .timeline-role {
      color: var(--muted);
      font-size: 11px;
      text-align: right;
    }

    .more-experience {
      margin-top: 28px;
    }

    .more-experience summary {
      width: fit-content;
      cursor: pointer;
      color: var(--accent-dark);
      font-size: 12px;
      font-weight: 600;
    }

    .more-experience .timeline {
      margin-top: 20px;
    }

    /* Education and skills */
    .details-grid {
      display: grid;
      grid-template-columns: 1fr 1fr;
      gap: 60px;
    }

    .detail-heading {
      margin: 0 0 25px;
      font-size: 23px;
      font-weight: 500;
      letter-spacing: -.05em;
    }

    .education-item {
      padding: 19px 0;
      border-top: 1px solid var(--line);
    }

    .education-item:last-child {
      border-bottom: 1px solid var(--line);
    }

    .education-date {
      color: var(--accent-dark);
      font-family: var(--serif);
      font-size: 12px;
    }

    .education-item h4 {
      margin: 6px 0;
      font-size: 15px;
    }

    .education-item p {
      margin: 0;
      color: var(--muted);
      font-size: 12px;
    }

    .skill-group {
      padding: 19px 0;
      border-top: 1px solid var(--line);
    }

    .skill-group:last-of-type {
      border-bottom: 1px solid var(--line);
    }

    .skill-top {
      display: flex;
      justify-content: space-between;
      align-items: center;
      gap: 16px;
      margin-bottom: 12px;
    }

    .skill-top strong { font-size: 14px; }

    .skill-top span {
      color: var(--accent-dark);
      font-size: 11px;
    }

    .skill-list {
      display: flex;
      flex-wrap: wrap;
      gap: 8px;
    }

    .skill-list span {
      padding: 7px 10px;
      border: 1px solid var(--line);
      border-radius: 5px;
      color: #64665c;
      font-size: 11px;
    }

    .certifications {
      margin-top: 32px;
    }

    .certifications h4 {
      margin: 0 0 12px;
      font-size: 14px;
    }

    .certifications p {
      margin: 0;
      color: var(--muted);
      font-size: 12px;
      line-height: 2;
    }

    /* Awards */
    .awards {
      background: var(--paper);
    }

    .award-list {
      border-top: 1px solid var(--line);
    }

    .award-item {
      display: grid;
      grid-template-columns: 70px 1fr 120px;
      gap: 20px;
      align-items: center;
      padding: 22px 0;
      border-bottom: 1px solid var(--line);
    }

    .award-year {
      color: var(--accent-dark);
      font-family: var(--serif);
      font-size: 17px;
    }

    .award-item h3 {
      margin: 0;
      font-size: 15px;
      font-weight: 600;
    }

    .award-item p {
      margin: 5px 0 0;
      color: var(--muted);
      font-size: 12px;
    }

    .award-badge {
      justify-self: end;
      padding: 6px 11px;
      border: 1px solid var(--line);
      border-radius: 99px;
      font-size: 11px;
    }

    /* Contact */
    .contact {
      padding: 110px 0 80px;
    }

    .contact-panel {
      position: relative;
      overflow: hidden;
      padding: clamp(32px, 7vw, 78px);
      border-radius: 12px;
      background: #e7e8dc;
    }

    .contact-panel::after {
      position: absolute;
      content: "";
      width: 330px;
      height: 330px;
      right: -95px;
      bottom: -170px;
      border: 1px solid rgba(98, 107, 80, .3);
      border-radius: 50%;
      box-shadow: 0 0 0 30px rgba(98, 107, 80, .04),
                  0 0 0 60px rgba(98, 107, 80, .04);
      pointer-events: none;
    }

    .contact-panel h2 {
      position: relative;
      z-index: 1;
      max-width: 680px;
      margin: 0;
      font-size: clamp(38px, 6vw, 70px);
      font-weight: 500;
      line-height: 1.15;
      letter-spacing: -.075em;
    }

    .contact-panel h2 em {
      color: var(--accent-dark);
      font-family: var(--serif);
      font-weight: 400;
    }

    .contact-panel > p {
      position: relative;
      z-index: 1;
      margin: 22px 0 30px;
      color: #6b6d60;
      font-size: 14px;
    }

    .contact-links {
      position: relative;
      z-index: 1;
      display: flex;
      flex-wrap: wrap;
      gap: 10px;
    }

    .contact-link {
      display: inline-flex;
      align-items: center;
      gap: 10px;
      padding: 12px 17px;
      border: 1px solid rgba(98, 107, 80, .35);
      border-radius: 99px;
      background: rgba(255, 253, 248, .48);
      font-size: 12px;
      transition: background .2s, transform .2s;
    }

    .contact-link:hover {
      background: var(--paper);
      transform: translateY(-2px);
    }

    .footer {
      display: flex;
      justify-content: space-between;
      gap: 20px;
      padding: 26px 0 32px;
      border-top: 1px solid var(--line);
      color: var(--muted);
      font-size: 10px;
    }

    .footer a { color: var(--ink); }

    @media (min-width: 1400px) {
      .hero { min-height: 730px; }
    }

    @media (max-width: 800px) {
      .container { width: min(100% - 40px, var(--width)); }
      .section { padding: 80px 0; }
      .hero { min-height: auto; padding: 76px 0; }
      .hero-grid { grid-template-columns: 1fr; gap: 45px; }
      .hero-visual { min-height: 310px; max-width: 440px; width: 100%; margin-inline: auto; }
      .hero h1 { font-size: clamp(64px, 13vw, 94px); }
      .project-card:first-child .project-art { min-height: 310px; }
      .about-grid { grid-template-columns: 1fr; gap: 36px; }
      .about-title { position: static; }
      .timeline-item { grid-template-columns: 110px 1fr; gap: 16px; }
      .timeline-role { grid-column: 2; text-align: left; }
      .details-grid { gap: 36px; }
    }

    @media (max-width: 560px) {
      .container { width: calc(100% - 36px); }
      .nav { min-height: 62px; }
      .nav-links { gap: 14px; font-size: 11px; }
      .nav-links a:nth-child(2) { display: none; }
      .nav-contact { padding: 7px 11px; }
      .hero { padding: 62px 0 72px; }
      .hero h1 { font-size: clamp(58px, 15vw, 78px); }
      .hero-description { font-size: 15px; }
      .hero-visual { min-height: 270px; }
      .section { padding: 68px 0; }
      .section-heading { align-items: start; flex-direction: column; gap: 14px; margin-bottom: 30px; }
      .section-heading h2 { font-size: 35px; }
      .project-grid { grid-template-columns: 1fr; gap: 34px; }
      .project-card:first-child { grid-column: auto; }
      .project-card:first-child .project-art,
      .project-art { min-height: 260px; }
      .project-info h3 { font-size: 17px; }
      .values { grid-template-columns: 1fr; }
      .value-card { padding: 15px; }
      .timeline-item { grid-template-columns: 1fr; gap: 5px; padding: 20px 0; }
      .timeline-role { grid-column: auto; }
      .details-grid { grid-template-columns: 1fr; gap: 54px; }
      .award-item { grid-template-columns: 48px 1fr; gap: 12px; }
      .award-badge { grid-column: 2; justify-self: start; }
      .contact { padding: 68px 0 50px; }
      .contact-panel { padding: 32px 24px; }
      .contact-panel h2 { font-size: 43px; }
      .contact-links { align-items: stretch; flex-direction: column; }
      .contact-link { width: fit-content; max-width: 100%; overflow-wrap: anywhere; }
      .footer { flex-direction: column; gap: 8px; }
    }

    @media (prefers-reduced-motion: reduce) {
      *, *::before, *::after {
        scroll-behavior: auto !important;
        transition-duration: .01ms !important;
        animation-duration: .01ms !important;
      }
    }
  </style>
</head>
<body>
  <header class="header">
    <nav class="nav container" aria-label="주요 메뉴">
      <a class="logo" href="#home" aria-label="임채율 포트폴리오 홈">CHAEYUL LIM.</a>
      <div class="nav-links">
        <a href="#projects">PROJECTS</a>
        <a href="#about">ABOUT</a>
        <a href="#experience">EXPERIENCE</a>
        <a class="nav-contact" href="#contact">CONTACT ↗</a>
      </div>
    </nav>
  </header>

  <main>
    <section class="hero container" id="home">
      <div class="hero-grid">
        <div>
          <p class="eyebrow">Space · Exhibition · Experience</p>
          <h1>임채율<span>공간을 기획하다.</span></h1>
          <p class="hero-description">
            전시와 브랜드 행사 등 공간 기반 프로젝트를 기획하고,
            일정과 자원을 조율해 사람과 공간을 연결하는 기획자입니다.
          </p>
          <div class="hero-meta" aria-label="주요 관심 분야">
            <span class="pill">Exhibition</span>
            <span class="pill">Brand Experience</span>
            <span class="pill">Pop-up & Event</span>
          </div>
          <div class="hero-bottom">
            <span class="scroll-line"></span>
            SCROLL TO EXPLORE
          </div>
        </div>

        <div class="hero-visual" role="img" aria-label="공간과 경험의 연결을 표현한 추상 그래픽">
          <div class="orbit"></div>
          <div class="visual-center">CY.</div>
          <span class="visual-note note-one">IDEA</span>
          <span class="visual-note note-two">SPACE</span>
          <span class="visual-note note-three">PEOPLE</span>
        </div>
      </div>
    </section>

    <section class="section projects" id="projects">
      <div class="container">
        <div class="section-heading">
          <div>
            <p class="eyebrow">Selected Works · 2023—2026</p>
            <h2>기획이 경험이 되는 순간</h2>
          </div>
          <p>콘텐츠 제작과 행사 현장 경험을 통해 사람들의 참여와 반응을 가까이에서 배웠습니다.</p>
        </div>

        <div class="project-grid">
          <article class="project-card">
            <div class="project-art art-fair" role="img" aria-label="박람회 부스의 구조와 동선을 표현한 그래픽">
              <span class="art-tag">FIELD EXPERIENCE / 01</span>
              <div class="fair-stage">
                <div class="fair-block one"></div>
                <div class="fair-block two"></div>
                <div class="fair-block three"></div>
              </div>
              <span class="art-index">COEX · 2025</span>
            </div>
            <div class="project-info">
              <div>
                <h3>컬리푸드페스타 코엑스 부스 운영</h3>
                <p>2025.12 · 행사 부스 운영 스태프 · 팀 8명</p>
              </div>
              <span class="project-number">01</span>
            </div>
            <p class="project-description">
              행사 부스 운영과 방문객 응대 및 안내를 담당했습니다.
              대기 동선과 물품을 관리하며 방문객이 원활하게 부스를 이용할 수 있도록 현장 운영을 지원했습니다.
            </p>
            <div class="project-tags">
              <span>현장 운영</span><span>방문객 응대</span><span>대기 동선 관리</span><span>팀 협업</span>
            </div>
          </article>

          <article class="project-card">
            <div class="project-art art-film" role="img" aria-label="따뜻한 빛과 필름 프레임을 활용한 영상 프로젝트 그래픽">
              <span class="art-tag">VIDEO PROJECT / 02</span>
              <div class="film-frame">
                <div class="film-sun"></div>
              </div>
              <span class="film-caption">A GIFT IN 10 SECONDS</span>
              <span class="art-index">AWARD · 2024</span>
            </div>
            <div class="project-info">
              <div>
                <h3>하루 10초 부모님께 선물해 보세요</h3>
                <p>2024 · 효 공모전 대상 · 세계일보</p>
              </div>
              <span class="project-number">02</span>
            </div>
            <p class="project-description">
              프로젝트 총괄로서 감독, 대본, 섭외, 연기, 편집 등 제작 전반을 담당했습니다.
              아이디어를 하나의 영상 콘텐츠로 구체화하고 기획 의도가 결과물에 드러나도록 제작 과정을 이끌었습니다.
            </p>
            <div class="project-tags">
              <span>프로젝트 총괄</span><span>콘셉트 기획</span><span>대본</span><span>연출·편집</span>
            </div>
          </article>

          <article class="project-card">
            <div class="project-art art-festival" role="img" aria-label="축제의 체험 공간과 참여 동선을 표현한 그래픽">
              <span class="art-tag">FIELD EXPERIENCE / 03</span>
              <div class="festival-circle"></div>
              <div class="festival-circle inner"></div>
              <div class="festival-panel">PLAY<br>&nbsp;WITH<br>US</div>
              <span class="art-index">EUNPYEONG · 2026</span>
            </div>
            <div class="project-info">
              <div>
                <h3>은평구 무차별대로 축제</h3>
                <p>2026.09 · 축제 부스 운영 스태프</p>
              </div>
              <span class="project-number">03</span>
            </div>
            <p class="project-description">
              축제 부스 운영과 방문객 응대·안내를 담당했습니다.
              체험 프로그램을 소개하고 참여를 유도하며, 방문객이 행사에 자연스럽게 참여할 수 있도록 현장 운영을 지원했습니다.
            </p>
            <div class="project-tags">
              <span>축제 운영</span><span>체험 프로그램</span><span>참여 유도</span><span>현장 커뮤니케이션</span>
            </div>
          </article>
        </div>
      </div>
    </section>

    <section class="section" id="about">
      <div class="container about-grid">
        <div class="about-title">
          <p class="eyebrow">About Me</p>
          <h2>아이디어에서<br><em>현장까지.</em></h2>
        </div>

        <div class="about-copy">
          <p class="about-lead">
            콘텐츠를 만드는 일에서 출발해, 사람들이 직접 참여하고 경험하는 공간을 기획하는 일로 관심을 넓혀 왔습니다.
          </p>
          <p>
            미디어 콘텐츠를 전공하며 영상 프로젝트의 아이디어를 구체화하고 콘셉트와 연출을 통해 결과물로 구현하는 과정을 경험했습니다.
            이후 팝업 행사와 캐릭터 콜라보 카페, 박람회 등 다양한 현장에서 방문객 응대와 체험 프로그램 운영을 맡았습니다.
          </p>
          <p>
            현장에서는 기획된 경험이 실제로 전달되기 위해 동선과 물품, 방문객의 반응 등 여러 요소가 함께 고려되어야 한다는 점을 배웠습니다.
            이제는 현장 운영 경험을 바탕으로 공간 기반 프로젝트의 기획 단계부터 실행까지 참여하고 싶습니다.
          </p>
          <p>
            아이디어를 실현 가능한 계획으로 발전시키고, 세부 사항을 꼼꼼하게 살피며,
            여러 요소를 조율해 프로젝트를 완성하는 기획자로 성장하겠습니다.
          </p>

          <div class="values">
            <div class="value-card">
              <strong>01. 기획력</strong>
              <span>아이디어를 콘셉트와 실행 계획으로 구체화합니다.</span>
            </div>
            <div class="value-card">
              <strong>02. 꼼꼼함</strong>
              <span>일정과 세부 사항을 확인해 완성도를 높입니다.</span>
            </div>
            <div class="value-card">
              <strong>03. 현장 감각</strong>
              <span>방문객의 입장에서 참여와 경험을 살핍니다.</span>
            </div>
          </div>
        </div>
      </div>
    </section>

    <section class="section experience" id="experience">
      <div class="container">
        <div class="section-heading">
          <div>
            <p class="eyebrow">Experience</p>
            <h2>현장에서 쌓은 경험</h2>
          </div>
          <p>서로 다른 행사와 프로그램을 경험하며 운영과 커뮤니케이션 역량을 쌓았습니다.</p>
        </div>

        <div class="timeline">
          <article class="timeline-item">
            <span class="timeline-date">2026.09</span>
            <div>
              <h3>은평구 무차별대로 축제</h3>
              <p>축제 부스 운영, 방문객 응대 및 체험 프로그램 안내</p>
            </div>
            <span class="timeline-role">운영 스태프</span>
          </article>
          <article class="timeline-item">
            <span class="timeline-date">2025.12</span>
            <div>
              <h3>컬리푸드페스타 코엑스 부스 운영</h3>
              <p>방문객 안내, 대기 동선 및 물품 관리</p>
            </div>
            <span class="timeline-role">운영 스태프 · 8명</span>
          </article>
          <article class="timeline-item">
            <span class="timeline-date">2025.04—08</span>
            <div>
              <h3>대원미디어 팝퍼블 캐릭터 콜라보 카페</h3>
              <p>매장 세팅, 물품 관리, 방문객 응대, 판매 및 결제</p>
            </div>
            <span class="timeline-role">매장 운영 · 12명</span>
          </article>
          <article class="timeline-item">
            <span class="timeline-date">2023.05—06</span>
            <div>
              <h3>마포청소년센터 미디어 리터러시 교육</h3>
              <p>교육 자료 준비, 참여자 안내 및 프로그램 운영 지원</p>
            </div>
            <span class="timeline-role">운영 지원 · 8명</span>
          </article>
        </div>

        <details class="more-experience">
          <summary>이전 행사 경험 더 보기 +</summary>
          <div class="timeline">
            <article class="timeline-item">
              <span class="timeline-date">2023.04</span>
              <div>
                <h3>어린이날 그래비트랙스 장난감 팝업 부스</h3>
                <p>체험 프로그램 운영, 참여 유도 및 대기 동선 관리</p>
              </div>
              <span class="timeline-role">체험 부스 · 2명</span>
            </article>
            <article class="timeline-item">
              <span class="timeline-date">2022.02</span>
              <div>
                <h3>발렌타인데이 롯데제과 행사 부스</h3>
                <p>방문객 응대, 안내 및 현장 물품 관리</p>
              </div>
              <span class="timeline-role">행사 운영 · 2명</span>
            </article>
            <article class="timeline-item">
              <span class="timeline-date">2022.01</span>
              <div>
                <h3>해우촌 설 선물세트 행사 부스</h3>
                <p>제품 소개, 방문객 안내, 판매 및 결제</p>
              </div>
              <span class="timeline-role">행사 운영 · 6명</span>
            </article>
            <article class="timeline-item">
              <span class="timeline-date">2021.11</span>
              <div>
                <h3>롯데몰 락앤락 행사 부스</h3>
                <p>방문객 응대, 제품 소개 및 판매 관련 업무</p>
              </div>
              <span class="timeline-role">행사 운영 · 5명</span>
            </article>
            <article class="timeline-item">
              <span class="timeline-date">2021.11</span>
              <div>
                <h3>롯데 빼빼로데이 부스</h3>
                <p>행사 부스 운영 및 방문객 응대·안내</p>
              </div>
              <span class="timeline-role">행사 운영 · 2명</span>
            </article>
          </div>
        </details>
      </div>
    </section>

    <section class="section" id="education">
      <div class="container">
        <div class="section-heading">
          <div>
            <p class="eyebrow">Education & Skills</p>
            <h2>배움과 도구</h2>
          </div>
          <p>미디어 전공을 바탕으로 콘텐츠를 이해하고, 기획과 실행에 필요한 도구를 활용합니다.</p>
        </div>

        <div class="details-grid">
          <div>
            <h3 class="detail-heading">Education</h3>
            <article class="education-item">
              <span class="education-date">2025.03 — 2027.02</span>
              <h4>명지대학교</h4>
              <p>미디어앤아트테크놀로지학과 · 학사 · 졸업 예정</p>
            </article>
            <article class="education-item">
              <span class="education-date">2023.03 — 2024.08</span>
              <h4>명지전문대학교</h4>
              <p>디지털콘텐츠학과 · 전문학사 · 평점 3.8 / 4.5</p>
            </article>
          </div>

          <div>
            <h3 class="detail-heading">Tools</h3>
            <div class="skill-group">
              <div class="skill-top">
                <strong>Advanced</strong>
                <span>상급</span>
              </div>
              <div class="skill-list">
                <span>Adobe Premiere Pro</span>
                <span>미리캔버스</span>
              </div>
            </div>
            <div class="skill-group">
              <div class="skill-top">
                <strong>Intermediate</strong>
                <span>중급</span>
              </div>
              <div class="skill-list">
                <span>CapCut</span>
                <span>Adobe Illustrator</span>
                <span>Adobe Photoshop</span>
                <span>Figma</span>
                <span>Microsoft Excel</span>
              </div>
            </div>
            <div class="skill-group">
              <div class="skill-top">
                <strong>Beginner</strong>
                <span>초급</span>
              </div>
              <div class="skill-list">
                <span>Adobe After Effects</span>
              </div>
            </div>
            <div class="certifications">
              <h4>Certifications</h4>
              <p>서비스경영자격 SMAT<br>컴퓨터활용능력 2급<br>자동차운전면허 2종 보통</p>
            </div>
          </div>
        </div>
      </div>
    </section>

    <section class="section awards" id="awards">
      <div class="container">
        <div class="section-heading">
          <div>
            <p class="eyebrow">Awards</p>
            <h2>콘텐츠로 만든 결과</h2>
          </div>
          <p>기획과 대본, 촬영, 연출 등 다양한 역할로 영상 프로젝트를 완성했습니다.</p>
        </div>

        <div class="award-list">
          <article class="award-item">
            <span class="award-year">2024</span>
            <div>
              <h3>하루 10초 부모님께 선물해 보세요</h3>
              <p>세계일보 · 프로젝트 총괄, 감독, 대본, 섭외, 연기, 편집</p>
            </div>
            <span class="award-badge">대상</span>
          </article>
          <article class="award-item">
            <span class="award-year">2023</span>
            <div>
              <h3>MY DAILY LIFE — FLIX of 청춘</h3>
              <p>한국청년지속가능발전협의회 · 촬영 및 연출</p>
            </div>
            <span class="award-badge">대상</span>
          </article>
          <article class="award-item">
            <span class="award-year">2023</span>
            <div>
              <h3>야 너두 할 수 있어!</h3>
              <p>명지전문대학 전공심화 홍보영상 경진대회 · 대본, 연출, 연기</p>
            </div>
            <span class="award-badge">금상</span>
          </article>
          <article class="award-item">
            <span class="award-year">2023</span>
            <div>
              <h3>뭐? 아직도 우리를 모른다고?</h3>
              <p>명지전문대학 학과홍보 Shots 경진대회 · 대본, 연출, 섭외</p>
            </div>
            <span class="award-badge">금상</span>
          </article>
        </div>
      </div>
    </section>

    <section class="contact" id="contact">
      <div class="container">
        <div class="contact-panel">
          <p class="eyebrow">Let's Make It Happen</p>
          <h2>좋은 아이디어를<br><em>실제 경험으로.</em></h2>
          <p>
            사람과 공간을 연결하는 프로젝트를 함께 만들고 싶습니다.<br>
            새로운 기회와 협업 제안을 기다립니다.
          </p>
          <div class="contact-links">
            <a class="contact-link" href="mailto:icyul319030@naver.com">
              <span aria-hidden="true">✉</span>
              icyul319030@naver.com
            </a>
            <a class="contact-link" href="tel:01067620913">
              <span aria-hidden="true">↗</span>
              010-6762-0913
            </a>
            <a class="contact-link" href="#home">
              <span aria-hidden="true">↑</span>
              Back to top
            </a>
          </div>
        </div>
      </div>
    </section>
  </main>

  <footer
