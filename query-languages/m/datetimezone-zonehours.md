---
title: "DateTimeZone.ZoneHours | Microsoft Docs"
ms.date: 4/16/2018
ms.prod: power-query
ms.reviewer: owend
ms.topic: reference
author: minewiskan
ms.author: owend
manager: kfile
---
# DateTimeZone.ZoneHours

  
## About  
Returns a time zone hour value from a DateTime value.  
  
```  
DateTimeZone.ZoneHours(dateTime as datetimezone) as nullable number  
```  
  
## Arguments  
  
|Argument|Description|  
|------------|---------------|  
|dateTime|The DateTimeZone to check against.|  
  
## Example  
  
```  
DateTimeZone.ZoneHours(DateTime.FromText("12:56:20-08:00")) equals -8  
```  