---
title: "ISQLServerPreparedStatement-Schnittstelle"
ms.custom: na
ms.date: 07/27/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - drivers
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: cf87892e-5c34-4ac6-8258-c2a81e117b26
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
# ISQLServerPreparedStatement-Schnittstelle
  Stellt die grundlegende Implementierung der JDBC\-Funktion für vorbereitete Anweisungen dar. Die Schnittstelle wurde in [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] JDBC Driver 3.0 hinzugefügt.  
  
 **Paket:** com.microsoft.sqlserver.jdbc  
  
 **erweitert:** java.sql.PreparedStatement, [ISQLServerStatement](../content/ISQLServerStatement-Interface.md)  
  
## Syntax  
  
```  
  
public interface ISQLServerPreparedStatement  
```  
  
## Hinweise  
 Diese Schnittstelle wird durch [SQLServerPreparedStatement-Klasse](../content/SQLServerPreparedStatement-Class.md) implementiert.  
  
 Diese Schnittstelle legt die folgenden [!INCLUDE[jdbcNoVersion](../content/includes/jdbcNoVersion_md.md)]\-spezifischen Methoden dar:  
  
|Methode|Weitere Informationen finden Sie unter|  
|-------------|--------------------------------------------|  
|öffentliche void setDateTimeOffset\(int, microsoft.sql.DateTimeOffset\)|[setDateTimeOffset](../content/setDateTimeOffset-Method--SQLServerPreparedStatement-.md)|  
  
## Siehe auch  
 [API-Referenz für den JDBC-Treiber](../content/JDBC-Driver-API-Reference.md)  
  
  