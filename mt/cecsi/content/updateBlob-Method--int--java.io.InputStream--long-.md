---
title: "updateBlob-Methode (int, java.io.InputStream, long)"
ms.custom: na
ms.date: 07/27/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - drivers
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 2edf9b51-63e1-4c28-afdf-2d4af593d5f7
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
# updateBlob-Methode (int, java.io.InputStream, long)
  Aktualisiert die angegebene Spalte unter Verwendung des angegebenen Eingabedatenstroms mit der angegebenen Anzahl von Bytes.  
  
## Syntax  
  
```  
  
public void updateBlob(int columnIndex,  
                       java.io.InputStream inputStream,  
                                              long length)  
```  
  
#### Parameter  
 *columnIndex*  
  
 Ein Wert vom Typ **int** zum Angeben des Spaltenindex.  
  
 *inputStream*  
  
 Ein InputStream\-Objekt.  
  
 *length*  
  
 Ein Wert vom Typ **long** zum Angeben der Datenstromlänge.  
  
## Ausnahmen  
 [SQLServerException](../content/SQLServerException-Class.md)  
  
## Hinweise  
 Diese updateBlob\-Methode wird von der updateBlob\-Methode in der java.sql.ResultSet\-Schnittstelle angegeben.  
  
## Siehe auch  
 [updateBlob-Methode &#40;ISQLServerResultSet&#41;](../content/updateBlob-Method--SQLServerResultSet-.md)   
 [ISQLServerResultSet-Elemente](../content/SQLServerResultSet-Members.md)   
 [SQLServerResultSet-Klasse](../content/SQLServerResultSet-Class.md)  
  
  