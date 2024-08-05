---
date: 2024-07-31
author:
  - Andrew ng
topic:
  - Ai
  - machine learning
---

dev set =  validation set = development set 

**definition** : to check accuracy of different models 

الطريقة كالأتي : 

we select the best model between some models using training and dev sets after that using testing set to check the actual performance of the model . 

so ,
**training set** : used to train the model . 
**validation set** : used to tune hyperparameters and select the best model . 
**test set** : used only once for the final evaluation after the model is fully trained and tuned  . 


### what is the different between [cross validation](_ZettleNotes/programming%20Notes/Ai%20Notes/cross%20validation.md) and [Regularization](Regularization.md) ? 
**Regularization**
reduce overfitting by add a penalty 
**Cross validation**
try to add advise and lead the model to correct roadmap (tuning parameters) 
is a check point to ensure the model is learning effectively and generalizing well to new data 



----
LINKS TO THIS PAGE 
```dataview
LIST FROM [[#]] OR outgoing([[#]]) WHERE file.name != this.file.name SORT file.name ASC
```
