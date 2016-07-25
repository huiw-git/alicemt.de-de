---
title: "updateBinaryStream-Methode (int, java.io.InputStream, int)"
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
  - SQLServerResultSet.updateBinaryStream (int, java.io.InputStream, int)
apilocation: 
  - sqljdbc.jar
apitype: Assembly
ms.assetid: c8e55377-aaea-4415-8159-938fab1b2a93
caps.latest.revision: 21
caps.handback.revision: 20
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
# updateBinaryStream-Methode (int, java.io.InputStream, int)
    
## updateBinaryStream\-Methode \(int, java.io.InputStream, int\)  
 Aktualisiert die angegebene Spalte mit einem Binärdatenstromwert mit der angegebenen Anzahl von Bytes.  
  
## Syntax  
  
```  
  
public void updateBinaryStream(int columnIndex,  
                               java.io.InputStream x,  
                               int length)  
```  
  
#### Parameter  
 *columnIndex*  
  
 Ein Wert vom Typ **int** zum Angeben des Spaltenindexes.  
  
 *x*  
  
 Ein InputStream\-Objekt.  
  
 *length*  
  
 Ein Wert vom Typ **int** zum Angeben der Datenstromlänge.  
  
## Ausnahmen  
 [SQLServerException](../content/SQLServerException-Class.md)  
  
## Hinweise  
 Diese updateBinaryStream\-Methode wird von der updateBinaryStream\-Methode in der java.sql.ResultSet\-Schnittstelle angegeben.  
  
 Von dieser Methode werden Bytes aus einem InputStream\-Objekt an ausgewählte [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)]\-Binärspalten wie "binary", "varbinary", "varbinary\(max\)", "image", "xml" oder "udt" übergeben. Das Aktualisieren von Zeichenspalten wird für diese Methode nicht unterstützt. Verwenden Sie die [updateAsciiStream](../content/updateAsciiStream-Method--SQLServerResultSet-.md)\-Methode, um Zeichenspalten mit einem InputStream zu aktualisieren.  
  
 Entspricht die Länge des Datenstroms nicht der Angabe im *length*\-Parameter, wird vom JDBC\-Treiber beim Aktualisieren oder Einfügen der Zeile eine Ausnahme ausgelöst.  
  
 Ist die Länge des Datenstroms nicht bekannt, kann der *length*\-Parameter auf "\-1" festgelegt werden, um anzugeben, dass der Datenstrom unabhängig von seiner Länge akzeptiert werden soll. Bei "sqljdbc4.jar" empfiehlt sich die Verwendung der JDBC 4.0\-Methode [updateBinaryStream-Methode &#40;int, java.io.InputStream&#41;](../content/updateBinaryStream-Method--int--java.io.InputStream-.md), wenn von der Anwendung versucht wird, die Spalte aus einem Datenstrom mit unbekannter Länge zu aktualisieren.  
  
## Siehe auch  
 [updateBinaryStream-Methode &#40;ISQLServerResultSet&#41;](../content/updateBinaryStream-Method--SQLServerResultSet-.md)   
 [ISQLServerResultSet-Elemente](../content/SQLServerResultSet-Members.md)   
 [SQLServerResultSet-Klasse](../content/SQLServerResultSet-Class.md)  
  
  