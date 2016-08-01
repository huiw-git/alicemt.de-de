---
title: "Abfragen von Servern"
ms.custom: na
ms.date: 07/27/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - tools-ssms
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 96f5fd43-3edd-4418-9dd0-4d34e618890e
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
# Abfragen von Servern
Wenn die Multiserververwaltung implementiert ist, stellen die Zielserver regelmäßig eine Verbindung mit dem Masterserver her, um Informationen zu ausgeführten Aufträgen hochzuladen und neue Aufträge herunterzuladen. Herstellen einer Verbindung mit dem Masterserver ist bezeichnet *Server abrufen,* findet in regelmäßigen *Abrufintervallen.*  
  
## Abrufintervalle  
Das Abrufintervall (standardmäßig eine Minute) steuert, wie oft der Zielserver eine Verbindung mit dem Masterserver herstellt, um Anweisungen herunterzuladen und die Ergebnisse der Auftragsausführung hochzuladen.  
  
Wenn ein Zielserver den Masterserver abruft, liest er die der Zielserver vom zugewiesenen Vorgänge die **Sysdownloadlist** -Tabelle in der **Msdb** Datenbank. Diese Operationen steuern Multiserveraufträge sowie verschiedene Aspekte des Verhaltens eines Zielservers. Dazu gehören beispielsweise das Löschen, Einfügen oder Starten eines Auftrags und das Aktualisieren des Abrufintervalls eines Zielservers.  
  
Operationen werden bereitgestellt, um die **Sysdownloadlist** -Tabelle auf eine der folgenden Methoden:  
  
-   Explizit durch Verwenden der **sp\_buchen\_Msx\_Vorgang** gespeicherte Prozedur.  
  
-   Implizit durch Verwenden anderer gespeicherter Auftragsprozeduren.  
  
Bei Verwendung des Auftrags gespeicherte Prozeduren zum Ändern von multiserver-Auftragszeitplänen oder Multiserverauftragsschritten bzw. von SQL Distributed Management Objects (SQL\-DMO) zum Steuern von Multiserveraufträgen, führen Sie folgenden Befehl nach dem Ändern der Multiserverauftragsschritte oder Zeitpläne eines Multiserverauftrags:  
  
```  
EXECUTE msdb.dbo.sp_post_msx_operation 'INSERT', 'JOB', '<job id>'  
```  
  
Durch die Ausgabe dieses Befehls bleiben die Zielserver mit der aktuellen Auftragsdefinition synchronisiert.  
  
Es ist nicht notwendig, Vorgänge explizit bereitzustellen, wenn Sie Folgendes verwenden:  
  
-   Microsoft [!INCLUDE[ssManStudioFull](../content/includes/ssManStudioFull_md.md)] zum Steuern von Multiserveraufträgen.  
  
-   Gespeicherte Auftragsprozeduren, die weder Auftragszeitpläne noch Auftragsschritte ändern.  
  
**So erzwingen Sie, dass ein Zielserver den Masterserver abruft**  
  
-   [SQL Server Management Studio](../content/Force-a-Target-Server-to-Poll-the-Master-Server.md)  
  
-   [Transact-SQL](assetId:///085deef8-2709-4da9-bb97-9ab32effdacf)  
  
## Siehe auch  
[Verwalten von Ereignissen](../content/Manage-Events.md)  
  
