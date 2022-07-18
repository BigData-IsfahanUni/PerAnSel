<span align="center">
    <a href="https://www.kaggle.com/jamshidjdmy/peransel"><img alt="Kaggle" src="https://img.shields.io/static/v1?label=Kaggle&message=PerAnSel&logo=Kaggle&color=20BEFF"/></a>
</span>

# PerAnSel: A Novel Deep Neural Network-based System for Persian Question Answering
About 110 million people from Iran, Tajikistan, Afghanistan, and six other countries speak Persian. The Persian language is: (1) free word order, (2) right-to-left, (3) morphologically-rich, and (4) low-resource. In order to address the need for a high-quality answer selection dataset for the Persian language, we present PASD; the first large-scale native answer selection dataset for the Persian language. PASD contains approximately 100,000 question-answer pairs on [Persian Wikipedia](https://fa.wikipedia.org/) articles and is the first large-scale native answer selection dataset for the Persian language which is created by native annotators. We also translate [WikiQA](https://www.microsoft.com/en-us/download/details.aspx?id=52419) dataset to Persian. To show the quality of PASD, we employed it to train state of the art answer selection systems. Finally, we present PerAnSel: A Novel Deep Neural Network-based System for Persian Question Answering.

# Dataset
### Download
The PASD and WikiFA datasets are available for download from the [`PASD`](https://github.com/BigData-IsfahanUni/PerAnSel/tree/main/PASD) and [`WikiFA`](https://github.com/BigData-IsfahanUni/PerAnSel/tree/main/WikiFA), respectively. The statistics of the PASD and WikiFA are shown below:
|  Split | Train |  Dev |  Test |
| :----: | :---: | :--: | :---: |
|  PASD  | 17567 | 1000 |  1000 |
| WikiFA |  2118 |  396 |  633  |

In the following, question type distribution over PASD dataset is illustrated:
| Question Word | Distribution |
| :-----------: | :----------: |
|      What     |    28.57%    |
|      How      |    15.54%    |
|      When     |    11.00%    |
|     Where     |    13.21%    |
|      Who      |    16.13%    |
|     Which     |    14.61%    |
|      Why      |    00.94%    |
# Evalution
We implement two baseline systems: (1) ASBERT and (2) CETE. We also implement PerAnSel method for persian answer selection whose kernel are MBERT, Distilmbert, ALBERT-FA, ParsBERT. We evaluate each of the answer selection systems according to *MRR* evaluation metric.
|    Method   |       LM     |     PASD    |   WikiFA   |
| :---------: | :----------: | :---------: | :--------: |
|    ASBERT   |     MBERT    |    81.45%   |   51.32%   |
|     CETE    |     MBERT    |    79.99%   |   42.74%   |
|   PerAnSel  |   ParsBERT   |    74.30%   |   50.38%   |
|   PerAnSel  |   AlbertFA   |    77.21%   |   47.59%   |
|   PerAnSel  |  DistilmBert |    81.55%   |   62.66%   |
|   **PerAnSel**  |     **MBERT**    |    **89.36%**   |   **66.08%**   |

We also presented a question classifier which use PASD as the training set and classifies the questions. Here, we evaluate the question classifier both intrinsically and extrinsically.

### Intrinsically
|    Model     |     PASD    |
| :----------: | :---------: |
|   ParsBERT   |    88.20%   |
|   AlbertFA   |    90.70%   |
|  DistilmBert |    95.30%   |
|     **MBERT**    |    **97.90%**   |

### Extrinsically
|    Method   |       LM     |     PASD    |   WikiFA   |
| :---------: | :----------: | :---------: | :--------: |
|   PerAnSel  |     MBERT    |    92.11%   |   62.77%   |

# Citation
### Plain
Jamshid Mozafari, Arefeh Kazemi, Parham Moradi, Mohammad Ali Nematbakhsh, "PerAnSel:  A  Novel Deep Neural Network-Based System for Persian Question Answering", Computational Intelligence and Neuroscience, vol. 2022, Article ID 3661286, 21 pages, 2022. https://doi.org/10.1155/2022/3661286

### Bibtex
```bibtex
﻿@Article{Mozafari2022,
    author={Mozafari, Jamshid and Kazemi, Arefeh and Moradi, Parham and Nematbakhsh, Mohammad Ali},
    title={PerAnSel: A Novel Deep Neural Network-Based System for Persian Question Answering},
    journal={Computational Intelligence and Neuroscience},
    year={2022},
    month={Jul},
    day={18},
    publisher={Hindawi},
    volume={2022},
    pages={3661286},
    issn={1687-5265},
    doi={https://doi.org/10.1155/2022/3661286}
}
```
