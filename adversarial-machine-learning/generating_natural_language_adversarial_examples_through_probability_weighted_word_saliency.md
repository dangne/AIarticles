# Generating Natural Language Adversarial Examples through Probability Weighted Word Saliency

- Link: https://www.aclweb.org/anthology/P19-1103.pdf
  - [x] First pass
  - [x] Second pass
  - [x] Third pass
- Key-points:
  - PWWS attack
  - **Word Substitution Strategy:** For each word <img src="https://latex.codecogs.com/gif.latex?w_i" title="w_i" />, find its synonyms using WordNet. If it is a Name Entity (NE), find NEs that have the same type. Select the one that causes the most significant change in the classification probability after replacement <img src="https://latex.codecogs.com/gif.latex?w^*_i" title="w^*_i" /> (i.e. maximize <img src="https://latex.codecogs.com/gif.latex?\dpi{110}&space;\Delta&space;P^{*}_{i}&space;=&space;P\left&space;(&space;y_{\text{\textbf{true}}}\mid&space;\mathbf{x}&space;\right&space;)&space;-&space;P\left&space;(&space;y_{\text{\textbf{true}}}\mid&space;\mathbf{x}^{*}_{i}&space;\right&space;)" title="\Delta P^{*}_{i} = P\left ( y_{\text{\textbf{true}}}\mid \mathbf{x} \right ) - P\left ( y_{\text{\textbf{true}}}\mid \mathbf{x}^{*}_{i} \right )" />)
  - **Replacement Order Strategy:** Sort the <img src="https://latex.codecogs.com/gif.latex?w_i" title="w_i" /> by it's H score. Where <img src="https://latex.codecogs.com/gif.latex?H(\mathbf{x},&space;\mathbf{x}^*_i,&space;w_i)&space;=&space;\phi&space;(\mathbf{S}(x))_i&space;\cdot&space;\Delta&space;P^*_i" title="H(\mathbf{x}, \mathbf{x}^*_i, w_i) = \phi (\mathbf{S}(x))_i \cdot \Delta P^*_i" /> and <img src="https://latex.codecogs.com/gif.latex?\phi&space;(\mathbf{z})_i" title="\phi (\mathbf{z})_i" /> is the softmax function. Then iteratively replace each <img src="https://latex.codecogs.com/gif.latex?w_i" title="w_i" /> by <img src="https://latex.codecogs.com/gif.latex?w^*_i" title="w^*_i" /> until the victim model misclassify.
- Dataset:
  - IMDB
  - AG's News
  - Yahoo! Answers
- Performance:
  - Unclear PWWS's performance vs GA's performance (Alzantot, 2018)
  - ![](https://github.com/dangne/paper-notes/blob/img/Annotation%202020-08-20%20062829.png?raw=true)
