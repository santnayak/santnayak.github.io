---
layout: default
title: Home
---
<section class="hero">
  <p class="eyebrow"><span class="status-dot"></span> An engineer’s personal notebook</p>
  <h1>Building systems.<br>Making sense of <span>what’s next.</span></h1>
  <p class="hero-intro">Hi, I’m <strong>Santhosh.</strong> I design and build backend and distributed systems, with a focus on AI agents, observability, and security-first architecture.</p>
  <p class="hero-note">A place for things I’m building, ideas I’m exploring, and notes from life along the way.</p>
  <div class="hero-links"><a class="button" href="{{ '/projects/' | relative_url }}">Explore my work <span aria-hidden="true">↗</span></a><a class="text-link" href="{{ '/journal/' | relative_url }}">Read the journal →</a></div>
  <div class="hero-code" aria-hidden="true"><span>01 /</span> build · observe · learn · repeat</div>
</section>
<section class="home-section" aria-labelledby="working-title">
  <div class="section-heading"><div><p class="eyebrow">01 / In progress</p><h2 id="working-title">What I’m working on</h2></div><a class="text-link" href="{{ '/projects/' | relative_url }}">All projects ↗</a></div>
  <div class="project-grid">{% for project in site.data.projects limit:2 %}{% include project.html project=project %}{% endfor %}</div>
  <div class="now-note"><span class="eyebrow">Also exploring</span><p>Context health metrics, LLM evaluation, and how to make AI systems debuggable by default.</p></div>
</section>
<section class="home-section" aria-labelledby="journal-title">
  <div class="section-heading"><div><p class="eyebrow">02 / Field notes</p><h2 id="journal-title">The journal</h2></div><a class="text-link" href="{{ '/journal/' | relative_url }}">All entries ↗</a></div>
  <p class="section-intro">Technical deep dives today. Weekly notes on work, life, and everything in between to come.</p>
  <div class="entry-list">{% for post in site.posts limit:3 %}{% include entry.html post=post %}{% endfor %}</div>
</section>
