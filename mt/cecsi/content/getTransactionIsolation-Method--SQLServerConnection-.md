---
title: "getTransactionIsolation-Methode (ISQLServerConnection)"
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
  - SQLServerConnection.getTransactionIsolation
apilocation: 
  - sqljdbc.jar
apitype: Assembly
ms.assetid: 179772e9-6572-4ce5-83c5-ab2b196cee67
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
# getTransactionIsolation-Methode (ISQLServerConnection)
    
## getTransactionIsolation\-Methode \(ISQLServerConnection\)  
 Ruft die aktuelle Transaktionsisolationsstufe dieses [SQLServerConnection](../content/SQLServerConnection-Class.md)\-Objekt ab.  
  
## Syntax  
  
```  
  
public int getTransactionIsolation()  
```  
  
## Rückgabewert  
 Ein Wert vom Typ **int** mit einer der folgenden Isolationsstufen:  
  
 TRANSACTION\_NONE  
  
 TRANSACTION\_READ\_UNCOMMITTED  
  
 TRANSACTION\_READ\_COMMITTED  
  
 TRANSACTION\_REPEATABLE\_READ  
  
 TRANSACTION\_SERIALIZABLE  
  
 TRANSACTION\_SNAPSHOT \= 0x1000  
  
## Ausnahmen  
 [SQLServerException](../content/SQLServerException-Class.md)  
  
## Hinweise  
 Diese getTransactionIsolation\-Methode wird von der getTransactionIsolation\-Methode in der java.sql.Connection\-Schnittstelle angegeben.  
  
## Siehe auch  
 [SQLServerConnection-Elemente](../content/SQLServerConnection-Members.md)   
 [SQLServerConnection-Klasse](../content/SQLServerConnection-Class.md)  
  
  