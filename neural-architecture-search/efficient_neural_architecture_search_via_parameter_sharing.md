# Efficient Neural Architecture Search via Parameter Sharing

- Link: https://arxiv.org/pdf/1802.03268.pdf
  - [x] First pass
  - [x] Second pass
  - [ ] Third pass
- Key-points:
  - Central to the idea of ENAS is the observation that all of the graphs which NAS ends up iterating over can be viewed as sub-graphs of a larger graph.
  - ENAS uses a controller (an RNN) to discover an optimal sub-graph within a larger computational graph
  - The controller sample children models from a distribution
- Training process:
    - Freeze controller, train child models (the paramaters) with cross entropy loss on training set
    - Freeze child models (the parameters), train the controller with policy gradient on validation set
  - The shared parameters is what help the searching process much faster.
- Performances:
