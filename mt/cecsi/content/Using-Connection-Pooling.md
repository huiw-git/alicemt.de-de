---
title: "Verwenden von Verbindungspools"
ms.custom: na
ms.date: 07/01/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - drivers
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 699d4e8a-34bf-4c60-b0d5-4a10dad6084a
caps.latest.revision: 30
caps.handback.revision: 29
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
# Verwenden von Verbindungspools
  [!INCLUDE[jdbcNoVersion](../content/includes/jdbcNoVersion_md.md)] unterstützt Verbindungspoolfunktionen der Java\-Plattform, Enterprise Edition \(Java EE\). Der JDBC\-Treiber implementiert die erforderlichen JDBC 3.0\-Schnittstellen, damit der Treiber Verbindungspoolimplementierungen von Middlewareherstellern nutzen kann. Der JDBC\-Treiber ist JDBC 3.0\-kompatibel. Middleware wie Java EE\-Anwendungsserver bieten häufig kompatible Verbindungspoolfunktionen. Der JDBC\-Treiber nutzt in diesen Umgebungen Verbindungspools.  
  
> [!NOTE]  
>  Obwohl der JDBC\-Treiber Java EE\-Verbindungspools unterstützt, stellt er keine eigene Poolimplementierung bereit. Der Treiber benötigt Java\-Anwendungsserver eines Drittanbieters zum Verwalten der Verbindungen.  
  
## Hinweise  
 Für die Verbindungspoolimplementierung stehen die folgenden Klassen zur Verfügung.  
  
|Class|Implementiert|Beschreibung|  
|-----------|-------------------|------------------|  
|com.microsoft.sqlserver.jdbc.SQLServerXADataSource|javax.sql.ConnectionPoolDataSource und javax.sql.XADataSource|Sie sollten für alle erforderlichen Java EE\-Serverfunktionen die [SQLServerXADataSource](../content/SQLServerXADataSource-Class.md)\-Klasse verwenden, da sie alle JDBC 3.0\-Poolfunktionen und XA\-Schnittstellen implementiert.|  
|com.microsoft.sqlserver.jdbc.SQLServerConnectionPoolDataSource|javax.sql.ConnectionPoolDataSource|Bei dieser Klasse handelt es sich um ein Verbindungsfactory, das es dem Java EE\-Anwendungsserver ermöglicht, den Verbindungspool mit physischen Verbindungen zu füllen. Wenn die Konfiguration des Java EE\-Herstellers eine Klasse erfordert, die javax.sql.ConnectionPoolDataSource implementiert, geben Sie den Klassennamen als [SQLServerConnectionPoolDataSource](../content/SQLServerConnectionPoolDataSource-Class.md) an. Sie sollten stattdessen im Allgemeinen die [SQLServerXADataSource](../content/SQLServerXADataSource-Class.md)\-Klasse verwenden, da sie sowohl Poolfunktionen als auch XA\-Schnittstellen implementiert und in einer größeren Zahl von Java EE\-Serverkonfigurationen überprüft wurde.|  
  
 Der JDBC\-Anwendungscode sollte die Verbindungen immer explizit schließen, damit die Pools optimal genutzt werden können. Wenn die Anwendung eine Verbindung explizit schließt, kann die Poolimplementierung die Verbindung sofort wiederverwenden kann. Wenn die Verbindung nicht geschlossen wird, kann sie von anderen Anwendungen nicht wiederverwendet werden. Die Anwendungen können im  `finally` \-Konstrukt sicherstellen, dass Poolverbindungen auch beim Auftreten von Fehlern geschlossen werden.  
  
> [!NOTE]  
>  Der JDBC\-Treiber ruft zurzeit nicht die gespeicherte Prozedur "sp\_reset\_connection" auf, wenn die Verbindung an den Pool zurückgegeben wird. Der Treiber geht stattdessen davon aus, dass die Java\-Anwendungsserver der Drittanbieter die Verbindungen wieder in den ursprünglichen Status zurück versetzen.  
  
## Siehe auch  
 [Verbinden von SQL Server mit dem JDBC-Treiber](../content/Connecting-to-SQL-Server-with-the-JDBC-Driver.md)  
  
  