---
title: "Hinzuf&#252;gen von Schritten zu einem Masterauftrag f&#252;r den SQL Server-Agent"
ms.custom: na
ms.date: 07/15/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - tools-ssms
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 9cc1e8ab-7ddc-427b-859e-203aa7e24642
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
# Hinzuf&#252;gen von Schritten zu einem Masterauftrag f&#252;r den SQL Server-Agent
In diesem Thema wird beschrieben, wie Sie einem Masterauftrag für den SQL Server-Agent in [!INCLUDE[ssCurrent](../content/includes/ssCurrent_md.md)] mithilfe von [!INCLUDE[ssManStudioFull](../content/includes/ssManStudioFull_md.md)] oder [!INCLUDE[tsql](../content/includes/tsql_md.md)]Schritte hinzufügen.  
  
**In diesem Thema**  
  
-   **Vorbereitungen:**  
  
    [Einschränkungen](#Restrictions)  
  
    [Sicherheit](#Security)  
  
-   **Hinzufügen von Schritten zu einem Masterauftrag für den SQL Server-Agent mit:**  
  
    [SQL Server Management Studio](#SSMSProcedure)  
  
    [Transact-SQL](#TsqlProcedure)  
  
## <a name="BeforeYouBegin"></a>Vorbereitungen  
  
### <a name="Restrictions"></a>Einschränkungen  
Ein Masterauftrag für den [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] -Agent kann nicht gleichzeitig lokale Server und Remoteserver als Ziel haben.  
  
### <a name="Security"></a>Sicherheit  
  
#### <a name="Permissions"></a>Berechtigungen  
Sie können nur Aufträge ändern, die in Ihrem Besitz sind, es sei denn, Sie sind ein Mitglied der festen Serverrolle **sysadmin** . Ausführliche Informationen finden Sie unter [Implement SQL Server Agent Security](../content/Implement-SQL-Server-Agent-Security.md).  
  
## <a name="SSMSProcedure"></a>Verwendung von SQL Server Management Studio  
  
#### So fügen Sie einem Masterauftrag für den SQL Server-Agent Schritte hinzu  
  
1.  Klicken Sie im **Objekt-Explorer** auf das Pluszeichen, um den Server zu erweitern, der den Auftrag enthält, dem Sie Schritte hinzufügen möchten.  
  
2.  Klicken Sie auf das Pluszeichen, um **SQL Server-Agent**zu erweitern.  
  
3.  Klicken Sie auf das Pluszeichen, um den Ordner **Aufträge** zu erweitern.  
  
4.  Rechts\-Klicken Sie auf den Auftrag, dem Sie Schritte hinzufügen, und wählen Sie möchten **Eigenschaften**.  
  
5.  In der **Auftragseigenschaften –***Auftrag\_Namen* Dialogfeld **Wählen Sie eine Seite**, Option **Schritte**. Weitere Informationen zu den Optionen auf dieser Seite finden Sie unter [Auftragseigenschaften - neuer Auftrag & #40; Seite & #41; die Schritte](../content/Job-Properties---New-Job--Steps-Page-.md).  
  
6.  Wenn Sie fertig sind, klicken Sie auf **OK**.  
  
## <a name="TsqlProcedure"></a>Mithilfe von Transact\-SQL  
  
#### So fügen Sie einem Masterauftrag für den SQL Server-Agent Schritte hinzu  
  
1.  Stellen Sie im Objekt-Explorer ** **eine Verbindung mit einer [!INCLUDE[ssDE](../content/includes/ssDE_md.md)]-Instanz her.  
  
2.  Klicken Sie in der Standardleiste auf **Neue Abfrage**.  
  
3.  Kopieren Sie das folgende Beispiel, fügen Sie es in das Abfragefenster ein, und klicken Sie auf **Ausführen**.  
  
    ```  
    -- creates a job step that changes database access to read-only for the Sales database.   
    -- specifies 5 retry attempts, with each retry to occur after a 5 minute wait.   
    -- assumes that the Weekly Sales Data Backup job already exists  
    USE msdb;  
    GO  
    EXEC sp_add_jobstep  
        @job_name = N'Weekly Sales Data Backup',  
        @step_name = N'Set database to read only',  
        @subsystem = N'TSQL',  
        @command = N'ALTER DATABASE SALES SET READ_ONLY',   
        @retry_attempts = 5,  
        @retry_interval = 5 ;  
    GO  
    ```  
  
Weitere Informationen finden Sie unter [Sp_add_jobstep (Transact-SQL)](assetId:///97900032-523d-49d6-9865-2734fba1c755).  
  
