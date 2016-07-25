---
title: "updateAsciiStream-Methode (int, java.io.InputStream, long)"
ms.custom: na
ms.date: 07/01/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - drivers
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 143bff3e-2b5c-485d-9529-1c2387560094
caps.latest.revision: 19
caps.handback.revision: 18
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
# updateAsciiStream-Methode (int, java.io.InputStream, long)
  Aktualisiert die angegebene Spalte mit einem ASCII\-Datenstromwert mit der angegebenen Anzahl von Bytes.  
  
## Syntax  
  
```  
  
public void updateAsciiStream(int columnIndex,  
                              java.io.InputStream x,  
                              long length)  
```  
  
#### Parameter  
 *columnIndex*  
  
 Ein Wert vom Typ **int** zum Angeben des Spaltenindex.  
  
 *x*  
  
 Ein InputStream\-Objekt.  
  
 *length*  
  
 Die Länge des Datenstroms.  
  
## Ausnahmen  
 [SQLServerException](../content/SQLServerException-Class.md)  
  
## Hinweise  
 Diese updateAsciiStream\-Methode wird von der updateAsciiStream\-Methode in der java.sql.ResultSet\-Schnittstelle angegeben.  
  
 Von dieser Methode werden ASCII\-Zeichen \(Bytes\) von einem InputStream\-Objekt an konvertierbare Zeichenspalten übergeben, bei denen es sich um den ASCII\-Bereich "\[0x00 \- 0x7F\]" von Unicode sowie um die Codepages 874, 932, 936, 949, 950 und 1250 bis 1258 handelt. Von dieser Methode wird eine Konvertierung zur Zielsortierseite vorgenommen. Beim Versuch, eine nicht konvertierbare Zielspalte zu aktualisieren, wird eine Ausnahme ausgelöst. Für Binärspalten werden Rohbytes übergeben.  
  
 Entspricht die Länge des Datenstroms nicht der Angabe im *length*\-Parameter, wird vom JDBC\-Treiber beim Aktualisieren oder Einfügen der Zeile eine Ausnahme ausgelöst.  
  
 Ist die Länge des Datenstroms nicht bekannt, kann der *length*\-Parameter auf "\-1" festgelegt werden, um anzugeben, dass der Datenstrom unabhängig von seiner Länge akzeptiert werden soll. Bei "sqljdbc4.jar" empfiehlt sich die Verwendung der JDBC 4.0\-Methode [updateAsciiStream-Methode &#40;int, java.io.InputStream&#41;](../content/updateAsciiStream-Method--int--java.io.InputStream-.md), wenn von der Anwendung versucht wird, die Spalte aus einem Datenstrom mit unbekannter Länge zu aktualisieren.  
  
## Siehe auch  
 [updateAsciiStream-Methode &#40;ISQLServerResultSet&#41;](../content/updateAsciiStream-Method--SQLServerResultSet-.md)   
 [ISQLServerResultSet-Elemente](../content/SQLServerResultSet-Members.md)   
 [SQLServerResultSet-Klasse](../content/SQLServerResultSet-Class.md)  
  
  