---
title: "Erstellen eines CmdExec-Auftragsschritts"
ms.custom: na
ms.date: 07/15/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - tools-ssms
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: b48da5b4-6fe7-4eb7-bade-dc7d697c6d5c
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
# Erstellen eines CmdExec-Auftragsschritts
In diesem Thema wird beschrieben, wie Sie einen [!INCLUDE[msCoName](../content/includes/msCoName_md.md)] [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] -Agent-Auftragsschritt in [!INCLUDE[ssCurrent](../content/includes/ssCurrent_md.md)] , der ein ausführbares Programm oder einen Betriebssystembefehl verwendet, mithilfe von [!INCLUDE[ssManStudioFull](../content/includes/ssManStudioFull_md.md)], [!INCLUDE[tsql](../content/includes/tsql_md.md)] oder SQL Server Management Objects erstellen und definieren können.  
  
**In diesem Thema**  
  
-   **Vorbereitungen:**  
  
    [Sicherheit](#Security)  
  
-   **So erstellen Sie einen CmdExec-Auftragsschritt mit**  
  
    [SQL Server Management Studio](#SSMS)  
  
    [Transact-SQL](#TSQL)  
  
    [SQL Server Management Objects](#SMO)  
  
## <a name="BeforeYouBegin"></a>Vorbereitungen  
  
### <a name="Security"></a>Sicherheit  
Standardmäßig können nur Mitglieder der festen Serverrolle **sysadmin** CmdExec-Auftragsschritte erstellen. Diese Aufträge werden im Kontext des Kontos des SQL Server-Agent-Dienstes ausgeführt, außer der **sysadmin** -Benutzer erstellt ein Proxykonto. Benutzer, die keine Mitglieder der **sysadmin** -Rolle sind, können CmdExec-Auftragsschritte erstellen, wenn sie Zugriff auf ein CmdExec-Proxykonto haben.  
  
#### <a name="Permissions"></a>Berechtigungen  
Ausführliche Informationen finden Sie unter [Implement SQL Server Agent Security](../content/Implement-SQL-Server-Agent-Security.md).  
  
## <a name="SSMS"></a>Verwendung von SQL Server Management Studio  
  
#### So erstellen Sie einen CmdExec-Auftragsschritt  
  
1.  Stellen Sie im **Objekt-Explorer** eine Verbindung mit einer Instanz von [!INCLUDE[ssDEnoversion](../content/includes/ssDEnoversion_md.md)]her, und erweitern Sie dann diese Instanz.  
  
2.  Erweitern Sie **SQL Server-Agent**, erstellen Sie einen neuen Auftrag oder rechts\-Klicken Sie auf einen vorhandenen Auftrag aus, und klicken Sie dann auf **Eigenschaften**.  
  
3.  Klicken Sie im Dialogfeld **Auftragseigenschaften** auf die Seite **Schritte** und dann auf **Neu**.  
  
4.  Geben Sie im Dialogfeld **Neuer Auftragsschritt** unter **Schrittname**einen Schrittnamen für den Auftrag ein.  
  
5.  In den **Typ** wählen **Betriebssystem (CmdExec)**.  
  
6.  Wählen Sie in der Liste **Ausführen als** das Proxykonto mit den Anmeldeinformationen für den Auftrag aus. Standardmäßig werden CmdExec-Auftragsschritte im Kontext des Kontos des SQL Server-Agent-Dienstes ausgeführt.  
  
7.  Geben Sie in das Feld **Prozessexitcode eines erfolgreichen Befehls** einen Wert zwischen 0 und 999999 ein.  
  
8.  Geben Sie in das Feld **Befehl** den Betriebssystembefehl oder das ausführbare Programm ein. Finden Sie unter "Using Transact T\-SQL für ein Beispiel.  
  
9. Klicken Sie auf die Seite **Erweitert** , um Optionen für Auftragsschritte festzulegen, z. B. welche Aktion bei der erfolgreichen oder fehlerhaften Ausführung des Auftragsschrittes jeweils auszuführen ist, wie oft der [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] -Agent versuchen soll, den Auftragsschritt auszuführen, und in welche Datei der [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] -Agent die Auftragsschrittausgabe schreiben soll. Nur Mitglieder der festen Serverrolle **sysadmin** können die Auftragsschrittausgabe in eine Betriebssystemdatei schreiben.  
  
## <a name="TSQL"></a>Mithilfe von Transact\-SQL  
  
#### So erstellen Sie einen CmdExec-Auftragsschritt  
  
1.  Stellen Sie im **Objekt-Explorer**eine Verbindung mit einer [!INCLUDE[ssDE](../content/includes/ssDE_md.md)]-Instanz her.  
  
2.  Klicken Sie in der Standardleiste auf **Neue Abfrage**.  
  
3.  Kopieren Sie das folgende Beispiel, fügen Sie es in das Abfragefenster ein, und klicken Sie auf **Ausführen**.  
  
    ```  
    -- creates a job step that that uses CmdExec  
    USE msdb;  
    GO  
    EXEC sp_add_jobstep  
        @job_name = N'Weekly Sales Data Backup',  
        @step_name = N'Set database to read only',  
        @subsystem = N'CMDEXEC',  
        @command = C:\clickme_scripts\SQL11\PostBOLReorg GetHsX.exe',   
        @retry_attempts = 5,  
        @retry_interval = 5 ;  
    GO  
    ```  
  
Weitere Informationen finden Sie unter [Sp_add_jobstep (Transact-SQL)](assetId:///97900032-523d-49d6-9865-2734fba1c755)  
  
## <a name="SMO"></a>Verwendung von SQL Server Management Objects  
**So erstellen Sie einen CmdExec-Auftragsschritt**  
  
Verwenden der **JobStep** Klasse, indem Sie eine Programmiersprache, die Sie, wie z. B. Visual Basic, Visual C# auswählen\#, oder PowerShell.  
  
