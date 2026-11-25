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

<style>
  .smt-links { display: flex; flex-wrap: wrap; gap: 0.75rem; margin: 1rem 0 1.5rem; }
  .smt-links a { display: inline-block; padding: 0.5rem 1rem; border: 1px solid rgba(127,127,127,.4); border-radius: 999px; text-decoration: none; font-weight: 600; transition: transform .15s ease, box-shadow .15s ease; }
  .smt-links a:hover, .smt-links a:focus-visible { transform: translateY(-2px); box-shadow: 0 4px 12px rgba(0,0,0,.15); }
  .smt-hint { font-size: 0.95rem; opacity: .75; margin: 0 0 1rem; }
  .smt-grid { display: grid; grid-template-columns: repeat(auto-fit, minmax(210px, 1fr)); gap: 1rem; margin-bottom: 1.5rem; }
  .smt-tile { text-align: left; font: inherit; color: inherit; cursor: pointer; padding: 1rem; border: 1px solid rgba(127,127,127,.35); border-radius: 12px; background: rgba(127,127,127,.06); transition: transform .18s ease, box-shadow .18s ease, border-color .18s ease; }
  .smt-tile:hover, .smt-tile:focus-visible { transform: translateY(-4px); box-shadow: 0 8px 20px rgba(0,0,0,.18); border-color: rgba(127,127,127,.7); outline: none; }
  .smt-tile-num { font-size: 0.8rem; opacity: .65; text-transform: uppercase; letter-spacing: .06em; }
  .smt-tile-title { display: block; font-size: 1.1rem; font-weight: 700; margin: 0.15rem 0 0.5rem; }
  .smt-badge { display: inline-block; font-size: 0.78rem; font-weight: 700; padding: 0.15rem 0.6rem; border-radius: 999px; }
  .smt-badge.ok { background: rgba(46,160,67,.18); color: #2a8a3e; }
  .smt-badge.unsat { background: rgba(207,34,46,.16); color: #c0262f; }
  .smt-badge.illus { background: rgba(130,80,223,.16); color: #7b4fd0; }
  .smt-teaser { display: block; max-height: 0; opacity: 0; overflow: hidden; font-size: 0.9rem; margin-top: 0; transition: max-height .25s ease, opacity .25s ease, margin-top .25s ease; }
  .smt-tile:hover .smt-teaser, .smt-tile:focus-visible .smt-teaser { max-height: 8rem; opacity: .9; margin-top: 0.6rem; }
  .smt-overlay { position: fixed; inset: 0; z-index: 9999; display: none; align-items: center; justify-content: center; padding: 1rem; background: rgba(0,0,0,.55); }
  .smt-overlay.open { display: flex; }
  .smt-modal { position: relative; width: 100%; max-width: 680px; max-height: 88vh; overflow-y: auto; padding: 1.75rem; border-radius: 14px; background: var(--bg, #fff); color: var(--text, #1f2328); box-shadow: 0 20px 50px rgba(0,0,0,.4); animation: smt-pop .18s ease; }
  @keyframes smt-pop { from { transform: scale(.96); opacity: 0; } to { transform: scale(1); opacity: 1; } }
  .smt-close { position: absolute; top: 0.6rem; right: 0.8rem; font-size: 1.6rem; line-height: 1; background: none; border: none; cursor: pointer; color: inherit; opacity: .7; }
  .smt-close:hover, .smt-close:focus-visible { opacity: 1; }
  .smt-modal h3 { margin: 0 0 0.4rem; }
  .smt-sec { margin-top: 1rem; }
  .smt-sec-label { font-size: 0.8rem; font-weight: 700; text-transform: uppercase; letter-spacing: .06em; opacity: .65; margin-bottom: 0.25rem; }
  .smt-sec p, .smt-sec ul { margin: 0; }
  .smt-sec ul { padding-left: 1.2rem; }
  .smt-note { font-size: 0.9rem; opacity: .8; margin-top: 0.5rem; }
</style>

<div class="project-card" style="margin-bottom: 4rem;">
  <h2>SMTpip: Solver-Based Dependency Management for Python</h2>
  <p><strong>University of Windsor (M.Sc. Thesis component) | 2024 – 2025</strong></p>
  <p>
    Prototype tool that translates Python dependency requirements into SMT constraints for optimal, conflict-free resolution — outperforming greedy pip in complex scenarios. Directly tied to thesis on better dependency ecosystems.
  </p>
  <p><strong>Tools & Techniques:</strong> Python, SMT solvers (Z3), PyPI API, Constraint satisfaction, Version modeling</p>

  <div class="smt-links">
    <a href="https://github.com/SMTpip" target="_blank" rel="noopener">GitHub: SMTpip</a>
    <a href="https://www.youtube.com/watch?v=KkNRGhvMwxw" target="_blank" rel="noopener">Demo Video (YouTube)</a>
  </div>

  <img src="{{ site.baseurl }}/assets/images/architecture.png"
       alt="SMTpip interface or resolution example"
       class="project-img" loading="lazy">

  <h3 style="margin-top: 2rem;">Example Scenarios</h3>
  <p class="smt-hint">Hover over a scenario for a preview; click it for full details.</p>
  <div class="smt-grid" id="smt-grid"></div>
  <p class="smt-note">
    Resolution success denotes that SMTpip produced a satisfiable installation plan; it does not imply that the project's source code executes successfully once installed.
  </p>
</div>

<div class="smt-overlay" id="smt-overlay" aria-hidden="true">
  <div class="smt-modal" role="dialog" aria-modal="true" aria-labelledby="smt-modal-title">
    <button class="smt-close" id="smt-close" type="button" aria-label="Close">&times;</button>
    <h3 id="smt-modal-title"></h3>
    <span class="smt-badge" id="smt-modal-badge"></span>
    <div id="smt-modal-body"></div>
  </div>
</div>

<script>
(function () {
  var scenarios = [
    {
      title: "fflpy", tag: "Issue #1", status: "ok", label: "Resolved",
      teaser: "A pinned click==6.6 conflicts with recent pip-tools releases; SMTpip selects pip-tools==4.4.0.",
      sections: [
        ["Requirements", "<ul><li><code>click==6.6</code></li><li><code>pip-tools&gt;=4.0.0</code></li></ul>"],
        ["Conflict", "<p>Newer <code>pip-tools</code> releases, such as 7.4.1, depend on <code>click&gt;=8.0</code>, which contradicts the pinned <code>click</code>.</p>"],
        ["pip behavior", "<p>pip selects <code>click==6.6</code>, tries the latest candidate <code>pip-tools==7.4.1</code>, detects the conflict, and backtracks through earlier releases until it reaches 4.4.0, which does not impose the conflicting constraint.</p>"],
        ["SMTpip result", "<p>Selects <code>pip-tools==4.4.0</code> and generates the installation plan (<code>install_script.txt</code>).</p>"]
      ]
    },
    {
      title: "ltiauthenticator", tag: "Real project", status: "ok", label: "Resolved",
      teaser: "A wildcard oauthlib==2.* excludes recent JupyterHub releases; SMTpip selects jupyterhub==0.9.1.",
      sections: [
        ["Requirements", "<ul><li><code>oauthlib==2.*</code> (a wildcard constraint)</li><li><code>jupyterhub&gt;=0.8</code></li></ul>"],
        ["Conflict", "<p>Recent JupyterHub releases require <code>oauthlib&gt;=3.0</code>.</p>"],
        ["SMTpip result", "<p>Selects the older release <code>jupyterhub==0.9.1</code> and generates an installation plan.</p>"]
      ]
    },
    {
      title: "AutoGPT", tag: "Real project", status: "unsat", label: "Not satisfiable",
      teaser: "googlesearch_python==1.1.0 caps requests below the required minimum; no valid plan exists.",
      sections: [
        ["Requirements", "<ul><li><code>requests&gt;=2.26.0</code></li><li><code>googlesearch_python==1.1.0</code></li></ul>"],
        ["Conflict", "<p><code>googlesearch_python==1.1.0</code> requires <code>requests&lt;=2.25.1</code>, which contradicts the minimum version of <code>requests</code>.</p>"],
        ["SMTpip result", "<p>Reports <strong>Not satisfiable</strong>.</p>"]
      ]
    },
    {
      title: "Constructed example", tag: "Constructed", status: "unsat", label: "Not satisfiable",
      teaser: "requests==2.22.0 requires idna<2.9, contradicting idna>=3.",
      sections: [
        ["Requirements", "<ul><li><code>idna&gt;=3</code></li><li><code>click==6.6</code></li><li><code>requests==2.22.0</code></li><li><code>pip-tools&lt;4.4.1</code></li></ul>"],
        ["Conflict", "<p><code>requests==2.22.0</code> requires <code>idna&lt;2.9</code>, which contradicts <code>idna&gt;=3</code>.</p>"],
        ["SMTpip result", "<p>Reports <strong>Not satisfiable</strong>.</p>"]
      ]
    },
    {
      title: "Framework illustration", tag: "Illustrative", status: "illus", label: "Illustrative",
      teaser: "Placeholder packages showing how a release is ruled out and when no solution exists.",
      sections: [
        ["Note", "<p>This scenario uses placeholder package names (<code>pkgA</code>, <code>pkgB</code>); it is not a real project.</p>"],
        ["Setup", "<p>The project requires <code>pkgA&gt;=2.0</code> and <code>pkgB==1.5</code>. Release <code>pkgA 2.0</code> requires <code>pkgB&gt;=1.0</code>, and <code>pkgA 2.1</code> requires <code>pkgB&gt;=1.6</code>.</p>"],
        ["Outcome", "<p><code>pkgA 2.1</code> is ruled out because it needs <code>pkgB&gt;=1.6</code>, so <code>pkgA 2.0</code> is chosen.</p>"],
        ["Unsatisfiable variant", "<p>Requiring <code>pkgA&gt;=2.1</code> and <code>pkgB==1.5</code> has no solution.</p>"]
      ]
    }
  ];

  var grid = document.getElementById("smt-grid");
  var overlay = document.getElementById("smt-overlay");
  var titleEl = document.getElementById("smt-modal-title");
  var badgeEl = document.getElementById("smt-modal-badge");
  var bodyEl = document.getElementById("smt-modal-body");
  var closeBtn = document.getElementById("smt-close");
  var lastFocus = null;

  scenarios.forEach(function (s, i) {
    var b = document.createElement("button");
    b.type = "button";
    b.className = "smt-tile";
    b.innerHTML =
      '<span class="smt-tile-num">Scenario ' + (i + 1) + ' · ' + s.tag + '</span>' +
      '<span class="smt-tile-title">' + s.title + '</span>' +
      '<span class="smt-badge ' + s.status + '">' + s.label + '</span>' +
      '<span class="smt-teaser">' + s.teaser + '</span>';
    b.addEventListener("click", function () { openModal(i); });
    grid.appendChild(b);
  });

  function openModal(i) {
    var s = scenarios[i];
    lastFocus = document.activeElement;
    titleEl.textContent = "Scenario " + (i + 1) + ": " + s.title;
    badgeEl.className = "smt-badge " + s.status;
    badgeEl.textContent = s.label;
    bodyEl.innerHTML = s.sections.map(function (sec) {
      return '<div class="smt-sec"><div class="smt-sec-label">' + sec[0] + '</div>' + sec[1] + '</div>';
    }).join("");
    overlay.classList.add("open");
    overlay.setAttribute("aria-hidden", "false");
    closeBtn.focus();
  }

  function closeModal() {
    overlay.classList.remove("open");
    overlay.setAttribute("aria-hidden", "true");
    if (lastFocus) { lastFocus.focus(); }
  }

  closeBtn.addEventListener("click", closeModal);
  overlay.addEventListener("click", function (e) { if (e.target === overlay) { closeModal(); } });
  document.addEventListener("keydown", function (e) { if (e.key === "Escape" && overlay.classList.contains("open")) { closeModal(); } });
})();
</script>

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
