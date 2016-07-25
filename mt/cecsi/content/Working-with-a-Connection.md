---
title: "Arbeiten mit einer Verbindung"
ms.custom: na
ms.date: 07/01/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - drivers
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: cf8ee392-8a10-40a3-ae32-31c7b1efdd04
caps.latest.revision: 22
caps.handback.revision: 21
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
# Arbeiten mit einer Verbindung
  Die folgenden Abschnitte enthalten Beispiele für die verschiedenen Möglichkeiten, um mit der [SQLServerConnection](../content/SQLServerConnection-Class.md)\-Klasse von [!INCLUDE[jdbcNoVersion](../content/includes/jdbcNoVersion_md.md)] eine Verbindung mit einer [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)]\-Datenbank herzustellen.  
  
> [!NOTE]  
>  Wenn beim Herstellen von Verbindungen zu [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] mit dem JDBC\-Treiber Probleme auftreten, finden Sie unter [Behandlung von Verbindungsproblemen](../content/Troubleshooting-Connectivity.md) Vorschläge zum Beheben der Probleme.  
  
## Erstellen einer Verbindung mit der DriverManager\-Klasse  
 Die einfachste Vorgehensweise zum Erstellen einer Verbindung zu einer [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)]\-Datenbank besteht darin, den JDBC\-Treiber zu laden und die getConnection\-Methode der DriverManager\-Klasse aufzurufen, wie im Folgenden dargestellt:  
  
```  
Class.forName("com.microsoft.sqlserver.jdbc.SQLServerDriver");  
String connectionUrl = "jdbc:sqlserver://localhost;database=AdventureWorks;integratedSecurity=true;"  
Connection con = DriverManager.getConnection(connectionUrl);  
```  
  
 Bei diesem Verfahren wird eine Datenbankverbindung mit dem ersten verfügbaren Treiber in der Liste der Treiber erstellt, der erfolgreich eine Verbindung mit der angegebenen URL herstellen kann.  
  
> [!NOTE]  
>  Bei Verwendung der sqljdbc4.jar\-Klassenbibliothek brauchen Anwendungen den Treiber nicht mit der Class.forName\-Methode explizit registriert oder geladen werden. Wenn die getConnection\-Methode der DriverManager\-Klasse aufgerufen wird, wird aus der Gruppe der registrierten JDBC\-Treiber ein geeigneter Treiber ausgewählt. Weitere Informationen finden Sie unter "Verwenden des JDBC\-Treibers".  
  
## Erstellen einer Verbindung mit der SQLServerDriver\-Klasse  
 Wenn Sie in der Liste der Treiber für DriverManager einen bestimmten Treiber angeben müssen, können Sie eine Datenbankverbindung mit der [connect](../content/connect-Method--SQLServerDriver-.md)\-Methode der [SQLServerDriver](../content/SQLServerDriver-Class.md)\-Klasse erstellen, wie im Folgenden dargestellt:  
  
```  
Driver d = (Driver) Class.forName("com.microsoft.sqlserver.jdbc.SQLServerDriver").newInstance();  
String connectionUrl = "jdbc:sqlserver://localhost;database=AdventureWorks;integratedSecurity=true;"  
Connection con = d.connect(connectionUrl, new Properties());  
```  
  
## Erstellen einer Verbindung mit der SQLServerDataSource\-Klasse  
 Wenn Sie eine Verbindung mit der [SQLServerDataSource](../content/SQLServerDataSource-Class.md)\-Klasse erstellen müssen, können Sie verschiedene Festlegungsmethoden der Klasse verwenden, bevor Sie die [getConnection](../content/getConnection-Method---.md)\-Methode aufrufen, wie z. B.:  
  
```  
SQLServerDataSource ds = new SQLServerDataSource();  
ds.setUser("MyUserName");  
ds.setPassword("*****");  
ds.setServerName("localhost");  
ds.setPortNumber(1433);   
ds.setDatabaseName("AdventureWorks");  
Connection con = ds.getConnection();  
```  
  
## Erstellen einer Verbindung mit eine sehr speziellen Datenquelle als Ziel  
 Wenn Sie eine Datenbankverbindung mit einer sehr speziellen Datenquelle herstellen müssen, können Sie mehrere Verfahren verwenden. Das jeweilige Verfahren hängt von den Eigenschaften ab, die Sie mit der Verbindungs\-URL festlegen.  
  
 Um eine Verbindung zur Standardinstanz auf einem Remoteserver herzustellen, verwenden Sie die folgende URL:  
  
 `String url = "jdbc:sqlserver://MyServer;integratedSecurity=true;"`  
  
 Um eine Verbindung zu einem bestimmten Port eines Servers herzustellen, verwenden Sie die folgende URL:  
  
 `String url = "jdbc:sqlserver://MyServer:1533;integratedSecurity=true;"`  
  
 Um eine Verbindung zu einer benannten Instanz eines Servers herzustellen, verwenden Sie die folgende URL:  
  
 `String url = "jdbc:sqlserver://209.196.43.19;instanceName=INSTANCE1;integratedSecurity=true;"`  
  
 Um eine Verbindung zu einer bestimmten Datenbank eines Servers herzustellen, verwenden Sie die folgende URL:  
  
 `String url = "jdbc:sqlserver://172.31.255.255;database=AdventureWorks;integratedSecurity=true;"`  
  
 Weitere Beispiele für Verbindungs\-URLs finden Sie unter [Erstellen der Verbindungs-URL](../content/Building-the-Connection-URL.md).  
  
## Erstellen einer Verbindung mit einem benutzerdefinierten Anmeldetimeout  
 Wenn Sie Serverlast oder Netzwerkverkehr berücksichtigen müssen, können Sie eine Verbindung mit einem bestimmten Timeoutwert für die Anmeldung in Sekunden erstellen, wie z. B.:  
  
 `String url = "jdbc:sqlserver://MyServer;loginTimeout=90;integratedSecurity=true;"`  
  
## Erstellen einer Verbindung mit Identität auf Anwendungsebene  
 Wenn Sie Protokollierung und Profilerstellung verwenden, müssen Sie die Verbindung mit einer bestimmten Anwendung als Ursprung kennzeichnen, wie z. B.:  
  
 `String url = "jdbc:sqlserver://MyServer;applicationName=MYAPP.EXE;integratedSecurity=true;"`  
  
## Trennen einer Verbindung  
 Sie können durch Aufrufen der [close](../content/close-Method--SQLServerConnection-.md)\-Methode der SQLServerConnection\-Klasse eine Datenbankverbindung explizit schließen, wie im Folgenden dargestellt:  
  
 `con.close();`  
  
 Dadurch werden die vom SQLServerConnection\-Objekt verwendeten Datenbankressourcen freigegeben bzw. die Verbindung in Poolszenarien an den Verbindungspool zurückgegeben.  
  
> [!NOTE]  
>  Durch den Aufruf der close\-Methode wird auch ein Rollback aller anstehenden Transaktionen ausgeführt.  
  
## Siehe auch  
 [Verbinden von SQL Server mit dem JDBC-Treiber](../content/Connecting-to-SQL-Server-with-the-JDBC-Driver.md)  
  
  