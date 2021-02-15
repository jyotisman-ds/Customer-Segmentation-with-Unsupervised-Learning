# Customer-Segmentation-with-Unsupervised-Learning

- [Overview](#overview)
- [The problem](#the-problem)
- [Technical Details](#technical-details)
- [Credits](#credits)

## Overview

This repo covers an unsupervised learning problem in finance. It leverages credit info. of several thousand customers to segment them into groups with certain characteristics. A KMeans Clustering method is employed to achieve the same.


## The problem

- The problem is based on a Kaggle [dataset](https://www.kaggle.com/arjunbhasin2013/ccdata) to develop a marketing strategy targeting credit card holders based on their credit card usage.
- As the name suggests it is an unsupervised problem as there are no labels for the data. So, idea here will be to divide customers into segments based on their similarities in the feature space considered.

## Technical Details

- The details are in the [notebook](https://github.com/jyotisman-ds/Customer-Segmentation-with-Unsupervised-Learning/blob/main/Performing_Customer_Segmentation.ipynb). Techniques employed include clustering techniques like (*Kmeans*) and dimensionality reduction techniques like Principal Component Analysis ((*PCA*)) and (*Autoencoders*). The dataset consists of around 9000 observations with 18 different features.
- Extensive use of visualizations to explore the dataset. One thing that gets immediately clear is that most variables have a narrow spread of values with a few that stand out as a clear differentiator, for example 'PURCHASES_FREQUENCY'.
- Not to say that the other variables are not predictive, but the clustering might create imbalances in the explicit counts in each category. This is what we actually see as well.
- Coming to the technical aspects of the unsupervised learning, We use the elbow technique to find the optimal clusters needed. We do it manually as well as use the 'KElbowVisulaizer' from yellowbrick.
- Some of the clusters are clearly differentiable under certain brackets and we try explain them in our notebook.
- We use PCA mostly for demonstration purposes and also to visualize the clusters if at all a 2-component formulation of the problem was possible.
- We also use deep learning mostly as a dimensionality reduction technique. We employ a simple autoencoder using only dense layers to encode a 10 dimensional representation of the dataset. This is followed by a second KMeans on this reduced dataset and we now end up with 5 clusters as opposed to 5 previously.

## Credits

I am deeply thankful to Udemy and all the instructors for hosting this wonderful course for [machine learning in Finance](https://www.udemy.com/course/ml-and-python-in-finance-real-cases-and-practical-solutions/). My curiosity to learn Machine Learning/deep learning applications led me to this course and I am glad not only to have learnt some useful techniques but also a great deal about the world of finance in general.
