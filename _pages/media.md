---
layout: page
title: media
sorted_title: 05_media
permalink: /media/
description: Pictures and videos from the lab, conferences and from outreach events.
nav: true
display_categories: [talks, lab, team and funnies]
horizontal: false
---

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        <img class="img-fluid rounded" src="{{ '/assets/img/projects/research_topics_word_cloud.jpg' | relative_url }}" alt="" title="Research topics"/>
    </div>
</div>

<!-- NOTE: add caption of image, possibly give credits. -->

<p>
<div>
On this page you can read about my <a href="#research topics">research topics</a>, my <a href="#funded projects">funded projects</a>, my <a href="#past projects">past projects</a> and <a href="#available student projects">available student projects</a>.
</div>

<div class="projects">
  {% if site.enable_project_categories and page.display_categories %}
  <!-- Display categorized projects -->
    {% for category in page.display_categories %}
      <section id="{{category}}">
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
      </section>
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


