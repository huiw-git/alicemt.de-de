---
title: "isReadOnly-Methode (SQLServerResultSetMetaData)"
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
  - SQLServerResultSetMetaData.isReadOnly
apilocation: 
  - sqljdbc.jar
apitype: Assembly
ms.assetid: aba234d9-04ec-46a5-ba9e-7903f48b4ecc
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
# isReadOnly-Methode (SQLServerResultSetMetaData)
    
## isReadOnly\-Methode \(SQLServerResultSetMetaData\)  
 Gibt an, ob die angegebene Spalte definitiv schreibgeschützt ist.  
  
## Syntax  
  
```  
  
public boolean isReadOnly(int column)  
```  
  
#### Parameter  
 *column*  
  
 Ein Wert vom Typ **int** zum Angeben des Spaltenindexes.  
  
## Rückgabewert  
 Der Wert ist **true**, wenn die Spalte schreibgeschützt ist. Andernfalls wird **false** verwendet.  
  
## Ausnahmen  
 [SQLServerException](../content/SQLServerException-Class.md)  
  
## Hinweise  
 Diese isReadOnly\-Methode wird von der isReadOnly\-Methode in der java.sql.ResultSetMetaData\-Schnittstelle angegeben.  
  
## Siehe auch  
 [SQLServerResultSetMetaData-Methoden](../content/SQLServerResultSetMetaData-Methods.md)   
 [SQLServerResultSetMetaData-Elemente](../content/SQLServerResultSetMetaData-Members.md)   
 [SQLServerResultSetMetaData-Klasse](../content/SQLServerResultSetMetaData-Class.md)  
  
  