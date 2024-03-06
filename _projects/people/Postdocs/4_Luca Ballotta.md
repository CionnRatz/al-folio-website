---
layout: page
title: Luca Ballotta
description: Postdoc on security of distributed systems
img: /assets/img/people/Luca.jpg
importance: 4
category: Postdocs
---

<!-- NOTE: make the profile picture appear here as in my about page (copy the code for floating image) -->

<div class="row justify-content-sm-center">
    <div class="col-sm-8 mt-3 mt-md-0">
        <u>Period</u>: Dec. 2023 - current
        <br>
        <u>Topics</u>: control of distributed systems, security and fault diagnosis.
        <u>Projects</u>: <a href=" {{ "projects/funded_projects/8_TWAIN" | relative_url }}">TWAIN</a>.
    </div>
    <div class="col-sm-4 mt-3 mt-md-0">
        <img class="img-fluid rounded z-depth-1" src="{{ '/assets/img/people/Luca.jpg' | relative_url }}" alt="" title="example image"/>
    </div>
</div>




<!-- NOTE: add projects to everybody, with links to their page -->

## Publications

<div class="publications">
    {% bibliography -f my_papers -q @*[author ~= Ballotta] %}
</div>

<!-- Find out how to search for complete author name, not just surname -->