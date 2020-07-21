---
layout: post
title: "Datawhale X Tianchi NLP - News Text Classification"
categories: ml
author:
- Yi Zhang
---

## TASK 1

### Dataset

#### Train

Number of training samples: 200, 000

Number of classes: 14



#### Test A

Number of training samples: 50, 000



### Task

News text classification



### Metrics

[F1 score](https://en.wikipedia.org/wiki/F1_score)
$$
\text{F1} = 2 \cdot \frac{\text{Precision} \cdot \text{Recall}}{\text{Precision} + \text{Recall}}
$$


### Challenge

* Class imbalance
* Text is encoded, that is hard to be interpreted, i.e., proper embedding or pretaining matter



### Proposed Solutions

1. TF-IDF (LSI) + ML classifier
2. fastText
3. Word2Vec (Skim-Gram) + DL (textCNN, textRNN, BiLSTM...)
4. pretaining, BERT



### Reference

* [Stanford CS224n](http://web.stanford.edu/class/cs224n/)
* [Datawhale NLP: news text classification - Task 1](https://tianchi.aliyun.com/notebook-ai/detail?spm=5176.12586969.1002.6.6406111aIKCSLV&postId=118252)
