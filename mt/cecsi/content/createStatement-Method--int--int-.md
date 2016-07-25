---
title: "createStatement-Methode (int, int)"
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
  - SQLServerConnection.createStatement (int, int)
apilocation: 
  - sqljdbc.jar
apitype: Assembly
ms.assetid: 90dbf639-c3d8-4519-9300-5447c79aec17
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
# createStatement-Methode (int, int)
    
## createStatement\-Methode \(int, int\)  
 Erstellt ein [SQLServerStatement](../content/SQLServerStatement-Class.md)\-Objekt, von dem [SQLServerResultSet](../content/SQLServerResultSet-Class.md)\-Objekte mit dem angegebenen Typ und der angegebenen Parallelität generiert werden.  
  
## Syntax  
  
```  
  
public java.sql.Statement createStatement(int resultSetType,  
                                          int resultSetConcurrency)  
```  
  
#### Parameter  
 *resultSetType*  
  
 Der Wert vom Typ **int** , der den Resultsettyp darstellt.  
  
 *resultSetConcurrency*  
  
 Der Wert vom Typ **int** , der den Parallelitätstyp darstellt.  
  
## Rückgabewert  
 Das Statement\-Objekt.  
  
## Ausnahmen  
 [SQLServerException](../content/SQLServerException-Class.md)  
  
## Hinweise  
 Diese createStatement\-Methode wird von der createStatement\-Methode in der java.sql.Connection\-Schnittstelle angegeben.  
  
## Siehe auch  
 [createStatement-Methode &#40;ISQLServerConnection&#41;](../content/createStatement-Method--SQLServerConnection-.md)   
 [SQLServerConnection-Elemente](../content/SQLServerConnection-Members.md)   
 [SQLServerConnection-Klasse](../content/SQLServerConnection-Class.md)  
  
  