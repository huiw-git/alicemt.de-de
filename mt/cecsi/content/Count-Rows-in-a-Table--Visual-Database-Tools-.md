---
title: "Z&#228;hlen der Zeilen in einer Tabelle (Visual Database Tools)"
ms.custom: na
ms.date: 07/27/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - tools-ssms
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: dda4296a-1d16-4e77-8d6f-e295f6dd4e87
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
# Z&#228;hlen der Zeilen in einer Tabelle (Visual Database Tools)
Mit dem Zählen der Zeilen in einer Tabelle können folgende Werte bestimmt werden:  
  
-   Die Gesamtanzahl von Zeilen in einer Tabelle, beispielsweise die Anzahl von allen Büchern in einer `titles`-Tabelle  
  
-   Die Anzahl von Zeilen in einer Tabelle, die eine bestimmte Bedingung erfüllen, beispielsweise die Anzahl von Büchern eines Herausgebers in einer Tabelle `titles`  
  
-   Die Anzahl von Werten in einer bestimmten Spalte  
  
Beim Zählen der Werte in einer Spalte werden NULL-Werte nicht berücksichtigt. So kann z. B. in einer Tabelle `titles` die Anzahl von Büchern gezählt werden, für die in der Spalte `advance` Werte vorhanden sind. In der Standardeinstellung werden nicht nur eindeutige, sondern alle Werte berücksichtigt.  
  
Die Prozeduren für die drei Zählverfahren ähneln sich.  
  
### So zählen Sie alle Zeilen in einer Tabelle  
  
1.  Stellen Sie sicher, dass die Tabelle, die Sie zusammenfassen möchten, bereits im Diagrammbereich angezeigt wird.  
  
2.  Rechts\-Klicken Sie auf den Hintergrund des Diagrammbereichs, und wählen Sie dann **Gruppe hinzufügen nach** aus dem Kontextmenü. Die [Abfrage- und Sicht-Designer](../content/Query-and-View-Designer-Tools--Visual-Database-Tools-.md) Fügt eine **Group By** der Datenblatt im Kriterienbereich die Spalte.  
  
3.  Wählen Sie **\&#42; (Alle Spalten)** in dem Rechteck darstellt, der Tabelle oder\-bewertet Objekt.  
  
    Der Abfrage- und Ansicht-Designer fügt automatisch den Ausdruck **Anzahl** in der **Group By** Spalte im Kriterienbereich und weist einen Spaltenalias an die Spalte, die zusammengefasst werden soll. Sie können diesen automatisch generierten durch einen aussagekräftigeren Alias ersetzen. Weitere Informationen finden Sie unter [Erstellen von Spaltenaliasen & #40; Visual Database Tools & #41;](../content/Create-Column-Aliases--Visual-Database-Tools-.md).  
  
4.  Führen Sie die Abfrage aus.  
  
### So zählen Sie alle Zeilen, die eine Bedingung erfüllen  
  
1.  Stellen Sie sicher, dass die Tabelle, die Sie zusammenfassen möchten, bereits im Diagrammbereich angezeigt wird.  
  
2.  Rechts\-Klicken Sie auf den Hintergrund des Diagrammbereichs, und wählen Sie dann **Gruppe hinzufügen nach** aus dem Kontextmenü. Der Abfrage- und Ansicht-Designer fügt eine **Group By** der Datenblatt im Kriterienbereich die Spalte.  
  
3.  Wählen Sie **\&#42; (alle Spalten)** in dem Rechteck darstellt, der Tabelle oder\-strukturiertes Objekt.  
  
    Der Abfrage- und Ansicht-Designer fügt automatisch den Ausdruck **Anzahl** in der **Group By** Spalte im Kriterienbereich und weist einen Spaltenalias an die Spalte, die zusammengefasst werden soll. Zum Erstellen einer aussagekräftigeren Spaltenüberschrift im Abfrageergebnis finden Sie unter [Erstellen von Spaltenaliasen & #40; Visual Database Tools & #41;](../content/Create-Column-Aliases--Visual-Database-Tools-.md).  
  
4.  Fügen Sie die Datenspalte, die Sie suchen möchten, und deaktivieren Sie das Kontrollkästchen in der **Ausgabe** Spalte.  
  
    Der Abfrage- und Ansicht-Designer fügt automatisch den Ausdruck **Group By** in der **Group By** -Spalte des Rasters.  
  
5.  Änderung **Group By** in der **Group By** Spalte **in dem**.  
  
6.  In der **Filter** Spalte für die Datenspalte zu suchen, geben die Suchbedingung.  
  
7.  Führen Sie die Abfrage aus.  
  
### So zählen Sie die Werte in einer Spalte  
  
1.  Stellen Sie sicher, dass die Tabelle, die Sie zusammenfassen möchten, bereits im Diagrammbereich angezeigt wird.  
  
2.  Rechts\-Klicken Sie auf den Hintergrund des Diagrammbereichs, und wählen Sie dann **Gruppe hinzufügen nach** aus dem Kontextmenü. Der Abfrage- und Ansicht-Designer fügt eine **Group By** der Datenblatt im Kriterienbereich die Spalte.  
  
3.  Fügen Sie dem Kriterienbereich die Spalte hinzu, in der gezählt werden soll.  
  
    Der Abfrage- und Ansicht-Designer fügt automatisch den Ausdruck **Group By** in der **Group By** -Spalte des Rasters.  
  
4.  Änderung **Group By** in der **Group By** Spalte **Anzahl**.  
  
    > [!NOTE]  
    > Wenn Sie nur eindeutige Werte gezählt werden, wählen Sie **Count Distinct**.  
  
5.  Führen Sie die Abfrage aus.  
  
## Siehe auch  
[Sortieren und Gruppieren von Abfrageergebnissen & #40; Visual Database Tools & #41;](../content/Sort-and-Group-Query-Results--Visual-Database-Tools-.md)  
[Zusammenfassen von Abfrageergebnissen & #40; Visual Database Tools & #41;](../content/Summarize-Query-Results--Visual-Database-Tools-.md)  
  
