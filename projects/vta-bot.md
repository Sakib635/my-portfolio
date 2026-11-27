---
title: "VTA Bot"
layout: default
permalink: /projects/vta-bot/
---

<div style="text-align: center; margin: 4rem 0 0;">
  <h1 style="font-size: 3rem; margin-bottom: 0.5rem;">Projects</h1>
</div>

<style>
  .proj-tabs { display: flex; flex-wrap: wrap; justify-content: center; gap: 0.5rem; margin: 2rem 0 2.5rem; padding-bottom: 0.75rem; border-bottom: 1px solid rgba(127,127,127,.3); }
  .proj-tabs a { padding: 0.5rem 1.1rem; border-radius: 999px; border: 1px solid rgba(127,127,127,.35); text-decoration: none; font-weight: 600; color: inherit; transition: background .15s ease, transform .15s ease; }
  .proj-tabs a:hover, .proj-tabs a:focus-visible { background: rgba(127,127,127,.14); transform: translateY(-1px); outline: none; }
  .proj-tabs a.active { background: #3b82f6; border-color: #3b82f6; color: #fff; }
  .proj-open { display: inline-block; margin-top: 0.5rem; padding: 0.45rem 1rem; border-radius: 999px; border: 1px solid rgba(127,127,127,.4); text-decoration: none; font-weight: 600; }
  .proj-open:hover, .proj-open:focus-visible { background: rgba(127,127,127,.14); outline: none; }
</style>
<nav class="proj-tabs" aria-label="Project navigation">
  <a href="{{ site.baseurl }}/projects/"{% if page.url == '/projects/' %} class="active" aria-current="page"{% endif %}>Overview</a>
  <a href="{{ site.baseurl }}/projects/smtpip/"{% if page.url == '/projects/smtpip/' %} class="active" aria-current="page"{% endif %}>SMTpip</a>
  <a href="{{ site.baseurl }}/projects/pyhealer/"{% if page.url == '/projects/pyhealer/' %} class="active" aria-current="page"{% endif %}>PyHealer</a>
  <a href="{{ site.baseurl }}/projects/vta-bot/"{% if page.url == '/projects/vta-bot/' %} class="active" aria-current="page"{% endif %}>VTA Bot</a>
</nav>

<div class="project-card">
  <h2>VTA Bot: Virtual Teaching Assistant</h2>
  <p><strong>BRAC University (Undergrad Thesis) | 2021 – 2022</strong></p>
  <p>
    Conversational AI bot powered by NLP and deep learning to answer student queries, explain concepts, and assist with coursework — early exploration of AI in education.
  </p>
  <p><strong>Tools & Techniques:</strong> NLTK, PyTorch, Intent classification, Dialogue management, Data collection</p>
  <p><strong>Link:</strong> <a href="https://github.com/Sakib635/Virtual-Teaching-Assistant-VTA-bot-" target="_blank" rel="noopener">GitHub: VTA Bot</a></p>
  <img src="{{ site.baseurl }}/assets/images/vta.png"
       alt="VTA Bot conversation interface"
       class="project-img" loading="lazy">
</div>
