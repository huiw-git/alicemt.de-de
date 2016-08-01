---
title: "Unterst&#252;tzte Abfragetypen (Visual Database Tools)"
ms.custom: na
ms.date: 07/27/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - tools-ssms
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 72b9116c-c128-4078-a78d-257a2955a3f6
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
# Unterst&#252;tzte Abfragetypen (Visual Database Tools)
Sie können die folgenden Typen von Abfragen erstellen, in den Bereichen Diagramm und Kriterien (den grafischen Bereichen) des dem [Abfrage- und Sicht-Designer](../content/Query-and-View-Designer-Tools--Visual-Database-Tools-.md):  
  
-   **SELECT-Abfrage** Ruft Daten aus einer oder mehreren Tabellen oder Sichten ab. Dieser Abfragetyp wird durch eine SELECT-Anweisung in SQL ausgedrückt.  
  
-   **Ergebnisse einfügen** erstellt neue Zeilen durch Kopieren vorhandener Zeilen aus einer Tabelle in eine andere oder in dieselbe Tabelle als neue Zeilen. Dieser Abfragetyp wird durch eine INSERT INTO...SELECT-Anweisung in SQL ausgedrückt.  
  
-   **Fügen Sie Werte** erstellt eine neue Zeile und fügt Werte in die angegebenen Spalten. Dieser Abfragetyp wird durch eine INSERT INTO...VALUES-Anweisung in SQL ausgedrückt.  
  
-   **Aktualisierungsabfrage** ändert die Werte einzelner Spalten in einer oder mehreren vorhandenen Zeilen in einer Tabelle. Dieser Abfragetyp wird durch eine UPDATE…SET-Anweisung in SQL ausgedrückt.  
  
-   **Löschabfrage** entfernt eine oder mehrere Zeilen aus einer Tabelle. Dieser Abfragetyp wird durch eine DELETE-Anweisung in SQL ausgedrückt.  
  
    > [!NOTE]  
    > Bei einer Löschabfrage werden ganze Zeilen aus der Tabelle gelöscht. Wenn Sie Werte aus einzelnen Datenspalten löschen möchten, verwenden Sie eine UPDATE-Abfrage.  
  
-   **Tabelle Abfrage** erstellt eine neue Tabelle sowie Zeilen in diese durch die Ergebnisse einer Abfrage in diese kopiert. Dieser Abfragetyp wird durch eine SELECT...INTO-Anweisung in SQL ausgedrückt.  
  
Zusätzlich zu den in den grafischen Bereichen erstellten Abfragen können Sie jede SQL-Anweisung im SQL-Bereich eingeben, z. B. UNION-Abfragen.  
  
Wenn Sie mithilfe von SQL-Anweisungen Abfragen erstellen, die nicht in den grafischen Bereichen dargestellt werden können, blendet der Abfrage- und Sicht-Designer diese Bereiche ab und zeigt damit an, dass in diesen Bereichen nicht die erstellte Abfrage wiedergegeben wird. Die abgeblendeten Bereiche bleiben allerdings aktiv, und in vielen Fällen können Sie in diesen Bereichen Änderungen an der Abfrage vornehmen. Wenn sich aus den von Ihnen vorgenommenen Änderungen eine Abfrage ergibt, die in den grafischen Bereichen dargestellt werden kann, werden die Bereiche nicht länger abgeblendet angezeigt.  
  
## Siehe auch  
[Entwerfen von Abfragen und Sichten Gewusst-wie-Themen &#40; Visual Database Tools &#41;](../content/Design-Queries-and-Views-How-to-Topics--Visual-Database-Tools-.md)  
[Typen von Abfragen &#40. Visual Database Tools &#41;](../content/Types-of-Queries--Visual-Database-Tools-.md)  
  
