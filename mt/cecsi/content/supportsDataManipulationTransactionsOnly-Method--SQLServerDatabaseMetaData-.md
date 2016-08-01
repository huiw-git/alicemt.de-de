---
title: "supportsDataManipulationTransactionsOnly-Methode (SQLServerDatabaseMetaData)"
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
  - SQLServerDatabaseMetaData.supportsDataManipulationTransactionsOnly
apilocation: 
  - sqljdbc.jar
apitype: Assembly
ms.assetid: bdc182db-4518-4bf2-b63a-05f58fdb4eb8
caps.latest.revision: 6
caps.handback.revision: 6
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
# supportsDataManipulationTransactionsOnly-Methode (SQLServerDatabaseMetaData)
    
## supportsDataManipulationTransactionsOnly\-Methode \(SQLServerDatabaseMetaData\)  
 Ruft ab, ob von dieser Datenbank in einer Transaktion nur Datenbearbeitungsanweisungen unterstützt werden.  
  
## Syntax  
  
```  
  
public boolean supportsDataManipulationTransactionsOnly()  
```  
  
## Rückgabewert  
 **true**, sofern unterstützt. Andernfalls wird **false** verwendet.  
  
## Ausnahmen  
 [SQLServerException](../content/SQLServerException-Class.md)  
  
## Hinweise  
 Diese supportsDataManipulationTransactionsOnly\-Methode wird von der supportsDataManipulationTransactionsOnly\-Methode in der java.sql.DatabaseMetaData\-Schnittstelle angegeben.  
  
## Siehe auch  
 [SQLServerDatabaseMetaData-Methoden](../content/SQLServerDatabaseMetaData-Methods.md)   
 [SQLServerDatabaseMetaData-Elemente](../content/SQLServerDatabaseMetaData-Members.md)   
 [SQLServerDatabaseMetaData-Klasse](../content/SQLServerDatabaseMetaData-Class.md)  
  
  