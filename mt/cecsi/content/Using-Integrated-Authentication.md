---
title: "Nutzung der Integrierten Authentifizierung"
ms.custom: na
ms.date: 06/09/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - drivers
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 9499ffdf-e0ee-4d3c-8bca-605371eb52d9
caps.latest.revision: 23
caps.handback.revision: 22
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
  - zh-cn
  - zh-tw
---
# Nutzung der Integrierten Authentifizierung
Der [!INCLUDE[msCoName](../content/includes/msCoName_md.md)]ODBC\-Treiber für [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] unter Linux unterstützt Verbindungen, die eine Kerberos\-integrierte Authentifizierung verwenden Der ODBC\-Treiber unter Linux unterstützt das MIT Kerberos Key Distribution Center \(KDC\) und funktioniert mit der Generic Security Services Anwendungsprogramm\-Schnittstelle \(GSSAPI\) und mit Kerberos\-Bibliotheken.  
  
## Mithilfe der integrierten Authentifizierung eine Verbindung zu [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] aus einer ODBC\-Anwendung herstellen  
Sie können Kerberos Windows integrierte Authentifizierung aktivieren, indem Sie **Trusted\_Connection\=yes** in der Verbindungszeichenfolge des **SQLDriverConnect** oder **SQLConnect** angeben. Zum Beispiel:  
  
```  
Driver='ODBC Driver 11 for SQL Server';Server=your_server;Trusted_Connection=yes  
```  
  
Sie können auch **Trusted\_Connection\=yes** dem DSN\-Eintrag der ODBC.ini zufügen.  
  
Sie können auch die **\-E** Option in **sqlcmd** verwenden. Weitere Informationen finden Sie unter [Herstellen einer Verbindung mit sqlcmd](../content/Connecting-with-sqlcmd.md).  
  
Stellen Sie sicher, dass der Linux\-Prinzipalserver, der mit [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] verbunden werden soll, bereits mit Kerberos KDC authentifiziert ist.  
  
**ServerSPN** und **FailoverPartnerSPN** werden nicht unterstützt.  
  
## Bereitstellen von einem ODBC\-Treiber für Linux\-Anwendung, die als Dienst ausgeführt werden soll  
Ein Systemadministrator kann eine Anwendung bereitstellen, die als Dienst laufen soll, der eine Kerberos\-Authentifizierung verwendet, um sich mit [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] zu verbinden.  
  
Sie müssen zuerst Kerberos auf dem Linux\-Computer konfigurieren und sicherstellen, dass die Anwendung die Kerberos\-Anmeldeinformationen des Prinzipals Standard verwenden kann.  
  
Stellen Sie sicher, dass Sie kinit oder PAM \(Pluggable Authentication Module\) verwenden, um das TGT für den Prinzipal, der die Verbindung verwendet, abzurufen und zwischenzuspeichern:  
  
-   Führen Sie kinit aus und spezifizieren Sie Prinzipalnamen und \-Kennwort.  
  
-   Führen Sie kinit aus und spezifizieren Sie einen Prinzipalnamen und den Speicherort einer Schlüsseltabellendatei, die den Prinzipalschlüssel enthält, den ktutil erstellt hat.  
  
-   Stellen Sie sicher, dass die Anmeldung am System mit PAM \(Pluggable Authentication Module\) vorgenommen wurde.  
  
Da eine Anwendung als Dienst ausgeführt wird und die Kerberos\-Anmeldeinformationen programmbedingt ablaufen, erneuern Sie die Anmeldeinformationen, um kontinuierliche Verfügbarkeit des Diensts sicherzustellen. Der ODBC\-Treiber für Linux stellt keine Erneuerung der Anmeldeinformationen bereit. Stellen Sie sicher, dass ein Cron\-Job oder ein Skript existiert, das regelmäßig ausgeführt wird, um die Anmeldeinformationen vor dem Ablauf zu erneuern. Um zu vermeiden, dass für jede Erneuerung das Passwort bereitgestellt werden muss, können Sie in diesem Fall die Schlüsseltabellendatei verwenden, die zuvor erstellt wurde.  
  
[Kerberos\-Konfiguration und Verwendung](http://commons.oreilly.com/wiki/index.php/Linux_in_a_Windows_World/Centralized_Authentication_Tools/Kerberos_Configuration_and_Use) bietet ausführliche Informationen zu Methoden zum kerberisieren von Diensten unter Linux.  
  
## Nachverfolgen von Zugriffen auf eine Datenbank  
Ein Datenbankadministrator kann einen Audit\-Trail des Zugriffs auf eine Datenbank erstellen, wenn Systemkonten genutzt werden, um mithilfe integrierter Authentifizierung auf [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] zuzugreifen.  
  
Beim Anmelden in [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] wird das Systemkonto verwendet und es gibt keine Funktionalität für Linux, um die Identität des Sicherheitskontexts anzunehmen. Aus diesem Grund muss der Benutzer genauer bestimmt werden.  
  
Um Aktivitäten in [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] für Benutzer zu überwachen, muss die Anwendung statt des Systemkontos [!INCLUDE[tsql](../content/includes/tsql_md.md)] **EXECUTE AS** verwenden.  
  
Zum Verbessern der Anwendungsleistung kann eine Anwendung Verbindungspooling mit integrierten Authentifizierung und Überwachung verwenden. Das Kombinieren von Verbindungspooling, integrierter Authentifizierung und Überwachung stellt jedoch ein Sicherheitsrisiko dar, da der UnixODBC\-Treiber\-Manager unterschiedlichen Benutzern ermöglicht, gepoolte Verbindungen wiederzuverwenden. Weitere Informationen finden Sie unter [ODBC\-Verbindungspooling](http://www.unixodbc.org/doc/conn_pool.html).  
  
Vor der Wiederverwendung muss eine Anwendung gepoolte Verbindungen durch Ausführen von sp\_reset\_connection zurücksetzen.  
  
## Verwalten von Benutzeridentitäten mithilfe von Active Directory  
Ein Systemadministrator, der für Anwendungen zuständig ist, muss keine separaten Sätze von Anmeldeinformationen für [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] verwalten. Es ist möglich, Active Directory als ein Schlüsselverteilungscenter \(KDC\) für die integrierte Authentifizierung zu konfigurieren.  
  
## Verbindungsserver und verteilte Abfragen nutzen  
Entwickler können eine Anwendung bereitstellen, die einen Verbindungsserver oder verteilte Abfragen nutzt. Dies geschieht ohne einen Datenbankadministrator, der separate Sätze von SQL\-Anmeldeinformationen verwaltet. In diesem Fall muss ein Entwickler eine Anwendung so konfigurieren, dass sie integrierte Authentifizierung nutzt.  
  
-   Der Benutzer meldet sich bei einem Clientcomputer an und authentifiziert sich beim Anwendungsserver.  
  
-   Der Anwendungsserver ist mit anderem Datenbanknamen authentifiziert und stellt eine Verbindung mit [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] her.  
  
-   [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] authentifiziert sich gegenüber einer anderen Datenbank \([!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)]\) als Datenbankbenutzer.  
  
Nachdem die integrierte Authentifizierung konfiguriert ist, werden Anmeldeinformationen für den Verbindungsserver übergeben.  
  
## Integrierte Authentifizierung und sqlcmd  
Für den Zugriff auf [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] mithilfe der integrierten Authentifizierung verwenden Sie die sqlcmd\-Option \-E. Stellen Sie sicher, dass das Konto, auf dem sqlcmd ausgeführt wird, dem Standard\-Kerberos\-Prinzipalserver zugeordnet ist.  
  
## Integrierte Authentifizierung und bcp  
Für den Zugriff auf [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] mithilfe der integrierten Authentifizierung, verwenden Sie die bcp\-Option „\-T“. Stellen Sie sicher, dass das Konto, auf dem bcp ausgeführt wird, dem Standard\-Kerberos\-Prinzipalserver zugeordnet ist.  
  
Es ist ein Fehler, „\-T“ mit der Option „\-U“ oder „\-P“ zu verwenden.  
  
## Unterstützte Syntax für einen SPN registriert von [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)]  
Die Syntax, die SPNs in Attributen für Verbindungszeichenfolgen und Verbindungen verwenden, lautet wie folgt:  
  
|Syntax|Beschreibung|  
|----------|----------------|  
|MSSQLSvc\/*fqdn*:*port*|Der vom Anbieter erstellte Standard\-SPN, wenn TCP verwendet wird.*port* ist eine TCP\-Portnummer.*fqdn* ist ein vollqualifizierter Domänenname.|  
  
## Authentifizieren eines Linux\-Computers mit Active Directory  
\(Weitere Informationen zur Authentifizierung Ihres Linux\-Computer mit Active Directory, finden Sie unter [Linux\-Clients mit Active Directory authentifizieren](http://technet.microsoft.com/magazine/2008.12.linux.aspx#id0060048).\)  
  
Geben Sie die Daten in die Datei krb5.conf ein. krb5.conf ist in \/etc\/, aber Sie können sich auf eine andere Datei \(**export KRB5\_CONFIG\=\/home\/dbapp\/etc\/krb5.conf**\) beziehen. Im Folgenden finden Sie eine krb5.conf\-Beispieldatei.  
  
```  
[libdefaults]  
default_realm = YYYY.CORP.CONTOSO.COM  
dns_lookup_realm = false  
dns_lookup_kdc = true  
ticket_lifetime = 24h  
forwardable = yes  
  
[domain_realm]  
.yyyy.corp.contoso.com = YYYY.CORP.CONTOSO.COM  
.zzzz.corp.contoso.com = ZZZZ.CORP.CONTOSO.COM  
```  
  
Falls Ihr Linux\-Computer das Dynamic Host Configuration Protocol \(DHCP\) verwendet und der Windows\-DHCP\-Server die verwendeten DNS\-Server verwendet, können Sie **dns\_lookup\_kdc\=true** verwenden. Nun können Sie Kerberos verwenden, um sich wie folgt in Ihrer Domäne anzumelden: `kinit  alias@YYYY.CORP.CONTOSO.COM`. Parameter, die an kinit übermittelt werden, berücksichtigen die Groß\-\/Kleinschreibung und der für die Domäne konfigurierte [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] Computer muss den Benutzer alias@YYYY.CORP.CONTOSO.COM als gültigen Anmeldenamen hinzugefügt haben. Der ODBC\-Treiber für [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] unter Linux unterstützt die Generierung von Kerberos\-Anmeldeinformationen über eine Schlüsseltabellendatei. Sie können nun vertrauenswürdige Verbindungen \(**Trusted\_Connection\=YES** in einer Verbindungszeichenfolge oder **sqlcmd \-E**\) verwenden.  
  
Die Zeit auf dem Linux\-Computer und die Uhrzeit für die Kerberos\-Domänencontroller \(KDC\) müssen möglichst übereinstimmen. Stellen Sie sicher, dass die Systemzeit richtig eingestellt ist und dem Network Time Protocol \(NTP\) entspricht.  
  
Wenn die Kerberos\-Authentifizierung fehlschlägt, verwendet der ODBC\-Treiber unter Linux nicht die NTLM\-Authentifizierung.  
  
## Siehe auch  
[Microsoft ODBC Driver for SQL Server on Linux](../content/Microsoft-ODBC-Driver-for-SQL-Server-on-Linux.md)  
  
