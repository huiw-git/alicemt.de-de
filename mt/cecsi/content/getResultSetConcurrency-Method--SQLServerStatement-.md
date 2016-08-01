---
title: "getResultSetConcurrency-Methode (ISQLServerStatement)"
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
  - SQLServerStatement.getResultSetConcurrency
apilocation: 
  - sqljdbc.jar
apitype: Assembly
ms.assetid: 47ef6547-5ec7-4cf5-a4d4-e34cbeec72eb
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
# getResultSetConcurrency-Methode (ISQLServerStatement)
    
## getResultSetConcurrency\-Methode \(ISQLServerStatement\)  
 Ruft die Resultsetparallelität für [SQLServerResultSet](../content/SQLServerResultSet-Class.md)\-Objekte ab, die von diesem [SQLServerStatement](../content/SQLServerStatement-Class.md)\-Objekt generiert werden.  
  
## Syntax  
  
```  
  
public final int getResultSetConcurrency()  
```  
  
## Rückgabewert  
 Ein Wert vom Typ **int** zur Angabe des Paralellitätstyps des Resultsets.  
  
## Ausnahmen  
 [SQLServerException](../content/SQLServerException-Class.md)  
  
## Hinweise  
 Diese getResultSetConcurrency\-Methode wird von der getResultSetConcurrency\-Methode in der java.sql.Statement\-Schnittstelle angegeben.  
  
## Siehe auch  
 [SQLServerStatement-Elemente](../content/SQLServerStatement-Members.md)   
 [SQLServerStatement-Klasse](../content/SQLServerStatement-Class.md)  
  
  