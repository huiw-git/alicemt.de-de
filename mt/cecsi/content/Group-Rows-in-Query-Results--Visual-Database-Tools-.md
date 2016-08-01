---
title: "Gruppieren von Zeilen in Abfrageergebnissen (Visual Database Tools)"
ms.custom: na
ms.date: 07/27/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - tools-ssms
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: b07082d5-4d55-4903-9af9-4c470554c6d3
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
# Gruppieren von Zeilen in Abfrageergebnissen (Visual Database Tools)
Zum Bilden von Teilergebnissen oder zum Anzeigen weiterer Kurzinformationen für Teilbereiche einer Tabelle erstellen Sie Gruppen mithilfe einer Aggregatabfrage. In jeder Gruppe werden die Daten aus allen Zeilen der Tabelle mit demselben Wert zusammengefasst.  
  
Angenommen, Sie möchten den durchschnittlichen Preis für ein Buch in der Tabelle `titles` anzeigen lassen, wobei die Ergebnisse nach Herausgeber aufgeteilt werden sollen. Dazu gruppieren Sie die Abfrage nach Herausgeber (z. B. `pub_id`). Hierfür kann folgende Abfrageausgabe formuliert werden:  
  
![Abfrageergebnisse: Durchschnittspreis gruppiert nach Verleger](../content/media/dv3w9e1.png "dv3w9e1")  
  
Beim Gruppieren von Daten können nur Daten aus Zusammenfassungen bzw. gruppierte Daten angezeigt werden, z. B.:  
  
-   Die Werte der gruppierten Spalten (die in der GROUP BY-Klausel auftreten). Im oben angeführten Beispiel ist `pub_id` die gruppierte Spalte.  
  
-   Werte, die von Aggregatfunktionen wie SUM und AVG () erzeugt werden. Im obigen Beispiel, die zweite Spalte erstellt, indem der AVG-Funktion mit der `price` Spalte.  
  
Werte aus einzelnen Zeilen können nicht angezeigt werden. Wenn Sie z. B. nur nach Herausgeber gruppieren, können nicht gleichzeitig die einzelnen Titel in der Abfrage angezeigt werden. Daher, wenn Sie die Ausgabe der Abfrage Spalten hinzufügen der [Abfrage- und Sicht-Designer](../content/Query-and-View-Designer-Tools--Visual-Database-Tools-.md) fügt diese automatisch der GROUP BY-Klausel der Anweisung in der [SQL-Bereich](../content/SQL-Pane--Visual-Database-Tools-.md). Wenn eine Spalte stattdessen aggregiert werden soll, können Sie für diese Spalte eine Aggregatfunktion angeben.  
  
Wenn Sie nach mehreren Spalten gruppieren, werden von jeder Gruppe der Abfrage die Aggregatwerte für alle Gruppenspalten angezeigt.  
  
In der folgenden Abfrage für die Tabelle `titles` sind die Zeilen beispielsweise sowohl nach Herausgeber (`pub_id`) als auch nach Buchtyp (`type`) gruppiert. Die Abfrageergebnisse sind nach Herausgeber geordnet und zeigen für jeden Buchtyp des jeweiligen Herausgebers Kurzinformationen an:  
  
```  
SELECT pub_id, type, SUM(price) Total_price  
FROM titles  
GROUP BY pub_id, type  
```  
  
Die entsprechende Ausgabe könnte folgendermaßen aussehen:  
  
![Abfrageergebnisse: Preis gruppiert nach Verleger und Typ](../content/media/dv3w9e2.png "dv3w9e2")  
  
### So gruppieren Sie Zeilen  
  
1.  Starten Sie die Abfrage, indem Sie dem Diagrammbereich die Tabellen hinzufügen, die zusammengefasst werden sollen.  
  
2.  Rechts\-Klicken Sie auf den Hintergrund des Diagrammbereichs, und wählen Sie dann **Gruppe hinzufügen nach** aus dem Kontextmenü. Der Abfrage- und Ansicht-Designer fügt eine **Group By** der Datenblatt im Kriterienbereich die Spalte.  
  
3.  Fügen Sie dem Kriterienbereich die Spalte(n) hinzu, die gruppiert werden soll(en). Wenn Sie die Spalte in der Abfrageausgabe angezeigt werden soll, stellen sicher, dass die **Ausgabe** Spalte für die Ausgabe ausgewählt ist.  
  
    Der Abfrage- und Sicht-Designer fügt der Anweisung im SQL-Bereich eine GROUP BY-Klausel hinzu. Die SQL-Anweisung könnte z. B. folgendermaßen aussehen:  
  
    ```  
    SELECT pub_id  
    FROM titles  
    GROUP BY pub_id  
    ```  
  
4.  Fügen Sie dem Kriterienbereich die Spalte(n) hinzu, die aggregiert werden soll(en). Vergewissern Sie sich, dass die Spalte für die Ausgabe ausgewählt ist.  
  
5.  In der **Group By** Rasterzelle für die Spalte, die aggregiert werden soll, wählen Sie die entsprechende Aggregatfunktion.  
  
    Der Abfrage- und Sicht-Designer weist der Spalte, die zusammengefasst wird, automatisch einen Spaltenalias zu. Sie können diesen automatisch generierten durch einen aussagekräftigeren Alias ersetzen. Weitere Informationen finden Sie unter [Erstellen von Spaltenaliasen &#40; Visual Database Tools &#41;](../content/Create-Column-Aliases--Visual-Database-Tools-.md).  
  
    ![Hinzufügen eines Spaltenalias zum Resultset der Abfrage](../content/media/dv3w9e3.png "dv3w9e3")  
  
    Die entsprechende Anweisung in der **SQL** Bereich könnte folgendermaßen aussehen:  
  
    ```  
    SELECT   pub_id, SUM(price) AS Totalprice  
    FROM     titles  
    GROUP BY pub_id  
    ```  
  
## Siehe auch  
[Sortieren und Gruppieren von Abfrageergebnissen &#40; Visual Database Tools &#41;](../content/Sort-and-Group-Query-Results--Visual-Database-Tools-.md)  
  
