---
layout: page
title: NEWS
permalink: /news/
nav: true
nav_order: 5
---

<div class="news">
  {% if site.news != blank -%}
    {% assign news = site.news | sort: 'date' | reverse %}
    {% for item in news %}
      <div class="row">
        <div class="col-sm-2 text-muted">{{ item.date | date: "%b %d, %Y" }}</div>
        <div class="col-sm-10">
          {% if item.inline -%}
            {{ item.content | remove: '<p>' | remove: '</p>' }}
          {%- else -%}
            <a class="news-title" href="{{ item.url | relative_url }}">{{ item.title }}</a>
          {%- endif %}
        </div>
      </div>
    {% endfor %}
  {% else -%}
    <p>No news so far.</p>
  {%- endif %}
</div>