---
title: "Feste Datenbankrollen des SQL Server-Agents"
ms.custom: na
ms.date: 07/27/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - tools-ssms
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 719ce56b-d6b2-414a-88a8-f43b725ebc79
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
# Feste Datenbankrollen des SQL Server-Agents
[!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] bietet die folgenden **Msdb** festen Datenbankrollen, die Administratoren eine genauere Kontrolle über Zugriff auf geben [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] Agent. In der folgenden Auflistung sind die Rollen von den niedrigsten bis hin zu den höchsten Zugriffsberechtigungen enthalten:  
  
-   **SQLAgentUserRole**  
  
-   **SQLAgentReaderRole**  
  
-   **SQLAgentOperatorRole**  
  
Wenn der Benutzer nicht Mitglied einer dieser Rollen sind mit verbunden sind [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] in [!INCLUDE[ssManStudioFull](../content/includes/ssManStudioFull_md.md)],  **SQL Server-Agent** Knoten im Objekt-Explorer ist nicht sichtbar. Ein Benutzer muss Mitglied einer dieser festen Datenbankrollen oder ein Mitglied der **Sysadmin** festen Serverrolle verwenden [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] Agent.  
  
## Berechtigungen der festen Datenbankrollen des SQL Server-Agents  
Die [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] -Agent-Datenbankrollen-Berechtigungen werden in Relation zueinander konzentrischen \-\- Rollen erben die Berechtigungen der Rollen mit niedrigeren Berechtigungen auf [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] -Agent-Objekte (einschließlich Warnungen, Operatoren, Aufträge, Zeitpläne und Proxys). Z. B. wenn Mitglieder am wenigsten\-privilegierten **SQLAgentUserRole** wurde der Zugriff gewährt, Proxy\_ein, die Member beider **SQLAgentReaderRole** und **SQLAgentOperatorRole** automatisch Zugriff auf diesen Proxy, obwohl Zugriff auf Proxy\_ein wurde nicht explizit erteilt an Sie. Dies kann zu Sicherheitsrisiken führen, die in den folgenden Abschnitten zu den einzelnen Rollen erläutert werden.  
  
### SQLAgentUserRole-Berechtigungen  
**SQLAgentUserRole** den geringsten ist die [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] Agent festen Datenbankrollen. Sie hat lediglich Berechtigungen für Operatoren, lokale Aufträge und Auftragszeitpläne. Mitglieder der **SQLAgentUserRole** lediglich Berechtigungen für lokale Aufträge und Auftragszeitpläne, deren Besitzer sie, sind. Sie können keine Multiserveraufträge (Master- und Zielserveraufträge) verwenden, und sie können den Auftragsbesitz nicht ändern, um Zugriff auf Aufträge zu erhalten, deren Besitzer sie nicht bereits sind. **SQLAgentUserRole** Mitglieder können eine Liste mit vorhandenen Proxys anzeigen nur in der **Auftragsschritt-Eigenschaften** Dialogfeld [!INCLUDE[ssManStudioFull](../content/includes/ssManStudioFull_md.md)]. Nur die **Aufträge** Knoten [!INCLUDE[ssManStudioFull](../content/includes/ssManStudioFull_md.md)] Objekt-Explorer wird für Mitglieder angezeigt **SQLAgentUserRole**.  
  
> [!IMPORTANT]  
> Beachten Sie die Sicherheitsrisiken vor dem Gewähren von Zugriff auf Mitglieder der **der**[!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)]**Agentdatabaseroles**. Die **SQLAgentReaderRole** und **SQLAgentOperatorRole** sind automatisch Mitglieder der **' SQLAgentUserRole '**. Dies bedeutet, dass Mitglieder **SQLAgentReaderRole** und **SQLAgentOperatorRole** haben Zugriff auf alle [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] -Agent-Proxys, die gewährt wurden die **SQLAgentUserRole** und diese Proxys verwenden können.  
  
Die folgende Tabelle enthält **SQLAgentUserRole** Berechtigungen für [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] -Agent-Objekte.  
  
|Aktion|Operatoren|Lokale Aufträge<br /><br />(nur Aufträge mit Besitzern)|Auftragszeitpläne<br /><br />(nur Zeitpläne mit Besitzern)|Proxys|  
|----------|-------------|-----------------------------------|-------------------------------------------|-----------|  
|Erstellen Sie\/Ändern\/Löschen|Nein|ja<br /><br />Auftragsbesitz kann nicht geändert werden.|ja|Nein|  
|Liste anzeigen (aufzählen)|ja<br /><br />Können Sie die Liste der verfügbaren Operatoren für die Verwendung in abrufen **sp\_Benachrichtigen\_Operator** und die **Auftragseigenschaften** Dialogfeld von Management Studio.|ja|ja|ja<br /><br />Liste der Proxys nur verfügbar in der **Auftragsschritt-Eigenschaften** Dialogfeld von Management Studio.|  
|Aktivieren Sie\/deaktivieren|Nein|ja|ja|Nicht verfügbar|  
|Eigenschaften anzeigen|Nein|ja|ja|Nein|  
|Führen Sie\/Beenden\/Starten|Nicht verfügbar|ja|Nicht verfügbar|Nicht verfügbar|  
|Auftragsverlauf anzeigen|Nicht verfügbar|ja|Nicht verfügbar|Nicht verfügbar|  
|Auftragsverlauf löschen|Nicht verfügbar|Nein<br /><br />Mitglieder der **SQLAgentUserRole** explizit die EXECUTE-Berechtigung erteilt werden auf **sp\_Löschen\_Jobhistory** zum Löschen des Auftragsverlaufs für Aufträge, die sie besitzen. Sie können den Auftragsverlauf für keine anderen Aufträge löschen.|Nicht verfügbar|Nicht verfügbar|  
|Fügen Sie\/Trennen|Nicht verfügbar|Nicht verfügbar|ja|Nicht verfügbar|  
  
### SQLAgentReaderRole-Berechtigungen  
**SQLAgentReaderRole** umfasst alle der **SQLAgentUserRole** Berechtigungen sowie Berechtigungen zum Anzeigen der Liste verfügbarer Multiserveraufträge, ihre Eigenschaften und ihres Verlaufs. Die Mitglieder dieser Rolle können auch die Liste aller verfügbaren Aufträge und Auftragszeitpläne sowie ihre Eigenschaften anzeigen, nicht nur die Aufträge und Auftragszeitpläne, deren Besitzer sie sind. **SQLAgentReaderRole** Elemente Auftragsbesitz Zugriff auf Aufträge, die sie nicht besitzen, nicht ändern kann. Nur die **Aufträge** Knoten [!INCLUDE[ssManStudioFull](../content/includes/ssManStudioFull_md.md)] Objekt-Explorer wird angezeigt, auf Mitglieder der **SQLAgentReaderRole**.  
  
> [!IMPORTANT]  
> Beachten Sie die Sicherheitsrisiken vor dem Gewähren von Zugriff auf Mitglieder der **der**[!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)]**Agentdatabaseroles**. Mitglieder der **SQLAgentReaderRole** sind automatisch Mitglieder der **' SQLAgentUserRole '**. Dies bedeutet, dass Mitglieder **SQLAgentReaderRole** haben Zugriff auf alle [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] -Agent-Proxys, die gewährt wurden **SQLAgentUserRole** und diese Proxys verwenden können.  
  
Die folgende Tabelle enthält **SQLAgentReaderRole** Berechtigungen für [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] -Agent-Objekte.  
  
|Aktion|Operatoren|Lokale Aufträge|Multiserveraufträge|Auftragszeitpläne|Proxys|  
|----------|-------------|--------------|--------------------|-----------------|-----------|  
|Erstellen Sie\/Ändern\/Löschen|Nein|Ja (nur Aufträge mit Besitzer)<br /><br />Auftragsbesitz kann nicht geändert werden.|Nein|Ja (nur Zeitpläne mit Besitzer)|Nein|  
|Liste anzeigen (aufzählen)|ja<br /><br />Können Sie die Liste der verfügbaren Operatoren für die Verwendung in abrufen **sp\_Benachrichtigen\_Operator** und die **Auftragseigenschaften** Dialogfeld von Management Studio.|ja|ja|ja|ja<br /><br />Liste der Proxys nur verfügbar in der **Auftragsschritt-Eigenschaften** Dialogfeld von Management Studio.|  
|Aktivieren Sie\/deaktivieren|Nein|Ja (nur Aufträge mit Besitzer)|Nein|Ja (nur Zeitpläne mit Besitzer)|Nicht verfügbar|  
|Eigenschaften anzeigen|Nein|ja|ja|ja|Nein|  
|Eigenschaften bearbeiten|Nein|Ja (nur Aufträge mit Besitzer)|Nein|Ja (nur Zeitpläne mit Besitzer)|Nein|  
|Führen Sie\/Beenden\/Starten|Nicht verfügbar|Ja (nur Aufträge mit Besitzer)|Nein|Nicht verfügbar|Nicht verfügbar|  
|Auftragsverlauf anzeigen|Nicht verfügbar|ja|ja|Nicht verfügbar|Nicht verfügbar|  
|Auftragsverlauf löschen|Nicht verfügbar|Nein<br /><br />Mitglieder der **SQLAgentReaderRole** explizit die EXECUTE-Berechtigung erteilt werden auf **sp\_Löschen\_Jobhistory** zum Löschen des Auftragsverlaufs für Aufträge, die sie besitzen. Sie können den Auftragsverlauf für keine anderen Aufträge löschen.|Nein|Nicht verfügbar|Nicht verfügbar|  
|Fügen Sie\/Trennen|Nicht verfügbar|Nicht verfügbar|Nicht verfügbar|Ja (nur Zeitpläne mit Besitzer)|Nicht verfügbar|  
  
### SQLAgentOperatorRole-Berechtigungen  
**SQLAgentOperatorRole** wird von den höchsten Berechtigungen der [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] Agent festen Datenbankrollen. Sie enthält alle Berechtigungen von **SQLAgentUserRole** und **SQLAgentReaderRole**. Die Mitglieder dieser Rolle können auch die Eigenschaften für Operatoren und Proxys anzeigen und die verfügbaren Proxys und Warnungen auf dem Server aufzählen.  
  
**SQLAgentOperatorRole** Elemente verfügen über zusätzliche Berechtigungen für lokale Aufträge und Zeitpläne. Sie können alle lokalen Aufträge ausführen, beenden oder starten, und sie können den Auftragsverlauf eines lokalen Auftrags auf dem Server löschen. Sie können auch alle lokalen Aufträge und Zeitpläne auf dem Server aktivieren und deaktivieren. Zum Aktivieren oder deaktivieren Sie lokale Aufträge oder Zeitpläne, müssen Mitglieder dieser Rolle die gespeicherten Prozeduren verwenden **sp\_Aktualisieren\_Auftrag** und **sp\_Aktualisieren\_Zeitplan**. Nur die Parameter, die der Auftrag oder ein Zeitplanname angegeben oder Bezeichner angeben und die **@ aktiviert** Parameter angegeben werden kann, von Mitgliedern der **SQLAgentOperatorRole**. Wenn sie andere Parameter angeben, erzeugt die Ausführung dieser gespeicherten Prozeduren einen Fehler. **SQLAgentOperatorRole** Mitglieder Auftragsbesitz Zugriff auf Aufträge, die sie nicht besitzen, nicht ändern kann.  
  
Die **Aufträge**, **Warnungen**, **Operatoren**, und **Proxys** Knoten im [!INCLUDE[ssManStudioFull](../content/includes/ssManStudioFull_md.md)] Objekt-Explorer stehen für Mitglieder **SQLAgentOperatorRole**. Nur die **Fehlerprotokolle** Knoten ist nicht für Mitglieder dieser Rolle sichtbar.  
  
> [!IMPORTANT]  
> Beachten Sie die Sicherheitsrisiken vor dem Gewähren von Zugriff auf Mitglieder der **der**[!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)]**Agentdatabaseroles**. Mitglieder der **SQLAgentOperatorRole** sind automatisch Mitglieder **SQLAgentUserRole** und **SQLAgentReaderRole**. Dies bedeutet, dass Mitglieder **SQLAgentOperatorRole** haben Zugriff auf alle [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] -Agent-Proxys, die entweder gewährt wurden **SQLAgentUserRole** oder **SQLAgentReaderRole** und diese Proxys verwenden können.  
  
Die folgende Tabelle enthält **SQLAgentOperatorRole** Berechtigungen für [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] -Agent-Objekte.  
  
|Aktion|Warnungen|Operatoren|Lokale Aufträge|Multiserveraufträge|Auftragszeitpläne|Proxys|  
|----------|----------|-------------|--------------|--------------------|-----------------|-----------|  
|Erstellen Sie\/Ändern\/Löschen|Nein|Nein|Ja (nur Aufträge mit Besitzer)<br /><br />Auftragsbesitz kann nicht geändert werden.|Nein|Ja (nur Zeitpläne mit Besitzer)|Nein|  
|Liste anzeigen (aufzählen)|ja|ja<br /><br />Können Sie die Liste der verfügbaren Operatoren für die Verwendung in abrufen **sp\_Benachrichtigen\_Operator** und die **Auftragseigenschaften** Dialogfeld von Management Studio.|ja|ja|ja|ja|  
|Aktivieren Sie\/deaktivieren|Nein|Nein|ja<br /><br />**SQLAgentOperatorRole** Elemente aktivieren oder deaktivieren Sie die lokale Aufträge, die sie keine besitzen mithilfe der gespeicherten Prozedur **sp\_Aktualisieren\_Auftrag** und Angeben von Werten für die **@ aktiviert** und **@job\_Id** (oder **@job\_Namen**) Parameter. Wenn ein Mitglied dieser Rolle einen anderen Parameter für diese gespeicherte Prozedur angibt, erzeugt die Ausführung der Prozedur einen Fehler.|Nein|ja<br /><br />**SQLAgentOperatorRole** Mitglieder können Zeitpläne aktivieren oder deaktivieren sie keine besitzen mithilfe der gespeicherten Prozedur **sp\_Aktualisieren\_Zeitplan** und Angeben von Werten für die **@ aktiviert** und **@schedule\_Id** (oder **@name**) Parameter. Wenn ein Mitglied dieser Rolle einen anderen Parameter für diese gespeicherte Prozedur angibt, erzeugt die Ausführung der Prozedur einen Fehler.|Nicht verfügbar|  
|Eigenschaften anzeigen|ja|ja|ja|ja|ja|ja|  
|Eigenschaften bearbeiten|Nein|Nein|Ja (nur Aufträge mit Besitzer)|Nein|Ja (nur Zeitpläne mit Besitzer)|Nein|  
|Führen Sie\/Beenden\/Starten|Nicht verfügbar|Nicht verfügbar|ja|Nein|Nicht verfügbar|Nicht verfügbar|  
|Auftragsverlauf anzeigen|Nicht verfügbar|Nicht verfügbar|ja|ja|Nicht verfügbar|Nicht verfügbar|  
|Auftragsverlauf löschen|Nicht verfügbar|Nicht verfügbar|ja|Nein|Nicht verfügbar|Nicht verfügbar|  
|Fügen Sie\/Trennen|Nicht verfügbar|Nicht verfügbar|Nicht verfügbar|Nicht verfügbar|Ja (nur Zeitpläne mit Besitzer)|Nicht verfügbar|  
  
## Zuweisen von mehreren Rollen an Benutzer  
Mitglieder der **Sysadmin** festen Serverrolle haben Zugriff auf alle [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] -Agent-Funktionalität. Ist ein Benutzer nicht Mitglied der **Sysadmin** Rolle, ist aber Mitglied von mehr als einem [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] Agent feste Datenbankrolle, es ist wichtig, das konzentrische Berechtigungsmodell dieser Rollen berücksichtigen. Da die Rollen mit höheren Berechtigungen immer alle Berechtigungen der Rollen mit niedrigeren Berechtigungen enthalten, hat ein Benutzer, der Mitglied von mehreren Rollen ist, automatisch die Berechtigungen der Rolle mit den höchsten Berechtigungen, deren Mitglied der Benutzer ist.  
  
## Siehe auch  
[Implementieren der SQL Server-Agent-Sicherheit](../content/Implement-SQL-Server-Agent-Security.md)  
[sp_update_job (Transact-SQL)](assetId:///cbdfea38-9e42-47f3-8fc8-5978b82e2623)  
[sp_update_schedule (Transact-SQL)](assetId:///97b3119b-e43e-447a-bbfb-0b5499e2fefe)  
[sp_notify_operator (Transact-SQL)](assetId:///c440f5c9-9884-4196-b07c-55d87afb17c3)  
[sp_purge_jobhistory (Transact-SQL)](assetId:///237f9bad-636d-4262-9bfb-66c034a43e88)  
  
