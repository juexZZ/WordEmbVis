# Word Embedding Visualization via Dictionary Learning

[Juexiao Zhang*](https://juexzz.github.io/), [Yubei Chen*](https://yubeichen.com/), [Brian Cheung](https://scholar.google.com/citations?user=7N-ethYAAAAJ&hl=zh-CN) and [Bruno Olshausen](http://www.rctn.org/bruno/)

![Teaser Image](https://github.com/juexzz/WordEmbVis/blob/main/imgs/word-emb-vis.jpg "Teaser Image!")

This repository hosts our work *Word Embedding Visualization via Dictionary Learning*.

The arxiv preprint is at [this link](https://arxiv.org/abs/1910.03833).

## Outline

An outline of the files contained in thie repository:

 - `sparsify_Pytorch.py` is our library for dictionary learning.

 - `WordFactor_reproduce.ipynb` and `FactorGroup_reproduce.ipynb` are our reorginzed and renewed notebooks for to show how to learn a dicionary containing the *word factors* and reproduce the results. The reader can refer to the notebooks for more details

 - `data` directory stores the corpus data used for training, for example text8, [download](http://mattmahoney.net/dc/text8.zip).
 
 - `embeddings` directory stores the pretrained word embeddings, for example the [GloVe](https://nlp.stanford.edu/projects/glove/).
 
 - `results` directory stores the results you can obtain from running the notebooks. Take the provided as an example, `basis.pt` stores the trained dictionary elements, aka the *word factors*. `nmed_factor_cooc.npy` is the normalized factor cooccurrence matrix and `sym_labels_knn20_c175.npy` stores the factor clustering labels. Both are obtained from `FactorGroup_reproduce.ipynb`.
 
## Usage

Follow the instructions in the notebook, particularly `WordFactor_reproduce.ipynb`, and have the corpus and embeddings placed in `data/` and `embeddings` respectively. The reader should be able to reproduce the results of `results/glove-text8-reproduce-1k-factors`. Please refer to the notebooks for specific instructions.

This project is tested with:

 - Python 3.7
 
 - PyTorch 1.1.0
 
 - scipy 1.2.0
 
 - scikit-learn 0.21.2
 
 - matplotlib 3.1.0
 
 - plotly 4.1.1

## Citation

```
@article{DBLP:journals/corr/abs-1910-03833,
  author    = {Juexiao Zhang and
               Yubei Chen and
               Brian Cheung and
               Bruno A. Olshausen},
  title     = {Word Embedding Visualization Via Dictionary Learning},
  journal   = {CoRR},
  volume    = {abs/1910.03833},
  year      = {2019},
  url       = {http://arxiv.org/abs/1910.03833},
  eprinttype = {arXiv},
  eprint    = {1910.03833},
  timestamp = {Wed, 16 Oct 2019 16:25:53 +0200},
  biburl    = {https://dblp.org/rec/journals/corr/abs-1910-03833.bib},
  bibsource = {dblp computer science bibliography, https://dblp.org}
}
```