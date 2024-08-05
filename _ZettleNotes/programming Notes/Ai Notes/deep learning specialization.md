---
date: 2024-07-30
author:
  - Andrew ng
topic:
  - Ai
  - machine learning
---

Notes : 
# First course : Neural Network 


what is deep NN ? 
meaning add more hidden layers in the [[deep learning specialization]]

![[Pasted image 20240723091655.png |500]]

[[Forward propagation]] equation : 
![[Pasted image 20240723092041.png]]

Formula : Z^[L] = w^[L] *  A^[L] + b^[L] 
parameters w^[L] and b^[L] : 
w^[L] : (n^[L] , n^[L-1]) 
b^[L] : (n^[L] , 1 ) 
[[vectorization]] : 
w^[L] : (n^[L] , n^[L-1]) 
Z = {z^[1]^[1] +z^[1]^[2] +...+z^[1]^[m]  } : (n^[L] , m )
A = {a^[1]^[1] +a^[1]^[2] +...+a^[1]^[m]  } : (n^[L-1] , m )
b [in python ] = (n^[L] , m ) 

building blocks of [[deep NN]]
![[Pasted image 20240723101305.png]]

Parameters vs. Hyperparameters : 
parameters : w , b 
[[hyperparameters]] : learning rate  (alpha) , # iterations , # hidden layers L , # hidden units , choice of [[activation function]] (RELU , SIGMOID ) , also can be : momentum , mini batch size , [[Regularization]] 

Tips & Tricks : 
1. in back propagation the dimension of dw and db must be equal the dimension of w and b in forward propagation . 
2. when count the number of layers in [[deep learning specialization]] we count the hidden layers and output layer . 

----

# Second course : Improving deep Neural Networks : hyperparameter tuning , regularization and optimization 

Notes : 
## Train / dev / test sets 
![[Pasted image 20240727085600.png#center | 500]]
we aim to improve this cycle 
لذلك يمكننا تطوير و رفع كفائة هذه الدائرة و من ضمن الاشياء هذه هو تقسيم الداتا سيت الي ثلاث اقسام اساسية : training set / validation set / testing set 
و كذلك سيسمح لك بقياس اكثر فاعلية لتحيز و تباين خوارزميتك 

- في data sets الصغيرة نسبة توزيع الثلاث اقسام يكون جيد تطبيق التوزيع التقليدي : 
 60 , 20 , 20 % 

- اما في حالة كانت الداتا كبيره مثلا مليون او اكثر فيفضل تقسيم السيتس الي :
90 , 5 , 5 % 
فيفضل توزيع ال dev and testing set بنسبة اقل من 20 او حتي اقل من 10 في المية من الداتا الكبيرة 
### mismatched train / test distribution 
- make sure dev and test come from same distribution 

- not having a test set might be okay . (only dev set . ) . 


Tips and Tricks : 
- the goal of testing set is avoid unbiased estimate of the performance of the model . 
- validation / dev set : to test multiple models and choose what is the best model . 

## [[bias and variance ]] 

العوامل الاساسية في تحديد ما اذا حدث bias or variance من خلال  


|                  | variance  | bias |
|------------------|-----------|------|
| train set error  | low       | high |
| dev set error    | high      | low  |



----
## basic recipe for machine learning 
solve bias problem : 

|                                          |     | bigger network   |
|------------------------------------------|-----|------------------|
| high bias ( training data performance )  | ->  | training longer  |
|                                          |     |  NN archicture   |

solve variance problem  : 

|                                    |     | more data       |
|------------------------------------|-----|-----------------|
| high variance ( dev set problem )  | ->  | reguralization  |
|                                    |     |  NN archicture  |

---
how to apply [[Regularization]] in [[deep NN]] , and what is the types of regularization 


----
setting up your optimization problem : 
[[Normalizing]]





---
LINKS TO THIS PAGE 
```dataview
LIST FROM ([[#]]) OR outgoing([[#]]) WHERE file.name != this.file.name SORT file.name ASC 
```