---
layout: page
title: autonomous rovers
description: using small scale RC cars as autonomous rovers
img: assets/img/albums/lab/rovers/assembling_rover.jpg
head_banner: assets/img/albums/lab/rovers/assembling_rover.jpg
importance: 1
category: lab
---

In order to test control algorithms for ground and aerial drones, our lab is equipped with a motion capture arena of about 4x7x3 meters (lxwxh), with an [Optitrack](https://optitrack.com) system running at 120 Hz.

During the project SURE, and then for several BSc and MSc final projects we tested the implementation of safe platooning algorithms on a set of small scale, autnomous RC cars. The cars, based on a platform produced by Erle Robotics (unfortunately no longer in business), features the following

* 1/10th RC car platform, with high torque custom motors
* Erle Brain local controller, based on a Raspberry PI 3
* NVidia Jetson TX2 single board computer for real time stereo vision
* Zed camera for stereo vision imaging

While originally the RC cars had only the Raspberry PI onboard controller, an NVidia Jetson and a Zed stero camera were added later through custom modifications (including PCBs and 3D printed or laser cut components). A peculiarity of the custom cars is that theyy features on the front, back and sides one controllable led matrix that can be used for visual car-to-car communication, using dot patterns similar to QR codes.

More information on our experimental cars is available here:

* T. De Jager, N. Meinders, T. Van Vugt, and W. Zomerdijk, “Autonomous rc cars for control research and education: Implementation of virtual potential based navigation and platooning,” in *2022 IEEE Conference on Control Technology and Applications (CCTA)*, pp. 504–509, IEEE, 2022.
* Simon van der Marel, "[Development of a Platform for Stereo Visual Odometry based Platooning](https://repository.tudelft.nl/islandora/object/uuid%3A1b520436-feed-4a81-8684-ea3d5b1e55e0?collection=education)," MSc thesis, TU Delft, 2022.
  
<div class="row justify-content-sm-center">
    <div class="col-sm mt-3 mt-md-0">
        <a href="{{ '/assets/img/albums/lab/rovers/arena.jpeg' | relative_url }}"><img class="img-fluid rounded z-depth-1" src="{{ '/assets/img/albums/lab/rovers/arena.jpeg' | relative_url }}" alt="" title="example image"/></a>
    </div>
</div>
<div class="caption">
    The mocap arena, with BSc students De Jager, N. Meinders, T. Van Vugt, and W. Zomerdijk.
</div>

<div class="row justify-content-sm-center">
    <div class="col-sm mt-3 mt-md-0">
        <video width="320" height="180" controls>
        <source src="{{ '/assets/img/albums/lab/rovers/platooning.mp4' | relative_url }}" type="video/mp4">
        </video>
    </div>
    <div class="col-sm mt-3 mt-md-0">
        <video width="320" height="180" controls>
        <source src="{{ '/assets/img/albums/lab/rovers/demo_fault_tolerance.mp4' | relative_url }}" type="video/mp4">
        </video>
    </div>
</div>
<div class="caption">
    A platooning test with two cars (left), a simulation showing the performances of anomaly detection algorithms (right).
</div>

<div class="row justify-content-sm-center">
    <div class="col-sm mt-3 mt-md-0">
        <video width="640" height="360" controls>
        <source src="{{ '/assets/img/albums/lab/rovers/assembling_rover.mp4' | relative_url }}" type="video/mp4">
        </video>
    </div>
<div class="caption">
    Time lapse of the assembly of one custom RC car by MSc student Simon van Marel and PhD student Twan Keijzer.
</div>
