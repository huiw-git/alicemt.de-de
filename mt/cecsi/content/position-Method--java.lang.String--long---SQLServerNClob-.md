---
title: "position-Methode (java.lang.String, long) (SQLServerNClob)"
ms.custom: na
ms.date: 07/27/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - drivers
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 46d4beec-831a-449f-98b6-322a80cc499a
caps.latest.revision: 12
caps.handback.revision: 11
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
# position-Methode (java.lang.String, long) (SQLServerNClob)
  Ruft die Zeichenposition ab, an der sich die angegebene *searchstr*\-Teilzeichenfolge im **NCLOB**\-Wert befindet, der von diesem **NClob**\-Objekt dargestellt wird.  
  
## Syntax  
  
```  
  
public long position(java.lang.String searchstr,  
              long start)  
```  
  
#### Parameter  
 *searchstr*  
  
 Die zu suchende Teilzeichenfolge.  
  
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
  
  