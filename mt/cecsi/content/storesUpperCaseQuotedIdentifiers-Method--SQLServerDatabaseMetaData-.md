---
title: "storesUpperCaseQuotedIdentifiers-Methode (SQLServerDatabaseMetaData)"
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
  - SQLServerDatabaseMetaData.storesUpperCaseQuotedIdentifiers
apilocation: 
  - sqljdbc.jar
apitype: Assembly
ms.assetid: 936ec140-2597-44e6-82d3-3994a676ee35
caps.latest.revision: 8
caps.handback.revision: 7
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
# storesUpperCaseQuotedIdentifiers-Methode (SQLServerDatabaseMetaData)
    
## storesUpperCaseQuotedIdentifiers\-Methode \(SQLServerDatabaseMetaData\)  
 Ruft ab, ob bei SQL\-Bezeichnern mit gemischter Groß\-\/Kleinschreibung, die in Anführungszeichen gesetzt sind, die Groß\-\/Kleinschreibung nicht berücksichtigt wird und die Bezeichner in Großbuchstaben gespeichert werden.  
  
## Syntax  
  
```  
  
public boolean storesUpperCaseQuotedIdentifiers()  
```  
  
## Rückgabewert  
 **true**, wenn die Bezeichner in Großbuchstaben gespeichert werden. Andernfalls wird **false** verwendet.  
  
## Ausnahmen  
 [SQLServerException](../content/SQLServerException-Class.md)  
  
## Hinweise  
 Diese storesUpperCaseQuotedIdentifiers\-Methode wird von der storesUpperCaseQuotedIdentifiers\-Methode in der java.sql.DatabaseMetaData\-Schnittstelle angegeben.  
  
## Siehe auch  
 [SQLServerDatabaseMetaData-Methoden](../content/SQLServerDatabaseMetaData-Methods.md)   
 [SQLServerDatabaseMetaData-Elemente](../content/SQLServerDatabaseMetaData-Members.md)   
 [SQLServerDatabaseMetaData-Klasse](../content/SQLServerDatabaseMetaData-Class.md)  
  
  