---
title: "autoCommitFailureClosesAllResultSets-Methode (SQLServerDatabaseMetaData)"
ms.custom: na
ms.date: 07/01/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - drivers
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 1739ecb5-e5cb-4807-b5a8-97c0299929d0
caps.latest.revision: 14
caps.handback.revision: 13
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
# autoCommitFailureClosesAllResultSets-Methode (SQLServerDatabaseMetaData)
  Gibt an, ob vom JDBC\-Treiber alle geöffneten Resultsets \(einschließlich Resultsets mit Haltbarkeit\) geschlossen werden, wenn ein automatischer Commit aktiviert und eine Ausnahme ausgelöst wird.  
  
## Syntax  
  
```  
  
public boolean autoCommitFailureClosesAllResultSets()  
```  
  
## Rückgabewert  
 **true**, wenn alle geöffneten Resultsets \(einschließlich Resultsets mit Holdability\) geschlossen werden, sobald ein automatischer Commit aktiviert und eine Ausnahme ausgelöst wird. Andernfalls wird **false** verwendet.  
  
## Ausnahmen  
 [SQLServerException](../content/SQLServerException-Class.md)  
  
## Hinweise  
 Diese autoCommitFailureClosesAllResultSets\-Methode wird von der autoCommitFailureClosesAllResultSets\-Methode in der java.sql.DatabaseMetaData\-Schnittstelle angegeben.  
  
## Siehe auch  
 [SQLServerDatabaseMetaData-Methoden](../content/SQLServerDatabaseMetaData-Methods.md)   
 [SQLServerDatabaseMetaData-Elemente](../content/SQLServerDatabaseMetaData-Members.md)   
 [SQLServerDatabaseMetaData-Klasse](../content/SQLServerDatabaseMetaData-Class.md)  
  
  