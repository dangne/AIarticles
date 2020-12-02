# Robustness May Be at Odds with Accuracy

- Link: https://arxiv.org/pdf/1805.12152.pdf
  - [x] First pass
  - [x] Second pass
  - [x] Third pass
- Key-points:
  - The paper shows that there may exist a trade-off between accuracy and robustness (even if we have inifinite data)
  - However, their argument was only demonstrated in a very simple adversarial setting: 
  - Consider this simple adversarial setting: a binary classifier, where the set of input features contains **1 robust feature** (feature that highly correlated with the label) and the rest are **d non-robust features** (features that have very weakly correlation with it). We can easily draw the conclusion that: **If we have sufficiently large d non-robust features, the model can achieve near 100% accuracy without relying on the 1 robust feature (proof in paper)**. And because of this, when apply an adversarial attack on non-robust features, the classifier can easily be fooled.
    - This is where the trade-off between standard accuracy and robustness happens: when we want the classifier to be robust (focus on only the **robust feature**) it ignores the non-robust features and therefore decrease in standard accuracy. In contrast, when we want the classifier to be accurate, the classifier utilize all features (both robust and non-robust ones), which yields high standard accuracy but very vulnarable to adversarial examples.
  - The paper shows that by increasing the adversarial data in training, it improves the robustness but damages the standard accuracy of the model. There **might** be a trade-off between standard accuracy vs robustness (even if we have infite data!).
  - The paper shows that adversarial robustness had some unexpected benefits:
    - The loss gradient of robust models align well with human perception, whereas in standard models, the loss gradients often are noisy and hard to intepret.
    - Adversarial examples exhibit salient data characteristics
    - Smooth cross-class interpolations via gradient descent
- Dataset:
  - MNIST
  - CIFAR-10
  - Restricted ImageNet
