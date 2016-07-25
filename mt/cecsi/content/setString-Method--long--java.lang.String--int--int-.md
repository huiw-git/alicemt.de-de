---
title: "setString-Methode (long, java.lang.String, int, int)"
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
  - SQLServerClob.setString (long, java.lang.String, int, int)
apilocation: 
  - sqljdbc.jar
apitype: Assembly
ms.assetid: 9fb59b09-e825-46a6-ba5d-85d4a8dc143a
caps.latest.revision: 10
caps.handback.revision: 9
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
# setString-Methode (long, java.lang.String, int, int)
    
## setString\-Methode \(long, java.lang.String, int, int\)  
 Schreibt die angegebene Zeichenfolge auf der Grundlage des angegebenen Offsets und der angegebenen Länge ab der angegebenen Position in das CLOB.  
  
## Syntax  
  
```  
  
public int setString(long pos,  
                     java.lang.String str,  
                     int offset,  
                     int len)  
```  
  
#### Parameter  
 *pos*  
  
 Die Position, an der Daten in das CLOB geschrieben werden sollen.  
  
 *str*  
  
 Die Zeichenfolge, die in das CLOB geschrieben werden soll.  
  
 *offset*  
  
 Das Offset innerhalb der Zeichenfolge, ab der Zeichen gelesen werden sollen.  
  
 *len*  
  
 Die Anzahl der zu schreibenden Zeichen.  
  
## Rückgabewert  
 Die Anzahl der geschriebenen Zeichen.  
  
## Ausnahmen  
 java.sql.SQLException  
  
## Hinweise  
 Diese setString\-Methode wird von der setString\-Methode in der java.sql.Clob\-Schnittstelle angegeben.  
  
 Zeichendaten werden beginnend mit der angegebenen Position überschrieben, und sie können die ursprüngliche Länge des CLOB überschreiben. Durch Angeben eines Werts vom Typ "Position\+1" wird die Zeichenfolge angefügt. Durch Angeben eines Werts vom Typ "Position\+2" oder größer \(oder null oder weniger\) wird ein Positionsfehler ausgelöst.  
  
## Siehe auch  
 [setString-Methode &#40;SQLServerClob&#41;](../content/setString-Method--SQLServerClob-.md)   
 [SQLServerClob-Methoden](../content/SQLServerClob-Methods.md)   
 [SQLServerClob-Elemente](../content/SQLServerClob-Members.md)   
 [SQLServerClob-Klasse](../content/SQLServerClob-Class.md)  
  
  