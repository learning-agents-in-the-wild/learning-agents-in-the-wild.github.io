---
layout: page
title: Home
permalink: /
nav: false
description: ""
---

<style>
/* Remove default spacing */
.post-header { display: none !important; margin: 0 !important; padding: 0 !important; height: 0 !important; }
.post { margin-top: 0 !important; padding-top: 0 !important; }
.post > article { margin-top: 0 !important; padding-top: 0 !important; }

/* ===== Hero Banner ===== */
.hero {
  position: relative;
  width: 100vw;
  left: 50%;
  transform: translateX(-50%);
  padding: 80px 24px;
  margin-top: -20px;
  margin-bottom: 48px;
  text-align: center;
  background: url('{{ "/assets/img/banner.jpeg" | relative_url }}') center/cover no-repeat;
}

.hero::before {
  content: '';
  position: absolute;
  inset: 0;
  background: linear-gradient(180deg, rgba(15,23,42,0.6) 0%, rgba(30,27,75,0.55) 50%, rgba(15,23,42,0.65) 100%);
}

.hero::after {
  content: '';
  position: absolute;
  inset: 0;
  background: radial-gradient(ellipse at 50% 30%, rgba(99, 102, 241, 0.1) 0%, transparent 60%);
}

.hero-content {
  position: relative;
  z-index: 1;
  max-width: 720px;
  margin: 0 auto;
}

.hero-badge {
  display: inline-block;
  background: rgba(99, 102, 241, 0.15);
  border: 1px solid rgba(99, 102, 241, 0.3);
  color: #a5b4fc;
  padding: 8px 18px;
  border-radius: 20px;
  font-size: 0.8rem;
  font-weight: 500;
  letter-spacing: 0.5px;
  margin-bottom: 28px;
}

.hero h1 {
  font-size: 2.4rem;
  font-weight: 600;
  color: #fff;
  margin: 0 0 12px;
  letter-spacing: -0.3px;
  line-height: 1.2;
}

.hero h1 .subtitle {
  display: block;
  font-size: 1.35rem;
  font-weight: 300;
  color: rgba(255,255,255,0.7);
  margin-top: 10px;
  letter-spacing: 0.3px;
}

.hero-meta {
  display: flex;
  justify-content: center;
  gap: 24px;
  margin-top: 32px;
  flex-wrap: wrap;
}

.hero-meta-item {
  display: flex;
  align-items: center;
  gap: 8px;
  color: rgba(255,255,255,0.6);
  font-size: 0.9rem;
}

.hero-meta-item i {
  font-size: 1rem;
  color: #818cf8;
}

/* ===== Sections ===== */
.section { margin: 48px 0; }

.section h2 {
  font-size: 1.3rem;
  font-weight: 600;
  color: #1e293b;
  margin: 0 0 20px;
  padding-bottom: 12px;
  border-bottom: 1.5px solid #e2e8f0;
  letter-spacing: -0.02em;
}

.section p {
  color: #475569;
  line-height: 1.85;
  font-size: 1rem;
  letter-spacing: 0.01em;
  font-weight: 400;
}

/* ===== Topics List ===== */
.topics-list {
  list-style: none;
  padding: 0;
  margin: 16px 0;
}

.topics-list li {
  position: relative;
  padding: 7px 0 7px 22px;
  color: #475569;
  font-size: 0.95rem;
  line-height: 1.65;
  letter-spacing: 0.01em;
}

.topics-list li::before {
  content: '•';
  position: absolute;
  left: 0;
  color: #818cf8;
  font-weight: 600;
  font-size: 1.1rem;
}

.topics-list li strong {
  color: #111827;
  font-weight: 600;
}

/* ===== People ===== */
.people {
  display: grid;
  grid-template-columns: repeat(4, 1fr);
  gap: 1.25rem;
  margin: 24px 0;
}

@media (max-width: 768px) {
  .people { grid-template-columns: repeat(2, 1fr); }
}

.person {
  text-align: center;
  padding: 20px 12px 16px;
}

.person img {
  width: 88px;
  height: 88px;
  border-radius: 50%;
  object-fit: cover;
  margin-bottom: 10px;
  border: 3px solid #e5e7eb;
  transition: all 0.2s;
}

.person:hover img {
  border-color: #a5b4fc;
  transform: scale(1.03);
}

.person-link,
.person-link:hover,
.person-link:focus,
.person-link:active {
  text-decoration: none !important;
  color: inherit;
}

.person-link .person-name,
.person-link .person-aff {
  text-decoration: none !important;
}

.person-link:hover .person-name {
  color: #6366f1;
}

.person-name {
  font-size: 0.78rem;
  font-weight: 500;
  color: #1f2937;
  margin: 0 0 2px;
  line-height: 1.3;
  letter-spacing: -0.01em;
}

.person-aff {
  font-size: 0.65rem;
  font-weight: 400;
  color: #9ca3af;
  margin: 0;
  line-height: 1.25;
  letter-spacing: 0.01em;
  transform: scale(0.85);
  transform-origin: center top;
}

/* ===== Dates ===== */
.dates-list {
  list-style: none;
  padding: 0;
  margin: 20px 0;
}

.dates-list li {
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding: 12px 0;
  border-bottom: 1px solid #f1f5f9;
  font-size: 0.95rem;
}

.dates-list li:last-child {
  border-bottom: none;
}

.dates-list .label {
  color: #475569;
  font-weight: 400;
  letter-spacing: 0.01em;
}

.dates-list .value {
  color: #6366f1;
  font-weight: 500;
  letter-spacing: -0.01em;
}

/* ===== Contact ===== */
.contact-box {
  background: #f8fafc;
  border-radius: 12px;
  padding: 24px;
  text-align: center;
  margin: 24px 0;
}

.contact-box p {
  margin: 0;
  color: #475569;
  font-size: 0.95rem;
  letter-spacing: 0.01em;
}

.contact-box a {
  color: #6366f1;
  font-weight: 500;
}

/* ===== Responsive ===== */
@media (max-width: 640px) {
  .hero { padding: 56px 20px; }
  .hero h1 { font-size: 1.7rem; }
  .hero h1 .subtitle { font-size: 1rem; margin-top: 8px; }
  .hero-meta { gap: 16px; margin-top: 24px; }
  .hero-meta-item { font-size: 0.8rem; }
  .people { gap: 1rem; }
  .person { padding: 16px 8px 12px; }
  .person img { width: 72px; height: 72px; }
  .person-name { font-size: 0.75rem; }
  .person-aff { font-size: 0.4rem; }
  .dates-list li { flex-direction: column; align-items: flex-start; gap: 4px; }
}

/* ===== Dark Mode ===== */
html[data-theme='dark'] .section h2 { color: #f3f4f6; border-color: #374155; }
html[data-theme='dark'] .section p { color: #d1d5db; }
html[data-theme='dark'] .topics-list li { color: #d1d5db; }
html[data-theme='dark'] .topics-list li strong { color: #f3f4f6; }
html[data-theme='dark'] .person-name { color: #f3f4f6; }
html[data-theme='dark'] .person-aff { color: #6b7280; }
html[data-theme='dark'] .person img { border-color: #4b5563; }
html[data-theme='dark'] .person:hover img { border-color: #818cf8; }
html[data-theme='dark'] .person-link:hover .person-name { color: #a5b4fc; }
html[data-theme='dark'] .dates-list li { border-color: #374155; }
html[data-theme='dark'] .dates-list .label { color: #d1d5db; }
html[data-theme='dark'] .dates-list .value { color: #a5b4fc; }
html[data-theme='dark'] .contact-box { background: #1f2937; }
html[data-theme='dark'] .contact-box p { color: #d1d5db; }
html[data-theme='dark'] .contact-box a { color: #a5b4fc; }
</style>

<div class="hero">
  <div class="hero-content">
    <div class="hero-badge">ICML 2026 Workshop</div>
    <h1>Trustworthy Agentic AI<span class="subtitle">Failure Modes, Control, and Recovery</span></h1>
    <div class="hero-meta">
      <span class="hero-meta-item"><i class="ti ti-map-pin"></i> Seoul, South Korea</span>
      <span class="hero-meta-item"><i class="ti ti-calendar"></i> July 2026</span>
    </div>
  </div>
</div>

<div class="section">
<h2>About</h2>
<p>Agentic AI systems with long-horizon autonomy and real-world interaction are rapidly advancing toward real-world deployment, introducing new safety challenges. This workshop provides a forum for researchers and practitioners to study failure modes, risks, and approaches for improving the safety and robustness of agentic AI systems.</p>
</div>

<div class="section">
  <h2>Topics</h2>
  <ul class="topics-list">
  <li>Risk assessment and failure analysis for agentic AI systems</li>
  <li>Red-teaming and adversarial evaluation of agentic behavior</li>
  <li>Robustness and generalization under distribution shift</li>
  <li>Safety challenges in multi-agent systems and coordination</li>
  <li>Guardrails and safety mechanisms for agentic systems</li>
  <li>Governance, oversight, and policy considerations for agentic AI</li>
  <li>Case studies of real-world deployment such as web agents and workflow automation</li>
</ul>
</div>



<div class="section">
<h2>Speakers</h2>
<div class="people">
{% for speaker in site.data.speakers %}
  {% if speaker.url and speaker.url != "" %}
  <a href="{{ speaker.url }}" target="_blank" class="person-link">
  {% endif %}
    <div class="person">
      <img src="{{ speaker.image | relative_url }}" alt="{{ speaker.name }}">
      <p class="person-name">{{ speaker.name }}</p>
      <p class="person-aff">{{ speaker.affiliation }}</p>
    </div>
  {% if speaker.url and speaker.url != "" %}
  </a>
  {% endif %}
{% endfor %}
</div>
</div>

<div class="section">
<h2>Organizers</h2>
<div class="people">
{% for organizer in site.data.organizers %}
  {% if organizer.url and organizer.url != "" %}
  <a href="{{ organizer.url }}" target="_blank" class="person-link">
  {% endif %}
    <div class="person">
      <img src="{{ organizer.image | relative_url }}" alt="{{ organizer.name }}">
      <p class="person-name">{{ organizer.name }}</p>
      <p class="person-aff">{{ organizer.affiliation }}</p>
    </div>
  {% if organizer.url and organizer.url != "" %}
  </a>
  {% endif %}
{% endfor %}
</div>
</div>

<div class="section">
<h2>Important Dates</h2>
<ul class="dates-list">
  <li><span class="label">Submission Deadline</span><span class="value">TBA</span></li>
  <li><span class="label">Notification</span><span class="value">TBA</span></li>
  <li><span class="label">Camera-Ready</span><span class="value">TBA</span></li>
  <li><span class="label">Workshop</span><span class="value">TBA</span></li>
</ul>
</div>

<div class="section">
  <h2>Contact</h2>
  <div class="contact-box">
    <p>
      Questions? Email us at
      <a href="mailto:zijing.shi-1@uts.edu.au">zijing.shi-1@uts.edu.au</a>
    </p>
  </div>
</div>

