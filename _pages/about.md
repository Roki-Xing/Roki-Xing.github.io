---
permalink: /
title: "About"
author_profile: true
redirect_from:
  - /about/
  - /about.html
---

<style>
/* ========== 滚动进度条 ========== */
.scroll-progress {
  position: fixed;
  top: 0;
  left: 0;
  height: 3px;
  background: linear-gradient(90deg, #c56f6f, #e8a0a0);
  width: 0%;
  z-index: 9999;
  transition: width 0.1s ease;
}

/* ========== 返回顶部按钮 ========== */
.back-to-top {
  position: fixed;
  bottom: 30px;
  right: 30px;
  width: 45px;
  height: 45px;
  background: linear-gradient(135deg, #c56f6f, #a85858);
  color: white;
  border: none;
  border-radius: 50%;
  cursor: pointer;
  font-size: 20px;
  box-shadow: 0 4px 15px rgba(197, 111, 111, 0.4);
  opacity: 0;
  visibility: hidden;
  transition: all 0.3s ease;
  z-index: 9998;
}
.back-to-top:hover {
  transform: translateY(-3px);
  box-shadow: 0 6px 20px rgba(197, 111, 111, 0.5);
}
.back-to-top.visible {
  opacity: 1;
  visibility: visible;
}

/* ========== 打字机效果 ========== */
.typewriter {
  overflow: hidden;
  border-right: 2px solid #c56f6f;
  white-space: nowrap;
  animation: typing 3s steps(40, end), blink-caret 0.75s step-end infinite;
  font-size: 1.1em;
  color: #c56f6f;
  font-weight: 500;
}
@keyframes typing {
  from { width: 0 }
  to { width: 100% }
}
@keyframes blink-caret {
  from, to { border-color: transparent }
  50% { border-color: #c56f6f }
}

/* ========== GitHub Stats 卡片容器 ========== */
.github-stats {
  display: flex;
  flex-wrap: wrap;
  gap: 15px;
  margin: 20px 0;
  justify-content: center;
}
.github-stats img {
  border-radius: 8px;
  transition: transform 0.3s ease;
}
.github-stats img:hover {
  transform: scale(1.02);
}

/* ========== 原有样式 ========== */
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

.award-list { margin: 15px 0; }
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
.award-text { color: #444; }

.section-header {
  border-bottom: 2px solid #c56f6f;
  padding-bottom: 8px;
  margin: 30px 0 15px 0;
  color: #333;
}

/* ========== 欢迎区域 ========== */
.welcome-section {
  text-align: center;
  padding: 20px 0 30px 0;
  margin-bottom: 10px;
}
.welcome-section h1 {
  font-size: 2em;
  margin-bottom: 10px;
  color: #333;
}
.welcome-emoji {
  font-size: 1.5em;
  animation: wave 2s ease-in-out infinite;
  display: inline-block;
}
@keyframes wave {
  0%, 100% { transform: rotate(0deg); }
  25% { transform: rotate(20deg); }
  75% { transform: rotate(-10deg); }
}
</style>

<!-- 滚动进度条 -->
<div class="scroll-progress" id="scrollProgress"></div>

<!-- 返回顶部按钮 -->
<button class="back-to-top" id="backToTop" onclick="window.scrollTo({top: 0, behavior: 'smooth'})">↑</button>

<!-- 欢迎区域 -->
<div class="welcome-section">
  <h1><span class="welcome-emoji">👋</span> Hi, I'm Roky Xing</h1>
  <div class="typewriter">Building intelligent optimizers & reproducible benchmarks</div>
</div>

I'm **邢若琦**, an undergraduate researcher in Mathematics & Applied Mathematics at [Xidian University](https://www.xidian.edu.cn/), Xi'an, China.

I focus on **learning-augmented optimization**, including EOH (Evolution of Heuristics), neural optimizers (POM/EPOM-style), MoE routing, and reproducible black-box benchmarking.

<h2 class="section-header">📊 GitHub Stats</h2>

<div class="github-stats">
  <img src="https://github-readme-stats.vercel.app/api?username=Roki-Xing&show_icons=true&theme=default&hide_border=true&bg_color=fdfcfb&title_color=c56f6f&icon_color=c56f6f&text_color=555" alt="GitHub Stats" />
  <img src="https://github-readme-streak-stats.herokuapp.com/?user=Roki-Xing&theme=default&hide_border=true&background=fdfcfb&ring=c56f6f&fire=c56f6f&currStreakLabel=c56f6f" alt="GitHub Streak" />
</div>

<h2 class="section-header">🔬 Research Interests</h2>

<div class="interest-pills">
  <span class="interest-pill">🔬 Learning-augmented Optimization</span>
  <span class="interest-pill">🧠 Neural Optimizers (POM/EPOM)</span>
  <span class="interest-pill">🎛️ Mixture-of-Experts</span>
  <span class="interest-pill">📦 Black-box Optimization</span>
  <span class="interest-pill">📊 Reproducible Benchmarking</span>
  <span class="interest-pill">📈 Quantitative Finance</span>
</div>

<h2 class="section-header">📰 News</h2>

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

<h2 class="section-header">🎓 Experience</h2>

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

<h2 class="section-header">🚀 Projects</h2>

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

<h2 class="section-header">🏆 Awards</h2>

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

<h2 class="section-header">🎤 Talks</h2>

<div class="timeline">
  <div class="timeline-item">
    <h4>From Memory to Thinking: Pretrained Optimizers with Adaptive Reasoning</h4>
    <div class="meta">Internal seminar · 2025-12 <em style="color:#999">(TODO: verify)</em></div>
  </div>
</div>

---

<p style="text-align: center; color: #999; font-size: 0.85em; margin-top: 40px;">
  <em>✨ Last updated: December 2024</em>
</p>

<!-- JavaScript for scroll progress and back-to-top -->
<script>
// 滚动进度条
window.addEventListener('scroll', function() {
  var scrollTop = document.documentElement.scrollTop || document.body.scrollTop;
  var scrollHeight = document.documentElement.scrollHeight - document.documentElement.clientHeight;
  var progress = (scrollTop / scrollHeight) * 100;
  document.getElementById('scrollProgress').style.width = progress + '%';

  // 返回顶部按钮显示/隐藏
  var backToTop = document.getElementById('backToTop');
  if (scrollTop > 300) {
    backToTop.classList.add('visible');
  } else {
    backToTop.classList.remove('visible');
  }
});
</script>
