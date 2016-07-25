---
title: "setCharacterStream-Methode (SQLServerClob)"
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
  - SQLServerClob.setCharacterStream
apilocation: 
  - sqljdbc.jar
apitype: Assembly
ms.assetid: c02778f2-6681-4a84-a58b-2bcfac4233e4
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
# setCharacterStream-Methode (SQLServerClob)
    
## setCharacterStream\-Methode \(SQLServerClob\)  
 Gibt einen Datenstrom zurück, der verwendet wird, um ab der angegebenenPosition einen Unicode\-Zeichendatenstrom in das CLOB zu schreiben.  
  
## Syntax  
  
```  
  
public java.io.Writer setCharacterStream(long pos)  
```  
  
#### Parameter  
 *pos*  
  
 Die Position, an der Daten in das CLOB\-Objekt geschrieben werden sollen.  
  
## Rückgabewert  
 Ein Datenstrom, in den Unicode\-codierte Zeichen geschrieben werden können.  
  
## Ausnahmen  
 java.sql.SQLException  
  
## Hinweise  
 Diese setCharacterStream\-Methode wird von der setCharacterStream\-Methode in der java.sql.Clob\-Schnittstelle angegeben.  
  
 Zeichendaten im CLOB werden beginnend mit der angegebenen Position vom Schreiber überschrieben, und sie können die ursprüngliche Länge des CLOB übersteigen. Durch Angeben eines Werts vom Typ Position\+1 werden Zeichen angefügt. Durch Angeben eines Werts vom Typ Position\+2 oder größer \(oder null oder weniger\) wird ein Positionsfehler ausgelöst.  
  
## Siehe auch  
 [SQLServerClob-Methoden](../content/SQLServerClob-Methods.md)   
 [SQLServerClob-Elemente](../content/SQLServerClob-Members.md)   
 [SQLServerClob-Klasse](../content/SQLServerClob-Class.md)  
  
  