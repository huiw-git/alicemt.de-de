---
title: "setAsciiStream-Methode (SQLServerClob)"
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
  - SQLServerClob.setAsciiStream
apilocation: 
  - sqljdbc.jar
apitype: Assembly
ms.assetid: 6e1779df-3b2a-41d1-8dca-99692cc9da14
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
# setAsciiStream-Methode (SQLServerClob)
    
## setAsciiStream\-Methode \(SQLServerClob\)  
 Gibt einen Datenstrom zurück, der verwendet wird, um ab der angegebenen Position ASCII\-Zeichen in das CLOB zu schreiben.  
  
## Syntax  
  
```  
  
public java.io.OutputStream setAsciiStream(long pos)  
```  
  
#### Parameter  
 *pos*  
  
 Die Position, an der Daten in das CLOB\-Objekt geschrieben werden sollen.  
  
## Rückgabewert  
 Der Datenstrom, in den ASCII\-codierte Zeichen geschrieben werden können.  
  
## Ausnahmen  
 java.sql.SQLException  
  
## Hinweise  
 Diese setAsciiStream\-Methode wird von der setAsciiStream\-Methode in der java.sql.Clob\-Schnittstelle angegeben.  
  
 Zeichendaten im CLOB werden beginnend mit der angegebenen Position vom Ausgabedatenstrom überschrieben, und sie können die ursprüngliche Länge des CLOB übersteigen. Durch Angeben eines Werts vom Typ Position\+1 werden ASCII\-Zeichen angefügt. Durch Angeben eines Werts vom Typ Position\+2 oder größer \(oder null oder weniger\) wird ein Positionsfehler ausgelöst.  
  
## Siehe auch  
 [SQLServerClob-Methoden](../content/SQLServerClob-Methods.md)   
 [SQLServerClob-Elemente](../content/SQLServerClob-Members.md)   
 [SQLServerClob-Klasse](../content/SQLServerClob-Class.md)  
  
  