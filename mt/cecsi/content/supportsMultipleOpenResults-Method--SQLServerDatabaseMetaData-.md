---
title: "supportsMultipleOpenResults-Methode (SQLServerDatabaseMetaData)"
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
  - SQLServerDatabaseMetaData.supportsMultipleOpenResults
apilocation: 
  - sqljdbc.jar
apitype: Assembly
ms.assetid: 9480d280-5e3d-46ae-80e6-1bba3ac5a641
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
# supportsMultipleOpenResults-Methode (SQLServerDatabaseMetaData)
    
## supportsMultipleOpenResults\-Methode \(SQLServerDatabaseMetaData\)  
 Ruft ab, ob von einem [SQLServerCallableStatement](../content/SQLServerCallableStatement-Class.md)\-Objekt gleichzeitig mehrere [SQLServerResultSet](../content/SQLServerResultSet-Class.md)\-Objekte zurückgegeben werden können.  
  
## Syntax  
  
```  
  
public boolean supportsMultipleOpenResults()  
```  
  
## Rückgabewert  
 **true**, sofern unterstützt. Andernfalls wird **false** verwendet.  
  
## Ausnahmen  
 [SQLServerException](../content/SQLServerException-Class.md)  
  
## Hinweise  
 Diese supportsMultipleOpenResults\-Methode wird von der supportsMultipleOpenResults\-Methode in der java.sql.DatabaseMetaData\-Schnittstelle angegeben.  
  
## Siehe auch  
 [SQLServerDatabaseMetaData-Methoden](../content/SQLServerDatabaseMetaData-Methods.md)   
 [SQLServerDatabaseMetaData-Elemente](../content/SQLServerDatabaseMetaData-Members.md)   
 [SQLServerDatabaseMetaData-Klasse](../content/SQLServerDatabaseMetaData-Class.md)  
  
  