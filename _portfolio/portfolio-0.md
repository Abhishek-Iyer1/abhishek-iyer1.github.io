---
title: "Smores - Searching while modelling perceptually degraded environments for time critical rescues"
excerpt: "I am currently leading the Smores project at the AirLab at Carnegie Mellon University. Our focus is to perform real-time mapping and 3D reconstruction of indoor environments with dense smoke so we can provide critical information to first responders like firefighters. Additionally, we are building a drone which will be able to navigate autonomously in addition to mapping and displaying Points of Interests (PoIs) like humans, open doors, active fires to the ground control station in real-time with limited computing power. <br/><img src='/images/depth_estimation.png'>"
collection: portfolio
---
 
### Demonstration and Discussion
<style>
    .special {
        text-align: justify;
        text-justify: inter-word;
    }
</style>

<!-- <div style="width: 70%; height: 70%; padding-top: 20px; padding-bottom: 20px; margin-left: 7.5vw;">
    <iframe width="1052" height="631" src="https://www.youtube.com/embed/UC5mCCvOfWg?autoplay=1&mute=1" title="Smores - Integrated Depth Estimation Pipeline" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>
    <img src='/images/smoke_demo.gif'>
</div> -->
<!-- <div style="display: flex; gap: 20px; justify-content: center; align-items: stretch; 
           max-width: 1400px; margin: 0 auto; padding: 20px; background: #f0f0f0; height: auto;">
  <div style="flex: 1 1 60%; min-width: 0; max-height: 1000px; background: #00ffff;">
    <iframe style="width: 100%; height: auto; aspect-ratio: 16/9; border: none;"
            src="https://www.youtube.com/embed/UC5mCCvOfWg?autoplay=1&mute=1"
            allowfullscreen>
    </iframe>
  </div>
  
  <div style="flex: 0 0 auto; width: calc(40% - 20px); background: #ff00ff;">
    <img src='/images/smoke_demo.gif' 
         style="height: 50%; width: auto; object-fit: contain; border-radius: 8px;">
  </div>
</div> -->
<div style="display: flex; gap: 20px; justify-content: center; align-items: flex-start; 
           max-width: 1400px; margin: 0 auto; padding: 20px; background: #f0f0f0;">
  <!-- Video Container -->
  <div style="flex: 1 1 60%; min-width: 0;">
    <iframe style="width: 100%; height: 0; min-height: 600px; padding-bottom: 56.25%; border: none;"
            src="https://www.youtube.com/embed/UC5mCCvOfWg?autoplay=1&mute=1"
            allowfullscreen>
    </iframe>
  </div>

  <!-- GIF Container -->
  <div style="flex: 0 0 auto; width: auto;">
    <img src='/images/smoke_demo.gif' 
         style="height: 300px; width: auto; object-fit: contain; border-radius: 8px;">
  </div>
</div>


<p class="special">Recent events have shed light on the importance of arming first responders with critical information about their environments, especially in hazardous environments like an active fire. Through smores, we aim to deliver an autonomous drone capable of mapping the environment through dense smoke and annotating points of Interests (POIs) on this map so firefighters can take informed actions and utilize resources more efficiently.</p>

The different technical verticals of our system are:
<ul>
    <li class="special"><b>Real-time Mapping</b>: Using a stereo thermal camera setup on the drone to perceive through dense smoke and recovering dense depth. Using the dense depth we can reconstruct a pointcloud representation of the environment.</li>
    <li class="special"><b>State Estimation</b>: Fusing RGB cameras, thermal cameras, and 9 DOF IMU to predict state through dense smoke. The recovered odometry is crucial for autonomy and combining separate pointclouds of a specific scene into one combined representation.</li>
    <li class="special"><b>Autonomy</b>: Since firefighters have extremely limited manpower, we aim to provide safe and autonomous flight so we can provide crucial information at no additional cost to firefighters.</li>
    <li class="special"><b>Identifying POIs</b>: Recognizing and annotating points of interests on the map such as humans, open doors, and origin of fires on the reconstructed map to allow for informed planning for firefighters.</li>
</ul>

<div style="display: flex; justify-content: center; align-items: center; padding: 20px;">
    <img src='/images/drone_cad.png' alt="Image of hardware">
</div>

<p class="special">In order to deliver a solution of the highest quality, we decided to build our own platform. In addition to building the hardware and electrical subsystems, we are focusing on accelerating our depth perception pipeline to work in real-time since we are working with limited computing power (NVIDIA Jetson AGX Orin). Our coming priorities are relaying all information in real-time to the ground control station where the incident commander can utilize this information to plan a response.</p>

<p class="special">My focus so far has been leading the development on the perception pipeline to recover dense depth and making a consistent 3D reconstruction of the environment. In conjuction, I have been overseeing the electrical subsystem and sensor interfacing for the build of the drone. Finally, in the coming semster, I will be focusing on accelerating existing machine learning models to work in real-time and creating models for detecting points of interests.</p>


<body><b>Technologies: </b> Python, C++, PyTorch, TensorRT, ROS2, Foxglove, Docker</body>

**Project Website:** [Link](https://mrsdprojects.ri.cmu.edu/2025teamg/project-media/)\
**GitHub Code Repository:** Private Repository
