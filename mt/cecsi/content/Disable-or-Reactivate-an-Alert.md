---
title: "Deaktivieren oder erneutes Aktivieren einer Warnung"
ms.custom: na
ms.date: 07/15/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - tools-ssms
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 4cb37dc6-1134-405d-8590-58b44dcf63b2
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
# Deaktivieren oder erneutes Aktivieren einer Warnung
In diesem Thema wird beschrieben, wie Sie eine [!INCLUDE[msCoName](../content/includes/msCoName_md.md)] [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] -Agent-Warnung in [!INCLUDE[ssCurrent](../content/includes/ssCurrent_md.md)] mithilfe von [!INCLUDE[ssManStudioFull](../content/includes/ssManStudioFull_md.md)] oder [!INCLUDE[tsql](../content/includes/tsql_md.md)]deaktivieren oder erneut aktivieren können.  
  
**In diesem Thema**  
  
-   **Vorbereitungen:**  
  
    [Sicherheit](#Security)  
  
-   **So deaktivieren oder aktivieren eine Warnung erneut mit**  
  
    [SQL Server Management Studio](#SSMSProcedure)  
  
    [Transact-SQL](#TsqlProcedure)  
  
## <a name="BeforeYouBegin"></a>Vorbereitungen  
  
### <a name="Security"></a>Sicherheit  
  
#### <a name="Permissions"></a>Berechtigungen  
Standardmäßig können nur Mitglieder der festen Serverrolle **sysadmin** Information in einer Warnung bearbeiten. Andere Benutzer müssen Mitglieder der festen Datenbankrolle **SQLAgentOperatorRole** in der **msdb** -Datenbank sein.  
  
## <a name="SSMSProcedure"></a>Verwendung von SQL Server Management Studio  
  
#### So deaktivieren oder reaktivieren Sie eine Warnung  
  
1.  Klicken Sie im Objekt-Explorer ****auf das Pluszeichen, um den Server zu erweitern, der die Warnung enthält, die Sie deaktivieren oder erneut aktivieren möchten.  
  
2.  Klicken Sie auf das Pluszeichen, um **SQL Server-Agent**zu erweitern.  
  
3.  Klicken Sie auf das Pluszeichen, um den Ordner **Warnungen** zu erweitern.  
  
4.  Rechts\-Klicken Sie auf die Warnung, die Sie verwenden möchten, aktivieren, und wählen Sie **aktivieren** um eine Warnung zu deaktivieren, mit der rechten Maustaste\-Klicken Sie auf die Warnung, die Sie deaktivieren möchten und wählen Sie **deaktivieren**.  
  
5.  Die Dialogfelder **Warnungen deaktivieren** oder **Warnungen aktivieren** werden angezeigt. Außerdem wird der Status des Vorgangs angezeigt. Wenn Sie fertig sind, klicken Sie auf **Schließen**.  
  
## <a name="TsqlProcedure"></a>Mithilfe von Transact\-SQL  
  
#### So deaktivieren oder reaktivieren Sie eine Warnung  
  
1.  Stellen Sie im Objekt-Explorer ** **eine Verbindung mit einer [!INCLUDE[ssDE](../content/includes/ssDE_md.md)]-Instanz her.  
  
2.  Klicken Sie in der Standardleiste auf **Neue Abfrage**.  
  
3.  Kopieren Sie das folgende Beispiel, fügen Sie es in das Abfragefenster ein, und klicken Sie auf **Ausführen**.  
  
    ```  
    -- changes the enabled setting of Test Alert to 0  
    USE msdb ;  
    GO  
  
    EXEC dbo.sp_update_alert  
        @name = N'Test Alert',  
        @enabled = 0 ;  
    GO  
    ```  
  
Weitere Informationen finden Sie unter [Sp_update_alert (Transact-SQL)](assetId:///4bbaeaab-8aca-4c9e-abc1-82ce73090bd3).  
  
