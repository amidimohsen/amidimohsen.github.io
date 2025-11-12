---
layout: default
title: Projects
permalink: /projects/
---

<link rel="stylesheet" href="/custom.css">

<!-- Name and Title -->
<div class="header-intro">
  <h1>Mohsen Amidzadeh</h1>
  <p>Postdoctoral Researcher | Stochastic Control & Reinforcement Learning</p>
</div>

<!-- Top navigation -->
<nav class="topnav">
  <a href="/">Home</a>
  <a href="/publications">Publications</a>
  <a href="/projects">Projects</a>
  <a href="/contact">Contact / CV</a>
</nav>

<!-- Page Content -->
<div class="projects-list">
  <h2>Projects</h2>

  <!-- Project Entry 1 -->
  <div class="project-entry">
    <h3>Reinforcement Learning Algorithms for Forward-Backward Markov Decision Processes</h3>
    <p>In this project, the notion of forward-backward Markov decision processes (FB-MDPs) is introduced, for the first time, and its application has been studied. We develop new RL theory for this project, and devise nolve bidirectional learning algorithm sitable to FB-MDPs. We also discover the connection between FB-MDPs and forward-backward stochastic differentil equations.</p>

    <div class="project-gallery">
      <div class="gallery-item">
        <img src="/assets/FB-MDPv3.png" alt="An exemplary illustration of a FB-MDP" class="gallery-img">
        <p class="gallery-caption">An examplery illustration of a FB-MDP: forward states <strong>$s_t$</strong> and backward states  <strong>y_t</strong> apply the same actions <strong>a_t</strong>, but with a different ordering in time. Moreover, FB-MDPs includes forward transition probability determining the evolution of the forward state and backward transition probability specifying the evolution of the backward state.</p>
      </div>
      <div class="gallery-item">
        <img src="/assets/fwbw-moac-1.png" alt="Diagram of FB-MOAC" class="gallery-img">
        <p class="gallery-caption">Diagram of FB-MOAC, an RL algorithm for FB-MDPs: The FB-MOAC algorithm consists <strong>forward evaluation</strong>, <strong>backward evaluation</strong> and <strong>bidirectional learning</strong> steps. During the first two steps, the forward and backward dynamics are evaluated, using forward/backward critics, and the resulting experiences are buffered. By a proper chronological order, the policy distribution is optimized in the bidirectional learning step based on the experiences of both forward and backward dynamics and using a <strong>forward-backward multi-objective learning</strong>. The algorithm is additionally equipped with an add-on <strong>episodic MCS-average</strong> to boost the convergence to Pareto-optimal solutions.</p>
      </div>
      <div class="gallery-item">
        <img src="/assets/fwbw-moac-2.png" alt="Forward-Backward Multi-Objective Optimization mechanism" class="gallery-img">
        <p class="gallery-caption">Forward-Backward Multi-Objective Optimization mechanism of FB-MOAC: This step first computes the vector-valued gradients of forward and backward objectives, then compute the descent direction q(.) to ensure that all rewards increase simultaneously, and finally update the parameters of actor network based on q(.).</p>
      </div>
    </div>
    
    <p><a href="https://openreview.net/pdf?id=li5DyC6rfS" class="publication-link" target="_blank">View Publication: FB-MOAC</a></p>
  </div>

  <!-- Project Entry 2 -->
  <div class="project-entry">
    <h3>Malliavin-based Iterative ALgorithms for Stochastic Optimal Control Problems</h3>
    <p>There exist various iterative algorithms, under framework of stochastic maximum principle, that sequentially find the optimal control decision. However, they are based on the adjoint sensitivity analysis that necessitates simulation of an adjoint process — typically a backward SDE that must simultaneously be adapted to a forward filtration and satisfy a terminal condition — which substantially increases complexity and exacerbates the curse of dimensionality. We instead develop a stochastic maximum principle based on the Malliavin calculus, which enables us to devise iterative algorithms without need of an adjoint process. Our algorithms however need the Malliavin derivative which is hopefully adapted to a backward filtration and as such can be efficiently computed based on a time-reversed computation.</p>
  </div>

  <!-- Project Entry 3 -->
  <div class="project-entry">
    <h3>Multi-Objective Deep Learning Algorithms for Stochastic Control Problems with Forward-Backward Dynamics</h3>
    <p>By introducing the notion of Pareto-optimality for multi-objective stochastic control problems through a novel stochastic maximum principle, we study the utilization of DL techniques to address the challenges of multi-functional SOCPs.</p>
  </div>

</div>
