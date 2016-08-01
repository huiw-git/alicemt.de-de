---
title: "doesMaxRowSizeIncludeBlobs-Methode (SQLServerDatabaseMetaData)"
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
  - SQLServerDatabaseMetaData.doesMaxRowSizeIncludeBlobs
apilocation: 
  - sqljdbc.jar
apitype: Assembly
ms.assetid: 0c90a7a7-5a59-4858-bb26-3e725d8611d7
caps.latest.revision: 7
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
# doesMaxRowSizeIncludeBlobs-Methode (SQLServerDatabaseMetaData)
    
## doesMaxRowSizeIncludeBlobs\-Methode \(SQLServerDatabaseMetaData\)  
 Ruft ab, ob der Rückgabewert für die [getMaxRowSize](../content/getMaxRowSize-Method--SQLServerDatabaseMetaData-.md)\-Methode die SQL\-Datentypen "LONGVARCHAR" und "LONGVARBINARY" beinhaltet.  
  
## Syntax  
  
```  
  
public boolean doesMaxRowSizeIncludeBlobs()  
```  
  
## Rückgabewert  
 **true**, wenn der Rückgabewert die Datentypen einschließt. Andernfalls wird **false** verwendet.  
  
## Ausnahmen  
 [SQLServerException](../content/SQLServerException-Class.md)  
  
## Hinweise  
 Diese doesMoxRowSizeIncludeBlobs\-Methode wird von der doesMoxRowSizeIncludeBlobs\-Methode in der java.sql.DatabaseMetaData\-Schnittstelle angegeben.  
  
## Siehe auch  
 [SQLServerDatabaseMetaData-Methoden](../content/SQLServerDatabaseMetaData-Methods.md)   
 [SQLServerDatabaseMetaData-Elemente](../content/SQLServerDatabaseMetaData-Members.md)   
 [SQLServerDatabaseMetaData-Klasse](../content/SQLServerDatabaseMetaData-Class.md)  
  
  