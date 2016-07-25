---
title: "updateDate-Methode (int, java.sql.Date)"
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
  - SQLServerResultSet.updateDate (int, java.sql.Date)
apilocation: 
  - sqljdbc.jar
apitype: Assembly
ms.assetid: c5fb1292-a5cf-4cdd-8c4a-d1679944a6d0
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
# updateDate-Methode (int, java.sql.Date)
    
## updateDate\-Methode \(int, java.sql.Date\)  
 Aktualisiert die angegebene Spalte mit einem Wert vom Typ "date" unter Berücksichtigung des Spaltenindexes.  
  
## Syntax  
  
```  
  
public void updateDate(int index,  
                       java.sql.Date x)  
```  
  
#### Parameter  
 *index*  
  
 Ein Wert vom Typ **int** zum Angeben des Spaltenindexes.  
  
 *x*  
  
 Ein Datumswert.  
  
## Ausnahmen  
 [SQLServerException](../content/SQLServerException-Class.md)  
  
## Hinweise  
 Diese updateDate\-Methode wird von der updateDate\-Methode in der java.sql.ResultSet\-Schnittstelle angegeben.  
  
## Siehe auch  
 [updateDate-Methode &#40;ISQLServerResultSet&#41;](../content/updateDate-Method--SQLServerResultSet-.md)   
 [ISQLServerResultSet-Elemente](../content/SQLServerResultSet-Members.md)   
 [SQLServerResultSet-Klasse](../content/SQLServerResultSet-Class.md)  
  
  