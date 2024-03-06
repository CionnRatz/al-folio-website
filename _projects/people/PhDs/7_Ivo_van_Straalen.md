---
layout: page
title: Ivo van Straalen
description: PhD student on cyber security
img: /assets/img/people/Ivo.jpg
importance: 7
category: PhDs
---

<!-- NOTE: make the profile picture appear here as in my about page (copy the code for floating image) -->

<div class="row justify-content-sm-center">
    <div class="col-sm-8 mt-3 mt-md-0">
        <u>Period</u>: Jan. 2024 - Dec. 2027 (estimated).
        <br>
        <u>Topics</u>: Cyber attack detection, Event Triggered Control, Wind Farm Control.
        <br>
        <u>Projects</u>: <a href=" {{ "projects/funded_projects/7_SUDOCO" | relative_url }}">SUDOCO</a>.
    </div>
    <div class="col-sm-4 mt-3 mt-md-0">
        <img class="img-fluid rounded z-depth-1" src="{{ '/assets/img/people/Ivo.jpg' | relative_url }}" alt="" title="example image"/>
    </div>
</div>


<!-- NOTE: add projects to everybody, with links to their page -->

## Publications

<div class="publications">
    {% bibliography -f my_papers -q @*[author ~= Straalen] %}
</div>

<!-- Find out how to search for complete author name, not just surname -->