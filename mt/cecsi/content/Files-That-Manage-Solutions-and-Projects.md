---
title: "Dateien zum Verwalten von Projektmappen und Projekten"
ms.custom: na
ms.date: 07/27/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - tools-ssms
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: e19d2859-0b97-4727-ac27-c4c226d86b2f
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
# Dateien zum Verwalten von Projektmappen und Projekten
Dieses Thema beschreibt die Dateitypen, die für spezifisch sind [!INCLUDE[msCoName](../content/includes/msCoName_md.md)] [!INCLUDE[ssManStudioFull](../content/includes/ssManStudioFull_md.md)]. In der Standardeinstellung alle Projektmappen und Projekte werden in erstellt \\Eigene\\SQL Server Management Studio Projects.  
  
## Management Studio-Projektmappendateien  
[!INCLUDE[ssManStudioFull](../content/includes/ssManStudioFull_md.md)] verwendet verschiedene Dateitypen als [!INCLUDE[msCoName](../content/includes/msCoName_md.md)] [!INCLUDE[ssBIDevStudioFull](../content/includes/ssBIDevStudioFull_md.md)] oder [!INCLUDE[msCoName](../content/includes/msCoName_md.md)] Visual Studio. Dies bedeutet, Sie können nicht geöffnet werden eine [!INCLUDE[ssManStudioFull](../content/includes/ssManStudioFull_md.md)] Lösung in [!INCLUDE[ssBIDevStudioFull](../content/includes/ssBIDevStudioFull_md.md)] oder in Visual Studio. [!INCLUDE[ssManStudioFull](../content/includes/ssManStudioFull_md.md)] -Projektmappendateien ermöglichen dem Projektmappen-Explorer, um eine Benutzeroberfläche zum Verwalten Ihrer Dateien anzuzeigen.  
  
|Erweiterung|Dateityp|Beschreibung|Erstellt von|  
|-------------|-------------|---------------|--------------|  
|SSMSSLN|[!INCLUDE[ssManStudioFull](../content/includes/ssManStudioFull_md.md)] Solution-Objekt|Stellt die Umgebung Verweise auf den Speicherort auf dem Datenträger von [!INCLUDE[msCoName](../content/includes/msCoName_md.md)] [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] Projekte, Projektelemente und -Lösung|[!INCLUDE[ssManStudioFull](../content/includes/ssManStudioFull_md.md)]|  
  
## Management Studio-Projektdateien  
In derselben Weise, wie Projektmappen Projektmappendateien zum Verwalten von Objekten in einer Projektmappe enthalten, enthalten Projekte Projektdateien. Der Projektdateityp, der von [!INCLUDE[ssManStudioFull](../content/includes/ssManStudioFull_md.md)] für ein Projekt erstellt wird, hängt von der Vorlage ab, mit der das Projekt erstellt wurde. In der folgenden Tabelle werden die Dateitypen beschrieben, die für die einzelnen Projekte erstellt werden.  
  
|Erweiterung|Projektvorlage|  
|-------------|--------------------|  
|SSMSSQLPROJ|[!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] -Skriptprojekt|  
|SSMSASPROJ|[!INCLUDE[ssASnoversion](../content/includes/ssASnoversion_md.md)] -Skriptprojekt|  
  
## Speicherort der Lösung\-Ebene von Dateien  
Standardmäßig Lösung\-Ebene Dateien werden erstellt, im physischen Verzeichnis des ersten Projekts, das mit der Projektmappe erstellt wird. Sie können ein Verzeichnis für die Projektmappe angeben, indem Sie eine Projektmappe erstellen. Sie können das Verzeichnis auch angeben, wenn Sie ein neues Projekt erstellen.  
  
Wenn eine Verzeichnisstruktur vorhanden ist, die der logischen Struktur im Projektmappen-Explorer ähnelt, lassen sich Projekt- und Projektmappendateien einfacher suchen und mit anderen Entwicklern im Team gemeinsam nutzen.  
  
## Siehe auch  
[Verwalten von Dateien mit Codierung](../content/Manage-Files-with-Encoding.md)  
[Sonstige Dateien](../content/Miscellaneous-Files.md)  
[Projektmappen-Explorer](../content/Solution-Explorer.md)  
[Solutions & #40; SQL Server Management Studio & #41;](../content/Solutions--SQL-Server-Management-Studio-.md)  
[Projekte & #40; SQL Server Management Studio & #41;](../content/Projects--SQL-Server-Management-Studio-.md)  
[Quellcodeverwaltung des Projektmappen-Explorers](https://msdn.microsoft.com/en-us/library/ms173879.aspx)  
  
