---
layout: page
title: PUBLICATIONS
permalink: /publications/
description: Peer-reviewed publications, patents and presentations.
nav: true
nav_order: 4
---

<link rel="stylesheet" href="{{ '/assets/css/loop.css' | relative_url }}">

<div class="publications">
{% bibliography -f papers %}
</div>

<h2 class="mt-5">Patents and Presentations</h2>

<div class="publications no-thumbs">
{% bibliography -f patents_talks %}
</div>
