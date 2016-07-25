---
title: "Festlegen der Vorgehensweise nach Erfolg oder Fehlschlagen eines Auftragsschritts"
ms.custom: na
ms.date: 07/15/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - tools-ssms
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 23041ccf-8a07-41d3-85b9-c449a54b7e1e
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
# Festlegen der Vorgehensweise nach Erfolg oder Fehlschlagen eines Auftragsschritts
Bei der Erstellung von [!INCLUDE[msCoName](../content/includes/msCoName_md.md)] [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] -Agent-Aufträgen können Sie angeben, welche Aktion von [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] ausgeführt werden soll, wenn während der Auftragsausführung ein Fehler auftritt. Bestimmen Sie die Aktion, die von [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] nach Erfolg oder Fehlschlagen eines Auftragsschrittes ausgeführt wird. Verwenden Sie anschließend die folgende Prozedur, um mithilfe des [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] -Agents die Logik der Vorgehensweise für die Auftragsschrittaktion zu konfigurieren.  
  
-   **Vorbereitungen:**  
  
    [Sicherheit](#Security)  
  
-   **So legen Sie die Vorgehensweise nach Erfolg oder einem Fehler eines Auftragsschritts fest, und zwar mit**  
  
    [SQL Server Management Studio](#SSMS)  
  
    [Transact-SQL](#TSQL)  
  
    [SQL Server Management Objects](#SMO)  
  
## Vorbereitungen  
  
### <a name="Security"></a>Sicherheit  
Ausführliche Informationen finden Sie unter [Implement SQL Server Agent Security](../content/Implement-SQL-Server-Agent-Security.md).  
  
## <a name="SSMS"></a>Verwendung von SQL Server Management Studio  
  
#### So legen Sie die Vorgehensweise nach Erfolg oder Fehlschlagen eines Auftragsschrittes fest  
  
1.  Erweitern Sie in **Objekt-Explorer**den Eintrag **SQL Server-Agent**, und erweitern Sie anschließend **Aufträge**.  
  
2.  Rechts\-Klicken Sie auf den Auftrag zu bearbeiten, und klicken Sie dann auf **Eigenschaften**.  
  
3.  Wählen Sie die Seite **Schritte** aus, und klicken Sie erst auf einen Schritt und dann auf **Bearbeiten**.  
  
4.  Wählen Sie im Dialogfeld **Auftragsschritt-Eigenschaften** die Seite **Erweitert** aus.  
  
5.  Wählen Sie im Dialogfeld **Aktion bei Erfolg**auf die Aktion, die nach erfolgreicher Durchführung des Auftragsschrittes ausgeführt werden soll.  
  
6.  Geben Sie im Feld **Wiederholungsversuche** mit einer Zahl zwischen 0 und 9999 an, wie oft der Auftragsschritt wiederholt werden soll, bevor er als fehlgeschlagen gilt. Wenn Sie einen Wert größer 0 eingegeben haben die **Wiederholungsversuche** Geben Sie der **Intervall für Verbindungsversuche (Minuten)** Feld die Anzahl der Minuten zwischen 1 und 9999 ein, die verstreichen müssen, bevor der Auftragsschritt erneut versucht wird.  
  
7.  Klicken Sie in der Liste **Aktion bei Fehler** auf die Aktion, die nach einem fehlgeschlagenen Auftragsschritt ausgeführt werden soll.  
  
8.  Wenn es sich bei dem Auftrag um ein [!INCLUDE[tsql](../content/includes/tsql_md.md)] -Skript handelt, können Sie eine der folgenden Optionen auswählen:  
  
    -   Geben Sie im Feld **Ausgabedatei** den Namen der Ausgabedatei ein, in die die Skriptausgabe geschrieben werden soll. Diese Datei wird standardmäßig bei jeder Ausführung des Auftragsschrittes überschrieben. Wenn Sie nicht möchten, dass die Ausgabedatei überschrieben wird, aktivieren Sie **Ausgabe an vorhandene Datei anfügen**.  
  
    -   Aktivieren Sie **In Tabelle protokollieren** , wenn der Auftragsschritt in einer Datenbanktabelle protokolliert werden soll. Standardmäßig wird der Tabelleninhalt bei jeder Ausführung des Auftragsschrittes überschrieben. Wenn der Tabelleninhalt nicht überschrieben werden soll, aktivieren Sie **Ausgabe an vorhandenen Eintrag in Tabelle anfügen**. Nachdem der Auftragsschritt ausgeführt wurde, können Sie den Inhalt dieser Tabelle anzeigen, indem Sie auf **Anzeigen**klicken.  
  
    -   Aktivieren Sie **Schrittausgabe in Verlauf einschließen** , wenn die Ausgabe in den Schrittverlauf eingeschlossen werden soll. Die Ausgabe wird nur angezeigt, wenn keine Fehler auftraten. Es kann auch vorkommen, dass die Ausgabe abgeschnitten wird.  
  
9. Wenn die Liste **Als Benutzer ausführen** verfügbar ist, wählen Sie daraus das Proxykonto mit den Benutzerinformationen aus, das für den Auftrag verwendet werden wird.  
  
## <a name="TSQL"></a>Mithilfe von Transact\-SQL  
  
#### So legen Sie die Vorgehensweise nach Erfolg oder Fehlschlagen eines Auftragsschrittes fest  
  
1.  Stellen Sie im **Objekt-Explorer**eine Verbindung mit einer [!INCLUDE[ssDE](../content/includes/ssDE_md.md)]-Instanz her.  
  
2.  Klicken Sie in der Standardleiste auf **Neue Abfrage**.  
  
3.  Kopieren Sie das folgende Beispiel, fügen Sie es in das Abfragefenster ein, und klicken Sie auf **Ausführen**.  
  
    ```  
    USE msdb;  
    GO  
    EXEC sp_add_jobstep  
        @job_name = N'Weekly Sales Data Backup',  
        @step_name = N'Set database to read only',  
        @subsystem = N'TSQL',  
        @command = N'ALTER DATABASE SALES SET READ_ONLY',   
        @on_success_action = 1;  
    GO  
    ```  
  
Weitere Informationen finden Sie unter [Sp_add_jobstep (Transact-SQL)](assetId:///97900032-523d-49d6-9865-2734fba1c755).  
  
## <a name="SMO"></a>Verwendung von SQL Server Management Objects  
**So legen Sie die Vorgehensweise nach Erfolg oder Fehlschlagen eines Auftragsschrittes fest**  
  
Verwenden der **JobStep** Klasse, indem Sie eine Programmiersprache, die Sie, wie z. B. Visual Basic, Visual C# auswählen\#, oder PowerShell. Weitere Informationen finden Sie unter [SQL Server Management Objects (SMO)](http://msdn.microsoft.com/library/ms162169.aspx).  
  
