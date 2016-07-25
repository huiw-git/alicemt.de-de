---
title: "isSearchable-Methode (SQLServerResultSetMetaData)"
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
  - SQLServerResultSetMetaData.isSearchable
apilocation: 
  - sqljdbc.jar
apitype: Assembly
ms.assetid: 10cf54f9-ef42-475e-8397-790306934573
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
# isSearchable-Methode (SQLServerResultSetMetaData)
    
## isSearchable\-Methode \(SQLServerResultSetMetaData\)  
 Gibt an, ob die angegebene Spalte in einer SQL\-Klausel vom Typ "WHERE" verwendet werden kann.  
  
## Syntax  
  
```  
  
public boolean isSearchable(int column)  
```  
  
#### Parameter  
 *column*  
  
 Ein Wert vom Typ **int** zum Angeben des Spaltenindexes.  
  
## Rückgabewert  
 **true**, wenn die Spalte in einer Klausel vom Typ "WHERE" verwendet werden kann. Andernfalls wird **false** verwendet.  
  
## Ausnahmen  
 [SQLServerException](../content/SQLServerException-Class.md)  
  
## Hinweise  
 Diese isSearchable\-Methode wird von der isSearchable\-Methode in der java.sql.ResultSetMetaData\-Schnittstelle angegeben.  
  
## Siehe auch  
 [SQLServerResultSetMetaData-Methoden](../content/SQLServerResultSetMetaData-Methods.md)   
 [SQLServerResultSetMetaData-Elemente](../content/SQLServerResultSetMetaData-Members.md)   
 [SQLServerResultSetMetaData-Klasse](../content/SQLServerResultSetMetaData-Class.md)  
  
  