---
title: "valueOf-Methode (java.sql.Timestamp, int)"
ms.custom: na
ms.date: 07/01/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - drivers
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 114f55af-62ab-4c60-8724-0affbbbbbcdc
caps.latest.revision: 6
caps.handback.revision: 6
manager: jhubbard
translation.priority.ht: 
  - de-de
  - es-es
  - fr-fr
  - it-it
  - ja-jp
  - ko-kr
  - pt-br
  - ru-ru
  - sv-se
  - zh-cn
  - zh-tw
---
# valueOf-Methode (java.sql.Timestamp, int)
    
## valueOf\-Methode \(java.sql.Timestamp, int\)  
 Erstellt ein **DateTimeOffset**\-Objekt, das einen Zeitpunkt in einem bestimmten Offset von GMT darstellt, wenn ein java.sql.Timestamp\-Wert sowie ein den Offset in Minuten angegebener Wert gegeben ist.  
  
## Syntax  
  
```  
  
public static DateTimeOffset valueOf(java.sql.Timestamp timestamp, int minutesOffset)  
```  
  
#### Parameter  
 *timestamp*  
  
 Ein java.sql.Timestamp\-Wert.  
  
 *minutesOffset*  
  
 Das Offset in Minuten.  
  
## Rückgabewert  
 Gibt ein DateTimeOffset\-Objekt zurück, das den vom  java.sql.Timestamp\-Objekt gegebenen Zeitpunkt zum gegebenen Offset in Minuten von GMT darstellt.  
  
## Siehe auch  
 [DateTimeOffset-Klasse](../content/DateTimeOffset-Class.md)   
 [DateTimeOffset-Elemente](../content/DateTimeOffset-Members.md)  
  
  