---
title: "getParameterMetaData-Methode (ISQLServerPreparedStatement)"
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
  - SQLServerPreparedStatement.getParameterMetaData
apilocation: 
  - sqljdbc.jar
apitype: Assembly
ms.assetid: c2876dec-ce29-4b61-9d74-ec3173b8cba5
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
# getParameterMetaData-Methode (ISQLServerPreparedStatement)
    
## getParameterMetaData\-Methode \(ISQLServerPreparedStatement\)  
 Ruft Anzahl, Typ und Eigenschaften der Parameter für dieses [SQLServerPreparedStatement](../content/SQLServerPreparedStatement-Class.md)\-Objekt ab.  
  
## Syntax  
  
```  
  
public final java.sql.ParameterMetaData getParameterMetaData()  
```  
  
## Rückgabewert  
 Ein [SQLServerParameterMetaData](../content/SQLServerParameterMetaData-Class.md)\-Objekt.  
  
## Ausnahmen  
 [SQLServerException](../content/SQLServerException-Class.md)  
  
## Hinweise  
 Die getParameterMetaData\-Methode wird von der getParameterMetaData\-Methode in der java.sql.PreparedStatement\-Schnittstelle angegeben.  
  
## Siehe auch  
 [SQLServerPreparedStatement-Elemente](../content/SQLServerPreparedStatement-Members.md)   
 [SQLServerPreparedStatement-Klasse](../content/SQLServerPreparedStatement-Class.md)  
  
  