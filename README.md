<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>Md. Siddik Alom, Ph.D. — Biochemist & Structural Biologist</title>
  <link href="https://fonts.googleapis.com/css2?family=EB+Garamond:ital,wght@0,400;0,500;0,600;1,400&family=Inter:wght@300;400;500;600&display=swap" rel="stylesheet"/>
  <style>
    *, *::before, *::after { box-sizing: border-box; margin: 0; padding: 0; }

    :root {
      --ink:       #1a1a2e;
      --ink-soft:  #3d3d5c;
      --ink-muted: #7a7a99;
      --accent:    #2e6b9e;
      --accent-lt: #d6eaf8;
      --gold:      #b8860b;
      --bg:        #f9f8f5;
      --bg-card:   #ffffff;
      --rule:      #e2e0da;
      --serif:     'EB Garamond', Georgia, serif;
      --sans:      'Inter', system-ui, sans-serif;
    }

    html { scroll-behavior: smooth; }

    body {
      font-family: var(--sans);
      background: var(--bg);
      color: var(--ink);
      font-size: 16px;
      line-height: 1.7;
    }

    /* NAV */
    nav {
      position: fixed; top: 0; left: 0; right: 0;
      background: rgba(249,248,245,0.94);
      backdrop-filter: blur(8px);
      border-bottom: 1px solid var(--rule);
      z-index: 100;
      padding: 0 2rem;
      display: flex;
      align-items: center;
      justify-content: space-between;
      height: 60px;
    }
    .nav-name {
      font-family: var(--serif);
      font-size: 1.1rem;
      font-weight: 500;
      color: var(--ink);
    }
    .nav-links { display: flex; gap: 1.6rem; list-style: none; }
    .nav-links a {
      text-decoration: none;
      font-size: 0.78rem;
      font-weight: 500;
      letter-spacing: 0.07em;
      text-transform: uppercase;
      color: var(--ink-soft);
      transition: color 0.2s;
    }
    .nav-links a:hover { color: var(--accent); }

    /* HERO */
    #hero {
      min-height: 100vh;
      display: flex;
      align-items: center;
      padding: 7rem 2rem 5rem;
      max-width: 920px;
      margin: 0 auto;
    }
    .hero-inner { width: 100%; }
    .hero-eyebrow {
      font-size: 0.78rem;
      font-weight: 600;
      letter-spacing: 0.14em;
      text-transform: uppercase;
      color: var(--accent);
      margin-bottom: 1.2rem;
    }
    .hero-name {
      font-family: var(--serif);
      font-size: clamp(2.8rem, 7vw, 5rem);
      font-weight: 500;
      line-height: 1.08;
      color: var(--ink);
      margin-bottom: 1.4rem;
    }
    .hero-name em { font-style: italic; color: var(--accent); }
    .hero-tagline {
      font-size: 1.15rem;
      color: var(--ink-soft);
      max-width: 640px;
      line-height: 1.75;
      margin-bottom: 2.4rem;
    }
    .hero-links { display: flex; gap: 1rem; flex-wrap: wrap; }
    .btn {
      display: inline-block;
      padding: 0.65rem 1.5rem;
      border-radius: 4px;
      font-size: 0.85rem;
      font-weight: 500;
      text-decoration: none;
      letter-spacing: 0.03em;
      transition: all 0.2s;
    }
    .btn-primary { background: var(--accent); color: #fff; }
    .btn-primary:hover { background: #1d5480; }
    .btn-outline { border: 1.5px solid var(--accent); color: var(--accent); background: transparent; }
    .btn-outline:hover { background: var(--accent-lt); }

    .hero-stats {
      display: flex;
      gap: 3rem;
      margin-top: 3.5rem;
      padding-top: 2.5rem;
      border-top: 1px solid var(--rule);
      flex-wrap: wrap;
    }
    .stat-num {
      font-family: var(--serif);
      font-size: 2.4rem;
      font-weight: 500;
      color: var(--ink);
      line-height: 1;
    }
    .stat-label {
      font-size: 0.75rem;
      color: var(--ink-muted);
      letter-spacing: 0.05em;
      text-transform: uppercase;
      margin-top: 0.3rem;
    }

    /* SECTIONS */
    section {
      max-width: 920px;
      margin: 0 auto;
      padding: 5rem 2rem;
      border-top: 1px solid var(--rule);
    }
    .section-label {
      font-size: 0.75rem;
      font-weight: 600;
      letter-spacing: 0.14em;
      text-transform: uppercase;
      color: var(--accent);
      margin-bottom: 0.5rem;
    }
    .section-title {
      font-family: var(--serif);
      font-size: clamp(1.8rem, 4vw, 2.6rem);
      font-weight: 500;
      color: var(--ink);
      margin-bottom: 2.5rem;
      line-height: 1.2;
    }

    /* ABOUT */
    .about-grid {
      display: grid;
      grid-template-columns: 1fr 1fr;
      gap: 3rem;
      align-items: start;
    }
    .about-text p {
      color: var(--ink-soft);
      margin-bottom: 1.2rem;
      font-size: 1rem;
    }
    .about-highlight {
      background: var(--accent-lt);
      border-left: 3px solid var(--accent);
      padding: 1rem 1.4rem;
      border-radius: 0 4px 4px 0;
      font-size: 0.93rem;
      color: var(--ink-soft);
      margin-top: 1.5rem;
      line-height: 1.65;
    }
    .sidebar-card {
      background: var(--bg-card);
      border: 1px solid var(--rule);
      border-radius: 6px;
      padding: 1.4rem;
      margin-bottom: 1rem;
    }
    .sidebar-card h4 {
      font-size: 0.72rem;
      font-weight: 600;
      letter-spacing: 0.1em;
      text-transform: uppercase;
      color: var(--ink-muted);
      margin-bottom: 0.8rem;
    }
    .sidebar-card ul { list-style: none; }
    .sidebar-card ul li {
      font-size: 0.88rem;
      color: var(--ink-soft);
      line-height: 1.6;
      padding-left: 1rem;
      position: relative;
      margin-bottom: 0.3rem;
    }
    .sidebar-card ul li::before { content: "→ "; position: absolute; left: 0; color: var(--accent); }

    /* EXPERIENCE */
    .timeline { position: relative; }
    .timeline-item {
      display: grid;
      grid-template-columns: 140px 1fr;
      gap: 2rem;
      margin-bottom: 3rem;
      position: relative;
    }
    .timeline-date { text-align: right; padding-top: 0.2rem; }
    .timeline-date span {
      font-size: 0.75rem;
      font-weight: 600;
      letter-spacing: 0.05em;
      color: var(--ink-muted);
      text-transform: uppercase;
    }
    .timeline-dot {
      position: absolute;
      left: 150px;
      top: 8px;
      width: 9px; height: 9px;
      border-radius: 50%;
      background: var(--accent);
      border: 2px solid var(--bg);
      box-shadow: 0 0 0 1.5px var(--accent);
    }
    .timeline-line {
      position: absolute;
      left: 153px; top: 20px; bottom: 0;
      width: 1px;
      background: var(--rule);
    }
    .timeline-body { padding-left: 1.5rem; }
    .timeline-role {
      font-family: var(--serif);
      font-size: 1.22rem;
      font-weight: 500;
      color: var(--ink);
      margin-bottom: 0.15rem;
    }
    .timeline-org {
      font-size: 0.84rem;
      color: var(--accent);
      font-weight: 500;
      margin-bottom: 0.8rem;
    }
    .timeline-body ul { list-style: none; }
    .timeline-body ul li {
      font-size: 0.92rem;
      color: var(--ink-soft);
      padding-left: 1.1rem;
      position: relative;
      margin-bottom: 0.5rem;
      line-height: 1.6;
    }
    .timeline-body ul li::before { content: "–"; position: absolute; left: 0; color: var(--accent); }
    .timeline-tag {
      display: inline-block;
      background: var(--accent-lt);
      color: var(--accent);
      font-size: 0.7rem;
      font-weight: 600;
      letter-spacing: 0.06em;
      text-transform: uppercase;
      padding: 0.2rem 0.6rem;
      border-radius: 3px;
      margin-bottom: 0.7rem;
    }

    /* SKILLS */
    .skills-grid {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(240px, 1fr));
      gap: 1.2rem;
    }
    .skill-card {
      background: var(--bg-card);
      border: 1px solid var(--rule);
      border-radius: 6px;
      padding: 1.4rem;
      transition: border-color 0.2s, box-shadow 0.2s;
    }
    .skill-card:hover {
      border-color: var(--accent);
      box-shadow: 0 2px 12px rgba(46,107,158,0.08);
    }
    .skill-card h4 {
      font-size: 0.72rem;
      font-weight: 600;
      letter-spacing: 0.1em;
      text-transform: uppercase;
      color: var(--accent);
      margin-bottom: 0.9rem;
    }
    .skill-tags { display: flex; flex-wrap: wrap; gap: 0.4rem; }
    .skill-tag {
      background: var(--bg);
      border: 1px solid var(--rule);
      color: var(--ink-soft);
      font-size: 0.78rem;
      padding: 0.22rem 0.55rem;
      border-radius: 3px;
    }

    /* PUBLICATIONS */
    .pub-list { list-style: none; }
    .pub-item {
      display: flex;
      gap: 1.5rem;
      padding: 1.4rem 0;
      border-bottom: 1px solid var(--rule);
      align-items: flex-start;
    }
    .pub-num {
      font-family: var(--serif);
      font-size: 1rem;
      color: var(--ink-muted);
      min-width: 28px;
      font-style: italic;
      padding-top: 0.15rem;
    }
    .pub-title {
      font-family: var(--serif);
      font-size: 1.02rem;
      color: var(--ink);
      line-height: 1.45;
      margin-bottom: 0.25rem;
    }
    .pub-authors { font-size: 0.82rem; color: var(--ink-muted); margin-bottom: 0.25rem; }
    .pub-journal { font-size: 0.82rem; color: var(--accent); font-weight: 500; }
    .pub-badge {
      display: inline-block;
      font-size: 0.68rem;
      font-weight: 600;
      padding: 0.15rem 0.5rem;
      border-radius: 3px;
      margin-left: 0.5rem;
      letter-spacing: 0.05em;
      text-transform: uppercase;
      vertical-align: middle;
    }
    .badge-first { background: #fff3cd; color: #856404; }
    .badge-equal { background: #e8f5e9; color: #2e7d32; }
    .badge-prep  { background: #f3e5f5; color: #6a1b9a; }

    /* CONFERENCES */
    .conf-list { list-style: none; }
    .conf-item {
      padding: 0.9rem 0;
      border-bottom: 1px solid var(--rule);
      display: flex;
      gap: 1.2rem;
      align-items: flex-start;
    }
    .conf-year {
      font-size: 0.78rem;
      font-weight: 600;
      color: var(--ink-muted);
      min-width: 38px;
      padding-top: 0.15rem;
    }
    .conf-body { font-size: 0.9rem; color: var(--ink-soft); line-height: 1.55; }
    .conf-body strong { color: var(--ink); font-weight: 500; }
    .conf-type {
      display: inline-block;
      font-size: 0.68rem;
      font-weight: 600;
      letter-spacing: 0.05em;
      text-transform: uppercase;
      padding: 0.12rem 0.45rem;
      border-radius: 3px;
      margin-left: 0.5rem;
      vertical-align: middle;
    }
    .type-oral { background: #fce4ec; color: #880e4f; }
    .type-poster { background: #e3f2fd; color: #0d47a1; }

    /* LEADERSHIP */
    .lead-grid {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(260px, 1fr));
      gap: 1.2rem;
    }
    .lead-card {
      background: var(--bg-card);
      border: 1px solid var(--rule);
      border-radius: 6px;
      padding: 1.4rem;
    }
    .lead-card h4 {
      font-family: var(--serif);
      font-size: 1.05rem;
      color: var(--ink);
      margin-bottom: 0.3rem;
    }
    .lead-card .lead-org {
      font-size: 0.8rem;
      color: var(--accent);
      font-weight: 500;
      margin-bottom: 0.6rem;
    }
    .lead-card p { font-size: 0.88rem; color: var(--ink-soft); line-height: 1.6; }

    /* CONTACT */
    #contact {
      background: var(--ink);
      color: #fff;
      max-width: 100%;
      padding: 5rem 2rem;
      border-top: none;
    }
    #contact .inner { max-width: 920px; margin: 0 auto; }
    #contact .section-label { color: #7ca8cc; }
    #contact .section-title { color: #fff; margin-bottom: 1rem; }
    #contact p { color: #a0b0c0; max-width: 520px; margin-bottom: 2.5rem; }
    .contact-grid { display: flex; gap: 2rem; flex-wrap: wrap; margin-bottom: 2.5rem; }
    .contact-item { display: flex; flex-direction: column; }
    .contact-item span { font-size: 0.7rem; letter-spacing: 0.1em; text-transform: uppercase; color: #7ca8cc; margin-bottom: 0.2rem; }
    .contact-item a { color: #fff; text-decoration: none; font-size: 0.93rem; transition: color 0.2s; }
    .contact-item a:hover { color: #7ca8cc; }
    .contact-note { font-size: 0.82rem; color: #5a7080; border-top: 1px solid #2a3a4a; padding-top: 1.5rem; }

    @media (max-width: 700px) {
      .about-grid { grid-template-columns: 1fr; }
      .timeline-item { grid-template-columns: 1fr; }
      .timeline-date { text-align: left; }
      .timeline-dot, .timeline-line { display: none; }
      .timeline-body { padding-left: 0; }
      nav .nav-links { display: none; }
      .hero-stats { gap: 1.5rem; }
    }
  </style>
</head>
<body>

<nav>
  <div class="nav-name">Md. Siddik Alom, Ph.D.</div>
  <ul class="nav-links">
    <li><a href="#about">About</a></li>
    <li><a href="#experience">Experience</a></li>
    <li><a href="#skills">Skills</a></li>
    <li><a href="#publications">Publications</a></li>
    <li><a href="#conferences">Conferences</a></li>
    <li><a href="#leadership">Leadership</a></li>
    <li><a href="#contact">Contact</a></li>
  </ul>
</nav>

<!-- HERO -->
<section id="hero" style="border-top:none;">
  <div class="hero-inner">
    <div class="hero-eyebrow">Postdoctoral Scholar · Brown University · Providence, RI</div>
    <h1 class="hero-name">Md. Siddik<br>Alom, <em>Ph.D.</em></h1>
    <p class="hero-tagline">
      Biochemist and structural biologist with 7+ years studying how ribosomes are assembled, regulated, and go wrong in disease — from purifying 5.8 kDa proteins nobody else could isolate, to solving cryo-EM structures of cancer-associated stalled ribosomes.
    </p>
    <div class="hero-links">
      <a href="#contact" class="btn btn-primary">Get in Touch</a>
      <a href="https://scholar.google.com/citations?user=1ujg8QkAAAAJ&hl=en" target="_blank" class="btn btn-outline">Google Scholar</a>
      <a href="https://linkedin.com" target="_blank" class="btn btn-outline">LinkedIn</a>
    </div>
    <div class="hero-stats">
      <div>
        <div class="stat-num">7+</div>
        <div class="stat-label">Years Research</div>
      </div>
      <div>
        <div class="stat-num">7</div>
        <div class="stat-label">Publications</div>
      </div>
      <div>
        <div class="stat-num">10</div>
        <div class="stat-label">Conferences</div>
      </div>
      <div>
        <div class="stat-num">4</div>
        <div class="stat-label">Countries</div>
      </div>
    </div>
  </div>
</section>

<!-- ABOUT -->
<section id="about">
  <div class="section-label">About</div>
  <h2 class="section-title">The science behind the résumé</h2>
  <div class="about-grid">
    <div class="about-text">
      <p>
        I'm a biochemist who is genuinely fascinated by the ribosome — not just as a textbook machine, but as a dynamic, tightly regulated assembly that cells invest enormous energy to get right. My Ph.D. at Ohio State focused on a deceptively simple question: what happens when a single ribosomal protein is missing? The answer turned out to involve a cascade of compensatory mechanisms, structural rearrangements, and cross-species evolutionary surprises.
      </p>
      <p>
        My current work at Brown University pushes that curiosity into human disease. I'm working to determine the cryo-EM structure of PA2G4-stalled ribosomes — a system directly tied to cancer-associated translational dysregulation. It's the kind of problem where protein biochemistry, structural biology, and cell biology all have to speak the same language.
      </p>
      <p>
        Before my U.S. research career, I spent nearly two years in GMP pharmaceutical manufacturing at ACI Pharmaceuticals in Bangladesh — an experience that shaped how I think about rigor, documentation, and quality in a regulated environment. It's not something most academic scientists have, and I bring that mindset into everything I do.
      </p>
      <div class="about-highlight">
        I'm actively exploring Research Scientist and Senior Scientist roles in biotech and pharmaceuticals — particularly where deep protein biochemistry, structural biology, or RNA biology expertise can drive real therapeutic impact.
      </div>
    </div>
    <div class="about-sidebar">
      <div class="sidebar-card">
        <h4>Current Position</h4>
        <ul>
          <li>Postdoctoral Scholar, Brown University</li>
          <li>Providence, RI · Open to Relocation</li>
          <li>Lawful Permanent Resident</li>
        </ul>
      </div>
      <div class="sidebar-card">
        <h4>Education</h4>
        <ul>
          <li>Ph.D. Biochemistry — Ohio State (2025)</li>
          <li>M.S. Biophysical Chemistry — Mississippi State (2020)</li>
          <li>M.S. Biochemistry & Mol. Bio. — Univ. of Dhaka (2015)</li>
          <li>B.S. Biochemistry & Mol. Bio. — Univ. of Dhaka (2013)</li>
        </ul>
      </div>
      <div class="sidebar-card">
        <h4>Professional Societies</h4>
        <ul>
          <li>The RNA Society</li>
          <li>American Society of Biochemistry & Molecular Biology</li>
          <li>American Chemistry Society</li>
          <li>Biophysical Society</li>
        </ul>
      </div>
      <div class="sidebar-card">
        <h4>Awards</h4>
        <ul>
          <li>Travel Grant, Center for RNA Biology, OSU (2024)</li>
          <li>National Science & Technology Fellowship, Bangladesh (2014–2015)</li>
        </ul>
      </div>
    </div>
  </div>
</section>

<!-- EXPERIENCE -->
<section id="experience">
  <div class="section-label">Experience</div>
  <h2 class="section-title">Where I've done the work</h2>
  <div class="timeline">

    <div class="timeline-item">
      <div class="timeline-date"><span>Feb 2026 – Present</span></div>
      <div class="timeline-dot"></div>
      <div class="timeline-line"></div>
      <div class="timeline-body">
        <div class="timeline-tag">Current</div>
        <div class="timeline-role">Postdoctoral Scholar</div>
        <div class="timeline-org">Brown University · Providence, RI</div>
        <ul>
          <li>Purifying factors associated with ribosome biogenesis by RAPPL and characterizing multi-protein complexes by cryo-EM, LC-MS, and biochemical techniques.</li>
          <li>Determining the cryo-EM structure of PA2G4-stalled ribosomes to uncover how polyA-track cancer-associated variants drive translational dysregulation — a direct mechanistic link between ribosome biology and cancer.</li>
        </ul>
      </div>
    </div>

    <div class="timeline-item">
      <div class="timeline-date"><span>Jun 2025 – Jan 2026</span></div>
      <div class="timeline-dot"></div>
      <div class="timeline-line"></div>
      <div class="timeline-body">
        <div class="timeline-role">Postdoctoral Scholar</div>
        <div class="timeline-org">The Ohio State University · Columbus, OH</div>
        <ul>
          <li>Characterized suppressor strains carrying dual chromosomal copies of uL6 and bL19/uS15 mutations, identifying compensatory mechanisms that restore growth in the absence of bL38.</li>
          <li>Probed the structural dynamics of uL6 from <em>F. johnsoniae</em> and <em>E. coli</em> by NMR to define the molecular basis of bL38-mediated ribosome stabilization.</li>
        </ul>
      </div>
    </div>

    <div class="timeline-item">
      <div class="timeline-date"><span>Aug 2020 – May 2025</span></div>
      <div class="timeline-dot"></div>
      <div class="timeline-line"></div>
      <div class="timeline-body">
        <div class="timeline-role">Graduate Research Associate</div>
        <div class="timeline-org">The Ohio State University · Columbus, OH</div>
        <ul>
          <li>Uncovered the function of ribosomal protein bL38 in 50S subunit assembly — published as first author in <em>Nucleic Acids Research</em> (2025); second paper in preparation.</li>
          <li>Purified some of the most challenging targets in the field: a 5.8 kDa ribosomal protein, chimeric constructs, and insoluble inclusion body-derived proteins — using affinity, ion exchange, and SEC on AKTA-FPLC.</li>
          <li>Determined ribosomal protein stoichiometry by LC-MS/MS; mapped rRNA processing sites; measured in vivo ribosome turnover and in vitro subunit dissociation rates.</li>
          <li>Collaborated with three external labs (Ortega, Foster, Bundschuh) on multidisciplinary structural and computational studies; mentored REU-funded undergraduates.</li>
        </ul>
      </div>
    </div>

    <div class="timeline-item">
      <div class="timeline-date"><span>Aug 2018 – Jul 2020</span></div>
      <div class="timeline-dot"></div>
      <div class="timeline-line"></div>
      <div class="timeline-body">
        <div class="timeline-role">Graduate Research Associate</div>
        <div class="timeline-org">Mississippi State University · Mississippi State, MS</div>
        <ul>
          <li>Built a first-of-its-kind residue-level affinity scale for protein–nanoparticle interactions by designing, expressing, and purifying 19 mutant variants of GB3 protein.</li>
          <li>Developed a novel <sup>15</sup>N-indole NMR method to quantify protein copy number on gold nanoparticle surfaces — published in <em>Nature Communications</em> and <em>Analytical Chemistry</em>.</li>
          <li>Mentored two REU-funded undergraduates; trained in LC-MS, ITC, and HPLC.</li>
        </ul>
      </div>
    </div>

    <div class="timeline-item">
      <div class="timeline-date"><span>Aug 2017 – Jul 2018</span></div>
      <div class="timeline-dot"></div>
      <div class="timeline-line"></div>
      <div class="timeline-body">
        <div class="timeline-role">Research Associate</div>
        <div class="timeline-org">Chonnam National University · Gwangju, South Korea</div>
        <ul>
          <li>Synthesized N-acryloyl glutamic acid and copolymerized it with acrylamide to engineer a mechanically tunable, self-recovering conductive hydrogel.</li>
          <li>Contributed to a parallel project on liquid crystalline monomeric compounds for functional hydrogel design.</li>
        </ul>
      </div>
    </div>

    <div class="timeline-item">
      <div class="timeline-date"><span>Sep 2015 – Jul 2017</span></div>
      <div class="timeline-dot"></div>
      <div class="timeline-line"></div>
      <div class="timeline-body">
        <div class="timeline-role">Quality Control Officer</div>
        <div class="timeline-org">ACI Pharmaceuticals Ltd. · Narayanganj, Bangladesh</div>
        <ul>
          <li>Executed in-process QC inspections of solid dosage forms in an FDA-approved GMP manufacturing environment — hardness, disintegration, dissolution, pH, moisture, and leakage testing per SOPs.</li>
          <li>Maintained complete batch records supporting regulatory audits; enforced line clearance protocols to eliminate cross-contamination risk between production runs.</li>
        </ul>
      </div>
    </div>

    <div class="timeline-item">
      <div class="timeline-date"><span>Spring 2023 – May 2025</span></div>
      <div class="timeline-dot"></div>
      <div class="timeline-line"></div>
      <div class="timeline-body">
        <div class="timeline-role">Graduate Teaching Assistant</div>
        <div class="timeline-org">The Ohio State University · Columbus, OH</div>
        <ul>
          <li>Assisted and graded Micro 4000 (Introductory Microbiology) and Micro 4140 (Molecular Microbiology); helped students work through PCR, SDS-PAGE, Western blotting, mutagenesis, and gene reporter systems.</li>
        </ul>
      </div>
    </div>

  </div>
</section>

<!-- SKILLS -->
<section id="skills">
  <div class="section-label">Technical Skills</div>
  <h2 class="section-title">What I can do in the lab</h2>
  <div class="skills-grid">
    <div class="skill-card">
      <h4>Protein Biochemistry</h4>
      <div class="skill-tags">
        <span class="skill-tag">Recombinant Expression</span>
        <span class="skill-tag">Affinity Chromatography</span>
        <span class="skill-tag">Ion Exchange</span>
        <span class="skill-tag">SEC</span>
        <span class="skill-tag">AKTA-FPLC (UNICORN)</span>
        <span class="skill-tag">Inclusion Body Recovery</span>
        <span class="skill-tag">SDS-PAGE / Native-PAGE</span>
        <span class="skill-tag">Western Blot</span>
        <span class="skill-tag">EMSA</span>
        <span class="skill-tag">DSF</span>
      </div>
    </div>
    <div class="skill-card">
      <h4>Analytical Techniques</h4>
      <div class="skill-tags">
        <span class="skill-tag">NMR (1D/2D/3D)</span>
        <span class="skill-tag">SEC-MALS</span>
        <span class="skill-tag">HPLC-SEC</span>
        <span class="skill-tag">LC-MS/MS</span>
        <span class="skill-tag">DLS</span>
        <span class="skill-tag">Circular Dichroism</span>
        <span class="skill-tag">UV-Vis</span>
        <span class="skill-tag">Autoradiography</span>
        <span class="skill-tag">ITC</span>
        <span class="skill-tag">TopSpin / NMRPipe / Sparky</span>
      </div>
    </div>
    <div class="skill-card">
      <h4>Molecular Biology</h4>
      <div class="skill-tags">
        <span class="skill-tag">Molecular Cloning</span>
        <span class="skill-tag">Vector Design</span>
        <span class="skill-tag">PCR / RT-PCR</span>
        <span class="skill-tag">DNA / RNA Extraction</span>
        <span class="skill-tag">Polysome Profiling</span>
        <span class="skill-tag">Primer Extension</span>
        <span class="skill-tag">Ribosome & Subunit Purification</span>
        <span class="skill-tag">ELISA</span>
      </div>
    </div>
    <div class="skill-card">
      <h4>Structural Biology</h4>
      <div class="skill-tags">
        <span class="skill-tag">Cryo-EM Sample Prep</span>
        <span class="skill-tag">CryoSPARC</span>
        <span class="skill-tag">ChimeraX</span>
        <span class="skill-tag">PyMOL</span>
      </div>
    </div>
    <div class="skill-card">
      <h4>GMP & Regulatory</h4>
      <div class="skill-tags">
        <span class="skill-tag">FDA GMP Environment</span>
        <span class="skill-tag">SOP Compliance</span>
        <span class="skill-tag">Batch Records</span>
        <span class="skill-tag">In-Process Testing</span>
        <span class="skill-tag">Regulatory Documentation</span>
      </div>
    </div>
    <div class="skill-card">
      <h4>Scientific & Software</h4>
      <div class="skill-tags">
        <span class="skill-tag">Scientific Writing</span>
        <span class="skill-tag">Manuscript Review</span>
        <span class="skill-tag">Adobe Illustrator</span>
        <span class="skill-tag">Microsoft Office</span>
        <span class="skill-tag">R (Beginner)</span>
        <span class="skill-tag">English</span>
        <span class="skill-tag">Bangla</span>
      </div>
    </div>
  </div>
</section>

<!-- PUBLICATIONS -->
<section id="publications">
  <div class="section-label">Publications</div>
  <h2 class="section-title">Research output</h2>
  <ul class="pub-list">

    <li class="pub-item">
      <div class="pub-num">1</div>
      <div class="pub-body">
        <div class="pub-title">
          Protein bL38 facilitates incorporation of uL6 during assembly of the 50S subunit in <em>Flavobacterium johnsoniae</em>
          <span class="pub-badge badge-first">First Author</span>
        </div>
        <div class="pub-authors">Alom, M.S., Arpin, D., Zhu, H., Hay, B.N., Foster, L.J., Ortega, J., Fredrick, K.</div>
        <div class="pub-journal">Nucleic Acids Research, 2025 · <a href="https://doi.org/10.1093/nar/gkaf120" target="_blank" style="color:var(--accent);">doi:10.1093/nar/gkaf120</a></div>
      </div>
    </li>

    <li class="pub-item">
      <div class="pub-num">2</div>
      <div class="pub-body">
        <div class="pub-title">
          Structure-Guided Antiviral Peptides Identification Targeting the HIV-1 Integrase
          <span class="pub-badge badge-equal">Equal Contribution</span>
        </div>
        <div class="pub-authors">Hossain, M.S.*, Alom, M.S.*, Kader, M.S., Hossain, M.A., Halim, M.A.</div>
        <div class="pub-journal">ACS Physical Chemistry Au, 2024 · <a href="https://doi.org/10.1021/acsphyschemau.4c00006" target="_blank" style="color:var(--accent);">doi:10.1021/acsphyschemau.4c00006</a></div>
      </div>
    </li>

    <li class="pub-item">
      <div class="pub-num">3</div>
      <div class="pub-body">
        <div class="pub-title">Unraveling the Impact of ORF3a Q57H Mutation on SARS-CoV-2: Insights from Molecular Dynamics</div>
        <div class="pub-authors">Islam, M.J., Alom, M.S., Hossain, M.S., et al.</div>
        <div class="pub-journal">Journal of Biomolecular Structure and Dynamics, 2023</div>
      </div>
    </li>

    <li class="pub-item">
      <div class="pub-num">4</div>
      <div class="pub-body">
        <div class="pub-title">A review on structural, non-structural, and accessory proteins of SARS-CoV-2: Highlighting drug target sites</div>
        <div class="pub-authors">Islam, M.J., Islam, N.N., Alom, M.S., Kabir, M., Halim, M.A.</div>
        <div class="pub-journal">Immunobiology, 2023</div>
      </div>
    </li>

    <li class="pub-item">
      <div class="pub-num">5</div>
      <div class="pub-body">
        <div class="pub-title">Predicting protein function and orientation on a gold nanoparticle surface using a residue-based affinity scale</div>
        <div class="pub-authors">Xu, J.X., Alom, M.S., Yadav, R., Fitzkee, N.C.</div>
        <div class="pub-journal">Nature Communications, 2022 · <a href="https://doi.org/10.1038/s41467-022-34749-w" target="_blank" style="color:var(--accent);">doi:10.1038/s41467-022-34749-w</a></div>
      </div>
    </li>

    <li class="pub-item">
      <div class="pub-num">6</div>
      <div class="pub-body">
        <div class="pub-title">Antioxidant Assessment of Agricultural Produce Using Fluorescence Techniques: A Review</div>
        <div class="pub-authors">Khaliduzzaman, A., Omwange, K.A., Al Riza, D.F., ..., Alom, M.S., et al.</div>
        <div class="pub-journal">Critical Reviews in Food Science and Nutrition, 2021</div>
      </div>
    </li>

    <li class="pub-item">
      <div class="pub-num">7</div>
      <div class="pub-body">
        <div class="pub-title">
          Quantitative Measurement of Multiprotein Nanoparticle Interactions Using NMR Spectroscopy
          <span class="pub-badge badge-equal">Equal Contribution</span>
        </div>
        <div class="pub-authors">Xu, J.X.*, Alom, M.S.*, Fitzkee, N.C.</div>
        <div class="pub-journal">Analytical Chemistry, 2021 · <a href="https://doi.org/10.1021/acs.analchem.1c01911" target="_blank" style="color:var(--accent);">doi:10.1021/acs.analchem.1c01911</a></div>
      </div>
    </li>

    <li class="pub-item">
      <div class="pub-num">—</div>
      <div class="pub-body">
        <div class="pub-title">
          Identification of suppressors with mutations in uS15 and bL19 that grow in the absence of bL38 by destabilizing intersubunit bridges in <em>F. johnsoniae</em>
          <span class="pub-badge badge-prep">In Preparation</span>
        </div>
        <div class="pub-authors">Alom, M.S., Gemler, B.T., Bundschuh, R., Fredrick, K.</div>
        <div class="pub-journal">Manuscript in preparation</div>
      </div>
    </li>

  </ul>
</section>

<!-- CONFERENCES -->
<section id="conferences">
  <div class="section-label">Conferences & Presentations</div>
  <h2 class="section-title">Sharing the science</h2>
  <ul class="conf-list">

    <li class="conf-item">
      <div class="conf-year">2024</div>
      <div class="conf-body">
        <strong>Annual Micro Symposium</strong>, Dept. of Microbiology, OSU
        <span class="conf-type type-oral">Oral</span><br>
        "Protein L38 facilitates L6 incorporation during 50S subunit assembly in <em>F. johnsoniae</em>"
      </div>
    </li>
    <li class="conf-item">
      <div class="conf-year">2024</div>
      <div class="conf-body">
        <strong>Translational Control Meeting</strong>, Cold Spring Harbor Laboratory, USA
        <span class="conf-type type-poster">Poster</span>
      </div>
    </li>
    <li class="conf-item">
      <div class="conf-year">2024</div>
      <div class="conf-body">
        <strong>Rustbelt RNA Meeting</strong>, Newark, OH, USA
        <span class="conf-type type-poster">Poster</span>
      </div>
    </li>
    <li class="conf-item">
      <div class="conf-year">2024</div>
      <div class="conf-body">
        <strong>Biophysical Society Annual Meeting</strong>, Philadelphia, USA
        <span class="conf-type type-poster">Poster</span>
      </div>
    </li>
    <li class="conf-item">
      <div class="conf-year">2023</div>
      <div class="conf-body">
        <strong>Annual Symposium, Center for RNA Biology</strong>, The Ohio State University
        <span class="conf-type type-poster">Poster</span>
      </div>
    </li>
    <li class="conf-item">
      <div class="conf-year">2022</div>
      <div class="conf-body">
        <strong>Ribosome Structure and Function Conference</strong>, Bordeaux, France
        <span class="conf-type type-poster">Poster</span><br>
        "Ribosomal protein bL38, a uniquely conserved component of the Bacteroidia ribosome"
      </div>
    </li>
    <li class="conf-item">
      <div class="conf-year">2022</div>
      <div class="conf-body">
        <strong>28th tRNA Conference</strong>, The Ohio State University
        <span class="conf-type type-poster">Poster</span>
      </div>
    </li>
    <li class="conf-item">
      <div class="conf-year">2022</div>
      <div class="conf-body">
        <strong>Annual Symposium, Center for RNA Biology</strong>, The Ohio State University
        <span class="conf-type type-poster">Poster</span>
      </div>
    </li>
    <li class="conf-item">
      <div class="conf-year">2021</div>
      <div class="conf-body">
        <strong>EMBL Conference on Protein Synthesis and Translational Control</strong>, Heidelberg, Germany
        <span class="conf-type type-poster">Poster</span><br>
        "Protein bL38 is an essential protein, uniquely conserved in the Bacteroidota"
      </div>
    </li>
    <li class="conf-item">
      <div class="conf-year">2020</div>
      <div class="conf-body">
        <strong>64th Annual Meeting of the Biophysical Society</strong>, San Diego, CA
        <span class="conf-type type-poster">Poster</span><br>
        "A Host-Guest System for understanding Protein-Nanoparticle Interactions"
      </div>
    </li>

  </ul>
</section>

<!-- LEADERSHIP -->
<section id="leadership">
  <div class="section-label">Leadership & Community</div>
  <h2 class="section-title">Beyond the bench</h2>
  <div class="lead-grid">
    <div class="lead-card">
      <h4>Founding President, BGSA</h4>
      <div class="lead-org">The Ohio State University · Columbus, OH</div>
      <p>Founded and led the Bangladeshi Graduate Student Association at OSU, building a support community for Bangladeshi researchers and students on campus.</p>
    </div>
    <div class="lead-card">
      <h4>President, BACABANA Ohio Chapter</h4>
      <div class="lead-org">2023 – Present</div>
      <p>Leading the Ohio chapter of the Bangladeshi-American community organization, coordinating events and fostering professional and cultural connections across the state.</p>
    </div>
    <div class="lead-card">
      <h4>VITA Tax Volunteer</h4>
      <div class="lead-org">UMBC · 2022 – Present</div>
      <p>Volunteering with the IRS Volunteer Income Tax Assistance program, helping low-income community members file taxes accurately and access credits they're entitled to.</p>
    </div>
    <div class="lead-card">
      <h4>Undergraduate Mentor</h4>
      <div class="lead-org">Ohio State & Mississippi State</div>
      <p>Mentored multiple REU-funded undergraduate researchers across two institutions, guiding them through research design, lab techniques, and scientific communication.</p>
    </div>
  </div>
</section>

<!-- CONTACT -->
<section id="contact">
  <div class="inner">
    <div class="section-label">Contact</div>
    <h2 class="section-title">Let's talk science</h2>
    <p>I'm actively exploring Research Scientist and Senior Scientist opportunities in biotech and pharmaceuticals. If your team works on protein therapeutics, RNA biology, or structural biology — I'd love to hear from you.</p>
    <div class="contact-grid">
      <div class="contact-item">
        <span>Email</span>
        <a href="mailto:alom.1@buckeyemail.osu.edu">alom.1@buckeyemail.osu.edu</a>
      </div>
      <div class="contact-item">
        <span>Phone</span>
        <a href="tel:6626942392">(662) 694-2392</a>
      </div>
      <div class="contact-item">
        <span>Location</span>
        <a href="#">Providence, RI · Open to Relocation</a>
      </div>
      <div class="contact-item">
        <span>LinkedIn</span>
        <a href="https://linkedin.com" target="_blank">linkedin.com/in/siddikalom</a>
      </div>
      <div class="contact-item">
        <span>Google Scholar</span>
        <a href="https://scholar.google.com/citations?user=1ujg8QkAAAAJ&hl=en" target="_blank">View Publications</a>
      </div>
    </div>
    <div class="contact-note">Lawful Permanent Resident · No visa sponsorship required</div>
  </div>
</section>

</body>
</html>
