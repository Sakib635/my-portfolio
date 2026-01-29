---
title: "Projects"
layout: default
permalink: /projects/
---

<div style="text-align: center; margin: 4rem 0 3rem;">
  <h1 style="font-size: 3rem; margin-bottom: 0.5rem;">Projects</h1>
  <p style="font-size: 1.3rem; color: var(--text-light); max-width: 720px; margin: 0 auto;">
    Open-source tools and research prototypes focused on AI-assisted software engineering, dependency resolution, program analysis, and automated repair.
  </p>
</div>

<div class="project-card" style="margin-bottom: 4rem;">
  <h2>tooool: Transforming Software Engineering Problems into SAT/SMT</h2>
  <p><strong>University of Windsor / Independent | 2024 – Ongoing</strong></p>
  <p>
    Core passion project: Converts complex SE challenges (dependency solving, configuration, Boolean reasoning) into <strong>Boolean Satisfiability (SAT)</strong> problems solvable by high-performance SMT solvers. Bridges classical constraint solving with modern software engineering pain points.
  </p>
  <p><strong>Tools & Techniques:</strong> Python, Z3/PySMT, SAT/SMT solvers, Constraint modeling, PyPI/Maven integration</p>
  <p><strong>Status:</strong> Active prototype – expanding to more SE domains</p>
  <p><strong>Link:</strong> <a href="https://github.com/Sakib635/tooool" target="_blank">GitHub: tooool</a></p>
  <!-- Add image if you have one: <img src="{{ site.baseurl }}/assets/images/tooool.png" alt="tooool Screenshot" class="project-img" loading="lazy"> -->
</div>

<div class="project-card" style="margin-bottom: 4rem;">
  <h2>PyHealer: LLM- and RAG-enabled Agentic Repair of Python Execution Failures</h2>
  <p><strong>University of Windsor | 2025 – 2026</strong></p>
  <p>
    Agentic AI system using <strong>LLMs + Retrieval-Augmented Generation (RAG)</strong> to diagnose and auto-repair Python runtime errors from missing deps, env mismatches, config issues, or code faults. Aims to reduce manual debugging in research/scientific Python workflows.
  </p>
  <p><strong>Tools & Techniques:</strong> Python, LLMs (e.g., GPT/Llama), LangChain/LlamaIndex-style RAG, Agent frameworks, Error parsing, Virtual env automation</p>
  <p><strong>Link:</strong> <a href="https://zenodo.org/records/18218624" target="_blank">Zenodo Record</a> (dataset/tool artifact)</p>
  <img src="{{ site.baseurl }}/assets/images/pyhealer.png"
       alt="PyHealer architecture or demo screenshot"
       class="project-img" loading="lazy">
</div>

<div class="project-card" style="margin-bottom: 4rem;">
  <h2>SMTpip: Solver-Based Dependency Management for Python</h2>
  <p><strong>University of Windsor (M.Sc. Thesis component) | 2024 – 2025</strong></p>
  <p>
    Prototype tool that translates Python dependency requirements into SMT constraints for optimal, conflict-free resolution — outperforming greedy pip in complex scenarios. Directly tied to thesis on better dependency ecosystems.
  </p>
  <p><strong>Tools & Techniques:</strong> Python, SMT solvers (Z3), PyPI API, Constraint satisfaction, Version modeling</p>
  <p><strong>Link:</strong> <a href="https://github.com/Sakib635/SMTpip" target="_blank">GitHub: SMTpip</a></p>
  <img src="{{ site.baseurl }}/assets/images/smtpip.png"
       alt="SMTpip interface or resolution example"
       class="project-img" loading="lazy">
</div>

<div class="project-card" style="margin-bottom: 4rem;">
  <h2>Custom AST Parsers for Python & Java</h2>
  <p><strong>University of Windsor | 2023 – 2024</strong></p>
  <p>
    Built extensible parsers and visualizers for <strong>Abstract Syntax Trees</strong> to support static analysis, code transformation, and research tooling in program comprehension.
  </p>
  <p><strong>Tools:</strong> Python ast module, Eclipse JDT (Java), Graph visualization</p>
  <p><strong>Links:</strong><br>
    • <a href="https://github.com/Sakib635/Custom-python-ast-parser" target="_blank">Python AST Parser</a><br>
    • <a href="https://github.com/Sakib635/Custom-java-ast-parser" target="_blank">Java AST Parser</a>
  </p>
  <!-- Add combined or example image if available -->
</div>

<div class="project-card">
  <h2>VTA Bot: Virtual Teaching Assistant</h2>
  <p><strong>BRAC University (Undergrad Thesis) | 2021 – 2022</strong></p>
  <p>
    Conversational AI bot powered by NLP and deep learning to answer student queries, explain concepts, and assist with coursework — early exploration of AI in education.
  </p>
  <p><strong>Tools & Techniques:</strong> NLTK, PyTorch, Intent classification, Dialogue management, Data collection</p>
  <p><strong>Link:</strong> <a href="https://github.com/Sakib635/Virtual-Teaching-Assistant-VTA-bot-" target="_blank">GitHub: VTA Bot</a></p>
  <img src="{{ site.baseurl }}/assets/images/vta.png"
       alt="VTA Bot conversation interface"
       class="project-img" loading="lazy">
</div>

<p style="text-align: center; margin-top: 4rem; font-style: italic;">
  All projects are open-source where possible. Interested in collaborating on agentic AI for SE, SMT applications, or dependency tools? Reach out via LinkedIn or GitHub!
</p>