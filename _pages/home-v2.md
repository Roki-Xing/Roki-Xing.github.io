---
permalink: /v2/
title: "Home (Preview)"
author_profile: true
---

<div class="home-v2">
  <div class="home-v2__top">
    <div class="home-v2__intro">
      <p><strong>Ruoqi Xing</strong> (邢若琦)</p>
      <p>Undergraduate student, Mathematics &amp; Applied Mathematics, <a href="https://www.xidian.edu.cn/">Xidian University</a> (Xi&#39;an, China).</p>
      <p>Email: <a href="mailto:24049200145@stu.xidian.edu.cn">24049200145@stu.xidian.edu.cn</a></p>
      <div class="home-v2__links">
        <a class="home-v2__chip" href="https://github.com/Roki-Xing">GitHub</a>
        <a class="home-v2__chip" href="/cv/">CV</a>
        <a class="home-v2__chip" href="/year-archive/">Blog</a>
      </div>
    </div>

    <div class="home-v2__panel">
      <h2 class="home-v2__panel-title">Research Interests</h2>
      <div class="interest-pills">
        <span class="interest-pill">Learning-augmented Optimization</span>
        <span class="interest-pill">Neural Optimizers (POM/EPOM)</span>
        <span class="interest-pill">Mixture-of-Experts (MoE)</span>
        <span class="interest-pill">Black-box Optimization</span>
        <span class="interest-pill">Reproducible Benchmarking</span>
      </div>
    </div>
  </div>

  <h2>What I’m Exploring</h2>

  <div class="media-card">
    <div class="media-card__thumb media-card__thumb--eoh">EOH</div>
    <div class="media-card__body">
      <strong>EOH (Evolution of Heuristics)</strong>
      <span class="media-card__desc">Exploring learning-augmented search pipelines and reproducible evaluation.</span>
      <div class="media-card__tags">
        <span class="tag">Optimization</span>
        <span class="tag">Evaluation</span>
      </div>
    </div>
  </div>

  <div class="media-card">
    <div class="media-card__thumb media-card__thumb--moe">MoE</div>
    <div class="media-card__body">
      <strong>MoE routing for neural optimizers</strong>
      <span class="media-card__desc">Experimenting with routing designs and stability/ablation setups.</span>
      <div class="media-card__tags">
        <span class="tag">MoE</span>
        <span class="tag">Neural Optimizer</span>
      </div>
    </div>
  </div>

  <div class="media-card">
    <div class="media-card__thumb media-card__thumb--bench">Bench</div>
    <div class="media-card__body">
      <strong>Reproducible black-box benchmarking</strong>
      <span class="media-card__desc">Building small, repeatable baselines and evaluation scripts.</span>
      <div class="media-card__tags">
        <span class="tag">Benchmarking</span>
        <span class="tag">Reproducibility</span>
      </div>
    </div>
  </div>

  <h2>News</h2>

  <div class="news-item">
    <span class="news-date">2025-12</span>
    <span class="news-text">Exploring a MoE-based neural optimizer (MoE-POM) and improving evaluation protocols for cross-task robustness.</span>
  </div>
  <div class="news-item">
    <span class="news-date">2025-12</span>
    <span class="news-text">Experimenting with an LLM-assisted workflow for paper reading, algorithm design, and experiment automation.</span>
  </div>

  <h2>Quote</h2>

  <div class="quote-rotator" aria-live="polite">
    <p class="quote-rotator__text">All models are wrong, but some are useful.</p>
    <p class="quote-rotator__author">— George E. P. Box</p>
  </div>

  <script>
    (() => {
      const prefersReducedMotion = window.matchMedia && window.matchMedia('(prefers-reduced-motion: reduce)').matches;
      const quotes = [
        { text: 'All models are wrong, but some are useful.', author: 'George E. P. Box' },
        { text: 'Simplicity is prerequisite for reliability.', author: 'Edsger W. Dijkstra' },
        { text: 'What I cannot create, I do not understand.', author: 'Richard P. Feynman' },
        { text: 'If I have seen further it is by standing on the shoulders of Giants.', author: 'Isaac Newton' },
        { text: 'We can only see a short distance ahead, but we can see plenty there that needs to be done.', author: 'Alan Turing' },
      ];

      const root = document.querySelector('.quote-rotator');
      if (!root) return;
      const textEl = root.querySelector('.quote-rotator__text');
      const authorEl = root.querySelector('.quote-rotator__author');
      if (!textEl || !authorEl || quotes.length === 0) return;

      let idx = Math.floor(Math.random() * quotes.length);
      const render = (q) => {
        textEl.textContent = q.text;
        authorEl.textContent = `— ${q.author}`;
      };

      render(quotes[idx]);

      const tick = () => {
        idx = (idx + 1) % quotes.length;
        const q = quotes[idx];

        if (prefersReducedMotion) {
          render(q);
          return;
        }

        root.classList.add('is-fading');
        window.setTimeout(() => {
          render(q);
          root.classList.remove('is-fading');
        }, 220);
      };

      window.setInterval(tick, 6500);
    })();
  </script>
</div>
