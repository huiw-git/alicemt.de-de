---
title: "Erstellen der Verbindungs-URL"
ms.custom: na
ms.date: 07/01/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - drivers
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 44996746-d373-4f59-9863-a8a20bb8024a
caps.latest.revision: 53
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
# Erstellen der Verbindungs-URL
  Die allgemeine Form der Verbindungs\-URL lautet:  
  
 `jdbc:sqlserver://[serverName[\instanceName][:portNumber]][;property=value[;property=value]]`  
  
 Dabei gilt:  
  
-   **jdbc:sqlserver:\/\/** \(erforderlich\) als Subprotokoll bezeichnet wird und konstant ist.  
  
-   **serverName** \(optional\) die Adresse des Servers, darstellt, zu dem eine Verbindung hergestellt werden soll. Dabei kann es sich um eine DNS\- oder IP\-Adresse bzw. "localhost" oder "127.0.0.1" für den lokalen Computer handeln. Wenn der Servername nicht in der Verbindungs\-URL angegeben wird, muss er in der properties\-Auflistung angegeben werden.  
  
-   **instanceName** \(optional\) bezeichnet die Instanz auf "serverName", zu der eine Verbindung hergestellt werden soll. Ohne Angabe wird eine Verbindung zur Standardinstanz erstellt.  
  
-   **portNumber** \(optional\) bezeichnet den Port auf "serverName", zu dem eine Verbindung hergestellt werden soll. Der Standardwert ist "1433". Bei Verwendung des Standardwerts müssen der Port und der vorangestellte Doppelpunkt \(":"\) in der URL nicht angegeben werden.  
  
    > [!NOTE]  
    >  Um eine optimale Leistung der Verbindung zu gewährleisten, sollten Sie "portNumber" festlegen, wenn Sie eine Verbindung zu einer benannten Instanz herstellen. Dadurch werden Roundtrips zum Server vermieden, um die Portnummer zu ermitteln. Wenn "portNumber" und "instanceName" verwendet werden, hat "portNumber" Vorrang und "instanceName" wird ignoriert.  
  
-   **property** \(optional\) ist mindestens eine optionale Verbindungseigenschaft. Weitere Informationen finden Sie unter [Einstellen der Verbindungseigenschaften](../content/Setting-the-Connection-Properties.md). Sie können eine beliebige Eigenschaft aus der Liste angeben. Mehrere Eigenschaften müssen durch ein Semikolon \(';'\) getrennt werden und dürfen nicht doppelt vorkommen.  
  
> [!CAUTION]  
>  Aus Sicherheitsgründen sollten Sie es vermeiden, die Verbindungs\-URLs basierend auf Benutzereingaben zu erstellen. Sie sollten in der URL lediglich Servername und Treiber angeben. Verwenden Sie für Werte von Benutzernamen und Kennwörtern die properties\-Auflistungen für Verbindungen. Weitere Informationen zur Sicherheit in JDBC\-Anwendungen finden Sie unter [Sichern von JDBC-Treiberanwendungen](../content/Securing-JDBC-Driver-Applications.md).  
  
## Verbindungsbeispiele  
 Herstellen einer Verbindung zur Standarddatenbank auf dem lokalen Computer mit Benutzername und Kennwort:  
  
 `jdbc:sqlserver://localhost;user=MyUserName;password=*****;`  
  
> [!NOTE]  
>  Obwohl im vorherigen Beispiel in der Verbindungszeichenfolge ein Benutzername und ein Kennwort verwendet wurden, sollten Sie aufgrund der höheren Sicherheit die integrierte Sicherheit verwenden. Weitere Informationen finden Sie im Abschnitt [Herstellen einer Verbindung mit integrierter Authentifizierung](#Connectingintegrated) weiter unten in diesem Thema.  
  
 Anhand der folgenden Verbindungszeichenfolge wird veranschaulicht, wie Sie von einer Anwendung, die unter einem vom [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] unterstützten Betriebssystem ausgeführt wird, über die integrierte Authentifizierung und Kerberos eine Verbindung mit einer [!INCLUDE[jdbcNoVersion](../content/includes/jdbcNoVersion_md.md)]\-Datenbank herstellen:  
  
```  
jdbc:sqlserver://;servername=server_name;integratedSecurity=true;authenticationScheme=JavaKerberos  
```  
  
 Herstellen einer Verbindung zur Standarddatenbank auf dem lokalen Computer mit integrierter Authentifizierung:  
  
 `jdbc:sqlserver://localhost;integratedSecurity=true;`  
  
 Herstellen einer Verbindung zu einer benannten Datenbank auf einem Remoteserver:  
  
 `jdbc:sqlserver://localhost;databaseName=AdventureWorks;integratedSecurity=true;`  
  
 Herstellen einer Verbindung zum Standardport auf dem Remoteserver:  
  
 `jdbc:sqlserver://localhost:1433;databaseName=AdventureWorks;integratedSecurity=true;`  
  
 Herstellen einer Verbindung mit Angabe eines angepassten Anwendungsnamens:  
  
 `jdbc:sqlserver://localhost;databaseName=AdventureWorks;integratedSecurity=true;applicationName=MyApp;`  
  
## Benannte und mehrere SQL Server\-Instanzen  
 [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] lässt die Installation mehrerer Datenbankinstanzen auf einem Server zu. Jede Instanz wird durch einen bestimmten Namen gekennzeichnet. Um eine Verbindung zu einer benannten Instanz von [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] herzustellen, können Sie entweder die Portnummer der benannten Instanz angeben \(vorzugsweise\) oder den Instanznamen als JDBC\-URL\-Eigenschaft oder **datasource**\-Eigenschaft angeben. Wenn keine Eigenschaft für Instanzname oder Portnummer angegeben wurde, wird eine Verbindung zur Standardinstanz erstellt. Vergleichen Sie die folgenden Beispiele:  
  
 Gehen Sie folgendermaßen vor, wenn eine Portnummer verwendet werden soll:  
  
 `jdbc:sqlserver://localhost:1433;integratedSecurity=true;<more properties as required>;`  
  
 Gehen Sie folgendermaßen vor, wenn eine JDBC\-URL\-Eigenschaft verwendet werden soll:  
  
 `jdbc:sqlserver://localhost;instanceName=instance1;integratedSecurity=true;<more properties as required>;`  
  
## Maskieren von Werten in der Verbindungs\-URL  
 Eventuell müssen Sie bestimmte Teile von Werten der Verbindungs\-URL aufgrund enthaltener Sonderzeichen wie Leerzeichen, Semikolons und Anführungszeichen maskieren. Der JDBC\-Treiber unterstützt die Maskierung dieser Zeichen, indem sie in geschweifte Klammern gesetzt werden. So maskiert {;} beispielsweise ein Semikolon.  
  
 Maskierte Werte können Sonderzeichen enthalten \(insbesondere '\=', ';', '\[\]' und Leerzeichen\), dürfen aber keine geschweiften Klammern enthalten. Werte, die maskiert werden müssen und geschweifte Klammern enthalten, müssen zu einer properties\-Auflistung hinzugefügt werden.  
  
> [!NOTE]  
>  Leerräume innerhalb der Klammern sind literal und werden nicht gekürzt.  
  
##  <a name="Connectingintegrated"></a> Herstellen einer Verbindung mit integrierter Authentifizierung unter Windows  
 Der JDBC\-Treiber unterstützt über die integratedSecurity\-Verbindungszeichenfolgeneigenschaft die Verwendung der integrierten Authentifizierung vom Typ 2 auf Windows\-Betriebssystemen. Wenn Sie die integrierte Authentifizierung verwenden möchten, müssen Sie die Datei „sqljdbc\_auth.dll“ in ein Verzeichnis im Windows\-Systempfad des Computers kopieren, auf dem der JDBC\-Treiber installiert ist.  
  
 Die „sqljdbc\_auth.dll“\-Dateien werden im folgenden Pfad installiert:  
  
 \<*installationsverzeichnis*\>\\sqljdbc\_\<*version*\>\\\<*sprache*\>\\auth\\  
  
 Unter [!INCLUDE[jdbcNoVersion](../content/includes/jdbcNoVersion_md.md)] finden Sie für alle vom [Herstellen von Verbindungen mit SQL Server mit der integrierten Kerberos-Authentifizierung](../content/Using-Kerberos-Integrated-Authentication-to-Connect-to-SQL-Server.md) unterstützten Betriebssysteme eine Beschreibung einer in [!INCLUDE[jdbc_40](../content/includes/jdbc_40_md.md)] eingeführten Funktion, über die eine Anwendung mithilfe der integrierten Kerberos\-Authentifizierung Typ 4 eine Verbindung mit einer Datenbank herstellen kann.  
  
> [!NOTE]  
>  Wenn Sie eine 32\-Bit\-JVM \(Java Virtual Machine\) ausführen, verwenden Sie die Datei „sqljdbc\_auth.dll“ im Ordner „x86“, auch wenn es sich bei dem Betriebssystem um die x64\-Version handelt. Wenn Sie eine 64\-Bit\-JVM mit einem x64\-Prozessor ausführen, verwenden Sie die Datei „sqljdbc\_auth.dll“ im Ordner „x64“.  
  
 Alternativ können Sie mit der java.libary.path\-Systemeigenschaft das Verzeichnis von „sqljdbc\_auth.dll“ angeben. Wenn der JDBC\-Treiber beispielsweise im Standardverzeichnis installiert ist, können Sie den Speicherort der DLL beim Start der Java\-Anwendung mit dem folgenden VM\-Argument \(Virtual Machine\) angeben:  
  
 `-Djava.library.path=C:\Microsoft JDBC Driver 4.0 for SQL Server\sqljdbc_<version>\enu\auth\x86`  
  
## Herstellen von Verbindungen mit IPv6\-Adressen  
 Der JDBC\-Treiber unterstützt die Verwendung von IPv6\-Adressen in der properties\-Auflistung der Verbindung und in der serverName\-Eigenschaft der Verbindungszeichenfolge. Der ursprüngliche serverName\-Werte wie "jdbc:*sqlserver*:\/\/*serverName*" wird in Verbindungszeichenfolgen nicht für IPv6\-Adressen unterstützt. Für *serverName* kann in allen Fällen anstatt einer IPv6\-Adresse problemlos ein Name in der Verbindung verwendet werden. Die folgenden Beispiele enthalten weitere Informationen.  
  
 **So verwenden Sie die serverName\-Eigenschaft:**  
  
 `jdbc:sqlserver://;serverName=3ffe:8311:eeee:f70f:0:5eae:10.203.31.9\\instance1;integratedSecurity=true;`  
  
 **So verwenden Sie die properties\-Auflistung:**  
  
 `Properties pro = new Properties();`  
  
 `pro.setProperty("serverName", "serverName=3ffe:8311:eeee:f70f:0:5eae:10.203.31.9\\instance1");`  
  
 `Connection con = DriverManager.getConnection("jdbc:sqlserver://;integratedSecurity=true;", pro);`  
  
## Siehe auch  
 [Verbinden von SQL Server mit dem JDBC-Treiber](../content/Connecting-to-SQL-Server-with-the-JDBC-Driver.md)  
  
  