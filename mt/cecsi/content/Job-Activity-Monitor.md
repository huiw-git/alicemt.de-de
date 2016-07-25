---
title: "Auftragsaktivit&#228;tsmonitor"
ms.custom: na
ms.date: 07/15/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - tools-ssms
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 11f2182c-5f71-46f8-8d2b-74f0fc48f2d6
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
# Auftragsaktivit&#228;tsmonitor
Mithilfe dieser Seite können Sie die aktuelle Aktivität von Aufträgen des [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] -Agents anzeigen. Klicken Sie auf **Filter** , um die Anzahl der angezeigten Aufträge zu beschränken. Die **Agentauftragsaktivität** Raster gelesen\-nur. Klicken Sie auf die Spaltenheader, um das Raster zu sortieren. Um einen Auftrag zu ändern, doppelklicken\-Klicken Sie auf den Auftrag zum Öffnen der **Auftragseigenschaften** Dialogfeld. Rechts\-Klicken Sie auf einen Auftrag im Raster, um alle Auftragsschritte ausführen starten, starten Sie über einen bestimmten Auftragsschritt, deaktivieren oder den Auftrag aktivieren, aktualisieren, den Auftrag, den Auftrag zu löschen, zeigen Sie den Verlauf des Auftrags oder zeigen Sie die Eigenschaften des Auftrags. Klicken Sie auf **Aktualisieren** , um das Raster mit den aktuellen Informationen zu aktualisieren.  
  
## Optionen  
**Name**  
Name des Auftrags.  
  
**Aktiviert**  
Gibt an, ob der Auftrag aktiviert ist (**Ja**) oder deaktiviert (**keine**).  
  
**Status**\*  
Aktueller Status des Auftrags  
  
**Ergebnis der letzten Ausführung**  
Auftragsstatus bei der letzten Ausführung  
  
**Zuletzt ausgeführt**  
Datum und Uhrzeit, an dem bzw. zu der der Auftrag zuletzt ausgeführt wurde (ausgehend vom lokalen Datum und der lokalen Uhrzeit des Servers).  
  
**Nächste Ausführung**\*  
Datum und Uhrzeit des Zeitpunkts, an dem die nächste Ausführung des Auftrags geplant ist (ausgehend vom lokalen Datum und der lokalen Uhrzeit des Servers).  
  
**Kategorie**  
Die dem Auftrag zugewiesene Auftragskategorie.  
  
**Ausführbar**  
**Ja,** wenn der Auftrag ausgeführt werden kann; **Keine** Wenn der Auftrag ausgeführt werden kann. Ein Auftrag kann nicht ausgeführt werden, wenn er keine Schritte oder keinen Zielserver aufweist.  
  
**Geplant**  
**Ja,** wenn der Auftrag einem Auftragszeitplan; zugewiesen ist **Keine** Wenn der Auftrag kein Zeitplan vorhanden ist.  
  
\*Nur Mitglieder der festen [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] -Serverrolle sysadmin und die Serveradministratorgruppe können Werte in dieser Spalte sehen. Mitglieder der SQLAgentOperatorRole-Rolle können keine Werte in dieser Spalte sehen.  
  
#### So öffnen Sie den Auftragsaktivitätsmonitor  
  
-   In **Objekt-Explorer**, erweitern Sie Ihren Server, erweitern Sie **SQL Server-Agent**, mit der rechten Maustaste\-Klicken Sie auf **Auftragsaktivitätsmonitor**, und klicken Sie dann auf **Anzeigen der Auftragsaktivität**.  
  
## Siehe auch  
[Überwachen der Auftragsaktivität](../content/Monitor-Job-Activity.md)  
  
