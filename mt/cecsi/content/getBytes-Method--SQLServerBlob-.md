---
title: "getBytes-Methode (SQLServerBlob)"
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
  - SQLServerBlob.getBytes
apilocation: 
  - sqljdbc.jar
apitype: Assembly
ms.assetid: bea1b810-b5c1-466d-bdc4-561468214632
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
# getBytes-Methode (SQLServerBlob)
  Ruft die BLOB\-Daten als Bytearray ab.  
  
## Syntax  
  
```  
  
public byte[] getBytes(long pos,  
                       int length)  
```  
  
#### Parameter  
 *pos*  
  
 Die Startposition, beginnend bei "1" \(nicht "0"\).  
  
 *length*  
  
 Die Länge der abzurufenden Daten.  
  
## Rückgabewert  
 Ein **byte** \-Array mit den angeforderten Daten.  
  
## Ausnahmen  
 [SQLServerException](../content/SQLServerException-Class.md)  
  
## Hinweise  
 Diese getBytes\-Methode wird von der getBytes\-Methode in der java.sql.Blob\-Schnittstelle angegeben.  
  
 Bei einem BLOB, der NULL ist oder die Länge 0 besitzt, wird ein leeres **byte**\-Array zurückgegeben \(ein Bytearray der Länge "0"\), wenn Sie versuchen, genau 0 Bytes an Position "1" abzurufen.  
  
 Bei einem BLOB mit der Länge Null wird beim Versuch, eine beliebige Länge in Bytes an einer anderen Position als "1" abzurufen, eine Positionsausnahme ausgelöst.  
  
## Siehe auch  
 [SQLServerBlob-Methoden](../content/SQLServerBlob-Methods.md)   
 [SQLServerBlob-Elemente](../content/SQLServerBlob-Members.md)   
 [SQLServerBlob-Klasse](../content/SQLServerBlob-Class.md)  
  
  