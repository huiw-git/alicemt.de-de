---
title: "&#220;berwachen der Auftragsaktivit&#228;t"
ms.custom: na
ms.date: 07/15/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - tools-ssms
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 71cb432b-631d-4b8b-9965-e731b3d8266d
caps.latest.revision: 6
caps.handback.revision: 5
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
# &#220;berwachen der Auftragsaktivit&#228;t
Sie können die aktuellen Aktivitäten aller definierten Aufträge auf einer Instanz von [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] überwachen, indem Sie den Auftragsaktivitätsmonitor des [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)]-Agents verwenden.  
  
## Sitzungen des SQL Server-Agents  
[!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] Agent erstellt eine neue Sitzung bei jedem des Diensts Start. Wenn eine neue Sitzung erstellt wird, die **Sysjobactivity** -Tabelle in der **Msdb** Datenbank wird mit allen vorhandenen definierten Aufträgen aufgefüllt. Beim Neustart des [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)]-Agents bleibt die letzte Auftragsaktivität in dieser Tabelle erhalten. Jede Sitzung zeichnet die normale Auftragsaktivität des [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)]-Agents vom Anfang bis zum Ende des Auftrags auf. Informationen zu diesen Sitzungen befindet sich in der **Syssessions** Tabelle mit den **Msdb** Datenbank.  
  
## Auftragsaktivitätsmonitor  
Im Auftragsaktivitätsmonitor können Sie zum Anzeigen der **Sysjobactivity** Tabelle mit [!INCLUDE[ssManStudioFull](../content/includes/ssManStudioFull_md.md)]. Sie können alle Aufträge auf dem Server anzeigen oder Filter definieren, um die Anzahl der angezeigten Aufträge zu beschränken. Sie können die Auftragsinformationen auch sortieren, durch Klicken auf eine Spaltenüberschrift in der **Agentauftragsaktivität** Raster. Wenn Sie z. B. Auswählen der **Letzte Ausführung** Spalte Überschrift, Sie können die Aufträge anzeigen in der Reihenfolge, die sie zuletzt ausgeführt wurden. Wenn Sie erneut auf die Spaltenüberschrift klicken, werden die Aufträge je nach ihrem letzten Ausführungsdatum so umgeschaltet, dass sie in auf- bzw. absteigender Reihenfolge angezeigt werden.  
  
Mit dem Auftragsaktivitätsmonitor können Sie folgende Aufgaben ausführen:  
  
-   Starten und Beenden von Aufträgen  
  
-   Anzeigen von Auftragseigenschaften  
  
-   Anzeigen des Verlaufsprotokolls für einen bestimmten Auftrag  
  
-   Aktualisieren Sie die Informationen in der **Agentauftragsaktivität** Raster manuell oder festlegen ein automatischen Aktualisierungsintervalls durch Klicken auf **aktualisierungseinstellungen anzeigen**.  
  
Verwenden Sie den Auftragsaktivitätsmonitor, um zu ermitteln, für welche Aufträge eine Ausführung geplant ist, oder um festzustellen, welche Aufträge derzeit ausgeführt werden bzw. im Leerlauf sind. Sie können mit dem Auftragsaktivitätsmonitor auch das Ergebnis von Aufträgen anzeigen, die während der aktuellen Sitzung ausgeführt wurden. Wenn der [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)]-Agent-Dienst unerwartet einen Fehler erzeugt, können Sie ermitteln, welche Aufträge zum Zeitpunkt des Fehlers ausgeführt wurden, indem Sie im Auftragsaktivitätsmonitor die vorherige Sitzung anzeigen.  
  
Um den Auftragsaktivitätsmonitor zu öffnen, erweitern Sie **SQL Server-Agent** in [!INCLUDE[ssManStudio](../content/includes/ssManStudio_md.md)] Objekt-Explorer rechts\-Klicken Sie auf **Auftragsaktivitätsmonitor**, und klicken Sie auf **Anzeigen der Auftragsaktivität**.  
  
Sie können auch Aktivitäten für die aktuelle Sitzung anzeigen, indem Sie mit der gespeicherten Prozedur **sp\_Hilfe\_Jobactivity**.  
  
## Verwandte Aufgaben  
  
|||  
|-|-|  
|**Beschreibung**|**Thema**|  
|Beschreibt, wie der Laufzeitstatus von [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)]-Agent-Aufträgen angezeigt wird.|[Anzeigen der Auftragsaktivität](../content/View-Job-Activity.md)|  
  
## Siehe auch  
[Anzeigen der Auftragsaktivität](../content/View-Job-Activity.md)  
[sysjobactivity (Transact-SQL)](assetId:///fd17cac9-5d1f-4b44-b2dc-ee9346d8bf1e)  
[syssessions (Transact-SQL)](assetId:///187819b6-c7f4-4a26-b74c-0a89e96695cf)  
[sp_help_jobactivity (Transact-SQL)](assetId:///d344864f-b4d3-46b1-8933-b81dec71f511)  
  
