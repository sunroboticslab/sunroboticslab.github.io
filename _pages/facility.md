---
layout: page
title: Facilities
permalink: /facility/
nav: true
nav_order: 7
---

Our lab develops and uses robotic systems, customized devices, and shared equipment for research in soft robotics, actuation, sensing, control, and robot characterization. This page summarizes the main facilities currently available in the lab.

{% assign categories = "Robots and Devices,Customized Devices,Equipment and Capabilities" | split: "," %}

{% for category in categories %}
{% assign items = site.facilities | where: "category", category | sort: "importance" %}
{% if items.size > 0 %}
## {{ category }}

<div class="facility-grid">
{% for item in items %}
  <div class="facility-card">
    <img src="{{ item.image | relative_url }}" alt="{{ item.title }}">
    <h3>{{ item.title }}</h3>
    <p>{{ item.description }}</p>
    <p><a href="{{ item.url | relative_url }}">Read more</a></p>
    {% if item.external_link %}
    <p><a href="{{ item.external_link }}" target="_blank" rel="noopener">{{ item.external_link_text | default: "Detailed external site" }}</a></p>
    {% endif %}
  </div>
{% endfor %}
</div>
{% endif %}
{% endfor %}

<style>
.facility-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, 280px);
  justify-content: start;
  gap: 1.25rem;
  margin: 1rem 0 2rem;
}

.facility-card {
  width: 280px;
  border: 1px solid #e5e5e5;
  border-radius: 8px;
  padding: 1rem;
  background: #fff;
}

.facility-card img {
  width: 100%;
  height: 180px;
  object-fit: contain;
  background: #f8f8f8;
  border-radius: 6px;
  margin-bottom: 0.75rem;
  display: block;
}

.facility-card h3 {
  margin-top: 0;
  margin-bottom: 0.4rem;
}

.facility-card p {
  margin-bottom: 0.5rem;
}
</style>
