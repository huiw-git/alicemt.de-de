---
title: "getCharacterStream-Methode (java.lang.String)"
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
  - SQLServerResultSet.getCharacterStream (java.lang.String)
apilocation: 
  - sqljdbc.jar
apitype: Assembly
ms.assetid: cdddc572-05c1-480d-b3e5-28270001575c
caps.latest.revision: 9
caps.handback.revision: 8
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
# getCharacterStream-Methode (java.lang.String)
    
## getCharacterStream\-Methode \(java.lang.String\)  
 Ruft den Wert des angegebenen Spaltennamens in der aktuellen Zeile dieses [SQLServerResultSet](../content/SQLServerResultSet-Class.md)\-Objekts als java.io.Reader\-Objekt ab.  
  
## Syntax  
  
```  
  
public java.io.Reader getCharacterStream(java.lang.String columnName)  
```  
  
#### Parameter  
 *columnName*  
  
 Ein **String** mit dem Spaltennamen.  
  
## Rückgabewert  
 Ein Reader\-Objekt.  
  
## Ausnahmen  
 [SQLServerException](../content/SQLServerException-Class.md)  
  
## Hinweise  
 Diese getCharacterStream\-Methode wird von der getCharacterStream\-Methode in der java.sql.ResultSet\-Schnittstelle angegeben.  
  
 Mit dieser Methode werden nur [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)]\-Unicodezeichen\-Datentypen wie "nchar", "nvarchar", "nvarchar\(max\)" und "ntext" gelesen. Alle anderen Datentypen, einschließlich der ASCII\-Zeichentypen lösen eine Ausnahme aus. Verwenden Sie zum Lesen der ASCII\-Datentypen die [getAsciiStream](../content/getAsciiStream-Method--SQLServerResultSet-.md)\-Methode.  
  
## Siehe auch  
 [getCharacterStream-Methode &#40;ISQLServerResultSet&#41;](../content/getCharacterStream-Method--SQLServerResultSet-.md)   
 [ISQLServerResultSet-Elemente](../content/SQLServerResultSet-Members.md)   
 [SQLServerResultSet-Klasse](../content/SQLServerResultSet-Class.md)  
  
  