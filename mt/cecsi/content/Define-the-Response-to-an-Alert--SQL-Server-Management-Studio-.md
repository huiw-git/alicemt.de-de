---
title: "Definieren der Antwort auf eine Warnung (SQL Server Management Studio)"
ms.custom: na
ms.date: 07/15/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - tools-ssms
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: c86ca6eb-c59f-46e9-bc32-d474e7c3b170
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
# Definieren der Antwort auf eine Warnung (SQL Server Management Studio)
In diesem Thema wird beschrieben, wie Sie definieren können, wie [!INCLUDE[msCoName](../content/includes/msCoName_md.md)] [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] auf [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] -Agent-Warnungen in [!INCLUDE[ssCurrent](../content/includes/ssCurrent_md.md)] mithilfe von [!INCLUDE[ssManStudioFull](../content/includes/ssManStudioFull_md.md)] oder [!INCLUDE[tsql](../content/includes/tsql_md.md)]reagiert.  
  
**In diesem Thema**  
  
-   **Vorbereitungen:**  
  
    [Einschränkungen](#Restrictions)  
  
    [Sicherheit](#Security)  
  
-   **So definieren Sie die Antwort auf eine Warnung mit**  
  
    [SQL Server Management Studio](#SSMSProcedure)  
  
    [Transact-SQL](#TsqlProcedure)  
  
## <a name="BeforeYouBegin"></a>Vorbereitungen  
  
### <a name="Restrictions"></a>Einschränkungen  
  
-   Die Pager- und **net send** -Optionen werden in zukünftigen Versionen von [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] nicht mehr im [!INCLUDE[msCoName](../content/includes/msCoName_md.md)][!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)]. Vermeiden Sie die Verwendung dieser Funktionen bei neuen Entwicklungsarbeiten, und planen Sie die Änderung von Anwendungen, die diese Funktionen zurzeit verwenden.  
  
-   Beachten Sie, dass SQL Server-Agent konfiguriert werden müssen, um Datenbank-Mail verwenden, um e-Mail senden\-an Operatoren senden, e-Mail und Pager. Weitere Informationen finden Sie unter [Zuweisen von Warnungen zu einem Operator](http://msdn.microsoft.com/library/ms190038.aspx).  
  
-   [!INCLUDE[ssManStudioFull](../content/includes/ssManStudioFull_md.md)] können Aufträge problemlos mithilfe einer grafischen Oberfläche verwaltet werden. Dies ist die empfohlene Vorgehensweise für die Erstellung und Verwaltung der Auftragsinfrastruktur.  
  
### <a name="Security"></a>Sicherheit  
  
#### <a name="Permissions"></a>Berechtigungen  
Nur Mitglieder der festen Serverrolle **sysadmin** können die Antwort auf eine Warnung definieren.  
  
## <a name="SSMSProcedure"></a>Verwendung von SQL Server Management Studio  
  
#### So definieren Sie die Antwort auf eine Warnung  
  
1.  Klicken Sie im Objekt-Explorer ****auf das Pluszeichen, um den Server zu erweitern, der die Warnung enthält, für die Sie eine Warnung definieren möchten.  
  
2.  Klicken Sie auf das Pluszeichen, um **SQL Server-Agent**zu erweitern.  
  
3.  Klicken Sie auf das Pluszeichen, um den Ordner **Warnungen** zu erweitern.  
  
4.  Rechts\-Klicken Sie auf die Warnung, die Sie auf eine Antwort definieren, und wählen Sie **Eigenschaften**.  
  
5.  In der *Warnung\_Namen***Eigenschaften von Warnung** Dialogfeld **Wählen Sie eine Seite**, Option **Antwort**.  
  
6.  Aktivieren Sie das Kontrollkästchen **Auftrag ausführen** , und wählen Sie aus der Liste unter dem Kontrollkästchen **Auftrag ausführen** einen Auftrag aus, der ausgeführt werden soll, wenn die Warnung angezeigt wird. Sie können einen neuen Auftrag erstellen, indem Sie auf **Neuer Auftrag**klicken. Um weitere Informationen zu dem Auftrag anzuzeigen, klicken Sie auf **Auftrag anzeigen**. Weitere Informationen zu den verfügbaren Optionen in der **Neuer Auftrag** und **Auftragseigenschaften***Auftrag\_Namen* Dialogfelder, finden Sie unter [Erstellen eines Auftrags](../content/Create-a-Job.md) und [Anzeigen eines Auftrags](../content/View-a-Job.md).  
  
7.  Aktivieren Sie das Kontrollkästchen **Operatoren benachrichtigen** , sofern Sie Operatoren benachrichtigen möchten, wenn eine Warnung aktiviert ist. In der **Operatorliste**, wählen Sie eine oder mehrere der folgenden Methoden für die Benachrichtung eines Operators bzw. Operatoren: **E\-Mail**, **Pager**, oder **Net Send**. Sie können einen neuen Operator erstellen, indem Sie auf **Neuer Operator**klicken. Um weitere Informationen über einen Operator anzuzeigen, klicken Sie auf **Operator anzeigen**. Weitere Informationen zu den verfügbaren Optionen im Dialogfeld **Neuer Operator** und im Dialogfeld zum Anzeigen von Operatoreigenschaften **** unter [Create an Operator](../content/Create-an-Operator.md) und [View Information About an Operator](../content/View-Information-About-an-Operator.md).  
  
8.  Wenn Sie fertig sind, klicken Sie auf **OK**.  
  
## <a name="TsqlProcedure"></a>Mithilfe von Transact\-SQL  
  
#### So definieren Sie die Antwort auf eine Warnung  
  
1.  Stellen Sie im **Objekt-Explorer**eine Verbindung mit einer [!INCLUDE[ssDE](../content/includes/ssDE_md.md)]-Instanz her.  
  
2.  Klicken Sie in der Standardleiste auf **Neue Abfrage**.  
  
3.  Kopieren Sie das folgende Beispiel, fügen Sie es in das Abfragefenster ein, und klicken Sie auf **Ausführen**.  
  
    ```  
    -- adds an e-mail notification for Test Alert.  
    -- assumes that Test Alert already exists and that François Ajenstat is a valid operator name   
    USE msdb ;  
    GO  
  
    EXEC dbo.sp_add_notification  
     @alert_name = N'Test Alert',  
     @operator_name = N'François Ajenstat',  
     @notification_method = 1 ;  
    GO  
    ```  
  
Weitere Informationen finden Sie unter [Sp_add_notification (Transact-SQL)](assetId:///0525e0a2-ed0b-4e69-8a4c-a9e3e3622fbd).  
  
