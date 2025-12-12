---
permalink: /
title: "About"
author_profile: true
redirect_from:
  - /about/
  - /about.html
---

<style>
/* ========== 渐变动态标题 ========== */
.gradient-text {
  background: linear-gradient(90deg, #c56f6f, #e8a0a0, #f0c0a0, #c56f6f);
  background-size: 300% 300%;
  -webkit-background-clip: text;
  -webkit-text-fill-color: transparent;
  background-clip: text;
  animation: gradient-flow 4s ease infinite;
  font-weight: 700;
}
@keyframes gradient-flow {
  0% { background-position: 0% 50%; }
  50% { background-position: 100% 50%; }
  100% { background-position: 0% 50%; }
}

/* ========== 鼠标跟随光点 ========== */
.cursor-dot {
  position: fixed;
  width: 8px;
  height: 8px;
  background: #c56f6f;
  border-radius: 50%;
  pointer-events: none;
  z-index: 99999;
  transition: transform 0.1s ease;
  box-shadow: 0 0 10px #c56f6f, 0 0 20px #c56f6f;
}
.cursor-ring {
  position: fixed;
  width: 30px;
  height: 30px;
  border: 2px solid rgba(197, 111, 111, 0.5);
  border-radius: 50%;
  pointer-events: none;
  z-index: 99998;
  transition: all 0.15s ease-out;
}

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
  transform: translateY(-3px) scale(1.1);
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

/* ========== GitHub Stats ========== */
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

/* ========== 技能进度条 ========== */
.skills-section { margin: 20px 0; }
.skill-item { margin-bottom: 15px; }
.skill-header {
  display: flex;
  justify-content: space-between;
  margin-bottom: 5px;
  font-size: 0.95em;
}
.skill-name { font-weight: 600; }
.skill-percent { color: #c56f6f; font-weight: 700; }
.skill-bar {
  height: 8px;
  background: #eee;
  border-radius: 10px;
  overflow: hidden;
}
.skill-progress {
  height: 100%;
  background: linear-gradient(90deg, #c56f6f, #e8a0a0);
  border-radius: 10px;
  width: 0;
  transition: width 1.5s ease-out;
}

/* ========== 访客统计 ========== */
.visitor-stats {
  display: flex;
  justify-content: center;
  gap: 30px;
  margin: 20px 0;
  padding: 15px;
  background: #fdfcfb;
  border-radius: 10px;
  border: 1px solid #eee;
}
.stat-item { text-align: center; }
.stat-number {
  font-size: 1.5em;
  font-weight: 700;
  color: #c56f6f;
}
.stat-label { font-size: 0.85em; color: #888; }

/* ========== 彩蛋提示 ========== */
.easter-egg-hint {
  position: fixed;
  bottom: 10px;
  left: 10px;
  font-size: 0.7em;
  color: #ddd;
  cursor: default;
  user-select: none;
}
.easter-egg-hint:hover { color: #c56f6f; }

/* ========== 彩蛋弹窗 ========== */
.konami-popup {
  display: none;
  position: fixed;
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
  background: linear-gradient(135deg, #c56f6f, #e8a0a0);
  color: white;
  padding: 40px;
  border-radius: 20px;
  text-align: center;
  z-index: 100000;
  box-shadow: 0 20px 60px rgba(0,0,0,0.3);
  animation: popup-bounce 0.5s ease;
}
@keyframes popup-bounce {
  0% { transform: translate(-50%, -50%) scale(0); }
  50% { transform: translate(-50%, -50%) scale(1.1); }
  100% { transform: translate(-50%, -50%) scale(1); }
}
.konami-popup h2 { margin: 0 0 15px 0; font-size: 1.8em; }
.konami-popup p { margin: 0; font-size: 1.1em; }
.konami-overlay {
  display: none;
  position: fixed;
  top: 0; left: 0; right: 0; bottom: 0;
  background: rgba(0,0,0,0.5);
  z-index: 99999;
}

/* ========== 随机名言 ========== */
.random-quote {
  text-align: center;
  font-style: italic;
  color: #888;
  margin: 30px 0;
  padding: 20px;
  border-left: 3px solid #c56f6f;
  background: #fdfcfb;
  border-radius: 0 8px 8px 0;
}
.quote-text { font-size: 1em; margin-bottom: 10px; }
.quote-author { font-size: 0.85em; color: #aaa; }
/* ========== 刷新语录按钮 ========== */
.refresh-quote-btn {
  background: transparent;
  border: 1px solid #c56f6f;
  color: #c56f6f;
  padding: 5px 12px;
  border-radius: 15px;
  cursor: pointer;
  margin-top: 12px;
  font-size: 0.85em;
  transition: all 0.3s ease;
}
.refresh-quote-btn:hover {
  background: #c56f6f;
  color: white;
  transform: scale(1.05);
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
  cursor: default;
}
.interest-pill:hover {
  background: #c56f6f;
  color: white;
  border-color: #c56f6f;
  transform: translateY(-2px);
  box-shadow: 0 4px 12px rgba(197, 111, 111, 0.3);
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
.timeline-item h4 { margin: 0 0 4px 0; color: #333; font-size: 1.05em; }
.timeline-item .meta { color: #888; font-size: 0.9em; margin-bottom: 6px; }
.timeline-item p { margin: 0; color: #555; font-size: 0.95em; line-height: 1.5; }

.project-grid { display: grid; gap: 20px; margin: 20px 0; }
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
.project-card h3 { margin: 0 0 10px 0; color: #c56f6f; font-size: 1.15em; }
.project-card p { margin: 0 0 12px 0; color: #555; font-size: 0.95em; line-height: 1.5; }
.project-tags { display: flex; flex-wrap: wrap; gap: 6px; }
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
.award-year { font-weight: 700; color: #c56f6f; min-width: 55px; font-size: 0.95em; }
.award-text { color: #444; }

.section-header {
  border-bottom: 2px solid #c56f6f;
  padding-bottom: 8px;
  margin: 30px 0 15px 0;
  color: #333;
}

.welcome-section {
  text-align: center;
  padding: 20px 0 30px 0;
  margin-bottom: 10px;
}
.welcome-section h1 { font-size: 2.2em; margin-bottom: 10px; }
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

.click-effect {
  position: fixed;
  pointer-events: none;
  z-index: 99999;
  animation: click-burst 0.6s ease-out forwards;
}
@keyframes click-burst {
  0% { transform: scale(0) rotate(0deg); opacity: 1; }
  100% { transform: scale(1.5) rotate(180deg); opacity: 0; }
}

.project-card { transform-style: preserve-3d; }
.project-card.tilt-effect { transition: transform 0.1s ease-out, box-shadow 0.3s ease; }
</style>

<!-- 不蒜子统计 -->
<!-- <script async src="//busuanzi.ibruce.info/busuanzi/2.3/busuanzi.pure.mini.js"></script> -->

<!-- 鼠标光点 -->
<div class="cursor-dot" id="cursorDot"></div>
<div class="cursor-ring" id="cursorRing"></div>

<!-- 滚动进度条 -->
<div class="scroll-progress" id="scrollProgress"></div>

<!-- 返回顶部按钮 -->


<button class="back-to-top" id="backToTop" onclick="window.scrollTo({top: 0, behavior: 'smooth'})">↑</button>

<!-- Konami 彩蛋 -->
<div class="konami-overlay" id="konamiOverlay" onclick="hideKonami()"></div>
<div class="konami-popup" id="konamiPopup">
  <h2>🎉 You found it!</h2>
  <p>Thanks for exploring! Keep optimizing! 🚀</p>
  <p style="margin-top: 15px; font-size: 0.9em;">Press anywhere to close</p>
</div>
<div class="easter-egg-hint">↑↑↓↓←→←→BA</div>

<!-- 欢迎区域 -->
<div class="welcome-section">
  <h1><span class="welcome-emoji">👋</span> Hi, I'm <span class="gradient-text">Roky Xing</span></h1>
  <div class="typewriter">Building intelligent optimizers & reproducible benchmarks</div>
</div>

I'm **邢若琦**, an undergraduate researcher in Mathematics & Applied Mathematics at [Xidian University](https://www.xidian.edu.cn/), Xi'an, China.

I focus on **learning-augmented optimization**, including EOH (Evolution of Heuristics), neural optimizers (POM/EPOM-style), MoE routing, and reproducible black-box benchmarking.

<!-- 访客统计 -->
<div class="visitor-stats">
  <div class="stat-item">
    <div class="stat-number" id="busuanzi_value_site_pv">--</div>
    <div class="stat-label">Total Views</div>
  </div>
  <div class="stat-item">
    <div class="stat-number" id="busuanzi_value_site_uv">--</div>
    <div class="stat-label">Visitors</div>
  </div>
</div>

<h2 class="section-header">📊 GitHub Stats</h2>

<div class="github-stats">
  <img src="https://github-readme-stats.vercel.app/api?username=Roki-Xing&show_icons=true&theme=default&hide_border=true&bg_color=fdfcfb&title_color=c56f6f&icon_color=c56f6f&text_color=555" alt="GitHub Stats" />
  <img src="https://github-readme-streak-stats.herokuapp.com/?user=Roki-Xing&theme=default&hide_border=true&background=fdfcfb&ring=c56f6f&fire=c56f6f&currStreakLabel=c56f6f" alt="GitHub Streak" />
</div>

<h2 class="section-header">💻 Skills</h2>

<div class="skills-section">
  <div class="skill-item">
    <div class="skill-header">
      <span class="skill-name">Python</span>
      <span class="skill-percent">90%</span>
    </div>
    <div class="skill-bar"><div class="skill-progress" data-width="90"></div></div>
  </div>
  <div class="skill-item">
    <div class="skill-header">
      <span class="skill-name">PyTorch / Deep Learning</span>
      <span class="skill-percent">85%</span>
    </div>
    <div class="skill-bar"><div class="skill-progress" data-width="85"></div></div>
  </div>
  <div class="skill-item">
    <div class="skill-header">
      <span class="skill-name">Optimization Algorithms</span>
      <span class="skill-percent">80%</span>
    </div>
    <div class="skill-bar"><div class="skill-progress" data-width="80"></div></div>
  </div>
  <div class="skill-item">
    <div class="skill-header">
      <span class="skill-name">Machine Learning</span>
      <span class="skill-percent">75%</span>
    </div>
    <div class="skill-bar"><div class="skill-progress" data-width="75"></div></div>
  </div>
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

<h2 class="section-header">💬 Random Quote</h2>

<div class="random-quote" id="randomQuote">
  <div class="quote-text">"The only way to do great work is to love what you do."</div>
  <div class="quote-author">— Steve Jobs</div>
</div>

---

<p style="text-align: center; color: #999; font-size: 0.85em; margin-top: 40px;">
  <em>✨ Last updated: December 2024</em>
</p>

<script>
// ========== 全局函数（需要在 HTML 解析时就可用）==========
window.hideKonami = function() {
  document.getElementById("konamiOverlay").style.display = "none";
  document.getElementById("konamiPopup").style.display = "none";
};

window.updateQuote = function() { var el = document.getElementById("randomQuote"); if(el) el.innerHTML = "Loading..."; };

window.showKonami = function() {
  document.getElementById("konamiOverlay").style.display = "block";
  document.getElementById("konamiPopup").style.display = "block";
  for (var i = 0; i < 50; i++) {
    createConfetti();
  }
};




document.addEventListener("DOMContentLoaded", function() {

  var dot = document.getElementById("cursorDot");
  var ring = document.getElementById("cursorRing");
  var mouseX = 0, mouseY = 0;
  var ringX = 0, ringY = 0;

  if (dot && ring) {
    document.addEventListener("mousemove", function(e) {
      mouseX = e.clientX;
      mouseY = e.clientY;
      dot.style.left = mouseX - 4 + "px";
      dot.style.top = mouseY - 4 + "px";
    });

    function animateRing() {
      ringX += (mouseX - ringX) * 0.15;
      ringY += (mouseY - ringY) * 0.15;
      ring.style.left = ringX - 15 + "px";
      ring.style.top = ringY - 15 + "px";
      requestAnimationFrame(animateRing);
    }
    animateRing();

    if ("ontouchstart" in window) {
      dot.style.display = "none";
      ring.style.display = "none";
    }
  }

  window.addEventListener("scroll", function() {
    var scrollTop = document.documentElement.scrollTop || document.body.scrollTop;
    var scrollHeight = document.documentElement.scrollHeight - document.documentElement.clientHeight;
    var progress = (scrollTop / scrollHeight) * 100;
    var progressBar = document.getElementById("scrollProgress");
    if (progressBar) progressBar.style.width = progress + "%";

    var backToTop = document.getElementById("backToTop");
    if (backToTop) {
      if (scrollTop > 300) {
        backToTop.classList.add("visible");
      } else {
        backToTop.classList.remove("visible");
      }
    }
  });

  function animateSkills() {
    document.querySelectorAll(".skill-progress").forEach(function(skill) {
      skill.style.width = skill.getAttribute("data-width") + "%";
    });
  }
  setTimeout(animateSkills, 500);

  var observer = new IntersectionObserver(function(entries) {
    entries.forEach(function(entry) {
      if (entry.isIntersecting) animateSkills();
    });
  }, { threshold: 0.5 });
  var skillsSection = document.querySelector(".skills-section");
  if (skillsSection) observer.observe(skillsSection);

  var konamiCode = ["ArrowUp","ArrowUp","ArrowDown","ArrowDown","ArrowLeft","ArrowRight","ArrowLeft","ArrowRight","KeyB","KeyA"];
  var konamiIndex = 0;

  document.addEventListener("keydown", function(e) {
    if (e.code === konamiCode[konamiIndex]) {
      konamiIndex++;
      if (konamiIndex === konamiCode.length) {
        showKonami();
        konamiIndex = 0;
      }
    } else {
      konamiIndex = 0;
    }
  });

  // showKonami 和 hideKonami 已在全局定义

  function createConfetti() {
    var confetti = document.createElement("div");
    var hue = Math.random() * 360;
    var left = Math.random() * 100;
    var radius = Math.random() > 0.5 ? "50%" : "0";
    confetti.style.cssText = "position:fixed;width:10px;height:10px;background:hsl(" + hue + ",80%,60%);left:" + left + "vw;top:-10px;z-index:100001;pointer-events:none;border-radius:" + radius + ";";
    document.body.appendChild(confetti);

    var duration = 2000 + Math.random() * 2000;
    var rotation = Math.random() * 720;
    confetti.animate([
      { transform: "translateY(0) rotate(0deg)", opacity: 1 },
      { transform: "translateY(100vh) rotate(" + rotation + "deg)", opacity: 0 }
    ], { duration: duration, easing: "ease-out" });

    setTimeout(function() { confetti.remove(); }, duration);
  }

  var quotes = [
    { text: "The only way to do great work is to love what you do.", author: "Steve Jobs" },
    { text: "Premature optimization is the root of all evil.", author: "Donald Knuth" },
    { text: "Simplicity is the ultimate sophistication.", author: "Leonardo da Vinci" },
    { text: "In theory, there is no difference between theory and practice. In practice, there is.", author: "Yogi Berra" },
    { text: "The best way to predict the future is to invent it.", author: "Alan Kay" },
    { text: "Make it work, make it right, make it fast.", author: "Kent Beck" },
    { text: "Any sufficiently advanced technology is indistinguishable from magic.", author: "Arthur C. Clarke" },
    { text: "Talk is cheap. Show me the code.", author: "Linus Torvalds" },
    { text: "First, solve the problem. Then, write the code.", author: "John Johnson" },
    { text: "Code is like humor. When you have to explain it, it is bad.", author: "Cory House" }
  ];

  var lastQuoteIndex = -1;

  function updateQuote() {
    var newIndex;
    do {
      newIndex = Math.floor(Math.random() * quotes.length);
    } while (newIndex === lastQuoteIndex && quotes.length > 1);
    lastQuoteIndex = newIndex;

    var quote = quotes[newIndex];
    var quoteElement = document.getElementById("randomQuote");
    if (quoteElement) {
      quoteElement.style.opacity = "0";
      quoteElement.style.transition = "opacity 0.3s ease";
      
      setTimeout(function() {
        quoteElement.innerHTML = '<div class="quote-text">"' + quote.text + '"</div><div class="quote-author">— ' + quote.author + '</div><button class="refresh-quote-btn" onclick="window.updateQuote()" title="换一条">🔄 换一条</button>';
        quoteElement.style.opacity = "1";
      }, 300);
    }
  }

  window.updateQuote = updateQuote;
  updateQuote();
  setInterval(updateQuote, 15000);



  // ========== 鼠标点击特效 ==========
  var emojis = ["❤️", "✨", "💫", "⭐", "🌟", "💖"];
  document.addEventListener("click", function(e) {
    if (e.target.tagName === "BUTTON" || e.target.tagName === "A") return;
    for (var i = 0; i < 3; i++) {
      var el = document.createElement("div");
      el.className = "click-effect";
      el.innerHTML = emojis[Math.floor(Math.random() * emojis.length)];
      el.style.left = (e.clientX + (Math.random()-0.5)*30) + "px";
      el.style.top = (e.clientY + (Math.random()-0.5)*30) + "px";
      el.style.fontSize = (16 + Math.random()*10) + "px";
      document.body.appendChild(el);
      setTimeout(function(elem) { return function() { elem.remove(); }; }(el), 700);
    }
  });

  // ========== 3D 卡片悬浮 ==========
  document.querySelectorAll(".project-card").forEach(function(card) {
    card.classList.add("tilt-effect");
    card.addEventListener("mousemove", function(e) {
      var rect = card.getBoundingClientRect();
      var x = e.clientX - rect.left;
      var y = e.clientY - rect.top;
      var rotateX = (y - rect.height/2) / 10;
      var rotateY = (rect.width/2 - x) / 10;
      card.style.transform = "perspective(1000px) rotateX(" + rotateX + "deg) rotateY(" + rotateY + "deg) scale3d(1.02,1.02,1.02)";
    });
    card.addEventListener("mouseleave", function() {
      card.style.transform = "perspective(1000px) rotateX(0) rotateY(0) scale3d(1,1,1)";
    });
  });

});
</script>
