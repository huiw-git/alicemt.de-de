---
title: "Implementieren von Auftr&#228;gen"
ms.custom: na
ms.date: 07/27/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - tools-ssms
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 69e06724-25c7-4fb3-8a5b-3d4596f21756
caps.latest.revision: 4
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
# Implementieren von Auftr&#228;gen
Sie können [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)]-Agent-Aufträge verwenden, um regelmäßig anfallende administrative Tasks zu automatisieren und periodisch ausführen, sodass die Effizienz der Verwaltung verbessert wird.  
  
Ein Auftrag besteht aus einer festgelegten Folge von Operationen, die der [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)]-Agent der Reihenfolge nach ausführt. Durchführung einer Aufgabe kann eine Vielzahl von Aktivitäten, einschließlich der Ausführung [!INCLUDE[tsql](../content/includes/tsql_md.md)] Skripts, Befehl\-Zeile Applikationen, Microsoft ActiveX-Skripts, Integration Services-Paketen, Analysis Services-Befehlen und Abfragen oder Replikationstasks. Aufträge können wiederkehrende oder planbare Tasks ausführen, und sie können Benutzer durch Generieren von Warnungen automatisch über den Auftragsstatus informieren, sodass die [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)]-Verwaltung erheblich vereinfacht wird.  
  
Sie können einen Auftrag manuell ausführen oder ihn so konfigurieren, dass er gemäß einem Zeitplan oder als Reaktion auf Warnungen ausgeführt wird.  
  
## Verwandte Aufgaben  
  
|||  
|-|-|  
|**Beschreibung**|**Thema**|  
|Enthält Informationen zum Erstellen von Aufträgen und Zuweisen des Besitz.|[Erstellen von Aufträgen](../content/Create-Jobs.md)|  
|Enthält Informationen zum Organisieren von Aufträgen in Kategorien.|[Organisieren von Aufträgen](../content/Organize-Jobs.md)|  
|Enthält Informationen zu den verschiedenen Auftragsschritten, die Sie erstellen können, und beschreibt, wie Sie diese Auftragsschritte verwalten.|[Verwalten von Auftragsschritten](../content/Manage-Job-Steps.md)|  
|Enthält Informationen zur Definition des Auftragsbeginns sowie der Häufigkeit der Ausführung.|[Anlegen und Zuweisen von Zeitplänen zu Aufträgen](../content/Create-and-Attach-Schedules-to-Jobs.md)|  
|Enthält Informationen zur manuellen Ausführung von Aufträgen (ohne Zeitplan).|[Ausführen von Aufträgen](../content/Run-Jobs.md)|  
|Enthält Informationen zur Konfiguration des [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)]-Agents für die Reaktion auf Aufträge. Sie können den [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)]-Agent z. B. so konfigurieren, dass Administratoren bei der Beendigung von Aufträgen benachrichtigt werden.|[Angeben von Auftragsantworten](../content/Specify-Job-Responses.md)|  
|Enthält Informationen zum Anzeigen vorhandener Aufträge, zum Auftragsverlauf nach der Ausführung und zum Ändern von Aufträgen.|[Anzeigen oder Ändern von Aufträgen](../content/View-or-Modify-Jobs.md)|  
|Enthält Informationen zum Löschen von Aufträgen.|[Löschen von Aufträgen](../content/Delete-Jobs.md)|  
  
## Siehe auch  
[Implementieren der SQL Server-Agent-Sicherheit](../content/Implement-SQL-Server-Agent-Security.md)  
  
