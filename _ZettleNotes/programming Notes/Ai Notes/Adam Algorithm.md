---
date: 2024-07-31
author:
  - Andrew ng
topic:
  - Ai
  - machine learning
---
not just one $\alpha$

**definition** : ( adaptive moment estimation  )  can adjust learning rate automatically 
يعني بيعرف امتي يسرع ال $\alpha$ و امتي يخليها ابطأ و هكذا ... 
و بيستخدم $\alpha$ لكل parameter عندك في ال model 
**how can do that** (Abstraction) : 
if $W_{j}$ or (b) keeps moving in same direction => increase $\alpha$
if $W_{j}$ or (b) keeps oscillating (تتأرجح)  => reducing $\alpha$


----
LINKS TO THIS PAGE 
```dataview
LIST FROM [[#]] OR outgoing([[#]]) WHERE file.name != this.file.name SORT file.name ASC
```

