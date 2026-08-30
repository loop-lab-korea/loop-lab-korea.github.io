---
layout: page
title: PUBLICATIONS
permalink: /publications/
description: Peer-reviewed publications, patents and presentations.
nav: true
nav_order: 4
years: [2026, 2025, 2024, 2022, 2021, 2018]
---

<!-- Grouped by year. Entries come from _bibliography/papers.bib -->
<div class="publications">
{% for y in page.years %}
  <h2 class="year">{{ y }}</h2>
  {% bibliography -f papers -q @*[year={{ y }}]* %}
{% endfor %}
</div>

---

## Patents and Presentations

<div class="publications">
{% bibliography -f patents_talks %}
</div>
