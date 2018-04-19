---
title: "List.Generate | Microsoft Docs"
ms.date: 4/16/2018
ms.prod: power-query
ms.reviewer: owend
ms.topic: reference
author: minewiskan
ms.author: owend
manager: kfile
---
# List.Generate

  
## About  
Generates a list of values given four functions that generate the initial value <code>initial</code>, test against a condition <code>condition</code>, and if successful select the result and generate the next value <code>next</code>. An optional parameter, <code>selector</code>, may also be specified.
  
## Examples  
 #### Example 1
Create a list that starts at 10, remains greater than 0 and decrements by 1. 
```  
List.Generate(()=>10, each _ > 0, each _ - 1)
```  
<table> <tr><td>10</td></tr> <tr><td>9</td></tr> <tr><td>8</td></tr> <tr><td>7</td></tr> <tr><td>6</td></tr> <tr><td>5</td></tr> <tr><td>4</td></tr> <tr><td>3</td></tr> <tr><td>2</td></tr> <tr><td>1</td></tr> </table>  
      
#### Example 2
Generate a list of records containing x and y, where x is a value and y is a list. x should remain less than 10 and represent the number of items in the list y. After the list is generated, return only the x values.  
```  
List.Generate(()=> [ x = 1 , y = {}] , each [x] < 10 , each [x = List.Count([y]), y = [y] & {x}] , each [x])
```  
<table> <tr><td>1</td></tr> <tr><td>0</td></tr> <tr><td>1</td></tr> <tr><td>2</td></tr> <tr><td>3</td></tr> <tr><td>4</td></tr> <tr><td>5</td></tr> <tr><td>6</td></tr> <tr><td>7</td></tr> <tr><td>8</td></tr> <tr><td>9</td></tr> </table>