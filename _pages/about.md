---
permalink: /
title: "About me"
excerpt: "Boxiang Rong's HomePage"
author_profile: true
redirect_from: 
  - /about/
  - /about.html
---

My name is Boxiang Rong(荣波翔), I am currently a Master student of Robotics, Systems, and Control (RSC) in [ETH Zurich](https://ethz.ch/en.html). I obtained my Bachelor degree in [Tianjin University](http://www.tju.edu.cn/english/index.htm), and I was supervised by Prof. Dr. [Yuxiong Wang](https://yxw.web.illinois.edu/) for my Bachelor thesis.

My interests lie in the fields of computer graphics and computer vision. I am fascinated with creating immersive virtual world and committed to working in the areas of rendering, character motion, and physics-based simulation.

## Education

* 2022 - Present, Master of Science, Robotics Systems and Contorl, ETH Zurich, Switzerland.
* 2018 - 2022, Bachelor of Engineering, Communication Engineering, Tianjin University, China.



# Selected Projects
## ETH 2022 Rendering Competition
<strong>Boxiang Rong</strong>\*, Ziyao Shang\*  
Course project of Computer Graphics 2022 in ETH Zurich  
[[Website]()][Code(not available)]  
<!-- ![Project Profile](../images/rendering_competition.gif) -->
<img src="../images/rendering_competition.gif" alt="Project Profile" width="600px">  

Theme for this year's rendering competition is _"Out Of Place"_. Our work is inspired by Chinese anime movie [Big Fish & Begonia](https://www.imdb.com/title/tt1920885/) and ancient literature [A Happy Excursion(逍遥游)](https://link.springer.com/chapter/10.1007/978-3-662-48075-5_1). In which we built huge fishes(named K'un) flying in the universe, and voyagers sailing on clouds towards the northernmost of the world.

Our renderer is built from stratch using Nori codebase. In the project, I built the whole scene using blender and implemented rendering functions, including Multi-Importance Sampling, Path Tracing, Photon Mapping, Environment Map, Disney BSDF, Procedural Volume, Texture Mapping and Low-Discrepancy Sampling .etc


## Motion Matching for Responsive Animation for Digital Humans
<strong>Boxiang Rong</strong>\*, Longteng Duan\*, Guo Han*, Hang Yin*  
Course project of Digital Humans 2023 in ETH Zurich  
[[Report]()][[Code](https://github.com/Ribosome-rbx/Motion-Matching-for-Human-Skeleton)][[Demos](https://youtube.com/playlist?list=PLUffCQyBEYtYXr-pVqqUgSG1Ncxp4UzAb)][[Slides](https://docs.google.com/presentation/d/13Kz_PvJAkfzi9m_gFjUCRpPG92N0RBROceEzudvjc8I/edit?usp=sharing)]  
<img src="../images/dg.gif" alt="Project Profile" width="600px">

Motion matching is a simple yet effective character animation tool for synthesizing motions that follow a user’s high-level command input. In this project, we implement a motion matching pipeline from scratch by utilizing publicly available motion capture datasets ([LaFan1](https://github.com/ubisoft/ubisoft-laforge-animation-dataset)).
C++ implementation of a motion matching algorithm with our code base (similar with the code base provided for the assignments)
A real-time (video game-like!) demo of responsive character animation  

To summarize the pipeline: After loading human skeleton motion data, we constructed **2d and 3d feature base** for all frames of motions. Then we use **spring damper system** to generate smooth trajectories, this information will be combined with current states to match next motion. After each metching, **inertialization** is implemented to get a smooth pose transformation.

Apart from the pipeline, we achieved **multiple means of control**: keyboard, painting and real-time human pose. We collected a [pose dataset](https://github.com/Ribosome-rbx/pose-classifier-on-fastpose) to turn pose into command by classification, and leveraged [FastPose](https://drnoodle.github.io/fastpose_html/) to capture poses in real-time. 
## Head-Worn Camera Image Stabilization using Neural Radiance Field
<strong>Boxiang Rong</strong>, Zilong Deng, Ziyao Shang, Minjing Shi  
Course project of 3D Vision 2023 in ETH Zurich  
[[Report]()][[Code1](https://github.com/Ribosome-rbx/Color_Map_Optimization)][[Code2](https://github.com/Ribosome-rbx/TrajDeblur-NeRF)][[Demos](https://youtube.com/playlist?list=PLUffCQyBEYtbOQg4-66ZrcuNmsX0OXVKv)][[Poster](https://docs.google.com/presentation/d/1ka6ztHGhPxwDq_VgpPXk0cOhuihfD-ee4sKPxdE_RLg/edit?usp=sharing)]  
<img src="../images/room.gif" alt="Project Profile" width="600px">  

Motion blur happens with fast head-camera movement and long exposure times. In this project, we proposed to reconstruct the indoor environment in advance and render clear images to replace blurry camera views to achieve the goal of image stabilization. We used four pipelines, including traditional reconstruction and NeRF-based ones ([Depth-Supervised NeRF](https://github.com/dunbar12138/DSNeRF), [Deblur NeRF](https://github.com/limacv/Deblur-NeRF), [Instant NGP](https://github.com/NVlabs/instant-ngp)). Experiments were done on three scenes to test the stabilizing performance and analyze the pros and cons of each pipeline. We also proposed **adding camera motion information** to Deblur NeRF for better deblurring and verified the performance of our modification.

Main Contributions:
* Build mesh reconstruction pipeline with Open3d, including aligning depth to RGB images, Point-Cloud reconstruction and stitching, Poisson surface reconstruction, and Color Map Optimization
* Modified Deblur Nerf to load our dataset and add trajectory information to better model blurry pattern

<!-- 
<script type="text/javascript" id="clustrmaps" src="//clustrmaps.com/map_v2.js?d=Y25n2MtaECuXONMSqo0Fre6WDGJdufXd4bRMP2MIYxg&cl=ffffff&w=a"></script> -->
