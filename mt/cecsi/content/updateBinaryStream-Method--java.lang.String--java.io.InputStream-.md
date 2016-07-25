---
title: "updateBinaryStream-Methode (java.lang.String, java.io.InputStream)"
ms.custom: na
ms.date: 07/01/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - drivers
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 56883144-26a0-4f45-ad36-4f616369af3e
caps.latest.revision: 16
caps.handback.revision: 15
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
# updateBinaryStream-Methode (java.lang.String, java.io.InputStream)
  Aktualisiert die angegebene Spalte mit einem Binärdatenstromwert.  
  
## Syntax  
  
```  
  
public void updateBinaryStream(java.lang.String columnLabel,  
                               java.io.InputStream x)  
```  
  
#### Parameter  
 *columnLabel*  
  
 Ein **String** mit der Spaltenbezeichnung.  
  
 *x*  
  
 Ein InputStream\-Objekt.  
  
## Ausnahmen  
 [SQLServerException](../content/SQLServerException-Class.md)  
  
## Hinweise  
 Diese updateBinaryStream\-Methode wird von der updateBinaryStream\-Methode in der java.sql.ResultSet\-Schnittstelle angegeben.  
  
 Die Verwendung dieser Methode für die Datentypen **image**, **text** und **ntext** von SQL Server kann sich negativ auf die Leistung auswirken.  
  
 Von dieser Methode werden Bytes aus einem InputStream\-Objekt an ausgewählte [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)]\-Binärspalten wie "binary", "varbinary", "varbinary\(max\)", "image", "xml" oder "udt" übergeben. Das Aktualisieren von Zeichenspalten wird für diese Methode nicht unterstützt. Verwenden Sie die [updateAsciiStream](../content/updateAsciiStream-Method--SQLServerResultSet-.md)\-Methode, um Zeichenspalten mit einem InputStream zu aktualisieren.  
  
## Siehe auch  
 [updateBinaryStream-Methode &#40;ISQLServerResultSet&#41;](../content/updateBinaryStream-Method--SQLServerResultSet-.md)   
 [ISQLServerResultSet-Elemente](../content/SQLServerResultSet-Members.md)   
 [SQLServerResultSet-Klasse](../content/SQLServerResultSet-Class.md)  
  
  