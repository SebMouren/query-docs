---
title: "PERCENTILEX.EXC Function (DAX) | Microsoft Docs"
ms.prod: dax
ms.date: 4/13/2018
ms.reviewer: owend
ms.topic: reference
author: minewiskan
ms.author: owend
manager: kfile
---
# PERCENTILEX.EXC Function (DAX)
  
Returns the percentile number of an expression evaluated for each row in a table.  
  
To return the percentile of numbers in a column, use [PERCENTILE.EXC Function &#40;DAX&#41;](percentile-exc-function-dax.md).  
  
## Syntax  
  
```  
PERCENTILEX.EXC(<table>, <expression>, k)  
```  
  
#### Parameters  
  
|Term|Definition|  
|--------|--------------|  
|table|The table containing the rows for which the expression will be evaluated.|  
|expression|The expression to be evaluated for each row of the table.|  
|k|The desired percentile value in the range 0 to 1 exclusive.|  
  
## Return Value  
The percentile number of an expression evaluated for each row in a table.  
  
## Remarks  
If k is zero or blank, percentile rank of 1/(n+1) returns the smallest value. If zero, it is out of range and an error is returned.  
  
If k is nonnumeric or outside the range 0 to 1, an error is returned.  
  
If k is not a multiple of 1/(n + 1), PERCENTILEX.EXC will interpolate to determine the value at the k-th percentile.  
  
PERCENTILEX.EXC will interpolate when the value for the specified percentile is between two values in the array. If it cannot interpolate for the k percentile specified, an error is returned.  
  
## See Also  
[PERCENTILE.EXC Function &#40;DAX&#41;](percentile-exc-function-dax.md)  
  