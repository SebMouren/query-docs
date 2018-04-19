---
title: "Date.IsInNextNMonths | Microsoft Docs"
ms.date: 4/16/2018
ms.prod: power-query
ms.reviewer: owend
ms.topic: reference
author: minewiskan
ms.author: owend
manager: kfile
---
# Date.IsInNextNMonths
<code>Date.IsInNextNMonths(**dateTime** as any, **months** as number) as nullable logical</code>
## About
Indicates whether the given datetime value <code>dateTime</code> occurs during the next number of months, as determined by the current date and time on the system. 
- <code>dateTime</code>: A <code>date</code>, <code>datetime</code>, or <code>datetimezone</code> value to be evaluated. 
- <code>months</code>: The number of months.

## Example 
Determine if the month after the current system time is in the next two months.

<code>Date.IsInNextNMonths(Date.AddMonths(DateTime.FixedLocalNow(), 1), 2)</code>

<code>true</code>
