---
permalink: /
title: "About me"
excerpt: "Boxiang Rong's HomePage"
author_profile: true
redirect_from: 
  - /about/
  - /about.html
---

{% include toc %}

My name is Boxiang Rong(荣波翔), I am currently a Master student of Robotics, Systems, and Control (RSC) in [ETH Zurich](https://ethz.ch/en.html). I obtained my Bachelor degree in [Tianjin University](http://www.tju.edu.cn/english/index.htm).

My interests lie in the fields of computer graphics and computer vision. I am fascinated with creating immersive virtual world and committed to working in the areas of rendering, character motion, and physics-based simulation.

# Education

* 2022 - Present, MSc, Robotics Systems and Contorl, ETH Zurich, Switzerland.
* 2018 - 2022, B.E., Communication Engineering, Tianjin University, China.

# Publication

## 4D-DRESS: A 4D Dataset of Real-World Human Clothing With Semantic Annotations
Wenbo Wang\*, Hsuan-I Ho\*, Chen Guo, <strong>Boxiang Rong</strong>, Artur Grigorev, Jie Song, Juan Jose Zarate, Otmar Hilliges   
Conference on Computer Vision and Pattern Recognition (CVPR), 2024  
[[Project Page](https://eth-ait.github.io/4d-dress/)][[Arxiv](https://files.ait.ethz.ch/projects/4d-dress/4d-dress.pdf)][[Video](https://youtu.be/dEQ4dvO8BsE?si=4AlflvLnFFsrbmMl)]
<img src="../images/4ddress_simu.gif" alt="Project Profile" width="600px">  

# Selected Projects

## Nori CPU Render
<strong>Boxiang Rong</strong>\*, Ziyao Shang\*  
Course project of Computer Graphics 2022 in ETH Zurich  
[[Website](https://ribosome-rbx.github.io/files/2022_rendering_competition.html)][[Present](https://www.youtube.com/live/wtH4PCtMOoY?feature=share&t=3691)][Code(not available)]  
<!-- ![Project Profile](../images/rendering_competition.gif) -->
<img src="../images/rendering_competition.gif" alt="Project Profile" width="600px">  

We built our own offline physically-based renderer on Nori -- an educational ray tracing framework, written in C++. Our final image is selected for presentation in ETH 2022 Rendering Competition. 

Theme for this year's rendering competition is _"Out Of Place"_. Our work is inspired by Chinese anime movie [Big Fish & Begonia](https://www.imdb.com/title/tt1920885/) and ancient literature [A Happy Excursion(逍遥游)](https://link.springer.com/chapter/10.1007/978-3-662-48075-5_1). In which we built huge fishes(named K'un) flying in the universe, and voyagers sailing on clouds towards the northernmost of the world.

In the project, I built the whole scene in blender and implemented rendering functions, like Multi-Importance Sampling, Path Tracing, Photon Mapping, Environment Map, Disney BSDF, Procedural Volume, Texture Mapping and Low-Discrepancy Sampling .etc


## Position-based Fluid and Foam Simulation
<strong>Boxiang Rong</strong>\*, Longteng Duan\*, Guo Han\*  
Course project of Physically-Based Simulation 2023 in ETH Zurich  
[[Slide](https://docs.google.com/presentation/d/1FDaCpLuZ-d3ePbB2i_EjrVKCm3rL1_fY/edit?usp=sharing&ouid=113618116785952766072&rtpof=true&sd=true)][[Demo](https://youtu.be/6cz7K6m6m8M?si=7OyMHdkqVaCZ09Kk)][[Code](https://github.com/guo-han/Position-Based-Fluids.git)]  
<img src="../images/bunny_in_the_water.png" alt="Project Profile" width="600px">  

"Bunny in the water" -- We implemented the 3D position-based fluids simulation using __Taichi language__. And we handled collisions of simple __static rigid body__ and used AABB to facilitate. We reimplemented __foam simulation__ from SPlisHSPlasH in Taichi to simulate white particles: spray, foam and bubbles. Thanks to the CPU/GPU parallelization empowered by Taichi, our whole pipeline can be simulated in __real-time__(~25FPS).

For the rendering part, we used `splashsurf` to reconstruct fluid surface and built the whole scene in Blender. We used `bpy` to instantiate models, materials and finish final rendering.


## Motion Matching for Responsive Animation for Digital Humans
<strong>Boxiang Rong</strong>\*, Longteng Duan\*, Guo Han\*, Hang Yin\*  
Course project of Digital Humans 2023 in ETH Zurich  
[[Report](https://ribosome-rbx.github.io/files/motion_matching.pdf)][[Code](https://github.com/Ribosome-rbx/Motion-Matching-for-Human-Skeleton)][[Demos](https://youtube.com/playlist?list=PLUffCQyBEYtYXr-pVqqUgSG1Ncxp4UzAb)][[Slides](https://docs.google.com/presentation/d/13Kz_PvJAkfzi9m_gFjUCRpPG92N0RBROceEzudvjc8I/edit?usp=sharing)]  
<img src="../images/motion_matching.gif" alt="Project Profile" width="600px">

Motion matching is a simple yet effective character animation tool for synthesizing motions that follow a user’s high-level command input. In this project, we implement a motion matching pipeline from scratch by utilizing publicly available motion capture dataset ([LaFan1](https://github.com/ubisoft/ubisoft-laforge-animation-dataset)). Checkout the real-time (game-like video!) [demo](https://youtube.com/playlist?list=PLUffCQyBEYtYXr-pVqqUgSG1Ncxp4UzAb) of responsive character animation. 

To summarize the pipeline: After loading human skeleton motion data, we constructed **2d and 3d feature base** for all frames of motions. Then we use **spring damper system** to generate smooth trajectories, this information will be combined with current states to match next motion. After each matching, **inertialization** is implemented to get a smooth pose transformation.

Apart from the pipeline, we achieved **multiple means of control**: keyboard, painting and real-time human pose. We collected a [pose dataset](https://github.com/Ribosome-rbx/pose-classifier-on-fastpose) to turn pose into command by classification, and leveraged [FastPose](https://drnoodle.github.io/fastpose_html/) to capture poses in real-time. 

## Rendering Trees in Mixed Reality
<strong>Boxiang Rong</strong>\*,  Marius Debussche\*, David Kamm\*, Adrien Lanne\*  
Course project of Mixed Reality 2023 in ETH Zurich   
[[Report](https://ribosome-rbx.github.io/files/MR.pdf)][[Video](https://youtu.be/BjEJ_WHgWJg)][[Poster](https://docs.google.com/presentation/d/1MjJEeYk3IWrWuV2Ctf4495X7Q1sQIUH11DDMn2zhPJI/edit?usp=sharing)]    
<img src="../images/tree.gif" alt="Project Profile" width="600px">


We developed an MR program in Unity for [MagicLeap2](https://www.magicleap.com/magic-leap-2) device, where you can select different types of trees and plant them on the reconstructed ground. 

We built upon Unity's URP rendering pipeline, and achieved realistic rendering of trees by custimizing Shader Graph. Our pipeline supports billboard-based models, RGB and normal mapping, environment map. Additionally, we employ Perlin Noise to create dynamic leaf oscillation animations. Leveraging the Mixed Reality Toolkit (MRTK), we customize the user interface for enhanced interactivity, elevating the tree planting experience.


## Head-Worn Camera Image Stabilization using Neural Radiance Field
<strong>Boxiang Rong</strong>, Zilong Deng, Ziyao Shang, Minjing Shi  
Course project of 3D Vision 2023 in ETH Zurich  
[[Report](https://ribosome-rbx.github.io/files/3DV.pdf)][[Code1](https://github.com/Ribosome-rbx/Color_Map_Optimization)][[Code2](https://github.com/Ribosome-rbx/TrajDeblur-NeRF)][[Demos](https://youtube.com/playlist?list=PLUffCQyBEYtbOQg4-66ZrcuNmsX0OXVKv)][[Poster](https://docs.google.com/presentation/d/1ka6ztHGhPxwDq_VgpPXk0cOhuihfD-ee4sKPxdE_RLg/edit?usp=sharing)]  
<img src="../images/annaroom.gif" alt="Project Profile" width="600px">  

Motion blur happens with fast head-camera movement and long exposure times. In this project, we proposed to reconstruct the indoor environment in advance and render clear images to replace blurry camera views to achieve the goal of image stabilization. We used four pipelines, including traditional reconstruction and NeRF-based methods ([Depth-Supervised NeRF](https://github.com/dunbar12138/DSNeRF), [Deblur NeRF](https://github.com/limacv/Deblur-NeRF), [Instant NGP](https://github.com/NVlabs/instant-ngp)). We did experiments to test the stabilizing performance and analyze the pros and cons of each pipeline. We also proposed **adding camera motion information** to Deblur NeRF for better deblurring and verified the performance of our modification.

Main Contributions:
* Build mesh reconstruction pipeline with Open3d, including aligning depth to RGB images, Point-Cloud reconstruction and stitching, Poisson surface reconstruction, and Color Map Optimization
* Modified Deblur Nerf to load our dataset and add trajectory information to better model blurry pattern

## Priority Labeling in the Scenarios of Self-Driving
<strong>Boxiang Rong</strong>, [Hang Zhao](https://hangzhaomit.github.io/)  
Research project in Shanghai [Qizhi AI Lab](https://sqz.ac.cn/en) 2022  
[[Code](https://github.com/Ribosome-rbx/detmetric)][[Slides](https://docs.google.com/presentation/d/1IhTVg7qeNFhnkSjIlrXehNOPWBuDZcuHGkt0_8GhFJ0/edit?usp=sharing)]   
<img src="../images/drive.gif" alt="Project Profile" width="600px">

Street scenarios are generally complex, where numbers of pedestrains, vehicles and obstacles interact with each other. However, we don't need to pay equal attention to all of the visible targets. Instead, similar to human drivers, we only care about the important target that are most likely to appear in our way and influence our driving.

Our work is done on on Nuscenes dataset. We arranged human drivers to **manually annotate** priority levels to all visible targets. And we also designed **rule-based algorithm** to automatically annotate priorities, which considers information, like distance and relative velocity between ego and targets, trajectory intersections, and map-based terrain information.

<!-- <div style="position: relative; width: 50%;"> -->
<script type="text/javascript" id="clustrmaps" src="//clustrmaps.com/map_v2.js?d=Y25n2MtaECuXONMSqo0Fre6WDGJdufXd4bRMP2MIYxg&cl=ffffff&w=a" width="200px">
</script>
<!-- </div> -->
