---
title: "Auftragsschritt-Eigenschaften - Neuer Auftragsschritt (Seite Allgemein)"
ms.custom: na
ms.date: 07/15/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - tools-ssms
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 8d1885ba-4386-4528-8f2b-68c16852720c
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
# Auftragsschritt-Eigenschaften - Neuer Auftragsschritt (Seite Allgemein)
Verwenden Sie diese Seite zum Anzeigen und Ändern der Eigenschaften einer [!INCLUDE[msCoName](../content/includes/msCoName_md.md)] [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] -Agentauftragsschritt, oder um einen neuen Auftragsschritt definieren.  
  
Navigieren Sie zu dieser Seite im [!INCLUDE[ssManStudioFull](../content/includes/ssManStudioFull_md.md)] Objekt-Explorer, erweitern Sie [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] Agent rechts\-Klicken Sie auf **Aufträge**, klicken Sie auf **neue Aufträge**, wählen die **Schritte** und klicken Sie auf **Neu**. Sie können auch auf dieser Seite navigieren, nach rechts\-auf einen Auftrag im Objekt-Explorer auf **Eigenschaften**, wählen die **Schritte** Seite klicken und **Neu**, **Einfügen**, oder **Bearbeiten**.  
  
## Optionen  
**Schrittname**  
Legt den Namen des Auftrags fest.  
  
**Typ**  
Legt das durch den Auftrag verwendete Subsystem fest. Basierend auf dem von Ihnen ausgewählten Subsystem ändern sich die für das Definieren des Auftragsschritts angezeigten Optionen.  
  
**Ausführen als**  
Legt das Proxykonto für den Auftragsschritt fest. Mitglieder der festen Serverrolle Sysadmin können auch angeben, die **SQL Agent-Dienstkonto**.  
  
**Datenbank**  
Legt die Datenbank fest, in der der Auftragsschritt ausgeführt wird. Diese Option ist nicht für alle Auftragsschritttypen verfügbar.  
  
**Befehl**  
Legt den durch den Auftrag ausgeführten Befehl fest.  
  
## Optionen für Transact\-SQL-Auftragsschritte  
**Öffnen**  
Lädt den Befehl aus einer Datei.  
  
**Alles auswählen**  
Markiert den Text des Befehls.  
  
**Kopieren**  
Kopiert den ausgewählten Text in die Zwischenablage.  
  
**Einfügen**  
Fügt die Inhalte aus der Zwischenablage ein.  
  
**Analysieren**  
Überprüft die Syntax des Befehls.  
  
## Optionen für Auftragsschritte von ActiveX-Skript  
  
> [!IMPORTANT]  
> Das ActiveX Scripting-Subsystem aufgehoben [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] -Agent in einer zukünftigen Version von [!INCLUDE[msCoName](../content/includes/msCoName_md.md)][!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)]. Verwenden Sie diese Funktion beim Entwickeln neuer Anwendungen nicht, und planen Sie das Ändern von Anwendungen, in denen es zurzeit verwendet wird.  
  
**VBScript**  
Gibt [!INCLUDE[msCoName](../content/includes/msCoName_md.md)] VBScript als Sprache für die Auftragsschritte an.  
  
**JScript**  
Gibt JScript als Sprache für die Auftragsschritte an.  
  
**Andere**  
Geben Sie den Namen der Sprache für Auftragsschritte ein, die in einer anderen Skriptsprache geschrieben wurden.  
  
**Öffnen**  
Lädt den Befehl aus einer Datei.  
  
**Alles auswählen**  
Markiert den Text des Befehls.  
  
**Kopieren**  
Kopiert den markierten Text.  
  
**Einfügen**  
Fügt die Inhalte aus der Zwischenablage ein.  
  
## Optionen für Auftragsschritte des Betriebssystems (CmdExec)  
**Prozessexitcode eines erfolgreichen Befehls**  
Geben Sie den Exitcode ein, den der Befehl zurückgibt, um einen Erfolg zu melden.  
  
**Öffnen**  
Lädt den Befehl aus einer Datei.  
  
**Alles auswählen**  
Markiert den Text des Befehls.  
  
**Kopieren**  
Kopiert den markierten Text.  
  
**Einfügen**  
Fügt die Inhalte aus der Zwischenablage ein.  
  
## Optionen für PowerShell-Auftragsschritte  
**Öffnen**  
Lädt das Skript aus einer Datei.  
  
**Alles auswählen**  
Markiert den Text des Skripts.  
  
**Kopieren**  
Kopiert den markierten Text.  
  
**Einfügen**  
Fügt die Inhalte aus der Zwischenablage ein.  
  
## Optionen für Replikationsverteiler-Auftragsschritte  
**Alles auswählen**  
Markiert den Text des Befehls.  
  
**Kopieren**  
Kopiert den markierten Text.  
  
**Einfügen**  
Fügt die Inhalte aus der Zwischenablage ein.  
  
## Optionen für Replikationsmerge-Auftragsschritte  
**Alles auswählen**  
Markiert den Text des Befehls.  
  
**Kopieren**  
Kopiert den markierten Text.  
  
**Einfügen**  
Fügt die Inhalte aus der Zwischenablage ein.  
  
## Optionen für Auftragsschritte des Replikation-Warteschlangenlesers  
**Datenbank**  
Die Datenbank, die für den Auftragsschritt verwendet werden soll.  
  
**Alles auswählen**  
Markiert den Text des Befehls.  
  
**Kopieren**  
Kopiert den markierten Text.  
  
**Einfügen**  
Fügt die Inhalte aus der Zwischenablage ein.  
  
## Optionen für Replikationsmomentaufnahme-Auftragsschritte  
**Alles auswählen**  
Markiert den Text des Befehls.  
  
**Kopieren**  
Kopiert den markierten Text.  
  
**Einfügen**  
Fügt die Inhalte aus der Zwischenablage ein.  
  
## Optionen für Replikationstransaktion\-Protokollieren Reader-Auftragsschritte  
**Alles auswählen**  
Markiert den Text des Befehls.  
  
**Kopieren**  
Kopiert den markierten Text.  
  
**Einfügen**  
Fügt die Inhalte aus der Zwischenablage ein.  
  
## Optionen für Auftragsschritte von SQL Server Analysis Services-Befehlen  
**Server**  
Wählt den Server aus, auf dem der Auftragsschritt ausgeführt wird.  
  
**Öffnen**  
Lädt den Befehl aus einer Datei.  
  
**Alles auswählen**  
Markiert den Text des Befehls.  
  
**Kopieren**  
Kopiert den markierten Text.  
  
**Einfügen**  
Fügt die Inhalte aus der Zwischenablage ein.  
  
## Optionen für Auftragsschritte von SQL Server Analysis Services-Abfragen  
**Server**  
Wählt den Server aus, auf dem der Auftragsschritt ausgeführt wird.  
  
**Datenbank**  
Die Datenbank, die für den Auftragsschritt verwendet werden soll.  
  
**Öffnen**  
Lädt den Befehl aus einer Datei.  
  
**Alles auswählen**  
Markiert den Text des Befehls.  
  
**Kopieren**  
Kopiert den markierten Text.  
  
**Einfügen**  
Fügt die Inhalte aus der Zwischenablage ein.  
  
## Optionen für Auftragsschritte von Integration Services-Paketausführungen  
  
### Registerkarte 'Allgemein'  
Gibt den Speicherort des [!INCLUDE[ssISnoversion](../content/includes/ssISnoversion_md.md)] ([!INCLUDE[ssIS](../content/includes/ssIS_md.md)])-Pakets an, und welche Authentifizierungsmethode verwendet werden soll. Wenn Sie diese Registerkarte auswählen, sind die folgenden Optionen verfügbar.  
  
**Paketquelle**  
Gibt den Speicherort des [!INCLUDE[ssIS](../content/includes/ssIS_md.md)]-Pakets an. Wählen Sie eine der folgenden Optionen aus:  
  
-   **SQL Server**  
  
-   **File system**  
  
-   **SSIS-Paketspeicher**  
  
**Server**  
Geben Sie den Namen des Servers ein, auf dem das [!INCLUDE[ssIS](../content/includes/ssIS_md.md)]-Paket gespeichert ist. Diese Option ist nur verfügbar, wenn **SQL Server** oder **SSIS-Paketspeicher** angegeben **Paketquelle**.  
  
**Windows-Authentifizierung verwenden**  
Für Anmeldungen bei [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] wird die [!INCLUDE[msCoName](../content/includes/msCoName_md.md)] Windows-Authentifizierung verwendet.  
  
**SQL Server-Authentifizierung verwenden**  
Für Anmeldungen an [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] wird die [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)]-Authentifizierung verwendet. Wenn diese Authentifizierungsmethode ausgewählt ist, geben Sie die entsprechenden **Benutzernamen** und **Kennwort**.  
  
> [!IMPORTANT]  
> [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] -Authentifizierung wird aus Gründen der Abwärtskompatibilität bereitgestellt. Aus Sicherheitsgründen sollte möglichst die Windows-Authentifizierung verwendet werden.  
  
**Paket**  
Geben Sie den Speicherort des Pakets ein.  
  
> [!IMPORTANT]  
> Kennwort\-geschützt [!INCLUDE[ssIS](../content/includes/ssIS_md.md)] Pakete, klicken Sie auf die **Konfigurationen** Registerkarte geben das Kennwort in die **Paketkennwort** Dialogfeld. Andernfalls der [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] -Agent-Auftrag, der das Kennwort ausführt\-geschützten Paket fehl.  
  
### Registerkarte Konfigurationen  
Gibt Konfigurationsoptionen für das [!INCLUDE[ssIS](../content/includes/ssIS_md.md)]-Paket an. Wenn Sie diese Registerkarte auswählen, sind die folgenden Optionen verfügbar.  
  
**Konfigurationsdateien**  
Führt die Konfigurationsdateien für das Paket in einer Liste auf.  
  
**Hinzufügen**  
Fügt eine Konfigurationsdatei für das Paket hinzu.  
  
**Entfernen**  
Entfernt eine Konfigurationsdatei für das Paket.  
  
**Nach oben**  
Verschiebt die ausgewählte Konfigurationsdatei nach oben.  
  
**Nach unten**  
Verschiebt die ausgewählte Konfigurationsdatei nach unten.  
  
### Registerkarte Befehlsdateien  
Wählt Befehlsdateien für das Paket aus. Befehlsdateien werden entsprechend ihrer Reihenfolge in der Liste verarbeitet. Wenn Sie diese Registerkarte auswählen, sind die folgenden Optionen verfügbar.  
  
**Befehlsdateien**  
Führt die Befehlsdateien für das Paket in einer Liste auf.  
  
**Hinzufügen**  
Fügt eine Befehlsdatei hinzu.  
  
**Entfernen**  
Entfernt die ausgewählte Befehlsdatei.  
  
**Nach oben**  
Verschiebt die ausgewählte Befehlsdatei nach oben.  
  
**Nach unten**  
Verschiebt die ausgewählte Befehlsdatei nach unten.  
  
### Registerkarte Datenquellen  
Zeigt die im Paket angegebenen Datenquellen auf dieser Registerkarte an.  
  
**Verbindungs-Manager**  
Zeigt den Namen der Datenquelle an.  
  
**Beschreibung**  
Zeigt die Beschreibung der Datenquelle an.  
  
**Verbindungszeichenfolge**  
Zeigt die Verbindungszeichenfolge für die Datenquelle an.  
  
### Registerkarte Ausführungsoptionen  
Zeigt die Ausführungsoptionen für das Paket auf dieser Registerkarte an oder ändert die Werte.  
  
**Paket bei Überprüfungswarnungen fehlschlagen lassen**  
Wählen Sie diese Option aus, wenn die Paketausführung bei Überprüfungswarnungen fehlschlagen soll.  
  
**Paket ohne Ausführung überprüfen**  
Wählen Sie diese Option für den Auftragsschritt aus, wenn das Paket überprüft, nicht jedoch ausgeführt werden soll.  
  
**Maximale Anzahl von gleichzeitig ausführbaren Dateien**  
Die maximale Anzahl der gleichzeitig ausführbaren Dateien.  
  
**Paketprüfpunkte aktivieren**  
Wählen Sie diese Option für den Auftragsschritt aus, wenn Paketprüfpunkte verwendet werden sollen.  
  
**Prüfpunktdatei**  
Geben Sie den Namen der Prüfpunktdatei des Pakets ein.  
  
**...**  
Sucht nach der Prüfpunktdatei des Pakets.  
  
**Neustartoptionen überschreiben**  
Wenn Sie diese Option auswählen, können Sie für diesen Auftragsschritt Neustartoptionen angeben, die von den im Paket angegebenen Optionen abweichen.  
  
**Neustartoption**  
Wählt die Aktion aus, die bei einem Neustart des Pakets durchgeführt werden soll.  
  
### Registerkarte Protokollierung  
Zeigt die Protokollanbieter für das Paket auf dieser Registerkarte an oder ändert diese.  
  
**Protokollanbieter**  
Wählt die ClassID für den Protokollanbieter aus.  
  
**Konfigurationszeichenfolge**  
Geben Sie die Konfigurationszeichenfolge für den Protokollanbieter ein.  
  
**Entfernen**  
Entfernt den Protokollanbieter.  
  
### Registerkarte Werte festlegen  
Zeigt die Eigenschaftswerte für das Paket auf dieser Registerkarte an oder ändert die Werte.  
  
**Eigenschaftspfad**  
Zeigt einen Pfad für die Eigenschaft an oder ändert diese.  
  
**Wert**  
Zeigt einen Wert für die Eigenschaft an oder ändert diesen.  
  
**Entfernen**  
Entfernt die Eigenschaft.  
  
### Registerkarte Überprüfung  
Wählt die Überprüfungsoptionen für den Auftragsschritt auf dieser Registerkarte aus.  
  
**Nur signierte Pakete ausführen**  
Führt nur Pakete aus, die signiert wurden. Bei Auswahl dieser Option schlägt der Auftragsschritt fehlt, wenn das Paket nicht signiert ist.  
  
**Paketbuild überprüfen**  
Führt nur Pakete aus, die eine bestimmte Buildnummer besitzen. Bei Auswahl dieser Option schlägt der Auftragsschritt fehl, wenn das Paket nicht die angegebene Buildnummer besitzt.  
  
**Erstellen**  
Geben Sie die Buildnummer des Pakets ein.  
  
**Paket-ID überprüfen**  
Führt nur Pakete aus, die eine bestimmte ID besitzen. Bei Auswahl dieser Option schlägt der Auftragsschritt fehl, wenn das Paket nicht die angegebene ID besitzt.  
  
**Paket-ID**  
Geben Sie die Paket-ID ein.  
  
**Versions-ID überprüfen**  
Führt nur Pakete mit einer bestimmten Versions-ID aus. Bei Auswahl dieser Option schlägt der Auftragsschritt fehl, wenn das Paket nicht die angegebene Versions-ID besitzt.  
  
**Versions-ID**  
Geben Sie die Versions-ID ein.  
  
### Registerkarte Befehlszeile  
Geben Sie Befehl\-Zeile Optionen für das Paket. Wenn Sie diese Registerkarte auswählen, sind die folgenden Optionen verfügbar.  
  
**Die ursprünglichen Optionen wiederherstellen**  
Verwenden Sie den Befehl\-Zeile in diesem Dialogfeld festgelegten Optionen.  
  
**Befehlszeile manuell bearbeiten**  
Geben Sie im Befehl Optionen\-Fenster.  
  
**Befehlszeile**  
Geben Sie die für dieses Paket zu verwendenden Befehlszeilenoptionen ein.  
  
## Siehe auch  
[Verwalten von Auftragsschritten](../content/Manage-Job-Steps.md)  
[Aufträge des SQL Server-Agents für Pakete](assetId:///ecf7a5f9-b8a7-47f1-9ac0-bac07cb89e31)  
[Verwalten der Replikations-Agents](assetId:///f27186b8-b1b2-4da0-8b2b-91f632c2ab7e)  
  
