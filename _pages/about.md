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
  margin: 60px 0;
  position: relative;
  padding: 0 60px;
}

.carousel-wrapper {
  position: relative;
  height: 400px;
  perspective: 1000px;
}

.project-card {
  position: absolute;
  width: 100%;
  max-width: 450px;
  aspect-ratio: 4 / 3;
  left: 50%;
  transform: translateX(-50%);
  background: rgba(255, 255, 255, 0.7);
  backdrop-filter: blur(10px);
  -webkit-backdrop-filter: blur(10px);
  border: 1px solid rgba(255, 255, 255, 0.3);
  border-radius: 20px;
  box-shadow: 0 8px 32px rgba(0, 0, 0, 0.1);
  overflow: hidden;
  text-decoration: none;
  color: inherit;
  transition: transform 0.6s ease, opacity 0.6s ease;
  opacity: 0;
  pointer-events: none;
}

.project-card.active {
  opacity: 1;
  pointer-events: auto;
  z-index: 2;
}

.project-card.next {
  transform: translateX(-50%) translateX(100px) rotateY(-15deg) scale(0.9);
  opacity: 0.5;
  z-index: 1;
}

.project-card.prev {
  transform: translateX(-50%) translateX(-100px) rotateY(15deg) scale(0.9);
  opacity: 0.5;
  z-index: 1;
}

.project-card:hover {
  box-shadow: 0 12px 40px rgba(0, 0, 0, 0.15);
}

.project-image {
  width: 100%;
  height: 100%;
  object-fit: contain;
  background: #f5f5f5;
  transition: all 0.5s ease;
}

.project-card:hover .project-image {
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

.project-card:hover .project-overlay {
  opacity: 1;
}

.project-content {
  text-align: center;
}

.project-card h3 {
  margin: 0 0 10px 0;
  font-size: 1.4em;
  color: #fff;
  font-weight: 600;
  text-shadow: 0 2px 8px rgba(0, 0, 0, 0.5);
}

.project-card p {
  margin: 0;
  color: #fff;
  font-size: 0.95em;
  line-height: 1.4;
  opacity: 0.95;
}

.project-date {
  font-size: 0.85em;
  color: #fff;
  margin-top: 10px;
  opacity: 0.8;
  font-style: italic;
  display: block;
}

.carousel-nav {
  position: absolute;
  top: 50%;
  transform: translateY(-50%);
  background: rgba(255, 255, 255, 0.25);
  backdrop-filter: blur(10px);
  -webkit-backdrop-filter: blur(10px);
  border: 1px solid rgba(255, 255, 255, 0.3);
  color: #000;
  width: 50px;
  height: 50px;
  border-radius: 50%;
  display: flex;
  align-items: center;
  justify-content: center;
  cursor: pointer;
  font-size: 24px;
  font-weight: bold;
  z-index: 10;
  transition: all 0.3s ease;
  box-shadow: 0 4px 15px rgba(0, 0, 0, 0.1);
  user-select: none;
}

.carousel-nav:hover {
  background: rgba(255, 255, 255, 0.4);
  box-shadow: 0 6px 20px rgba(0, 0, 0, 0.15);
  transform: translateY(-50%) scale(1.1);
}

.carousel-nav.disabled {
  opacity: 0.3;
  cursor: not-allowed;
  pointer-events: none;
}

.carousel-nav.prev {
  left: 0;
}

.carousel-nav.next {
  right: 0;
}

.carousel-dots {
  display: flex;
  justify-content: center;
  gap: 10px;
  margin-top: 30px;
}

.dot {
  width: 12px;
  height: 12px;
  border-radius: 50%;
  background: rgba(0, 0, 0, 0.2);
  cursor: pointer;
  transition: all 0.3s ease;
}

.dot.active {
  background: rgba(0, 0, 0, 0.6);
  transform: scale(1.2);
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

html.dark .project-image,
body.dark .project-image,
.greedy-nav--dark .project-image {
  background: #2a2a2a;
}

html.dark .carousel-nav,
body.dark .carousel-nav,
.greedy-nav--dark .carousel-nav {
  background: rgba(255, 255, 255, 0.1);
  border: 1px solid rgba(255, 255, 255, 0.2);
  color: #fff;
}

html.dark .carousel-nav:hover,
body.dark .carousel-nav:hover,
.greedy-nav--dark .carousel-nav:hover {
  background: rgba(255, 255, 255, 0.2);
}

html.dark .dot,
body.dark .dot,
.greedy-nav--dark .dot {
  background: rgba(255, 255, 255, 0.2);
}

html.dark .dot.active,
body.dark .dot.active,
.greedy-nav--dark .dot.active {
  background: rgba(255, 255, 255, 0.6);
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

[data-theme="air"] .portfolio-btn {
  background: rgba(255, 255, 255, 0.25);
  color: #000;
}

[data-theme="air-dark"] .portfolio-btn {
  background: rgba(255, 255, 255, 0.1);
  color: #fff;
}

/* Responsive */
@media (max-width: 768px) {
  .projects-carousel {
    padding: 0 50px;
  }
  
  .carousel-wrapper {
    height: 350px;
  }
  
  .carousel-nav {
    width: 40px;
    height: 40px;
    font-size: 20px;
  }
  
  .project-card {
    max-width: 350px;
  }
}
</style>

<div class="intro-text">
  <p>I'm a recent Rutgers BME graduate. I've been designing with SolidWorks for about three years, have experience with several programming languages, and build and develop hardware using 3D-printed parts. I'm looking to fill this page with future projects in robotics and assistive technology.</p>
</div>

<hr>

<div class="projects-carousel">
  <div class="carousel-wrapper" id="carouselWrapper">
    <div class="carousel-nav prev" onclick="moveCarousel(-1)">‹</div>
    <div class="carousel-nav next" onclick="moveCarousel(1)">›</div>
    
    {% assign project_index = 0 %}
    {% for post in site.portfolio %}
      <a href="{{ post.url | relative_url }}" class="project-card" data-index="{{ project_index }}">
        {% if post.header.teaser %}
          <img src="{{ post.header.teaser | relative_url }}" alt="{{ post.title }}" class="project-image">
        {% elsif post.image %}
          <img src="{{ post.image | relative_url }}" alt="{{ post.title }}" class="project-image">
        {% else %}
          <div class="project-image"></div>
        {% endif %}
        <div class="project-overlay">
          <div class="project-content">
            <h3>{{ post.title }}</h3>
            <p>{{ post.excerpt | strip_html | truncatewords: 20 }}</p>
            {% if post.date %}
              <span class="project-date">{{ post.date | date: "%B %Y" }}</span>
            {% endif %}
          </div>
        </div>
      </a>
      {% assign project_index = project_index | plus: 1 %}
    {% endfor %}
  </div>
  
  <div class="carousel-dots" id="dots"></div>
</div>

<div style="text-align: center; margin-top: 40px;">
  <a href="/portfolio/" class="portfolio-btn">
    📁 View All Projects
  </a>
</div>

<script>
let currentIndex = 0;
const cards = document.querySelectorAll('.project-card');
const totalCards = cards.length;
const dotsContainer = document.getElementById('dots');

// Create dots
for (let i = 0; i < totalCards; i++) {
  const dot = document.createElement('div');
  dot.className = 'dot';
  if (i === 0) dot.classList.add('active');
  dot.onclick = () => goToSlide(i);
  dotsContainer.appendChild(dot);
}

const dots = dotsContainer.querySelectorAll('.dot');

function updateCarousel() {
  cards.forEach((card, index) => {
    card.classList.remove('active', 'next', 'prev');
    
    if (index === currentIndex) {
      card.classList.add('active');
    } else if (index === currentIndex + 1 || (currentIndex === totalCards - 1 && index === 0)) {
      card.classList.add('next');
    } else if (index === currentIndex - 1 || (currentIndex === 0 && index === totalCards - 1)) {
      card.classList.add('prev');
    }
  });
  
  // Update dots
  dots.forEach((dot, index) => {
    dot.classList.toggle('active', index === currentIndex);
  });
  
  // Update navigation buttons
  document.querySelector('.carousel-nav.prev').classList.toggle('disabled', currentIndex === 0);
  document.querySelector('.carousel-nav.next').classList.toggle('disabled', currentIndex === totalCards - 1);
}

function moveCarousel(direction) {
  currentIndex += direction;
  if (currentIndex < 0) currentIndex = 0;
  if (currentIndex >= totalCards) currentIndex = totalCards - 1;
  updateCarousel();
}

function goToSlide(index) {
  currentIndex = index;
  updateCarousel();
}

// Keyboard navigation
document.addEventListener('keydown', (e) => {
  if (e.key === 'ArrowLeft') moveCarousel(-1);
  if (e.key === 'ArrowRight') moveCarousel(1);
});

// Initialize
updateCarousel();
</script>
