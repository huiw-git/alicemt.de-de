---
title: "getStatement-Methode (ISQLServerResultSet)"
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
  - SQLServerResultSet.getStatement
apilocation: 
  - sqljdbc.jar
apitype: Assembly
ms.assetid: 7dea981b-b4fd-4f8d-954f-e686124627e2
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
# getStatement-Methode (ISQLServerResultSet)
    
## getStatement\-Methode \(ISQLServerResultSet\)  
 Ruft das [SQLServerStatement](../content/SQLServerStatement-Class.md)\-Objekt ab, von dem dieses [SQLServerResultSet](../content/SQLServerResultSet-Class.md)\-Objekt erstellt wurde.  
  
## Syntax  
  
```  
  
public java.sql.Statement getStatement()  
```  
  
## Rückgabewert  
 Ein SQLServerStatement\-Objekt.  
  
## Ausnahmen  
 [SQLServerException](../content/SQLServerException-Class.md)  
  
## Hinweise  
 Diese getStatement\-Methode wird von der getStatement\-Methode in der java.sql.ResultSet\-Schnittstelle angegeben.  
  
 Wird das Resultset auf andere Art erstellt, z. B. mit einer [SQLServerDatabaseMetaData](../content/SQLServerDatabaseMetaData-Class.md)\-Methode, wird von der Methode NULL zurückgegeben.  
  
## Siehe auch  
 [ISQLServerResultSet-Elemente](../content/SQLServerResultSet-Members.md)   
 [SQLServerResultSet-Klasse](../content/SQLServerResultSet-Class.md)  
  
  