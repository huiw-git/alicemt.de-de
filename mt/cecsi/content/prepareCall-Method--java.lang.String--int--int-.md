---
title: "prepareCall-Methode (java.lang.String, int, int)"
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
  - SQLServerConnection.prepareCall (java.lang.String, int, int)
apilocation: 
  - sqljdbc.jar
apitype: Assembly
ms.assetid: 04d36a25-7f95-4675-9690-4462671b3d67
caps.latest.revision: 9
caps.handback.revision: 9
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
# prepareCall-Methode (java.lang.String, int, int)
    
## prepareCall\-Methode \(java.lang.String, int, int\)  
 Erstellt ein [SQLServerCallableStatement](../content/SQLServerCallableStatement-Class.md)\-Objekt, mit dem [SQLServerResultSet](../content/SQLServerResultSet-Class.md)\-Objekte mit dem angegebenen Typ und der Parallelität generiert werden.  
  
## Syntax  
  
```  
  
public java.sql.CallableStatement prepareCall(java.lang.String sql,  
                                              int resultSetType,  
                                              int resultSetConcurrency)  
```  
  
#### Parameter  
 *sql*  
  
 Ein **String** mit einer SQL\-Anweisung.  
  
 *resultSetType*  
  
 Ein Wert vom Typ **int**  zur Angabe des Resultsettyps.  
  
 *resultSetConcurrency*  
  
 Ein Wert vom Typ **int**  zur Angabe des Paralellitätstyps des Resultsets.  
  
## Rückgabewert  
 Ein CallableStatement\-Objekt.  
  
## Ausnahmen  
 [SQLServerException](../content/SQLServerException-Class.md)  
  
## Hinweise  
 Diese prepareCall\-Methode wird von der prepareCall\-Methode in der java.sql.Connection\-Schnittstelle angegeben.  
  
## Siehe auch  
 [prepareCall-Methode &#40;ISQLServerConnection&#41;](../content/prepareCall-Method--SQLServerConnection-.md)   
 [SQLServerConnection-Elemente](../content/SQLServerConnection-Members.md)   
 [SQLServerConnection-Klasse](../content/SQLServerConnection-Class.md)  
  
  