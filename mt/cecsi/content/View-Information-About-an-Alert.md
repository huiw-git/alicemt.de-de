---
title: "Anzeigen von Informationen zu einer Warnung"
ms.custom: na
ms.date: 07/27/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - tools-ssms
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: a0e3a8c4-e3c2-42a5-b2f8-aa06061d3fa6
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
# Anzeigen von Informationen zu einer Warnung
In diesem Thema wird beschrieben, wie Sie Infodermationen in Bezug auf [!INCLUDE[msCoName](../content/includes/msCoName_md.md)] [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] -Agent-Warnungen in [!INCLUDE[ssCurrent](../content/includes/ssCurrent_md.md)] mithilfe von [!INCLUDE[ssManStudioFull](../content/includes/ssManStudioFull_md.md)] oder [!INCLUDE[tsql](../content/includes/tsql_md.md)]anzeigen können.  
  
**In diesem Thema**  
  
-   **Vorbereitungen:**  
  
    [Sicherheit](#Security)  
  
-   **So zeigen Sie Informationen zu einer Warnung an mit**  
  
    [SQL Server Management Studio](#SSMSProcedure)  
  
    [Transact-SQL](#TsqlProcedure)  
  
## <a name="BeforeYouBegin"></a>Vorbereitungen  
  
### <a name="Security"></a>Sicherheit  
  
#### <a name="Permissions"></a>Berechtigungen  
Standardmäßig können nur Mitglieder der festen Serverrolle **sysadmin** Information über eine Warnung anzeigen. Andere Benutzer müssen Mitglieder der festen Datenbankrolle **SQLAgentOperatorRole** in der **msdb** -Datenbank sein.  
  
## <a name="SSMSProcedure"></a>Verwendung von SQL Server Management Studio  
  
#### So zeigen Sie Informationen zu einer Warnung an  
  
1.  Klicken Sie im Objekt-Explorer **** auf das Pluszeichen, um den Server zu erweitern, auf dem Sie Informationen über eine Warnung anzeigen möchten.  
  
2.  Klicken Sie auf das Pluszeichen, um **SQL Server-Agent**zu erweitern.  
  
3.  Klicken Sie auf das Pluszeichen, um den Ordner **Warnungen** zu erweitern.  
  
4.  Rechts\-Klicken Sie auf die Warnung, dessen Daten Sie anzeigen möchten und wählen Sie **Eigenschaften**.  
  
    Weitere Informationen zu den verfügbaren Optionen, die Bestandteil der *Warnung\_Namen***Eigenschaften von Warnung** Dialogfeld finden Sie unter:  
  
    -   [Eigenschaften von Warnung - neue Warnung & #40; Seite "Allgemein" & #41;](../content/Alert-Properties---New-Alert--General-Page-.md)  
  
    -   [Eigenschaften von Warnung - neue Warnung & #40; Seite ' Antwort ' & #41;](../content/Alert-Properties---New-Alert--Response-Page-.md)  
  
    -   [Eigenschaften von Warnung - neue Warnung & #40; Optionen & #41;](../content/Alert-Properties---New-Alert--Options-Page-.md)  
  
    -   [Eigenschaften von Warnung & #40; Verlaufsseite & #41;](../content/Alert-Properties--History-Page-.md)  
  
5.  Wenn Sie fertig sind, klicken Sie auf **OK**.  
  
## <a name="TsqlProcedure"></a>Mithilfe von Transact\-SQL  
  
#### So zeigen Sie Informationen zu einer Warnung an  
  
1.  Stellen Sie im Objekt-Explorer ** **eine Verbindung mit einer [!INCLUDE[ssDE](../content/includes/ssDE_md.md)]-Instanz her.  
  
2.  Klicken Sie in der Standardleiste auf **Neue Abfrage**.  
  
3.  Kopieren Sie das folgende Beispiel, fügen Sie es in das Abfragefenster ein, und klicken Sie auf **Ausführen**.  
  
    ```  
    -- reports information about the Demo: Sev. 25 Errors alert  
    -- This example assumes that the 'Demo: Sev. 25 Errors' alert exists.  
    USE msdb ;  
    GO  
  
    EXEC sp_help_alert @alert_name = 'Demo: Sev. 25 Errors'  
    GO  
    ```  
  
Weitere Informationen finden Sie unter [Sp_help_alert (Transact-SQL)](assetId:///850cef4e-6348-4439-8e79-fd1bca712091).  
  
