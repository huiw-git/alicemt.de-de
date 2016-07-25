---
title: "SQL Server-Agent-Eigenschaften (Seite Allgemein)"
ms.custom: na
ms.date: 07/15/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - tools-ssms
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: b51601e9-5454-43c6-bb5e-24eb2ff043c8
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
# SQL Server-Agent-Eigenschaften (Seite Allgemein)
Verwenden Sie diese Seite zum Anzeigen und ändern die allgemeinen Eigenschaften der [!INCLUDE[msCoName](../content/includes/msCoName_md.md)] [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] -Agent-Dienst.  
  
## Optionen  
**Dienststatus**  
Zeigt den aktuellen Status des [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)]-Agent-Dienstes an.  
  
**SQL Server nach unerwartetem Beenden automatisch neu starten**  
[!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] -Agent neu gestartet [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] Wenn [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] unerwartet beendet wird.  
  
**SQL Server-Agent nach unerwartetem Beenden automatisch neu starten**  
[!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] Neustart [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] Agent Wenn [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] -Agent unerwartet beendet wird.  
  
**Filename**  
Geben Sie den Dateinamen für das Fehlerprotokoll an.  
  
**...**  
Mit dieser Schaltfläche können Sie nach der Fehlerprotokolldatei suchen.  
  
**Meldungen zur Ablaufverfolgung einschließen**  
Meldungen zur Ablaufverfolgung werden in das Fehlerprotokoll eingeschlossen. Meldungen zur Ablaufverfolgung stellen detaillierte Informationen zu [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)]-Agent-Vorgängen bereit. Deshalb benötigt die Protokolldatei mehr Datenträgerspeicherplatz, wenn diese Option ausgewählt ist. Diese Option sollte nur bei der Behandlung eines Problems ausgewählt werden, bei dem der [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)]-Agent eine Rolle spielt.  
  
**OEM-Datei schreiben**  
Schreibt die Fehlerprotokolldatei ohne\-Unicode-Datei. Dadurch wird der für die Protokolldatei erforderliche Datenträgerspeicherplatz reduziert. Meldungen, die Unicode enthalten, können jedoch schwieriger lesbar sein, wenn diese Option aktiviert ist.  
  
**NET SEND-Empfänger**  
Geben Sie den Namen eines Operators ein, der NET SEND-Benachrichtigungen von Meldungen empfängt, die [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)]-Agent in die Protokolldatei schreibt.  
  
## Siehe auch  
[Operatoren](../content/Operators.md)  
[SQL Server-Agent-Fehlerprotokoll](../content/SQL-Server-Agent-Error-Log.md)  
  
