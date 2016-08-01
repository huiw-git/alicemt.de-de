---
title: "getGeneratedKeys-Methode (SQLServerStatement)"
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
  - SQLServerStatement.getGeneratedKeys
apilocation: 
  - sqljdbc.jar
apitype: Assembly
ms.assetid: a3325950-0e81-4ae8-aa0c-e1f6d371adcd
caps.latest.revision: 12
caps.handback.revision: 11
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
# getGeneratedKeys-Methode (SQLServerStatement)
    
## getGeneratedKeys\-Methode \(SQLServerStatement\)  
 Ruft sämtliche automatisch generierte Schlüssel ab, die aufgrund der Ausführung dieses [SQLServerStatement](../content/SQLServerStatement-Class.md)\-Objekts erstellt werden.  
  
## Syntax  
  
```  
  
public final java.sql.ResultSet getGeneratedKeys()  
```  
  
## Rückgabewert  
 Ein ResultSet\-Objekt.  
  
## Ausnahmen  
 [SQLServerException](../content/SQLServerException-Class.md)  
  
## Hinweise  
 Diese getGeneratedKeys\-Methode wird von der getGeneratedKeys\-Methode in der java.sql.Statement\-Schnittstelle angegeben.  
  
 Weitere Informationen zur Verwendung dieser Methode finden Sie unter [Verwenden von automatisch generierten Schlüsseln](../content/Using-Auto-Generated-Keys.md).  
  
## Siehe auch  
 [SQLServerStatement-Elemente](../content/SQLServerStatement-Members.md)   
 [SQLServerStatement-Klasse](../content/SQLServerStatement-Class.md)  
  
  