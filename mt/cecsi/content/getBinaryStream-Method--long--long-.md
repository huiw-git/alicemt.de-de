---
title: "getBinaryStream-Methode (long, long)"
ms.custom: na
ms.date: 07/27/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - drivers
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 30bc8882-04b4-4efd-95e4-7d3a2a8c1d47
caps.latest.revision: 11
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
# getBinaryStream-Methode (long, long)
  Gibt unter Verwendung der angegebenen Startposition und Länge ein Eingabedatenstrom\-Objekt mit einem BLOB\-Teilwert zurück.  
  
## Syntax  
  
```  
  
public java.io.InputStream getBinaryStream(long pos, long length)  
```  
  
#### Parameter  
 *pos*  
  
 Das Offset zum ersten Byte des abzurufenden Teilwerts.  
  
 *length*  
  
 Die Länge in Bytes des abzurufenden Teilwerts.  
  
## Rückgabewert  
 Ein Eingabedatenstrom mit den BLOB\-Daten.  
  
## Ausnahmen  
 [SQLServerException](../content/SQLServerException-Class.md)  
  
## Hinweise  
 Diese getBinaryStream\-Methode wird von der getBinaryStream\-Methode in der java.sql.Blob\-Schnittstelle angegeben.  
  
## Siehe auch  
 [SQLServerBlob-Methoden](../content/SQLServerBlob-Methods.md)   
 [SQLServerBlob-Elemente](../content/SQLServerBlob-Members.md)   
 [SQLServerBlob-Klasse](../content/SQLServerBlob-Class.md)  
  
  