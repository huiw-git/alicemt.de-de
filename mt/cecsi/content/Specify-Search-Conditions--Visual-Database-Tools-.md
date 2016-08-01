---
title: "Angeben von Suchbedingungen (Visual Database Tools)"
ms.custom: na
ms.date: 07/27/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - tools-ssms
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 18e2c759-68ec-4efe-b208-2f73418cd9bd
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
# Angeben von Suchbedingungen (Visual Database Tools)
Sie können die Datenzeilen festlegen, die in die Abfrage aufgenommen werden sollen, indem Sie Suchbedingungen angeben. Wenn Sie beispielsweise die Tabelle `employee` abfragen, können Sie angeben, dass Sie nur diejenigen Mitarbeiter suchen, die in einem bestimmten Gebiet arbeiten.  
  
Suchbedingungen werden mithilfe eines Ausdrucks angegeben. In der Regel besteht der Ausdruck aus einem Operator und einem Suchwert. Um beispielsweise Mitarbeiter in einem bestimmten Absatzgebiet zu suchen, können Sie für die Spalte `region` das folgende Suchkriterium angeben:  
  
```  
='UK'  
```  
  
> [!NOTE]  
> Wenn Sie mit mehreren Tabellen arbeiten, überprüft der Abfrage- und Sicht-Designer jede Bedingung daraufhin, ob der durchgeführte Vergleich zu einem Join führt. Wenn dies der Fall ist, konvertiert der Abfrage- und Sicht-Designer die Suchbedingung automatisch in einen Join. Weitere Informationen finden Sie unter [& #40; Tabellen automatisch verknüpfen Visual Database Tools & #41;](../content/Join-Tables-Automatically--Visual-Database-Tools-.md).  
  
### So geben Sie Suchbedingungen an  
  
1.  Fügen Sie im Kriterienbereich die Spalten oder Ausdrücke hinzu, die in der Suchbedingung verwendet werden sollen, falls dies nicht bereits geschehen ist.  
  
    Wenn Sie eine Select-Abfrage erstellen und die Suchspalten bzw. Suchausdrücke angezeigt in der Abfrageausgabe, deaktivieren möchten die **Ausgabe** Spalte für jede Suchspalte oder Ausdruck entfernen Sie diese als Ausgabespalten.  
  
2.  Suchen Sie die Zeile mit der Datenspalte oder den Ausdruck zu suchen und dann in der **Filter** Spalte Geben Sie eine Bedingung für die Suche.  
  
    > [!NOTE]  
    > Wenn einen Operator, der die Abfrage eingeben und Ansicht-Designer automatisch den Gleichheitsoperator fügt "\=".  
  
Der Abfrage- und Ansicht-Designer aktualisiert die SQL-Anweisung in der [SQL-Bereich](../content/SQL-Pane--Visual-Database-Tools-.md) durch Hinzufügen oder Ändern der WHERE-Klausel.  
  
## Siehe auch  
[Regeln für das Eingeben von Suchwerten & #40; Visual Database Tools & #41;](../content/Rules-for-Entering-Search-Values--Visual-Database-Tools-.md)  
[Geben Sie Suchkriterien & #40. Visual Database Tools & #41;](../content/Specify-Search-Criteria--Visual-Database-Tools-.md)  
  
