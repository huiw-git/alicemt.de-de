---
title: "Zuweisen von Warnungen zu einem Operator"
ms.custom: na
ms.date: 07/27/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - tools-ssms
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: aa818155-6fa2-4565-a09f-5c7e31c89754
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
# Zuweisen von Warnungen zu einem Operator
In diesem Thema wird beschrieben, wie Warnungen des [!INCLUDE[msCoName](../content/includes/msCoName_md.md)] [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] -Agents Operatoderen zugewiesen werden, damit diese in [!INCLUDE[ssCurrent](../content/includes/ssCurrent_md.md)] mithilfe von [!INCLUDE[ssManStudioFull](../content/includes/ssManStudioFull_md.md)] oder [!INCLUDE[tsql](../content/includes/tsql_md.md)]Benachrichtigungen über Aufträge empfangen können.  
  
**In diesem Thema**  
  
-   **Vorbereitungen:**  
  
    [Einschränkungen](#Restrictions)  
  
    [Sicherheit](#Security)  
  
-   **So weisen Sie einem Operator Warnungen zu mit**  
  
    [SQL Server Management Studio](#SSMSProcedure)  
  
    [Transact-SQL](#TsqlProcedure)  
  
## <a name="BeforeYouBegin"></a>Vorbereitungen  
  
### <a name="Restrictions"></a>Einschränkungen  
  
-   [!INCLUDE[ssManStudioFull](../content/includes/ssManStudioFull_md.md)] kann das gesamte Warnungssystem auf einfache Weise über eine grafische Oberfläche verwaltet werden. Für die Konfiguration einer Warnungsinfrastruktur sollte [!INCLUDE[ssManStudio](../content/includes/ssManStudio_md.md)] verwendet werden.  
  
-   Zum Senden einer Benachrichtigung als Reaktion auf eine Warnung müssen Sie zunächst den [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] -Agent für das Senden von E-Mail konfigurieren. Weitere Informationen finden Sie unter [Konfigurieren von SQL Server Agent-Mail mit Database Mail](assetId:///4b8b61bd-4bd1-43cd-b6e5-c6ed2e101dce).  
  
-   Wenn ein Fehler auftritt, senden Sie einen e\-e-Mail-Nachricht oder Pager Benachrichtigungen der Fehler wird gemeldet, der [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] -Agent-Dienst-Fehlerprotokoll.  
  
### <a name="Security"></a>Sicherheit  
  
#### <a name="Permissions"></a>Berechtigungen  
Nur Mitglieder der festen Serverrolle **sysadmin** können Operatoren Warnungen zuweisen.  
  
## <a name="SSMSProcedure"></a>Verwendung von SQL Server Management Studio  
  
#### So weisen Sie einem Operator Warnungen zu  
  
1.  Klicken Sie im Objekt-Explorer ****auf das Pluszeichen, um den Server zu erweitern, der den Operator enthält, dem Sie die Warnung zuweisen möchten.  
  
2.  Klicken Sie auf das Pluszeichen, um **SQL Server-Agent**zu erweitern.  
  
3.  Klicken Sie auf das Pluszeichen, um den Ordner **Operatoren** zu erweitern.  
  
4.  Rechts\-Klicken Sie auf den Operator, Sie möchten eine Warnung zuweisen, und wählen Sie **Eigenschaften**, und wählen Sie die **Benachrichtigungen** Seite.  
  
5.  In der *Operator\_Namen***Eigenschaften** Dialogfeld **Wählen Sie eine Seite**, Option **Benachrichtigungen**.  
  
6.  Wählen Sie unter **Benachrichtigungen an diesen Benutzer anzeigen von**die Option **Warnung** aus, um eine Liste der Warnungen anzuzeigen, die an diesen Operator gesendet wurden, oder wählen Sie **Aufträge** aus, um eine Liste der Aufträge anzuzeigen, von denen Benachrichtigungen an diesen Operator gesendet werden. Wählen Sie mindestens eines der folgenden Kontrollkästchen, um die Benachrichtigungsmethode für jede Benachrichtigung zu definieren: **E\-Mail**, **Pager**, oder **Net Send**.  
  
7.  Wenn Sie fertig sind, klicken Sie auf **OK**.  
  
## <a name="TsqlProcedure"></a>Mithilfe von Transact\-SQL  
  
#### So weisen Sie einem Operator Warnungen zu  
  
1.  Stellen Sie im Objekt-Explorer ** **eine Verbindung mit einer [!INCLUDE[ssDE](../content/includes/ssDE_md.md)]-Instanz her.  
  
2.  Klicken Sie in der Standardleiste auf **Neue Abfrage**.  
  
3.  Kopieren Sie das folgende Beispiel, fügen Sie es in das Abfragefenster ein, und klicken Sie auf **Ausführen**.  
  
    ```  
    -- adds an e-mail notification for the specified alert (Test Alert)  
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
  
