---
layout: page
permalink: /group/
title: Group
description: Members in Haiyun's Research Group 
nav: true
nav_order: 1
---

<!-- For now, this page is assumed to be a static description of your courses. You can convert it to a collection similar to `_projects/` so that you can have a dedicated page for each course.

Organize your courses by years, topics, or universities, however you like! -->

🌱 🌱 🌱  HH∞ Lab (tentative)

---

{% comment %}
Standardize roles in each person file:
  role: "PI" | "PhD Student" | "MPhil Student" | "RA"
Use `order:` in front matter to control the display order within each section.
Set `alumni: true` (and optionally years.end) for alumni.
{% endcomment %}

{%- assign current = site.group | where_exp: "p", "p.alumni != true" -%}

{% comment %}
## PI
<div class="row">
  {%- assign pi = current | where: "role", "PI" | sort: "order" -%}
  {%- for person in pi -%}
    {% include person-card.html person=person %}
  {%- endfor -%}
</div>

{% endcomment %}

## PhD Students
<div class="row">
  {%- assign phd = current | where: "role", "PhD Student" | sort: "order" -%}
  {%- for person in phd -%}
    {% include person-card.html person=person %}
  {%- endfor -%}
</div>

<!-- ---

## MPhil Students
<div class="row">
  {%- assign mphil = current | where: "role", "MPhil Student" | sort: "order" -%}
  {%- for person in mphil -%}
    {% include person-card.html person=person %}
  {%- endfor -%}
</div> -->

---

## Research Assistants
<div class="row">
  {%- assign ras = current | where: "role", "RA" | sort: "order" -%}
  {%- for person in ras -%}
    {% include person-card.html person=person %}
  {%- endfor -%}
</div>

<!-- ---

## Alumni
<div class="row">
  {%- assign alumni = site.group | where: "alumni", true | sort: "years.end" | reverse -%}
  {%- for person in alumni -%}
    {% include person-card.html person=person %}
  {%- endfor -%}
</div> -->