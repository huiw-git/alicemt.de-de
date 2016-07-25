---
title: "Herstellen von Verbindungen mit SQL Server mit der integrierten Kerberos-Authentifizierung"
ms.custom: na
ms.date: 07/01/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - drivers
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 687802dc-042a-4363-89aa-741685d165b3
caps.latest.revision: 30
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
# Herstellen von Verbindungen mit SQL Server mit der integrierten Kerberos-Authentifizierung
  Ab [!INCLUDE[jdbc_40](../content/includes/jdbc_40_md.md)] können Anwendungen mithilfe der **authenticationScheme**\-Verbindungseigenschaft angeben, dass eine Verbindung mit einer Datenbank unter Verwendung der integrierten Kerberos\-Authentifizierung Typ 4 hergestellt werden soll. Weitere Informationen zu Verbindungseigenschaften finden Sie unter [Einstellen der Verbindungseigenschaften](../content/Setting-the-Connection-Properties.md). Weitere Informationen zu Kerberos finden Sie unter [Technischer Anhang zu Kerberos für Windows](http://go.microsoft.com/fwlink/?LinkId=101449) und [Microsoft Kerberos](http://go.microsoft.com/fwlink/?LinkID=100758).  
  
 Bei Verwendung der integrierten Authentifizierung mit dem Java\-**Krb5LoginModule** können Sie das Modul mithilfe der [Krb5LoginModule\-Klasse](https://docs.oracle.com/javase/8/docs/jre/api/security/jaas/spec/com/sun/security/auth/module/Krb5LoginModule.html) konfigurieren.  
  
 [!INCLUDE[jdbcNoVersion](../content/includes/jdbcNoVersion_md.md)] legt für Java\-VMs von IBM die folgenden Eigenschaften fest:  
  
-   **useDefaultCcache \= true**  
  
-   **moduleBanner \= false**  
  
 [!INCLUDE[jdbcNoVersion](../content/includes/jdbcNoVersion_md.md)] legt für alle anderen Java\-VMs die folgenden Eigenschaften fest:  
  
-   **useTicketCache \= true**  
  
-   **doNotPrompt \= true**  
  
## Hinweise  
 Vor [!INCLUDE[jdbc_40](../content/includes/jdbc_40_md.md)] konnten Anwendungen die integrierte Authentifizierung \(mit Kerberos oder NTLM, je nach Verfügbarkeit\) mithilfe der **integratedSecurity**\-Verbindungseigenschaft und durch Verweisen auf **sqljdbc\_auth.dll** angeben, entsprechend der Beschreibung in [Erstellen der Verbindungs-URL](../content/Building-the-Connection-URL.md).  
  
 Ab [!INCLUDE[jdbc_40](../content/includes/jdbc_40_md.md)] können Anwendungen mit der **authenticationScheme**\-Verbindungseigenschaft angeben, dass eine Verbindung mit einer Datenbank mithilfe der integrierten Kerberos\-Authentifizierung hergestellt werden soll, unter Verwendung der reinen Java\-Kerberos\-Implementierung:  
  
-   Wenn die integrierte Authentifizierung mit dem **Krb5LoginModule** ausgeführt werden soll, müssen Sie dennoch die **integratedSecurity\=true**\-Verbindungseigenschaft angeben. In diesem Fall geben Sie auch die **authenticationScheme\=JavaKerberos**\-Verbindungseigenschaft an.  
  
-   Wenn weiterhin die integrierte Authentifizierung mit **sqljdbc\_auth.dll** verwendet werden soll, geben Sie einfach die **integratedSecurity\=true**\-Verbindungseigenschaft \(und optional **authenticationScheme\=NativeAuthentication**\) an.  
  
-   Wenn Sie **authenticationScheme\=JavaKerberos** angeben, jedoch nicht gleichzeitig **integratedSecurity\=true** angeben, ignoriert der Treiber die **authenticationScheme**\-Verbindungseigenschaft, und es wird davon ausgegangen, dass Benutzername und Kennwort für die Anmeldeinformationen in der Verbindungszeichenfolge enthalten sind.  
  
 Werden Verbindungen mit einer Datenquelle erstellt, können Sie das Authentifizierungsschema programmgesteuert mit „setAuthenticationScheme“ und optional den SPN für Kerberos mithilfe von **setServerSpn** festlegen.  
  
 Zur Unterstützung der Kerberos\-Authentifizierung wurde eine neue Protokollierung eingeführt: com.microsoft.sqlserver.jdbc.internals.KerbAuthentication. Weitere Informationen finden Sie unter [Ablaufverfolgung für Treibervorgänge](../content/Tracing-Driver-Operation.md).  
  
 Befolgen Sie beim Konfigurieren von Kerberos die folgenden Richtlinien:  
  
1.  Legen Sie **AllowTgtSessionKey** in der Registrierung für Windows auf 1 fest. Weitere Informationen finden Sie unter [KDC\-Konfigurationsschlüssel in Windows Server 2003 und Kerberos\-Protokoll\-Registrierungseinträge](http://support.microsoft.com/kb/837361).  
  
2.  Stellen Sie sicher, dass die Kerberos\-Konfiguration \(krb5.conf in UNIX\-Umgebungen\) auf den richtigen Bereich und KDC für Ihre Umgebung zeigt.  
  
3.  Initialisieren Sie den TGT\-Cache mit "kinit" oder indem Sie sich bei der Domäne anmelden.  
  
4.  Bei Ausführung einer Anwendung, die **authenticationScheme\=JavaKerberos** verwendet, unter dem Betriebssystem Windows Vista bzw. Windows 7 muss ein Standardbenutzerkonto verwendet werden. Wenn Sie jedoch die Anwendung unter einem Administratorkonto ausführen, muss sie mit Administratorberechtigungen ausgeführt werden.  
  
> [!NOTE]  
>  Das serverSpn\-Verbindungsattribut wird nur von Microsoft JDBC Driver 4.2 unterstützt.  
  
## Dienstprinzipalnamen  
 Ein Dienstprinzipalname \(SPN, Service Principal Name\) ist der Name, über den ein Client eine Instanz eines Diensts eindeutig identifiziert.  
  
 Sie können den SPN mithilfe der Verbindungseigenschaft **serverSpn** angeben oder ihn einfach vom Treiber erstellen lassen \(Standardeinstellung\).  Diese Eigenschaft hat die Form: „MSSQLSvc\/fqdn:port@REALM“, wobei „fqdn“ den vollqualifizierten Domänennamen, „Port“ die Portnummer und „REALM“ den Kerberos\-Bereich des SQL Server\-Computers in Großbuchstaben bedeuten.  Der Bereichsteil dieser Eigenschaft ist optional, wenn der Standardbereich Ihrer Kerberos\-Konfiguration der gleiche Bereich wie der des Servers ist, und wird standardmäßig nicht angegeben.  Wenn Sie ein bereichsübergreifendes Authentifizierungsszenario unterstützen möchten, in dem sich der Standardbereich der Kerberos\-Konfiguration vom Bereich des Servers unterscheidet, müssen Sie den SPN mithilfe der Eigenschaft „serverSpn“ angeben.  
  
 In diesem Fall kann Ihr SPN etwa so aussehen: “MSSQLSvc\/ein\-server.zzz.corp.contoso.com:1433@ZZZZ.CORP.CONTOSO.COM”  
  
 Weitere Informationen zu Dienstprinzipalnamen \(SPNs\) finden Sie in folgendem Thema:  
  
-   [Verwenden der Kerberos\-Authentifizierung in SQL Server](http://support.microsoft.com/kb/319723)  
  
-   [Verwenden von Kerberos mit SQL Server](http://go.microsoft.com/fwlink/?LinkId=207814)  
  
## Erstellen einer Anmeldemodul\-Konfigurationsdatei  
 Sie können optional eine Kerberos\-Konfigurationsdatei angeben. Wenn keine Konfigurationsdatei angegeben wird, gelten die folgenden Einstellungen:  
  
 Sun\-JVM  
 com.sun.security.auth.module.Krb5LoginModule required useTicketCache\=true doNotPrompt\=true;  
  
 IBM\-JVM  
 com.ibm.security.auth.module.Krb5LoginModule required useDefaultCcache \= true moduleBanner \= false;  
  
 Wenn Sie selbstständig eine Anmeldemodul\-Konfigurationsdatei erstellen, muss die Datei das folgende Format aufweisen:  
  
```  
<name> {  
    <LoginModule> <flag> <LoginModule options>;  
    <optional_additional_LoginModules, flags_and_options>;  
};  
```  
  
 Eine Anmeldemodul\-Konfigurationsdatei enthält einen oder mehrere Einträge, die jeweils angeben, welche zugrunde liegende Authentifizierungstechnologie für eine bestimmte Anwendung bzw. für bestimmte Anwendungen verwendet werden soll. Beispiel:  
  
```  
SQLJDBCDriver {  
   com.sun.security.auth.module.Krb5LoginModule required useTicketCache=true doNotPrompt=true;  
};  
```  
  
 Jeder Eintrag der Anmeldemodul\-Konfigurationsdatei besteht aus einem Namen, auf den ein oder mehrere LoginModule\-spezifische Einträge folgen. Jeder LoginModule\-spezifische Eintrag wird jeweils durch ein Semikolon abgeschlossen, und die gesamte Gruppe von LoginModule\-spezifischen Einträgen wird von geschweiften Klammern umschlossen. Jeder Konfigurationsdateieintrag wird durch ein Semikolon abgeschlossen.  
  
 Für den Treiber kann nicht nur festgelegt werden, dass Kerberos\-Anmeldeinformationen mit den Einstellungen in der Anmeldemodul\-Konfigurationsdatei erhalten werden können. Stattdessen kann der Treiber auch vorhandene Anmeldeinformationen verwenden. Dies kann hilfreich sein, wenn die Anwendung Verbindungen mit den Anmeldeinformationen mehrerer Benutzer herstellen muss.  
  
 Der Treiber versucht zunächst vorhandene Anmeldeinformationen zu verwenden \(sofern diese verfügbar sind\), bevor er die Anmeldung mit dem angegebenen Anmeldemodul ausführt. Bei Ausführung von Code unter einem bestimmten Kontext mithilfe der Subject.doAs\-Methode wird daher eine Verbindung mit den Anmeldeinformationen erstellt, die an den Aufruf von Subject.doAs übergeben werden.  
  
 Weitere Informationen finden Sie unter [JAAS Login Configuration File](https://docs.oracle.com/javase/8/docs/technotes/guides/security/jgss/tutorials/LoginConfigFile.html) und [Class Krb5LoginModule](https://docs.oracle.com/javase/8/docs/jre/api/security/jaas/spec/com/sun/security/auth/module/Krb5LoginModule.html).  
  
## Erstellen einer Kerberos\-Konfigurationsdatei  
 Weitere Informationen zu Kerberos\-Konfigurationsdateien finden Sie unter [Kerberos Requirements](https://docs.oracle.com/javase/8/docs/technotes/guides/security/jgss/tutorials/KerberosReq.html).  
  
 Dies ist eine Konfiguration für eine Beispieldomäne. YYYY und ZZZZ sind durch die Domänennamen an Ihrem Standort zu ersetzen.  
  
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
  
[realms]  
        YYYY.CORP.CONTOSO.COM = {  
  kdc = krbtgt/YYYY.CORP. CONTOSO.COM @ YYYY.CORP. CONTOSO.COM  
  default_domain = YYYY.CORP. CONTOSO.COM  
}  
  
        ZZZZ.CORP. CONTOSO.COM = {  
  kdc = krbtgt/ZZZZ.CORP. CONTOSO.COM @ ZZZZ.CORP. CONTOSO.COM  
  default_domain = ZZZZ.CORP. CONTOSO.COM  
}  
  
```  
  
## Aktivieren der Domänenkonfigurationsdatei und der Anmeldemodul\-Konfigurationsdatei  
 Sie können eine Domänenkonfigurationsdatei mit \-Djava.security.krb5.conf aktivieren. Sie können eine Anmeldemodul\-Konfigurationsdatei mit **\-Djava.security.auth.login.config** aktivieren.  
  
 Sie können beispielsweise beim Starten der Anwendung Folgendes an der Befehlszeile eingeben:  
  
```  
Java.exe -Djava.security.auth.login.config=SQLJDBCDriver.conf -Djava.security.krb5.conf=krb5.ini <APPLICATION_NAME>  
  
```  
  
## Überprüfen des Zugriffs auf SQL Server über Kerberos  
 Führen Sie in SQL Server Management Studio die folgende Abfrage aus:  
  
 **select auth\_scheme from sys.dm\_exec\_connections where session\_id\=@@spid**  
  
 Vergewissern Sie sich, dass Sie über die erforderliche Berechtigung zum Ausführen dieser Abfrage verfügen.  
  
## Siehe auch  
 [Verbinden von SQL Server mit dem JDBC-Treiber](../content/Connecting-to-SQL-Server-with-the-JDBC-Driver.md)  
  
  