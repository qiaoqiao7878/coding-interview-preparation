# Machine learning

Machine learning
- Supervised Learning
  - Classification
  - Regression
- Unsupervised Learning\
  Find struture in unlabeled data
  - Clustering\
    Group simliar objects together
  - Dimensionality Reduction\
    Project down high-dimensional data
  - Generalive Modeling\
    Generate new 'realistic' data
- Reinforcement learning\
  Learning by intercting with a dynamic environment

### Decision tree

- Entropy
- Gini index

can handle any combination of numerical and categorical features and targets

### K-fold cross validation

### k-Nearest Neighbor

vector is labeled by the mode of its neighbors' labels

weighted version: pick the weighted majority label, the weight is inverserly proportional to the distance

How to pick k?\
Use validation set

### Confusion table
Presision = TP/(TP + FP)
Recall = TP/(TP + FN)

Be careful when you have imbalanced classes

Problem with too high dimensional data

#### Handel scaling issues
- Data standardization\
Scale each features to zero mean and unit variances
- Use Mahalanobis distance

### Probability

i.i.d independent and identically distributed


### Linear regression

Control overfitting with regularization

Bias-variance tradeoff
- Bias: expected error due to model mismatch
- Variance: variation due to randomness in training data

High bias: model is too rigid, or regularization too high、
High variance: model is too flexible, captures noise in the data, overfitting\
typically happens when model has high capacity, or regularization

### Logistic regression
- binary classification
  sigmoid function
- multi-class
  softmax function\
  cross entropy
  
## Dimensionality Reduction
Reduce the dimensionality while avoiding information loss
Benefits:\
- Less storage required
- Faster processing possible
  
### Principal Component Analysis (PCA)
Transform the data, such that the covariance between the new dimensions is 0
1. Center the data
2. Computer the covariance matrix
3. Use the eigenvector decomposition to transform the coordinate system

### K-means 
1. Initialize the centroids
2. Update cluster indicators
3. Update centroids
4. It objective has not converged, return to step 2

