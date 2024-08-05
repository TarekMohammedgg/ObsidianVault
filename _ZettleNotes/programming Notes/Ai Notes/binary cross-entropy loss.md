---
date: 2024-07-31
author:
  - Andrew ng
topic:
  - Ai
  - machine learning
---
It measures the performance of a classification model whose output is a probability value between 0 and 1. The goal is to minimize this cost function during the training process.

$$
L(\hat{y} , y ) = - y \log(\hat{y}) - (1-y) \log(1-\hat{y}) 
$$

### cost function 
$$
J(\theta) = - \frac{1}{m} \sum_{i=1} ^{m} [y^{(i)} \log(h_{\theta}(x^{(i)}) ) + (1 - y^{(i)}) \log(1-h_{\theta} (x^{(i)}))] ~ , ~ h_{\theta}(x^{(i)} ) = \hat{y}
$$




----
LINKS TO THIS PAGE 
```dataview
LIST FROM ([#](#)) OR outgoing([#](#)) WHERE file.name != this.file.name SORT file.name ASC 
```

