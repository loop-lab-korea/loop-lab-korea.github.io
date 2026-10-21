---
layout: page
title: PEOPLE
permalink: /people/
nav: true
nav_order: 2
---

<link rel="stylesheet" href="{{ '/assets/css/loop.css' | relative_url }}">
## **Principal Investigator**

<div class="row">
  <div class="col-sm-4">
    {% include figure.liquid path="assets/img/pi-portrait.jpg" class="img-fluid rounded" %}
  </div>
  <div class="col-sm-8">
    <h3 class="mb-1"><b>김재상 (Jaesang Kim)</b></h3>
    <p class="pi-role">
      Assistant Professor · Graduate School of Data Science, Chonnam National University<br>
      <span class="pi-role-ko">조교수 · 전남대학교 데이터사이언스대학원 데이터사이언스학과</span><br>
      <a href="mailto:jsang@jnu.ac.kr">jsang@jnu.ac.kr</a>
    </p>

    <p class="pi-block">
      <b class="pi-label">Education</b>
      <b>Ph.D.</b> Mechanical Engineering, KAIST, <i>August 2024</i><br>
      <span class="pi-sub"><i>Three-dimensional musculoskeletal tissue engineering and
      its applications using organ-on-a-chip platform</i> · Advisor: Prof. Jessie S. Jeon</span><br>
      <b>M.S.</b> Mechanical Engineering, KAIST &nbsp;·&nbsp;
      <b>B.S.</b> Mechanical Engineering, KAIST, minor in Biological Sciences
    </p>

    <p class="pi-block">
      <b class="pi-label">Experience</b>
      <b>Postdoctoral Scholar</b>, Stanford University, <i>2026</i><br>
      <span class="pi-sub">Department of Cardiothoracic Surgery ·
      VA Palo Alto Health Care System</span>
    </p>

    <p class="pi-block">
      <b class="pi-label">Interests</b>
      Microphysiological systems, extracellular matrix mechanobiology, and machine
      learning for drug response.
    </p>

  </div>
</div>

---

## **Members**

{% comment %} 구성원 정보는 \_data/members.yml 에서 고친다. 이 아래는 건드릴 필요 없음. {% endcomment %}

<div class="row">
{%- for m in site.data.members %}
  <div class="col-md-6">
    <div class="member">
      {%- if m.photo %}
      <img class="member-photo" src="{{ '/assets/img/people/' | append: m.photo | relative_url }}" alt="{{ m.name_en }}" loading="lazy">
      {%- else %}
      {%- assign parts = m.name_en | split: " " %}
      <div class="member-photo member-photo-empty" aria-hidden="true">{{ parts.first | slice: 0 }}{% if parts.size > 1 %}{{ parts.last | slice: 0 }}{% endif %}</div>
      {%- endif %}
      <div class="member-body">
        <h3 class="member-name">{% if m.name_ko %}{{ m.name_ko }} ({{ m.name_en }}){% else %}{{ m.name_en }}{% endif %}</h3>
        <p class="member-role">{{ m.role }}{% if m.email %}<br><a href="mailto:{{ m.email }}">{{ m.email }}</a>{% endif %}</p>
        {%- if m.education %}
        <p class="member-block">
          <b class="pi-label">Education</b>
          {{ m.education | join: "<br>" }}
        </p>
        {%- endif %}
        {%- if m.interests %}
        <p class="member-block">
          <b class="pi-label">Interests</b>
          {{ m.interests }}
        </p>
        {%- endif %}
      </div>
    </div>
  </div>
{%- endfor %}
</div>

---

## **Join us**

We are recruiting **M.S. and Ph.D. students** and **undergraduate researchers**.
Backgrounds in mechanical engineering, life sciences, chemical engineering, computer
science and statistics are all suitable — the work moves between the bench and the
data, and you are not expected to arrive proficient in both.

Email <a href="mailto:jsang@jnu.ac.kr">jsang@jnu.ac.kr</a> and tell me what you have
been working on and what you would like to work on.

<sub>석·박사과정과 학부 인턴을 상시 모집합니다. 실험과 데이터 어느 쪽에서
출발하셔도 좋습니다.</sub>
