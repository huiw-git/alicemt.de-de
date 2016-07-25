---
title: "getColumnDisplaySize-Methode (SQLServerResultSetMetaData)"
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
  - SQLServerResultSetMetaData.getColumnDisplaySize
apilocation: 
  - sqljdbc.jar
apitype: Assembly
ms.assetid: 21c25443-bd2b-4b60-9798-4efe2c158952
caps.latest.revision: 12
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
# getColumnDisplaySize-Methode (SQLServerResultSetMetaData)
  Gibt die normale maximale Breite für die angegebene Spalte in Zeichen zurück.  
  
## Syntax  
  
```  
  
public int getColumnDisplaySize(int column)  
```  
  
#### Parameter  
 *column*  
  
 Ein Wert vom Typ **int** zum Angeben des Spaltenindex.  
  
## Rückgabewert  
 Ein Wert vom Typ **int** zum Angeben der maximalen Breite. Ist die Breite unbekannt, wird "0" zurückgegeben.  
  
## Ausnahmen  
 [SQLServerException](../content/SQLServerException-Class.md)  
  
## Hinweise  
 Diese getColumnDisplaySize\-Methode wird von der getColumnDisplaySize\-Methode in der java.sql.ResultSetMetaData\-Schnittstelle angegeben.  
  
 In [!INCLUDE[msCoName](../content/includes/msCoName_md.md)] [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] JDBC Driver 3.0 wurde das Verhalten in der COLUMN\_SIZE\-Spalte geändert. Weitere Informationen finden Sie unter [SQLServerDatabaseMetaData.getColumns](../content/getColumns-Method--SQLServerDatabaseMetaData-.md).  
  
## Siehe auch  
 [SQLServerResultSetMetaData-Elemente](../content/SQLServerResultSetMetaData-Members.md)   
 [SQLServerResultSetMetaData-Klasse](../content/SQLServerResultSetMetaData-Class.md)  
  
  