# Neural Architecture Search: A Survey

- Link: https://www.jmlr.org/papers/volume20/18-598/18-598.pdf
  - [x] First pass
  - [x] Second pass
  - [x] Third pass
- Key-points:
  - **Search space**: The search space defines which neural architectures a NAS approach might discover in
principle
    - **Chain-structured neural networks**: simple sequentially-stacked NN
    - **Multi-branch networks**: incorporates more complex design e.g. skip connection. 
    - **Cells or blocks search**: [Zoph et al. (2018)](https://arxiv.org/pdf/1707.07012.pdf) and [Zhong et al. (2018)](https://arxiv.org/pdf/1708.05552.pdf), Search for **cells** or **blocks** architectures, respectively, instead of searching the whole architecture. 
      - **Advantages**:
        - The size of the search space is drastically reduced since cells usually consist of significantly less layers than whole architectures (Zoph estimate a 7-times speed-up)
        - Architectures built from cells can more easily be transferred or adapted to other data sets by simply varying the number of cells and filters used within a model
        - Creating architectures by repeating building blocks has proven a useful design principle in general, such as repeating an LSTM block in RNNs or stacking a residual block.
      - **=> But how do we choose the macro-architecture?** 
        - [Zoph et al. (2018)](https://arxiv.org/pdf/1707.07012.pdf) used sequential model
        - [Cai et al. (2018b)](https://arxiv.org/abs/1806.02639) employ the architecture of well-known model, e.g. DenseNet
        - [Liu et al. (2018b)](https://arxiv.org/abs/1711.00436) hierarchical search space
  - **Search strategy**:
    - Random search, Bayesian optimization, evolutionary methods, reinforcement learning (RL), and gradient-based methods
  - **Performance estimation strategy**:
    - ![](/home/dang/Documents/paper-notes/neural-architecture-search/img/methods_for_speeding_up_performance_estimation.png)

