---
date: 
author: 
topic:
  - Ai
  - machine learning
---

**definition** : is generalization of [Logistic Regression (Classification )](Logistic%20Regression%20(Classification%20).md) , so able to solve [](_ZettleNotes/programming%20Notes/Ai%20Notes/neural%20network%20NN.md#multiclass%20classification) problem 

![Pasted image 20240731025428](Pasted%20image%2020240731025428.png)
### formula : 
$$
a_{j} = \frac{\exp^{Z_{j}}}{\sum_{k =1 }^{N} \exp^{Z_{k}}}
$$

يعني الفكرة انت بتشوف نسبة وجود  A من المجموعة (احتمالية و جود A من وسط المجموعة ) . 

the loss function for softmax in tensorflow : 
```python
loss = SparseCategoricalCrossEntropy() 
#sparse : take one digit (0 or 1 or 2 ...or 9) 
#CategoricalCrossEntroy : take digit from 0 to 9 
```


### Improved Implementation of softmax 
decrease Numerical roundoff error 



----
LINKS TO THIS PAGE 
```dataview
LIST FROM [[#]] OR outgoing([[#]]) WHERE file.name != this.file.name SORT file.name ASC
```
