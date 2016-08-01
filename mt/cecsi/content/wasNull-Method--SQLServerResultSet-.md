---
title: "wasNull-Methode (ISQLServerResultSet)"
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
  - SQLServerResultSet.wasNull
apilocation: 
  - sqljdbc.jar
apitype: Assembly
ms.assetid: d37f80ef-d72c-4429-ada3-1d685bdab6d7
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
# wasNull-Methode (ISQLServerResultSet)
    
## wasNull\-Methode \(ISQLServerResultSet\)  
 Überprüft, ob es sich beim letzten gelesenen Wert um einen NULL\-Wert handelt.  
  
## Syntax  
  
```  
  
public boolean wasNull()  
```  
  
## Rückgabewert  
 **true**, wenn der letzte gelesene Wert NULL war. Andernfalls wird **false** verwendet.  
  
## Ausnahmen  
 [SQLServerException](../content/SQLServerException-Class.md)  
  
## Hinweise  
 Diese wasNull\-Methode wird von der wasNull\-Methode in der java.sql.ResultSet\-Schnittstelle angegeben.  
  
## Siehe auch  
 [ISQLServerResultSet-Elemente](../content/SQLServerResultSet-Members.md)   
 [SQLServerResultSet-Klasse](../content/SQLServerResultSet-Class.md)  
  
  