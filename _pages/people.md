---
layout: page
title: People
permalink: /people/
nav: true
nav_order: 2
faculty_category: [Faculty]
display_categories: [Graduate Students, Undergraduates]
alumni_categories: [ Master Students, Undergraduates]
horizontal: false
title_ignore: true
---

<!-- pages/projects.md -->
<div class="projects">
{%- if site.enable_project_categories and page.display_categories %}

  <!-- Display Faculty with projects -->
  {%- for category in page.faculty_category %}
  <h2 class="category">{{ category }}</h2>
  {%- assign categorized_projects = site.projects | where: "category", category -%}
  {%- assign sorted_projects = categorized_projects | sort: "importance" %}
  <!-- Generate cards for each project -->

  <div class="container">
    <div class="row row-cols-1">
    {%- for project in sorted_projects -%}
      {% include projects_horizontal.html %}
    {%- endfor %}
    </div>
  </div>

  {% endfor %}

  <!-- Display students in grid projects -->
  {%- for category in page.display_categories %}
  <h2 class="category">{{ category }}</h2>
  {%- assign categorized_projects = site.projects | where: "category", category -%}
      <!-- Further filter projects by status -->
  {%- assign filtered_projects = categorized_projects | where: "status", "active" -%}

  {%- assign sorted_projects = filtered_projects | sort: "importance" %}
  <!-- Generate cards for each project -->
  {% if page.horizontal -%}
  <div class="container">
    <div class="row row-cols-1">
    {%- for project in sorted_projects -%}
      {% include projects_horizontal.html %}
    {%- endfor %}
    </div>
  </div>
  {%- else -%}
  <div class="grid">
    {%- for project in sorted_projects -%}
      {% include projects.html %}
    {%- endfor %}
  </div>
  {%- endif -%}
  {% endfor %}

<h2 class="category">Alumni</h2>

  <!-- Display Alumni students in grid projects -->
  {%- for category in page.alumni_categories %}

  <h5 class="category">{{ category }}</h5>
  {%- assign categorized_projects = site.projects | where: "category", category -%}
    <!-- Further filter projects by status -->
  {%- assign filtered_projects = categorized_projects | where: "status", "inactive" -%}

  {%- assign sorted_projects = filtered_projects | sort: "importance" %}
  <!-- Generate cards for each project -->

  <div class="grid">
    {%- for project in sorted_projects -%}
      {% include projects_alumni.html %}
    {%- endfor %}
  </div>
  {% endfor %}

{%- else -%}
<!-- Display projects without categories -->
  {%- assign sorted_projects = site.projects | sort: "importance" -%}
  <!-- Generate cards for each project -->
  {% if page.horizontal -%}
  <div class="container">
    <div class="row row-cols-2">
    {%- for project in sorted_projects -%}
      {% include projects_horizontal.html %}
    {%- endfor %}
    </div>
  </div>
  {%- else -%}
  <div class="grid">
    {%- for project in sorted_projects -%}
      {% include projects.html %}
    {%- endfor %}
  </div>
  {%- endif -%}
{%- endif -%}
</div>




<!-- Customized code for undergrads 
<div class="projects"> ==$0



##### Undergrad


-->