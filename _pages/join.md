---
layout: page
title: join us
permalink: /join/
nav: true
nav_order: 3
description: Chart the stars & oceans of AI with us.
_styles: |
  .post-header .post-title { text-transform: capitalize; }
  .post-header .post-description {
    font-size: 1.15rem;
    line-height: 1.6;
    color: var(--global-text-color-light);
    margin-bottom: 2.5rem;
  }
  .join-lead {
    font-size: 1.05rem;
    line-height: 1.75;
    margin-bottom: 2.5rem;
  }
  .join-section { margin-bottom: 3rem; }
  .join-section-title {
    font-size: 1.4rem;
    margin-bottom: 1.25rem;
    padding-bottom: 0.4rem;
    border-bottom: 2px solid var(--global-divider-color);
    color: var(--global-text-color);
  }
  .join-grid {
    display: grid;
    grid-template-columns: repeat(auto-fill, minmax(230px, 1fr));
    gap: 1.5rem;
  }
  .join-card {
    background: var(--global-card-bg-color);
    border: 1px solid var(--global-divider-color);
    border-radius: 14px;
    padding: 1.5rem 1.35rem;
    transition: transform 0.2s ease, box-shadow 0.2s ease, border-color 0.2s ease;
    display: flex;
    flex-direction: column;
  }
  .join-card:hover {
    transform: translateY(-4px);
    box-shadow: 0 10px 25px rgba(0, 0, 0, 0.12);
    border-color: var(--global-theme-color);
  }
  .join-card .card-icon {
    font-size: 1.6rem;
    color: var(--global-theme-color);
    margin-bottom: 0.75rem;
  }
  .join-card h3 {
    font-size: 1.1rem;
    margin: 0 0 0.5rem;
    color: var(--global-text-color);
  }
  .join-card p {
    font-size: 0.9rem;
    line-height: 1.55;
    color: var(--global-text-color-light);
    margin: 0;
  }
  .join-values { padding-left: 0; list-style: none; }
  .join-values li {
    position: relative;
    padding-left: 1.6rem;
    margin-bottom: 0.6rem;
    line-height: 1.6;
  }
  .join-values li::before {
    content: "\f111";
    font-family: "Font Awesome 6 Free";
    font-weight: 900;
    font-size: 0.45rem;
    color: var(--global-theme-color);
    position: absolute;
    left: 0;
    top: 0.55rem;
  }
  .apply-steps { counter-reset: step; padding-left: 0; list-style: none; }
  .apply-steps > li {
    position: relative;
    padding: 0 0 1.25rem 3.25rem;
    line-height: 1.65;
  }
  .apply-steps > li::before {
    counter-increment: step;
    content: counter(step);
    position: absolute;
    left: 0;
    top: 0;
    width: 2.25rem;
    height: 2.25rem;
    border-radius: 50%;
    background: var(--global-theme-color);
    color: #fff;
    font-weight: 700;
    display: flex;
    align-items: center;
    justify-content: center;
  }
  .apply-steps > li:not(:last-child)::after {
    content: "";
    position: absolute;
    left: 1.1rem;
    top: 2.25rem;
    bottom: 0;
    width: 2px;
    background: var(--global-divider-color);
  }
  .email-img {
    height: 1.15em;
    width: auto;
    max-width: 100%;
    vertical-align: -0.2em;
    margin-top: 0.3rem;
  }
  html[data-theme="dark"] .email-img { filter: brightness(1.25); }
  .join-note {
    font-size: 0.9rem;
    color: var(--global-text-color-light);
    border-left: 3px solid var(--global-divider-color);
    padding: 0.25rem 0 0.25rem 1rem;
    margin-top: 1.25rem;
  }
  .join-follow {
    display: flex;
    flex-wrap: wrap;
    gap: 1.25rem;
    align-items: center;
  }
  .join-follow a {
    display: inline-flex;
    align-items: center;
    gap: 0.5rem;
    color: var(--global-text-color-light);
    transition: color 0.2s ease;
    font-size: 0.95rem;
  }
  .join-follow a:hover { color: var(--global-theme-color); }
  .join-follow i { font-size: 1.15rem; }
---

<p class="join-lead">
We are always looking for curious, ambitious, and kind-hearted people to join the Blue Whale Lab. If you are excited about doing principled, impactful research at the intersection of AI and science, we would love to hear from you. Our work is generously supported by the NRF Fellowship, the NRF AI4S Catalytic Grant, the NUS AI Institute (NAII) Seed Grant, and the Singapore Ministry of Education, offering a well-resourced and collaborative environment to pursue big questions.
</p>

<div class="join-section">
<h2 class="join-section-title">Who We're Looking For</h2>

<div class="join-grid">
  <div class="join-card">
    <div class="card-icon"><i class="fa-solid fa-graduation-cap"></i></div>
    <h3>PhD Students</h3>
    <p>Fully funded positions for the 2027, 2028, 2029 Spring/Fall intakes, hosted in the NUS Department of Computer Science. We seek strong fundamentals in mathematics and machine learning, and a genuine passion for research.</p>
  </div>
  <div class="join-card">
    <div class="card-icon"><i class="fa-solid fa-flask"></i></div>
    <h3>Postdocs &amp; Research Fellows</h3>
    <p>For researchers with a strong first-author publication record at top venues. A typical appointment lasts 2&ndash;3 years, giving you the space to lead ambitious, high-impact projects.</p>
  </div>
  <div class="join-card">
    <div class="card-icon"><i class="fa-solid fa-plane-departure"></i></div>
    <h3>Visiting Students</h3>
    <p>Visiting PhD students (e.g., CSC-funded) are welcome, ideally with at least one first-author paper at a top conference.</p>
  </div>
  <div class="join-card">
    <div class="card-icon"><i class="fa-solid fa-lightbulb"></i></div>
    <h3>Master's &amp; Interns</h3>
    <p>A limited number of openings for NUS Master's (CS dissertation) students and research interns. Come build something impactful &mdash; and fun &mdash; with us.</p>
  </div>
</div>
</div>

<div class="join-section">
<h2 class="join-section-title">What We Value</h2>

<ul class="join-values">
  <li><strong>Integrity and a positive attitude toward life.</strong></li>
  <li><strong>Aim high and stay self-motivated</strong> &mdash; be passionate about making something impactful and fun.</li>
  <li><strong>Solid fundamentals</strong> in mathematics, machine learning, and programming.</li>
  <li><strong>Curiosity and collaboration</strong> &mdash; a desire to explore the stars and oceans of AI together.</li>
</ul>
</div>

<div class="join-section">
<h2 class="join-section-title">NUS Computer Science PhD Admission</h2>

<p>PhD students in the lab are admitted through the NUS Department of Computer Science. A few practical notes to help you plan your application:</p>

<ul class="join-values">
  <li>Apply online via the <a href="https://gradapp.nus.edu.sg/portal/app_manage">NUS Graduate Admission System</a>. See the official <a href="https://www.comp.nus.edu.sg/programmes/pg/phdcs/admissions/">CS PhD admissions page</a> for full requirements.</li>
  <li>Typical school requirements include a GPA above 3.5/4.0 and English scores (TOEFL or IELTS or GRE).</li>
  <!-- <li>If you are already in Singapore, or are open to a service obligation (e.g., a postdoc in our lab or a full-time role at a local company after graduation), the admission bar may be slightly more flexible.</li> -->
  <li><strong>Master's (CS dissertation):</strong> a limited number of openings. Please prepare a 2-page research proposal; you are welcome to brainstorm it together with our current PhD students and postdocs.</li>
</ul>
</div>

<div class="join-section">
<h2 class="join-section-title">How to Apply</h2>

<ol class="apply-steps">
  <li><strong>Fill out the Google Form first.</strong> To help us learn about your aspirations and background, please complete <a href="https://forms.gle/8SFfWkBXZwmizHM7A">this Google Form</a> <em>before</em> emailing. This lets us give your application the attention it deserves.</li>
  <li><strong>Email us your materials.</strong> Send your CV, transcripts, and a concise (1&ndash;2 page) research statement to the address below, along with anything else that showcases your excellence.
  <br>
  <img class="email-img" src="{{ '/assets/img/email.png' | relative_url }}" alt="Blue Whale Lab contact email (shown as an image to deter spam crawlers)"></li>
  <li><strong>Submit the official application (PhD).</strong> If there is a good match, apply online through the NUS Graduate Admission System so we can formally move things forward.</li>
</ol>

<p class="join-note">We read every message but, given the large volume of inquiries, may only be able to respond when there is a good match. Thank you for your understanding &mdash; we truly appreciate your interest.</p>
</div>