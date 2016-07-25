---
title: "Benachrichtigen eines Operators &#252;ber den Auftragsstatus"
ms.custom: na
ms.date: 07/15/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - tools-ssms
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: e7399505-27ac-48d9-a637-73bf92b9df49
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
# Benachrichtigen eines Operators &#252;ber den Auftragsstatus
In diesem Thema wird beschrieben, wie Sie Benachrichtigungsoptionen in [!INCLUDE[ssCurrent](../content/includes/ssCurrent_md.md)] mithilfe von [!INCLUDE[ssManStudioFull](../content/includes/ssManStudioFull_md.md)], [!INCLUDE[tsql](../content/includes/tsql_md.md)]oder SQL Server Management Objects festlegen können, damit der [!INCLUDE[msCoName](../content/includes/msCoName_md.md)] [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] -Agent den Operatoren Benachrichtigungen über Aufträge senden kann.  
  
**In diesem Thema**  
  
-   **Vorbereitungen:**  
  
    [Sicherheit](#Security)  
  
-   **So benachrichtigen Sie einen Operator über einen Auftragsstatus mit**  
  
    [SQL Server Management Studio](#SSMS)  
  
    [Transact-SQL](#TSQL)  
  
    [SQL Server Management Objects](#SMO)  
  
## <a name="BeforeYouBegin"></a>Vorbereitungen  
  
### <a name="Security"></a>Sicherheit  
Ausführliche Informationen finden Sie unter [Implement SQL Server Agent Security](../content/Implement-SQL-Server-Agent-Security.md).  
  
## <a name="SSMS"></a>Verwendung von SQL Server Management Studio  
  
#### So benachrichtigen Sie einen Operator über einen Auftragsstatus  
  
1.  Stellen Sie im **Objekt-Explorer** eine Verbindung mit einer Instanz von [!INCLUDE[ssDEnoversion](../content/includes/ssDEnoversion_md.md)]her, und erweitern Sie dann diese Instanz.  
  
2.  Erweitern Sie **SQL Server-Agent**, erweitern Sie **Aufträge**, mit der rechten Maustaste\-Klicken Sie auf den Auftrag zu bearbeiten, und wählen **Eigenschaften**.  
  
3.  Wählen Sie im Dialogfeld **Auftragseigenschaften** die Seite **Benachrichtigungen** aus.  
  
4.  Wenn ein Operator per e-Mail benachrichtigt werden sollen\-e-Mail Kontrollkästchen **E\-Mail**, wählen Sie einen Operator aus der Liste, und wählen Sie dann eine der folgenden:  
  
    -   **Bei erfolgreicher Auftragsausführung** , um den Operator zu benachrichtigen, wenn der Auftrag erfolgreich abgeschlossen wurde.  
  
    -   **Bei Auftragsfehler** , um den Operator zu benachrichtigen, wenn der Auftrag fehlgeschlagen ist.  
  
    -   **Beim Abschluss des Auftrags** , um den Operator unabhängig vom Abschlussstatus zu benachrichtigen.  
  
5.  Wenn ein Operator per Pager benachrichtigt werden soll, aktivieren Sie die Option **Pager**, wählen Sie aus der Liste einen Operator aus, und wählen Sie dann eine der folgenden Optionen aus:  
  
    -   **Bei erfolgreicher Auftragsausführung** , um den Operator zu benachrichtigen, wenn der Auftrag erfolgreich abgeschlossen wurde.  
  
    -   **Bei Auftragsfehler** , um den Operator zu benachrichtigen, wenn der Auftrag fehlgeschlagen ist.  
  
    -   **Beim Abschluss des Auftrags** , um den Operator unabhängig vom Abschlussstatus zu benachrichtigen.  
  
6.  Wenn ein Operator per NET SEND benachrichtigt werden soll, aktivieren Sie die Option **NET SEND**, wählen Sie aus der Liste einen Operator aus, und wählen Sie dann eine der folgenden Optionen aus:  
  
    -   **Bei erfolgreicher Auftragsausführung** , um den Operator zu benachrichtigen, wenn der Auftrag erfolgreich abgeschlossen wurde.  
  
    -   **Bei Auftragsfehler** , um den Operator zu benachrichtigen, wenn der Auftrag fehlgeschlagen ist.  
  
    -   **Beim Abschluss des Auftrags** , um den Operator unabhängig vom Abschlussstatus zu benachrichtigen.  
  
## <a name="TSQL"></a>Mithilfe von Transact\-SQL  
  
#### So benachrichtigen Sie einen Operator über einen Auftragsstatus  
  
1.  Stellen Sie im **Objekt-Explorer**eine Verbindung mit einer [!INCLUDE[ssDE](../content/includes/ssDE_md.md)]-Instanz her.  
  
2.  Klicken Sie in der Standardleiste auf **Neue Abfrage**.  
  
3.  Kopieren Sie das folgende Beispiel, fügen Sie es in das Abfragefenster ein, und klicken Sie auf **Ausführen**.  
  
    ```  
    -- adds an e-mail notification for the specified alert (Test Alert).  
    -- This example assumes that Test Alert already exists and that François Ajenstat is a valid operator name.  
    USE msdb ;  
    GO  
    EXEC dbo.sp_add_notification   
    @alert_name = N'Test Alert',   
    @operator_name = N'François Ajenstat',   
    @notification_method = 1 ;  
    GO  
    ```  
  
Weitere Informationen finden Sie unter [Sp_add_notification (Transact-SQL)](assetId:///0525e0a2-ed0b-4e69-8a4c-a9e3e3622fbd).  
  
## <a name="SMO"></a>Verwendung von SQL Server Management Objects  
**So benachrichtigen Sie einen Operator über einen Auftragsstatus**  
  
Verwenden der **Auftrag** Klasse, indem Sie eine Programmiersprache, die Sie, wie z. B. Visual Basic, Visual C# auswählen\#, oder PowerShell. Weitere Informationen finden Sie unter [SQL Server Management Objects (SMO)](http://msdn.microsoft.com/library/ms162169.aspx).  
  
