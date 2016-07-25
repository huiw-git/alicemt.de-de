---
title: "execute-Methode (java.lang.String, java.lang.String)"
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
  - SQLServerStatement.execute (java.lang.String.java.lang.String[])
apilocation: 
  - sqljdbc.jar
apitype: Assembly
ms.assetid: 9451c7c2-4c0d-4d1e-9b42-a26ff28e3f6a
caps.latest.revision: 13
caps.handback.revision: 12
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
# execute-Methode (java.lang.String, java.lang.String)
  Führt die angegebene SQL\-Anweisung aus, von der mehrere Ergebnisse zurückgegeben werden können, und signalisiert [!INCLUDE[jdbcNoVersion](../content/includes/jdbcNoVersion_md.md)], dass die automatisch generierten Schlüssel, die in dem angegebenen Array angegeben sind, zum Abrufen verfügbar gemacht werden sollen.  
  
## Syntax  
  
```  
  
public final boolean execute(java.lang.String sql,  
                             java.lang.String[] columnNames)  
```  
  
#### Parameter  
 *sql*  
  
 Ein **String** mit einer SQL\-Anweisung.  
  
 *columnNames*  
  
 Ein Zeichenfolgenarray, mit dem angegeben wird, welche Spaltennamen der automatisch generierten Schlüssel verfügbar gemacht werden sollen.  
  
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
  
  