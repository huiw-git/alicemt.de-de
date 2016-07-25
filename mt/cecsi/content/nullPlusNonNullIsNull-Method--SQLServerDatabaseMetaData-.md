---
title: "nullPlusNonNullIsNull-Methode (SQLServerDatabaseMetaData)"
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
  - SQLServerDatabaseMetaData.nullPlusNonNullIsNull
apilocation: 
  - sqljdbc.jar
apitype: Assembly
ms.assetid: c594736f-3a9b-463f-bbd8-eaf9221230ea
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
# nullPlusNonNullIsNull-Methode (SQLServerDatabaseMetaData)
    
## nullPlusNonNullIsNull\-Methode \(SQLServerDatabaseMetaData\)  
 Gibt an, ob von dieser Datenbank unterstützt wird, dass Verkettungen zwischen NULL\-Werten und Werten ungleich NULL einen NULL\-Wert ergeben.  
  
## Syntax  
  
```  
  
public boolean nullPlusNonNullIsNull()  
```  
  
## Rückgabewert  
 **true**, sofern Verkettungen unterstützt werden. Andernfalls wird **false** verwendet.  
  
## Ausnahmen  
 [SQLServerException](../content/SQLServerException-Class.md)  
  
## Hinweise  
 Diese nullPlusNonNullIsNull\-Methode wird von der nullPlusNonNullIsNull\-Methode in der java.sql.DatabaseMetaData\-Schnittstelle angegeben.  
  
## Siehe auch  
 [SQLServerDatabaseMetaData-Elemente](../content/SQLServerDatabaseMetaData-Members.md)   
 [SQLServerDatabaseMetaData-Klasse](../content/SQLServerDatabaseMetaData-Class.md)  
  
  