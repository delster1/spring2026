---
tags:
    - eecs649
---

# Intro to AI - Lec2

ML - take data and learn from it!

## **broad machine learning tasks:** 

1. classification \
                    - both supervised learning - learn from labeled training data
2. regression     /
3. clustering                   \
                                 - unsupervised learning - learn from unlabeled training data
4. dimensioinality reduction    /

### classification
Take info labels and features to classify information into one of specified categories

### regression

Take label and features and use "regressor" to predict information about something
- labels are continuous and ordered 

### clustering

*input* : vectors $x_1,...,x_n$ and number of clusters $ k ( << n)$
*output* : predicted classes $y_1,...y_n \in \Sigma_{1..k}$

identifies clusters and groups in data

### dimensionality reduction
EX: reducing / compressing large-dimensionality vector into smaller-dimensionality vector 

applications: 
- visualization & analysis
- data processing

methods:
- principal component analysis
- kernel principal component analysis 
- manifold learning 
- autoencoder 
- linear discriminant analysis

**Misc.**
    Ranking, recommendatoin, RL, etc.

## ML tasks in practice

Modeling:
- Neural Networks
- Tend to use pre-existing models
- This is a large area of research

Computation:
- Computation of loss

## Types of models

### Linear model 
- feature vector  - $x \in R^d$
    - ex: features of a house
- prediction - $f(x) = x^Tw$
    - ex: housing price

**goal:** - how to find w?
- training features: $x_1,...,x_n \in \Reals ^d$
- training targets: $y_1, ..., y_n \in \Reals$
- Loss function: $L(w)=\frac{1}{n}\Sum{i=1}{n}(x_i^Tw-y_i)^2$
- Least squares regression: $w^* = minL(w)$

**limitations:** 
not expressive for complicated tasks! 
- EX - predict age given a person's photo
    - Regression assumes the target is an average of every pixel in the photo :(

**how to fix?** 
- try handcrafting features 
EX: 
- take certain features out of image for model input
    - separates feature and model learning! - continuous

### CNNs 
Feature extraction and classification happen in the same model! 
- usually low-level, mid-level, high-level feature extractions
- fed into classfiier
    low-level feature       ->          mid-level feature       ->      high-level features             ->          classifier!

can handle image data!

convertations
    - feature extractions
    - compressions
    - image generation

analysis
    - face recognition
    - object detection

**CNNs - applications**

Great for any image detection!
- Medicine - Tumor Detection
- self-driving cars 

**Recurrent Neural Networks (RNNs)**
Built to process sequence data using feedback loops
- time series, text, speech data

**Deep Reinforcement Learning (DRL)** 

Model learns by interacting with inputs and observing results
- CNN outputs chosen input
- optimizes for a given reward - EX - winning a game

## Gradient Descent 
EX - least squares regression model

At each step, use randomized weight to compute a gradient 
1. update weights in opposite directions of gradient, prioritize loss minimization
2. compute output using new updated weights

**types of gradient descent:** 
- stochastic
- SGD w/ momentum
- RMSprop

### Gradient descent challenges:
**big data** 
- too many training samples 
**big model:** 
- too many model parameters
- ResNet has 25 million params! 

**big data + big model** - this is a common occurence!

> [!IMPORTANT]
> we need efficient algorithms & software!

## ML in practice
**modeling** 
- creating a model that fits data and problem 
- deciding network structure, activation function, loss function, etc.
- improve prediction accuracy
    - experience in ML models
    - model understanding of problem & data

**computation** 
- designing or applying efficient algorithms
- implementing algorithm using things like tensorfllow, pytorch, etc.
- optimizing your code!
    - experience using algorithms
    - experience using systems 


## Regression

**important starting info:** 
- Euclidian & Manhattan Distance
- Matrix Transpose & rank
    - square matrix 
    - symmetric matrices $A^T=A$
    - rank - number of linearly independent rows or columns
    - full rank - square matrix is full rank if rank = # columns
- eigenvalue decomposition
    - A is any nxn symmetric matrix 
    - eigenvalue decomp: $A = \Sum{i=1}{n}\lambda_iv_iv_i^T$
    - eigenvalues satisfy: $|\lambda_1| \leq |\lambda_2| \leq ... \leq |\lambda_n|$
    - eigenvectors satisfy $v_i^Tv_j = 0 \forall i \neq j$
