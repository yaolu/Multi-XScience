# Multi-XScience

Dataset for the EMNLP 2020 paper, [Multi-XScience: A Large-scale Dataset for Extreme Multi-document Summarization of Scientific Articles](https://arxiv.org/abs/2010.14235).

Authors: [Yao Lu](https://yaolu.github.io), [Yue Dong](https://www.cs.mcgill.ca/~ydong26/), [Laurent Charlin](http://www.cs.toronto.edu/~lcharlin/)

# Dataset Statistics

| train/val/test     | average document length | summary length | number of references |
| ------------------ | ----------------------- | -------------- | -------------------- |
| 30,369/5,066/5,093 | 778.08                  | 116.44         | 4.42                 |



We also calculate the percentage of novel n-grams in the target summary of previous datasets. Three of them are single-document summarization datasets. Our dataset has the highest abstractiveness among all existing multi-document summarization datasets.

|        Datasets        | % of novel unigrams | % of novel bi-grams | % of novel tri-grams | % of novel 4-grams |
| :--------------------: | :-----------------: | :-----------------: | :------------------: | :----------------: |
| CNN-DailyMail (single) |        17.00        |        53.91        |        71.98         |       80.29        |
|   NY Times (single)    |        22.64        |        55.59        |        71.93         |       80.16        |
|     XSum (single)      |        35.76        |        83.45        |        95.50         |       98.49        |
|        WikiSum         |        18.20        |        51.88        |        69.82         |       78.16        |
|       Multi-News       |        17.76        |        57.10        |        75.71         |       82.30        |
|     Multi-XScience     |        42.33        |        81.75        |        94.57         |       97.62        |

# Dataset Format

| key                          | description                                                  |
| ---------------------------- | ------------------------------------------------------------ |
| aid                          | arxiv id (e.g. 2010.14235)                                   |
| mid                          | microsoft academic graph id                                  |
| abstract                     | text of paper abstract                                       |
| ref_abstract                 | meta-information of reference papers                         |
| ref_abstract.cite_N          | meta-information of reference paper cite_N (special cite symbol) |
| ref_abstract.cite_N.mid      | reference paper's (cite_N) microsoft academic graph id       |
| ref_abstract.cite_N.abstract | text of reference paper (cite_N) abstract                    |

# Extended Usage

Our dataset is aligned with [Microsoft Academic Graph](https://www.microsoft.com/en-us/research/project/microsoft-academic-graph/). Anyone interested in the intersection of graph and summarization can use our dataset for exploration.

