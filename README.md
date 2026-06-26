<html lang="en">
<head>
<meta charset="UTF-8" />
<meta name="viewport" content="width=device-width, initial-scale=1.0"/>
<title>Akanksha Athavale — Digital Finance Portfolio</title>
<link href="https://fonts.googleapis.com/css2?family=Cormorant+Garamond:ital,wght@0,400;0,600;1,400&family=DM+Sans:wght@300;400;500&display=swap" rel="stylesheet"/>
<style>
  *, *::before, *::after { box-sizing: border-box; margin: 0; padding: 0; }

  :root {
    --ink:    #1a1a2e;
    --sage:   #4a7c6f;
    --gold:   #c9a84c;
    --cream:  #f8f5ef;
    --mist:   #e8e3d8;
    --white:  #ffffff;
    --body:   'DM Sans', sans-serif;
    --display:'Cormorant Garamond', Georgia, serif;
  }

  html { scroll-behavior: smooth; }

  body {
    font-family: var(--body);
    background: var(--cream);
    color: var(--ink);
    font-size: 15px;
    line-height: 1.7;
  }

  /* ── HERO ─────────────────────────────── */
  .hero {
    background: var(--ink);
    color: var(--white);
    min-height: 100vh;
    display: grid;
    grid-template-columns: 1fr 1fr;
    position: relative;
    overflow: hidden;
  }

  .hero::before {
    content: '';
    position: absolute;
    top: -120px; right: -120px;
    width: 480px; height: 480px;
    background: radial-gradient(circle, rgba(201,168,76,0.15) 0%, transparent 70%);
    pointer-events: none;
  }

  .hero-left {
    display: flex;
    flex-direction: column;
    justify-content: center;
    padding: 80px 60px 80px 80px;
  }

  .hero-eyebrow {
    font-family: var(--body);
    font-size: 11px;
    font-weight: 500;
    letter-spacing: 3px;
    text-transform: uppercase;
    color: var(--gold);
    margin-bottom: 28px;
  }

  .hero-name {
    font-family: var(--display);
    font-size: clamp(2.8rem, 5vw, 4.4rem);
    font-weight: 600;
    line-height: 1.1;
    margin-bottom: 20px;
  }

  .hero-name em {
    display: block;
    font-style: normal;
    font-weight: 600;
    color: var(--cream);
    font-size: 1em;
  }

  .hero-tagline {
    font-size: 16px;
    font-weight: 300;
    color: rgba(255,255,255,0.7);
    max-width: 400px;
    margin-bottom: 40px;
    line-height: 1.8;
  }

  .hero-contacts {
    display: flex;
    flex-direction: column;
    gap: 10px;
  }

  .contact-item {
    display: flex;
    align-items: center;
    gap: 12px;
    font-size: 13px;
    color: rgba(255,255,255,0.75);
  }

  .contact-item .icon {
    width: 28px; height: 28px;
    background: rgba(201,168,76,0.15);
    border: 1px solid rgba(201,168,76,0.3);
    border-radius: 50%;
    display: flex; align-items: center; justify-content: center;
    font-size: 12px;
    flex-shrink: 0;
  }

  .hero-right {
    display: flex;
    align-items: center;
    justify-content: center;
    padding: 80px 80px 80px 40px;
    position: relative;
  }

  .stat-grid {
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: 20px;
    width: 100%;
    max-width: 360px;
  }

  .stat-card {
    background: rgba(255,255,255,0.04);
    border: 1px solid rgba(255,255,255,0.1);
    border-radius: 12px;
    padding: 28px 24px;
    position: relative;
    overflow: hidden;
  }

  .stat-card::after {
    content: '';
    position: absolute;
    top: 0; left: 0;
    width: 3px; height: 100%;
    background: var(--gold);
  }

  .stat-card.wide { grid-column: 1 / -1; }

  .stat-number {
    font-family: var(--display);
    font-size: 2.8rem;
    font-weight: 600;
    color: var(--gold);
    line-height: 1;
    margin-bottom: 6px;
  }

  .stat-label {
    font-size: 12px;
    font-weight: 400;
    color: rgba(255,255,255,0.55);
    text-transform: uppercase;
    letter-spacing: 1px;
  }

  /* ── SECTION SHELL ────────────────────── */
  .section {
    padding: 90px 80px;
  }

  .section-alt { background: var(--white); }

  .section-header {
    display: flex;
    align-items: baseline;
    gap: 20px;
    margin-bottom: 56px;
  }

  .section-label {
    font-size: 10px;
    letter-spacing: 3px;
    text-transform: uppercase;
    color: var(--sage);
    font-weight: 500;
    white-space: nowrap;
  }

  .section-title {
    font-family: var(--display);
    font-size: clamp(1.9rem, 3vw, 2.6rem);
    font-weight: 600;
    color: var(--ink);
    line-height: 1.2;
  }

  .section-divider {
    flex: 1;
    height: 1px;
    background: var(--mist);
    align-self: center;
  }

  /* ── EXPERIENCE ───────────────────────── */
  .exp-list { display: flex; flex-direction: column; gap: 48px; }

  .exp-card {
    display: grid;
    grid-template-columns: 200px 1fr;
    gap: 40px;
    position: relative;
  }

  .exp-card::before {
    content: '';
    position: absolute;
    left: 200px;
    top: 0; bottom: 0;
    width: 1px;
    background: var(--mist);
    margin-left: 20px;
  }

  .exp-meta { padding-top: 4px; }

  .exp-period {
    font-size: 12px;
    font-weight: 500;
    color: var(--sage);
    letter-spacing: 0.5px;
    margin-bottom: 6px;
  }

  .exp-company {
    font-size: 13px;
    font-weight: 400;
    color: var(--ink);
    opacity: 0.55;
  }

  .exp-content { padding-left: 40px; }

  .exp-role {
    font-family: var(--display);
    font-size: 1.35rem;
    font-weight: 600;
    color: var(--ink);
    margin-bottom: 4px;
  }

  .exp-project {
    font-size: 12px;
    font-weight: 500;
    text-transform: uppercase;
    letter-spacing: 1.5px;
    color: var(--gold);
    margin-bottom: 16px;
  }

  .exp-bullets {
    list-style: none;
    display: flex;
    flex-direction: column;
    gap: 10px;
  }

  .exp-bullets li {
    padding-left: 20px;
    position: relative;
    font-size: 14px;
    color: #3a3a4a;
    line-height: 1.65;
  }

  .exp-bullets li::before {
    content: '';
    position: absolute;
    left: 0; top: 9px;
    width: 6px; height: 1px;
    background: var(--sage);
  }

  /* ── SKILLS ───────────────────────────── */
  .skills-grid {
    display: grid;
    grid-template-columns: repeat(3, 1fr);
    gap: 24px;
  }

  .skill-group {
    background: var(--cream);
    border-radius: 12px;
    padding: 28px 24px;
    border: 1px solid var(--mist);
  }

  .skill-group-title {
    font-size: 11px;
    font-weight: 500;
    letter-spacing: 2px;
    text-transform: uppercase;
    color: var(--sage);
    margin-bottom: 18px;
    padding-bottom: 14px;
    border-bottom: 1px solid var(--mist);
  }

  .skill-tags { display: flex; flex-wrap: wrap; gap: 8px; }

  .skill-tag {
    background: var(--white);
    border: 1px solid var(--mist);
    color: var(--ink);
    font-size: 12.5px;
    padding: 5px 12px;
    border-radius: 100px;
    font-weight: 400;
  }

  .skill-tag.highlight {
    background: var(--ink);
    color: var(--gold);
    border-color: var(--ink);
  }

  /* ── SAP DEEP-DIVE ────────────────────── */
  .sap-grid {
    display: grid;
    grid-template-columns: repeat(3, 1fr);
    gap: 16px;
  }

  .sap-item {
    background: var(--ink);
    color: var(--white);
    border-radius: 10px;
    padding: 22px 20px;
    position: relative;
    overflow: hidden;
  }

  .sap-item::before {
    content: '';
    position: absolute;
    bottom: -20px; right: -20px;
    width: 80px; height: 80px;
    background: rgba(201,168,76,0.08);
    border-radius: 50%;
  }

  .sap-code {
    font-family: 'Courier New', monospace;
    font-size: 1.1rem;
    font-weight: 700;
    color: var(--gold);
    margin-bottom: 6px;
  }

  .sap-desc {
    font-size: 12px;
    color: rgba(255,255,255,0.6);
    line-height: 1.5;
  }

  /* ── LANGUAGES ────────────────────────── */
  .lang-row {
    display: grid;
    grid-template-columns: repeat(4, 1fr);
    gap: 20px;
  }

  .lang-card {
    text-align: center;
    padding: 32px 20px;
    border: 1px solid var(--mist);
    border-radius: 12px;
    background: var(--white);
  }

  .lang-name {
    font-family: var(--display);
    font-size: 1.5rem;
    font-weight: 600;
    color: var(--ink);
    margin-bottom: 6px;
  }

  .lang-level {
    font-size: 11px;
    text-transform: uppercase;
    letter-spacing: 2px;
    color: var(--sage);
  }

  .lang-dots {
    display: flex;
    justify-content: center;
    gap: 5px;
    margin-top: 14px;
  }

  .dot {
    width: 8px; height: 8px;
    border-radius: 50%;
    background: var(--mist);
  }

  .dot.filled { background: var(--sage); }

  /* ── EDUCATION ────────────────────────── */
  .edu-list { display: flex; flex-direction: column; gap: 24px; }

  .edu-item {
    display: flex;
    align-items: flex-start;
    gap: 24px;
    padding: 28px;
    background: var(--white);
    border-radius: 12px;
    border-left: 3px solid var(--sage);
  }

  .edu-year {
    font-family: var(--display);
    font-size: 1.3rem;
    color: var(--sage);
    min-width: 80px;
    font-weight: 600;
  }

  .edu-degree {
    font-weight: 500;
    font-size: 15px;
    color: var(--ink);
    margin-bottom: 4px;
  }

  .edu-inst {
    font-size: 13px;
    color: #666;
  }

  /* ── FOOTER ───────────────────────────── */
  .footer {
    background: var(--ink);
    color: var(--white);
    text-align: center;
    padding: 60px 40px;
  }

  .footer-name {
    font-family: var(--display);
    font-size: 2rem;
    font-weight: 400;
    font-style: italic;
    color: var(--gold);
    margin-bottom: 14px;
  }

  .footer-note {
    font-size: 13px;
    color: rgba(255,255,255,0.5);
    letter-spacing: 1px;
  }

  @media (max-width: 900px) {
    .hero { grid-template-columns: 1fr; }
    .hero-left { padding: 60px 32px 40px; }
    .hero-right { padding: 0 32px 60px; }
    .stat-grid { max-width: 100%; }
    .section { padding: 60px 32px; }
    .exp-card { grid-template-columns: 1fr; }
    .exp-card::before { display: none; }
    .exp-content { padding-left: 0; }
    .skills-grid { grid-template-columns: 1fr; }
    .sap-grid { grid-template-columns: 1fr 1fr; }
    .lang-row { grid-template-columns: 1fr 1fr; }
  }
</style>
</head>
<body>

<!-- HERO -->
<section class="hero">
  <div class="hero-left">
    <p class="hero-eyebrow">Finance Professional · Digital Accountant</p>
    <h1 class="hero-name">
      Akanksha<br>
      Ashutosh<br>
      <em>Athavale</em>
    </h1>
    <p class="hero-tagline">
      AP &amp; GL Specialist | SAP FI · ERP · AI-Assisted Finance<br>
      5+ years across DE, AU, NZ, IN, USA environments.<br>
      Relocating to Germany/Europe. Open to work from day one.
    </p>
    <div class="hero-contacts">
      <div class="contact-item"><span class="icon">✉</span> akankshaathavale@gmail.com</div>
      <div class="contact-item"><span class="icon">📞</span> +91 7045089837 &nbsp;·&nbsp; +49 15210361068</div>
      <div class="contact-item"><span class="icon">📍</span> Mumbai, India · Relocating to Germany/Europe</div>
      <div class="contact-item"><span class="icon">in</span> <a href="https://www.linkedin.com/in/akankshaashutosh/" target="_blank" style="color:rgba(255,255,255,0.75); text-decoration:none;">Akanksha Athavale | LinkedIn</a></div>
    </div>
  </div>
  <div class="hero-right">
    <div class="stat-grid">
      <div class="stat-card">
        <div class="stat-number">5+</div>
        <div class="stat-label">Years AP Experience</div>
      </div>
      <div class="stat-card">
        <div class="stat-number">300+</div>
        <div class="stat-label">Vendors / Month</div>
      </div>
      <div class="stat-card">
        <div class="stat-number">150</div>
        <div class="stat-label">Daily Queries Handled</div>
      </div>
      <div class="stat-card">
        <div class="stat-number">100%</div>
        <div class="stat-label">Data Accuracy</div>
      </div>
      <div class="stat-card wide">
        <div class="stat-number">5</div>
        <div class="stat-label">Countries: DE · AU · NZ · IN · USA</div>
      </div>
    </div>
  </div>
</section>

<!-- PROFESSIONAL SUMMARY -->
<section class="section section-alt">
  <div class="section-header">
    <span class="section-label">About</span>
    <h2 class="section-title">Professional Summary</h2>
    <div class="section-divider"></div>
  </div>
  <p style="font-size:16px; line-height:1.9; max-width:820px; color:#3a3a4a;">
    Finance professional with over five years of hands-on Accounts Payable experience in SAP based multi-country environments. 
    Specialist in high volume invoice processing, 2-way/3-way PO matching, supplier master data management, and period end 
    reconciliation. Passionate about process automation and technology driven finance, actively building AI literacy to enhance 
    productivity and decision making. Experienced in applying ERP tools and digital workflows to streamline AP operations 
    in fast-paced international settings. <strong>Soon relocating to Germany/Europe; open to work from day one.</strong>
  </p>
</section>

<!-- EXPERIENCE -->
<section class="section">
  <div class="section-header">
    <span class="section-label">Career</span>
    <h2 class="section-title">Professional Experience</h2>
    <div class="section-divider"></div>
  </div>

  <div class="exp-list">

    <div class="exp-card">
      <div class="exp-meta">
        <div class="exp-period">May 2023 – Present</div>
        <div class="exp-company">Tata Consultancy Services</div>
      </div>
      <div class="exp-content">
        <div class="exp-role">Workflow Specialist</div>
        <div class="exp-project">Project Aurizon</div>
        <ul class="exp-bullets">
          <li>Managed end to end supplier master data lifecycle for 300+ vendors monthly in SAP, including bank account details, payment terms, tax IDs (ABN) and addresses, ensuring 100% data accuracy and compliance with internal controls.</li>
          <li>Acted as primary liaison between AP, procurement, and finance teams to resolve invoice discrepancies, PO mismatches, and payment exceptions.</li>
          <li>Created and maintained SOPs and operational playbooks for vendor payment and master data processes, supporting onboarding and process continuity.</li>
          <li>Utilised MS Excel for aging report preparation, payment prioritisation tracking, and vendor reconciliation dashboards including pivot tables and VLOOKUP-based data validation.</li>
          <li>Actively leveraged AI-assisted tools for data validation, SOP documentation, and workflow automation, contributing to a more efficient and scalable AP function.</li>
        </ul>
      </div>
    </div>

    <div class="exp-card">
      <div class="exp-meta">
        <div class="exp-period">May 2021 – Apr 2023</div>
        <div class="exp-company">Tata Consultancy Services</div>
      </div>
      <div class="exp-content">
        <div class="exp-role">Process Associate</div>
        <div class="exp-project">Project ELANCO · DE · AU · NZ · IN · USA</div>
        <ul class="exp-bullets">
          <li>Accounts Payable and Accounts Receivable for a US client spanning Germany, New Zealand, India, Australia, and the United States.</li>
          <li>Processed PO &amp; Non-PO invoices using SAP MIRO &amp; FB60 for Germany, compliant with HGB Standards (2-way/3-way matching).</li>
          <li>Performed GR/IR reconciliation and clearing for accurate inventory receipt valuation and liability recognition during monthly period end close across multiple company codes in SAP.</li>
          <li>Applied VAT compliance checks across European entities, verifying tax codes, VAT IDs, and documentation in SAP during invoice processing and period end close.</li>
          <li>Processed multi-currency invoices and payment runs across USD, EUR, AUD, and NZD, applying foreign currency valuation principles in SAP.</li>
          <li>Served as primary contact for 120–150 daily supplier and internal finance queries, resolving invoice disputes and payment status enquiries.</li>
          <li>Conducted QC audits to guarantee 100% accuracy in invoices and Purchase Orders.</li>
          <li>Supported month-end close including accrual postings, GL account clearing, and bank reconciliation across multiple company codes.</li>
        </ul>
      </div>
    </div>

  </div>
</section>

<!-- SAP SKILLS -->
<section class="section section-alt">
  <div class="section-header">
    <span class="section-label">Technical</span>
    <h2 class="section-title">SAP Transaction Codes</h2>
    <div class="section-divider"></div>
  </div>
  <div class="sap-grid">
    <div class="sap-item"><div class="sap-code">MIRO</div><div class="sap-desc">Incoming Invoice Verification against PO / GR</div></div>
    <div class="sap-item"><div class="sap-code">FB60</div><div class="sap-desc">Non-PO Vendor Invoice Entry</div></div>
    <div class="sap-item"><div class="sap-code">MR8M</div><div class="sap-desc">Reverse Invoice / Credit Memo against PO</div></div>
    <div class="sap-item"><div class="sap-code">F-44</div><div class="sap-desc">Manual Vendor Account Clearing</div></div>
    <div class="sap-item"><div class="sap-code">XK01</div><div class="sap-desc">Vendor Master Record Creation</div></div>
    <div class="sap-item"><div class="sap-code">XK03</div><div class="sap-desc">Display &amp; Maintain Vendor Master Record</div></div>
  </div>
</section>

<!-- CORE SKILLS -->
<section class="section">
  <div class="section-header">
    <span class="section-label">Capabilities</span>
    <h2 class="section-title">Core Skills</h2>
    <div class="section-divider"></div>
  </div>
  <div class="skills-grid">
    <div class="skill-group">
      <div class="skill-group-title">Accounts Payable</div>
      <div class="skill-tags">
        <span class="skill-tag highlight">PO Invoice Processing</span>
        <span class="skill-tag highlight">Non-PO Invoices</span>
        <span class="skill-tag">2-way / 3-way Matching</span>
        <span class="skill-tag">GR/IR Reconciliation</span>
        <span class="skill-tag">Payment Queue Mgmt</span>
        <span class="skill-tag">Duplicate Payment Control</span>
        <span class="skill-tag">EDI Invoice Handling</span>
      </div>
    </div>
    <div class="skill-group">
      <div class="skill-group-title">General Ledger & Compliance</div>
      <div class="skill-tags">
        <span class="skill-tag highlight">Month-End Close</span>
        <span class="skill-tag highlight">VAT Compliance (EU)</span>
        <span class="skill-tag">GL Account Clearing</span>
        <span class="skill-tag">Accrual Postings</span>
        <span class="skill-tag">Bank Reconciliation</span>
        <span class="skill-tag">HGB Standards (DE)</span>
        <span class="skill-tag">Audit Readiness</span>
      </div>
    </div>
    <div class="skill-group">
      <div class="skill-group-title">Tools & Technology</div>
      <div class="skill-tags">
        <span class="skill-tag highlight">SAP S/4HANA & ECC</span>
        <span class="skill-tag highlight">MS Excel</span>
        <span class="skill-tag">Pivot Tables</span>
        <span class="skill-tag">VLOOKUP / XLOOKUP</span>
        <span class="skill-tag">Aging Report Dashboards</span>
        <span class="skill-tag">AI-Assisted Workflows</span>
        <span class="skill-tag">SOP Documentation</span>
      </div>
    </div>
  </div>
</section>

<!-- EDUCATION -->
<section class="section section-alt">
  <div class="section-header">
    <span class="section-label">Education</span>
    <h2 class="section-title">Academic Background</h2>
    <div class="section-divider"></div>
  </div>
  <div class="edu-list">
    <div class="edu-item">
      <div class="edu-year">2024</div>
      <div>
        <div class="edu-degree">Master of Commerce (M.Com)</div>
        <div class="edu-inst">University of Mumbai, Mumbai, India · 2022–2024</div>
      </div>
    </div>
    <div class="edu-item">
      <div class="edu-year">2021</div>
      <div>
        <div class="edu-degree">Bachelor of Commerce (B.Com)</div>
        <div class="edu-inst">University of Mumbai, Mumbai, India · 2017–2021</div>
      </div>
    </div>
    <div class="edu-item">
      <div class="edu-year">🎵</div>
      <div>
        <div class="edu-degree">Bachelor's Degree in Music — First Class</div>
        <div class="edu-inst">Akhil Bharatiya Gandharva Mahavidyalaya · Indian Classical Music</div>
      </div>
    </div>
  </div>
</section>

<!-- LANGUAGES -->
<section class="section">
  <div class="section-header">
    <span class="section-label">Languages</span>
    <h2 class="section-title">Communication</h2>
    <div class="section-divider"></div>
  </div>
  <div class="lang-row">
    <div class="lang-card">
      <div class="lang-name">Marathi</div>
      <div class="lang-level">Native / Bilingual</div>
      <div class="lang-dots">
        <div class="dot filled"></div><div class="dot filled"></div><div class="dot filled"></div><div class="dot filled"></div><div class="dot filled"></div>
      </div>
    </div>
    <div class="lang-card">
      <div class="lang-name">Hindi</div>
      <div class="lang-level">Native / Bilingual</div>
      <div class="lang-dots">
        <div class="dot filled"></div><div class="dot filled"></div><div class="dot filled"></div><div class="dot filled"></div><div class="dot filled"></div>
      </div>
    </div>
    <div class="lang-card">
      <div class="lang-name">English</div>
      <div class="lang-level">Fluent</div>
      <div class="lang-dots">
        <div class="dot filled"></div><div class="dot filled"></div><div class="dot filled"></div><div class="dot filled"></div><div class="dot"></div>
      </div>
    </div>
    <div class="lang-card">
      <div class="lang-name">German</div>
      <div class="lang-level">Basic (Learning)</div>
      <div class="lang-dots">
        <div class="dot filled"></div><div class="dot"></div><div class="dot"></div><div class="dot"></div><div class="dot"></div>
      </div>
    </div>
  </div>
</section>

<!-- REFERENCES -->
<section class="section section-alt">
  <div class="section-header">
    <span class="section-label">References</span>
    <h2 class="section-title">Professional References</h2>
    <div class="section-divider"></div>
  </div>
  <div style="display:grid; grid-template-columns:1fr 1fr; gap:24px;">
    <div style="background:var(--cream); border:1px solid var(--mist); border-left:3px solid var(--gold); border-radius:12px; padding:28px 28px;">
      <div style="font-family:var(--display); font-size:1.2rem; font-weight:600; color:var(--ink); margin-bottom:4px;">Nimish Sharma</div>
      <div style="font-size:13px; color:var(--sage); font-weight:500; margin-bottom:14px;">Assistant General Manager · Tata Consultancy Services</div>
      <div style="font-size:13px; color:#555; display:flex; flex-direction:column; gap:6px;">
        <span>✉ nimish64@gmail.com</span>
        <span>📞 +91 8886177796</span>
      </div>
    </div>
    <div style="background:var(--cream); border:1px solid var(--mist); border-left:3px solid var(--gold); border-radius:12px; padding:28px 28px;">
      <div style="font-family:var(--display); font-size:1.2rem; font-weight:600; color:var(--ink); margin-bottom:4px;">
        <a href="https://www.linkedin.com/in/tanvi-shettigar-61022567/" target="_blank" style="color:var(--ink); text-decoration:none;">Tanvi Shettigar ↗</a>
      </div>
      <div style="font-size:13px; color:var(--sage); font-weight:500; margin-bottom:14px;">Team Lead Procurement AP · GEP Worldwide</div>
      <div style="font-size:13px; color:#555; display:flex; flex-direction:column; gap:6px;">
        <span>✉ Shettigartanvi@yahoo.com</span>
        <span>📞 +91 9769973539</span>
      </div>
    </div>
  </div>
</section>

<!-- FOOTER -->
<footer class="footer">
  <div class="footer-name">Akanksha Athavale</div>
  <p class="footer-note">akankshaathavale@gmail.com · +91 7045089837 · +49 15210361068 · Open to relocate to Germany / Europe</p>
</footer>

</body>
</html>
