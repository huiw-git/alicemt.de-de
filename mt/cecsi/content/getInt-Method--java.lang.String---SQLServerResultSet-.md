---
title: "getInt-Methode (java.lang.String) (ISQLServerResultSet)"
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
  - SQLServerResultSet.getInt (java.lang.String)
apilocation: 
  - sqljdbc.jar
apitype: Assembly
ms.assetid: 76b7054d-46dd-4d87-93a4-a7ea2ae9b7fd
caps.latest.revision: 9
caps.handback.revision: 9
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
# getInt-Methode (java.lang.String) (ISQLServerResultSet)
    
## getInt\-Methode \(java.lang.String\) \(ISQLServerResultSet\)  
 Ruft den Wert des angegebenen Spaltennamens in der aktuellen Zeile dieses [SQLServerResultSet](../content/SQLServerResultSet-Class.md)\-Objekts als Wert vom Typ **int** in der Programmiersprache Java ab.  
  
## Syntax  
  
```  
  
public int getInt(java.lang.String columnName)  
```  
  
#### Parameter  
 *columnName*  
  
 Ein **String** mit dem Spaltennamen.  
  
## Rückgabewert  
 Ein **int** \-Wert.  
  
## Ausnahmen  
 [SQLServerException](../content/SQLServerException-Class.md)  
  
## Hinweise  
 Diese getInt\-Methode wird von der getInt\-Methode in der java.sql.ResultSet\-Schnittstelle angegeben.  
  
 Die Methode wird nur für [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)]\-Datentypen unterstützt, die einen Ganzzahlwert wie "int", "smallint", "tinyint" und "bit" sicher zurückgeben. Bei Verwendung dieser Methode für andere Datentypen wird eine Ausnahme ausgelöst.  
  
## Siehe auch  
 [getInt-Methode &#40;ISQLServerResultSet&#41;](../content/getInt-Method--SQLServerResultSet-.md)   
 [ISQLServerResultSet-Elemente](../content/SQLServerResultSet-Members.md)   
 [SQLServerResultSet-Klasse](../content/SQLServerResultSet-Class.md)  
  
  