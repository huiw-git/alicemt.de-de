---
title: "updateTimestamp-Methode (int, java.sql.Timestamp)"
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
  - SQLServerResultSet.updateTimestamp (int, java.sql.Timestamp)
apilocation: 
  - sqljdbc.jar
apitype: Assembly
ms.assetid: db83d9d7-137b-4a28-a2ca-d4782e0a256e
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
# updateTimestamp-Methode (int, java.sql.Timestamp)
    
## updateTimestamp\-Methode \(int, java.sql.Timestamp\)  
 Aktualisiert die angegebene Spalte unter Berücksichtigung des Spaltenindexes mit einem Zeitstempelwert.  
  
## Syntax  
  
```  
  
public void updateTimestamp(int index,  
                            java.sql.Timestamp x)  
```  
  
#### Parameter  
 *index*  
  
 Ein Wert vom Typ **int** zum Angeben des Spaltenindexes.  
  
 *x*  
  
 Ein Zeitstempelwert.  
  
## Ausnahmen  
 [SQLServerException](../content/SQLServerException-Class.md)  
  
## Hinweise  
 Diese updateTimestamp\-Methode wird von der updateTimestamp\-Methode in der java.sql.ResultSet\-Schnittstelle angegeben.  
  
## Siehe auch  
 [updateTimestamp-Methode &#40;ISQLServerResultSet&#41;](../content/updateTimestamp-Method--SQLServerResultSet-.md)   
 [ISQLServerResultSet-Elemente](../content/SQLServerResultSet-Members.md)   
 [SQLServerResultSet-Klasse](../content/SQLServerResultSet-Class.md)  
  
  