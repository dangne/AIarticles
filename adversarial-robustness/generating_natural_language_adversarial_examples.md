# Generating Natural Language Adversarial Examples

- Link: https://arxiv.org/pdf/1804.07998.pdf
  - [x] First pass
  - [x] Second pass
  - [x] Third pass
- Key-points:
  - GA Attack. Use Genetic Algorithm (i.e. "black-box population-based optimization algorithm") to generate adversarial examples with similar semantic and syntax with minimum word replacements.
  - Adversarial training fails to defend.
  - **Perturb Subroutine:**
    - Randomly select a word. Compute its N nearest neighbors in GloVe embedding space. Filter out neighbors whose distance is above δ. Use counter-fitting method to ensure the nearest neighbors are synonyms. 
    - Use Google's 1 billion words LM to filter out words that do not fit in the context by ranking their likelihoods and keep only the top K words.
    - From the remaining set of words, pick the one that will maximize the target label prediction probability.
    - Replace the selected word.
  - The selection of which word to replace in the input sentence is done by random sampling with probabilities proportional to the number of neigh-bors each word has within Euclidean distance δ in the counter-fitted embedding space,
  
- Dataset:
  - IMDB
  - SNLI

- Performance:
  - Fool well-trained sentiment analysis and textual entailment models with success rates of 97% and 70%, respectively
