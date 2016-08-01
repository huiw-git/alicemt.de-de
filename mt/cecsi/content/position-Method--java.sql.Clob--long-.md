---
title: "position-Methode (java.sql.Clob, long)"
ms.custom: na
ms.date: 07/27/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - drivers
ms.tgt_pltfrm: na
ms.topic: article
apiname: 
  - SQLServerClob.position (java.sql.Clob, long)
apilocation: 
  - sqljdbc.jar
apitype: Assembly
ms.assetid: b2fb34d5-1d34-4764-a795-712d9c6aa313
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
# position-Methode (java.sql.Clob, long)
    
## position\-Methode \(java.sql.Clob, long\)  
 Gibt die Zeichenposition des angegebenen CLOB\-Objekts im CLOB auf Grundlage der angegebenen Startposition zurück.  
  
## Syntax  
  
```  
  
public long position(java.sql.Clob searchstr,  
                     long start)  
```  
  
#### Parameter  
 *searchstr*  
  
 Die zu suchende Teilzeichenfolge.  
  
 *start*  
  
 Die Position, ab der gesucht werden soll. Die erste Position ist "1".  
  
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
  
  