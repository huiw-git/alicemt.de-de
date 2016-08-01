---
title: "Planen eines Auftrags"
ms.custom: na
ms.date: 07/27/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - tools-ssms
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: f626390a-a3df-4970-b7a7-a0529e4a109c
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
# Planen eines Auftrags
In diesem Thema wird beschrieben, wie ein [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] -Agent-Auftrag geplant wird.  
  
-   **Vorbereitungen:**   
  
    [Sicherheit](#Security)  
  
-   **So planen Sie einen Auftrag mit**  
  
    [SQL Server Management Studio](#SSMS)  
  
    [Transact-SQL](#TSQL)  
  
    [SQL Server Management Objects](#SMO)  
  
## <a name="BeforeYouBegin"></a>Vorbereitungen  
  
### <a name="Security"></a>Sicherheit  
Ausführliche Informationen finden Sie unter [Implement SQL Server Agent Security](../content/Implement-SQL-Server-Agent-Security.md).  
  
## <a name="SSMS"></a>Verwendung von SQL Server Management Studio  
  
#### So erstellen Sie einen Zeitplan und weisen ihn einem Auftrag zu  
  
1.  Stellen Sie im **Objekt-Explorer** eine Verbindung mit einer Instanz von [!INCLUDE[ssDEnoversion](../content/includes/ssDEnoversion_md.md)]her, und erweitern Sie dann diese Instanz.  
  
2.  Erweitern Sie **SQL Server-Agent**, erweitern Sie **Aufträge**, mit der rechten Maustaste\-Klicken Sie auf den Auftrag, die Sie planen möchten, und klicken Sie auf **Eigenschaften**.  
  
3.  Wählen Sie die Seite **Zeitpläne** aus, und klicken Sie dann auf **Neu**.  
  
4.  Geben Sie in das Feld **Name** einen Namen für den neuen Zeitplan ein.  
  
5.  Deaktivieren Sie das Kontrollkästchen **Aktiviert** , wenn der Zeitplan nicht unmittelbar nach seiner Erstellung wirksam werden soll.  
  
6.  Wählen Sie für **Zeitplantyp**eine der folgenden Möglichkeiten aus:  
  
    -   Klicken Sie auf **Automatisch starten, wenn der SQL Server-Agent startet** , um den Auftrag zu starten, wenn der [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] -Agent-Dienst gestartet wird.  
  
    -   Klicken Sie auf **Starten, wenn sich die CPUs im Leerlauf befinden** , um den Auftrag zu starten, wenn die CPUs eine Leerlaufbedingung erfüllen.  
  
    -   Klicken Sie auf **Wiederholt** , wenn ein Zeitplan wiederholt ausgeführt werden soll. Um den wiederholten Zeitplan festzulegen, vervollständigen Sie im Dialogfeld die Gruppen **Häufigkeit**, **Häufigkeit pro Tag**und **Dauer** .  
  
    -   Klicken Sie auf **Einmal** , wenn der Zeitplan nur einmal ausgeführt werden soll. Festlegen der **einmal** Planen, führen Sie die **ein\-Zeit vorkommen** im Dialogfeld Gruppe.  
  
#### So weisen Sie einen Zeitplan einem Auftrag zu  
  
1.  Stellen Sie im **Objekt-Explorer** eine Verbindung mit einer Instanz von [!INCLUDE[ssDEnoversion](../content/includes/ssDEnoversion_md.md)]her, und erweitern Sie dann diese Instanz.  
  
2.  Erweitern Sie **SQL Server-Agent**, erweitern Sie **Aufträge**, mit der rechten Maustaste\-Klicken Sie auf den Auftrag, den Sie planen möchten, und klicken Sie auf **Eigenschaften**.  
  
3.  Wählen Sie die Seite **Zeitpläne** aus, und klicken Sie dann auf **Auswählen**.  
  
4.  Wählen Sie den Zeitplan aus, den Sie zuweisen möchten, und klicken Sie auf **OK**.  
  
5.  In der **Auftragseigenschaften** Dialogfeld doppelte\-Klicken Sie auf den zugewiesenen Zeitplan.  
  
6.  Überprüfen Sie, ob das **Startdatum** ordnungsgemäß festgelegt ist. Falls nicht, legen Sie das Datum fest, an dem der Zeitplan starten soll, und klicken Sie auf **OK**.  
  
7.  Klicken Sie im Dialogfeld **Auftragseigenschaften** auf **OK**.  
  
## <a name="TSQL"></a>Mithilfe von Transact\-SQL  
  
#### So planen Sie einen Auftrag  
  
1.  Stellen Sie im **Objekt-Explorer**eine Verbindung mit einer [!INCLUDE[ssDE](../content/includes/ssDE_md.md)]-Instanz her.  
  
2.  Klicken Sie in der Standardleiste auf **Neue Abfrage**.  
  
3.  Kopieren Sie das folgende Beispiel, fügen Sie es in das Abfragefenster ein, und klicken Sie auf **Ausführen**.  
  
    ```  
    USE msdb ;  
    GO  
    -- creates a schedule named NightlyJobs.   
    -- Jobs that use this schedule execute every day when the time on the server is 01:00.   
    EXEC sp_add_schedule  
        @schedule_name = N'NightlyJobs' ,  
        @freq_type = 4,  
        @freq_interval = 1,  
        @active_start_time = 010000 ;  
    GO  
    -- attaches the schedule to the job BackupDatabase  
    EXEC sp_attach_schedule  
       @job_name = N'BackupDatabase',  
       @schedule_name = N'NightlyJobs' ;  
    GO  
    ```  
  
Weitere Informationen finden Sie unter [Sp_add_schedule (Transact-SQL)](assetId:///9060aae3-3ddd-40a5-83bb-3ea7ab1ffbd7) und [Sp_attach_schedule (Transact-SQL)](assetId:///80c80eaf-cf23-4ed8-b8dd-65fe59830dd1).  
  
## <a name="SMO"></a>Verwendung von SQL Server Management Objects  
Verwenden der **JobSchedule** Klasse, indem Sie eine Programmiersprache, die Sie, wie z. B. Visual Basic, Visual C# auswählen\#, oder PowerShell. Weitere Informationen finden Sie unter[SQL Server Management Objects (SMO)](http://msdn.microsoft.com/library/ms162169.aspx).  
  
