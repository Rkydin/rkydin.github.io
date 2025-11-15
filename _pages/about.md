---
permalink: /
title: "About Me"
author_profile: true
redirect_from: 
  - /about/
  - /about.html
---

<style>
.intro-text {
  margin-bottom: 40px;
  font-size: 1.1em;
  line-height: 1.6;
}

.portfolio-masonry {
  column-count: 2;
  column-gap: 25px;
  margin: 40px 0;
  padding: 0;
}

.portfolio-item {
  display: inline-block;
  width: 100%;
  margin-bottom: 20px;
  break-inside: avoid;
  border-radius: 20px;
  overflow: hidden;
  cursor: pointer;
  background: rgba(255, 255, 255, 0.05);
  backdrop-filter: blur(10px);
  -webkit-backdrop-filter: blur(10px);
  border: 1px solid rgba(255, 255, 255, 0.1);
  box-shadow: 0 8px 32px rgba(0, 0, 0, 0.2);
  transition: all 0.3s ease;
  text-decoration: none;
  position: relative;
}

.portfolio-item:hover {
  transform: translateY(-5px);
  border: 1px solid rgba(255, 255, 255, 0.2);
  box-shadow: 0 12px 40px rgba(0, 0, 0, 0.3);
  text-decoration: none;
}

.portfolio-image {
  width: 100%;
  height: auto;
  display: block;
  background: transparent;
  transition: all 0.5s ease;
}

.portfolio-item:hover .portfolio-image {
  transform: scale(1.05);
  filter: blur(3px);
}

.portfolio-overlay {
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  background: rgba(0, 0, 0, 0.7);
  backdrop-filter: blur(10px);
  -webkit-backdrop-filter: blur(10px);
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  padding: 20px;
  opacity: 0;
  transition: opacity 0.3s ease;
}

.portfolio-item:hover .portfolio-overlay {
  opacity: 1;
}

.portfolio-title {
  color: #fff;
  font-size: 1.3em;
  font-weight: 600;
  margin: 0 0 10px 0;
  text-shadow: 0 2px 8px rgba(0, 0, 0, 0.5);
  line-height: 1.3;
  text-align: center;
}

.portfolio-excerpt {
  color: #fff;
  font-size: 0.9em;
  margin: 0;
  opacity: 0.95;
  line-height: 1.4;
  text-align: center;
}

.portfolio-date {
  color: #fff;
  font-size: 0.85em;
  margin-top: 8px;
  opacity: 0.8;
  font-style: italic;
  display: block;
  text-align: center;
}

html.dark .portfolio-item,
body.dark .portfolio-item,
.greedy-nav--dark .portfolio-item {
  background: rgba(255, 255, 255, 0.03);
  border: 1px solid rgba(255, 255, 255, 0.08);
}

html.dark .portfolio-item:hover,
body.dark .portfolio-item:hover,
.greedy-nav--dark .portfolio-item:hover {
  border: 1px solid rgba(255, 255, 255, 0.15);
}

@media (max-width: 1200px) {
  .portfolio-masonry {
    column-count: 1;
  }
}

@media (max-width: 768px) {
  .portfolio-masonry {
    column-count: 1;
  }
  
  .portfolio-item {
    border-radius: 15px;
  }
}
</style>

<div class="intro-text">
  <p>I'm a recent Rutgers BME graduate. I've been designing with SolidWorks for about three years, have experience with several programming languages, and build and develop hardware using 3D-printed parts. I'm looking to fill this page with future projects in robotics and assistive technology.</p>
</div>

<h2>Projects</h2>

<div class="portfolio-masonry">
  {% for post in site.portfolio %}
    <a href="{{ post.url | relative_url }}" clas
