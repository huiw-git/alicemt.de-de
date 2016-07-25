---
title: "&#196;ndern eines SQL Server-Agent-Proxys"
ms.custom: na
ms.date: 07/15/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - tools-ssms
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 6e1dfbaa-8089-4813-940c-d5a2e13d8552
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
# &#196;ndern eines SQL Server-Agent-Proxys
In diesem Thema wird beschrieben, wie Sie ein [!INCLUDE[msCoName](../content/includes/msCoName_md.md)] [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] -Agent-Proxy in [!INCLUDE[ssCurrent](../content/includes/ssCurrent_md.md)] mithilfe von [!INCLUDE[ssManStudioFull](../content/includes/ssManStudioFull_md.md)] oder [!INCLUDE[tsql](../content/includes/tsql_md.md)]ändern können.  
  
**In diesem Thema**  
  
-   **Vorbereitungen:**  
  
    [Einschränkungen](#Restrictions)  
  
    [Sicherheit](#Security)  
  
-   **So ändern Sie einen SQL Server-Agent-Proxy mit**  
  
    [SQL Server Management Studio](#SSMSProcedure)  
  
    [Transact-SQL](#TsqlProcedure)  
  
## <a name="BeforeYouBegin"></a>Vorbereitungen  
  
### <a name="Restrictions"></a>Einschränkungen  
  
-   [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] -Agent-Proxys werden Anmeldeinformationen zum Speichern von Informationen zu Windows-Benutzerkonten verwendet. Der in der Anmeldeinformation angegebene Benutzer muss über eine Berechtigung des Typs "Anmelden als Stapelverarbeitungsauftrag" auf dem Computer verfügen, auf dem [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] ausgeführt wird.  
  
-   [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] -Agent wird der Subsystemzugriff für einen Proxy überprüft und der Zugriff auf den Proxy jedes Mal dann gewährt, wenn der Auftragsschritt ausgeführt wird. Wenn der Proxyzugriff auf das Subsystem nicht mehr länger möglich ist, erzeugt der Auftragsschritt einen Fehler. Ansonsten wird vom [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] -Agent die Identität des Benutzers angenommen, der im Proxy angegeben ist und von dem der Auftragsschritt ausgeführt wird.  
  
-   Wenn die Anmeldung für den Benutzer Zugriffsrecht auf den Proxy hat, oder der Benutzer zu einer Rolle mit Zugriffsrechten auf den Proxy gehört, kann der Benutzer den Proxy in einem Auftragsschritt verwenden.  
  
### <a name="Security"></a>Sicherheit  
  
#### <a name="Permissions"></a>Berechtigungen  
Nur Mitglieder der festen Serverrolle **sysadmin** können Proxykonten erstellen, ändern oder löschen.  
  
## <a name="SSMSProcedure"></a>Verwendung von SQL Server Management Studio  
  
#### So ändern Sie einen [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] -Agent-Proxy  
  
1.  Klicken Sie im Objekt-Explorer ****auf das Pluszeichen, um den Server zu erweitern, der das [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] -Agent-Proxykonto enthält, das Sie ändern möchten.  
  
2.  Klicken Sie auf das Pluszeichen, um **SQL Server-Agent**zu erweitern.  
  
3.  Klicken Sie auf das Pluszeichen, um den Ordner **Proxys** zu erweitern.  
  
4.  Klicken Sie auf das Pluszeichen, um den subsystemknoten für den Proxy zu erweitern (z. B. **ActiveX-Skript**).  
  
5.  Rechts\-Klicken Sie auf das Proxykonto zu ändern, und wählen Sie **Eigenschaften**.  
  
6.  In der *Proxy\_Namen***Proxyeigenschaften** Dialogfeld ändern Sie den Proxy Konto nach Bedarf. Weitere Informationen zu den Optionen in diesem Dialogfeld finden Sie unter [Erstellen Sie eine SQL Server-Agent-Proxy](../content/Create-a-SQL-Server-Agent-Proxy.md).  
  
7.  Wenn Sie fertig sind, klicken Sie auf **OK**.  
  
## <a name="TsqlProcedure"></a>Mithilfe von Transact\-SQL  
  
#### So ändern Sie einen [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] -Agent-Proxy  
  
1.  Stellen Sie im Objekt-Explorer ** **eine Verbindung mit einer [!INCLUDE[ssDE](../content/includes/ssDE_md.md)]-Instanz her.  
  
2.  Klicken Sie in der Standardleiste auf **Neue Abfrage**.  
  
3.  Kopieren Sie das folgende Beispiel, fügen Sie es in das Abfragefenster ein, und klicken Sie auf **Ausführen**.  
  
    ```  
    -- Disables the proxy named 'Catalog application proxy'.  
    USE msdb ;  
    GO  
    EXEC dbo.sp_update_proxy  
        @proxy_name = 'Catalog application proxy',  
        @enabled = 0;  
    GO  
    ```  
  
Weitere Informationen finden Sie unter [Sp_update_proxy (Transact-SQL)](assetId:///864fd0e6-9d61-4f07-92ef-145318d2f881).  
  
