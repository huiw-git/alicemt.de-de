---
title: "compareTo-Methode (DateTimeOffset)"
ms.custom: na
ms.date: 07/27/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - drivers
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: e4cf2ea4-0fe9-40ce-ba79-f2a2b616997e
caps.latest.revision: 12
caps.handback.revision: 12
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
# compareTo-Methode (DateTimeOffset)
    
## compareTo\-Methode \(DateTimeOffset\)  
 Vergleicht dieses **DateTimeOffset**\-Objekt mit einem anderen **DateTimeOffset**\-Objekt basierend auf der Uhrzeit nach GMT.  
  
## Syntax  
  
```  
  
public int compareTo(DateTimeOffset other)  
```  
  
#### Parameter  
 Ein [DateTimeOffset](../content/DateTimeOffset-Class.md)\-Wert, der mit der aktuellen Instanz verglichen werden soll.  
  
## Rückgabewert  
 In der folgenden Tabelle wird der Rückgabewert für diese Methode beschrieben:  
  
|Rückgabewert|Beschreibung|  
|------------------|------------------|  
|0|Beide **DateTimeOffset**\-Objekte stellen denselben Zeitpunkt dar.|  
|Negative Zahl|Dieses **DateTimeOffset**\-Objekt stellt einen vor *other* liegenden Zeitpunkt dar.|  
|Positive Zahl|Dieses **DateTimeOffset**\-Objekt stellt einen nach *other* liegenden Zeitpunkt dar.|  
  
## Hinweise  
 Wenn zwei **DateTimeOffset**\-Objekte dieselbe Uhrzeit nach GMT haben, werden die Objekte nicht zusätzlich nach Offset geordnet.  
  
## Siehe auch  
 [DateTimeOffset-Klasse](../content/DateTimeOffset-Class.md)   
 [DateTimeOffset-Elemente](../content/DateTimeOffset-Members.md)  
  
  