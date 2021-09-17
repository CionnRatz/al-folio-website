---
layout: page
title: people
sorted_title: 03_people
permalink: /people/
description: The greatest asset in our lab.
nav: true
display_categories: [PhDs, Postdocs, former PhDs]
horizontal: false
---

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        <img class="img-fluid rounded" src="{{ '/assets/img/people/research_group.jpg' | relative_url }}" alt="" title="Research group"/>
    </div>
</div>

<div class="projects">
  {% if site.enable_project_categories and page.display_categories %}
  <!-- Display categorized projects -->
    {% for category in page.display_categories %}
      <h2 class="category">{{category}}</h2>
      {% assign categorized_projects = site.projects | where: "category", category %}
      {% assign sorted_projects = categorized_projects | sort: "importance" %}
      <!-- Generate cards for each project -->
      {% if page.horizontal %}
        <div class="container">
          <div class="row row-cols-2">
          {% for project in sorted_projects %}
            {% include projects_horizontal.html %}
          {% endfor %}
          </div>
        </div>
      {% else %}
        <div class="grid">
          {% for project in sorted_projects %}
            {% include projects.html %}
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
          {% include projects_horizontal.html %}
        {% endfor %}
        </div>
      </div>
    {% else %}
      <div class="grid">
        {% for project in sorted_projects %}
          {% include projects.html %}
        {% endfor %}
      </div>
    {% endif %}

  {% endif %}

</div>

<div class="projects">
      <h2 class="category">come visit us!</h2>
  <div class="row">
      <div class="col-sm mt-3 mt-md-0">
          <img class="img-fluid rounded" src="{{ '/assets/img/people/research_group_beers.jpg' | relative_url }}" alt="" title="Research group toasting"/>
      </div>
  </div>
</div>