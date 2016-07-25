---
title: "Implementieren der SQL Server-Agent-Sicherheit"
ms.custom: na
ms.date: 07/15/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - tools-ssms
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: d770d35c-c8de-4e00-9a85-7d03f45a0f0d
caps.latest.revision: 4
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
# Implementieren der SQL Server-Agent-Sicherheit
[!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] -Agent kann den Datenbankadministrator jeden Auftragsschritt in einem Sicherheitskontext ausführen, die nur die erforderlichen Berechtigungen zum Durchführen dieses Auftragsschritts, der vom bestimmt wird ein [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] -Agent-Proxy. Um Berechtigungen für einen bestimmten Auftragsschritt festzulegen, erstellen Sie einen Proxy mit den erforderlichen Berechtigungen und weisen dann diesen Proxy dem Auftragsschritt zu. Ein Proxy kann für mehrere Auftragsschritte angegeben werden. Für Auftragsschritte, für die dieselben Berechtigungen erforderlich sind, verwenden Sie denselben Proxy.  
  
Im folgenden Abschnitt wird erläutert, welche Datenbankrolle Sie Benutzern erteilen müssen, damit sie Aufträge mithilfe des [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)]-Agents erstellen oder ausführen können.  
  
## Erteilen des Zugriffs auf den SQL Server-Agent  
Um den [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)]-Agent zu verwenden, müssen die Benutzer Mitglied mindestens einer der folgenden festen Datenbankrollen sein:  
  
-   **SQLAgentUserRole**  
  
-   **SQLAgentReaderRole**  
  
-   **SQLAgentOperatorRole**  
  
Diese Funktionen befinden sich der **Msdb** Datenbank. Standardmäßig ist kein Benutzer Mitglied dieser Datenbankrollen. Die Mitgliedschaft in diesen Rollen muss explizit erteilt werden. Mitglieder von der **Sysadmin** -Serverrolle verfügen über Vollzugriff auf [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] -Agent, und müssen nicht Mitglied dieser festen Datenbankrollen verwenden [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] Agent. Ist ein Benutzer nicht Mitglied einer dieser Datenbankrollen oder der die **Sysadmin** Rolle, die [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] -Agent-Knoten ist nicht verfügbar, bei der Verbindung [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] mit [!INCLUDE[ssManStudioFull](../content/includes/ssManStudioFull_md.md)].  
  
Die Mitglieder dieser Datenbankrollen können Aufträge anzeigen und ausführen, deren Besitzer sie sind, und Auftragsschritte erstellen, die als bereits vorhandenes Proxykonto ausgeführt werden. Weitere Informationen zu den einzelnen Berechtigungen, die jeder dieser Rollen zugeordnet sind, finden Sie unter [SQL Server-Agent festen Datenbankrollen](../content/SQL-Server-Agent-Fixed-Database-Roles.md).  
  
Mitglieder der **Sysadmin** festen Serverrolle über die Berechtigung zum Erstellen, ändern und Löschen von Proxykonten. Mitglieder der **Sysadmin** Rolle über die Berechtigung zum Auftragsschritte erstellen, geben Sie einen Proxy nicht, sondern stattdessen als ausführen, der [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] -Agent-Dienstkonto wird das Konto, das zum Starten [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] Agent.  
  
## Richtlinien  
Befolgen Sie diese Richtlinien, um die Sicherheit Ihrer [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)]-Agent-Implementierung zu verbessern:  
  
-   Erstellen Sie dedizierte Benutzerkonten speziell für Proxys, und verwenden Sie diese Proxybenutzerkonten nur zum Ausführen von Auftragsschritten.  
  
-   Erteilen Sie die erforderlichen Berechtigungen lediglich den Proxybenutzerkonten. Erteilen Sie lediglich die Berechtigungen, die zum Ausführen der Auftragsschritte erforderlich sind, die einem bestimmten Proxykonto zugewiesen sind.  
  
-   Führen Sie nicht die [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] Agent-Dienst unter einem Microsoft Windows-Benutzerkonto, das ein Mitglied der Windows **Administratoren** Gruppe.  
  
-   Proxys sind nur so sicher wie der [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)]-Anmeldeinformationenspeicher.  
  
-   Wenn Benutzerschreibvorgänge in das NT-Ereignisprotokoll schreiben können, können sie Warnungen über den [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)]-Agent auslösen.  
  
-   Geben Sie das NT-Adminkonto nicht als Dienst- oder Proxykonto an.  
  
-   Hinweis: [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] und der [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)]-Agent können gegenseitig auf ihre Ressourcen zugreifen. Die beiden Dienste verwenden einen einzelnen Prozessraum, und der [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)]-Agent fungiert mit der Rolle "sysadmin" auf dem [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)]-Dienst.  
  
-   Wenn für ein TSX ein MSX eingetragen wird, erhält die MSX-Rolle "sysadmins" die vollständige Kontrolle über die TSX-Instanz von [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)].  
  
-   ACE ist eine Erweiterung und kann sich nicht selbst aufrufen. ACE wird von der "Chainer ScenarioEngine.exe" (auch als bekannt als "Microsoft.SqlServer.Chainer.Setup.exe") oder einem anderen Hostprozess aufgerufen.  
  
-   ACE hängt von den folgenden Konfigurations-DLL-Elementen ab, die sich im Besitz von SSDP befinden, da diese DLL-APIs von ACE aufgerufen werden:  
  
    -   **SCO** – Microsoft.SqlServer.Configuration.Sco.dll, einschließlich neue SCO-Überprüfungen für virtuelle Konten  
  
    -   **Cluster** – Microsoft.SqlServer.Configuration.Cluster.dll  
  
    -   **SFC** – Microsoft.SqlServer.Configuration.SqlConfigBase.dll  
  
    -   **Erweiterung** – Microsoft.SqlServer.Configuration.ConfigExtension.dll  
  
## Siehe auch  
[Verwenden vordefinierter Rollen](assetId:///6b46db51-7c30-467d-a251-50f50647fe21)  
[sp_addrolemember (Transact-SQL)](assetId:///a583c087-bdb3-46d2-b9e5-3921b3e6d10b)  
[sp_droprolemember (Transact-SQL)](assetId:///c2f19ab1-e742-4d56-ba8e-8ffd40cf4925)  
[Sicherheit und Schutz (Datenbankmodul)](assetId:///dfb39d16-722a-4734-94bb-98e61e014ee7)  
  
