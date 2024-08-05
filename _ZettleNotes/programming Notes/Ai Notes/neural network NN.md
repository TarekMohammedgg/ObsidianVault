---
date: 2024-07-31
author:
  - Andrew ng
topic:
  - Ai
  - machine learning
---

![[Pasted image 20240731015629.png]]

---
### how neural network actually work  ? 
**Neural Network component :**
1. input layers 
2. hidden layers 
3. output layers 
#### demand prediction
![[Pasted image 20240731020023.png]]
[[activation function]]
$$
a = f(x)_{\vec{w},b} = \frac{1}{1+\exp{(w.x + b)}}
$$
#### face recognition 
![[Pasted image 20240731020843.png]]

---
عند حساب عدد ال layers مش بنحسب ال inputs layers . 
$$
a^{(L)}_{j} = g(\vec{w}_{j}^{(L)} . \vec{a}^{(L-1)} + b_{j}^{(L)} ) 
$$
we use [[sigmoid function]] as an [[activation function]]

[[Forward propagation]]

[[vectorization]]

- خلي بالك في ان ال w كانت vector في ال [[linear Regression]] and [[_ZettleNotes/Logistic Regression (Classification )]] و لكن في ال [[neural network NN]] بقت matrix . 

### how to train [[neural network NN]] in tensorflow  :
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

**if is the problem can handle true or not use logistic loss known ass [[Binary Cross-Entropy Loss]]**

**if is the problem can handle predict the value [[Mean Squared Error (MSE)]]**

### Gradient descent in [[neural network NN]] 
we compute derivatives for gradient descent using [[Back Propagation]] 
```python
model.fit(x,y,epoches  = 100 ) 
#doing backpropagation also 
```

---

### choosing activation functions 
**choosing g(z) for hidden layers ?**
- [[Relu Functon]] most common choice why not [[sigmoid function]] ? 
	1. relu faster than sigmoid 
	2. faster learning because relu have one **flat region** , but sigmoid have two flat region  , the **flat region** make the gradient descent be slower  
**choosing g(z) for outputs layer ?** 
[[sigmoid function]] => [[_ZettleNotes/programming Notes/Ai Notes/Logistic Regression (Classification )]]
[[Linear function]] => [[linear Regression]]
[[Relu Functon]] => [[linear Regression]]

**why do we need activation functions ?**
because Neural Network not be able to fit any things more complex rather than [[Linear function]]( no activation function )

### [[multiclass classification]] 

### [[multilabel label classification ]]

### [[advanced optimization]] 

### additional layers types : 
#### 1. dense layer 
each neuron output is a function of all the activation outputs of the previous layer 
$a^{[2]}_{1} = g(\vec{w_{1}^{[2]}}.a^{[1]} + b^{[2]})$

#### 2. convolutional layers  
each neuron only looks at part of the previous layer's outputs . 
that make it : 
1. faster computation 
2. need less training data (less prone to overfitting) 

[[Back Propagation]]
[[bias and variance]]
[[loop of ML development ]]




----
LINKS TO THIS PAGE 
```dataview
LIST FROM ([[#]]) OR outgoing([[#]]) WHERE file.name != this.file.name SORT file.name ASC 
```

