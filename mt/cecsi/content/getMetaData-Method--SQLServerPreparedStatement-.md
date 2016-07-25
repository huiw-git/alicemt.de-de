---
title: "getMetaData-Methode (ISQLServerPreparedStatement)"
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
  - SQLServerPreparedStatement.getMetaData
apilocation: 
  - sqljdbc.jar
apitype: Assembly
ms.assetid: 5ed49a53-ed61-4e95-ad67-45957aaabb6a
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
# getMetaData-Methode (ISQLServerPreparedStatement)
    
## getMetaData\-Methode \(ISQLServerPreparedStatement\)  
 Ruft ein [SQLServerResultSetMetaData-Klasse](../content/SQLServerResultSetMetaData-Class.md)\-Objekt mit Informationen zu den Spalten des [SQLServerResultSet](../content/SQLServerResultSet-Class.md)\-Objekts ab, das beim Ausführen dieses [SQLServerPreparedStatement](../content/SQLServerPreparedStatement-Class.md)\-Objekts zurückgegeben wird.  
  
## Syntax  
  
```  
  
public final java.sql.ResultSetMetaData getMetaData()  
```  
  
## Rückgabewert  
 Ein ResultSetMetaData\-Objekt.  
  
## Ausnahmen  
 [SQLServerException](../content/SQLServerException-Class.md)  
  
## Hinweise  
 Die getMetaData\-Methode wird von der getMetaData\-Methode in der java.sql.PreparedStatement\-Schnittstelle angegeben.  
  
## Siehe auch  
 [SQLServerPreparedStatement-Elemente](../content/SQLServerPreparedStatement-Members.md)   
 [SQLServerPreparedStatement-Klasse](../content/SQLServerPreparedStatement-Class.md)  
  
  