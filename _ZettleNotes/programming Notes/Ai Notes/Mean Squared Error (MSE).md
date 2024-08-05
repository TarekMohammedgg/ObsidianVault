---
date: 2024-07-31
author:
  - Andrew ng
topic:
  - machine learning
  - Ai
---
loss  function is [convex](convex) cost function 
cost function is summation of loss function 

$$
min(J(w,b ) = \frac{1}{2m} \sum_{i = 1 } ^ m ( f(x^{i} - y^{i} ) ) ^ 2 )  
$$

- the error or different between y & $\hat{y}$ is the *vertical* line between y and $\hat{y}$ 


### RMSE 
It is especially useful when dealing with data that contains both positive and negative values, as it gives a single value representing the overall magnitude.

$$
RMSE = \sqrt{ \frac{1}{n} \sum_{i =1 } ^{n} (y_{i} - \hat{y}_{i} )^2}
$$

----
LINKS TO THIS PAGE 
```dataview
LIST FROM ([#](#)) OR outgoing([#](#)) WHERE file.name != this.file.name SORT file.name ASC 
```
