---
title: "getDefaultTransactionIsolation-Methode (SQLServerDatabaseMetaData)"
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
  - SQLServerDatabaseMetaData.getDefaultTransactionIsolation
apilocation: 
  - sqljdbc.jar
apitype: Assembly
ms.assetid: 85b867ed-de5a-4879-b3f8-bce897879077
caps.latest.revision: 11
caps.handback.revision: 10
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
# getDefaultTransactionIsolation-Methode (SQLServerDatabaseMetaData)
  Ruft die standardmäßige Transaktionsisolationsstufe für diese Datenbank ab.  
  
## Syntax  
  
```  
  
public int getDefaultTransactionIsolation()  
```  
  
## Rückgabewert  
 Ein Wert vom Typ **int** zum Angeben der standardmäßigen Transaktionsisolationsstufe.  
  
## Ausnahmen  
 [SQLServerException](../content/SQLServerException-Class.md)  
  
## Hinweise  
 Diese getDefaultTransactionIsolation\-Methode wird von der getDefaultTransactionIsolation\-Methode in der java.sql.DatabaseMetaData\-Schnittstelle angegeben.  
  
 Bei Verwendung von [!INCLUDE[jdbcNoVersion](../content/includes/jdbcNoVersion_md.md)] mit einer [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)]\-Datenbank wird von dieser Methode entweder der Wert "TRANSACTION\_READ\_COMMITTED" oder der Wert "2" vom Typ **int** zurückgegeben.  
  
## Siehe auch  
 [SQLServerDatabaseMetaData-Methoden](../content/SQLServerDatabaseMetaData-Methods.md)   
 [SQLServerDatabaseMetaData-Elemente](../content/SQLServerDatabaseMetaData-Members.md)   
 [SQLServerDatabaseMetaData-Klasse](../content/SQLServerDatabaseMetaData-Class.md)  
  
  