---
layout: default
title: Blog
---
<header class="page-heading"><p class="eyebrow">A new home for these notes</p><h1>The blog is now the journal.</h1><p class="lede">Technical writing and future weekly notes, together in one place.</p><a class="button" href="{{ '/journal/' | relative_url }}">Visit the journal →</a></header>
<div class="entry-list">{% for post in site.posts %}{% include entry.html post=post %}{% endfor %}</div>
