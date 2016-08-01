---
title: "dataDefinitionCausesTransactionCommit-Methode (SQLServerDatabaseMetaData)"
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
  - SQLServerDatabaseMetaData.dataDefinitionCausesTransactionCommit
apilocation: 
  - sqljdbc.jar
apitype: Assembly
ms.assetid: bf04fa73-b9f1-4403-b6a0-e53d0d27c671
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
# dataDefinitionCausesTransactionCommit-Methode (SQLServerDatabaseMetaData)
    
## dataDefinitionCausesTransactionCommit\-Methode \(SQLServerDatabaseMetaData\)  
 Ruft ab, ob durch eine Datendefinitionsanweisung innerhalb einer Transaktion ein Commit der Transaktion erzwungen wird.  
  
## Syntax  
  
```  
  
public boolean dataDefinitionCausesTransactionCommit()  
```  
  
## Rückgabewert  
 **true**, wenn von der DDL\-Anweisung ein Commit erzwungen wird. Andernfalls wird **false** verwendet.  
  
## Ausnahmen  
 [SQLServerException](../content/SQLServerException-Class.md)  
  
## Hinweise  
 Diese dataDefinitionCausesTransactionCommit\-Methode wird von der dataDefinitionCausesTransactionCommit\-Methode in der java.sql.DatabaseMetaData\-Schnittstelle angegeben.  
  
## Siehe auch  
 [SQLServerDatabaseMetaData-Methoden](../content/SQLServerDatabaseMetaData-Methods.md)   
 [SQLServerDatabaseMetaData-Elemente](../content/SQLServerDatabaseMetaData-Members.md)   
 [SQLServerDatabaseMetaData-Klasse](../content/SQLServerDatabaseMetaData-Class.md)  
  
  