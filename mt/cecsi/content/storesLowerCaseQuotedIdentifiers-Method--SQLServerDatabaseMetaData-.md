---
title: "storesLowerCaseQuotedIdentifiers-Methode (SQLServerDatabaseMetaData)"
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
  - SQLServerDatabaseMetaData.storesLowerCaseQuotedIdentifiers
apilocation: 
  - sqljdbc.jar
apitype: Assembly
ms.assetid: 3e104c9e-66d4-436b-8b5b-a00ff667c95b
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
# storesLowerCaseQuotedIdentifiers-Methode (SQLServerDatabaseMetaData)
    
## storesLowerCaseQuotedIdentifiers\-Methode \(SQLServerDatabaseMetaData\)  
 Ruft ab, ob bei SQL\-Bezeichnern mit gemischter Groß\-\/Kleinschreibung, die in Anführungszeichen gesetzt sind, die Groß\-\/Kleinschreibung nicht berücksichtigt wird und die Bezeichner in Kleinbuchstaben gespeichert werden.  
  
## Syntax  
  
```  
  
public boolean storesLowerCaseQuotedIdentifiers()  
```  
  
## Rückgabewert  
 **true**, wenn die Bezeichner in Kleinbuchstaben gespeichert werden. Andernfalls wird **false** verwendet.  
  
## Ausnahmen  
 [SQLServerException](../content/SQLServerException-Class.md)  
  
## Hinweise  
 Diese storesLowerCaseQuotedIdentifiers\-Methode wird von der storesLowerCaseQuotedIdentifiers\-Methode in der java.sql.DatabaseMetaData\-Schnittstelle angegeben.  
  
## Siehe auch  
 [SQLServerDatabaseMetaData-Methoden](../content/SQLServerDatabaseMetaData-Methods.md)   
 [SQLServerDatabaseMetaData-Elemente](../content/SQLServerDatabaseMetaData-Members.md)   
 [SQLServerDatabaseMetaData-Klasse](../content/SQLServerDatabaseMetaData-Class.md)  
  
  