---
layout: page
title: NEWS
permalink: /news/
nav: true
nav_order: 5
---

<div class="news">
  {% assign news = site.news | sort: 'date' | reverse %}
  {% if news.size > 0 %}
    {% for item in news %}
      <div class="row mb-3">
        <div class="col-sm-2 text-muted">{{ item.date | date: "%b %Y" }}</div>
        <div class="col-sm-10">
          {% if item.inline %}
            {{ item.content | remove: '<p>' | remove: '</p>' }}
          {% else %}
            <a class="news-title" href="{{ item.url | relative_url }}">{{ item.title }}</a>
          {% endif %}
        </div>
      </div>
    {% endfor %}
  {% else %}
    <p>No news so far.</p>
  {% endif %}
</div>
