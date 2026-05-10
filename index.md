---
layout: default
title: Gracie Zeller
---

<div class="hero">
  <div class="hero-inner" style="display: flex; justify-content: space-between; align-items: flex-start; gap: 2rem;">
    <div>
      <p><strong>Laboratory manager at UW-Madison.</strong></p>
      <p>I’m interested in children’s conceptual development, particularly how they come to understand numerical concepts and principles. I currently work as a lab manager in the <a href="https://cognitiveoriginslab.psych.wisc.edu/">Cognitive Origins Lab (Stephen Ferrigno)</a> at UW-Madison. In Fall 2026, I will be joining the <a href="https://cognitiveconstructionlab.com/">Cognitive Contruction Lab (Ben Pitt)</a> at UMass Amherst as a PhD student.</p>
    </div>
    <img src="/headshot.jpg" alt="Gracie Zeller"
      style="width: 175px; height: 175px; object-fit: cover; border-radius: 12px; flex-shrink: 0; border: 1px solid #d9cfc0;">
  </div>
</div>

<div class="divider"></div>

<section id="work">
  <p class="section-label">projects</p>
  {% for project in site.data.projects %}
  <div class="work-item">
    <div class="work-header" onclick="toggleAbstract(this.closest('.work-item'))">
      <span class="work-title">{{ project.title }}</span>
      <span class="work-year">{{ project.year }}</span>
    </div>
    <span class="work-abstract">
      {{ project.description }}
      {% if project.poster %}
        You can find our {{ project.poster_label | default: "poster" }} <a href="{{ project.poster }}" target="_blank">here</a>.
      {% endif %}
      {% if project.paper %}
        You can find the paper <a href="{{ project.paper }}" target="_blank">here</a>.
      {% endif %}
    </span>
  </div>
  {% endfor %}
</section>


<div class="divider"></div>

<section id="cv">
  <p class="section-label">curriculum vitae</p>
  <p><a href="/cv.pdf" target="_blank" class="cv-link">cv</a></p>
</section>

<div class="divider"></div>

<section id="contact">
  <p class="section-label">contact</p>
  <div class="contact-links">
    <p><a href="#" id="email-link">email</a></p>
    <script>
      const u = 'gzeller2';
      const d = 'wisc.edu';
      const el = document.getElementById('email-link');
      el.href = 'mailto:' + u + '@' + d;
      el.textContent = u + '@' + d;
    </script>
    <p><a href="https://bsky.app/profile/graciezeller.bsky.social" target="_blank">bluesky</a></p>
    <p><a href="https://www.linkedin.com/in/gracie-zeller" target="_blank">linkedin</a></p>
  </div>
</section>
