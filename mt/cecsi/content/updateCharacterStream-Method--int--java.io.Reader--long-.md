---
title: "updateCharacterStream-Methode (int, java.io.Reader, long)"
ms.custom: na
ms.date: 07/01/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - drivers
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: c426b0e3-2f9d-425a-b7da-1d0325e292d1
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
# updateCharacterStream-Methode (int, java.io.Reader, long)
  Aktualisiert die angegebene Spalte mit einem Zeichendatenstromwert mit der angegebenen Anzahl von Zeichen.  
  
## Syntax  
  
```  
  
public void updateCharacterStream(int columnIndex,  
                                  java.io.Reader x,  
                                  long length)  
```  
  
#### Parameter  
 *columnIndex*  
  
 Ein Wert vom Typ **int** zum Angeben des Spaltenindex.  
  
 *x*  
  
 Ein Reader\-Objekt.  
  
 *length*  
  
 Die Länge des Datenstroms.  
  
## Ausnahmen  
 [SQLServerException](../content/SQLServerException-Class.md)  
  
## Hinweise  
 Diese updateCharacterStream\-Methode wird von der updateCharacterStream\-Methode in der java.sql.ResultSet\-Schnittstelle angegeben.  
  
 Von dieser Methode werden Unicode\-Zeichen aus einem Reader\-Objekt an ausgewählte Text\- und Binärspalten übergeben. Hierzu zählen alle Textspalten sowie Spalten vom Typ "binary", "varbinary", "varbinary\(max\)", "image" und "XML", aber keine UDT\-Spalten.  
  
 Entspricht die Länge des Datenstroms nicht der Angabe im *length*\-Parameter, wird vom JDBC\-Treiber beim Aktualisieren oder Einfügen der Zeile eine Ausnahme ausgelöst.  
  
 Ist die Länge des Datenstroms nicht bekannt, kann der *length*\-Parameter auf "\-1" festgelegt werden, um anzugeben, dass der Datenstrom unabhängig von seiner Länge akzeptiert werden soll. Bei "sqljdbc4.jar" empfiehlt sich die Verwendung der JDBC 4.0\-Methode [updateCharacterStream-Methode &#40;int, java.io.Reader&#41;](../content/updateCharacterStream-Method--int--java.io.Reader-.md), wenn von der Anwendung versucht wird, die Spalte aus einem Datenstrom mit unbekannter Länge zu aktualisieren.  
  
## Siehe auch  
 [updateCharacterStream-Methode &#40;ISQLServerResultSet&#41;](../content/updateCharacterStream-Method--SQLServerResultSet-.md)   
 [ISQLServerResultSet-Elemente](../content/SQLServerResultSet-Members.md)   
 [SQLServerResultSet-Klasse](../content/SQLServerResultSet-Class.md)  
  
  