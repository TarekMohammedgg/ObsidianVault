---
date: 2024-07-31
author:
  - Andrew ng
topic:
  - Ai
  - machine learning
---
*definition* : [Logistic Regression (Classification )](_ZettleNotes/programming%20Notes/AI_Notes/Logistic%20Regression%20(Classification%20).md) is a statistical method used for binary classification problems, where the goal is to predict the probability that a given input belongs to one of two possible classes. Unlike[linear Regression](_ZettleNotes/programming%20Notes/AI_Notes/linear%20Regression.md), which predicts a continuous output, logistic regression predicts a probability that is then mapped to a discrete class label.

use logistic function ([sigmoid function](_ZettleNotes/programming%20Notes/AI_Notes/sigmoid%20function.md) )

think in logistic regression the probability that class is 1 
### formula 
$$ \begin{align}
z = \vec{w , x }  + b  \\ g(z) = \frac{1}{1+\exp^z}
\end{align} 
$$
**another format** : 
$$
f(x)_{\vec{w} , b } = p(y=1 | x; \vec{w} , b )

$$
the probability that y is 1 given input $\vec{x}$, parameters $\vec{w}$, b 

$p(y=1) + p(y=0 ) = 1$

$f_{\vec{w}, b }(x) \ge thresold(0.5) \implies y=1$
$f_{\vec{w}, b }(x) < thresold(0.5) \implies y=0$


### cost function 

[binary cross-entropy loss](_ZettleNotes/programming%20Notes/AI_Notes/binary%20cross-entropy%20loss.md)


### Gradient descent 
$$
\frac{d}{dw_{j}} J(\vec{w} , b) = \frac{1}{m} \sum_{i=1}^{m} (f_{\vec{w} , b } (\vec{x}^{(i)}) - y^{(i)}) . x_{y}^{(i)}
$$

$$
\frac{d}{db_{j}} J(\vec{w} , b) = \frac{1}{m} \sum_{i=1}^{m} (f_{\vec{w} , b } (\vec{x}^{(i)}) - y^{(i)})
$$


[underverfitting & overfitting](_ZettleNotes/programming%20Notes/AI_Notes/underverfitting%20&%20overfitting.md)
[Softmax regression](_ZettleNotes/programming%20Notes/AI_Notes/Softmax%20regression.md)

----
LINKS TO THIS PAGE 
```dataview
LIST FROM [[#]] OR outgoing([[#]]) WHERE file.name != this.file.name SORT file.name ASC
```
