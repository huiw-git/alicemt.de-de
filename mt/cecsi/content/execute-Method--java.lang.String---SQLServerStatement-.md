---
title: "execute-Methode (java.lang.String) (ISQLServerStatement)"
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
  - SQLServerStatement.execute (java.lang.String)
apilocation: 
  - sqljdbc.jar
apitype: Assembly
ms.assetid: 64ac78b8-d5b3-4134-9b72-d2b0c52168a2
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
# execute-Methode (java.lang.String) (ISQLServerStatement)
    
## execute\-Methode \(java.lang.String\) \(ISQLServerStatement\)  
 Führt die angegebene SQL\-Anweisung aus. Hierbei können mehrere Ergebnisse zurückgegeben werden.  
  
## Syntax  
  
```  
  
public boolean execute(java.lang.String sql)  
```  
  
#### Parameter  
 *sql*  
  
 Ein **String** mit einer SQL\-Anweisung.  
  
## Rückgabewert  
 **true**, wenn es sich beim ersten Ergebnis um ein Resultset handelt. Andernfalls wird **false** verwendet.  
  
## Ausnahmen  
 [SQLServerException](../content/SQLServerException-Class.md)  
  
## Hinweise  
 Diese execute\-Methode wird von der execute\-Methode in der java.sql.Statement\-Schnittstelle angegeben.  
  
## Siehe auch  
 [execute-Methode &#40;SQLServerStatement&#41;](../content/execute-Method--SQLServerStatement-.md)   
 [SQLServerStatement-Elemente](../content/SQLServerStatement-Members.md)   
 [SQLServerStatement-Klasse](../content/SQLServerStatement-Class.md)  
  
  