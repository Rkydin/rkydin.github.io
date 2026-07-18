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

.exp-node--media {
  padding-right: 92px;
}

.exp-node-media {
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

.exp-node-media img {
  max-width: 100%;
  max-height: 100%;
  object-fit: contain;
  display: block;
}

.exp-node-media--photo {
  padding: 0;
}

.exp-node-media--photo img {
  width: 100%;
  height: 100%;
  object-fit: cover;
}

@media (max-width: 540px) {
  .exp-node--media {
    padding-right: 44px;
  }

  .exp-node-media {
    position: static;
    width: 56px;
    height: 56px;
    margin-bottom: 12px;
  }
}

.exp-photo-river {
  position: relative;
  overflow: hidden;
  margin-top: 16px;
  margin-right: -92px;
  -webkit-mask-image: linear-gradient(to right, transparent, black 32px, black calc(100% - 32px), transparent);
  mask-image: linear-gradient(to right, transparent, black 32px, black calc(100% - 32px), transparent);
}

.exp-photo-track {
  display: flex;
  gap: 10px;
  width: max-content;
  animation: exp-river-flow 26s linear infinite;
}

.exp-photo-track:hover {
  animation-play-state: paused;
}

@keyframes exp-river-flow {
  from { transform: translateX(0); }
  to { transform: translateX(-50%); }
}

@media (prefers-reduced-motion: reduce) {
  .exp-photo-track {
    animation: none;
  }
}

.exp-photo-track img {
  height: 140px;
  width: auto;
  object-fit: cover;
  border: 1px solid var(--global-border-color);
  flex-shrink: 0;
}

@media (max-width: 540px) {
  .exp-photo-river {
    margin-right: -44px;
  }

  .exp-photo-track img {
    height: 100px;
  }
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

<div class="exp-section-head">
  <h2>Experience</h2>
  <span class="exp-count">Latest → Earliest</span>
</div>

<div class="exp-tree">

  <div class="exp-node exp-node--media" data-cat="experience">
    <div class="exp-node-media">
      <img src="{{ '/images/logos/volta.png' | relative_url }}" alt="Volta Space Technologies logo">
    </div>
    <div class="exp-node-head">
      <span class="exp-tag">Experience</span>
      <span class="exp-dates">Apr 2026 – Jul 2026</span>
    </div>
    <h3>Mechanical Design Intern</h3>
    <p class="exp-org">Volta Space Technologies — Broomfield, CO</p>
    <ul>
      <li>Designed a CAD enclosure housing a laser assembly and its associated optical fixtures for shipment and testing, supporting delivery to the European Space Agency (ESA).</li>
      <li>Gained hands-on exposure to electromechanical assembly, including soldering and cable harnessing, through hardware build support.</li>
      <li>Developed SolidWorks CAD models and mechanical hardware for internal and electro-optical support applications.</li>
      <li>Designed optical-mount fixtures and supported hardware development for future thermal vacuum (TVAC) testing.</li>
      <li>Maintained drawing and BOM revision control through ECOs and redlines, ensuring documentation accuracy across engineering and technical reporting.</li>
    </ul>
    <div class="exp-photo-river">
      <div class="exp-photo-track">
        <img src="{{ '/images/volta/optics-fixture.jpg' | relative_url }}" alt="3D-printed optical fixture on a test bench">
        <img src="{{ '/images/volta/gantry-control-setup.jpg' | relative_url }}" alt="Laser gantry control software setup">
        <img src="{{ '/images/volta/beaming-demo.jpg' | relative_url }}" alt="Wireless power beaming demo across the test hangar">
        <img src="{{ '/images/volta/receiver-panel.jpg' | relative_url }}" alt="Laser striking the photovoltaic receiver panel">
        <img src="{{ '/images/volta/optics-fixture.jpg' | relative_url }}" alt="3D-printed optical fixture on a test bench">
        <img src="{{ '/images/volta/gantry-control-setup.jpg' | relative_url }}" alt="Laser gantry control software setup">
        <img src="{{ '/images/volta/beaming-demo.jpg' | relative_url }}" alt="Wireless power beaming demo across the test hangar">
        <img src="{{ '/images/volta/receiver-panel.jpg' | relative_url }}" alt="Laser striking the photovoltaic receiver panel">
      </div>
    </div>
  </div>

  <div class="exp-node exp-node--media" data-cat="experience">
    <div class="exp-node-media exp-node-media--photo">
      <img src="{{ '/images/moleiq/moleiq.png' | relative_url }}" alt="MoleIQ pallet-handling robot">
    </div>
    <div class="exp-node-head">
      <span class="exp-tag">Experience</span>
      <span class="exp-dates">Nov 2025 – Feb 2026</span>
    </div>
    <h3>Mechanical Engineer (Contract, 3 months)</h3>
    <p class="exp-org">Robomekanics — Teterboro, NJ</p>
    <ul>
      <li>Reduced part count by 15% across pallet-handling robotics assemblies by redesigning and merging components during the metric-to-inch CAD conversion, cutting fabrication and assembly labor.</li>
      <li>Converted legacy metric CAD assemblies into inch-based production models and ASME Y14.5-compliant drawings within an ISO 9001 quality program.</li>
      <li>Resolved fit-up, interference, and failure issues on sheet-metal and welded assemblies by performing tolerance stack-ups and revising geometry with machinists and fabricators.</li>
      <li>Designed welding/assembly fixtures and updated build procedures with redlined drawings, improving fabrication repeatability and reducing prototype rework.</li>
    </ul>
  </div>

  <div class="exp-node" data-cat="experience">
    <div class="exp-node-head">
      <span class="exp-tag">Experience</span>
      <span class="exp-dates">Apr 2021 – Aug 2021</span>
    </div>
    <h3>Research Assistant</h3>
    <p class="exp-org">Lamont-Doherty Earth Observatory — Palisades, NY</p>
    <ul>
      <li>Supported research on microplastic contamination in consumer detergents through sample preparation, filtration, UV-Vis spectrophotometry, and cleanroom laboratory testing.</li>
    </ul>
  </div>

</div>

<div class="exp-section-head">
  <h2>Education</h2>
  <span class="exp-count">Latest → Earliest</span>
</div>

<div class="exp-tree">

  <div class="exp-node exp-node--media" data-cat="education">
    <div class="exp-node-media">
      <img src="{{ '/images/logos/northeastern.svg' | relative_url }}" alt="Northeastern University logo">
    </div>
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

  <div class="exp-node exp-node--media" data-cat="education">
    <div class="exp-node-media">
      <img src="{{ '/images/logos/rutgers.svg' | relative_url }}" alt="Rutgers University logo">
    </div>
    <div class="exp-node-head">
      <span class="exp-tag">Education</span>
      <span class="exp-dates">Sep 2021 – May 2025</span>
    </div>
    <h3>B.S. Biomedical Engineering</h3>
    <p class="exp-org">Rutgers University, School of Engineering — New Brunswick, NJ</p>
    <ul>
      <li>Coursework in biomaterials, biomechanics, and biomedical devices, focused on the mechanical, biological, and chemical behavior of engineered systems.</li>
      <li>Performed mechanical testing, failure analysis, and data analysis using Instron machines and optical microscopy.</li>
      <li>Conducted electronics lab coursework using oscilloscopes and digital multimeters, and ran FEA/simulation coursework in SolidWorks, SolidWorks Simulation, and Abaqus.</li>
    </ul>
  </div>

</div>

<p class="exp-more">See the full project portfolio → <a href="{{ '/' | relative_url }}">home</a>, or the <a href="{{ '/resume/' | relative_url }}">full resume</a>.</p>
