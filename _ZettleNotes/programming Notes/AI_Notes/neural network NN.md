---
date: 2024-07-31
author:
  - Andrew ng
topic:
  - Ai
  - machine learning
---

![Pasted image 20240731015629](Attachment/Pasted%20image%2020240731015629.png)

---
### how neural network actually work  ? 
**Neural Network component :**
1. input layers 
2. hidden layers 
3. output layers 
#### demand prediction
![Pasted image 20240731020023](Attachment/Pasted%20image%2020240731020023.png)
[activation function](_ZettleNotes/programming%20Notes/AI_Notes/activation%20function.md)
$$
a = f(x)_{\vec{w},b} = \frac{1}{1+\exp{(w.x + b)}}
$$
#### face recognition 
![Pasted image 20240731020843](Attachment/Pasted%20image%2020240731020843.png)

---
عند حساب عدد ال layers مش بنحسب ال inputs layers . 
$$
a^{(L)}_{j} = g(\vec{w}_{j}^{(L)} . \vec{a}^{(L-1)} + b_{j}^{(L)} ) 
$$
we use [sigmoid function](_ZettleNotes/programming%20Notes/AI_Notes/sigmoid%20function.md) as an [activation function](_ZettleNotes/programming%20Notes/AI_Notes/activation%20function.md)

[Forward propagation](_ZettleNotes/programming%20Notes/AI_Notes/Forward%20propagation.md)

[vectorization](_ZettleNotes/programming%20Notes/AI_Notes/vectorization.md)

- خلي بالك في ان ال w كانت vector في ال [linear Regression](_ZettleNotes/programming%20Notes/AI_Notes/linear%20Regression.md) and [Logistic Re`gression (Classification )](Logistic%20Re`gression%20(Classification%20)) و لكن في ال [neural network NN](_ZettleNotes/programming%20Notes/AI_Notes/neural%20network%20NN.md) بقت matrix . 

### how to train [neural network NN](_ZettleNotes/programming%20Notes/AI_Notes/neural%20network%20NN.md) in tensorflow  :
1. create a Neural Network " how to compute output give input x and parameters "
	```python 
	model = sequential([layer 1  , layer 2 ])
	layer : dense(units = , activation = )
	```
2. specify the loss function 
	```python 
	model.compile(loss = BinaryCrossEntropy()) 
	```
3. fit the first step using the second step to set data (x, y ) 
	```python
	model.fit(x,y,epoches = 100 ) , #epoches => number of steps in gradient descent  
	```

**note that loss function for 1 example , but cost function take average of loss function** 

**if is the problem can handle true or not use logistic loss known ass [binary cross-entropy loss](_ZettleNotes/programming%20Notes/AI_Notes/binary%20cross-entropy%20loss.md)**

**if is the problem can handle predict the value [Mean Squared Error (MSE)](_ZettleNotes/programming%20Notes/AI_Notes/Mean%20Squared%20Error%20(MSE).md)**

### Gradient descent in [neural network NN](_ZettleNotes/programming%20Notes/AI_Notes/neural%20network%20NN.md) 
we compute derivatives for gradient descent using [Back Propagation](_ZettleNotes/programming%20Notes/AI_Notes/Back%20Propagation.md) 
```python
model.fit(x,y,epoches  = 100 ) 
#doing backpropagation also 
```

---

### choosing activation functions 
**choosing g(z) for hidden layers ?**
- [Relu Functon](_ZettleNotes/programming%20Notes/AI_Notes/Relu%20Functon.md) most common choice why not [sigmoid function](_ZettleNotes/programming%20Notes/AI_Notes/sigmoid%20function.md) ? 
	1. relu faster than sigmoid 
	2. faster learning because relu have one **flat region** , but sigmoid have two flat region  , the **flat region** make the gradient descent be slower  
**choosing g(z) for outputs layer ?** 
[sigmoid function](_ZettleNotes/programming%20Notes/AI_Notes/sigmoid%20function.md) => [Logistic Regression (Classification )](_ZettleNotes/programming%20Notes/AI_Notes/Logistic%20Regression%20(Classification%20).md)
[Linear function](_ZettleNotes/programming%20Notes/AI_Notes/Linear%20function.md) => [linear Regression](_ZettleNotes/programming%20Notes/AI_Notes/linear%20Regression.md)
[Relu Functon](_ZettleNotes/programming%20Notes/AI_Notes/Relu%20Functon.md) => [linear Regression](_ZettleNotes/programming%20Notes/AI_Notes/linear%20Regression.md)

**why do we need activation functions ?**
because Neural Network not be able to fit any things more complex rather than [[Linear function](%20no%20activation%20function%20)

### [multiclass classification](_ZettleNotes/programming%20Notes/AI_Notes/multiclass%20classification.md) 

### [multilabel label classification](_ZettleNotes/programming%20Notes/AI_Notes/multilabel%20label%20classification.md)

### [advanced optimization](_ZettleNotes/programming%20Notes/AI_Notes/advanced%20optimization.md) 

### additional layers types : 
#### 1. dense layer 
each neuron output is a function of all the activation outputs of the previous layer 
$a^{[2]}_{1} = g(\vec{w_{1}^{[2]}}.a^{[1]} + b^{[2]})$

#### 2. convolutional layers  
each neuron only looks at part of the previous layer's outputs . 
that make it : 
1. faster computation 
2. need less training data (less prone to overfitting) 

[Back Propagation](_ZettleNotes/programming%20Notes/AI_Notes/Back%20Propagation.md)
[bias and variance](_ZettleNotes/programming%20Notes/AI_Notes/bias%20and%20variance.md)
[loop of ML development](_ZettleNotes/programming%20Notes/AI_Notes/loop%20of%20ML%20development.md)




----
LINKS TO THIS PAGE 
```dataview 
LIST FROM [[#]] OR outgoing([[#]]) WHERE file.name != this.file.name SORT file.name ASC
```
