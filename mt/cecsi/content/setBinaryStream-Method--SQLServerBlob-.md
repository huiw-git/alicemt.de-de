---
title: "setBinaryStream-Methode (SQLServerBlob)"
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
  - SQLServerBlob.setBinaryStream
apilocation: 
  - sqljdbc.jar
apitype: Assembly
ms.assetid: abcec31f-1a60-4765-9725-8cf7e9f1f8ab
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
# setBinaryStream-Methode (SQLServerBlob)
    
## setBinaryStream\-Methode \(SQLServerBlob\)  
 Ruft einen Datenstrom ab, mit dem in den BLOB\-Wert geschrieben werden kann.  
  
## Syntax  
  
```  
  
public java.io.OutputStream setBinaryStream(long pos)  
```  
  
#### Parameter  
 *Pos*  
  
 Die Position im BLOB\-Wert, an der geschrieben werden soll.  
  
## Rückgabewert  
 Ein Ausgabedatenstrom.  
  
## Ausnahmen  
 java.sql.SQLException  
  
## Hinweise  
 Diese setBinaryStream\-Methode wird von der setBinaryStream\-Methode in der java.sql.Blob\-Schnittstelle angegeben.  
  
 Daten im BLOB werden beginnend mit der angegebenen Position vom Ausgabedatenstrom überschrieben, und sie können die ursprüngliche Länge des BLOB übersteigen. Durch Angeben eines Werts vom Typ Position\+1 werden Bytes an die Zeichenfolge angefügt. Durch Weitergeben eines Werts vom Typ Position\+2 oder größer \(oder null oder weniger\) wird ein Positionsfehler ausgelöst.  
  
## Siehe auch  
 [SQLServerBlob-Methoden](../content/SQLServerBlob-Methods.md)   
 [SQLServerBlob-Elemente](../content/SQLServerBlob-Members.md)   
 [SQLServerBlob-Klasse](../content/SQLServerBlob-Class.md)  
  
  