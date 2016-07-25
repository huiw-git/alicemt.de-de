---
title: "getWarnings-Methode (SQLServerResultSet)"
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
  - SQLServerResultSet.getWarnings
apilocation: 
  - sqljdbc.jar
apitype: Assembly
ms.assetid: eb4339b0-383b-4337-a935-e8ec3f0d4123
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
# getWarnings-Methode (SQLServerResultSet)
  Ruft die erste Warnung ab, die von Aufrufen für dieses [SQLServerResultSet](../content/SQLServerResultSet-Class.md)\-Objekt gemeldet wurde.  
  
> [!NOTE]  
>  Diese Methode wird von [!INCLUDE[jdbcNoVersion](../content/includes/jdbcNoVersion_md.md)] derzeit nicht unterstützt. Bei Aufruf wird von dieser Methode immer ein NULL\-Wert zurückgegeben.  
  
## Syntax  
  
```  
  
public java.sql.SQLWarning getWarnings()  
```  
  
## Rückgabewert  
 Ein SQLWarning\-Objekt.  
  
## Ausnahmen  
 [SQLServerException](../content/SQLServerException-Class.md)  
  
## Hinweise  
 Diese getWarnings\-Methode wird von der getWarnings\-Methode in der java.sql.ResultSet\-Schnittstelle angegeben.  
  
## Siehe auch  
 [ISQLServerResultSet-Elemente](../content/SQLServerResultSet-Members.md)   
 [SQLServerResultSet-Klasse](../content/SQLServerResultSet-Class.md)  
  
  