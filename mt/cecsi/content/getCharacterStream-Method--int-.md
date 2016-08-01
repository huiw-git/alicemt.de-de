---
title: "getCharacterStream-Methode (int)"
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
  - SQLServerResultSet.getCharacterStream (int)
apilocation: 
  - sqljdbc.jar
apitype: Assembly
ms.assetid: 4f9f230d-be4c-469a-b3dc-f24531429aae
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
# getCharacterStream-Methode (int)
    
## getCharacterStream\-Methode \(int\)  
 Ruft den Wert des angegebenen Spaltenindexes in der aktuellen Zeile dieses [SQLServerResultSet](../content/SQLServerResultSet-Class.md)\-Objekts als java.io.Reader\-Objekt ab.  
  
## Syntax  
  
```  
  
public java.io.Reader getCharacterStream(int columnIndex)  
```  
  
#### Parameter  
 *columnIndex*  
  
 Ein Wert vom Typ **int** zum Angeben des Spaltenindexes.  
  
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
  
  