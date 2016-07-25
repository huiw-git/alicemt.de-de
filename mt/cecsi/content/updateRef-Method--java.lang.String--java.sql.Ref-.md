---
title: "updateRef-Methode (java.lang.String, java.sql.Ref)"
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
  - SQLServerResultSet.updateRef (java.lang.String, java.sql.Ref)
apilocation: 
  - sqljdbc.jar
apitype: Assembly
ms.assetid: 7740d17d-282f-4f1d-91f9-c68a873b069a
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
# updateRef-Methode (java.lang.String, java.sql.Ref)
    
## updateRef\-Methode \(java.lang.String, java.sql.Ref\)  
 Aktualisiert die angegebene Spalte unter Berücksichtigung des Spaltennamens mit einem java.sql.Ref\-Wert.  
  
## Syntax  
  
```  
  
public void updateRef(java.lang.String columnName,  
                      java.sql.Ref x)  
```  
  
#### Parameter  
 *columnName*  
  
 Ein **String** mit dem Spaltennamen.  
  
 *x*  
  
 Ein Ref\-Objekt.  
  
## Ausnahmen  
 [SQLServerException](../content/SQLServerException-Class.md)  
  
## Hinweise  
 Diese updateRef\-Methode wird von der updateRef\-Methode in der java.sql.ResultSet\-Schnittstelle angegeben.  
  
## Siehe auch  
 [updateRef-Methode &#40;ISQLServerResultSet&#41;](../content/updateRef-Method--SQLServerResultSet-.md)   
 [ISQLServerResultSet-Elemente](../content/SQLServerResultSet-Members.md)   
 [SQLServerResultSet-Klasse](../content/SQLServerResultSet-Class.md)  
  
  