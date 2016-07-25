---
title: "Wertzusammenfassung oder -aggregation f&#252;r alle Zeilen in einer Tabelle (Visual Database Tools)"
ms.custom: na
ms.date: 07/15/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - tools-ssms
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: f5af876e-f937-4110-ba09-07999c35a699
caps.latest.revision: 5
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
# Wertzusammenfassung oder -aggregation f&#252;r alle Zeilen in einer Tabelle (Visual Database Tools)
Mithilfe einer Aggregatfunktion können Sie eine Zusammenfassung für alle Werte in einer Tabelle erstellen. Sie können z. B. folgende Abfrage erstellen, um den Gesamtpreis aller Bücher in der Tabelle `titles` anzeigen zu lassen:  
  
```  
SELECT SUM(price)  
FROM titles  
```  
  
Sie können mehrere Aggregationen in derselben Abfrage erstellen, wenn Sie Aggregatfunktionen auf mehrere Spalten anwenden. Beispielsweise können Sie eine Abfrage erstellen, in der die Gesamtsumme der `price`-Spalte und der Durchschnittswert der `discount`-Spalte berechnet werden.  
  
Sie können jedoch auch eine einzige Spalte in derselben Abfrage auf unterschiedliche Weise aggregieren (z. B. Ausgabe der Gesamtsumme, der Anzahl und des Durchschnittswerts). In der folgenden Abfrage wird beispielsweise der Durchschnittswert und die Gesamtsumme für die `price`-Spalte in der Tabelle `titles` berechnet:  
  
```  
SELECT AVG(price), SUM(price)  
FROM titles  
```  
  
Wenn Sie eine Suchbedingung hinzufügen, können Sie die Teilmenge von Zeilen aggregieren, die die entsprechende Bedingung erfüllt.  
  
> [!NOTE]  
> Sie können außerdem alle Zeilen in der Tabelle oder nur die Zeilen zählen, die eine bestimmte Bedingung erfüllen. Weitere Informationen finden Sie unter [zählen der Zeilen in einer Tabelle & #40; Visual Database Tools & #41;](../content/Count-Rows-in-a-Table--Visual-Database-Tools-.md).  
  
Wenn Sie für alle Zeilen in einer Tabelle einen einzigen Aggregatwert erstellen, werden nur die Aggregatwerte selbst angezeigt. Wenn Sie z. B. die Gesamtsumme des Werts für die `price`-Spalte in der Tabelle `titles` berechnen, werden die einzelnen Buchtitel, Herausgebernamen usw. nicht angezeigt.  
  
> [!NOTE]  
> Wenn Sie Teilergebnisse berechnen, d. h. Gruppen erstellen, können Sie die Spaltenwerte für jede Gruppe anzeigen lassen. Weitere Informationen finden Sie unter [Gruppieren von Zeilen in Abfrageergebnissen & #40; Visual Database Tools & #41;](../content/Group-Rows-in-Query-Results--Visual-Database-Tools-.md).  
  
### So aggregieren Sie Werte für alle Zeilen  
  
1.  Stellen Sie sicher, dass die Tabelle, die Sie aggregieren möchten, bereits im Diagrammbereich angezeigt wird.  
  
2.  Rechts\-Klicken Sie auf den Hintergrund des Diagrammbereichs, und wählen Sie dann **Group By** aus dem Kontextmenü. Die [Abfrage- und Sicht-Designer](../content/Query-and-View-Designer-Tools--Visual-Database-Tools-.md) Fügt eine **Group By** der Datenblatt im Kriterienbereich die Spalte.  
  
3.  Fügen Sie dem Kriterienbereich die Spalte hinzu, die aggregiert werden soll. Vergewissern Sie sich, dass die Spalte für die Ausgabe ausgewählt ist.  
  
    Der Abfrage- und Sicht-Designer weist der Spalte, die zusammengefasst wird, automatisch einen Spaltenalias zu. Sie können diesen Alias durch einen aussagekräftigeren Alias ersetzen. Weitere Informationen finden Sie unter [Erstellen von Spaltenaliasen & #40; Visual Database Tools & #41;](../content/Create-Column-Aliases--Visual-Database-Tools-.md).  
  
4.  In der **Group By** Spalte des Datenblatts, wählen Sie die gewünschte Aggregatfunktion, z. B.: **Summe**, **Avg**, **Min**, **Max**, **Anzahl**. Wenn im Resultset nur eindeutige Zeilen aggregiert werden sollen, wählen Sie eine Aggregatfunktion mit den DISTINCT-Optionen, z. B. **Min Distinct**. Wählen Sie nicht **Group By**, **Ausdruck**, oder ****, da diese Optionen bei einer Aggregation aller Zeilen sind nicht zulässig.  
  
    Der Abfrage- und Ansicht-Designer ersetzt den Spaltennamen in der Anweisung in der [SQL-Bereich](../content/SQL-Pane--Visual-Database-Tools-.md) mit der Aggregatfunktion, die Sie angeben. Die SQL-Anweisung könnte z. B. folgendermaßen aussehen:  
  
    ```  
    SELECT SUM(price)  
    FROM titles  
    ```  
  
5.  Wenn Sie mehrere Aggregationen in der Abfrage erstellen möchten, wiederholen Sie die Schritte 3 und 4.  
  
    Wenn Sie der Abfrageergebnisliste oder der Order by-Liste eine weitere Spalte hinzufügen, der Abfrage- und Ansicht-Designer fügt automatisch den Ausdruck **Group By** in der **Group By** -Spalte des Rasters. Wählen Sie die entsprechende Aggregatfunktion aus.  
  
6.  Fügen Sie bei Bedarf Suchbedingungen hinzu, um die Teilmenge der zusammenzufassenden Zeilen anzugeben.  
  
Bei Ausführung der Abfrage werden die angegebenen Aggregationen im Ergebnisbereich angezeigt.  
  
> [!NOTE]  
> Der Abfrage- und Sicht-Designer behält die Aggregatfunktionen so lange als Bestandteil der SQL-Anweisung im SQL-Bereich bei, bis Sie den Gruppieren nach-Modus explizit ausschalten. Daher, wenn die Abfrage ändern, indem die Änderung des Typs oder Ändern der Tabellen oder Tabelle\-wichtigen Objekte im Diagrammbereich vorhanden sind, die resultierende Abfrage möglicherweise ungültige Aggregatfunktionen enthalten.  
  
## Siehe auch  
[Sortieren und Gruppieren von Abfrageergebnissen & #40; Visual Database Tools & #41;](../content/Sort-and-Group-Query-Results--Visual-Database-Tools-.md)  
[Zusammenfassen von Abfrageergebnissen & #40; Visual Database Tools & #41;](../content/Summarize-Query-Results--Visual-Database-Tools-.md)  
  
