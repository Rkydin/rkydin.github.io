---
layout: archive
title: "Resume"
permalink: /resume/
author_profile: true
redirect_from:
  - /cv
---

{% include base_path %}

<div style="text-align: center; margin-bottom: 20px;">
  <a href="{{ base_path }}/files/resume.pdf" onclick="return confirmDownload();" class="btn btn--primary" style="font-size: 1.2em; padding: 12px 24px;">
    📄 Download Resume
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
