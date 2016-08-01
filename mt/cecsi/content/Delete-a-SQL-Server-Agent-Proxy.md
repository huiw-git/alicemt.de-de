---
title: "L&#246;schen eines SQL Server-Agent-Proxys"
ms.custom: na
ms.date: 07/27/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - tools-ssms
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 9248841d-7294-47d4-94f3-b34a0521fabc
caps.latest.revision: 4
caps.handback.revision: 3
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
# L&#246;schen eines SQL Server-Agent-Proxys
In diesem Thema wird beschrieben, wie Sie ein [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] -Agent-Proxykonto in [!INCLUDE[ssCurrent](../content/includes/ssCurrent_md.md)] mithilfe von [!INCLUDE[ssManStudioFull](../content/includes/ssManStudioFull_md.md)] oder [!INCLUDE[tsql](../content/includes/tsql_md.md)]löschen können.  
  
**In diesem Thema**  
  
-   **Vorbereitungen:**  
  
    [Einschränkungen](#Restrictions)  
  
    [Sicherheit](#Security)  
  
-   **So löschen Sie einen SQL Server-Agent-Proxykonto mit**  
  
    [SQL Server Management Studio](#SSMSProcedure)  
  
    [Transact-SQL](#TsqlProcedure)  
  
## <a name="BeforeYouBegin"></a>Vorbereitungen  
  
### <a name="Restrictions"></a>Einschränkungen  
  
-   Wenn Sie das Proxykonto eines [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)]-Agents löschen, sollten Sie sicherstellen, dass der Proxy keine Verweise auf aktive Auftragsschritte enthält. Um für alle Schritte eines Auftrags zu überprüfen, die auf den Proxy verweisen, mit der rechten Maustaste\-Klicken Sie auf den Proxy **Eigenschaften**, und klicken Sie dann auf die *Proxy\_Namen***Proxyeigenschaften** Wählen Sie im Dialogfeld die **Verweise** Seite. Beim Löschen eines Proxys können Sie im Dialogfeld **Objekt löschen** die Auftragsschritte, die diesen Proxy verwenden, neu zuweisen.  
  
-   [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] -Agent-Proxys werden Anmeldeinformationen zum Speichern von Informationen zu Windows-Benutzerkonten verwendet. Der in der Anmeldeinformation angegebene Benutzer muss über eine Berechtigung des Typs "Anmelden als Stapelverarbeitungsauftrag" auf dem Computer verfügen, auf dem [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] ausgeführt wird.  
  
-   [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] -Agent wird der Subsystemzugriff für einen Proxy überprüft und der Zugriff auf den Proxy jedes Mal dann gewährt, wenn der Auftragsschritt ausgeführt wird. Wenn der Proxyzugriff auf das Subsystem nicht mehr länger möglich ist, erzeugt der Auftragsschritt einen Fehler. Ansonsten wird vom [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] -Agent die Identität des Benutzers angenommen, der im Proxy angegeben ist und von dem der Auftragsschritt ausgeführt wird.  
  
-   Wenn die Anmeldung für den Benutzer Zugriffsrecht auf den Proxy hat, oder der Benutzer zu einer Rolle mit Zugriffsrechten auf den Proxy gehört, kann der Benutzer den Proxy in einem Auftragsschritt verwenden.  
  
### <a name="Security"></a>Sicherheit  
  
#### <a name="Permissions"></a>Berechtigungen  
Nur Mitglieder der festen Serverrolle **sysadmin** können Proxykonten erstellen, ändern oder löschen.  
  
## <a name="SSMSProcedure"></a>Verwendung von SQL Server Management Studio  
  
#### So löschen Sie ein SQL Server-Agent-Proxykonto  
  
1.  Klicken Sie im Objekt-Explorer ****auf das Pluszeichen, um den Server zu erweitern, der das Proxykonto enthält, das Sie löschen möchten.  
  
2.  Klicken Sie auf das Pluszeichen, um **SQL Server-Agent**zu erweitern.  
  
3.  Klicken Sie auf das Pluszeichen, um den Ordner **Proxys** zu erweitern.  
  
4.  Klicken Sie auf das Pluszeichen, um das Subsystem zu erweitern, die das Proxykonto enthält Sie löschen möchten (z. B. **ActiveX-Skript)**.  
  
5.  Rechts\-Klicken Sie auf das Proxykonto an, das Sie löschen möchten und wählen Sie **Löschen**.  
  
6.  Bestätigen Sie im Dialogfeld **Objekt löschen** , dass das richtige Proxykonto ausgewählt ist. Aktivieren Sie das Kontrollkästchen **Neu zuweisen an** , um die Auftragsschritte, die auf dieses Proxykonto verweisen, einem anderen Proxykonto zuzuweisen.  
  
7.  Klicken Sie auf **OK**.  
  
## <a name="TsqlProcedure"></a>Mithilfe von Transact\-SQL  
  
#### So löschen Sie ein SQL Server-Agent-Proxykonto  
  
1.  Stellen Sie im Objekt-Explorer ** **eine Verbindung mit einer [!INCLUDE[ssDE](../content/includes/ssDE_md.md)]-Instanz her.  
  
2.  Klicken Sie in der Standardleiste auf **Neue Abfrage**.  
  
3.  Kopieren Sie das folgende Beispiel, fügen Sie es in das Abfragefenster ein, und klicken Sie auf **Ausführen**.  
  
    ```  
    -- deletes the proxy "Catalog application proxy"  
    USE msdb ;  
    GO  
    EXEC dbo.sp_delete_proxy  
        @proxy_name = N'Catalog application proxy' ;  
    GO  
    ```  
  
Weitere Informationen finden Sie unter [Sp_delete_proxy (Transact-SQL)](assetId:///44a1db13-b7f2-4dab-a1b5-b8dafb41737c).  
  
