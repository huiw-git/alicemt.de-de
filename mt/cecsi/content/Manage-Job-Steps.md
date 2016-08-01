---
title: "Verwalten von Auftragsschritten"
ms.custom: na
ms.date: 07/27/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - tools-ssms
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 51352afc-a0a4-428b-8985-f9e58bb57c31
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
# Verwalten von Auftragsschritten
Ein Auftragsschritt ist eine Aktion, die der Auftrag auf einer Datenbank oder einem Server ausführt. Jeder Auftrag muss mindestens einen Auftragsschritt aufweisen. Folgende Auftragsschritte sind möglich:  
  
-   Ausführbare Programme und Betriebssystembefehle.  
  
-   [!INCLUDE[tsql](../content/includes/tsql_md.md)] Anweisungen, z. B. gespeicherte Prozeduren und erweiterte gespeicherte Prozeduren.  
  
-   PowerShell-Skripts.  
  
-   [!INCLUDE[msCoName](../content/includes/msCoName_md.md)] ActiveX-Skripts.  
  
-   Replikationstasks.  
  
-   [!INCLUDE[ssASnoversion](../content/includes/ssASnoversion_md.md)] Aufgaben.  
  
-   [!INCLUDE[ssISnoversion](../content/includes/ssISnoversion_md.md)] Pakete.  
  
Jeder Auftragsschritt wird in einem bestimmten Sicherheitskontext ausgeführt. Wenn der Auftragsschritt einen Proxy erfordert, wird er im Sicherheitskontext der Anmeldeinformationen des Proxys ausgeführt. Wenn ein Auftragsschritt keinen Proxy erfordert, wird er im Kontext des [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)]-Agent-Dienstkontos ausgeführt. Nur Mitglieder der festen Serverrolle sysadmin können Aufträge erstellen, die nicht ausdrücklich einen Proxy angeben.  
  
Weil Auftragsschritte im Kontext einer bestimmten ausführen [!INCLUDE[msCoName](../content/includes/msCoName_md.md)] Windows-Benutzer, müssen die Berechtigungen und die Konfiguration für den Auftragsschritt ausgeführt. Wenn Sie beispielsweise einen Auftrag erstellen, der einen Laufwerkbuchstaben oder einen UNC-Pfad (Universal Naming Convention) erfordert, können die Auftragsschritte unter Ihrem Windows-Benutzerkonto ausgeführt werden, während die Tasks getestet werden. Allerdings muss der Windows-Benutzer für den Auftragsschritt auch über die notwendigen Berechtigungen, die Laufwerkbuchstabenkonfigurationen oder den Zugriff auf das erforderliche Laufwerk verfügen. Andernfalls erzeugt der Auftragsschritt einen Fehler. Um dieses Problem zu verhindern, stellen Sie sicher, dass der Proxy für jeden Auftragsschritt über die notwendigen Berechtigungen für den Task verfügt, von dem der Auftragsschritt ausgeführt wird. Weitere Informationen finden Sie unter [Sicherheit und Schutz (Datenbankmodul)](assetId:///dfb39d16-722a-4734-94bb-98e61e014ee7).  
  
## Auftragsschrittprotokolle  
[!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] Agents kann Ausgabe bestimmter Auftragsschritte entweder in eine Betriebssystemdatei oder in die Sysjobstepslogs-Tabelle in der Msdb-Datenbank schreiben. Von den folgenden Auftragsschritttypen können Ausgaben in beide Ziele geschrieben werden:  
  
-   Ausführbare Programme und Betriebssystembefehle.  
  
-   [!INCLUDE[tsql](../content/includes/tsql_md.md)] Anweisungen verwendet werden.  
  
-   [!INCLUDE[ssASnoversion](../content/includes/ssASnoversion_md.md)] Aufgaben.  
  
Nur von Auftragsschritten, die von Benutzern ausgeführt werden, die Mitglieder der festen Serverrolle sysadmin sind, können Auftragsschrittausgaben in Betriebssystemdateien geschrieben werden. Wenn die Auftragsschritte von Benutzern ausgeführt werden, die Mitglieder der festen Datenbankrolle SQLAgentUserRole, SQLAgentReaderRole oder SQLAgentOperatorRole der msdb-Datenbank sind, kann die Ausgabe dieser Auftragsschritte nur in die sysjobstepslogs-Tabelle geschrieben werden.  
  
Auftragsschritte werden automatisch gelöscht, wenn Aufträge oder Auftragsschritte gelöscht werden.  
  
> [!NOTE]  
> Das Protokollieren von Replikationstasks und [!INCLUDE[ssISnoversion](../content/includes/ssISnoversion_md.md)]-Paketauftragsschritten wird vom jeweiligen Subsystem durchgeführt. Sie können zum Konfigurieren der Auftragsschrittprotokollierung nicht den [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)]-Agent für diese Art von Auftragsschritten verwenden.  
  
## Ausführbare Programme und Betrieb\-Systembefehle als Auftragsschritte  
Ausführbare Programme und Betrieb\-Systembefehle als Auftragsschritte verwendet werden können. Diese Dateien können die Dateierweiterungen BAT, CMD, COM oder EXE aufweisen.  
  
Wenn Sie ein ausführbares Programm oder ein Betriebssystem verwenden\-Systembefehl als Auftrag ausführen, müssen Sie angeben:  
  
-   Den Prozessexitcode, der zurückgegeben wird, wenn der Befehl erfolgreich ausgeführt wurde.  
  
-   Den auszuführenden Befehl. Beim Ausführen eines Betriebssystembefehls handelt es sich hierbei einfach um den Befehl selbst. Bei einem externen Programm, dies ist der Name des Programms und die Argumente für das Programm, z. B.: **C:\\Programmdateien\\Microsoft SQL Server\\100\\Tools\\Binn\\sqlcmd.exe \-e \-Q "sp\_"**  
  
    > [!NOTE]  
    > Sie müssen den vollständigen Pfad zur ausführbaren Datei angeben, wenn diese sich nicht in dem Verzeichnis befindet, das im Systempfad oder dem Pfad für den Benutzer angegeben ist, als der der Auftragsschritt ausgeführt wird.  
  
## Transact\-SQL-Auftragsschritte  
Beim Erstellen eines [!INCLUDE[tsql](../content/includes/tsql_md.md)]-Auftragsschritts müssen Sie folgende Schritte durchführen:  
  
-   Identifizieren der Datenbank, in der Sie den Auftrag ausführen.  
  
-   Eingeben der auszuführenden [!INCLUDE[tsql](../content/includes/tsql_md.md)]-Anweisung. Von der Anweisung wird möglicherweise eine gespeicherte Prozedur oder eine erweiterte gespeicherte Prozedur aufgerufen.  
  
Sie können auch eine vorhandene [!INCLUDE[tsql](../content/includes/tsql_md.md)]-Datei als Befehl für den Auftragsschritt öffnen.  
  
[!INCLUDE[tsql](../content/includes/tsql_md.md)] Verwenden Sie Auftragsschritte nicht [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] -Agent-Proxys. Stattdessen wird der Auftragsschritt als Besitzer des Auftragsschritts bzw. als [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)]-Agent-Dienstkonto ausgeführt, wenn der Besitzer des Auftragsschritts Mitglied der festen Serverrolle sysadmin ist. Mitglieder der festen Serverrolle Sysadmin können auch angeben, [!INCLUDE[tsql](../content/includes/tsql_md.md)] Auftragsschritte im Kontext eines anderen Benutzers ausgeführt, mit der *Datenbank\_Benutzer\_Namen* Parameter der gespeicherten Prozedur\_Hinzufügen\_Jobstep gespeicherte Prozedur. Weitere Informationen finden Sie unter [Sp_add_jobstep (Transact-SQL)](assetId:///97900032-523d-49d6-9865-2734fba1c755).  
  
> [!NOTE]  
> Ein einzelner [!INCLUDE[tsql](../content/includes/tsql_md.md)]-Auftragsschritt kann mehrere Batches enthalten. [!INCLUDE[tsql](../content/includes/tsql_md.md)] Auftragsschritte können eingebettete GO-Befehle enthalten.  
  
## PowerShell-Skript-Auftragsschritte  
Wenn Sie einen PowerShell-Skript-Auftragsschritt erstellen, müssen Sie eins von zwei Elementen als Befehl für den Schritt angeben:  
  
-   Den Text eines PowerShell-Skripts.  
  
-   Eine vorhandene PowerShell-Skriptdatei, die geöffnet werden soll.  
  
Die [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] Agent PowerShell-Subsystem öffnet eine PowerShell-Sitzung und lädt die [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] PowerShell-Snap-\-ins. Das PowerShell-Skript, das als Auftragsschrittbefehl verweisen kann verwendet die [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] PowerShell-Anbieter sowie Cmdlets. Weitere Informationen zum Schreiben von PowerShell-Skripts mithilfe der [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] PowerShell-Snap-\-ins finden Sie unter der [SQL Server PowerShell](assetId:///89b70725-bbe7-4ffe-a27d-2a40005a97e7).  
  
## ActiveX-Skript-Auftragsschritte  
  
> [!IMPORTANT]  
> Die ActiveX-Skript-Auftragsschritt aus entfernt [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] -Agent in einer zukünftigen Version von [!INCLUDE[msCoName](../content/includes/msCoName_md.md)][!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)]. Verwenden Sie diese Funktion beim Entwickeln neuer Anwendungen nicht, und planen Sie das Ändern von Anwendungen, in denen es zurzeit verwendet wird.  
  
Wenn Sie einen ActiveX-Skriptauftragsschritt erstellen, ist Folgendes notwendig:  
  
-   Identifizieren der Skriptsprache, in der der Auftragsschritt geschrieben ist.  
  
-   Erstellen des ActiveX-Skripts.  
  
Sie können auch eine vorhandene ActiveX-Skriptdatei als Befehl für den Auftragsschritt öffnen. ActiveX-Skriptbefehle können alternativ auch extern (beispielsweise mithilfe von Microsoft Visual Basic) kompiliert und anschließend als ausführbare Programme ausgeführt werden.  
  
Handelt es sich bei dem Befehl eines Auftragsschritts um ein ActiveX-Skript, können Sie das SQLActiveScriptHost-Objekt verwenden, um Ausgaben in das Verlaufsprotokoll des Auftragsschritts zu drucken oder COM-Objekte zu erstellen. Bei SQLActiveScriptHost handelt es sich um ein globales Objekt, das vom Hostsystem des [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)]-Agents in den Skriptnamensbereich eingefügt wird. Das Objekt verfügt über zwei Methoden ("Drucken" und "CreateObject"). Das folgende Beispiel veranschaulicht, wie ActiveX-Skripts in Visual Basic Scripting Edition (VBScript) funktionieren.  
  
```  
' VBScript example for ActiveX Scripting job step  
' Create a Dmo.Server object. The object connects to the  
' server on which the script is running.  
  
Set oServer = CreateObject("SQLDmo.SqlServer")  
oServer.LoginSecure = True  
oServer.Connect "(local)"  
'Disconnect and destroy the server object  
oServer.DisConnect  
Set oServer = nothing  
```  
  
## Replikationsauftragsschritte  
Wenn Sie Veröffentlichungen und Abonnements mithilfe der Replikation erstellen, werden standardmäßig Replikationsaufträge erstellt. Der Typ der erstellten Aufträge wird durch den Typ der Replikation (Momentaufnahme, Transaktion oder Merge) und die verwendeten Optionen bestimmt.  
  
Replikationsauftragsschritte aktivieren einen dieser Replikations-Agents:  
  
-   Momentaufnahme-Agent (Momentaufnahmeauftrag)  
  
-   Protokolllese-Agent (Protokollleserauftrag)  
  
-   Verteilungs-Agent (Verteilungsauftrag)  
  
-   Merge-Agent (Mergeauftrag)  
  
-   Warteschlangenlese-Agent (Warteschlangenleser-Auftrag)  
  
Beim Einrichten der Replikation können Sie zwischen drei Ausführungsarten für die Replikations-Agents wählen: immer nach dem Start des [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)]-Agents, bei Bedarf oder gemäß einem Zeitplan. Weitere Informationen zu Replikations-Agents finden Sie unter [Replikations-Agenten (Übersicht)](assetId:///a35ecd7d-f130-483c-87e3-ddc8927bb91b).  
  
## Analysis Services-Auftragsschritte  
[!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] -Agent unterstützt zwei unterschiedliche Arten von Analysis Services-Auftragsschritten, befehlsauftragsschritte und abfrageauftragsschritte.  
  
### Analysis Services-Befehlsauftragsschritte  
Wenn Sie einen [!INCLUDE[ssASnoversion](../content/includes/ssASnoversion_md.md)]-Befehlsauftragsschritt erstellen, müssen Sie folgende Schritte durchführen:  
  
-   Identifizieren der OLAP-Datenbank, in der Sie den Auftragsschritt ausführen.  
  
-   Eingeben der auszuführenden Anweisung. Die Anweisung muss eine XML-Code für [!INCLUDE[ssASnoversion](../content/includes/ssASnoversion_md.md)] **Execute** Methode. Die Anweisung enthält möglicherweise keinen vollständigen SOAP-Umschlag oder ein XML for [!INCLUDE[ssASnoversion](../content/includes/ssASnoversion_md.md)] **Discover** Methode. Beachten Sie, dass während [!INCLUDE[ssManStudioFull](../content/includes/ssManStudioFull_md.md)] unterstützt vollständige SOAP-Umschläge und die **Discover** Methode [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] -Agent-Auftragsschritten nicht der Fall.  
  
### Analysis Services-Abfrageauftragsschritte  
Wenn Sie einen [!INCLUDE[ssASnoversion](../content/includes/ssASnoversion_md.md)]-Abfrageauftragsschritt erstellen, müssen Sie folgende Schritte durchführen:  
  
-   Identifizieren der OLAP-Datenbank, in der Sie den Auftragsschritt ausführen.  
  
-   Eingeben der auszuführenden Anweisung. Bei der Anweisung muss es sich um eine MDX-Abfrage handeln (Multidimensional Expressions, mehrdimensionale Ausdrücke).  
  
Weitere Informationen zu MDX finden Sie unter [MDX-Anweisung Fundamentals (MDX)](assetId:///a560383b-bb58-472e-95f5-65d03d8ea08b).  
  
## Integration Services-Pakete  
Wenn Sie einen [!INCLUDE[ssISnoversion](../content/includes/ssISnoversion_md.md)]-Paketauftragsschritt erstellen, müssen Sie folgende Schritte durchführen:  
  
-   Identifizieren der Paketquelle.  
  
-   Identifizieren des Paketspeicherorts.  
  
-   Identifizieren der Konfigurationsdateien, wenn diese für das Paket erforderlich sind.  
  
-   Identifizieren der Befehlsdateien, wenn diese für das Paket erforderlich sind.  
  
-   Identifizieren der für das Paket zu verwendenden Überprüfung. Sie können beispielsweise angeben, dass das Paket signiert werden oder eine bestimmte Paket-ID aufweisen muss.  
  
-   Identifizieren der Datenquellen für das Paket.  
  
-   Identifizieren der Protokollanbieter für das Paket.  
  
-   Angeben von Variablen und Werten, die vor dem Ausführen des Pakets festgelegt werden.  
  
-   Identifizieren von Ausführungsoptionen.  
  
-   Hinzufügen oder Ändern von Befehl\-Zeile Optionen.  
  
Beachten Sie, dass, wenn Sie das Paket im SSIS-Katalog bereitgestellt, und Sie geben **SSIS-Katalog** als Paketquelle, ein Großteil dieser Informationen stammt automatisch aus dem Paket. Klicken Sie unter der **Konfiguration** Registerkarte können Sie angeben, die Umgebung, die Parameterwerte, die Verbindungs-Manager-Werte, die Eigenschaft überschreibt und angibt, ob das Paket ausgeführt wird, in eine 32\-Bit-Common Language Runtime-Umgebung.  
  
Führen Sie für Weitere Informationen zum Erstellen von Auftragsschritten, die [!INCLUDE[ssISnoversion](../content/includes/ssISnoversion_md.md)] -Paketen finden Sie [Aufträge des SQL Server-Agents für Pakete](assetId:///ecf7a5f9-b8a7-47f1-9ac0-bac07cb89e31).  
  
## Verwandte Aufgaben  
  
|||  
|-|-|  
|**Beschreibung**|**Thema**|  
|Beschreibt, wie ein Auftragsschritt mit einem ausführbaren Programm erstellt wird.|[Erstellen eines CmdExec-Auftragsschritts](../content/Create-a-CmdExec-Job-Step.md)|  
|Beschreibt, wie [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)]-Agent-Berechtigungen zurückgesetzt werden.|[Konfigurieren eines Benutzers zum Erstellen und Verwalten von SQL Server-Agent-Aufträgen](../content/Configure-a-User-to-Create-and-Manage-SQL-Server-Agent-Jobs.md)|  
|Beschreibt, wie ein [!INCLUDE[tsql](../content/includes/tsql_md.md)]-Auftragsschritt erstellt wird.|[Erstellen eines Transact-SQL-Auftragsschritts](../content/Create-a-Transact-SQL-Job-Step.md)|  
|Beschreibt, wie Optionen für Microsoft [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] Agent Transact\-SQL-Auftragsschritte.|[Definieren von Optionen für Transact-SQL-Auftragsschritte](../content/Define-Transact-SQL-Job-Step-Options.md)|  
|Beschreibt, wie ein ActiveX-Skript-Auftragsschritt erstellt wird.|[Erstellen eines ActiveX-Skript-Auftragsschritts](../content/Create-an-ActiveX-Script-Job-Step.md)|  
|Beschreibt, wie [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)]-Agent-Auftragsschritte erstellt und definiert werden, die [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] Analysis Services-Befehle und -Abfragen ausführen.|[Erstellen eines Analysis Services-Auftragsschritts](../content/Create-an-Analysis-Services-Job-Step.md)|  
|Beschreibt, welche Aktion [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] ausführen sollte, wenn während der Auftragsausführung ein Fehler auftritt.|[Festlegen der Vorgehensweise nach Erfolg oder Fehlschlagen eines Auftragsschritts](../content/Set-Job-Step-Success-or-Failure-Flow.md)|  
|Beschreibt, wie Auftragsschrittdetails im Dialogfeld Auftragsschritt-Eigenschaften angezeigt werden.|[Anzeigen von Auftragsschrittinformationen](../content/View-Job-Step-Information.md)|  
|Beschreibt, wie ein Auftragsschrittprotokoll des [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)]-Agents gelöscht wird.|[Löschen eines Auftragsschrittprotokolls](../content/Delete-a-Job-Step-Log.md)|  
  
## Siehe auch  
[sysjobstepslogs (Transact-SQL)](assetId:///128c25db-0b71-449d-bfb2-38b8abcf24a0)  
[Erstellen von Aufträgen](../content/Create-Jobs.md)  
[sp_add_job (Transact-SQL)](assetId:///6ca8fe2c-7b1c-4b59-b4c7-e3b7485df274)  
  
