---
title: "Eigenschaften von Warnung - neue Warnung (Seite Allgemein)"
ms.custom: na
ms.date: 07/15/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - tools-ssms
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: f5c11610-62e3-44df-9800-a5dc35be4a09
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
# Eigenschaften von Warnung - neue Warnung (Seite Allgemein)
Verwenden Sie diese Seite zum Anzeigen und ändern die allgemeinen Eigenschaften des [!INCLUDE[msCoName](../content/includes/msCoName_md.md)] [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] -Agent-Warnungen.  
  
## Optionen  
**Name**  
Ändern Sie den Namen der Warnung.  
  
**Aktivieren**  
Aktivieren Sie die Warnung. Wenn die Warnung nicht aktiviert ist, werden die in der Warnung angegebenen Aktionen nicht ausgeführt.  
  
**Typ**  
Wählen Sie den Typ der Warnung aus:  
  
-   **SQL Server-ereigniswarnung** reagiert auf Nachrichten in der [!INCLUDE[msCoName](../content/includes/msCoName_md.md)] Windows-Ereignisprotokoll.  
  
-   **SQL Server-leistungsstatuswarnung** reagiert auf eine bestimmte Bedingung in einem Leistungsindikator.  
  
-   **WMI-ereigniswarnung** reagiert auf ein Ereignis (Windows Management Instrumentation, WMI).  
  
## Optionen für die SQL Server-Ereigniswarnung  
**Datenbankname**  
Geben Sie eine Datenbank für das Ereignis oder **alle Datenbanken** So reagieren Sie auf eine Meldung unabhängig von der Datenbank, in dem das Ereignis auftritt.  
  
**Fehlernummer**  
Geben Sie an, dass dieses Ereignis auf einen Fehler reagiert, und geben Sie die Fehlernummer an.  
  
**Severity**  
Geben Sie an, dass dieses Ereignis auf alle Meldungen innerhalb eines bestimmten Schweregrads reagiert, und geben Sie den Schweregrad an.  
  
**Warnung auslösen, wenn eine Meldung Folgendes enthält**  
Filtert Ereignisse nach einer bestimmten Zeichenfolge. Wenn diese Option ausgewählt ist, reagiert die Warnung nur auf Ereignisse, die eine bestimmte Zeichenfolge enthalten.  
  
**Meldungstext**  
Geben Sie die Zeichenfolge ein, die zum Filtern von Ereignissen verwendet werden soll.  
  
## SQL Server-Leistungsstatuswarnungen  
**Objekt**  
Geben Sie das zu überwachende Leistungsobjekt an.  
  
**Leistungsindikator**  
Geben Sie den Leistungsindikator innerhalb des Leistungsobjekts an, der überwacht werden soll.  
  
**Instanz**  
Geben Sie die Instanz des Leistungsindikators an, die überwacht werden soll.  
  
**Warnung, falls Leistungsindikator**  
Geben Sie das Verhalten des Leistungsindikators an, auf das die Warnung reagiert. Sie können z. B. die Warnung auf eine Bedingung reagieren, in dem der Wert des der **freien Speicherplatz in ' tempdb ' (KB)** Leistungsindikator unter einen bestimmten Wert fällt, oder Sie können der Warnung, die auf eine Bedingung zu reagieren, in denen die **SQL-Kompilierungen\/s** einen bestimmten Wert übersteigt.  
  
**Wert**  
Geben Sie einen Wert für den Leistungsindikator an.  
  
## WMI-Ereigniswarnungsoptionen  
**Namespace**  
Geben Sie den Namespace an, der für die WQL-Anweisung (WMI Query Language) verwendet werden soll. Es werden nur Namespaces auf dem Computer unterstützt, auf dem der [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)]-Agent ausgeführt wird.  
  
**Query**  
Geben Sie die WQL-Anweisung an, die das Ereignis identifiziert, auf das die Warnung reagiert.  
  
## Siehe auch  
[Warnungen](../content/Alerts.md)  
[Verwenden von WQL mit dem WMI-Anbieter für Serverereignisse](assetId:///58b67426-1e66-4445-8e2c-03182e94c4be)  
[Erstellen einer Warnung mithilfe einer Fehlernummer](../content/Create-an-Alert-Using-an-Error-Number.md)  
[Erstellen einer Warnung mithilfe von Schweregraden](../content/Create-an-Alert-Using-Severity-Level.md)  
  
