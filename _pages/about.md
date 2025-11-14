---
permalink: /
title: "About Me"
author_profile: true
redirect_from: 
  - /about/
  - /about.html
---

I'm a recent Rutgers BME graduate. I've been designing with SolidWorks for about three years, have experience with several programming languages, and build and develop hardware using 3D-printed parts. I'm looking to fill this page with future projects in robotics and assistive technology.

---

## Projects

<style>
.projects-masonry {
  column-count: 3;
  column-gap: 20px;
  margin: 40px 0;
}

.project-item {
  display: inline-block;
  width: 100%;
  margin-bottom: 20px;
  break-inside: avoid;
  border-radius: 20px;
  overflow: hidden;
  box-shadow: 0 4px 12px rgba(0, 0, 0, 0.1);
  transition: all 0.3s ease;
  text-decoration: none;
  position: relative;
}

.project-item:hover {
  transform: translateY(-5px);
  box-shadow: 0 8px 24px rgba(0, 0, 0, 0.2);
  text-decoration: none;
}

.project-image {
  width: 100%;
  height: auto;
  display: block;
  background: #f5f5f5;
  transition: all 0.5s ease;
}

.project-item:hover .project-image {
  filter: blur(3px);
  transform: scale(1.05);
}

.project-overlay {
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  background: rgba(0, 0, 0, 0.7);
  backdrop-filter: blur(10px);
  display: flex;
  align-items: center;
  justify-content: center;
  padding: 20px;
  opacity: 0;
  transition: opacity 0.3s ease;
  text-align: center;
}

.project-item:hover .project-overlay {
  opacity: 1;
}

.project-title {
  color: #fff;
  font-size: 1.2em;
  font-weight: 600;
  margin: 0;
  text-shadow: 0 2px 8px rgba(0, 0, 0, 0.5);
}

@media (max-width: 1200px) {
  .projects-masonry {
    column-count: 2;
  }
}

@media (max-width: 768px) {
  .projects-masonry {
    column-count: 1;
  }
}
</style>

<div class="projects-masonry">
{% for post in site.portfolio %}
  <a href="{{ post.url | relative_url }}" class="project-item">
    {% if post.header.teaser %}
      <img src="{{ post.header.teaser | relative_url }}" alt="{{ post.title }}" class="project-image">
    {% elsif post.image %}
      <img src="{{ post.image | relative_url }}" alt="{{ post.title }}" class="project-image">
    {% else %}
      <div class="project-image" style="height: 300px; background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);"></div>
    {% endif %}
    <div class="project-overlay">
      <h2 class="project-title">{{ post.title }}</h2>
    </div>
  </a>
{% endfor %}
</div>
