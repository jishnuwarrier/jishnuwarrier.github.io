---
layout: page
permalink: /resume/
title: resume
nav: true
nav_order: 4
---

<style>
.resume-iframe {
  position: fixed;
  top: 0;
  left: 0;
  width: 100vw;
  height: 100vh;
  border: none;
  z-index: 1000;
  background: white;
}

.resume-container {
  position: relative;
  width: 100%;
  height: 100vh;
  margin: 0;
  padding: 0;
}

.post {
  margin: 0 !important;
  padding: 0 !important;
}

.container {
  max-width: none !important;
  padding: 0 !important;
}

body {
  overflow: hidden;
}
</style>

<div class="resume-container">
  <iframe 
    src="{{ 'assets/pdf/jishnu_resume.pdf' | relative_url }}" 
    class="resume-iframe"
    title="Jishnu Warrier Resume">
    <p style="padding: 2rem; text-align: center;">
      Your browser does not support PDFs. 
      <a href="{{ 'assets/pdf/jishnu_resume.pdf' | relative_url }}" target="_blank">
        Download the PDF
      </a> 
      to view it.
    </p>
  </iframe>
</div>