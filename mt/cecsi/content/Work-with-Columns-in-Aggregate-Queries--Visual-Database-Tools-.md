---
title: "Verwenden von Spalten in Aggregatabfragen (Visual Database Tools)"
ms.custom: na
ms.date: 07/27/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - tools-ssms
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 1b82681f-3d4f-4b9a-bb1d-2060e44f2577
caps.latest.revision: 3
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
# Verwenden von Spalten in Aggregatabfragen (Visual Database Tools)
Wenn Sie Aggregatabfragen erstellen die [Abfrage- und Sicht-Designer](../content/Query-and-View-Designer-Tools--Visual-Database-Tools-.md) von bestimmten Annahmen, damit eine gültige Abfrage konstruiert werden kann. Wenn Sie z. B. eine Aggregatabfrage erstellen und eine Datenspalte für die Ausgabe kennzeichnen, nimmt der Abfrage- und Sicht-Designer die Spalte automatisch in die GROUP BY-Klausel auf und verhindert so, dass der Inhalt einer einzelnen Zeile in einer Zusammenfassung angezeigt werden kann.  
  
## Verwenden von Gruppieren nach  
Der Abfrage- und Sicht-Designer greift beim Arbeiten mit Spalten auf folgende Richtlinien zurück:  
  
-   Wenn Sie die Option Gruppieren nach auswählen oder einer Abfrage eine Aggregatfunktion hinzufügen, werden alle für die Ausgabe gekennzeichneten oder in Sortiervorgängen verwendeten Spalten automatisch in die GROUP BY-Klausel aufgenommen. Spalten werden nicht automatisch in die GROUP BY-Klausel aufgenommen, wenn sie bereits Teil einer Aggregatfunktion sind.  
  
    Wenn Sie eine bestimmte Spalte aus der GROUP BY-Klausel herausnehmen möchten, müssen Sie im Kriterienbereich in der Spalte Gruppieren nach manuell eine andere Option auswählen. Der Abfrage- und Sicht-Designer prüft hierbei jedoch nicht, ob die Abfrage mit der von Ihnen ausgewählten Option nach wie vor ausgeführt werden kann.  
  
-   Wenn Sie einer Aggregatfunktion im Kriterien- oder SQL-Bereich manuell eine Ausgabespalte für die Abfrage hinzufügen, entfernt der Abfrage- und Sicht-Designer andere Ausgabespalten nicht automatisch aus der Abfrage. Sie müssen die verbleibenden Spalten daher manuell aus der Abfrageausgabe entfernen oder sie in die GROUP BY-Klausel einer Aggregatfunktion aufnehmen.  
  
Wenn Sie eine Suchbedingung im Kriterienbereich in die Spalte Filter eingeben, folgt der Abfrage- und Sicht-Designer bestimmten Regeln:  
  
-   Wenn der **Group By** -Spalte des Rasters (da Sie noch nicht mit eine Aggregatabfrage angegeben haben) nicht angezeigt wird, wird die Suchbedingung in der WHERE-Klausel platziert.  
  
-   Wenn Sie bereits in einer Aggregatabfrage und ausgewählt haben, **** in der **Group By** Spalte die Bedingung in der WHERE-Klausel platziert.  
  
-   Wenn der **Group By** Spalte enthält einen beliebigen Wert außer ****, wird die Suchbedingung in der HAVING-Klausel platziert.  
  
## Verwenden der HAVING- und WHERE-Klauseln  
Die folgenden Prinzipien beschreiben, wie Sie in einer Aggregatabfrage beim Festlegen von Suchbedingungen auf Spalten verweisen können. Im Allgemeinen können Sie eine Spalte in einer Suchbedingung verwenden, um die zusammengefassten Zeilen zu filtern (WHERE-Klausel) oder um zu bestimmen, welche gruppierten Ergebnisse in der endgültigen Ausgabe angezeigt werden sollen (HAVING-Klausel).  
  
-   Einzelne Datenspalten können entweder in der WHERE- oder in der HAVING-Klausel angegeben werden. Dies hängt davon ab, wie die Spalten an anderer Stelle in der Abfrage verwendet wurden.  
  
-   WHERE-Klauseln dienen zum Auswählen einer Teilmenge der Zeilen für die Zusammenfassung und Gruppierung. Sie werden daher angewendet, bevor Gruppierungsvorgänge ausgeführt werden. Aus diesem Grund können Sie eine Datenspalte auch dann in einer WHERE-Klausel verwenden, wenn sie nicht in der GROUP BY-Klausel oder in einer Aggregatfunktion enthalten ist. Beispielsweise gibt die folgende Anweisung alle Titel mit einem Preis über $10,00 zurück und berechnet den Durchschnittspreis:  
  
    ```  
    SELECT AVG(price)  
    FROM titles  
    WHERE price > 10  
    ```  
  
-   Wenn Sie beim Erstellen einer Suchbedingung eine Spalte verwenden, die ebenfalls Bestandteil einer GROUP BY-Klausel oder Aggregatfunktion ist, kann die Suchbedingung entweder als WHERE- oder als HAVING-Klausel eingebunden werden. Sie können dies entscheiden, sobald Sie die Bedingung erstellen. Die folgende Anweisung erstellt z. B. einen Durchschnittspreis aller Bücher für jeden Herausgeber und zeigt anschließend den Mittelwert derjenigen Herausgeber an, bei denen der Durchschnittspreis über 10,00 $ liegt:  
  
    ```  
    SELECT pub_id, AVG(price)  
    FROM titles  
    GROUP BY pub_id  
    HAVING (AVG(price) > 10)  
    ```  
  
-   Wenn Sie eine Aggregatfunktion in einer Suchbedingung verwenden, beinhaltet die Bedingung eine Zusammenfassung und muss somit Teil der HAVING-Klausel sein.  
  
## Siehe auch  
[Zusammenfassen von Abfrageergebnissen & #40; Visual Database Tools & #41;](../content/Summarize-Query-Results--Visual-Database-Tools-.md)  
[Sortieren und Gruppieren von Abfrageergebnissen & #40; Visual Database Tools & #41;](../content/Sort-and-Group-Query-Results--Visual-Database-Tools-.md)  
  
