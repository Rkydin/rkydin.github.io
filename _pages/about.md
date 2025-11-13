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

.projects-carousel h2 {
  margin-bottom: 20px;
  font-size: 1.8em;
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
  background: #fff;
  border-radius: 10px;
  box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
  overflow: hidden;
  transition: transform 0.3s ease, box-shadow 0.3s ease;
  text-decoration: none;
  color: inherit;
  display: flex;
  flex-direction: column;
}

.project-card:hover {
  transform: translateY(-5px);
  box-shadow: 0 8px 12px rgba(0, 0, 0, 0.2);
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

/* Dark mode styles */
html.dark .project-card,
body.dark .project-card,
.greedy-nav--dark .project-card {
  background: #1a1a1a;
  color: #fff;
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
</style>

<div class="intro-text">
  <p>I'm a recent Rutgers BME graduate. I've been designing with SolidWorks for about three years, have experience with several programming languages, and build and develop hardware using 3D-printed parts. I'm looking to fill this page with future projects in robotics and assistive technology.</p>
</div>

## What I Do

I focus on mechanical design, prototyping, and hands-on hardware development. My work combines CAD design, 3D printing, and programming to create functional prototypes and robotic systems.

<div class="projects-carousel">
  <h2>Featured Projects</h2>
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
  <a href="/portfolio/" class="btn btn--primary" style="padding: 12px 30px; font-size: 1.1em;">View All Projects</a>
</div>
