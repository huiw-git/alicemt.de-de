---
title: "setBytes-Methode (long, byte, int, int)"
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
  - SQLServerBlob.setBytes (long.byte[], int, int)
apilocation: 
  - sqljdbc.jar
apitype: Assembly
ms.assetid: 7def226c-b211-459e-8c1a-08592d75d4a4
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
# setBytes-Methode (long, byte, int, int)
    
## setBytes\-Methode \(long, byte\[\], int, int\)  
 Schreibt ab der angegebenen Position, dem Offset und der Länge das gesamte Bytearray oder einen Teil des Bytearrays in das BLOB und gibt anschließend die Anzahl der geschriebenen Bytes zurück.  
  
## Syntax  
  
```  
  
public int setBytes(long pos,  
                    byte[] bytes,  
                    int offset,  
                    int len)  
```  
  
#### Parameter  
 *pos*  
  
 Die Position \(1\-basiert\) im BLOB, ab der Daten geschrieben werden.  
  
 *bytes*  
  
 Das in den BLOB zu schreibende Bytearray.  
  
 *offset*  
  
 Das Offset im Bytearray, ab dem Daten im **byte** \-Array gelesen werden sollen.  
  
 *len*  
  
 Die Anzahl von Bytes, die aus dem Bytearray in das BLOB geschrieben werden sollen.  
  
## Rückgabewert  
 Ein Element vom Typ **int** mit der Anzahl der geschriebenen Bytes.  
  
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
  
  