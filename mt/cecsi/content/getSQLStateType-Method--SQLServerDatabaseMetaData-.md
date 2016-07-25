---
title: "getSQLStateType-Methode (SQLServerDatabaseMetaData)"
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
  - SQLServerDatabaseMetaData.getSQLStateType
apilocation: 
  - sqljdbc.jar
apitype: Assembly
ms.assetid: ee4d6751-68a3-4d04-831c-e6d704c59e63
caps.latest.revision: 17
caps.handback.revision: 16
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
# getSQLStateType-Methode (SQLServerDatabaseMetaData)
    
## getSQLStateType\-Methode \(SQLServerDatabaseMetaData\)  
 Gibt an, ob "SQLSTATE" \(zurückgegeben von der SQLException.getSQLState\-Methode\) den Wert "X\/Open" \(jetzt "Open Group"\), "SQL CLI", "SQL99" \(JDBC 3.0\) oder "SQL:2003" \(JDBC 4.0\) besitzt.  
  
## Syntax  
  
```  
  
public int getSQLStateType()  
```  
  
## Rückgabewert  
 Ein Wert vom Typ **int** zum Angeben des SQLSTATE\-Typs. Mögliche Werte:  
  
-   Java Runtime Environment 5.0: Ist die **xopenStates**\-Verbindungseigenschaft auf **true** festgelegt, wird von dieser Methode DatabaseMetaData.sqlStateXOpen zurückgegeben. Andernfalls wird DatabaseMetaData.sqlStateSQL99 verwendet.  
  
-   Java Runtime Environment 6.0: Ist die **xopenStates**\-Verbindungseigenschaft auf **true** festgelegt, wird von dieser Methode DatabaseMetaData.sqlStateXOpen zurückgegeben. Andernfalls wird DatabaseMetaData.sqlStateSQL verwendet.  
  
## Ausnahmen  
 [SQLServerException](../content/SQLServerException-Class.md)  
  
## Hinweise  
 Diese getSQLStateType\-Methode wird von der getSQLStateType\-Methode in der java.sql.DatabaseMetaData\-Schnittstelle angegeben.  
  
## Siehe auch  
 [SQLServerDatabaseMetaData-Methoden](../content/SQLServerDatabaseMetaData-Methods.md)   
 [SQLServerDatabaseMetaData-Elemente](../content/SQLServerDatabaseMetaData-Members.md)   
 [SQLServerDatabaseMetaData-Klasse](../content/SQLServerDatabaseMetaData-Class.md)  
  
  