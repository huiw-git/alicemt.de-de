---
title: "SQL Server-Agent"
ms.custom: na
ms.date: 07/27/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - tools-ssms
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 8d1dc600-aabb-416f-b3af-fbc9fccfd0ec
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
# SQL Server-Agent
[!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] -Agent ist eAufträge Microsoft WAufträgedows-Dienst, der geplante admAufträgeistrative Tasks Aufträge *ausführt, die als* Aufträge [!INCLUDE[ssCurrent](../content/includes/ssCurrent_md.md)].  
  
**In diesem Thema**  
  
-   [Vorteile des SQL Server-Agents](#Benefits)  
  
-   [Komponenten des SQL Server-Agents](#Components)  
  
-   [Sicherheit für die Administration mit dem SQL Server-Agent](#Security)  
  
## <a name="Benefits"></a>Vorteile des SQL Server-Agents  
[!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] -Agent verwendet [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] , um Auftragsinformationen zu speichern. Aufträge enthalten einen oder mehrere Auftragsschritte. Jeder Schritt enthält einen eigenen Task, z. B. das Sichern einer Datenbank.  
  
[!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] -Agent kann einen Auftrag anhand eines Zeitplans, als Reaktion auf ein bestimmtes Ereignis oder bei Bedarf ausführen. Wenn Sie z. B. am Ende jedes Arbeitstages alle Server des Unternehmens sichern möchten, können Sie diesen Task automatisieren. Planen Sie die Sicherung so, dass sie montags bis freitags nach 22:00 Uhr ausgeführt wird. Falls bei der Sicherung ein Problem auftritt, kann der SQL Server-Agent das Ereignis aufzeichnen und Sie benachrichtigen.  
  
> [!NOTE]  
> Standardmäßig der [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] -Agent-Dienst ist deaktiviert Wenn [!INCLUDE[ssCurrent](../content/includes/ssCurrent_md.md)] wenn der Benutzer explizit, dass den Dienst wählt installiert ist.  
  
## <a name="Components"></a>Komponenten des SQL Server-Agents  
[!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] -Agent verwendet die folgenden Komponenten, um die auszuführenden Aufgaben, den Zeitpunkt der Ausführung und die Meldung erfolgreicher bzw. fehlgeschlagener Aufgaben zu definieren.  
  
### ausführt, die als  
Ein *Auftrag* umfasst eine angegebene Reihe von Aktionen, die der [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] -Agent ausführt. Durch die Verwendung von Aufträgen können Sie eine Verwaltungsaufgabe so definieren, dass diese ein- oder mehrmals ausgeführt und der erfolgreiche oder fehlgeschlagene Abschluss der Ausführung überwacht werden kann. Aufträge können auf einem lokalen oder mehreren Remoteservern ausgeführt werden.  
  
> [!IMPORTANT]  
> [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] -Agentaufträge, die zu der Zeit eines Failoverereignisses auf einer [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] -Failoverclusterinstanz ausgeführt werden, werden nach dem Failover nicht zu einem anderen Failoverclusterknoten fortgesetzt. [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] Agentaufträge, die zum Zeitpunkt einer Hyper ausgeführt werden\-V-Knoten angehalten werden nicht fortgesetzt werden, wenn die Pause ein Failover auf einen anderen Knoten verursacht. Aufträge, die begonnen, aber wegen eines Failoverereignisses nicht abgeschlossen werden, werden als gestartet protokolliert, zeigen jedoch keine weiteren Protokolleinträge für Abschluss oder Fehler an. [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] Agentaufträge in diesen Szenarien wurden scheinbar nie beendet.  
  
Für die Ausführung von Aufträgen gibt es mehrere Möglichkeiten:  
  
-   Ausführung gemäß einem Zeitplan oder mehreren Zeitplänen.  
  
-   Ausführung als Reaktion auf eine oder mehrere Warnungen.  
  
-   Durch Ausführen des sp\_start\_gespeicherte Prozedur.  
  
Die einzelnen Aktionen im Rahmen eines Auftrags werden als *Auftragsschritte*bezeichnet. Ein Auftragsschritt kann beispielsweise in der Ausführung einer [!INCLUDE[tsql](../content/includes/tsql_md.md)] -Anweisung, der Ausführung eines [!INCLUDE[ssIS](../content/includes/ssIS_md.md)] -Pakets oder der Ausgabe eines Befehls an einen Analysis Services-Server bestehen. Auftragsschritte werden als Teil des Auftrags verwaltet.  
  
Jeder Auftragsschritt wird in einem bestimmten Sicherheitskontext ausgeführt. Bei Auftragsschritten, die [!INCLUDE[tsql](../content/includes/tsql_md.md)]verwenden, nutzen Sie zum Festlegen des Sicherheitskontexts für den Auftragsschritt die EXECUTE AS-Anweisung. Bei anderen Arten von Auftragsschritten verwenden Sie ein Proxykonto, um den Sicherheitskontext für den Auftragsschritt festzulegen.  
  
### Zeitpläne  
Durch einen *Zeitplan* wird angegeben, wann ein Auftrag ausgeführt wird. Im Rahmen eines Zeitplans können auch mehrere Aufträge ausgeführt werden, und für einen Auftrag können mehrere Zeitpläne gelten. Ein Zeitplan kann bezüglich des Ausführungszeitpunktes für einen Auftrag folgende Bedingungen definieren:  
  
-   Ausführung sobald der [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] -Agent startet.  
  
-   Ausführung, wenn sich die CPU-Auslastung des Computers in einem Bereich befindet, den Sie als Leerlauf definiert haben.  
  
-   Einmalige Ausführung zu einem angegebenen Zeitpunkt und Datum.  
  
-   Ausführung auf wiederkehrender Basis.  
  
Weitere Informationen finden Sie unter [Erstellen und Anfügen von Zeitplänen für Aufträge](../content/Create-and-Attach-Schedules-to-Jobs.md).  
  
### Warnungen  
Eine *Warnung* ist eine automatische Reaktion auf ein bestimmtes Ereignis. Bei einem Ereignis kann es sich z. B. um das Starten eines Auftrags oder um das Erreichen eines bestimmten Schwellenwertes im Hinblick auf die Systemressourcen handeln. Sie definieren die Bedingungen, unter denen eine Warnung auftritt.  
  
Eine Warnung kann als Reaktion auf eine der folgenden Bedingungen ausgegeben werden:  
  
-   [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] -Ereignisse  
  
-   [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] -Leistungsbedingungen  
  
-   Microsoft Windows-Verwaltungsinstrumentation (WMI)-Ereignisse auf dem Computer, auf dem SQL Server-Agent ausgeführt wird  
  
Eine Warnung kann die folgenden Aktionen ausführen:  
  
-   Benachrichtigen eines oder mehrerer Operatoren.  
  
-   Ausführen eines Auftrags.  
  
Weitere Informationen finden Sie unter [Warnungen](../content/Alerts.md).  
  
### Operatoren  
Ein *Operator* definiert die Kontaktinformationen einer Person, die für die Verwaltung einer oder mehrerer [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)]-Instanzen zuständig ist. In einigen Unternehmen werden die Aufgaben eines Operators einer einzelnen Person zugewiesen. In größeren Unternehmen mit mehreren Servern teilen sich mehrere Personen die Aufgaben des Operators. Der Operator enthält keine Sicherheitsinformationen und definiert auch nicht den Sicherheitsprinzipal.  
  
[!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] kann Operatoren bei Warnungen folgendermaßen benachrichtigen:  
  
-   E\-e-Mail-Nachrichten  
  
-   Pager (bis e\-Mail)  
  
-   **NET send**  
  
> [!NOTE]  
> Zum Senden von Benachrichtigungen mit **net Send**, der Windows Messenger-Dienst muss auf dem Computer gestartet werden, in denen [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] Agent befindet.  
  
> [!IMPORTANT]  
> Pager und **net Send** Optionen aufgehoben [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] -Agent in einer zukünftigen Version von [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)]. Vermeiden Sie die Verwendung dieser Funktionen bei neuen Entwicklungsarbeiten, und planen Sie die Änderung von Anwendungen, die diese Funktionen zurzeit verwenden.  
  
Zum Senden von Benachrichtigungen an Operatoren mit e\-e-Mail oder Pager, müssen Sie konfigurieren [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] Datenbank-e-Mail-Agent. Weitere Informationen finden Sie unter [Database Mail](assetId:///9e4563dd-4799-4b32-a78a-048ea44a44c1).  
  
Ein Operator kann auch als Alias für eine Gruppe von Personen definiert werden. Auf diese Weise werden alle Mitglieder dieses Alias zur selben Zeit benachrichtigt. Weitere Informationen finden Sie unter [Operatoren](../content/Operators.md).  
  
## <a name="Security"></a>Sicherheit für die Administration mit dem SQL Server-Agent  
[!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] -Agent verwendet die festen Datenbankrollen **SQLAgentUserRole**, **SQLAgentReaderRole**und **SQLAgentOperatorRole** in der **msdb** -Datenbank, um den Zugriff auf den [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] -Agent für Benutzer zu steuern, die keine Mitglieder der festen Serverrolle **sysadmin** sind. Neben diesen festen Datenbankrollen können Datenbankadministratoren mithilfe von Subsystemen und Proxys sicherstellen, dass jeder Auftragsschritt mit den mindestens erforderlichen Berechtigungen ausgeführt wird.  
  
### Rollen  
Mitglieder der festen Datenbankrollen **SQLAgentUserRole**, **SQLAgentReaderRole**und **SQLAgentOperatorRole** in **msdb**und Mitglieder der festen Serverrolle **sysadmin** haben Zugriff auf den [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] -Agent. Ein Benutzer, der keiner dieser Rollen angehört, kann den [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] -Agent nicht verwenden. Weitere Informationen zu den Rollen, die von verwendet [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] -Agent finden Sie unter [implementieren SQL Server-Agent-Sicherheit](../content/Implement-SQL-Server-Agent-Security.md).  
  
### Subsysteme  
Ein Subsystem ist ein vordefiniertes Objekt, das die für einen Auftragsschritt verfügbare Funktionalität darstellt. Jeder Proxy hat Zugriff auf mindestens ein Subsystem. Subsysteme bieten Sicherheit, weil sie den Zugriff auf die für ein Proxykonto verfügbare Funktionalität begrenzen. Jeder Auftragsschritt wird im Kontext eines Proxys ausgeführt, mit Ausnahme von [!INCLUDE[tsql](../content/includes/tsql_md.md)] -Auftragsschritten. [!INCLUDE[tsql](../content/includes/tsql_md.md)] -Auftragsschritten wird der Sicherheitskontext mithilfe des EXECUTE AS-Befehls festgelegt.  
  
[!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] definiert die in der folgenden Tabelle aufgeführten Subsysteme:  
  
|Name des Subsystems|Beschreibung|  
|------------------|---------------|  
|Microsoft ActiveX-Skript|Ausführen eines ActiveX-Skript-Auftragsschritts.<br /><br />**\&#42;\&#42; Warnung \&#42;\&#42;** Das ActiveX Scripting-Subsystem aufgehoben [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] -Agent in einer zukünftigen Version von [!INCLUDE[msCoName](../content/includes/msCoName_md.md)][!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)]. Verwenden Sie diese Funktion beim Entwickeln neuer Anwendungen nicht, und planen Sie das Ändern von Anwendungen, in denen es zurzeit verwendet wird.|  
|Betriebssystem (**CmdExec**)|Ausführen eines ausführbaren Programms.|  
|PowerShell|Ausführen eines PowerShell-Skripterstellungs-Auftragsschritts.|  
|Replikationsverteiler|Ausführen eines Auftragsschritts, der den Replikationsverteilungs-Agent aktiviert.|  
|Replikationsmerge|Ausführen eines Auftragsschritts, der den Replikationsmerge-Agent aktiviert.|  
|Replikation-Warteschlangenleser|Ausführen eines Auftragsschritts, der den Warteschlangenlese-Agent der Microsoft SQL Server-Replikation aktiviert.|  
|Replikationsmomentaufnahme|Ausführen eines Auftragsschritts, der den Replikationsmomentaufnahme-Agent aktiviert.|  
|Replikationstransaktionsprotokoll-Leser|Ausführen eines Auftragsschritts, der den Protokolllese-Agent aktiviert.|  
|[!INCLUDE[ssASnoversion](../content/includes/ssASnoversion_md.md)] -Befehl|Ausführen eines [!INCLUDE[ssASnoversion](../content/includes/ssASnoversion_md.md)] -Befehls.|  
|[!INCLUDE[ssASnoversion](../content/includes/ssASnoversion_md.md)] -Abfrage|Ausführen einer [!INCLUDE[ssASnoversion](../content/includes/ssASnoversion_md.md)] -Abfrage.|  
|[!INCLUDE[ssIS](../content/includes/ssIS_md.md)] -Paketausführung|Ausführen eines [!INCLUDE[ssIS](../content/includes/ssIS_md.md)] -Pakets.|  
  
> [!NOTE]  
> Da [!INCLUDE[tsql](../content/includes/tsql_md.md)] Auftragsschritte keine Proxys verwenden, gibt es keine [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] -Agent-Subsystem für [!INCLUDE[tsql](../content/includes/tsql_md.md)] Auftragsschritten.  
  
[!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] -Agent erzwingt Subsystemeinschränkungen, selbst wenn der Sicherheitsprinzipal für den Proxy normalerweise die Berechtigung zum Ausführen des Tasks im Auftragsschritt hätte. Z. B. ein Proxy für einen Benutzer, der Mitglied der festen Serverrolle Sysadmin kann nicht ausgeführt ein [!INCLUDE[ssIS](../content/includes/ssIS_md.md)] Auftragsschritt, es sei denn, der Proxy den Zugriff auf die [!INCLUDE[ssIS](../content/includes/ssIS_md.md)] -Subsystem, obwohl der Benutzer ausführen kann [!INCLUDE[ssIS](../content/includes/ssIS_md.md)] Pakete.  
  
### Proxys  
[!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] -Agent verwendet Proxys zum Verwalten von Sicherheitskontexten. Ein Proxy kann für mehrere Auftragsschritte verwendet werden. Mitglieder der festen Serverrolle **sysadmin** können Proxys erstellen.  
  
Jeder Proxy entspricht Sicherheitsanmeldeinformationen. Jeder Proxy kann einer Gruppe von Subsystemen und Anmeldenamen zugeordnet werden. Der Proxy kann nur für Auftragsschritte benutzt werden, die ein dem Proxy zugeordnetes Subsystem verwenden. Um einen Auftragsschritt zu erstellen, der einen bestimmten Proxy verwendet, muss der Auftragsbesitzer einen Anmeldenamen verwenden, der diesem Proxy zugeordnet ist, oder er muss ein Mitglied einer Rolle mit unbeschränktem Zugriff auf Proxys sein. Mitglieder der festen Serverrolle **sysadmin** haben unbeschränkten Zugriff auf Proxys. Mitglieder von **SQLAgentUserRole**, **SQLAgentReaderRole**oder **SQLAgentOperatorRole** können nur Proxys verwenden, für die Ihnen der Zugriff erteilt wurde. Jedem Benutzer, der Mitglied einer dieser festen Datenbankrollen des [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] -Agents ist, muss Zugriff auf bestimmte Proxys gewährt werden, damit er Auftragsschritte erstellen kann, bei denen diese Proxys verwendet werden.  
  
## Verwandte Aufgaben  
Konfigurieren Sie den [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] -Agent anhand der folgenden Schritte zur Automatisierung der [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] -Verwaltung:  
  
1.  Überprüfen Sie, welche administrativen Tasks oder Serverereignisse regelmäßig auftreten und ob diese Tasks oder Ereignisse programmgesteuert verwaltet werden können. Ein Task eignet sich für die Automatisierung, wenn er eine festgelegte Reihenfolge von Schritten umfasst und zu einem bestimmten Zeitpunkt oder als Reaktion auf ein bestimmtes Ereignis auftritt.  
  
2.  Definieren Sie einen Satz von Aufträgen, Zeitplänen, Warnungen und Operatoren mit [!INCLUDE[ssManStudioFull](../content/includes/ssManStudioFull_md.md)], [!INCLUDE[tsql](../content/includes/tsql_md.md)] -Skripts oder [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] Management Objects (SMO). Weitere Informationen finden Sie unter [Erstellen von Aufträgen](../content/Create-Jobs.md).  
  
3.  Führen Sie die [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] -Agent-Aufträge aus, die Sie definiert haben.  
  
> [!NOTE]  
> Für die Standardinstanz von [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)]erhält der [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] -Dienst den Namen SQLSERVERAGENT. Für benannte Instanzen erhält der [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] -Agent-Dienst den Namen SQLAgent$*instancename*.  
  
Falls Sie mehrere Instanzen von [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)]ausführen, können Sie Tasks, die auf allen Instanzen ausgeführt werden müssen, mithilfe der Multiserververwaltung automatisieren. Weitere Informationen finden Sie unter [automatisierte Verwaltung in einem Unternehmen](../content/Automated-Administration-Across-an-Enterprise.md).  
  
Verwenden Sie für die ersten Schritte mit dem [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] -Agent die folgenden Aufgaben:  
  
|||  
|-|-|  
|**Beschreibung**|**Thema**|  
|Beschreibt, wie SQL Server-Agent konfiguriert wird.|[Configure SQL Server Agent](../content/Configure-SQL-Server-Agent.md)|  
|Beschreibt, wie der SQL Server-Agent-Dienst gestartet, beendet und angehalten wird.|[Start, Stop, or Pause the SQL Server Agent Service](../content/Start--Stop--or-Pause-the-SQL-Server-Agent-Service.md)|  
|Beschreibt Überlegungen zum Angeben eines Kontos für den SQL Server-Agent-Dienst.|[Wählen Sie ein Konto für den SQL Server-Agent-Dienst](../content/Select-an-Account-for-the-SQL-Server-Agent-Service.md)|  
|Beschreibt, wie das SQL Server-Agent-Fehlerprotokoll verwendet wird.|[SQL Server-Agent-Fehlerprotokolls](../content/SQL-Server-Agent-Error-Log.md)|  
|||  
|Beschreibt, wie Leistungsobjekte verwendet werden.|[Verwenden von Leistungsobjekten](../content/Use-Performance-Objects.md)|  
|Beschreibt den Wartungsplanungs-Assistenten, ein Hilfsprogramm, mit dem Sie Aufträge, Warnungen und Operatoren erstellen können, um die Verwaltung einer Instanz von SQL Server zu automatisieren.|[Use the Maintenance Plan Wizard](assetId:///db65c726-9892-480c-873b-3af29afcee44)|  
|Beschreibt, wie administrative Aufgaben mit dem SQL Server-Agent automatisiert werden.|[Automatisierte Administrationstasks & #40; SQL Server-Agent & #41;](../content/Automated-Administration-Tasks--SQL-Server-Agent-.md)|  
  
## Siehe auch  
[Oberflächenkonfiguration](assetId:///f741169c-1453-4ad2-830b-bf2be27d712f)  
  
