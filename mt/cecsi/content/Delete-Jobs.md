---
title: "L&#246;schen von Auftr&#228;gen"
ms.custom: na
ms.date: 07/15/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - tools-ssms
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: bffb915e-bc84-4417-aa35-183243ca3312
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
# L&#246;schen von Auftr&#228;gen
Ein Auftrag besteht aus einer festgelegten Folge von Operationen, die der SQL Server-Agent der Reihenfolge nach ausführt. Standardmäßig werden Aufträge nicht gelöscht, wenn die Ausführung beendet wird. Sie können eine oder mehrere löschen [!INCLUDE[msCoName](../content/includes/msCoName_md.md)][!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] Agentaufträge unabhängig von Erfolg oder Misserfolg des Auftrags. Sie können auch konfigurieren [!INCLUDE[msCoName](../content/includes/msCoName_md.md)][!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] Agent Aufträge automatisch zu löschen, wenn sie erfolgreich ausgeführt werden, ein Fehler auf oder abschließen.  
  
Standardmäßig Mitglieder der **Sysadmin** feste Serverrolle die [Sp_delete_job (Transact-SQL)](assetId:///b85db6e4-623c-41f1-9643-07e5ea38db09) gespeicherte Systemprozedur, um einen Auftrag zu löschen. Andere Benutzer müssen Mitglieder der festen [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] -Agent-Datenbankrollen in der **msdb** -Datenbank sein:  
  
-   **SQLAgentUserRole**  
  
-   **SQLAgentReaderRole**  
  
-   **SQLAgentOperatorRole**  
  
Weitere Informationen zu den Berechtigungen dieser Rollen finden Sie unter [SQL Server-Agent festen Datenbankrollen](../content/SQL-Server-Agent-Fixed-Database-Roles.md).  
  
Mitglieder der **Sysadmin** feste Serverrolle **sp\_Löschen\_Auftrag** einen beliebigen Auftrag zu löschen. Ein Benutzer, der nicht Mitglied der **Sysadmin** -Serverrolle kann nur Aufträge im Besitz dieses Benutzers gelöscht.  
  
## Verwandte Aufgaben  
  
|||  
|-|-|  
|**Beschreibung**|**Thema**|  
|Beschreibt, wie Sie eine oder mehrere löschen [!INCLUDE[msCoName](../content/includes/msCoName_md.md)][!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] -Agent-Aufträge.|[Löschen eines oder mehrerer Aufträge](../content/Delete-One-or-More-Jobs.md)|  
|Beschreibt das Konfigurieren [!INCLUDE[msCoName](../content/includes/msCoName_md.md)][!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] Agent Aufträge automatisch zu löschen, wenn sie erfolgreich ausgeführt werden, ein Fehler auf oder abschließen.|[Automatisches Löschen eines Auftrags](../content/Automatically-Delete-a-Job.md)|  
  
