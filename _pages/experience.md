---
title: "Experience"
permalink: /experience/
author_profile: true
---

<style>
.exp-eyebrow {
  display: flex;
  align-items: center;
  gap: 10px;
  font-family: "IBM Plex Mono", monospace;
  font-size: 0.72rem;
  letter-spacing: 0.12em;
  text-transform: uppercase;
  color: var(--global-text-color-light);
  margin-bottom: 18px;
}

.exp-eyebrow .exp-dot {
  width: 7px;
  height: 7px;
  background: var(--global-accent-color);
  flex-shrink: 0;
}

.exp-intro {
  max-width: 62ch;
  font-size: 1.08em;
  line-height: 1.6;
  margin-bottom: 44px;
}

.exp-section-head {
  display: flex;
  align-items: baseline;
  justify-content: space-between;
  gap: 20px;
  margin: 0 0 28px;
  padding-bottom: 14px;
  border-bottom: 1px solid var(--global-border-color);
}

.exp-section-head h2 {
  margin: 0;
  font-size: 1.5em;
  text-transform: uppercase;
}

.exp-section-head .exp-count {
  font-family: "IBM Plex Mono", monospace;
  font-size: 0.72rem;
  letter-spacing: 0.1em;
  text-transform: uppercase;
  color: var(--global-text-color-light);
  white-space: nowrap;
}

.exp-tree + .exp-section-head {
  margin-top: 56px;
}

.exp-tree {
  position: relative;
  margin: 0 0 40px;
  padding-left: 0;
}

.exp-tree::before {
  content: "";
  position: absolute;
  top: 6px;
  bottom: 6px;
  left: 8px;
  width: 2px;
  background: var(--global-line-color);
}

.exp-node {
  position: relative;
  padding-left: 44px;
  margin-bottom: 40px;
}

.exp-node:last-child {
  margin-bottom: 0;
}

.exp-node::before {
  content: "";
  position: absolute;
  left: 3px;
  top: 6px;
  width: 12px;
  height: 12px;
  border-radius: 50%;
  background: var(--global-bg-color);
  border: 2px solid var(--global-accent-color);
  z-index: 1;
}

.exp-node[data-cat="education"]::before {
  border-color: var(--global-line-color);
}

.exp-node::after {
  content: "";
  position: absolute;
  left: 9px;
  top: 11px;
  width: 30px;
  height: 2px;
  background: var(--global-line-color);
}

.exp-node-head {
  display: flex;
  align-items: center;
  justify-content: space-between;
  flex-wrap: wrap;
  gap: 8px;
  margin-bottom: 6px;
}

.exp-tag {
  font-family: "IBM Plex Mono", monospace;
  font-size: 0.66rem;
  letter-spacing: 0.1em;
  text-transform: uppercase;
  padding: 3px 8px;
  border: 1px solid var(--global-accent-color);
  color: var(--global-accent-color);
}

.exp-node[data-cat="education"] .exp-tag {
  border-color: var(--global-line-color);
  color: var(--global-line-color);
}

.exp-dates {
  font-family: "IBM Plex Mono", monospace;
  font-size: 0.78rem;
  color: var(--global-text-color-light);
}

.exp-node h3 {
  margin: 0 0 4px;
  font-size: 1.2em;
  text-transform: uppercase;
}

.exp-org {
  font-family: "IBM Plex Mono", monospace;
  font-size: 0.86rem;
  color: var(--global-text-color-light);
  margin: 0 0 10px;
}

.exp-node ul {
  margin: 0;
  padding-left: 18px;
}

.exp-node li {
  margin-bottom: 4px;
  line-height: 1.5;
}

.exp-node li:last-child {
  margin-bottom: 0;
}

.exp-more {
  font-family: "IBM Plex Mono", monospace;
  font-size: 0.82rem;
  color: var(--global-text-color-light);
  border-top: 1px solid var(--global-border-color);
  padding-top: 20px;
}

.exp-more a {
  color: var(--global-accent-color);
}
</style>

<div class="exp-eyebrow">
  <span class="exp-dot"></span>
  <span>Career &amp; Education Timeline</span>
</div>

<div class="exp-intro">
  <p>Work experience and education, each newest first.</p>
</div>

<div class="exp-section-head">
  <h2>Experience</h2>
  <span class="exp-count">Latest → Earliest</span>
</div>

<div class="exp-tree">

  <div class="exp-node" data-cat="experience">
    <div class="exp-node-head">
      <span class="exp-tag">Experience</span>
      <span class="exp-dates">Apr 2026 – Jul 2026</span>
    </div>
    <h3>Mechanical Design Intern</h3>
    <p class="exp-org">Volta Space Technologies — Broomfield, CO</p>
    <ul>
      <li>Developed SolidWorks CAD models and mechanical hardware for internal and electro-optical support applications.</li>
      <li>Designed optical-mount fixtures and supported hardware development for future thermal vacuum (TVAC) testing.</li>
      <li>Participated in tolerance analysis, design iteration, and system-integration discussions.</li>
    </ul>
  </div>

  <div class="exp-node" data-cat="experience">
    <div class="exp-node-head">
      <span class="exp-tag">Experience</span>
      <span class="exp-dates">Nov 2025 – Feb 2026</span>
    </div>
    <h3>Mechanical Engineer (Contract, 3 months)</h3>
    <p class="exp-org">Robomekanics — Teterboro, NJ</p>
    <ul>
      <li>Converted legacy metric CAD assemblies into inch-based production models and ASME Y14.5-compliant drawings for pallet-handling robotics within an ISO 9001 quality program.</li>
      <li>Performed tolerance stack-ups on sheet-metal and welded assemblies to resolve fit-up, interference, and failure issues.</li>
      <li>Designed welding and assembly fixtures to control distortion, maintain alignment, and improve fabrication repeatability.</li>
    </ul>
  </div>

  <div class="exp-node" data-cat="experience">
    <div class="exp-node-head">
      <span class="exp-tag">Experience</span>
      <span class="exp-dates">Summer 2021</span>
    </div>
    <h3>Research Assistant</h3>
    <p class="exp-org">Lamont-Doherty Earth Observatory — Palisades, NY</p>
    <ul>
      <li>Supported research on microplastic contamination in consumer detergents through sample preparation, filtration, and laboratory testing.</li>
      <li>Performed UV-Vis spectrophotometry, followed cleanroom procedures, analyzed data, and documented preliminary findings.</li>
    </ul>
  </div>

</div>

<div class="exp-section-head">
  <h2>Education</h2>
  <span class="exp-count">Latest → Earliest</span>
</div>

<div class="exp-tree">

  <div class="exp-node" data-cat="education">
    <div class="exp-node-head">
      <span class="exp-tag">Education</span>
      <span class="exp-dates">Sep 2026 – May 2028</span>
    </div>
    <h3>M.S. Mechanical Engineering — Materials Concentration</h3>
    <p class="exp-org">Northeastern University — Boston, MA</p>
    <ul>
      <li>Incoming Fall 2026.</li>
    </ul>
  </div>

  <div class="exp-node" data-cat="education">
    <div class="exp-node-head">
      <span class="exp-tag">Education</span>
      <span class="exp-dates">Sep 2021 – May 2025</span>
    </div>
    <h3>B.S. Biomedical Engineering</h3>
    <p class="exp-org">Rutgers University, School of Engineering — New Brunswick, NJ</p>
    <ul>
      <li>Coursework in biomaterials, biomechanics, and biomedical devices, focused on the mechanical, biological, and chemical behavior of engineered systems.</li>
      <li>Performed mechanical testing, failure analysis, and data analysis using Instron machines and optical microscopy.</li>
    </ul>
  </div>

</div>

<p class="exp-more">See the full project portfolio → <a href="{{ '/' | relative_url }}">home</a>, or the <a href="{{ '/resume/' | relative_url }}">full resume</a>.</p>
