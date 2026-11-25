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
  .smt-paper { margin: 1.25rem 0; padding: 1rem 1.25rem; border-left: 4px solid #3b82f6; border-radius: 8px; background: rgba(59,130,246,.08); }
  .smt-paper-label { font-size: 0.78rem; font-weight: 700; text-transform: uppercase; letter-spacing: .07em; opacity: .7; }
  .smt-paper-title { display: block; font-size: 1.1rem; font-weight: 700; margin: 0.2rem 0 0.35rem; }
  .smt-paper-venue { margin: 0 0 0.6rem; font-size: 0.95rem; }
  .smt-links { display: flex; flex-wrap: wrap; gap: 0.75rem; margin: 1rem 0 1.5rem; }
  .smt-links a { display: inline-block; padding: 0.5rem 1rem; border: 1px solid rgba(127,127,127,.4); border-radius: 999px; text-decoration: none; font-weight: 600; transition: transform .15s ease, box-shadow .15s ease; }
  .smt-links a:hover, .smt-links a:focus-visible { transform: translateY(-2px); box-shadow: 0 4px 12px rgba(0,0,0,.15); }
  .smt-links a.primary { background: #3b82f6; border-color: #3b82f6; color: #fff; }
  .smt-hint { font-size: 0.95rem; opacity: .75; margin: 0 0 1rem; }
  .smt-legend-btn { font: inherit; color: inherit; cursor: pointer; padding: 0.4rem 0.9rem; margin-bottom: 1rem; border: 1px dashed rgba(127,127,127,.6); border-radius: 999px; background: transparent; }
  .smt-legend-btn:hover, .smt-legend-btn:focus-visible { background: rgba(127,127,127,.12); outline: none; }
  .smt-grid { display: grid; grid-template-columns: repeat(auto-fit, minmax(220px, 1fr)); gap: 1rem; margin-bottom: 1.5rem; }
  .smt-tile { text-align: left; font: inherit; color: inherit; cursor: pointer; padding: 1rem; border: 1px solid rgba(127,127,127,.35); border-radius: 12px; background: rgba(127,127,127,.06); transition: transform .18s ease, box-shadow .18s ease, border-color .18s ease; }
  .smt-tile:hover, .smt-tile:focus-visible { transform: translateY(-4px); box-shadow: 0 8px 20px rgba(0,0,0,.18); border-color: rgba(127,127,127,.7); outline: none; }
  .smt-tile-num { font-size: 0.8rem; opacity: .65; text-transform: uppercase; letter-spacing: .06em; }
  .smt-tile-title { display: block; font-size: 1.1rem; font-weight: 700; margin: 0.15rem 0 0.5rem; }
  .smt-badge { display: inline-block; font-size: 0.78rem; font-weight: 700; padding: 0.15rem 0.6rem; border-radius: 999px; }
  .smt-badge.ok { background: rgba(46,160,67,.18); color: #2a8a3e; }
  .smt-badge.unsat { background: rgba(207,34,46,.16); color: #c0262f; }
  .smt-badge.info { background: rgba(59,130,246,.16); color: #2563eb; }
  .smt-teaser { display: block; max-height: 0; opacity: 0; overflow: hidden; font-size: 0.9rem; margin-top: 0; transition: max-height .25s ease, opacity .25s ease, margin-top .25s ease; }
  .smt-tile:hover .smt-teaser, .smt-tile:focus-visible .smt-teaser { max-height: 9rem; opacity: .9; margin-top: 0.6rem; }
  .smt-overlay { position: fixed; inset: 0; z-index: 9999; display: none; align-items: center; justify-content: center; padding: 1rem; background: rgba(0,0,0,.55); }
  .smt-overlay.open { display: flex; }
  .smt-modal { position: relative; width: 100%; max-width: 720px; max-height: 90vh; overflow-y: auto; padding: 1.75rem; border-radius: 14px; background: var(--bg, #fff); color: var(--text, #1f2328); box-shadow: 0 20px 50px rgba(0,0,0,.4); animation: smt-pop .18s ease; }
  @keyframes smt-pop { from { transform: scale(.96); opacity: 0; } to { transform: scale(1); opacity: 1; } }
  .smt-close { position: absolute; top: 0.6rem; right: 0.8rem; font-size: 1.6rem; line-height: 1; background: none; border: none; cursor: pointer; color: inherit; opacity: .7; }
  .smt-close:hover, .smt-close:focus-visible { opacity: 1; }
  .smt-modal h3 { margin: 0 0 0.4rem; }
  .smt-sec { margin-top: 1.1rem; }
  .smt-sec-label { font-size: 0.8rem; font-weight: 700; text-transform: uppercase; letter-spacing: .06em; opacity: .65; margin-bottom: 0.35rem; }
  .smt-sec p, .smt-sec ul { margin: 0 0 0.5rem; }
  .smt-sec ul { padding-left: 1.2rem; }
  .smt-chips { display: flex; flex-wrap: wrap; gap: 0.5rem; }
  .smt-chip { font-family: monospace; font-size: 0.9rem; padding: 0.25rem 0.6rem; border-radius: 6px; border: 1px solid rgba(127,127,127,.4); background: rgba(127,127,127,.1); }
  .smt-clash { display: flex; flex-wrap: wrap; align-items: stretch; gap: 0.5rem; margin: 0.4rem 0 0.6rem; }
  .smt-clash-side { flex: 1 1 200px; padding: 0.6rem 0.75rem; border-radius: 8px; border: 1px solid rgba(127,127,127,.4); background: rgba(127,127,127,.08); font-size: 0.9rem; }
  .smt-clash-side b { display: block; font-size: 0.75rem; text-transform: uppercase; letter-spacing: .05em; opacity: .65; margin-bottom: 0.15rem; }
  .smt-clash-x { align-self: center; font-size: 1.5rem; font-weight: 700; color: #c0262f; }
  .smt-verdict { width: 100%; padding: 0.5rem 0.75rem; border-radius: 8px; background: rgba(207,34,46,.12); color: inherit; font-size: 0.92rem; }
  .smt-outcome { margin-top: 0.9rem; padding: 0.55rem 0.8rem; border-radius: 8px; font-weight: 600; }
  .smt-outcome.ok { background: rgba(46,160,67,.15); }
  .smt-outcome.unsat { background: rgba(207,34,46,.14); }
  .smt-note { font-size: 0.9rem; opacity: .8; margin-top: 0.5rem; }
</style>

<div class="project-card" style="margin-bottom: 4rem;">
  <h2>SMTpip: Solver-Based Dependency Management for Python</h2>
  <p><strong>University of Windsor (M.Sc. Thesis component) | 2024 – 2025</strong></p>

  <div class="smt-paper">
    <span class="smt-paper-label">Main Paper</span>
    <span class="smt-paper-title">SMTpip: Interpreter-Aware SMT-Based Dependency Conflict Resolution for Restoring Python Source-Code Executability</span>
    <p class="smt-paper-venue">Presented at The 26th IEEE International Conference on Source Code Analysis and Manipulation (SCAM 2026)</p>
    <div class="smt-links" style="margin: 0;">
      <a class="primary" href="https://ieeexplore.ieee.org/abstract/document/11768862" target="_blank" rel="noopener">Read the Paper (IEEE Xplore)</a>
    </div>
  </div>

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

  <h3 style="margin-top: 2rem;">Usage Scenarios</h3>
  <p>
    SMTpip is illustrated on four projects. For each, we give the requirements, the reason they conflict (or not), what pip does where reported, and what SMTpip returns.
  </p>
  <button type="button" class="smt-legend-btn" id="smt-legend-btn">How to read the requirements</button>
  <p class="smt-hint">Hover over a scenario for a preview; click it for full details.</p>
  <div class="smt-grid" id="smt-grid"></div>
  <p class="smt-note">
    The explanations of the conflicts are derived from the dependency metadata of the packages; SMTpip itself reports the result. Resolution success denotes that SMTpip produced a satisfiable installation plan; it does not imply that the project's source code executes successfully once installed.
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
  function chips(list) {
    return '<div class="smt-chips">' + list.map(function (c) { return '<span class="smt-chip">' + c + '</span>'; }).join("") + '</div>';
  }
  function clash(a, b, verdict) {
    return '<div class="smt-clash">' +
      '<div class="smt-clash-side"><b>' + a[0] + '</b><code>' + a[1] + '</code></div>' +
      '<div class="smt-clash-x" aria-hidden="true">&#10007;</div>' +
      '<div class="smt-clash-side"><b>' + b[0] + '</b><code>' + b[1] + '</code></div>' +
      '<div class="smt-verdict">' + verdict + '</div></div>';
  }
  function outcome(kind, text) {
    return '<div class="smt-outcome ' + kind + '">' + text + '</div>';
  }
  var UNSAT_MEANING = "In this example, no set of package versions satisfies all requirements, so no installation plan exists and the developer must change at least one requirement.";

  var legend = {
    title: "How to read the requirements",
    status: "info", label: "Guide",
    sections: [
      ["Notation used in requirements.txt", "<ul>" +
        "<li><code>pkg==1.2</code>: exactly version 1.2</li>" +
        "<li><code>pkg&gt;=1.2</code>: version 1.2 or later</li>" +
        "<li><code>pkg&lt;=1.2</code> and <code>pkg&lt;1.2</code>: set an upper bound (at most 1.2, and strictly below 1.2, respectively)</li>" +
        "<li><code>pkg==2.*</code>: any 2.x release</li></ul>"],
      ["What the scenarios show", "<p>Each scenario lists the requirements, explains why they conflict (or not), describes what pip does where reported, and states what SMTpip returns.</p>"]
    ]
  };

  var scenarios = [
    {
      title: "fflpy", tag: "Issue #1", status: "ok", label: "A solution exists",
      teaser: "click is fixed at 6.6, so newer pip-tools releases are excluded; SMTpip selects pip-tools==4.4.0.",
      sections: [
        ["Requirements", chips(["click==6.6", "pip-tools&gt;=4.0.0"])],
        ["Why they conflict", clash(["Project requires", "click==6.6"], ["pip-tools 7.4.1 requires", "click&gt;=8.0"], "Because the project fixes click at exactly 6.6, which is lower than 8.0, the newest pip-tools releases (such as 7.4.1) cannot be installed with it.")],
        ["With pip", "<p>pip first selects <code>click==6.6</code> and the latest <code>pip-tools</code>, finds the conflict, and then tries earlier <code>pip-tools</code> releases one after another until it reaches 4.4.0.</p>"],
        ["With SMTpip", "<p>The developer runs <code>python SMTpip.py -d &lt;project&gt;</code>. SMTpip considers the requirements of all <code>pip-tools</code> releases together and selects <code>pip-tools==4.4.0</code>, the latest release compatible with <code>click==6.6</code>.</p><p>It writes the versions to <code>install_script.txt</code>, which the developer runs to create the environment.</p>"]
      ],
      outcome: ["ok", "Result: <code>click==6.6</code> and <code>pip-tools==4.4.0</code>, with an installation plan in <code>install_script.txt</code>."]
    },
    {
      title: "ltiauthenticator", tag: "Real project", status: "ok", label: "A solution exists",
      teaser: "oauthlib is limited to 2.x, so recent JupyterHub releases are excluded; SMTpip selects jupyterhub==0.9.1.",
      sections: [
        ["Requirements", chips(["oauthlib==2.*", "jupyterhub&gt;=0.8"])],
        ["Why they conflict", clash(["Project allows", "oauthlib==2.* (any 2.x release)"], ["Recent JupyterHub requires", "oauthlib&gt;=3.0"], "The project allows only oauthlib 2.x, which never reaches 3.0, so recent JupyterHub releases cannot be used.")],
        ["With SMTpip", "<p>SMTpip selects the older release <code>jupyterhub==0.9.1</code> together with an <code>oauthlib</code> 2.x release and generates an installation plan.</p>"]
      ],
      outcome: ["ok", "Result: <code>jupyterhub==0.9.1</code> with an <code>oauthlib</code> 2.x release, and an installation plan."]
    },
    {
      title: "AutoGPT", tag: "Real project", status: "unsat", label: "No solution",
      teaser: "googlesearch_python==1.1.0 caps requests at 2.25.1, below the required minimum of 2.26.0.",
      sections: [
        ["Requirements", chips(["requests&gt;=2.26.0", "googlesearch_python==1.1.0"])],
        ["Why they conflict", clash(["Project requires", "requests&gt;=2.26.0"], ["googlesearch_python 1.1.0 requires", "requests&lt;=2.25.1"], "No version of requests can be both at least 2.26.0 and at most 2.25.1, so no version satisfies both.")],
        ["With SMTpip", "<p>SMTpip reports <strong>&ldquo;Not satisfiable&rdquo;</strong>.</p>"],
        ["What &ldquo;Not satisfiable&rdquo; means", "<p>" + UNSAT_MEANING + "</p>"]
      ],
      outcome: ["unsat", "Result: Not satisfiable. The developer must change at least one requirement."]
    },
    {
      title: "Constructed project", tag: "Constructed example", status: "unsat", label: "No solution",
      teaser: "requests==2.22.0 requires idna<2.9, which contradicts idna>=3.",
      sections: [
        ["Requirements", chips(["idna&gt;=3", "click==6.6", "requests==2.22.0", "pip-tools&lt;4.4.1"])],
        ["Why they conflict", clash(["Project requires", "idna&gt;=3"], ["requests 2.22.0 requires", "idna&lt;2.9"], "These two requirements alone cannot both hold: no version of idna is both at least 3 and below 2.9.")],
        ["With SMTpip", "<p>SMTpip reports <strong>&ldquo;Not satisfiable&rdquo;</strong>.</p>"],
        ["What &ldquo;Not satisfiable&rdquo; means", "<p>" + UNSAT_MEANING + "</p>"]
      ],
      outcome: ["unsat", "Result: Not satisfiable. The developer must change at least one requirement."]
    }
  ];

  var grid = document.getElementById("smt-grid");
  var overlay = document.getElementById("smt-overlay");
  var titleEl = document.getElementById("smt-modal-title");
  var badgeEl = document.getElementById("smt-modal-badge");
  var bodyEl = document.getElementById("smt-modal-body");
  var closeBtn = document.getElementById("smt-close");
  var legendBtn = document.getElementById("smt-legend-btn");
  var lastFocus = null;

  scenarios.forEach(function (s, i) {
    var b = document.createElement("button");
    b.type = "button";
    b.className = "smt-tile";
    b.innerHTML =
      '<span class="smt-tile-num">Example ' + (i + 1) + ' · ' + s.tag + '</span>' +
      '<span class="smt-tile-title">' + s.title + '</span>' +
      '<span class="smt-badge ' + s.status + '">' + s.label + '</span>' +
      '<span class="smt-teaser">' + s.teaser + '</span>';
    b.addEventListener("click", function () { openModal(s, "Example " + (i + 1) + ": " + s.title); });
    grid.appendChild(b);
  });

  legendBtn.addEventListener("click", function () { openModal(legend, legend.title); });

  function openModal(s, heading) {
    lastFocus = document.activeElement;
    titleEl.textContent = heading;
    badgeEl.className = "smt-badge " + s.status;
    badgeEl.textContent = s.label;
    var html = s.sections.map(function (sec) {
      return '<div class="smt-sec"><div class="smt-sec-label">' + sec[0] + '</div>' + sec[1] + '</div>';
    }).join("");
    if (s.outcome) { html += outcome(s.outcome[0], s.outcome[1]); }
    bodyEl.innerHTML = html;
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
