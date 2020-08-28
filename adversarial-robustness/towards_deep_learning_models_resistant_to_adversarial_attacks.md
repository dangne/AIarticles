# Towards Deep Learning Models Resistant to Adversarial Attacks

- Link: https://arxiv.org/pdf/1706.06083.pdf
  - [x] First pass
  - [x] Second pass
  - [x] Third pass
- Key-points:
  - New terms:
    - **The saddle point problem:** The universal adversarial empirical risk minimization (adversarial ERM) problem:
    <p align="center"><img src="https://latex.codecogs.com/png.latex?\min_{\theta}&space;\underset{(x,&space;y)\sim&space;D}{\mathbb{E}}&space;\left&space;[&space;\max_{\delta&space;\in&space;S}{&space;L\left&space;(&space;\theta,x&plus;\delta,&space;y&space;\right&space;)}&space;\right&space;]" title="\min_{\theta} \underset{(x, y)\sim D}{\mathbb{E}} \left [ \max_{\delta \in S}{ L\left ( \theta,x+\delta, y \right )} \right ]" /></p>
    - **Inner-maximization problem (attack):** aims to find an adversarial version of a given data point x that achieves a high loss (corresponds to the max term inside the square brackets)
    - **Outer-minimization problem (defense):** find model parameters so that the “adversarial loss” given by the inner attack problem is minimized (corresponds to the min term outside the square brackets)
    - **First-order attack (white-box attack?):** 
    - **Zero-order attack (black-box attack?):** attacks in which the adversary has no direct access to the classifier and is only able to evaluate it on chosen examples without gradient feedback.
    - **Danskin's theorem**
    
  - The paper provides an optimization view of the adversarial problems, gives it a clear mathematical formulation.
  
  - If we train the network to be robust against Projected Gradient Descent (PGD) adversaries, it will be robust against a wide range of attacks that encompasses all current approaches
  
  - **Capacity alone helps:** 
  
  - **FGSM adversaries don’t increase robustness (for large ε):**
  
  - **Weak models may fail to learn non-trivial classifiers:**
  
  - **The value of the saddle point problem decreases as we increase the capacity:**
  
  - **More capacity and stronger adversaries decrease transferability:**
- *Dataset:
  
  - MNIST
  - CIFAR10

