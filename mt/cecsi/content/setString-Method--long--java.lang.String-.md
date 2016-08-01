---
title: "setString-Methode (long, java.lang.String)"
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
  - SQLServerClob.setString (long, java.lang.String)
apilocation: 
  - sqljdbc.jar
apitype: Assembly
ms.assetid: 1b2190e9-5ace-497a-8554-0e913ea9b0cb
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
# setString-Methode (long, java.lang.String)
    
## setString\-Methode \(long, java.lang.String\)  
 Schreibt den angegebenen **String** in das CLOB \(beginnt bei der angegebenen Position\).  
  
## Syntax  
  
```  
  
public int setString(long pos,  
                     java.lang.String s)  
```  
  
#### Parameter  
 *pos*  
  
 Die Position, an der Daten in das CLOB geschrieben werden sollen.  
  
 *s*  
  
 Der **String** , der in das CLOB geschrieben werden soll.  
  
## Rückgabewert  
 Die Anzahl der geschriebenen Zeichen.  
  
## Ausnahmen  
 java.sql.SQLException  
  
## Hinweise  
 Diese setString\-Methode wird von der setString\-Methode in der java.sql.Clob\-Schnittstelle angegeben.  
  
 Zeichendaten werden beginnend mit der angegebenen Position überschrieben, und sie können die ursprüngliche Länge des CLOB übersteigen. Durch Angeben eines Werts vom Typ Position\+1 wird die Zeichenfolge angefügt. Durch Angeben eines Werts vom Typ Position\+2 oder größer \(oder null oder weniger\) wird ein Positionsfehler ausgelöst.  
  
## Siehe auch  
 [setString-Methode &#40;SQLServerClob&#41;](../content/setString-Method--SQLServerClob-.md)   
 [SQLServerClob-Methoden](../content/SQLServerClob-Methods.md)   
 [SQLServerClob-Elemente](../content/SQLServerClob-Members.md)   
 [SQLServerClob-Klasse](../content/SQLServerClob-Class.md)  
  
  