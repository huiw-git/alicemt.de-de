---
title: "supportsResultSetHoldability-Methode (SQLServerDatabaseMetaData)"
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
  - SQLServerDatabaseMetaData.supportsResultSetHoldability
apilocation: 
  - sqljdbc.jar
apitype: Assembly
ms.assetid: ab575792-fd11-4ff3-8847-1368e7a322c5
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
# supportsResultSetHoldability-Methode (SQLServerDatabaseMetaData)
    
## supportsResultSetHoldability\-Methode \(SQLServerDatabaseMetaData\)  
 Ruft ab, ob von dieser Datenbank die angegebene Resultsethaltbarkeit unterstützt wird.  
  
## Syntax  
  
```  
  
public boolean supportsResultSetHoldability(int holdability)  
```  
  
#### Parameter  
 *holdability*  
  
 Ein Wert vom Typ **int** zum Angeben der Resultsethaltbarkeit. Mögliche Werte:  
  
 ResultSet.HOLD\_CURSORS\_OVER\_COMMIT  
  
 ResultSet.CLOSE\_CURSORS\_AT\_COMMIT  
  
## Rückgabewert  
 **true**, sofern unterstützt. Andernfalls wird **false** verwendet.  
  
## Ausnahmen  
 [SQLServerException](../content/SQLServerException-Class.md)  
  
## Hinweise  
 Diese supportsResultSetHoldability\-Methode wird von der supportsResultSetHoldability\-Methode in der java.sql.DatabaseMetaData\-Schnittstelle angegeben.  
  
## Siehe auch  
 [SQLServerDatabaseMetaData-Methoden](../content/SQLServerDatabaseMetaData-Methods.md)   
 [SQLServerDatabaseMetaData-Elemente](../content/SQLServerDatabaseMetaData-Members.md)   
 [SQLServerDatabaseMetaData-Klasse](../content/SQLServerDatabaseMetaData-Class.md)  
  
  