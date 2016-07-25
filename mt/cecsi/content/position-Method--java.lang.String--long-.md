---
title: "position-Methode (java.lang.String, long)"
ms.custom: na
ms.date: 07/01/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - drivers
ms.tgt_pltfrm: na
ms.topic: article
apiname: 
  - SQLServerClob.position (java.lang.String, long)
apilocation: 
  - sqljdbc.jar
apitype: Assembly
ms.assetid: 86fad8ed-375a-42e1-b40e-1fa085957a2c
caps.latest.revision: 9
caps.handback.revision: 8
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
# position-Methode (java.lang.String, long)
    
## position\-Methode \(java.lang.String, long\)  
 Gibt die Zeichenposition der angegebenen Teilzeichenfolge im CLOB auf Grundlage der angegebenen Startposition zurück.  
  
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
 Diese position\-Methode wird von der position\-Methode in der java.sql.Clob\-Schnittstelle angegeben.  
  
## Siehe auch  
 [position-Methode &#40;SQLServerClob&#41;](../content/position-Method--SQLServerClob-.md)   
 [SQLServerClob-Methoden](../content/SQLServerClob-Methods.md)   
 [SQLServerClob-Elemente](../content/SQLServerClob-Members.md)   
 [SQLServerClob-Klasse](../content/SQLServerClob-Class.md)  
  
  