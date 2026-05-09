<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>Pablo Angelo Cruz — Resume</title>
  <link href="https://fonts.googleapis.com/css2?family=Cormorant+Garamond:ital,wght@0,400;0,600;0,700;1,400&family=DM+Sans:ital,wght@0,300;0,400;0,500;1,300&display=swap" rel="stylesheet"/>
  <style>
    *, *::before, *::after { box-sizing: border-box; margin: 0; padding: 0; }

    :root {
      --ink:    #0f0f0f;
      --dark:   #1a1a1a;
      --mid:    #444;
      --muted:  #888;
      --rule:   #e8e8e8;
      --bg:     #fafaf8;
      --accent: #1d4ed8;
      --tag-bg: #f0f4ff;
    }

    html { scroll-behavior: smooth; }

    body {
      font-family: 'DM Sans', sans-serif;
      background: var(--bg);
      color: var(--dark);
      min-height: 100vh;
      padding: 3rem 1rem 5rem;
    }

    .page {
      max-width: 780px;
      margin: 0 auto;
      opacity: 0;
      transform: translateY(18px);
      animation: rise 0.7s ease forwards;
    }

    @keyframes rise {
      to { opacity: 1; transform: translateY(0); }
    }

    /* HEADER */
    header {
      border-bottom: 2px solid var(--ink);
      padding-bottom: 1.5rem;
      margin-bottom: 2.2rem;
    }

    .name {
      font-family: 'Cormorant Garamond', serif;
      font-size: clamp(2.6rem, 6vw, 3.8rem);
      font-weight: 700;
      color: var(--ink);
      letter-spacing: -0.02em;
      line-height: 1;
      margin-bottom: 0.6rem;
    }

    .contact {
      display: flex;
      flex-wrap: wrap;
      gap: 0.3rem 1.4rem;
      font-size: 0.82rem;
      font-weight: 300;
      color: var(--muted);
    }

    .contact span { display: flex; align-items: center; gap: 0.35rem; }

    .contact svg { width: 12px; height: 12px; opacity: 0.55; flex-shrink: 0; }

    /* SECTIONS */
    section { margin-bottom: 2.1rem; }

    .section-label {
      font-size: 0.67rem;
      font-weight: 500;
      letter-spacing: 0.2em;
      text-transform: uppercase;
      color: var(--muted);
      margin-bottom: 1rem;
      display: flex;
      align-items: center;
      gap: 0.8rem;
    }

    .section-label::after {
      content: '';
      flex: 1;
      height: 1px;
      background: var(--rule);
    }

    /* SUMMARY */
    .summary p {
      font-size: 0.88rem;
      line-height: 1.8;
      color: var(--mid);
      font-weight: 300;
    }

    /* SKILLS */
    .skills-grid {
      display: flex;
      flex-wrap: wrap;
      gap: 0.45rem;
    }

    .skill-tag {
      background: var(--tag-bg);
      color: var(--accent);
      font-size: 0.77rem;
      font-weight: 500;
      padding: 0.35rem 0.8rem;
      border-radius: 4px;
      border: 1px solid #dbeafe;
      letter-spacing: 0.01em;
    }

    /* ENTRY */
    .entry {
      display: grid;
      grid-template-columns: 1fr auto;
      column-gap: 1.2rem;
      margin-bottom: 1.6rem;
    }

    .entry:last-child { margin-bottom: 0; }

    .entry-org {
      font-family: 'Cormorant Garamond', serif;
      font-size: 1.15rem;
      font-weight: 600;
      color: var(--ink);
      line-height: 1.2;
    }

    .entry-role {
      font-size: 0.81rem;
      font-weight: 500;
      color: var(--accent);
      margin-top: 0.22rem;
    }

    .entry-stack {
      font-size: 0.75rem;
      color: var(--muted);
      font-weight: 300;
      margin-top: 0.2rem;
      font-style: italic;
    }

    .entry-meta {
      text-align: right;
      padding-top: 0.1rem;
    }

    .entry-meta .date {
      display: block;
      font-size: 0.78rem;
      color: var(--muted);
      font-weight: 300;
      white-space: nowrap;
    }

    .entry-meta .loc {
      display: block;
      font-size: 0.73rem;
      color: var(--rule);
      font-style: italic;
      margin-top: 0.2rem;
      white-space: nowrap;
    }

    .entry-bullets {
      grid-column: 1 / -1;
      margin-top: 0.7rem;
      list-style: none;
      display: flex;
      flex-direction: column;
      gap: 0.45rem;
    }

    .entry-bullets li {
      font-size: 0.84rem;
      line-height: 1.7;
      color: var(--mid);
      font-weight: 300;
      padding-left: 1.1rem;
      position: relative;
    }

    .entry-bullets li::before {
      content: '—';
      position: absolute;
      left: 0;
      color: #ccc;
    }

    .edu-note {
      grid-column: 1 / -1;
      margin-top: 0.55rem;
      font-size: 0.79rem;
      color: var(--muted);
      font-weight: 300;
      font-style: italic;
      line-height: 1.65;
    }

    footer {
      text-align: center;
      margin-top: 3.5rem;
      font-size: 0.68rem;
      color: #ccc;
      letter-spacing: 0.12em;
      text-transform: uppercase;
    }

    @media (max-width: 520px) {
      .entry { grid-template-columns: 1fr; }
      .entry-meta { text-align: left; margin-top: 0.3rem; }
      .entry-meta .loc { color: var(--muted); }
    }
  </style>
</head>
<body>
<div class="page">

  <header>
    <h1 class="name">Pablo Angelo Cruz</h1>
    <div class="contact">
      <span>
        <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2"><path d="M21 10c0 7-9 13-9 13s-9-6-9-13a9 9 0 0118 0z"/><circle cx="12" cy="10" r="3"/></svg>
        Bulacan, Philippines
      </span>
      <span>
        <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2"><path d="M22 16.92v3a2 2 0 01-2.18 2 19.79 19.79 0 01-8.63-3.07A19.5 19.5 0 013.07 9.81 19.79 19.79 0 01.07 1.18 2 2 0 012.03 0h3a2 2 0 012 1.72c.127.96.361 1.903.7 2.81a2 2 0 01-.45 2.11L6.09 7.91a16 16 0 006 6l1.27-1.27a2 2 0 012.11-.45c.907.339 1.85.573 2.81.7A2 2 0 0122 14.92z"/></svg>
        0938 *** ****
      </span>
      <span>
        <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2"><path d="M4 4h16c1.1 0 2 .9 2 2v12c0 1.1-.9 2-2 2H4c-1.1 0-2-.9-2-2V6c0-1.1.9-2 2-2z"/><polyline points="22,6 12,13 2,6"/></svg>
        pabacruz2020@gmail.com
      </span>
    </div>
  </header>

  <section class="summary">
    <div class="section-label">Profile</div>
    <p>Motivated IT fresh graduate with a Bachelor of Science in Information Systems, seeking an entry-level position in software development, QA, or related IT roles. Demonstrates hands-on experience in full-stack development, object-oriented programming, and database management gained through a government internship and academic projects. A fast learner, team player, and detail-oriented professional committed to delivering quality work and growing within a dynamic organization.</p>
  </section>

  <section>
    <div class="section-label">Skills</div>
    <div class="skills-grid">
      <div class="skill-tag">HTML</div>
      <div class="skill-tag">CSS</div>
      <div class="skill-tag">Python</div>
      <div class="skill-tag">Django</div>
      <div class="skill-tag">SQL</div>
      <div class="skill-tag">PostgreSQL</div>
      <div class="skill-tag">C#</div>
      <div class="skill-tag">WinForms</div>
      <div class="skill-tag">OOP</div>
      <div class="skill-tag">Full-Stack Dev</div>
      <div class="skill-tag">Agile</div>
      <div class="skill-tag">DB Design</div>
    </div>
  </section>

  <section>
    <div class="section-label">Experience</div>
    <div class="entry">
      <div>
        <div class="entry-org">Provincial Information Technology Office</div>
        <div class="entry-role">Developer Intern · Capstone</div>
        <div class="entry-stack">Python · Django · PostgreSQL</div>
      </div>
      <div class="entry-meta">
        <span class="date">Aug – Nov 2025</span>
        <span class="loc">Bulacan, Philippines</span>
      </div>
      <ul class="entry-bullets">
        <li>Designed and developed a full-stack Queueing Management System for the Provincial Treasury Office using Python and Django, reducing manual queue handling and improving service efficiency for government clients.</li>
        <li>Engineered queue flow logic, user interface, and database models for real-time ticket issuance and multi-counter status tracking.</li>
        <li>Collaborated with staff to gather requirements, conducted user testing, and iterated on features based on stakeholder feedback using agile development practices.</li>
        <li>Deployed and maintained the application within the provincial government's internal network, ensuring system stability and reliability.</li>
      </ul>
    </div>
  </section>

  <section>
    <div class="section-label">Academic Experience</div>
    <div class="entry">
      <div>
        <div class="entry-org">Car Rental Management System</div>
        <div class="entry-role">Lead Programmer · Mini Thesis (Group of 3)</div>
        <div class="entry-stack">C# · WinForms · SQL</div>
      </div>
      <div class="entry-meta">
        <span class="date">Aug – Dec 2023</span>
        <span class="loc">Bulacan Polytechnic College</span>
      </div>
      <ul class="entry-bullets">
        <li>Architected a Windows Forms desktop application in C# to automate car rental operations including vehicle inventory, booking, and client records.</li>
        <li>Implemented SQL database integration to manage rental transactions, customer data, and vehicle availability in real time.</li>
        <li>Served as sole programmer responsible for coding, debugging, and quality verification, gaining practical exposure to end-to-end software delivery.</li>
      </ul>
    </div>
  </section>

  <section>
    <div class="section-label">Education</div>
    <div class="entry">
      <div>
        <div class="entry-org">Bulacan Polytechnic College</div>
        <div class="entry-role">Bachelor of Science in Information Systems</div>
      </div>
      <div class="entry-meta">
        <span class="date">Aug 2022 – May 2026</span>
        <span class="loc">Bulacan, Philippines</span>
      </div>
      <p class="edu-note">Relevant Coursework: Systems Analysis &amp; Design · Database Management · Web Development · Software Engineering · Object-Oriented Programming</p>
    </div>
  </section>

  <footer>Pablo Angelo Cruz &nbsp;·&nbsp; Information Systems Graduate</footer>

</div>
</body>
</html>
