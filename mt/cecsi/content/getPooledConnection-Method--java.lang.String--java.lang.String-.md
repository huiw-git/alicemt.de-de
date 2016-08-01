---
title: "getPooledConnection-Methode (java.lang.String, java.lang.String)"
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
  - SQLServerConnectionPoolDataSource.getPooledConnection (java.lang.String, java.lang.String)
apilocation: 
  - sqljdbc.jar
apitype: Assembly
ms.assetid: f2e6391d-9aaf-4b09-ae1c-a27c1ada6301
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
# getPooledConnection-Methode (java.lang.String, java.lang.String)
    
## getPooledConnection\-Methode \(java.lang.String, java.lang.String\)  
 Stellt eine physische Datenbankverbindung her, die auf Grundlage des angegebenen Benutzernamens und Kennworts als Poolverbindung verwendet werden kann.  
  
## Syntax  
  
```  
  
public javax.sql.PooledConnection getPooledConnection(java.lang.String user,  
                                                      java.lang.String password)  
```  
  
#### Parameter  
 *user*  
  
 Ein **String** mit dem Benutzernamen.  
  
 *passwword*  
  
 Ein **String** mit dem Kennwort.  
  
## Rückgabewert  
 Ein [SQLServerPooledConnection](../content/SQLServerPooledConnection-Class.md)\-Objekt.  
  
## Ausnahmen  
 java.sql.SQLException  
  
## Hinweise  
 Diese getPooledConnection\-Methode wird von der getPooledConnection\-Methode in der javax.sql.ConnectionPoolDataSource\-Schnittstelle angegeben.  
  
## Siehe auch  
 [getPooledConnection](../content/getPooledConnection-Method--SQLServerConnectionPoolDataSource-.md)   
 [SQLServerConnectionPoolDataSource-Methoden](../content/SQLServerConnectionPoolDataSource-Methods.md)   
 [SQLServerConnectionPoolDataSource-Elemente](../content/SQLServerConnectionPoolDataSource-Members.md)   
 [SQLServerConnectionPoolDataSource-Klasse](../content/SQLServerConnectionPoolDataSource-Class.md)  
  
  