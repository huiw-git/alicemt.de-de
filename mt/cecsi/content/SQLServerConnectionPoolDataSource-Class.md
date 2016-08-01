---
title: "SQLServerConnectionPoolDataSource-Klasse"
ms.custom: na
ms.date: 07/27/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - drivers
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: b00e5a90-2af7-4d04-8ef8-256183777dcf
caps.latest.revision: 13
caps.handback.revision: 12
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
# SQLServerConnectionPoolDataSource-Klasse
  Stellt die physischen Datenbankverbindungen für Verbindungspool\-Manager dar.  
  
 **Paket:** com.microsoft.sqlserver.jdbc  
  
 **Erweitert:** [SQLServerDataSource](../content/SQLServerDataSource-Class.md)  
  
 **Implementiert:** javax.sql.ConnectionPoolDataSource  
  
## Syntax  
  
```  
  
public class SQLServerConnectionPoolDataSource  
```  
  
## Hinweise  
 SQLServerConnectionPoolDataSource wird üblicherweise in Java Application Server\-Umgebungen verwendet, von denen integrierte Verbindungspools unterstützt werden und zum Bereitstellen physischer Verbindungen eine ConnectionPoolDataSource\-Klasse benötigt wird – beispielsweise Java EE\-Anwendungsserver \(Java Platform Enterprise Edition\), von denen Verbindungspools gemäß der Spezifikation der JDBC 3.0\-API bereitgestellt werden.  
  
## Siehe auch  
 [SQLServerConnectionPoolDataSource-Elemente](../content/SQLServerConnectionPoolDataSource-Members.md)   
 [API-Referenz für den JDBC-Treiber](../content/JDBC-Driver-API-Reference.md)  
  
  