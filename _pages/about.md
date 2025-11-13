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
  position: relative;
}

.carousel-wrapper {
  overflow: hidden;
  position: relative;
}

.carousel-container {
  display: flex;
  transition: transform 0.5s ease;
  gap: 20px;
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
  flex-shrink: 0;
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
  left: -25px;
}

.carousel-nav.next {
  right: -25px;
}

.carousel-dots {
  display: flex;
  justify-content: center;
  gap: 10px;
  margin-top: 20px;
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
</style>

<div class="intro-text">
  <p>I'm a recent Rutgers BME graduate. I've been designing with SolidWorks for about three years, have experience with several programming languages, and build and develop hardware using 3D-printed parts. I'm looking to fill this page with future projects in robotics and assistive technology.</p>
</div>

<hr>

<div class="projects-carousel">
  <div class="carousel-wrapper">
    <div class="carousel-nav prev" onclick="moveCarousel(-1)">‹</div>
    <div class="carousel-nav next" onclick="moveCarousel(1)">›</div>
    
    <div class="carousel-container" id="carousel">
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
  
  <div class="carousel-dots" id="dots"></div>
</div>

<div style="text-align: center; margin-top: 40px;">
  <a href="/portfolio/" class="portfolio-btn">
    📁 View All Projects
  </a>
</div>

<script>
let currentIndex = 0;
const carousel = document.getElementById('carousel');
const cards = carousel.querySelectorAll('.project-card');
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
  const cardWidth = cards[0].offsetWidth;
  const gap = 20;
  const offset = -(currentIndex * (cardWidth + gap));
  carousel.style.transform = `translateX(${offset}px)`;
  
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
