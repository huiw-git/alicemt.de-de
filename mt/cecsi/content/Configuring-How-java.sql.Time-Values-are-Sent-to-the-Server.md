---
title: "Konfigurieren der Art und Weise, wie java.sql.Time-Werte an den Server gesendet werden"
ms.custom: na
ms.date: 07/27/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - drivers
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 07eb00dd-621a-46f9-a5a5-8cab4d6058b5
caps.latest.revision: 18
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
# Konfigurieren der Art und Weise, wie java.sql.Time-Werte an den Server gesendet werden
  Wenn Sie ein java.sql.Time\-Objekt oder den java.sql.Types.TIME\-JDBC\-Typ zum Festlegen eines Parameters verwenden, können Sie konfigurieren, wie der java.sql.Time\-Wert an den Server gesendet wird: als [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)]**time**\- oder als **datetime**\-Typ.  
  
 Dies trifft zu, wenn eine der folgenden Methoden verwendet wird:  
  
-   [SQLServerCallableStatement.registerOutParameter\(int, int\)](../content/registerOutParameter-Method--int--int-.md)  
  
-   [SQLServerCallableStatement.registerOutParameter\(int, int, int\)](../content/registerOutParameter-Method--int--int--int-.md)  
  
-   [SQLServerCallableStatement.setTime](../content/setTime-Method--SQLServerCallableStatement-.md)  
  
-   [SQLServerPreparedStatement.setTime](../content/setTime-Method--SQLServerPreparedStatement-.md)  
  
-   [SQLServerCallableStatement.setObject](../content/setObject-Method--SQLServerCallableStatement-.md)  
  
-   [SQLServerPreparedStatement.setObject](../content/setObject-Method--SQLServerPreparedStatement-.md)  
  
 Verwenden Sie die **sendTimeAsDatetime**\-Verbindungseigenschaft, um die Art und Weise zu konfigurieren, auf die der java.sql.Time\-Wert gesendet wird. Weitere Informationen finden Sie unter [Einstellen der Verbindungseigenschaften](../content/Setting-the-Connection-Properties.md).  
  
 Der Wert der **sendTimeAsDatetime**\-Verbindungseigenschaft kann mit dem [SQLServerDataSource.setSendTimeAsDatetime](../content/setSendTimeAsDatetime-Method--SQLServerDataSource-.md)\-Element geändert werden.  
  
 In den [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)]\-Versionen vor [!INCLUDE[ssKatmai](../content/includes/ssKatmai_md.md)] wurde der **time**\-Datentyp nicht unterstützt, und von Anwendungen, die den java.sql.Time\-Typ verwendeten, wurden java.sql.Time\-Werte entweder als **datetime**\- oder **smalldatetime**\-[!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)]\-Datentypen gespeichert.  
  
 Wenn Sie beim Arbeiten mit java.sql.Time\-Werten die Datentypen **datetime** und **smalldatetime**[!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] verwenden möchten, sollten Sie die Verbindungseigenschaft **sendTimeAsDatetime** auf **true** setzen. Wenn Sie beim Arbeiten mit java.sql.Time\-Werten den Datentyp **time**[!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] verwenden möchten, sollten Sie die Verbindungseigenschaft **sendTimeAsDatetime** auf **false** setzen.  
  
 Wenn Sie ausschließlich java.sql.Time\-Werte in einen Parameter senden, deren Datentyp ebenfalls das Datum speichern kann, unterscheiden sich die Standarddaten je nach dem, ob der java.sql.Time\-Wert als **datetime** \(01.01.1970\)\- oder **time** \(01.01.1900\)\-Wert gesendet wird. Weitere Informationen zu Datenkonvertierungen beim Senden von Daten an [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] finden Sie unter [Verwenden von Datums\- und Uhrzeitangaben](http://go.microsoft.com/fwlink/?LinkID=145211).  
  
 In [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] JDBC Driver 3.0 ist **sendTimeAsDatetime** standardmäßig als „true“ festgelegt. In künftigen Versionen wird die **sendTimeAsDatetime**\-Verbindungseigenschaft ggf. standardmäßig auf "false" festgelegt.  
  
 Gehen Sie wie folgt vor, um zu gewährleisten, dass die Anwendung unabhängig vom Standardwert der **sendTimeAsDatetime**\-Verbindungseigenschaft weiterhin funktioniert:  
  
-   Verwenden Sie den java.sql.Time\-Typ, wenn Sie den **time**\-[!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)]\-Datentyp verwenden.  
  
-   Verwenden Sie den java.sql.Timestamp\-Typ, wenn Sie die **datetime**\-,  **smalldatetime** und **datetime2**\-[!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)]\-Datentypen verwenden.  
  
## Siehe auch  
 [Grundlegendes zu den Datentypen in JDBC Driver](../content/Understanding-the-JDBC-Driver-Data-Types.md)  
  
  