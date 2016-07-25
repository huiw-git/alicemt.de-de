---
title: "L&#246;schen eines oder mehrerer Auftr&#228;ge"
ms.custom: na
ms.date: 07/15/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - tools-ssms
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 67dcdad0-57b2-431c-b77f-4ffc926af93d
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
# L&#246;schen eines oder mehrerer Auftr&#228;ge
In diesem Thema wird beschrieben, wie Sie [!INCLUDE[msCoName](../content/includes/msCoName_md.md)] [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] -Agent-Aufträge in [!INCLUDE[ssCurrent](../content/includes/ssCurrent_md.md)] mithilfe von [!INCLUDE[ssManStudioFull](../content/includes/ssManStudioFull_md.md)], [!INCLUDE[tsql](../content/includes/tsql_md.md)]oder SQL Server Management Objects löschen können.  
  
**In diesem Thema**  
  
-   **Vorbereitungen:**  
  
    [Sicherheit](#Security)  
  
-   **So löschen Sie einen oder mehrere Aufträge mit:**  
  
    [SQL Server Management Studio](#SSMS)  
  
    [Transact-SQL](#TSQL)  
  
    [SQL Server Management Objects](#SMO)  
  
## <a name="BeforeYouBegin"></a>Vorbereitungen  
  
### <a name="Security"></a>Sicherheit  
Sie können nur Aufträge löschen, die in Ihrem Besitz sind, es sei denn, Sie sind ein Mitglied der festen Serverrolle **sysadmin** .  
  
## <a name="SSMS"></a>Verwendung von SQL Server Management Studio  
  
#### So löschen Sie einen Auftrag  
  
1.  Stellen Sie im **Objekt-Explorer** eine Verbindung mit einer Instanz von [!INCLUDE[ssDEnoversion](../content/includes/ssDEnoversion_md.md)]her, und erweitern Sie dann diese Instanz.  
  
2.  Erweitern Sie **SQL Server-Agent**, erweitern Sie **Aufträge**, mit der rechten Maustaste\-Klicken Sie auf den Auftrag zu löschen, und klicken Sie dann auf **Löschen**.  
  
3.  Bestätigen Sie im Dialogfeld **Objekt löschen** , dass der Auftrag tatsächlich gelöscht werden soll.  
  
4.  Klicken Sie auf **OK**.  
  
#### So löschen Sie mehrere Aufträge  
  
1.  Stellen Sie im **Objekt-Explorer** eine Verbindung mit einer Instanz von [!INCLUDE[ssDEnoversion](../content/includes/ssDEnoversion_md.md)]her, und erweitern Sie dann diese Instanz.  
  
2.  Erweitern Sie **SQL Server-Agent**.  
  
3.  Rechts\-Klicken Sie auf **Auftragsaktivitätsmonitor**, und klicken Sie auf **Anzeigen der Auftragsaktivität**.  
  
4.  Wählen Sie im Auftragsaktivitätsmonitor die Aufträge, die Sie löschen rechts, möchten\-Klicken Sie auf die Auswahl, und wählen Sie **Aufträge löschen**.  
  
## <a name="TSQL"></a>Mithilfe von Transact\-SQL  
  
#### So löschen Sie einen Auftrag  
  
1.  Stellen Sie im **Objekt-Explorer**eine Verbindung mit einer [!INCLUDE[ssDE](../content/includes/ssDE_md.md)]-Instanz her.  
  
2.  Klicken Sie in der Standardleiste auf **Neue Abfrage**.  
  
3.  Kopieren Sie das folgende Beispiel, fügen Sie es in das Abfragefenster ein, und klicken Sie auf **Ausführen**.  
  
    ```  
    USE msdb ;  
    GO  
  
    EXEC sp_delete_job  
        @job_name = N'NightlyBackups' ;  
    GO  
    ```  
  
Weitere Informationen finden Sie unter [Sp_delete_job (Transact-SQL)](assetId:///b85db6e4-623c-41f1-9643-07e5ea38db09).  
  
## <a name="SMO"></a>Verwendung von SQL Server Management Objects  
**So löschen Sie mehrere Aufträge**  
  
Verwenden der **Auftragssammlung** Klasse, indem Sie eine Programmiersprache, die Sie, wie z. B. Visual Basic, Visual C# auswählen\#, oder PowerShell. Weitere Informationen finden Sie unter [SQL Server Management Objects (SMO)](http://msdn.microsoft.com/library/ms162169.aspx).  
  
