---
title: "Erstellen eines PowerShell-Skript-Auftragsschritts"
ms.custom: na
ms.date: 07/15/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - tools-ssms
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 50afcf84-fae0-4eb5-9b0f-f2cf144c1433
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
# Erstellen eines PowerShell-Skript-Auftragsschritts
In diesem Thema wird beschrieben, wie Sie einen Auftragsschritt des [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] -Agents erstellen und definieren, der in [!INCLUDE[ssCurrent](../content/includes/ssCurrent_md.md)] mithilfe von [!INCLUDE[ssManStudioFull](../content/includes/ssManStudioFull_md.md)] oder [!INCLUDE[tsql](../content/includes/tsql_md.md)]ein PowerShell-Skript ausführt.  
  
**In diesem Thema**  
  
-   **Vorbereitungen:**  
  
    [Sicherheit](#Security)  
  
-   **So erstellen Sie einen PowerShell-Skript-Auftragsschritt mit**  
  
    [SQL Server Management Studio](#SSMS)  
  
    [Transact-SQL](#TSQL)  
  
    [SQL Server Management Objects](#SMO)  
  
## <a name="BeforeYouBegin"></a>Vorbereitungen  
  
### <a name="Security"></a>Sicherheit  
Ausführliche Informationen finden Sie unter [Implement SQL Server Agent Security](../content/Implement-SQL-Server-Agent-Security.md).  
  
## <a name="SSMS"></a>Verwendung von SQL Server Management Studio  
  
#### So erstellen Sie einen PowerShell-Skript-Auftragsschritt  
  
1.  Stellen Sie im **Objekt-Explorer** eine Verbindung mit einer Instanz von [!INCLUDE[ssDEnoversion](../content/includes/ssDEnoversion_md.md)]her, und erweitern Sie dann diese Instanz.  
  
2.  Erweitern Sie **SQL Server-Agent**, erstellen Sie einen neuen Auftrag oder rechts\-Klicken Sie auf einen vorhandenen Auftrag aus, und klicken Sie dann auf **Eigenschaften**. Weitere Informationen zum Erstellen eines Auftrags finden Sie unter [Erstellen von Aufträgen](../content/Create-Jobs.md).  
  
3.  Klicken Sie im Dialogfeld **Auftragseigenschaften** auf die Seite **Schritte** und dann auf **Neu**.  
  
4.  Geben Sie im Dialogfeld **Neuer Auftragsschritt** unter **Schrittname**einen Schrittnamen für den Auftrag ein.  
  
5.  Klicken Sie in der Liste **Typ** auf **PowerShell**.  
  
6.  Wählen Sie in der Liste **Ausführen als** das Proxykonto mit den Anmeldeinformationen für den Auftrag aus.  
  
7.  Geben Sie im Feld **Befehl** die PowerShell-Skriptsyntax ein, die für den Auftragsschritt ausgeführt wird. Klicken Sie alternativ auf **Öffnen** , und wählen Sie eine Datei aus, die die Skriptsyntax enthält. Ein Beispiel für ein PowerShell-Skript, finden Sie unter **mithilfe von Transact\-SQL** unten.  
  
8.  Klicken Sie auf die Seite **Erweitert** , um die folgenden Optionen für den Auftragsschritt festzulegen: welche Aktion bei der erfolgreichen oder fehlerhaften Ausführung des Auftragsschrittes jeweils auszuführen ist, wie oft der [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] -Agent versuchen soll, den Auftragsschritt auszuführen, und wie viele Wiederholungsversuche unternommen werden sollen.  
  
## <a name="TSQL"></a>Mithilfe von Transact\-SQL  
  
#### So erstellen Sie einen PowerShell-Skript-Auftragsschritt  
  
1.  Stellen Sie im **Objekt-Explorer**eine Verbindung mit einer [!INCLUDE[ssDE](../content/includes/ssDE_md.md)]-Instanz her.  
  
2.  Klicken Sie in der Standardleiste auf **Neue Abfrage**.  
  
3.  Kopieren Sie das folgende Beispiel, fügen Sie es in das Abfragefenster ein, und klicken Sie auf **Ausführen**.  
  
    ```  
    -- creates a PowerShell job step that finds the processes that use more than 1000 MB of memory and kills them  
    USE msdb;  
    GO  
    EXEC sp_add_jobstep  
        @job_name = N'Weekly Sales Data Backup',  
        @step_name = N'Kills all processes that use more than 1000 MB of memory',  
        @subsystem = N'PowerShell',  
        @command = N'Get-Process | Where-Object { $_.WS -gt 1000MB } | Stop-Process',   
        @retry_attempts = 5,  
        @retry_interval = 5 ;  
    GO  
    ```  
  
Weitere Informationen finden Sie unter [Sp_add_jobstep (Transact-SQL)](assetId:///97900032-523d-49d6-9865-2734fba1c755).  
  
## <a name="SMO"></a>Verwendung von SQL Server Management Objects  
**So erstellen Sie einen PowerShell-Skript-Auftragsschritt**  
  
Verwenden der **JobStep** Klasse, indem Sie eine Programmiersprache, die Sie, wie z. B. Visual Basic, Visual C# auswählen\#, oder PowerShell.  
  
