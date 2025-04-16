---
title: 'Multi-goal Rapidly Exploring Random Tree with Safety and Dynamic Constraints for UAV Cooperative Path Planning'
collection: publications
category: articles
permalink: /publications/2025-04-multirrt
doi: 10.1109/TVT.2025.3560658
authors: 'Thu Hang Khuat, Duy-Nam Bui, Hoa TT. Nguyen, Mien L. Trinh, Minh T. Nguyen & Manh Duong Phung'
date: 2025-04-12
venue: 'IEEE Transactions on Vehicular Technology'
# arxivurl: 'https://arxiv.org/pdf/2501.03261'
codeurl: 'https://github.com/duynamrcv/multi-target_RRT'
---

Cooperative path planning is gaining its importance due to the increasing demand on using multiple unmanned aerial vehicles (UAVs) for complex missions. This work addresses the problem by introducing a new algorithm named MultiRRT that extends the rapidly exploring random tree (RRT) to generate paths for a group of UAVs to reach multiple goal locations at the same time. We first derive the dynamics constraint of the UAV and include it in the problem formulation. MultiRRT is then developed, taking into account the cooperative requirements and safe constraints during its path-searching process. The algorithm features two new mechanisms, node reduction and Bezier interpolation, to ensure the feasibility and optimality of the paths generated. Importantly, the interpolated paths are proven to meet the safety and dynamics constraints imposed by obstacles and the UAVs. A number of simulations, comparisons, and experiments have been conducted to evaluate the performance of the proposed approach. The results show that MultiRRT can generate collision-free paths for multiple UAVs to reach their goals with better scores in path length and smoothness metrics than state-of-the-art RRT variants including Theta-RRT, FN-RRT, RRT*, and RRT*-Smart. The generated paths are also tested in practical flights with real UAVs to evaluate their validity for cooperative tasks. The source code of the algorithm is available at [https://github.com/duynamrcv/multi-target_RRT](https://github.com/duynamrcv/multi-target_RRT).

## Installation
<pre>
git@github.com:duynamrcv/multi-target_RRT.git
</pre>

## Run simulation
The current version have four different scenarios, from 1 to 4. Before run our method, please change the value of `scenario` in file. To run our method, run:
<pre>
python3 contraint_rrt.py
python3 post_processing.py
</pre>

We also implement some methods to conduct the comparisons, i.e. `compare_*.py`. To run those methods, run:
<pre>
python3 compare_rrt_star.py
python3 compare_rrt_smart.py
</pre>

The data will be saved in `*.txt` file. This file is used for the statistic, i.e. `analys_*.py`.

## Results and Comparison
### Path
<img src="https://github.com/duynamrcv/multi-target_RRT/raw/master/result/path.jpeg" alt="Path" width="70%" >

### Comparisons
<table>
    <tr>
        <td><img src="https://github.com/duynamrcv/multi-target_RRT/raw/master/result/length.jpeg" alt=""></td>
        <td><img src="https://github.com/duynamrcv/multi-target_RRT/raw/master/result/smooth.jpeg" alt=""></td>
        <td><img src="https://github.com/duynamrcv/multi-target_RRT/raw/master/result/time.jpeg" alt=""></td>
    </tr>
</table>
