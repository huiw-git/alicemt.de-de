---
title: "execute-Methode (java.lang.String, int)"
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
  - SQLServerStatement.execute (java.lang.String.int)
apilocation: 
  - sqljdbc.jar
apitype: Assembly
ms.assetid: c8ea589e-5736-412d-9cd1-79bc4964f847
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
  Führt die angegebene SQL\-Anweisung aus, von der mehrere Ergebnisse zurückgegeben werden können, und signalisiert [!INCLUDE[jdbcNoVersion](../content/includes/jdbcNoVersion_md.md)], dass alle automatisch generierten Schlüssel zum Abrufen verfügbar gemacht werden sollen.  
  
## Syntax  
  
```  
  
public final boolean execute(java.lang.String sql,  
                             int flag)  
```  
  
#### Parameter  
 *sql*  
  
 Ein **String** mit einer SQL\-Anweisung.  
  
 *flag*  
  
 Ein Wert vom Typ **int** zum Angeben, ob automatisch generierte Schlüssel verfügbar gemacht werden sollen. Dabei muss es sich um eine der folgenden Konstanten handeln:  
  
 RETURN\_GENERATED\_KEYS  
  
 NO\_GENERATED\_KEYS  
  
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
  
  