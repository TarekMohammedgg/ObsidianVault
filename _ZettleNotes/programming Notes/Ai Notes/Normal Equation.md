---
draft: false
date: 2024-07-30
author:
  - Andrew ng
topic:
  - machine learning
  - Ai
---



The Normal Equation is a method used in linear regression to find the parameters (weights) that minimize the cost function. It provides a direct solution to the least squares problem without the need for iterative optimization algorithms like gradient descent. The Normal Equation is derived from setting the gradient of the cost function to zero and solving for the parameters.

that is for any [linear Regression](linear%20Regression.md)

### The formula 
$$
\theta=(X^TX)^{-1}X^Ty
$$

### disadvantages for this method 
slow when Number of features is large > 10,000 

----
LINKS TO THIS PAGE 
```dataview
LIST FROM ([#](#)) OR outgoing([#](#)) WHERE file.name != this.file.name SORT file.name ASC 
```
