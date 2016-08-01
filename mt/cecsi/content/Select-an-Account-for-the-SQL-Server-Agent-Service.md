---
title: "Ausw&#228;hlen eines Kontos f&#252;r den SQL Server-Agent-Dienst"
ms.custom: na
ms.date: 07/27/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - tools-ssms
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: fe658e32-9e6b-4147-a189-7adc3bd28fe7
caps.latest.revision: 5
caps.handback.revision: 4
manager: jhubbard
translation.priority.mt: 
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
# Ausw&#228;hlen eines Kontos f&#252;r den SQL Server-Agent-Dienst
Das Dienststartkonto definiert das [!INCLUDE[msCoName](../content/includes/msCoName_md.md)] Windows-Konto, in dem der [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)]-Agent ausgeführt wird, und legt dessen Netzwerkberechtigungen fest. [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] -Agent wird als angegebenes Benutzerkonto ausgeführt. Sie wählen ein Konto für den [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)]-Agent-Dienst mithilfe des [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)]-Konfigurations-Managers aus. Dort können Sie zwischen folgenden Optionen wählen:  
  
-   **Erstellt\-in Konto**. Sie können aus einer Liste von folgende integrierte\-in Windows-Dienstkonten:  
  
    -   **Lokales System** Konto. Der Name dieses Kontos ist NT-Autorität\\System. Hierbei handelt es sich um ein Konto mit weit reichenden Befugnissen, das über unbeschränkten Zugriff auf alle lokalen Systemressourcen verfügt. Es ist ein Mitglied der Windows **Administratoren** auf dem lokalen Computer, und ist daher ein Mitglied der [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] **Sysadmin** feste Serverrolle  
  
        > [!IMPORTANT]  
        > Die **Konto Lokales System** Option wird nur für Abwärtskompatibilität bereitgestellt. Ein lokales Systemkonto verfügt über Berechtigungen, die für den [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)]-Agent nicht erforderlich sind. Vermeiden Sie die Ausführung des [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)]-Agents als lokales Systemkonto. Zur Verbesserung der Sicherheit sollten Sie ein Windows-Domänenkonto zusammen mit den im folgenden Abschnitt "Berechtigungen für Windows-Domänenkonten" aufgelisteten Berechtigungen verwenden.  
  
-   **Dieses Konto**. Hier können Sie das Windows-Domänenkonto angeben, unter dem der [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)]-Agent-Dienst ausgeführt wird. Es wird empfohlen, ein Windows-Benutzerkonto, das nicht Mitglied der Windows ist auswählen **Administratoren** Gruppe. Es gibt jedoch Einschränkungen für die Verwendung der Multiserveradministration bei der [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] -Agent-Dienstkonto ist kein Mitglied der lokalen **Administratoren** Gruppe. Weitere Informationen finden Sie unter "Unterstützte Dienstkontotypen" weiter unten in diesem Thema.  
  
## Berechtigungen für Windows-Domänenkonten  
Wählen Sie zum Erhöhen der Sicherheit **dieses Konto**, gibt ein Windows-Domänenkonto an. Das von Ihnen angegebene Windows-Domänenkonto muss folgende Berechtigungen haben:  
  
-   Berechtigung zum Anmelden als Dienst für alle Windows-Versionen (SeServiceLogonRight)  
  
> [!NOTE]  
> Die [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] -Agent-Dienstkonto muss Mitglied der Prä\-Gruppe von Windows 2000 kompatibler Zugriff auf den Domänencontroller oder Aufträge, die Domänen-Benutzer gehören, die nicht Mitglied der Gruppe der Administratoren Windows fehl.  
  
-   Auf Servern unter Windows erfordert das vom [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)]-Agent-Dienst ausgeführte Konto folgende Berechtigungen, um Proxys für den [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)]-Agent unterstützen zu können.  
  
    -   Berechtigung zum Umgehen von durchsuchenden Prüfungen (SeChangeNotifyPrivilege)  
  
    -   Berechtigung zum Ersetzen eines Prozesses\-Tokens auf Prozessebene (SeAssignPrimaryTokenPrivilege)  
  
    -   Berechtigung zum Anpassen des Arbeitsspeicherkontingents für einen Prozess (SeIncreaseQuotaPrivilege)   
  
    -   Berechtigung zum Anmelden mithilfe der Batchanmeldung (SeBatchLogonRight)  
  
> [!NOTE]  
> Wenn das Konto nicht über die zur Unterstützung von Proxys nur von Mitgliedern der erforderlichen Berechtigungen verfügt die **Sysadmin** -Serverrolle kann Aufträge erstellen.  
  
> [!NOTE]  
> Um WMI-Warnbenachrichtigungen zu empfangen, muss das Dienstkonto des [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)]-Agents über die Berechtigung für den Namespace verfügen, der die WMI-Ereignisse enthält. Außerdem muss es dazu berechtigt sein, EREIGNISBERECHTIGUNGEN ZU ÄNDERN.  
  
## SQL Server-Rollenmitgliedschaft  
Das Konto, als das der [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)]-Agent-Dienst ausgeführt wird, muss Mitglied der folgenden [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)]-Rollen sein:  
  
-   Das Konto muss ein Mitglied der **Sysadmin** festen Serverrolle.  
  
-   Zum Verarbeiten von Multiserveraufträgen verwenden zu können, muss das Konto ein Mitglied der **Msdb** Datenbankrolle **TargetServersRole** auf dem Masterserver.  
  
## Unterstützte Dienstkontotypen  
In der folgenden Tabelle werden die Windows-Kontotypen aufgelistet, die für den [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)]-Agent-Dienst verwendet werden können.  
  
|Dienstkontotyp|Nicht\-gruppierte Server|Gruppierter Server|Domänencontroller (nicht\-gruppierten)|  
|------------------------|-------------------------|--------------------|--------------------------------------|  
|[!INCLUDE[msCoName](../content/includes/msCoName_md.md)] Windows-Domänenkonto (Mitglied der Windows-Administratorengruppe)|Supported|Supported|Supported|  
|Windows-Domänenkonto (nicht\-administrative)|Supported<br /><br />Weitere Informationen Sie zu Einschränkung 1 unten.|Supported<br /><br />Weitere Informationen Sie zu Einschränkung 1 unten.|Supported<br /><br />Weitere Informationen Sie zu Einschränkung 1 unten.|  
|Netzwerkdienstkonto (NT-Autorität\\NetworkService)|Supported<br /><br />Weitere Informationen Sie zu Einschränkung 1, 3 und 4 unten.|Nicht unterstützt|Nicht unterstützt|  
|Lokales Benutzerkonto (nicht\-administrative)|Supported<br /><br />Weitere Informationen Sie zu Einschränkung 1 unten.|Nicht unterstützt|Nicht verfügbar|  
|Lokales Systemkonto (NT-Autorität\\System)|Supported<br /><br />Weitere Informationen Sie zu Einschränkung 2 weiter unten.|Nicht unterstützt|Supported<br /><br />Weitere Informationen Sie zu Einschränkung 2 weiter unten.|  
|Lokales Dienstkonto (NT-Autorität\\LocalService)|Nicht unterstützt|Nicht unterstützt|Nicht unterstützt|  
  
### Einschränkung 1: Verwenden nicht\-Administratorkonten für die Multiserveradministration  
Beim Eintragen von Zielservern auf einem Masterserver kann ein Fehler mit einer Fehlermeldung, die der folgenden ähnlich ist, auftreten: "Fehler beim Eintragen."  
  
Starten Sie [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] und die [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)]-Agent-Dienste neu, um diesen Fehler zu beheben. Weitere Informationen finden Sie unter [starten, beenden, anhalten, fortsetzen, neu starten, den Datenbank-Engine, SQL Server-Agent oder SQL Server-Browser-Dienst](assetId:///32660a02-e5a1-411a-9e57-7066ca459df6).  
  
### Einschränkung 2: Verwenden des lokalen Systemkontos für die Multiserververwaltung  
Die Multiserververwaltung wird bei Ausführung des [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)]-Agent-Diensts unter dem lokalen Systemkonto nur dann unterstützt, wenn sich der Masterserver und der Zielserver auf demselben Computer befinden. Wenn Sie diese Konfiguration verwenden, wird beim Eintragen der Zielserver auf dem Masterserver etwa die folgende Meldung zurückgegeben:  
  
"Sicherstellen der-Agent-Start\-Einrichten des Kontos für *< Ziel\_Server\_Computer\_Name >* Anmeldung als Zielserver besitzt."  
  
Sie können diese zu Informationszwecken ausgegebene Meldung ignorieren. Der Eintragungsvorgang wird dennoch erfolgreich abgeschlossen. Weitere Informationen finden Sie unter [Erstellen einer Multiserver-Umgebung](../content/Create-a-Multiserver-Environment.md).  
  
### Einschränkung 3: Verwenden des Netzwerkdienstkontos als SQL Server-Benutzer  
[!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] Agent möglicherweise nicht gestartet werden, wenn das Ausführen der [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] Agent-Dienst unter dem Netzwerkdienstkonto und das Netzwerkdienstkonto explizit Zugriff gewährt wurde, sich anzumelden eine [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] -Instanz als ein [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] Benutzer.  
  
Starten Sie den Computer, auf dem [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] ausgeführt wird, neu, um diesen Fehler zu beheben. Dies muss nur einmal erfolgen.  
  
### Einschränkung 4: Verwenden des Netzwerkdienstkontos bei Ausführung von SQL Server Reporting Services auf demselben Computer  
[!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] Agent möglicherweise nicht gestartet werden, wenn das Ausführen der [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] Agent-Dienst unter dem Konto Netzwerkdienst und [!INCLUDE[ssRSnoversion](../content/includes/ssRSnoversion_md.md)] auch auf dem gleichen Computer ausgeführt wird.  
  
Starten Sie den Computer, auf dem [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] ausgeführt wird, neu, um diesen Fehler zu beheben. Starten Sie anschließend [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] und die [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)]-Agent-Dienste neu. Dies muss nur einmal erfolgen.  
  
## Allgemeine Aufgaben  
**So geben Sie das Startkonto für den SQL Server-Agent-Dienst an**  
  
-   [Festlegen des Dienststartkontos für SQL Server-Agent & #40; SQL Server-Konfigurations-Manager & #41;](../content/Set-the-Service-Startup-Account-for-SQL-Server-Agent--SQL-Server-Configuration-Manager-.md)  
  
**So geben Sie das Mailprofil für den SQL Server-Agent an**  
  
-   [Vorgehensweise: Konfigurieren der Verwendung von Datenbank-E-Mail für SQL Server-Agent-Mail (SQL Server Management Studio)](assetId:///4b8b61bd-4bd1-43cd-b6e5-c6ed2e101dce)  
  
> [!NOTE]  
> Verwenden Sie den [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)]-Konfigurations-Manager, um anzugeben, dass der [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)]-Agent beim Start des Betriebssystems starten soll.  
  
## Siehe auch  
[Einrichten von Windows-Dienstkonten](assetId:///309b9dac-0b3a-4617-85ef-c4519ce9d014)  
[Verwalten von Diensten mit SQL-Computer-Manager](assetId:///78dee169-df0c-4c95-9af7-bf033bc9fdc6)  
[Implementieren der SQL Server-Agent-Sicherheit](../content/Implement-SQL-Server-Agent-Security.md)  
  
