---
title: "setAsciiStream-Methode (java.lang.String, java.io.InputStream, int)"
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
  - SQLServerCallableStatement.setAsciiStream
apilocation: 
  - sqljdbc.jar
apitype: Assembly
ms.assetid: 6ea23386-201f-41af-8232-225de3476765
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
# setAsciiStream-Methode (java.lang.String, java.io.InputStream, int)
    
## setAsciiStream\-Methode \(java.lang.String, java.io.InputStream, int\)  
 Legt den angegebenen Parameter auf den angegebenen Eingabedatenstrom mit der angegebenen Anzahl von Bytes fest.  
  
## Syntax  
  
```  
  
public void setAsciiStream(java.lang.String parameterName,  
                           java.io.InputStream value,  
                           int length)  
```  
  
#### Parameter  
 *parameterName*  
  
 Ein **String** mit dem Parameternamen.  
  
 *value*  
  
 Ein InputStream\-Objekt.  
  
 *length*  
  
 Ein Wert vom Typ **int** zum Angeben der Länge als Anzahl von Bytes.  
  
## Ausnahmen  
 [SQLServerException](../content/SQLServerException-Class.md)  
  
## Hinweise  
 Diese setAsciiStream\-Methode wird von der setAsciiStream\-Methode in der java.sql.CallableStatement\-Schnittstelle angegeben.  
  
 Entspricht die Länge des Datenstroms nicht der Angabe im *length*\-Parameter, wird vom JDBC\-Treiber beim Aktualisieren oder Einfügen der Zeile eine Ausnahme ausgelöst.  
  
 Ist die Länge des Datenstroms nicht bekannt, kann der *length*\-Parameter auf "\-1" festgelegt werden, um anzugeben, dass der Datenstrom unabhängig von seiner Länge akzeptiert werden soll. Bei "sqljdbc4.jar" empfiehlt sich die Verwendung der JDBC 4.0\-Methode [setAsciiStream\-Methode \(java.lang.String, java.io.InputStream\)](../content/setAsciiStream-Method--java.lang.String--java.io.InputStream-.md), wenn von der Anwendung versucht wird, die Spalte aus einem Datenstrom mit unbekannter Länge zu aktualisieren.  
  
## Siehe auch  
 [SQLServerCallableStatement-Elemente](../content/SQLServerCallableStatement-Members.md)   
 [SQLServerCallableStatement-Klasse](../content/SQLServerCallableStatement-Class.md)  
  
  