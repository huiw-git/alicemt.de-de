---
title: "updateCharacterStream-Methode (int, java.io.Reader, int)"
ms.custom: na
ms.date: 07/01/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - drivers
ms.tgt_pltfrm: na
ms.topic: article
apiname: 
  - SQLServerResultSet.updateCharacterStream (int, java.io.Reader, int)
apilocation: 
  - sqljdbc.jar
apitype: Assembly
ms.assetid: b692c372-f6d7-4528-9c5d-cd8421bdb12e
caps.latest.revision: 22
caps.handback.revision: 21
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
# updateCharacterStream-Methode (int, java.io.Reader, int)
    
## updateCharacterStream\-Methode \(int, java.io.Reader, int\)  
 Aktualisiert die angegebene Spalte mit einem Zeichendatenstromwert mit der angegebenen Anzahl von Zeichen.  
  
## Syntax  
  
```  
  
public void updateCharacterStream(int columnIndex,  
                                  java.io.Reader readerValue,  
                                  int length)  
```  
  
#### Parameter  
 *columnIndex*  
  
 Ein Wert vom Typ **int** zum Angeben des Spaltenindex.  
  
 *readerValue*  
  
 Ein Reader\-Objekt.  
  
 *length*  
  
 Ein Wert vom Typ **int** zum Angeben der Datenstromlänge.  
  
## Ausnahmen  
 [SQLServerException](../content/SQLServerException-Class.md)  
  
## Hinweise  
 Diese updateCharacterStream\-Methode wird von der updateCharacterStream\-Methode in der java.sql.ResultSet\-Schnittstelle angegeben.  
  
 Von dieser Methode werden Unicode\-Zeichen aus einem Reader\-Objekt an ausgewählte Text\- und Binärspalten übergeben. Hierzu zählen alle Textspalten sowie Spalten vom Typ **binary**, **varbinary**, **varbinary\(max\)**, **image** und **xml**, aber keine **udt**\-Spalten.  
  
 Entspricht die Länge des Datenstroms nicht der Angabe im *length*\-Parameter, wird vom JDBC\-Treiber beim Aktualisieren oder Einfügen der Zeile eine Ausnahme ausgelöst.  
  
 Ist die Länge des Datenstroms nicht bekannt, kann der *length*\-Parameter auf "\-1" festgelegt werden, um anzugeben, dass der Datenstrom unabhängig von seiner Länge akzeptiert werden soll. Bei "sqljdbc4.jar" empfiehlt sich die Verwendung der JDBC 4.0\-Methode [updateCharacterStream-Methode &#40;int, java.io.Reader&#41;](../content/updateCharacterStream-Method--int--java.io.Reader-.md), wenn von der Anwendung versucht wird, die Spalte aus einem Datenstrom mit unbekannter Länge zu aktualisieren.  
  
## Siehe auch  
 [updateCharacterStream-Methode &#40;ISQLServerResultSet&#41;](../content/updateCharacterStream-Method--SQLServerResultSet-.md)   
 [ISQLServerResultSet-Elemente](../content/SQLServerResultSet-Members.md)   
 [SQLServerResultSet-Klasse](../content/SQLServerResultSet-Class.md)  
  
  