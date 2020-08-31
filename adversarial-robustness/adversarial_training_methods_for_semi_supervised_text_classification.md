# Adversarial Training Methods For Semi-Supervised Text Classification

- Link: https://arxiv.org/pdf/1605.07725.pdf
  - [x] First pass
  - [x] Second pass
  - [ ] Third pass
- Key-points:
  - Because the set of high-dimensional one-hot vectors does not admit infinitesimal perturbation, we define the perturbation on continuous word embeddings instead of discrete word inputs. 
  - Traditional adversarial and virtual adversarial training can be interpreted both as a regularization strategy and as defense against an adversary who can supply malicious inputs.
  - Apply both **Adversarial Training** and **Virtual Adversarial Training** on models and they improved the word embeddings over the baseline methods.
  - we found that adversarial and virtual adversarial training have good regularization performance in sequence models on text classification tasks. On all datasets, our proposed method exceeded or was on par with the state of the art performance. We also found that adversarial and virtual adversarial training improved not only classification performance but also the quality of word embeddings.
- Dataset:
  - Elec
  - RCV1
  - Rotten Tomatoes sentiment classification task
