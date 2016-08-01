---
title: "Entfernen von Joins (Visual Database Tools)"
ms.custom: na
ms.date: 07/27/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - tools-ssms
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: ccc212a1-fd13-48d6-85e5-5ff310c34bbd
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
# Entfernen von Joins (Visual Database Tools)
Wenn Tabellen nicht über einen inneren oder äußeren Join miteinander verknüpft werden sollen, können Sie den Join zwischen diesen Tabellen entfernen. Sie können z. B. einen Join entfernen, die die [Abfrage- und Sicht-Designer](../content/Query-and-View-Designer-Tools--Visual-Database-Tools-.md) automatisch zwischen zwei Tabellen erstellt wurde.  
  
> [!NOTE]  
> Durch das Entfernen eines Joins aus einer Abfrage wird die zugrunde liegende Beziehung in der Datenbank nicht geändert.  
  
Wenn zwei verknüpfte Tabellen Teil der Abfrage sind und Sie alle Joinbedingungen zwischen diesen entfernen, entsteht die resultierende Abfrage als Produkt aus beiden Tabellen, d. h. sie wird als CROSS JOIN bezeichnet.  
  
### So entfernen Sie einen Join  
  
-   In der [Diagrammbereich](../content/Diagram-Pane--Visual-Database-Tools-.md), wählen Sie die Joinlinie für den zu entfernenden Join, und drücken Sie dann die ENTF-Taste. Sie können mehrere Joinlinien gleichzeitig markieren und löschen.  
  
Der Abfrage- und Ansicht-Designer entfernt die Joinlinie und ändert die Anweisung in der [SQL-Bereich](../content/SQL-Pane--Visual-Database-Tools-.md).  
  
## Siehe auch  
[Automatisches Verknüpfen von Tabellen & #40; Visual Database Tools & #41;](../content/Join-Tables-Automatically--Visual-Database-Tools-.md)  
[Manuelles Verknüpfen von Tabellen & #40; Visual Database Tools & #41;](../content/Join-Tables-Manually--Visual-Database-Tools-.md)  
[Abfragen mit Joins & #40; Visual Database Tools & #41;](../content/Query-with-Joins--Visual-Database-Tools-.md)  
  
