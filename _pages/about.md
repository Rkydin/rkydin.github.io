---
permalink: /
title: "About Me"
author_profile: true
redirect_from: 
  - /about/
  - /about.html
---

<style>
.bp-eyebrow {
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

.bp-eyebrow .bp-dot {
  width: 7px;
  height: 7px;
  background: var(--global-accent-color);
  flex-shrink: 0;
}

.bp-intro {
  max-width: 62ch;
  font-size: 1.15em;
  line-height: 1.6;
}

.bp-titleblock {
  margin: 36px 0 48px;
  border: 1px solid var(--global-border-color);
  display: grid;
  grid-template-columns: repeat(4, 1fr);
}

.bp-titleblock-cell {
  padding: 14px 18px;
  border-right: 1px solid var(--global-border-color);
}
.bp-titleblock-cell:last-child { border-right: none; }

.bp-titleblock-cell .bp-label {
  display: block;
  margin-bottom: 6px;
  font-family: "IBM Plex Mono", monospace;
  font-size: 0.68rem;
  letter-spacing: 0.1em;
  text-transform: uppercase;
  color: var(--global-text-color-light);
}

.bp-titleblock-cell .bp-value {
  font-family: "IBM Plex Mono", monospace;
  font-size: 0.85rem;
  font-weight: 500;
}

@media (max-width: 860px) {
  .bp-titleblock { grid-template-columns: repeat(2, 1fr); }
  .bp-titleblock-cell:nth-child(2) { border-right: none; }
}
@media (max-width: 480px) {
  .bp-titleblock { grid-template-columns: 1fr; }
  .bp-titleblock-cell { border-right: none; border-bottom: 1px solid var(--global-border-color); }
}

.bp-section-head {
  display: flex;
  align-items: baseline;
  justify-content: space-between;
  gap: 20px;
  margin: 0 0 28px;
  padding-bottom: 14px;
  border-bottom: 1px solid var(--global-border-color);
}

.bp-section-head h2 {
  margin: 0;
  font-size: 1.6em;
  text-transform: uppercase;
}

.bp-section-head .bp-label {
  font-family: "IBM Plex Mono", monospace;
  font-size: 0.72rem;
  letter-spacing: 0.1em;
  text-transform: uppercase;
  color: var(--global-text-color-light);
  white-space: nowrap;
}

.bp-tags-river {
  position: relative;
  overflow: hidden;
  margin-top: 24px;
  -webkit-mask-image: linear-gradient(to right, transparent, black 48px, black calc(100% - 48px), transparent);
  mask-image: linear-gradient(to right, transparent, black 48px, black calc(100% - 48px), transparent);
}

.bp-tags-track {
  display: flex;
  gap: 8px;
  width: max-content;
  animation: bp-river-flow 32s linear infinite;
}

.bp-tags-track:hover {
  animation-play-state: paused;
}

@keyframes bp-river-flow {
  from { transform: translateX(0); }
  to { transform: translateX(-50%); }
}

@media (prefers-reduced-motion: reduce) {
  .bp-tags-track {
    animation: none;
  }
}

.bp-tag {
  font-family: "IBM Plex Mono", monospace;
  font-size: 0.72rem;
  letter-spacing: 0.05em;
  text-transform: uppercase;
  padding: 5px 9px;
  border: 1px solid var(--global-border-color);
  color: var(--global-text-color-light);
  white-space: nowrap;
  flex-shrink: 0;
}

.bp-tree {
  position: relative;
  margin: 0 0 40px;
  padding-left: 0;
}

.bp-tree::before {
  content: "";
  position: absolute;
  top: 6px;
  bottom: 6px;
  left: 8px;
  width: 2px;
  background: var(--global-line-color);
}

.bp-node {
  position: relative;
  padding-left: 44px;
  margin-bottom: 40px;
}

.bp-node:last-child {
  margin-bottom: 0;
}

.bp-node--media {
  padding-right: 92px;
}

.bp-node-media {
  position: absolute;
  top: 0;
  right: 0;
  width: 72px;
  height: 72px;
  display: flex;
  align-items: center;
  justify-content: center;
  border: 1px solid var(--global-border-color);
  background: #fff;
  padding: 10px;
}

.bp-node-media img {
  max-width: 100%;
  max-height: 100%;
  object-fit: contain;
  display: block;
}

.bp-node-media--photo {
  padding: 0;
}

.bp-node-media--photo img {
  width: 100%;
  height: 100%;
  object-fit: cover;
}

@media (max-width: 540px) {
  .bp-node--media {
    padding-right: 44px;
  }

  .bp-node-media {
    position: static;
    width: 56px;
    height: 56px;
    margin-bottom: 12px;
  }
}

.bp-photo-river {
  position: relative;
  overflow: hidden;
  margin-top: 16px;
  margin-right: -92px;
  -webkit-mask-image: linear-gradient(to right, transparent, black 32px, black calc(100% - 32px), transparent);
  mask-image: linear-gradient(to right, transparent, black 32px, black calc(100% - 32px), transparent);
}

.bp-photo-track {
  display: flex;
  gap: 10px;
  width: max-content;
  animation: bp-river-flow-photo 26s linear infinite;
}

.bp-photo-track:hover {
  animation-play-state: paused;
}

@keyframes bp-river-flow-photo {
  from { transform: translateX(0); }
  to { transform: translateX(-50%); }
}

@media (prefers-reduced-motion: reduce) {
  .bp-photo-track {
    animation: none;
  }
}

.bp-photo-track img {
  height: 140px;
  width: auto;
  object-fit: cover;
  border: 1px solid var(--global-border-color);
  flex-shrink: 0;
}

@media (max-width: 540px) {
  .bp-photo-river {
    margin-right: -44px;
  }

  .bp-photo-track img {
    height: 100px;
  }
}

.bp-node::before {
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

.bp-node[data-cat="education"]::before {
  border-color: var(--global-line-color);
}

.bp-node::after {
  content: "";
  position: absolute;
  left: 9px;
  top: 11px;
  width: 30px;
  height: 2px;
  background: var(--global-line-color);
}

.bp-node-head {
  display: flex;
  align-items: center;
  justify-content: space-between;
  flex-wrap: wrap;
  gap: 8px;
  margin-bottom: 6px;
}

.bp-node-tag {
  font-family: "IBM Plex Mono", monospace;
  font-size: 0.66rem;
  letter-spacing: 0.1em;
  text-transform: uppercase;
  padding: 3px 8px;
  border: 1px solid var(--global-accent-color);
  color: var(--global-accent-color);
}

.bp-node[data-cat="education"] .bp-node-tag {
  border-color: var(--global-line-color);
  color: var(--global-line-color);
}

.bp-node-dates {
  font-family: "IBM Plex Mono", monospace;
  font-size: 0.78rem;
  color: var(--global-text-color-light);
}

.bp-node h3 {
  margin: 0 0 4px;
  font-size: 1.2em;
  text-transform: uppercase;
}

.bp-node-org {
  font-family: "IBM Plex Mono", monospace;
  font-size: 0.86rem;
  color: var(--global-text-color-light);
  margin: 0 0 10px;
}

.bp-node ul {
  margin: 0;
  padding-left: 18px;
}

.bp-node li {
  margin-bottom: 4px;
  line-height: 1.5;
}

.bp-node li:last-child {
  margin-bottom: 0;
}

.bp-node li strong {
  color: var(--global-accent-color);
  font-weight: 600;
}

.bp-cta-row {
  display: flex;
  flex-wrap: wrap;
  gap: 12px;
  margin-top: 24px;
  padding-top: 24px;
  border-top: 1px solid var(--global-border-color);
}

.bp-btn {
  display: inline-flex;
  align-items: center;
  gap: 8px;
  padding: 12px 22px;
  font-family: "IBM Plex Mono", monospace;
  font-size: 0.78rem;
  letter-spacing: 0.06em;
  text-transform: uppercase;
  text-decoration: none !important;
  border: 1px solid var(--global-accent-color);
  transition: opacity 0.15s ease;
}

.bp-btn:hover {
  opacity: 0.8;
  text-decoration: none !important;
}

.bp-btn--solid {
  background: var(--global-accent-color);
  color: #fff;
}

.bp-btn--outline {
  background: transparent;
  color: var(--global-accent-color);
}

</style>

<div class="bp-eyebrow">
  <span class="bp-dot"></span>
  <span>Engineering Portfolio — Rev. 2026</span>
</div>

<div class="bp-intro">
  <p>I'm a Rutgers BME graduate working as a mechanical designer, and I'm working to grow beyond design alone into more theoretical and R&amp;D-focused engineering. I'll be starting an MS in Mechanical Engineering with a concentration in Materials at Northeastern this fall. I've been designing in CAD for about four years, work across a few programming languages, and build and develop hardware using 3D-printed parts. My interests span space, robotics, MEMS, and energy systems — looking to fill this page with projects that push the boundaries of what's possible.</p>
  <div class="bp-tags-river">
    <div class="bp-tags-track">
      <span class="bp-tag">GD&amp;T</span>
      <span class="bp-tag">Tolerance Analysis</span>
      <span class="bp-tag">SolidWorks</span>
      <span class="bp-tag">Siemens NX</span>
      <span class="bp-tag">DFM</span>
      <span class="bp-tag">DFA</span>
      <span class="bp-tag">FEA</span>
      <span class="bp-tag">Abaqus</span>
      <span class="bp-tag">Oscilloscopes</span>
      <span class="bp-tag">3D Printing</span>
      <span class="bp-tag">Rapid Prototyping</span>
      <span class="bp-tag">Mechanism Design</span>
      <span class="bp-tag">Fixture Design</span>
      <span class="bp-tag">Mechanical Testing</span>
      <span class="bp-tag">Failure Analysis</span>
      <span class="bp-tag">BOM Management</span>
      <span class="bp-tag">Root Cause Analysis</span>
      <span class="bp-tag">Python</span>
      <span class="bp-tag">MATLAB</span>
      <span class="bp-tag">C++</span>
      <span class="bp-tag">GD&amp;T</span>
      <span class="bp-tag">Tolerance Analysis</span>
      <span class="bp-tag">SolidWorks</span>
      <span class="bp-tag">Siemens NX</span>
      <span class="bp-tag">DFM</span>
      <span class="bp-tag">DFA</span>
      <span class="bp-tag">FEA</span>
      <span class="bp-tag">Abaqus</span>
      <span class="bp-tag">Oscilloscopes</span>
      <span class="bp-tag">3D Printing</span>
      <span class="bp-tag">Rapid Prototyping</span>
      <span class="bp-tag">Mechanism Design</span>
      <span class="bp-tag">Fixture Design</span>
      <span class="bp-tag">Mechanical Testing</span>
      <span class="bp-tag">Failure Analysis</span>
      <span class="bp-tag">BOM Management</span>
      <span class="bp-tag">Root Cause Analysis</span>
      <span class="bp-tag">Python</span>
      <span class="bp-tag">MATLAB</span>
      <span class="bp-tag">C++</span>
    </div>
  </div>
</div>

<div class="bp-titleblock">
  <div class="bp-titleblock-cell">
    <span class="bp-label">Location</span>
    <span class="bp-value">Boston, MA — open to relocation</span>
  </div>
  <div class="bp-titleblock-cell">
    <span class="bp-label">Next</span>
    <span class="bp-value">MS ME (Materials), Northeastern — Fall 2026</span>
  </div>
  <div class="bp-titleblock-cell">
    <span class="bp-label">Focus</span>
    <span class="bp-value">Space / Robotics / MEMS / Energy</span>
  </div>
  <div class="bp-titleblock-cell">
    <span class="bp-label">Primary Tool</span>
    <span class="bp-value">CAD — 4 yrs</span>
  </div>
</div>

<div class="bp-section-head">
  <h2>Experience</h2>
  <span class="bp-label">Latest → Earliest</span>
</div>

<div class="bp-tree">

  <div class="bp-node bp-node--media" data-cat="experience">
    <div class="bp-node-media">
      <img src="{{ '/images/logos/volta.png' | relative_url }}" alt="Volta Space Technologies logo">
    </div>
    <div class="bp-node-head">
      <span class="bp-node-tag">Experience</span>
      <span class="bp-node-dates">Apr 2026 – Jul 2026</span>
    </div>
    <h3>Mechanical Design Intern</h3>
    <p class="bp-node-org">Volta Space Technologies — Broomfield, CO</p>
    <ul>
      <li>Designed and built a laser assembly enclosure from aluminum extrusions and sheet metal in <strong>SolidWorks</strong> for delivery to the <strong>European Space Agency</strong>.</li>
      <li>Assembled electromechanical hardware, including <strong>soldering</strong> and <strong>cable harnessing</strong>.</li>
      <li>Designed and 3D-printed optical-mount fixtures for fibers, lasers, lenses, and mirrors in <strong>SolidWorks</strong> and <strong>Fusion 360</strong>, applying <strong>GD&amp;T</strong> tolerancing for optical alignment ahead of future <strong>TVAC</strong> testing.</li>
      <li>Sourced vendor quotes and coordinated manufacturing of aluminum sheet-metal and machined parts, designed and ordered optical breadboards, and documented procurement using the <strong>Microsoft 365</strong> suite.</li>
    </ul>
    <div class="bp-photo-river">
      <div class="bp-photo-track">
        <img src="{{ '/images/volta/esa-enclosure.jpg' | relative_url }}" alt="ESA laser assembly enclosure, aluminum extrusion and sheet metal">
        <img src="{{ '/images/volta/optics-fixture.jpg' | relative_url }}" alt="3D-printed optical fixture on a test bench">
        <img src="{{ '/images/volta/gantry-control-setup.jpg' | relative_url }}" alt="Laser gantry control software setup">
        <img src="{{ '/images/volta/beaming-demo.jpg' | relative_url }}" alt="Wireless power beaming demo across the test hangar">
        <img src="{{ '/images/volta/receiver-panel.jpg' | relative_url }}" alt="Laser striking the photovoltaic receiver panel">
        <img src="{{ '/images/volta/esa-enclosure.jpg' | relative_url }}" alt="ESA laser assembly enclosure, aluminum extrusion and sheet metal">
        <img src="{{ '/images/volta/optics-fixture.jpg' | relative_url }}" alt="3D-printed optical fixture on a test bench">
        <img src="{{ '/images/volta/gantry-control-setup.jpg' | relative_url }}" alt="Laser gantry control software setup">
        <img src="{{ '/images/volta/beaming-demo.jpg' | relative_url }}" alt="Wireless power beaming demo across the test hangar">
        <img src="{{ '/images/volta/receiver-panel.jpg' | relative_url }}" alt="Laser striking the photovoltaic receiver panel">
      </div>
    </div>
  </div>

  <div class="bp-node bp-node--media" data-cat="experience">
    <div class="bp-node-media bp-node-media--photo">
      <img src="{{ '/images/moleiq/moleiq.png' | relative_url }}" alt="MoleIQ pallet-handling robot">
    </div>
    <div class="bp-node-head">
      <span class="bp-node-tag">Experience</span>
      <span class="bp-node-dates">Nov 2025 – Feb 2026</span>
    </div>
    <h3>Mechanical Engineer (Contract, 3 months)</h3>
    <p class="bp-node-org">Robomekanics — Teterboro, NJ</p>
    <ul>
      <li>Reduced part count by <strong>15%</strong> across pallet-handling robotics assemblies by redesigning and merging components during the metric-to-inch CAD conversion, cutting fabrication and assembly labor.</li>
      <li>Converted legacy metric CAD assemblies into inch-based production models and <strong>ASME Y14.5-2018</strong>-compliant drawings within an <strong>ISO 9001</strong> quality program, documented using the <strong>Microsoft 365</strong> suite.</li>
      <li>Resolved fit-up, interference, and failure issues on sheet-metal and welded assemblies by performing <strong>tolerance stack-ups</strong> and revising geometry with machinists and fabricators.</li>
      <li>Built on-demand prototypes directly from rough concept sketches, translating informal design intent into functional hardware under tight turnaround.</li>
    </ul>
  </div>

  <div class="bp-node" data-cat="experience">
    <div class="bp-node-head">
      <span class="bp-node-tag">Experience</span>
      <span class="bp-node-dates">Apr 2021 – Aug 2021</span>
    </div>
    <h3>Research Assistant</h3>
    <p class="bp-node-org">Lamont-Doherty Earth Observatory — Palisades, NY</p>
    <ul>
      <li>Supported research on microplastic contamination in consumer detergents through sample preparation, filtration, <strong>UV-Vis spectrophotometry</strong>, and cleanroom laboratory testing.</li>
    </ul>
  </div>

</div>

<div class="bp-section-head">
  <h2>Education</h2>
  <span class="bp-label">Latest → Earliest</span>
</div>

<div class="bp-tree">

  <div class="bp-node bp-node--media" data-cat="education">
    <div class="bp-node-media">
      <img src="{{ '/images/logos/northeastern.svg' | relative_url }}" alt="Northeastern University logo">
    </div>
    <div class="bp-node-head">
      <span class="bp-node-tag">Education</span>
      <span class="bp-node-dates">Sep 2026 – May 2028</span>
    </div>
    <h3>M.S. Mechanical Engineering — Materials Concentration</h3>
    <p class="bp-node-org">Northeastern University — Boston, MA</p>
    <ul>
      <li>Incoming Fall 2026.</li>
    </ul>
  </div>

  <div class="bp-node bp-node--media" data-cat="education">
    <div class="bp-node-media">
      <img src="{{ '/images/logos/rutgers.svg' | relative_url }}" alt="Rutgers University logo">
    </div>
    <div class="bp-node-head">
      <span class="bp-node-tag">Education</span>
      <span class="bp-node-dates">Sep 2021 – May 2025</span>
    </div>
    <h3>B.S. Biomedical Engineering</h3>
    <p class="bp-node-org">Rutgers University, School of Engineering — New Brunswick, NJ</p>
    <ul>
      <li>Coursework in <strong>biomaterials</strong>, <strong>biomechanics</strong>, and <strong>biomedical devices</strong>, focused on the mechanical, biological, and chemical behavior of engineered systems.</li>
      <li>Performed mechanical testing, failure analysis, and data analysis using <strong>Instron</strong> machines and optical microscopy.</li>
      <li>Completed electronics labs with <strong>oscilloscopes</strong> and <strong>DMMs</strong>, and FEA/simulation coursework in <strong>SolidWorks</strong> and <strong>Abaqus</strong>.</li>
    </ul>
  </div>

</div>

<div class="bp-cta-row">
  <a href="{{ '/portfolio/' | relative_url }}" class="bp-btn bp-btn--solid">View Full Portfolio →</a>
  <a href="{{ '/resume/' | relative_url }}" class="bp-btn bp-btn--outline">Full Resume →</a>
</div>
