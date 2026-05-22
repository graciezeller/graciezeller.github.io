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
  <p><a href="/cv.pdf" target="_blank" class="cv-link">full cv (pdf)</a></p>

  <style>
    .cv-section {
      border-top: 1px solid #e8e8e8;
    }
    .cv-section:last-child {
      border-bottom: 1px solid #e8e8e8;
    }
    .cv-section-toggle {
      width: 100%;
      background: none;
      border: none;
      text-align: left;
      padding: 14px 0;
      cursor: pointer;
      display: flex;
      justify-content: space-between;
      align-items: center;
    }
    .cv-section-label {
      font-size: 15px;
      font-weight: 500;
      color: #111;
    }
    .cv-section-toggle:hover .cv-section-label {
      color: #444;
    }
    .cv-chevron {
      width: 16px;
      height: 16px;
      stroke: #999;
      fill: none;
      stroke-width: 2;
      stroke-linecap: round;
      stroke-linejoin: round;
      transition: transform 0.2s;
      flex-shrink: 0;
    }
    .cv-chevron.open {
      transform: rotate(180deg);
    }
    .cv-section-body {
      overflow: hidden;
      max-height: 0;
      transition: max-height 0.3s ease;
    }
    .cv-section-body.open {
      max-height: 1000px;
    }
    .cv-section-inner {
      padding-bottom: 1.25rem;
    }
    .cv-entry {
      display: flex;
      gap: 1rem;
      margin-bottom: 1rem;
    }
    .cv-entry:last-child {
      margin-bottom: 0;
    }
    .cv-entry-date {
      font-size: 12px;
      color: #999;
      min-width: 80px;
      padding-top: 2px;
    }
    .cv-entry-content {
      flex: 1;
    }
    .cv-entry-title {
      font-size: 14px;
      font-weight: 500;
      color: #111;
      margin: 0 0 2px;
    }
    .cv-entry-place {
      font-size: 13px;
      color: #666;
      margin: 0 0 4px;
    }
    .cv-entry-desc {
      font-size: 13px;
      color: #666;
      margin: 0;
      line-height: 1.6;
    }
    .cv-pub-item {
      margin-bottom: 0.75rem;
    }
    .cv-pub-item:last-child {
      margin-bottom: 0;
    }
    .cv-pub-title {
      font-size: 13px;
      font-weight: 500;
      color: #111;
      margin: 0 0 2px;
    }
    .cv-pub-meta {
      font-size: 12px;
      color: #999;
      margin: 0;
    }
    .cv-pub-meta a {
      color: #3b82f6;
      text-decoration: none;
    }
  </style>

  <div class="cv-wrap">

    <!-- ── Education ── -->
    <div class="cv-section">
      <button class="cv-section-toggle" onclick="cvToggle(this)" aria-expanded="false">
        <span class="cv-section-label">education</span>
        <svg class="cv-chevron" viewBox="0 0 24 24" aria-hidden="true"><polyline points="6 9 12 15 18 9"/></svg>
      </button>
      <div class="cv-section-body">
        <div class="cv-section-inner">
          <div class="cv-entry">
            <span class="cv-entry-date">2026 –</span>
            <div class="cv-entry-content">
              <p class="cv-entry-title">PhD student, Psychology (Cognition and Cognitive Neuroscience)</p>
              <p class="cv-entry-place">UMass Amherst</p>
              <p class="cv-entry-desc">Cognitive Construction Lab, advised by Ben Pitt.</p>
            </div>
          </div>
          <div class="cv-entry">
            <span class="cv-entry-date">2021 – 2025</span>
            <div class="cv-entry-content">
              <p class="cv-entry-title">B.S., Psychology & Anthropology</p>
              <p class="cv-entry-place">UW-Madison</p>
            </div>
          </div>
        </div>
      </div>
    </div>

    <!-- ── Experience ── -->
    <div class="cv-section">
      <button class="cv-section-toggle" onclick="cvToggle(this)" aria-expanded="false">
        <span class="cv-section-label">experience</span>
        <svg class="cv-chevron" viewBox="0 0 24 24" aria-hidden="true"><polyline points="6 9 12 15 18 9"/></svg>
      </button>
      <div class="cv-section-body">
        <div class="cv-section-inner">
        
          <div class="cv-entry">
            <span class="cv-entry-date">2025 – 2026</span>
            <div class="cv-entry-content">
              <p class="cv-entry-title">Laboratory Manager</p>
              <p class="cv-entry-place">Cognitive Origins Lab, UW-Madison</p>
              <p class="cv-entry-desc">PI: Stephen Ferrigno</p>
            </div>
          </div>

          <div class="cv-entry">
            <span class="cv-entry-date">2023 – 2025</span>
            <div class="cv-entry-content">
              <p class="cv-entry-title">Research Assistant</p>
              <p class="cv-entry-place">Cognitive Origins Lab, UW-Madison</p>
              <p class="cv-entry-desc">PI: Stephen Ferrigno</p>
            </div>
          </div>

          <div class="cv-entry">
            <span class="cv-entry-date">2024 – 2025</span>
            <div class="cv-entry-content">
              <p class="cv-entry-title">Research Assistant</p>
              <p class="cv-entry-place">DeLuca Biochemistry Lab, UW-Madison</p>
              <p class="cv-entry-desc">PIs: Hector DeLuca, Lori Plum</p>
            </div>
          </div>
          
        </div>
      </div>
    </div>

    <!-- ── Publications ── -->
    <div class="cv-section">
      <button class="cv-section-toggle" onclick="cvToggle(this)" aria-expanded="false">
        <span class="cv-section-label">publications</span>
        <svg class="cv-chevron" viewBox="0 0 24 24" aria-hidden="true"><polyline points="6 9 12 15 18 9"/></svg>
      </button>
      <div class="cv-section-body">
        <div class="cv-section-inner">
          <div class="cv-pub-item">
            <p class="cv-pub-title">Reasoning Through the Logic of One-to-one Correspondence in Children and Macaques</p>
            <p class="cv-pub-meta">Zeller, G., Ferrigno, S. · (in prep)
          </div>
        </div>
      </div>
    </div>

  </div>

  <script>
    function cvToggle(btn) {
      var body = btn.nextElementSibling;
      var chevron = btn.querySelector('.cv-chevron');
      var isOpen = body.classList.contains('open');
      body.classList.toggle('open', !isOpen);
      chevron.classList.toggle('open', !isOpen);
      btn.setAttribute('aria-expanded', String(!isOpen));
    }
  </script>

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
