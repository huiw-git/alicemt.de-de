---
title: "Festlegen der SQL Server-Verbindung f&#252;r den SQL Server-Agent-Dienst (SQL Server Management Studio)"
ms.custom: na
ms.date: 07/27/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - tools-ssms
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 28b6178b-0a9e-4f2c-8562-7a62d2d2a285
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
# Festlegen der SQL Server-Verbindung f&#252;r den SQL Server-Agent-Dienst (SQL Server Management Studio)
In diesem Thema wird beschrieben, wie Sie die Verbindung zwischen dem [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] -Agent und [!INCLUDE[ssDE](../content/includes/ssDE_md.md)] in [!INCLUDE[ssCurrent](../content/includes/ssCurrent_md.md)] mithilfe von [!INCLUDE[ssManStudioFull](../content/includes/ssManStudioFull_md.md)]festlegen. Mithilfe des [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] -Agent-Diensts kann eine Verbindung mit einer lokalen Instanz von SQL Server mit der Windows-Authentifizierung hergestellt werden.  
  
**In diesem Thema**  
  
-   **Vorbereitungen:**  
  
    [Einschränkungen](#Restrictions)  
  
    [Sicherheit](#Security)  
  
-   **Festlegen der SQL Server-Verbindung für den SQL Server-Agent mit:**  
  
    [SQL Server Management Studio](#SSMSProcedure)  
  
## <a name="BeforeYouBegin"></a>Vorbereitungen  
  
### <a name="Restrictions"></a>Einschränkungen  
  
-   Der [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] -Agent-Knoten wird nur im Objekt-Explorer angezeigt, wenn Sie die Berechtigung besitzen, ihn zu verwenden.  
  
-   Seit [!INCLUDE[ssVersion2005](../content/includes/ssVersion2005_md.md)]unterstützt der [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] -Agent keine [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] -Authentifizierung. Diese Option ist nur beim Verwalten früherer Versionen von [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)]verfügbar.  
  
### <a name="Security"></a>Sicherheit  
  
#### <a name="Permissions"></a>Berechtigungen  
Der [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] -Agent muss zur Verwendung der Anmeldeinformationen eines Kontos konfiguriert werden, das Mitglied der festen Serverrolle **sysadmin** in [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)]ist, um seine Funktionen ausführen zu können. Das Konto muss über die folgenden Windows-Berechtigungen verfügen:  
  
-   Anmelden als Dienst (SeServiceLogonRight)  
  
-   Ersetzen Sie einen Prozess\-Tokens auf Prozessebene (SeAssignPrimaryTokenPrivilege)  
  
-   Umgehen von durchsuchenden Prüfungen (SeChangeNotifyPrivilege)  
  
-   Anpassen des Arbeitsspeicherkontingents für einen Prozess (SeIncreaseQuotaPrivilege)  
  
Weitere Informationen zu den Windows-Berechtigungen erforderlich sind, für die [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] -Agent-Dienstkonto finden Sie unter [Wählen Sie ein Konto für den SQL Server-Agent-Dienst](../content/Select-an-Account-for-the-SQL-Server-Agent-Service.md) und [Einrichten von Windows-Dienstkonten](assetId:///309b9dac-0b3a-4617-85ef-c4519ce9d014).  
  
## <a name="SSMSProcedure"></a>Verwendung von SQL Server Management Studio  
  
#### So legen Sie die SQL Server-Verbindung fest  
  
1.  Klicken Sie im **Objekt-Explorer**auf das Pluszeichen, um den Server zu erweitern, für den Sie eine Verbindung mit dem SQL Server-Agent-Dienst einrichten möchten.  
  
2.  Rechts\-Klicken Sie auf **SQL Server-Agent** und wählen Sie **Eigenschaften**.  
  
3.  In der **Eigenschaften des SQL Server-Agent***Server\_Namen* Dialogfeld **Wählen Sie eine Seite**, klicken Sie auf **Verbindung**.  
  
4.  Wählen Sie unter **SQL Server-Verbindung**die Option **Windows-Authentifizierung verwenden** aus, damit der [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] -Agent beim Herstellen einer Verbindung mit einer Instanz von [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] [!INCLUDE[ssDE](../content/includes/ssDE_md.md)] die [!INCLUDE[msCoName](../content/includes/msCoName_md.md)] Windows-Authentifizierung verwenden kann. Für Verbindungen mit [!INCLUDE[ssVersion2005](../content/includes/ssVersion2005_md.md)] und höher muss die Windows-Authentifizierung verwendet werden.  
  
