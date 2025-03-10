---
layout: page
permalink: /alumni/
title: Alumni
nav: false
faculty_category: [Faculty]
display_categories: [Graduate Students, Undergraduates, High School Students]
alumni_categories: [ Master Students, Undergraduates]
horizontal: false
title_ignore: true
---

<!-- pages/projects.md -->
<div class="projects">
{%- if site.enable_project_categories and page.display_categories %}

  
  <!-- Display students in grid projects -->
  {%- for category in page.alumni_categories %}
  <h2 class="category">{{ category }}</h2>
  {%- assign categorized_projects = site.projects | where: "category", category -%}
      <!-- Further filter projects by status -->
  {%- assign filtered_projects = categorized_projects | where: "status", "inactive" -%}

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

{%- endif -%}
</div>




<!-- Customized code for undergrads 
<div class="projects"> ==$0



##### Undergrad


-->