---
title: "Erstellen von Abfragen mit unbenannten Parametern (Visual Database Tools)"
ms.custom: na
ms.date: 07/27/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - tools-ssms
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 5f4b664b-3d3d-4d07-a0e7-791d78743504
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
# Erstellen von Abfragen mit unbenannten Parametern (Visual Database Tools)
Sie können eine Abfrage mit einem unbenannten Parameter erstellen, indem Sie ein Fragezeichen (?) als Platzhalter für den Literalwert angeben. Der Abfrage- und Sicht-Designer weist dann einen temporären Namen zu. In der Abfrage können beliebig viele unbenannte Parameter festgelegt werden.  
  
Wenn Sie die Abfrage im Abfrage- und Sicht-Designer ausführen, wird das Dialogfeld Abfrageparameter mit dem temporären Namen angezeigt.  
  
### So geben Sie einen unbenannten Parameter an  
  
1.  Fügen Sie die Spalten oder Ausdrücke, die Sie durchsuchen möchten die [im Kriterienbereich](../content/Criteria-Pane--Visual-Database-Tools-.md). Wenn in den Abfrageergebnissen keine Suchspalten bzw. Suchausdrücke angezeigt werden sollen, entfernen Sie die entsprechenden Ausgabespalten.  
  
2.  Suchen Sie die Zeile mit der Datenspalte oder den Ausdruck zu suchen und dann in der **Filter** Spalte des Datenblatts ein Fragezeichen (?) eingeben.  
  
    In der Standardeinstellung der Abfrage- und Ansicht-Designer fügt der "\=" Operator. Sie können die Zelle jedoch so bearbeiten, dass dafür ">", "<" oder ein beliebiger anderer SQL-Vergleichsoperator eingesetzt wird.  
  
## Siehe auch  
[Abfrage mit Parametern & #40; Visual Database Tools & #41;](../content/Query-with-Parameters--Visual-Database-Tools-.md)  
  
