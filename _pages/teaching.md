---
layout: page
title: Teaching
permalink: /teaching/
description: Here is a list of the courses that I taught in the past or I am currently teaching.
nav: true
nav_order: 3
display_categories: [University of Oklahoma (Summer 24), University of Oklahoma (Winter 23-24), University of Oklahoma (Summer 23)]
horizontal: false
---

<!-- pages/projects.md -->
<div class="projects">
{% if site.enable_project_categories and page.display_categories %}
  <!-- Display categorized projects -->
  {% for category in page.display_categories %}
  <a id="{{ category }}" href=".#{{ category }}">
    <h2 class="category">{{ category }}</h2>
  </a>
  {% assign categorized_projects = site.projects | where: "category", category %}
  {% assign sorted_projects = categorized_projects | sort: "importance" %}
  <!-- Generate cards for each project -->
  {% if page.horizontal %}
  <div class="container">
    <div class="row row-cols-1 row-cols-md-2">
    {% for project in sorted_projects %}
      {% include projects_horizontal.liquid %}
    {% endfor %}
    </div>
  </div>
  {% else %}
  <div class="row row-cols-1 row-cols-md-3">
    {% for project in sorted_projects %}
      {% include projects.liquid %}
    {% endfor %}
  </div>
  {% endif %}
  {% endfor %}

{% else %}

<!-- Display projects without categories -->

{% assign sorted_projects = site.projects | sort: "importance" %}

  <!-- Generate cards for each project -->

{% if page.horizontal %}

  <div class="container">
    <div class="row row-cols-1 row-cols-md-2">
    {% for project in sorted_projects %}
      {% include projects_horizontal.liquid %}
    {% endfor %}
    </div>
  </div>
  {% else %}
  <div class="row row-cols-1 row-cols-md-3">
    {% for project in sorted_projects %}
      {% include projects.liquid %}
    {% endfor %}
  </div>
  {% endif %}
{% endif %}
</div>


---

### Teaching Assistant (University of Oklahoma)

***Fall 2025 for Dr. Ibrahim Kekec***
+ ECON 5213-001 Advanced Econometrics
+ ECON 5283-999 Data Visualization With Python
+ ECON 5023-001 Statistics for Decision Making
+ ECON 1113-003 Principles of Macroeconomics

***Spring 2025 for Dr. Ibrahim Kekec***
+ ECON 4223-001 Econometric Analysis
+ ECON 5043-001 Managerial Economics II
+ ECON 1113-005 Principles of Macroeconomics

***Fall 2024 for Dr. Ibrahim Kekec***
+ ECON 5213-001 Advanced Econometrics
+ ECON 5023-001 Statistics for Decision Making

***Spring 2024 for Prof. Cynthia Rogers***
+ ECON 4353-001 Public Finance
+ ECON 4983-001 Economics as Social Science

***Spring 2023 for Dr. Brent Norwood***
+ ECON 1113-002 Principles of Economics-Macro

***Fall 2022 for Asst. Prof. Jayash Paudel***
+ ECON 3213-001 & 002 Environmental Economics

***Fall 2022 for Asst. Prof. Mu-Jeung Yang***
+ ECON 4970-001 Economics of Capital Markets

***Spring 2022 for Dr. Samantha Johnson***
+ ECON 1123-004 Principles of Economics-Micro

***Fall 2021 for Asst. Prof. Kevin Kuruc***
+ ECON 1113-002 & 003 Principles of Economics-Macro

