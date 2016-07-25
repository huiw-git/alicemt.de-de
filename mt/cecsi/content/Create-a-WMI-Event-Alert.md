---
title: "Erstellen einer WMI-Ereigniswarnung"
ms.custom: na
ms.date: 07/15/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - tools-ssms
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: b8c46db6-408b-484e-98f0-a8af3e7ec763
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
# Erstellen einer WMI-Ereigniswarnung
In diesem Thema wird beschrieben, wie Sie in [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] mithilfe von [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] oder [!INCLUDE[ssCurrent](../content/includes/ssCurrent_md.md)] eine Warnung des [!INCLUDE[ssManStudioFull](../content/includes/ssManStudioFull_md.md)]-Agents erstellen, die beim Auftreten eines bestimmten [!INCLUDE[tsql](../content/includes/tsql_md.md)]-Ereignisses ausgelöst wird, das vom WMI-Anbieter für Serverereignisse überwacht wird.  
  
Informationen zur Verwendung der WMI-Anbieter zum Überwachen von [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] -Ereignissen finden Sie unter [WMI-Anbieter für Eigenschaften und Ereignisse Serverklassen](assetId:///80767fe0-32ac-406a-81a0-8212cd6ce7e4). Informationen über die erforderlichen Berechtigungen zum WMI-ereignisbenachrichtigungen erhalten, finden Sie unter [Wählen Sie ein Konto für den SQL Server-Agent-Dienst](../content/Select-an-Account-for-the-SQL-Server-Agent-Service.md). Weitere Informationen zu WQL finden Sie unter [Verwenden von WQL mit dem WMI-Anbieter für Serverereignisse](assetId:///58b67426-1e66-4445-8e2c-03182e94c4be).  
  
**In diesem Thema**  
  
-   **Vorbereitungen:**  
  
    [Einschränkungen](#Restrictions)  
  
    [Sicherheit](#Security)  
  
-   **Erstellen einer WMI-Ereigniswarnung mit:**  
  
    [SQL Server Management Studio](#SSMSProcedure)  
  
    [Transact-SQL](#TsqlProcedure)  
  
## <a name="BeforeYouBegin"></a>Vorbereitungen  
  
### <a name="Restrictions"></a>Einschränkungen  
  
-   [!INCLUDE[ssManStudioFull](../content/includes/ssManStudioFull_md.md)] lässt sich das gesamte Warnungssystem auf einfache Weise mit einer grafischen Oberfläche verwalten. Dies ist die empfohlene Vorgehensweise, um eine Warnungsinfrastruktur zu konfigurieren.  
  
-   Mit generierten Ereignisse **Xp\_Logevent** treten in der master-Datenbank. Aus diesem Grund **Xp\_Logevent** löst keine Warnung aus, es sei denn, die **@database\_Namen** für die Warnung **'master'** oder NULL.  
  
-   Es werden nur WMI-Namespaces auf dem Computer unterstützt, auf dem der [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)]-Agent ausgeführt wird.  
  
### <a name="Security"></a>Sicherheit  
  
#### <a name="Permissions"></a>Berechtigungen  
Standardmäßig nur Mitglieder der **Sysadmin** feste Serverrolle **sp\_Hinzufügen\_Warnung**.  
  
## <a name="SSMSProcedure"></a>Verwendung von SQL Server Management Studio  
  
#### So erstellen Sie eine WMI-Ereigniswarnung  
  
1.  Klicken Sie im **** Objekt-Explorer auf das Pluszeichen, um den Server zu erweitern, auf dem Sie eine WMI-Ereigniswarnung erstellen möchten.  
  
2.  Klicken Sie auf das Pluszeichen, um **SQL Server-Agent**zu erweitern.  
  
3.  Rechts\-Klicken Sie auf **Warnungen** und wählen Sie **neue Warnung**.  
  
4.  Geben Sie im Dialogfeld **Neue Warnung** einen ** ** Namen für diese Warnung ein.  
  
5.  Aktivieren Sie das Kontrollkästchen **Aktivieren** , um die Ausführung der Warnung zu ermöglichen. Standardmäßig ist **Aktivieren** aktiviert.  
  
6.  Klicken Sie in der Liste **Typ** auf **WMI-Ereigniswarnung**.  
  
7.  Unter **WMI-ereigniswarnungsdefinition**, in den **Namespace** geben den WMI-Namespace für die Windows-Verwaltungsinstrumentation (WMI Query Language, WQL)-Anweisung, die die WMI-Ereignis identifiziert diese Warnung auslöst.  
  
8.  Geben Sie im Feld **Abfrage** die WQL-Anweisung an, die das Ereignis identifiziert, auf das diese Warnung reagiert.  
  
9. Klicken Sie auf **OK**.  
  
## <a name="TsqlProcedure"></a>Mithilfe von Transact\-SQL  
  
#### So erstellen Sie eine WMI-Ereigniswarnung  
  
1.  Stellen Sie im Objekt-Explorer ** **eine Verbindung mit einer [!INCLUDE[ssDE](../content/includes/ssDE_md.md)]-Instanz her.  
  
2.  Klicken Sie in der Standardleiste auf **Neue Abfrage**.  
  
3.  Kopieren Sie das folgende Beispiel, fügen Sie es in das Abfragefenster ein, und klicken Sie auf **Ausführen**.  
  
    ```  
    -- creates a WMI event alert that retrieves all event properties for any ALTER_TABLE event that occurs on table AdventureWorks2012.Sales.SalesOrderDetail  
    -- This example assumes that the message 54001 already exists.  
    USE msdb ;  
    GO  
  
    EXEC dbo.sp_add_alert  
        @name = N'Test Alert 2',  
        @message_id = 54001  
        @notification_message = N'Error 54001 has occurred on the Sales.SalesOrderDetail table on the AdventureWorks2012 database. Please see the following information…',  
        @wmi_namespace = '\\.\root\Microsoft\SqlServer\ServerEvents\,  
        @wmi_query = N'SELECT * FROM ALTER_TABLE   
    WHERE DatabaseName = 'AdventureWorks2012' AND SchemaName = 'Sales'   
        AND ObjectType='Table' AND ObjectName = 'SalesOrderDetail'';  
    GO  
    ```  
  
Weitere Informationen finden Sie unter [Sp_add_alert (Transact-SQL)](assetId:///d9b41853-e22d-4813-a79f-57efb4511f09).  
  
