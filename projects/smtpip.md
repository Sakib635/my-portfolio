---
title: "SMTpip"
layout: default
permalink: /projects/smtpip/
---

<div style="text-align: center; margin: 4rem 0 0;">
  <h1 style="font-size: 3rem; margin-bottom: 0.5rem;">Projects</h1>
</div>

<style>
  .proj-tabs { display: flex; flex-wrap: wrap; justify-content: center; gap: 0.5rem; margin: 2rem 0 2.5rem; padding-bottom: 0.75rem; border-bottom: 1px solid rgba(127,127,127,.3); }
  .proj-tabs a { padding: 0.5rem 1.1rem; border-radius: 999px; border: 1px solid rgba(127,127,127,.35); text-decoration: none; font-weight: 600; color: inherit; transition: background .15s ease, transform .15s ease; }
  .proj-tabs a:hover, .proj-tabs a:focus-visible { background: rgba(127,127,127,.14); transform: translateY(-1px); outline: none; }
  .proj-tabs a.active { background: #3b82f6; border-color: #3b82f6; color: #fff; }
</style>
<nav class="proj-tabs" aria-label="Project navigation">
  <a href="{{ site.baseurl }}/projects/"{% if page.url == '/projects/' %} class="active" aria-current="page"{% endif %}>Overview</a>
  <a href="{{ site.baseurl }}/projects/smtpip/"{% if page.url == '/projects/smtpip/' %} class="active" aria-current="page"{% endif %}>SMTpip</a>
  <a href="{{ site.baseurl }}/projects/pyhealer/"{% if page.url == '/projects/pyhealer/' %} class="active" aria-current="page"{% endif %}>PyHealer</a>
  <a href="{{ site.baseurl }}/projects/vta-bot/"{% if page.url == '/projects/vta-bot/' %} class="active" aria-current="page"{% endif %}>VTA Bot</a>
</nav>

<style>
  .smt-page { --smt-accent: #3b82f6; --smt-card: rgba(127,127,127,.06); --smt-border: rgba(127,127,127,.3); max-width: 1000px; margin: 0 auto; }
  .smt-page section { margin-top: 3rem; }
  .smt-h { font-size: 1.5rem; margin: 0 0 0.35rem; }
  .smt-sub { margin: 0 0 1.25rem; opacity: .75; }
  .smt-hero { position: static; padding: 2rem; border: 1px solid var(--smt-border); border-radius: 18px; background: linear-gradient(135deg, rgba(59,130,246,.12), rgba(139,92,246,.08)); }
  .smt-eyebrow { font-size: 0.8rem; font-weight: 700; letter-spacing: .09em; text-transform: uppercase; color: var(--smt-accent); }
  .smt-title { font-size: 2.6rem; line-height: 1.1; margin: 0.35rem 0 0.4rem; }
  .smt-tagline { font-size: 1.2rem; font-weight: 600; margin: 0 0 1rem; }
  .smt-lead { font-size: 1.05rem; line-height: 1.65; margin: 0 0 1.25rem; max-width: 760px; }
  .smt-tags { display: flex; flex-wrap: wrap; gap: 0.5rem; margin-bottom: 1.5rem; }
  .smt-tag { font-size: 0.82rem; font-weight: 600; padding: 0.25rem 0.7rem; border-radius: 999px; border: 1px solid var(--smt-border); background: var(--smt-card); }
  .smt-actions { display: flex; flex-wrap: wrap; gap: 0.75rem; }
  .smt-btn { display: inline-flex; align-items: center; gap: 0.55rem; padding: 0.65rem 1.2rem; border-radius: 10px; border: 1px solid transparent; text-decoration: none; font-weight: 700; font-size: 0.98rem; color: #fff; transition: transform .15s ease, box-shadow .15s ease, filter .15s ease; }
  .smt-btn:hover, .smt-btn:focus-visible { transform: translateY(-2px); box-shadow: 0 8px 18px rgba(0,0,0,.25); filter: brightness(1.08); outline: none; color: #fff; }
  .smt-btn svg { width: 1.25rem; height: 1.25rem; fill: currentColor; flex: none; }
  .smt-btn.paper { background: #3b82f6; }
  .smt-btn.paper svg { fill: none; stroke: currentColor; stroke-width: 2; stroke-linecap: round; stroke-linejoin: round; }
  .smt-btn.github { background: #24292f; border-color: rgba(255,255,255,.15); }
  .smt-btn.youtube { background: #e5231a; }
  .smt-paper { display: flex; gap: 1.25rem; align-items: flex-start; padding: 1.5rem; border: 1px solid var(--smt-border); border-left: 5px solid var(--smt-accent); border-radius: 14px; background: var(--smt-card); }
  .smt-paper-label { font-size: 0.78rem; font-weight: 700; text-transform: uppercase; letter-spacing: .08em; opacity: .7; }
  .smt-paper-title { display: block; font-size: 1.2rem; line-height: 1.35; font-weight: 700; margin: 0.25rem 0 0.4rem; }
  .smt-paper-venue { margin: 0 0 1rem; opacity: .85; }
  .smt-video { position: relative; aspect-ratio: 16 / 9; width: 100%; border-radius: 14px; overflow: hidden; background: #000; border: 1px solid var(--smt-border); }
  .smt-video iframe, .smt-video-play { position: absolute; inset: 0; width: 100%; height: 100%; border: 0; }
  .smt-video-play { padding: 0; cursor: pointer; background: #000; }
  .smt-video-play img { width: 100%; height: 100%; object-fit: cover; opacity: .85; transition: opacity .2s ease, transform .3s ease; }
  .smt-video-play:hover img, .smt-video-play:focus-visible img { opacity: 1; transform: scale(1.02); }
  .smt-video-play:focus-visible { outline: 3px solid var(--smt-accent); outline-offset: -3px; }
  .smt-play-icon { position: absolute; left: 50%; top: 50%; width: 76px; height: 54px; margin: -27px 0 0 -38px; border-radius: 14px; background: #e5231a; display: flex; align-items: center; justify-content: center; box-shadow: 0 6px 20px rgba(0,0,0,.45); }
  .smt-play-icon svg { width: 26px; height: 26px; fill: #fff; margin-left: 3px; }
  .smt-flow { display: grid; grid-template-columns: repeat(auto-fit, minmax(240px, 1fr)); gap: 1rem; counter-reset: step; }
  .smt-step { position: relative; padding: 1.25rem 1.25rem 1.25rem 1.25rem; border: 1px solid var(--smt-border); border-radius: 14px; background: var(--smt-card); }
  .smt-step::before { counter-increment: step; content: counter(step); display: inline-flex; align-items: center; justify-content: center; width: 2rem; height: 2rem; margin-bottom: 0.6rem; border-radius: 50%; background: var(--smt-accent); color: #fff; font-weight: 700; }
  .smt-step h3 { margin: 0 0 0.35rem; font-size: 1.05rem; }
  .smt-step p { margin: 0; font-size: 0.95rem; line-height: 1.55; }
  .smt-fig { margin: 0; }
  .smt-fig img { max-width: 100%; height: auto; display: block; margin: 0 auto; border-radius: 12px; border: 1px solid var(--smt-border); }
  .smt-fig figcaption { text-align: center; font-size: 0.9rem; opacity: .75; margin-top: 0.6rem; }
  .smt-legend-btn { font: inherit; color: inherit; cursor: pointer; padding: 0.45rem 1rem; margin-bottom: 1.25rem; border: 1px dashed rgba(127,127,127,.6); border-radius: 999px; background: transparent; }
  .smt-legend-btn:hover, .smt-legend-btn:focus-visible { background: rgba(127,127,127,.12); outline: none; }
  .smt-grid { display: grid; grid-template-columns: repeat(auto-fit, minmax(220px, 1fr)); gap: 1rem; }
  .smt-tile { display: flex; flex-direction: column; text-align: left; font: inherit; color: inherit; cursor: pointer; padding: 1.1rem; border: 1px solid var(--smt-border); border-radius: 14px; background: var(--smt-card); transition: transform .18s ease, box-shadow .18s ease, border-color .18s ease; }
  .smt-tile:hover, .smt-tile:focus-visible { transform: translateY(-4px); box-shadow: 0 10px 24px rgba(0,0,0,.2); border-color: rgba(127,127,127,.7); outline: none; }
  .smt-tile-num { font-size: 0.78rem; opacity: .65; text-transform: uppercase; letter-spacing: .06em; }
  .smt-tile-title { display: block; font-size: 1.15rem; font-weight: 700; margin: 0.2rem 0 0.6rem; }
  .smt-tile-more { margin-top: auto; padding-top: 0.8rem; font-size: 0.85rem; font-weight: 600; color: var(--smt-accent); }
  .smt-teaser { display: block; max-height: 0; opacity: 0; overflow: hidden; font-size: 0.9rem; line-height: 1.5; transition: max-height .25s ease, opacity .25s ease, margin-top .25s ease; }
  .smt-tile:hover .smt-teaser, .smt-tile:focus-visible .smt-teaser { max-height: 9rem; opacity: .95; margin-top: 0.6rem; }
  .smt-badge { display: inline-block; font-size: 0.78rem; font-weight: 700; padding: 0.15rem 0.65rem; border-radius: 999px; }
  .smt-badge.ok { background: rgba(46,160,67,.18); color: #2a8a3e; }
  .smt-badge.unsat { background: rgba(207,34,46,.16); color: #c0262f; }
  .smt-badge.info { background: rgba(59,130,246,.16); color: #2563eb; }
  .smt-callout { margin-top: 1.5rem; padding: 1rem 1.25rem; border-radius: 12px; border: 1px solid var(--smt-border); border-left: 5px solid #f59e0b; background: rgba(245,158,11,.08); font-size: 0.95rem; line-height: 1.6; }
  .smt-callout p { margin: 0 0 0.4rem; }
  .smt-callout p:last-child { margin: 0; }
  .smt-overlay { position: fixed; inset: 0; z-index: 9999; display: none; align-items: center; justify-content: center; padding: 1rem; background: rgba(0,0,0,.6); }
  .smt-overlay.open { display: flex; }
  .smt-modal { position: relative; width: 100%; max-width: 740px; max-height: 90vh; overflow-y: auto; padding: 1.75rem; border-radius: 16px; background: #fff; color: #1f2328; box-shadow: 0 24px 60px rgba(0,0,0,.45); animation: smt-pop .18s ease; }
  @keyframes smt-pop { from { transform: scale(.96); opacity: 0; } to { transform: scale(1); opacity: 1; } }
  .smt-close { position: absolute; top: 0.6rem; right: 0.8rem; font-size: 1.7rem; line-height: 1; background: none; border: none; cursor: pointer; color: inherit; opacity: .7; }
  .smt-close:hover, .smt-close:focus-visible { opacity: 1; }
  .smt-modal h3 { margin: 0 0 0.5rem; padding-right: 2rem; }
  .smt-sec { margin-top: 1.2rem; }
  .smt-sec-label { font-size: 0.8rem; font-weight: 700; text-transform: uppercase; letter-spacing: .06em; opacity: .65; margin-bottom: 0.4rem; }
  .smt-sec p, .smt-sec ul { margin: 0 0 0.5rem; line-height: 1.6; }
  .smt-sec ul { padding-left: 1.2rem; }
  .smt-chips { display: flex; flex-wrap: wrap; gap: 0.5rem; }
  .smt-chip { font-family: monospace; font-size: 0.92rem; padding: 0.3rem 0.65rem; border-radius: 6px; border: 1px solid rgba(127,127,127,.4); background: rgba(127,127,127,.1); }
  .smt-clash { display: flex; flex-wrap: wrap; align-items: stretch; gap: 0.5rem; margin: 0.4rem 0 0.6rem; }
  .smt-clash-side { flex: 1 1 200px; padding: 0.65rem 0.8rem; border-radius: 10px; border: 1px solid rgba(127,127,127,.4); background: rgba(127,127,127,.08); font-size: 0.92rem; }
  .smt-clash-side b { display: block; font-size: 0.75rem; text-transform: uppercase; letter-spacing: .05em; opacity: .65; margin-bottom: 0.2rem; }
  .smt-clash-x { align-self: center; font-size: 1.5rem; font-weight: 700; color: #c0262f; }
  .smt-verdict { width: 100%; padding: 0.55rem 0.8rem; border-radius: 10px; background: rgba(207,34,46,.12); font-size: 0.93rem; line-height: 1.5; }
  .smt-outcome { margin-top: 1rem; padding: 0.65rem 0.9rem; border-radius: 10px; font-weight: 600; }
  .smt-outcome.ok { background: rgba(46,160,67,.15); }
  .smt-outcome.unsat { background: rgba(207,34,46,.14); }
  .smt-pager { display: flex; align-items: center; justify-content: space-between; gap: 0.75rem; margin-top: 1.5rem; padding-top: 1rem; border-top: 1px solid rgba(127,127,127,.3); }
  .smt-pager button { font: inherit; font-weight: 600; cursor: pointer; padding: 0.4rem 0.9rem; border-radius: 8px; border: 1px solid rgba(127,127,127,.45); background: transparent; color: inherit; }
  .smt-pager button:hover:not(:disabled), .smt-pager button:focus-visible { background: rgba(127,127,127,.15); outline: none; }
  .smt-pager button:disabled { opacity: .35; cursor: default; }
  .smt-pager span { font-size: 0.9rem; opacity: .7; }
  html.dark .smt-modal { background: #161b22; color: #e6edf3; box-shadow: 0 24px 60px rgba(0,0,0,.75); }
  html.dark .smt-badge.ok { color: #56d364; }
  html.dark .smt-badge.unsat { color: #ff7b72; }
  html.dark .smt-badge.info { color: #79c0ff; }
  html.dark .smt-clash-x { color: #ff7b72; }
  html.dark .smt-hero { background: linear-gradient(135deg, rgba(59,130,246,.2), rgba(139,92,246,.14)); }
  html.dark .smt-tile:hover, html.dark .smt-tile:focus-visible { box-shadow: 0 10px 24px rgba(0,0,0,.6); }
  html.dark .smt-btn.github { background: #30363d; }
  @media (max-width: 640px) {
    .smt-title { font-size: 2rem; }
    .smt-hero { padding: 1.25rem; }
    .smt-paper { flex-direction: column; }
  }
</style>

<div class="smt-page">
  <div class="smt-hero">
    <span class="smt-eyebrow">Research Project &middot; SCAM 2026</span>
    <h2 class="smt-title">SMTpip</h2>
    <p class="smt-tagline">Interpreter-Aware SMT-Based Dependency Conflict Resolution for Python</p>
    <p class="smt-lead">Prototype tool that translates Python dependency requirements into SMT constraints for optimal, conflict-free resolution &mdash; outperforming greedy pip in complex scenarios. Directly tied to thesis on better dependency ecosystems.</p>
    <div class="smt-tags">
      <span class="smt-tag">Python</span>
      <span class="smt-tag">SMT solvers (Z3)</span>
      <span class="smt-tag">PyPI API</span>
      <span class="smt-tag">Constraint satisfaction</span>
      <span class="smt-tag">Version modeling</span>
    </div>
    <div class="smt-actions">
      <a class="smt-btn paper" href="https://ieeexplore.ieee.org/abstract/document/11768862" target="_blank" rel="noopener">
        <svg viewBox="0 0 24 24" aria-hidden="true"><path d="M14 2H6a2 2 0 0 0-2 2v16a2 2 0 0 0 2 2h12a2 2 0 0 0 2-2V8z"/><path d="M14 2v6h6M8 13h8M8 17h8"/></svg>
        Read the Paper
      </a>
      <a class="smt-btn github" href="https://github.com/SMTpip" target="_blank" rel="noopener">
        <svg viewBox="0 0 16 16" aria-hidden="true"><path d="M8 0C3.58 0 0 3.58 0 8c0 3.54 2.29 6.53 5.47 7.59.4.07.55-.17.55-.38 0-.19-.01-.82-.01-1.49-2.01.37-2.53-.49-2.69-.94-.09-.23-.48-.94-.82-1.13-.28-.15-.68-.52-.01-.53.63-.01 1.08.58 1.23.82.72 1.21 1.87.87 2.33.66.07-.52.28-.87.51-1.07-1.78-.2-3.64-.89-3.64-3.95 0-.87.31-1.59.82-2.15-.08-.2-.36-1.02.08-2.12 0 0 .67-.21 2.2.82.64-.18 1.32-.27 2-.27.68 0 1.36.09 2 .27 1.53-1.04 2.2-.82 2.2-.82.44 1.1.16 1.92.08 2.12.51.56.82 1.27.82 2.15 0 3.07-1.87 3.75-3.65 3.95.29.25.54.73.54 1.48 0 1.07-.01 1.93-.01 2.2 0 .21.15.46.55.38A8.013 8.013 0 0 0 16 8c0-4.42-3.58-8-8-8z"/></svg>
        View on GitHub
      </a>
      <a class="smt-btn youtube" href="https://www.youtube.com/watch?v=KkNRGhvMwxw" target="_blank" rel="noopener">
        <svg viewBox="0 0 24 24" aria-hidden="true"><path d="M23.498 6.186a3.016 3.016 0 0 0-2.122-2.136C19.505 3.545 12 3.545 12 3.545s-7.505 0-9.377.505A3.017 3.017 0 0 0 .502 6.186C0 8.07 0 12 0 12s0 3.93.502 5.814a3.016 3.016 0 0 0 2.122 2.136c1.871.505 9.376.505 9.376.505s7.505 0 9.377-.505a3.015 3.015 0 0 0 2.122-2.136C24 15.93 24 12 24 12s0-3.93-.502-5.814zM9.545 15.568V8.432L15.818 12l-6.273 3.568z"/></svg>
        Watch the Demo
      </a>
    </div>
  </div>
  <section>
    <h2 class="smt-h">Publication</h2>
    <div class="smt-paper">
      <div>
        <span class="smt-paper-label">Main Paper</span>
        <span class="smt-paper-title">SMTpip: Interpreter-Aware SMT-Based Dependency Conflict Resolution for Restoring Python Source-Code Executability</span>
        <p class="smt-paper-venue">Presented at The 26th IEEE International Conference on Source Code Analysis and Manipulation (SCAM 2026)</p>
        <div class="smt-actions">
          <a class="smt-btn paper" href="https://ieeexplore.ieee.org/abstract/document/11768862" target="_blank" rel="noopener">
            <svg viewBox="0 0 24 24" aria-hidden="true"><path d="M14 2H6a2 2 0 0 0-2 2v16a2 2 0 0 0 2 2h12a2 2 0 0 0 2-2V8z"/><path d="M14 2v6h6M8 13h8M8 17h8"/></svg>
            IEEE Xplore
          </a>
        </div>
      </div>
    </div>
  </section>
  <section>
    <h2 class="smt-h">Demo</h2>
    <p class="smt-sub">Press play to watch SMTpip in action, or open the video on YouTube.</p>
    <div class="smt-video" id="smt-video">
      <button type="button" class="smt-video-play" id="smt-video-play" aria-label="Play the SMTpip demo video">
        <img src="https://img.youtube.com/vi/KkNRGhvMwxw/hqdefault.jpg" alt="SMTpip demo video thumbnail" loading="lazy">
        <span class="smt-play-icon"><svg viewBox="0 0 24 24" aria-hidden="true"><path d="M8 5v14l11-7z"/></svg></span>
      </button>
    </div>
  </section>
  <section>
    <h2 class="smt-h">How SMTpip Works</h2>
    <p class="smt-sub">From a requirements file to an installation plan, in three steps.</p>
    <div class="smt-flow">
      <div class="smt-step">
        <h3>Read the requirements</h3>
        <p>The input is a <code>requirements.txt</code> file listing package versions, for example <code>click==6.6</code> and <code>pip-tools&gt;=4.0.0</code>.</p>
      </div>
      <div class="smt-step">
        <h3>Solve as SMT constraints</h3>
        <p>SMTpip considers the requirements of all candidate releases together, rather than trying releases one after another as pip does when it backtracks.</p>
      </div>
      <div class="smt-step">
        <h3>Return a verdict</h3>
        <p>If a solution exists, SMTpip writes an installation plan to <code>install_script.txt</code>. Otherwise, it reports &ldquo;Not satisfiable&rdquo;.</p>
      </div>
    </div>
  </section>
  <section>
    <h2 class="smt-h">Architecture</h2>
    <figure class="smt-fig">
      <img src="{{ site.baseurl }}/assets/images/architecture.png" alt="SMTpip architecture overview" loading="lazy">
      <figcaption>Architecture overview of SMTpip.</figcaption>
    </figure>
  </section>
  <section>
    <h2 class="smt-h">Usage Scenarios</h2>
    <p class="smt-sub">SMTpip is illustrated on four projects. Hover over a scenario for a preview; click it for the requirements, the reason they conflict (or not), what pip does where reported, and what SMTpip returns.</p>
    <button type="button" class="smt-legend-btn" id="smt-legend-btn">How to read the requirements</button>
    <div class="smt-grid" id="smt-grid"></div>
    <div class="smt-callout">
      <p><strong>Resolution success is not execution success.</strong> Resolution success denotes that SMTpip produced a satisfiable installation plan; it does not imply that the project's source code executes successfully once installed.</p>
      <p>The explanations of the conflicts are derived from the dependency metadata of the packages; SMTpip itself reports the result.</p>
    </div>
  </section>
</div>

<div class="smt-overlay" id="smt-overlay" aria-hidden="true">
  <div class="smt-modal" role="dialog" aria-modal="true" aria-labelledby="smt-modal-title">
    <button class="smt-close" id="smt-close" type="button" aria-label="Close">&times;</button>
    <h3 id="smt-modal-title"></h3>
    <span class="smt-badge" id="smt-modal-badge"></span>
    <div id="smt-modal-body"></div>
    <div class="smt-pager" id="smt-pager">
      <button type="button" id="smt-prev">&larr; Previous</button>
      <span id="smt-count"></span>
      <button type="button" id="smt-next">Next &rarr;</button>
    </div>
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
  var pager = document.getElementById("smt-pager");
  var prevBtn = document.getElementById("smt-prev");
  var nextBtn = document.getElementById("smt-next");
  var countEl = document.getElementById("smt-count");
  var current = -1;
  var lastFocus = null;

  scenarios.forEach(function (s, i) {
    var b = document.createElement("button");
    b.type = "button";
    b.className = "smt-tile";
    b.innerHTML =
      '<span class="smt-tile-num">Example ' + (i + 1) + ' &middot; ' + s.tag + '</span>' +
      '<span class="smt-tile-title">' + s.title + '</span>' +
      '<span><span class="smt-badge ' + s.status + '">' + s.label + '</span></span>' +
      '<span class="smt-teaser">' + s.teaser + '</span>' +
      '<span class="smt-tile-more">View details &rarr;</span>';
    b.addEventListener("click", function () { openScenario(i); });
    grid.appendChild(b);
  });

  legendBtn.addEventListener("click", function () { render(legend, legend.title, -1); show(); });

  function render(s, heading, idx) {
    current = idx;
    titleEl.textContent = heading;
    badgeEl.className = "smt-badge " + s.status;
    badgeEl.textContent = s.label;
    var html = s.sections.map(function (sec) {
      return '<div class="smt-sec"><div class="smt-sec-label">' + sec[0] + '</div>' + sec[1] + '</div>';
    }).join("");
    if (s.outcome) { html += outcome(s.outcome[0], s.outcome[1]); }
    bodyEl.innerHTML = html;
    if (idx >= 0) {
      pager.style.display = "flex";
      prevBtn.disabled = idx === 0;
      nextBtn.disabled = idx === scenarios.length - 1;
      countEl.textContent = "Example " + (idx + 1) + " of " + scenarios.length;
    } else {
      pager.style.display = "none";
    }
    overlay.querySelector(".smt-modal").scrollTop = 0;
  }

  function openScenario(i) {
    render(scenarios[i], "Example " + (i + 1) + ": " + scenarios[i].title, i);
    show();
  }

  function show() {
    if (!overlay.classList.contains("open")) { lastFocus = document.activeElement; }
    overlay.classList.add("open");
    overlay.setAttribute("aria-hidden", "false");
    closeBtn.focus();
  }

  function closeModal() {
    overlay.classList.remove("open");
    overlay.setAttribute("aria-hidden", "true");
    if (lastFocus) { lastFocus.focus(); }
  }

  prevBtn.addEventListener("click", function () { if (current > 0) { openScenario(current - 1); } });
  nextBtn.addEventListener("click", function () { if (current >= 0 && current < scenarios.length - 1) { openScenario(current + 1); } });
  closeBtn.addEventListener("click", closeModal);
  overlay.addEventListener("click", function (e) { if (e.target === overlay) { closeModal(); } });
  document.addEventListener("keydown", function (e) {
    if (!overlay.classList.contains("open")) { return; }
    if (e.key === "Escape") { closeModal(); }
    else if (e.key === "ArrowLeft" && current > 0) { openScenario(current - 1); }
    else if (e.key === "ArrowRight" && current >= 0 && current < scenarios.length - 1) { openScenario(current + 1); }
  });

  var playBtn = document.getElementById("smt-video-play");
  playBtn.addEventListener("click", function () {
    var f = document.createElement("iframe");
    f.src = "https://www.youtube-nocookie.com/embed/KkNRGhvMwxw?autoplay=1&rel=0";
    f.title = "SMTpip demo video";
    f.allow = "autoplay; encrypted-media; picture-in-picture; fullscreen";
    f.allowFullscreen = true;
    playBtn.parentNode.replaceChild(f, playBtn);
  });
})();
</script>
