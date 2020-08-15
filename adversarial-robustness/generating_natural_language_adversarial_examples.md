# Generating Natural Language Adversarial Examples

- Link: https://arxiv.org/pdf/1804.07998.pdf
  - [x] First pass
  - [x] Second pass
  - [x] Third pass
- Key-points:
  - Use Genetic Algorithm (i.e. "black-box population-based optimization algorithm") to generate adversarial examples with similar semantic and syntax with minimum word replacements. (GA attack)
  
  - Adversarial training fails to improve the robustness. (fails to defend)
  
- Dataset:
  - IMDB: Sentiment analysis
  - SNLI: Textual entailment

- Performance:
  - Fool well-trained sentiment analysis and textual entailment models with success rates of 97% and 70%, respectively
