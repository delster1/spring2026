---
tags:
    - eecs649
---

# Week 3 - Classification

## Missed L1


## L2


## Evaluation Metrics - False Positives & Negatives 
- True & false positives are crucial 

Classification Goal:
- eliminate false positives & false negatives

Certain applications can allow for more or less false positives / negatives:
- EX - spam email filter
    - we would rather have false negatives - evaluating something as not spam when it is
    - this is much better than accidentally classifying important emails as spam!


**Receiver Operating Characteristic (ROC) Curves** 
- x axis - false positive rate 
- y axis - true positive rate
    - (0.2, 0.2) 
        - 20 % of data is correctly guessed
        - 20% of data is incorrectly labeled as true
    - x=y line is can represent a random guessed
        - anything above this line (kinda) means a model is performing better than random guessing

## Multi-class Classification

Examples: 
- Face Recognition - each face is classified as as a different person
- number Recognition

**can we use linear regression?** 
- there's a problem!
EX: input w/ a digit 3 that kinda looks like 8
- the linear regression would output something ~5 because it's the middle of 3 & 8
- 

**the right approach:** 
vectorization! - compute one score per-number
- these are output layers
- now we have individual confidences for each possible output!

- the weight vector, which influences the output, is what allows us to perform on multiple classes at once!

**softmax function** 
- exponentiate each score
- makes larger scores grow faster than smaller ones! 
good when only one class is correct!


**cross-entropy** 
- vectors $y, p$ are K-dim vectors with nonnegative entries
    - $y_1 + ... + y_k = 1$ and same for $p$
- cross-entropy between y and p: 
    - strongly discourage confident mistakes 
    - how surprised a model is by the true prediction label 
- mostly finds dissimilarity between y and p 
- better for probability-based predictions


**softmax classifier**  - Method
inputs:
- feature vectors x_1,...,x_n
- labels x_1,...,x_n
- n - # samples
- d - # features 
- k - # classes 

$\phi = Wx \in R^K$ - x is in the feature vector
- this contains our confidence - how likely x is in the k class - $\phi_k_$
- we now apply softmax to $\phi_k$ to exagerrate our confident guesses

we are trying to make our W accurately learn over time - Weight
- we do this by measuring our softmax output with the label using cross-entropy loss
- we minimize the function that compares our softmax output and the label's prediction
- encourages model to assign high probability to correct classes and low probability to incorrect

**softmax classifier - algrotithm** 
Gradient 
- applies derivatives to understand changes in inputs 


