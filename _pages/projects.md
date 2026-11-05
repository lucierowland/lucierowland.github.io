---
layout: page
title: Research
permalink: /research/
description: 
nav: true
nav_order: 3
display_categories: [The Distant Giants, The Local Dwarves]
horizontal: false
social: true # 
---


My research focuses on understanding how galaxies form and evolve, particularly during the first billion years of cosmic history. I am interested in how the earliest galaxies assembled their stars and gas, became enriched with heavy elements and dust, and developed the structures and dynamics we observe in galaxies today.

To investigate these processes, I combine observations from the **James Webb Space Telescope (JWST)** and the **Atacama Large Millimeter/submillimeter Array (ALMA)**, studying the physical conditions, chemical enrichment, and kinematics of galaxies in the early Universe. I am particularly interested in what these observations can tell us about the surprisingly rapid evolution of massive galaxies at high redshift.

My research also extends to nearby galaxies, where spatially resolved observations allow us to investigate star formation, stellar feedback, and the interstellar medium in greater detail. By studying galaxies across cosmic time, I aim to better understand the physical processes that drive their formation and evolution.



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
    <div class="row row-cols-1 row-cols-md-1">
    {% for project in sorted_projects %}
      {% include projects_horizontal.liquid %}
    {% endfor %}
    </div>
  </div>
  {% else %}
  <div class="row row-cols-1 row-cols-md-2">
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
