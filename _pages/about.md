---
permalink: /
title: "About"
author_profile: true
redirect_from:
  - /about/
  - /about.html
---

<style>
/* Custom styles for this page */
.interest-pills {
  display: flex;
  flex-wrap: wrap;
  gap: 8px;
  margin: 15px 0 25px 0;
}
.interest-pill {
  background: linear-gradient(135deg, #fef5f1 0%, #fff 100%);
  border: 1px solid #e8dcd6;
  padding: 6px 14px;
  border-radius: 20px;
  font-size: 0.88em;
  color: #555;
  transition: all 0.2s ease;
}
.interest-pill:hover {
  background: #c56f6f;
  color: white;
  border-color: #c56f6f;
  transform: translateY(-1px);
}

.news-section {
  background: #fdfcfb;
  border-radius: 8px;
  padding: 15px 20px;
  margin: 15px 0;
  border-left: 3px solid #c56f6f;
}
.news-item {
  padding: 8px 0;
  border-bottom: 1px dashed #eee;
  display: flex;
  align-items: flex-start;
  gap: 12px;
}
.news-item:last-child { border-bottom: none; }
.news-date {
  font-weight: 700;
  color: #c56f6f;
  white-space: nowrap;
  min-width: 70px;
}

.timeline {
  position: relative;
  padding-left: 25px;
  margin: 20px 0;
}
.timeline::before {
  content: '';
  position: absolute;
  left: 6px;
  top: 5px;
  bottom: 5px;
  width: 2px;
  background: linear-gradient(to bottom, #c56f6f, #e8dcd6);
}
.timeline-item {
  position: relative;
  padding-bottom: 20px;
}
.timeline-item::before {
  content: '';
  position: absolute;
  left: -22px;
  top: 6px;
  width: 12px;
  height: 12px;
  background: #c56f6f;
  border-radius: 50%;
  border: 2px solid white;
  box-shadow: 0 0 0 2px #c56f6f;
}
.timeline-item h4 {
  margin: 0 0 4px 0;
  color: #333;
  font-size: 1.05em;
}
.timeline-item .meta {
  color: #888;
  font-size: 0.9em;
  margin-bottom: 6px;
}
.timeline-item p {
  margin: 0;
  color: #555;
  font-size: 0.95em;
  line-height: 1.5;
}

.project-grid {
  display: grid;
  gap: 20px;
  margin: 20px 0;
}
.project-card {
  background: #fdfcfb;
  border: 1px solid #eee;
  border-radius: 10px;
  padding: 20px;
  transition: all 0.3s ease;
}
.project-card:hover {
  box-shadow: 0 8px 25px rgba(197, 111, 111, 0.15);
  transform: translateY(-3px);
  border-color: #c56f6f;
}
.project-card h3 {
  margin: 0 0 10px 0;
  color: #c56f6f;
  font-size: 1.15em;
}
.project-card p {
  margin: 0 0 12px 0;
  color: #555;
  font-size: 0.95em;
  line-height: 1.5;
}
.project-tags {
  display: flex;
  flex-wrap: wrap;
  gap: 6px;
}
.tag {
  display: inline-block;
  padding: 3px 10px;
  font-size: 0.8em;
  background: #f0ebe8;
  border-radius: 4px;
  color: #666;
}

.award-list {
  margin: 15px 0;
}
.award-item {
  display: flex;
  align-items: baseline;
  padding: 8px 0;
  border-bottom: 1px solid #f5f5f5;
}
.award-item:last-child { border-bottom: none; }
.award-year {
  font-weight: 700;
  color: #c56f6f;
  min-width: 55px;
  font-size: 0.95em;
}
.award-text {
  color: #444;
}

.section-header {
  border-bottom: 2px solid #c56f6f;
  padding-bottom: 8px;
  margin: 30px 0 15px 0;
  color: #333;
}
</style>

I'm **Roky Xing (邢若琦)**, an undergraduate researcher in Mathematics & Applied Mathematics at [Xidian University](https://www.xidian.edu.cn/), Xi'an, China.

I build **learning-augmented optimizers** and **evaluation pipelines**, focusing on EOH (Evolution of Heuristics), neural optimizers (POM/EPOM-style), MoE routing, and reproducible black-box benchmarking.

<h2 class="section-header">Research Interests</h2>

<div class="interest-pills">
  <span class="interest-pill">🔬 Learning-augmented Optimization</span>
  <span class="interest-pill">🧠 Neural Optimizers (POM/EPOM)</span>
  <span class="interest-pill">🎛️ Mixture-of-Experts</span>
  <span class="interest-pill">📦 Black-box Optimization</span>
  <span class="interest-pill">📊 Reproducible Benchmarking</span>
  <span class="interest-pill">📈 Quantitative Finance</span>
</div>

<h2 class="section-header">News</h2>

<div class="news-section">
  <div class="news-item">
    <span class="news-date">2025-12</span>
    <span>Developing a MoE-based neural optimizer (MoE-POM) and tightening evaluation protocols for cross-task robustness.</span>
  </div>
  <div class="news-item">
    <span class="news-date">2025-12</span>
    <span>Building an LLM4AD workflow for paper reading, algorithm design, and experiment automation.</span>
  </div>
</div>

<h2 class="section-header">Experience</h2>

<div class="timeline">
  <div class="timeline-item">
    <h4>Undergraduate Researcher</h4>
    <div class="meta">Xidian University · 2024 - Present</div>
    <p>Research on learning-augmented optimization: EOH pipelines, neural optimizer policy design, MoE routing, and reproducible benchmarking.</p>
  </div>
  <div class="timeline-item">
    <h4>B.S. in Mathematics & Applied Mathematics</h4>
    <div class="meta">Xidian University (信息数学拔尖班) · 2024 - Present</div>
    <p>Core training in analysis, algebra, probability, and optimization, with applied focus on ML systems.</p>
  </div>
</div>

<h2 class="section-header">Projects</h2>

<div class="project-grid">
  <div class="project-card">
    <h3>🔧 EOH Research Toolkit</h3>
    <p>A research codebase for generating, evaluating, and iterating on optimization heuristics with reproducible experiment runners and structured logging.</p>
    <div class="project-tags">
      <span class="tag">Optimization</span>
      <span class="tag">Benchmarking</span>
      <span class="tag">Python</span>
    </div>
  </div>

  <div class="project-card">
    <h3>🎯 MoE-POM Neural Optimizer</h3>
    <p>A MoE-routed optimizer policy inspired by POM/EPOM. Targets robustness across tasks and scale variation, with careful training stability and ablations.</p>
    <div class="project-tags">
      <span class="tag">MoE</span>
      <span class="tag">Neural Optimizer</span>
      <span class="tag">Black-box</span>
    </div>
  </div>

  <div class="project-card">
    <h3>🤖 LLM4AD Workflow</h3>
    <p>A Claude/LLM-assisted workflow for paper reading, algorithm design, and experiment automation. Focus on turning reading into runnable baselines.</p>
    <div class="project-tags">
      <span class="tag">LLM</span>
      <span class="tag">Automation</span>
      <span class="tag">Research</span>
    </div>
  </div>
</div>

<h2 class="section-header">Awards</h2>

<div class="award-list">
  <div class="award-item">
    <span class="award-year">2025</span>
    <span class="award-text">Mathematical Modeling Competition Award <em style="color:#999">(TODO: verify)</em></span>
  </div>
  <div class="award-item">
    <span class="award-year">2025</span>
    <span class="award-text">Academic Ranking - 2/31 in major <em style="color:#999">(TODO: verify)</em></span>
  </div>
</div>

<h2 class="section-header">Talks</h2>

<div class="timeline">
  <div class="timeline-item">
    <h4>From Memory to Thinking: Pretrained Optimizers with Adaptive Reasoning</h4>
    <div class="meta">Internal seminar · 2025-12 <em style="color:#999">(TODO: verify)</em></div>
  </div>
</div>

---

<p style="text-align: center; color: #999; font-size: 0.85em; margin-top: 40px;">
  <em>Last updated: December 2024</em>
</p>
