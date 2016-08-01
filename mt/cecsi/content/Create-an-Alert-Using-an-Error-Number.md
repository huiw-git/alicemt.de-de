---
title: "Erstellen einer Warnung mithilfe einer Fehlernummer"
ms.custom: na
ms.date: 07/27/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - tools-ssms
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 03dd7fac-5073-4f86-babd-37e45a86023c
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
# Erstellen einer Warnung mithilfe einer Fehlernummer
In diesem Thema wird beschrieben, wie Sie eine [!INCLUDE[msCoName](../content/includes/msCoName_md.md)] [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] -Agentwarnung in [!INCLUDE[ssCurrent](../content/includes/ssCurrent_md.md)] erstellen, die bei einem Fehler mit einer bestimmten Nummer ausgegeben wird, wenn [!INCLUDE[ssManStudioFull](../content/includes/ssManStudioFull_md.md)] oder [!INCLUDE[tsql](../content/includes/tsql_md.md)]verwendet wird.  
  
**In diesem Thema**  
  
-   **Vorbereitungen:**  
  
    [Einschränkungen](#Restrictions)  
  
    [Sicherheit](#Security)  
  
-   **So erstellen Sie eine Warnung mithilfe einer Fehlernummer mit**  
  
    [SQL Server Management Studio](#SSMSProcedure)  
  
    [Transact-SQL](#TsqlProcedure)  
  
## <a name="BeforeYouBegin"></a>Vorbereitungen  
  
### <a name="Restrictions"></a>Einschränkungen  
  
-   [!INCLUDE[ssManStudioFull](../content/includes/ssManStudioFull_md.md)] lässt sich das gesamte Warnungssystem auf einfache Weise mit einer grafischen Oberfläche verwalten. Dies ist die empfohlene Vorgehensweise, um eine Warnungsinfrastruktur zu konfigurieren.  
  
-   Mit generierten Ereignisse **Xp\_Logevent** treten in der master-Datenbank. Aus diesem Grund **Xp\_Logevent** löst keine Warnung aus, es sei denn, die **@database\_Namen** für die Warnung **'master'** oder NULL.  
  
### <a name="Security"></a>Sicherheit  
  
#### <a name="Permissions"></a>Berechtigungen  
Standardmäßig nur Mitglieder der **Sysadmin** feste Serverrolle **sp\_Hinzufügen\_Warnung**.  
  
## <a name="SSMSProcedure"></a>Verwendung von SQL Server Management Studio  
  
#### So erstellen Sie eine Warnung mithilfe einer Fehlernummer  
  
1.  Klicken Sie im **Objekt-Explorer** auf das Pluszeichen, um den Server zu erweitern, auf dem Sie eine Warnung mithilfe der Fehlernummer erstellen möchten.  
  
2.  Klicken Sie auf das Pluszeichen, um **SQL Server-Agent**zu erweitern.  
  
3.  Rechts\-Klicken Sie auf **Warnungen** und wählen Sie **neue Warnung**.  
  
4.  Geben Sie im Dialogfeld **Neue Warnung** einen ** ** Namen für diese Warnung ein.  
  
5.  Aktivieren Sie das Kontrollkästchen **Aktivieren** , um die Ausführung der Warnung zu ermöglichen. Standardmäßig ist **Aktivieren** aktiviert.  
  
6.  Klicken Sie in der Liste **Typ** auf **SQL Server-Ereigniswarnung**.  
  
7.  Klicken Sie in der Liste **Datenbankname**auf den ** ** Datenbanknamen, um die Warnung auf eine bestimmte Datenbank zu beschränken.  
  
8.  Klicken Sie unter **Warnungen werden ausgelöst basierend auf**auf **Fehlernummer**, und geben Sie anschließend eine gültige Fehlernummer für diese Warnung ein. Klicken Sie alternativ auf **Schweregrad** , und wählen Sie anschließend den spezifischen Schweregrad, mit dem die Warnung ausgelöst wird.  
  
9. Aktivieren Sie das Kontrollkästchen neben **Warnung auslösen, wenn eine Meldung Folgendes enthält** , um die Warnung auf eine bestimmte Zeichenfolge zu beschränken, und geben Sie dann ein Schlüsselwort oder Zeichenfolge für den Meldungstext ** **ein. Es können maximal 100 Zeichen eingegeben werden.  
  
10. Klicken Sie auf **OK**.  
  
## <a name="TsqlProcedure"></a>Mithilfe von Transact\-SQL  
  
#### So erstellen Sie eine Warnung mithilfe einer Fehlernummer  
  
1.  Stellen Sie im **Objekt-Explorer**eine Verbindung mit einer [!INCLUDE[ssDE](../content/includes/ssDE_md.md)]-Instanz her.  
  
2.  Klicken Sie in der Standardleiste auf **Neue Abfrage**.  
  
3.  Kopieren Sie das folgende Beispiel, fügen Sie es in das Abfragefenster ein, und klicken Sie auf **Ausführen**.  
  
    ```  
    -- adds an alert (Test Alert) that runs the Back up the AdventureWorks2012 Database job when fired   
    -- assumes that the message 55001 and the Back up the AdventureWorks2012 Database job already exist.  
    USE msdb ;  
    GO  
  
    EXEC dbo.sp_add_alert  
        @name = N'Test Alert',  
        @message_id = 55001,   
       @severity = 0,   
       @notification_message = N'Error 55001 has occurred. The database will be backed up...',   
       @job_name = N'Back up the AdventureWorks2012 Database' ;  
    GO  
    ```  
  
Weitere Informationen finden Sie unter [Sp_add_alert (Transact-SQL)](assetId:///d9b41853-e22d-4813-a79f-57efb4511f09).  
  
