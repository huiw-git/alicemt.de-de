---
title: "Kombinieren von Bedingungen, wenn AND Vorrang hat (Visual Database Tools)"
ms.custom: na
ms.date: 07/27/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - tools-ssms
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 450eb2eb-6ea3-405b-8dd2-1ff926c016e7
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
# Kombinieren von Bedingungen, wenn AND Vorrang hat (Visual Database Tools)
Kombinieren Sie Bedingungen mit und Hinzufügen der neuen Spalte zur Abfrage zweimal\-\-einmal für jede Bedingung. Kombinieren Sie Bedingungen mit, oder setzen Sie die erste Bedingung in der Spalte Filter und weiteren Bedingungen in einem **oder** Spalte.  
  
Angenommen, dass Sie entweder Mitarbeiter suchen, die mit dem Unternehmen mehr als fünf Jahren in der unteren waren möchten\-Aufträge oder Mitarbeiter mit der mittleren Ebene\-Aufträge unabhängig vom Einstellungsdatum Ebene. Diese Abfrage erfordert drei Bedingungen, von denen zwei mit AND verknüpft sind:  
  
-   Mitarbeiter, die vor weniger als fünf Jahren eingestellt wurden UND deren Tätigkeitsstufe 100 beträgt.  
  
    \-oder\-  
  
-   Mitarbeiter mit der Tätigkeitsstufe 200.  
  
### So kombinieren Sie Bedingungen, wenn AND Vorrang hat  
  
1.  In der [im Kriterienbereich](../content/Criteria-Pane--Visual-Database-Tools-.md), fügen Sie die Datenspalten, die Sie suchen möchten. Wenn Sie dieselbe Spalte nach zwei oder mehr mit AND verbundenen Bedingungen durchsuchen möchten, müssen Sie den Namen der Datenspalte für jeden zu suchenden Wert einmal in das Datenblatt einfügen.  
  
2.  In der **Filter** Spalte Geben Sie die Bedingungen aus, die Sie verknüpfen möchten und. Um beispielsweise Bedingungen mit AND zu verknüpfen, nach denen in den Spalten `hire_date` und `job_lvl` gesucht werden soll, geben Sie in die Filterspalte die Werte `< '1/1/91'` und `= 100` ein.  
  
    Diese Datenblatteinträge generieren die folgende WHERE-Klausel in der Anweisung in der [SQL-Bereich](../content/SQL-Pane--Visual-Database-Tools-.md):  
  
    ```  
    WHERE (hire_date < '01/01/91') AND  
      (job_lvl = 100)  
    ```  
  
3.  In der **oder** Spalte des Datenblatts, geben Sie für die Verbindung mit oder. Z. B. eine Bedingung hinzuzufügen, sucht nach einem anderen Wert in, der `job_lvl` Spalte Geben Sie einen zusätzlichen Wert in die **oder** Spalte, wie z. B. `= 200`.  
  
    Hinzufügen eines Werts in der **oder** Spalte der WHERE-Klausel in der Anweisung im SQL-Bereich eine weitere Bedingung hinzugefügt:  
  
    ```  
    WHERE (hire_date < '01/01/91' ) AND  
      (job_lvl = 100) OR   
      (job_lvl = 200)  
    ```  
  
## Siehe auch  
[Kombinieren von Bedingungen, wenn OR hat Vorrang vor &#40; Visual Database Tools &#41;](../content/Combine-Conditions-When-OR-Has-Precedence--Visual-Database-Tools-.md)  
[Konventionen für das Kombinieren von Suchbedingungen im Kriterienbereich &#40; Visual Database Tools &#41;](../content/Conventions-for-Combining-Search-Conditions-in-the-Criteria-Pane--Visual-Database-Tools-.md)  
[Regeln für das Eingeben von Suchwerten &#40; Visual Database Tools &#41;](../content/Rules-for-Entering-Search-Values--Visual-Database-Tools-.md)  
[Geben Sie Suchkriterien &#40. Visual Database Tools &#41;](../content/Specify-Search-Criteria--Visual-Database-Tools-.md)  
  
