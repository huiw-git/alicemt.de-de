---
title: "getMaxColumnsInGroupBy-Methode (SQLServerDatabaseMetaData)"
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
  - SQLServerDatabaseMetaData.getMaxColumnsInGroupBy
apilocation: 
  - sqljdbc.jar
apitype: Assembly
ms.assetid: a59cfe98-c0f4-46ad-9243-62aa56855f1a
caps.latest.revision: 7
caps.handback.revision: 7
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
# getMaxColumnsInGroupBy-Methode (SQLServerDatabaseMetaData)
    
## getMaxColumnsInGroupBy\-Methode \(SQLServerDatabaseMetaData\)  
 Ruft die maximale Anzahl von Spalten ab, die bei dieser Datenbank in einer GROUP BY\-Klausel zulässig sind.  
  
## Syntax  
  
```  
  
public int getMaxColumnsInGroupBy()  
```  
  
## Rückgabewert  
 Ein Wert vom Typ **int** zum Angeben der maximalen Anzahl der zulässigen Spalten.  
  
## Ausnahmen  
 [SQLServerException](../content/SQLServerException-Class.md)  
  
## Hinweise  
 Diese getMaxColumnsInGroupBy\-Methode wird von der getMaxColumnsInGroupBy\-Methode in der java.sql.DatabaseMetaData\-Schnittstelle angegeben.  
  
## Siehe auch  
 [SQLServerDatabaseMetaData-Methoden](../content/SQLServerDatabaseMetaData-Methods.md)   
 [SQLServerDatabaseMetaData-Elemente](../content/SQLServerDatabaseMetaData-Members.md)   
 [SQLServerDatabaseMetaData-Klasse](../content/SQLServerDatabaseMetaData-Class.md)  
  
  