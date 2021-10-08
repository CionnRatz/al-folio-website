---
layout: page
title: fault diagnosis
description: from deterministic to probabilistic
img: /assets/img/projects/1_fault_diagnosis/failing_wind_turbine.jpg
head_banner: /assets/img/projects/1_fault_diagnosis/failing_wind_turbine.jpg
importance: 1
category: research topics
---

<!-- <span class="project--description">Summary</span>: one/two sentences. Link to [why this is important](#motivation) and what is the [state of the art](#state-of-the-art) of the research on it, [how we are contributing](#our-contribution) to the problem and what [challenges we are looking to](#open-problems) for the future.

<span class="project--description">Motivation</span>: xx, yy, zz.  -->

<!-- <span class="project--description">Summary</span>:  -->

Critical infrastructures such as power grids, communication and energy networks; potentially dangerous industrial processes such as nuclear or chemical plants; transportation systems or autonomous robots. These are examples of systems for which safety and resiliency should be an integral part of their design. The occurrence of faults in these cases can lead to unacceptable losses, or simply make their operation uneconomical. For instance, in the offshore wind energy sector Operation&Maintenance cost can already reach up to 30% of the total lifetime cost {% cite may2015economic --file papers %}.
Detecting and accommodating faults before they lead to consequences is thus a key requirement.

<!-- NOTE: add hoverable footnotes such as in <d-footnote> from the distill script -->

Model-based techniques constitute a powerful way to detect faults, by comparing the predictions of a mathematical model (or _digital twin_ as often referred to in the industry) of the system to real-time measurements coming from sensors. The central problem of fault diagnosis then becomes detecting when differences between the two are caused by physiological _uncertainties_ present in the model and the sensors, and when they are due to an actual, pathological _fault_.

<!-- In
blah blah, for simple cases where effects from faults are separable from uncertainties, blah blah, but real interesting cases are systems that are very large and complex, with nonlinear and uncertain dynamics. Good fault diagnosis is the basis of fault tolerant approaches which can use diagnostic results to reconfigure the system blah blah. -->

We contributed by extending centralized model-based methods in order to handle large-scale, uncertain nonlinear systems {% cite Ferrari_2012aa --file my_papers%}. Then we focused on the central problem of getting better diagnosis performances in terms of the so-called _False Alarm Rates_ and _Missed Detection Rates_. Our key to reaching this objective is moving from a deterministic to a probabilistic approach: in {% cite Rostampour_2017aa --file my_papers%}, {% cite Rostampour_2018aa --file my_papers%}, {% cite Rostampour_2020ab --file my_papers%} we used a _scenario approach_ to derive set-based thresholds with user-desired probabilistic robustness. Our research efforts are now focusing on deriving fast, general and efficient methods for quantifying and propagating uncertainties through arbitrary nonlinear systems.
Our work on fault diagnosis found applications in <a href=" {{ "projects/research_topics/4_wind_energy" | relative_url }}">wind energy</a>, <a href=" {{ "projects/research_topics/2_safety_security_privacy_CPS" | relative_url }}">cyber-physical systems</a> security
<a href=" {{ "projects/research_topics/3_automotive" | relative_url }}">automotive</a> and aerospace fault tolerant control and <a href=" {{ "projects/research_topics/5_active_inference" | relative_url }}">robotics</a>.



<span class="project--description">Joint work with (mostly)</span>: Thomas Parisini, Marios M. Polycarpou, Francesca Boem, Vahab Rostampour, Yichao Liu.

## Publications

<div class="publications">
    {% bibliography -f my_papers -q @*[keywords ~= fault] %}
</div>

## Additional References

<div class="publications">
    {% bibliography -f papers --cited_in_order %}
</div>