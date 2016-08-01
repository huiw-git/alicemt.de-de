---
title: "allProceduresAreCallable-Methode (SQLServerDatabaseMetaData)"
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
  - SQLServerDatabaseMetaData.allProceduresAreCallable
apilocation: 
  - sqljdbc.jar
apitype: Assembly
ms.assetid: 8886137d-455e-497c-afea-4b326eda52f1
caps.latest.revision: 9
caps.handback.revision: 9
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
# allProceduresAreCallable-Methode (SQLServerDatabaseMetaData)
    
## allProceduresAreCallable\-Methode \(SQLServerDatabaseMetaData\)  
 Ruft ab, ob der aktuelle Benutzer zum Aufrufen aller Prozeduren berechtigt ist, die von der [getProcedures](../content/getProcedures-Method--SQLServerDatabaseMetaData-.md)\-Methode zurückgegeben werden.  
  
## Syntax  
  
```  
  
public boolean allProceduresAreCallable()  
```  
  
## Rückgabewert  
 **true**, wenn der Benutzer über Berechtigungen zum Aufrufen aller Prozeduren verfügt. Andernfalls wird **false** verwendet.  
  
## Ausnahmen  
 [SQLServerException](../content/SQLServerException-Class.md)  
  
## Hinweise  
 Diese allProceduresAreCallable\-Methode wird von der allProceduresAreCallable\-Methode in der java.sql.DatabaseMetaData\-Schnittstelle angegeben.  
  
## Siehe auch  
 [SQLServerDatabaseMetaData-Methoden](../content/SQLServerDatabaseMetaData-Methods.md)   
 [SQLServerDatabaseMetaData-Elemente](../content/SQLServerDatabaseMetaData-Members.md)   
 [SQLServerDatabaseMetaData-Klasse](../content/SQLServerDatabaseMetaData-Class.md)  
  
  