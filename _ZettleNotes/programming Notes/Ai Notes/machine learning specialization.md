---
date: 2024-07-31
author:
  - Andrew ng
topic:
  - Ai
  - machine learning
---
machine learning : *"Field of study that gives computers the ability to learn without being explicitly programmed "* - #Arthur_Samuel 1959 
## [Supervised learning](Supervised%20learning.md)

### [unsupervised learning](unsupervised%20learning.md) 

[neural network NN](_ZettleNotes/programming%20Notes/Ai%20Notes/neural%20network%20NN.md)

### Diagnostics for improve learning algorithm performance 
how to evaluate the performance of learning algorithm 
- split training set to 70 % training set and 30 % testing set 
- note that in training sets and testing sets we not add the [Regularization](Regularization.md) term , because we want show the performance of the models themselves 
#### how to select model ? 
فيه مشكلة انك لو اخترت علي اساس ال training set فهيكون النسبة زيادة عن اللزوم و كذلك لو اخترت علي اساس ال testing set  بس هتلاقي النسبة زيادة عن اللزوم برده ، فالحل في ال [cross validation ](cross%20validation%20) 
split data into three parts 

| training set | cross validation set | testing set |
| ------------ | -------------------- | ----------- |
| 60 %         | 20 %                 | 20 %        |
[learning curves](learning%20curves.md)








----
LINKS TO THIS PAGE 
```dataview
LIST FROM [[#]] OR outgoing([[#]]) WHERE file.name != this.file.name SORT file.name ASC
```