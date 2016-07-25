---
title: "getCharacterStream-Methode (long, long)"
ms.custom: na
ms.date: 07/01/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - drivers
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: d70f502f-f60f-436a-83e6-797a0ed71bf3
caps.latest.revision: 17
caps.handback.revision: 17
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
# getCharacterStream-Methode (long, long)
  Gibt die **Clob**\-Daten als Reader\-Objekt oder als Zeichendatenstrom mit der angegebenen Position und Länge zurück.  
  
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
 Ein Reader\-Objekt, das die **Clob**\-Daten enthält.  
  
## Ausnahmen  
 [SQLServerException](../content/SQLServerException-Class.md)  
  
## Hinweise  
 Diese getCharacterStream\-Methode wird von der getCharacterStream\-Methode in der java.sql.Clob\-Schnittstelle angegeben.  
  
## Siehe auch  
 [getCharacterStream-Methode &#40;SQLServerClob&#41;](../content/getCharacterStream-Method--SQLServerClob-.md)   
 [SQLServerClob-Methoden](../content/SQLServerClob-Methods.md)   
 [SQLServerClob-Elemente](../content/SQLServerClob-Members.md)  
  
  