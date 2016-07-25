---
title: "setSendTimeAsDatetime-Methode (SQLServerDataSource)"
ms.custom: na
ms.date: 07/01/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - drivers
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 705a0494-b5e2-43db-940a-1b8cec550cdb
caps.latest.revision: 14
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
# setSendTimeAsDatetime-Methode (SQLServerDataSource)
    
## setSendTimeAsDatetime\-Methode \(SQLServerDataSource\)  
 Diese Methode wurde in [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] JDBC Driver 3.0 hinzugefügt.  
  
 Ändert die Einstellung der **sendTimeAsDatetime**\-Verbindungseigenschaft.  
  
## Syntax  
  
```  
  
public void setSendTimeAsDatetime(boolean sendTimeAsDateTime)  
```  
  
#### Parameter  
 *sendTimeAsDateTime*  
  
 Ein boolescher Wert. Wenn "true", werden java.sql.Time\-Werte als [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)]**datetime**\-Typen an den Server gesendet. Wenn "false", werden java.sql.Time\-Werte als [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)]**time**\-Typen an den Server gesendet.  
  
## Hinweise  
 Von [SQLServerDataSource.getSendTimeAsDatetime](../content/getSendTimeAsDatetime-Method--SQLServerDataSource-.md) wird die Einstellung der **sendTimeAsDatetime**\-Verbindungseigenschaft zurückgegeben.  
  
 Weitere Informationen zur **sendTimeAsDatetime**\-Verbindungseigenschaft finden Sie unter [Einstellen der Verbindungseigenschaften](../content/Setting-the-Connection-Properties.md).  
  
 Weitere Informationen finden Sie unter [Konfigurieren der Art und Weise, wie java.sql.Time-Werte an den Server gesendet werden](../content/Configuring-How-java.sql.Time-Values-are-Sent-to-the-Server.md).  
  
## Siehe auch  
 [SQLServerDataSource-Elemente](../content/SQLServerDataSource-Members.md)   
 [SQLServerDataSource-Klasse](../content/SQLServerDataSource-Class.md)  
  
  