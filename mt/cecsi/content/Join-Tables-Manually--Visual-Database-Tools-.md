---
title: "Manuelles Verkn&#252;pfen von Tabellen (Visual Database Tools)"
ms.custom: na
ms.date: 07/27/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - tools-ssms
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 9c785356-646b-4c87-82d4-25efd6051d9d
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
# Manuelles Verkn&#252;pfen von Tabellen (Visual Database Tools)
Wenn Sie einer Abfrage zwei (oder mehr) Tabellen hinzufügen der [Abfrage- und Sicht-Designer](../content/Query-and-View-Designer-Tools--Visual-Database-Tools-.md) versucht zu verknüpfen, basierend auf gemeinsamen Daten oder Informationen in der Datenbank wie die Tabellen verknüpft sind. Weitere Informationen finden Sie unter [& #40; Tabellen automatisch verknüpfen Visual Database Tools & #41;](../content/Join-Tables-Automatically--Visual-Database-Tools-.md). Wenn der Abfrage- und Sicht-Designer die Tabellen jedoch nicht automatisch verknüpft hat oder wenn Sie weitere Joinbedingungen zwischen Tabellen erstellen möchten, können Sie Tabellen manuell verknüpfen.  
  
Sie können Joins auf der Grundlage von Vergleichen zwischen zwei beliebigen Spalten erstellen, die aber nicht dieselben Informationen enthalten müssen. Wenn z. B. die Datenbank die zwei Tabellen `titles` und `roysched` enthält, können Sie die Werte in der Spalte `ytd_sales` der Tabelle `titles` mit den Spalten `lorange` und `hirange` in der Tabelle `roysched` vergleichen. Das Erstellen dieses Joins ermöglicht Ihnen die Titel für das Suchen im Jahr\-zu\-Datum sales liegt zwischen dem niedrigen und hohen Bereiche der tantiemenzahlungen liegen.  
  
> [!TIP]  
> Joins funktionieren am schnellsten, wenn die Spalten in der Joinbedingung indiziert sind. In einigen Fällen kann der Join über nicht indizierte Spalten zu einer langsamen Abfrage führen.  
  
### So verknüpfen Tabellen oder manuell\-Objekte mit Tabellenstruktur  
  
1.  Hinzufügen der [Diagrammbereich](../content/Diagram-Pane--Visual-Database-Tools-.md) die Objekte, die Sie hinzufügen möchten.  
  
2.  Ziehen Sie den Namen der Joinspalte in der ersten Tabelle oder\-strukturierten Objekt, und legen Sie sie auf der entsprechenden Spalte in der zweiten Tabelle oder\-strukturiertes Objekt. Einen Join kann nicht auf Grundlage **Text**, **Ntext**, oder ich**Mage** Spalten.  
  
    > [!NOTE]  
    > Die Joinspalten müssen denselben (oder einen kompatiblen) Datentyp aufweisen. Wenn z. B. die Joinspalte in der ersten Tabelle eine Datenspalte ist, müssen Sie diese mit einer Datenspalte in der zweiten Tabelle verknüpfen. Wenn es sich jedoch bei der ersten Joinspalte um eine Integer-Spalte handelt, muss die zu verknüpfende Spalte ebenfalls vom Integer-Datentyp sein, kann jedoch eine andere Größe aufweisen. Der Abfrage- und Sicht-Designer überprüft die Datentypen der für einen Join verwendeten Spalten nicht. Wenn Sie jedoch die Abfrage ausführen, zeigt die Datenbank bei nicht kompatiblen Datentypen einen Fehler an.  
  
3.  Ändern Sie ggf. den Join-Operator; Standardmäßig ist der Operator ein Gleichheitszeichen (\=). Weitere Informationen finden Sie unter [Ändern von Verknüpfungsoperatoren & #40; Visual Database Tools & #41;](../content/Modify-Join-Operators--Visual-Database-Tools-.md).  
  
Der Abfrage- und Ansicht-Designer fügt eine INNER JOIN-Klausel der SQL-Anweisung in der [SQL-Bereich](../content/SQL-Pane--Visual-Database-Tools-.md). Sie können den Typ in einen äußeren Join ändern. Weitere Informationen finden Sie [Create Outer Joins & #40; Visual Database Tools & #41;](../content/Create-Outer-Joins--Visual-Database-Tools-.md).  
  
## Siehe auch  
[Abfragen mit Joins & #40; Visual Database Tools & #41;](../content/Query-with-Joins--Visual-Database-Tools-.md)  
  
