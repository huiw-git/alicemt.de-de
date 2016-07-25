---
title: "Starten eines Auftrags"
ms.custom: na
ms.date: 07/15/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - tools-ssms
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: cec9f7f7-d0a7-4239-9dc5-a69c011ebaa0
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
# Starten eines Auftrags
In diesem Thema wird beschrieben, wie Sie das Ausführen eines [!INCLUDE[msCoName](../content/includes/msCoName_md.md)] [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] -Agent-Auftrags in [!INCLUDE[ssCurrent](../content/includes/ssCurrent_md.md)] mithilfe von [!INCLUDE[ssManStudioFull](../content/includes/ssManStudioFull_md.md)], [!INCLUDE[tsql](../content/includes/tsql_md.md)] oder SQL Server Management Objects starten können.  
  
Ein Auftrag ist eine festgelegte Reihe von Aktionen, die der [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] -Agent ausführt. [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] -Agent-Aufträge können auf einem lokalen oder mehreren Remoteservern ausgeführt werden.  
  
-   **Vorbereitungen:**  
  
    [Sicherheit](#Security)  
  
-   **So starten Sie einen Auftrag an mit**  
  
    [SQL Server Management Studio](#SSMS)  
  
    [Transact-SQL](#TSQL)  
  
    [SQL Server Management Objects](#SMO)  
  
## <a name="BeforeYouBegin"></a>Vorbereitungen  
  
### <a name="Security"></a>Sicherheit  
Ausführliche Informationen finden Sie unter [Implement SQL Server Agent Security](../content/Implement-SQL-Server-Agent-Security.md).  
  
## <a name="SSMS"></a>Verwendung von SQL Server Management Studio  
  
#### So starten Sie einen Auftrag  
  
1.  Stellen Sie im **Objekt-Explorer** eine Verbindung mit einer Instanz von [!INCLUDE[ssDEnoversion](../content/includes/ssDEnoversion_md.md)]her, und erweitern Sie dann diese Instanz.  
  
2.  Erweitern Sie **SQL Server-Agent** , und erweitern Sie dann **Aufträge**. Führen Sie, je nachdem, wie der Auftrag gestartet werden soll, eine der folgenden Aktionen aus:  
  
    -   Wenn Sie Arbeit auf einem einzelnen Server oder auf einem Zielserver arbeiten, oder einen lokalen Serverauftrag auf einem Masterserver ausführen, mit der rechten Maustaste\-Klicken Sie auf den Auftrag zu starten, und klicken Sie dann auf **Auftrag starten**.  
  
    -   Wenn Sie mehrere Aufträge starten möchten, mit der rechten Maustaste\-Klicken Sie auf **Auftragsaktivitätsmonitor**, und klicken Sie dann auf **Anzeigen der Auftragsaktivität**. Im Auftragsaktivitätsmonitor können Sie mehrere Aufträge direkt auswählen\-Klicken Sie auf die Auswahl, und klicken Sie auf **Aufträge starten**.  
  
    -   Wenn Sie auf einem Masterserver arbeiten und alle Zielserver den Auftrag gleichzeitig ausführen sollen, mit der rechten Maustaste\-Klicken Sie auf den Auftrag, die Sie starten möchten, klicken Sie auf **Auftrag starten**, und klicken Sie dann auf **auf allen Zielservern starten**.  
  
    -   Wenn Sie auf einem Masterserver arbeiten und Zielserver für den Auftrag angeben möchten, mit der rechten Maustaste\-Klicken Sie auf den Auftrag, die Sie starten möchten, klicken Sie auf **Auftrag starten**, und klicken Sie dann auf **auf angegebenen Zielservern starten**. Aktivieren Sie im Dialogfeld **Downloadanweisungen bereitstellen** das Kontrollkästchen **Diese Zielserver** , und wählen Sie dann alle Zielserver aus, auf denen dieser Auftrag ausgeführt werden soll.  
  
## <a name="TSQL"></a>Mithilfe von Transact\-SQL  
  
#### So starten Sie einen Auftrag  
  
1.  Stellen Sie im **Objekt-Explorer**eine Verbindung mit einer [!INCLUDE[ssDE](../content/includes/ssDE_md.md)]-Instanz her.  
  
2.  Klicken Sie in der Standardleiste auf **Neue Abfrage**.  
  
3.  Kopieren Sie das folgende Beispiel, fügen Sie es in das Abfragefenster ein, und klicken Sie auf **Ausführen**.  
  
    ```  
    -- starts a job named Weekly Sales Data Backup.    
    USE msdb ;  
    GO  
  
    EXEC dbo.sp_start_job N'Weekly Sales Data Backup' ;  
    GO  
    ```  
  
Weitere Informationen finden Sie unter [Sp_start_job (Transact-SQL)](assetId:///8a91df6a-eb84-4512-9a17-4a6e32a9538a).  
  
## <a name="SMO"></a>Verwendung von SQL Server Management Objects  
**So starten Sie einen Auftrag**  
  
Rufen Sie die **Starten** Methode der **Auftrag** Klasse, indem Sie eine Programmiersprache, die Sie, wie z. B. Visual Basic, Visual C# auswählen\#, oder PowerShell. Weitere Informationen finden Sie unter [SQL Server Management Objects (SMO)](http://msdn.microsoft.com/library/ms162169.aspx).  
  
