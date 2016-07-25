---
title: "L&#246;schen von Abfragen (Visual Database Tools)"
ms.custom: na
ms.date: 07/15/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - tools-ssms
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 0db3af43-1ec4-48c8-b769-2bb9c76d3434
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
# L&#246;schen von Abfragen (Visual Database Tools)
Sie können alle Zeilen in einer Tabelle löschen, indem Sie eine Löschabfrage verwenden.  
  
> [!NOTE]  
> Wenn Sie alle Zeilen in einer Tabelle löschen, werden zwar die enthaltenen Daten, jedoch nicht die Tabelle selbst gelöscht. Um eine Tabelle aus einer Datenbank zu löschen, mit der rechten Maustaste\-Klicken Sie auf die Tabelle im Objekt-Explorer, und klicken Sie auf **Löschen**.  
  
Wenn Sie eine Löschabfrage erstellen, ändert sich der Kriterienbereich entsprechend und zeigt die verfügbaren Optionen zum Löschen von Zeilen an. Da in einer Löschabfrage keine Daten angezeigt werden, sind die Spalten "Ausgabe", "Sortieren nach" und "Sortierreihenfolge" ausgeblendet. Darüber hinaus benennt die Kontrollkästchen neben der Spalte in dem Rechteck darstellt, der Tabelle oder\-bewertet Objekt werden entfernt, da keine einzelne Spalten zum Löschen angegeben werden können.  
  
Falls der Abfrage- und Sicht-Designer eine oder mehrere der Zeilen nicht löschen kann, werden keine Zeilen gelöscht. Eine Meldung gibt an, welche Zeilen Informationen enthalten, die nicht aus der Datenbank gelöscht werden können.  
  
> [!CAUTION]  
> Eine ausgeführte Löschabfrage kann nicht mehr rückgängig gemacht werden. Erstellen Sie vorsichtshalber vor Ausführung der Löschabfrage eine Sicherungskopie der Daten.  
  
### So erstellen Sie eine Löschabfrage  
  
1.  Fügen Sie dem Diagrammbereich die Tabelle hinzu, aus der Zeilen gelöscht werden sollen.  
  
2.  Aus der **-Abfrage-Designer** auf **Änderungstyp**, und klicken Sie dann auf **Löschen**. **Hinweis** Wenn mehr als eine Tabelle im Diagrammbereich angezeigt wird, wenn beim Starten der Delete-Abfrage die Abfrage und Sicht-Designer zeigt die [Löschen Sie im Dialogfeld Tabelle](../content/Delete-Table-Dialog-Box--Visual-Database-Tools-.md) für den Namen des zu löschenden Zeilen aus Tabelle aufgefordert.  
  
Beim Ausführen einer Löschabfrage werden keine Ergebnisse der [im Ergebnisbereich](../content/Results-Pane--Visual-Database-Tools-.md). Stattdessen wird eine Meldung mit der Anzahl der gelöschten Zeilen angezeigt.  
  
## Siehe auch  
[Unterstützte Abfragetypen & #40; Visual Database Tools & #41;](../content/Supported-Query-Types--Visual-Database-Tools-.md)  
[Entwerfen von Abfragen und Sichten Gewusst-wie-Themen & #40; Visual Database Tools & #41;](../content/Design-Queries-and-Views-How-to-Topics--Visual-Database-Tools-.md)  
  
