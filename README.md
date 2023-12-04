# Deep Clustering for Unsupervised Learning of Visual Features

## Overview
This GitHub repository contains the implementation of a deep clustering method for unsupervised learning of visual features. Traditional supervised learning methods often require large annotated datasets, which can be time-consuming and challenging to obtain. This project aims to address this issue by leveraging unsupervised learning, using a deep clustering approach to learn meaningful representations of visual features without the need for annotations.

## Motivation
The motivation behind this project is to explore alternative approaches to training deep learning models, specifically in scenarios where obtaining large labeled datasets is difficult. By using deep clustering method, the goal is to make use of unlabelled data to learn valuable visual representations.

## Problem Statement
Most deep learning models demand a significant amount of labeled data for training. Manual annotation of datasets is a time-intensive process, and the absence of annotations can hinder the learning process. The challenge is to create a deep clustering method that effectively learns visual features without relying on annotations.

## Solution
The proposed solution involves the following steps:
1. Utilize a clustering algorithm, such as K-means, to cluster image representations.
2. Use these cluster assignments as pseudo-labels for the data and train the model end-to-end.

## Scope
- Adapt unsupervised learning to the end-to-end training of visual features.
- Develop DeepCluster, a clustering method that jointly learns the parameters of the network and the cluster assignments of the resulting features.
- DeepCluster iteratively groups the features with a standard clustering algorithm and uses these cluster assignments as labels.

## Implementation
- **Dataset:** CIFAR10
- **Components:**
  - Convnet: Alexnet
  - Clustering Algorithm: K-means
  - Dimensionality Reduction: PCA

1. Retrieve image representations from the pre-trained model (Alexnet).
2. Perform dimensionality reduction before clustering.
3. Cluster these image representations.
4. Use cluster labels as pseudo-labels for the data.
5. Re-train the model end-to-end using these labels.
6. Repeat the process.

## Experiments
- Number of epochs
- Number of reassignments
- Choosing the number of clusters

## Analysis
- Initial accuracy of pre-trained AlexNet was low; fine-tuned for CIFAR10.
- General upward trend in NMI graphs, suggesting improved representation learning.
- Better results with lower k values, indicating a well-separated dataset (CIFAR10).

## References
- [Devin A. et al. Deep Clustering for Unsupervised Learning of Visual Features. In: Proceedings of the 31st International Conference on Machine Learning (ICML 2014), JMLR Workshop and Conference Proceedings vol 32, 2014.](reference_link)
