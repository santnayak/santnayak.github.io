---
layout: default
title: Projects
---
<header class="page-heading"><p class="eyebrow">Things I’m building</p><h1>Projects & experiments<span class="accent">.</span></h1><p class="lede">Practical tools, curious experiments, and the systems behind them.</p></header>
<div class="project-grid">{% for project in site.data.projects %}{% include project.html project=project %}{% endfor %}</div>
<p class="closing-note">More code and experiments on <a href="https://github.com/santnayak">GitHub ↗</a></p>
