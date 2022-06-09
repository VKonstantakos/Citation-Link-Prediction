# Citation-Link-Prediction
Building a model to predict whether a paper cites another paper.

 ## Table of contents

* [Introduction](#Introduction)
* [Data](#Data)
* [Code](#Code)
* [Methods](#Methods)
* [Support](#Support)

## Introduction

Link prediction is the problem of predicting the existence of a link between two entities in a network. In this project, we deal with the problem of predicting whether a research paper cites another research paper. We are given a citation network consisting of several thousands of research papers, along with their abstracts and their list of authors. The pipeline that is typically followed to deal with the problem is similar to the one applied in any classification problem; the goal is to use edge information to learn the parameters of a classifier and then to use the classifier to predict whether two nodes are linked by an edge or not.

## Data

You can download the data [here](https://drive.google.com/drive/folders/1YtvcvyWoQASn0OhQOBVEK10NnZq08Ndz?usp=sharing). It contains information about the edges of the network, as well as the abstracts and authors of the papers. You can also download the embeddings we generated [here](https://drive.google.com/drive/folders/1BdKare4opRmOQiSQyjUEtCYylqPt4GqA?usp=sharing). They must be respectively placed in the folders `data/` and `embeddings/`.

## Code

All jupyter notebooks can be run in Google Colab without any changes after placing the data (and embeddings) at the appropriate paths.

- Node2Vec_embeddings.ipynb: used to generate and save the Node2Vec embeddings.
- SciBERT_Embeddings.ipynb: used to generate and save the SciBERT embeddings.
- Final submission.ipynb: used to create the final feature set, train the models, and provide the final submission file.

## Methods

- Data Pre-processing:
  - Tokenization
  - Lemmatization
  - Data Cleaning
- Feature creation:
    - TF-IDF vectorizer
    - Node2Vec embeddings
    - SciBERT embeddings
    - Graph features:
        - Degree
        - Overlap
        - Common neighbors
        - Adamic–Adar index
        - Preferential attachment
- Models:
  - CatBoost Classifier
  - LightGBM Classifier
  - XGBoost Classifier

## Support

For questions, email vkonstantakos@iit.demokritos.gr
