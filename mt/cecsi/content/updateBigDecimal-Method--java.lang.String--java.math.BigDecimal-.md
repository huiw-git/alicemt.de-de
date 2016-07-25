---
title: "updateBigDecimal-Methode (java.lang.String, java.math.BigDecimal)"
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
  - SQLServerResultSet.updateBigDecimal (java.lang.String, java.math.BigDecimal)
apilocation: 
  - sqljdbc.jar
apitype: Assembly
ms.assetid: b844cd9d-3d2d-4385-ab01-ecc89692054f
caps.latest.revision: 8
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
# updateBigDecimal-Methode (java.lang.String, java.math.BigDecimal)
    
## updateBigDecimal\-Methode \(java.lang.String, java.math.BigDecimal\)  
 Aktualisiert die angegebene Spalte mit einem BigDecimal\-Objekt unter Verwendung des angegebenen Spaltennamens.  
  
## Syntax  
  
```  
  
public void updateBigDecimal(java.lang.String columnName,  
                             java.math.BigDecimal x)  
```  
  
#### Parameter  
 *columnName*  
  
 Ein **String** mit dem Spaltennamen.  
  
 *x*  
  
 Ein BigDecimal\-Objekt.  
  
## Ausnahmen  
 [SQLServerException](../content/SQLServerException-Class.md)  
  
## Hinweise  
 Diese updateBigDecimal\-Methode wird von der updateBigDecimal\-Methode in der java.sql.ResultSet\-Schnittstelle angegeben.  
  
## Siehe auch  
 [updateBigDecimal-Methode &#40;ISQLServerResultSet&#41;](../content/updateBigDecimal-Method--SQLServerResultSet-.md)   
 [ISQLServerResultSet-Elemente](../content/SQLServerResultSet-Members.md)   
 [SQLServerResultSet-Klasse](../content/SQLServerResultSet-Class.md)  
  
  