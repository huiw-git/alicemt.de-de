---
title: "ISQLServerStatement-Schnittstelle"
ms.custom: na
ms.date: 07/27/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - drivers
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 7f83b514-6e76-4f37-baf3-a10db2010e7c
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
# ISQLServerStatement-Schnittstelle
  Stellt die grundlegende Implementierung der JDBC\-Anweisungsfunktion dar. Die Schnittstelle wurde in [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] JDBC Driver 3.0 hinzugefügt.  
  
 **Paket:** com.microsoft.sqlserver.jdbc  
  
 **Erweitert:** java.sql.Statement  
  
## Syntax  
  
```  
  
public interface ISQLServerStatement  
```  
  
## Hinweise  
 Diese Schnittstelle wird durch [SQLServerStatement-Klasse](../content/SQLServerStatement-Class.md) implementiert.  
  
 Diese Schnittstelle legt die folgenden [!INCLUDE[jdbcNoVersion](../content/includes/jdbcNoVersion_md.md)]\-spezifischen Methoden dar:  
  
|Methode|Weitere Informationen finden Sie unter|  
|-------------|--------------------------------------------|  
|öffentliche Zeichenfolge getResponseBuffering|[getResponseBuffering](../content/getResponseBuffering-Method--SQLServerStatement-.md)|  
|öffentliches void setResponseBuffering|[setResponseBuffering](../content/setResponseBuffering-Method--SQLServerStatement-.md)|  
  
## Siehe auch  
 [API-Referenz für den JDBC-Treiber](../content/JDBC-Driver-API-Reference.md)  
  
  