---
title: "supportsTransactionIsolationLevel-Methode (SQLServerDatabaseMetaData)"
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
  - SQLServerDatabaseMetaData.supportsTransactionIsolationLevel
apilocation: 
  - sqljdbc.jar
apitype: Assembly
ms.assetid: b716ed6c-6ec3-47a7-8e6d-16cbf2469d6d
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
# supportsTransactionIsolationLevel-Methode (SQLServerDatabaseMetaData)
    
## supportsTransactionIsolationLevel\-Methode \(SQLServerDatabaseMetaData\)  
 Ruft ab, ob von dieser Datenbank die angegebene Transaktionsisolationsstufe unterstützt wird.  
  
## Syntax  
  
```  
  
public boolean supportsTransactionIsolationLevel(int level)  
```  
  
#### Parameter  
 *level*  
  
 Ein Wert vom Typ **int** zum Angeben der Transaktionsisolationsstufe.  
  
## Rückgabewert  
 **true**, sofern unterstützt. Andernfalls wird **false** verwendet.  
  
## Ausnahmen  
 [SQLServerException](../content/SQLServerException-Class.md)  
  
## Hinweise  
 Diese supportsTransactionIsolationLevel\-Methode wird von der supportsTransactionIsolationLevel\-Methode in der java.sql.DatabaseMetaData\-Schnittstelle angegeben.  
  
## Siehe auch  
 [SQLServerDatabaseMetaData-Methoden](../content/SQLServerDatabaseMetaData-Methods.md)   
 [SQLServerDatabaseMetaData-Elemente](../content/SQLServerDatabaseMetaData-Members.md)   
 [SQLServerDatabaseMetaData-Klasse](../content/SQLServerDatabaseMetaData-Class.md)  
  
  