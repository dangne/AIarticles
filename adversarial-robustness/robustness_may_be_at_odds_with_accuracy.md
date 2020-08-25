# Robustness May Be at Odds with Accuracy

- Link: https://arxiv.org/pdf/1805.12152.pdf
  - [x] First pass
  - [x] Second pass
  - [ ] Third pass
- Key-points:
  - The paper shows that by increasing the adversarial data in training, it improves the robustness but damages the standard accuracy of the model. There **might** be a trade-off between standard accuracy vs robustness (even if we have infite data!).
  - The paper shows that adversarial robustness had some unexpected benefits:
    - The loss gradient of robust models align well with human perception, whereas in standard models, the loss gradients often are noisy and hard to intepret.
    - Adversarial examples exhibit salient data characteristics
    - Smooth cross-class interpolations via gradient descent
- Dataset:
  - MNIST
  - CIFAR-10
  - Restricted ImageNet
