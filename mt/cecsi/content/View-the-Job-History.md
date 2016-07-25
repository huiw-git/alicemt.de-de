---
title: "Anzeigen des Auftragsverlaufs"
ms.custom: na
ms.date: 07/15/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - tools-ssms
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 3bbd1556-abdb-48a3-b249-546eace76343
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
# Anzeigen des Auftragsverlaufs
In diesem Thema wird beschrieben, wie das [!INCLUDE[msCoName](../content/includes/msCoName_md.md)] [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] -Agent-Auftragsverlaufprotokoll in [!INCLUDE[ssCurrent](../content/includes/ssCurrent_md.md)] mithilfe von [!INCLUDE[ssManStudioFull](../content/includes/ssManStudioFull_md.md)], [!INCLUDE[tsql](../content/includes/tsql_md.md)], oder SQL Server Management Objects angezeigt werden kann.  
  
-   **Vorbereitungen:**  
  
    [Sicherheit](#Security)  
  
-   **So zeigen Sie das Auftragsverlaufsprotokoll an, und zwar mit**  
  
    [SQL Server Management Studio](#SSMS)  
  
    [Transact-SQL](#TSQL)  
  
    [SQL Server Management Objects](#SMO)  
  
## <a name="BeforeYouBegin"></a>Vorbereitungen  
  
### <a name="Security"></a>Sicherheit  
Ausführliche Informationen finden Sie unter [Implement SQL Server Agent Security](../content/Implement-SQL-Server-Agent-Security.md).  
  
## <a name="SSMS"></a>Verwendung von SQL Server Management Studio  
  
#### So zeigen Sie das Auftragsverlaufsprotokoll an  
  
1.  Stellen Sie im **Objekt-Explorer** eine Verbindung mit einer Instanz von [!INCLUDE[ssDEnoversion](../content/includes/ssDEnoversion_md.md)]her, und erweitern Sie dann diese Instanz.  
  
2.  Erweitern Sie **SQL Server-Agent**, und klicken Sie auf **Aufträge**.  
  
3.  Rechts\-Klicken Sie auf einen Auftrag, und klicken Sie dann auf **Verlauf anzeigen**.  
  
4.  Zeigen Sie im Protokolldatei-Viewer den Auftragsverlauf an.  
  
5.  Klicken Sie auf **Aktualisieren**, um den Auftragsverlauf zu aktualisieren. Um weniger Zeilen anzuzeigen, klicken Sie auf **Filter** , und geben Sie Filterparameter ein.  
  
## <a name="TSQL"></a>Mithilfe von Transact\-SQL  
  
#### So zeigen Sie das Auftragsverlaufsprotokoll an  
  
1.  Stellen Sie im **Objekt-Explorer**eine Verbindung mit einer [!INCLUDE[ssDE](../content/includes/ssDE_md.md)]-Instanz her.  
  
2.  Klicken Sie in der Standardleiste auf **Neue Abfrage**.  
  
3.  Kopieren Sie das folgende Beispiel, fügen Sie es in das Abfragefenster ein, und klicken Sie auf **Ausführen**.  
  
    ```  
    -- lists all job information for the NightlyBackups job.  
    USE msdb ;  
    GO  
  
    EXEC dbo.sp_help_jobhistory   
        @job_name = N'NightlyBackups' ;  
    GO  
    ```  
  
Weitere Informationen finden Sie unter [Sp_help_jobhistory (Transact-SQL)](assetId:///a944d44e-411b-4735-8ce4-73888d4262d7).  
  
## <a name="SMO"></a>Verwendung von SQL Server Management Objects  
**So zeigen Sie das Auftragsverlaufsprotokoll an**  
  
Rufen Sie die **EnumHistory** Methode der **Auftrag** Klasse, indem Sie eine Programmiersprache, die Sie, wie z. B. Visual Basic, Visual C# auswählen\#, oder PowerShell. Weitere Informationen finden Sie unter [SQL Server Management Objects (SMO)](http://msdn.microsoft.com/library/ms162169.aspx).  
  
