---
title: "setAsciiStream-Methode (int, java.io.InputStream, long)"
ms.custom: na
ms.date: 07/01/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - drivers
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 9dfa7781-d72f-407a-a8d4-1c78c9446d09
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
# setAsciiStream-Methode (int, java.io.InputStream, long)
  Legt die angegebene Parameternummer auf das angegebene java.io.InputStream\-Objekt mit der angegebenen Anzahl von Bytes fest.  
  
## Syntax  
  
```  
  
public final void setAsciiStream(int parameterIndex,  
                                 java.io.InputStream x,  
                                    long length)  
```  
  
#### Parameter  
 *parameterIndex*  
  
 Ein Wert vom Typ **int** zum Angeben der Parameternummer.  
  
 *x*  
  
 Ein java.io.InputStream\-Objekt.  
  
 *length*  
  
 Ein **long**\-Wert zum Angeben der Anzahl von Bytes.  
  
## Ausnahmen  
 [SQLServerException](../content/SQLServerException-Class.md)  
  
## Hinweise  
 Diese setAsciiStream\-Methode wird von der setAsciiStream\-Methode in der java.sql.PreparedStatement\-Schnittstelle angegeben.  
  
 Entspricht die Länge des Datenstroms nicht der Angabe im *length*\-Parameter, wird vom JDBC\-Treiber beim Aktualisieren oder Einfügen der Zeile eine Ausnahme ausgelöst.  
  
 Ist die Länge des Datenstroms nicht bekannt, kann der *length*\-Parameter auf "\-1" festgelegt werden, um anzugeben, dass der Datenstrom unabhängig von seiner Länge akzeptiert werden soll. Bei "sqljdbc4.jar" empfiehlt sich die Verwendung der JDBC 4.0\-Methode [setAsciiStream-Methode &#40;int, java.io.InputStream&#41;](../content/setAsciiStream-Method--int--java.io.InputStream-.md), wenn von der Anwendung versucht wird, die Spalte aus einem Datenstrom mit unbekannter Länge zu aktualisieren.  
  
## Siehe auch  
 [setAsciiStream-Methode &#40;ISQLServerPreparedStatement&#41;](../content/setAsciiStream-Method--SQLServerPreparedStatement-.md)   
 [SQLServerPreparedStatement-Elemente](../content/SQLServerPreparedStatement-Members.md)  
  
  