---
title: "Entfernen von Schritten aus einem Masterauftrag f&#252;r den SQL Server-Agent"
ms.custom: na
ms.date: 07/15/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - tools-ssms
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 871e6162-1221-464d-8f7f-7e454dcd9edb
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
# Entfernen von Schritten aus einem Masterauftrag f&#252;r den SQL Server-Agent
In diesem Thema wird beschrieben, wie Sie Schritte aus einem Masterauftrag für den SQL Server-Agent in [!INCLUDE[ssCurrent](../content/includes/ssCurrent_md.md)] mithilfe von [!INCLUDE[ssManStudioFull](../content/includes/ssManStudioFull_md.md)] oder [!INCLUDE[tsql](../content/includes/tsql_md.md)]entfernen.  
  
**In diesem Thema**  
  
-   **Vorbereitungen:**  
  
    [Einschränkungen](#Restrictions)  
  
    [Sicherheit](#Security)  
  
-   **Entfernen von Schritten aus einem Masterauftrag für den SQL Server-Agent mit:**  
  
    [SQL Server Management Studio](#SSMSProcedure)  
  
    [Transact-SQL](#TsqlProcedure)  
  
## <a name="BeforeYouBegin"></a>Vorbereitungen  
  
### <a name="Restrictions"></a>Einschränkungen  
Ein Masterauftrag für den [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] -Agent kann nicht gleichzeitig lokale Server und Remoteserver als Ziel haben.  
  
### <a name="Security"></a>Sicherheit  
  
#### <a name="Permissions"></a>Berechtigungen  
Sie können nur Aufträge ändern, die in Ihrem Besitz sind, es sei denn, Sie sind ein Mitglied der festen Serverrolle **sysadmin** . Ausführliche Informationen finden Sie unter [Implement SQL Server Agent Security](../content/Implement-SQL-Server-Agent-Security.md).  
  
## <a name="SSMSProcedure"></a>Verwendung von SQL Server Management Studio  
  
#### So entfernen Sie Schritte aus einem Masterauftrag für den SQL Server-Agent  
  
1.  Klicken Sie im **Objekt-Explorer** auf das Pluszeichen, um den Server zu erweitern, der den Auftrag mit den zu löschenden Schritten enthält.  
  
2.  Klicken Sie auf das Pluszeichen, um **SQL Server-Agent**zu erweitern.  
  
3.  Klicken Sie auf das Pluszeichen, um den Ordner **Aufträge** zu erweitern.  
  
4.  Rechts\-Klicken Sie auf den Sinn, löschen die Schritte, und wählen Sie Auftrag **Eigenschaften**.  
  
5.  In der **Auftragseigenschaften –***Auftrag\_Namen* Dialogfeld **Wählen Sie eine Seite**, Option **Schritte**.  
  
6.  Wählen Sie unter **Auftragsschrittliste**den zu löschenden Auftragsschritt aus, und klicken Sie auf **Löschen**.  
  
7.  Wenn Sie fertig sind, klicken Sie auf **OK**.  
  
## <a name="TsqlProcedure"></a>Mithilfe von Transact\-SQL  
  
#### So entfernen Sie Schritte aus einem Masterauftrag für den SQL Server-Agent  
  
1.  Stellen Sie im Objekt-Explorer ** **eine Verbindung mit einer [!INCLUDE[ssDE](../content/includes/ssDE_md.md)]-Instanz her.  
  
2.  Klicken Sie in der Standardleiste auf **Neue Abfrage**.  
  
3.  Kopieren Sie das folgende Beispiel, fügen Sie es in das Abfragefenster ein, und klicken Sie auf **Ausführen**.  
  
    ```  
    -- removes job step 1 from the job Weekly Sales Data Backup   
    USE msdb ;  
    GO  
  
    EXEC dbo.sp_delete_jobstep  
        @job_name = N'Weekly Sales Data Backup',  
        @step_id = 1 ;  
    GO  
    ```  
  
Weitere Informationen finden Sie unter [Sp_delete_jobstep (Transact-SQL)](assetId:///421ede8e-ad57-474a-9fb9-92f70a3e77e3).  
  
