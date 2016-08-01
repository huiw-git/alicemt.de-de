---
title: "updateAsciiStream-Methode (java.lang.String, java.io.InputStream)"
ms.custom: na
ms.date: 07/27/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - drivers
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 747b0308-1ce6-4eba-bdfc-af29c21c18cf
caps.latest.revision: 17
caps.handback.revision: 16
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
# updateAsciiStream-Methode (java.lang.String, java.io.InputStream)
  Aktualisiert die angegebene Spalte mit einem ASCII\-Datenstromwert.  
  
## Syntax  
  
```  
  
public void updateAsciiStream(java.lang.String columnLabel,  
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
 Diese updateAsciiStream\-Methode wird von der updateAsciiStream\-Methode in der java.sql.ResultSet\-Schnittstelle angegeben.  
  
 Von dieser Methode werden ASCII\-Zeichen \(Bytes\) von einem InputStream\-Objekt an konvertierbare Zeichenspalten übergeben, bei denen es sich um den ASCII\-Bereich "\[0x00 \- 0x7F\]" von Unicode sowie um die Codepages 874, 932, 936, 949, 950 und 1250 bis 1258 handelt. Von dieser Methode wird eine Konvertierung zur Zielsortierseite vorgenommen. Beim Versuch, eine nicht konvertierbare Zielspalte zu aktualisieren, wird eine Ausnahme ausgelöst. Für Binärspalten werden Rohbytes übergeben.  
  
 Die Verwendung dieser Methode für die Datentypen **image**, **text** und **ntext** von [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] kann sich negativ auf die Leistung auswirken.  
  
## Siehe auch  
 [updateAsciiStream-Methode &#40;ISQLServerResultSet&#41;](../content/updateAsciiStream-Method--SQLServerResultSet-.md)   
 [ISQLServerResultSet-Elemente](../content/SQLServerResultSet-Members.md)   
 [SQLServerResultSet-Klasse](../content/SQLServerResultSet-Class.md)  
  
  