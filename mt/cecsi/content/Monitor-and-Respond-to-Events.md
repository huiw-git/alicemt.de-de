---
title: "&#220;berwachen und Reagieren auf Ereignisse"
ms.custom: na
ms.date: 07/27/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - tools-ssms
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: f7fbe155-5b68-4777-bc71-a47637471f32
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
# &#220;berwachen und Reagieren auf Ereignisse
[!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] Agents überwachen und reagieren automatisch auf *Ereignisse*, z. B. Nachrichten von [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)], bestimmte leistungsbedingungen und Windows-Verwaltungsinstrumentation (Windows Management Instrumentation, WMI)-Ereignisse.  
  
## In diesem Abschnitt  
[Warnungen](../content/Alerts.md)  
Enthält Informationen zum Benennen von Warnungen und Auswählen von Ereignissen oder Leistungsbedingungen, für die Warnungen ausgegeben werden.  
  
[Erstellen eines benutzerdefinierten Ereignisses](../content/Create-a-User-Defined-Event.md)  
Enthält Informationen zum Erstellen von Ereignissen, die nicht von [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] vordefiniert sind.  
  
[Operatoren](../content/Operators.md)  
Enthält Informationen zum Erstellen von Aliasen für Administratoren, die vom [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)]-Agent zum Versenden von Benachrichtigungen verwendet werden können, wenn Aufträge einen Fehler erzeugen oder erfolgreich ausgeführt werden.  
  
## Informationen zum Überwachen von und Reagieren auf Ereignisse  
Automatische Reaktionen auf Ereignisse heißen *Warnungen*. Sie können Warnungen für Ereignisse definieren um anzugeben, wie vom [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)]-Agent auf das Auftreten dieser Ereignisse reagiert werden soll. Von einer Warnung kann auf ein Ereignis reagiert werden, indem ein Administrator benachrichtigt oder ein Auftrag ausgeführt wird, oder indem beide Aktionen ausgeführt werden. Von einer Warnung kann ein Ereignis auch an das Microsoft Windows-Anwendungsprotokoll auf einem anderen Computer weitergeleitet werden. Sie können beispielsweise angeben, dass bei einem Ereignis mit dem Schweregrad 19 sofort ein Operator benachrichtigt wird. Durch das Definieren von Warnungen können Datenbankadministratoren [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] effektiver überwachen und verwalten.  
  
[!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] Agent reagiert nur auf Ereignisse, die für die Warnung definiert ist. Die vom [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)]-Agent zum Überwachen von Ereignissen verwendete Methode hängt vom Typ des Ereignisses ab.  
  
Wenn eine [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)]-Agent-Warnung für einen Leistungsindikator definiert ist, wird der Leistungsindikator direkt vom [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)]-Agent überwacht. Bei einem WMI-Ereignis wird vom [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)]-Agent eine Ereignisabfrage für das WMI-Ereignis registriert.  
  
Um auf Meldungen von [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] zu reagieren, wird vom [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)]-Agent das Windows-Anwendungsprotokoll überwacht. [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] Agent kann nur auf Nachrichten reagieren, die in diesem Protokoll angezeigt werden. Standardmäßig protokolliert SQL Server die folgenden Meldungen im Windows-Anwendungsprotokoll:  
  
-   Der Schweregrad 19 oder höher Sysmessages-Fehler.  
  
    Wenn Sie auch bestimmte Sysmessages-Fehler zu melden, die einen Schweregrad niedriger als 19 haben möchten, verwenden Sie sp\_Altermessage gespeicherte Prozedur, um solche Fehler als "immer protokolliert" kennzeichnen.  
  
-   Jede RAISERROR-Anweisung, die durch Verwenden der WITH LOG-Syntax aufgerufen wurde.  
  
    Das Verwenden von RAISERROR WITH LOG wird empfohlen, um von einer Instanz von SQL Server in das Windows-Anwendungsprotokoll zu schreiben.  
  
-   Jeder Anwendungsereignis, das protokolliert wird, mithilfe von Xp\_Logevent.  
  
    > [!NOTE]  
    > Das Protokollieren von Anwendungsereignissen belegt Protokollspeicher und kann dazu führen, dass das Windows-Anwendungsprotokoll die Maximalgröße überschreitet. Stellen Sie sicher, dass das Windows-Anwendungsprotokoll über eine ausreichende Größe verfügt, damit es nicht zu einem Verlust von SQL Server-Ereignisinformationen kommt.  
  
Wenn von [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] eine Meldung protokolliert wird, vergleicht der [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)]-Agent-Dienst die Meldung mit den Warnungen, die vom [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)]-Administrator definiert worden sind.  
  
Unabhängig von der Ereignisquelle reagiert der [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)]-Agent-Dienst auf das Ereignis, indem die Tasks ausgeführt werden, die in der Warnung für das Ereignis angegeben worden sind.  
  
## Siehe auch  
[sp_altermessage](assetId:///1b28f280-8ef9-48e9-bd99-ec14d79abaca)  
  
