---
title: "getCharacterStream-Methode (long, long) (SQLServerNClob)"
ms.custom: na
ms.date: 07/27/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - drivers
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 5a8028bc-c877-4668-b662-0746d462040e
caps.latest.revision: 14
caps.handback.revision: 14
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
# getCharacterStream-Methode (long, long) (SQLServerNClob)
  Ruft die **NCLOB**\-Daten als **Reader**\-Objekt oder als Zeichendatenstrom mit angegebener Position und Länge ab.  
  
## Syntax  
  
```  
  
public java.io.Reader getCharacterStream(long pos,  
                                  long length)  
```  
  
#### Parameter  
 *pos*  
  
 Ein **long**\-Wert, mit dem das Offset zum ersten Zeichen des abzurufenden Teilwerts angegeben wird.  
  
 *length*  
  
 Ein **long**\-Wert, mit dem die Länge \(in Zeichen\) des abzurufenden Teilwerts angegeben wird.  
  
## Rückgabewert  
 Ein Reader\-Objekt, das die **NCLOB**\-Daten enthält.  
  
## Ausnahmen  
 [SQLServerException](../content/SQLServerException-Class.md)  
  
## Hinweise  
 Diese getCharacterStream\-Methode wird von der getCharacterStream\-Methode in der java.sql.NClob\-Schnittstelle angegeben.  
  
## Siehe auch  
 [getCharacterStream-Methode &#40;SQLServerNClob&#41;](../content/getCharacterStream-Method--SQLServerNClob-.md)   
 [SQLServerNClob-Methoden](../content/SQLServerNClob-Methods.md)   
 [SQLServerNClob-Elemente](../content/SQLServerNClob-Members.md)   
 [SQLServerNClob-Klasse](../content/SQLServerNClob-Class.md)  
  
  