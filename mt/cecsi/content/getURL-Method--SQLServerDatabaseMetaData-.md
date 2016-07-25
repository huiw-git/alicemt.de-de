---
title: "getURL-Methode (SQLServerDatabaseMetaData)"
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
  - SQLServerDatabaseMetaData.getURL
apilocation: 
  - sqljdbc.jar
apitype: Assembly
ms.assetid: fcb66851-db5f-4ae8-b728-d129480b6f42
caps.latest.revision: 20
caps.handback.revision: 19
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
# getURL-Methode (SQLServerDatabaseMetaData)
  Ruft die URL für diese Datenbank ab.  
  
## Syntax  
  
```  
  
public java.lang.String getURL()  
```  
  
## Rückgabewert  
 Ein **String** mit der URL.  
  
## Ausnahmen  
 [SQLServerException](../content/SQLServerException-Class.md)  
  
## Hinweise  
 Diese getURL\-Methode wird von der getURL\-Methode in der java.sql.DatabaseMetaData\-Schnittstelle angegeben.  
  
 Wird [!INCLUDE[jdbcNoVersion](../content/includes/jdbcNoVersion_md.md)] mit einer [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)]\-Datenbank verwendet, wird von dieser Methode ein **String**\-Wert mit den folgenden Informationen zurückgegeben:  
  
-   URL\-Wert "jdbc:sqlserver:\/\/"  
  
-   Optionale Verbindungseigenschaften wie **serverName**, **instanceName** und **portNumber**  
  
-   Andere, vom Benutzer festgelegte Verbindungseigenschaften sowie alle Verbindungseigenschaften mit Treiberstandardwerten, die nicht leer und nicht NULL sind \(mit Ausnahme von **userName**, **password** und **integratedSecurity**\)  
  
## Siehe auch  
 [SQLServerDatabaseMetaData-Methoden](../content/SQLServerDatabaseMetaData-Methods.md)   
 [SQLServerDatabaseMetaData-Elemente](../content/SQLServerDatabaseMetaData-Members.md)   
 [SQLServerDatabaseMetaData-Klasse](../content/SQLServerDatabaseMetaData-Class.md)  
  
  