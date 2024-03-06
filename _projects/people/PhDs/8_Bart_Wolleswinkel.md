---
layout: page
title: Bart Wolleswinkel
description: PhD student on on cyber security
img: /assets/img/people/Bart.jpg
importance: 8
category: PhDs
---

<!-- NOTE: make the profile picture appear here as in my about page (copy the code for floating image) -->

<div class="row justify-content-sm-center">
    <div class="col-sm-8 mt-3 mt-md-0">
        <u>Period</u>: Mar. 2024 - Feb. 2028 (estimated).
        <br>
        <u>Topics</u>: Cyber attack detection, Event Triggered Control, Wind Farm Control.
        <br>
        <u>Projects</u>: <a href=" {{ "projects/funded_projects/7_8_TWAIN" | relative_url }}">TWAIN</a>.
    </div>
    <div class="col-sm-4 mt-3 mt-md-0">
        <img class="img-fluid rounded z-depth-1" src="{{ '/assets/img/people/Bart.jpg' | relative_url }}" alt="" title="example image"/>
    </div>
</div>


<!-- NOTE: add projects to everybody, with links to their page -->

## Publications

<div class="publications">
    {% bibliography -f my_papers -q @*[author ~= Wolleswinkel] %}
</div>

<!-- Find out how to search for complete author name, not just surname -->