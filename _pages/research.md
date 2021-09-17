---
layout: page
title: research
sorted_title: 02_research
permalink: /research/
description: My mission is to bring Safety and Resiliency to Dynamical Systems.
nav: true
display_categories: [research topics, funded projects, available student projects]
horizontal: false
---

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        <img class="img-fluid rounded" src="{{ '/assets/img/projects/research_topics_word_cloud.jpg' | relative_url }}" alt="" title="Research topics"/>
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
      <h2 class="category">some pictures from our lab</h2>

  <p class="post-content">Please check our <a href=" {{ "media" | relative_url }}">media page</a> to see some more photos and videos.</p>
  <div class="row">
    <div class="col-sm mt-3 mt-md-0">
        <img class="img-fluid rounded" src="{{ '/assets/img/projects/research_lab.jpg' | relative_url }}" alt="" title="Research in our lab"/>
    </div>
  </div>
</div>