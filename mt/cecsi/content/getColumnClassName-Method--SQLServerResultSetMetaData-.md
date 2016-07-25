---
title: "getColumnClassName-Methode (SQLServerResultSetMetaData)"
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
  - SQLServerResultSetMetaData.getColumnClassName
apilocation: 
  - sqljdbc.jar
apitype: Assembly
ms.assetid: 2c118790-5dd2-4b10-93b6-7f065ee324ce
caps.latest.revision: 8
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
# getColumnClassName-Methode (SQLServerResultSetMetaData)
    
## getColumnClassName\-Methode \(SQLServerResultSetMetaData\)  
 Gibt den vollqualifizierten Namen der Java\-Klasse zurück, deren Instanzen erstellt werden, wenn die [getObject](../content/getObject-Method--SQLServerResultSet-.md)\-Methode der [SQLServerResultSet](../content/SQLServerResultSet-Class.md)\-Klasse aufgerufen wird, um einen Wert aus der Spalte abzurufen.  
  
## Syntax  
  
```  
  
public java.lang.String getColumnClassName(int column)  
```  
  
#### Parameter  
 *column*  
  
 Ein Wert vom Typ **int** zum Angeben des Spaltenindexes.  
  
## Rückgabewert  
 Ein **String** , der den vollqualifizierten Namen der Klasse enthält.  
  
## Ausnahmen  
 [SQLServerException](../content/SQLServerException-Class.md)  
  
## Hinweise  
 Diese getColumnClassName\-Methode wird von der getColumnClassName\-Methode in der java.sql.ResultSetMetaData\-Schnittstelle angegeben.  
  
## Siehe auch  
 [SQLServerResultSetMetaData-Methoden](../content/SQLServerResultSetMetaData-Methods.md)   
 [SQLServerResultSetMetaData-Elemente](../content/SQLServerResultSetMetaData-Members.md)   
 [SQLServerResultSetMetaData-Klasse](../content/SQLServerResultSetMetaData-Class.md)  
  
  