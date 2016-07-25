---
title: "Erstellen eines Operators"
ms.custom: na
ms.date: 07/15/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - tools-ssms
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 1359d790-5905-4927-a208-e7155e7768a2
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
# Erstellen eines Operators
In diesem Thema wird beschrieben, wie Sie in der Konfiguration festlegen können, dass ein Benutzer Benachrichtigungen über [!INCLUDE[msCoName](../content/includes/msCoName_md.md)] [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] -Agent-Aufträge in [!INCLUDE[ssCurrent](../content/includes/ssCurrent_md.md)] mithilfe von [!INCLUDE[ssManStudioFull](../content/includes/ssManStudioFull_md.md)] oder [!INCLUDE[tsql](../content/includes/tsql_md.md)]empfängt.  
  
**In diesem Thema**  
  
-   **Vorbereitungen:**  
  
    [Einschränkungen](#Restrictions)  
  
    [Sicherheit](#Security)  
  
-   **So erstellen Sie einen Operator mit**  
  
    [SQL Server Management Studio](#SSMSProcedure)  
  
    [Transact-SQL](#TsqlProcedure)  
  
## <a name="BeforeYouBegin"></a>Vorbereitungen  
  
### <a name="Restrictions"></a>Einschränkungen  
  
-   Die Pager- und **net send** -Optionen werden in zukünftigen Versionen von [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] nicht mehr im [!INCLUDE[msCoName](../content/includes/msCoName_md.md)][!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)]. Vermeiden Sie die Verwendung dieser Funktionen bei neuen Entwicklungsarbeiten, und planen Sie die Änderung von Anwendungen, die diese Funktionen zurzeit verwenden.  
  
-   Beachten Sie, dass SQL Server-Agent konfiguriert werden müssen, um Datenbank-Mail verwenden, um e-Mail senden\-an Operatoren senden, e-Mail und Pager. Weitere Informationen finden Sie unter [Zuweisen von Warnungen zu einem Operator](http://msdn.microsoft.com/library/ms190038.aspx).  
  
-   [!INCLUDE[ssManStudioFull](../content/includes/ssManStudioFull_md.md)] können Aufträge problemlos mithilfe einer grafischen Oberfläche verwaltet werden. Dies ist die empfohlene Vorgehensweise für die Erstellung und Verwaltung der Auftragsinfrastruktur.  
  
### <a name="Security"></a>Sicherheit  
  
#### <a name="Permissions"></a>Berechtigungen  
Nur Mitglieder der festen Serverrolle **sysadmin** können Operatoren erstellen.  
  
## <a name="SSMSProcedure"></a>Verwendung von SQL Server Management Studio  
  
#### So erstellen Sie einen Operator  
  
1.  Klicken Sie im **Objekt-Explorer**auf das Pluszeichen, um den Server zu erweitern, auf dem Sie den SQL Server-Agent-Operator erstellen möchten.  
  
2.  Klicken Sie auf das Pluszeichen, um **SQL Server-Agent**zu erweitern.  
  
3.  Rechts\-Klicken Sie auf die **Operatoren** Ordner und wählen Sie **Operator New**.  
  
    Die folgenden Optionen befinden sich im Dialogfeld **Neuer Operator** auf der Seite **Allgemein** :  
  
    **Name**  
    Ändern Sie den Namen des Operators.  
  
    **Aktiviert**  
    Aktiviert den Operator. Bei fehlender Aktivierung werden keine Benachrichtigungen an den Operator gesendet.  
  
    **E\-Mail-Name**  
    Gibt e\-e-Mail-Adresse des Operators.  
  
    **NET SEND-Adresse**  
    Geben Sie die Adresse mit **net Send**.  
  
    **Pager-e\-Mail-Name**  
    Gibt e\-e-Mail-Adresse für den Pager des Operators.  
  
    **Pager empfangsbereit am**  
    Legt fest, zu welchen Zeiten der Pager aktiv ist.  
  
    **Montag \- Sonntag**  
    Wählen Sie die Tage aus, an denen der Pager aktiv ist.  
  
    **Arbeitstag - Beginn**  
    Wählen Sie die Tageszeit aus, nach deren Eintreten der [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)]-Agent Meldungen an den Pager sendet.  
  
    **Arbeitstag - Ende**  
    Wählen Sie die Tageszeit aus, nach deren Eintreten der [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)]-Agent keine weiteren Meldungen an den Pager sendet.  
  
    Die folgenden Optionen befinden sich im Dialogfeld **Neuer Operator** auf der Seite **Benachrichtigungen** :  
  
    **Warnungen**  
    Zeigt die Warnungen in der Instanz an.  
  
    **Aufträge**  
    Zeigt die Aufträge in der Instanz an.  
  
    **Warnungsliste**  
    Listet die Warnungen in der Instanz auf.  
  
    **Auftragsliste**  
    Listet die Aufträge in der Instanz auf.  
  
    **E\-e-Mail-Nachrichten**  
    Benachrichtigt den Operator per e-Mail\-e-Mail-Nachrichten.  
  
    **Pager**  
    Benachrichtigt den Operator per e-Mail\-e-Mail-Nachrichten an die Pageradresse.  
  
    **NET SEND**  
    Benachrichtigt den Operator per **net Send**.  
  
4.  Klicken Sie auf **OK**, wenn Sie das Erstellen des neuen Operators abgeschlossen haben.  
  
## <a name="TsqlProcedure"></a>Mithilfe von Transact\-SQL  
  
#### So erstellen Sie einen Operator  
  
1.  Stellen Sie im **Objekt-Explorer**eine Verbindung mit einer [!INCLUDE[ssDE](../content/includes/ssDE_md.md)]-Instanz her.  
  
2.  Klicken Sie in der Standardleiste auf **Neue Abfrage**.  
  
3.  Kopieren Sie das folgende Beispiel, fügen Sie es in das Abfragefenster ein, und klicken Sie auf **Ausführen**.  
  
    ```  
    -- sets up the operator information for user 'danwi.' The operator is enabled.   
    -- SQL Server Agent sends notifications by pager from Monday through Friday from 8 A.M. to 5 P.M.  
    USE msdb ;  
    GO  
  
    EXEC dbo.sp_add_operator  
        @name = N'Dan Wilson',  
        @enabled = 1,  
        @email_address = N'danwi',  
        @pager_address = N'5551290AW@pager.Adventure-Works.com',  
        @weekday_pager_start_time = 080000,  
        @weekday_pager_end_time = 170000,  
        @pager_days = 62 ;  
    GO  
    ```  
  
Weitere Informationen finden Sie unter [Sp_add_operator (Transact-SQL)](assetId:///817cd98a-4dff-4ed8-a546-f336c144d1e0).  
  
