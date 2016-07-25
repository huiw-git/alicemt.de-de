---
title: "updateObject-Methode (java.lang.String, java.lang.Object, int)"
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
  - SQLServerResultSet.updateObject (java.lang.String, java.lang.Object, int)
apilocation: 
  - sqljdbc.jar
apitype: Assembly
ms.assetid: 27283ce1-637e-4e2c-91ee-8ad379114ac5
caps.latest.revision: 15
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
# updateObject-Methode (java.lang.String, java.lang.Object, int)
    
## updateObject\-Methode \(java.lang.String, java.lang.Object, int\)  
 Aktualisiert die angegebene Spalte mit einem Wert vom Typ **Object** unter Verwendung des angegebenen Spaltennamens und der Dezimalstellen.  
  
## Syntax  
  
```  
  
public void updateObject(java.lang.String columnName,  
                         java.lang.Object x,  
                         int scale)  
```  
  
#### Parameter  
 *columnName*  
  
 Ein **String** mit dem Spaltennamen.  
  
 *obj*  
  
 Ein **Object** \-Wert.  
  
 *scale*  
  
 Gilt für java.sql.Types.DECIMAL\- oder java.sql.Types.NUMERIC\-Typen. Dieser Wert gibt die Anzahl der Dezimalstellen an. Bei allen anderen Typen wird dieser Wert ignoriert.  
  
## Ausnahmen  
 [SQLServerException](../content/SQLServerException-Class.md)  
  
## Hinweise  
 Diese updateObject\-Methode wird von der updateObject\-Methode in der java.sql.ResultSet\-Schnittstelle angegeben.  
  
## Siehe auch  
 [updateObject-Methode &#40;SQLServerResultSet&#41;](../content/updateObject-Method--SQLServerResultSet-.md)   
 [ISQLServerResultSet-Elemente](../content/SQLServerResultSet-Members.md)   
 [SQLServerResultSet-Klasse](../content/SQLServerResultSet-Class.md)  
  
  