---
title: "Festlegen des Dienststartkontos f&#252;r den SQL Server-Agent (SQL Server-Konfigurations-Manager)"
ms.custom: na
ms.date: 07/15/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - tools-ssms
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 46ffe818-ebb5-43a0-840b-923f219a2472
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
# Festlegen des Dienststartkontos f&#252;r den SQL Server-Agent (SQL Server-Konfigurations-Manager)
Das Dienststartkonto des [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] -Agents definiert das Windows-Konto, unter dem der [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] -Agent ausgeführt wird, sowie die zugehörigen Netzwerkberechtigungen. In diesem Thema wird beschrieben, wie Sie das Dienstkonto für den [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] -Agent mit dem [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] -Konfigurations-Manager in [!INCLUDE[ssCurrent](../content/includes/ssCurrent_md.md)] mithilfe von [!INCLUDE[ssManStudioFull](../content/includes/ssManStudioFull_md.md)]festlegen.  
  
**In diesem Thema**  
  
-   **Vorbereitungen:**  
  
    [Einschränkungen](#Restrictions)  
  
    [Sicherheit](#Security)  
  
-   [So legen Sie das Dienststartkonto für den SQL Server-Agent mit SQL Server Management Studio fest](#SSMSProcedure)  
  
## <a name="BeforeYouBegin"></a>Vorbereitungen  
  
### <a name="Restrictions"></a>Einschränkungen  
  
-   Seit [!INCLUDE[ssVersion2005](../content/includes/ssVersion2005_md.md)] muss das Dienststartkonto für den [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)]-Agent nicht mehr ein Mitglied der Administratorengruppe von [!INCLUDE[msCoName](../content/includes/msCoName_md.md)] sein. Allerdings die [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] Agent-Dienststartkonto muss ein Mitglied der [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)]festen Serverrolle Sysadmin. Das Konto muss auch ein Mitglied der Msdb-Datenbankrolle TargetServersRole auf dem Masterserver sein, wenn die multiserver-auftragsverarbeitung verwendet wird.  
  
-   Der [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)]-Agent-Knoten wird nur im Objekt-Explorer angezeigt, wenn Sie die Berechtigung besitzen, ihn zu verwenden.  
  
### <a name="Security"></a>Sicherheit  
  
#### <a name="Permissions"></a>Berechtigungen  
Der [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] -Agent muss zur Verwendung der Anmeldeinformationen eines Kontos konfiguriert werden, das Mitglied der festen Serverrolle **sysadmin** in [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)]ist, um seine Funktionen ausführen zu können. Das Konto muss über die folgenden Windows-Berechtigungen verfügen:  
  
-   Anmelden als Dienst (SeServiceLogonRight)  
  
-   Ersetzen Sie einen Prozess\-Tokens auf Prozessebene (SeAssignPrimaryTokenPrivilege)  
  
-   Umgehen von durchsuchenden Prüfungen (SeChangeNotifyPrivilege)  
  
-   Anpassen des Arbeitsspeicherkontingents für einen Prozess (SeIncreaseQuotaPrivilege)  
  
Weitere Informationen zu den Windows-Berechtigungen erforderlich sind, für die [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] -Agent-Dienstkonto finden Sie unter [Wählen Sie ein Konto für den SQL Server-Agent-Dienst](../content/Select-an-Account-for-the-SQL-Server-Agent-Service.md) und [Einrichten von Windows-Dienstkonten](assetId:///309b9dac-0b3a-4617-85ef-c4519ce9d014).  
  
## <a name="SSMSProcedure"></a>Verwendung von SQL Server Management Studio  
  
#### So legen Sie das Dienststartkonto für den SQL Server-Agent fest  
  
1.  Klicken Sie in **Registrierte Server**auf das Pluszeichen, um **Datenbankmodul**zu erweitern.  
  
2.  Klicken Sie auf das Pluszeichen, um den Ordner **Lokale Servergruppen** zu erweitern.  
  
3.  Rechts\-Klicken Sie auf der Serverinstanz, in dem Sie das Dienststartkonto festlegen möchten, und wählen **SQL Server-Konfigurationsmanager...**.  
  
4.  Klicken Sie im Dialogfeld **Benutzerkontensteuerung** auf **Ja**.  
  
5.  Wählen Sie im [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] -Konfigurations-Manager im Konsolenbereich **SQL Server-Dienste**aus.  
  
6.  Klicken Sie im Detailbereich mit der rechten Maustaste\-Klicken Sie auf **SQL Server-Agent***(Server\_Name)*, wobei *Server\_Namen* ist der Name des der [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] -Agent-Instanz, für die Sie das Dienststartkonto ändern, und wählen Sie möchten **Eigenschaften**.  
  
7.  In der **SQL Server-Agent***(Server\_Name)* **Eigenschaften** Dialogfeld die **Anmelden** Registerkarte, wählen Sie eine der folgenden Optionen unter **Melden Sie sich als**:  
  
    -   **Erstellt\-in Konto**: Wählen Sie diese Option aus, wenn Ihre Aufträge Ressourcen vom lokalen Server benötigen. Informationen zum Auswählen eines integrierten Windows\-unter Kontotyp finden Sie unter [Auswählen eines Kontos für SQL Server-Agent-Dienst.](http://msdn.microsoft.com/library/ms191543.aspx)  
  
        > [!IMPORTANT]  
        > Die [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] -Agent-Dienst unterstützt nicht die **Lokaler Dienst** Konto [!INCLUDE[ssManStudioFull](../content/includes/ssManStudioFull_md.md)].  
  
    -   **Dieses Konto**: Wählen Sie diese Option aus, wenn Ihre Aufträge Ressourcen erfordern, über das Netzwerk, einschließlich Anwendungsressourcen, wenn Sie Ereignisse an andere Windows-Anwendungsprotokolle weiterleiten möchten oder wenn Sie Operatoren per e-Mail benachrichtigen möchten\-e-Mail oder Pager.  
  
        Bei Auswahl dieser Option:  
  
        1.  Geben Sie das Konto, das verwendet wird, um den SQL Server-Agent auszuführen, in das Feld **Kontoname** ein. Klicken Sie alternativ auf **Durchsuchen** , um das Dialogfeld **Benutzer oder Gruppe auswählen** zu öffnen, und wählen Sie das zu verwendende Konto aus.  
  
        2.  Geben Sie im Feld **Kennwort** das Kennwort für das Konto ein. Re\-Geben Sie das Kennwort in die **Kennwort bestätigen** Feld.  
  
8.  Klicken Sie auf **OK**.  
  
9. Klicken Sie im [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] -Konfigurations-Manager auf die Schaltfläche **Schließen** .  
  
