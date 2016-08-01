---
title: "setTime-Methode (ISQLServerPreparedStatement)"
ms.custom: na
ms.date: 07/27/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - drivers
ms.tgt_pltfrm: na
ms.topic: article
apiname: 
  - SQLServerPreparedStatement.setTime
apilocation: 
  - sqljdbc.jar
apitype: Assembly
ms.assetid: b3a83ea3-6636-4096-842b-71b37340fa07
caps.latest.revision: 17
caps.handback.revision: 16
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
# setTime-Methode (ISQLServerPreparedStatement)
    
## setTime\-Methode \(ISQLServerPreparedStatement\)  
 Legt den angegebenen Parameter auf den angegebenen Zeitwert fest.  
  
 Ab [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] JDBC Driver 3.0 wird das Verhalten der Methode durch die **sendTimeAsDatetime**\-Verbindungseigenschaft \([Einstellen der Verbindungseigenschaften](../content/Setting-the-Connection-Properties.md)\) und [SQLServerDataSource.setSendTimeAsDatetime](../content/setSendTimeAsDatetime-Method--SQLServerDataSource-.md) geändert.  
  
 Weitere Informationen finden Sie unter [Konfigurieren der Art und Weise, wie java.sql.Time-Werte an den Server gesendet werden](../content/Configuring-How-java.sql.Time-Values-are-Sent-to-the-Server.md).  
  
### Überladungsliste  
  
|Name|Beschreibung|  
|----------|------------------|  
|[setTime \(int, java.sql.Time\)](../content/setTime-Method--int--java.sql.Time-.md)|Legt den angegebenen Parameter auf den angegebenen Zeitwert fest.|  
|[setTime \(int, java.sql.Time, java.util.Calendar\)](../content/setTime-Method--int--java.sql.Time--java.util.Calendar-.md)|Legt den angegebenen Parameter auf die angegebenen Zeit\- und Kalenderwerte fest.|  
  
## Siehe auch  
 [SQLServerPreparedStatement-Elemente](../content/SQLServerPreparedStatement-Members.md)   
 [SQLServerPreparedStatement-Klasse](../content/SQLServerPreparedStatement-Class.md)  
  
  