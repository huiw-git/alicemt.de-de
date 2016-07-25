---
title: "supportsDataDefinitionAndDataManipulationTransactions-Methode (SQLServerDatabaseMetaData)"
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
  - SQLServerDatabaseMetaData.supportsDataDefinitionAndDataManipulationTransactions
apilocation: 
  - sqljdbc.jar
apitype: Assembly
ms.assetid: fe91c601-9bb3-4364-9131-575a94d3a1b3
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
# supportsDataDefinitionAndDataManipulationTransactions-Methode (SQLServerDatabaseMetaData)
    
## supportsDataDefinitionAndDataManipulationTransactions\-Methode \(SQLServerDatabaseMetaData\)  
 Ruft ab, ob von dieser Datenbank in einer Transaktion sowohl Datendefinitions\- als auch Datenbearbeitungsanweisungen unterstützt werden.  
  
## Syntax  
  
```  
  
public boolean supportsDataDefinitionAndDataManipulationTransactions()  
```  
  
## Rückgabewert  
 **true**, sofern unterstützt. Andernfalls wird **false** verwendet.  
  
## Ausnahmen  
 [SQLServerException](../content/SQLServerException-Class.md)  
  
## Hinweise  
 Diese suportsDataDefinitionAndDataManipulationTransactions\-Methode wird von der suportsDataDefinitionAndDataManipulationTransactions\-Methode in der java.sql.DatabaseMetaData\-Schnittstelle angegeben.  
  
## Siehe auch  
 [SQLServerDatabaseMetaData-Methoden](../content/SQLServerDatabaseMetaData-Methods.md)   
 [SQLServerDatabaseMetaData-Elemente](../content/SQLServerDatabaseMetaData-Members.md)   
 [SQLServerDatabaseMetaData-Klasse](../content/SQLServerDatabaseMetaData-Class.md)  
  
  