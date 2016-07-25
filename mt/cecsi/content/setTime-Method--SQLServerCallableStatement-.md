---
title: "setTime-Methode (SQLServerCallableStatement)"
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
  - SQLServerCallableStatement.setTime
apilocation: 
  - sqljdbc.jar
apitype: Assembly
ms.assetid: 04ea83b2-db5e-4b46-b016-9e496363827e
caps.latest.revision: 18
caps.handback.revision: 17
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
# setTime-Methode (SQLServerCallableStatement)
    
## setTime\-Methode \(SQLServerCallableStatement\)  
 Legt den angegebenen Parameter auf den angegebenen Zeitwert fest.  
  
 Ab [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] JDBC Driver 3.0 wird das Verhalten der Methode durch die **sendTimeAsDatetime**\-Verbindungseigenschaft \([Einstellen der Verbindungseigenschaften](../content/Setting-the-Connection-Properties.md)\) und [SQLServerDataSource.setSendTimeAsDatetime](../content/setSendTimeAsDatetime-Method--SQLServerDataSource-.md) geändert.  
  
 Weitere Informationen finden Sie unter [Konfigurieren der Art und Weise, wie java.sql.Time-Werte an den Server gesendet werden](../content/Configuring-How-java.sql.Time-Values-are-Sent-to-the-Server.md).  
  
### Überladungsliste  
  
|Name|Beschreibung|  
|----------|------------------|  
|[setTime \(java.lang.String, java.sql.Time\)](../content/setTime-Method--java.lang.String--java.sql.Time-.md)|Legt den angegebenen Parameter auf den angegebenen Zeitwert fest.|  
|[setTime \(java.lang.String, java.sql.Time, java.util.Calendar\)](../content/setTime-Method--java.lang.String--java.sql.Time--java.util.Calendar-.md)|Legt den angegebenen Parameter auf die angegebenen Zeit\- und Kalenderwerte fest.|  
  
## Siehe auch  
 [SQLServerCallableStatement-Methoden](../content/SQLServerCallableStatement-Methods.md)   
 [SQLServerCallableStatement-Klasse](../content/SQLServerCallableStatement-Class.md)  
  
  