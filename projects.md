

# Reinforcement Learning Algorithms for Forward-Backward Markov Decision Processes
In this project, the notion of forward-backward Markov decision processes (FB-MDPs) is introduced, for the first time, and its application has been studied.
We develop new RL theory for this project, and devise nolve bidirectional learning algorithm sitable to FB-MDPs.
We also discover the connection between FB-MDPs and forward-backward stochastic differentil equations.


|  An examplery illustration of a FB-MDP  |Diagram of FB-MOAC, an RL algorithm for FB-MDPs|  Forward-Backward Multi-Objective Optimization mechanism of FB-MOAC  |
| :-------------------------:| :-------------------------:| :-------------------------:|
| <img src="assets/FB-MDPv3.png" alt="Alt Text" style="width:200px;"> |<img src="assets/fwbw-moac-1.png" alt="Alt Text" style="width:200px;">  |  <img src="assets/fwbw-moac-2.png" alt="Alt Text" style="width:150px;"> |
|forward states **$s_t$** and backward states  **y_t** apply the same actions **a_t**, but with a different ordering in time. Moreover, FB-MDPs includes forward transition probability determining the evolution of the forward state and backward transition probability specifying the evolution of the backward state.|The FB-MOAC algorithm consists **forward evaluation**, **backward evaluation** and **bidirectional learning** steps. During the first two steps, the forward and backward dynamics are evaluated, using forward/backward critics, and the resulting experiences are buffered. By a proper chronological order, the policy distribution is optimized in the bidirectional learning step based on the experiences of both forward and backward dynamics and using a **forward-backward multi-objective learning**. The algorithm is additionally equipped with an add-on **episodic MCS-average** to boost the convergence to Pareto-optimal solutions. | This step first computes the vector-valued gradients of forward and backward objectives, then compute the descent direction q(\.) to ensure that all rewards increase simultaneously,  and finally update the parameters of actor network based on q(.).|

[publication: FB-MOAC: A Reinforcement Learning Algorithm
for Forward-Backward Markov Decision Processes](https://openreview.net/pdf?id=li5DyC6rfS)


# Malliavin-based Iterative ALgorithms for Stochastic Optimal Control Problems
There exist various iterative algorithms, under framework of stochastic maximum principle, that sequentially
find the optimal control decision.
However, they are based on the adjoint sensitivity analysis that necessitates simulation of an adjoint process 
— typically a backward SDE that must simultaneously be adapted to a forward filtration and satisfy a terminal condition 
— which substantially increases complexity and exacerbates the curse of dimensionality.
We instead develop a stochastic maximum principle based on the Malliavin calculus,
which enables us to devise iterative algorithms without need of an adjoint process.
Our algorithms however need the Malliavin derivative which is hopefully adapted to a backward filtration
and as such can be efficiently computed based on a time-reversed computation.


# Multi-Objective Deep Learning Algorithms for Stochastic Control Problems with Forward-Backward Dynamics
By introducing the notion of Pareto-optimality for multi-objective stochastic control problems 
through a novel stochastic maximum principle, we study  the utilization of DL techniques to address the challenges of multi-functional SOCPs.
