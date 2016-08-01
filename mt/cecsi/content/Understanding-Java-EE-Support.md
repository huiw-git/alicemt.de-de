---
title: "Grundlegendes zur Java EE-Unterst&#252;tzung"
ms.custom: na
ms.date: 07/27/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - drivers
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: a9448b80-b7a3-49cf-8bb4-322c73676005
caps.latest.revision: 26
caps.handback.revision: 25
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
# Grundlegendes zur Java EE-Unterst&#252;tzung
  In den folgenden Abschnitten wird dokumentiert, wie [!INCLUDE[jdbcNoVersion](../content/includes/jdbcNoVersion_md.md)] die optionalen API\-Funktionen für die Java\-Plattform, Enterprise Edition \(Java EE\) und JDBC 3.0 unterstützt. Die Quellcodebeispiele in diesem Hilfesystem stellen eine gute Referenz für erste Schritte mit diesen Funktionen dar.  
  
 Stellen Sie zunächst sicher, dass die Java\-Umgebung \(JDK, JRE\) das Paket javax.sql einschließt. Dies ist ein erforderliches Paket für alle JDBC\-Anwendungen, die die optionale API verwenden. JDK 1.5 und höhere Versionen umfassen dieses Paket bereits, sodass Sie es nicht separat installieren müssen.  
  
## Treibername  
 Der Treiberklassenname lautet **com.microsoft.sqlserver.jdbc.SQLServerDriver**. Der Treiber ist in der Datei "sqljdbc.jar", "sqljdb4.jar", "sqljdbc41.jar" oder "sqljdbc42.jar" enthalten.  
  
 Der Klassenname wird immer dann verwendet, wenn Sie den Treiber mit der JDBC\-Klasse DriverManager laden. Er wird außerdem verwendet, wenn Sie den Klassennamen des Treibers in einer Treiberkonfiguration angeben müssen. Für das Konfigurieren einer Datenquelle in einem Java EE\-Anwendungsserver kann es beispielsweise erforderlich sein, den Treiberklassennamen einzugeben.  
  
## Datenquellen  
 Der JDBC\-Treiber unterstützt Java EE\-\/JDBC 3.0\-Datenquellen. Die [SQLServerXADataSource](../content/SQLServerXADataSource-Class.md)\-Klasse des JDBC\-Treibers wird von **com.microsoft.sqlserver.jdbc.SQLServerXADataSource** implementiert.  
  
### Datenquellennamen  
 Sie können Datenbankverbindungen mithilfe von Datenquellen herstellen. Die mit dem JDBC\-Treiber verfügbaren Datenquellen werden in der folgenden Tabelle beschrieben:  
  
|DataSource\-Typ|Klassenname|Beschreibung|  
|---------------------|-----------------|------------------|  
|DataSource|com.microsoft.sqlserver.jdbc.SQLServerDataSource|Die Datenquelle ohne Pooling.|  
|ConnectionPoolDataSource|com.microsoft.sqlserver.jdbc.SQLServerConnectionPoolDataSource|Die Datenquelle zum Konfigurieren von Verbindungspools für Java EE\-Anwendungsserver. Wird normalerweise verwendet, wenn die Anwendung innerhalb eines Java EE\-Anwendungsservers ausgeführt wird.|  
|XADataSource|com.microsoft.sqlserver.jdbc.SQLServerXADataSource|Die Datenquelle zum Konfigurieren von Java EE\-XA\-Datenquellen. Wird normalerweise verwendet, wenn die Anwendung innerhalb eines Java EE\-Anwendungsservers und eines XA\-Transaktionsmanagers ausgeführt wird.|  
  
### Datenquelleneigenschaften  
 Alle Datenquellen unterstützen die Möglichkeit zum Festlegen und Abrufen aller Eigenschaften, die dem Eigenschaftenset des zugrunde liegenden Treibers zugeordnet sind.  
  
 Beispiele:  
  
 `setServerName("localhost");`  
  
 `setDatabaseName("AdventureWorks");`  
  
 Im Folgenden wird veranschaulicht, wie eine Anwendung mit einer Datenquelle eine Verbindung herstellt:  
  
```  
initialize JNDI ..  
Context ctx = new InitialContext(System.getProperties());  
...  
DataSource ds = (DataSource) ctx.lookup("MyDataSource");  
Connection c = ds.getConnection("user", "pwd");  
```  
  
 Weitere Informationen zu den Datenquelleneigenschaften finden Sie unter [Festlegen von Datenquelleneigenschaften](../content/Setting-the-Data-Source-Properties.md).  
  
## Siehe auch  
 [Übersicht über den JDBC-Treiber](../content/Overview-of-the-JDBC-Driver.md)  
  
  