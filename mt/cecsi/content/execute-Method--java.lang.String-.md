---
title: "execute-Methode (java.lang.String)"
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
  - SQLServerPreparedStatement.execute (java.lang.String)
apilocation: 
  - sqljdbc.jar
apitype: Assembly
ms.assetid: a871917e-d286-46c3-96cf-2e8e8b22111c
caps.latest.revision: 10
caps.handback.revision: 10
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
# execute-Methode (java.lang.String)
    
## execute\-Methode \(java.lang.String\)  
 Führt die angegebene SQL\-Anweisung aus. Hierbei können mehrere Ergebnisse zurückgegeben werden.  
  
## Syntax  
  
```  
  
public final boolean execute(java.lang.String sql)  
```  
  
#### Parameter  
 *sql*  
  
 Ein **String** mit einer SQL\-Anweisung.  
  
## Rückgabewert  
 **true**, wenn von der Anweisung ein Resultset zurückgegeben wird. **false**, wenn eine Updatezählung oder kein Ergebnis zurückgegeben wird.  
  
## Ausnahmen  
 [SQLServerException](../content/SQLServerException-Class.md)  
  
## Hinweise  
 Diese execute\-Methode wird von der execute\-Methode in der java.sql.Statement\-Schnittstelle angegeben.  
  
 Die Methode überschreibt die [execute](../content/execute-Method--SQLServerStatement-.md)\-Methode, die sich in der [SQLServerStatement](../content/SQLServerStatement-Class.md)\-Klasse befindet.  
  
 Durch den Aufruf dieser Methode wird eine Ausnahme ausgelöst, da die SQL\-Anweisung für das SQLServerPreparedStatement\-Objekt bei der Erstellung des Objekts angegeben wird.  
  
## Siehe auch  
 [execute-Methode &#40;ISQLServerPreparedStatement&#41;](../content/execute-Method--SQLServerPreparedStatement-.md)   
 [SQLServerPreparedStatement-Elemente](../content/SQLServerPreparedStatement-Members.md)   
 [SQLServerPreparedStatement-Klasse](../content/SQLServerPreparedStatement-Class.md)  
  
  