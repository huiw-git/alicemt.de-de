---
title: "getSendTimeAsDatetime-Methode (SQLServerDataSource)"
ms.custom: na
ms.date: 07/27/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - drivers
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 02287122-5dc1-455d-987f-95fd9a69d503
caps.latest.revision: 15
caps.handback.revision: 14
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
# getSendTimeAsDatetime-Methode (SQLServerDataSource)
    
## getSendTimeAsDatetime\-Methode \(SQLServerDataSource\)  
 Diese Methode wurde in [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] JDBC Driver 3.0 hinzugefügt.  
  
 Sie gibt die Einstellung der **sendTimeAsDatetime**\-Verbindungseigenschaft zurück.  
  
## Syntax  
  
```  
  
public boolean getSendTimeAsDatetime();  
```  
  
## Rückgabewert  
 **true**, wenn java.sql.Time\-Werte als [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)]\-**datetime**\-Typ an den Server gesendet werden. **false**, wenn java.sql.Time\-Werte als [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)]\-**time**\-Typ an den Server gesendet werden.  
  
## Hinweise  
 Weitere Informationen zur **sendTimeAsDatetime**\-Verbindungseigenschaft finden Sie unter [Einstellen der Verbindungseigenschaften](../content/Setting-the-Connection-Properties.md).  
  
 Mit [SQLServerDataSource.setSendTimeAsDatetime](../content/setSendTimeAsDatetime-Method--SQLServerDataSource-.md) kann die **sendTimeAsDatetime**\-Verbindungseigenschaft programmatisch geändert werden.  
  
 Weitere Informationen finden Sie unter [Konfigurieren der Art und Weise, wie java.sql.Time-Werte an den Server gesendet werden](../content/Configuring-How-java.sql.Time-Values-are-Sent-to-the-Server.md).  
  
## Siehe auch  
 [SQLServerDataSource-Elemente](../content/SQLServerDataSource-Members.md)   
 [SQLServerDataSource-Klasse](../content/SQLServerDataSource-Class.md)  
  
  