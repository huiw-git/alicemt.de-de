---
title: "Erstellen von Datenbankprojekten mit SQL Server Management Studio"
ms.custom: na
ms.date: 07/27/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - tools-ssms
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: c2e80045-894d-44cf-b65c-e547ed738947
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
# Erstellen von Datenbankprojekten mit SQL Server Management Studio
Bei einem Datenbankskriptprojekt handelt es sich um einen organisierten Satz von Skripts, Verbindungsinformationen und Vorlagen, die alle einer Datenbank oder einem Teil einer Datenbank zugeordnet sind. [!INCLUDE[msCoName](../content/includes/msCoName_md.md)] [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] Stellt die [!INCLUDE[ssManStudioFull](../content/includes/ssManStudioFull_md.md)] für verwalten und Entwerfen von [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] Datenbanken innerhalb des Kontexts eines skriptprojekts. [!INCLUDE[ssManStudioFull](../content/includes/ssManStudioFull_md.md)] umfasst Designer, Editoren, Handbücher und Assistenten, um Benutzer in die Entwicklung, Bereitstellung und Verwaltung von Datenbanken zu unterstützen.  
  
## SQL Server Management Studio  
[!INCLUDE[ssManStudioFull](../content/includes/ssManStudioFull_md.md)] ist eine Suite von Verwaltungstools zum Verwalten der Komponenten zur [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)]. Diese integrierte Umgebung ermöglicht es Benutzern, eine Reihe von Aufgaben, wie z. B. das Sichern von Daten, das Bearbeiten von Abfragen und das Automatisieren häufiger Funktionen, in einer einzigen Benutzeroberfläche auszuführen.  
  
[!INCLUDE[ssManStudioFull](../content/includes/ssManStudioFull_md.md)] enthält die folgenden Tools:  
  
-   Der Code-Editor ist ein Skript-Editor mit vielen Funktionen zum Erstellen und Bearbeiten von Skripts. [!INCLUDE[ssManStudioFull](../content/includes/ssManStudioFull_md.md)] bietet vier Versionen des Code-Editors. die [!INCLUDE[ssDE](../content/includes/ssDE_md.md)] Abfrage-Editor für [!INCLUDE[tsql](../content/includes/tsql_md.md)] Skripts, die DMX-Abfrage-Editor, MDX-Abfrage-Editor und die XML-\/ein Abfrage-Editor.  
  
-   Objekt-Explorer, um Objekte, die zu Instanzen von [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] gehören, zu suchen, zu ändern, auszuführen oder um ein Skript für diese Objekte zu erstellen.  
  
-   Vorlagen-Explorer, um Vorlagen zu suchen und ein Skript dafür zu erstellen  
  
-   Projektmappen-Explorer, um zusammengehörige Skripts als Teile eines Projekts anzuordnen und zu speichern  
  
-   Eigenschaftenfenster, um die aktuellen Eigenschaften von ausgewählten Objekten anzuzeigen  
  
[!INCLUDE[ssManStudioFull](../content/includes/ssManStudioFull_md.md)] unterstützt rationelle Arbeitsprozesse durch bereitstellen:  
  
-   Zugriff bei getrennter Verbindung. Sie können Skripts erstellen und bearbeiten, ohne mit einer Instanz von [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] verbunden zu sein.  
  
-   Skripterstellung in jedem Dialogfeld. Sie können ein Skript in jedem Dialogfeld erstellen, damit Sie die Skripts nach dem Erstellen lesen, ändern, speichern und wieder verwenden können.  
  
-   Nicht-modale Dialogfelder. Wenn Sie auf ein Benutzeroberflächen-Dialogfeld zugreifen, können Sie andere Ressourcen in [!INCLUDE[ssManStudioFull](../content/includes/ssManStudioFull_md.md)] durchsuchen, ohne das Dialogfeld zu schließen.  
  
## Projektmappen und Skriptprojekte  
Mit dem Projektmappen-Explorer können Sie Datenbankprojektmappen speichern und erneut öffnen. Mit Projektmappen werden zusammengehörige Skriptprojekte und Dateien angeordnet. In Skriptprojekten werden [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)]-Skriptdateien, SQL-Vorlagen, Verbindungsinformationen und sonstige Dateien gespeichert. Wenn ein Skript in einem Skriptprojekt gespeichert wird, können Benutzer folgende Aktionen ausführen:  
  
-   Aufrechterhalten der Versionskontrolle für Skripts  
  
-   Speichern von Ergebnisoptionen mit einem Skript  
  
-   Organisieren von zusammengehörigen Skripts zu einem einzigen Skriptprojekt  
  
-   Speichern von Verbindungsinformationen mit Skripts  
  
Der Projektmappen-Explorer ist ein Tool für Entwickler, die Skripts, die zum gleichen Projekt gehören, erstellen und wieder verwenden. Wenn ein ähnlicher Task später erforderlich ist, können Sie Skriptgruppen verwenden, die in einem Projekt gespeichert wurden. Wenn Sie die Anwendung mithilfe von erstellt haben [!INCLUDE[msCoName](../content/includes/msCoName_md.md)] [!INCLUDE[vsprvs](../content/includes/vsprvs_md.md)], finden Sie Projektmappen-Explorer rasch vertraut sein.  
  
Eine Projektmappe besteht aus mindestens einem Skriptprojekt. Ein Projekt besteht aus mindestens einem Skript oder mindestens einer Verbindung. In einem Projekt können außerdem andere Dateien als nur Skriptdateien vorhanden sein.  
  
## Siehe auch  
[Verwenden von SQL Server Management Studio](../content/Use-SQL-Server-Management-Studio.md)  
[Schreiben, analysieren und Bearbeiten von Abfragen mit SQL Server Management Studio](assetId:///062051e4-4b77-4969-98ae-d2547c24ce3e)  
[Solutions & #40; SQL Server Management Studio & #41;](../content/Solutions--SQL-Server-Management-Studio-.md)  
  
