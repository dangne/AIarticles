# Adversarial Examples Are Not Bugs, They Are Features

- Link: https://arxiv.org/pdf/1905.02175.pdf
  - [x] First pass
  - [ ] Second pass
  - [ ] Third pass
- Key-points:
  - The paper shows that all of our datasets contain "non-robust" features that are incomprehensible to human but highly predictive for standard classifiers. Classifiers exploit both robust and non-robust features to perform prediction and the paper suggests that we should not be surprised when classifiers do that. 
- The authors were able to split the non-robust features from the dataset that help classifiers to achieve good standard accuracy and good robust accuracy at the same time.
- Dataset:
  - CIFAR-10
  - ImageNet
