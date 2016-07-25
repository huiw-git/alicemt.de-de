---
title: "ISQLServerCallableStatement-Schnittstelle"
ms.custom: na
ms.date: 07/01/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - drivers
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 030a1631-cfcd-41e0-beb5-47f93c01e8e0
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
# ISQLServerCallableStatement-Schnittstelle
  Stellt aufrufbare JDBC\-Anweisungen dar. Die Schnittstelle wurde in [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] JDBC Driver 3.0 hinzugefügt.  
  
 **Paket:** com.microsoft.sqlserver.jdbc  
  
 **Erweitert:** java.sql.CallableStatement, [ISQLServerPreparedStatement](../content/ISQLServerPreparedStatement-Interface.md)  
  
## Syntax  
  
```  
  
public interface ISQLServerCallableStatement  
```  
  
## Hinweise  
 Diese Schnittstelle wird durch [SQLServerCallableStatement-Klasse](../content/SQLServerCallableStatement-Class.md) implementiert.  
  
 Diese Schnittstelle legt die folgenden [!INCLUDE[jdbcNoVersion](../content/includes/jdbcNoVersion_md.md)]\-spezifischen Methoden dar:  
  
|Methode|Weitere Informationen finden Sie unter|  
|-------------|--------------------------------------------|  
|microsoft.sql.DateTimeOffset getDateTimeOffset\(int\)|[getDateTimeOffset\(int\)](../content/getDateTimeOffset-Method--int-.md)|  
|microsoft.sql.DateTimeOffset getDateTimeOffset\(String\)|[getDateTimeOffset\(String\)](../content/getDateTimeOffset-Method--String-.md)|  
|void setDateTimeOffset\(String, microsoft.sql.DateTimeOffset\)|[setDateTimeOffset](../content/setDateTimeOffset-Method--SQLServerCallableStatement-.md)|  
  
## Siehe auch  
 [API-Referenz für den JDBC-Treiber](../content/JDBC-Driver-API-Reference.md)  
  
  