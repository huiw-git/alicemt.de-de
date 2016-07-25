---
title: "Senden von SQL Server-Agent-Fehlermeldungen"
ms.custom: na
ms.date: 07/15/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - tools-ssms
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 2597d0d7-951a-48cf-989f-abb67b9fdb36
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
# Senden von SQL Server-Agent-Fehlermeldungen
In diesem Thema wird beschrieben, wie der [!INCLUDE[msCoName](../content/includes/msCoName_md.md)] [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] -Agent konfiguriert wird, sodass Agent-Fehlermeldungen mit NET SEND in [!INCLUDE[ssCurrent](../content/includes/ssCurrent_md.md)] mithilfe von [!INCLUDE[ssManStudioFull](../content/includes/ssManStudioFull_md.md)]übermittelt werden.  
  
**In diesem Thema**  
  
-   **Vorbereitungen:**  
  
    [Einschränkungen](#Restrictions)  
  
    [Sicherheit](#Security)  
  
-   [So senden Sie SQL Server-Agent-Fehlermeldungen mithilfe von SQL Server Management Studio](#SSMSProcedure)  
  
## <a name="BeforeYouBegin"></a>Vorbereitungen  
  
### <a name="Restrictions"></a>Einschränkungen  
  
-   Der [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] -Agent-Knoten wird nur im Objekt-Explorer angezeigt, wenn Sie die Berechtigung besitzen, ihn zu verwenden.  
  
-   Der [!INCLUDE[msCoName](../content/includes/msCoName_md.md)] Windows Messenger-Dienst muss ausgeführt werden, damit NET SEND-Ereignisse empfangen werden können.  
  
### <a name="Security"></a>Sicherheit  
  
#### <a name="Permissions"></a>Berechtigungen  
Der [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] -Agent muss zur Verwendung der Anmeldeinformationen eines Kontos konfiguriert werden, das Mitglied der festen Serverrolle **sysadmin** in [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)]ist, um seine Funktionen ausführen zu können. Das Konto muss über die folgenden Windows-Berechtigungen verfügen:  
  
-   Anmelden als Dienst (SeServiceLogonRight)  
  
-   Ersetzen Sie einen Prozess\-Tokens auf Prozessebene (SeAssignPrimaryTokenPrivilege)  
  
-   Umgehen von durchsuchenden Prüfungen (SeChangeNotifyPrivilege)  
  
-   Anpassen des Arbeitsspeicherkontingents für einen Prozess (SeIncreaseQuotaPrivilege)  
  
Weitere Informationen zu den Windows-Berechtigungen erforderlich sind, für die [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] -Agent-Dienstkonto finden Sie unter [Wählen Sie ein Konto für den SQL Server-Agent-Dienst](../content/Select-an-Account-for-the-SQL-Server-Agent-Service.md) und [Einrichten von Windows-Dienstkonten](assetId:///309b9dac-0b3a-4617-85ef-c4519ce9d014).  
  
## <a name="SSMSProcedure"></a>Verwendung von SQL Server Management Studio  
  
#### So senden Sie SQL Server-Agent-Fehlermeldungen  
  
1.  Klicken Sie im **Objekt-Explorer**auf das Pluszeichen neben dem Server, der das [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] -Agent-Fehlerprotokoll enthält, von dem Sie Fehlermeldungen über NET SEND senden möchten.  
  
2.  Rechts\-Klicken Sie auf **SQL Server-Agent** und wählen Sie **Eigenschaften**.  
  
3.  In der **SQL Server-Agent-Eigenschaften –***Server\_Namen* Dialogfeld **Fehlerprotokoll** auf die **Allgemein** Seite, geben Sie den Benutzernamen oder Computernamen, die Fehlermeldungen gesendet werden soll, die **Net send-Empfänger** Feld.  
  
4.  Klicken Sie auf **OK**.  
  
