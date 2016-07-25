---
title: "updateBinaryStream-Methode (int, java.io.InputStream)"
ms.custom: na
ms.date: 07/01/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - drivers
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 1db3a975-c108-45d1-8c0d-14a094f391bd
caps.latest.revision: 18
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
# updateBinaryStream-Methode (int, java.io.InputStream)
  Aktualisiert die angegebene Spalte mit einem Binärdatenstromwert.  
  
## Syntax  
  
```  
  
public void updateBinaryStream(int columnIndex,  
                               java.io.InputStream x)  
```  
  
#### Parameter  
 *columnIndex*  
  
 Ein Wert vom Typ **int** zum Angeben des Spaltenindex.  
  
 *x*  
  
 Ein InputStream\-Objekt.  
  
## Ausnahmen  
 [SQLServerException](../content/SQLServerException-Class.md)  
  
## Hinweise  
 Diese updateBinaryStream\-Methode wird von der updateBinaryStream\-Methode in der java.sql.ResultSet\-Schnittstelle angegeben.  
  
 Die Verwendung dieser Methode für die Datentypen **image**, **text** und **ntext** von [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] kann sich negativ auf die Leistung auswirken.  
  
 Von dieser Methode werden Bytes aus einem InputStream\-Objekt an ausgewählte [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)]\-Binärspalten wie "binary", "varbinary", "varbinary\(max\)", "image", "xml" oder "udt" übergeben. Das Aktualisieren von Zeichenspalten wird für diese Methode nicht unterstützt. Verwenden Sie die [updateAsciiStream](../content/updateAsciiStream-Method--SQLServerResultSet-.md)\-Methode, um Zeichenspalten mit einem InputStream zu aktualisieren.  
  
## Siehe auch  
 [updateBinaryStream-Methode &#40;ISQLServerResultSet&#41;](../content/updateBinaryStream-Method--SQLServerResultSet-.md)   
 [ISQLServerResultSet-Elemente](../content/SQLServerResultSet-Members.md)   
 [SQLServerResultSet-Klasse](../content/SQLServerResultSet-Class.md)  
  
  