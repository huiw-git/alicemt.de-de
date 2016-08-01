---
title: "getResultSetHoldability-Methode (SQLServerDatabaseMetaData)"
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
  - SQLServerDatabaseMetaData,getResultSetHoldability
apilocation: 
  - sqljdbc.jar
apitype: Assembly
ms.assetid: f0bd6283-83ab-4a0a-b825-ec4cdccf03e1
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
# getResultSetHoldability-Methode (SQLServerDatabaseMetaData)
  Ruft die Standardhaltbarkeit von Resultsets für diese Datenbank ab.  
  
## Syntax  
  
```  
  
public int getResultSetHoldability()  
```  
  
## Rückgabewert  
 Ein Wert vom Typ **int** zum Angeben der Standardhaltbarkeit.  
  
## Ausnahmen  
 [SQLServerException](../content/SQLServerException-Class.md)  
  
## Hinweise  
 Diese getResultSetHoldability\-Methode wird von der getResultSetHoldability\-Methode in der java.sql.DatabaseMetaData\-Schnittstelle angegeben.  
  
 Wird [!INCLUDE[jdbcNoVersion](../content/includes/jdbcNoVersion_md.md)] mit einer [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)]\-Datenbank verwendet, wird von dieser Methode der Wert "1" \(entspricht der ResultSet.HOLD\_CURSORS\_OVER\_COMMIT\-Konstanten\) zurückgegeben.  
  
## Siehe auch  
 [SQLServerDatabaseMetaData-Methoden](../content/SQLServerDatabaseMetaData-Methods.md)   
 [SQLServerDatabaseMetaData-Elemente](../content/SQLServerDatabaseMetaData-Members.md)   
 [SQLServerDatabaseMetaData-Klasse](../content/SQLServerDatabaseMetaData-Class.md)  
  
  