---
title: "ERROR Function | Microsoft Docs"
ms.prod: dax
ms.date: 4/13/2018
ms.reviewer: owend
ms.topic: reference
author: minewiskan
ms.author: owend
manager: kfile
---
# ERROR Function
Raises an error with an error message.  
  
## Syntax  
  
```  
ERROR(<text>)  
```  
  
#### Parameters  
  
|Term|Definition|  
|--------|--------------|  
|text|A text string containing an error message.|  
  
## Return Value  
None 
  
## Remarks  
The ERROR function can be placed in a DAX expression anywhere a scalar value is expected.
   
  
## Examples  
### Example 1

The following DAX query:
```
DEFINE
MEASURE DimProduct[Measure] = 
		IF(
			SELECTEDVALUE(DimProduct[Color]) = "Red",
			ERROR("red color encountered"),
			SELECTEDVALUE(DimProduct[Color])
		)
EVALUATE SUMMARIZECOLUMNS(DimProduct[Color], "Measure", [Measure])
ORDER BY [Color]
```

Fails and raises and error message containing “red color encountered”.


### Example 2
The following DAX query:

```
DEFINE
MEASURE DimProduct[Measure] = 
		IF(
			SELECTEDVALUE(DimProduct[Color]) = "Magenta",
			ERROR("magenta color encountered"),
			SELECTEDVALUE(DimProduct[Color])
		)
EVALUATE SUMMARIZECOLUMNS(DimProduct[Color], "Measure", [Measure])
ORDER BY [Color] 
```

Returns the following table: 

DimProduct[Color]  |[Measure] 
---------|---------
Black     |        Black 
Blue     |       Blue  
Grey     |      Grey   
Multi     |    Multi     
NA     |        NA 
Red     |     Red    
Silver     |     Silver    
Silver\Black     |   Silver\Black      
White    |       White  
Yellow    |        Yellow 

Because Magenta is not one of the product colors, the ERROR function is not executed.