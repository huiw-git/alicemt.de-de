---
title: "SQL Server-Agent-Fehlerprotokoll"
ms.custom: na
ms.date: 07/15/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - tools-ssms
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 0b2d6e6e-cd2d-4b8b-9fa2-2bbd2fc0da41
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
# SQL Server-Agent-Fehlerprotokoll
[!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] Agent erstellt ein Fehlerprotokoll, Datensätze Warnungen und Fehler in der Standardeinstellung. Die folgenden Warnungen und Fehler werden im Protokoll angezeigt:  
  
-   Fehlermeldungen, die Informationen zu potenziellen Problemen, wie z. B. "Job <*Auftrag\_Namen*> wurde gelöscht, während es ausgeführt wurde."  
  
-   Fehlermeldungen, die in der Regel Eingriff eines Systemadministrators erfordern, z. B. "Mailsitzung kann nicht gestartet werden". Fehlermeldungen können an einen bestimmten Benutzer oder Computer gesendet werden **net Send**.  
  
[!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] verwaltet bis zu neun [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] -Agent-Fehlerprotokolle. Jedes archivierte Fehlerprotokoll verfügt über eine Dateierweiterung, durch die das relative Alter des Protokolls angegeben wird. So gibt z. B. die Erweiterung ".1" das zuletzt archivierte Fehlerprotokoll an, während die Erweiterung ".9" das Fehlerprotokoll kennzeichnet, das zuerst archiviert wurde.  
  
Standardmäßig werden Meldungen zur Ablaufverfolgung nicht in das [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)]-Agent-Fehlerprotokoll geschrieben, da das Protokoll dadurch zu schnell aufgefüllt werden könnte. Wenn das Fehlerprotokoll voll ist, sind Ihre Möglichkeiten zur Auswahl und Analyse schwierigerer Fehler eingeschränkt. Da durch das Protokoll die Verarbeitungsmenge für den Server erhöht wird, sollten Sie genau überlegen, welche Vorteile Ihnen das Aufzeichnen der Meldungen zur Ablaufverfolgung im Fehlerprotokoll bietet. Im Allgemeinen ist es am besten, alle Meldungen nur beim Debuggen eines bestimmten Problems aufzuzeichnen.  
  
Beim Beenden des [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)]-Agents können Sie den Speicherort des [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)]-Agent-Fehlerprotokolls ändern. Leere Fehlerprotokolle können nicht geöffnet werden. Sie können das [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)]-Agent-Protokoll jederzeit durchlaufen, ohne den [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)]-Agent anhalten zu müssen.  
  
**So zeigen Sie das SQL Server-Agent-Fehlerprotokoll an**  
  
-   [SQL Server-Agent-Fehlerprotokolls & #40 anzeigen; SQL Server Management Studio & #41;](../content/View-SQL-Server-Agent-Error-Log--SQL-Server-Management-Studio-.md)  
  
**So benennen Sie ein SQL Server-Agent-Fehlerprotokoll um**  
  
-   [Umbenennen eines SQL Server-Agent-Fehlerprotokolls & #40. SQL Server Management Studio & #41;](../content/Rename-a-SQL-Server-Agent-Error-Log--SQL-Server-Management-Studio-.md)  
  
**So senden Sie SQL Server-Agent-Fehlermeldungen**  
  
-   [Senden von SQL Server-Agent-Fehlermeldungen](../content/Send-SQL-Server-Agent-Error-Messages.md)  
  
**So schreiben Sie Meldungen zur Ablaufverfolgung in das SQL Server-Agent-Fehlerprotokoll**  
  
-   [Schreiben Sie Meldungen zur Ablaufverfolgung in der SQL Server-Agent-Fehlerprotokolls & #40. SQL Server Management Studio & #41;](../content/Write-Execution-Trace-Messages-to-the-SQL-Server-Agent-Error-Log--SQL-Server-Management-Studio-.md)  
  
