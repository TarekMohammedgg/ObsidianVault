---
date: 
author: 
topic:
  - Ai
  - machine learning
---

**definition** : is generalization of [[_ZettleNotes/programming Notes/Ai Notes/Logistic Regression (Classification )]] , so able to solve [[neural network NN#multiclass classification]] problem 

![[Pasted image 20240731025428.png]]
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
LIST FROM ([[#]]) OR outgoing([[#]]) WHERE file.name != this.file.name SORT file.name ASC 
```
