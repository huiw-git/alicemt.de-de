---
title: "executeQuery-Methode (java.lang.String)"
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
  - SQLServerPreparedStatement.executeQuery (java.lang.String)
apilocation: 
  - sqljdbc.jar
apitype: Assembly
ms.assetid: 610205c2-6bcd-426c-ad6f-9682551efdec
caps.latest.revision: 11
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
# executeQuery-Methode (java.lang.String)
    
## executeQuery\-Methode \(java.lang.String\)  
 Führt die angegebene SQL\-Anweisung aus und gibt ein einzelnes [SQLServerResultSet](../content/SQLServerResultSet-Class.md)\-Objekt zurück.  
  
## Syntax  
  
```  
  
public final java.sql.ResultSet executeQuery(java.lang.String sql)  
```  
  
#### Parameter  
 *sql*  
  
 Ein **String** mit einer SQL\-Anweisung.  
  
## Rückgabewert  
 Ein SQLServerResultSet\-Objekt.  
  
## Ausnahmen  
 [SQLServerException](../content/SQLServerException-Class.md)  
  
## Hinweise  
 Diese executeQuery\-Methode wird von der executeQuery\-Methode in der java.sql.Statement\-Schnittstelle angegeben.  
  
 Die Methode überschreibt die [executeQuery](../content/executeQuery-Method--SQLServerStatement-.md)\-Methode, die sich in der [SQLServerStatement](../content/SQLServerStatement-Class.md)\-Klasse befindet.  
  
 Durch den Aufruf dieser Methode wird eine Ausnahme ausgelöst, da die SQL\-Anweisung für das SQLServerPreparedStatement\-Objekt bei der Erstellung des Objekts angegeben wird.  
  
 [SQLServerException](../content/SQLServerException-Class.md) wird ausgelöst, wenn die angegebene SQL\-Anweisung etwas anderes als ein einzelnes [SQLServerResultSet](../content/SQLServerResultSet-Class.md)\-Objekt produziert.  
  
## Siehe auch  
 [executeQuery-Methode &#40;ISQLServerPreparedStatement&#41;](../content/executeQuery-Method--SQLServerPreparedStatement-.md)   
 [SQLServerPreparedStatement-Elemente](../content/SQLServerPreparedStatement-Members.md)   
 [SQLServerPreparedStatement-Klasse](../content/SQLServerPreparedStatement-Class.md)  
  
  