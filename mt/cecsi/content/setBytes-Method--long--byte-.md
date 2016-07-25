---
title: "setBytes-Methode (long, byte)"
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
  - SQLServerBlob.setBytes (long.byte[])
apilocation: 
  - sqljdbc.jar
apitype: Assembly
ms.assetid: ffb8f107-0f9d-4410-957f-62b718e1e872
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
# setBytes-Methode (long, byte)
    
## setBytes\-Methode \(long, byte\[\]\)  
 Schreibt das angegebene Bytearray ab der angegebenen Position in das BLOB und gibt anschließend die Anzahl der geschriebenen Bytes zurück.  
  
## Syntax  
  
```  
  
public int setBytes(long pos,  
                    byte[] bytes)  
```  
  
#### Parameter  
 *pos*  
  
 Die Position \(1\-basiert\) im BLOB, ab der Daten geschrieben werden.  
  
 *bytes*  
  
 Das in den BLOB zu schreibende Bytearray.  
  
## Rückgabewert  
 Ein **long** \-Wert, der die Anzahl geschriebener Bytes angibt.  
  
## Ausnahmen  
 java.sql.SQLException  
  
## Hinweise  
 Diese setBytes\-Methode wird von der setBytes\-Methode in der java.sql.Blob\-Schnittstelle angegeben.  
  
 Daten werden beginnend mit der angegebenen Position überschrieben, und sie können die ursprüngliche Länge des BLOB übersteigen. Durch Angeben eines Werts vom Typ Position\+1 werden Bytes an die Zeichenfolge angefügt. Durch Weitergeben eines Werts vom Typ Position\+2 oder größer \(oder null oder weniger\) wird ein Positionsfehler ausgelöst. Durch Weitergeben eines **byte** arrays mit einer Länge von NULL wird NULL zurückgegeben, weil keine Bytes geschrieben wurden.  
  
## Siehe auch  
 [setBytes-Methode &#40;SQLServerBlob&#41;](../content/setBytes-Method--SQLServerBlob-.md)   
 [SQLServerBlob-Methoden](../content/SQLServerBlob-Methods.md)   
 [SQLServerBlob-Elemente](../content/SQLServerBlob-Members.md)   
 [SQLServerBlob-Klasse](../content/SQLServerBlob-Class.md)  
  
  