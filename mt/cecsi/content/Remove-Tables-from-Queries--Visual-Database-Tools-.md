---
title: "Entfernen von Tabellen aus Abfragen (Visual Database Tools)"
ms.custom: na
ms.date: 07/27/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - tools-ssms
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 8fea0b4f-99b7-4050-8d6f-a97ffb839619
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
# Entfernen von Tabellen aus Abfragen (Visual Database Tools)
Sie können eine Tabelle entfernen – oder eine Tabelle\-bewertet Objekt – aus der Abfrage.  
  
> [!NOTE]  
> Entfernen einer Tabelle oder Tabellen\-bewertet Objekt werden nicht alle aus der Datenbank gelöscht; nur aus der aktuellen Abfrage entfernt. Weitere Informationen zum Entfernen einer Tabelle aus einer Datenbank finden Sie unter [Gewusst wie: Löschen von Tabellen aus einer Datenbank (Visual Database Tools)](assetId:///ca6aa3e9-9885-44c3-bafc-aec441fd97ec).  
  
### So entfernen Sie eine Tabelle oder eine Tabelle\-strukturiertes Objekt  
  
-   In der **Diagrammbereich**, wählen Sie die Tabelle, Sicht, Benutzer\-definierte Funktion, das Synonym oder Abfrage, und drücken Sie ENTF, oder rechts\-Klicken Sie auf das Objekt, und wählen Sie dann **Entfernen** in dem daraufhin angezeigten Dialogfeld. Sie können mehrere Objekte auswählen und gleichzeitig entfernen.  
  
    – Oder –  
  
-   Entfernen Sie alle Verweise auf das Objekt in der **SQL-Bereich.**  
  
Wenn Sie einer Tabelle oder Tabellen entfernen\-bewertet Objekt der Abfrage- und Ansicht-Designer entfernt automatisch Verknüpfungen, die diese Tabelle oder die Tabelle umfassen\-Werten Objekt auf und entfernt Verweise auf die Spalten des Objekts in der **SQL-Bereich** und **im Kriterienbereich**. Wenn die Abfrage jedoch komplexe, auf das Objekt bezogene Ausdrücke enthält, wird das Objekt erst nach dem Entfernen aller zugehörigen Verweise entfernt.  
  
## Siehe auch  
[Hinzufügen von Tabellen zu Abfragen &#40; Visual Database Tools &#41;](../content/Add-Tables-to-Queries--Visual-Database-Tools-.md)  
[Erstellen von Tabellenaliasen &#40. Visual Database Tools &#41;](../content/Create-Table-Aliases--Visual-Database-Tools-.md)  
[Geben Sie Suchkriterien &#40. Visual Database Tools &#41;](../content/Specify-Search-Criteria--Visual-Database-Tools-.md)  
[Zusammenfassen von Abfrageergebnissen &#40; Visual Database Tools &#41;](../content/Summarize-Query-Results--Visual-Database-Tools-.md)  
[Durchführen Sie grundlegende Operationen mit Abfragen &#40; Visual Database Tools &#41;](../content/Perform-Basic-Operations-with-Queries--Visual-Database-Tools-.md)  
  
