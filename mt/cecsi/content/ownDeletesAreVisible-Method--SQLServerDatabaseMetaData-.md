---
title: "ownDeletesAreVisible-Methode (SQLServerDatabaseMetaData)"
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
  - SQLServerDatabaseMetaData.ownDeletesAreVisible
apilocation: 
  - sqljdbc.jar
apitype: Assembly
ms.assetid: 2dd6d976-9f8f-4a24-9354-ff239cfd4364
caps.latest.revision: 10
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
# ownDeletesAreVisible-Methode (SQLServerDatabaseMetaData)
    
## ownDeletesAreVisible\-Methode \(SQLServerDatabaseMetaData\)  
 Ruft ab, ob die eigenen Löschvorgänge eines Resultsets sichtbar sind.  
  
## Syntax  
  
```  
  
public boolean ownDeletesAreVisible(int type)  
```  
  
#### Parameter  
 *type*  
  
 Ein Wert vom Typ **int** zum Angeben des Resultsettyps, bei dem es sich gemäß Definition in "java.sql.ResultSet" oder "SQLServerResultSet" um einen der folgenden Werte handeln kann:  
  
### java.sql.ResultSet\-Typen  
 TYPE\_FORWARD\_ONLY  
  
 TYPE\_SCROLL\_SENSITIVE  
  
 TYPE\_SCROLL\_INSENSITIVE  
  
### SQLServerResultSet\-Typen  
 TYPE\_SS\_SCROLL\_STATIC  
  
 TYPE\_SS\_SCROLL\_KEYSET  
  
 TYPE\_SS\_DIRECT\_FORWARD\_ONLY  
  
 TYPE\_SS\_SERVER\_CURSOR\_FORWARD\_ONLY  
  
 TYPE\_SS\_SCROLL\_DYNAMIC  
  
## Rückgabewert  
 **true**, wenn die Löschvorgänge sichtbar sind. Andernfalls wird **false** verwendet.  
  
## Ausnahmen  
 [SQLServerException](../content/SQLServerException-Class.md)  
  
## Hinweise  
 Diese ownDeletesAreVisible\-Methode wird von der ownDeletesAreVisible\-Methode in der java.sql.DatabaseMetaData\-Schnittstelle angegeben.  
  
## Siehe auch  
 [SQLServerDatabaseMetaData-Methoden](../content/SQLServerDatabaseMetaData-Methods.md)   
 [SQLServerDatabaseMetaData-Elemente](../content/SQLServerDatabaseMetaData-Members.md)   
 [SQLServerDatabaseMetaData-Klasse](../content/SQLServerDatabaseMetaData-Class.md)  
  
  