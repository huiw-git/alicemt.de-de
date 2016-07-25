---
title: "setTime-Methode (int, java.sql.Time)"
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
  - SQLServerPreparedStatement.setTime (int, java.sql.Time)
apilocation: 
  - sqljdbc.jar
apitype: Assembly
ms.assetid: 1e3878dc-42fe-4fac-8fe3-22a7bd70c6da
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
# setTime-Methode (int, java.sql.Time)
    
## setTime\-Methode \(int, java.sql.Time\)  
 Legt den angegebenen Parameter auf den angegebenen Zeitwert fest.  
  
## Syntax  
  
```  
  
public final void setTime(int n,  
                          java.sql.Time x)  
```  
  
#### Parameter  
 *n*  
  
 Ein Wert vom Typ **int** zum Angeben der Parameternummer.  
  
 *x*  
  
 Ein Time\-Objekt.  
  
## Ausnahmen  
 [SQLServerException](../content/SQLServerException-Class.md)  
  
## Hinweise  
 Die setTime\-Methode wird von der setTime\-Methode in der java.sql.PreparedStatement\-Schnittstelle angegeben.  
  
 Ab [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] JDBC Driver 3.0 wird das Verhalten der Methode durch die **sendTimeAsDatetime**\-Verbindungseigenschaft \([Einstellen der Verbindungseigenschaften](../content/Setting-the-Connection-Properties.md)\) und [SQLServerDataSource.setSendTimeAsDatetime](../content/setSendTimeAsDatetime-Method--SQLServerDataSource-.md) geändert.  
  
 Weitere Informationen finden Sie unter [Konfigurieren der Art und Weise, wie java.sql.Time-Werte an den Server gesendet werden](../content/Configuring-How-java.sql.Time-Values-are-Sent-to-the-Server.md).  
  
## Siehe auch  
 [setTime-Methode &#40;ISQLServerPreparedStatement&#41;](../content/setTime-Method--SQLServerPreparedStatement-.md)   
 [SQLServerPreparedStatement-Elemente](../content/SQLServerPreparedStatement-Members.md)   
 [SQLServerPreparedStatement-Klasse](../content/SQLServerPreparedStatement-Class.md)  
  
  