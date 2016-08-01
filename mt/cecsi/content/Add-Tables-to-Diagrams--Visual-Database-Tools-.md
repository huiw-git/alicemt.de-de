---
title: "Hinzuf&#252;gen von Tabellen zu Diagrammen (Visual Database Tools)"
ms.custom: na
ms.date: 07/27/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - tools-ssms
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 5440fdf7-ac04-4325-9f32-181f4cd402e5
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
# Hinzuf&#252;gen von Tabellen zu Diagrammen (Visual Database Tools)
Sie können dem Datenbankdiagramm eine Tabelle hinzufügen, um die Diagrammstruktur zu bearbeiten oder Beziehungen zu anderen Tabellen im Diagramm zu erstellen. Sie können der Datenbank entweder bereits vorhandene Datenbanktabellen oder eine neue Tabelle hinzufügen, die noch nicht in der Datenbank definiert ist.  
  
### So fügen Sie eine neue Tabelle in ein Diagramm ein  
  
1.  Vergewissern Sie sich, dass Sie mit der Datenbank verbunden sind, in der die Tabelle erstellt werden soll.  
  
    Zum Erstellen einer Tabelle im aktuellen Diagramm klicken Sie auf der Symbolleiste auf die Schaltfläche **Neue Tabelle** .  
  
    – Oder –  
  
    Rechts\-Klicken Sie im Diagramm, und wählen **neue Tabelle**.  
  
2.  Das System übernehmen oder ändern Sie\-zugewiesenen Namen der Tabelle der **Namen auswählen** Dialogfeld ein, und wählen Sie dann **OK**.  
  
    In der Standardansicht des Diagramms wird nun eine neue Tabelle angezeigt.  
  
3.  Geben Sie in der ersten Zelle der neuen Tabelle einen Spaltennamen ein. Drücken Sie dann die TAB-TASTE, um zur nächsten Zelle zu wechseln.  
  
4.  Wählen Sie unter **Datentyp**einen Datentyp für die Spalte aus. Jeder Spalte muss ein Name und ein Datentyp zugewiesen werden.  
  
    Sie können die anderen Eigenschaften der Spalte im Tabellen-Designer festlegen.  
  
5.  Wiederholen Sie die Schritte 3 und 4 für jede Spalte, die Sie der Tabelle hinzufügen möchten.  
  
> [!NOTE]  
> Wenn Sie das Datenbankdiagramm speichern, wird die neue Tabelle der Datenbank hinzugefügt.  
  
### So fügen Sie einem Diagramm eine vorhandene Tabelle zu  
  
1.  Vergewissern Sie sich, dass Sie mit der Datenbank verbunden sind, deren Tabellen Sie bearbeiten möchten.  
  
2.  Markieren Sie eine Tabelle im Ordner **Tabellen** .  
  
3.  Ziehen Sie die Tabelle in das Datenbankdiagramm.  
  
4.  Lassen Sie die Maustaste los.  
  
> [!NOTE]  
> Wenn Beziehungen zwischen der ausgewählten Tabelle und anderen Tabellen im Diagramm bestehen, werden automatisch Beziehungslinien gezogen.  
  
### So fügen Sie einem Diagramm verknüpfte Tabellen hinzu  
  
1.  Wählen Sie eine oder mehrere Tabellen mit Fremdschlüsseleinschränkungen im Datenbankdiagramm aus.  
  
2.  Rechts\-Klicken Sie auf eine der ausgewählten Tabellen, und wählen Sie **verknüpfte Tabellen hinzufügen**.  
  
> [!NOTE]  
> Daraufhin werden dem Diagramm sowohl die Tabellen hinzugefügt, auf die die ausgewählten Tabellen mit einer Fremdschlüsseleinschränkung verweisen, als auch die Tabellen, die mit einer Fremdschlüsseleinschränkung auf die ausgewählten Tabellen verweisen.  
  
## Siehe auch  
[Arbeiten Sie mit Datenbankdiagrammen &#40. Visual Database Tools &#41;](../content/Work-with-Database-Diagrams--Visual-Database-Tools-.md)  
[Arbeiten Sie mit Tabellen im Datenbankdiagramm &#40. Visual Database Tools &#41;](../content/Work-with-Tables-in-Database-Diagram--Visual-Database-Tools-.md)  
  
