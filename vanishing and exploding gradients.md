---
date: 2024-08-04
author:
  - Andrew ng
topic:
  - Ai
  - machine learning
references:
  - https://www.analyticsvidhya.com/blog/2021/06/the-challenge-of-vanishing-exploding-gradients-in-deep-neural-networks/
  - https://stackoverflow.com/questions/47506521/what-exactly-is-gradient-checking
---

**vanishing**  
معناها اني في مرحلة ال [Back Propagation](_ZettleNotes/programming%20Notes/Ai%20Notes/Back%20Propagation.md) ال weights بتبدأ تقل تدريجيا و بعدين تقترب من الصفر و ده بيؤدي انها اكنها مش موجوده يعني ال [gradient descent](_ZettleNotes/programming%20Notes/Ai%20Notes/gradient%20descent.md) متنفز في ال layers الاولية  .

**exploding**
عكس ال vanishing  و هو انك بتبدأ ب weights قليله و بعدين بتكتبر عادة بشكل exponentially فالبتالي ال layers الاخيرة مش بيحصلها [gradient descent](_ZettleNotes/programming%20Notes/Ai%20Notes/gradient%20descent.md) 

---
### solve the problem 
initialize weights , use [Relu Functon](_ZettleNotes/programming%20Notes/Ai%20Notes/Relu%20Functon.md) or [[tansh function ]] 

----
### what is the gradient checking  
check manually on the derivative of the [Back Propagation](_ZettleNotes/programming%20Notes/Ai%20Notes/Back%20Propagation.md) of the [neural network NN](_ZettleNotes/programming%20Notes/Ai%20Notes/neural%20network%20NN.md) to avoid any type of error when run the [deep NN](deep%20NN)

----
### Gradient checking implementation Nots 
- Don't use gradient checking in training - only to debug 
- if algorithm fails grad check , look at components to try to identify bug . 
- remember [Regularization](_ZettleNotes/programming%20Notes/Ai%20Notes/Regularization.md) 
- doesn't work with [Dropout Regularization](Regularization#Dropout%20Regularization)
- run at random initialization ; perhaps again after some training . 




----
LINKS TO THIS PAGE 
```dataview 
LIST FROM [[#]] OR outgoing([[#]]) WHERE file.name != this.file.name SORT file.name ASC
```

