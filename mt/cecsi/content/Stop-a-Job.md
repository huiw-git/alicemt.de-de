---
title: "Beenden eines Auftrags"
ms.custom: na
ms.date: 07/27/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - tools-ssms
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 4249328a-24d8-4284-9d1d-7d04ed90e3d7
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
# Beenden eines Auftrags
In diesem Thema wird das Beenden eines [!INCLUDE[msCoName](../content/includes/msCoName_md.md)] [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] -Agent-Auftrags beschrieben. Ein Auftrag ist eine festgelegte Reihe von Aktionen, die der SQL Server-Agent ausführt.  
  
-   **Vorbereitungen:**  ,  
  
    [Einschränkungen](#Restrictions)  
  
    [Sicherheit](#Security)  
  
-   **So halten Sie einen Auftrag an mit**  
  
    [SQL Server Management Studio](#SSMS)  
  
    [Transact-SQL](#TSQL)  
  
    [SQL Server Management Objects](#SMO)  
  
## <a name="BeforeYouBegin"></a>Vorbereitungen  
  
### <a name="Restrictions"></a>Einschränkungen  
  
-   Wenn ein Auftrag einen Schritt vom Typ derzeit ausgeführten **CmdExec** oder **PowerShell**, vorzeitig beendet der Prozess, der (z. B. MyProgram.exe) ausgeführt wird erzwungen wird. Dies kann zu unvorhersehbarem Verhalten führen, so werden z.&amp;nbsp;B. Dateien, die vom Prozess verwendet werden, geöffnet bleiben.  
  
-   Bei einem Multiserverauftrag wird eine STOP-Anweisung für den Auftrag an alle Zielserver des Auftrags gesendet.  
  
### <a name="Security"></a>Sicherheit  
Ausführliche Informationen finden Sie unter [Implement SQL Server Agent Security](../content/Implement-SQL-Server-Agent-Security.md).  
  
## <a name="SSMS"></a>Verwendung von SQL Server Management Studio  
  
#### So beenden Sie einen Auftrag  
  
1.  Stellen Sie im **Objekt-Explorer** eine Verbindung mit einer Instanz von [!INCLUDE[ssDEnoversion](../content/includes/ssDEnoversion_md.md)]her, und erweitern Sie dann diese Instanz.  
  
2.  Erweitern Sie **SQL Server-Agent**, erweitern Sie **Aufträge**, mit der rechten Maustaste\-Klicken Sie auf den Auftrag zu beenden, und klicken Sie dann auf **Auftrag zum Beenden des**.  
  
3.  Wenn Sie mehrere Aufträge beenden möchten, mit der rechten Maustaste\-Klicken Sie auf **Auftragsaktivitätsmonitor**, und klicken Sie dann auf **Anzeigen der Auftragsaktivität**. Wählen Sie in den Auftragsaktivitätsmonitor die Aufträge zu beenden, rechts\-Klicken Sie auf die Auswahl, und klicken Sie dann auf **Aufträge beenden**.  
  
## <a name="TSQL"></a>Mithilfe von Transact\-SQL  
  
#### So beenden Sie einen Auftrag  
  
1.  Stellen Sie im Objekt-Explorer ** **eine Verbindung mit einer [!INCLUDE[ssDE](../content/includes/ssDE_md.md)]-Instanz her.  
  
2.  Klicken Sie in der Standardleiste auf **Neue Abfrage**.  
  
3.  Kopieren Sie das folgende Beispiel, fügen Sie es in das Abfragefenster ein, und klicken Sie auf **Ausführen**.  
  
    ```  
    -- stops a job named Weekly Sales Data Backup  
    USE msdb ;  
    GO  
  
    EXEC dbo.sp_stop_job  
        N'Weekly Sales Data Backup' ;  
    GO  
    ```  
  
Weitere Informationen finden Sie unter [Sp_stop_job (Transact-SQL)](assetId:///64b4cc75-99a0-421e-b418-94e37595bbb0).  
  
## <a name="SMO"></a>Verwendung von SQL Server Management Objects  
**So beenden Sie einen Auftrag**  
  
Rufen Sie die **Beenden** Methode der **Auftrag** Klasse, indem Sie eine Programmiersprache, die Sie, wie z. B. Visual Basic, Visual C# auswählen\#, oder PowerShell. Weitere Informationen finden Sie unter [SQL Server Management Objects (SMO)](http://msdn.microsoft.com/library/ms162169.aspx).  
  
