---
date: 2024-07-30
author:
  - Andrew ng
topic:
  - Ai
  - machine learning
---


*definition* : mechanism used in training data to minimize loss function ( find local minimum )  
لانك لما تبدأ من مكان مختلف في كل مره هتلاقي نفسك و صلت لقاع (وادي ) مختلف عن الي قبلهم . 

$w = w - \alpha \frac{dw}{d} J(w,b) :   \alpha ~ is ~ size ~ step$


$\alpha$ => [0,1] $\approx$ 0,01 
$\frac{dw}{d} J(w,b)$=> بيحدد الاتجاه الي همشي فيه 


$b = b - \alpha ~ \frac{d}{dw} J(w,b)$


correct  simulate new update 
```python 
temp - w = w - a d/dw J(w,b) 
temp - b = b - a d/dw J(w,b) 
w = temp-w 
b = temp - b 
```

in correct simulate new update 
```python 
temp - w = w - a d/dw J(w,b) 
w = temp-w 
temp - b = b - a d/dw J(w,b) 
b = temp - b 
```

الغلط في المثال التاني اني مادام شغال في simulate ازاي احط القيمة الجديدة بتاعة ال w في ال b الي المفروض تكون الحدث في نفس الوقت الي w  بتحدث فيه . 

![](Pasted%20image%2020240730234540.png#center%20|%20500%20)


in [gradient descent](gradient%20descent.md) can reach minimum without decreasing learning rate 
عشان كلما اقترب من ال local minimum الاشتقاق بيقل لحد ما يوصل للصفر 
![](Pasted%20image%2020240730235441.png#center%20|%20500%20)



----
LINKS TO THIS PAGE 
```dataview
LIST FROM [[#]] OR outgoing([[#]]) WHERE file.name != this.file.name SORT file.name ASC
```

