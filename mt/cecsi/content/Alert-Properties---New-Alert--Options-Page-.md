---
title: "Eigenschaften von Warnung - neue Warnung (Optionsseite)"
ms.custom: na
ms.date: 07/27/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - tools-ssms
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 6e4f41aa-832d-46ba-b6b5-cf1d3b15d33f
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
# Eigenschaften von Warnung - neue Warnung (Optionsseite)
Mithilfe dieser Seite können Sie die Optionen für Agentwarnungen in [!INCLUDE[msCoName](../content/includes/msCoName_md.md)] [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] anzeigen und ändern.  
  
## Optionen  
**E\-e-Mail-Nachrichten**  
Einschließen von Fehlertext des Ereignisses ggf. in e\-e-Mail-Benachrichtigungen.  
  
**Pager**  
Schließt Fehlertext des Ereignisses ggf. in Pagerbenachrichtigungen ein.  
  
**NET SEND**  
Schließt Fehlertext des Ereignisses ggf. in NET SEND-Benachrichtigungen ein.  
  
**Zusätzlich zu sendende Warnbenachrichtigung**  
Geben Sie hier zusätzlichen Text ein, der in die Benachrichtigungsmeldungen aufgenommen werden soll.  
  
**Antwortverzögerung**  
Geben Sie eine Verzögerung für das wiederholte Auftreten des Ereignisses an. Einige Ereignisse können innerhalb einer kurzen Zeitspanne häufig auftreten. In diesem Fall könnte es sinnvoll sein, zwar über das Auftreten des Ereignisses informiert zu werden, nicht aber für jedes Auftreten eine Meldung zu erhalten. Mit dieser Option können Sie einen Zeitpunkt festlegen,\-heraus. Durch die Angabe einer Verzögerung nach der Warnungsantwort auf ein Ereignis wartet der [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)]-Agent die angegebene Verzögerungszeit ab, bevor eine weitere Antwort zurückgegeben wird, unabhängig davon, ob das Ereignis in der Zwischenzeit wieder auftritt.  
  
**Minuten**  
Geben Sie eine Verzögerung in Minuten an. Wenn bei jedem Auftreten des Ereignisses geantwortet werden soll, geben Sie 0 Minuten und 0 Sekunden an.  
  
**Sekunden**  
Geben Sie eine Verzögerung in Sekunden an. Wenn bei jedem Auftreten des Ereignisses geantwortet werden soll, geben Sie 0 Minuten und 0 Sekunden an.  
  
## Siehe auch  
[Warnungen](../content/Alerts.md)  
  
