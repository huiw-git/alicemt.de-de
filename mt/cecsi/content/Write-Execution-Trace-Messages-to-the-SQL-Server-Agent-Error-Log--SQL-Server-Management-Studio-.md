---
title: "Schreiben von Meldungen zur Ablaufverfolgung in das SQL Server-Agent-Fehlerprotokoll (SQL Server Management Studio)"
ms.custom: na
ms.date: 07/15/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - tools-ssms
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 90e3731e-6fae-43db-833e-9accecdd1c03
caps.latest.revision: 6
caps.handback.revision: 5
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
# Schreiben von Meldungen zur Ablaufverfolgung in das SQL Server-Agent-Fehlerprotokoll (SQL Server Management Studio)
In diesem Thema wird die Vorgehensweise zum Konfigurieren des [!INCLUDE[msCoName](../content/includes/msCoName_md.md)] [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] -Agents zum Einschließen von Meldungen zur Ablaufverfolgung in das Fehlerprotokoll in [!INCLUDE[ssCurrent](../content/includes/ssCurrent_md.md)] mithilfe von [!INCLUDE[ssManStudioFull](../content/includes/ssManStudioFull_md.md)]beschrieben.  
  
**In diesem Thema**  
  
-   **Vorbereitungen:**  
  
    [Einschränkungen](#Restrictions)  
  
    [Sicherheit](#Security)  
  
-   So schreiben Sie Meldungen zur Ablaufverfolgung in das SQL Server-Agent-Fehlerprotokoll mit SQL Server Management Studio  
  
## <a name="BeforeYouBegin"></a>Vorbereitungen  
  
### <a name="Restrictions"></a>Einschränkungen  
  
-   Der [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] -Agent-Knoten wird nur im Objekt-Explorer angezeigt, wenn Sie die Berechtigung besitzen, ihn zu verwenden.  
  
-   Schließen Sie Meldungen zur Ablaufverfolgung in [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] -Agent-Fehlerprotokolle ein, wenn Sie ein bestimmtes Problem des [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] -Agents untersuchen, denn die Option kann dazu führen, dass das Fehlerprotokoll sehr umfangreich wird.  
  
### <a name="Security"></a>Sicherheit  
  
#### <a name="Permissions"></a>Berechtigungen  
Der [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] -Agent muss zur Verwendung der Anmeldeinformationen eines Kontos konfiguriert werden, das Mitglied der festen Serverrolle **sysadmin** in [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)]ist, um seine Funktionen ausführen zu können. Das Konto muss über die folgenden Windows-Berechtigungen verfügen:  
  
-   Anmelden als Dienst (SeServiceLogonRight)  
  
-   Ersetzen Sie einen Prozess\-Tokens auf Prozessebene (SeAssignPrimaryTokenPrivilege)  
  
-   Umgehen von durchsuchenden Prüfungen (SeChangeNotifyPrivilege)  
  
-   Anpassen des Arbeitsspeicherkontingents für einen Prozess (SeIncreaseQuotaPrivilege)  
  
Weitere Informationen zu den Windows-Berechtigungen erforderlich sind, für die [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] -Agent-Dienstkonto finden Sie unter [Wählen Sie ein Konto für den SQL Server-Agent-Dienst](../content/Select-an-Account-for-the-SQL-Server-Agent-Service.md) und [Einrichten von Windows-Dienstkonten](assetId:///309b9dac-0b3a-4617-85ef-c4519ce9d014).  
  
## <a name="SSMSProcedure"></a>  
#### So schreiben Sie Meldungen zur Ablaufverfolgung in das SQL Server-Agent-Fehlerprotokoll  
  
1.  Klicken Sie im Objekt-Explorer ****auf das Pluszeichen neben dem Server, der das [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] -Agent-Fehlerprotokoll enthält, in das Sie Meldungen zur Ablaufverfolgung schreiben möchten.  
  
2.  Rechts\-Klicken Sie auf **SQL Server-Agent** und wählen Sie **Eigenschaften**.  
  
3.  In der **SQL Server-Agent-Eigenschaften –***Server\_Namen* Dialogfeld **Fehlerprotokoll** auf die **Allgemein** Seite auf die **enthalten Meldungen zur Ablaufverfolgung** das Kontrollkästchen.  
  
4.  Klicken Sie auf **OK**.  
  
