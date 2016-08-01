---
title: "Ergebnisbereich (Visual Database Tools)"
ms.custom: na
ms.date: 07/27/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - tools-ssms
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 6309a1bc-a628-4141-8bb5-b35924bd19f9
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
# Ergebnisbereich (Visual Database Tools)
Im Ergebnisbereich werden die Ergebnisse der zuletzt ausgeführten SELECT-Abfrage angezeigt. (Die Ergebnisse anderer Abfragetypen werden in Meldungsfeldern angezeigt.) Um den Ergebnisbereich zu öffnen, öffnen oder erstellen Sie eine Abfrage bzw. eine Sicht oder kehren zu den Daten einer Tabelle zurück. Wird der Ergebnisbereich standardmäßig nicht angezeigt, zeigen Sie im **Abfrage-Designer** auf **Bereich**, und klicken Sie dann auf **Ergebnisse**.  
  
## Mögliche Aktionen im Ergebnisbereich  
  
-   Anzeigen des Resultsets für die zuletzt ausgeführte SELECT-Abfrage in einer Kalkulationstabelle\-wie Raster.  
  
-   In Abfragen oder Sichten, die Daten aus einer einzelnen Tabelle oder Sicht anzeigen, können Sie die Werte in einzelnen Spalten im Resultset bearbeiten, neue Zeilen hinzufügen und vorhandene Zeilen löschen.  
  
## Einschränkungen im Ergebnisbereich  
  
-   Zurückgegebene Tabelle Ergebnisse\-Tabellenwertfunktionen können nur in einigen Fällen aktualisiert werden.  
  
-   Abfragen oder Sichten, die Spalten von mehr als einer Tabelle oder Sicht beinhalten, können nicht aktualisiert werden.  
  
-   Von einer gespeicherten Prozedur zurückgegebene Ergebnisse können nicht aktualisiert werden.  
  
-   Abfragen oder Sichten, die GROUP BY-Klauseln oder DISTINCT-Klauseln enthalten, sind nicht aktualisierbar.  
  
## Navigieren im Ergebnisbereich  
Verwenden Sie die Navigationsleiste am unteren Rand des Ergebnisbereichs, um schnell durch die Datensätze zu navigieren.  
  
Die Navigationsleiste ist mit Schaltflächen versehen, um zu den ersten und letzten Datensatz zu gehen, den nächsten und vorhergehenden Datensatz, und zu einem bestimmten Datensatz.  
  
Um zu einem bestimmten Datensatz zu gelangen, geben Sie die Zahl der Zeile in das Textfeld der Navigationsleiste ein, und drücken Sie die EINGABETASTE.  
  
Weitere Informationen zum Verwenden von Tastenkombinationen im Abfrage- und Ansicht-Designer finden Sie unter [Navigieren in der Abfrage und Sicht-Designer & #40; Visual Database Tools & #41;](../content/Navigate-in-the-Query-and-View-Designer--Visual-Database-Tools-.md).  
  
## Synchronhalten des Resultsets mit der Abfragedefinition  
Während Sie mit den Ergebnissen einer Abfrage oder Sicht arbeiten, ist es möglich, dass die Datensätze im Ergebnisbereich nicht mehr mit der Abfragedefinition synchron sind. Wenn Sie z. B. eine Abfrage für vier von fünf Spalten einer Tabelle ausführen und dann den Diagrammbereich verwenden, um die fünfte Spalte zur Abfragedefinition hinzuzufügen, werden die Daten der fünften Spalte nicht automatisch dem Ergebnisbereich hinzugefügt. Führen Sie die Abfrage erneut aus, damit der Ergebnisbereich die neue Abfragedefinition wiedergibt.  
  
Wenn eine Abfrage geändert wird, ein Warnsymbol und der Text "Abfrage geändert" wird angezeigt, in der unteren\-rechts im Ergebnisbereich. Das Symbol wird in der oberen wiederholt\-linken Ecke des Bereichs.  
  
## Siehe auch  
[Erstellen Sie Abfragen & #40; Visual Database Tools & #41;](../content/Create-Queries--Visual-Database-Tools-.md)  
[Ausführen von Abfragen & #40; Visual Database Tools & #41;](../content/Run-Queries--Visual-Database-Tools-.md)  
[Entwerfen von Abfragen und Sichten Gewusst-wie-Themen & #40; Visual Database Tools & #41;](../content/Design-Queries-and-Views-How-to-Topics--Visual-Database-Tools-.md)  
[Diagrammbereich & #40; Visual Database Tools & #41;](../content/Diagram-Pane--Visual-Database-Tools-.md)  
[Im Kriterienbereich & #40; Visual Database Tools & #41;](../content/Criteria-Pane--Visual-Database-Tools-.md)  
[Arbeiten Sie mit Daten im Ergebnisbereich & #40. Visual Database Tools & #41;](../content/Work-with-Data-in-the-Results-Pane--Visual-Database-Tools-.md)  
  
