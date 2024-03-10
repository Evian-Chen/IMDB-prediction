# IMDB-prediction
## Overview
This is a practice project of NLP with transformer architecture. Using IMDB dataset, the model is trained to predict whether a comment is positive or negative.

## Dataset
IMDB dataset has 50K movie reviews.
> This is a dataset for binary sentiment classification containing substantially more data than previous benchmark datasets. We provide a set of 25,000 highly polar movie reviews for training and 25,000 for testing. So, predict the number of positive and negative reviews using either classification or deep learning algorithms.

The csv file looks like:
| review | sentiment | 
|-------|:-----:|
| This show pulls no punches...   | positive  |
| because two people are kille...  |  negative  | 
| ... | ... |
| Robert Colomb has two full-time... |  negative  | 

## Methodology
* Data Preproccessing
  * After reading in the data, use one hot encoding on labels. Positive to 1, negative to 0.
  * Replace uncnssary tokens in every review with spaces.
  * Give every token an index. (indexing)
  * Turn tokens into indexs and split data into training and validation.
* Model Setting
  * Word embedding, give every word a vector.
  * Positonal encoding, give every word a positional vector with the same dimension with word embedding.
  * Multi-head attention, do the QKV calculation from paper.
  * Feed forwarding, use two linear function and one ReLU activation.
  * Normalization, both feed forward and multi-head attention need normalization.
* Training
  * Use the above architecture to train the model.

## References
<a href="https://arxiv.org/abs/1706.03762">Attention Is All You Need</a>

<a href="https://medium.com/ml-note/word-embedding-3ca60663999d">Word Embeddings</a>

<a href="https://machinelearningmastery.com/the-transformer-model/">The Transformer Model</a>

<a href="https://youtu.be/ugWDIIOHtPA?si=U7t-7csnvTG4kK0T">李宏毅教授-Transformer</a>

<a href="https://www.kaggle.com/datasets/lakshmi25npathi/imdb-dataset-of-50k-movie-reviews/discussion">IMDB Dataset of 50K Movie Reviews</a>
