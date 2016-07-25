---
title: "Schreiben des Auftragsstatus in das Windows-Anwendungsprotokoll"
ms.custom: na
ms.date: 07/15/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - tools-ssms
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 3b813702-8f61-40ec-bf3b-ce9deb7e68be
caps.latest.revision: 4
caps.handback.revision: 3
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
# Schreiben des Auftragsstatus in das Windows-Anwendungsprotokoll
In diesem Thema wird beschrieben, wie Sie den [!INCLUDE[msCoName](../content/includes/msCoName_md.md)] [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] -Agent in [!INCLUDE[ssCurrent](../content/includes/ssCurrent_md.md)] konfigurieren müssen, damit der Auftragsstatus mithilfe von [!INCLUDE[ssManStudioFull](../content/includes/ssManStudioFull_md.md)], [!INCLUDE[tsql](../content/includes/tsql_md.md)], oder SQL Server Management Objects in das Windows Anwendungsereignisprotokoll geschrieben wird.  
  
Sie stellen sicher, dass Datenbankadministratoren wissen, wann Aufträge fertig gestellt sind und wie oft diese ausgeführt werden. Zu den typischen Auftragsantworten gehören folgende:  
  
-   Benachrichtigen den Operator per e\-e-Mail, elektronische auslagern, oder ein **net Send** Nachricht. Verwenden Sie eine dieser Auftragsantworten, wenn der Operator Schritte ausführen muss\-Aktion einrichten. Wenn beispielsweise ein Sicherungsauftrag erfolgreich ausgeführt wurde, muss der Operator darüber informiert werden, um das Sicherungsband entfernen zu können und an einem sicheren Standort aufbewahren zu lassen.  
  
-   Schreiben einer Ereignismeldung in das Windows-Anwendungsprotokoll. Diese Art der Antwort können Sie nur bei fehlgeschlagenen Aufträgen verwenden.  
  
-   Automatisches Löschen des Auftrags. Verwenden Sie diese Auftragsantwort, wenn Sie sicher sind, dass Sie diesen Auftrag nicht erneut ausführen müssen.  
  
**In diesem Thema**  
  
-   **Vorbereitungen:**  
  
    [Sicherheit](#Security)  
  
-   **So schreiben Sie den Auftragsstatus in das Windows-Anwendungsprotokoll, und zwar mit**  
  
    [SQL Server Management Studio](#SSMS)  
  
    [SQL Server Management Objects](#SMO)  
  
## <a name="BeforeYouBegin"></a>Vorbereitungen  
  
### <a name="Security"></a>Sicherheit  
Ausführliche Informationen finden Sie unter [Implement SQL Server Agent Security](../content/Implement-SQL-Server-Agent-Security.md).  
  
## <a name="SSMS"></a>Verwendung von SQL Server Management Studio  
  
#### So schreiben Sie den Auftragsstatus in das Windows-Anwendungsprotokoll  
  
1.  Stellen Sie im **Objekt-Explorer** eine Verbindung mit einer Instanz von [!INCLUDE[ssDEnoversion](../content/includes/ssDEnoversion_md.md)]her, und erweitern Sie dann diese Instanz.  
  
2.  Erweitern Sie **SQL Server-Agent**, erweitern Sie **Aufträge**, mit der rechten Maustaste\-Klicken Sie auf den Auftrag zu bearbeiten, und klicken Sie dann auf **Eigenschaften**.  
  
3.  Wählen Sie die Seite **Benachrichtigungen** aus.  
  
4.  Aktivieren Sie **In Windows-Anwendungsereignisprotokoll schreiben**, und wählen Sie eine der folgenden Optionen aus:  
  
    -   Klicken Sie auf**Bei erfolgreicher Auftragsausführung**, um den Auftragsstatus zu protokollieren, wenn der Auftrag erfolgreich abgeschlossen wurde.  
  
    -   Klicken Sie auf**Bei Auftragsfehler**, um den Auftragsstatus zu protokollieren, wenn der Auftrag nicht erfolgreich abgeschlossen wurde.  
  
    -   Klicken Sie auf**Beim Abschluss des Auftrags** , um den Auftragsstatus unabhängig vom Abschlussstatus zu protokollieren.  
  
## <a name="SMO"></a>Verwendung von SQL Server Management Objects  
**So schreiben Sie den Auftragsstatus in das Windows-Anwendungsprotokoll**  
  
Rufen Sie die **EventLogLevel** Eigenschaft der **Auftrag** Klasse, indem Sie eine Programmiersprache, die Sie, wie z. B. Visual Basic, Visual C# auswählen\#, oder PowerShell.  
  
Im folgenden Codebeispiel wird der Auftrag so festgelegt, dass bei Abschluss der Auftragsausführung ein Betriebssystem-Ereignisprotokolleintrag generiert wird.  
  
**PowerShell**  
  
```  
$srv = new-object Microsoft.SqlServer.Management.Smo.Server("(local)")  
$jb = new-object Microsoft.SqlServer.Management.Smo.Agent.Job($srv.JobServer, "Test Job")  
$jb.EventLogLevel = [Microsoft.SqlServer.Management.Smo.Agent.CompletionAction]::Always  
```  
  
