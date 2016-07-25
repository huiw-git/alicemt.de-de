---
title: "supportsOrderByUnrelated-Methode (SQLServerDatabaseMetaData)"
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
  - SQLServerDatabaseMetaData.supportsOrderByUnrelated
apilocation: 
  - sqljdbc.jar
apitype: Assembly
ms.assetid: 9ea6c534-8132-49f3-aac3-a12ec4c46df2
caps.latest.revision: 6
caps.handback.revision: 6
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
# supportsOrderByUnrelated-Methode (SQLServerDatabaseMetaData)
    
## supportsOrderByUnrelated\-Methode \(SQLServerDatabaseMetaData\)  
 Ruft ab, ob von dieser Datenbank die Verwendung einer Spalte, die sich nicht in der SELECT\-Anweisung befindet, in einer ORDER BY\-Klausel unterstützt wird.  
  
## Syntax  
  
```  
  
public boolean supportsOrderByUnrelated()  
```  
  
## Rückgabewert  
 **true**, sofern unterstützt. Andernfalls wird **false** verwendet.  
  
## Ausnahmen  
 [SQLServerException](../content/SQLServerException-Class.md)  
  
## Hinweise  
 Diese supportsOrderByUnrelated\-Methode wird von der supportsOrderByUnrelated\-Methode in der java.sql.DatabaseMetaData\-Schnittstelle angegeben.  
  
## Siehe auch  
 [SQLServerDatabaseMetaData-Methoden](../content/SQLServerDatabaseMetaData-Methods.md)   
 [SQLServerDatabaseMetaData-Elemente](../content/SQLServerDatabaseMetaData-Members.md)   
 [SQLServerDatabaseMetaData-Klasse](../content/SQLServerDatabaseMetaData-Class.md)  
  
  