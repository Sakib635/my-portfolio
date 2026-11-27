---
title: "Projects"
layout: default
permalink: /projects/
---

<div style="text-align: center; margin: 4rem 0 0;">
  <h1 style="font-size: 3rem; margin-bottom: 0.5rem;">Projects</h1>
  <p style="font-size: 1.3rem; color: var(--text-light); max-width: 720px; margin: 0 auto;">
    Open-source tools and research prototypes focused on AI-assisted software engineering, dependency resolution, program analysis, and automated repair.
  </p>
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

<div class="project-card" style="margin-bottom: 4rem;">
  <h2>SMTpip: Solver-Based Dependency Management for Python</h2>
  <p><strong>University of Windsor (M.Sc. Thesis component) | 2024 – 2025</strong></p>
  <p>
    Prototype tool that translates Python dependency requirements into SMT constraints for optimal, conflict-free resolution — outperforming greedy pip in complex scenarios. Directly tied to thesis on better dependency ecosystems.
  </p>
  <p>Presented at The 26th IEEE International Conference on Source Code Analysis and Manipulation (SCAM 2026).</p>
  <a class="proj-open" href="{{ site.baseurl }}/projects/smtpip/">View SMTpip details &rarr;</a>
</div>

<div class="project-card" style="margin-bottom: 4rem;">
  <h2>PyHealer: LLM- and RAG-enabled Agentic Repair of Python Execution Failures</h2>
  <p><strong>University of Windsor | 2025 – 2026</strong></p>
  <p>
    Agentic AI system using <strong>LLMs + Retrieval-Augmented Generation (RAG)</strong> to diagnose and auto-repair Python runtime errors from missing deps, env mismatches, config issues, or code faults. Aims to reduce manual debugging in research/scientific Python workflows.
  </p>
  <a class="proj-open" href="{{ site.baseurl }}/projects/pyhealer/">View PyHealer details &rarr;</a>
</div>

<div class="project-card">
  <h2>VTA Bot: Virtual Teaching Assistant</h2>
  <p><strong>BRAC University (Undergrad Thesis) | 2021 – 2022</strong></p>
  <p>
    Conversational AI bot powered by NLP and deep learning to answer student queries, explain concepts, and assist with coursework — early exploration of AI in education.
  </p>
  <a class="proj-open" href="{{ site.baseurl }}/projects/vta-bot/">View VTA Bot details &rarr;</a>
</div>

<p style="text-align: center; margin-top: 4rem; font-style: italic;">
  All projects are open-source where possible. Interested in collaborating on agentic AI for SE, SMT applications, or dependency tools? Reach out via LinkedIn or GitHub!
</p>
