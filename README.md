
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />

  <title>InteriorWise | Know Your Interior Cost Before You Start</title>

  <meta
    name="description"
    content="InteriorWise helps Delhi homeowners understand interior costs, compare requirements and connect for an interior consultation."
  />

  <style>
    * {
      box-sizing: border-box;
      margin: 0;
      padding: 0;
    }

    :root {
      --ink: #18211d;
      --muted: #69736e;
      --cream: #f7f5ef;
      --white: #ffffff;
      --green: #24483d;
      --green-dark: #18352d;
      --line: #e4e5df;
      --soft-green: #e9f0eb;
      --gold: #b39a68;
    }

    html {
      scroll-behavior: smooth;
    }

    body {
      font-family: Arial, Helvetica, sans-serif;
      color: var(--ink);
      background: var(--cream);
      line-height: 1.5;
    }

    a {
      text-decoration: none;
      color: inherit;
    }

    button {
      font: inherit;
      cursor: pointer;
    }

    .container {
      width: min(1120px, calc(100% - 36px));
      margin: auto;
    }

    /* ---------------- HEADER ---------------- */

    header {
      position: sticky;
      top: 0;
      z-index: 100;
      background: rgba(247, 245, 239, 0.94);
      backdrop-filter: blur(12px);
      border-bottom: 1px solid rgba(228, 229, 223, 0.8);
    }

    .nav {
      min-height: 72px;
      display: flex;
      align-items: center;
      justify-content: space-between;
      gap: 20px;
    }

    .logo {
      font-size: 22px;
      font-weight: 800;
      letter-spacing: -0.7px;
    }

    .logo span {
      color: var(--green);
    }

    .desktop-nav {
      display: flex;
      align-items: center;
      gap: 28px;
      color: #48534e;
      font-size: 14px;
    }

    .desktop-nav a:hover {
      color: var(--green);
    }

    .nav-button {
      padding: 11px 17px;
      border-radius: 999px;
      background: var(--green);
      color: white;
      font-weight: 700;
    }

    .menu {
      display: none;
      border: 0;
      background: transparent;
      font-size: 26px;
    }

    /* ---------------- HERO ---------------- */

    .hero {
      padding: 70px 0 55px;
    }

    .hero-grid {
      display: grid;
      grid-template-columns: 1.02fr 0.98fr;
      align-items: center;
      gap: 55px;
    }

    .eyebrow {
      display: inline-flex;
      align-items: center;
      gap: 8px;
      color: var(--green);
      font-weight: 800;
      font-size: 12px;
      letter-spacing: 1.4px;
      text-transform: uppercase;
      margin-bottom: 18px;
    }

    .eyebrow::before {
      content: "";
      width: 26px;
      height: 1px;
      background: var(--gold);
    }

    h1 {
      font-size: clamp(42px, 6vw, 72px);
      line-height: 0.99;
      letter-spacing: -3.5px;
      max-width: 700px;
    }

    h1 span {
      color: var(--green);
    }

    .hero-text {
      color: var(--muted);
      font-size: 17px;
      max-width: 580px;
      margin: 25px 0 30px;
    }

    .actions {
      display: flex;
      flex-wrap: wrap;
      gap: 12px;
    }

    .primary {
      border: 0;
      background: var(--green);
      color: white;
      padding: 15px 22px;
      border-radius: 9px;
      font-weight: 800;
      transition: 0.2s ease;
    }

    .primary:hover {
      background: var(--green-dark);
      transform: translateY(-1px);
    }

    .secondary {
      border: 1px solid var(--line);
      background: white;
      color: var(--ink);
      padding: 15px 22px;
      border-radius: 9px;
      font-weight: 700;
    }

    .hero-note {
      margin-top: 17px;
      color: #858c88;
      font-size: 12px;
    }

    .hero-visual {
      position: relative;
    }

    .image-frame {
      min-height: 490px;
      border-radius: 24px;
      overflow: hidden;
      position: relative;
      background:
        linear-gradient(
          145deg,
          rgba(30, 55, 46, 0.12),
          rgba(0, 0, 0, 0.02)
        ),
        url("https://images.unsplash.com/photo-1600607687920-4e2a09cf159d?auto=format&fit=crop&w=1200&q=85")
        center / cover;
    }

    .image-label {
      position: absolute;
      left: 20px;
      bottom: 20px;
      background: rgba(255, 255, 255, 0.94);
      border-radius: 13px;
      padding: 14px 17px;
      min-width: 190px;
    }

    .image-label small {
      display: block;
      color: var(--muted);
      font-size: 11px;
      margin-bottom: 3px;
    }

    .image-label strong {
      font-size: 14px;
    }

    /* ---------------- TRUST BAR ---------------- */

    .trust {
      padding: 0 0 75px;
    }

    .trust-box {
      background: white;
      border: 1px solid var(--line);
      border-radius: 18px;
      padding: 23px 25px;
      display: grid;
      grid-template-columns: repeat(3, 1fr);
      gap: 20px;
    }

    .trust-item {
      display: flex;
      align-items: center;
      gap: 12px;
    }

    .trust-icon {
      width: 38px;
      height: 38px;
      border-radius: 50%;
      display: grid;
      place-items: center;
      background: var(--soft-green);
      color: var(--green);
      font-weight: 800;
    }

    .trust-item strong {
      display: block;
      font-size: 13px;
    }

    .trust-item span {
      color: var(--muted);
      font-size: 11px;
    }

    /* ---------------- SECTIONS ---------------- */

    section {
      padding: 85px 0;
    }

    .section-heading {
      max-width: 650px;
      margin-bottom: 42px;
    }

    .section-heading h2 {
      font-size: clamp(31px, 5vw, 48px);
      line-height: 1.05;
      letter-spacing: -2px;
      margin-bottom: 13px;
    }

    .section-heading p {
      color: var(--muted);
      font-size: 15px;
    }

    /* ---------------- HOW IT WORKS ---------------- */

    .how {
      background: white;
    }

    .steps {
      display: grid;
      grid-template-columns: repeat(4, 1fr);
      gap: 16px;
    }

    .step {
      border: 1px solid var(--line);
      border-radius: 16px;
      padding: 25px;
      min-height: 190px;
    }

    .step-number {
      color: var(--gold);
      font-weight: 900;
      font-size: 13px;
      margin-bottom: 30px;
    }

    .step h3 {
      font-size: 17px;
      margin-bottom: 8px;
    }

    .step p {
      color: var(--muted);
      font-size: 13px;
    }

    /* ---------------- CALCULATOR CTA ---------------- */

    .calculator-preview {
      background: var(--green);
      color: white;
      border-radius: 25px;
      padding: 42px;
      display: grid;
      grid-template-columns: 1fr 0.85fr;
      gap: 35px;
      align-items: center;
    }

    .calculator-preview h2 {
      font-size: clamp(31px, 5vw, 47px);
      line-height: 1.05;
      letter-spacing: -2px;
      margin-bottom: 14px;
    }

    .calculator-preview p {
      color: #d5dfda;
      max-width: 540px;
      font-size: 14px;
    }

    .calc-card {
      background: white;
      color: var(--ink);
      border-radius: 18px;
      padding: 24px;
    }

    .calc-card-label {
      font-size: 11px;
      color: var(--muted);
      margin-bottom: 5px;
    }

    .calc-card-title {
      font-size: 22px;
      font-weight: 800;
      margin-bottom: 18px;
    }

    .fake-select {
      border: 1px solid var(--line);
      border-radius: 9px;
      padding: 13px;
      margin-bottom: 10px;
      font-size: 13px;
      display: flex;
      justify-content: space-between;
    }

    .calc-button {
      width: 100%;
      border: 0;
      border-radius: 9px;
      background: var(--green);
      color: white;
      padding: 14px;
      margin-top: 8px;
      font-weight: 800;
    }

    /* ---------------- CATEGORIES ---------------- */

    .categories {
      display: grid;
      grid-template-columns: repeat(5, 1fr);
      gap: 12px;
    }

    .category {
      background: white;
      border: 1px solid var(--line);
      border-radius: 14px;
      padding: 21px 17px;
      transition: 0.2s ease;
    }

    .category:hover {
      transform: translateY(-3px);
      border-color: #cbd4cf;
    }

    .category-icon {
      font-size: 21px;
      margin-bottom: 18px;
    }

    .category strong {
      display: block;
      font-size: 13px;
      margin-bottom: 4px;
    }

    .category span {
      color: var(--muted);
      font-size: 11px;
    }

    /* ---------------- TRANSPARENCY ---------------- */

    .compare {
      background: white;
    }

    .compare-grid {
      display: grid;
      grid-template-columns: 0.85fr 1.15fr;
      gap: 55px;
      align-items: center;
    }

    .compare-text h2 {
      font-size: clamp(31px, 5vw, 47px);
      line-height: 1.05;
      letter-spacing: -2px;
      margin-bottom: 17px;
    }

    .compare-text p {
      color: var(--muted);
      font-size: 15px;
      margin-bottom: 22px;
    }

    .quote-box {
      background: var(--cream);
      border: 1px solid var(--line);
      border-radius: 18px;
      padding: 22px;
    }

    .quote-row {
      display: flex;
      align-items: center;
      justify-content: space-between;
      padding: 15px 0;
      border-bottom: 1px solid var(--line);
      font-size: 13px;
    }

    .quote-row:last-child {
      border-bottom: 0;
    }

    .quote-row span {
      color: var(--muted);
    }

    .warning {
      color: #8c6540;
      background: #f3ede5;
      padding: 4px 8px;
      border-radius: 999px;
      font-size: 10px;
      font-weight: 700;
    }

    /* ---------------- CTA ---------------- */

    .final-cta {
      text-align: center;
      padding: 100px 20px;
    }

    .final-cta h2 {
      font-size: clamp(34px, 6vw, 57px);
      letter-spacing: -2.5px;
      line-height: 1;
      max-width: 700px;
      margin: 0 auto 18px;
    }

    .final-cta p {
      color: var(--muted);
      max-width: 550px;
      margin: 0 auto 27px;
    }

    /* ---------------- FOOTER ---------------- */

    footer {
      background: var(--ink);
      color: white;
      padding: 50px 0 25px;
    }

    .footer-top {
      display: flex;
      justify-content: space-between;
      gap: 30px;
      padding-bottom: 35px;
      border-bottom: 1px solid rgba(255,255,255,0.12);
    }

    .footer-logo {
      font-size: 21px;
      font-weight: 800;
    }

    .footer-logo span {
      color: #a9c2b7;
    }

    .footer-text {
      color: #aab4af;
      font-size: 12px;
      max-width: 320px;
      margin-top: 9px;
    }

    .footer-links {
      display: flex;
      gap: 22px;
      color: #c5ccc8;
      font-size: 12px;
    }

    .copyright {
      padding-top: 22px;
      color: #7f8b85;
      font-size: 10px;
    }

    /* ---------------- MOBILE ---------------- */

    @media (max-width: 850px) {

      .container {
        width: min(100% - 28px, 650px);
      }

      .desktop-nav {
        display: none;
      }

      .menu {
        display: block;
      }

      .hero {
        padding: 45px 0 35px;
      }

      .hero-grid {
        grid-template-columns: 1fr;
        gap: 32px;
      }

      h1 {
        font-size: 48px;
        letter-spacing: -2.7px;
      }

      .hero-text {
        font-size: 15px;
      }

      .image-frame {
        min-height: 390px;
        border-radius: 19px;
      }

      .trust-box {
        grid-template-columns: 1fr;
        gap: 14px;
      }

      section {
        padding: 65px 0;
      }

      .steps {
        grid-template-columns: 1fr 1fr;
      }

      .calculator-preview {
        grid-template-columns: 1fr;
        padding: 28px;
        border-radius: 20px;
      }

      .categories {
        grid-template-columns: 1fr 1fr;
      }

      .compare-grid {
        grid-template-columns: 1fr;
        gap: 32px;
      }

      .footer-top {
        flex-direction: column;
      }

      .footer-links {
        flex-wrap: wrap;
      }
    }

    @media (max-width: 480px) {

      .nav {
        min-height: 64px;
      }

      .logo {
        font-size: 20px;
      }

      h1 {
        font-size: 42px;
      }

      .actions {
        flex-direction: column;
      }

      .primary,
      .secondary {
        width: 100%;
      }

      .image-frame {
        min-height: 330px;
      }

      .steps {
        grid-template-columns: 1fr;
      }

      .categories {
        grid-template-columns: 1fr 1fr;
      }

      .category {
        padding: 17px 14px;
      }

      .calculator-preview {
        padding: 23px;
      }

      .final-cta {
        padding: 75px 10px;
      }
    }
  </style>
</head>

<body>

  <!-- HEADER -->
  <header>
    <div class="container nav">

      <a href="#" class="logo">
        Interior<span>Wise</span>
      </a>

      <nav class="desktop-nav">
        <a href="#calculator">Calculator</a>
        <a href="#rates">Interior Rates</a>
        <a href="#how">How It Works</a>
        <a href="#consultation" class="nav-button">Get Consultation</a>
      </nav>

      <button class="menu" aria-label="Menu">☰</button>

    </div>
  </header>


  <main>

    <!-- HERO -->
    <section class="hero">
      <div class="container hero-grid">

        <div>

          <div class="eyebrow">
            Delhi Interior Planning
          </div>

          <h1>
            Know your interior cost
            <span>before you start.</span>
          </h1>

          <p class="hero-text">
            Understand your home's interior requirements, explore realistic
            cost ranges and take your next step with more confidence.
          </p>

          <div class="actions">

            <a href="#calculator" class="primary">
              Calculate My Budget →
            </a>

            <a href="#consultation" class="secondary">
              Get Consultation
            </a>

          </div>

          <p class="hero-note">
            Built for homeowners in Delhi · Planning estimates, not final quotations
          </p>

        </div>


        <div class="hero-visual">

          <div class="image-frame">

            <div class="image-label">
              <small>Plan smarter</small>
              <strong>Know what you're paying for.</strong>
            </div>

          </div>

        </div>

      </div>
    </section>


    <!-- TRUST -->
    <div class="trust">
      <div class="container">

        <div class="trust-box">

          <div class="trust-item">
            <div class="trust-icon">₹</div>
            <div>
              <strong>Understand the cost</strong>
              <span>Work-wise planning estimates</span>
            </div>
          </div>

          <div class="trust-item">
            <div class="trust-icon">✓</div>
            <div>
              <strong>Compare what's included</strong>
              <span>Materials, scope & specifications</span>
            </div>
          </div>

          <div class="trust-item">
            <div class="trust-icon">→</div>
            <div>
              <strong>Talk to a professional</strong>
              <span>Request a consultation</span>
            </div>
          </div>

        </div>

      </div>
    </div>


    <!-- HOW IT WORKS -->
    <section class="how" id="how">

      <div class="container">

        <div class="section-heading">

          <div class="eyebrow">
            Simple process
          </div>

          <h2>
            From confusion to a clear plan.
          </h2>

          <p>
            InteriorWise helps you understand your project before you commit
            to a professional or quotation.
          </p>

        </div>


        <div class="steps">

          <div class="step">
            <div class="step-number">01</div>
            <h3>Tell us about your home</h3>
            <p>
              Select your BHK, approximate area and location.
            </p>
          </div>

          <div class="step">
            <div class="step-number">02</div>
            <h3>Select your work</h3>
            <p>
              Kitchen, wardrobes, ceiling, painting and more.
            </p>
          </div>

          <div class="step">
            <div class="step-number">03</div>
            <h3>Choose your quality</h3>
            <p>
              Compare Basic, Standard and Premium requirements.
            </p>
          </div>

          <div class="step">
            <div class="step-number">04</div>
            <h3>Get your estimate</h3>
            <p>
              See an estimated project range before your consultation.
            </p>
          </div>

        </div>

      </div>

    </section>


    <!-- CALCULATOR -->
    <section id="calculator">

      <div class="container">

        <div class="calculator-preview">

          <div>

            <div class="eyebrow" style="color:#cbd9d3;">
              Delhi Budget Calculator
            </div>

            <h2>
              What could your interior cost?
            </h2>

            <p>
              Tell us about your home and requirements. We'll calculate a
              planning estimate based on the work you select.
            </p>

          </div>


          <div class="calc-card">

            <div class="calc-card-label">
              START WITH YOUR HOME
            </div>

            <div class="calc-card-title">
              Your project
            </div>

            <div class="fake-select">
              <span>Delhi</span>
              <span>⌄</span>
            </div>

            <div class="fake-select">
              <span>Choose BHK</span>
              <span>⌄</span>
            </div>

            <div class="fake-select">
              <span>Select interior work</span>
              <span>⌄</span>
            </div>

            <button
              class="calc-button"
              onclick="startCalculator()"
            >
              Start My Estimate →
            </button>

          </div>

        </div>

      </div>

    </section>


    <!-- CATEGORIES -->
    <section id="rates">

      <div class="container">

        <div class="section-heading">

          <div class="eyebrow">
            Explore
          </div>

          <h2>
            Interior work, clearly explained.
          </h2>

          <p>
            We'll show pricing by category and quality level, with clear
            information about what is included.
          </p>

        </div>


        <div class="categories">

          <div class="category">
            <div class="category-icon">▦</div>
            <strong>Modular Kitchen</strong>
            <span>Layout · Finish · Hardware</span>
          </div>

          <div class="category">
            <div class="category-icon">▥</div>
            <strong>Wardrobes</strong>
            <span>Material · Shutters · Hardware</span>
          </div>

          <div class="category">
            <div class="category-icon">□</div>
            <strong>TV Unit</strong>
            <span>Storage · Panels · Finish</span>
          </div>

          <div class="category">
            <div class="category-icon">⌂</div>
            <strong>False Ceiling</strong>
            <span>Material · Lighting · Finish</span>
          </div>

          <div class="category">
            <div class="category-icon">◫</div>
            <strong>Painting</strong>
            <span>Surface · Paint · Labour</span>
          </div>

          <div class="category">
            <div class="category-icon">◈</div>
            <strong>Furniture</strong>
            <span>Beds · Tables · Storage</span>
          </div>

          <div class="category">
            <div class="category-icon">⌁</div>
            <strong>Electrical</strong>
            <span>Points · Fixtures · Labour</span>
          </div>

          <div class="category">
            <div class="category-icon">◇</div>
            <strong>Flooring</strong>
            <span>Material · Installation</span>
          </div>

          <div class="category">
            <div