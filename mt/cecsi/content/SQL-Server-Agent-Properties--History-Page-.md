---
title: "SQL Server-Agent-Eigenschaften (Seite Verlauf)"
ms.custom: na
ms.date: 07/27/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - tools-ssms
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: dc73734c-b3c3-407f-bbd1-8714b4fa47b0
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
# SQL Server-Agent-Eigenschaften (Seite Verlauf)
Auf dieser Seite können Sie die Einstellungen für die Verwaltung des Verlaufsprotokolls für den [!INCLUDE[msCoName](../content/includes/msCoName_md.md)] [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] -Agent-Dienst anzeigen und bearbeiten.  
  
## Optionen  
**Größe des Auftragsverlaufsprotokolls beschränken**  
Legt die Grenzen für die Menge der Auftragsverlaufsinformationen fest, die im Protokoll des [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)]-Agents verbleiben.  
  
**Maximale Länge des Auftragsverlaufsprotokolls (in Zeilen)**  
Legt die maximale Anzahl der Zeilen fest, die der [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)]-Agent beibehält. Wenn das Protokoll diese Anzahl von Zeilen überschreitet, werden die ältesten Zeilen vom [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)]-Agent entfernt, sobald neue Zeilen eingetragen werden.  
  
**Maximale Zeilenanzahl pro Auftrag in Auftragsverlauf**  
Legt die maximale Anzahl der Zeilen fest, die der [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)]-Agent pro Auftrag beibehält. Wenn der Verlauf eines bestimmten Auftrags diese Anzahl von Zeilen überschreitet, werden die ältesten Zeilen vom [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)]-Agent entfernt, sobald neue Zeilen eingetragen werden.  
  
**Agentverlauf entfernen**  
Gibt an, dass der [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)]-Agent Einträge entfernt, die länger als eine bestimmte Zeitspanne im Protokoll vorhanden sind. Dies ist eine\-Mal ausführen, um den Verlauf zu entfernen. Wenn ein erneut auftretender Auftrag benötigt wird, erstellen und planen Sie einen Wartungsplan mit einem Cleanupauftrag.  
  
**Älter als**  
Legt die Zeitspanne fest, für die der [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)]-Agent die Einträge beibehält.  
  
## Siehe auch  
[SQL Server-Agent-Fehlerprotokoll](../content/SQL-Server-Agent-Error-Log.md)  
  
