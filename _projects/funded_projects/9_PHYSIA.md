---
layout: page
title: PHYSIA
description: RVO TKI project
img: /assets/img/projects/offshore_turbine_small.jpg
importance: -9
category: funded projects
---


<div class="container">
  <div class="row">
    <div class="col-sm-9">
        <p><u>Title:</u> Physics Informed-AI models for cyber-attack detection in offshore wind farms (PHYSIA)</p>
        <p><u>Period:</u> 2024 - 25</p>
        <p><u>Budget:</u> 100 KEur</p>
        <p><u>Role:</u> PI</p>
        <p><u>Funding source:</u> TKI Offshore Energy (RVO),  Open Innovation Call - Cyber resilience for offshore wind farms</p>
    </div>
    <!-- <div class="col-sm-3">
        <p><img class="img-fluid rounded z-depth-1" src="{{ '/assets/img/projects/horizon_2020.png' | relative_url }}" alt="" title="Horizon 2020 logo"/></p>
    </div> -->
  </div>
</div>


<u>Description:</u> Europe's aim to achieve climate neutrality by 2050, combined with goals of energy independence and security, requires optimizing modern wind energy systems. Wind farm control, especially for large offshore farms, is critical to this effort. This project focuses on developing AI tools to detect cyber-attacks on wind farm control systems, emphasizing automatic threat detection and advancing these technologies from TRL 4 to 5 through risk-based assessments.

Traditional IT security measures fall short for operational technology (OT) systems, which prioritize availability and integrity due to safety and real-time requirements. Preventive security methods like firewalls are insufficient against sophisticated attackers. Therefore, the project employs reactive techniques from fault-tolerant fields and novel methods like watermarking and homomorphic encryption to detect cyber anomalies.
In collaboration with Delft University of Technology (TUD) and [Batenburg Magion]() (BM), the project will test these techniques in realistic settings, aiming to validate their effectiveness and promote broader adoption. The ultimate goal is to enhance the security of renewable energy assets in the offshore wind industry by establishing a robust second line of defense.

## Publications

<div class="publications">
    {% bibliography -f my_papers -q @*[keywords ~= {{ page.title}}] %}
</div>