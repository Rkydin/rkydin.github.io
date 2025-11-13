---
layout: archive
title: "Resume"
permalink: /resume/
author_profile: true
redirect_from:
  - /cv
---

{% include base_path %}

<div style="text-align: center; margin: 20px 0;">
  <a href="{{ base_path }}/files/resume.pdf" onclick="return confirmDownload();" target="_blank">
    <img src="{{ base_path }}/files/resume.pdf" alt="Resume" style="max-width: 100%; height: auto; border: 2px solid #ccc; cursor: pointer;" />
  </a>
</div>

<div style="text-align: center; margin-top: 20px;">
  <p><em>Click the resume image above to download</em></p>
</div>

<script>
function confirmDownload() {
  return confirm("Would you like to download the resume PDF?");
}
</script>
