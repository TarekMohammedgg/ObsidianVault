---
date: 
author: 
references: 
topic:
---
=REPT(char(129001),(B2/C2*100)/10)& REPT(CHAR(11036) , (100 -(B2/C2*100) ) /10) & ROUND((B2/C2*100) , 2 ) & "%" & if(B2=C2 , "🎉" , "")
