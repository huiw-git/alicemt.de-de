---
title: "storesMixedCaseIdentifiers-Methode (SQLServerDatabaseMetaData)"
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
  - SQLServerDatabaseMetaData.storesMixedCaseIdentifiers
apilocation: 
  - sqljdbc.jar
apitype: Assembly
ms.assetid: a91e5cd6-22b1-464e-aeec-665590737a74
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
# storesMixedCaseIdentifiers-Methode (SQLServerDatabaseMetaData)
    
## storesMixedCaseIdentifiers\-Methode \(SQLServerDatabaseMetaData\)  
 Ruft ab, ob bei SQL\-Bezeichnern mit gemischter Groß\-\/Kleinschreibung, die nicht in Anführungszeichen gesetzt sind, die Groß\-\/Kleinschreibung nicht berücksichtigt wird und die Bezeichner mit gemischter Groß\-\/Kleinschreibung gespeichert werden.  
  
## Syntax  
  
```  
  
public boolean storesMixedCaseIdentifiers()  
```  
  
## Rückgabewert  
 **true**, wenn die Bezeichner sowohl in Klein\- als auch in Großbuchstaben gespeichert werden. Andernfalls wird **false** verwendet.  
  
## Ausnahmen  
 [SQLServerException](../content/SQLServerException-Class.md)  
  
## Hinweise  
 Diese storesMixedCaseIdentifiers\-Methode wird von der storesMixedCaseIdentifiers\-Methode in der java.sql.DatabaseMetaData\-Schnittstelle angegeben.  
  
## Siehe auch  
 [SQLServerDatabaseMetaData-Methoden](../content/SQLServerDatabaseMetaData-Methods.md)   
 [SQLServerDatabaseMetaData-Elemente](../content/SQLServerDatabaseMetaData-Members.md)   
 [SQLServerDatabaseMetaData-Klasse](../content/SQLServerDatabaseMetaData-Class.md)  
  
  