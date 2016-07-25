---
title: "dataDefinitionIgnoredInTransactions-Methode (SQLServerDatabaseMetaData)"
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
  - SQLServerDatabaseMetaData.dataDefinitionIgnoredInTransactions
apilocation: 
  - sqljdbc.jar
apitype: Assembly
ms.assetid: 1674fb46-43a7-46d0-9f05-cf993d3bc032
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
# dataDefinitionIgnoredInTransactions-Methode (SQLServerDatabaseMetaData)
    
## dataDefinitionIgnoredInTransactions\-Methode \(SQLServerDatabaseMetaData\)  
 Ruft ab, ob von dieser Datenbank eine Datendefinitionsanweisung innerhalb einer Transaktion ignoriert wird.  
  
## Syntax  
  
```  
  
public boolean dataDefinitionIgnoredInTransactions()  
```  
  
## Rückgabewert  
 **true**, falls DDL\-Anweisungen innerhalb von Transaktionen ignoriert werden. Andernfalls wird **false** verwendet.  
  
## Ausnahmen  
 [SQLServerException](../content/SQLServerException-Class.md)  
  
## Hinweise  
 Diese dataDefinitionIgnoredInTransactions\-Methode wird von der dataDefinitionIgnoredInTransactions\-Methode in der java.sql.DatabaseMetaData\-Schnittstelle angegeben.  
  
## Siehe auch  
 [SQLServerDatabaseMetaData-Methoden](../content/SQLServerDatabaseMetaData-Methods.md)   
 [SQLServerDatabaseMetaData-Elemente](../content/SQLServerDatabaseMetaData-Members.md)   
 [SQLServerDatabaseMetaData-Klasse](../content/SQLServerDatabaseMetaData-Class.md)  
  
  