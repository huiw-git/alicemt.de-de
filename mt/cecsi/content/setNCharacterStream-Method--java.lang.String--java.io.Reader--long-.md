---
title: "setNCharacterStream-Methode (java.lang.String, java.io.Reader, long)"
ms.custom: na
ms.date: 07/01/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - drivers
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: af9a1ba8-7980-43fa-88e5-14f6cc5e897c
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
# setNCharacterStream-Methode (java.lang.String, java.io.Reader, long)
  Legt den angegebenen Parameter auf das angegebene Reader\-Objekt fest, dessen Länge der angegebenen Zeichenanzahl entspricht.  
  
## Syntax  
  
```  
  
public final void setNCharacterStream(java.lang.String parameterName,  
                     java.io.Reader value,  
                     long length)  
```  
  
#### Parameter  
 *parameterName*  
  
 Ein **String** zum Angeben des Parameternamens.  
  
 *value*  
  
 Ein Reader\-Objekt.  
  
 *length*  
  
 Ein **long**\-Wert zum Angeben der Anzahl von Zeichen im Datenstrom.  
  
## Ausnahmen  
 [SQLServerException](../content/SQLServerException-Class.md)  
  
## Hinweise  
 Diese setNCharacterStream\-Methode wird von der setNCharacterStream\-Methode in der java.sql.CallableStatement\-Schnittstelle angegeben.  
  
 Diese Methode sollte für die Datentypen **NCHAR**, **NVARCHAR**, **NTEXT** und **XML** verwendet werden.  
  
 Entspricht die Länge des Datenstroms nicht der Angabe im *length*\-Parameter, wird vom JDBC\-Treiber beim Aktualisieren oder Einfügen der Zeile eine Ausnahme ausgelöst.  
  
 Ist die Länge des Datenstroms nicht bekannt, kann der *length*\-Parameter auf "\-1" festgelegt werden, um anzugeben, dass der Datenstrom unabhängig von seiner Länge akzeptiert werden soll. Bei "sqljdbc4.jar" empfiehlt sich die Verwendung der JDBC 4.0\-Methode [setNCharacterStream-Methode &#40;java.lang.String, java.io.Reader&#41;](../content/setNCharacterStream-Method--java.lang.String--java.io.Reader-.md), wenn von der Anwendung versucht wird, die Spalte aus einem Datenstrom mit unbekannter Länge zu aktualisieren.  
  
## Siehe auch  
 [setNCharacterStream-Methode &#40;SQLServerCallableStatement&#41;](../content/setNCharacterStream-Method--SQLServerCallableStatement-.md)   
 [SQLServerCallableStatement-Elemente](../content/SQLServerCallableStatement-Members.md)  
  
  