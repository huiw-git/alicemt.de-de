---
title: "Erstellen von Spaltenaliasen (Visual Database Tools)"
ms.custom: na
ms.date: 07/15/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - tools-ssms
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: e2e1c166-8ea7-47a2-b6a7-e419bf0fa3bb
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
# Erstellen von Spaltenaliasen (Visual Database Tools)
Zur Arbeitserleichterung können Sie Aliase für Spaltennamen, Berechnungen und zusammengefasste Werte erstellen. Beispielsweise können Sie einen Spaltenalias mit folgenden Funktionen erstellen:  
  
-   Erstellen eines Spaltennamens, z. B. "Total Amount" für einen Ausdruck wie `(quantity * unit_price)` oder für eine Aggregatfunktion.  
  
-   Erstellen eine Kurzform für einen Spaltennamen, z. B. `"d_id"` für `"discounts.stor_id."`  
  
Wenn Sie einen Spaltenalias definiert haben, können Sie den Alias in einer SELECT-Abfrage zum Angeben der Ausgabe der Abfrageergebnisse verwenden.  
  
### So erstellen Sie einen Spaltenalias  
  
1.  In der **im Kriterienbereich**, suchen Sie die Zeile mit der Datenspalte, für die Sie einen Alias erstellen möchten, und markieren Sie es ggf. für die Ausgabe. Wenn die Datenspalte noch nicht im Datenblatt vorhanden ist, fügen Sie sie hinzu.  
  
2.  In der **Alias** Spalte für diese Zeile, geben Sie den Alias. Der Alias muss allen Namenskonventionen für SQL entsprechen. Wenn der eingegebene Aliasname Leerzeichen enthält, wird er vom Abfrage- und Sicht-Designer automatisch in Trennzeichen eingeschlossen.  
  
## Siehe auch  
[Abfragen & #40 Spalten hinzugefügt. Visual Database Tools & #41;](../content/Add-Columns-to-Queries--Visual-Database-Tools-.md)  
[Sortieren und Gruppieren von Abfrageergebnissen & #40; Visual Database Tools & #41;](../content/Sort-and-Group-Query-Results--Visual-Database-Tools-.md)  
[Zusammenfassen von Abfrageergebnissen & #40; Visual Database Tools & #41;](../content/Summarize-Query-Results--Visual-Database-Tools-.md)  
[Durchführen Sie grundlegende Operationen mit Abfragen & #40; Visual Database Tools & #41;](../content/Perform-Basic-Operations-with-Queries--Visual-Database-Tools-.md)  
  
