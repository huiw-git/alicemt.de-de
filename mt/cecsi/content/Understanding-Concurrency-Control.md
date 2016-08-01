---
title: "Grundlegendes zur Parallelit&#228;tssteuerung"
ms.custom: na
ms.date: 07/27/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - drivers
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 98b7dabe-9b12-4e1d-adeb-e5b5cb0c96f3
caps.latest.revision: 24
caps.handback.revision: 23
manager: jhubbard
translation.priority.ht: 
  - de-de
  - es-es
  - fr-fr
  - it-it
  - ja-jp
  - ko-kr
  - pt-br
  - ru-ru
  - sv-se
  - zh-cn
  - zh-tw
---
# Grundlegendes zur Parallelit&#228;tssteuerung
  Als Parallelitätssteuerung werden unterschiedliche Verfahren beschrieben, mit denen die Integrität der Datenbank erhalten wird, wenn mehrere Benutzer gleichzeitig Zeilen aktualisieren. Falsche Parallelität kann zu Problemen führen, beispielsweise Dirty Reads, Phantomlesezugriffe und nicht wiederholbare Lesevorgänge.[!INCLUDE[jdbcNoVersion](../content/includes/jdbcNoVersion_md.md)] stellt Schnittstellen für alle von [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] verwendeten Parallelitätsverfahren bereit, um diese Probleme zu beheben.  
  
> [!NOTE]  
>  Weitere Informationen zur [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)]\-Parallelität finden Sie unter "Verwalten des parallelen Datenzugriffs" in der [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)]\-Onlinedokumentation.  
  
## Hinweise  
 Der JDBC\-Treiber unterstützt die folgenden Parallelitätstypen:  
  
|Parallelitätstyp|Merkmale|Zeilensperren|Beschreibung|  
|----------------------|--------------|-------------------|------------------|  
|CONCUR\_READ\_ONLY|Read Only|Nein|Updates über den Cursor sind nicht zulässig; es werden keine Sperren für die Zeilen aufrechterhalten, aus denen das Resultset besteht.|  
|CONCUR\_UPDATABLE|Optimistic Read Write|Nein|Die Datenbank geht davon aus, dass Zeilenkonflikte unwahrscheinlich, aber möglich sind. Zeilenintegrität wird mit einem Timestampvergleich geprüft.|  
|CONCUR\_SS\_SCROLL\_LOCKS|Pessimistic Read Write|Ja|Die Datenbank geht davon aus, dass Zeilenkonflikte wahrscheinlich sind. Zeilenintegrität wird mit Zeilensperren sichergestellt.|  
|CONCUR\_SS\_OPTIMISTIC\_CC|Optimistic Read Write|Nein|Die Datenbank geht davon aus, dass Zeilenkonflikte unwahrscheinlich, aber möglich sind. Zeilenintegrität wird mit einem Timestampvergleich überprüft.<br /><br /> Bei [!INCLUDE[ssVersion2005](../content/includes/ssVersion2005_md.md)] und höher ändert der Server dies in CONCUR\_SS\_OPTIMISTIC\_CCVAL, wenn die Tabelle keine Timestampspalte enthält.<br /><br /> Wenn in [!INCLUDE[ssVersion2000](../content/includes/ssVersion2000_md.md)] die zugrunde liegende Tabelle eine timestamp\-Spalte aufweist, wird OPTIMISTIC WITH ROW VERSIONING selbst dann verwendet, wenn OPTIMISTIC WITH VALUES angegeben wurde. Wenn OPTIMISTIC WITH ROW VERSIONING angegeben wurde und die Tabelle keine Timestamps aufweist, wird OPTIMISTIC WITH VALUES verwendet.|  
|CONCUR\_SS\_OPTIMISTIC\_CCVAL|Optimistic Read Write|Nein|Die Datenbank geht davon aus, dass Zeilenkonflikte unwahrscheinlich, aber möglich sind. Zeilenintegrität wird mit einem Zeilendatenvergleich geprüft.|  
  
## Nicht aktualisierbare Resultsets  
 Ein aktualisierbares Resultset ist ein Resultset, in dem Zeilen eingefügt, aktualisiert und gelöscht werden können. In den folgenden Fällen kann [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] keinen aktualisierbaren Cursor erstellen. Die generierte Ausnahme lautet "Das Resultset kann nicht aktualisiert werden".  
  
|Ursache|Beschreibung|Lösung|  
|-------------|------------------|------------|  
|Anweisung wurde nicht mit JDBC 2.0\-Syntax \(oder neuer\) erstellt|In JDBC 2.0 wurden neue Methoden eingeführt, um Anweisungen zu erstellen. Bei der Verwendung von JDBC 1.0\-Syntax ist das Resultset standardmäßig schreibgeschützt.|Geben Sie den Resultsettyp und die Parallelität beim Erstellen der Anweisung an.|  
|Anweisung wurde mit TYPE\_SCROLL\_INSENSITIVE erstellt|[!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] erstellt einen statischen Momentaufnahmencursor. Dieser ist von den zugrunde liegenden Tabellenzeilen getrennt, um den Cursor vor Zeilenudpates durch andere Benutzer zu schützen.|Verwenden Sie TYPE\_SCROLL\_SENSITIVE, TYPE\_SS\_SCROLL\_KEYSET, TYPE\_SS\_SCROLL\_DYNAMIC oder TYPE\_FORWARD\_ONLY mit CONCUR\_UPDATABLE, um das Erstellen eines statischen Cursors zu vermeiden.|  
|Tabellenentwurf schließt einen KEYSET\-Cursor oder einen DYNAMIC\-Cursor aus|Die zugrunde liegende Tabelle weist keine eindeutigen Schlüssel auf, mit denen [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] eine Zeile eindeutig identifizieren kann.|Fügen Sie der Tabelle eindeutige Schlüssel hinzu, um eine eindeutige Identifikation jeder Zeile bereitzustellen.|  
  
## Siehe auch  
 [Verwalten von Resultsets mit dem JDBC-Treiber](../content/Managing-Result-Sets-with-the-JDBC-Driver.md)  
  
  