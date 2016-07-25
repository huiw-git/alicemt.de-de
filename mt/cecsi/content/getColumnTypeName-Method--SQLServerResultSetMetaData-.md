---
title: "getColumnTypeName-Methode (SQLServerResultSetMetaData)"
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
  - SQLServerResultSetMetaData.getColumnTypeName
apilocation: 
  - sqljdbc.jar
apitype: Assembly
ms.assetid: a444da82-c1af-40a5-9774-02476416c92c
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
# getColumnTypeName-Methode (SQLServerResultSetMetaData)
  Ruft den datenbankspezifischen Typnamen für die angegebene Spalte ab.  
  
## Syntax  
  
```  
  
public java.lang.String getColumnTypeName(int column)  
```  
  
#### Parameter  
 *column*  
  
 Ein Wert vom Typ **int** zum Angeben des Spaltenindex.  
  
## Rückgabewert  
 Ein **String** mit dem Servernamen für die Spalte.  
  
## Ausnahmen  
 [SQLServerException](../content/SQLServerException-Class.md)  
  
## Hinweise  
 Diese getColumnTypeName\-Methode wird von der getColumnTypeName\-Methode in der java.sql.ResultSetMetaData\-Schnittstelle angegeben.  
  
 In [!INCLUDE[msCoName](../content/includes/msCoName_md.md)] [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] JDBC Driver 3.0 wurde das Verhalten in der TYPE\_NAME\-Spalte geändert. Weitere Informationen finden Sie unter [SQLServerDatabaseMetaData.getColumns](../content/getColumns-Method--SQLServerDatabaseMetaData-.md).  
  
## Siehe auch  
 [SQLServerResultSetMetaData-Elemente](../content/SQLServerResultSetMetaData-Members.md)   
 [SQLServerResultSetMetaData-Klasse](../content/SQLServerResultSetMetaData-Class.md)  
  
  