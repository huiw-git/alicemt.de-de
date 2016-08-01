---
title: "setString-Methode (SQLServerCallableStatement)"
ms.custom: na
ms.date: 07/27/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - drivers
ms.tgt_pltfrm: na
ms.topic: article
apiname: 
  - SQLServerCallableStatement.setString
apilocation: 
  - sqljdbc.jar
apitype: Assembly
ms.assetid: f38b97b5-d4f0-4f74-a33d-740241a85842
caps.latest.revision: 13
caps.handback.revision: 13
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
# setString-Methode (SQLServerCallableStatement)
  Legt den angegebenen Parameter auf den angegebenen Java\-**String**\-Wert fest.  
  
## Syntax  
  
```  
  
public void setString(java.lang.String sCol,  
                      java.lang.String s)  
```  
  
#### Parameter  
 *sCol*  
  
 Ein **String** mit dem Namen des Parameters.  
  
 *s*  
  
 Ein Wert vom Typ **String**.  
  
## Ausnahmen  
 [SQLServerException](../content/SQLServerException-Class.md)  
  
## Hinweise  
 Diese setString\-Methode wird von der setString\-Methode in der java.sql.CallableStatement\-Schnittstelle angegeben.  
  
 Konvertierungen von Zeichenfolgen zu Binärwerten werden nur ausgeführt, wenn [!INCLUDE[jdbcNoVersion](../content/includes/jdbcNoVersion_md.md)] bekannt ist, dass der Zieltyp binär ist. Ist der zugrunde liegende Typ nicht bekannt, wird vom JDBC\-Treiber das **String**\-Literal übergeben. Kann die Konvertierung vom Server nicht ausgeführt werden, wird ein Serverfehler zurückgegeben.  
  
## Siehe auch  
 [SQLServerCallableStatement-Elemente](../content/SQLServerCallableStatement-Members.md)   
 [SQLServerCallableStatement-Klasse](../content/SQLServerCallableStatement-Class.md)  
  
  