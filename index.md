---
layout: default
title: Gracie Zeller
---

<div class="hero">
  <div class="hero-inner" style="display: flex; justify-content: space-between; align-items: flex-start; gap: 2rem;">
    <div>
      <p>Laboratory manager at UW-Madison.</p>
      <p>I'm interested in children's conceptual development, particularly how they come to understand numerical concepts and principles. I currently work as a lab manager in the <a href="https://cognitiveoriginslab.psych.wisc.edu/">Cognitive Origins Lab (Stephen Ferrigno)</a> at UW-Madison. In Fall 2026, I will be joining the <a href="https://cognitiveconstructionlab.com/">Cognitive Contruction Lab (Ben Pitt)</a> at UMass Amherst as a PhD student.</p>
    </div>
    <img src="/headshot.jpg" alt="Gracie Zeller"
      style="width: 175px; height: 175px; object-fit: cover; border-radius: 12px; flex-shrink: 0; border: 1px solid #d9cfc0;">
  </div>
</div>

<div class="divider"></div>

<section id="cv">
  <p class="section-label">curriculum vitae</p>

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
              <p class="cv-entry-place">Cognitive Construction Lab, UMass Amherst</p>
              <p class="cv-entry-desc">PI: Benjamin Pitt</p>
            </div>
          </div>
          <div class="cv-entry">
            <span class="cv-entry-date">2021 – 2025</span>
            <div class="cv-entry-content">
              <p class="cv-entry-title">BS, Psychology & Anthropology</p>
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
          <p class="cv-entry-desc" style="margin-top: 1rem; font-style: italic;">
          Other experience includes caring for monkeys and mice, paperboard manufacturing (read: cardboard box factory), pizza artistry, toddler swim coaching, waterslide supervision, and extensive babysitting.
          </p>

        </div>
      </div>
    </div>


    <!-- ── Download button ── -->
    <a href="/cv.pdf" target="_blank" class="cv-download-btn">
      <svg viewBox="0 0 24 24" aria-hidden="true"><path d="M21 15v4a2 2 0 0 1-2 2H5a2 2 0 0 1-2-2v-4"/><polyline points="7 10 12 15 17 10"/><line x1="12" y1="15" x2="12" y2="3"/></svg>
      full cv (pdf)
    </a>

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
