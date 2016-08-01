---
title: "Erstellen von Auftr&#228;gen"
ms.custom: na
ms.date: 07/27/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - tools-ssms
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 465fb7fc-7622-4252-a178-ea51691c935b
caps.latest.revision: 3
caps.handback.revision: 3
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
# Erstellen von Auftr&#228;gen
Ein Auftrag besteht aus einer festgelegten Folge von Operationen, die der [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)]-Agent der Reihenfolge nach ausführt. Über einen Auftrag können zahlreiche Aktivitäten ausgeführt werden, u. a. das Ausführen von [!INCLUDE[tsql](../content/includes/tsql_md.md)]-Skripts, Eingabeaufforderungsanwendungen, Microsoft ActiveX-Skripts, Integration Services-Paketen, Analysis Services-Befehlen und -abfragen bzw. Replikationstasks. Aufträge können wiederholte oder planbare Tasks ausführen, und sie können Benutzer in Form von Warnungen hinsichtlich des Auftragsstatus benachrichtigen. Dies führt zu einer deutlichen Vereinfachung der  [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)]-Verwaltung.  
  
Um einen Auftrag erstellen zu können, muss ein Benutzer Mitglied einer der festen Datenbankrollen des [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] -Agents oder Mitglied der festen Serverrolle **sysadmin** sein. Ein Auftrag kann nur von seinem Besitzer bzw. Mitgliedern der **sysadmin** -Rolle bearbeitet werden. Mitglieder der **Sysadmin** Rolle anderen Benutzern Auftragsbesitz zuweisen kann, und sie können jeden Auftrag, ungeachtet des Auftragsbesitzers ausgeführt. Weitere Informationen zu den [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] Agent festen Datenbankrollen finden Sie unter [SQL Server-Agent-festen Datenbankrollen](../content/SQL-Server-Agent-Fixed-Database-Roles.md).  
  
Aufträge können so geschrieben werden, dass sie auf der lokalen Instanz von [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] oder auf mehreren Instanzen in einem Unternehmen ausgeführt werden. Zum Ausführen von Aufträgen auf mehreren Servern müssen Sie mindestens einen Masterserver und einen oder mehrere Zielserver einrichten. Weitere Informationen zu Master-und Zielservern, finden Sie unter [automatisierte Verwaltung in einem Unternehmen](../content/Automated-Administration-Across-an-Enterprise.md)  
  
[!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] Datensätze Agentauftrag Informationen und Auftragsschritten im Auftragsverlauf.  
  
## Verwandte Aufgaben  
  
|||  
|-|-|  
|**Beschreibung**|**Thema**|  
|Beschreibt, wie ein [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)]-Agent-Auftrag erstellt wird.|[Erstellen eines Auftrags](../content/Create-a-Job.md)|  
|Beschreibt, wie Sie den Besitz eines [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)]-Agent-Auftrags einem anderen Benutzer neu zuweisen können.|[Ändern des Besitzes eines Auftrags](../content/Give-Others-Ownership-of-a-Job.md)|  
|Beschreibt, wie Sie das Auftragsverlaufsprotokoll des [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)]-Agents einrichten.|[Einrichten des Auftragsverlaufsprotokolls](../content/Set-Up-the-Job-History-Log.md)|  
  
## Siehe auch  
[Verwalten von Auftragsschritten](../content/Manage-Job-Steps.md)  
[Automatisierte Verwaltung in einem Unternehmen](../content/Automated-Administration-Across-an-Enterprise.md)  
[Anlegen und Zuweisen von Zeitplänen zu Aufträgen](../content/Create-and-Attach-Schedules-to-Jobs.md)  
[Ausführen von Aufträgen](../content/Run-Jobs.md)  
[Anzeigen oder Ändern von Aufträgen](../content/View-or-Modify-Jobs.md)  
  
