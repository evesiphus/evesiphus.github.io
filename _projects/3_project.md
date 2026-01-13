---
layout: page
title: Spatiotemporal Modeling & Learning for Dynamic Networks
description: "Ph.D. Research: Integrating Stochastic Geometry, Queueing Theory, and Reinforcement Learning."
img: assets/img/publication_preview/finite_queue.jpg
importance: 3
category: Research
related_publications: false
---

This research, conducted during my Ph.D. at **IETR & CNRS**, addresses the fundamental limits of coverage and stability in large-scale random networks by jointly considering spatial topology and temporal traffic dynamics.

### 1. Tractable Mathematical Modeling
We developed analytical frameworks to characterize the performance of downlink cellular networks with random link distances. Unlike static models, our work accounts for:
* **Coverage Probability:** Analyzed under various interference scenarios.
* **Queueing Performance:** Modeled both **infinite and finite buffer** scenarios to derive packet loss probability and queue delay.



### 2. The $\epsilon$-Stable Region
A key contribution of this work is the characterization of the **$\epsilon$-stable region**. We defined this as the set of arrival rates where the proportion of unstable queues in the network remains below a threshold $\epsilon$. This provides a new metric for assessing the reliability of large-scale dynamic networks with multi-cell interference.

### 3. Learning-based Transmission Policies
To optimize network performance under uncertainty, we explored policies based on Channel State Information (CSI) and queue states:
* **MDP Framework:** Modeled the transmission process as a Markov Decision Process with an infinite horizon.
* **Reinforcement Learning:** Applied online RL algorithms to minimize transmission costs and buffer delays at base stations, adapting to dynamic interference and traffic fluctuations.

---

### Technical Highlights
* **Theoretical Tools:** Stochastic Geometry (Poisson Point Processes), Queueing Theory ($M/G/1$ systems), Markov Decision Processes (MDP).
* **Optimization:** Reinforcement Learning (Q-Learning/Actor-Critic), Constrained Optimization.

> Related Publications:
> * *$\epsilon$-stable region analysis in dynamic downlink cellular networks*, VTC 2022.
> * *Queue analysis with finite buffer by stochastic geometry*, VTC 2021.
