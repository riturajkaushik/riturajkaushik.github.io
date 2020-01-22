---
layout: home
hide: true
title: Rituraj Kaushik
---

## Research Updates

* **Recent paper**: "Adaptive Prior Selection for Repertoire-based Adaptation in Robotics", Frontiers in Robotics & AI (2019) [Read here](https://arxiv.org/abs/1907.07029)
  
    - **Abstract :** Repertoire-based learning is a data-efficient adaptation approach based on a two-step process in which (1) a large and diverse set of policies is learned in simulation, and (2) a planning or learning algorithm chooses the most appropriate policies according to the current situation (e.g., a damaged robot, a new object, etc.). In this paper, we relax the assumption of previous works that a single repertoire is enough for adaptation. Instead, we generate repertoires for many different situations (e.g., with a missing leg, on different floors, etc.) and let our algorithm selects the most useful prior. Our main contribution is an algorithm, APROL (Adaptive Prior selection for Repertoire-based Online Learning) to plan the next action by incorporating these priors when the robot has no information about the current situation. We evaluate APROL on two simulated tasks: (1) pushing unknown objects of various shapes and sizes with a robotic arm and (2) a goal reaching task with a damaged hexapod robot. We compare with "Reset-free Trial and Error" (RTE) and various single repertoire-based baselines. The results show that APROL solves both the tasks in less interaction time than the baselines. Additionally, we demonstrate APROL on a real, damaged hexapod that quickly learns to pick compensatory policies to reach a goal by avoiding obstacles in the path.

	- **Python code for APROL** : [Link to github](https://github.com/resibots/kaushik_2019_aprol)
	- **Video**

	<div align="center">
	<iframe width="790" height="300" src="https://www.youtube.com/embed/sbhW2rdIxA0" frameborder="0" allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
	</div>

* **Paper**: "Multi-objective Model-based Policy Search for Data-efficient Learning with Sparse Rewards" , CoRL 2018 (Z\"urich). [Read here](https://arxiv.org/pdf/1806.09351.pdf)

	- **Abstract :** The most data-efficient algorithms for reinforcement learning in robotics are model-based policy search algorithms, which alternate between learning a dynamical model of the robot and optimizing a policy to maximize the expected return given the model and its uncertainties. However, the current algorithms lack an effective exploration strategy to deal with sparse or misleading reward scenarios: if they do not experience any state with a positive reward during the initial random exploration, it is very unlikely to solve the problem. Here, we propose a novel model-based policy search algorithm, **Multi-DEX**, that leverages a learned dynamical model to efficiently explore the task space and solve tasks with sparse rewards in a few episodes. To achieve this, we frame the policy search problem as a multi-objective, model-based policy optimization problem with three objectives: (1) generate maximally novel state trajectories, (2) maximize the expected return and (3) keep the system in state-space regions for which the model is as accurate as possible. We then optimize these objectives using a Pareto-based multi-objective optimization algorithm. The experiments show that Multi-DEX is able to solve sparse reward scenarios (with a simulated robotic arm) in much lower interaction time than VIME, TRPO, GEP-PG, CMA-ES and Black-DROPS.

	- **C++ codes for Multi-Dex** : [Link to github](https://github.com/resibots/kaushik_2018_multi-dex)
	- **Video**
	<div align="center">
	<iframe width="790" height="300" src="https://www.youtube.com/embed/9ZLwUxAAq6M" frameborder="0" allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
	</div>

## Youtube channel : **[AI Talks - Rituraj Kaushik](https://www.youtube.com/channel/UCwrblBV2g0m8SuG8jQbhjuA/videos?view_as=subscriber)**

Latest videos
<!-- <justify> -->
<div align="left">
<iframe width="790" height="300" src="https://www.youtube.com/embed/HLnGZe-R0Xg" frameborder="0" allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
<iframe width="790" height="300" src="https://www.youtube.com/embed/BAetsPIojg4" frameborder="0" allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
</div>
<!-- </justify> -->