---
title: "supportsGroupByBeyondSelect-Methode (SQLServerDatabaseMetaData)"
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
  - SQLServerDatabaseMetaData.supportsGroupByBeyondSelect
apilocation: 
  - sqljdbc.jar
apitype: Assembly
ms.assetid: eadd2c37-d9ec-4b47-a91e-ed90b1eaf4b4
caps.latest.revision: 7
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
# supportsGroupByBeyondSelect-Methode (SQLServerDatabaseMetaData)
    
## supportsGroupByBeyondSelect\-Methode \(SQLServerDatabaseMetaData\)  
 Ruft ab, ob von dieser Datenbank die Verwendung von Spalten, die sich nicht in einer SELECT\-Anweisung befinden, in einer GROUP BY\-Klausel unterstützt wird, wenn gewährleistet ist, dass alle Spalten aus der SELECT\-Anweisung in der GROUP BY\-Klausel enthalten sind.  
  
## Syntax  
  
```  
  
public boolean supportsGroupByBeyondSelect()  
```  
  
## Rückgabewert  
 **true**, sofern unterstützt. Andernfalls wird **false** verwendet.  
  
## Ausnahmen  
 [SQLServerException](../content/SQLServerException-Class.md)  
  
## Hinweise  
 Diese supportsGroupByBeyondSelect\-Methode wird von der supportsGroupByBeyondSelect\-Methode in der java.sql.DatabaseMetaData\-Schnittstelle angegeben.  
  
## Siehe auch  
 [SQLServerDatabaseMetaData-Methoden](../content/SQLServerDatabaseMetaData-Methods.md)   
 [SQLServerDatabaseMetaData-Elemente](../content/SQLServerDatabaseMetaData-Members.md)   
 [SQLServerDatabaseMetaData-Klasse](../content/SQLServerDatabaseMetaData-Class.md)  
  
  