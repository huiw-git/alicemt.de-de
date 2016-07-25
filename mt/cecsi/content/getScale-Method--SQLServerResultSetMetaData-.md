---
title: "getScale-Methode (SQLServerResultSetMetaData)"
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
  - SQLServerResultSetMetaData.getScale
apilocation: 
  - sqljdbc.jar
apitype: Assembly
ms.assetid: fe29aa5f-4cc5-413f-8bbd-a58064993d87
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
# getScale-Methode (SQLServerResultSetMetaData)
  Ruft für die angegebene Spalte die Anzahl von Stellen hinter dem Dezimalzeichen ab.  
  
## Syntax  
  
```  
  
public int getScale(int column)  
```  
  
#### Parameter  
 *column*  
  
 Ein Wert vom Typ **int** zum Angeben des Spaltenindex.  
  
## Rückgabewert  
 Ein Wert vom Typ **int** zum Angeben der Dezimalstellen der Spalte.  
  
## Ausnahmen  
 [SQLServerException](../content/SQLServerException-Class.md)  
  
## Hinweise  
 Diese getScale\-Methode wird von der getScale\-Methode in der java.sql.ResultSetMetaData\-Schnittstelle angegeben.  
  
 In [!INCLUDE[msCoName](../content/includes/msCoName_md.md)] [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] JDBC Driver 3.0 wurde das Verhalten in der DECIMAL\_DIGITS\-Spalte geändert. Weitere Informationen finden Sie unter [SQLServerDatabaseMetaData.getColumns](../content/getColumns-Method--SQLServerDatabaseMetaData-.md).  
  
## Siehe auch  
 [SQLServerResultSetMetaData-Elemente](../content/SQLServerResultSetMetaData-Members.md)   
 [SQLServerResultSetMetaData-Klasse](../content/SQLServerResultSetMetaData-Class.md)  
  
  