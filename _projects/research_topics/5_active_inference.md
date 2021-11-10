---
layout: page
title: Active Inference
description: making robotic manipulators adapt autonomously to faults
img: /assets/img/projects/active_inference.jpg
head_banner: /assets/img/projects/active_inference.jpg
importance: 5
category: research topics
---


We are used to see "armies" of robots manufacturing cars or handling packages at sorting facilities. These are very structured environments, with restricted access, where robots can be programmed in a deterministic way. In order to move to unstructured environments, and have them sharing their workspace with humans, we need to account for uncertainties and develop stochastic, adaptive control schemes.

_Active inference_ is a stepping stone we are currently using to address this challenge. Active Inference is prominent in the neuroscientific literature as a general theory of the human brain {% cite friston2 --file papers %}. We can loosely describe it here as the tendency of our brain to both update its own beliefs about the world around us, and act upon it in a way that minimizes "surprise". In particular, such _surprise_ is defined through the so-called _Free Energy_ and depends on the difference between an internal _generative model_ of the word held by the brain, and _sensory information_.
Several recent approaches in robotics have taken inspiration from it {% cite buckley --file papers %} for tasks such as state-estimation {% cite baioumy2020active --file papers %}, adaptive control {% cite Pezzato_2020ab --file my_papers %}, predictive control {% cite 2020ICRA_baioumy --file papers %}, human-robot interaction {% cite Ohata_2020 --file papers %}, reinforcement learning {% cite tschantz2020reinforcement --file papers %} and many more. 

Together with TUD colleagues Corrado Pezzato and Carlos Hernandez Corbato, and Mohamed Bayoumi and Nick Hawes from Oxford Robotics Institute, we recently proposed a novel fault tolerant controller for robotic manipulators based on Active Inference {% cite Pezzato_2020ac Baioumy_2021aa --file my_papers %}. We are currently working on extending it to learn online the accuracy of its own sensors, which can be used to adapt to natural degradations or complete failures {% cite Baioumy_2021qm --file my_papers %}.


<span class="project--description">Joint work with (mostly)</span>: Corrado Pezzato, Carlos Hernandez Corbato, Mohamed Bayoumi and Nick Hawes.

## Publications

<div class="publications">
    {% bibliography -f my_papers -q @*[keywords ~= active inference] %}
</div>

## Additional References

<div class="publications">
    {% bibliography -f papers --cited_in_order %}
</div>