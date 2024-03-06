---
layout: page
title: Wind Energy
description: reducing the cost of renewables by advanced control
img: /assets/img/projects/offshore_turbine_small.jpg
head_banner: /assets/img/offshore-wind-turbines-sunrise-1.jpeg
importance: 4
category: research topics
---


More than 90 GW of new wind power was installed in 2020, which accounts for a 53% growth compared to 2019 {% cite GWEC_2021 --file papers %}. Still, to meet the ambitious global plans for decarbonization, a growth of 180 GW per year would be required. This goal can be met by introducing larger turbines, especially in the offshore sector {% cite wiser2021expert --file papers %}. Such turbines will need to be lighter and more flexible, and this requires advanced control systems that can reduce structural loads. In particular, there is a need for optimal control schemes that can optimize the utilization of a wind turbine over its entire life cycle, taking into consideration power requirements from the grid, the accumulation of fatigue damage and the costs of maintenance, decomissioning or repowering at the end of the service life.

We are currently working on such control schemes as parts of our projects <a href=" {{ "projects/funded_projects/7_SUDOCO" | relative_url }}">SUDOCO</a>, <a href=" {{ "projects/funded_projects/8_TWAIN" | relative_url }}">TWAIN</a> and <a href=" {{ "projects/funded_projects/5_AIMWIND" | relative_url }}">AIMWIND</a>. Our results included fault tolerant control schemes {% cite Liu_2020ae --file my_papers %}, load reduction control at wind turbine level {% cite Liu_2021ab --file my_papers %}, improved wind speed estimation algorithms at rotor {% cite Liu_2021ad --file my_papers %} and blade level {% cite pamososuryo2023convex --file my_papers %}, and controllers for dynamic power derating and load balancing at wind farm level {% cite Gonzales-Silva_2021aa --file my_papers %}.

<span class="project--description">Joint work with (mostly)</span>: Bart Wolleswinkel, Ivo Van Straalen, Alex Gallo, Yichao Liu, Jean Gonzales Silva, Zhixin Feng, Atindryo Pamososuryo, Joeri Frederik, Sebastiaan Mulders.

## Publications

<div class="publications">
    {% bibliography -f my_papers -q @*[keywords ~= wind] %}
</div>

## Additional References

<div class="publications">
    {% bibliography -f papers --cited_in_order %}
</div>