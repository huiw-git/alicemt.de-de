---
title: "Verwenden des JDBC-Treibers"
ms.custom: na
ms.date: 07/27/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - drivers
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 6faaf05b-8b70-4ed2-9b44-eee5897f1cd0
caps.latest.revision: 54
caps.handback.revision: 52
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
# Verwenden des JDBC-Treibers
  Dieser Abschnitt enthält die Schnellstart\-Anleitung zum Herstellen einer einfachen Verbindung mit einer [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)]\-Datenbank mittels [!INCLUDE[jdbcNoVersion](../content/includes/jdbcNoVersion_md.md)]. Bevor Sie eine Verbindung mit einer [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)]\-Datenbank herstellen können, muss zunächst [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] auf Ihrem lokalen Computer oder einem Server und der JDBC\-Treiber auf Ihrem lokalen Computer installiert sein.  
  
## Auswählen der richtigen JAR\-Datei  
 Sowohl der Microsoft JDBC Driver 6.0 \(Vorschau\) als auch 4.2 für SQL Server enthalten die JAR\-Klassenbibliotheken **sqljdbc.jar, sqljdbc4.jar, sqljdbc41** und **sqljdbc42.jar** zur Verfügung, die sich je nach Ihren bevorzugten JRE\-Einstellungen verwenden lassen.  
  
 Microsoft JDBC\-Treiber für SQL Server 4.1 enthält die Klassenbibliotheksdateien **sqljdbc.jar**, **sqljdbc4.jar** und **sqljdbc41.jar** für die jeweilige Verwendung mit den bevorzugten JRE \(Java Runtime Environment\)\-Einstellungen.  
  
 Der [!INCLUDE[jdbcNoVersion](../content/includes/jdbcNoVersion_md.md)] 4.0 enthält die Klassenbibliotheksdateien **sqljdbc.jar** und **sqljdbc4.jar** für die jeweilige Verwendung mit Ihren bevorzugten JRE \(Java Runtime Environment\)\-Einstellungen.  
  
 Ihre Auswahl entscheidet auch über die verfügbaren Funktionen. Weitere Informationen zum Auswählen der richtigen JAR\-Datei finden Sie unter [Systemanforderungen für den JDBC-Treiber](../content/System-Requirements-for-the-JDBC-Driver.md).  
  
## Festlegen des Klassenpfads  
 Der JDBC\-Treiber ist kein Bestandteil des Java SDK. Wenn Sie ihn verwenden möchten, müssen Sie den Klassenpfad so festlegen, dass die Datei **sqljdbc.jar**, **sqljdbc4.jar**, **sqljdbc41.jar** oder **sqljdbc42.jar** eingeschlossen ist. Wenn die Angabe des Klassenpfads fehlt, gibt die Anwendung die allgemeine Ausnahme „Klasse nicht gefunden“ aus.  
  
 Die JAR\-Datei sqljdbc.jar file, sqljdbc4.jar file, sqljdbc41.jar oder sqljdbc42.jar wird an folgendem Speicherorten installiert.  
  
 \<*installationsverzeichnis*\>\\sqljdbc\_\<*version*\>\\\<*sprache*\>\\sqljdbc.jar  
  
 \<*Installationsverzeichnis directory*\>\\sqljdbc\_\<*version*\>\\\<*language*\>\\sqljdbc4.jar  
  
 \<*Installationsverzeichnis*\> \\sqljdbc\_ \<*Version*\> \\ \<*Sprache*\> \\sqljdbc41.jar  
  
 \<*Installationsverzeichnis*\> \\sqljdbc\_ \<*Version*\> \\ \<*Sprache*\> \\sqljdbc42.jar  
  
 Für eine Windows\-Anwendung wird beispielsweise die folgende KLASSENPFAD\-Anweisung verwendet:  
  
 `CLASSPATH =.;C:\Program Files\Microsoft JDBC Driver 6.0 for SQL Server\sqljdbc_4.2\enu\sqljdbc42.jar`  
  
 Für eine Unix\-\/Linux\-Anwendung wird beispielsweise die folgende KLASSENPFAD\-Anweisung verwendet:  
  
 `CLASSPATH =.:/home/usr1/mssqlserverjdbc/Driver/sqljdbc_4.2/enu/sqljdbc42.jar`  
  
 Sie müssen sicherstellen, dass die KLASSENPFAD\-Anweisung nur einen [!INCLUDE[jdbcNoVersion](../content/includes/jdbcNoVersion_md.md)] enthält, beispielsweise sqljdbc4.jar enthält, sqljdbc41.jar oder sqljdbc42.jar.  
  
> [!NOTE]  
>  Auf Windows\-Systemen können Verzeichnisnamen, die länger als die 8.3\-Namenskonvention sind, oder Ordnernamen mit Leerzeichen zu Problemen bei Klassenpfaden führen. Wenn Sie ein derartiges Problem vermuten, sollten Sie die Datei „sqljdbc.jar“, „sqljdbc4.jar“ oder „sqljdbc41.jar“ vorübergehend in ein Verzeichnis mit einem einfachen Namen wie  `C:\Temp` verschieben, den Klassenpfad ändern und prüfen, ob das Problem dadurch behoben wurde.  
  
### Anwendungen, die direkt an der Eingabeaufforderung ausgeführt werden  
 Der Klassenpfad wird im Betriebssystem konfiguriert. Fügen Sie dem Klassenpfad des Systems „sqljdbc.jar“ oder „sqljdbc4.jar“ hinzu. Alternativ können Sie den Klassenpfad in der Java\-Befehlszeile, mit der die Anwendung ausgeführt wird, mit der Option  `java -classpath`  angeben.  
  
### Anwendungen, die in einer IDE ausgeführt werden  
 Jeder IDE\-Hersteller verwendet eine andere Methode, um den Klassenpfad in seiner IDE festzulegen.  Es reicht jedoch nicht aus, den Klassenpfad lediglich im Betriebssystem festzulegen. Fügen Sie dem IDE\-Klassenpfad „sqljdbc.jar“, „sqljdbc4.jar“ oder „sqljdbc41.jar“ hinzu.  
  
### Servlets und JSPs  
 Servlets und JSPs werden in einem Servlet\-\/JSP\-Modul wie Tomcat ausgeführt. Der Klassenpfad muss, wie in der Dokumentation für das Servlet\-\/JSP\-Modul angegeben, festgelegt werden. Es reicht jedoch nicht aus, den Klassenpfad lediglich im Betriebssystem festzulegen. Einige Servlet\-\/JSP\-Module verfügen über Setupfenster, in denen Sie den Klassenpfad des Moduls festlegen können.  In dieser Situation müssen Sie dem jeweiligen Klassenpfad des Moduls anhängen die richtige JAR\-Datei für den JDBC\-Treiber hinzufügen und das Modul neu starten.  In anderen Situationen können Sie den Treiber bereitstellen, indem Sie „sqljdbc.jar“, „sqljdbc4.jar“ oder „sqljdbc41.jar“ bei der Modulinstallation in ein bestimmtes Verzeichnis wie z. B. „lib“ kopieren. Der Klassenpfad für den Modultreiber kann auch in einer modulspezifischen Konfigurationsdatei angegeben werden.  
  
### Enterprise Java Beans  
 Enterprise Java Beans \(EJB\) werden in einem EJB\-Container ausgeführt. EJB\-Container sind von verschiedenen Herstellern erhältlich. Java\-Applets werden in einem Browser ausgeführt, aber von einem Webserver heruntergeladen. Kopieren Sie „sqljdbc.jar“, „sqljdbc4.jar“ oder „sqljdbc41.jar“ in das Stammverzeichnis des Webservers und geben Sie den Namen der JAR\-Datei auf der HTML\-Archivregisterkarte des Applets an. Dies kann z. B. in der Form `<applet ... archive=sqljdbc.jar>` erfolgen.  
  
## Herstellen einer einfachen Verbindung mit einer Datenbank  
 Mithilfe der sqljdbc.jar\-Klassenbibliothek müssen Anwendungen zuerst den Treiber wie folgt zu registrieren:  
  
 `Class.forName("com.microsoft.sqlserver.jdbc.SQLServerDriver");`  
  
 Sobald der Treiber geladen wurde, können Sie die Verbindung mittels einer Verbindungs\-URL und der getConnection\-Methode der DriverManager\-Klasse einrichten:  
  
```  
String connectionUrl = "jdbc:sqlserver://localhost:1433;" + "databaseName=AdventureWorks;user=MyUserName;password=*****;"; Connection con = DriverManager.getConnection(connectionUrl);  
```  
  
 In der JDBC\-4.0\-API wurde die DriverManager.getConnection Methode verbessert, um die JDBC\-Treiber automatisch zu laden. Daher müssen Anwendungen die Class.forName\-Methode bei Verwendung der sqljdbc4.jar\-, sqljdbc41.jar\-oder sqljdbc42.jar\-Klassenbibliothek nicht aufrufen, um den Treiber zu registrieren oder zu laden.  
  
 Wenn die getConnection\-Methode der DriverManager\-Klasse aufgerufen wird, erfolgt aus der Gruppe der registrierten JDBC\-Treiber eine geeignete Auswahl getroffen. „sqljdbc4.jar“, „sqljdbc41.jar“ oder „sqljdbc42.jar“ enthalten die Datei „META\-INF\/services\/java.sql.Driver“, die den **com.microsoft.sqlserver.jdbc.SQLServerDriver** als registrierten Treiber enthält. Die vorhandenen Anwendungen, die  die Treiber aktuell mittels der Class.forName\-Methode laden, funktionieren ohne zusätzliche Änderungen weiter.  
  
> [!NOTE]  
>  Die Klassenbibliothek „sqljdbc4.jar“, „sqljdbc41.jar“ oder „sqljdbc42.jar“ kann nicht mit älteren Versionen von Java Runtime Environment \(JRE\) verwendet werden. Unter [Systemanforderungen für den JDBC-Treiber](../content/System-Requirements-for-the-JDBC-Driver.md) finden Sie eine Liste mit JRE\-Versionen, die [!INCLUDE[jdbcNoVersion](../content/includes/jdbcNoVersion_md.md)] unterstützt.  
  
 Weiterführende Informationen zum Herstellen von Verbindungen mit Datenquellen und zur Verwendung einer Verbindungs\-URL finden Sie unter [Erstellen der Verbindungs-URL](../content/Building-the-Connection-URL.md) und [Einstellen der Verbindungseigenschaften](../content/Setting-the-Connection-Properties.md).  
  
## Siehe auch  
 [Übersicht über den JDBC-Treiber](../content/Overview-of-the-JDBC-Driver.md)  
  
  