---
title: "Diagrammbereich (Visual Database Tools)"
ms.custom: na
ms.date: 07/15/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - tools-ssms
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 399dfc7b-e2e7-47d3-bd11-163cbe0ce13c
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
# Diagrammbereich (Visual Database Tools)
Der Diagrammbereich liefert eine grafische Darstellung der Tabellen bzw.\-Werte von Objekten, die Sie aus der Datenverbindung ausgewählt haben. Weiterhin werden alle Joinbeziehungen zwischen ihnen angezeigt.  
  
Im Diagrammbereich können Sie folgende Aktionen ausführen:  
  
-   Hinzufügen oder Entfernen von Tabellen und\-Objekte zu bewerten und Datenspalten für die Ausgabe festlegen.  
  
-   Erstellen oder Ändern von Joins zwischen Tabellen und\-Objekte bewertet.  
  
Wenn Sie Änderungen im Diagrammbereich vornehmen, werden die Werte im Kriterienbereich und im SQL-Bereich entsprechend aktualisiert. Beispielsweise, wenn Sie eine Spalte für die Ausgabe in einer Tabelle oder Tabellen auswählen\-Fenster bewertet Objekt im Diagrammbereich, der Abfrage- und Ansicht-Designer wird die Datenspalte im Kriterienbereich und die SQL-Anweisung im SQL-Bereich hinzugefügt.  
  
Jede Tabelle oder eine Tabelle\-bewertet Objekt wird als separates Fenster im Diagrammbereich angezeigt. Das Symbol in der Titelleiste jedes Rechtecks gibt den dargestellten Objekttyp wieder, wie in der folgenden Tabelle beschrieben.  
  
## Optionen  
**Tabellen**  
Listet die Tabellen auf, die dem Diagrammbereich hinzugefügt werden können. Um eine Tabelle hinzuzufügen, wählen Sie sie aus, und klicken Sie auf **Hinzufügen**. Um mehrere Tabellen gleichzeitig hinzuzufügen, wählen Sie sie aus, und klicken Sie auf **Hinzufügen**.  
  
**Sichten**  
Listet die Sichten auf, die dem Diagrammbereich hinzugefügt werden können. Um eine Sicht hinzuzufügen, wählen Sie sie aus, und klicken Sie auf **Hinzufügen**. Um mehrere Sichten gleichzeitig hinzuzufügen, wählen Sie sie aus, und klicken Sie auf **Hinzufügen**.  
  
**Funktionen**  
Zeigt den Benutzer\-benutzerdefinierte Funktionen, die Sie dem Diagrammbereich hinzufügen können. Um eine Funktion hinzuzufügen, wählen Sie sie aus, und klicken Sie auf **Hinzufügen**. Um mehrere Funktionen gleichzeitig hinzuzufügen, wählen Sie sie aus, und klicken Sie auf **Hinzufügen**.  
  
**Lokale Tabellen**  
Listet die von Abfragen erstellten Tabellen auf, nicht die zur Datenbank gehörigen.  
  
**Synonyme**  
Listet die Synonyme auf, die dem Diagrammbereich hinzugefügt werden können. Um ein Synonym hinzuzufügen, wählen Sie es aus, und klicken Sie auf **Hinzufügen**. Um mehrere Synonyme gleichzeitig hinzuzufügen, wählen Sie sie aus, und klicken Sie auf **Hinzufügen**.  
  
|Symbol|Objekttyp|  
|--------|---------------|  
|![Visual Database Tools (Symbol)](../content/media/dv3wbi1.png "dv3wbi1")|Tabelle|  
|![Visual Database Tools (Symbol)](../content/media/dv3wbi2.png "dv3wbi2")|Abfrage oder Sicht|  
|![Visual Database Tools (Symbol)](../content/media/dv3wbi3.png "dv3wbi3")|Verknüpfte Tabelle|  
|![Visual Database Tools (Symbol)](../content/media/dvudficon.png "dvudficon")|Benutzer\-benutzerdefinierten Funktion|  
|![Visual Database Tools (Symbol)](../content/media/dv3wbi5.png "dv3wbi5")|Verknüpfte Sicht|  
  
Jedes Rechteck zeigt die Datenspalten für die Tabelle oder die Tabelle\-bewertet Objekt. Neben den Spaltennamen finden Sie Kontrollkästchen und Symbole, die Informationen zum Verwenden der Spalten in der Abfrage liefern. In QuickInfos erhalten Sie u. a. Informationen zum Datentyp und zur Größe der Spalten.  
  
Die folgende Tabelle enthält die Kontrollkästchen und Symbole in das Rechteck für jede Tabelle oder eine Tabelle\-bewertet Objekt.  
  
|Kontrollkästchen oder Symbol|Beschreibung|  
|-----------------------|---------------|  
|![Visual Database Tools (Symbol)](../content/media/dv3wbi7.png "dv3wbi7")<br /><br />![Visual Database Tools (Symbol)](../content/media/dv3wbi8.png "dv3wbi8")<br /><br />![Visual Database Tools (Symbol)](../content/media/dv3wbi9.png "dv3wbi9")<br /><br />![Visual Database Tools (Symbol)](../content/media/dv3wbia.png "dv3wbia")|Gibt an, ob eine Datenspalte im Resultset der Abfrage enthalten ist oder nicht (SELECT-Abfrage) oder ob sie in einer UPDATE-, INSERT FROM-, MAKE TABLE- oder INSERT INTO-Abfrage verwendet wird. Wählen Sie die Spalte aus, um sie in die Ergebnisse aufzunehmen. Wenn **(alle Spalten)** ausgewählt ist, wird in der Ausgabe alle Datenspalten angezeigt.<br /><br />Das mit dem Kontrollkästchen verwendete Symbol ändert sich entsprechend dem Typ der erstellten Abfrage. Beim Erstellen einer DELETE-Abfrage können Sie keine einzelnen Spalten auswählen.|  
|![Visual Database Tools (Symbol)](../content/media/dv3wbib.png "dv3wbib")<br /><br />![Visual Database Tools (Symbol)](../content/media/dv3wbic.png "dv3wbic")|Zeigt an, dass die Datenspalte zum Sortieren der Abfrageergebnisse verwendet wird (d. h. Teil einer ORDER BY-Klausel ist). Das Symbol wird als ein\-Z, wenn die Sortierreihenfolge aufsteigend ist oder Z\-A bei absteigender Sortierreihenfolge dargestellt.|  
|![Visual Database Tools (Symbol)](../content/media/dv3wbid.png "dv3wbid")|Zeigt an, dass die Datenspalte in einer Aggregatabfrage zum Erstellen eines gruppierten Resultsets verwendet wird (d. h. Teil einer GROUP BY-Klausel ist).|  
|![Visual Database Tools (Symbol)](../content/media/dv3wbie.png "dv3wbie")|Zeigt an, dass die Datenspalte in eine Suchbedingung der Abfrage eingebunden ist (d. h. Teil einer WHERE- oder HAVING-Klausel ist).|  
|![Visual Database Tools (Symbol)](../content/media/dv3wbif.png "dv3wbif")|Zeigt an, dass die Inhalte der Datenspalte für die Ausgabe zusammengefasst werden (d. h. in eine SUM- oder AVG- oder eine andere Aggregatfunktion eingebunden sind).|  
  
> [!NOTE]  
> Abfrage- und Sicht-Designer zeigt keine Datenspalten für eine Tabelle oder eine Tabelle\-bewertet-Objekt, wenn Sie keinen erforderlichen Zugriffsrechte verfügen oder der ODBC-Treiber Informationen zurückgeben kann. In solchen Fällen zeigt der Abfrage- und Ansicht-Designer nur die Titelleiste für die Tabelle oder die Tabelle\-strukturiertes Objekt.  
  
## Verknüpfte Tabellen im Diagrammbereich  
Wenn die Abfrage einen Join enthält, wird eine Joinlinie zwischen den verknüpften Datenspalten angezeigt. Wenn die verknüpften Datenspalten nicht angezeigt werden (z. B. der Tabelle oder\-bewertet Fenster minimiert ist oder die Verknüpfung einen Ausdruck beinhaltet), der Abfrage- und Ansicht-Designer setzt die Joinlinie in die Titelleiste des Rechtecks, das für die Tabelle oder die Tabelle\-bewertet Objekt. Der Abfrage- und Sicht-Designer zeigt eine Joinlinie für jede Joinbedingung an.  
  
Die Form des Symbols in der Mitte der Joinlinie zeigt an, wie Tabellen bzw.\-strukturierter Objekte verknüpft werden. Die Join-Klausel einer anderen als gleich verwendet (\=), wird der Operator im Symbol Joinlinie angezeigt. In der folgenden Tabelle werden die in Joinlinien verwendeten Symbole aufgelistet.  
  
|Joinliniensymbol|Beschreibung|  
|------------------|---------------|  
|![Visual Database Tools (Symbol)](../content/media/dv3wbih.png "dv3wbih")|Innerer Join (erstellt mit einem Gleichheitszeichen).|  
|![Visual Database Tools (Symbol)](../content/media/dv3wbii.png "dv3wbii")|Innerer Join mit dem Operator "größer als". (Der im Symbol der Joinlinie angezeigte Operator gibt den im Join verwendeten Operator wieder.)|  
|![Visual Database Tools (Symbol)](../content/media/dv3wbij.png "dv3wbij")|Äußerer Join, bei dem sämtliche Zeilen aus der links angezeigten Tabelle aufgenommen werden, auch wenn keine Übereinstimmungen in der verknüpften Tabelle vorliegen.|  
|![Visual Database Tools (Symbol)](../content/media/dv3wbik.png "dv3wbik")|Äußerer Join, bei dem sämtliche Zeilen aus der rechts angezeigten Tabelle aufgenommen werden, auch wenn keine Übereinstimmungen in der verknüpften Tabelle vorliegen.|  
|![Visual Database Tools (Symbol)](../content/media/dv3wbil.png "dv3wbil")|Ein vollständiger äußerer Join, bei dem alle Zeilen aus beiden Tabellen aufgenommen werden, auch wenn keine Übereinstimmungen in der verknüpften Tabelle vorliegen.|  
  
Symbole an den Enden der Joinlinie zeigen den Jointyp an. In der folgenden Tabelle werden die Jointypen und die an den Enden der Joinlinien verwendeten Symbole aufgelistet.  
  
|Symbole an den Enden der Joinlinien|Beschreibung|  
|-----------------------------|---------------|  
|![Visual Database Tools (Symbol)](../content/media/dv3wbim.png "dv3wbim")|Eine\-zum\-eine Verknüpfung|  
|![Visual Database Tools (Symbol)](../content/media/dv3wbin.png "dv3wbin")|Eine\-auf\-viele Join|  
|![Visual Database Tools (Symbol)](../content/media/dv3wbio.png "dv3wbio")|Der Abfrage- und Sicht-Designer konnte den Jointyp nicht ermitteln.|  
  
## Siehe auch  
[Entwerfen von Abfragen und Sichten Gewusst-wie-Themen & #40; Visual Database Tools & #41;](../content/Design-Queries-and-Views-How-to-Topics--Visual-Database-Tools-.md)  
[Im Kriterienbereich & #40; Visual Database Tools & #41;](../content/Criteria-Pane--Visual-Database-Tools-.md)  
[Sortieren und Gruppieren von Abfrageergebnissen & #40; Visual Database Tools & #41;](../content/Sort-and-Group-Query-Results--Visual-Database-Tools-.md)  
  
