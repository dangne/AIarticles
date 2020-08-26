# Adversarial Examples Are Not Bugs, They Are Features

- Link: https://arxiv.org/pdf/1905.02175.pdf
  - [x] First pass
  - [x] Second pass
  - [ ] Third pass
- Key-points:
  - The paper shows that in our datasets exist two types of features:
    - Robust feature: Normal feature that is comprehensible to human
    - Non-robust feature: Incomprehensible to human but have high predictive power for classifiers
  - Standard classifiers exploit both types of these features to perform prediction.
  - The reason why adversarial examples can fool classifiers easily but appear normal to human eyes is because most of the non-robust features (incomprehensible, highly predictive) point toward the wrong class while robust features (comprehensible, less predictive) point toward the correct class 
  - The authors were able to split the non-robust and robust features into different datasets.
    - The robust dataset (contains only robust features): yields high accuracy and high robustness
    - The non-robust dataset (contains only non-robust features): yield high accuracy but low robustness
  - This also shows that only the non-robust features (appears to be like random noise and incomprehensible to human eyes) are sufficient for classifier to achieve high accuracy.
  - It also explains the transferability of the adversarial examples - which is because classifiers all learn from the same non-robust (highly predictive) features.
- Dataset:
  - CIFAR-10
  - ImageNet
