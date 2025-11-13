---
layout: archive
title: "Resume"
permalink: /resume/
author_profile: true
redirect_from:
  - /cv
---

{% include base_path %}

<style>
.resume-download-btn {
  display: inline-block;
  padding: 15px 40px;
  background-color: #000;
  color: #fff;
  text-decoration: none !important;
  border-radius: 50px;
  font-weight: 600;
  font-size: 1.1em;
  text-transform: uppercase;
  letter-spacing: 1px;
  transition: all 0.3s ease;
  box-shadow: 0 4px 15px rgba(0, 0, 0, 0.2);
  border: 2px solid transparent;
}

.resume-download-btn:hover {
  transform: translateY(-2px);
  box-shadow: 0 6px 20px rgba(0, 0, 0, 0.3);
  background-color: #333;
  text-decoration: none !important;
}

.resume-download-btn:focus,
.resume-download-btn:active {
  text-decoration: none !important;
}

/* Dark mode styles */
.greedy-nav--dark .resume-download-btn,
html.dark .resume-download-btn,
body.dark .resume-download-btn {
  background-color: #fff;
  color: #000;
  box-shadow: 0 4px 15px rgba(255, 255, 255, 0.2);
}

.greedy-nav--dark .resume-download-btn:hover,
html.dark .resume-download-btn:hover,
body.dark .resume-download-btn:hover {
  background-color: #f0f0f0;
  box-shadow: 0 6px 20px rgba(255, 255, 255, 0.3);
}

/* Air theme compatibility */
[data-theme="air"] .resume-download-btn {
  background-color: #000;
  color: #fff;
}

[data-theme="air-dark"] .resume-download-btn {
  background-color: #fff;
  color: #000;
}
</style>

<div style="text-align: center; margin-bottom: 30px; margin-top: 20px;">
  <a href="{{ base_path }}/files/resume.pdf" onclick="return confirmDownload();" class="resume-download-btn">
    📄 Download Resume PDF
  </a>
</div>

<div style="text-align: center; margin: 20px 0;">
  <iframe src="https://docs.google.com/viewer?url=https://rkydin.github.io/files/resume.pdf&embedded=true" width="100%" height="1200px" style="border: none;"></iframe>
</div>

<script>
function confirmDownload() {
  return confirm("Would you like to download the resume PDF?");
}
</script>
