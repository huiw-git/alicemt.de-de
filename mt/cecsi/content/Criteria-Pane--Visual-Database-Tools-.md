---
title: "Kriterienbereich (Visual Database Tools)"
ms.custom: na
ms.date: 07/27/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - tools-ssms
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 6291affe-580e-482f-a7ff-45ce3837956a
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
# Kriterienbereich (Visual Database Tools)
Im Kriterienbereich können Sie Abfrageoptionen festlegen, z. B. welche Datenspalten angezeigt, wie die Ergebnisse sortiert und welche Zeilen ausgewählt – durch Eingabe Ihrer Auswahl in eine Kalkulationstabelle\-wie Raster. Im Kriterienbereich können Sie Folgendes angeben:  
  
-   die anzuzeigenden Spalten sowie Aliase für Spaltennamen  
  
-   die Tabelle, zu der eine Spalte gehört  
  
-   Ausdrücke für berechnete Spalten  
  
-   die Sortierreihenfolge für die Abfrage  
  
-   Suchbedingungen  
  
-   Gruppierungskriterien für Zusammenfassungsberichte, einschließlich Aggregatfunktionen  
  
-   Neue Werte für UPDATE- oder INSERT INTO-Abfragen  
  
-   Zielspaltennamen für INSERT FROM-Abfragen  
  
Änderungen im Kriterienbereich werden automatisch im Diagrammbereich und im SQL-Bereich wiedergegeben. Entsprechend wird auch der Kriterienbereich automatisch aktualisiert, wenn Sie Änderungen in den anderen Bereichen vornehmen.  
  
## Informationen über den Kriterienbereich  
Die Zeilen im Kriterienbereich zeigen die Datenspalten an, die in der Abfrage verwendet werden. Die Spalten im Kriterienbereich geben die Abfrageoptionen wieder.  
  
Welche Informationen genau im Kriterienbereich angezeigt werden, ist abhängig vom Typ der erstellten Abfrage.  
  
Wenn im Kriterienbereich nicht sichtbar ist, mit der rechten Maustaste\-Klicken Sie auf den Designer, zeigen Sie auf **Bereich**, und klicken Sie dann auf **Kriterien**.  
  
## Optionen  
  
|**Column**|**Abfragetyp**|**Beschreibung**|  
|--------------|------------------|-------------------|  
|Column|Alle|Zeigt entweder den Namen einer in der Abfrage verwendeten Datenspalte oder den Ausdruck für eine berechnete Spalte an. Diese Spalte ist gesperrt und bleibt somit bei einem horizontalen Bildlauf immer sichtbar.|  
|Alias|SELECT, INSERT FROM, UPDATE, MAKE TABLE|Gibt entweder einen alternativen Namen für eine Spalte an oder den Namen, den Sie für eine berechnete Spalte verwenden können.|  
|Tabelle|SELECT, INSERT FROM, UPDATE, MAKE TABLE|Gibt den Namen der Tabelle oder\-strukturiertes Objekt für die zugeordnete Datenspalte. Diese Spalte ist bei berechneten Spalten leer.|  
|Ausgabe|SELECT, INSERT FROM, MAKE TABLE|Gibt an, ob eine Datenspalte in der Abfrageausgabe aufgeführt wird oder nicht.<br /><br />Hinweis: Wenn die Datenbank zulässig ist, eine Datenspalte für Sortier- oder Suchklauseln können Sie ohne sie im Resultset anzuzeigen.|  
|Sortiertyp|SELECT, INSERT FROM|Gibt an, dass die zugeordnete Datenspalte zum Sortieren der Abfrageergebnisse verwendet wird. Zeigt außerdem an, ob aufsteigend oder absteigend sortiert wird.|  
|Sortierreihenfolge|SELECT, INSERT FROM|Gibt die Sortierpriorität für Datenspalten an, die zum Sortieren des Resultsets verwendet werden. Wenn Sie die Sortierreihenfolge für eine Datenspalte ändern, wird die Sortierreihenfolge für alle anderen Spalten entsprechend aktualisiert.|  
|Gruppieren nach|SELECT, INSERT FROM, MAKE TABLE|Gibt an, dass die zugeordnete Datenspalte zum Erstellen einer Aggregatabfrage verwendet wird. Diese Datenblattspalte wird nur, wenn Sie ausgewählt haben **Group By** aus der **Tools** Menü oder SQL-Bereich eine GROUP BY-Klausel hinzugefügt haben.<br /><br />Standardmäßig ist der Wert dieser Spalte auf festgelegt **Group By**, und die Spalte ist Teil der GROUP BY-Klausel.<br /><br />Wenn Sie in eine Zelle in dieser Spalte wechseln und eine Aggregatfunktion auf die zugeordnete Datenspalte anwenden, wird für den sich ergebenden Ausdruck eine Ausgabespalte zum Resultset hinzugefügt.|  
|Kriterien|Alle|Gibt eine Suchbedingung (Filter) für die zugeordnete Datenspalte an. Geben Sie einen Operator (der Standardwert ist "\=") und die zu suchende Wert. Setzen Sie Textwerte in einfache Anführungszeichen.<br /><br />Wenn die zugeordnete Datenspalte Teil einer GROUP BY-Klausel ist, wird der von Ihnen eingegebene Ausdruck für eine HAVING-Klausel verwendet.<br /><br />Bei der Eingabe von Werten für mehr als eine Zelle in der **Kriterien** Spalte, die sich ergebende Suche Startbedingungen automatisch durch ein logisches AND verknüpft sind<br /><br />An mehrere Ausdrücke für suchbedingungen für eine einzelne Datenbankspalte, z. B. (Fname > 'A') AND (Fname < bin "), fügen Sie die Datenspalte zweimal im Kriterienbereich, und geben Sie unterschiedliche Werte in die **Kriterien** Spalte für jede Instanz der Datenspalte.|  
|Oder|Alle|Gibt einen zusätzlichen Ausdruck für eine Suchbedingung für die Datenspalte an, der mit vorherigen Ausdrücken durch ein logisches OR verknüpft wird. Sie können weitere hinzufügen **oder** Rasterspalten durch Drücken der TAB-Taste in der rechten **oder** Spalte.|  
|Anfügen|INSERT FROM|Gibt den Namen der Zieldatenspalte für die zugeordnete Datenspalte an. Wenn Sie eine INSERT FROM-Abfrage erstellen, versucht der Abfrage- und Sicht-Designer, die Quelle einer übereinstimmenden Zieldatenspalte zuzuordnen. Wenn der Abfrage- und Sicht-Designer keine Übereinstimmung finden kann, müssen Sie den Spaltennamen angeben.|  
|Neuer Wert|UPDATE, INSERT INTO|Gibt den Wert an, der in der zugeordneten Spalte gesetzt werden soll. Geben Sie einen Literalwert oder einen Ausdruck ein.|  
  
## Siehe auch  
[Entwerfen von Abfragen und Sichten Gewusst-wie-Themen & #40; Visual Database Tools & #41;](../content/Design-Queries-and-Views-How-to-Topics--Visual-Database-Tools-.md)  
[Diagrammbereich & #40; Visual Database Tools & #41;](../content/Diagram-Pane--Visual-Database-Tools-.md)  
[Regeln für das Eingeben von Suchwerten & #40; Visual Database Tools & #41;](../content/Rules-for-Entering-Search-Values--Visual-Database-Tools-.md)  
[Sortieren und Gruppieren von Abfrageergebnissen & #40; Visual Database Tools & #41;](../content/Sort-and-Group-Query-Results--Visual-Database-Tools-.md)  
[Ergebnisbereich & #40; Visual Database Tools & #41;](../content/Results-Pane--Visual-Database-Tools-.md)  
[SQL-Bereich & #40; Visual Database Tools & #41;](../content/SQL-Pane--Visual-Database-Tools-.md)  
  
