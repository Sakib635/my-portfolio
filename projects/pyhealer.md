---
title: "PyHealer"
layout: default
permalink: /projects/pyhealer/
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
  <h2>PyHealer: LLM- and RAG-enabled Agentic Repair of Python Execution Failures</h2>
  <p><strong>University of Windsor | 2025 – 2026</strong></p>
  <p>
    Agentic AI system using <strong>LLMs + Retrieval-Augmented Generation (RAG)</strong> to diagnose and auto-repair Python runtime errors from missing deps, env mismatches, config issues, or code faults. Aims to reduce manual debugging in research/scientific Python workflows.
  </p>
  <p><strong>Tools & Techniques:</strong> Python, LLMs (e.g., GPT/Llama), LangChain/LlamaIndex-style RAG, Agent frameworks, Error parsing, Virtual env automation</p>
  <p><strong>Link:</strong> <a href="https://zenodo.org/records/18218624" target="_blank" rel="noopener">Zenodo Record</a> (dataset/tool artifact)</p>
  <img src="{{ site.baseurl }}/assets/images/pyhealer.png"
       alt="PyHealer architecture or demo screenshot"
       class="project-img" loading="lazy">
</div>
