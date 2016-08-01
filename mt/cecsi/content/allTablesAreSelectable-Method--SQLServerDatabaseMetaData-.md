---
title: "allTablesAreSelectable-Methode (SQLServerDatabaseMetaData)"
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
  - SQLServerDatabaseMetaData.allTablesAreSelectable
apilocation: 
  - sqljdbc.jar
apitype: Assembly
ms.assetid: eb340450-45a7-49c8-84bc-1b9dd5ee842f
caps.latest.revision: 9
caps.handback.revision: 9
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
# allTablesAreSelectable-Methode (SQLServerDatabaseMetaData)
    
## allTablesAreSelectable\-Methode \(SQLServerDatabaseMetaData\)  
 Ruft ab, ob der aktuelle Benutzer zum Verwenden aller Tabellen berechtigt ist, die von der [getTables](../content/getTables-Method--SQLServerDatabaseMetaData-.md)\-Methode in einer SELECT\-Anweisung zurückgegeben werden.  
  
## Syntax  
  
```  
  
public boolean allTablesAreSelectable()  
```  
  
## Rückgabewert  
 **true**, wenn der Benutzer über Berechtigungen zum Aufrufen aller Tabellen verfügt. Andernfalls wird **false** verwendet.  
  
## Ausnahmen  
 [SQLServerException](../content/SQLServerException-Class.md)  
  
## Hinweise  
 Diese allTablesAreSelectable\-Methode wird von der allTablesAreSelectable\-Methode in der java.sql.DatabaseMetaData\-Schnittstelle angegeben.  
  
## Siehe auch  
 [SQLServerDatabaseMetaData-Methoden](../content/SQLServerDatabaseMetaData-Methods.md)   
 [SQLServerDatabaseMetaData-Elemente](../content/SQLServerDatabaseMetaData-Members.md)   
 [SQLServerDatabaseMetaData-Klasse](../content/SQLServerDatabaseMetaData-Class.md)  
  
  