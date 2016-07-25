---
title: "Herstellen einer Verbindung mit einer beliebigen SQL Server-Komponente aus SQL Server Management Studio"
ms.custom: na
ms.date: 07/15/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - tools-ssms
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 5eeb41bd-b25b-4d3b-a005-a7d9e4b5978e
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
# Herstellen einer Verbindung mit einer beliebigen SQL Server-Komponente aus SQL Server Management Studio
[!INCLUDE[ssManStudioFull](../content/includes/ssManStudioFull_md.md)] bietet Funktionen für das Verwalten aller Komponenten von [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)]. Mit [!INCLUDE[ssManStudio](../content/includes/ssManStudio_md.md)] können Sie eine Verbindung zu folgenden Komponenten herstellen:  
  
-   Eine Instanz von [!INCLUDE[ssDEnoversion](../content/includes/ssDEnoversion_md.md)].  
  
-   [!INCLUDE[ssASnoversion](../content/includes/ssASnoversion_md.md)].  
  
-   [!INCLUDE[ssISnoversion](../content/includes/ssISnoversion_md.md)].  
  
-   [!INCLUDE[ssRSnoversion](../content/includes/ssRSnoversion_md.md)].  
  
Obwohl [!INCLUDE[ssManStudio](../content/includes/ssManStudio_md.md)] es Ihnen ermöglicht, mit Abfragen zu arbeiten, ohne zuerst eine Verbindung mit einer Datenquelle herzustellen, ist für die meisten anderen Aufgaben eine Verbindung erforderlich. [!INCLUDE[ssManStudio](../content/includes/ssManStudio_md.md)] Stellt die **Verbindung mit Server herstellen** Dialogfeld zum Konfigurieren von Verbindungseigenschaften für die [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] Komponenten. Wenn [!INCLUDE[ssManStudio](../content/includes/ssManStudio_md.md)] gestartet wird, wird die **Verbindung mit Server herstellen** im Dialogfeld aufgefordert, zu einem Server herstellen. Die **mit Server verbinden** Dialogfeld behält die Verbindungseinstellungen von der letzten Ausführung wurde verwendet.  
  
> [!NOTE]  
> Diese Funktion lässt sich deaktivieren, sodass keine automatische Initialisierung einer Verbindung stattfindet. Weitere Informationen finden Sie unter [Startoptionen für Datenbank-Engine-Dienst](assetId:///d373298b-f6cf-458a-849d-7083ecb54ef5).  
  
## Speichern von Verbindungen  
Sie können Verbindungen mit bestimmten Servern in der Liste der registrierten Server speichern, oder Sie können mit dem Projektmappen-Explorer Verbindungen in Projekten speichern.  
  
### Speichern von Verbindungen in der Liste der registrierten Server  
Wenn Sie einen Server registrieren, speichert [!INCLUDE[ssManStudio](../content/includes/ssManStudio_md.md)] die Verbindungsinformationen in der Liste der registrierten Server. Doppelklicken Sie zum Verbinden mit einem registrierten Server\-Klicken Sie auf den Namen des Servers in registrierte Server. Daraufhin öffnet der Objekt-Explorer eine Verbindung zum Server.  
  
### Speichern von Verbindungen im Projektmappen-Explorer  
Mit dem Projektmappen-Explorer können Sie zugehörige Abfragen, Skripts, Verbindungen und andere Informationen in einem Projekt speichern. Jedes skriptprojekt enthält einen Knoten namens **Verbindungen**, in dem Sie eine oder mehrere Verbindungen speichern können. Zum Hinzufügen einer Verbindung mit der rechten Maustaste\-Klicken Sie auf **Verbindungen**, und klicken Sie dann auf **neue Verbindung**. Erweitern Sie den Zugriff auf eine gespeicherte Verbindung **Verbindungen** und double\-Klicken Sie auf die Verbindung. [!INCLUDE[ssManStudio](../content/includes/ssManStudio_md.md)] Öffnet ein Abfragefenster mit dieser Verbindung verknüpft ist. Beim Speichern behalten Skripts die Verknüpfung zu einer bestimmten Verbindung bei.  
  
## Siehe auch  
[Verwenden von SQL Server Management Studio](../content/Use-SQL-Server-Management-Studio.md)  
[Objekt-Explorer](../content/Object-Explorer.md)  
  
