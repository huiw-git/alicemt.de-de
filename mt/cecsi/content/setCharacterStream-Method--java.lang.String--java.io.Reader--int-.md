---
title: "setCharacterStream-Methode (java.lang.String, java.io.Reader, int)"
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
  - SQLServerCallableStatement.setCharacterStream
apilocation: 
  - sqljdbc.jar
apitype: Assembly
ms.assetid: 88a8e89e-8817-4161-85b1-9a9a2fd01cdb
caps.latest.revision: 23
caps.handback.revision: 22
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
# setCharacterStream-Methode (java.lang.String, java.io.Reader, int)
    
## setCharacterStream\-Methode \(java.lang.String, java.io.Reader, int\)  
 Legt den angegebenen Parameter auf das angegebeneReader\-Objekt fest, dessen Längeder angegebenen Zeichenanzahl entspricht.  
  
## Syntax  
  
```  
  
public final void setCharacterStream(java.lang.String parameterName,  
                              java.io.Reader value,  
                              int length)  
```  
  
#### Parameter  
 *parameterName*  
  
 Ein **String** mit dem Namen des Parameters.  
  
 *value*  
  
 Ein Reader\-Objekt, das die Unicode\-Daten enthält.  
  
 *length*  
  
 Ein Wert vom Typ **int** zum Angeben der Länge als Anzahl von Zeichen.  
  
## Ausnahmen  
 [SQLServerException](../content/SQLServerException-Class.md)  
  
## Hinweise  
 Diese setCharacterStream\-Methode wird von der setCharacterStream\-Methode in der java.sql.CallableStatement\-Schnittstelle angegeben.  
  
 Entspricht die Länge des Datenstroms nicht der Angabe im *length*\-Parameter, wird vom JDBC\-Treiber beim Aktualisieren oder Einfügen der Zeile eine Ausnahme ausgelöst.  
  
 Ist die Länge des Datenstroms nicht bekannt, kann der *length*\-Parameter auf "\-1" festgelegt werden, um anzugeben, dass der Datenstrom unabhängig von seiner Länge akzeptiert werden soll. Bei "sqljdbc4.jar" empfiehlt sich die Verwendung der JDBC 4.0\-Methode [setCharacterStream\-Methode \(java.lang.String, java.io.Reader\)](../content/setCharacterStream-Method--java.lang.String--java.io.Reader-.md), wenn von der Anwendung versucht wird, die Spalte aus einem Datenstrom mit unbekannter Länge zu aktualisieren.  
  
## Siehe auch  
 [SQLServerCallableStatement-Elemente](../content/SQLServerCallableStatement-Members.md)   
 [SQLServerCallableStatement-Klasse](../content/SQLServerCallableStatement-Class.md)  
  
  