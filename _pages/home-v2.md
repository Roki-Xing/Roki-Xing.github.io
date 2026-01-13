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

  <h2>Hamilton</h2>

  <div class="lyrics-rotator" aria-live="polite">
    <div class="lyrics-rotator__header">
      <span class="lyrics-rotator__badge">Musical</span>
      <a class="lyrics-rotator__link" href="https://hamiltonmusical.com/" target="_blank" rel="noopener">Official site</a>
    </div>
    <p class="lyrics-rotator__text">I’m not throwing away my shot.</p>
    <p class="lyrics-rotator__meta">— Hamilton (Lin-Manuel Miranda)</p>
  </div>

  <script>
    (() => {
      const prefersReducedMotion = window.matchMedia && window.matchMedia('(prefers-reduced-motion: reduce)').matches;
      const lines = [
        "There's a million things I haven’t done. Just you wait.",
        "I’m not throwing away my shot.",
        "Rise up. When you’re living on your knees you rise up.",
        "Raise a glass to freedom,\\nSomething they can never take away.",
        "Tou want a revolution? I want a revelation.",
        "“We hold these truths to be self-evident\\nThat all men are created equal.”",
        "Look around, look around at\\nHow lucky we’re to be alive right now.",
        "Oceans rise. Empires fall.",
        "Dying is easy, young man. Living is harder.\\nWhen you got skin in the game you stay in the game.\\nBut you don’t get a win unless you play in the game.",
        "If there’s a fire you’re trying to douse.\\nYou can’t put it out from inside the house.",
        "I wanna sit under their own vine and fig tree,\\nA moment alone in the shade.",
        "I picked up a pen. I wrote my own deliverance.\\nIn the eye of a hurricane. There is quiet.",
        "We push away what we can never understand.\\nWe push away the unimaginable.",
        "See them walking in the park long after dark,\\nTaking in the sights of the city.\\nLook into your eyes and the sky’s the limit.",
        "The feeling of freedom of seeing the light\\nIt’s Ben Franklin with a key and a kite.",
        "Love|Death|Life doesn’t discriminate between the sinners\\nand the saints. It takes and it takes and it takes.",
        "I’m not inimitable. I am an original.\\nI’m not standing still. I’m lying in wait.",
        "Ready for the moment of the adrenaline\\nWhen you finally face your opponent.",
        "History has its eyes on you.",
        "You have no control. Who lives. Who dies. Who tells your story.",
        "The world turned upside down.\\nOh Philip, you outshine the morning sun.",
        "I’ll do whatever it takes. I’ll make a million mistakes.",
        "If we lay a strong enough foundation. We’ll pass it on to you.\\nWe’ll give the world to you. You’ll blow us all away.",
        "I’ll be Socrates throwing verbal rocks at these\\nmediocrities.",
        "How do you write like you’re running out of time?\\nWrite day and night like you’re running out of time.",
        "Life, liberty, and the pursuit of happiness.\\nWe fought for these ideals; we shouldn’t settle for less.",
        "Close your eyes and dream when the night gets dark.",
      ];

      const root = document.querySelector('.lyrics-rotator');
      if (!root) return;
      const textEl = root.querySelector('.lyrics-rotator__text');
      if (!textEl || lines.length === 0) return;

      let idx = Math.floor(Math.random() * lines.length);

      const render = (t) => {
        textEl.textContent = t;
      };

      render(lines[idx]);

      const tick = () => {
        idx = (idx + 1) % lines.length;
        const t = lines[idx];

        if (prefersReducedMotion) {
          render(t);
          return;
        }

        root.classList.add('is-fading');
        window.setTimeout(() => {
          render(t);
          root.classList.remove('is-fading');
        }, 220);
      };

      window.setInterval(tick, 6500);
    })();
  </script>
</div>
