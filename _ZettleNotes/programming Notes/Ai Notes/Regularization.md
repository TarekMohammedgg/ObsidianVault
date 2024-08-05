---
date: 
author: 
topic:
  - Ai
  - machine learning
---


Regularization is a set of methods for reducing overfitting in machine learning models.


$$
min_{w,b}  J(w,b)=\frac{1}{m}\sum_{i=1}^{n}L(\hat{y}^{(i)},y^{(i)})+\frac{Q}{2m}\|w\|_{2}^{2}

$$

### L2 Regularization 

L2 regularization 
$$
\|w\|_{2}^{2} = \sum_{j=1}^{nx} wj^2 = w^T * w  
$$

L1 regularization 
$$
\frac{Q}{2m}\|w\|_{1}
$$
w will be sparse 


### why regularization reduces overfitting ? 

- الفكرة بشكل عام اني كلما قللت قيمة ال w  كلما كانت ال [neural network NN](_ZettleNotes/programming%20Notes/Ai%20Notes/neural%20network%20NN.md) اصغر و ده الي بيخليها ابسط و بالتالي  بيقلل ال overfitting . 
- شرح مفصل اكتر 
![ 500 ](Pasted%20image%2020240729030348.png%20)


---
### Dropout Regularization
Dropout regularization is a technique used in machine learning, particularly in neural networks, to prevent overfitting. Overfitting occurs when a model learns the training data too well, including its noise and outliers, leading to poor performance on new, unseen data. Dropout helps to mitigate this by randomly "dropping out" a fraction of the neurons during the training process. Here’s a detailed explanation:

#### How Dropout Works

1. **Random Dropping of Neurons**: During each training iteration, dropout randomly selects a subset of neurons and sets their output to zero. This means the selected neurons are temporarily removed from the network for that iteration.
    
2. **Scaling during Training**: To maintain the overall scale of the inputs to the next layer, the remaining neurons are scaled up by a factor of$$ \frac{1}{(1 - p)}​$$, where ppp is the dropout rate (the probability of dropping a neuron).
    
3. **Training Phase vs. Inference Phase**:
    
    - **Training Phase**: Dropout is only applied during the training phase. The network becomes an ensemble of many smaller networks, each trained with different subsets of neurons.
    - **Inference Phase**: During the inference phase (testing/prediction), dropout is not applied. Instead, the full network is used, but the weights are scaled down by a factor of 1−p1 - p1−p to account for the effect of dropout during training.


![ 200](Pasted%20image%2020240729033013.png%20)

#### Benefits of Dropout

- **Prevents Overfitting**: By randomly dropping neurons, dropout forces the network to learn redundant representations and prevents it from relying too heavily on specific neurons.
- **Improves Generalization**: Dropout encourages the network to be more robust and generalize better to new data, as it cannot rely on the presence of any particular neuron during training.
#### Down side 
- the cost function (J) no longer well defined 


### Other regularization methods 
#### data augmentation
using some of distortion on the same image or item to increase the size of training data , that reduce the overfitting  . 
 يعد من المبادئ المستخدمة لحل مشكلة overfitting الا و هو زيادة حجم ال data set 

#### Early stopping
![ 300](Pasted%20image%2020240729040224.png%20)

يعتبر نفس المبدأ بتاع ال l2 regularization الا و هو اختار او تقليل قيمة ال w علي امل ان 
ال [neural network NN](_ZettleNotes/programming%20Notes/Ai%20Notes/neural%20network%20NN.md) تكون قيمة ال w مناسبة معاها و لكن ليها عيب واحد الا و هو : 
[orthogonalization](orthogonalization.md) 



### what is the different between [Regularization](Regularization.md) and [feature selection](feature%20selection.md)  ? 

in [Regularization](Regularization.md) : we don't delete feature completely , but decrease the effect of  unimportant features 

in [feature selection](feature%20selection.md) : we delete  unimportant features completely 


----
LINKS TO THIS PAGE 
```dataview
LIST FROM [#](#) OR outgoing([#](#)) WHERE file.name != this.file.name SORT file.name ASC
```