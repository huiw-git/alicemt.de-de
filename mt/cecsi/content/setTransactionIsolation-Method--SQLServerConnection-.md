---
title: "setTransactionIsolation-Methode (ISQLServerConnection)"
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
  - SQLServerConnection.setTransactionIsolation
apilocation: 
  - sqljdbc.jar
apitype: Assembly
ms.assetid: 6a8fa4d3-5237-40f8-8a02-b40a3d7a1131
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
# setTransactionIsolation-Methode (ISQLServerConnection)
    
## setTransactionIsolation\-Methode \(ISQLServerConnection\)  
 Ändert die Transaktionsisolationsstufe für dieses [SQLServerConnection](../content/SQLServerConnection-Class.md)\-Objekt zur angegebenen Stufe.  
  
## Syntax  
  
```  
  
public void setTransactionIsolation(int level)  
```  
  
#### Parameter  
 *level*  
  
 Ein Wert vom Typ **int** mit einer der folgenden Isolationsstufen:  
  
 TRANSACTION\_READ\_UNCOMMITTED  
  
 TRANSACTION\_READ\_COMMITTED  
  
 TRANSACTION\_REPEATABLE\_READ  
  
 TRANSACTION\_SERIALIZABLE  
  
 TRANSACTION\_SNAPSHOT \= 0x1000  
  
## Ausnahmen  
 [SQLServerException](../content/SQLServerException-Class.md)  
  
## Hinweise  
 Diese setTransactionIsolation\-Methode wird von der setTransactionIsolation\-Methode in der java.sql.Connection\-Schnittstelle angegeben.  
  
 Für Transaktionen wird kein Commit ausgeführt, wenn diese Methode während einer Transaktion aufgerufen wird.  
  
## Siehe auch  
 [SQLServerConnection-Elemente](../content/SQLServerConnection-Members.md)   
 [SQLServerConnection-Klasse](../content/SQLServerConnection-Class.md)  
  
  