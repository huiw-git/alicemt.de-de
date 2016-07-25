---
title: "Erstellen eines Auftrags"
ms.custom: na
ms.date: 07/15/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - tools-ssms
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: b35af2b6-6594-40d1-9861-4d5dd906048c
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
# Erstellen eines Auftrags
In diesem Thema wird beschrieben, wie Sie eine SQL Server-Agent-Auftragskategorie in [!INCLUDE[ssCurrent](../content/includes/ssCurrent_md.md)] mithilfe von [!INCLUDE[ssManStudioFull](../content/includes/ssManStudioFull_md.md)], [!INCLUDE[tsql](../content/includes/tsql_md.md)] oder SQL Server Management Objects (SMO) erstellen können.  
  
Informationen zum Hinzufügen von Auftragsschritten, Zeitplänen, Warnungen und Benachrichtigungen, die an Benutzer gesendet werden können, finden Sie in den Links im Abschnitt "Siehe auch".  
  
-   **Vorbereitungen:**  
  
    [Einschränkungen](#Restrictions)  
  
    [Sicherheit](#Security)  
  
-   **So erstellen Sie einen Auftrag Sicht mit**  
  
    [SQL Server Management Studio](#SSMSProcedure),  
  
    [Transact-SQL](#TsqlProcedure)  
  
    [SQL Server Management Objects](#SMOProcedure)  
  
## <a name="BeforeYouBegin"></a>Vorbereitungen  
  
### <a name="Restrictions"></a>Einschränkungen  
  
-   Um einen Auftrag erstellen zu können, muss ein Benutzer Mitglied einer der festen Datenbankrollen des [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] -Agents oder Mitglied der festen Serverrolle **sysadmin** sein. Ein Auftrag kann nur von seinem Besitzer bzw. Mitgliedern der **sysadmin** -Rolle bearbeitet werden. Weitere Informationen zu den [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] Agent festen Datenbankrollen finden Sie unter [SQL Server-Agent-festen Datenbankrollen](../content/SQL-Server-Agent-Fixed-Database-Roles.md).  
  
-   Wenn Sie einen Auftrag einem anderen Anmeldenamen zuweisen, ist nicht sichergestellt, dass die Berechtigungen des neuen Besitzers zum erfolgreichen Ausführen des Auftrags ausreichen.  
  
-   Lokale Aufträge werden vom lokalen [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)]-Agent zwischengespeichert. Aus diesem Grund alle Änderungen implizit zwingen [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] re-Agent\-Zwischenspeichern des Auftrags. Da [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] Agent zwischenspeichert, wenn der Auftrag erst **sp\_Hinzufügen\_Jobserver** wird aufgerufen, es ist effizienter, rufen Sie **sp\_Hinzufügen\_Jobserver** letzten.  
  
### <a name="Security"></a>Sicherheit  
  
-   Den Besitzer eines Auftrags können Sie nur ändern, wenn Sie als Systemadministrator angemeldet sind.  
  
-   Aus Sicherheitsgründen kann nur der Auftragsbesitzer bzw. ein Mitglied der **sysadmin** -Rolle die Definition des Auftrags ändern. Nur Mitglieder der festen Serverrolle **sysadmin** können anderen Benutzern den Auftragsbesitz zuweisen. Zudem können sie unabhängig vom Auftragsbesitzer alle Aufträge ausführen.  
  
    > [!NOTE]  
    > Wenn Auftragsbesitz einem Benutzer ändern, der kein Mitglied von der **Sysadmin** festen Serverrolle und der Auftrag Schritte ausgeführt werden, die Proxykonten erforderlich sind (z. B. [!INCLUDE[ssIS](../content/includes/ssIS_md.md)] Ausführung von Paketen), stellen Sie sicher, dass der Benutzer hat Zugriff auf dieses Proxykonto, sonst schlägt der Auftrag fehl.  
  
#### <a name="Permissions"></a>Berechtigungen  
Ausführliche Informationen finden Sie unter [Implement SQL Server Agent Security](../content/Implement-SQL-Server-Agent-Security.md).  
  
## <a name="SSMSProcedure"></a>Verwendung von SQL Server Management Studio  
  
#### So erstellen Sie einen Auftrag für den SQL Server-Agent  
  
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
  
#### So erstellen Sie einen Auftrag für den SQL Server-Agent  
  
1.  Stellen Sie im Objekt-Explorer ** **eine Verbindung mit einer [!INCLUDE[ssDE](../content/includes/ssDE_md.md)]-Instanz her.  
  
2.  Klicken Sie in der Standardleiste auf **Neue Abfrage**.  
  
3.  Kopieren Sie das folgende Beispiel, fügen Sie es in das Abfragefenster ein, und klicken Sie auf **Ausführen**.  
  
    ```  
    USE msdb ;  
    GO  
    EXEC dbo.sp_add_job  
        @job_name = N'Weekly Sales Data Backup' ;  
    GO  
    EXEC sp_add_jobstep  
        @job_name = N'Weekly Sales Data Backup',  
        @step_name = N'Set database to read only',  
        @subsystem = N'TSQL',  
        @command = N'ALTER DATABASE SALES SET READ_ONLY',   
        @retry_attempts = 5,  
        @retry_interval = 5 ;  
    GO  
    EXEC dbo.sp_add_schedule  
        @schedule_name = N'RunOnce',  
        @freq_type = 1,  
        @active_start_time = 233000 ;  
    USE msdb ;  
    GO  
    EXEC sp_attach_schedule  
       @job_name = N'Weekly Sales Data Backup',  
       @schedule_name = N'RunOnce';  
    GO  
    EXEC dbo.sp_add_jobserver  
        @job_name = N'Weekly Sales Data Backup';  
    GO  
    ```  
  
Weitere Informationen finden Sie in den folgenden Themen:  
  
-   [sp_add_job (Transact-SQL)](assetId:///6ca8fe2c-7b1c-4b59-b4c7-e3b7485df274)  
  
-   [sp_add_jobstep (Transact-SQL)](assetId:///97900032-523d-49d6-9865-2734fba1c755)  
  
-   [sp_add_schedule (Transact-SQL)](assetId:///9060aae3-3ddd-40a5-83bb-3ea7ab1ffbd7)  
  
-   [sp_attach_schedule (Transact-SQL)](assetId:///80c80eaf-cf23-4ed8-b8dd-65fe59830dd1)  
  
-   [sp_add_jobserver (Transact-SQL)](assetId:///485252cc-0081-490a-9bd1-cbbd68eea286)  
  
## <a name="SMOProcedure"></a>Verwendung von SQL Server Management Objects  
**So erstellen Sie einen Auftrag für den SQL Server-Agent**  
  
Rufen Sie die **Erstellen** Methode der **Auftrag** Klasse, indem Sie eine Programmiersprache, die Sie, wie z. B. Visual Basic, Visual C# auswählen\#, oder PowerShell. Beispielcode, finden Sie unter [Planen von automatischen, administrativen Tasks im SQL Server-Agent](assetId:///900242ad-d6a2-48e9-8a1b-f0eea4413c16).  
  
