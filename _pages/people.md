---
layout: page
title: People
permalink: /people/
nav: true
nav_order: 2
faculty_category: [Faculty]
display_categories: [Graduate Students, Undergraduates, High School Students]
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
      {% include people_horizontal.html %}
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
      {% include people_horizontal.html %}
    {%- endfor %}
    </div>
  </div>
  {%- else -%}
  <div class="grid">
    {%- for project in sorted_projects -%}
      {% include people_card.html %} <!--UPDATED: projects.html to people_card.html-->
    {%- endfor %}
  </div>
  {%- endif -%}
  {% endfor %}

  {%- endif -%}

<h2 class="category">
  <a href="{{ '/alumni/' | relative_url }}">Alumni --> </a>
</h2>


<!-- <h3><a href="{{ '/alumni/' | relative_url }}" style="color: inherit;padding-top:5rem">Alumni -></a></h3> -->
</div>

 <!-- <a class="news-title" href="{{ item.url | relative_url }}">{{ item.title }}</a> -->


<!-- Customized code for undergrads 
<div class="projects"> ==$0



##### Undergrad


-->