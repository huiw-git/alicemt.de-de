---
title: "getMaxColumnsInOrderBy-Methode (SQLServerDatabaseMetaData)"
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
  - SQLServerDatabaseMetaData.getMaxColumnsInOrderBy
apilocation: 
  - sqljdbc.jar
apitype: Assembly
ms.assetid: d6af9bb4-c55d-41f4-a266-d10ebee61194
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
# getMaxColumnsInOrderBy-Methode (SQLServerDatabaseMetaData)
    
## getMaxColumnsInOrderBy\-Methode \(SQLServerDatabaseMetaData\)  
 Ruft die maximale Anzahl von Spalten ab, die bei dieser Datenbank in einer ORDER BY\-Klausel zulässig sind.  
  
## Syntax  
  
```  
  
public int getMaxColumnsInOrderBy()  
```  
  
## Rückgabewert  
 Ein Wert vom Typ **int** zum Angeben der maximalen Anzahl der zulässigen Spalten.  
  
## Ausnahmen  
 [SQLServerException](../content/SQLServerException-Class.md)  
  
## Hinweise  
 Diese getMaxColumnsInOrderBy\-Methode wird von der getMaxColumnsInOrderBy\-Methode in der java.sql.DatabaseMetaData\-Schnittstelle angegeben.  
  
## Siehe auch  
 [SQLServerDatabaseMetaData-Methoden](../content/SQLServerDatabaseMetaData-Methods.md)   
 [SQLServerDatabaseMetaData-Elemente](../content/SQLServerDatabaseMetaData-Members.md)   
 [SQLServerDatabaseMetaData-Klasse](../content/SQLServerDatabaseMetaData-Class.md)  
  
  