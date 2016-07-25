---
title: "Erstellen eines Transact-SQL-Auftragsschritts"
ms.custom: na
ms.date: 07/15/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - tools-ssms
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 69c571a7-debe-4063-9d38-e4b6a1e8e84c
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
# Erstellen eines Transact-SQL-Auftragsschritts
In diesem Thema wird beschrieben, wie Sie einen Auftragsschritt des [!INCLUDE[msCoName](../content/includes/msCoName_md.md)] [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] -Agents, der [!INCLUDE[tsql](../content/includes/tsql_md.md)] - Skripts in [!INCLUDE[ssCurrent](../content/includes/ssCurrent_md.md)] mithilfe von [!INCLUDE[ssManStudioFull](../content/includes/ssManStudioFull_md.md)], [!INCLUDE[tsql](../content/includes/tsql_md.md)]oder SQL Server Management Objects ausführt, erstellen können.  
  
Diese Auftragsschrittskripts können gespeicherte Prozeduren und erweiterte gespeicherte Prozeduren aufrufen. Ein einzelner [!INCLUDE[tsql](../content/includes/tsql_md.md)] -Auftragsschritt kann mehrere Batches und eingebettete GO-Befehle enthalten. Weitere Informationen zum Erstellen eines Auftrags finden Sie unter [Erstellen von Aufträgen](../content/Create-Jobs.md).  
  
**In diesem Thema**  
  
-   **Vorbereitungen:**  
  
    [Sicherheit](#Security)  
  
-   **Erstellen Sie ein Transact\-SQL-Auftragsschritt mit:**  
  
    [SQL Server Management Studio](#SSMS)  
  
    [Transact-SQL](#TSQL)  
  
    [SQL Server Management Objects](#SMO)  
  
## <a name="BeforeYouBegin"></a>Vorbereitungen  
  
### <a name="Security"></a>Sicherheit  
Ausführliche Informationen finden Sie unter [Implement SQL Server Agent Security](../content/Implement-SQL-Server-Agent-Security.md).  
  
## <a name="SSMS"></a>Verwendung von SQL Server Management Studio  
  
#### Erstellen Sie ein Transact\-SQL-Auftragsschritt  
  
1.  Stellen Sie im **Objekt-Explorer** eine Verbindung mit einer Instanz von [!INCLUDE[ssDEnoversion](../content/includes/ssDEnoversion_md.md)]her, und erweitern Sie dann diese Instanz.  
  
2.  Erweitern Sie **SQL Server-Agent**, erstellen Sie einen neuen Auftrag oder rechts\-Klicken Sie auf einen vorhandenen Auftrag aus, und klicken Sie dann auf **Eigenschaften**.  
  
3.  Klicken Sie im Dialogfeld **Auftragseigenschaften** auf die Seite **Schritte** und dann auf **Neu**.  
  
4.  Geben Sie im Dialogfeld **Neuer Auftragsschritt** unter **Schrittname**einen Schrittnamen für den Auftrag ein.  
  
5.  In den **Typ** auf **Transact\-SQL-Skript (TSQL)**.  
  
6.  Geben Sie im Feld **Befehl** die [!INCLUDE[tsql](../content/includes/tsql_md.md)] -Befehlsbatches ein, oder klicken Sie auf **Öffnen** , um eine [!INCLUDE[tsql](../content/includes/tsql_md.md)] -Datei auszuwählen, die als Befehl verwendet werden soll.  
  
7.  Klicken Sie auf **Analysieren** , um die Syntax zu überprüfen.  
  
8.  Wenn die Syntax richtig ist, wird die Meldung "Analyse erfolgreich" angezeigt. Wenn ein Fehler gefunden wird, müssen Sie die Syntax korrigieren, bevor Sie den Vorgang fortsetzen.  
  
9. Klicken Sie auf die Seite **Erweitert** , um Optionen für Auftragsschritte festzulegen, z.&amp;nbsp;B. welche Aktion ausgeführt werden soll, wenn ein Auftragsschritt erfolgreich ausgeführt wird oder einen Fehler erzeugt, wie häufig der [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] -Agent versuchen soll, den Auftragsschritt auszuführen, und in welche Datei oder Tabelle der [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] -Agent die Auftragsschrittausgabe schreiben soll. Nur Mitglieder der festen Serverrolle **sysadmin** können die Auftragsschrittausgabe in eine Betriebssystemdatei schreiben. Alle Benutzer des SQL Server-Agents können die Ausgabe in einer Tabelle protokollieren.  
  
10. Wenn Sie ein Mitglied der festen Serverrolle **sysadmin** sind und diesen Auftragsschritt unter einem anderen SQL-Anmeldenamen ausführen möchten, wählen Sie den SQL-Anmeldenamen in der Liste **Ausführen als Benutzer** aus.  
  
## <a name="TSQL"></a>Mithilfe von Transact\-SQL  
  
#### Erstellen Sie ein Transact\-SQL-Auftragsschritt  
  
1.  Stellen Sie im Objekt-Explorer ** **eine Verbindung mit einer [!INCLUDE[ssDE](../content/includes/ssDE_md.md)]-Instanz her.  
  
2.  Klicken Sie in der Standardleiste auf **Neue Abfrage**.  
  
3.  Kopieren Sie das folgende Beispiel, fügen Sie es in das Abfragefenster ein, und klicken Sie auf **Ausführen**.  
  
    ```  
    -- creates a job step that that uses Transact-SQL  
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
  
## <a name="SMO"></a>Verwendung von SQL Server Management Objects  
**Erstellen Sie ein Transact\-SQL-Auftragsschritt**  
  
Verwenden der **JobStep** Klasse, indem Sie eine Programmiersprache, die Sie, wie z. B. Visual Basic, Visual C# auswählen\#, oder PowerShell.  
  
