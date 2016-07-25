---
title: "Bearbeiten eines Operators"
ms.custom: na
ms.date: 07/15/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - tools-ssms
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: b2ba2168-ca0b-4b59-9007-4e1e4c30679e
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
# Bearbeiten eines Operators
In diesem Thema wird beschrieben, wie Operatoren die Möglichkeit zum Empfangen von Benachrichtigungen und ihre e bearbeiten\-e-Mail, Pager und Net send-Adressen in [!INCLUDE[ssCurrent](../content/includes/ssCurrent_md.md)] mit [!INCLUDE[ssManStudioFull](../content/includes/ssManStudioFull_md.md)] oder [!INCLUDE[tsql](../content/includes/tsql_md.md)].  
  
**In diesem Thema**  
  
-   **Vorbereitungen:**  
  
    [Einschränkungen](#Restrictions)  
  
    [Sicherheit](#Security)  
  
-   **So bearbeiten Sie einen Operator mit**  
  
    [SQL Server Management Studio](#SSMSProcedure)  
  
    [Transact-SQL](#TsqlProcedure)  
  
## <a name="BeforeYouBegin"></a>Vorbereitungen  
  
### <a name="Restrictions"></a>Einschränkungen  
  
-   Die Pager- und **net send** -Optionen werden in zukünftigen Versionen von [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] nicht mehr im [!INCLUDE[msCoName](../content/includes/msCoName_md.md)][!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)]. Vermeiden Sie die Verwendung dieser Funktionen bei neuen Entwicklungsarbeiten, und planen Sie die Änderung von Anwendungen, die diese Funktionen zurzeit verwenden.  
  
-   Beachten Sie, dass SQL Server-Agent konfiguriert werden müssen, um Datenbank-Mail verwenden, um e-Mail senden\-an Operatoren senden, e-Mail und Pager. Weitere Informationen finden Sie unter [Zuweisen von Warnungen zu einem Operator](http://msdn.microsoft.com/library/ms190038.aspx).  
  
-   [!INCLUDE[ssManStudioFull](../content/includes/ssManStudioFull_md.md)] können Aufträge problemlos mithilfe einer grafischen Oberfläche verwaltet werden. Dies ist die empfohlene Vorgehensweise für die Erstellung und Verwaltung der Auftragsinfrastruktur.  
  
### <a name="Security"></a>Sicherheit  
  
#### <a name="Permissions"></a>Berechtigungen  
Nur Mitglieder der festen Serverrolle **sysadmin** können Operatoren bearbeiten.  
  
## <a name="SSMSProcedure"></a>Verwendung von SQL Server Management Studio  
  
#### So bearbeiten Sie einen Operator  
  
1.  Klicken Sie im Objekt-Explorer ****auf das Pluszeichen, um den Server zu erweitern, der den Operator enthält, den Sie bearbeiten möchten.  
  
2.  Klicken Sie auf das Pluszeichen, um **SQL Server-Agent**zu erweitern.  
  
3.  Klicken Sie auf das Pluszeichen, um den Ordner **Operatoren** zu erweitern.  
  
4.  Rechts\-Klicken Sie auf den Operator, den Sie bearbeiten möchten und wählen Sie **Eigenschaften**.  
  
    Weitere Informationen zu den verfügbaren Optionen, die Bestandteil der *Operator\_Namen***Eigenschaften** Dialogfeld finden Sie unter:  
  
    -   [Operatoreigenschaften - New-Operator & #40; Seite "Allgemein" & #41;](../content/Operator-Properties---New-Operator--General-Page-.md)  
  
    -   [Operatoreigenschaften - New-Operator & #40; Benachrichtigungsseite & #41;](../content/Operator-Properties---New-Operator--Notifications-Page-.md)  
  
    -   [Operatoreigenschaften & #40; Verlaufsseite & #41;](../content/Operator-Properties--History-Page-.md)  
  
5.  Wenn Sie fertig sind, klicken Sie auf **OK**.  
  
## <a name="TsqlProcedure"></a>Mithilfe von Transact\-SQL  
  
#### So bearbeiten Sie einen Operator  
  
1.  Stellen Sie im **Objekt-Explorer**eine Verbindung mit einer [!INCLUDE[ssDE](../content/includes/ssDE_md.md)]-Instanz her.  
  
2.  Klicken Sie in der Standardleiste auf **Neue Abfrage**.  
  
3.  Kopieren Sie das folgende Beispiel, fügen Sie es in das Abfragefenster ein, und klicken Sie auf **Ausführen**.  
  
    ```  
    -- updates the operator status to enabled, and sets the days   
    -- (from Monday through Friday, from 8 A.M. through 5 P.M.) when the operator can be paged.   
    USE msdb ;  
    GO  
  
    EXEC dbo.sp_update_operator   
        @name = N'François Ajenstat',  
        @enabled = 1,  
        @email_address = N'françoisa',  
        @pager_address = N'5551290AW@pager.Adventure-Works.com',  
        @weekday_pager_start_time = 080000,  
        @weekday_pager_end_time = 170000,  
        @pager_days = 64 ;  
    GO  
    ```  
  
Weitere Informationen finden Sie unter [Sp_update_operator (Transact-SQL)](assetId:///231750a6-4828-4d03-afe6-b91d38c42ed3).  
  
