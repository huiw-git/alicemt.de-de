---
title: "getUnicodeStream-Methode (java.lang.String)"
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
  - SQLServerResultSet.getUnicodeStream (java.lang.String)
apilocation: 
  - sqljdbc.jar
apitype: Assembly
ms.assetid: e8ea50a3-804a-4752-96e5-eb3d521f93c1
caps.latest.revision: 10
caps.handback.revision: 10
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
# getUnicodeStream-Methode (java.lang.String)
    
## getUnicodeStream\-Methode \(java.lang.String\)  
 Ruft den Wert des angegebenen Spaltennamens in der aktuellen Zeile dieses [SQLServerResultSet](../content/SQLServerResultSet-Class.md)\-Objekts als Unicode\-Zeichendatenstrom ab.  
  
> [!NOTE]  
>  Diese Methode wurde in der JDBC\-Spezifikation als veraltet angegeben. Bei Aufruf der Methode wird eine Ausnahme vom Typ "Nicht implementiert" ausgelöst. Verwenden Sie stattdessen die [getCharacterStream](../content/getCharacterStream-Method--SQLServerResultSet-.md)\-Methode.  
  
## Syntax  
  
```  
  
public java.io.InputStream getUnicodeStream(java.lang.String columnName)  
```  
  
#### Parameter  
 *columnName*  
  
 Ein **String** mit dem Spaltennamen.  
  
## Rückgabewert  
 Ein InputStream\-Objekt.  
  
## Ausnahmen  
 [SQLServerException](../content/SQLServerException-Class.md)  
  
## Hinweise  
 Diese getUnicodeString\-Methode wird von der getUnicodeString\-Methode in der java.sql.ResultSet\-Schnittstelle angegeben.  
  
## Siehe auch  
 [getUnicodeStream-Methode &#40;ISQLServerResultSet&#41;](../content/getUnicodeStream-Method--SQLServerResultSet-.md)   
 [ISQLServerResultSet-Elemente](../content/SQLServerResultSet-Members.md)   
 [SQLServerResultSet-Klasse](../content/SQLServerResultSet-Class.md)  
  
  