---
title: "position-Methode (java.sql.NClob, long)"
ms.custom: na
ms.date: 07/27/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - drivers
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: f2354278-d128-4cf4-a170-22c05fcb763b
caps.latest.revision: 13
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
# position-Methode (java.sql.NClob, long)
  Ruft die Zeichenposition ab, an der sich das angegebene **NClob**\-Objekt *searchstr* in diesem **NClob**\-Objekt befindet.  
  
## Syntax  
  
```  
  
long position(java.sql.NClob searchstr,  
              long start)  
```  
  
#### Parameter  
 *searchstr*  
  
 Ein zu suchendes NClob\-Objekt.  
  
 *start*  
  
 Die Position, an der mit der Suche begonnen wird. Die erste Position ist "1".  
  
## Rückgabewert  
 Die Position, an der sich die Teilzeichenfolge befindet, oder "\-1", wenn sie nicht vorhanden ist. Die erste Position ist "1".  
  
## Ausnahmen  
 [SQLServerException](../content/SQLServerException-Class.md)  
  
## Hinweise  
 Diese position\-Methode wird von der position\-Methode in der java.sql.NClob\-Schnittstelle angegeben.  
  
## Siehe auch  
 [position-Methode &#40;SQLServerNClob&#41;](../content/position-Method--SQLServerNClob-.md)   
 [SQLServerNClob-Methoden](../content/SQLServerNClob-Methods.md)   
 [SQLServerNClob-Elemente](../content/SQLServerNClob-Members.md)   
 [SQLServerNClob-Klasse](../content/SQLServerNClob-Class.md)  
  
  