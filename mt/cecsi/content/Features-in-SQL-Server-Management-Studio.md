---
title: "Funktionen in SQL Server Management Studio"
ms.custom: na
ms.date: 07/27/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - tools-ssms
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: e75504b9-7968-4e3b-8411-fd79fe09021e
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
# Funktionen in SQL Server Management Studio
[!INCLUDE[ssManStudioFull](../content/includes/ssManStudioFull_md.md)] enthält die folgenden allgemeinen Funktionen:  
  
-   Unterstützt die meisten Verwaltungsaufgaben für [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)].  
  
-   Eine integrierte Umgebung für [!INCLUDE[ssDEnoversion](../content/includes/ssDEnoversion_md.md)] Verwaltung und Erstellung.  
  
-   Dialogfelder für das Verwalten von Objekten in der [!INCLUDE[ssDEnoversion](../content/includes/ssDEnoversion_md.md)], [!INCLUDE[ssASnoversion](../content/includes/ssASnoversion_md.md)], und [!INCLUDE[ssRSnoversion](../content/includes/ssRSnoversion_md.md)], können Sie Aktionen unmittelbar ausführen, um einen Code-Editor senden, oder ein Skript zur späteren Ausführung.  
  
-   Nicht\-gebunden und in der Größe veränderbaren Dialogfelder ermöglichen den Zugriff auf mehrere Tools, während ein Dialogfeld geöffnet ist.  
  
-   Einem allgemeinen planungsdialogfeld können, die Ihnen ermöglicht, die Aktion den verwaltungsdialogfeldern zu einem späteren Zeitpunkt auszuführen.  
  
-   Exportieren und Importieren von [!INCLUDE[ssManStudioFull](../content/includes/ssManStudioFull_md.md)] -serverregistrierung aus einer [!INCLUDE[ssManStudio](../content/includes/ssManStudio_md.md)] Umgebung in eine andere.  
  
-   Speichern oder Drucken von XML-Showplan oder Deadlock-Dateien, die von SQL Server Profiler generiert, später überprüfen oder zur Analyse an Administratoren senden.  
  
-   Ein neues Fehler- und informationsmeldungsfeld, die bietet deutlich mehr Informationen können Sie senden [!INCLUDE[msCoName](../content/includes/msCoName_md.md)] einen Kommentar zu den Nachrichten können Sie Nachrichten in die Zwischenablage kopieren und ermöglicht es Ihnen, problemlos e\-e-Mail-Nachrichten an das Supportteam.  
  
-   Ein integrierter Webbrowser zum schnellen Durchsuchen von MSDN oder online-Hilfe.  
  
-   Integration von Hilfe aus Onlinecommunities.  
  
-   Ein Lernprogramm zum [!INCLUDE[ssManStudioFull](../content/includes/ssManStudioFull_md.md)] können Sie die vielen neuen Features nutzen und steigern der Produktivität sofort.  
  
-   Ein neuer Aktivitätsmonitor mit Filtern und automatischen Aktualisieren.  
  
-   Integrierte Database Mail-Schnittstellen.  
  
## Neue Skripterstellungsfunktionen  
Der Code-Editor-Komponente des [!INCLUDE[ssManStudioFull](../content/includes/ssManStudioFull_md.md)] enthält integrierte Skript-Editoren zum Erstellen [!INCLUDE[tsql](../content/includes/tsql_md.md)], MDX-, DMX- und XML-\/A. Merkmale und Funktionen:  
  
-   Dynamische Hilfe für den direkten Zugriff auf relevante Informationen, während Sie arbeiten.  
  
-   Eine Vielzahl von Vorlagen mit der Möglichkeit, benutzerdefinierte Vorlagen erstellen.  
  
-   Unterstützung für das Schreiben und Bearbeiten von Abfragen oder Skripts ohne Verbindung mit einem Server.  
  
-   Unterstützung für Skripting für SQLCMD-Abfragen und Skripts.  
  
-   Eine neue Schnittstelle für die Anzeige von XML-Ergebnissen.  
  
-   Integrierte quellcodeverwaltung für Projektmappen und Projekte, unterstützt das Speichern und verwalten Kopien von Skripts, sich im Laufe der Zeit ändern.  
  
-   [!INCLUDE[msCoName](../content/includes/msCoName_md.md)] IntelliSense-Unterstützung für MDX-Anweisungen.  
  
## Objekt-Explorer-Funktionen  
Die Objekt-Explorer-Komponente des [!INCLUDE[ssManStudioFull](../content/includes/ssManStudioFull_md.md)] ist ein integriertes Tool zum Anzeigen und Verwalten von Objekten in allen Servertypen. Merkmale und Funktionen:  
  
-   Filtern nach ganz oder teilweise ein Name, Schema oder Datum.  
  
-   Das asynchrone Auffüllen von Objekten mit der Möglichkeit zum Filtern von Objekten auf Grundlage der Metadaten.  
  
-   Der Zugriff auf [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] -Agent auf Replikationsservern zu Verwaltungszwecken.  
  
Weitere Informationen finden Sie unter [Objekt-Explorer](../content/Object-Explorer.md).  
  
## Erweiterbarkeit  
[!INCLUDE[ssManStudioFull](../content/includes/ssManStudioFull_md.md)] basiert auf der Visual Studio Isolated Shell, die grundsätzlich Erweiterbarkeit unterstützt (hinzufügen\-ins\/Schließen\-ins). Es ist möglich, die Visual Studio-Erweiterbarkeit zu benutzerdefinierten Funktionen in Dienste nutzen [!INCLUDE[ssManStudioFull](../content/includes/ssManStudioFull_md.md)]aber diese Erweiterbarkeit wird nicht unterstützt.  
  
Es gibt einige Benutzer und Drittanbieter, die Erweiterungen für entwickelt wurden [!INCLUDE[ssManStudioFull](../content/includes/ssManStudioFull_md.md)]. Während wir dies zu nicht verhindern, sollten Sie bedenken, dass eine derartige Erweiterbarkeit nicht unterstützt wird, daher ggf. Probleme mit rückwärts\/Kompatibilität weiterleiten. Microsoft veröffentlicht keine Dokumentation für die Erweiterung [!INCLUDE[ssManStudioFull](../content/includes/ssManStudioFull_md.md)]. Es gibt jedoch Community-Blogs und Beispiel-Code, die Sie möglicherweise nutzen.  
  
Microsoft unterstützt nicht [!INCLUDE[ssManStudioFull](../content/includes/ssManStudioFull_md.md)] Installationen mit [!INCLUDE[ssManStudioFull](../content/includes/ssManStudioFull_md.md)] Extensions vorhanden, wenn Sie installiert haben [!INCLUDE[ssManStudioFull](../content/includes/ssManStudioFull_md.md)] Extensions, möchten sie vor dem Aufruf von Microsoft-Kundensupport zu entfernen ein [!INCLUDE[ssManStudioFull](../content/includes/ssManStudioFull_md.md)] Problem.  
  
## Siehe auch  
[Verwenden Sie SQL Server Management Studio](../content/Use-SQL-Server-Management-Studio.md)  
  
