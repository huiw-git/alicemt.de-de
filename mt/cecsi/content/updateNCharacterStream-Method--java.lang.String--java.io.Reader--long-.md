---
title: "updateNCharacterStream-Methode (java.lang.String, java.io.Reader, long)"
ms.custom: na
ms.date: 07/01/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - drivers
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: db0a96a8-248f-4664-9c13-f480f309ab91
caps.latest.revision: 20
caps.handback.revision: 19
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
# updateNCharacterStream-Methode (java.lang.String, java.io.Reader, long)
  Aktualisiert die angegebene Spalte mit einem Zeichendatenstromwert mit der angegebenen Anzahl von Bytes.  
  
## Syntax  
  
```  
  
public void updateNCharacterStream(java.lang.String columnLabel,  
                                    java.io.Reader reader,  
                                    long length)  
```  
  
#### Parameter  
 *columnLabel*  
  
 Ein **String** mit der Spaltenbezeichnung.  
  
 *reader*  
  
 Ein Reader\-Objekt.  
  
 *length*  
  
 Die Länge des Datenstroms.  
  
## Ausnahmen  
 [SQLServerException](../content/SQLServerException-Class.md)  
  
## Hinweise  
 Diese updateNCharacterStream\-Methode wird von der updateNCharacterStream\-Methode in der java.sql.ResultSet\-Schnittstelle angegeben.  
  
 Von dieser Methode werden Unicode\-Zeichen aus einem Reader\-Objekt an ausgewählte Spalten vom Typ **nchar**, **nvarchar\(max\)**, **ntext** und **xml** übergeben. Bei Verwendung dieser Methode für andere Datentypspalten wird eine Ausnahme ausgelöst.  
  
 Entspricht die Länge des Datenstroms nicht der Angabe im *length*\-Parameter, wird vom JDBC\-Treiber beim Aktualisieren oder Einfügen der Zeile eine Ausnahme ausgelöst.  
  
 Ist die Länge des Datenstroms nicht bekannt, kann der *length*\-Parameter auf "\-1" festgelegt werden, um anzugeben, dass der Datenstrom unabhängig von seiner Länge akzeptiert werden soll. Bei "sqljdbc4.jar" empfiehlt sich die Verwendung der JDBC 4.0\-Methode [updateNCharacterStream-Methode &#40;java.lang.String, java.io.Reader&#41;](../content/updateNCharacterStream-Method--java.lang.String--java.io.Reader-.md), wenn von der Anwendung versucht wird, die Spalte aus einem Datenstrom mit unbekannter Länge zu aktualisieren.  
  
## Siehe auch  
 [updateNCharacterStream-Methode &#40;ISQLServerResultSet&#41;](../content/updateNCharacterStream-Method--SQLServerResultSet-.md)   
 [ISQLServerResultSet-Elemente](../content/SQLServerResultSet-Members.md)   
 [SQLServerResultSet-Klasse](../content/SQLServerResultSet-Class.md)  
  
  