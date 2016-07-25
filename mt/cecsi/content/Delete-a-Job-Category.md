---
title: "L&#246;schen einer Auftragskategorie"
ms.custom: na
ms.date: 07/15/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - tools-ssms
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 47a7640b-20b3-4639-ab37-b6fc73575e6c
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
# L&#246;schen einer Auftragskategorie
In diesem Thema wird beschrieben, wie Sie eine [!INCLUDE[msCoName](../content/includes/msCoName_md.md)] [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] -Agent-Auftragskategorie in [!INCLUDE[ssCurrent](../content/includes/ssCurrent_md.md)] mithilfe von [!INCLUDE[ssManStudioFull](../content/includes/ssManStudioFull_md.md)], [!INCLUDE[tsql](../content/includes/tsql_md.md)] oder SQL Server Management Objects löschen können.  
  
Auftragskategorien helfen Ihnen dabei, Ihre Aufträge zum einfachen Filtern und Gruppieren zu organisieren. Sie können z. B. alle Aufträge für die Datenbanksicherung in der Datenbankwartungskategorie organisieren.  
  
**In diesem Thema**  
  
-   **Vorbereitungen:**  
  
    [Einschränkungen](#Restrictions)  
  
    [Sicherheit](#Security)  
  
-   **So löschen Sie eine Auftragskategorie mit**  
  
    [SQL Server Management Studio](#SSMS)  
  
    [Transact-SQL](#TSQL)  
  
    [SQL Server Management Objects](#SMO)  
  
## <a name="BeforeYouBegin"></a>Vorbereitungen  
  
### <a name="Restrictions"></a>Einschränkungen  
Wenn Sie einen Benutzer löschen\-definierten Auftragskategorie [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] aufgefordert, die Aufträge neu zuzuweisen, die in einer anderen Auftragskategorie zugewiesen werden. Sie können nur Benutzer löschen\-Auftragskategorien definiert.  
  
### <a name="Security"></a>Sicherheit  
Ausführliche Informationen finden Sie unter [Implement SQL Server Agent Security](../content/Implement-SQL-Server-Agent-Security.md).  
  
## <a name="SSMS"></a>Verwendung von SQL Server Management Studio  
  
#### So löschen Sie eine Auftragskategorie  
  
1.  Klicken Sie im Objekt-Explorer ** **auf das Pluszeichen, um den Server zu erweitern, auf dem Sie eine Auftragskategorie löschen möchten.  
  
2.  Klicken Sie auf das Pluszeichen, um **SQL Server-Agent**zu erweitern.  
  
3.  Rechts\-Klicken Sie auf die **Aufträge** Ordner und wählen Sie **Auftragskategorien verwalten**.  
  
4.  In der **Auftragskategorien verwalten***Server\_Namen* Dialogfeld Wählen Sie die zu löschende Auftragskategorie.  
  
5.  Klicken Sie auf **Löschen**.  
  
6.  Klicken Sie im Dialogfeld **Auftragskategorien** auf **Ja**.  
  
7.  Schließen der **Auftragskategorien verwalten***Server\_Namen* Dialogfeld.  
  
## <a name="TSQL"></a>Mithilfe von Transact\-SQL  
  
#### So löschen Sie eine Auftragskategorie  
  
1.  Stellen Sie im Objekt-Explorer ** **eine Verbindung mit einer [!INCLUDE[ssDE](../content/includes/ssDE_md.md)]-Instanz her.  
  
2.  Klicken Sie in der Standardleiste auf **Neue Abfrage**.  
  
3.  Kopieren Sie das folgende Beispiel, fügen Sie es in das Abfragefenster ein, und klicken Sie auf **Ausführen**.  
  
    ```  
    -- deletes the job category named AdminJobs.  
    USE msdb ;  
    GO   
    EXEC dbo.sp_delete_category  
        @name = N'AdminJobs',  
        @class = N'JOB' ;  
    GO  
    ```  
  
Weitere Informationen finden Sie unter [Sp_delete_category (Transact-SQL)](assetId:///63ea7d0d-a567-456e-a778-bee99e21d16c).  
  
## <a name="SMO"></a>Verwendung von SQL Server Management Objects  
**So löschen Sie eine Auftragskategorie**  
  
Rufen Sie die **JobCategory** Klasse, indem Sie eine Programmiersprache, die Sie, wie z. B. Visual Basic, Visual C# auswählen\#, oder PowerShell.  
  
