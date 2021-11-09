---
layout: page
title: Cyber Physical Systems
description: safety, security and privacy
img: /assets/img/projects/2_safety_security_privacy_CPS/platooning_cars.jpg
head_banner: /assets/img/projects/2_safety_security_privacy_CPS/platooning_cars.jpg
importance: 2
category: research topics
---

Cyber-physical systems (CPSs) represent a class of networked control systems with vast and promising applications. This class may include for instance smart cities, intelligent transportation systems based on fleets of cooperative and autonomous vehicles or distributed sensing and control solutions that leverage Internet-of-Things (IoT) devices. As a common trait, these systems are expected to provide important functionalities that may positively influence our life and society.
However, said positive outcomes may be hindered by novel threats to the safety of CPSs, such as malicious cyber-attacks that could negatively affect the physical domain. Furthermore, the sheer amount of data gathered, exchanged and processed by those architectures are going to pose fundamental societal interrogatives regarding privacy and confidentiality, and the fair use of such data {% cite Ferrari2021-xs --file my_papers %}.
_Prevention_, _resilience_ and _detection_ are key functionalities through which we can avoid that attacks in the cyber domain lead to loss of safety in the physical one.

<!-- NOTE: add hoverable footnotes such as in <d-footnote> from the distill script -->

We contributed to the problem of detecting stealthy cyber attacks in networked control systems by proposing a multiplicative sensor watermarking technique {% cite Ferrari_2021vk Gallo_2021yd --file my_papers%}. By taking inspiration from lightweight authentication techniques, we introduce a deterministic distortion into data sent by sensors to the controller, which is unknown to the attacker. This leads to a knowledge imbalance between an eavesdropping attacker and a defender, where the latter can use knowledge of the watermark and a model-based residual generator to detect otherwise stealthy attacks such as rerouting {% cite Ferrari_2017aa --file my_papers%}, replay {% cite Ferrari_2017ab --file my_papers%} and zero-dynamics {% cite Teixeira_2018aa --file my_papers%} injection ones. Differently than physical watermarking, our approach allows for perfect watermarking removal at controller level, thus unaffecting control performances.

We further explored the use of _Differential Privacy_ {% cite Dwork2014-aa --file papers %} to allow for privacy preserving distributed state estimation and anomaly detection, thus preventing the leakage of private data by eavesdroppers or by curious, although not necessarily malicious, third parties {% cite Rostampour_2018aa Rostampour_2020ab --file my_papers%}.
Currently we are working towards fast, real time implementations of _Fully Homomorphic Encryption_ schemes as a tool to guarantee confidentiality and integrity in a much more robust, albeit computationally expensive way {% cite Gentry2013-hj --file papers%}.



<span class="project--description">Joint work with (mostly)</span>: André Teixeira, Twan Keijzer, Alex Gallo, Vahab Rostampour.

## Publications

<div class="publications">
    {% bibliography -f my_papers -q @*[keywords ~= cyber || keywords ~= privacy] %}
</div>

## Additional References

<div class="publications">
    {% bibliography -f papers --cited_in_order %}
</div>