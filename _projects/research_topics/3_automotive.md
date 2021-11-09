---
layout: page
title: Automotive
description: electric and autonomous vehicles
img: /assets/img/projects/truck_Volvo.png
head_banner: /assets/img/Volvo_trucks_wide.jpg
importance: 3
category: research topics
---

The transportation sector currently account for 24% of the CO2 worldwide emissions {% cite Teter_2020bc --file papers %}, as well as 3.2 million <a href="https://www.unep.org/explore-topics/energy/what-we-do/transport" target="_blank">premature deaths</a>  due to pollution alone . Solutions to make the sector greenier, healthier and safer include, amongst other, the introduction of _electric_ and _autonomous_ vehicles. Fleets of road freight vehicles are ideal candidates for electrification and for early introduction of autonomous driving capabilities, including cooperative functionalities such as platooning.

We provided a first set of theoretical contributions to such pressing challenge, by developing detection methods that can make tomorrow's cooperative autonomous vehicles safer {% cite FKeijzer_2019aa Keijzer_2021ab --file my_papers %}.
As part of the project <a href=" {{ "projects/funded_projects/6_SPARSITY" | relative_url }}">SPARSITY</a>, in collaboration with AB Volvo, we are now investigating how to extend system identification and leverage physics-informed Machine Learning to obtain mathematical models of key electric drive train components. Such models will be instrumental in optimizing the life cycle of such components and implement circular economy solutions.


<span class="project--description">Joint work with (mostly)</span>: Twan Keijzer, Tushar Desai, Mahmood Mirzakhalili, Paula Chanfreut, José M. Maestre, Fabian Jarmolowitz, Kausihan Selvam.

## Publications

<div class="publications">
    {% bibliography -f my_papers -q @*[keywords ~= vehicles] %}
</div>

## Additional References

<div class="publications">
    {% bibliography -f papers --cited_in_order %}
</div>