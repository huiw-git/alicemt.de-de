---
title: "ISQLServerConnection-Schnittstelle"
ms.custom: na
ms.date: 07/27/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - drivers
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 031c01e2-2c65-4fe4-9700-fdbcc7a39f30
caps.latest.revision: 9
caps.handback.revision: 8
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
# ISQLServerConnection-Schnittstelle
  Stellt eine JDBC\-Verbindung mit einer [!INCLUDE[msCoName](../content/includes/msCoName_md.md)][!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)]\-Datenbank dar. Die Schnittstelle wurde in [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] JDBC Driver 3.0 hinzugefügt.  
  
 **Paket:** com.microsoft.sqlserver.jdbc  
  
 **Erweitert:** java.sql.Connection  
  
## Syntax  
  
```  
  
public interface ISQLServerConnection  
```  
  
## Hinweise  
 Diese Schnittstelle wird durch [SQLServerConnection-Klasse](../content/SQLServerConnection-Class.md) implementiert.  
  
 Diese Schnittstelle legt das folgende [!INCLUDE[jdbcNoVersion](../content/includes/jdbcNoVersion_md.md)]\-spezifische Feld dar:  
  
|Feld|Weitere Informationen finden Sie unter|  
|----------|--------------------------------------------|  
|öffentliches final static int TRANSACTION\_SNAPSHOT|[TRANSACTION\_SNAPSHOT](../content/TRANSACTION_SNAPSHOT-Field--SQLServerConnection-.md)|  
|öffentliche UUID getClientConnectionId\(\)|[getClientConnectionID\(\)](../content/getClientConnectionID-Method--SQLServerConnection-.md)|  
  
## Siehe auch  
 [API-Referenz für den JDBC-Treiber](../content/JDBC-Driver-API-Reference.md)  
  
  