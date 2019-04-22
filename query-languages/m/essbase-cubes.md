---
title: "Essbase.Cubes | Microsoft Docs"
ms.date: 4/16/2019
ms.service: powerquery

ms.reviewer: owend
ms.topic: reference
author: minewiskan
ms.author: owend
manager: kfile
---
# Essbase.Cubes

## About  

Returns a table of cubes grouped by Essbase server from an Essbase instance at APS server <code>url</code>. An optional record parameter, <code>options</code>, may be specified to control the following options: <ul> <li><code>CommandTimeout</code> : A duration which controls how long the server-side query is allowed to run before it is canceled. The default value is ten minutes.</li> </ul> 

## Syntax

<pre>
Essbase.Cubes(<b>url</b> as text, optional <b>options</b> as nullable record) as table
</pre>