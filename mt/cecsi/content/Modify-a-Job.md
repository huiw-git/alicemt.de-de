---
title: "&#196;ndern eines Auftrags"
ms.custom: na
ms.date: 07/15/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - tools-ssms
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: dd5e5f20-20c4-4ab9-a19a-db87577dcd43
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
# &#196;ndern eines Auftrags
In diesem Thema wird beschrieben, wie Sie die Eigenschaften der [!INCLUDE[msCoName](../content/includes/msCoName_md.md)] [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] -Auftragskategorien in [!INCLUDE[ssCurrent](../content/includes/ssCurrent_md.md)] mithilfe von [!INCLUDE[ssManStudioFull](../content/includes/ssManStudioFull_md.md)], [!INCLUDE[tsql](../content/includes/tsql_md.md)]oder SQL Server Management Objects ändern können.  
  
**In diesem Thema**  
  
-   **Vorbereitungen:**   
  
    [Einschränkungen](#Restrictions)  
  
    [Sicherheit](#Security)  
  
-   **So ändern Sie einen Auftrag mit**  
  
    [SQL Server Management Studio](#SSMS)  
  
    [Transact-SQL](#TSQL)  
  
    [SQL Server Management Objects](#SMO)  
  
## <a name="BeforeYouBegin"></a>Vorbereitungen  
  
### <a name="Restrictions"></a>Einschränkungen  
Ein Masterauftrag für den [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] -Agent kann nicht gleichzeitig lokale Server und Remoteserver als Ziel haben.  
  
### <a name="Security"></a>Sicherheit  
Sie können nur Aufträge ändern, die in Ihrem Besitz sind, es sei denn, Sie sind ein Mitglied der festen Serverrolle **sysadmin** . Ausführliche Informationen finden Sie unter [Implement SQL Server Agent Security](../content/Implement-SQL-Server-Agent-Security.md).  
  
## <a name="SSMS"></a>Verwendung von SQL Server Management Studio  
  
#### So ändern Sie einen Auftrag  
  
1.  Stellen Sie im **Objekt-Explorer** eine Verbindung mit einer Instanz von [!INCLUDE[ssDEnoversion](../content/includes/ssDEnoversion_md.md)]her, und erweitern Sie dann diese Instanz.  
  
2.  Erweitern Sie **SQL Server-Agent**, erweitern Sie **Aufträge**, mit der rechten Maustaste\-Klicken Sie auf den Auftrag zu ändern, und klicken Sie dann auf **Eigenschaften**.  
  
3.  Aktualisieren Sie im Dialogfeld **Auftragseigenschaften** mithilfe der entsprechenden Seiten die Eigenschaften, die Schritte, den Zeitplan, die Warnungen und die Benachrichtigungen des Auftrags.  
  
## <a name="TSQL"></a>Mithilfe von Transact\-SQL  
  
#### So ändern Sie einen Auftrag  
  
1.  Stellen Sie im Objekt-Explorer eine Verbindung mit einer Instanz von Database Engine (Datenbankmodul) her, und erweitern Sie dann diese Instanz.  
  
2.  Klicken Sie auf der Symbolleiste auf **Neue Abfrage**.  
  
3.  Verwenden Sie im Abfragefenster die folgenden gespeicherten Systemprozeduren, um einen Auftrag zu ändern.  
  
    -   Führen Sie [Sp_update_job (Transact-SQL)](assetId:///cbdfea38-9e42-47f3-8fc8-5978b82e2623) So ändern Sie die Attribute eines Auftrags.  
  
    -   Führen Sie [Sp_update_schedule (Transact-SQL)](assetId:///97b3119b-e43e-447a-bbfb-0b5499e2fefe) die Zeitplandetails für eine Auftragsdefinition zu ändern.  
  
    -   Führen Sie [Sp_add_jobstep (Transact-SQL)](assetId:///97900032-523d-49d6-9865-2734fba1c755) um neue Auftragsschritte hinzuzufügen.  
  
    -   Führen Sie [Sp_update_jobstep (Transact-SQL)](assetId:///e158802c-c347-4a5d-bf75-c03e5ae56e6b) vor ändern\-vorhandene Auftragsschritte.  
  
    -   Führen Sie [Sp_delete_jobstep (Transact-SQL)](assetId:///421ede8e-ad57-474a-9fb9-92f70a3e77e3) auf einen Auftragsschritt aus einem Auftrag zu entfernen.  
  
    -   Weitere gespeicherte Prozeduren zum Ändern von SQL Server-Agent-Masteraufträgen:  
  
        -   Führen Sie [Sp_delete_jobserver (Transact-SQL)](assetId:///6d63ed32-68cf-4d8f-aa40-05a3826e05b8) zum Löschen eines Servers, der einem Auftrag gegenwärtig zugeordnet.  
  
        -   Führen Sie [Sp_add_jobserver (Transact-SQL)](assetId:///485252cc-0081-490a-9bd1-cbbd68eea286) auf dem aktuellen Auftrag einen Server zuzuordnen.  
  
## <a name="SMO"></a>Verwendung von SQL Server Management Objects  
**So ändern Sie einen Auftrag**  
  
Verwenden der **Auftrag** Klasse, indem Sie eine Programmiersprache, die Sie, wie z. B. Visual Basic, Visual C# auswählen\#, oder PowerShell. Weitere Informationen finden Sie unter [SQL Server Management Objects (SMO)](http://msdn.microsoft.com/library/ms162169.aspx).  
  
