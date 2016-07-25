---
title: "updateClob-Methode (java.lang.String, java.sql.Clob)"
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
  - SQLServerResultSet.updateClob (java.lang.String, java.sql.Clob)
apilocation: 
  - sqljdbc.jar
apitype: Assembly
ms.assetid: 5da64915-1c13-44fd-90c0-52168889bae0
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
# updateClob-Methode (java.lang.String, java.sql.Clob)
    
## updateClob\-Methode \(java.lang.String, java.sql.Clob\)  
 Aktualisiert die angegebene Spalte unter Berücksichtigung des Spaltennamens mit einem java.sql.Clob\-Wert.  
  
## Syntax  
  
```  
  
public void updateClob(java.lang.String columnName,  
                       java.sql.Clob clobValue)  
```  
  
#### Parameter  
 *columnName*  
  
 Ein **String** mit dem Spaltennamen.  
  
 *clobValue*  
  
 Ein Clob\-Objekt.  
  
## Ausnahmen  
 [SQLServerException](../content/SQLServerException-Class.md)  
  
## Hinweise  
 Diese updateClob\-Methode wird von der updateClob\-Methode in der java.sql.ResultSet\-Schnittstelle angegeben.  
  
## Siehe auch  
 [updateClob-Methode &#40;ISQLServerResultSet&#41;](../content/updateClob-Method--SQLServerResultSet-.md)   
 [ISQLServerResultSet-Elemente](../content/SQLServerResultSet-Members.md)   
 [SQLServerResultSet-Klasse](../content/SQLServerResultSet-Class.md)  
  
  