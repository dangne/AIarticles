# The Evolved Transformer

- Link: https://arxiv.org/pdf/1901.11117.pdf
  - [x] First pass
  - [x] Second pass
  - [x] Third pass
- Key-points:
  - Use NAS to search for a better architecture of Transformer
  - Use evolution-based architecture search
  - Use tournament selection with the aging regularization omitted
    - First, define a **gene encoding** that describes a NN architecture. A child model’s genetic encoding is expressed as: [left input, left normalization, left layer, left relative output dimension, left activation, right input, right normalization, right layer, right relative output dimension, right activation, combiner function] × 14 + [number of cells] × 2, with the first 6 blocks allocated to the encoder and the latter 8 allocated to the decoder.
    - An initial population is created by randomly sample from the gene encoding space
    - Each individual in the population is trained and assign a fitness score (negative log perplexities on the WMT’14 En-De validation set)
    - Then select best individuals for the next generation
    - Repeat until converge
  - To quickly identify promising models without having to fully train, they propose a method **Progressive Dynamic Hurdles (PDH)** 
- Performances:
  - The Evolved Transformer shows a consistent improvement over four well-established language tasks: WMT 2014 English-German, WMT 2014 English-French, WMT 2014 EnglishCzech and LM1B.
  - ![](https://github.com/dangne/paper-notes/blob/img/evolved_transformer.png?raw=true)
  - ![](https://github.com/dangne/paper-notes/blob/img/evolved_transformer_comparison.png?raw=true)

