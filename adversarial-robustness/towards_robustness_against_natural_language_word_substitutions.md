# Towards Robustness Against Natural Language Word Substitutions

- Link: Proceedings
  - [x] First pass
  - [x] Second pass
  - [ ] Third pass
  
- Key-points:

  - Instead of using l2-ball or axis-align bounds to model the perturbation set, this paper use convex hull which is the smallest convex set that contains all the substitutions.
  
  - ASCC-defense loss: ![](https://github.com/dangne/paper-notes/blob/img/ASCC_loss_function.png?raw=true)
  
    Where the KL term is similar to Miyato et. al. in virtual adversarial training and the H term is the word-level entropy-based regularization: ![](https://github.com/dangne/paper-notes/blob/img/word_level_entropy_based_regularization.png?raw=true)
  
- Dataset:

  - IMDB
  - SNLI

- Performance:

  - ![](https://github.com/dangne/paper-notes/blob/img/ASCC_performance.png?raw=true)
  - ![](https://github.com/dangne/paper-notes/blob/img/ASCC_performance_2.png?raw=true)
  - ![](https://github.com/dangne/paper-notes/blob/img/ASCC_performance_3.png?raw=true)