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

.bp-grid {
  display: grid;
  grid-template-columns: repeat(auto-fill, minmax(260px, 1fr));
  gap: 1px;
  background: var(--global-border-color);
  border: 1px solid var(--global-border-color);
  margin-bottom: 40px;
}

.bp-grid a.bp-card {
  background: var(--global-card-bg-color);
  display: flex;
  flex-direction: column;
  text-decoration: none;
  color: var(--global-text-color);
  transition: background 0.18s ease;
}

.bp-grid a.bp-card:hover,
.bp-grid a.bp-card:hover * {
  text-decoration: none;
}

.bp-grid a.bp-card:hover {
  background: var(--global-bg-color);
}

.bp-card-strip {
  display: flex;
  align-items: center;
  justify-content: space-between;
  padding: 10px 16px;
}

.bp-card-tag {
  font-family: "IBM Plex Mono", monospace;
  font-size: 0.64rem;
  letter-spacing: 0.1em;
  text-transform: uppercase;
  padding: 3px 7px;
  border: 1px solid var(--global-line-color);
  color: var(--global-line-color);
}

.bp-card-sheet {
  font-family: "IBM Plex Mono", monospace;
  font-size: 0.68rem;
  color: var(--global-text-color-light);
}

.bp-card-image {
  height: 168px;
  border-top: 1px solid var(--global-border-color);
  border-bottom: 1px solid var(--global-border-color);
  overflow: hidden;
}

.bp-card-image img {
  width: 100%;
  height: 100%;
  object-fit: cover;
  display: block;
  transition: transform 0.4s ease;
}

.bp-card:hover .bp-card-image img {
  transform: scale(1.04);
}

.bp-card-body {
  padding: 16px;
  flex: 1;
  display: flex;
  flex-direction: column;
  gap: 8px;
}

.bp-card-body h3 {
  font-size: 1.05em;
  margin: 0;
  text-transform: uppercase;
}

.bp-card-body p {
  margin: 0;
  color: var(--global-text-color-light);
  font-size: 0.92em;
  line-height: 1.5;
  flex: 1;
}

.bp-card-foot {
  display: flex;
  align-items: center;
  justify-content: space-between;
  padding-top: 8px;
  border-top: 1px solid var(--global-border-color);
  font-family: "IBM Plex Mono", monospace;
  font-size: 0.72rem;
}

.bp-card-foot .bp-date { color: var(--global-text-color-light); }

.bp-card-open {
  color: var(--global-accent-color);
  letter-spacing: 0.05em;
  text-transform: uppercase;
  display: flex;
  align-items: center;
  gap: 4px;
}

.bp-card-open svg { width: 10px; height: 10px; transition: transform 0.15s ease; }
.bp-card:hover .bp-card-open svg { transform: translateX(3px); }

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
</style>

<div class="bp-eyebrow">
  <span class="bp-dot"></span>
  <span>Engineering Portfolio — Rev. 2026</span>
</div>

<div class="bp-intro">
  <p>I'm a recent Rutgers BME graduate committed to Northeastern University's MS in Mechanical Engineering starting Fall 2026. I've been designing in SolidWorks for about four years, work across a few programming languages, and build and develop hardware using 3D-printed parts. I'm passionate about robotics, assistive technology, and space exploration — looking to fill this page with projects that push the boundaries of what's possible.</p>
  <div class="bp-tags-river">
    <div class="bp-tags-track">
      <span class="bp-tag">SolidWorks</span>
      <span class="bp-tag">Siemens NX</span>
      <span class="bp-tag">GD&amp;T</span>
      <span class="bp-tag">Tolerance Analysis</span>
      <span class="bp-tag">DFM</span>
      <span class="bp-tag">DFA</span>
      <span class="bp-tag">FEA</span>
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
      <span class="bp-tag">SolidWorks</span>
      <span class="bp-tag">Siemens NX</span>
      <span class="bp-tag">GD&amp;T</span>
      <span class="bp-tag">Tolerance Analysis</span>
      <span class="bp-tag">DFM</span>
      <span class="bp-tag">DFA</span>
      <span class="bp-tag">FEA</span>
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
    <span class="bp-value">New Jersey, US</span>
  </div>
  <div class="bp-titleblock-cell">
    <span class="bp-label">Next</span>
    <span class="bp-value">MS ME, Northeastern — Fall 2026</span>
  </div>
  <div class="bp-titleblock-cell">
    <span class="bp-label">Focus</span>
    <span class="bp-value">Robotics / Assistive Tech / Space</span>
  </div>
  <div class="bp-titleblock-cell">
    <span class="bp-label">Primary Tool</span>
    <span class="bp-value">SolidWorks — 4 yrs</span>
  </div>
</div>

<div class="bp-section-head">
  <h2>Selected Work</h2>
  <span class="bp-label">{{ site.portfolio.size }} Sheets</span>
</div>

<div class="bp-grid">
{% for post in site.portfolio %}
  <a href="{{ post.url | relative_url }}" class="bp-card">
    <div class="bp-card-strip">
      <span class="bp-card-tag">{{ post.category | default: "Project" }}</span>
      <span class="bp-card-sheet">SHT {{ forloop.index | prepend: "00" | slice: -2, 2 }}/{{ site.portfolio.size | prepend: "00" | slice: -2, 2 }}</span>
    </div>
    <div class="bp-card-image">
      {% if post.header.teaser %}
        <img src="{{ post.header.teaser | relative_url }}" alt="{{ post.title }}">
      {% elsif post.image %}
        <img src="{{ post.image | relative_url }}" alt="{{ post.title }}">
      {% endif %}
    </div>
    <div class="bp-card-body">
      <h3>{{ post.title }}</h3>
      <p>{{ post.excerpt | strip_html | truncatewords: 22 }}</p>
      <div class="bp-card-foot">
        <span class="bp-date">{% if post.date %}{{ post.date | date: "%b %Y" }}{% else %}Ongoing{% endif %}</span>
        <span class="bp-card-open">Open <svg viewBox="0 0 12 12"><path d="M2 10 L10 2 M4 2 H10 V8" fill="none" stroke="currentColor" stroke-width="1.4"/></svg></span>
      </div>
    </div>
  </a>
{% endfor %}
</div>
