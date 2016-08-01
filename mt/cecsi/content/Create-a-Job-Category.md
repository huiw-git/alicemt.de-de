---
title: "Erstellen einer Auftragskategorie"
ms.custom: na
ms.date: 07/27/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - tools-ssms
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: e24a6d38-d231-4f64-ab89-2d1ef6f5792c
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
# Erstellen einer Auftragskategorie
In diesem Thema wird beschrieben, wie Sie eine Auftragskategorie in [!INCLUDE[ssCurrent](../content/includes/ssCurrent_md.md)] mithilfe von [!INCLUDE[ssManStudioFull](../content/includes/ssManStudioFull_md.md)], [!INCLUDE[tsql](../content/includes/tsql_md.md)] oder [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] Management Objects erstellen können.  
  
[!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] Agent stellt integrierte\-in Auftragskategorien, die Aufträge zugewiesen, oder Sie können eine Auftragskategorie erstellen und Aufträge zuweisen. Auftragskategorien helfen Ihnen dabei, Ihre Aufträge zum einfachen Filtern und Gruppieren zu organisieren. Sie können z. B. alle Aufträge für die Datenbanksicherung in der Datenbankwartungskategorie organisieren. Sie können zudem eigene Auftragskategorien erstellen.  
  
**In diesem Thema**  
  
-   **Vorbereitungen:**  
  
    [Einschränkungen](#Restrictions)  
  
    [Sicherheit](#Security)  
  
-   **So erstellen Sie eine Auftragskategorie mit**  
  
    [SQL Server Management Studio](#SSMS)  
  
    [Transact-SQL](#TSQL)  
  
    [SQL Server Management Objects](#SMO)  
  
## <a name="BeforeYouBegin"></a>Vorbereitungen  
  
### <a name="Restrictions"></a>Einschränkungen  
Multiserverkategorien sind nur auf einem Masterserver vorhanden. Auf einem Masterserver ist nur eine Standardauftragskategorie verfügbar: \[**nicht kategorisiert (mit mehreren\-Server)**]. Beim Herunterladen eines Multiserverauftrags wird seine Kategorie auf dem Zielserver in **Aufträge vom MSX** geändert.  
  
### <a name="Security"></a>Sicherheit  
Ausführliche Informationen finden Sie unter [Implement SQL Server Agent Security](../content/Implement-SQL-Server-Agent-Security.md).  
  
## <a name="SSMS"></a>Verwendung von SQL Server Management Studio  
  
#### So erstellen Sie eine Auftragskategorie  
  
1.  Klicken Sie im Objekt-Explorer ** **auf das Pluszeichen, um den Server zu erweitern, auf dem Sie eine Auftragskategorie erstellen möchten.  
  
2.  Klicken Sie auf das Pluszeichen, um **SQL Server-Agent**zu erweitern.  
  
3.  Rechts\-Klicken Sie auf die **Aufträge** Ordner und wählen Sie **Auftragskategorien verwalten**.  
  
4.  In der **Auftragskategorien verwalten***Server\_Namen* Dialogfeld klicken Sie auf **Hinzufügen**.  
  
5.  Geben Sie im neuen Dialogfeld **Name** einen Namen für die neue Auftragskategorie ein.  
  
6.  Aktivieren Sie das Kontrollkästchen **Alle Aufträge anzeigen** . Wählen Sie für die neue Kategorie mindestens einen Auftrag aus, indem Sie die Kontrollkästchen der entsprechenden Aufträge aktivieren.  
  
7.  Klicken Sie auf **OK**.  
  
8.  In der **Auftragskategorien verwalten***Server\_Namen* Dialogfeld klicken Sie auf **Aktualisieren** um sicherzustellen, dass die neue Auftragskategorie aktiv ist. Schließen Sie das Dialogfeld, wenn alles normal aussieht.  
  
Weitere Informationen zu diesen Dialogfeldern finden Sie unter [Auftragskategorien - Auftragskategorien verwalten](../content/Job-Categories---Manage-Job-Categories.md) und [Kategorien Auftragseigenschaften - neue Auftragskategorie](../content/Job-Categories-Properties---New-Job-Category.md).  
  
## <a name="TSQL"></a>Mithilfe von Transact\-SQL  
  
#### So erstellen Sie eine Auftragskategorie  
  
1.  Stellen Sie im Objekt-Explorer ** **eine Verbindung mit einer [!INCLUDE[ssDE](../content/includes/ssDE_md.md)]-Instanz her.  
  
2.  Klicken Sie in der Standardleiste auf **Neue Abfrage**.  
  
3.  Kopieren Sie das folgende Beispiel, fügen Sie es in das Abfragefenster ein, und klicken Sie auf **Ausführen**.  
  
    ```  
    -- creates a local job category named AdminJobs   
    USE msdb ;  
    GO  
    EXEC dbo.sp_add_category  
        @class=N'JOB',  
        @type=N'LOCAL',  
        @name=N'AdminJobs' ;  
    GO  
    ```  
  
Weitere Informationen finden Sie unter [Sp_add_category (Transact-SQL)](assetId:///6cca32cd-d941-4378-aed6-a7c90cb7520a).  
  
## <a name="SMO"></a>Verwendung von SQL Server Management Objects  
**So erstellen Sie eine Auftragskategorie**  
  
Rufen Sie die **JobCategory** Klasse, indem Sie eine Programmiersprache, die Sie, wie z. B. Visual Basic, Visual C# auswählen\#, oder PowerShell. Beispielcode, finden Sie unter [Planen von automatischen, administrativen Tasks im SQL Server-Agent](assetId:///900242ad-d6a2-48e9-8a1b-f0eea4413c16).  
  
