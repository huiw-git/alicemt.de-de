---
title: "Projekte (SQL Server Management Studio)"
ms.custom: na
ms.date: 07/15/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - tools-ssms
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: c13af859-ca66-4e43-b76a-0650ac6566c0
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
# Projekte (SQL Server Management Studio)
Ein [!INCLUDE[ssManStudio](../content/includes/ssManStudio_md.md)] -Projekt ist eine Sammlung logisch verbundener Skripts und Dateien, die zusammen zur Verwaltung und Entwicklung von Datenbanken gespeichert werden können.  
  
## Übersicht über das Skriptprojekt  
[!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] -Skriptprojekte werden in der Projektmappen-Explorer-Komponente von [!INCLUDE[ssManStudio](../content/includes/ssManStudio_md.md)]angezeigt. Ein Skriptprojekt kann null oder mehr Projektdateien enthalten. Sie können einer Projektmappe ein Projekt hinzufügen oder mehrere Projekte innerhalb einer Projektmappe kombinieren.  
  
Projekte können Folgendes umfassen:  
  
-   **Verbindungen**. Eine dauerhafte Verbindung in einem Projekt enthält Anmeldeinformationen, den Servernamen, die Standarddatenbank, das bevorzugte Protokoll, den Authentifizierungstyp und Verbindungseigenschaften. Verbindungsinformationen lassen sich optional auch zusammen mit einem Skript speichern (siehe unten).  
  
-   **SQLScripts**. Häufig verwendete SQL-Skripts für den Benutzer. Doppelte\-auf eine SQL-Datei innerhalb des Projekts führt dazu, dass der SQL-Editor, um das ausgewählte Skript zu öffnen.  
  
-   **MDX, DMX und XMLAScripts**. Häufig verwendete MDX-Skripts für den Benutzer. Doppelte\-auf einer MDX-Datei innerhalb des Projekts führt dazu, dass den Editor, um das ausgewählte Skript zu öffnen.  
  
-   **Verschiedenes**. Dieser Ordner kann für Dateien verwendet werden, die sich nicht problemlos einem der anderen standardmäßigen Knotentypen zuordnen lassen. Dazu zählen z. B. Textdateien mit Projektzielen.  
  
Projekte können auch in ein Quellcodeverwaltungs-System integriert werden.  
  
## Herstellen einer Verbindung mit einer SQL Server-Instanz aus einem Skriptprojekt  
Ein Skriptprojekt kann Verbindungen zu einer Instanz von [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)]enthalten. Sie können eine Verbindung mit einer Instanz von [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] in einem Projekt durch Klicken auf die Verbindung herstellen. Daraufhin wird ein SQL-Skriptfenster geöffnet, das mit der Instanz von [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] verbunden ist, die in der ausgewählten Verbindung definiert ist. Beim Öffnen eines [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] - oder MDX-Skripts mit einer Verbindung, von der [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] -Authentifizierung verwendet wird, werden Sie zum Angeben des Kennworts aufgefordert. Dabei wird nach dem Öffnen des Editors und Laden des Skripts das Dialogfeld **Verbindung mit SQL Server herstellen** angezeigt.  
  
Die Verbindung wird geschlossen, sobald das entsprechende Fenster geschlossen wird.  
  
Mit dem Eigenschaftenfenster in [!INCLUDE[ssManStudio](../content/includes/ssManStudio_md.md)]können Sie Informationen zu einer Verbindung ändern.  
  
## Projekttasks  
  
|Taskbeschreibung|Thema|  
|--------------------|---------|  
|Beschreibt, wie ein neues Projekt in einer Projektmappe erstellt wird.|[Erstellen eines Projekts](../content/Create-a-Project.md)|  
|Beschreibt, wie einer Projektmappe ein vorhandenes Projekt hinzugefügt wird.|[Hinzufügen eines vorhandenen Projekts zu einer Projektmappe](../content/Add-an-Existing-Project-to-a-Solution.md)|  
|Beschreibt, wie der Standardspeicherort zum Speichern von Projektdateien geändert wird.|[Ändern des Standardspeicherorts für Projekte](../content/Change-the-Default-Location-for-Projects.md)|  
|Beschreibt, wie die aktuellen Eigenschaften eines Projekts angezeigt werden.|[Anzeigen der Projekteigenschaften](../content/View-Project-Properties.md)|  
|Beschreibt, wie einem Projekt neue Elemente hinzugefügt werden, z. B. Verbindungen oder Skriptdateien.|[Hinzufügen neuer Elemente zu einem Projekt](../content/Add-New-Items-to-a-Project.md)|  
|Beschreibt, wie die Verbindungsinformationen für eine Abfrage festgelegt werden.|[Verknüpfen einer Abfrage mit einer Verbindung in einem Projekt](../content/Associate-a-Query-with-a-Connection-in-a-Project.md)|  
|Beschreibt, wie die Verbindungsinformationen für eine Abfrage geändert werden.|[Ändern der mit einer Abfrage verknüpften Verbindung](../content/Change-the-Connection-Associated-with-a-Query.md)|  
|Beschreibt, wie Verbindungseigenschaften geändert werden.|[Anzeigen oder Ändern der Eigenschaften einer Verbindung in einem Projekt](../content/View-or-Change-the-Properties-of-a-Connection-in-a-Project.md)|  
  
## Siehe auch  
[Projektmappen-Explorer](../content/Solution-Explorer.md)  
[Solutions & #40; SQL Server Management Studio & #41;](../content/Solutions--SQL-Server-Management-Studio-.md)  
[Quellcodeverwaltung des Projektmappen-Explorers](https://msdn.microsoft.com/en-us/library/ms173879.aspx)  
  
