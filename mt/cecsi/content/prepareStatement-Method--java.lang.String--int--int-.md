---
title: "prepareStatement-Methode (java.lang.String, int, int)"
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
  - SQLServerConnection.prepareStatement (java.lang.String, int, int)
apilocation: 
  - sqljdbc.jar
apitype: Assembly
ms.assetid: 5bb96dbe-f673-41b5-911b-8f661cca071a
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
# prepareStatement-Methode (java.lang.String, int, int)
    
## prepareStatement\-Methode \(java.lang.String, int, int\)  
 Erstellt ein [SQLServerPreparedStatement](../content/SQLServerPreparedStatement-Class.md)\-Objekt, mit dem [SQLServerResultSet](../content/SQLServerResultSet-Class.md)\-Objekte mit dem angegebenen Typ und der Parallelität generiert werden.  
  
## Syntax  
  
```  
  
public java.sql.PreparedStatement prepareStatement(java.lang.String sSql,  
                                                   int resultSetType,  
                                                   int resultSetConcurrency)  
```  
  
#### Parameter  
 *sSql*  
  
 Ein **String** mit einer SQL\-Anweisung.  
  
 *resultSetType*  
  
 Ein Wert vom Typ **int**  zur Angabe des Resultsettyps.  
  
 *resultSetConcurrency*  
  
 Ein Wert vom Typ **int**  zur Angabe des Paralellitätstyps des Resultsets.  
  
## Rückgabewert  
 Ein PreparedStatement\-Objekt.  
  
## Ausnahmen  
 [SQLServerException](../content/SQLServerException-Class.md)  
  
## Hinweise  
 Diese prepareStatement\-Methode wird von der prepareStatement\-Methode in der java.sql.Connection\-Schnittstelle angegeben.  
  
## Siehe auch  
 [ISQLServerConnection-Methoden](../content/SQLServerConnection-Methods.md)   
 [SQLServerConnection-Elemente](../content/SQLServerConnection-Members.md)   
 [SQLServerConnection-Klasse](../content/SQLServerConnection-Class.md)  
  
  