---
title: "Unterschiedliche Abfragedefinitionen (Dialogfeld) (Visual Database Tools)"
ms.custom: na
ms.date: 07/15/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - tools-ssms
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 90383473-2922-40e5-9682-3850849aa856
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
# Unterschiedliche Abfragedefinitionen (Dialogfeld) (Visual Database Tools)
In diesem Dialogfeld werden Sie darauf hingewiesen, dass die Abfrage in den Bereichen Diagramm und Kriterien grafisch nicht dargestellt und daher nur im SQL-Bereich bearbeitet werden kann.  
  
Dieses Dialogfeld wird angezeigt, wenn Sie eine SQL-Anweisung im SQL-Bereich eingeben oder bearbeiten, dann zu einem anderen Bereich wechseln, die Abfrage überprüfen oder versuchen, sie auszuführen, und gleichzeitig eine der folgenden Bedingungen zutrifft:  
  
-   Die SQL-Anweisung ist unvollständig oder enthält mindestens einen Syntaxfehler.  
  
-   Die SQL-Anweisung ist gültig, wird aber von den grafischen Bereichen nicht unterstützt (z. B. eine Union-Abfrage).  
  
-   Die SQL-Anweisung ist gültig, enthält aber Syntax, die nur für die verwendete Datenverbindung gilt.  
  
> [!TIP]  
> Sie können überprüfen, ob eine Anweisung gültig ist mit der **SQL-Anweisung überprüfen** auf die Schaltfläche der **Abfrage** Symbolleiste.  
  
Das Dialogfeld zeigt eine Meldung mit dem Hinweis an, dass die SQL-Anweisung nicht dargestellt werden kann. Geben Sie an, wie Sie weiter vorgehen möchten.  
  
> [!NOTE]  
> Die **Abfragedefinitionen** Dialogfeld wird nicht angezeigt, wenn Sie die Bereichen Diagramm und Kriterien ausgeblendet sind.  
  
## Optionen  
**Schaltfläche Ignorieren**  
Mit dieser Schaltfläche können Sie die SQL-Anweisung übernehmen, um sie weiter zu bearbeiten oder auszuführen. Wenn Sie die Anweisung übernehmen, werden die Bereiche Diagramm und Kriterien abgeblendet, um anzuzeigen, dass die Anweisung im SQL-Bereich darin nicht dargestellt wird.  
  
**Schaltfläche Rückgängig**  
Mit dieser Schaltfläche können Sie die im SQL-Bereich vorgenommenen Änderungen verwerfen.  
  
> [!NOTE]  
> Wenn die Anweisung richtig ist, aber vom Abfrage- und Sicht-Designer nicht grafisch unterstützt wird, können Sie sie ausführen, obwohl sie nicht in den Bereichen Diagramm und Kriterien dargestellt wird. Wenn Sie beispielsweise eine Union-Abfrage eingeben, kann die Anweisung ausgeführt, aber nicht in den anderen Bereichen dargestellt werden.  
  
## Siehe auch  
[Abfrage- und Sicht-Designer-Tools & #40; Visual Database Tools & #41;](../content/Query-and-View-Designer-Tools--Visual-Database-Tools-.md)  
  
