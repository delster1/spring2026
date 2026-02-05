---
tags:
    - eecs649
---

# week 3 - regression

## Lec 1 - Linear Regression

### Optimization Basics 

common problem:
- find min of $f(w)$ s.t. $w \in C$
- f : some objective function $\in \Reals^d \rarrow \Reals$
- $C$ is a subset of $\Reals^d$ - some feasible set
- optimal soln: $w* = argmin $f(w)$
    - $w \in C$
- $f(w*) \leq f(w) \forall w \in C$ - w is a vector
- $w*$ may not exist - EX $C$ is empty set
- if $w*$ exists, may not be unique

**linear regression** 
input:
- vectors: $x_1,...,x_n \in \Reals^d$ and labels $y_1,...,y_n \in \Reals$

output:
- vector $w \in \Reals^d$ and scalar $b \in \Reals$ s.t. $x_i^Tw + b = y_i$
- we've found a vector scalar $y = mx + b$ that represents the xs & ys (dots) given 
**least squares regression** 
input: 
- vector $w \in \Reals^d$ and scalar $b \in \Reals$  - dots on a graph

output: 
