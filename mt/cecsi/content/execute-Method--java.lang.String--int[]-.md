---
title: "execute-Methode (java.lang.String, int)"
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
  - SQLServerStatement.execute (javal.lang.String.int[])
apilocation: 
  - sqljdbc.jar
apitype: Assembly
ms.assetid: dc73d1c3-e756-43af-b1fc-ac438cbd0965
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
# execute-Methode (java.lang.String, int)
  Führt die angegebene SQL\-Anweisung aus, von der mehrere Ergebnisse zurückgegeben werden können, und signalisiert [!INCLUDE[jdbcNoVersion](../content/includes/jdbcNoVersion_md.md)], dass die automatisch generierten Schlüssel, die in dem angegebenen Array angegeben sind, zum Abrufen verfügbar gemacht werden sollen.  
  
## Syntax  
  
```  
  
public final boolean execute(java.lang.String sql,  
                             int[] columnIndexes)  
```  
  
#### Parameter  
 *sql*  
  
 Ein **String** mit einer SQL\-Anweisung.  
  
 *columnIndexes*  
  
 Ein Array von **int**\-Werten, mit dem angegeben wird, welche Spaltenindizes der automatisch generierten Schlüssel verfügbar gemacht werden sollen.  
  
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
  
  