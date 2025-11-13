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

.projects-carousel {
  margin: 40px 0;
}

.carousel-container {
  display: flex;
  overflow-x: auto;
  scroll-behavior: smooth;
  gap: 20px;
  padding: 20px 0;
  scrollbar-width: thin;
}

.carousel-container::-webkit-scrollbar {
  height: 8px;
}

.carousel-container::-webkit-scrollbar-track {
  background: #f1f1f1;
  border-radius: 10px;
}

.carousel-container::-webkit-scrollbar-thumb {
  background: #888;
  border-radius: 10px;
}

.carousel-container::-webkit-scrollbar-thumb:hover {
  background: #555;
}

.project-card {
  min-width: 350px;
  max-width: 350px;
  background: rgba(255, 255, 255, 0.7);
  backdrop-filter: blur(10px);
  -webkit-backdrop-filter: blur(10px);
  border: 1px solid rgba(255, 255, 255, 0.3);
  border-radius: 15px;
  box-shadow: 0 8px 32px rgba(0, 0, 0, 0.1);
  overflow: hidden;
  transition: transform 0.3s ease, box-shadow 0.3s ease, background 0.3s ease;
  text-decoration: none;
  color: inherit;
  display: flex;
  flex-direction: column;
}

.project-card:hover {
  transform: translateY(-5px);
  box-shadow: 0 12px 40px rgba(0, 0, 0, 0.15);
  background: rgba(255, 255, 255, 0.85);
  text-decoration: none;
}

.project-image {
  width: 100%;
  height: 200px;
  object-fit: cover;
  background: #f0f0f0;
}

.project-content {
  padding: 20px;
  flex-grow: 1;
  display: flex;
  flex-direction: column;
}

.project-card h3 {
  margin-top: 0;
  margin-bottom: 10px;
  font-size: 1.3em;
  color: #000;
}

.project-card p {
  flex-grow: 1;
  margin-bottom: 15px;
  color: #555;
  font-size: 0.95em;
  line-height: 1.4;
}

.project-date {
  font-size: 0.85em;
  color: #888;
  font-style: italic;
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

.portfolio-btn:focus,
.portfolio-btn:active {
  text-decoration: none !important;
}

/* Glass Follow Button in Sidebar */
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

/* Dark mode styles */
html.dark .project-card,
body.dark .project-card,
.greedy-nav--dark .project-card {
  background: rgba(26, 26, 26, 0.7);
  border: 1px solid rgba(255, 255, 255, 0.1);
  color: #fff;
}

html.dark .project-card:hover,
body.dark .project-card:hover,
.greedy-nav--dark .project-card:hover {
  background: rgba(26, 26, 26, 0.85);
}

html.dark .project-card h3,
body.dark .project-card h3,
.greedy-nav--dark .project-card h3 {
  color: #fff;
}

html.dark .project-card p,
body.dark .project-card p,
.greedy-nav--dark .project-card p {
  color: #ccc;
}

html.dark .carousel-container::-webkit-scrollbar-track,
body.dark .carousel-container::-webkit-scrollbar-track,
.greedy-nav--dark .carousel-container::-webkit-scrollbar-track {
  background: #333;
}

html.dark .project-image,
body.dark .project-image,
.greedy-nav--dark .project-image {
  background: #2a2a2a;
}

/* Dark mode button styles */
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

/* Dark mode Follow button */
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

[data-theme="air"] .portfolio-btn {
  background: rgba(255, 255, 255, 0.25);
  color: #000;
}

[data-theme="air-dark"] .portfolio-btn {
  background: rgba(255, 255, 255, 0.1);
  color: #fff;
}
</style>

<div class="intro-text">
  <p>I'm a recent Rutgers BME graduate. I've been designing with SolidWorks for about three years, have experience with several programming languages, and build and develop hardware using 3D-printed parts. I'm looking to fill this page with future projects in robotics and assistive technology.</p>
</div>

<hr>

<div class="projects-carousel">
  <div class="carousel-container">
    {% for post in site.portfolio %}
      <a href="{{ post.url | relative_url }}" class="project-card">
        {% if post.header.teaser %}
          <img src="{{ post.header.teaser | relative_url }}" alt="{{ post.title }}" class="project-image">
        {% elsif post.image %}
          <img src="{{ post.image | relative_url }}" alt="{{ post.title }}" class="project-image">
        {% else %}
          <div class="project-image"></div>
        {% endif %}
        <div class="project-content">
          <h3>{{ post.title }}</h3>
          <p>{{ post.excerpt | strip_html | truncatewords: 25 }}</p>
          {% if post.date %}
            <span class="project-date">{{ post.date | date: "%B %Y" }}</span>
          {% endif %}
        </div>
      </a>
    {% endfor %}
  </div>
</div>

<div style="text-align: center; margin-top: 40px;">
  <a href="/portfolio/" class="portfolio-btn">
    📁 View All Projects
  </a>
</div>
