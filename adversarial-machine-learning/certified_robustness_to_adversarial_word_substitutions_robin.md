# Certified Robustness to Adversarial Word Substitutions Robin

- Link: https://arxiv.org/pdf/1909.00986.pdf
  - [x] First pass
  - [x] Second pass
  - [ ] Third pass
  
- Key-points:

  - **Interval Bound Propagation:** 
    - Goal: construct the upper-bound of the final loss to put it in the loss function as a regularization term
    - Start from the input layer: construct upper and lower bounds of the input layer
    - Use the bounds of the previous layer to compute the bounds of the current layer (different activation functions need different formula to compute the current layer's bounds)
    - Up until the final layer => and we got the bounds of the loss function

- Dataset:

  - IMDB
  - SNLI

- Performance:

  - IMDB:

    ![IMDB](https://github.com/dangne/paper-notes/blob/img/Screenshot%20from%202020-08-31%2021-05-48.png?raw=true)

  - SNLI:
  
    ![SNLI](https://github.com/dangne/paper-notes/blob/img/Screenshot%20from%202020-08-31%2021-05-53.png?raw=true)

  - ![](https://github.com/dangne/paper-notes/blob/img/Screenshot%20from%202020-08-31%2021-05-59.png?raw=true)