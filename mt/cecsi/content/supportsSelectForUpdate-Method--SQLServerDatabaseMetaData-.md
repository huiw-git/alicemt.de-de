---
title: "supportsSelectForUpdate-Methode (SQLServerDatabaseMetaData)"
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
  - SQLServerDatabaseMetaData.supportsSelectForUpdate
apilocation: 
  - sqljdbc.jar
apitype: Assembly
ms.assetid: 721bc8e3-36c0-4fa6-8561-4f8d54c8265a
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
# supportsSelectForUpdate-Methode (SQLServerDatabaseMetaData)
    
## supportsSelectForUpdate\-Methode \(SQLServerDatabaseMetaData\)  
 Ruft ab, ob positionierte SELECT FOR UPDATE\-Anweisungen von dieser Datenbank unterstützt werden.  
  
## Syntax  
  
```  
  
public boolean supportsSelectForUpdate()  
```  
  
## Rückgabewert  
 **true**, sofern unterstützt. Andernfalls wird **false** verwendet.  
  
## Ausnahmen  
 [SQLServerException](../content/SQLServerException-Class.md)  
  
## Hinweise  
 Diese supportsSelectForUpdate\-Methode wird von der supportsSelectForUpdate\-Methode in der java.sql.DatabaseMetaData\-Schnittstelle angegeben.  
  
## Siehe auch  
 [SQLServerDatabaseMetaData-Methoden](../content/SQLServerDatabaseMetaData-Methods.md)   
 [SQLServerDatabaseMetaData-Elemente](../content/SQLServerDatabaseMetaData-Members.md)   
 [SQLServerDatabaseMetaData-Klasse](../content/SQLServerDatabaseMetaData-Class.md)  
  
  