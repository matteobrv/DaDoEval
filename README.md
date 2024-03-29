## DaDoEval at Evalita 2020 - An SVM-based approach for Automatic Document Dating

Temporal information, such as the publication date of a document, is of major relevance in a number of domains. Building on this idea, the [**DaDoEval**](https://dhfbk.github.io/DaDoEval/) – Dating Document Evaluation – shared task, hosted at [Evalita 2020](http://www.evalita.it/2020), invites participants to tackle a series of automatic document dating sub-tasks, working with documents related to Italian statesman [Alcide De Gasperi](https://en.wikipedia.org/wiki/Alcide_De_Gasperi).

This repository stores the data and the implementation for my solution to the first two sub-tasks: *Coarse-grained classification on same-genre data* and *Coarse-grained classification on cross-genre data*.
Both sub-tasks require to correctly assign document samples to one out of five historical periods identified in De Gasperi’s political life, spanning a range of over fifty years from 1901 to 1954.

| Habsburg years | Beginning of political activity | Internal exile | From fascism to the Italian Republic | Building the Italian Republic |
|:--------------:|:-------------------------------:|:--------------:|:------------------------------------:|:-----------------------------:|
|    1901-1918   |            1919-1926            |    1927-1942   |               1943-1947              |           1948-1954           |


The solution is based on a linear multi-class Support Vector Machine classifier trained on a combination of character and word n-grams, as well as number of word tokens per document.

A detailed description of the approach is outlined in my [system description paper](http://ceur-ws.org/Vol-2765/paper96.pdf), while the code is available in the [DaDoEval_2020 notebook](DaDoEval_2020.ipynb).

Despite its simplicity, the system ranked first in both sub-tasks, achieving a macro-average F1 score of 0.934 and 0.413, respectively.

#### Requirements

```text
python 3.6
numpy 1.19.2
matplotlib 3.3.2
scikit-learn 0.23.2
scikit-optimize 0.8.1
```
