---
title: "Konfigurieren des SQL Server-Agents"
ms.custom: na
ms.date: 07/15/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - tools-ssms
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 2e361a62-9e92-4fcd-80d7-d6960f127900
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
# Konfigurieren des SQL Server-Agents
In diesem Thema wird beschrieben, wie Sie einige Konfigurationsoptionen für den [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)]-Agent während der Installation von [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] angeben. Der vollständige Satz von [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] Agent-Konfigurationsoptionen ist nur verfügbar in [!INCLUDE[ssManStudioFull](../content/includes/ssManStudioFull_md.md)], [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] Management Objects (SMO) oder die [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] Agent gespeicherte Prozeduren.  
  
**In diesem Thema**  
  
-   **Vorbereitungen:**  
  
    [Einschränkungen](#Restrictions)  
  
    [Sicherheit](#Security)  
  
-   [Sie konfigurieren Sie den SQL Server-Agent](#SSMSProcedure)  
  
## <a name="BeforeYouBegin"></a>Vorbereitungen  
  
### <a name="Restrictions"></a>Einschränkungen  
  
-   Klicken Sie im Objekt-Explorer von **auf** SQL Server-Agent [!INCLUDE[ssManStudioFull](../content/includes/ssManStudioFull_md.md)] , um Aufträge, Operatoren, Warnungen und den [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] -Agent-Dienst zu verwalten. Der Objekt-Explorer zeigt den [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] Agent-Knoten jedoch nur dann an, wenn Sie die Berechtigung haben, ihn zu verwenden.  
  
-   Automatische\-Neustart darf nicht aktiviert werden, für die [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] Dienst oder die [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] Agent-Dienst auf dem Failovercluster-Instanzen.  
  
### <a name="Security"></a>Sicherheit  
  
#### <a name="Permissions"></a>Berechtigungen  
Der [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] -Agent muss zur Verwendung der Anmeldeinformationen eines Kontos konfiguriert werden, das Mitglied der festen Serverrolle **sysadmin** in [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)]ist, um seine Funktionen ausführen zu können. Das Konto muss über die folgenden Windows-Berechtigungen verfügen:  
  
-   Anmelden als Dienst (SeServiceLogonRight)  
  
-   Ersetzen Sie einen Prozess\-Tokens auf Prozessebene (SeAssignPrimaryTokenPrivilege)  
  
-   Umgehen von durchsuchenden Prüfungen (SeChangeNotifyPrivilege)  
  
-   Anpassen des Arbeitsspeicherkontingents für einen Prozess (SeIncreaseQuotaPrivilege)  
  
Weitere Informationen zu den Windows-Berechtigungen erforderlich sind, für die [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] -Agent-Dienstkonto finden Sie unter [Wählen Sie ein Konto für den SQL Server-Agent-Dienst](../content/Select-an-Account-for-the-SQL-Server-Agent-Service.md) und [Einrichten von Windows-Dienstkonten](assetId:///309b9dac-0b3a-4617-85ef-c4519ce9d014).  
  
## <a name="SSMSProcedure"></a>Verwendung von SQL Server Management Studio  
  
#### Sie konfigurieren Sie den SQL Server-Agent  
  
1.  Klicken Sie auf die Schaltfläche **Start** und anschließend im Menü **Start**  auf **Systemsteuerung**.  
  
2.  Klicken Sie in der Systemsteuerung unter **System und Sicherheit**auf **Verwaltung**, und wählen Sie dann **Lokale Sicherheitsrichtlinie**aus.  
  
3.  Klicken Sie in Lokale Sicherheitsrichtlinie auf das Chevron, um den Ordner **Sicherheitsrichtlinien** zu erweitern, und klicken Sie dann auf den Ordner **Zuweisen von Benutzerrechten** .  
  
4.  Rechts\-Klicken Sie auf eine Berechtigung, die Sie konfigurieren möchten, für die Verwendung mit [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] und wählen Sie **Eigenschaften**.  
  
5.  Überprüfen Sie im Eigenschaftendialogfeld der Berechtigung, ob das Konto aufgeführt ist, unter dem der [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)]-Agent ausgeführt wird. Falls dies nicht der Fall ist, klicken Sie auf **Benutzer oder Gruppe hinzufügen**, geben Sie im Dialogfeld zum Auswählen von Benutzern, Computern, Dienstkonten oder Gruppen [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)]**das Konto ein, unter dem der** -Agent ausgeführt wird, und klicken Sie dann auf **OK**.  
  
6.  Wiederholen Sie diese Schritte für jede Berechtigung, die Sie für die Ausführung mit dem [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] -Agent hinzufügen möchten. Wenn Sie fertig sind, klicken Sie auf **OK**.  
  
