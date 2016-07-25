---
title: "Configure a User to Create and Manage SQL Server Agent Jobs"
ms.custom: na
ms.date: 07/15/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - tools-ssms
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 67897e3e-b7d0-43dd-a2e2-2840ec4dd1ef
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
# Configure a User to Create and Manage SQL Server Agent Jobs
In diesem Thema wird beschrieben, wie Sie einen Benutzer zum Erstellen oder Ausführen von [!INCLUDE[msCoName](../content/includes/msCoName_md.md)] [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] -Agent-Aufträgen konfigurieren.  
  
-   **Vorbereitungen:**  [Sicherheit](#Security)  
  
-   **Konfigurieren eines Benutzers zum Erstellen und Verwalten von SQL Server-Agent-Aufträgen mit:**  [SQL Server Management Studio](#SSMS)  
  
## <a name="BeforeYouBegin"></a>Vorbereitungen  
  
### <a name="Security"></a>Sicherheit  
So konfigurieren Sie einen Benutzer erstellen oder ausführen [!INCLUDE[msCoName](../content/includes/msCoName_md.md)] [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] Agent-Aufträge müssen Sie zunächst eine vorhandene SQL Server-Anmeldung oder Msdb-Rolle hinzufügen, um einen der folgenden [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] Agent festen Datenbankrollen in der Msdb-Datenbank: SQLAgentUserRole, SQLAgentReaderRole oder SQLAgentOperatorRole.  
  
Standardmäßig können Mitglieder dieser Datenbankrollen ihre eigenen Auftragsschritte erstellen, die unter ihrem Konto ausgeführt werden. Wenn diese nicht\-Administratoren zum Ausführen von Aufträgen, die andere Arten von Auftragsschritten ausgeführt werden soll (z. B. [!INCLUDE[ssIS](../content/includes/ssIS_md.md)] Pakete), müssen sie den Zugriff auf ein Proxykonto. Alle Mitglieder der festen Serverrolle Sysadmin haben die Berechtigung zum Erstellen, ändern und Löschen von Proxykonten. Weitere Informationen zu den Berechtigungen, die mit diesen verknüpft sind [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] Agent festen Datenbankrollen finden Sie unter [SQL Server-Agent-festen Datenbankrollen](../content/SQL-Server-Agent-Fixed-Database-Roles.md).  
  
#### <a name="Permissions"></a>Berechtigungen  
Ausführliche Informationen finden Sie unter [Implement SQL Server Agent Security](../content/Implement-SQL-Server-Agent-Security.md).  
  
## <a name="SSMS"></a>Verwendung von SQL Server Management Studio  
**So fügen Sie einer festen Datenbankrolle des SQL Server-Agents einen SQL-Anmeldenamen oder eine msdb-Rolle hinzu**  
  
1.  Erweitern Sie im **Objekt-Explorer**einen Server.  
  
2.  Erweitern Sie **Sicherheit**und anschließend **Anmeldungen**.  
  
3.  Rechts\-Klicken Sie auf die Anmeldung, die Sie hinzufügen möchten ein [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] Agent, der festen Datenbankrolle, und wählen **Eigenschaften**.  
  
4.  Wählen Sie auf der Seite **Benutzerzuordnung** des Dialogfelds **Anmeldungseigenschaften** die Zeile aus, die **msdb**enthält.  
  
5.  Aktivieren Sie unter **Mitgliedschaft in Datenbankrolle für: msdb**das Kontrollkästchen für die entsprechende feste Datenbankrolle des [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] -Agents.  
  
**So konfigurieren Sie ein Proxykonto zum Erstellen und Verwalten von Auftragsschritten des SQL Server-Agents**  
  
1.  Erweitern Sie im **Objekt-Explorer**einen Server.  
  
2.  Erweitern Sie **SQL Server-Agent**.  
  
3.  Rechts\-Klicken Sie auf **Proxys** und wählen Sie **neuen Proxy**.  
  
4.  Geben Sie im Dialogfeld **Neues Proxykonto** auf der Seite **Allgemein** den Proxynamen, den Anmeldeinformationsnamen und eine Beschreibung für den neuen Proxy an. Beachten Sie, dass Sie Anmeldeinformationen erstellen müssen, bevor Sie ein Proxykonto des SQL Server-Agents erstellen. Weitere Informationen zum Erstellen von Anmeldeinformationen finden Sie unter [Gewusst wie: Erstellen von Anmeldeinformationen (SQL Server Management Studio)](assetId:///c1e77e91-2a69-40d9-b8b3-97cffc710586) und [CREATE CREDENTIAL (Transact-SQL)](assetId:///d5e9ae69-41d9-4e46-b13d-404b88a32d9d).  
  
5.  Aktivieren Sie die entsprechenden Subsysteme für diesen Proxy.  
  
6.  Auf der Seite **Prinzipale** können Sie Anmeldenamen oder Rollen hinzufügen oder entfernen, um den Zugriff auf das Proxykonto zu erteilen oder zu entziehen.  
  
## Siehe auch  
[Implementieren von SQL Server-Agent-Sicherheit](../content/Implement-SQL-Server-Agent-Security.md)  
  
