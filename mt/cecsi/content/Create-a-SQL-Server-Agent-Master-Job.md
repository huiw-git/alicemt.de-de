---
title: "Erstellen eines Masterauftrag f&#252;r den SQL Server-Agent"
ms.custom: na
ms.date: 07/15/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - tools-ssms
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: c12ab23f-d7ee-43a5-8cd2-0a9121292bcd
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
# Erstellen eines Masterauftrag f&#252;r den SQL Server-Agent
In diesem Thema wird beschrieben, wie einen Master erstellt [!INCLUDE[msCoName](../content/includes/msCoName_md.md)] [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] Agent-Auftrag in [!INCLUDE[ssCurrent](../content/includes/ssCurrent_md.md)] mit [!INCLUDE[ssManStudioFull](../content/includes/ssManStudioFull_md.md)] oder [!INCLUDE[tsql](../content/includes/tsql_md.md)].  
  
**In diesem Thema**  
  
-   **Vorbereitungen:**  
  
    [Einschränkungen](#Restrictions)  
  
    [Sicherheit](#Security)  
  
-   **So erstellen Sie einen Masterauftrag für den SQL Server-Agent mit**  
  
    [SQL Server Management Studio](#SSMSProcedure)  
  
    [Transact-SQL](#TsqlProcedure)  
  
## <a name="BeforeYouBegin"></a>Vorbereitungen  
  
### <a name="Restrictions"></a>Einschränkungen  
Änderungen an Masteraufträgen für den [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)]-Agent müssen an alle beteiligten Zielserver weitergegeben werden. Da Zielserver einen Auftrag erst herunterladen, wenn diese Ziele angegeben werden, empfiehlt [!INCLUDE[msCoName](../content/includes/msCoName_md.md)], alle Auftragsschritte und -zeitpläne für einen bestimmten Auftrag abzuschließen, bevor Sie Zielserver angeben. Andernfalls müssen Sie manuell anfordern, dass die Zielserver des geänderten Auftrags erneut herunterladen, entweder durch Ausführen der **sp\_buchen\_Msx\_Vorgang** gespeicherte Prozedur oder ändern den Auftrag mithilfe [!INCLUDE[ssManStudioFull](../content/includes/ssManStudioFull_md.md)]. Weitere Informationen finden Sie unter [Sp_post_msx_operation (Transact-SQL)](assetId:///085deef8-2709-4da9-bb97-9ab32effdacf) oder [Ändern eines Auftrags](../content/Modify-a-Job.md).  
  
### <a name="Security"></a>Sicherheit  
  
#### <a name="Permissions"></a>Berechtigungen  
Verteilte Aufträge mit Schritten, die einem Proxy zugeordnet sind, werden im Kontext des Proxykontos auf dem Zielserver ausgeführt. Stellen Sie sicher, dass die folgenden Bedingungen erfüllt sind, da andernfalls einem Proxy zugeordnete Auftragsschritte nicht vom Masterserver auf den Zielserver heruntergeladen werden:  
  
-   Der Registrierungsunterschlüssel **\\HKEY\_lokalen\_Computer\\SOFTWARE\\Microsoft\\Microsoft SQL Server\\< & #42; Instanz\_Name & #42; >\\SQL Server-Agent\\AllowDownloadedJobsToMatchProxyName** (REG\_DWORD) auf 1 (True) festgelegt ist. Dieser Unterschlüssel ist standardmäßig auf 0 (false) festgelegt.  
  
-   Auf dem Zielserver ist ein Proxykonto vorhanden, das den gleichen Namen wie das Proxykonto des Masterservers hat, unter dem der Auftragsschritt ausgeführt wird.  
  
Wenn Auftragsschritte, die Verwendung von Proxykonten fehlschlagen, wenn sie auf dem Zielserver vom Masterserver herunterladen können Sie überprüfen die **Fehler\_Nachricht** -Spalte in der **Sysdownloadlist** -Tabelle in der **Msdb** Datenbank für die folgenden Fehlermeldungen:  
  
-   "Für den Auftragsschritt ist ein Proxykonto erforderlich, das Proxyabgleichen ist auf dem Zielserver aber deaktiviert." Um diesen Fehler zu beheben, legen Sie den Registrierungsunterschlüssel **AllowDownloadedJobsToMatchProxyName** auf 1 fest.  
  
-   "Proxy nicht gefunden." Um diesen Fehler zu beheben, stellen Sie sicher, dass auf dem Zielserver ein Proxykonto vorhanden ist, das den gleichen Namen wie das Proxykonto des Masterservers hat, unter dem der Auftragsschritt ausgeführt wird.  
  
## <a name="SSMSProcedure"></a>Verwendung von SQL Server Management Studio  
  
#### So erstellen Sie einen Masterauftrag für den SQL Server-Agent  
  
1.  Klicken Sie im Objekt-Explorer ****auf das Pluszeichen, um den Server zu erweitern, auf dem Sie den SQL Server-Agent-Auftrag erstellen möchten.  
  
2.  Klicken Sie auf das Pluszeichen, um **SQL Server-Agent**zu erweitern.  
  
3.  Rechts\-Klicken Sie auf die **Aufträge** Ordner und wählen Sie **Neuer Auftrag**.  
  
4.  Ändern Sie im Dialogfeld **Neuer Auftrag** auf der Seite **Allgemein** die allgemeinen Eigenschaften des Auftrags. Weitere Informationen zu den Optionen auf dieser Seite finden Sie unter [Auftragseigenschaften - neuer Auftrag & #40; Seite "Allgemein" & #41;](../content/Job-Properties---New-Job--General-Page-.md)  
  
5.  Organisieren Sie die Auftragsschritte auf der Seite **Schritte** . Weitere Informationen zu den Optionen auf dieser Seite finden Sie unter [Auftragseigenschaften - neuer Auftrag & #40; Schrittseite & #41;](../content/Job-Properties---New-Job--Steps-Page-.md)  
  
6.  Organisieren Sie auf der Seite **Zeitpläne** Zeitpläne für den Auftrag. Weitere Informationen zu den Optionen auf dieser Seite finden Sie unter [Auftragseigenschaften - neuer Auftrag & #40; Seite "Zeitpläne" & #41;](../content/Job-Properties---New-Job--Schedules-Page-.md)  
  
7.  Organisieren Sie auf der Seite **Warnungen** die Warnungen für den Auftrag. Weitere Informationen zu den Optionen auf dieser Seite finden Sie unter [Auftragseigenschaften - neuer Auftrag & #40; Seite "Warnungen" & #41;](../content/Job-Properties---New-Job--Alerts-Page-.md)  
  
8.  Legen Sie auf der Seite **Benachrichtigungen** die Aktionen für den [!INCLUDE[msCoName](../content/includes/msCoName_md.md)] [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] -Agent fest, die bei Abschluss des Auftrags auszuführen sind. Weitere Informationen zu den Optionen auf dieser Seite finden Sie unter [Auftragseigenschaften - neuer Auftrag & #40; Benachrichtigungsseite & #41;](../content/Job-Properties---New-Job--Notifications-Page-.md).  
  
9. Verwalten Sie auf der Seite **Ziele** die Zielserver für den Auftrag. Weitere Informationen zu den Optionen auf dieser Seite finden Sie unter [Auftragseigenschaften - neuer Auftrag & #40; Seite & #41; abzielt](../content/Job-Properties---New-Job--Targets-Page-.md).  
  
10. Wenn Sie fertig sind, klicken Sie auf **OK**.  
  
## <a name="TsqlProcedure"></a>Mithilfe von Transact\-SQL  
  
#### So erstellen Sie einen Masterauftrag für den SQL Server-Agent  
  
1.  Stellen Sie im Objekt-Explorer ** **eine Verbindung mit einer [!INCLUDE[ssDE](../content/includes/ssDE_md.md)]-Instanz her.  
  
2.  Klicken Sie in der Standardleiste auf **Neue Abfrage**.  
  
3.  Kopieren Sie das folgende Beispiel, fügen Sie es in das Abfragefenster ein, und klicken Sie auf **Ausführen**.  
  
    ```  
    USE msdb ;  
    GO  
    -- Adds a new job executed by the SQLServerAgent service called 'Weekly Sales Data Backup'  
    EXEC dbo.sp_add_job  
        @job_name = N'Weekly Sales Data Backup' ;  
    GO  
    -- Adds a step (operation) to the 'Weekly Sales Data Backup' job.  
    EXEC sp_add_jobstep  
        @job_name = N'Weekly Sales Data Backup',  
        @step_name = N'Set database to read only',  
        @subsystem = N'TSQL',  
        @command = N'ALTER DATABASE SALES SET READ_ONLY',   
        @retry_attempts = 5,  
        @retry_interval = 5 ;  
    GO  
    -- Creates a schedule called RunOnce  
    EXEC dbo.sp_add_schedule  
        @schedule_name = N'RunOnce',  
        @freq_type = 1,  
        @active_start_time = 233000 ;  
    USE msdb ;  
    GO  
    -- Sets the 'RunOnce' schedule to the "Weekly Sales Data Backup' Job  
    EXEC sp_attach_schedule  
       @job_name = N'Weekly Sales Data Backup',  
       @schedule_name = N'RunOnce';  
    GO  
    -- assigns the multiserver job Weekly Sales Backups to the server SEATTLE2  
    -- assumes that SEATTLE2 is registered as a target server for the current instance.  
    EXEC dbo.sp_add_jobserver  
        @job_name = N'Weekly Sales Data Backups',  
        @server_name = N'SEATTLE2' ;  
    GO  
    ```  
  
Weitere Informationen finden Sie in den folgenden Themen:  
  
-   [sp_add_job (Transact-SQL)](assetId:///6ca8fe2c-7b1c-4b59-b4c7-e3b7485df274)  
  
-   [sp_add_jobstep (Transact-SQL)](assetId:///97900032-523d-49d6-9865-2734fba1c755)  
  
-   [sp_add_schedule (Transact-SQL)](assetId:///9060aae3-3ddd-40a5-83bb-3ea7ab1ffbd7)  
  
-   [sp_attach_schedule (Transact-SQL)](assetId:///80c80eaf-cf23-4ed8-b8dd-65fe59830dd1)  
  
-   [sp_add_jobserver (Transact-SQL)](assetId:///485252cc-0081-490a-9bd1-cbbd68eea286)  
  
