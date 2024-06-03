---
layout: page
title: projects
permalink: /projects/
description: Some of my research, either from classes or independent work.
nav: true
nav_order: 3
display_categories: [work, fun]
horizontal: false
---

<!-- pages/projects.md -->
<div class="projects">
<!-- Static list of projects -->
<ul>
  <li><a href="https://evan-wang-13.github.io/assets/pdf/CompGPT.pdf">CompGPT: Probing the Compositional Understanding of Visual Language Models</a></li>
  <li><a href="https://evan-wang-13.github.io/assets/pdf/Interpretable_RL.pdf">Towards Interpretable Deep Reinforcement Learning: Extension and Limitations</a></li>
  <li><a href="https://evan-wang-13.github.io/assets/pdf/ExpBERT.pdf">Improving ExpBERT: Representation Engineering with GPT-Generated, Natural Language Explanations</a></li>
  <li><a href="https://evan-wang-13.github.io/assets/pdf/RacialBiasCaption.pdf">Exploring Racial Bias in Modern Image Captioning Systems/a></li>
  <!-- Add more projects as needed -->
</ul>

{% comment %}
Following code has been commented out to temporarily disable dynamic projects
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
    <div class="row row-cols-2">
    {% for project in sorted_projects %}
      {% include projects_horizontal.liquid %}
    {% endfor %}
    </div>
  </div>
  {% else %}
  <div class="grid">
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
    <div class="row row-cols-2">
    {% for project in sorted_projects %}
      {% include projects_horizontal.liquid %}
    {% endfor %}
    </div>
  </div>
  {% else %}
  <div class="grid">
    {% for project in sorted_projects %}
      {% include projects.liquid %}
    {% endfor %}
  </div>
  {% endif %}
{% endif %}

{% endcomment %}

</div>
