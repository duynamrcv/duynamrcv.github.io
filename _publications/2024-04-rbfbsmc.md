---
title: 'Radial basis function neural networks for formation control of unmanned aerial vehicles'
collection: publications
category: articles
permalink: /publications/2024-04-rbfbsmc
doi: 10.1017/S0263574724000559
authors: 'Duy-Nam Bui & Manh Duong Phung'
date: 2024-04-19
venue: 'Robotica'
arxivurl: 'https://arxiv.org/pdf/2404.13583'
codeurl: 'https://github.com/duynamrcv/rbf_bsmc'
videourl: 'https://youtu.be/LYD7269n1-c'
---

This paper addresses the problem of controlling multiple unmanned aerial vehicles (UAVs) cooperating in a formation to carry out a complex task such as surface inspection. We first use the virtual leader-follower model to determine the topology and trajectory of the formation. A double-loop control system combining backstepping and sliding mode control techniques is then designed for the UAVs to track the trajectory. A radial basis function neural network capable of estimating external disturbances is developed to enhance the robustness of the controller. The stability of the controller is proven by using the Lyapunov theorem. A number of comparisons and software-in-the-loop tests have been conducted to evaluate the performance of the proposed controller. The results show that our controller not only outperforms other state-of-the-art controllers but is also sufficient for complex tasks of UAVs such as collecting surface data for inspection. The source code of our controller can be found at [https://github.com/duynamrcv/rbf_bsmc](https://github.com/duynamrcv/rbf_bsmc).

## Demo
Firstly, run file `parameter.m` to load the essential parameters. Then open `adaptive.slx` and press `Run` in the simulink.

<iframe width="560" height="315" src="https://www.youtube.com/embed/LYD7269n1-c?si=3tB0ksmILvNHhHOP" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>

### Scenario 1
<img src="https://github.com/duynamrcv/rbf_bsmc/raw/main/results/rbf-bsmc-traj-top.png" width="54%" />
<img src="https://github.com/duynamrcv/rbf_bsmc/raw/main/results/rbf-bsmc-traj-side.png" width="45%"/>

### Scenario 2
<img src="https://github.com/duynamrcv/rbf_bsmc/raw/main/results/rbf-bsmc-traj-top2.png" width="48%" />
<img src="https://github.com/duynamrcv/rbf_bsmc/raw/main/results/rbf-bsmc-traj-3d2.png" width="50%" /> 

### Experiment Results
<iframe width="560" height="315" src="https://www.youtube.com/embed/1yUCzWRDcp0?si=hJOCjZ2gnQTpkVpw" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>