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

.projects-grid {
  display: grid;
  grid-template-columns: repeat(auto-fill, minmax(350px, 1fr));
  gap: 20px;
  margin: 40px 0;
  padding: 0;
}

.project-item {
  position: relative;
  aspect-ratio: 4 / 3;
  border-radius: 20px;
  overflow: hidden;
  cursor: pointer;
  box-shadow: 0 4px 12px rgba(0, 0, 0, 0.1);
  transition: all 0.3s ease;
  text-decoration: none;
}

.project-item:hover {
  transform: translateY(-5px);
  box-shadow: 0 8px 24px rgba(0, 0, 0, 0.2);
  text-decoration: none;
}

.project-image {
  width: 100%;
  height: 100%;
  object-fit: contain;
  background: #f5f5f5;
  transition: all 0.5s ease;
}

.project-item:hover .project-image {
  transform: scale(1.05);
  filter: blur(3px);
}

.project-overlay {
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

.project-item:hover .project-overlay {
  opacity: 1;
}

.project-title {
  color: #fff;
  font-size: 1.4em;
  font-weight: 600;
  margin: 0 0 10px 0;
  text-shadow: 0 2px 8px rgba(0, 0, 0, 0.5);
  line-height: 1.3;
  text-align: center;
}

.project-excerpt {
  color: #fff;
  font-size: 0.9em;
  margin: 0;
  opacity: 0.95;
  line-height: 1.4;
  text-align: center;
}

.project-date {
  color: #fff;
  font-size: 0.85em;
  margin-top: 8px;
  opacity: 0.8;
  font-style: italic;
  display: block;
  text-align: center;
}

.portfolio-btn {
  display: inline-block;
  padding: 15px 40px;
  background: rgba(255, 255, 255, 0.25);
  backdrop-filter: blur(10px);
  -webkit-backdrop-filter: blur(10px);
  border: 1px solid rgba(255, 255, 255, 0.3);
  color: #000;
  text-decoration: none !important;
  border-radius: 50px;
  font-weight: 600;
  font-size: 1.1em;
  text-transform: uppercase;
  letter-spacing: 1px;
  transition: all 0.3s ease;
  box-shadow: 0 8px 32px rgba(0, 0, 0, 0.1);
}

.portfolio-btn:hover {
  transform: translateY(-2px);
  box-shadow: 0 12px 40px rgba(0, 0, 0, 0.15);
  background: rgba(255, 255, 255, 0.4);
  text-decoration: none !important;
}

.author__urls.social-icons .btn {
  background: rgba(255, 255, 255, 0.25) !important;
  backdrop-filter: blur(10px) !important;
  -webkit-backdrop-filter: blur(10px) !important;
  border: 1px solid rgba(255, 255, 255, 0.3) !important;
  color: #000 !important;
  text-decoration: none !important;
  border-radius: 50px !important;
  font-weight: 600 !important;
  transition: all 0.3s ease !important;
  box-shadow: 0 8px 32px rgba(0, 0, 0, 0.1) !important;
}

.author__urls.social-icons .btn:hover {
  transform: translateY(-2px) !important;
  box-shadow: 0 12px 40px rgba(0, 0, 0, 0.15) !important;
  background: rgba(255, 255, 255, 0.4) !important;
  text-decoration: none !important;
}

html.dark .project-item,
body.dark .project-item,
.greedy-nav--dark .project-item {
  box-shadow: 0 4px 12px rgba(0, 0, 0, 0.3);
}

html.dark .project-item:hover,
body.dark .project-item:hover,
.greedy-nav--dark .project-item:hover {
  box-shadow: 0 8px 24px rgba(0, 0, 0, 0.5);
}

html.dark .project-image,
body.dark .project-image,
.greedy-nav--dark .project-image {
  background: #2a2a2a;
}

.greedy-nav--dark .portfolio-btn,
html.dark .portfolio-btn,
body.dark .portfolio-btn {
  background: rgba(255, 255, 255, 0.1);
  border: 1px solid rgba(255, 255, 255, 0.2);
  color: #fff;
  box-shadow: 0 8px 32px rgba(0, 0, 0, 0.3);
}

.greedy-nav--dark .portfolio-btn:hover,
html.dark .portfolio-btn:hover,
body.dark .portfolio-btn:hover {
  background: rgba(255, 255, 255, 0.2);
  box-shadow: 0 12px 40px rgba(0, 0, 0, 0.4);
}

.greedy-nav--dark .author__urls.social-icons .btn,
html.dark .author__urls.social-icons .btn,
body.dark .author__urls.social-icons .btn {
  background: rgba(255, 255, 255, 0.1) !important;
  border: 1px solid rgba(255, 255, 255, 0.2) !important;
  color: #fff !important;
  box-shadow: 0 8px 32px rgba(0, 0, 0, 0.3) !important;
}

.greedy-nav--dark .author__urls.social-icons .btn:hover,
html.dark .author__urls.social-icons .btn:hover,
body.dark .author__urls.social-icons .btn:hover {
  background: rgba(255, 255, 255, 0.2) !important;
  box-shadow: 0 12px 40px rgba(0, 0, 0, 0.4) !important;
}

@media (max-width: 768px) {
  .projects-grid {
    grid-template-columns: 1fr;
    gap: 15px;
  }
}
</style>

<div class="intro-text">
  <p>I'm a recent Rutgers BME graduate. I've been designing with SolidWorks for about three years, have experience with several programming languages, and build and develop hardware using 3D-printed parts. I'm looking to fill this page with future projects in robotics and assistive technology.</p>
</div>

<hr>

<div class="projects-grid">
  {% for post in site.portfolio %}
    <a href="{{ post.url | relative_url }}" class="project-item">
      {% if post.header.teaser %}
        <img src="{{ post.header.teaser | relative_url }}" alt="{{ post.title }}" class="project-image">
      {% elsif post.image %}
        <img src="{{ post.image | relative_url }}" alt="{{ post.title }}" class="project-image">
      {% else %}
        <div class="project-image" style="background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);"></div>
      {% endif %}
      
      <div class="project-overlay">
        <h2 class="project-title">{{ post.title }}</h2>
        <p class="project-excerpt">{{ post.excerpt | strip_html | truncatewords: 20 }}</p>
        {% if post.date %}
          <span class="project-date">{{ post.date | date: "%B %Y" }}</span>
        {% endif %}
      </div>
    </a>
  {% endfor %}
</div>

<div style="text-align: center; margin-top: 40px;">
  <a href="/portfolio/" class="portfolio-btn">
    📁 View All Projects
  </a>
</div>
