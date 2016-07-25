---
title: "SQL-Bereich (Visual Database Tools)"
ms.custom: na
ms.date: 07/15/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - tools-ssms
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: dbabab18-0614-415b-a2ef-9bcd0d320d5c
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
# SQL-Bereich (Visual Database Tools)
Sie können den SQL-Bereich verwenden, um eine eigene SQL-Anweisung zu erstellen. Sie können auch den Kriterienbereich und den Diagrammbereich verwenden, um die Anweisung zu erstellen, wobei dadurch die SQL-Anweisungen im SQL-Bereich erstellt werden. Beim Erstellen einer Abfrage wird der SQL-Bereich automatisch aktualisiert und neu formatiert, um die Lesbarkeit zu verbessern.  
  
SQL-Bereich zunächst öffnen Sie Abfrage- und Sicht-Designer (mit einem Datenbankobjekt im Server-Explorer aus der **Datenbank** Menü klicken Sie auf **neue Abfrage**). Dann von der **-Abfrage-Designer** zeigen Sie im Menü auf **Bereich** und klicken Sie auf **SQL**.  
  
Im SQL-Bereich können Sie folgende Aktionen ausführen:  
  
-   neue Abfragen durch die Eingabe von SQL-Anweisungen erstellen  
  
-   die SQL-Anweisung ändern, die vom Abfrage- und Sicht-Designer basierend auf Ihren Einstellungen im Diagrammbereich und im Kriterienbereich erstellt wurde.  
  
-   Anweisungen eingeben, die auf spezielle Funktionen der von Ihnen verwendeten Datenbank zugreifen  
  
> [!NOTE]  
> Machen Sie sich mit den Regeln vertraut, über die Datenbankobjekte in der von Ihnen verwendeten Datenbank identifiziert werden können. Ausführliche Informationen finden Sie in der Dokumentation des Datenbankverwaltungssystems.  
  
## Anweisungen im SQL-Bereich  
Sie können die aktuelle Abfrage direkt im SQL-Bereich bearbeiten. Sobald Sie in einen anderen Bereich wechseln, formatiert der Abfrage- und Sicht-Designer automatisch Ihre Anweisung und aktualisiert anschließend die Angaben im Diagrammbereich und im Kriterienbereich.  
  
Wenn der Diagramm- und der Kriterienbereich angezeigt werden und Ihre Anweisung nicht in diesen Bereichen dargestellt werden kann, meldet der Abfrage- und Sicht-Designer einen Fehler und bietet Ihnen zwei Optionen an:  
  
-   Ignorieren, dass die Anweisung nicht im Diagrammbereich und im Kriterienbereich dargestellt werden kann.  
  
-   Rückgängigmachen der nicht darstellbaren Änderung und Zurücksetzen auf die aktuellste Version der SQL-Anweisung.  
  
Wenn Sie ignorieren, dass die Anweisung nicht im Diagrammbereich und im Kriterienbereich dargestellt werden kann, werden die anderen Bereiche im Abfrage- und Sicht-Designer ausgeblendet. Damit wird angegeben, dass der Inhalt des SQL-Bereichs in diesen Bereichen nicht wiedergegeben wird.  
  
Sie können mit dem Bearbeiten der Anweisung fortfahren und diese wie jede andere SQL-Anweisung ausführen.  
  
> [!NOTE]  
> Wenn Sie eine SQL-Anweisung eingeben und anschließend weitere Änderungen an der Abfrage im Diagrammbereich bzw. Kriterienbereich vornehmen, erstellt der Abfrage- und Sicht-Designer die SQL-Anweisung neu und aktualisiert ihre Anzeige. In einigen Fällen wird hierbei eine SQL-Anweisung generiert, die in ihrer Struktur von der ursprünglich eingegebenen Anweisung abweicht (jedoch nach wie vor die gleichen Ergebnisse liefert). Diese Abweichung tritt häufig dann auf, wenn Sie Suchbedingungen verwenden, in denen mehrere Klauseln durch AND und OR verknüpft wurden.  
  
## Siehe auch  
[Erstellen Sie Abfragen & #40; Visual Database Tools & #41;](../content/Create-Queries--Visual-Database-Tools-.md)  
[Ausführen von Abfragen & #40; Visual Database Tools & #41;](../content/Run-Queries--Visual-Database-Tools-.md)  
[Entwerfen von Abfragen und Sichten Gewusst-wie-Themen & #40; Visual Database Tools & #41;](../content/Design-Queries-and-Views-How-to-Topics--Visual-Database-Tools-.md)  
[Diagrammbereich & #40; Visual Database Tools & #41;](../content/Diagram-Pane--Visual-Database-Tools-.md)  
[Im Kriterienbereich & #40; Visual Database Tools & #41;](../content/Criteria-Pane--Visual-Database-Tools-.md)  
[Ergebnisbereich & #40; Visual Database Tools & #41;](../content/Results-Pane--Visual-Database-Tools-.md)  
  
