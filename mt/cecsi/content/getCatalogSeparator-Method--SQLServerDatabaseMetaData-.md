---
title: "getCatalogSeparator-Methode (SQLServerDatabaseMetaData)"
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
  - SQLServerDatabaseMetaData.getCatalogSeparator
apilocation: 
  - sqljdbc.jar
apitype: Assembly
ms.assetid: 0bbd6842-7210-432a-bef4-e15a63f5cc96
caps.latest.revision: 11
caps.handback.revision: 10
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
# getCatalogSeparator-Methode (SQLServerDatabaseMetaData)
  Ruft den **String** ab, der von dieser Datenbank als Trennzeichen zwischen einem Katalog\- und Tabellennamen verwendet wird.  
  
## Syntax  
  
```  
  
public java.lang.String getCatalogSeparator()  
```  
  
## Rückgabewert  
 Ein **String** mit dem Katalogtrennzeichen.  
  
## Ausnahmen  
 [SQLServerException](../content/SQLServerException-Class.md)  
  
## Hinweise  
 Diese getCatalogSeparator\-Methode wird von der getCatalogSeparator\-Methode in der java.sql.DatabaseMetaData\-Schnittstelle angegeben.  
  
 Wird [!INCLUDE[jdbcNoVersion](../content/includes/jdbcNoVersion_md.md)] mit einer [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)]\-Datenbank verwendet, wird von dieser Methode ein Punkt \("."\) als Katalogtrennzeichen zurückgegeben.  
  
## Siehe auch  
 [SQLServerDatabaseMetaData-Methoden](../content/SQLServerDatabaseMetaData-Methods.md)   
 [SQLServerDatabaseMetaData-Elemente](../content/SQLServerDatabaseMetaData-Members.md)   
 [SQLServerDatabaseMetaData-Klasse](../content/SQLServerDatabaseMetaData-Class.md)  
  
  