---
title: "getIdentifierQuoteString-Methode (SQLServerDatabaseMetaData)"
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
  - SQLServerDatabaseMetaData.getIdentifierQuoteString
apilocation: 
  - sqljdbc.jar
apitype: Assembly
ms.assetid: 6dea35a0-56a8-412c-8cd3-6539527ff597
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
# getIdentifierQuoteString-Methode (SQLServerDatabaseMetaData)
    
## getIdentifierQuoteString\-Methode \(SQLServerDatabaseMetaData\)  
 Ruft den **String** ab, mit dem SQL\-Bezeichner in Anführungszeichen gesetzt werden.  
  
## Syntax  
  
```  
  
public java.lang.String getIdentifierQuoteString()  
```  
  
## Rückgabewert  
 Ein **String** , der die Bezeichner für Anführungszeichen enthält.  
  
## Ausnahmen  
 [SQLServerException](../content/SQLServerException-Class.md)  
  
## Hinweise  
 Diese getIdentifierQuoteString\-Methode wird von der getIdentifierQuoteString\-Methode in der java.sql.DatabaseMetaData\-Schnittstelle angegeben.  
  
 Bei Verwendung von JDBC Driver von [!INCLUDE[msCoName](../content/includes/msCoName_md.md)] mit einer [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)]\-Datenbank werden von dieser Methode **double** Anführungszeichen \(""\) zurückgegeben.  
  
## Siehe auch  
 [SQLServerDatabaseMetaData-Methoden](../content/SQLServerDatabaseMetaData-Methods.md)   
 [SQLServerDatabaseMetaData-Elemente](../content/SQLServerDatabaseMetaData-Members.md)   
 [SQLServerDatabaseMetaData-Klasse](../content/SQLServerDatabaseMetaData-Class.md)  
  
  