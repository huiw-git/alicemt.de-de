---
title: "Externe Tools"
ms.custom: na
ms.date: 07/15/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - tools-ssms
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: d7dae88f-0781-4162-96cd-d3a3a4d82035
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
# Externe Tools
Verwenden Sie dieses Dialogfeld Externe Tools, z. B. SQL Server-Konfigurations-Manager oder den Editor zum Hinzufügen von der **Tools** Menü. Durch das Hinzufügen externer Tools erleichtern Sie das Starten anderer Anwendungen während der Arbeit mit [!INCLUDE[ssManStudioFull](../content/includes/ssManStudioFull_md.md)]. Sie können beim Starten des Tools Argumente und ein Arbeitsverzeichnis angeben. Zusätzlich können die Ausgaben einiger Tools im Ausgabefenster angezeigt werden. Die **Externe Tools** Dialogfeld steht auf der **Tools** Menü.  
  
## Optionen  
**Menüinhalt**  
Listet die Titel der gerade hinzugefügten Elemente der **Tools** Menü. Verwenden der **nach oben** und **nach unten** Pfeile, um die Reihenfolge der Elemente ändern, die im Menü angezeigt werden. Verwenden der **Löschen** Schaltfläche, um ein Element aus dem Menü zu entfernen.  
  
**Nach oben**  
Verschieben Sie das ausgewählte Tool höher in der Liste der Tools im der **Tools** Menü.  
  
**Nach unten**  
Verschieben Sie das ausgewählte Tool unten in der Liste der Tools im der **Tools** Menü.  
  
**Hinzufügen**  
Löscht die Textfelder, sodass Sie ein neues Tool angeben können.  
  
**Delete**  
Entfernen Sie das Tool oder den Befehl aus der **Menüinhalt** Liste auch auf die **Tools** Menü.  
  
**Titel**  
Der Name des Tools oder Befehls, der angezeigt wird die **Externe Tools** Untermenü der **Tools** Menü. Setzen Sie ein kaufmännisches Und-Zeichen vor einen Buchstaben im Namen des Tools, um diesen Buchstaben als Zugriffstaste für das Tool zu verwenden. Z. B. `&Spy++` würde anzeigen **Spy++\+\+** auf der **Tools** Menü.  
  
**Befehl**  
Gibt den Pfad zu der Datei mit der Endung EXE, COM, PIF, BAT, CMD oder einer anderen Datei an, die gestartet werden soll. Die Ausgabe von `.bat`, `.com`, und anderen Dateien können im Ausgabefenster angezeigt werden, wenn Sie auswählen, die **Ausgabefenster verwenden** das Kontrollkästchen.  
  
**Argumente**  
Gibt die Variablen an, die an das Tool übergeben werden, wenn es im Menü aufgerufen wird. Argumente können Werte festlegen, die beim Starten an das Tool oder den Befehl übergeben werden. Ein Wert kann beispielsweise einen Dateinamen oder ein Verzeichnis angeben. Verwenden der **Pfeil** Schaltfläche auswählen aus einer Liste vordefinierter Argumente. Sie können mehrere Argumente hinzufügen. Eine vollständige Liste vordefinierter Argumente und ihrer Definitionen finden Sie unter [Arguments for External Tools](../content/Arguments-for-External-Tools.md). Sie können auch benutzerdefinierte Argumente eingeben (Befehl\-Switches, z. B. auffordern), je nach den Befehl oder ein Tool, das Sie verwenden.  
  
**Ausgangsverzeichnis**  
Gibt das Arbeitsverzeichnis für das Tool an. Verwenden der **Pfeil** klicken, um Verzeichnisse auszuwählen. Sie können mehrere Verzeichnisse auswählen.  
  
**Ausgabefenster verwenden**  
Gibt an, ob die Ergebnisse des Tools im Ausgabefenster angezeigt werden sollen oder nicht. Diese Option ist nur für Dateien verfügbar, die normalerweise eine Ausgabe im Befehlszeilenfenster anzeigen (z. B. BAT- und COM-Dateien). Ist sie aktiviert, vereinfacht diese Option die Fensterverwaltung beim Verfolgen der Fortschritte eines Tools.  
  
**Zur Argumenteingabe auffordern**  
Anzeigen der **Argumente** Dialogfeld, mit denen Sie Werte eingeben oder bearbeiten für die Argumente jedes Mal, wenn Sie das externe Tool starten.  
  
**Ausgabe als Unicode behandeln**  
Ermöglicht dem Ausgabefenster die Annahme von Unicode.  
  
**Nach Beenden schließen**  
Schließt das vom Fenster geöffnete Tool, wenn das Tool geschlossen wird.  
  
## Beispiel  
  
#### SQL Server-Konfigurations-Manager im Menü Extras hinzufügen  
  
1.  Auf der **Tools** Menü klicken Sie auf **Externe Tools**.  
  
2.  In der **Titel** Geben **SQL Server-Konfigurations-Manager**.  
  
3.  In der **Befehl** Geben Sie den Pfad zu der [!INCLUDE[msCoName](../content/includes/msCoName_md.md)] -Verwaltungskonsole, die ausführbare Datei, z. B. **C:\\WINNT\\system32\\mmc.exe**  
  
4.  In der **Argumente** Geben Sie den Pfad zur MSC-Datei, z. B. **"C:\\WINNT\\system32\\SQLServerManager.msc"**  
  
> [!NOTE]  
> Anzeigen der Eigenschaften der [!INCLUDE[ssManStudioFull](../content/includes/ssManStudioFull_md.md)] -Verknüpfung auf der **Starten** Menü, um den Speicherort der Dateien auf Ihrem Computer zu überprüfen.  
  
