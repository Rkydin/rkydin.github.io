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
  background-color: var(--global-accent-color);
  color: #fff;
  text-decoration: none !important;
  font-family: "IBM Plex Mono", monospace;
  font-weight: 500;
  font-size: 1em;
  text-transform: uppercase;
  letter-spacing: 0.06em;
  transition: opacity 0.15s ease;
  border: 1px solid var(--global-accent-color);
}

.resume-download-btn:hover {
  opacity: 0.85;
  text-decoration: none !important;
}

.resume-download-btn:focus,
.resume-download-btn:active {
  text-decoration: none !important;
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
