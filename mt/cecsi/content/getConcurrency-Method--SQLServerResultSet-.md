---
title: "getConcurrency-Methode (ISQLServerResultSet)"
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
  - SQLServerResultSet.getConcurrency
apilocation: 
  - sqljdbc.jar
apitype: Assembly
ms.assetid: 207e25f4-769c-4ff3-913c-3517b06208e4
caps.latest.revision: 9
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
# getConcurrency-Methode (ISQLServerResultSet)
    
## getConcurrency\-Methode \(ISQLServerResultSet\)  
 Ruft den Parallelitätsmodus dieses [SQLServerResultSet](../content/SQLServerResultSet-Class.md)\-Objekts ab.  
  
## Syntax  
  
```  
  
public int getConcurrency()  
```  
  
## Rückgabewert  
 Ein Wert vom Typ **int** zum Angeben des Parallelitätstyps. Mögliche Werte:  
  
 ResultSet.CONCUR\_READ\_ONLY  
  
 ResultSet.CONCUR\_UPDATABLE  
  
## Ausnahmen  
 [SQLServerException](../content/SQLServerException-Class.md)  
  
## Hinweise  
 Diese getConcurrency\-Methode wird von der getConcurrency\-Methode in der java.sql.ResultSet\-Schnittstelle angegeben.  
  
 Die verwendete Parallelität wird vom [SQLServerStatement](../content/SQLServerStatement-Class.md)\-Objekt bestimmt, von dem das Resultset erstellt wurde.  
  
 Diese Methode kann zur Bestimmung der eigentlichen Parallelität verwendet werden. Wurde von der Anwendung "CONCUR\_READ\_ONLY" oder "CONCUR\_UPDATABLE" ausgewählt, werden diese Elemente zurückgegeben. Wurde von der Anwendung die Standardparallelität verwendet, wird "CONCUR\_READ\_ONLY" zurückgegeben.  
  
## Siehe auch  
 [ISQLServerResultSet-Elemente](../content/SQLServerResultSet-Members.md)   
 [SQLServerResultSet-Klasse](../content/SQLServerResultSet-Class.md)  
  
  